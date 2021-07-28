---
title: Drukājamu FTI veidlapu ģenerēšana
description: Šajā tēmā ir paskaidrots, kā izmantot elektronisko pārskatu izveides (Electronic reporting — ER) struktūru, lai ģenerētu drukājamas brīva teksta rēķinu (free text invoice — FTI) formas Microsoft Office dokumentu formātā.
author: NickSelin
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: f5556195a1a787420061fbcaef5d97ac47823221
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359009"
---
# <a name="generate-printable-fti-forms"></a>Drukājamu FTI formu ģenerēšana

[!include[banner](../includes/banner.md)]

Elektronisko pārskatu izveides (ER) struktūra sniedz iespēju ģenerēt drukājamas brīva teksta rēķinu (FTI) formas Microsoft Office dokumentu formātā. Šajā tēmā ir sniegta informācija par to, kā veidot savas konfigurācijas, kā arī detalizēta informācija par pieejamajām konfigurācijas veidnēm.

## <a name="overview"></a>Pārskats

Papildus esošajai iespējai ģenerēt drukājamas FTI formas, izmantojot Microsoft SQL Server Reporting Services (SSRS), tagad varat izmantot arī ER struktūru. Varat pārvaldīt drukājamās FTI formas programmās Microsoft Office Excel un Word. Varat arī modificēt izkārtojumu, datu plūsmu un formatējumu, lai nodrošinātu atbilstību konkrētām prasībām, neveicot koda izmaiņas.

> [!NOTE]
> Ja vēlaties vispirms iepazīties ar pārskatu par esošajām drukājamo FTI veidlapu risinājuma parauga ER konfigurācijām, atveriet uzreiz sadaļu **ER konfigurāciju parauga lejupielāde, lai ģenerētu drukājamas FTI veidlapas**, kas pieejama tālāk šajā tēmā.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>FTI drukājamajām veidlapām paredzētu pielāgotu konfigurāciju izveide
Jums ir jāizveido ER konfigurāciju kopa kā daļa no pielāgotā drukājamo FTI veidlapu risinājuma.

