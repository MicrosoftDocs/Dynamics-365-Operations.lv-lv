---
title: "Kreditoru sadarbība ar ārējiem kreditoriem"
description: "Šajā tēmā ir aprakstīts, kā iepirkuma aģenti var sadarboties ar ārējiem kreditoriem, lai apmainītos ar informāciju par pirkšanas pasūtījumiem un sūtījuma krājumiem."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c8947f9335b3a2de83ab00bad1043ee14d35f2c8
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Kreditoru sadarbība ar ārējiem kreditoriem

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā iepirkuma aģenti var sadarboties ar ārējiem kreditoriem, lai apmainītos ar informāciju par pirkšanas pasūtījumiem un sūtījuma krājumiem.

Modulis **Kreditoru sadarbība** ir paredzēts kreditoriem, kuri neizmanto elektroniskās datu apmaiņas (EDI) integrāciju ar Microsoft Dynamics 365 for Operations. Tas kreditoriem ļauj strādāt ar pirkšanas pasūtījumu, rēķinu un sūtījuma krājumu informāciju. Šajā tēmā ir aprakstīts, kā jūs varat sadarboties ar ārējiem kreditoriem, kuri izmanto kreditoru sadarbības interfeisu, lai strādātu ar pirkšanas pasūtījumiem un sūtījumu krājumiem. Tajā ir arī aprakstīts, kā konkrētam kreditoram sniegt iespēju lietot kreditoru sadarbību un kā definēt informāciju, kuru redz visi kreditori, kad viņi atbild uz kādu pirkšanas pasūtījumu. Papildinformāciju par to, ko ārējie kreditori var darīt kreditoru sadarbības interfeisā, skatiet tēmā [Kreditoru sadarbība ar debitoriem](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Papildinformāciju par to, kā kreditori var lietot kreditoru sadarbības rēķinu izrakstīšanas procesus, skatiet tēmā [Kreditoru sadarbības rēķinu izrakstīšanas darbvieta](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Informāciju par to, kā nodrošināt jauna kreditora sadarbības lietotājus, skatiet tēmā [Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Definēt informāciju, kas tiek rādīta kreditoriem, kad viņi atbild uz pirkšanas pasūtījumiem
Kad kreditori atbild uz kādu pirkšanas pasūtījumu, kurus viņiem nosūtat, viņi redz dialoglodziņu, kur ir nepieciešams apstiprināt, ka viņi vēlas pieņemt, noraidīt vai pieņemt šo pirkšanas pasūtījumu ar izmaiņām. Informācija, ko šajā brīdī ir nepieciešams rādīt kreditoram, var būt jūsu uzņēmumam specifiska, tāpēc varat norādīt, kādu tekstu rādīt katrā no šiem trim apstiprinājuma ziņojumiem. Piemēram, šis teksts varētu kreditoru informēt par nākamajām šī procesa darbībām vai par noteikumiem un nosacījumiem.  

Lai definētu tekstu, kas tiek rādīts pirkšanas pasūtījuma atbildē, rīkojieties tālāk aprakstītajā veidā.

1.  Atveriet lapu **Informācija kreditoriem, kas atbild uz PP**.
2.  Atlasiet vienu no atbildes tipiem.
3.  Noklikšķiniet uz **Rediģēt.**
4.  Lodziņā **Informācijas ziņojums** ievadiet informāciju, kuru vēlaties rādīt kreditoriem.

Ja nepieciešams pievienot ziņojumus vairākās valodās, izveidojiet atsevišķus ziņojumus ar atbilstošajiem valodu kodiem. Kreditoram tiks rādīts ziņojums tajā valodā, ko šis kreditors izmanto.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Iestatīt kreditoru sadarbības opcijas konkrētam kreditoram
Kreditoru sadarbības vispārīgos iestatījumus programmā Dynamics 365 for Operations konfigurē administrators. Piemēram, viņi nosaka, kuras drošības lomas ir pieejamas visiem kreditoriem, ar kuriem jūs sadarbojaties. Pastāv arī daži tālāk aprakstītie iestatījumi, kas dažādiem kreditoru kontiem var atšķirties, un šie iestatījumi ir jāiestata jums.

-   Iespējojiet kreditoru sadarbību.
-   Izlemiet, vai vēlaties, lai kreditors redzētu informāciju par cenu.

### <a name="enable-vendor-collaboration"></a>Iespējot kreditoru sadarbību

Lai ārējam kreditoram varētu izveidot lietotāju kontus, jums šis kreditora konts ir jākonfigurē, lai kreditoram ļautu lietot kreditoru sadarbību. Lai to izdarītu, lapas **Kreditori** cilnē **Vispārīgi** lauku **Sadarbības aktivizēšana** iestatiet kā aktīvu. Varat izvēlēties no divām tālāk aprakstītajām opcijām.

-   **Aktīvs (PP tiek akceptēts automātiski)**— kad kreditors pirkšanas pasūtījumus pieņem bez izmaiņām, šie pirkšanas pasūtījumi tiek akceptēti automātiski.
-   **Aktīvs (PP netiek akceptēts automātiski)**— kad kreditors ir pieņēmis pirkšanas pasūtījumus, jūsu organizācijai šie pirkšanas pasūtījumi ir jāakceptē manuāli.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Izlemt, vai vēlaties, lai kreditors redzētu informāciju par cenu

Ja sadarbības saskarnē vēlaties kopīgot informāciju par cenu, piemēram, vienības cenu, atlaides un maksas, tad kreditora kontā opcijai **Pirkšanas pasūtījumu cenas/summa** ir jānorāda vērtība **Jā**. Šī opcija ir pieejama cilnē **Pirkšanas pasūtījuma noklusējuma informācija**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Darbs ar pirkšanas pasūtījumiem, izmantojot kreditoru sadarbību
### <a name="sending-a-po-to-the-vendor"></a>Pirkšanas pasūtījuma sūtīšana kreditoram

Pirkšanas pasūtījumi tiek sagatavoti programmā Dynamics 365 for Operations. Kad pirkšanas pasūtījuma statuss ir **Apstiprināts**, jūs to sūtat kreditoram, izmantojot darbību **Sūtīt apstiprināšanai** lapā **Pirkšanas pasūtījums**. Pirkšanas pasūtījuma statuss mainās uz **Tiek pārskatīts ārēji**. Pēc pirkšanas pasūtījuma nosūtīšanas kreditors to var redzēt kreditoru sadarbības interfeisa lapā **Pārskatāmie pirkšanas pasūtījumi**, kur kreditors pasūtījumu var pieņemt, noraidīt vai ierosināt tā izmaiņas. Kreditors var arī pievienot komentārus, lai darītu zināmu informāciju, piemēram, PO izmaiņas. Ja vēlaties pievērst kreditora uzmanību jaunam PP, var izmantot arī drukas pārvaldības sistēmu, lai nosūtītu PP pa e-pastu.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Kreditora veikta pirkšanas pasūtījuma apstiprināšana un pieņemšana

Kad kreditors ir pieņēmis kādu pirkšanas pasūtījumu, šis pirkšanas pasūtījums var tikt akceptēts automātiski, vai var būt nepieciešams to akceptēt manuāli. Tas ir atkarīgs no tā, vai lauks **Kreditora aktivizēšana** šim kreditoram ir iestatīts uz **Aktīvs (PP tiek akceptēts automātiski)** vai uz **Aktīvs (PP netiek akceptēts automātiski)**.  

Nākamajā tabulā ir parādīta tipiska informācijas apmaiņa, atkarībā no tā, kā kreditors atbild, kad apstiprināšanai nosūtat pirkšanas pasūtījumu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kreditora atbilde</strong></td>
<td><strong>Rezultāts</strong></td>
</tr>
<tr class="even">
<td>Kreditors <strong>pieņem</strong> pasūtījumu. Programma Dynamics 365 for Operations ir konfigurēta automātiski apstiprināt pirkšanas pasūtījumus, kad šis kreditors tos pieņem.</td>
<td>Pasūtījuma statuss tiek atjaunināts uz <strong>Akceptēts</strong>. Ja kaut kas liedz šo pasūtījumu atjaunināt, tad kreditora atbilde joprojām tiek ierakstīta kā <strong>Pieņemts</strong>, bet pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>.</td>
</tr>
<tr class="odd">
<td>Kreditors <strong>pieņem</strong> pasūtījumu. Programma Dynamics 365 for Operations nav konfigurēta automātiski apstiprināt pirkšanas pasūtījumus, kad šis kreditors tos pieņem.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Pieņemts</strong>, bet pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>.</td>
</tr>
<tr class="even">
<td>Kreditors <strong>noraida</strong> pasūtījumu.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Noraidīts</strong>, un PP joprojām paliek statuss <strong>Tiek pārskatīts ārēji</strong>. Noraidījums tiek saņemts kopā ar kreditoru piezīmi.</td>
</tr>
<tr class="odd">
<td>Kreditors <strong>pieņem pasūtījumu ar izmaiņām</strong>. Izmaiņas tiek ierosinātas rindas līmenī. Iespējams pieņemt vai noraidīt atsevišķas rindas. Tostarp ir iespējamas citas tālāk uzskaitītās izmaiņas.
<ul>
<li>Datumu vai daudzumu maiņa.</li>
<li>Rindu sadalīšana dažādiem piegādes datumiem vai daudzumiem.</li>
<li>Kāda krājuma aizstāšana.</li>
</ul>
Kreditors nevar mainīt preces informāciju un maksas. Ierosinājumus par to izmaiņām var veikt, izmantojot piezīmes.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Pieņemts ar izmaiņām</strong>, <strong></strong>un pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>.</td>
</tr>
</tbody>
</table>

Varat izmantot darbvietu **Pirkšanas pasūtījuma** **sagatavošana**, lai uzraudzītu, uz kuriem pirkšanas pasūtījumiem kreditors ir atbildējis. Šajā darbvietā ietilpst divi tālāk norādītie saraksti, kuros ir pirkšanas pasūtījumi ar statusu **Tiek pārskatīts ārēji**.

-   Tiek pārskatīts ārēji, ir jāveic darbība.
-   Tiek pārskatīts ārēji, gaida kreditora atbildi.

### <a name="changing-a-po"></a>Pirkšanas pasūtījuma maiņa

Kad ir nepieciešams mainīt pirkšanas pasūtījumu, uz kuru jau ir atbildēts, jūs kreditoram nosūtat jaunu šī pirkšanas pasūtījuma versiju. Jaunam PP ir versijas sufikss, lai norādītu, ka tas ir iepriekš nosūtīta PP mainīta versija. Lapā **Pirkšanas pasūtījuma kreditora apstiprinājumu vēsture** jūs un jūsu kreditori var izsekot katra pasūtījuma vēsturei. Iepriekš akceptētā pirkšanas pasūtījuma versija saglabājas akceptēto PP sarakstā, līdz tiek akceptēts jaunais PP.

### <a name="cancelling-a-po"></a>Pirkšanas pasūtījumu atcelšana

Kad atceļat kādu pirkšanas pasūtījumu, tā statuss tiek mainīts uz **Apstiprināts**. Jums ir jāsūta PP atpakaļ kreditoram, izmantojot kreditoru portālu, lai tas varētu apstiprināt vai noraidīt atcelšanu. Kad atcelšana ir apstiprināta, šis pirkšanas pasūtījums kreditora akceptēto pirkšanas pasūtījumu sarakstā tiek rādīts kā **Atcelts**.

### <a name="adding-attachments-to-a-po"></a>Pielikumu pievienošana pirkšanas pasūtījumam

Pirkšanas pasūtījumam varat pievienot pielikumus, piemēram, failus, attēlus un piezīmes, izmantojot dokumentu pārvaldības sistēmu. Pielikumi, kas ir pievienoti ar tipa **Ārējs** ierobežojumu, ir redzami kreditoram, kad šim kreditoram sūtat pirkšanas pasūtījumu.

## <a name="purchase-order-statuses-and-versions"></a>Pirkšanas pasūtījumu statusi un versijas
Šajā sadaļā ir aprakstīti dažādie statusi, kas pirkšanas pasūtījumam var būt līdz brīdim, kad pasūtījums tiek akceptēts, un kurā brīdī pirkšanas pasūtījuma jaunā versija kļūst pieejama kreditoram. Šajā ziņā pastāv atšķirības atkarībā no tā, vai pirkšanas pasūtījumiem jūs izmantojat izmaiņu pārvaldību. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versijas un statusi, ja nelietojat izmaiņu pārvaldību

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Darbība**                                                               | **Statuss un versija**                                                                                                                                       |
| PP sākotnējā versija tiek izveidota programmā Dynamics 365 for Operations. | Statuss ir **Apstiprināts**.                                                                                                                                  |
| PP tiek nosūtīts kreditoram.                                            | Versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                          |
| Kreditors nosūta atbildi **Pieņemts ar izmaiņām**.                  | Statuss joprojām ir **Tiek pārskatīts ārēji**.                                                                                                                  |
| Jūs veicat izmaiņas pēc kreditora pieprasījuma.                  | Statuss tiek mainīts uz **Apstiprināts**.                                                                                                                        |
| Jūs PP jauno versiju nosūtāt kreditoram.                        | Jauna versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                      |
| Kreditors pieņem PP jauno versiju.                            | Statuss joprojām ir **Tiek pārskatīts ārēji**, ja vien kreditora konts nav konfigurēts pirkšanas pasūtījumu automātiski iestatīt uz **Akceptēts**, kad kreditors to pieņem. |

Kreditoriem nav jāapstiprina pirkšanas pasūtījums, izmantojot kreditoru sadarbības interfeisu. Tie var arī nosūtīt e-pasta ziņojumu vai informēt par PP pieņemšanu, izmantojot citus kanālus. Pēc tam pasūtījumu varat apstiprināt manuāli programmā Dynamics 365 for Operations. Tādā gadījumā jūs saņemat brīdinājumu, ka pasūtījums tiek akceptēts, lai gan nav atbildes no kreditora. Pēc tam PP tiek parādīts apstiprināšanas vēsturē kā atvērts akceptēts pasūtījums, kuram nav atbilžu. Kreditoram vairs nav iespējas apstiprināt vai noraidīt šo PP.  

**Piezīme.** PO versija, kas ir pieejama citiem procesiem programmā Dynamics 365 for Operations, vienmēr ir jaunākā versija, pat ja šī versija vēl nav reģistrēta kreditoru sadarbības interfeisā.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versijas un statusi, ja lietojat izmaiņu pārvaldību

Ja pirkšanas pasūtījumiem ir iespējota izmaiņu pārvaldība, tad pirkšanas pasūtījumiem tiek veikta apstiprināšanas darbplūsma, lai sasniegtu statusu **Apstiprināts**. Šis process kreditoram nav redzams.  

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP, kad ir aktivizēta izmaiņu pārvaldība. Versija tiek reģistrēta, kad PP tiek apstiprināts, nevis kad PP tiek nosūtīts kreditoram vai akceptēts.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Darbība**                                                                                                    | **Statuss un versija**                                                                                                                                                                                                                                                                                                                                                                      |
| PP sākotnējā versija tiek izveidota programmā Dynamics 365 for Operations.                                      | Statuss ir **Melnraksts**.                                                                                                                                                                                                                                                                                                                                                                    |
| PP tiek iesniegts apstiprināšanas procesam. (Tas ir iekšējs process, kurā kreditors nav iesaistīts.) | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja PP netiek noraidīts apstiprināšanas procesa laikā. Apstiprināts PP tiek reģistrēts kā versija.                                                                                                                                                                                                                     |
| PP tiek nosūtīts kreditoram                                                                                  | Šī versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                                                                                                                                                                                                                                                       |
| Jūs veicat izmaiņas pēc kreditora pieprasījuma.                                                       | Statuss tiek mainīts atpakaļ uz **Melnraksts**.                                                                                                                                                                                                                                                                                                                                                    |
| PP tiek atkārtoti iesniegts apstiprināšanas procesam.                                                            | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja PP netiek noraidīts apstiprināšanas procesa laikā. Ja vēlaties, sistēmu var konfigurēt tā, lai noteiktu lauku izmaiņām nebūtu nepieciešams atkārtots apstiprinājums. Šajā gadījumā statuss vispirms tiek mainīts uz **Melnraksts** un pēc tam tiek automātiski atjaunināts uz **Apstiprināts**. Apstiprinātais PP tiek reģistrēts kā jauna versija. |
| Jūs PP jauno versiju nosūtāt kreditoram.                                                             | Jaunā versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                                                                                                                                                                                                                                                   |
| Kreditors apstiprina PP jauno versiju.                                                                | Statuss tiek mainīts uz **Akceptēts** automātiski vai saņemot atbildi no kreditora un pēc tam akceptējot PP.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Kopīgot informāciju par sūtījuma krājumiem
Ja izmantojat sūtījuma krājumus, tad kreditori var izmantot kreditoru sadarbības interfeisu, lai skatītu informāciju tālāk norādītajās lapās.

-   **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi** — pirkšanas pasūtījumi par sūtījuma krājumiem tiek ģenerēti, kad krājumu īpašumtiesības mainās no kreditora uz jūsu uzņēmumu. Tajā pašā laikā tiek grāmatota preču ieejas plūsma. Šie sūtījuma pirkšanas pasūtījumi tiek rādīti tikai lapā **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi**. Tie nav iekļauti moduļa **Kreditoru sadarbība** lapā **Visi akceptētie pirkšanas pasūtījumi**.
-   **No sūtījuma krājumiem saņemtās preces** — šajā lapā ir uzskaitītas visas transakcijas, kur preces īpašumtiesības no kreditora tiek nodotas jūsu uzņēmumam. Kreditori var izmantot šo informāciju, lai debitoram izrakstītu rēķinu.
-   **Rīcībā esošie sūtījuma krājumi** — šajā lapā tiek rādīti kreditoram piederošie rīcībā esošie sūtījuma krājumi, kas ir saņemti jūsu noliktavā.





