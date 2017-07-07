---
title: "Elektronisko atskaišu galamērķi"
description: "Varat konfigurēt adresātu katrai elektronisko atskaišu (Electronic Reporting — ER) formāta konfigurācijai un tā izvades komponentu (mapi vai failu). Lietotāji, kuriem ir piešķirtas atbilstošas piekļuves tiesības, galamērķa iestatījumus var modificēt arī izpildlaikā. Šajā rakstā ir paskaidrota ER galamērķu pārvaldība, atbalstītie galamērķu tipi un drošības apsvērumi."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fb2aeee1f38823e7ea96071f773e8448d65ba8ff
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="electronic-reporting-destinations"></a>Elektronisko atskaišu galamērķi

[!include[banner](../includes/banner.md)]


Varat konfigurēt adresātu katrai elektronisko atskaišu (Electronic Reporting — ER) formāta konfigurācijai un tā izvades komponentu (mapi vai failu). Lietotāji, kuriem ir piešķirtas atbilstošas piekļuves tiesības, galamērķa iestatījumus var modificēt arī izpildlaikā. Šajā rakstā ir paskaidrota ER galamērķu pārvaldība, atbalstītie galamērķu tipi un drošības apsvērumi.

Elektronisko atskaišu (ER) formāta konfigurācijas parasti satur vismaz vienu izvades komponentu: failu. Parasti konfigurācijas ietver vairākus dažādu tipu failu izvades komponentus (piemēram, XML, TXT vai XLSX), kuri ir grupēti vienā mapē vai vairākās mapēs. ER galamērķu pārvaldība jums ļauj sākotnēji konfigurēt, kas notiek, kad tiek palaists katrs komponents. Pēc noklusējuma, kad tiek palaista kāda konfigurācija, tiek parādīts dialoglodziņš, ko lietotājs var izmantot, lai failu saglabātu vai atvērtu. Tāda pati uzvedība tiek izmantota arī tad, kad importējat kādu ER konfigurāciju un neesat tai konfigurējis nekādu noteiktu galamērķi. Kad galvenajam izvades komponentam ir izveidots galamērķis, šis galamērķis ignorē noklusējuma uzvedību un mape vai fails tiek nosūtīti saskaņā ar galamērķa iestatījumiem.

## <a name="availability-and-general-prerequisites"></a>Pieejamības un vispārīgie priekšnosacījumi
ER galamērķu funkcionalitāte nav pieejama programmatūrā Microsoft Dynamics AX 7.0 (2016. gada februāra laidienā). Tāpēc, lai varēti izmantot visas šajā tēmā aprakstītās funkcijas, ir jāinstalē programmatūras Microsoft Dynamics 365 for Operations versija 1611 (2016. gada novembra laidiens). Ja vēlaties, varat instalēt vienu no tālāk norādītajiem priekšnosacījumiem. Taču ņemiet vērā, ka šī alternatīva sniedz ierobežotāku ER galamērķa funkcionalitāti.

