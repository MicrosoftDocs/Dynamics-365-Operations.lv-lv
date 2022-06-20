---
title: Elektronisko pārskatu formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu
description: Šajā rakstā skaidrots, kā var konfigurēt elektronisko pārskatu (ER) formātus, lai lietotu parametrus, kas norādīti katrai juridiskajai personai.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eb44422c4cdcc87989cdfb28dcd7d5cfea9002eb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858833"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>ER formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

Daudzos no elektronisko pārskatu (ER) formātiem, kurus izstrādāsit, ir jāfiltrē dati, izmantojot vērtību kopu, kas ir specifiska katrai jūsu instances juridiskajai personai (piemēram, nodokļu kodu kopa nodokļu darbību filtrēšanai). Pašlaik, kad šī veida filtrēšana ir konfigurēta ER formātā, vērtības, kas ir atkarīgas no juridiskās personas (piemēram, nodokļu kodi), tiek izmantotas ER formāta izteiksmē, lai norādītu datu filtrēšanas nosacījumus. Tāpēc ER formāts ir padarīts juridiskai personai specifisks, un lai ģenerētu pieprasītos pārskatus, jums ir jāizveido iegūtas kopijas no sākotnējā ER formāta katrai juridiskajai personai, kurai jums ir jāpalaiž ER formāts. Katrs atvasinātais ER formāts ir jārediģē, lai tajā ieviestu juridiskajai personai specifiskās vērtības, pārbaudot, kad sākotnējā (bāzes) versija ir atjaunināta, eksportēta no testa vides un importēta ražošanas vidē, kad tā ir jāizvieto izmantošanai ražošanā un tā tālāk. Tāpēc šāda veida konfigurētā ER risinājuma uzturēšana ir sarežģīta un laikietilpīga vairāku iemeslu dēļ:

-   Jo vairāk ir juridisko personu, jo ir jāsaglabā vairāk ER formāta konfigurācijas.
-   ER konfigurāciju uzturēšana prasa, lai uzņēmuma lietotājiem būtu ER zināšanas.

ER programmai raksturīgo parametru līdzeklis ļauj pilnvarot lietotājus konfigurēt datu filtrēšanu ER formātā, lai tā būtu balstīta uz abstraktu noteikumu kopu. Šo noteikumu kopu var konfigurēt, lai izmantotu informācijas avotus, kas ir pieejami ER formātā. Pēc tam uzņēmuma lietotāji var noteikt reālos noteikumus ārpus ER struktūras, izmantojot lietotāja interfeisu (UI), kas tiek ģenerēts automātiski, pamatojoties uz atbilstošā ER formāta iestatījumiem un pašreizējo juridisko personu datiem, kuriem varēs piekļūt ER formāta datu avoti. Kārtulu kopu, kas norādīta ER formātam, var eksportēt no pašreizējās Dynamics 365 Finanšu (finanšu) instances juridiskās personas. Pēc tam to var importēt citā juridiskajā personā ar to pašu finanšu instanci vai citu instanci kā noteikumu kopumu vienam un tam pašam ER formātam.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai šajā rakstā pabeigtu piemērus, ir nepieciešama piekļuve regulēšanas konfigurācijas pakalpojumu (RCS) instancei, kas ir nodrošināta tam pašam nomniekam kā Finanses vienai no šīm lomām:

- Elektroniskā pārskata izstrādātājs
- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Ir ieteicams veikt darbības, kas jāveic atbalstītajā [ER datu avotu, kas satur aprēķinātā lauka tipa rakstu, atbalstīt parametru izsaukumus](er-calculated-field-type.md). Ja esat jau paveikuši šīs darbības, varat izlaist darbības, kas norādītas nākamajā sadaļā **ER konfigurāciju importēšana RCS**.

## <a name="import-er-configurations-into-rcs"></a>ER konfigurāciju importēšana RCS

Lejupielādējiet un lokāli saglabājiet šādas ER konfigurācijas.

