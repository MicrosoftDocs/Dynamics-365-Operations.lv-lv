---
title: Elektroniskās pārskatu veidošanas (ER) adresāti
description: Šajā rakstā ir sniegta informācija par elektronisko pārskatu adresātu pārvaldību, atbalstīto adresātu veidiem un drošības apsvērumiem.
author: kfend
ms.date: 08/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: DocuType, ERSolutionTable
ms.openlocfilehash: b1bf6289e80769dfe8858f307cbb9b217b42dbb4
ms.sourcegitcommit: f2edc193003564c5bee1747f9c2b800feee342bd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/29/2022
ms.locfileid: "9360984"
---
# <a name="electronic-reporting-er-destinations"></a>Elektroniskās pārskatu veidošanas (ER) adresāti

[!include [banner](../includes/banner.md)]

Varat konfigurēt adresātu katrai elektronisko atskaišu (Electronic Reporting — ER) formāta konfigurācijai un tā izvades komponentu (mapi vai failu). Lietotāji, kuriem ir atbilstošas piekļuves tiesības, mērķa iestatījumus var modificēt arī izpildlaikā. Šajā rakstā ir paskaidrota ER galamērķu pārvaldība, atbalstītie galamērķu tipi un drošības apsvērumi.

ER formāta konfigurācijas parasti satur vismaz vienu izvades komponentu: failu. Parasti konfigurācijas ietver vairākus dažādu tipu failu izvades komponentus (piemēram, XML, TXT XLSX, DOCX vai PDF), kuri ir grupēti vienā mapē vai vairākās mapēs. ER galamērķu pārvaldība jums ļauj sākotnēji konfigurēt, kas notiek, kad tiek palaists katrs komponents. Pēc noklusējuma, kad tiek palaista kāda konfigurācija, tiek parādīts dialoglodziņš, ko varat izmantot, lai failu saglabātu vai atvērtu. Tāda pati uzvedība parādās arī tad, kad importējat kādu ER konfigurāciju un neesat tai konfigurējis nekādu noteiktu galamērķi. Kad galvenajam izvades komponentam ir izveidots galamērķis, šis galamērķis ignorē noklusējuma uzvedību un mape vai fails tiek nosūtīti saskaņā ar galamērķa iestatījumiem.

## <a name="availability-and-general-prerequisites"></a>Pieejamības un vispārīgie priekšnosacījumi

Versijā Microsoft Dynamics AX 7.0 (2016. gada februāris) ER galamērķu funkcionalitāte nav pieejama. Tāpēc jāinstalējiet versiju Microsoft Dynamics 365 for Operations 1611 (2016. gada novembris) vai jaunāku, lai izmantotu tālāk norādītos galamērķu tipus:

