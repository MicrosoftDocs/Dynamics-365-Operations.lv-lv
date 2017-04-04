---
title: "Elektronisko atskaišu galamērķi"
description: "Varat konfigurēt adresātu katrai elektronisko atskaišu (Electronic Reporting — ER) formāta konfigurācijai un tā izvades komponentu (mapi vai failu). Lietotāji, kuriem ir piešķirtas atbilstošas piekļuves tiesības, galamērķa iestatījumus var modificēt arī izpildlaikā. Šajā rakstā ir paskaidrota ER galamērķu pārvaldība, atbalstītie galamērķu tipi un drošības apsvērumi."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Elektronisko atskaišu galamērķi

Varat konfigurēt adresātu katrai elektronisko atskaišu (Electronic Reporting — ER) formāta konfigurācijai un tā izvades komponentu (mapi vai failu). Lietotāji, kuriem ir piešķirtas atbilstošas piekļuves tiesības, galamērķa iestatījumus var modificēt arī izpildlaikā. Šajā rakstā ir paskaidrota ER galamērķu pārvaldība, atbalstītie galamērķu tipi un drošības apsvērumi.

Elektronisko atskaišu (ER) formāta konfigurācijas parasti satur vismaz vienu izvades komponentu: failu. Parasti konfigurācijas ietver vairākus dažādu tipu failu izvades komponentus (piemēram, XML, TXT vai XLSX), kuri ir grupēti vienā mapē vai vairākās mapēs. ER galamērķu pārvaldība jums ļauj sākotnēji konfigurēt, kas notiek, kad tiek palaists katrs komponents. Pēc noklusējuma, palaižot konfigurācijas, tiek parādīts dialoglodziņš, kas ļauj lietotājam saglabāt vai atvērt failu. Tāda pati uzvedība tiek izmantota arī tad, kad importējat kādu ER konfigurāciju un neesat tai konfigurējis nekādu noteiktu galamērķi. Kad galvenajam izvades komponentam ir izveidots galamērķis, šis galamērķis ignorē noklusējuma uzvedību un mape vai fails tiek nosūtīti saskaņā ar galamērķa iestatījumiem.

## <a name="availability-and-general-prerequisites"></a>Pieejamības un vispārīgie priekšnosacījumi
ER galamērķiem funkcionalitāte nav pieejama programmā Microsoft Dynamics 365 operācijas 7.0 (februārī 2016) izlaišanai. Tāpēc jāinstalē Microsoft Dynamics 365 operācijām (November 2016 izlaidums) izmantot visas funkcijas, kas ir aprakstīti šajā tēmā. Alternatīvi, jūs varat instalēt vienu no šādiem priekšnoteikumiem. Tomēr ir jāapzinās šo alternatīvas nodrošināt ierobežotāku ER mērķa pieredzi.

