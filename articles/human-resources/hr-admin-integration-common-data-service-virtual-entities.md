---
title: Dataverse virtuālo tabulu konfigurēšana
description: Šajā rakstā ir parādīts, kā konfigurēt, ģenerēt, atjaunināt esošās virtuālās tabulas, kā arī analizēt ģenerētās un pieejamās tabulas Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45155dba5063981eb3aeeed4dda1d79a57b7c8af
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067104"
---
# <a name="configure-dataverse-virtual-tables"></a>Dataverse virtuālo tabulu konfigurēšana


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dynamics 365 Human Resources ir virtuālais datu avots platformā Microsoft Dataverse. Tas nodrošina pilnīgas izveides, lasīšanas, atjaunināšanas un dzēšanas (CRUD) operācijas no Dataverse un Microsoft Power Platform. Dati virtuālajām tabulām netiek saglabāti Dataverse, bet gan programmas datu bāzē.

Lai iespējotu CRUD operācijas personāla vadības elementos no Dataverse, jums jāpadara šos elementus pieejamus kā virtuālas tabulas Dataverse. Tas ļauj veikt CRUD operācijas no Dataverse un Microsoft Power Platform personāla vadības datos. Operācijas atbalsta arī pilnas biznesa loģikas personāla vadības pārbaudes, lai nodrošinātu datu integritāti, rakstot datus elementos.

> [!NOTE]
> Human Resources elementi atbilst Dataverse tabulām. Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Pieejamās virtuālās tabulas Human Resources

Visi atvērtie datu protokola (OData) elementi Human Resources ir pieejamas kā virtuālās tabulas Dataverse. Tie ir pieejami arī Power Platform. Tagad varat veidot lietojumprogrammas un pieredzi ar datiem tieši no personāla vadības ar pilnām CRUD iespējām, nekopējot vai nesinhronizējot datus ar Dataverse. Varat izmantot Power Apps portālus, lai veidotu tīmekļa vietnes ar ārējo piekļuvi, kas iespējo sadarbības scenārijus biznesa procesiem personāla vadībā.