### <a name="configure-the-er-data-model"></a>ER datu modeļa konfigurēšana
Jūsu programmā ir jābūt ER datu modeļa konfigurācijai ar datu modeli, kas apraksta debitoru rēķinu izrakstīšanas biznesa domēnu. Datu modeļa nosaukumam ir jābūt **CustomersInvoicing**. Informāciju par EP datu modeļu izveidi skatiet tēmā [EP domēnam specifiska datu modeļa izveide elektronisko pārskatu veidošanai (EP)](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>ER modeļa kartējuma konfigurēšana
Jūsu programmā ir jābūt ietvertam CustomersInvoicing datu modelim paredzētam ER modeļa kartējumam. Modeļa kartējums var būt ER datu modeļa konfigurācija vai ER modeļa kartējuma konfigurācija. Taču modeļa kartējuma saknes deskriptoram ir jābūt **FreeTextInvoice**.

Kartējumā ir jābūt tālāk norādītajiem datu avotiem.

- Datu avota tips: **Tabulas ieraksti**

    - Šī datu avota nosaukumam ir jābūt **CustInvoiceJour**.
    - Tam ir jāattiecas uz programmas tabulu CustInvoiceJour.
    - Tas tiek izmantots izpildlaikā, lai drukāšanai atlasīto rēķinu sarakstu no programmas nodotu ER modeļa kartējumam.

- Datu avota tips: **Objekts**

    - Šī datu avota nosaukumam ir jābūt **PrintMgmtPrintSettingDetail**.
    - Tam ir jāattiecas uz programmas klasi **PrintMgmtPrintSettingDetail**.
    - Tas tiek izmantots izpildlaikā, lai palaistā ER formāta drukas pārvaldības iestatījumu informāciju no programmas nodotu ER modeļa kartējumam.

Detalizēta informācija par programmas integrāciju ar ER platformu ir pieejama programmas pirmkoda klasē **ERPrintMgmtReportFormatSubscriber** (ER programmu komplekta integrācijas modelis).

Papildinformāciju par ERPmodeļu kartējumu izveidi skatiet tēmā [EP modeļa kartējumu definēšana un datu avotu atlase tiem](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>ER formāta konfigurēšana
Programmas instancē ir jābūt ER formāta konfigurācijai, kas tiks izmantota FTI veidlapu ģenerēšanai. 

> [!NOTE]
> Šī formāta konfigurācija ir jāizveido datu modelim CustomersInvoicing, un tai ir jāizmanto modeļa kartējums ar saknes deskriptoru **FreeTextInvoice**.

Informāciju par EP formātu konfigurēšanu skatiet tēmā [EP Formāta konfigurācijas izveide elektronisko pārskatu veidošanai (2016. gada novembris)](tasks/er-format-configuration-2016-11.md). Informāciju par ER formātu izveidi pārskatu ģenerēšanai OpenXML formātā skatiet tēmā [ER Konfigurācijas izveide pārskatu ģenerēšanai OPENXML formātā elektronisko pārskatu veidošanai](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Drukas pārvaldības konfigurēšana
Lai ģenerētu FTI veidlapas, izmantojot ER platformu, ER formātus varat piešķirt tādā pašā veidā, kādā piešķirat SSRS pārskatus. Lai ER formātu saistītu ar visiem debitoru parādu FTI rēķiniem, atveriet sadaļas **Debitoru parādi** \> **Iestatīšana** \> **Veidlapas** \> **Veidlapu iestatīšana** \> **Vispārīgi** \> **Drukas pārvaldība** \> **Brīva teksta rēķins** \> **Sākotnējie**. Lai ER formātu saistītu ar konkrētu debitoru vai rēķinu, veiciet tālāk norādītās darbības.

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Atlasiet ar ER formātu saistāmo FTI un atveriet lapu **Drukas pārvaldības iestatīšana**.
3. Atlasiet dokumenta līmenī, lai apstrādei norādītu rēķinu tvērumu.
4. Atlasiet norādītā dokumenta līmeņa ER formātu.

![Drukāšanas parametru iestatīšana.](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Atlasītā formāta laukā **Pārskata formāta uzmeklēšana** tiek parādīti tikai tie ER formāti, kas izmanto datu modeļa **CustomersInvoicing** saknes deskriptoru **FreeTextInvoice**.

## <a name="generate-fti-forms"></a>FTI veidlapu ģenerēšana
FTI veidlapas ER platformā tiek ģenerētas tādā pašā veidā, kādā tiek ģenerēti SSRS pārskati.

Lai ģenerētu FTI veidlapas, rēķinus varat atlasīt pēc diapazona vai atlases. 

![Rēķina atlase.](media/FTIbyGER-InvoiceSelection.png)

![Rēķina priekšskatījums.](media/FTIbyGER-InvoiceExcelPreview.png)

Kad ER formātus izmanto, lai šādā veidā drukātu FTI veidlapas, tiek lietoti noklusējuma ER failu galamērķi. Galamērķi nevar mainīt. Papildinformāciju par EP formātu EP galamērķu konfigurēšanu skatiet tēmā [Elektronisko pārskatu (EP) galamērķi](electronic-reporting-destinations.md).

FTI veidlapas varat arī ģenerēt, kad grāmatojat FTI, ieslēdzot iestatījumu **Drukāt rēķinu** un izslēdzot iestatījumu **Izmantot drukas pārvaldības galamērķus**.

> [!NOTE]
> Kad ER formātus izmanto, lai šādā veidā drukātu FTI veidlapas, tiek lietoti noklusējuma ER failu galamērķi. Ja galamērķis jau ir konfigurēts, noklusējuma galamērķi var mainīt izpildlaikā. Lai mainītu galamērķi, ir nepieciešama tālāk norādītā drošības privilēģija.
>
> - **Nosaukums:** ERFormatDestinationRuntimeMaintain
> - **Etiķete:** Uzturēt elektronisko pārskatu veidošanas formāta galamērķi izpildlaikā

![Elektroniskās pārskatu veidošanas adresāts.](media/FTIbyGER-ERFileDestinationSetting.png)

![Elektronisko pārskatu veidošanas formāta galamērķis.](media/FTIbyGER-ERFileDestinationUsage.png)

ER platforma ģenerētajiem dokumentiem pašlaik atbalsta tālāk norādītos galamērķus.

- **Lejupielādētais fails** — ģenerētās veidlapas tiek piedāvātas kā lejupielādes, ko var saglabāt, izmantojot pārlūkprogrammu.
- **Ekrāns** — Microsoft 365 programma Excel tiek izmantota ģenerēto FTI veidlapu priekšskatīšanai Excel formātā.
- **SharePoint mape** — ģenerētās formas tiek saglabātas atbilstoši dokumentu pārvaldības struktūras iestatījumiem.
- **Lietojumprogrammas arhīvs** — ģenerētās formas tiek glabātas kā izpildes žurnāla ierakstu pielikumi Microsoft Azure krātuvē.
- **E-pasts** — ģenerētās veidlapas tiek nosūtītas kā e-pasta pielikumi.

> [!NOTE]
> Ģenerētās FTI veidlapas nevar nosūtīt tieši uz printeri, jo pašlaik netiek atbalstīta tiešā drukāšana, kas izmanto Dynamics printera maršrutēšanas aģentu.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>ER konfigurāciju parauga lejupielāde, lai ģenerētu drukājamas FTI veidlapas
Varat lejupielādēt ER konfigurāciju paraugu, lai to izmantotu kā FTI risinājuma veidni. Konfigurācijas tiek glabātas Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Tālāk norādītas ietvertās konfigurācijas.

- Konfigurācijā **Debitora rēķinu izrakstīšanas modelis** ir ietverts nepieciešamais datu modelis un modeļa kartējums.
- Konfigurācijā **Debitora FTI pārskats (GER)** ir ietverts formāta paraugs.

> [!NOTE]
> Šīs konfigurācijas ir izveidotas kā paraugi, lai izskaidrotu iespējamos scenārijus. Šo konfigurāciju turpmākais izmantojums ir atkarīgs no šī novērtējuma rezultātiem un jebkādām saņemtajām atsauksmēm.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>ER formāta paraugā ieviestie līdzekļi
ER formāta konfigurācijas paraugā Excel fails tiek izmantots kā veidne FTI veidlapu ģenerēšanai.

![Veidotāja formāts.](media/FTIbyGER-ERFormat.png)

Pašlaik šis ER formāta paraugs FTI veidlapu ģenerēšanai atbalsta tālāk norādītos līdzekļus.

- FTI veidlapas tiek ģenerētas gan sākotnējiem rēķiniem, kas ir grāmatoti, gan sākotnējiem rēķiniem, kas vēl nav grāmatoti. Labotie rēķini un kredīta notas netiek atbalstīti.
- FTI veidlapas tiek ģenerētas rēķina valodā. Ģenerētajās veidlapās ietverto vērtību un datumu formāta pamatā ir lietotāja klienta lokalizācijas iestatījumi.
- Ja netiek apstrādāta neviena rēķinu rinda, ģenerētajos rēķinos tiek parādīti datu nepieejamības paziņojumi.
- Ģenerēto rēķinu galveņu pamatā ir lapā **Debitoru parādu parametri** FTI veidlapai atlasītais papīra formāts. Uzņēmuma informācija ģenerētās rēķina veidlapas galvenē tiek parādīta tikai tad, ja papīra formāts ir tukšs.
- Ja lapā **Debitoru parādu parametri** FTI veidlapai ir atlasīta atbilstošā opcija, ģenerētajās rēķinu veidlapās tiek parādīti uzņēmumu un debitoru PVN reģistrācijas numuri.
- Ģenerētā rēķina rindās un rēķina kopsummu sadaļās rēķina reģistrācijas valūtā tiek parādīta rēķina noklusējuma naudas informācija.
- Ja lapā **Debitoru parādu parametri** ir iespējota opcija **Drukāt summu eiro atspoguļojošā valūtā**, ģenerētā rēķina kopsummu sadaļā naudas informācija var tikt parādīta eiro valūtā un rēķina reģistrācijas valūtā.
- Atbilstoši lapā **Debitoru parādu parametri** veiktajiem iestatījumiem ģenerētajās rēķina veidlapās tiek parādītas visas pieejamās rēķinu apstrādes piezīmes. Piezīmes tiek ietvertas gan visam rēķinam, gan katrai rēķina rindai.
- Ģenerētajās rēķina veidlapās tiek ietvertas debitora FTI veidlapai paredzētas piezīmes un rēķina apstrādes valoda, ja tās ir konfigurētas AR veidlapu piezīmju sarakstā.
- Atkarībā no drukas pārvaldības iestatījumiem ģenerētajos rēķinos ir ietverts kājenes teksts, ja tas ir konfigurēts rēķina valodai, ER formāts un FTI dokumenta tvērums.
- Ģenerēto rēķinu veidlapu kopsummu sadaļā tiek ietverta visa pieejamā termiņatlaides informācija.
- Ģenerēto rēķinu veidlapu maksājumu grafiku sadaļā tiek ietverta visa pieejamā maksājumu grafiku informācija.
- Ģenerēto rēķinu veidlapu uzcenojumu sadaļā tiek ietvertas visas pieejamās maksu transakcijas.
- Ģenerētajās rēķinu veidlapās atbilstoši lapā **Debitoru parādu parametri** veiktajam iestatījumam **PVN specifikācija** tiek ietverta PVN informācija. Šajā sadaļā nodokļu informācija var tikt parādīta tikai rēķina reģistrācijas valūtā vai arī gan rēķina reģistrācijas valūtā, gan uzņēmuma uzskaites valūtā.
- Ģenerētajās rēķinu veidlapās tiek parādīta tiešā debeta paziņojuma informācija. Piemēram, tajās tiek parādīts, kad rēķinam tika atlasīta maksāšanas metode ar obligāto tiešā debeta pilnvarojuma ID, kad apstrādātajam rēķinam tika reģistrēta eiro valūta un kad rēķinam tika definēts tiešā debeta pilnvarojuma ID.
- Ģenerētajos rēķinos tiek parādīta visa grāmatotajiem rēķiniem pieejamā priekšapmaksas informācija.
- Ģenerētās rēķinu veidlapas rēķina debitoriem var nosūtīt kā e-pasta pielikumus. Izmantotajam ER formātam ir jābūt konfigurētam atbilstošajam ER failu galamērķim.

### <a name="countryregion-specific-features"></a>Iespējas atbilstoši valstij/reģionam 
ER formāta paraugā ir ietvertas tālāk norādītās iespējas atbilstoši valstij/reģionam, lai parādītu, kā ER konfigurācijās var ievērot noteiktas prasības.

#### <a name="norway"></a>Norvēģija
Ja rēķins tiek apstrādāts juridiskajai personai, kas ir konfigurēta tālāk norādītajā veidā, ģenerētās rēķina veidlapas galvenē tiek ietverts uzņēmuma reģistrēšanas nosacījums.

- Tiek izmantots Norvēģijas valsts/reģiona konteksts.
- Pārdošanas dokumentos ir aktīvs parametrs **Drukāt Foretaksregisteret**.

#### <a name="spain"></a>Spānija
Ja rēķins tiek apstrādāts juridiskajai personai, kas ir konfigurēta tālāk norādītajā veidā, ģenerētās rēķina veidlapas galvenē tiek ietverts nosacījums **Skaidras naudas uzskaites metodes īpašais režīms**.

- Tiek izmantots Spānijas valsts/reģiona konteksts.
- Rēķina apstrādes datumam tiek iespējots skaidras naudas uzskaites metodes īpašais režīms.

Ja ģenerētā rēķina veidlapa ir apstrādāta juridiskajai personai, kas ir konfigurēta tālāk norādītajā veidā, un ir pieejama tāda termiņatlaides informācija kā termiņatlaides summa un rēķina rindas neto summa, šī informācija tiek norādīta ģenerētās rēķina veidlapas kopsummu sadaļā.

- Tiek izmantots Spānijas valsts/reģiona konteksts.
- Rēķina opcijai tiek ieslēgts iestatījums **Termiņatlaide attiecas uz rēķinu** (**Virsgrāmatas parametri** \> **PVN sadaļa**).

#### <a name="italy"></a>Itālija
Ja ģenerētais rēķins tiek apstrādāts juridiskajai personai, kas ir konfigurēta, izmantojot Itālijas valsts/reģiona kontekstu, rēķina rindā tiek ietverta preču atlaides atzīme.

#### <a name="finland"></a>Somija
Papildus ģenerētajai rēķina veidlapai var tikt ģenerētas žiro naudas pārsūtīšanas kvītis, kā norādīts tālāk.

- Juridiskajai personai, kura izmanto Somijas valsts/reģiona kontekstu un kam ir vismaz viens bankas konts, kas ir atzīmēts kā **Žiro konts** un **Banku svītrkods**. 
- Rēķinam, kas ir atzīmēts kā nepieciešams **Somu** saistītajam maksājuma pielikumam.

![Žiro kvīts.](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> ER formāta paraugs ir konfigurēts tā, lai žiro naudas pārsūtīšanas kvītis pēc izvēles varētu ģenerēt atsevišķā darblapā.

> [!NOTE]
> Vispirms ir jāinstalē fonts, ko izmantot, lai svītrkodu ģenerētu lokālajā datorā, kurā ģenerētā rēķina veidlapa tiks priekšskatīta Excel formātā.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>ER formāta parauga izmantošana e-pasta galamērķu konfigurēšanai
Lai konfigurētu e-pasta galamērķus, izmantojiet tālāk norādītos ER formāta parauga elementus.

- Debitora kontaktpersonas e-pasta adresei var piekļūt, izmantojot šādu ER izteiksmi: **model.InvoiceBase.Contact.ElectronicMail**.
- E-pasta ziņojuma tēmas tekstam var piekļūt, izmantojot šādu ER izteiksmi: **Emailing.TxtToUse.Subject**.
- E-pasta ziņojuma pamattekstam var piekļūt, izmantojot šādu ER izteiksmi: **Emailing.TxtToUse.Body**.

![Adresāta iestatījumi.](media/FTIbyGER-ERFileDestinationSettingEmail.png)

E-pasta ziņojuma noklusējuma tēmas teksts un pamatteksts ir definēts ER formāta paraugā. Valoda ir atkarīga no formāta etiķetēm. Šis noklusējuma teksts e-pasta ziņojumos tiks izmantots, ja nebūs pievienota pielāgotā organizācijas e-pasta ziņojumu veidne, kurai ir iepriekš definētais **ERFTITMP** ID.

> [!NOTE]
> **ERFTITMP** e-pasta veidnes ID ir definēts ER formāta paraugā. To var pēc nepieciešamības mainīt uz jaunu ER formātu, kas ir izveidots no šī formāta parauga.

Ja organizācijas e-pasta veidne, kam ir iepriekš definētais **ERFTITMP** ID, ir pievienota juridiskajai personai, kuras rēķinu apstrādājat, e-pasta ziņojuma ģenerēšanai tiks izmantota e-pasta ziņojuma tēmas un pamatteksta veidne. 

![Organizācijas e-pasta ziņojumu veidnes.](media/FTIbyGER-EmailTemplate.png)

![Augšupielādēt e-pasta veidni.](media/FTIbyGER-EmailTemplateBody.png)

ER formāta parauga ER izteiksme **Emailing.TxtToUse.Subject** ir konfigurēta tā, lai visas viettura %1 instances aizstātu ar apstrādes rēķina ID.

Formāta parauga izteiksme **Emailing.TxtToUse.Body** ir konfigurēta tālāk norādītajiem vietturu aizstāšanas gadījumiem.

- Vietturis "%1" tiek aizstāts ar debitora kontaktpersonas vārdu.
- Vietturis "%2" tiek aizstāts ar uzņēmuma nosaukumu.
- Vietturis "%3" tiek aizstāts ar debitora nosaukumu/vārdu.
- Vietturis "%4" tiek aizstāts ar uzņēmuma kontaktpersonas vārdu.
- Vietturis "%5" tiek aizstāts ar uzņēmuma kontaktpersonas amata nosaukumu.
- Vietturis "%6" tiek aizstāts ar uzņēmuma kontaktpersonas e-pasta adresi.

![E-pasts.](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Papildu resursi
[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]