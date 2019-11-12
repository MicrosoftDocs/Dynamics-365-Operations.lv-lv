---
title: Bieži uzdotie jautājumi par Dynamics 365 Talent integrāciju ar Dynamics 365 Finance
description: Šajā tēmā ir paskaidrots, kādi dati tiek sinhronizēti risinājumu Talent un Finance integrācijas laikā.
author: andreabichsel
manager: AnnBe
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8b9fa6b8d5109f873c784d384d49f685f94da228
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622772"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a>Bieži uzdotie jautājumi par Dynamics 365 Talent integrāciju ar Dynamics 365 Finance

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par to, kādi dati tiek sinhronizēti, integrējot Dynamics 365 Talent ar Dynamics 365 Finance.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Vai tiek sinhronizēti visi dati vai tikai daži datu elementi?

Core HR gadījumā tiek sinhronizēta datu apakškopa. Visu elementu sarakstu skatiet tēmā [Integrācija no Dynamics 365 Talent uz Dynamics 365 Finance](talent-financeandoperations-integration.md).

Attract un Onboard gadījumā visi dati tiek iegūti no Common Data Service.

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a>Kāpēc es neredzu nevienu datu sinhronizāciju Common Data Service?

Pēc noklusējuma Common Data Service integrēšana ir izslēgta jaunās vidēs, kurās nav ietverti nodrošinātie demonstrācijas dati. Pēc noklusējuma tas ir ieslēgts jaunās vidēs, kas ietver demo datus, un datu sinhronizācija sākas, kad tiek nodrošināta vide. Pēc tam, kad jūsu vide ir gatava sinhronizēt datus, varat ieslēgt integrāciju. Papildinformāciju skatiet sadaļu [Konfigurēt Common Data Service integrāciju](hr-common-data-service-integration.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Vai var izveidot jaunu kartējumu, neizmantojot veidnes?

Veidnes ir sākumpunkts. Varat izveidot savu veidni, taču veidne vienmēr ir nepieciešama, veidojot integrācijas projektu. Plašāku informāciju par datu integrētāju (DI), veidnēm un projektiem skatiet rakstā [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a>Vai var kartēt finanšu dimensijas pārsūtīšanai starp Talent un Finance?

Finanšu dimensijas pašlaik nav pakalpojumā Common Data Service un līdz ar to nav noklusējuma veidnes sastāvdaļa. Šis elements ir plānots, bet pašlaik nav zināms izlaišanas laiks.

Tādu datu gadījumā, kuri atrodas risinājumā Finance, bet kuru nav risinājumā Talent, saistiet abas sistēmas kopā, izmantojot vienumu **Konfigurēt saites** risinājumā Talent. Plašāku informāciju par to, kā konfigurēt saites starp Talent un Finance, skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 Talent: Core HR (2018. gada 31. oktobris)](whats-new-talent-october-31.md).

![Kartēt finanšu dimensijas](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Dažreiz, importējot darbiniekus, tie tiek iekļauti neaktīvo darbinieku sarakstā risinājumā Finance. Kādēļ?

Šī kļūda var rasties, ja darbiniekiem nav aktīva nodarbinātības detalizētas informācijas ieraksta risinājumā Talent. Lai to atrisinātu, atveriet sadaļu **Personāla vadība \> Darbinieki \> Nodarbinātības vēsture \> Datumu pārvaldnieks** un pārbaudiet, vai ir aktīvs nodarbinātības detalizētas informācijas ieraksts.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Vai, izvēloties kartēt tikai lauku apakškopu, izmaiņas, kas veiktas nekartētiem laukiem, izraisīs sinhronizāciju?

Datu sinhronizācija tiek veikta saskaņā ar izpildes grafiku. Integrācija ņems vērā ierakstu, ja ir mainīts kāds no ieraksta laukiem neatkarīgi no tā, vai lauks ietilpst integrācijas kartējumā.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Kā var nosūtīt tikai aktīvo nodarbināto izmaiņas, nevis pārtrauktu darba attiecību ierakstus?

Ar opciju “Papildu vaicājums” varat filtrēt un pārveidot avota datus pirms to nosūtīšanas uz galamērķi.

![Aktīvo darbinieku papildu vaicājums](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Vai var norādīt, kurus laukus nosūtīt uz risinājumu Finance konkrētam elementam?

Laukus var pievienot vai noņemt no integrācijas uzdevuma. Ne visi datu lauki, kas pastāv pakalpojuma Common Data Service elementā, tiks aizpildīti no Core HR.
Papildu datus var aizpildīt, izmantojot PowerApps.

![Pievienot vai noņemt laukus no integrācijas uzdevuma](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Es iestatīju integrāciju kā pakešuzdevumu, bet tika zaudēts risinājuma Talent savienojums ar mērķa sistēmu. Kā var nosūtīt to pašu izmaiņu kopumu uz mērķa sistēmu?

Izņēmumu apstrādei nav nepieciešama īpaša iestatīšana. Datu integrētājs automātiski konstatēs un ziņos par kļūdām, kas notiek avota un mērķa sistēmā, un ļaus manuāli veikt atkārtotu mēģinājumu. Tomēr tas neļauj manuāli veikt datu korekciju. Ja ir nepieciešami datu atjauninājumi, tie jāveic avota vai mērķa sistēmā.

## <a name="can-i-set-up-bi-directional-integration"></a>Vai var iestatīt divvirzienu integrāciju?

Nē, pašlaik tiek nodrošināta vienvirziena integrācija (no Talent uz Finance and Operations). Tomēr ir pieejama noklusējuma veidne datu sūtīšanai no Talent uz Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Vai var atļaut ieraksta dzēšanu integrācijas ietvaros?

Nē, datu integrētājs nevarēs iegūt dzēstos ierakstus datu pārsūtīšanai. Pašlaik ir iekļauta tikai datu izveide un atjauninājumi (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Vai var atkārtoti palaist izpildi ar kļūdām? Ja tas tā ir, vai tiks nosūtīts fails pilnībā vai tikai izmaiņas?

Pirmoreiz palaižot datu integrētāju, vienmēr tiek veikta pilna izpilde. Turpmāko palaišanas reižu pamatā ir izmaiņu izsekošana. Izpildot kļūdainu palaišanu, tiek izgūti ieraksti palaišanas ietvaros un tiek nosūtītas jaunākās izmaiņas no Common Data Service.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Saglabājot projektu, tiek parādīts kļūdas ziņojums: “Projektam ir kartēšanas kļūdas.” Ko darīt?

Pārbaudiet integrācijas atslēgu iestatījumus, veiciet nepieciešamās izmaiņas iestatījumos un pēc tam atsvaidziniet projekta elementus.

Ja tiek izmantota noklusējuma veidne, integrācijas atslēgas tiks importētas automātiski. Šī problēma var rasties, pievienojot jaunus uzdevumus esošai veidnei.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Ja ir noteikts skaits N juridisko personu, kurās nodarbinātajiem ir iestatītas nodarbinātības, vai ir jāveido kartējums katrai no tām?

Jā, katrai juridiskajai personai risinājumā Finance ir nepieciešams atsevišķs integrācijas projekts datu integrācijas ietvaros.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Ir nepieciešams pārsūtīt datus, kas nav daļa no Microsoft nodrošinātās noklusējuma veidnes. Vai to var izdarīt?

Jā, esošajai veidnei var pievienot vai noņemt laukus. Veidni var modificēt, lai iekļautu papildu datus no citiem Common Data Service elementiem. Lai elements tiktu iekļauts veidnē, tam ir jāatrodas pakalpojumā Common Data Service. 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Es tikko izveidoju jaunas Finance un Talent vides, un tiek rādīts kļūdas ziņojums “Datu vērtība ir ārpus integritātes ierobežojumiem”. Kādēļ?

Minētajai kļūdai var būt šādi iemesli:

- Datu pārsūtīšanas dēļ avotā (Common Data Service) tika izgūti dublēti ieraksti.

- Datu pārsūtīšanai ir nulles vērtības laukiem, kas ir nepieciešami risinājumā Finance and Operations. Pārbaudiet, vai dati, kas atrodas pakalpojumā Common Data Service, atbilst Finance and Operations prasībām.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Ja radušās izpildes kļūdas un darbinieka ID netika sinhronizēts, kā atrast vēsturē darbu, kurā ir nesekmīgi apstrādātais darbinieka ieraksts?

Datu integrētājs izveidos vairākus projektus risinājumā Finance. Relācija starp datu integrētāja uzdevumu un Finance projektu ir viens pret vienu.

Izsekojiet laiku datu integrētāja izpildes vēsturē un meklējiet projektu ar vērtību “indekss -1” risinājumā Finance. Ja datu integrētājā uzdevuma numurs ir 9, indekss risinājumā Finance ir 8.

1. Iegūstiet uzdevuma indeksu no datu integrētāja (šajā piemērā tas ir “9”).

![Uzdevuma indeksa iegūšana no datu integrētāja](media/CaptureTaskIndex.png)

2. Izsekojiet projekta izpildes laiku.

![Projekta izpildes laika izsekošana](media/CaptureTimeOfExecution.png)

3. Risinājumā Finance norādiet indeksu-1. Šajā piemērā projekts ar sufiksu “8” un projekta ar indeksu “0” izpildes laiks atbilst izpildes laikam 2. darbībā.

![Indeksa atrašana](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a>Pēc Talent un Finance integrācijas Talent dati netiek rādīti risinājumā Finance. Ko darīt?

Integrācija risinājumā Finance paredz divas darbības. Vispirms pārliecinieties, vai Talent dati ir atjaunināti un ir pieejami pakalpojumā Common Data Service. Šī sinhronizācija tiek veikta gandrīz reālā laikā, un to var pārbaudīt risinājumā PowerApps, skatot datus, kuri ir datu elementos.

![Dati pakalpojumā Common Data Service](media/DataInCDS.png)

Ja dati pakalpojumā Common Data Service netiek rādīti paredzētajā veidā, pārbaudiet, vai integrācijā šis elements tiek atbalstīts. Lai iekļautu papildu datus pakalpojumā Common Data Service, būs nepieciešamas izmaiņas no Microsoft puses.

Ja elements tiek atbalstīts un šie dati ir pieejami pakalpojumā Common Data Service, pārbaudiet, vai datu integrētājā ir pareizs kartējums. Ja integrētāja kartējums ir pareizs, pārbaudiet, vai ir veiksmīgi izpildīti datu pārvaldības darbi. Pakešveida darbu izpildes laikā var rasties kļūdas. Plašāku informāciju par to, kā izmantot rīku Datu pārvaldība, skatiet sadaļā [Datu pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Manu darbinieku adreses ir nepareizas pēc tam, kad tās ir importētas risinājumā Finance. Ko darīt?

Vienuma **Atrašanās vietas ID** numuru sērija izmanto vienu un to pašu modeli gan risinājumā Talent, gan Finance. Numuru sērijai ir jābūt unikālai abās pusēs, lai nebūtu adrešu sadursmju, integrējot datus no Common Data Service uz Finance and Operations.

Veicot Talent ieviešanu, pārbaudiet, vai numuru sērijas nav vienādas risinājumā Talent un Finance. Pārbaudiet, vai visas numuru sērijas nav identiskas, ja dati tiek uzturēti abās sistēmās.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Izveidojot savienojumu kopu, savienojums netiek rādīts nolaižamajā sarakstā Savienojums. Ko darīt?

Pārliecinieties, ka, veidojot savienojumus, izvēlaties Dynamics 365 Finance un Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Veicot nodarbinātību sinhronizāciju, tiek parādīti kļūdas ziņojumi “CompanyInfo_FK neeksistē” vai “Vērtība “31.12.2154. 23:59:59” laukā “Nodarbinātības beigu datums” nav atrasta saistītajā tabulā “Nodarbinātība”.” Ko darīt?

Pārliecinieties, ka veicat kartēšanu pareizajai juridiskajai personai. Juridiskās personas sinhronizēšana neietilpst noklusējuma veidnē, tāpēc ir paredzēts, ka visas juridiskās personas, kas atrodas programmā Talent un Common Data Service, atrodas arī programmā Finance.
Pārliecinieties, ka esat atlasījis pareizās juridiskās personas saistītajai savienojumu kopai.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Pēc mana projekta iestatīšanas lauku kartējums risinājumam Finance ir tukšs. Ko darīt?

Atsvaidziniet datu elementus risinājumā Finance, atverot sadaļu **Datu pārvaldība \> Struktūras parametri \> Elementu iestatījumi \> Atsvaidzināt elementu sarakstu.** Šīs darbības pabeigšanai ir nepieciešamas dažas minūtes, un pēc tam būs redzami attiecīgie kartējumi. Šī problēma rodas, veidojot jaunus projektus.

![Trūkst lauku kartējuma](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Papildu resursi

- Datu integrētājs (DI): 

  - [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [Datu integrētāja kļūdu pārvaldība un problēmu novēršana](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [Atbildes sniegšana uz DSR pieprasījumiem sistēmas ģenerētiem žurnāliem platformā PowerApps, Microsoft Flow un Common Data Service](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Datu pārvaldība:

  - [Datu pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