-   Microsoft Dynamics AX programmas versija 7.0.1 (2016. gada maijs)
-   ER galamērķa pārvaldības [programmas labojumfails](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Varat iestatīt galamērķus tikai ER konfigurācijām, kas ir importētas, un formātiem, kas ir pieejami lapā **Elektronisko atskaišu veidošanas konfigurācijas**.

## <a name="overview"></a>Pārskats
ER galamērķa pārvaldības funkcionalitāte ir pieejama sadaļā **Organizācijas administrēšana** &gt; **Elektronisko pārskatu veidošana**. Šeit varat ignorēt konfigurācijas noklusējuma uzvedību. Importētās konfigurācijas šeit tiek rādītas tikai pēc tam, kad noklikšķināt uz **Jauns** un laukā **Atsauce** atlasāt konfigurāciju, kurai izveidot galamērķa iestatījumus.

[![Konfigurācijas atlasīšana laukā Atsauce](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Kad esat izveidojis atsauci, varat izveidot failu galamērķi katrai mapei vai failam. 

[![Faili galamērķa izveidošana](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Piezīme.** Varat izveidot vienu failu galamērķi katram izvades komponentam ar tādu pašu formātu, piemēram, mapi vai failu, kas ir atlasīts laukā **Faila nosaukums**. Pēc tam šiem failu galamērķiem dialoglodziņā **Galamērķa iestatījumi** varat iespējot un atspējot atsevišķus galamērķus. Poga **Iestatījumi** tiek izmantota, lai kontrolētu visus galamērķus atlasītajam failu galamērķim. Dialoglodziņā **Galamērķa iestatījumi** varat kontrolēt katru galamērķi atsevišķi, iestatot tam opciju **Iespējots**.

[![Dialoglodziņš Galamērķu iestatījumi](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Galamērķu tipi
Tiek atbalstīti dažādi galamērķu tipi. Visus tipus varat atspējot vai iespējot vienlaicīgi. Tādējādi jūs varat nedarīt neko vai sūtīt komponentu uz visiem konfigurētajiem galamērķiem. Nākamajās sadaļās ir aprakstīti atbalstītie galamērķi.

### <a name="email-destination"></a>E-pasta galamērķis

Opciju **Iespējots** iestatiet uz **Jā**, lai izvades failu sūtītu pa e-pastu. Kad šī opcija ir iespējota, varat norādīt e-pasta adresātus, ka arī rediģēt tēmu un e-pasta ziņojuma pamattekstu. E-pasta ziņojuma tēmai un pamattekstam varat iestatīt konstantus tekstus, vai arī varat lietot ER formulas, lai e-pasta tekstus izveidotu dinamiski. E-pasta adreses lietošanai ar ER varat konfigurēt divos veidos. Konfigurēšanu var veikt tāpat, kā to nodrošina programmatūras Dynamics 365 for Finance and Operations līdzeklis Drukāšanas iestatījumi. Ja vēlaties, e-pasta adresi varat atrisināt, izmantojot tiešu atsauci uz ER konfigurāciju, lietojot formulu.

### <a name="email-address-types"></a>E-pasta adrešu tipi

Kad noklikšķināt uz **Rediģēt** laukam **Kam** vai **Kopija**, tiek parādīts dialoglodziņš **E-pasta ziņojuma adresāts**. Pēc tam varat atlasīt izmantojamo e-pasta adreses tipu.

[![Dialoglodziņš E-pasta ziņojuma adresāts](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Drukas pārvaldība

Ja atlasāt tipu **Drukas pārvaldības e-pasta ziņojums**, tad laukā **Kam** varat ievadīt fiksētas e-pasta adreses. Lai lietotu e-pasta adreses, kas nav fiksētas, jums faila galamērķim ir jāatlasa e-pasta avota tips. Tiek atbalstītas šādas vērtības: **Debitors**, **Kreditors**, **Potenciālais klients**, **Kontaktpersona**, **Konkurents**, **Nodarbinātais**, **Kandidāts**, **Potenciālais piegādātājs** un **Neatļauts piegādātājs**. Kad e-pasta avota tips ir atlasīts, izmantojiet pogu blakus laukam **E-pasta ziņojuma avota konts**, lai atvērtu formu **Formulas veidotājs**. Šo formu varat lietot, lai e-pasta galamērķim pievienotu formulu, kura apzīmē atlasītās puses kontu.

[![Konfigurēt drukas pārvaldības e-pasta tipu](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Ņemiet vērā, ka formulas ir atkarīgas no ER konfigurācijas. Laukā **Formula** ievadiet dokumentam specifisko atsauci uz debitora vai kreditora puses tipu. Tā vietā, lai rakstītu, varat atrast datu avota zaru, kas apzīmē debitora vai kreditora kontu, un pēc tam noklikšķināt uz **Pievienot datu avotu**, lai atjauninātu šo formulu. Piemēram, ja izmantojat konfigurāciju ISO 20022 kredīta pārskaitījums, tad zars, kas apzīmē kreditora kontu, ir **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Pretējā gadījumā ievadiet jebkuru virknes vērtību, piemēram, **DE-001**, lai saglabātu formulu.

[![Formulas veidotājs](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Dialoglodziņā **E-pasta ziņojuma adresāts** noklikšķiniet uz atkritnes, kas atrodas blakus laukam **E-pasta ziņojuma avota konts**, lai neatgriezeniski dzēstu formulu šim e-pasta avota kontam. Formulas veidotāju varat arī atvērt, lai mainītu iepriekš saglabātu formulu. Lai piešķirtu kādu e-pasta adresi, noklikšķiniet uz **Rediģēt**, lai atvērtu dialoglodziņu **Piešķirt e-pasta adreses**.

[![E-pasta adrešu piešķiršana e-pasta galamērķim](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurācijas e-pasta ziņojums

Izmantojiet šo e-pasta ziņojuma tipu, ja izmantotajā konfigurācijā ir zars datu avotos, kuri apzīmē e-pasta adresi. Formulu veidotājā varat izmantot datu avotus un funkcijas, lai iegūtu pareizi formatētu e-pasta adresi.

[![E-pasta adreses datu avota piešķiršana e-pasta galamērķim](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Piezīme.** Ir jābūt konfigurētam un pieejamam vienkāršā pasta pārsūtīšanas protokola (SMTP) serverim. Savu SMTP serveri varat norādīt programmatūras Dynamics 365 for Finance and Operations sadaļā **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **E-pasts** &gt; **E-pasta parametri**.

### <a name="archive-destination"></a>Arhīva galamērķis

Šo opciju varat izmantot, lai izvadi sūtītu uz Microsoft SharePoint mapi vai Microsoft Azure krātuvi. Opciju **Iespējots** iestatiet uz **Jā**, lai izvadi sūtītu uz galamērķi, kas ir definēts ar atlasīto dokumentu tipu. Atlasei ir pieejami tikai tie dokumentu tipi, kur grupa ir iestatīta uz **Fails**. Dokumentu tipus ir jādefinē sadaļā **Organizācijas administrēšana** &gt; **Dokumentu pārvaldība** &gt; **Dokumentu tipi**. Konfigurēšana ER galamērķiem ir tāda pati kā konfigurēšana dokumentu pārvaldības sistēmai.

[![Lapa Dokumentu tipi](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Atrašanās vieta nosaka, kur fails tiek saglabāts. Kad ir iespējots galamērķis **Arhīvs**, konfigurācijas izpildes rezultātus var saglabāt darbu arhīvā. Rezultātus varat skatīt sadaļā **Organizācijas administrēšana** &gt; **Elektronisko pārskatu veidošana** &gt; **Elektronisko pārskatu arhivētie darbi**. **Piezīme.** Programmatūrā Dynamics 365 for Finance and Operations darbu arhīva dokumenta veidu var atlasīt sadaļā **Organizācijas administrēšana** &gt; **Darbvietas** &gt; **Elektronisko pārskatu veidošana** &gt; **Elektronisko pārskatu parametri**.

#### <a name="sharepoint"></a>SharePoint

Failu varat saglabāt norādītajā SharePoint mapē. Noklusējuma SharePoint serveri varat definēt sadaļā **Organizācijas administrēšana** &gt; **Dokumentu pārvaldība** &gt; **Dokumentu pārvaldības parametri**, cilnē **SharePoint**. Kad SharePoint mape ir konfigurēta, varat to atlasīt kā mapi, kur tiks saglabāta ER izvade šim dokumentu tipam. 

[![SharePoint mapes atlasīšana](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure krātuve

Kad dokumentu tipa atrašanās vieta ir iestatīta uz **Arhīva direktorijs**, varat failu saglabāt Azure krātuvē.

### <a name="file-destination"></a>Faila adresāts

Ja opciju **Iespējots** iestatāt uz **Jā**, tad pēc konfigurācijas izpildīšanas tiek parādīts atvēršanas vai saglabāšanas dialoglodziņš.

### <a name="screen-destination"></a>Ekrāna galamērķis

Ja opciju **Iespējots** iestatāt uz **Jā**, tad tiek izveidots izvades priekšskatījums. Noteiktu tipu failus, piemēram, XML, TXT vai PDF failus, varat skatīt tieši pārlūkprogrammas logā. Citu tipu failiem, piemēram, Microsoft Excel vai Word failiem, tiek izmantots pakalpojums Microsoft Office Online.

### <a name="power-bi-destination"></a>Power BI galamērķis

Iestatiet opcijas **Iespējots** vērtību **Jā**, lai izmantotu savu ER konfigurāciju datu pārsūtīšanai no savas programmatūras Dynamics 365 for Finance and Operations instances uz Microsoft Power BI pakalpojumiem. Pārsūtītie faili tiek glabāti Microsoft SharePoint Server instancē, kura ir jākonfigurē šim nolūkam. Papildinformāciju skatiet tēmā [Elektronisko pārskatu veidošanas konfigurācijas izmantošana, lai pakalpojumā Power BI nodrošinātu datus no programmatūras Dynamics 365 for Finance and Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Padoms.** Lai ignorētu noklusējuma uzvedību (t.i., dialoglodziņu kādai konfigurācijai), varat izveidot galamērķa atsauci un faila galamērķi galvenajam izvades komponentam un pēc tam atspējot visus galamērķus.

## <a name="security-considerations"></a>Drošības apsvērumi
ER galamērķiem tiek izmantoti divu tipu privilēģijas un pienākumi. Viens tips kontrolē spēju uzturēt vispārējos galamērķus, kas ir konfigurēti kādai juridiskajai personai (t.i., tas kontrolē piekļuvi lapai **Elektronisko pārskatu veidošanas adresāti**). Otrs tips kontrolē programmas lietotāja spēju izpildes laikā ignorēt galamērķu iestatījumus, ko konfigurēja ER izstrādātājs vai ER funkcionālais konsultants.

| Loma (AOT nosaukums)                     | Lomas nosaukums                                  | Pienākums (AOT nosaukums)                     | Pienākuma nosaukums                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroniskā pārskata izstrādātājs             | ERFormatDestinationConfigure        | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu                |
| ERFunctionalConsultant              | Elektronisko pārskatu veidošanas funkcionālais konsultants | ERFormatDestinationConfigure        | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu                |
| PaymAccountsPayablePaymentsClerk    | Kreditoriem maksājamo rēķinu darbinieks            | ERFormatDestinationRuntimeConfigure | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu izpildlaikā |
| PaymAccountsReceivablePaymentsClerk | Debitoru parādu maksājumu darbinieks         | ERFormatDestinationRuntimeConfigure | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu izpildlaikā |

**Piezīme.** Iepriekš uzskaitītajos pienākumos tiek izmantotas divas privilēģijas. Šo privilēģiju nosaukumi ir tādi paši kā tām atbilstošo pienākumu nosaukumi: **ERFormatDestinationConfigure** un **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Esmu importējis elektroniskas konfigurācijas un tās redzu lapā Elektronisko atskaišu veidošanas konfigurācijas. Bet kāpēc tās nav redzamas lapā Elektronisko pārskatu veidošanas galamērķi?

Noteikti noklikšķiniet uz lauka **Jauns** un pēc tam atlasiet konfigurāciju laukā **Atsauce**. Lapā **Elektronisko atskaišu galamērķi** varat redzēt tikai tās konfigurācijas, kam ir konfigurēti galamērķi.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Vai var kaut kā definēt, kuru Azure krātuves kontu un Azure Blob krātuvi lietot?

Nē. Tiek lietota noklusējuma Azure Blob krātuve, kas ir definēta un lietota dokumentu pārvaldības sistēmai.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Kādam nolūkam galamērķa iestatījumos tiek izmantots galamērķis Fails? Ko šis iestatījums dara?

Galamērķis **Fails** tiek izmantots, lai kontrolētu dialoglodziņu. Ja iespējojat šo galamērķi vai ja konfigurācijai nav definēts nekāds galamērķis, tad pēc izvades faila izveidošanas jums tiek rādīts atvēršanas vai saglabāšanas dialoglodziņš.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Vai varat sniegt piemēru formulai, kas atsaucas uz kreditora kontu, uz kuru es varu sūtīt e-pastu?

Šī formula ir atkarīga no ER konfigurācijas. Piemēram, ja lietojat konfigurāciju ISO 20022 kredīta pārskaitījums, varat lietot **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** vai **model.Payments.Creditor.Identification.SourceID**, lai iegūtu saistītu kreditora kontu.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Viena no manām formāta konfigurācijām ietver vairākus failus, kas ir grupēti vienā mapē (piemēram, mapē Mape1 ietilpst faili Fails1, Fails2 un Fails3). Kā iestatīt galamērķus tā, lai fails Mape1.zip netiktu izveidots vispār, Fails1 tiktu nosūtīts pa e-pastu, Fails2 tiktu nosūtīts uz SharePoint, bet failu Fails3 es varētu atvērt uzreiz pēc konfigurācijas izpildīšanas?

Priekšnosacījums ir tāds, ka jūsu formātam ir jābūt pieejamam ER konfigurācijās. Ja jums ir jūsu formāts, atveriet lapu **Elektronisko atskaišu galamērķi** un izveidojiet jaunu atsauci uz šo konfigurāciju. Pēc tam jums ir nepieciešami četri failu galamērķi — viens katram izvades komponentam. Izveidojiet pirmo failu galamērķi, piešķiriet tam nosaukumu, piemēram, **Mape**, un atlasiet faila nosaukumu, kas apzīmē kādu mapi jūsu konfigurācijā. Pēc tam noklikšķiniet uz **Iestatījumi** un pārliecinieties, ka visi galamērķi ir atspējoti. Šim failu galamērķim mape netiks izveidota. Pēc noklusējuma, tā kā starp failiem un pamata mapēm pastāv hierarhiskas atkarības, šie faili darbosies tādā pašā veidā. Citiem vārdiem sakot — tie netiks nekur sūtīti. Lai ignorētu šo noklusējuma uzvedību, jums ir jāizveido vēl trīs failu galamērķi — viens katram failam. Katram galamērķa iestatījumos jums ir jāiespējo tas galamērķis, uz kuru šis fails ir jānosūta.

# <a name="see-also"></a>Skatiet arī

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)




