---
title: cXML uzlabojumu iegāde
description: cXML uzlabojumu iegādes līdzeklis tiek veidots uz esošās ārējā kataloga funkcionalitātes, PunchOut, kas tiek izmantota pirkšanas pieprasījumiem.
author: dasani-madipalli
manager: tfehr
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3113202b1f38bc528733c980321d60bb9ad23dde
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992199"
---
# <a name="purchasing-cxml-enhancements"></a>cXML uzlabojumu iegāde

[!include [banner](../includes/banner.md)]

_cXML uzlabojumu iegādes_ līdzeklis tiek veidots uz [esošās ārējā kataloga funkcionalitātes](set-up-external-catalog-for-punchout.md), kas tiek izmantota pirkšanas pieprasījumiem. Šī esošā funkcionalitāte ir zināma kā _PunchOut_. Lai gan pirkšanas pasūtījumam nav jābūt izveidotam no pirkšanas pieprasījuma, ir jābūt saistībai starp pirkšanas pasūtījuma kreditoru un parametriem, kas tiek izmantoti pirkšanas pasūtījuma dokumenta nosūtīšanai.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>cXML uzlabojumu iegādes līdzekļa ieslēgšana

Lai ieslēgtu šo līdzekli, atveriet lapu **[līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** un meklējiet līdzekli ar nosaukumu *cXML uzlabojumu iegāde*. Atlasiet līdzekli un pēc tam atlasiet **Iespējot tūlīt**, lai to ieslēgtu.

Pēc līdzekļa ieslēgšanas ir jākonfigurē iestatījumi tālāk aprakstītajās jomās:

- **[cXML parametri](#cxml-parameters)** — izmantojiet šos iestatījumus, lai iestatītu funkcionalitātes globālos parametrus pirkšanas pasūtījumu nosūtīšanai.
- **[Kreditora iestatīšana](#vendor-setup)** — ja komercijas paplašināmās iezīmēšanas valoda (cXML) ir jāizmanto pēc noklusējuma visiem jaunajiem pirkšanas pasūtījumiem, kas tiek izveidoti visiem kreditoriem, tad šim kreditoram iestatiet opciju **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** uz _Jā_.
- **[Ārējie katalogi](#external-catalog-setup)** — izmantojiet jaunos **Pasūtījuma rekvizīti** iestatījumus, lai definētu pirkšanas pasūtījuma dokumenta formātu un tā nosūtīšanas veidu.

Šī konfigurācija ir attēlota tālāk esošajā attēlā.

![cXML līdzekļu iestatīšanas apgabali](media/cxml-settings-areas.png "cXML līdzekļu iestatīšanas apgabali")

Turklāt ir jāiestata arī [Pirkšanas pasūtījuma pieprasījuma pakešuzdevums](#po-batch). Šis pakešuzdevums tiek izmantots apstiprināto pirkšanas pasūtījumu nosūtīšanai.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>cXML globālo parametru iestatīšana

Izmantojiet **cXML parametri** lapu, lai izveidotu dažus globālus iestatījumus, kas attiecas uz pirkšanas pasūtījumu nosūtīšanas funkcionalitāti.

![cXML parametru lapa](media/cxml-parameters.png "cXML parametru lapa")

Dodieties uz **Sagāde un avoti \> Iestatīšana \> cXML pārvaldība \> cXML parametri** un iestatiet šādus parametrus:

- **cXML pārbaudes režīms** — šis globālais parametrs ietekmē veidu, kādā pirkšanas pasūtījumi tiek fiziski nosūtīti no pakešuzdevuma. Atlasiet vienu no šīm vērtībām:

    - **Pārbaudīt** – šajā režīmā pakešuzdevums var darboties, un tiek ģenerēts ziņojuma XML dokuments, bet tas netiek nosūtīts. Tā vietā tas tiek saglabāts pirkšanas pasūtījuma pieprasījumā pārskatīšanas nolūkiem. Šis režīms ir noderīgs, kad atrodaties sākotnējā ieviešanā, un vēlaties redzēt, kā dati tiek ievadīti cXML ziņojumā. Varat arī izveidot ziņojumu paraugus, kurus var nosūtīt kreditoriem sākotnējās pārbaudes veikšanai.
    - **Izmantot** – šajā režīmā līdzeklis izmanto [ārējā kataloga iestatījumus](#external-catalog-setup), lai fiziski pārraidītu katru dokumentu kreditoram.

- **Nosūtīt pirkšanas pieprasījuma atjauninājumus** — iestatiet šo opciju uz *Jā*, lai nosūtītu pirkšanas pasūtījumu atjaunināšanas ziņojumu. Iestatiet to uz *Nē*, lai neatļautu ziņojuma nosūtīšanu. Vairums kreditoru nevēlas saņem atjaunināšanas ziņojumus. Tā vietā viņi pieprasa, lai klienti sazinās ar viņiem pa tālruni vai e-pastu, ja ir nepieciešams mainīt pirkšanas pasūtījumu. Šis ir globāls parametrs un katra kreditora ārējā katalogā pārlabošanu norādīt nav iespējams. Pirkšanas pasūtījums tiks atzīmēts kā atjaunināts, grāmatojot otru apstiprinājumu pirkšanas pasūtījumam, kamēr pirmais apstiprinājums jau ir nosūtīts un kreditora apstiprināts. Ja pastāv otrs apstiprinājums, kamēr pirmais apstiprinājums vēl nav nosūtīts, otrais apstiprinājums tiks uzskatīts par jaunu dokumentu. Pirkšanas pasūtījumu var apstiprināt tik reižu, cik vēlaties, līdz tiek nosūtīts viens apstiprinājums. Nākamais apstiprinājums tiks uzskatīts par atjaunināšanas ziņojumu.
- **Nosūtīt pirkšanas pieprasījuma dzēšanu** — iestatiet šo opciju uz *Jā*, lai nosūtītu pirkšanas pasūtījumu dzēšanas ziņojumu. Iestatiet to uz *Nē*, lai neatļautu ziņojuma nosūtīšanu. Vairums kreditoru nevēlas saņem dzēšanas ziņojumus. Tā vietā viņi pieprasa, lai klienti sazinās ar viņiem pa tālruni vai e-pastu, ja pirkšanas pasūtījums tika nosūtīts kļūdas dēļ. Šis ir globāls parametrs un katra kreditora ārējā katalogā pārlabošanu norādīt nav iespējams. Pirkšanas pasūtījums tiks atzīmēts kā dzēsts, ja atcelsit pirkšanas pasūtījumu programmā Supply Chain Management.
- **Arhīva fails** — norādiet faila ceļu, kur vēlaties eksportēt un saglabāt arhivētos cXML dokumentus. Ceļš tiek izmantots, izpildot dzēšanas funkciju no lapas **Pirkšanas pasūtījuma pieprasījums**.
- **Ielas rindas maksimālais rakstzīmju skaits** — ievadiet maksimālo rakstzīmju skaitu, ko var izmantot, adreses ielas laukā cXML dokumentā. Šis globālais parametrs ietekmē visus kreditorus, ja vien ārējā kataloga rekvizītos nav norādīts to ignorēt.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Kreditora pirkšanas pasūtījumu iestatīšana, lai izmantotu cXML

Katru reizi, apstiprinot pirkšanas pasūtījumu, kurā opcija **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** ir iestatīta uz _Jā_, sistēma automātiski ģenerē cXML ziņojumu un piegādā to kreditoram, kas ir saistīts ar konkrēto pirkšanas pasūtījumu. Pirkšanas pasūtījumiem šo opciju var kontrolēt divos veidos:

- Lai iestatītu kreditoru tā, lai tas automātiski izmanto cXML visiem jaunajiem pirkšanas pasūtījumiem, kas tiek izveidoti no pieprasījuma, dodieties uz **Sagāde un avoti \> Kreditori \> Visi kreditori** un atlasiet vai izveidojiet kreditoru, lai atvērtu tā informācijas lapu. Pēc tam kopsavilkuma cilnē **Pirkšanas pasūtījuma noklusējuma informācija** iestatiet opciju **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** uz _Jā_. Ja cXML ir automātiski jāizmanto arī jaunajiem pirkšanas pasūtījumiem, kas **nav** izveidoti no pieprasījuma, tad arī pasūtījuma rekvizīts **ENABLEMANUALPO** attiecīgajam ārējam katalogam ir jāiestata uz _Patiess_, kā aprakstīts šīs tēmas sadaļā [Pasūtījuma rekvizītu iestatīšana](#set-order-properties).
- Atsevišķu pirkšanas pasūtījumu gadījumā, dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi** un atlasiet vai izveidojiet pirkšanas pasūtījumu, lai atvērtu tā informācijas lapu. Pārejiet uz skatu **Galvene** un pēc tam kopsavilkuma cilnē **Iestatīšana** iestatiet opciju **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** pēc nepieciešamības.

![Kreditora pirkšanas pasūtījumu noklusējuma iestatījumi](media/cxml-order-defaults.png "Kreditora pirkšanas pasūtījumu noklusējuma iestatījumi")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Ārēja kataloga iestatīšana, lai izmantotu cXML

Katram katalogam lapā **Ārējie katalogi** varat iestatīt PunchOut funkcionalitāti un pirkšanas pasūtījumu nosūtīšanas funkcionalitāti. Lai atrastu atbilstošos iestatījumus, dodieties uz **Sagāde un avoti \> Katalogi \> Ārējie katalogi**. Sāciet, [iestatot katru katalogu kā parasti](set-up-external-catalog-for-punchout.md). Šis process ietver kreditora piešķiršanu, kategoriju atlasi, kuras kreditors drīkst piegādāt, un kataloga aktivizēšanu. Pēc tam konfigurējiet papildu iestatījumus, kas aprakstīti šajā sadaļā.

> [!NOTE]
> Apstiprinot pirkšanas pasūtījumu, ko var nosūtīt, izmantojot cXML, sistēma uzmeklē kreditoru, kas ir saistīts ar pirkšanas pasūtījumu, un pēc tam atrod pirmo aktīvo ārējo katalogu, kas ir saistīts ar šo kreditoru. Pēc tam sistēma izmanto iestatījumus no ārējā kataloga, lai nosūtītu pirkšanas pasūtījumu. Ja ir iestatīti vairāki ārējie katalogi, sistēma izmanto tikai pirmo atrasto ārējo katalogu, pamatojoties uz pirkšanas pasūtījumā norādīto kreditoru. Tāpēc ir ieteicams izveidot tikai vienu ārējo katalogu katram kreditoram.

![Ārējā kataloga iestatījumi](media/cxml-supplier-catalog.png "Ārējā kataloga iestatījumi")

### <a name="set-the-punchout-protocol-type"></a>PunchOut protokola iestatīšana

Lapas **Ārējie katalogi** kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Punchout protokols** uz _cXML_. Šī opcija būs vienīgā pieejamā opcija, izņemot gadījumus, kad partneris ir paplašinājis funkcionalitāti un sniedz paplašinājumu papildu opcijas.

Ja funkcionalitātei PunchOut izmantojat arī katalogu, ir [jāiestata arī ziņojuma formāts](set-up-external-catalog-for-punchout.md). Ziņojuma formāts tiek izmantots, lai no pieprasījuma izveidotu savienojumu ar kreditoru PunchOut darījumā. Nosūtot pirkšanas pasūtījumu, tiks izmantoti pasūtījuma rekvizīti, lai izveidotu savienojumu ar kreditoru.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Pasūtījuma rekvizītu iestatīšana

_cXML uzlabojumu iegādes_ līdzeklis pievieno jaunus **Pasūtījuma rekvizītus** kopsavilkuma cilnes ārējiem katalogiem. Šī kopsavilkuma cilne nodrošina režģi, kurā var definēt pasūtījuma rekvizītus. Tajā ir iekļauta arī rīkjosla. Šajā rīkjoslā ir tālāk norādītās trīs pogas, ko var izmantot, lai pārvaldītu pasūtījumu rekvizītus:

- **Noklusējuma rekvizīti** — iestatot jaunu katalogu, atlasiet šo pogu, lai režģim pievienotu iepriekš definētu biežāk izmantoto rekvizītu kolekciju.
- **Jauns** — pievienojiet režģim jaunu rekvizītu.
- **Dzēst** — dzēsiet pašlaik atlasīto rekvizītu no režģa. Ja nejauši izdzēšat noklusējuma rekvizītu, atlasiet **Noklusējuma rekvizīti**, lai atjaunotu visus trūkstošos rekvizītus.

Katru reizi, pievienojot režģim vienu vai vairākus rekvizītus, izmantojiet labajā pusē esošo kolonnu, lai norādītu katra rekvizīta vērtību.

Noklusējuma rekvizītus varat izmantot šādos veidos:

- **BUYER\_COOKIE** — šo izsekošanas lauku var izmantot, lai norādītu ar jūsu uzņēmumu saistītu informāciju. Ja vien ar kreditoru nav noslēgts līgums par šī rekvizīta izmantošanu, tam nav lielas nozīmes, nosūtot pirkšanas pasūtījumu. Tādēļ to jāiestata uz vienkāršu vērtību.
- **DELIVERTO** – kad piegādes adrese tiek ievadīta dokumentā no pirkšanas pasūtījuma, lauks **Brīdinājuma informācija** tiek izmantots, lai iestatītu lauku **DeliverTo** XML ziņojumā. Ja nepieciešams, lai šī vērtība būtu pieprasītāja nosaukums, un vēlaties pieprasītāja lauku iestatīt pirkšanas pasūtījuma galvenē, ievadiet šim rekvizītam vērtību _REQUESTER_, lai pieprasītāja nosaukums tiktu ievadīts laukā **DeliverTo** XML ziņojumā. Šādā gadījumā primārā e-pasta adrese un tālruņa numurs, kas tiek izmantots, būs pieprasītāja, nevis pasūtītāja.
- **DEPLOYMENTMODE** – iestatiet šo rekvizītu, kā to pieprasa kreditors. Parasti vērtības ir _PRODUCTION_ vai _TEST_. Iestatiet vērtību, pamatojoties uz saziņu ar kreditoru. Parasti tai ir jāatbilst paredzētajai sistēmai, kas atrodas aiz **ORDERCHECKURL** vērtības, ko kreditors norāda kā pārbaudes vai ražošanas sistēmu.
- **FIXEDBILLADDRESSID** – kad lauks **addressID** tiek iestatīts XML ziņojumā, tas izvēlas adresē norādīto atrašanās vietu. Ja ID vērtība, ko nosūtījāt kreditoram, kāda iemesla dēļ atšķiras no adreses atrašanās vietas vērtības, varat veikt pārlabošanu, norādot vērtību šeit. Pieņēmums ir tāds, ka kreditoram izmantosit tikai vienu adresi un ka adrese ir iestatīta kreditora sistēmā. Rēķina adrese ir primārā rēķina adrese, kas norādīta juridiskajai personai programmā Supply Chain Management.
- **FIXEDSHIPADDRESSID** – kad lauks **addressID** tiek iestatīts XML ziņojumā, tas izvēlas adresē norādīto atrašanās vietu. Ja ID vērtība, ko nosūtījāt kreditoram, kāda iemesla dēļ atšķiras no adreses atrašanās vietas vērtības, varat veikt pārlabošanu, norādot vērtību šeit. Pieņēmums ir tāds, ka kreditoram izmantosit tikai vienu adresi un ka adrese ir iestatīta kreditora sistēmā. Piegādes adrese ir adrese, kas norādīta pirkšanas pasūtījuma galvenē. Vairums kreditoru pieņem tikai galvenes adreses, nevis rindu adreses. Lai arī XML ir lauki rindu adresēm, tie tiks iestatīti uz galvenes adresi.
- **FROM\_DOMAIN** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **FROM\_IDENTITY** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **ORDERCHECKURL** — ievadiet URL, lai pārsūtītu pirkšanas pasūtījuma dokumentus. URL sākas ar `https://` un to nodrošina jūsu kreditors.
- **PAYLOAD\_ID** — ievadiet lietderīgās slodzes ID prefiksa vērtību, kas nepieciešama pašreizējā kreditora biznesa procesiem.
- **SENDER\_DOMAIN** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **SENDER\_IDENTITY** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **SHARED\_SECRET** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **STREETLENGTH** — ievadiet skaitli, kas norāda maksimālo rakstzīmju skaitu, ko kreditors pieņem kā ielas nosaukumu. Ja šeit ir ievadīta vērtība, tā pārlabo vērtību, kas ir norādīta lapā **cXML parametri**. Sistēma noņems rindiņu pārtraukumus un atstarpes, lai mēģinātu pielāgot standarta Supply Chain Management adresi šeit norādītajam rakstzīmju skaitam. Visas papildu rakstzīmes tiks aprautas.
- **TO\_DOMAIN** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **TO\_IDENTITY** — ievadiet vērtību, kas tiek izmantota pirkšanas pasūtījuma dokumentu nosūtīšanai. Šo vērtību nodrošina jūsu kreditors.
- **USERAGENT** — ievadiet vērtību, lai identificētu izmantoto sistēmu. Piemēram, ievadiet _Dynamics 365 Supply Chain Management_.
- **VERSION** — ievadiet cXML versijas numuru, ja šo informāciju pieprasa kreditors. Noklusējuma versija ir *1.2.008*. Šī versija ir stabila un to pieņem vairums kreditoru.
- **RESPONSETEXT** – ievadiet jebkādu pielāgotu tekstu, kas kreditoram ir jāatgriež cXML atbildes ziņojumā pēc pasūtījuma nosūtīšanas. Šādā veidā sistēma var atzīmēt ziņojumu kā _Apstiprināts_. Ja atbilde neatbilst standarta tekstam vai šeit ievadītajam debitora tekstam, pieprasījums tiks atzīmēts kā _Kļūda_.
- **RESPONSETEXTSUB** – iestatiet šo rekvizītu uz _TRUE_, ja vēlaties meklēt kreditora atbildes tekstu vērtībām, kas norādītas laukā **RESPONSETEXT**. Piemēram, kreditors var atgriezt garu atbildes virkni, kas ietver “labi”. Šādā gadījumā var ievadīt _labi_ laukā **RESPONSETEXT** un iestatīt **RESPONSETESTSUB** uz _TRUE_, lai atbildē meklētu “labi”. Pēc tam pasūtījums var tikt iestatīts kā _Apstiprināts_.
- **CONTENTTYPE** – tipiskā kataloga iestatījumā šis rekvizīts nav jāiestata. Ja, nosūtot pirkšanas pasūtījumu, no kreditora sistēmas saņemat servera 500 kļūdu, varat veikt pārbaudi, iestatot šo rekvizītu uz _FALSE_. Šī vērtība mainīs iestatījumu tīmekļa pieprasījumā un var iespējot ziņojumu nosūtīšanu dažām platformām.
- **ENABLEHEADERS** – iestatiet šo rekvizītu uz _TRUE_, lai nosūtītu galvenes kopā ar pirkšanas pasūtījumu. Šis rekvizīts ir jāiestata tikai tad, ja kreditors to pieprasa. Ja šo rekvizītu iestatāt uz _TRUE_, pievienojiet papildu pielāgotus rekvizītus, kuru pamatā ir kreditoru sniegtie nosaukumi, un pievienojiet tiem prefiksu _H\__. Raksturīgākie piemēri ir **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** un **H\_ACTIONREQUEST**. Noklusējuma rekvizītos ir ietverti šādi pielāgotie rekvizīti:

    - **H\_USERID** — ja tirdzniecības partnerim nepieciešams nosūtīt lietotāja ID kā daļu no URL, lai iesniegtu pirkšanas pasūtījumu, ievadiet šeit vērtību.
    - **H\_PASSWORD** — ja tirdzniecības partnerim nepieciešams nosūtīt paroli kā daļu no URL, lai iesniegtu pirkšanas pasūtījumu, ievadiet šeit vērtību.

- **ENABLEMANUALPO** – ja šis rekvizīts ir iestatīts uz _TRUE_, kad lietotāji manuāli izveido pirkšanas pasūtījumus (tas ir, kad tie nesākas no pieprasījuma), šie pirkšanas pasūtījumi pārmantos opciju **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** no kreditora. Ja šis rekvizīts nav iestatīts vai arī tas ir iestatīts uz _FALSE_, tad manuāli izveidotiem pirkšanas pasūtījumiem opcija **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** netiks iestatīta pirkšanas pasūtījuma galvenē. Pirkšanas pasūtījumiem, kas tiek izveidoti no pieprasījuma, iestatījuma opcija **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** vienmēr tiek pārmantota no kreditora, neatkarīgi no šī rekvizīta iestatījuma. Papildinformāciju skatiet šīs tēmas iepriekšējā sadaļā [kreditora pirkšanas pasūtījumu iestatīšana, lai izmantotu cXML](#vendor-setup).
- **PUNCHOUTPOONLY** – ja šis rekvizīts ir iestatīts uz _TRUE_, tikai pirkšanas pieprasījuma rindām, kas tiek veidotas, izmantojot PunchOut procesu, pirkšanas pasūtījuma galvenē tiks iestatīta opcija **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML**. Turklāt pirkšanas pieprasījuma rindas veidam visām pirkšanas pasūtījuma rindām ir jābūt _Ārējā kataloga krājumam_. Pretējā gadījumā cXML pirkšanas pasūtījumu nevar izveidot.
- **PUNCHOUTSHIPTO** – ja šis rekvizīts ir iestatīts uz _TRUE_, juridiskās personas noklusējuma adrese tiks pievienota PunchOut iestatīšanas pieprasījuma ziņojumam, kad lietotājs atvērs ārējo katalogu. Šī adrese tiek pievienota kā **ShipTo** adrese. Kreditori izmantos **ShipTo** adresi, lai parādītu izcenojumu, pamatojoties uz uzņēmuma atrašanās vietu.
- **TRACEPUNCHOUT** – iestatiet šo rekvizītu uz _TRUE_, ja saņemat kļūdas ziņojumu, mēģinot pārlūkot ārēju katalogu no pieprasījuma. Izsekošanas informācija tiks aizpildīta **PunchOutSetupRequest** un **PunchOutResponse** ziņojumiem, kas tiek nosūtīti starp Supply Chain Management un kreditora vietni. Šo informāciju var skatīt lapā **cXML groza ziņojumu žurnāls**, kuru var atvērt no lapas **Ārējā kataloga iestatīšana** tam piegādātāju katalogam, ar kuru jums ir radušās problēmas. Šo rekvizītu vajadzētu iestatīt uz _TRUE_, ja veicat problēmu novēršanu, jo tas izveido lielu veiktspēju katrai PunchOut datu bāzei. Papildinformāciju skatiet šīs tēmas sadaļā [cXML groza ziņojumu žurnāla skatīšana ārējam katalogam PunchOut](#message-log).
- **REPLACENEWLINE** – iestatiet šo rekvizītu uz _TRUE_, ja rodas problēma ar kreditora sistēmas sūtīto **PunchOutResponse** ziņojumu, kas ietver jaunās rindiņas rakstzīmes (\\n). Šī problēma var rasties, ja kreditora ziņojumi tiek parsēti, izmantojot starpprogrammatūru vai sagādes centrmezglu. Ja rodas problēma ar jaunu kreditora iestatījumu, iestatiet rekvizītu **TRACEPUNCHOUT** uz _TRUE_, lai skatītu **PunchOutResponse** ziņojumu un noteiktu, vai XML tagi ir sadalīti pēc jaunās rindiņas rakstzīmēm.
- **POCOMMENTS** – iestatiet šo rekvizītu uz _TRUE_, ja vēlaties, lai cXML dokumentā tiktu ietvertas piezīmes, kas pievienotas pirkšanas pasūtījumam programmā Supply Chain Management. Pielikuma teksts tiek iekļauts pirkšanas pasūtījuma ziņojuma galvenes komentāros. Papildinformāciju par to, kā sistēma atlasa un apstrādā šos pielikumus, skatiet šīs tēmas sadaļā [Piezīmju pievienošana pirkšanas pasūtījumam](#attach-po-notes).
- **VENDCOMMENTS** – iestatiet šo rekvizītu uz _TRUE_, ja vēlaties, lai cXML dokumentā tiktu ietvertas piezīmes, kas pievienotas pirkšanas pasūtījumam programmā Supply Chain Management. Pielikuma teksts tiek iekļauts pirkšanas pasūtījuma ziņojuma galvenes komentāros. Papildinformāciju par to, kā sistēma atlasa un apstrādā šos pielikumus, skatiet sadaļā [Piezīmju pievienošana pirkšanas pasūtījumam](#attach-po-notes).
- **CLEANAMP** – iestatiet šo rekvizītu uz _TRUE_, ja saņemat kļūdas ziņojumu, mēģinot veikt PunchOut kreditoram, un kreditora atgriešanas URL ietver nepareizi kodētas zīmes (\&).
- **PUNCHOUTTZ** – iestatiet šo rekvizītu uz _TRUE_, ja kreditors, ar kuru strādājat, lieto Starptautiskās Standartizācijas organizācijas (ISO) 8601 standartu, lai veiktu noteiktu PunchOut pieprasījuma ziņojuma datuma/laika pārbaudi. Supply Chain Management izmanto universālā koordinētā laika (UTC) datumu **PunchOutSetupRequest** ziņojumā. Tādēļ, iestatot šo rekvizītu uz _TRUE_, datuma/laika formātam tiek pievienots *+00:00*.
- **WMSADDRESSID** – iestatiet šo rekvizītu uz _TRUE_, lai izmantotu noliktavas numuru pirkšanas pasūtījuma galvenē kā **addressID** vērtību **ShipTo** adresē pirkšanas pasūtījuma pieprasījumam, kas tiek nosūtīts kreditoram. Ja iestatāt vērtību rekvizītam **FIXEDSHIPADDRESSID**, tad otrai vērtībai ir augstāka prioritāte pār šo vērtību. Tāpēc ir ieteicams izmantot vienu vai otru rekvizītu, lai iestatītu **addressID** vērtību **ShipTo** dokumenta adresē.
- **PUNCHOUTSHIPTOUSER** – šis rekvizīts darbojas kopā ar **PUNCHOUTSHIPTO** rekvizītu. Ja **PUNCHOUTSHIPTO** ir iestatīts uz _TRUE_, tiek atlasīta juridiskās personas adrese. Ja **PUNCHOUTSHIPTOUSER** ir iestatīts uz _TRUE_, juridiskās personas adreses vietā tiek izmantota primārā adrese no PunchOut lietotāja.

### <a name="activate-the-external-catalog"></a>Ārējā kataloga aktivizēšana

Pabeidzot visu rekvizītu iestatīšanu un citu ārējo katalogu iestatījumu konfigurēšanu, atgriezieties lapas **Ārējie katalogi** kopsavilkuma cilnē **Vispārīgi** un iestatiet opciju **Aktīvs** uz *Jā*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Piezīmju pievienošana pirkšanas pasūtījumam

Kā jau tika minēts iepriekš sadaļā [Pasūtījuma rekvizītu iestatīšana](#set-order-properties), ja vēlaties, lai piegādātā cXML iekļautu tekstu no piezīmēm, kas pievienotas atbilstošajam pirkšanas pasūtījumam un/vai kreditora ierakstiem, varat iestatīt **POCOMMENTS** un/vai **VENDCOMMENTS** rekvizītu uz _TRUE_ ārējā kataloga iestatījumā. Šajā sadaļā ir sniegta detalizētāka informācija par to, kā sistēma atlasa un apstrādā šos pielikumus, ja tos izmantojat.

Lai iestatītu to piezīmju veidus, kurus meklēs sistēma, dodieties uz **Sagāde un avoti \> Iestatījumi \> Formas \> No iestatījumiem**. Pēc tam cilnē **Pirkšanas pasūtījums** iestatiet **Iekļaut dokumentu veidus** lauku uz to veidu, ko vēlaties iekļaut. Tiek iekļautas tikai teksta piezīmes, nevis dokumentu pielikumi.

![Formas iestatījumu lapa](media/cxml-form-setup.png "Formas iestatījumu lapa")

Pielikumi tiks iekļauti pirkšanas pasūtījumā tikai tad, ja to lauks **Veids** ir iestatīts uz vērtību, kas atlasīta laukā **Iekļaut dokumentu veidu** un ja to lauks **Ierobežojums** ir iestatīts uz _Ārējs_. Lai izveidotu, skatītu vai rediģētu pirkšanas pasūtījuma pielikumus, dodieties uz **Sagāde un avoti \> Visi pirkšanas pasūtījumi**, atlasiet vai izveidojiet pirkšanas pasūtījumu un pēc tam augšējā labajā stūrī atlasiet pogu (saspraudes simbols) **Pielikumi**.

![Pievienotā piezīme, kas ir iestatīta nosūtīšanai kreditoram](media/cxml-note-to-vendor.png "Pievienotā piezīme, kas ir iestatīta nosūtīšanai kreditoram")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>cXML groza ziņojumu žurnāla skatīšana ārējam katalogam PunchOut

Iestatot lauku **Punchout protokols** uz _cXML_ ārējam katalogam, sistēma notvers tos groza žurnāla ziņojumus, kuri tiks atgriezti no kreditoriem. Šo žurnālu var izmantot problēmu novēršanai un citiem datu nolūkiem.

Lai atvērtu ārējā kataloga žurnālu, atlasiet atbilstošo katalogu un pēc tam darbību rūtī atlasiet **cXML groza ziņojumu žurnāls**. Lapa **cXML groza ziņojumu žurnāls** parāda atgriezto grozu sarakstu, ar šiem groziem saistītās XML un saistītajā pirkšanas pieprasījumā izveidotās rindas.

![cXML groza ziņojumu žurnāla lapa](media/cxml-cart-message-log.png "cXML groza ziņojumu žurnāla lapa")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Ārējā kataloga PunchOut ārējo elementu iestatīšana

Iestatot lauku **Punchout protokols** uz *cXML* ārējam katalogam, varat pievienot pielāgotus ārējos elementus, kas tiks ievietoti pareizajā vietā pieprasījuma XML ziņojumā.

Lai pievienotu ārējos elementus ārējam katalogam, izpildiet tālāk aprakstītos norādījumus.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Katalogi \> Ārējie katalogi**.
1. Atlasiet atbilstošo katalogu.
1. Kopsavilkuma cilnes **Ziņojuma formāts** sadaļā **Ārēji elementi** atlasiet **Pievienot**, lai režģī pievienotu rindu katram ārējam elementam, ko vēlaties iekļaut. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Nosaukums** – ievadiet elementa nosaukumu. Šī vērtība kļūs par katras rindas izveidotā **ārējā** XML elementa **nosaukuma** atribūta vērtību. Parasti jūs strādāsiet ar savu kreditoru, lai vienotos par katra ārējā elementa nosaukumu.
    - **Vērtība** – atlasiet elementa vērtību. Šī vērtība kļūs par katras rindas izveidotā XML elementa vērtību. Ir pieejamas šādas vērtības:

        - **Lietotāja vārds** – izmantojiet tā lietotāja vārdu, kurš veic PunchOut. Šis nosaukums ir Supply Chain Management pierakstīšanās nosaukums.
        - **Lietotāja e-pasts** – izmantojiet tā lietotāja e-pasta adresi, kurš veic PunchOut. Šī adrese ir vienāda ar adresi, ko lietotājs ir iestatījis cilnē **Konts** lapā **Lietotāja opcijas**.
        - **Nejauša vērtība** – izmantojiet unikālu nejaušu vērtību.
        - **Pilns lietotāja vārds** – izmantojiet pilnu vārdu kontaktpersonai, kas saistīta ar lietotāju, kurš piekļūst ārējam katalogam.
        - **Vārds** – izmantojiet vārdu kontaktpersonai, kas saistīta ar lietotāju, kurš piekļūst ārējam katalogam.
        - **Uzvārds** – izmantojiet uzvārdu kontaktpersonai, kas saistīta ar lietotāju, kurš piekļūst ārējam katalogam.
        - **Tālruņa numurs** – izmantojiet primāro tālruņa numuru kontaktpersonai, kas saistīta ar lietotāju, kurš piekļūst ārējam katalogam.

![Ārēja elementa iestatījumi](media/cxml-extrinsics.png "Ārēja elementa iestatījumi")

Lietotājs vai administrators neredzēs ārējos elementus, jo tie netiek pievienoti, kamēr lietotājs nav veicis PunchOut. Tie tiks automātiski ievietoti starp **BuyerCookie** un **BrowserFromPost** elementiem cXML iestatīšanas pieprasījuma ziņojumā. Tāpēc, iestatot ārējo katalogu, tie XML nav jāiestata manuāli.

![Ārējo elementu pievienošana XML](media/cxml-extrinsics-xml.png "Ārējo elementu pievienošana XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Pirkšanas pasūtījuma izveide un apstrāde

Izveidojot pirkšanas pasūtījumu kreditoram, tas mantos opcijas **Nosūtīt pirkšanas pasūtījumu, izmantojot cXML** iestatījumu no attiecīgā kreditora. Tomēr iestatījums ir pieejams kopsavilkuma cilnes **Iestatīšana** pirkšanas pasūtījuma skatā **Galvene**, lai to vēlāk varētu mainīt pēc nepieciešamības.

![Pirkšanas pasūtījuma iestatīšana, lai izmantotu cXML](media/cxml-purchase-order.png "Pirkšanas pasūtījuma iestatīšana, lai izmantotu cXML")

Izveidojot pirkšanas pasūtījumu no pirkšanas pieprasījuma, kas nāk no PunchOut plūsmas, tiks aizpildīta visu nepieciešamo rindu informācija. Pēc tam varat manuāli pievienot pirkšanas pasūtījuma rindas vai kopēt tās no citiem pirkšanas pasūtījumiem. Pārliecinieties, vai ir iestatīti visi obligātie lauki. Šie obligātie lauki ietver ārējās atsauces numuru, kas ir kreditora numurs, kas tiks izmantots cXML ziņojumā.

![Ārējā atsauces numura piemērs](media/cxml-line-details.png "Ārējā atsauces numura piemērs")

Pabeidzot aizpildīt informāciju par pirkšanas pasūtījumu, noteikti to apstipriniet. Ziņojums netiek nosūtīts, kamēr pirkšanas pasūtījums nav apstiprināts. Lai apstiprinātu pirkšanas pasūtījumu, darbību rūtī cilnē **Pirkšana** grupā **Darbības** atlasiet **Apstiprināt**. 

Pēc pirkšanas pasūtījuma apstiprināšanas, varat skatīt apstiprinājuma statusu, izmantojot žurnālus **Pirkšanas pasūtījuma apstiprinājumi**. Darbību rūts cilnē **Pirkšana**, grupā **Žurnāli**, atlasiet **Pirkšanas pasūtījuma apstiprinājumi**.

Katram pirkšanas pasūtījumam var būt vairāki apstiprinājumi. Katrs apstiprinājums tiek atzīmēts ar inkrementālu skaitli. Tālāk esošajā attēlā pirkšanas pasūtījums ir *00000275* un apstiprinājums ir *00000275-1*. Šī numerācija ataino standarta Supply Chain Management funkcionalitāti, kur izmaiņas pirkšanas pasūtījumā un arī cXML ziņojuma veidā, kas jāsūta kreditoram, tiek identificēts, pamatojoties uz apstiprinājumu. Kā redzams attēlā, lapa **Pirkšanas pasūtījuma apstiprinājumi** ietver arī laukus **Pasūtījuma nosūtīšanas statuss** un **Pasūtījuma pieprasījuma kreditora statuss**. Lai iegūtu papildinformāciju par dažādām šīs lapas statusa vērtībām, skatiet šīs tēmas sadaļu [Pirkšanas pasūtījumu pieprasījumu pārraudzīšana](#monitor-po-requests).

![Pirkšanas pasūtījumu apstiprinājumu lapa](media/cxml-po-confirmations.png "Pirkšanas pasūtījumu apstiprinājumu lapa")

Lai skatītu papildinformāciju par dokumentu, atlasiet virs režģa esošo **Pirkšanas pasūtījuma pieprasījums**.

Lapa **Pirkšanas pasūtījuma pieprasījums** ietver divus režģus. Režģim lapas augšdaļā ir viens ieraksts katram pirkšanas pasūtījumam, kas ir atzīmēts nosūtīšanai. Režģim cilnē **Pirkšanas pasūtījuma pieprasījumu vēsture** lapas apakšdaļā var būt vairāki ieraksti atlasītajam pirkšanas pasūtījumam, lai norādītu katra apstiprinājuma statusu. Tālāk esošajā attēlā ir parādīts pirkšanas pasūtījums 00000275 augšējā režģī un dokuments 00000275-1 cilnes **Pirkšanas pasūtījuma pieprasījumu vēsture** režģī.

![Pirkšanas pasūtījuma pieprasījuma lapa](media/cxml-po-request.png "Pirkšanas pasūtījuma pieprasījuma lapa")

Ja pakešuzdevums ir iestatīts un palaists, dokuments tiks nosūtīts. Statusa izmaiņas var skatīt pēc dokumenta nosūtīšanas. Tālāk esošajā attēlā lauks **Pasūtījuma nosūtīšanas statuss** ir iestatīts uz _Nosūtīts_. Lauks **Pasūtījuma pieprasījuma kreditora statuss** ir iestatīts uz _Apstiprināts_, lai norādītu, ka kreditors ir saņēmis dokumentu, un spēja to izlasīt un saglabāt savā sistēmā. Režģī cilnē **Pirkšanas pasūtījuma pieprasījumu vēsture** tiek rādīts laiks, kad dokuments tika nosūtīts. Lai iegūtu papildinformāciju par dažādām šīs lapas statusa vērtībām, skatiet sadaļu [Pirkšanas pasūtījumu pieprasījumu pārraudzīšana](#monitor-po-requests).

![Statusa ziņojumi pirkšanas pasūtījuma pieprasījuma lapā](media/cxml-po-request-2.png "Statusa ziņojumi pirkšanas pasūtījuma pieprasījuma lapā")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Pirkšanas pasūtījuma pieprasījuma pakešuzdevuma ieplānošana

Lai aktivizētu pakešuzdevumu pirkšanas pasūtījuma pieprasījumu nosūtīšanai, dodieties uz **Sagāde un avoti \> Iestatīšana \> cXML pārvaldība \> Pirkšanas pasūtījuma pieprasījums** un pēc tam darbību rūtī cilnē **Pirkšanas pasūtījuma pieprasījums**, kas atrodas **Pakešuzdevums** grupā, atlasiet **Iesniegt darbu**, lai atvērtu dialoglodziņu **Pirkšanas pieprasījuma sagatavošana un nosūtīšana**. Izmantojot šo dialoglodziņu, varat iestatīt atkārtošanu, tāpat kā to parasti darāt pakešuzdevumiem programmā Supply Chain Management. Atlasiet intervālu, pamatojoties uz pasūtījuma apjomu. Lai gan pakešuzdevumu var palaist katru minūti, tomēr ir ieteicams nosūtīt pakešuzdevumus visas darbadienas laikā, pamatojoties uz pasūtījumu saņemšanas logiem, kas atbilst kreditoru grafikiem.

Piemēram, kreditora politika nosaka, ka visi pasūtījumi, kas tiek saņemti līdz plkst. 13.00, tiks nosūtīti tajā pašā dienā. Šādā gadījumā pakešuzdevums būs jāpalaiž tikai dažas reizes no rīta, lai paziņotu par esošajiem pasūtījumiem. Atlikušie pasūtījumi tiks nosūtīti nākamajā dienā. Šis lēmums ir biznesa lēmums. Varat to pārskatīt un iestatīt tam atbilstošus parametrus.

Process meklēs pirkšanas pasūtījuma pieprasījuma dokumentus ar statusu *Gaida*. Ja jums ir pasūtījums, kas jānosūta kreditoram nekavējoties, varat atlasīt **Iesniegt darbu** un iestatīt opciju **Pakešapstrāde** uz *Nē*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Pirkšanas pasūtījumu pieprasījumu pārraudzīšana

### <a name="view-the-status-of-a-purchase-order"></a>Skatīt pirkšanas pasūtījuma statusu

Kad pasūtījumi, kurus var nosūtīt, izmantojot cXML, tiek apstiprināti, tie pāriet uz statusu _Gaida_. Kā jau aprakstīts sadaļā [Pirkšanas pasūtījuma izveide un apstrāde](#create-po), varat skatīt pirkšanas pasūtījuma statusu lapā **Pirkšanas pasūtījuma pieprasījums**. Katram pirkšanas pasūtījuma pieprasījumam var būt viens no statusiem, atkarībā no tā parametriem un datiem. Šajā sadaļā ir aprakstīti dažādi statusa veidi un vērtības, kas tiem var būt. Šī informācija var palīdzēt pārvaldīt problēmas un saprast jūsu pirkšanas pasūtījumu statusu.

![Pirkšanas pasūtījuma statuss pirkšanas pasūtījuma pieprasījuma lapā](media/cxml-monitor-po-request.png "Pirkšanas pasūtījuma statuss pirkšanas pasūtījuma pieprasījuma lapā")

Režģis, kas atrodas lapas **Pirkšanas pasūtījuma pieprasījums** augšējā daļā, var parādīt šādas statusa vērtības:

- **Pasūtījuma nosūtīšanas statuss** – šim laukam var būt kāda no šīm vērtībām:

    - **Gaida** – dokuments gaida nosūtīšanu.
    - **Nosūtīts** – dokuments ir nosūtīts.
    - **Apturēts** – dokuments tika atzīmēts kā _Apturēts_, pirms tā nosūtīšanas. (Lai atzīmētu dokumentu kā _Apturēts_, atlasiet **Apturēt** darbību rūtī, kas atrodas lapā **Pirkšanas pieprasījums**.)
    - **Arhivēts** — dokuments ir iztīrīts. (Lai iztīrītu dokumentu, atlasiet **Dzēst** darbību rūtī, kas atrodas lapā **Pirkšanas pieprasījums**.)

- **Pasūtījuma pieprasījuma kreditora statuss** – šim laukam var būt kāda no šīm vērtībām:

    - **Gaida** – dokuments gaida nosūtīšanu.
    - **Apstiprināts** – kreditors ir apstiprinājis, ka dokuments ir saņemts. Varat pārskatīt XML ziņojuma informāciju, kas tiek atgriezta no kreditora, atlasot cilni **Atbildes XML** lapas apakšējā daļā.
    - **Kļūda** – dokuments tika nosūtīts kreditoram, bet radās kļūda. Varat pārskatīt kļūdas ziņojumu, atlasot cilni **Atbildes XML** lapas apakšējā daļā.

Režģis **Pirkšanas pasūtījuma pieprasījumu vēsture** cilnē, kas atrodas lapas **Pirkšanas pasūtījuma pieprasījums** apakšējā daļā, var parādīt šādas vērtības:

- **Pasūtījuma pieprasījuma veids** – šim laukam var būt kāda no šīm vērtībām:

    - **Jauns** – rinda tiek atzīmēta kā jauna uzreiz pēc tam, kad pirkšanas pasūtījums ir apstiprināts.
    - **Atjaunināts** – ja apstiprinājumu kreditors jau ir nosūtījis un apstiprinājis, tad nākamais apstiprinājums tiks atzīmēts kā _Atjaunināts_. Atjauninājumi tiks nosūtīti tikai tad, ja opcija **Nosūtīt pirkšanas pieprasījuma atjauninājumus** ir iestatīta uz *Jā* [cXML globālajos parametros](#cxml-parameters).
    - **Dzēsts** – ja apstiprinājumu kreditors jau ir nosūtījis un apstiprinājis, bet pirkšanas pasūtījums ir atcelts, gaidošais apstiprinājums tiks atzīmēts kā _Dzēsts_. Dzēšanai tiks nosūtīts tikai tad, ja opcija **Nosūtīt pirkšanas pieprasījuma dzēšanu** ir iestatīta uz *Jā* [cXML globālajos parametros](#cxml-parameters).

- **Pieprasījuma laiks** – laiks, kad tika izveidots pasūtījuma apstiprinājums. Varat salīdzināt pieprasījuma laiku ar pasūtījuma statusa laiku, lai noteiktu laiku starp apstiprinājumu un kreditora apstiprinājumu.
- **Pasūtījuma nosūtīšanas statuss** – šis lauks ir tāds pats kā lauks **Pasūtījuma nosūtīšanas statuss** lapas augšējā daļā. Šeit tas tiek atkārtots, lai vienkāršotu statusa skatīšanu apstiprināšanas līmenī. Ja lauks **Pasūtījuma pieprasījuma veids** ir iestatīts uz *Jauns* un pirkšanas pasūtījums tiek atkārtoti apstiprināts pirms apstiprinājuma nosūtīšanas, tad lauks **Pasūtījuma nosūtīšanas statuss** tiek iestatīts uz *Arhivēts*.
- **Pasūtījuma statusa laiks** – laiks, kad pēdējoreiz tika atjaunināts pirkšanas pasūtījuma pieprasījuma vēstures ieraksts. (Atjauninājumi ietver statusa izmaiņas.)
- **Pasūtījuma pieprasījuma kreditora statuss** – šis lauks ir tāds pats kā lauks **Pasūtījuma pieprasījuma kreditora statuss** lapas augšējā daļā. Šeit tas tiek atkārtots, lai vienkāršotu statusa skatīšanu apstiprināšanas līmenī.
- **Atkārtotas iesniegšanas laiks** – laiks, kad ieraksts tika iesniegts atkārtoti.
- **Atkārtotu iesniegumu skaits** – ieraksta atkārtotu iesniegumu reižu skaits. Liels skaits norāda vairākas kļūmes, tādējādi, norādot uz problēmu saistībā ar jūsu datu iestatījumiem vai jūsu kreditoru datu iestatījumiem.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Skatīt pirkšanas pasūtījuma pieprasījuma ziņojumu XML

Lai skatītu pirkšanas pasūtījuma pieprasījuma ziņojumu XML, atlasiet cilni **Pieprasījuma XML teksts** lapas **Pirkšanas pasūtījuma pieprasījums** apakšā. Informācija šajā cilnē var būt noderīga pārbaudes vai kļūdas validēšanas laikā. Lai padarītu informāciju vienkāršāk lasāmu, varat to skatīt kā formatētu ziņojumu. Kopējiet cilnes saturu teksta failā un pēc tam skatiet to XML redaktorā.

![Pieprasījuma XML teksta cilne](media/cxml-request-xml-text.png "Pieprasījuma XML teksta cilne")

### <a name="view-the-details-of-the-vendor-response"></a>Skatīt kreditora atbildes informāciju

Lai skatītu kreditora apstiprinājuma vai kļūdas atbildes saturu, atlasiet cilni **Atbildes XML**, kas atrodas lapas **Pirkšanas pasūtījuma pieprasījums** apakšā.

![Atbildes XML cilne](media/cxml-response-xml.png "Atbildes XML cilne")

## <a name="additional-resources"></a>Papildu resursi

- [Ārēja kataloga iestatīšana elektroniskai atzīmēšanas sagādei](set-up-external-catalog-for-punchout.md)
- [Ārējo katalogu izmantošana elektroniskai atzīmēšanas sagādei](use-external-catalogs-for-punchout.md)