- [E-pasta adrese](er-destination-type-email.md)
- [Arhivēt](er-destination-type-archive.md)
- [Fails](er-destination-type-file.md)
- [Ekrāns](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Ja vēlaties, varat instalēt vienu no tālāk norādītajiem priekšnosacījumiem. Taču ņemiet vērā, ka šīs alternatīvas sniedz ierobežotāku ER galamērķa funkcionalitāti.

- Lietojumprogrammas Microsoft Dynamics AX versija 7.0.1 (2016. gada maijs)
- [Elektroniskās ziņošanas galamērķa pārvaldības programmas labojumfails](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Iekļauts arī [Drukāšanas](er-destination-type-print.md) adresāta tips. Lai to izmantotu, ir jāinstalē Microsoft Dynamics 365 Finanšu versija 10.0.9 (2020. gada aprīlis).

## <a name="overview"></a>Pārskats

Varat iestatīt galamērķus tikai ER konfigurācijām, kas ir [importētas](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) pašreizējā finanšu instancē, un formātiem, kas ir pieejami lapā **Elektronisko atskaišu veidošanas konfigurācijas**. ER galamērķa pārvaldības funkcionalitāte ir pieejama sadaļā **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu galamērķis**.

### <a name="default-behavior"></a>Noklusētā uzvedība

ER formāta konfigurācijas noklusētā uzvedība ir atkarīga no norādītā izpildes veida, kad tiek sākts ER formāts.

Ja dialoglodziņā **Intrastat pārskats** kopsavilkuma cilnē **Palaist fonā** iestatāt **Partijas apstrāde** opciju uz **Nē**, ER formāts nekavējoties tiek palaists interaktīvā režīmā. Kad šī izpilde ir veiksmīgi pabeigta, lejupielādei ir pieejams ģenerēts izejošais dokuments.

Iestatot opciju **Partijas apstrāde** uz **Jā**, ER formāts tiek palaists [partijas](../sysadmin/batch-processing-overview.md) režīmā. Tiek izveidots atbilstošais pakešuzdevums, pamatojoties uz parametriem, ko norādāt cilnē **Palaist fonā** dialoglodziņā **ER parametri**.

> [!NOTE]
> Darba apraksts tiek uzsākts, lai informētu par ER formāta kartēšanas izpildi. Tajā ir ietvertas arī izpildīto ER komponentu nosaukums.

[![Palaist ER formātu.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Informāciju par šo darbu varat atrast vairākās vietās:

- Dodieties uz **Kopīgi** \> **Vaicājumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**, lai pārbaudītu ieplānotā darba statusu.
- Dodieties uz **Uzņēmuma administrēšana** \> **Elektronisko pārskatu izveide** \> **Elektronisko pārskatu izveides darbi**, lai pārbaudītu plānotā darba statusu un pabeigtā darba izpildes rezultātus. Kad darba izpilde ir sekmīgi pabeigta, atlasiet **Rādīt failus** lapā **Elektronisko pārskatu izveides darbi**, lai iegūtu izveidoto izejošo dokumentu.

    > [!NOTE]
    > Šis dokuments tiek saglabāts kā pašreizējā darba ieraksta pielikums un to kontrolē [Dokumentu pārvaldības](../../fin-ops/organization-administration/configure-document-management.md) struktūra. [Dokumenta veids](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), kas tiek izmantots, lai uzglabātu šī veida ER artefaktus, ir konfigurēts [ER parametros](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- Lapā **Elektronisko pārskatu izveides darbi** atlasiet **Rādīt failus**, lai skatītu visu to kļūdu un brīdinājumu sarakstu, kas tika izveidoti darba izpildes laikā.

    [![Pārskatīt ER darbu sarakstu.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Lietotāja konfigurēta uzvedība

Lapā **Elektronisko pārskatu galamērķis** varat ignorēt konfigurācijas noklusējuma uzvedību. Importētās konfigurācijas šajā lapā tiek rādītas tikai pēc tam, kad atlasāt **Jauns** un laukā **Atsauce** atlasāt konfigurāciju, kurai izveidot galamērķa iestatījumus.

[![Konfigurācijas atlasīšana laukā Atsauce.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Kad esat izveidojis atsauci, varat izveidot faila galamērķi katram atsaucē minētā ER formāta **Mapes** vai **Faila** izvades komponentam.

[![Faili galamērķa izveidošana.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Pēc tam dialoglodziņā **Galamērķa iestatījumi** faila galamērķim varat iespējot un atspējot atsevišķus galamērķus. Poga **Iestatījumi** tiek izmantota, lai kontrolētu visus galamērķus atlasītajam failu galamērķim. Dialoglodziņā **Galamērķa iestatījumi** varat kontrolēt katru galamērķi atsevišķi, iestatot tam opciju **Iespējots**.

Finance versijās **pirms versijas 10.0.9** varat izveidot **viena faila galamērķi** katram izvades komponentam ar tādu pašu formātu, piemēram, mapi vai failu, kas ir atlasīts laukā **Faila nosaukums**. Tomēr **10.0.9 un jaunākā versijā** varat izveidot **vairākus failu galamērķus** katram tā paša formāta izvades komponentam.

Piemēram, varat izmantot šo iespēju, lai konfigurētu faila galamērķus faila komponentam, kas tiek izmantots izejošā dokumenta ģenerēšanai Excel formātā. Vienu galamērķi ([Arhīvs](er-destination-type-archive.md)) var konfigurēt, lai uzglabātu oriģinālo Excel failu ER darbu arhīvā, un citu galamērķi ([E-pastu](er-destination-type-email.md)) var konfigurēt, lai vienlaikus [konvertētu](#OutputConversionToPDF) Excel failu PDF formātā un nosūtītu PDF failu pa e-pastu.

[![Vairāku galamērķu konfigurēšana viena formāta elementam.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Kad jūs darbināt ER formātu, vienmēr tiek palaisti visi adresāti, kas tika konfigurēti formāta komponentiem. Turklāt finanšu versijā **10.0.17 un vēlāk** ER mērķa funkcionalitāte ir uzlabota un tagad ļauj konfigurēt dažādas adresātu kopas vienam ER formātam. Šī konfigurācija atzīmē katru kopu kā konfigurētu konkrētai lietotāja darbībai. ER API ir [paplašināts](er-apis-app10-0-17.md), lai var nodrošināt darbību, ko lietotājs veic, izpildot ER formātu. Nodrošinātais darbības kods tiek nodots ER adresātiem. Atkarībā no nodrošinātā darbības koda varat palaist dažādus ER formāta adresātus. Papildinformāciju skatiet sadaļā [No darbības atkarīgu ER adresātu konfigurēšana](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Galamērķu tipi

ER formātiem pašlaik tiek atbalstīti tālāk norādītie galamērķi. Visus tipus varat atspējot vai iespējot vienlaicīgi. Tādējādi jūs varat nedarīt neko vai sūtīt komponentu uz visiem konfigurētajiem galamērķiem.

- [E-pasta adrese](er-destination-type-email.md)
- [Arhivēt](er-destination-type-archive.md)
- [Fails](er-destination-type-file.md)
- [Ekrāns](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Drukāšana](er-destination-type-print.md)

## <a name="applicability"></a>Piemērojamība

Varat iestatīt galamērķus tikai ER konfigurācijām, kas ir importētas, un formātiem, kas ir pieejami lapā **Elektronisko atskaišu veidošanas konfigurācijas**.

> [!NOTE]
> Konfigurētie galamērķi ir raksturīgi uzņēmumam. Ja plānojat izmantot ER formāta līdzekļus dažādos pašreizējās Finance instances uzņēmumos, jākonfigurē mērķi šim ER formātam katram no šiem uzņēmumiem.

Konfigurējot failu galamērķus atlasītajam formātam, konfigurējiet tos visam formātam.

[![Konfigurācijas saite.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Tajā pašā laikā, iespējams, ir vairākas tā formāta versijas, kas importētas pašreizējā Finance instancē. Tos var apskatīt, atlasot saiti **Konfigurācija**, kas tiek piedāvāta, atlasot lauku **Atsauce**.

[![Konfigurācijas versijas.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Pēc noklusējuma konfigurētie galamērķi tiek piemēroti tikai tad, kad palaižat ER formāta versiju ar statusu **Pabeigts** vai **Koplietots**. Tomēr dažreiz konfigurētie galamērķi jāizmanto, kad tiek palaista ER formāta melnraksta versija. Piemēram, jūs modificējiet sava formāta melnraksta versiju un vēlaties izmantot konfigurētos galamērķus, lai pārbaudītu, kā tiek piegādāta ģenerētā izvade. Izpildiet tālāk norādītās darbības, lai pielietotu ER formāta galamērķus, kad tiek palaista melnraksta versija.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Iestatiet opciju **Izmantot galamērķus melnraksta statusam** uz **Jā**.

[![Opcija Izmantot galamērķus melnraksta statusam.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Lai izmantotu ER formāta melnraksta versiju, jums attiecīgi jāatzīmē ER formāts.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Atlasiet opcijai **Palaist iestatījumu** iestatījumu **Jā**.

[![Palaist iestatījuma opciju.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Pēc šīs iestatīšanas pabeigšanas opcija **Palaist melnrakstu** kļūst pieejama ER formātiem, ko jūs modificējat. Iestatiet šo opciju kā **Jā**, lai sāktu izmantot formāta melnraksta versiju, kad tiek palaists formāts.

[![Palaist melnraksta opciju.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Galamērķa kļūmes apstrāde

Parasti ER formāts tiek palaists noteiktā biznesa procesa tvērumā. Tomēr, tāda izejoša dokumenta nosūtīšana, kas tiek radīts ER formāta izpildes laikā, dažreiz ir jāuzskata par šī biznesa procesa daļu. Šādā gadījumā, ja ģenerētā izejošā dokumenta nosūtīšana uz konfigurēto galamērķi ir neveiksmīga, biznesa procesa izpilde jāatceļ. Lai konfigurētu atbilstošo ER galamērķi, atlasiet opciju **Pārtraukt apstrādi kļūmes gadījumā**.

Piemēram, jūs konfigurējiet kreditora maksājumu apstrādi tā, lai tiktu palaists **ISO20022 pārvietošana kredītā** ER formāts, lai ģenerētu maksājuma failu un papildu dokumentus (piemēram, pavadvēstuli un kontroles pārskatu). Ja maksājums ir jāuzskata par sekmīgu apstrādātu tikai tad, ja pavadvēstule tiek veiksmīgi piegādāta pa e-pastu, jāatlasa izvēles rūtiņa **Pārtraukt apstrādi kļūmes gadījumā** komponentam **Pavadvēstule** atbilstošajā faila galamērķī, kā parādīts tālak redzamajā ilustrācijā. Šādā gadījumā pārstrādei atlasītais maksājuma statuss tiks mainīts no **Neviens** uz **Nosūtīts** tikai tad, kad ģenerētā pavadvēstule tiek veiksmīgi pieņemta nosūtīšanai ar e-pasta pakalpojumu sniedzēju, kas konfigurēts Finance instancē.

[![Procesa apstrādes konfigurēšana faila galamērķa kļūmei.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Notīrot izvēles rūtiņu **Pārtraukt apstrādi kļūmes gadījumā** galamērķa komponentam **Pavadvēstule**, maksājums tiks uzskatīts par sekmīgu apstrādātu arī tad, ja pavadvēstule nav veiksmīgi piegādāta pa e-pastu. Maksājuma statuss tiks mainīts no **Nav** uz **Nosūtīts** pat tad, ja pavadvēstuli nevar nosūtīt, jo, piemēram, trūkst adresāta vai sūtītāja e-pasta adreses vai tā nav pareiza.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Izvades pārveide PDF formātā

Varat izmantot PDF pārveides opciju, lai pārveidotu izvadi no Microsoft Office formāta (Excel/Word) PDF formātā.

### <a name="make-pdf-conversion-available"></a>PDF pārveides pieejamības nodrošināšana

Lai PDF pārveides opciju padarītu pieejamu pašreizējā Finance instancē, atveriet darbvietu **Līdzekļu pārvaldība** un ieslēdziet līdzekli **Pārveidot elektronisko pārskatu izejošos dokumentus no Microsoft Office formātiem PDF formātā**.

[![Līdzekļa Izejošo dokumentu pārveide PDF formātā ieslēgšana līdzekļu pārvaldībā.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Piemērojamība

Programmas Finance versijās **pirms versijas 10.0.18** šo opciju var ieslēgt tikai **Excel\\Faila** tipa komponentiem, kas tiek izmantoti, lai ģenerētu izvadi Office Excel vai Word formātā. Kad šī opcija ir ieslēgta, izvade, kas tiek ģenerēta Office formātā, tiek automātiski pārveidota PDF formātā. Taču versijā **10.0.18 un jaunākā versijā** šo opciju var ieslēgt arī **kopējā\\failu** tipa komponentiem.

> [!NOTE]
> Jāpievērš uzmanība brīdinājuma ziņojumam, ko saņemat, ieslēdzot PDF pārveides opciju **kopējā\\failu** tipa ER komponentam. Šis ziņojums informē, ka izstrādes laikā nav veida, kā nodrošināt, lai atlasītais faila komponents izpildlaikā atklāj saturu PDF formātā vai PDF konvertējamu saturu. Tāpēc opciju vajadzētu ieslēgt tikai tad, ja esat pārliecināts, ka atlasītais faila komponents ir konfigurēts, lai izpildlaikā rādītu saturu PDF formātā vai PDF konvertējamu saturu.
> 
> Ja formāta komponentam ieslēdzat PDF pārveides opciju, ja šis komponents atklāj saturu formātā, kas nav PDF, un ja atklāto saturu nevar pārvērst PDF formātā, izpildlaikā parādās izņēmums. Saņemtais ziņojums informē, ka ģenerēto saturu nevar pārveidot PDF formātā.

### <a name="limitations"></a>Ierobežojumi

Finanšu versijas 10.0.9 **PDF** pārvēršanas opcija ir pieejama tikai mākoņa izvietošanai. Sākot ar finanšu versiju **10.0.27**, PDF pārvēršanas opcija ir pieejama jebkurai lokālai izvietošanai, kam ir [iespējota interneta savienojamība](../user-interface/client-disconnected.md).

Saražotais PDF dokuments ir ierobežots līdz maksimālam 300 lapu skaitam.

Finanšu versijas 10.0.9 **PDF** dokumentā, kas veidots no Excel izvades, tiek atbalstīta tikai ainavorientācija. Sākot no finanšu **versijas 10.0.10**, varat [norādīt](#SelectPdfPageOrientation) lapas orientāciju PDF dokumentam, kas tiek iegūts no Excel izvades, kamēr konfigurējat ER adresātu.

Lai pārveidotu izvadi, kas nesatur iegultus fontus, tiek izmantoti tikai Window operētājsistēmas bieži sastopamie sistēmas fonti.

### <a name="resources"></a>Resursi

Pirms finanšu versijas 10.0.29 PDF pārvēršanu var veikt tikai ārpus pašreizējās finanšu instances. Ģenerētais fails no Finanšu tika nosūtīts uz konversijas pakalpojumu, un šis pakalpojums pēc tam atgrieza konvertēto dokumentu. **Tomēr versijā 10.0.29** **Microsoft Office un jaunākās versijās papildus elektronisko pārskatu nosūtīšanas dokumentiem no formātiem uz PDF funkciju var iespējot Lietojuma programmas resursus,** lai veiktu CBD **dokumentu konversiju no Word uz PDF** formāta līdzekli. Šis līdzeklis ļauj jums konvertēt ģenerētos Word dokumentus PDF formātā lokāli, izmantojot programmas servera resursus pašreizējā Finanšu instancē. 

Šeit ir vietējā PDF pārveidošanas iespēja, **kad tiek aktivizēti lietojuma programmas resursi, lai veiktu CBD dokumentu pārveidošanu no Word uz** PDF formāta funkciju:

- Saražotais PDF dokuments nav ierobežots [ar](#limitations) maksimālo lapu skaitu.
- Konvertētais Word dokuments var saturēt lielu [satura vadīklu skaitu](https://fix.lcs.dynamics.com/Issue/Details?bugId=647877&dbType=3).
- Lokālajā izvietošanā nav nepieciešams savienojums ar internetu.

### <a name="use-the-pdf-conversion-option"></a>Opcijas pārveidei PDF formātā izmantošana

Lai ieslēgtu faila galamērķa pārveidi PDF formātā, atzīmējiet izvēles rūtiņu **Pārveidot PDF formātā**.

[![Pārveides PDF formātā ieslēgšana faila galamērķim.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Lappuses orientācijas atlasīšana konvertēšanai PDF formātā</a>

Ja Excel formātā ģenerējat ER konfigurāciju un vēlaties to konvertēt PDF formātā, varat norādīt PDF faila lappuses orientāciju. Ja atzīmējat izvēles rūtiņu **Konvertēt PDF formātā**, lai ieslēgtu PDF konvertēšanu faila galamērķim, kas ģenerē izvades failu Excel formātā, lauks **Lappuses orientācija** kļūst pieejams kopsavilkuma cilnē **PDF konvertēšanas iestatījumi**. Laukā **Lapas orientācija** var atlasīt vēlamo lapas orientāciju.

[![Lappuses orientācijas atlasīšana konvertēšanai PDF formātā.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

Lai būtu iespēja atlasīt PDF lappuses orientāciju, ir jāinstalē Finance 10.0.10 vai jaunāka versija. Finanšu versijās **pirms versijas 10.0.23** opcija piedāvā šādas lapas orientācijas opcijas:

- Portretorientācija
- Ainavorientācija

Atlasītā lappuses orientācija tiek lietota visām izejošā dokumenta konfigurācijām, kas tiek ģenerētas Excel formātā un pēc tam konvertētas PDF formātā.

Taču **versijā 10.0.23 un jaunākās** lapas orientācijas opciju saraksts ir paplašināts šādi:

- Portretorientācija
- Ainavorientācija
- Konkrēta darblapa

Atlasot opciju **Darblapai**, katra ģenerētās Excel darbgrāmatas darblapa tiek konvertēta uz PDF, izmantojot lapas orientāciju, kas ir konfigurēta šai darblapai izmantotajā Excel veidnē. Tātad, iespējams, jums ir gala PDF dokuments, kurā ir portretorientācijas un ainavorientācijas lapas. 

Ja konvertētais PDF tiek izveidots no ER konfigurācijas programmas Word formātā, PDF lappuses orientācija vienmēr tiek ņemta no Word dokumenta.

## <a name="output-unfolding"></a>Izvades izvēršana

Konfigurējot jūsu ER formāta **Mapes** komponenta adresātu, varat norādīt, kā šī komponenta izvade tiek piegādāta konfigurētajā gala mērķī.

### <a name="make-output-unfolding-available"></a>Padarīt izvades izvēršanu pieejamu

Lai pašreizējā Finance instancē būtu pieejama izvades izvēršanas opcija, atveriet **Līdzekļu pārvaldības** darbvietu un ieslēdziet funkciju **Atļaut konfigurējamiem ER adresātiem sūtīt mapes kā atsevišķu failu**.

### <a name="applicability"></a>Piemērojamība

Izvades izvēršanas opciju var konfigurēt tikai **Mapes** tipa formāta komponentiem. Kad sākat konfigurēt **Mapes** komponentu, kopsavilkuma cilne **Vispārīgi** kļūst pieejama **Elektronisko pārskatu adresāta** lapā. 

### <a name="use-the-output-unfolding-option"></a>Izmantojiet izvades izvēršanas opciju

Kopsavilkuma cilnes **Vispārīgi** laukā **Sūtīt mapi kā** atlasiet vienu no šīm vērtībām:

- **ZIP arhīvs** - piegādājiet ģenerēto failu kā zip failu.
- **Atsevišķi faili** - piegādāt katru ģenerēto zip failu kā atsevišķu failu.

    > [!NOTE]
    > Atlasot **Atsevišķus failus**, ģenerētā izvade tiek apkopota saspiestā stāvoklī. Tāpēc maksimālais [faila izmēra limits](er-compress-outbound-files.md) tiek pielietots saspiestam izvades failam, kad reālais faila izmērs var pārsniegt noteikto limitu. Šo vērtību ieteicams atlasīt, kad paredzams, ka ģenerētā izvades lielums būs ļoti liels.

[![Notiek mapes formāta komponenta adresāta konfigurēšana.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Ierobežojumi

Ja lauku **Sūtīt mapi kā** iestatāt uz **Atsevišķi faili** komponentam **Mape**, kas satur citus ligzdotos **Mapes** komponentus, iestatījums netiek rekursīvi pielietots ligzdotiem **Mapes** komponentiem.

## <a name="change-page-layout-properties-of-a-template"></a><a name="change-page-layout-properties-of-a-template"></a> Mainīt veidnes lapas izkārtojuma rekvizītus

ER formāta komponentam varat konfigurēt ER Microsoft Office adresātu, kas paredzēts veidnes izmantošanai pārskata ģenerēšanas formātā (Excel vai Word). Ja neesat šī formāta īpašnieks un formāta veidnes lapas izkārtojuma rekvizīti ir jāmaina, Finanšu versijās pirms versijas 10.0.29 ir jāizveido atvasināts formāts un jāmodificē veidņu rekvizīti. Pēc tam ir jāuztur atvasinātā formāta konfigurācija. Taču versijā 10.0.29 un jaunākā versijā var mainīt veidnes lapas izkārtojuma rekvizītus izpildlaikā, lai izvairītos no atvasinātā formāta konfigurācijas izveidošanas un uzturēšanas. Lai to izdarītu, iestatiet vēlamos rekvizītus kā daļu no konfigurētā ER adresāta iestatījumiem. Izpildot ER formātu un izpildot ER adresātu, kas ir konfigurēts noteiktu lapas izkārtojuma rekvizītu izmantošanai, izpildītā adresāta lapas izkārtojuma rekvizītu vērtības tiek piemērotas izmantotajām veidnēm, nomainot sākotnējās veidnes rekvizītus. Varat konfigurēt dažādus adresātus viena un tā paša formāta komponentam, kas konfigurē dažādus lapu izkārtojuma rekvizītus izmantotai veidnei.

ER mērķī var konfigurēt šādus rekvizītus formāta komponentam, kas paredzēts veidnes izmantošanai Excel vai Word formātā:

- Lapas orientācija
    - Portretorientācija
    - Ainavorientācija
- Papīra izmēri
    - A3
    - A4
    - A5
    - B4
    - B5
    - Executive
    - Juridiskā informācija
    - Letter
    - Statement
    - Tabloid
- Lapas malas
    - Augša
        - Galvene
    - Apakša
        - Kājene
    - Kreisā puse
    - Labā puse

> [!NOTE]
> Šādā veidā konfigurētās [veidnes lapas orientācijai ir jābūt saskaņotai ar lapas orientāciju PDF pārvēršanai, ja ir konfigurēta PDF](#select-a-page-orientation-for-pdf-conversion) pārvēršana.

Lappuses piemales iestatīšanai ir jāatlasa garuma vienība:

- Collas
- Centimetri
- Milimetri

![Iestatiet lapas izkārtojuma rekvizītus elektronisko pārskatu adresāta lapā.](./media/er_destinations-set-page-layout-properties.png)

> [!TIP]
> Kad uzcenojuma vērtība tiek iecelta centimetros un norādīta ar vairākām decimāldaļām, tas tiek noapaļots līdz tuvākajai vērtībai ar 1 decimālzīmi.
>
> Kad uzcenojuma vērtība tiek iecelta milimetros un norādīta ar decimāldaļām, tas tiek noapaļots excel izpildlaikā līdz tuvākajai vesela skaitļa vērtībai, bez decimālzīmēm.
>
> Kad uzcenojuma vērtība tiek iecelta milimetros un norādīta ar vairākām decimāldaļām, tas tiek noapaļots word izpildlaikā līdz tuvākajai vērtībai ar vienu decimāldaļskaitļu.

## <a name="security-considerations"></a>Drošības apsvērumi

ER galamērķiem tiek izmantoti divu tipu privilēģijas un pienākumi. Viens tips kontrolē lietotāja vispārējo spēju uzturēt galamērķus, kas ir konfigurēti kādai juridiskajai personai (t.i., tas kontrolē piekļuvi lapai **Elektronisko pārskatu veidošanas adresāti** ). Otrs tips kontrolē programmas lietotāja spēju izpildes laikā ignorēt galamērķu iestatījumus, ko konfigurēja ER izstrādātājs vai ER funkcionālais konsultants.

| Loma (AOT nosaukums)                     | Lomas nosaukums                                  | Pienākums (AOT nosaukums)                     | Pienākuma nosaukums                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroniskā pārskata izstrādātājs             | ERFormatDestinationConfigure        | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu                |
| ERFunctionalConsultant              | Elektronisko pārskatu veidošanas funkcionālais konsultants | ERFormatDestinationConfigure        | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu                |
| PaymAccountsPayablePaymentsClerk    | Kreditoriem maksājamo rēķinu darbinieks            | ERFormatDestinationRuntimeConfigure | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu izpildlaikā |
| PaymAccountsReceivablePaymentsClerk | Debitoru parādu maksājumu darbinieks         | ERFormatDestinationRuntimeConfigure | Konfigurēt elektronisko pārskatu veidošanas formāta adresātu izpildlaikā |

> [!NOTE]
> Iepriekš uzskaitītajos pienākumos tiek izmantotas divas privilēģijas. Šo privilēģiju nosaukumi ir tādi paši kā tām atbilstošo pienākumu nosaukumi: **ERFormatDestinationConfigure** un **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Esmu importējis elektroniskas konfigurācijas un tās redzu lapā Elektronisko atskaišu veidošanas konfigurācijas. Bet kāpēc tās nav redzamas lapā Elektronisko pārskatu veidošanas galamērķi?

Noteikti atlasiet lauku **Jauns** un pēc tam atlasiet konfigurāciju laukā **Atsauce**. Lapā **Elektronisko atskaišu galamērķi** ir parādītas tikai tās konfigurācijas, kam ir konfigurēti galamērķi.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Vai iespējams kaut kā definēt, kuru Microsoft Azure krātuves kontu un Azure Blob krātuvi lietot?

Nr.p.k. Tiek lietota noklusējuma Microsoft Azure Blob krātuve, kas ir definēta un lietota dokumentu pārvaldības sistēmai.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Kādam nolūkam galamērķa iestatījumos tiek izmantots galamērķis Fails? Ko šis iestatījums dara?

**Faila** mērķis tiek izmantots, lai kontrolētu jūsu tīmekļa pārlūkprogrammas dialoglodziņu, kad darbināt ER formātu interaktīvā režīmā. Ja iespējojat šo galamērķi vai ja konfigurācijai nav definēts nekāds galamērķis, tad pēc izvades faila izveidošanas tīmekļa pārlūkā tiek parādīts atvēršanas vai saglabāšanas dialoglodziņš.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Vai varat sniegt piemēru formulai, kas atsaucas uz kreditora kontu, uz kuru es varu sūtīt e-pastu?

Šī formula ir atkarīga no ER konfigurācijas. Piemēram, ja lietojat konfigurāciju ISO 20022 kredīta pārskaitījums, varat lietot **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** vai **model.Payments.Creditor.Identification.SourceID**, lai iegūtu saistītu kreditora kontu.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Viena no manām formāta konfigurācijām ietver vairākus failus, kas ir grupēti vienā mapē (piemēram, mapē Mape1 ietilpst faili Fails1, Fails2 un Fails3). Kā iestatīt galamērķus tā, lai fails Mape1.zip netiktu izveidots vispār, fails Fails1 tiktu nosūtīts pa e-pastu, fails Fails2 tiktu nosūtīts uz SharePoint, bet failu Fails3 varētu atvērt uzreiz pēc konfigurācijas izpildīšanas?

Jūsu formātam vispirms jābūt pieejamam ER konfigurācijās. Ja šis priekšnoteikums tiek ievērots, atveriet lapu **Elektronisko atskaišu galamērķi** un izveidojiet jaunu atsauci uz konfigurāciju. Pēc tam jums ir nepieciešami četri failu galamērķi — viens katram izvades komponentam. Izveidojiet pirmo failu galamērķi, piešķiriet tam nosaukumu, piemēram, **Mape**, un atlasiet faila nosaukumu, kas apzīmē kādu mapi jūsu konfigurācijā. Pēc tam atlasiet **Iestatījumi** un pārliecinieties, ka visi galamērķi ir atspējoti. Šim failu galamērķim mape netiks izveidota. Pēc noklusējuma, tā kā starp failiem un pamata mapēm pastāv hierarhiskas atkarības, šie faili darbosies tādā pašā veidā. Citiem vārdiem sakot — tie netiks nekur sūtīti. Lai ignorētu šo noklusējuma uzvedību, jums ir jāizveido vēl trīs failu galamērķi — viens katram failam. Katram galamērķa iestatījumos jums ir jāiespējo tas galamērķis, uz kuru šis fails ir jānosūta.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Konfigurēt no darbības atkarīgus ER adresātus](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