-   Microsoft Dynamics 365 darbības programmas versija 7.0.1 (maija 2016)
-   ER galamērķa pārvaldības [programmas labojumfails](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Varat iestatīt galamērķus tikai ER konfigurācijām, kas ir importētas, un formātiem, kas ir pieejami lapā **Elektronisko atskaišu veidošanas konfigurācijas**.

## <a name="overview"></a>Pārskats
ER mērķa pārvaldības funkcionalitāte ir pieejama pie **organizācijas administrācija**&gt;**elektroniskās ziņošanas**. Šeit varat ignorēt konfigurācijas noklusējuma uzvedību. Importētās konfigurācijas šeit tiek rādītas tikai pēc tam, kad noklikšķināt uz **Jauns** un laukā **Atsauce** atlasāt konfigurāciju, kurai izveidot galamērķa iestatījumus.

[![Izvēloties konfigurāciju laukā atsauce](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Pēc tam, kad esat izveidojis atsauci, var izveidot faila mērķi katrai mapei vai failam. 

[![Veidojot faila atrašanās vietu](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Piezīme.** Varat izveidot vienu failu galamērķi katram izvades komponentam ar tādu pašu formātu, piemēram, mapi vai failu, kas ir atlasīts laukā **Faila nosaukums**. Pēc tam var iespējot un atspējot atsevišķas faila atrašanās vietu, galamērķi **mērķa uzstādījumus** dialoglodziņš. Poga **Iestatījumi** tiek izmantota, lai kontrolētu visus galamērķus atlasītajam failu galamērķim. Dialoglodziņā **Galamērķa iestatījumi** varat kontrolēt katru galamērķi atsevišķi, iestatot tam opciju **Iespējots**.

[![Dialoglodziņā mērķa iestatījumi](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Galamērķu tipi
Tiek atbalstīti dažādi galamērķu tipi. Visus tipus varat atspējot vai iespējot vienlaicīgi. Tādējādi jūs varat nedarīt neko vai sūtīt komponentu uz visiem konfigurētajiem galamērķiem. Nākamajās sadaļās ir aprakstīti atbalstītie galamērķi.

### <a name="email-destination"></a>E-pasta galamērķis

Opciju **Iespējots **iestatiet uz **Jā**, lai izvades failu sūtītu pa e-pastu. Pēc tam, kad šī opcija ir iespējota, varat norādīt e-pasta adresāti un rediģēt tēmu un e-pasta ziņojuma pamattekstā. Varat iestatīt konstantu tekstu e-pasta tēmu un ķermeņa vai ER formulas var izmantot, lai dinamiski izveidotu e-pasta tekstu. Kurus var konfigurēt e-pasta adreses ER divos veidos. Konfigurāciju var pabeigt tādā pašā veidā, ka drukas pārvaldības līdzeklis programmā Dynamics 365 operācijām pabeidz to. Alternatīvi, var novērst e-pasta adresi, izmantojot tiešu atsauci uz ER konfigurāciju, izmantojot formulu.

### <a name="email-address-types"></a>E-pasta adrešu tipus

Noklikšķinot uz **rediģēt** par **ar** vai **Cc** jomā, **Email** parādās dialoglodziņš. Pēc tam var atlasīt veidu e-pasta adresi, kas jāizmanto.

[![Dialoglodziņā e-pasta](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Drukāšanas iestatījumi

Ja atlasāt **drukas pārvaldību e-pastu** tips, var ievadīt noteiktu e-pasta adreses **uz** lauku. Lai izmantotu e-pasta adreses, kas netiek noteikta, jāatlasa avota tipa e-pasta faila atrašanās vietu. Tiek atbalstītas šādas vērtības: **klienta**, **kreditoru**, **izredzes**, **kontaktu**, **konkurents**, **Worker**, **prasītāja**, **potenciālo piegādātāju**, un **neatļauts kreditoru**. Kad esat atlasījis e-pasta avota tipu, izmantojiet pogu blakus **Email avota konts** laukam, lai atvērtu * * formulu dizainers * * forma. Šo formu var lietot, lai pievienotu formulu, kas norāda atlasītās partijas konts e-pasta adresāts.

[![Konfigurēt e-pasta tips drukas pārvaldība](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Ņemiet vērā, ka formulas ir atkarīgas no ER konfigurācijas. Laukā **Formula** ievadiet dokumentam specifisko atsauci uz debitora vai kreditora puses tipu. Tā vietā, lai rakstītu, varat atrast datu avota zaru, kas apzīmē debitora vai kreditora kontu, un pēc tam noklikšķināt uz **Pievienot datu avotu**, lai atjauninātu šo formulu. Piemēram, ja izmantojat konfigurāciju ISO 20022 kredīta pārskaitījums, tad zars, kas apzīmē kreditora kontu, ir **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Pretējā gadījumā ievadiet jebkuru virknes vērtību, piemēram, **DE-001**, lai saglabātu formulu.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Šajā **Email** dialoglodziņā, noklikšķiniet uz atkritnes blakus **e-pasts avota konts** laukā, lai no datora neatgriezeniski izdzēstu formulu, pēc kuras e-pasta avotu kontā. Varat arī atvērt formulu dizainers, lai mainītu formulu, kas iepriekš tika saglabāts. Lai piešķirtu e-pasta adreses, noklikšķiniet uz **rediģēt** atvērt **piešķirt e-pasta adreses** dialoglodziņš.

[![Piešķiršanu e-pasta adresātu e-pasta adreses](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurācijas e-pasta ziņojums

Izmantojiet šo e-pasta tips, ja konfigurācijas, ko izmantojat, ir mezgla datu avotu, kas atspoguļo e-pasta adresi. Datu avotus un funkcijas, var izmantot formulu noformētājā pareizi formatētu e-pasta adresi.

[![Pievienojot e-pasta adrešu datu avots e-pasta adresātu](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Piezīme.** Ir jābūt konfigurētam un pieejamam vienkāršā pasta pārsūtīšanas protokola (SMTP) serverim. Jūs varat norādīt savu SMTP serveri Dynamics 365 operācijām, pie **sistēmas administrēšanu**&gt;**Setup**&gt;**e-pasts**&gt;**e-pasta parametri**.

### <a name="archive-destination"></a>Arhīva galamērķis

Šo opciju varat izmantot, lai izvadi sūtītu uz Microsoft SharePoint mapi vai Microsoft Azure krātuvi. Opciju **Iespējots** iestatiet uz **Jā**, lai izvadi sūtītu uz galamērķi, kas ir definēts ar atlasīto dokumentu tipu. Atlasei ir pieejami tikai tie dokumentu tipi, kur grupa ir iestatīta uz **Fails**. Noteiktu dokumentu tipiem pie **organizācijas administrācija**&gt;**dokumentu pārvaldību**&gt;**dokumentu tipus,**. Konfigurēšana ER galamērķiem ir tāda pati kā konfigurēšana dokumentu pārvaldības sistēmai.

[![Dokumentu tipu lapas](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Atrašanās vieta nosaka, kur fails tiek saglabāts. Pēc **arhīva** galamērķis ir aktivizēta, darbu arhīvā var saglabāt konfigurācijas izpildes rezultātus. Rezultātus var skatīt **organizācijas administrācija**&gt;**elektroniskās ziņošanas**&gt;**elektronisko ziņojumu arhivēt darbi**. **Piezīme:** var atlasīt dokumenta tipu, par arhīvu darbu programmā Dynamics 365 operācijām, pie **organizācijas administrācija**&gt;**darbvietām**&gt;**elektroniskās ziņošanas**&gt;**elektronisko atskaišu parametrus**.

#### <a name="sharepoint"></a>SharePoint

Failu varat saglabāt norādītajā SharePoint mapē. Var definēt noklusējuma SharePoint serveri pie **organizācijas administrācija**&gt;**dokumentu pārvaldība**&gt;**dokumentu pārvaldības parametrus**, **SharePoint** tab. Pēc SharePoint mape ir konfigurēta, jūs iespējams atlasīt mapi, kurā ER produkcija tiks saglabāta dokumenta tipa. 

[![Izvēloties SharePoint mapes](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure krātuve

Kad dokumentu tipa atrašanās vieta ir iestatīta uz **Arhīva direktorijs**, varat failu saglabāt Azure krātuvē.

### <a name="file-destination"></a>Faila adresāts

Ja iestatāt **Enabled** uz **Jā**, atvērt vai saglabāt dialoglodziņš parādās, kad konfigurācija ir beigusi darboties.

### <a name="screen-destination"></a>Ekrāna mērķa

Ja iestatāt **Enabled** uz **Jā**, izvades priekšskatījums tiek veidots. Daži failu tipi, piemēram, XML, TXT vai PDF failu var apskatīt tieši pārlūka logā. Citus failu tipus, šādi Microsoft Excel vai Word, Microsoft Office Online pakalpojums tiek izmantots.

### <a name="power-bi-destination"></a>Varas BI mērķa

Iestatiet **Enabled** uz **Jā** lietot ER konfigurāciju, lai sakārtotu datu pārsūtīšanai no jūsu gadījumu dinamika 365 operācijām Microsoft Power BI pakalpojumiem. Pārsūtīti faili tiek glabāti Microsoft SharePoint Server gadījumu, ko šim nolūkam ir jākonfigurē. Lai iegūtu papildinformāciju, skatiet [lieto elektronisko atskaišu konfigurācijas, lai nodrošinātu strāvas BI ar datiem no Dynamics 365 operācijām](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Padoms.** Lai ignorētu noklusējuma uzvedību (t.i., dialoglodziņu kādai konfigurācijai), varat izveidot galamērķa atsauci un faila galamērķi galvenajam izvades komponentam un pēc tam atspējot visus galamērķus.

## <a name="security-considerations"></a>Drošības apsvērumi
ER galamērķiem tiek izmantoti divu tipu privilēģijas un pienākumi. Viena tipa vadīklas spēja uzturēt vispārējo galamērķiem, kas ir konfigurēti juridiska persona (t.i., tā kontrolē piekļuvi **elektroniskās ziņošanas galamērķiem** lapā). Otrs tips kontrolē programmas lietotāja spēju izpildes laikā ignorēt galamērķu iestatījumus, ko konfigurēja ER izstrādātājs vai ER funkcionālais konsultants.

| Loma (AOT nosaukums)                     | Lomas nosaukums                                  | Pienākums (AOT nosaukums)                     | Pienākuma nosaukums                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroniskā pārskata izstrādātājs             | ERFormatDestinationConfigure        | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu                |
| ERFunctionalConsultant              | Elektronisko pārskatu veidošanas funkcionālais konsultants | ERFormatDestinationConfigure        | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu                |
| PaymAccountsPayablePaymentsClerk    | Kreditoriem maksājamo rēķinu darbinieks            | ERFormatDestinationRuntimeConfigure | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu izpildlaikā |
| PaymAccountsReceivablePaymentsClerk | Debitoru parādu maksājumu darbinieks         | ERFormatDestinationRuntimeConfigure | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu izpildlaikā |

**Piezīme.** Iepriekš uzskaitītajos pienākumos tiek izmantotas divas privilēģijas. Šo privilēģiju nosaukumi ir tādi paši kā tām atbilstošo pienākumu nosaukumi: **ERFormatDestinationConfigure** un **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Esmu importējis elektroniskas konfigurācijas un tās redzu lapā Elektronisko atskaišu veidošanas konfigurācijas. Bet kāpēc es neredzu tos elektronisko atskaišu galamērķiem lapā?

Pārliecinieties, vai ir noklikšķināts **New** un pēc tam atlasiet konfigurāciju formā **references** lauks. Lapā **Elektronisko atskaišu galamērķi** varat redzēt tikai tās konfigurācijas, kam ir konfigurēti galamērķi.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Vai ir kāds veids, kā noteikt, kuras Azure krātuves kontam un debeszils Blob krātuves tiek izmantoti?

Nr.p.k. Tiek izmantots noklusējuma Azure Blob uzglabāšanas, kas tiek definēta un dokumentu vadības sistēmu izmanto.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Kāds ir mērķis mērķa failu mērķa uzstādījumus? Ko šis iestatījums dara?

Galamērķis **Fails** tiek izmantots, lai kontrolētu dialoglodziņu. Iespējojot šo galamērķi vai nav galamērķis ir definēts konfigurāciju, jums skatiet atvērt vai saglabāt dialoglodziņš pēc izvades faila izveides.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Vai varat sniegt piemēru formulai, kas atsaucas uz kreditora kontu, uz kuru es varu sūtīt e-pastu?

Šī formula ir atkarīga no ER konfigurācijas. Piemēram, ja lietojat konfigurāciju ISO 20022 kredīta pārskaitījums, varat lietot **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** vai **model.Payments.Creditor.Identification.SourceID**, lai iegūtu saistītu kreditora kontu.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Viena no manām formāta konfigurācijām ietver vairākus failus, kas ir grupēti vienā mapē (piemēram, mapē Mape1 ietilpst faili Fails1, Fails2 un Fails3). Kā iestatīt galamērķus tā, lai fails Mape1.zip netiktu izveidots vispār, Fails1 tiktu nosūtīts pa e-pastu, Fails2 tiktu nosūtīts uz SharePoint, bet failu Fails3 es varētu atvērt uzreiz pēc konfigurācijas izpildīšanas?

Priekšnoteikums ir, ka jūsu formātam jābūt pieejamam ER konfigurācijās. Ja jums ir jūsu formāts, atveriet lapu **Elektronisko atskaišu galamērķi** un izveidojiet jaunu atsauci uz šo konfigurāciju. Pēc tam jums ir nepieciešami četri failu galamērķi — viens katram izvades komponentam. Izveidojiet pirmo failu galamērķi, piešķiriet tam nosaukumu, piemēram, **Mape**, un atlasiet faila nosaukumu, kas apzīmē kādu mapi jūsu konfigurācijā. Pēc tam noklikšķiniet uz **Iestatījumi** un pārliecinieties, ka visi galamērķi ir atspējoti. Šim failu galamērķim mape netiks izveidota. Pēc noklusējuma, tā kā starp failiem un pamata mapēm pastāv hierarhiskas atkarības, šie faili darbosies tādā pašā veidā. Citiem vārdiem sakot — tie netiks nekur sūtīti. Lai ignorētu šo noklusējuma uzvedību, jums ir jāizveido vēl trīs failu galamērķi — viens katram failam. Katram galamērķa iestatījumos jums ir jāiespējo tas galamērķis, uz kuru šis fails ir jānosūta.

# <a name="see-also"></a>Skatiet arī

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)


