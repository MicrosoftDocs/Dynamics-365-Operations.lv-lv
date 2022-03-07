---
title: Kreditoru sadarbība ar ārējiem kreditoriem
description: Šajā tēmā ir paskaidrots, kā iepirkuma aģenti var sadarboties ar ārējiem kreditoriem, lai apmainītos ar informāciju par pirkšanas pasūtījumiem un sūtījuma krājumiem.
author: Henrikan
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart, PurchaseOrderResponseActionRemarks, PurchVendorPortalAllResponse, PurchOrderInExternalReview, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3b679f8daed1e09c832a5d138473cccba03552f6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576980"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Kreditoru sadarbība ar ārējiem kreditoriem

[!include [banner](../includes/banner.md)]

Modulis **Kreditoru sadarbība** ir paredzēts kreditoriem, kuri neizmanto elektroniskās datu apmaiņas (EDI) integrāciju ar Microsoft Dynamics 365 Supply Chain Management. Tā ļauj kreditoriem strādāt ar pirkšanas pasūtījumiem (purchase order — PO), rēķiniem, sūtījuma krājumu informāciju un piedāvājumu pieprasījumiem (requests for quotation — RFQ), kā arī ļauj kreditoriem piekļūt daļām no saviem kreditora pamatdatiem. Šajā tēmā ir paskaidrots, kā jūs varat sadarboties ar ārējiem kreditoriem, kuri izmanto kreditoru sadarbības interfeisu, lai strādātu ar pirkšanas pasūtījumiem, piedāvājumu pieprasījumiem un sūtījumu krājumiem. Tajā ir arī paskaidrots, kā konkrētam kreditoram sniegt iespēju lietot kreditoru sadarbību un kā definēt informāciju, kuru redz visi kreditori, kad viņi atbild uz kādu pirkšanas pasūtījumu.