Varat apskatīt vidē iespējoto virtuālo tabulu sarakstu un sākt darbu ar tabulām pakalpojumā [Power Apps](https://make.powerapps.com), **Dynamics 365 HR Virtual Tables** risinājumā.

![Dynamics 365 HR Virtual Tables pakalpojumā Power Apps.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuālās tabulas pret vietējām tabulām

Virtuālās Human Resources tabulas atšķiras no vietējām Dataverse tabulām, kas veidotas Human Resources vajadzībām. 

Vietējās tabulas Human Resources vajadzībām tiek veidotas atsevišķi un uzturētas kopējā HCM risinājumā Dataverse. Vietējo tabulu gadījumā dati tiek saglabāti Dataverse un tiem nepieciešama sinhronizācija ar Human Resources programmas datu bāzi.

> [!NOTE]
> Vietējo Dataverse tabulu Human Resources vajadzībām sarakstu skatiet [Dataverse tabulas](./hr-developer-entities.md).

## <a name="setup"></a>Iestatīt

Sekojiet šīm iestatīšanas darbībām, lai iespējotu virtuālās tabulas jūsu vidē.

### <a name="enable-virtual-tables-in-human-resources"></a>Iespējot virtuālās tabulas Human Resources

Vispirms **Funkciju pārvaldības** darbvietā ir jāiespējo virtuālas tabulas.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Atlasiet elementu **Funkciju pārvaldība**.

3. Atlasiet **Virtuālās tabulas atbalsts HR programmā Dataverse** un pēc tam atlasiet **Iespējot**.

Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu un atspējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Lietojumprogrammas reģistrēšana Microsoft Azure

Vispirms jūsu Personāla vadības instance ir jāreģistrē Azure portālā, lai Microsoft Identity platforma var nodrošināt autentifikāciju un autorizācijas pakalpojumus lietojumprogrammai un lietotājiem. Lai iegūtu vairāk informācijas par lietojumprogrammu reģistrāciju Azure, skatiet [Īsa pamācība: lietojumprogrammas reģistrēšana platformā Microsoft Identity](/azure/active-directory/develop/quickstart-register-app).

1. Atveriet [Microsoft Azure portālu](https://portal.azure.com).

2. Azure pakalpojumu sarakstā atlasiet **Lietojumprogrammu reģistrācijas**.

3. Atlasiet **Jauna reģistrācija**.

4. Laukā **Nosaukums** ievadiet aprakstošu lietojumprogrammas nosaukumu. Piemēram, **Dynamics 365 Human Resources virtuālās tabulas**.

5. **Novirzīšanas URI** laukā ievadiet savas personāla vadības instances nosaukumvietas URL.

6. Atlasiet **Reģistrēt**.

7. Kad reģistrācija pabeigta, Azure portālā tiek parādīta lietojumprogrammas reģistrācijas **pārskata** rūts, kurā ir ietverts tās **lietojumprogrammas (klienta) ID**. Pašlaik ņemiet vērā **lietojumprogrammas (klienta) ID**. Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālās tabulas datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Kreisajā navigācijas rūtī atlasiet **sertifikāti un noslēpumi**.

9. Lapas sadaļā **Klienta noslēpumi** atlasiet **Jauns klienta noslēpums**.

10. Ievadiet aprakstu, atlasiet ilgumu un atlasiet **Pievienot**.

11. Ierakstiet neslēpuma vērtību no tabulas rekvizīta **Vērtība**. Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālās tabulas datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Pārliecinieties, ka ņemat vērā pašreizējo noslēpuma vērtību. Pēc iziešanas no šīs lapas noslēpums nekad vairs netiek parādīts.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Dynamics 365 HR Virtual Tables programmas instalēšana

Instalējiet Dynamics 365 HR Virtual Tables programmu jūsu Power Apps vidē, lai izvietotu virtuālās tabulas risinājuma pakotni Dataverse.

1. Human Resources atveriet lapu **Microsoft Dataverse integrācija**.

2. Atlasiet cilni **Virtuālās tabulas**.

3. Atlasiet **Instalēt virtuālās tabulas programmu**.

### <a name="configure-the-virtual-table-data-source"></a>Virtuālās tabulas datu avota konfigurēšana

Nākamais solis ir konfigurēt virtuālās tabulas datu avotu Power Apps vidē.

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).

2. Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.

3. Atlasiet **Vides URL** lapas sadaļā **Detalizēti**.

4. **Risinājumu darbspējas centrmezglā** atlasiet ikonu **Detalizētā atrašana** lietojumprogrammas lapas augšējā labajā stūrī.

5. Lapā Detalizētā **atrašana** nolaižamajā sarakstā Meklēt **nolaižamo** sarakstu atlasiet Finanšu un operāciju **virtuālā datu avota konfigurācijas**.

   > [!NOTE]
   > Virtuālās tabulas programmas instalēšana no iepriekšējās iestatīšanas darbības var ilgt dažas minūtes. Ja **finanšu un operāciju virtuālā datu** avota konfigurācijas nav pieejamas sarakstā, uzgaidiet kādu minūti un atsvaidziniet sarakstu.

6. Atlasiet **Rezultāti**.

7. Atlasiet ierakstu **Microsoft HR datu avots**.

8. Ievadiet nepieciešamo informāciju par datu avota konfigurāciju:

   - **Mērķa URL**: jūsu personāla vadības nosaukumvietas URL. Mērķa URL formāts ir:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Piemēram:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Noteikti iekļaujiet rakstzīmi "**/**" vietrāža URL beigās, lai izvairītos no kļūdas saņemšanas.

     >[!NOTE]
     >Mērķa vietrādis URL nosaka personāla vadības vidi, uz kuru virtuālās tabulas norādīs datu iegūšanai. Ja izveidojat izmēģināšanas vidi, veidojot ražošanas vides kopiju, atjauniniet šo vērtību uz jaunās izmēģināšanas vides nosaukumu telpas URL. Tādējādi tiek nodrošināts, ka virtuālās tabulas ir saistītas ar izmēģināšanas vides datiem, nevis turpina norādīt uz ražošanas vidi.

   - **Nomnieka ID**: Azure Active Directory (Azure AD) nomnieka ID.

   - **AAD lietojumprogrammas ID**: lietojumprogrammas (klienta) ID, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai. Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD lietojumprogrammas noslēpums**: klienta noslēpums, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai. Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR datu avots.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Atlasiet **Saglabāt un aizvērt**.

### <a name="grant-app-permissions-in-human-resources"></a>Piešķiriet lietojumprogrammas atļaujas personāla vadībā

Piešķiriet atļaujas abām Azure AD lietojumprogrammām personāla vadībā:

- Lietojumprogramma, kas izveidota jūsu nomniekam Microsoft Azure portālā
- Dynamics 365 HR Virtual Table programma, kas instalēta Power Apps vidē 

1. Personāla vadībā atveriet **Azure Active Directory lietojumprogrammu** lapu.

2. Atlasiet **Jauns**, lai izveidotu jaunu lietojumprogrammas ierakstu:

    - Laukā **Klienta ID**, ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas klienta ID.
    - Laukā **Nosaukums** ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas nosaukumu.
    - Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.

3. Atlasiet **Jauns**, lai izveidotu otru lietojumprogrammas ierakstu:

    - **Klienta Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Nosaukums**: Dynamics 365 HR Virtual Table
    - Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.

## <a name="generate-virtual-tables"></a>Virtuālo tabulu ģenerēšana

Kad iestatīšana ir pabeigta, varat atlasīt virtuālās tabulas, kuras vēlaties ģenerēt un iespējot savā Dataverse instancē.

1. Human Resources atveriet lapu **Microsoft Dataverse integrācija**.

2. Atlasiet cilni **Virtuālās tabulas**.

> [!NOTE]
> Kad visa nepieciešamā uzstādīšana būs pabeigta, slēdzis **Iespējot virtuālo tabulu** automātiski tiks iestatīts uz **Jā**. Ja slēdzis tiek iestatīts uz **Nē**, pārskatiet šā dokumenta iepriekšējās sadaļās norādītās darbības, lai nodrošinātu, ka visi priekšnosacījumu iestatīšana ir pabeigta.

3. Atlasiet tabulu vai tabulas, kuras vēlaties ģenerēt pakalpojumā Dataverse.

4. Atlasiet **Ģenerēt/atsvaidzināt**.

![Dataverse integrācija.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Tabulas ģenerēšanas statusa pārbaude

Virtuālās tabulas pakalpojumā Dataverse tiek ģenerētas, izmantojot asinhronu fona procesu. Procesa atjauninājumi tiek parādīti darbību centrā. Detalizēta informācija par procesu, ieskaitot kļūdu žurnālus, tiek parādīta lapā **Procesa automatizācija**.

1. Programmā Human Resources atveriet lapu **Procesa automatizācija**.

2. Atlasiet cilni **Fona procesi**.

3. Atlasiet **Virtuālo tabulu kopuma asinhronās darbības fona process**.

4. Atlasiet **Skatīt pēdējos rezultātus**.

Nolaižamā saraksta rūtī tiek rādīti pēdējie procesa izpildes rezultāti. Varat skatīt procesa žurnālu, tostarp visas kļūdas, kas atgrieztas no pakalpojuma Dataverse.

## <a name="see-also"></a>Skatiet arī

[Kas ir Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabulas Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Tabulas attiecību pārskats](/powerapps/maker/common-data-service/relationships-overview)<br>
[Izveidot un rediģēt virtuālās tabulas, kas satur datus no ārējo datu avota](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Kas ir Power Apps portāli?](/powerapps/maker/portals/overview)<br>
[Lietojumprogrammu izveides pārskats Power Apps](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

