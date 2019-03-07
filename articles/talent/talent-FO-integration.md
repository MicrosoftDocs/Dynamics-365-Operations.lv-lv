---
title: Bieži uzdotie jautājumi par Dynamics 365 for Talent integrāciju ar Dynamics 365 for Finance and Operations
description: Šajā tēmā ir paskaidrots, kādi dati tiek sinhronizēti risinājumu Talent un Finance and Operations integrācijas laikā.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305347"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Bieži uzdotie jautājumi par Dynamics 365 for Talent integrāciju ar Dynamics 365 for Finance and Operations

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par to, kādi dati tiek sinhronizēti, integrējot Dynamics 365 for Talent ar Dynamics 365 for Finance and Operations.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Vai tiek sinhronizēti visi dati vai tikai daži datu elementi?

Core Human Resources (HR) gadījumā tiek sinhronizēta datu apakškopa. Visu elementu sarakstu skatiet tēmā [Dynamics 365 for Talent integrācija ar Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).

Attract un Onboard gadījumā visi dati ir risinājuma Common Data Service (CDS) programmām sākotnējie dati.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Vai var izveidot jaunu kartējumu, neizmantojot veidnes?

Veidnes ir sākumpunkts. Varat izveidot savu veidni, taču veidne vienmēr ir nepieciešama, veidojot integrācijas projektu. Plašāku informāciju par datu integrētāju (DI), veidnēm un projektiem skatiet tēmā [Datu integrēšana risinājumā Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Vai var kartēt finanšu dimensijas pārsūtīšanai starp Talent un Finance and Operations?

Finanšu dimensijas pašlaik nav risinājumā CDS programmām un līdz ar to nav noklusējuma veidnes sastāvdaļa. Šis elements ir plānots, bet pašlaik nav zināms izlaišanas laiks.

Tādu datu gadījumā, kuri atrodas risinājumā Finance and Operations, bet kuru nav risinājumā Talent, saistiet abas sistēmas kopā, izmantojot vienumu **Konfigurēt saites** risinājumā Talent. Plašāku informāciju par to, kā konfigurēt saites starp Talent un Finance and Operations, skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 31. oktobris)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Dažreiz, importējot darbiniekus, tie tiek iekļauti neaktīvo darbinieku sarakstā risinājumā Finance and Operations. Kādēļ?

Šī kļūda var rasties, ja darbiniekiem nav aktīva nodarbinātības detalizētas informācijas ieraksta risinājumā Talent. Lai to atrisinātu, atveriet sadaļu **Personāla vadība \> Darbinieki \> Nodarbinātības vēsture \> Datumu pārvaldnieks** un pārbaudiet, vai ir aktīvs nodarbinātības detalizētas informācijas ieraksts.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Vai, izvēloties kartēt tikai lauku apakškopu, izmaiņas, kas veiktas nekartētiem laukiem, izraisīs sinhronizāciju?

Datu sinhronizācija tiek veikta saskaņā ar izpildes grafiku. Integrācija ņems vērā ierakstu, ja ir mainīts kāds no ieraksta laukiem neatkarīgi no tā, vai lauks ietilpst integrācijas kartējumā.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Kā var nosūtīt tikai aktīvo nodarbināto izmaiņas, nevis pārtrauktu darba attiecību ierakstus?

Ar opciju “Papildu vaicājums” varat filtrēt un pārveidot avota datus pirms to nosūtīšanas uz galamērķi.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Vai var norādīt, kurus laukus nosūtīt uz risinājumu Finance and Operations konkrētam elementam?

Laukus var pievienot vai noņemt no integrācijas uzdevuma. Ne visi datu lauki, kas pastāv risinājuma CDS programmām (CDS 2.0) elementā, tiks aizpildīti no Core HR.
Papildu datus var aizpildīt, izmantojot PowerApps.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Es iestatīju integrāciju kā pakešuzdevumu, bet tika zaudēts risinājuma Talent savienojums ar mērķa sistēmu. Kā var nosūtīt to pašu izmaiņu kopumu uz mērķa sistēmu?