| **Satura apraksts**                        | **Faila nosaukums**                                        |
|------------------------------------------------|------------------------------------------------------|
| Parauga **ER datu modeļa** konfigurācijas fails    | [Modelis, lai uzzinātu parametru izsaukumus.versija.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| Parauga **ER metadatu** konfigurācijas fails      | [Metadati, lai uzzinātu parametru izsaukumus.versija.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| Parauga **ER modeļa kartējuma** konfigurācijas fails | [Kartēšana, lai uzzinātu parametru izsaukumus.versija.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| Parauga **ER formāta** konfigurācija             | [Formāts, lai uzzinātu parametru izsaukumus.versija.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Pēc tam pierakstieties savā RCS instancē.

Šajā piemērā izveidosiet konfigurāciju Litware, Inc. parauga uzņēmumam. Pirms šīs procedūras veikšanas ir jāveic darbības, [kas soļi sadaļā Konfigurācijas nodrošinātāja izveidošana un jāatzīmē tas](tasks/er-configuration-provider-mark-it-active-2016-11.md) kā aktīvs raksts RCS.

1.  Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.
2.  Atlasiet **Pārskatu konfigurācijas**.
3.  Importējiet ER konfigurācijas, ko iepriekš esat lejupielādējis RCS, šādā secībā: datu modelis, metadati, modeļa kartēšana un formāts. Katrai ER konfigurācijai rīkojieties šādi.

    1.  Atlasiet **Maiņa**.
    2.  Atlasiet **Ielādēt no XML faila**.
    3.  Atlasiet **Pārlūkot**, lai atlasītu failu nepieciešamajai ER konfigurācijai XML formātā.
    4.  Atlasiet **Labi**.

## <a name="review-the-er-solution-that-is-provided"></a>Pārskatiet sniegto ER risinājumu.

1.  Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.
2.  Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus**.
3.  Atlasiet **Noformētājs**.
4.  Atlasiet **Izvērst/Sakļaut**.

    ER formāts **Formāts, lai uzzinātu parametru izsaukumus** ir izveidots, lai ģenerētu nodokļu deklarāciju XML formātā, kas parāda vairākus nodokļu līmeņus (regulārs, samazināts un nav). Katram līmenim ir atšķirīgs detaļu skaits.

    ![Vairāki ER formāta līmeņi, Formatēt, lai apgūtu parametru izsaukumus.](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Cilnē **Kartēšana** izvērsiet vienumus **Modelis**, **Dati** un **Kopsavilkums**.

    Datu avots **Modelis.Dati.Kopsavilkums** atgriež nodokļu transakciju sarakstu. Šīs transakcijas ir apkopotas pēc PVN koda. Šim datu avotam **Modelis.Dati.Kopsavilkums.Līmenis** aprēķinātais lauks ir konfigurēts tā, lai atgrieztu katra apkopotā ieraksta taksācijas līmeņa kodu. Jebkuram nodokļu kodam, kuru izpildlaikā var izgūt no datu avota **Modelis.Dati.Kopsavilkums**, aprēķinātais lauks atgriež nodokļu līmeņa kodu (**Parasts**, **Samazināts**, **Nav** vai **Cits**) kā teksta vērtību. Aprēķinātais lauks **Modelis.Dati.Kopsavilkums.Līmenis** tiek izmantots, lai filtrētu datu avota **Modelis.Dati.Kopsavilkums** ierakstus un ievadītu filtrētos datus katrā XML elementā, kas apzīmē nodokļu līmeni, izmantojot laukus **Modelis.Dati2.Līmenis1**, **Modelis.Dati2.Līmenis2** un **Modelis.Dati2.Līmenis3**.

    ![Modelis.Dati.Kopsavilkums nodokļu transakciju datu avota saraksts.](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Aprēķinātais lauks **Modelis.Dati.Kopsavilkums.Līmenis** ir konfigurēts tā, lai tas ietvertu ER izteiksmi. Nodokļu kodi (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** un **InVAT0**) šajā konfigurācijā ir stingri kodēti. Tāpēc šis ER formāts ir atkarīgs no juridiskās personas, kur šie nodokļu kodi tika konfigurēti.

    ![Modelis.Dati.Kopsavilkums.Līmenis aprēķinātais lauks ar cietiem nodokļu kodiem.](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Lai atbalstītu atšķirīgu nodokļu kodu kopu katrai juridiskajai personai, ir jāveic tālāk norādītās darbības.

    - Izveidojiet atvasinātu ER formāta versiju katrai juridiskajai personai.
    - Atjauniniet nodokļu kodus aprēķinātajā laukā **Modelis.Dati.Kopsavilkums.Līmenis**, pamatojoties uz juridiskās personas iestatījumu.

6.  Aizveriet lapu **Formāta veidotājs**.

## <a name="create-a-derived-format"></a>Atvasināta formāta izveide

Pēc tam jūs izmantosit ER programmai raksturīgo parametru līdzekli, lai atbalstītu citu nodokļu kodu kopu katrai juridiskajai personai vienotā ER formātā.

1.  Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.
2.  Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus**.
3.  Atlasiet **Izveidot konfigurāciju**.
4.  Atlasiet opciju **Atvasināt no nosaukuma: formatēt, lai uzzinātu parametru izsaukumus, Microsoft**.
5.  Laukā **Nosaukums** ievadiet **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.
6.  Atlasiet **Izveidot konfigurāciju**.

## <a name="configure-a-derived-format"></a>Konfigurējiet atvasināto formātu

### <a name="add-a-format-enumeration"></a>Pievienojiet formātu uzskaitījumu

Pēc tam jūs pievienosit jaunu ER formātu uzskaitījumu. Šī formāta uzskaitījuma vērtības tiks rādītas uzņēmuma lietotājiem, kuri norādīs no juridiskās personas atkarīgās nodokļu kodu kopas dažādiem nodokļu līmeņiem, kas tiek izmantoti ER formātā.

1.  Atlasiet **Noformētājs**.
2.  Atlasiet **Formātu uzskaitījumi**.
3.  Atlasiet **Pievienot**.
4.  Laukā **Nosaukums** ievadiet **Nodokļu līmeņu saraksts**.
5.  Atlasiet **Saglabāt**.
6.  Cilnē **Formātu uzskaitījuma vērtības** atlasiet **Pievienot**.
7.  Laukā **Nosaukums** ievadiet **Parasta nodokļu piemērošana**.
8.  Vēlreiz atlasiet **Pievienot**.
9.  Laukā **Nosaukums** ievadiet **Samazināta nodokļu piemērošana**.
10. Vēlreiz atlasiet **Pievienot**.
11. Laukā **Nosaukums** ievadiet **Nav nodokļa**.
12. Vēlreiz atlasiet **Pievienot**.
13. Laikā **Nosaukums** ievadiet **Cits**.

    ![Jauns ieraksts Formāta uzskaitījumu lapā.](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Tā kā uzņēmuma lietotāji var izmantot dažādas valodas, lai norādītu no juridiskās personas atkarīgās nodokļu kodu kopas, mēs iesakām pārtulkot šīs uzskaitījuma vērtības valodās, kas ir konfigurētas kā vēlamās valodas šiem lietotājiem programmā Finance.

14. Atlasiet ierakstu **Nav nodokļa**.
15. Noklikšķiniet laukā **Etiķete**.
16. Atlasiet **Tulkot**.
17. Rūts **Teksta tulkošana** laukā **Etiķetes ID** ievadiet **LBL_LEVELENUM_NO**.
18. Laukā **Teksts noklusējuma valodā** ievadiet **Nav nodokļa**.
19. Laukā **Valoda** atlasiet **DE**.
20. Laukā **Tulkotais teksts** ievadiet **keine Besteuerung**.
21. Atlasiet **Tulkot**.

    ![Teksta tulkojuma slaids.](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Atlasiet **Saglabāt**.
23. Aizveriet lapu **Formātu uzskaitījumi**.

### <a name="add-a-new-lookup-data-source"></a>Pievienot jaunu uzmeklēšanas datu avotu

Pēc tam jūs pievienosit jaunu datu avotu, lai norādītu, kā uzņēmuma lietotāji norādīs no juridiskās personas atkarīgos noteikumus, lai atpazītu pareizo nodokļu līmeni katram kopsavilkuma transakcijas ierakstam.

1.  Cilnē **Kartēšana** atlasiet **Pievienot**.
2.  Atlasiet **Formātu uzskaitījumi\Uzmeklēšana**.

    Jūs nupat identificējāt, ka katram noteikumam, ko uzņēmuma lietotāji nosaka nodokļu līmeņa atpazīšanai, tiks atgriezta ER formāta uzskaitījuma vērtība. Ievērojiet, ka datu avota veidam **Uzmeklēšana** var piekļūt zem bloka **Datu modelis** un **Dynamics 365 for Operations** papildus blokam **Formāta uzskaitījums**. Tādēļ ER datu modeļa uzskaitījumus un pieteikumu uzskaitījumus var izmantot, lai norādītu vērtību veidu, kas tiek atgriezts šā veida datu avotiem. Papildinformāciju par **Uzmeklēšanas** datu avotiem skatiet sadaļā [Uzmeklēšanas datu avotu konfigurēšana, lai lietotu ER programmai raksturīgo parametru līdzekli](er-lookup-data-sources.md).
    
3.  Laukā **Nosaukums** ievadiet **Atlasītājs**.
4.  Laukā **Formātu uzskaitījums** atlasiet **Nodokļu līmeņu saraksts**.

    Jūs norādījāt, ka katram šajā datu avotā norādītajam nosacījumam uzņēmuma lietotājam jāatlasa viena no **Nodokļu līmeņu saraksta** formāta uzskaitījuma vērtībām kā atgrieztā vērtība.
    
5.  Atlasiet **Rediģēt uzmeklēšanu**.
6.  Atlasiet **Kolonnas**.
7.  Izvērst **Modelis** vienumu.
8.  Izvērsiet vienumu **Dati**.
9.  Izvērsiet vienumu **Nodoklis**.
10. Atlasiet vienumu **Modelis.Dati.Nodoklis.Kods**.
11. Atlasiet pogu **Pievienot** (labā bultiņa).

    ![Kolonnu slaids.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Jūs tikko norādījāt, ka katram šajā datu avotā norādītajam noteikumam nodokļa līmeņa atpazīšanai uzņēmuma lietotājam jāatlasa viens no nodokļa kodiem kā nosacījums. To nodokļu kodu sarakstu, kurus var atlasīt uzņēmuma lietotājs, atgriezīs datu avots **Modelis.Dati.Nodoklis**. Tā kā šis datu avots ietver lauku **Nosaukums**, nodokļu koda nosaukums tiks parādīts katrai uzņēmuma lietotājam iesniegtajai nodokļa koda vērtībai.
    
12. Atlasiet **Labi**.

    ![Uzmeklēšanas veidotāja lapa.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Uzņēmuma lietotāji var pievienot vairākas kārtulas kā šī datu avota ierakstus. Katrs ieraksts tiks numurēts, izmantojot rindas kodu. Kārtulas tiks novērtētas, lai palielinātu rindu skaitu.

    Tā kā jūs atlasījāt lauku **Nodokļa kods** kā nosacījumu šī uzmeklēšanas datu avota kārtulām, un tāpēc, ka **Nodokļa kods** ir iestatīts kā lauka **Virkne** datu veids, katra kārtula tiks novērtēta izpildlaikā, salīdzinot nodokļa kodu, kas tiek nodots datu avotam, ar nodokļu kodu, kas definēts šajā datu avota ierakstā.

    Kad tiek atrasta kārtula, kas atbilst konfigurētajam nosacījumam, šis datu avots atgriež kārtulas uzmeklēšanas vērtību, kas definēta laukā **Uzmeklēšanas rezultāts**. Ja kārtula netiek atrasta, tiek izmests izņēmums, lai paziņotu lietotājam, ka pašreizējais datu avots nevar atgriezt pareizu vērtību.

13. Atlasiet **Saglabāt**.
14. Aizveriet lapu **Uzmeklēšanas veidotājs**.
15. Atlasiet **Labi**.

    Ņemiet vērā, ka jūs pievienojāt jaunu datu avotu, kas atgriezīs nodokļu līmeni kā formāta uzskaitījuma **Nodokļu līmeņu saraksts** vērtību jebkuram nodokļu kodam, kas tiek nodots datu avotam kā datu veida **Virkne** parametra **Kods** arguments.
    
    ![Formāta veidotāja lapa ar jaunu datu avotu.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Konfigurēto kārtulu novērtējums ir atkarīgs no to lauku datu veida, kas atlasīti, lai definētu šo kārtulu nosacījumus. Kad tiek atlasīts lauks, kas ir konfigurēts kā datu veida **Skaitlisks** vai **Datums** lauks, kritēriji atšķirsies no tiem kritērijiem, kas iepriekš tika aprakstīti datu veidam **Virkne**. Laukiem **Skaitlisks** un **Datums** kārtulai jābūt norādītai kā vērtību diapazonam. Pēc tam kārtulas nosacījums tiks uzskatīts par izpildītu, ja datu avotam nodotā vērtība būs konfigurētajā diapazonā.
    
    Nākamajā attēlā ir parādīts šāda iestatījuma veida piemērs. Papildus datu veida **Virkne** laukam **Modelis.Dati.Nodoklis.Kods** datu veida **Faktisks** lauks **Modelis.Nodoklis.Kopsavilkums.Bāze** tiek izmantots, lai norādītu nosacījumus datu avota uzmeklēšanai.
    
    ![Uzmeklēšanas veidotāja lapa ar papildu kolonnām.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Tā kā šim uzmeklēšanas datu avotam ir atlasīti lauki **Modelis.Dati.Nodoklis.Kods** un **Modelis.Nodoklis.Kopsavilkums.Bāze** katra šī datu avota kārtula tiks konfigurēta tālāk norādītajā veidā.
    
    -   Piedāvātajā sarakstā formāta uzskaitījuma **Nodokļu līmeņu saraksts** vērtība ir jāatlasa kā atgrieztā vērtība.
    -   Nodokļa kods jāievada kā šīs kārtulas nosacījums. Piemērojami ir tikai tie nodokļu kodi, kurus sniedzis datu avots **Modelis.Dati.Nodoklis**.
    -   Minimālās un maksimālās nodokļu bāzes summas vērtības ir jāievada kā šīs kārtulas nosacījumi.

    Lūk, kā katra šī datu avota kārtula tiks novērtēta izpildlaikā:
    -   Vai datu veida **Virkne** kods, kas tika nodots šim datu avotam, ir vienāds ar kārtulas nodokļu kodu?
    -   Vai datu veida **Faktiskais** vērtība, kas tika nodota šim datu avotam, atbilst noteiktajām minimālajām un maksimālajām vērtībām?

    Kārtula tiks uzskatīta par piemērojamu, ja abi nosacījumi būs izpildīti.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Tulkot pievienotā uzmeklēšanas datu avota etiķeti

Tā kā uzņēmuma lietotāji var izmantot dažādas valodas, lai norādītu no juridiskās personas atkarīgās nodokļu kodu kopas, mēs iesakām pārtulkot etiķeti katram uzmeklēšanas datu avotam, ko esat pievienojis, lai atbilstošajā lapā tā tiktu parādīta katra lietotāja vēlamajā valodā.

1.  Atlasiet datu avotu **Modelis.Dati.Atlasītājs**.
2.  Atlasiet **Rediģēt**.
3.  Noklikšķiniet laukā **Etiķete**.
4.  Atlasiet **Tulkot**.
5.  Rūts **Teksta tulkošana** laukā **Etiķetes ID** ievadiet **LBL_SELECTOR_DS**.
6.  Laukā **Teksts noklusētajā valodā** ievadiet **Atlasīt nodokļa līmeni pēc nodokļu koda**.
7.  Laukā **Valoda** atlasiet **DE**.
8.  Laukā **Tulkotais teksts** ievadiet **Steuerebene für Steuerkennzeichen auswählen**.
9.  Atlasiet **Tulkot**.
10. Atlasiet **Labi**.

    ![Datu avota rekvizītu slaids.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Pievienojiet jaunu lauku, lai izmantotu konfigurēto uzmeklēšanu

1.  Izvērsiet vienumu **Modelis.Dati**.
2.  Atlasiet vienumu **Modelis.Dati.Kopsavilkums**.
3.  Atlasiet **Pievienot**.
4.  Atlasiet **Funkcijas/Aprēķinātais lauks**.
5.  Laukā **Nosaukums** ievadiet **LevelByLookup**.
6.  Atlasiet **Rediģēt formulu**.
7.  Laukā **Formulas lauks** ievadiet **Modelis.Atlasītājs(Modelis.Dati.Kopsavilkums.Kods)**.
8.  Atlasiet **Saglabāt**.

    ![Pievieno Modelis.Atlasītājs(Modelis.Dati.Kopsavilkums.Kods) formulas veidotāja lapai.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Aizveriet lapu **Formulas redaktors**.
10. Atlasiet **Labi**.

    ![Formāta noformētāja lapa ar pievienotu jauno formulu.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Ņemiet vērā, ka aprēķinātais lauks **LevelByLookup**, kuru pievienojāt, atgriezīs nodokļa līmeni kā formāta uzskaitījuma **Nodokļu līmeņu saraksts** vērtību katram apkopotajam nodokļa transakciju ierakstam. Ieraksta nodokļa kods tiks nodots uzmeklēšanas datu avotam **Modelis.Atlasītājs** un kārtulu kopums šim datu avotam tiks izmantots, lai atlasītu pareizo nodokļa piemērošanas līmeni.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Pievienot jaunu uz formātu uzskaitījuma pamatotu datu avotu

Pēc tam jūs pievienosit jaunu datu avotu, kas attiecas uz iepriekš pievienoto formāta uzskaitījumu. Vēlāk šī datu avota vērtības tiks izmantotas ER formāta izteiksmē.

1.  Atlasiet **Pievienot sakni**.
2.  Atlasiet **Formātu uzskaitījumi\Uzskaitījums**.
3.  Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.
4.  Laukā **Formātu uzskaitījums** atlasiet **Nodokļu līmeņu saraksts**.
5.  Atlasiet **Saglabāt**.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Modificējiet esošu lauku, lai sāktu izmantot uzmeklēšanu

Pēc tam modificējiet esošo aprēķināto lauku, lai tas izmantotu konfigurēto uzmeklēšanas datu avotu, lai atgrieztu pareizo nodokļa piemērošanas līmeņa vērtību atkarībā no nodokļa koda.

1.  Atlasiet vienumu **Modelis.Dati.Kopsavilkums.Līmenis**.
2.  Atlasiet **Rediģēt**.
3.  Atlasiet **Rediģēt formulu**.

    Ievērojiet, ka pašreizējā lauka **Modelis.Dati.Kopsavilkums.Līmenis** izteiksme ietver tālāk minētos stingri kodētos nodokļu kodus.
    
    GADĪJUMS (@.Code, "VAT19", "Parasts", "InVAT19", "Parasts", "VAT7", "Samazināts", "InVAT7", "Samazināts", "TREŠAIS", "Nav", "InVAT0", "Nav", "Cits")

4.  Laukā **Formula** ievadiet **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Parasts", TaxationLevel.'Reduced taxation', "Samazināts", TaxationLevel.'No taxation', "Nav", "Cits")**.

    ![ER operācijas veidotāja lapa.](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Ņemiet vērā, ka lauka **Modelis.Dati.Kopsavilkums.Līmenis** izteiksme tagad atgriezīs nodokļa līmeni, pamatojoties uz pašreizējā ieraksta nodokļa kodu, un kārtulu kopumu, ko uzņēmuma lietotājs konfigurē uzmeklēšanas datu avotā **Modelis.Dati.Atlasītājs**.
    
5.  Atlasiet **Saglabāt**.
6.  Aizveriet lapu **Formāta veidotājs**.
7.  Atlasiet **Labi**.
8.  Atlasiet **Saglabāt**.
9.  Aizveriet lapu **Formāta noformētājs**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Pabeigta atvasinātā formāta melnraksta versija

1.  Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.
2.  Atlasiet **Pabeigt**.
3.  Atlasiet **Labi**.

## <a name="export-completed-version-of-modified-format"></a>Eksportēt modificētā formāta pabeigtu versiju

1.  Konfigurācijas kokā atlasiet vienumu **Formatēt, lai uzzinātu, kā uzmeklēt Le datus**.
2.  Kopsavilkuma cilnē **Versijas** atlasiet ierakstu, kura statuss ir **Pabeigts**.
3.  Atlasiet **Maiņa**.
4.  Atlasiet **Eksportēt kā XML failu**.
5.  Atlasiet **Labi**.
6.  Tīmekļa pārlūks lejupielādē failu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus. XML**. Saglabājiet šo failu lokāli.

Atkārtojiet šajā sadaļā norādītās darbības formāta **Formatēt, lai uzzinātu, kā uzmeklēt LE datus** vecākelementiem, un saglabājiet lokāli tālāk norādītos failus.

-   Formatēt, lai uzzinātu parametru izsaukumus.xml
-   Kartēšana, lai uzzinātu parametru izsaukumus.xml
-   Modelēt, lai uzzinātu parametru izsaukumus.xml

**Lai uzzinātu, kā izmantot konfigurēto formātu, lai uzzinātu, kā skatīt LE datu** ER formātu, lai iestatītu juridiskas personas atkarīgas nodokļu kodu kopas, lai filtrētu nodokļu darbības pēc dažādiem taksācijas līmeņiem, [veiciet soļus ER](er-app-specific-parameters-set-up.md) formāta parametru iestatīšanai juridiskās personas rakstam.

## <a name="additional-resources"></a>Papildu resursi

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko pārskatu formāta parametru iestatīšana juridiskai personai](er-app-specific-parameters-set-up.md)

[Uzmeklēšanas datu avotu konfigurēšana, lai izmantotu elektronisko pārskatu programmai raksturīgo parametru līdzekli](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