Papildinformāciju par to, ko ārējie kreditori var darīt kreditoru sadarbības interfeisā, skatiet tēmā [Kreditoru sadarbība ar debitoriem](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Šajā tēmā sniegtā informācija par kreditoru sadarbību attiecas tikai uz pašreizējo Supply Chain Management versiju. Programmā Microsoft Dynamics AX 7.0 (2016. gada februāris) un Microsoft Dynamics AX programmas versijā 7.0.1 (2016. gada maijs) jūs ar kreditoriem sadarbojaties, izmantojot moduli **Kreditoru portāls**. Informāciju par moduli **Kreditoru portāls** skatiet šeit: [Sadarbība ar kreditoriem, izmantojot moduli Kreditoru portāls](collaborate-vendors-vendor-portal.md).

Papildinformāciju par to, kā kreditori var lietot kreditoru sadarbības rēķinu izrakstīšanas procesus, skatiet tēmā [Kreditoru sadarbības rēķinu izrakstīšanas darbvieta](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). Informāciju par to, kā nodrošināt jauna kreditora sadarbības lietotājus, skatiet tēmā [Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Tās informācijas definēšana, kas tiek rādīta kreditoriem, kad viņi atbild uz pirkšanas pasūtījumiem

Kad kreditori atbild uz kādu viņiem nosūtīto pirkšanas pasūtījumu, šie kreditori redz vienu no trim ziņojuma lodziņiem, kur viņiem ir jāapstiprina tas, ka viņi vēlas pieņemt šo pirkšanas pasūtījumu, noraidīt to vai pieņemt to ar izmaiņām. Tā kā informācija, kas šajā brīdī ir jārāda kreditoram, var būt specifiska jūsu uzņēmumam, varat norādīt, kādu tekstu rādīt katrā no apstiprinājuma ziņojumiem. Piemēram, šis teksts var kreditoru informēt par nākamajām procesa darbībām vai arī par noteikumiem un nosacījumiem.

Lai definētu tekstu, kas tiek rādīts pirkšanas pasūtījuma atbildē, izpildiet tālāk aprakstītās darbības.

1. Lapā **Informācija kreditoriem, kas atbild uz pirkšanas pasūtījumiem** atlasiet atbildes veidu un pēc tam atlasiet **Rediģēt**.
2. Lodziņā **Informācijas ziņojums** ievadiet informāciju, kas ziņojuma lodziņā ir jārāda kreditoriem.

Ja nepieciešams pievienot ziņojumus vairākās valodās, izveidojiet atsevišķus ziņojumus un norādiet katram no tiem atbilstošo valodas kodu. Katram kreditoram rādītais ziņojums būs tajā valodā, kādu šis kreditors izmanto.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Kreditoru sadarbības opciju iestatīšana konkrētam kreditoram

Administrators konfigurē vispārīgos iestatījumus kreditoru sadarbībai, piemēram, drošības lomas, kas ir pieejamas visiem kreditoriem, ar kuriem jūs sadarbojaties. Taču pastāv arī iestatījumi, kas dažādiem kreditoru kontiem var atšķirties. Šos iestatījumus konfigurējat jūs.

- Iespējojiet kreditoru sadarbību.
- Norādiet, vai kreditoram vajadzētu redzēt cenu informāciju.

### <a name="enabling-vendor-collaboration"></a>Kreditoru sadarbības iespējošana

Lai ārējam kreditoram varētu izveidot lietotāju kontus, jums šis kreditora konts ir jākonfigurē, lai attiecīgais kreditors varētu izmantot kreditoru sadarbību. Lapas **Kreditori** cilnē **Vispārīgi** iestatiet lauku **Sadarbības aktivizēšana**. Ir pieejamas tālāk minētās opcijas.

- **Aktīvs (pirkšanas pasūtījums tiek akceptēts automātiski)** — ja kreditors pirkšanas pasūtījumus pieņem bez izmaiņām, šie pirkšanas pasūtījumi tiek akceptēti automātiski.
- **Aktīvs (pirkšanas pasūtījums netiek akceptēts automātiski)** — kad kreditors ir pieņēmis pirkšanas pasūtījumus, jūsu organizācijai šie pirkšanas pasūtījumi ir jāakceptē manuāli.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Norādīšana, vai kreditoram vajadzētu redzēt cenu informāciju

Lai kopīgotu cenas informāciju saistībā ar pirkšanas pasūtījumiem, izmantojot kreditoru sadarbības interfeisu, opcija **Pirkšanas pasūtījuma cenas/summa** cilnē **Pirkšanas pasūtījuma noklusējuma informācija** attiecīgā kreditora kontam ir jāiestata uz **Jā**. Šī cenu informācija ietver vienības cenas, atlaides un izmaksas.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Darbs ar pirkšanas pasūtījumiem, ja tiek izmantota kreditoru sadarbība

### <a name="sending-a-po-to-a-vendor"></a>Pirkšanas pasūtījuma sūtīšana kreditoram

PO tiek sagatavoti programmatūrā Supply Chain Management. Kad pirkšanas pasūtījuma statuss ir **Apstiprināts**, jūs to sūtat kreditoram, atlasot darbību **Sūtīt akceptēšanai** lapā **Pirkšanas pasūtījums**. Pēc tam pirkšanas pasūtījuma statuss mainās uz **Tiek pārskatīts ārēji**. Pēc pirkšanas pasūtījuma nosūtīšanas kreditors to var redzēt kreditoru sadarbības interfeisa lapā **Pārskatāmie pirkšanas pasūtījumi**. Kreditors pirkšanas pasūtījumu var pieņemt, noraidīt to vai ierosināt tā izmaiņas. Kreditors var arī pievienot komentārus, lai darītu zināmu informāciju, piemēram, PO izmaiņas. Ja vēlaties pievērst kreditora uzmanību jaunam pirkšanas pasūtījumam, var izmantot arī drukas pārvaldības sistēmu, lai pirkšanas pasūtījumu nosūtītu pa e-pastu.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Kreditora veikta pirkšanas pasūtījuma akceptēšana un pieņemšana

Kad kreditors pieņem kādu pirkšanas pasūtījumu, šo pirkšanas pasūtījumu var akceptēt automātiski vai to var būt nepieciešams akceptēt manuāli. Šī uzvedība ir atkarīga no tā, vai šim kreditoram lauks **Sadarbības aktivizēšana** ir iestatīts uz **Aktīvs (pirkšanas pasūtījums tiek automātiski akceptēts)** vai uz **Aktīvs (pirkšanas pasūtījums netiek automātiski akceptēts)**.

Nākamajā tabulā ir parādīta tipiska informācijas apmaiņa atkarībā no kreditora atbildes, kad akceptēšanai nosūtāt pirkšanas pasūtījumu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Kreditora atbilde</th>
<th>Rezultāts</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Kreditors <strong>pieņem</strong> pasūtījumu, un programmatūra Supply Chain Management ir konfigurēta tā, lai automātiski akceptētu šī kreditora pieņemtos pirkšanas pasūtījumus.</td>
<td>Pasūtījuma statuss tiek atjaunināts uz <strong>Akceptēts</strong>. Ja kaut kādu iemeslu dēļ pasūtījumu neva&#39;r atjaunināt, kreditora atbilde joprojām tiek ierakstīta kā <strong>Pieņemts</strong>, bet pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>. 

Kreditoram nosūtītais pirkšanas pasūtījums, kura statuss ir <strong>Tiek pārskatīts ārēji</strong>, tiek atjaunināts ar akceptētajiem piegādes datumiem rindās. Šis atjauninājums iniciē jaunu versiju, kas tiek automātiski iestatīta uz statusu <strong>Akceptēts</strong>. Kad pirkšanas pasūtījums ir akceptēts, tas tiek rādīts kreditoru sadarbības interfeisā.</td>
</tr>
<tr class="odd">
<td>Kreditors <strong>pieņem</strong>pasūtījumu, bet Supply Chain Management na&#39;v konfigurēta tā, lai automātiski akceptētu šī kreditora pieņemtos pirkšanas pasūtījumus.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Pieņemts</strong>, bet pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>.

Kreditoram nosūtītais pirkšanas pasūtījums, kura statuss ir <strong>Tiek pārskatīts ārēji</strong>, tiek atjaunināts ar akceptētajiem piegādes datumiem rindās. Šis atjauninājums iniciē jaunu versiju, kas tiek automātiski iestatīta uz statusu <strong>Tiek pārskatīts ārēji</strong>. Pēc tam šo pirkšanas pasūtījumu varat akceptēt manuāli.</td>
</tr>
<tr class="even">
<td>Kreditors <strong>noraida</strong> pasūtījumu.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Noraidīts</strong>, un PP joprojām paliek statuss <strong>Tiek pārskatīts ārēji</strong>. Noraidījums tiek saņemts kopā ar kreditor&#39;a piezīmi.</td>
</tr>
<tr class="odd">
<td>Kreditors <strong>pieņem</strong> pasūtījumu <strong>ar izmaiņām</strong>. Izmaiņas tiek ierosinātas rindas līmenī. Kreditors var pieņemt vai noraidīt atsevišķas rindas. Tālāk ir paradītas vēl dažas izmaiņas, ko kreditors var ierosināt.
<ul>
<li>Mainīt datumus vai daudzumus.</li>
<li>Sadalīt rindas dažādiem piegādes datumiem vai daudzumiem.</li>
<li>Aizstāt kādu krājumu.</li>
</ul>
Kreditors neva&#39;r mainīt preces informāciju un maksas. Taču kreditors var ierosināt šādu izmaiņu veikšanu, izmantojot piezīmes.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Pieņemts ar izmaiņām</strong>, un pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>. Statusi norāda, kāda veida izmaiņas kreditors ir ierosinājis. Lai iegūtu informāciju par izmaiņu automātisko patēriņu, skatiet sadaļu &quot;Pirkšanas pasūtījuma atjaunināšana, kad kreditors iesaka izmaiņas&quot; tālāk šajā tēmā. </td>
</tr>
</tbody>
</table>

Varat izmantot darbvietu **Pirkšanas pasūtījuma sagatavošana**, lai uzraudzītu, uz kuriem pirkšanas pasūtījumiem kreditors ir atbildējis. Šajā darbvietā ietilpst divi tālāk norādītie saraksti, kuros ir pirkšanas pasūtījumi ar statusu **Tiek pārskatīts ārēji**.

- Ārējā pārskatīšanā ir jāveic darbība
- Ārējā pārskatīšanā, gaida kreditora atbildi

### <a name="changing-a-po"></a>Pirkšanas pasūtījuma maiņa

Lai mainītu pirkšanas pasūtījumu, uz kuru kreditors jau ir atbildējis, jums šim kreditoram ir jānosūta jauna pirkšanas pasūtījuma versija. Jaunajam pirkšanas pasūtījumam ir versijas sufikss, lai norādītu, ka tas ir iepriekš nosūtīta pirkšanas pasūtījuma mainīta versija. Lapā **Pirkšanas pasūtījuma kreditora apstiprinājumu vēsture** jūs un jūsu kreditori var izsekot katra pasūtījuma vēsturei. Iepriekš apstiprinātā pirkšanas pasūtījuma versija saglabājas apstiprināto PP sarakstā, līdz tiek apstiprināts jaunais PP.

### <a name="canceling-a-po"></a>Pirkšanas pasūtījumu atcelšana

Kad atceļat kādu pirkšanas pasūtījumu, tā statuss tiek mainīts uz **Apstiprināts**. Šis pirkšanas pasūtījums jums ir jāsūta atpakaļ kreditoram, lai kreditors šo atcelšanu varētu apstiprināt vai noraidīt. Pēc tam, kad atcelšana ir apstiprināta, PP parādās apstiprināto PP kreditora sarakstā kā **Atcelts**.

### <a name="adding-attachments-to-a-po"></a>Pielikumu pievienošana pirkšanas pasūtījumam

Pirkšanas pasūtījumam varat pievienot pielikumus, piemēram, failus, attēlus un piezīmes, izmantojot dokumentu pārvaldības sistēmu. Tipa **Ārējs** pielikumi ir redzami kreditoram, kad sūtat pirkšanas pasūtījumu.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Pirkšanas pasūtījuma atjaunināšana, kad kreditors iesaka izmaiņas

Ja kreditors ir atbildējis uz kādu pirkšanas pasūtījumu un ieteicis izmaiņas, nākamā darbība ir atbildes apstrāde.

Darbvietas **Pirkšanas pasūtījumu sagatavošana** sarakstā **Tiek pārskatīts ārēji, ir jāveic darbība** varat identificēt pirkšanas pasūtījumus, kurus kreditors ir pieņēmis ar izmaiņām. No šī saraksta varat arī pāriet uz kreditora atbildi.

Atbildē kreditors var mainīt tālāk norādīto informāciju virsrakstā.
 
- Kreditora dokumenta atsauce
- Piegādes veids
- Piegādes nosacījumi
- Apstiprinātais piegādes datums

Kreditors var arī pievienot piezīmi vai pielikumu.

Rindās kreditors var mainīt daudzumu un piegādes datumus, pievienot piezīmes un pielikumus, noraidīt rindu, aizstāt rindu ar citu preci, kas ir ievadīta kā teksts, un sadalīt rindu vairākās piegādēs. Rindas statuss ir atkarīgs no tālāk norādītajām kreditora ierosinātajām izmaiņām.
    
- **Apstiprināts ar izmaiņām**
- **Noraidīts**
- **Aizstāts** — šajā gadījumā tiek pievienota papildu rinda ar statusu **Aizstājējs**.
- **Akceptēts**
- **Sadalīts grafikā** — šajā gadījumā tiek pievienotas papildu rindas ar statusu **Grafika rindas**.

Ja rinda ir bez izmaiņām, rindas statuss ir **Pieņemts**.

Atbildē rindas statusi jums norāda, kāda veida izmaiņas kreditors ir veicis. Turklāt visi mainītie lauki tiek rādīti treknrakstā, lai palīdzētu jums identificēt izmaiņas.

Pirkšanas pasūtījumu varat atjaunināt, atbildē vai atsevišķi katrā attiecīgajā rindā atlasot **Apstrādāt pirkšanas pasūtījuma atjauninājumu**. Virsraksta un rindu lauks **Vai pirkšanas pasūtījuma atjauninājums ir apstrādāts?** norāda, vai sistēma ir apstrādājusi virsrakstu vai rindas, lai pirkšanas pasūtījumu atjauninātu ar izmaiņām no atbildes. Darbību **Apstrādāt pirkšanas pasūtījuma atjauninājumu** katram virsrakstam vai rindai varat palaist tikai vienreiz.

Pirkšanas pasūtījumā nevar atjaunināt visas ieteiktās izmaiņas. Pirkšanas pasūtījumā automātiski var veikt tikai atjauninājumus virsrakstā, kā arī datumu un daudzumu atjauninājumus rindās. Lai veiktu citas izmaiņas, jums ir manuāli jāatjaunina pirkšanas pasūtījums. Šajā gadījumā lauka **Vai pirkšanas pasūtījuma atjauninājums ir apstrādāts?** vērtība ir **Manuāls atjauninājums**. Piemēram, ja kreditors ierosina sadalīt kādu rindu grafikā, šīs izmaiņas ir jāveic manuāli.

Visām rindām, kuru statuss ir **Pieņemts**, būs akceptēts piegādes datums. Kad palaižat darbību **Apstrādāt pirkšanas pasūtījuma atjauninājumu**, šis datums tiek atjaunināts uz pirkšanas pasūtījumu. Piezīmes un pielikumi netiek automātiski pārsūtīti uz pašreizējo pirkšanas pasūtījumu. Turklāt tirdzniecības līgumi netiek atkārtoti novērtēti pirkšanas pasūtījuma rindās, kad pašreizējo pirkšanas pasūtījumu atjaunināt, izmantojot darbību **Apstrādāt pirkšanas pasūtījuma atjauninājumu**.

## <a name="po-statuses-and-versions"></a>Pirkšanas pasūtījumu statusi un versijas

Šajā sadaļā ir aprakstīti dažādie statusi, kādi pirkšanas pasūtījumam var būt līdz tā akceptēšanas brīdim. Tajā ir arī aprakstīts, kad jaunās pirkšanas pasūtījuma versijas kļūst pieejamas kreditoram. Process atšķiras atkarībā no tā, vai pirkšanas pasūtījumiem izmantojat izmaiņu pārvaldību. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versijas un statusi, ja nelietojat izmaiņu pārvaldību

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP.

| Darbība | Statuss un versija |
|--------|--------------------|
| Pirkšanas pasūtījuma sākotnējā versija tiek izveidota programmatūrā Supply Chain Management. | Statuss ir **Apstiprināts**. |
| PP tiek nosūtīts kreditoram. | Versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**. |
| Kreditors nosūta atbildi **Pieņemts ar izmaiņām**. | Statuss joprojām ir **Tiek pārskatīts ārēji**. |
| Jūs veicat kreditora pieprasītās izmaiņas. | Statuss tiek mainīts uz **Apstiprināts**. |
| Jūs PP jauno versiju nosūtāt kreditoram. | Jauna versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**. |
| Kreditors pieņem PP jauno versiju. | Statuss joprojām ir **Tiek pārskatīts ārēji**, ja vien kreditora konts nav konfigurēts pirkšanas pasūtījumiem automātiski iestatīt statusu **Akceptēts**, kad kreditors tos pieņem. |

Kreditoriem nav jāakceptē pirkšanas pasūtījums, izmantojot kreditoru sadarbības interfeisu. Viņi var arī nosūtīt e-pasta ziņojumu vai informēt par pirkšanas pasūtījuma pieņemšanu, izmantojot citus kanālus. Pēc tam šo pasūtījumu varat apstiprināt manuāli. Šajā gadījumā jūs saņemat brīdinājumu par pasūtījuma akceptēšanu arī tad, ja nav saņemta atbilde no kreditora. Pēc tam šāds pirkšanas pasūtījums tiek rādīts akceptēšanas vēsturē kā atvērts akceptēts pasūtījums, kuram nav atbilžu. Šajā brīdī kreditoram vairs nav iespējas akceptēt vai noraidīt šo pirkšanas pasūtījumu.

> [!NOTE]
> Pirkšanas pasūtījuma versija, kas ir pieejama citiem Supply Chain Management procesiem, vienmēr ir visjaunākā versija, pat ja šī versija vēl nav reģistrēta kreditoru sadarbības interfeisā.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versijas un statusi, ja lietojat izmaiņu pārvaldību

Ja pirkšanas pasūtījumiem ir iespējota izmaiņu pārvaldība, pirkšanas pasūtījumiem tiek veikta apstiprināšanas darbplūsma, lai sasniegtu statusu **Apstiprināts**. Šis process nav redzams kreditoram.

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP, kad ir aktivizēta izmaiņu pārvaldība. Versija tiek reģistrēta, kad pirkšanas pasūtījums tiek apstiprināts, nevis kad pirkšanas pasūtījums tiek nosūtīts kreditoram vai akceptēts.

| Darbība | Statuss un versija |
|--------|--------------------|
| Pirkšanas pasūtījuma sākotnējā versija tiek izveidota programmatūrā Supply Chain Management. | Statuss ir **Melnraksts**. |
| PP tiek iesniegts apstiprināšanas procesam. (Apstiprināšanas process ir iekšējs process, kurā kreditors nav iesaistīts.) | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja PP nav noraidīts apstiprināšanas procesa laikā. Apstiprināts PP tiek reģistrēts kā versija. | 
| PP tiek nosūtīts kreditoram. | Šī versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**. |
| Jūs veicat dažas kreditora ierosinātās izmaiņas — manuāli vai izmantojot darbību **Apstrādāt pirkšanas pasūtījuma atjauninājumu** atbildē —, lai atjauninātu pirkšanas pasūtījumu. | Statuss tiek mainīts atpakaļ uz **Melnraksts**. |
| PP tiek atkārtoti iesniegts apstiprināšanas procesam. | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja PP nav noraidīts apstiprināšanas procesa laikā. Vai arī sistēmu var konfigurēt, lai noteiktu lauku izmaiņām nebūtu nepieciešams atkārtots apstiprinājums. Šajā gadījumā statuss vispirms tiek mainīts uz **Melnraksts** un pēc tam tiek automātiski atjaunināts uz **Apstiprināts**. Apstiprinātais PP tiek reģistrēts kā jauna versija. |
| Jūs PP jauno versiju nosūtāt kreditoram. | Jaunā versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**. |
| Kreditors apstiprina PP jauno versiju. | Statuss tiek mainīts uz **Akceptēts** automātiski vai saņemot atbildi no kreditora un pēc tam akceptējot PP. |

## <a name="sharing-information-about-consignment-inventory"></a>Informācijas kopīgošana par sūtījuma krājumiem

Ja izmantojat sūtījuma krājumus, kreditori var izmantot kreditoru sadarbības interfeisu, lai skatītu informāciju tālāk norādītajās lapās.

- **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi** — pirkšanas pasūtījumi par sūtījuma krājumiem tiek ģenerēti, kad krājumu īpašumtiesības no kreditora tiek mainītas uz jūsu uzņēmumu. Tajā pašā laikā tiek grāmatota preču ieejas plūsma. Šie sūtījuma pirkšanas pasūtījumi tiek rādīti tikai lapā **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi**. Tie netiek iekļauti moduļa **Kreditoru sadarbība** lapā **Visi akceptētie pirkšanas pasūtījumi**.
- **No sūtījuma krājumiem saņemtās preces** — šajā lapā ir uzskaitītas visas transakcijas, kur preču īpašumtiesības no kreditora tiek nodotas jūsu uzņēmumam. Kreditori var izmantot šo informāciju, lai debitoram izrakstītu rēķinu.
- **Rīcībā esošie sūtījuma krājumi** — šajā lapā tiek rādīti kreditoram piederošie rīcībā esošie sūtījuma krājumi, kas ir saņemti jūsu noliktavā.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Darbs ar piedāvājumu pieprasījumiem, ja izmantojat kreditoru sadarbību

Šajā sadaļā ir aprakstītas mijiedarbības starp debitoriem un kreditoriem piedāvājumu pieprasījumu procesa laikā. Tajā ir arī paskaidrots veids, kāda kreditoriem tiek nodota informācija. Pamata apskatu par atbalstu PP procesam skatiet šeit: [Piedāvājumu pieprasījumu (PP) pārskats](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternatīvas, pielikumi, grozījumi un atgriešanas

- **Alternatīvas** — piedāvājuma pieprasījuma gadījuma virsrakstā varat norādīt alternatīvas, kādas ir atļautas katalogā neesošo krājumu rindām. Ja alternatīvas ir iespējotas, kreditori var pievienot alternatīvu rindu katrai pieprasītajai rindai.
- **Pielikumi** — pielikumus piedāvājuma pieprasījuma gadījumam var pievienot gan virsraksta līmenī, gan rindas līmenī. Pielikumus var klasificēt kā iekšējos vai ārējos. Iekšējos pielikumus var skatīt tikai debitora pusē, bet ārējos pielikumus pēc to nosūtīšanas kreditori var apskatīt.

    Kreditori savai atbildei uz piedāvājumu var arī pievienot pielikumus. Šos pielikumus var skatīt debitora pusē, kad kreditors ir iesniedzis atbildi uz piedāvājumu. Kreditoru pievienotie pielikumi vienmēr tiek klasificēti kā ārēji. Lai piekļūtu pielikumam, kuru kreditors ir iesniedzis kopā ar piedāvājumu, atlasiet **Piedāvājuma pielikumi** vai **Piedāvājuma rindas pielikumi**.
    
    Lai atvērtu pielikumus, kas tika nosūtīti kopā ar piedāvājuma pieprasījuma gadījumu, izmantojiet dokumentu apstrādes papīra saspraudes simbolu uz atbildes.

- **Grozījumi** — kad grozījums ir finalizēts, esošās piedāvājuma atbildes tiek noņemtas, lai tās varētu aizstāt ar atjauninātajām vērtībām. Tādu informāciju kā rindas cena un daudzums no iepriekšējām piedāvājuma atbildēm var apskatīt, izmantojot žurnālus par piedāvājuma pieprasījuma gadījumu.

    Lai uzsāktu grozījuma apstrādi, lapas **Sagādes un avotu parametri** kopsavilkuma cilnē **Piedāvājumu pieprasījumi** opciju **Bloķēt piedāvājumu pieprasījumus pēc to nosūtīšanas** iestatiet uz **Jā**. (Šī opcija ir iestatīta, un publiskā sektora konfigurācijai tā ir obligāta.)

- **Atgriešanas** — ja kreditors ir iesniedzis kādu piedāvājumu, bet šim piedāvājuma pieprasījuma gadījumam ir nepieciešama papildinformācija vai informācijas modificēšana, debitors šo piedāvājumu var atgriezt kreditoram. Dati no iepriekš iesniegtā piedāvājuma tiek paturēti, un kreditors var veikt pieprasītās modifikācijas, nesākot piedāvājuma izteikšanas procesu no jauna.

## <a name="public-sector-extensions"></a>Publiskā sektora paplašinājumi

Publiskā sektora paplašinātā funkcionalitāte ļauj piedāvājuma pieprasījuma gadījumu nosūtīt kreditoriem un publicēt. Kad publicējat kādu piedāvājuma pieprasījumu, ikviens, kas šo informāciju pieprasa, var skatīt darbu, kas atbilst vairumam publiskā sektora noteikumu. Viss pieejamais darbs tiek atspoguļots saraksta lapā **Atvērtie publicētie piedāvājumu pieprasījumi**, un atceltos, gaidošos vai piešķirtos piedāvājumu pieprasījumus var skatīt saraksta lapā **Slēgtie publicētie piedāvājumu pieprasījumi**. Šos dokumentus var skatīt arī vietnē ārpus programmatūras Supply Chain Management, izmantojot integrāciju ar tālāk norādītajiem datu elementiem.

- Publicētie piedāvājumu pieprasījumi
- Publicētā piedāvājuma pieprasījumu rinda
- Publicētie piedāvājuma pieprasījumu virsrakstu pielikumi

Šie elementi pieejamos un slēgtos darbus ļauj skatīt personām, kuras nav nodrošināti lietotāji programmatūrā Supply Chain Management, bet kurām ir anonīma piekļuve ārējai vietnei. Turklāt lietotājam, kurš iestata parametrus piedāvājuma pieprasījuma procesam, paplašinātā funkcionalitāte sadaļā **Sūtīt un publicēt** ļauj definēt e-pasta ziņojuma veidni. Kad sagādes speciālists ir izveidojis piedāvājuma pieprasījuma gadījumu, šim speciālistam ir jāatlasa e-pasta ziņojuma veidne, lai kreditoriem sūtītu nepieciešamo informāciju saistībā ar šo piedāvājuma pieprasījuma gadījumu. 

Lietotājs, kurš iestata piedāvājuma pieprasījuma procesa parametrus, var izveidot vairākas e-pasta ziņojumu veidnes. Šajās e-pasta ziņojumu veidnēs var būt gan statisks teksts, gan tālāk norādītie aizstāšanas marķieri. E-pasta ziņojuma veidošanas laikā šie marķieri tiks aizstāti ar konteksta vērtībām.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Ja ir neieciešams kāds grozījums, un tas tiek nosūtīts pēc piedāvājuma pieprasījuma nosūtīšanas, šis piedāvājuma pieprasījums tiek atkārtoti nosūtīts visiem uzaicinātajiem kreditoriem. Publicētais dokuments tiek arī atjaunināts lapā **Atvērtie publicētie piedāvājumu pieprasījumi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]