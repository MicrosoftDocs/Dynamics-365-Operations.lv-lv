---
title: Dataverse virtuālās tabulas vaicājumu optimizācija
description: Optimizēt Dataverse virtuālās tabulas vaicājumu veiktspēju un novērst ar to saistītas problēmas
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1857d2e35e369bcd0c8f02a059a307f31da8b3b9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067458"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Dataverse virtuālās tabulas vaicājumu optimizācija


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Izsniegt

### <a name="overview"></a>Pārskats

Izmantojot Dataverse virtuālās tabulas, lai izstrādātu integrācijas un citus datu savienojumus ar Dynamics 365 Human Resources, var rasties veiktspējas problēmas ar virtuālo tabulu vaicājumiem. Lēna vaicājuma izpilde var notikt dažādos klientos vai interfeisos. Piemēram, var rasties problēma šādos apstākļos:

- Veicot vaicājumu virtuālajā tabulā, izmantojot Dataverse Web API
- Veidojot Power App pret virtuālo tabulu
- Veidojot Power BI pārskatu par virtuālo tabulu

Visiem šiem interfeisiem ir potenciāls radīt veiktspējas problēmu.

Viens no iemesliem lēnai darbībai ar Dataverse virtuālām tabulam pakalpojumam Human Resources ir ārējās atslēgas kolonnas virtuālajā tabulā, kas saistīta ar tabulas [navigācijas rekvizītiem](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties). Kad navigācijas rekvizīti ir izveidoti virtuālai tabulai, ārējās atslēgas kolonna tiek automātiski pievienota tabulai, lai attēlotu atslēgas vērtību saistītās virtuālās tabulas atslēgas kolonnai. Piemēram, kolonna **_mshr_fk_person_id_value** ir pievienota elementam **mshr_hcmworkerbaseentity** ar ārējās atslēgas rekvizītu no elementa **mshr_dirpersonentity**. Tā kā šo ārējo atslēgu kolonnu vērtības tiek uzturētas tabulā, vērtību iegūšana var negatīvi ietekmēt vaicājuma veiktspēju virtuālajā tabulā.

### <a name="potential-symptoms"></a>Iespējamie simptomi

Piemērs, kur, iespējams, redzat šo ietekmi, ir vaicājumos pret nodarbināto (**mshr_hcmworkerentity**) vai pamata nodarbināto (**mshr_hcmworkerbaseentity**) elementu. Jūs varat redzēt veiktspējas problēmas paradīsies dažos dažādos veidos:

- **Palēnināta vaicājuma izpilde**: vaicājums attiecībā uz virtuālo tabulu var atgriezt paredzamos rezultātus, bet tas var aizņemt vairāk laika, nekā paredzēts vaicājuma izpildes pabeigšanai.
- **Vaicājuma taimauts** : vaicājumam var beigties noildze un parādīties šāda kļūda: "Tika iegūts marķieris, lai izsauktu Finance and Operations, bet Finance and Operations atgrieza kļūdu, kuras veids ir InternalServerError."
- **Neparedzēta kļūda**: vaicājums var atgriezt 400 veida kļūdas ar šādu ziņojumu: "Radusies negaidīta kļūda."

  ![Kļūdas veids 400 uz HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Ierobežošana**: vaicājums var pārmērīgi izmantot servera resursus un tikt pakļauts ierobežošanai. Šajā gadījumā vaicājums atgriež šādu kļūdu: "Tika iegūts marķieris, lai izsauktu Finance and Operations, bet Finance and Operations atgrieza 429. tipa kļūdu." Papildinformāciju par ierobežošanu pakalpojumā Human Resources skatiet sadaļā [Bieži uzdotie jautājumi par ierobežošanu](./hr-admin-integration-throttling-faq.md).

  ![Kļūdas veids 429 uz HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Novēršana

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Ierobežot datu vaicājumā iekļauto kolonnu skaitu

Izmantojot virtuālās tabulas, viena no metodēm ar vislielāko potenciālu uzlabot vaicājuma veiktspēju ir ierobežot vaicājumā atlasīto kolonnu skaitu. Vispārīgie norādījumi vaicājuma veiktspējas optimizēšanai ir ierobežot vaicājumā atgrieztās kolonnas līdz tikai nepieciešamajiem rekvizītiem. Īpaši tas attiecas uz ārējo atslēgu kolonnām virtuālajās tabulās. Ja jūsu integrācijai vai pārskatam nav nepieciešamas vērtības ārējās atslēgas kolonnās, tad strukturējiet vaicājumu, lai atlasītu tikai tās kolonnas, kuras nepieciešamas, izņemot ārējās atslēgas kolonnas.

#### <a name="selecting-columns-in-an-odata-query"></a>Kolonnu atlase OData vaicājumā

Veicot vaicājumu virtuālajā tabulā, izmantojot Dataverse Web API, var ierobežot vaicājumā iekļauto kolonnu skaitu, izmantojot **$atlasīt** sistēmas vaicājuma opciju un definēt kolonnas, kurām jāatgriež rezultāti. Lai maksimizētu veiktspēju, no vaicājuma izslēdziet ārējās atslēgas (ar **_mshr_FK_** prefiksu).

Piemēram, nākamajā vaicājumā attiecībā pret elementu **mshr_hcmworkerbaseentity** tiks iekļautas tikai kolonnas, kas iekļautas vaicājuma opciju klauzulā **$atlasīt**, izņemot ārējās atslēgas vērtības. Tas nodrošina nozīmīgus veiktspējas uzlabojumus vaicājumā, kas ietver visas tabulas kolonnas.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Ieteikums ierobežot atlasīto kolonnu skaitu tiek lietots arī tad, ja izmantojat vaicājuma opciju **$paplašināt**, lai izvērstu vaicājumu uz saistītajām virtuālajām tabulām, izmantojot navigācijas rekvizītus. Piemēram, šajā vaicājumā ir iekļautas kolonnas no elementa **mshr_hcmworkerbaseentity** ar paplašinātām kolonnām no elementa **mshr_dirpersonentity**. Ievērojiet, ka vaicājuma opcija **$atlasīt** ir iekļauta arī vaicājuma opcijas klauzulā **$paplašināt**.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Izmantojot šo datu izgūšanas metodi ar vaicājuma opciju **$atlasīt** vaicājuma opciju klauzulā **$paplašināt**, parasti jūs redzēsiet lielākus veiktspējas uzlabojumus, ja navigācijas rekvizīts starp elementiem ir relācija daudzi pret vienu. Izvēršot relāciju “viens pret daudziem”, iespējams, neredzēsit tādu pašu vaicājuma izpildes laika samazinājumu. Plašāku informāciju par Dataverse virtuālo tabulu attiecību definīciju skatiet [Tabulu attiecībās](/powerapps/maker/data-platform/create-edit-entity-relationships).

Papildinformāciju par sistēmas vaicājuma opciju **$atlasīt** un **$paplašināt** izmantošanu Dataverse Web API skatiet sadaļā [Saistīto elementu ierakstu izgūšana ar vaicājumu](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Kolonnu atlase pakalpojumā Power BI

Ja, veidojot Power BI pārskatu Dataverse virtuālai tabulai, rodas kāda no iepriekšminētajām pazīmēm par lēnu veiktspēju, veiktspēju var uzlabot, izslēdzot ārējās atslēgas kolonnas no kolonnām, kas atlasītas atskaites tabulā. Piemēram, ja lietojat Power BI Desktop, lai izveidotu pārskatu pret elementu **mshr_hcmworkerbaseentity**, var veikt šādas darbības, lai atlasītu kolonnas, kuras vēlaties iekļaut atskaites vaicājumā.

1. Pakalpojumā Power BI Desktop atlasiet **Vairāk...** nolaižamajā sarakstā **Iegūt datus** darbību lentē.
2. Logā **Iegūt datus** ievadiet **Common Data Service** meklēšanas lodziņā, atlasiet savienotāju **Common Data Service** un atlasiet **Savienot**.
3. Laukā **Servera Url**, logā Common Data Service ievadiet uzņēmuma URI jūsu Dataverse videi un atlasiet **Labi**.
  
   ![Ievadiet URI jūsu Dataverse videi.](./media/PowerBIDataverseURLSetup.png)
  
4. Logā Navigators izvērsiet zaru **Elementi**.
5. Meklēšanas lodziņā ievadiet **mshr_hcmworkerbaseentity** un atlasiet elementu.
6. Atlasiet **Datu transformācija**.
7. Iekš Power Query Redaktora logs, atlasiet **Uzlabots redaktors**.
8. Logā **Paplašinātais redaktors** atjauniniet vaicājumu, lai tas izskatītos līdzīgi kā turpmāk, pēc nepieciešamības pievienojot vai noņemot kolonnas masīvam.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Atjauniniet vaicājumu uzlabotajā redaktorā Power Query Redaktors.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Atlasiet **Gatavs**.

   > [!NOTE]
   > Ja pirms atjaunināšanas jūs iepriekš saņēmāt no vaicājuma 429 vaida kļūdu, var būt nepieciešams gaidīt atkārtoto mēģinājumu periodu pirms vaicājuma atsvaidzināšanas, lai veiksmīgi to pabeigtu.

10. Klikšķis **Aizvērt un lietot** uz Power Query Redaktora darbības lente.

Pēc tam Power BI pārskatu ir iespējams izveidot pret kolonnām, kas atlasītas no virtuālās tabulas.

#### <a name="selecting-columns-in-power-apps"></a>Kolonnu atlase pakalpojumā Power Apps

Līdzīgi kā Dataverse Web API vaicājumiem un Power BI varat uzlabot Power Apps vaicājumu veiktspēju, pamatojoties uz Dataverse virtuālajām tabulām, izslēdzot saistīto tabulu kolonnas no programmas. Ja kāda kolonna no saistītās tabulas ir ietverta lapā, tad pieprasījuma URL, kas veidots, lai iegūtu datus, iekļaus saistītās tabulas ārējās atslēgas rekvizītus. Tas, tāpat kā augstāk minētie piemēri par [Kolonnu atlasīšanu OData vaicājumā](#selecting-columns-in-power-apps), samazina veiktspēju, radot papildu datu meklēšanas.

Lai to paveiktu, varat pārbaudīt, vai Power App datu veidlapā nav iekļauti datu lauki no saistītām tabulām.

1. Koka skata rūtī atlasiet datu veidlapu ekrānam.
2. Rūtī **Rekvizīti** atlasiet **Rediģēt** rekvizītā **Lauki**.
3. Rūtī **Dati** pārbaudiet, vai neviens no atlasītajiem laukiem nav datu avota virtuālās tabulas lauks.

Piemēram, ja vienam no datu laukiem, kas ietverti programmas lapā, ir atsauce uz citu tabulu, piemēram, **ThisItem.Worker.Name**, kur **Nodarbinātais** ir saistītā tabula, datu ienesē var samazināt veiktspēju.

Varat izmantot [Power Apps monitoru](/powerapps/maker/monitor-overview), lai nodrošinātu, ka tikai jums nepieciešamas kolonnas tiek iekļautas vaicājumā, lai iegūtu datus par programmu Power App. Varat skatīt URL, kas veidots getRows operācijai, lai nodrošinātu, ka jūsu programmai atlasītās kolonnas būs optimālas datu izgūšanai.

![Izmantojiet Power Apps monitoru, lai analizētu getData operāciju.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Datu vaicājuma filtrēšana

Cita metode vaicājuma izpildes veiktspējas uzlabošanai ir ierobežot vaicājuma rezultātos atgriezto ierakstu skaitu. To var izdarīt, filtrējot rezultātus, lai pārliecinātos, ka saņemat tikai tos ierakstus, kurus nepieciešams.

Lai iegūtu papildu informāciju par vaicājuma datu filtrēšanu, skatiet [Filtra rezultāti](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).

### <a name="limiting-the-page-size-of-the-query"></a>Vaicājuma lapas izmēra ierobežošana

Ja strādājat ar lielām datu kopām, vaicājuma rezultātus var sadalīt vairākās lapās, datu vaicājumiem pievienojot `odata.maxpagesize` preferenču virsrakstu.

Papildinformāciju par lapošanu skatiet sadaļā [Norādīt elementu skaitu, kas jāatgriež lapā](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Skatiet arī

- [Pakalpojuma Dataverse virtuālo tabulu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md)
- [Bieži uzdotie jautājumi par Human Resources tabulām](hr-admin-virtual-entity-faq.md)
- [Bieži uzdotie jautājumi par ierobežošanu](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