Izņēmumu apstrādei nav nepieciešama īpaša iestatīšana. Datu integrētājs automātiski konstatēs un ziņos par kļūdām, kas notiek avota un mērķa sistēmā, un ļaus manuāli veikt atkārtotu mēģinājumu. Tomēr tas neļauj manuāli veikt datu korekciju. Ja ir nepieciešami datu atjauninājumi, tie jāveic avota vai mērķa sistēmā.

## <a name="can-i-set-up-bi-directional-integration"></a>Vai var iestatīt divvirzienu integrāciju?

Nē, pašlaik tiek nodrošināta vienvirziena integrācija (no Talent uz Finance and Operations). Tomēr ir pieejama noklusējuma veidne datu sūtīšanai no Talent uz Finance and Operations.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Vai var atļaut ieraksta dzēšanu integrācijas ietvaros?

Nē, datu integrētājs nevarēs iegūt dzēstos ierakstus datu pārsūtīšanai. Pašlaik ir iekļauta tikai datu izveide un atjauninājumi (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Vai var atkārtoti palaist izpildi ar kļūdām? Ja tas tā ir, vai tiks nosūtīts fails pilnībā vai tikai izmaiņas?

Pirmoreiz palaižot datu integrētāju, vienmēr tiek veikta pilna izpilde. Turpmāko palaišanas reižu pamatā ir izmaiņu izsekošana. Izpildot kļūdainu palaišanu, tiek izgūti ieraksti palaišanas ietvaros un tiek nosūtītas jaunākās izmaiņas no CDS.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Saglabājot projektu, tiek parādīts kļūdas ziņojums: “Projektam ir kartēšanas kļūdas.” Ko darīt?

Pārbaudiet integrācijas atslēgu iestatījumus, veiciet nepieciešamās izmaiņas iestatījumos un pēc tam atsvaidziniet projekta elementus.

Ja tiek izmantota noklusējuma veidne, integrācijas atslēgas tiks importētas automātiski. Šī problēma var rasties, pievienojot jaunus uzdevumus esošai veidnei.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Ja ir noteikts skaits N juridisko personu, kurās nodarbinātajiem ir iestatītas nodarbinātības, vai ir jāveido kartējums katrai no tām?

Jā, katrai juridiskajai personai risinājumā Finance and Operations ir nepieciešams atsevišķs integrācijas projekts datu integrācijas ietvaros.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Ir nepieciešams pārsūtīt datus, kas nav daļa no Microsoft nodrošinātās noklusējuma veidnes. Vai to var izdarīt?

Jā, esošajai veidnei var pievienot vai noņemt laukus. Veidni var modificēt, lai iekļautu papildu datus no citiem risinājuma CDS programmām elementiem. Elementam jābūt risinājumā CDS programmām, lai tas tiktu iekļauts veidnē. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Es tikko izveidoju jaunas Finance and Operations un Talent vides, un tiek rādīts kļūdas ziņojums “Datu vērtība ir ārpus integritātes ierobežojumiem”. Kādēļ?

Minētajai kļūdai var būt šādi iemesli:

- Datu pārsūtīšanas rezultātā notika dublētu ierakstu ieguve avota sistēmā (CDS).

- Datu pārsūtīšanai ir nulles vērtības laukiem, kas ir nepieciešami risinājumā Finance and Operations. Pārbaudiet, vai dati, kas atrodas CDS, atbilst Finance and Operations prasībām.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Ja radušās izpildes kļūdas un darbinieka ID netika sinhronizēts, kā atrast vēsturē darbu, kurā ir nesekmīgi apstrādātais darbinieka ieraksts?

Datu integrētājs izveidos vairākus projektus risinājumā Finance and Operations. Relācija starp datu integrētāja uzdevumu un Finance and Operations projektu ir viens pret vienu.

Izsekojiet laiku datu integrētāja izpildes vēsturē un meklējiet projektu ar vērtību “indekss – 1” risinājumā Finance and Operations. Ja datu integrētājā uzdevuma numurs ir 9, indekss risinājumā Finance and Operations ir 8.

1. Iegūstiet uzdevuma indeksu no datu integrētāja (šajā piemērā tas ir “9”).

![Uzdevuma indeksa iegūšana no datu integrētāja](media/CaptureTaskIndex.png)

2. Izsekojiet projekta izpildes laiku.

![Projekta izpildes laika izsekošana](media/CaptureTimeOfExecution.png)

3. Risinājumā Finance and Operations atrodiet vērtību “indekss – 1”. Šajā piemērā projekts ar sufiksu “8” un projekta ar indeksu “0” izpildes laiks atbilst izpildes laikam 2. darbībā.

![Indeksa atrašana](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Pēc Talent un Finance and Operations integrācijas Talent dati netiek rādīti risinājumā Finance and Operations. Ko darīt?

Integrācija risinājumā Finance and Operations paredz divas darbības. Vispirms pārbaudiet, ka Talent dati ir atjaunināti un ir pieejami risinājumā CDS. Šī sinhronizācija tiek veikta gandrīz reālā laikā, un to var pārbaudīt risinājumā PowerApps, skatot datus, kuri ir datu elementos.

![Dati risinājumā CDS](media/DataInCDS.png)

Ja dati neparādās, kā paredzēts, risinājumā CDS, pārbaudiet, vai elements tiek atbalstīts integrācijas ietvaros. Lai iekļautu papildu datus risinājumā CDS, būs nepieciešamas izmaiņas no Microsoft puses.

Ja elements tiek atbalstīts un šie dati ir pieejami risinājumā CDS, pārbaudiet, vai kartējums ir pareizs datu integrētājā. Ja integrētāja kartējums ir pareizs, pārbaudiet, vai ir veiksmīgi izpildīti datu pārvaldības darbi. Pakešveida darbu izpildes laikā var rasties kļūdas. Plašāku informāciju par to, kā izmantot rīku Datu pārvaldība, skatiet sadaļā [Datu pārvaldība](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Manu darbinieku adreses ir nepareizas pēc tam, kad tās ir importētas risinājumā Finance and Operations. Ko darīt?

Vienuma **Atrašanās vietas ID** numuru sērija izmanto vienu un to pašu modeli gan risinājumā Talent, gan Finance and Operations. Numuru sērijai ir jābūt unikālai abās pusēs, lai nebūtu adrešu neatbilstības, integrējot datus no CD uz Finance and Operations.

Veicot Talent ieviešanu, pārbaudiet, vai numuru sērijas nav vienādas risinājumā Talent un Finance and Operations. Pārbaudiet, vai visas numuru sērijas nav identiskas, ja dati tiek uzturēti abās sistēmās.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Izveidojot savienojumu kopu, savienojums netiek rādīts nolaižamajā sarakstā Savienojums. Ko darīt?

Pārliecinieties, ka, veidojot savienojumus, izvēlaties Dynamics 365 for Finance and Operations (pašlaik priekšskatījumā) un Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Veicot nodarbinātību sinhronizāciju, tiek parādīti kļūdas ziņojumi “CompanyInfo_FK neeksistē” vai “Vērtība “31.12.2154. 23:59:59” laukā “Nodarbinātības beigu datums” nav atrasta saistītajā tabulā “Nodarbinātība”.” Ko darīt?

Pārliecinieties, ka veicat kartēšanu pareizajai juridiskajai personai. Juridiskās personas sinhronizēšana neietilpst noklusējuma veidnē, tāpēc paredzams, ka visas juridiskās personas, kas atrodas risinājumā Talent un CDS, atrodas arī risinājumā Finance and Operations.
Pārliecinieties, ka esat atlasījis pareizās juridiskās personas saistītajai savienojumu kopai.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Pēc mana projekta iestatīšanas lauku kartējums risinājumam Finance and Operations ir tukšs. Ko darīt?

Atsvaidziniet datu elementus risinājumā Finance and Operations, atverot sadaļu **Datu pārvaldība \> Struktūras parametri \> Elementu iestatījumi \> Atsvaidzināt elementu sarakstu.** Šīs darbības pabeigšanai ir nepieciešamas dažas minūtes, un pēc tam būs redzami attiecīgie kartējumi. Šī problēma rodas, veidojot jaunus projektus.

![Trūkst lauku kartējuma](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Papildu resursi

- Datu integrētājs (DI): 

  - [Integrējiet datus risinājumā Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Datu integrētāja kļūdu pārvaldība un problēmu novēršana](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [Atbildes sniegšanas uz DSR pieprasījumiem sistēmas ģenerētiem ziņojumiem risinājumā PowerApps, Microsoft Flow un Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Datu pārvaldība:

  - [Datu pārvaldība](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)