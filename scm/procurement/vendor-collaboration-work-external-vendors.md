---
title: "Kreditoru sadarbība ar ārējiem kreditoriem"
description: "Šajā tēmā ir aprakstīts, kā iepirkuma aģenti var sadarboties ar ārējiem kreditoriem, lai apmainītos ar informāciju par pirkšanas pasūtījumiem un sūtījuma krājumiem."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.sourcegitcommit: b0aefc62f2d54da963f03dc74d492260722cd451
ms.openlocfilehash: aabb8277218895566edada3c74d99c02a83dae1e
ms.contentlocale: lv-lv
ms.lasthandoff: 06/15/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Kreditoru sadarbība ar ārējiem kreditoriem

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā iepirkuma aģenti var sadarboties ar ārējiem kreditoriem, lai apmainītos ar informāciju par pirkšanas pasūtījumiem un sūtījuma krājumiem.

Modulis **Kreditoru sadarbība** ir paredzēts kreditoriem, kuri neizmanto elektroniskās datu apmaiņas (EDI) integrāciju ar Microsoft Dynamics 365 for Finance and Operations. Tas kreditoriem ļauj strādāt ar pirkšanas pasūtījumu, rēķinu un sūtījuma krājumu informāciju. Šajā tēmā ir aprakstīts, kā jūs varat sadarboties ar ārējiem kreditoriem, kuri izmanto kreditoru sadarbības interfeisu, lai strādātu ar pirkšanas pasūtījumiem un sūtījumu krājumiem. Tajā ir arī aprakstīts, kā konkrētam kreditoram sniegt iespēju lietot kreditoru sadarbību un kā definēt informāciju, kuru redz visi kreditori, kad viņi atbild uz kādu pirkšanas pasūtījumu. Papildinformāciju par to, ko ārējie kreditori var darīt kreditoru sadarbības interfeisā, skatiet tēmā [Kreditoru sadarbība ar debitoriem](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Papildinformāciju par to, kā kreditori var lietot kreditoru sadarbības rēķinu izrakstīšanas procesus, skatiet tēmā [Kreditoru sadarbības rēķinu izrakstīšanas darbvieta](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Informāciju par to, kā nodrošināt jauna kreditora sadarbības lietotājus, skatiet tēmā [Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md).

Papildinformāciju par to, kā kreditori var lietot kreditoru sadarbības rēķinu izrakstīšanas procesus, skatiet tēmā [Kreditoru sadarbības rēķinu izrakstīšanas darbvieta](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

Informāciju par to, kā nodrošināt jauna kreditora sadarbības lietotājus, skatiet tēmā [Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Tās informācijas definēšana, kas tiek rādīta kreditoriem, kad viņi atbild uz pirkšanas pasūtījumiem
Kad kreditori atbild uz kādu viņiem nosūtīto pirkšanas pasūtījumu, viņi redz ziņojuma lodziņu, kurā viņiem ir jāapstiprina tas, ka viņi vēlas pieņemt pirkšanas pasūtījumu, noraidīt to vai pieņemt to ar izmaiņām. Tā kā informācija, kas šajā brīdī ir jārāda kreditoram, var būt specifiska jūsu uzņēmumam, varat norādīt, kādu tekstu rādīt katrā no trīs apstiprinājuma ziņojumiem. Piemēram, šis teksts var kreditoru informēt par nākamajām procesa darbībām vai arī par noteikumiem un nosacījumiem.  

Lai definētu tekstu, kas tiek rādīts pirkšanas pasūtījuma atbildē, rīkojieties tālāk aprakstītajā veidā.

1.  Atveriet lapu **Informācija kreditoriem, kas atbild uz PP**.
2.  Atlasiet vienu no atbildes tipiem.
3.  Noklikšķiniet uz **Rediģēt**.
4.  Lodziņā **Informācijas ziņojums** ievadiet informāciju, kuru vēlaties rādīt kreditoriem.

Ja nepieciešams pievienot ziņojumus vairākās valodās, izveidojiet atsevišķus ziņojumus un norādiet katram no tiem atbilstošos valodu kodus. Kreditoram rādītais ziņojums būs tajā valodā, ko šis kreditors izmanto.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Iestatīt kreditoru sadarbības opcijas konkrētam kreditoram
Kreditoru sadarbības vispārīgos iestatījumus programmatūrā Finance and Operations konfigurē administrators. Piemēram, administrators nosaka, kuras drošības lomas ir pieejamas visiem kreditoriem, ar kuriem sadarbojaties. Pastāv arī tālāk aprakstītie iestatījumi, kas dažādiem kreditoru kontiem var atšķirties, un šie iestatījumi ir jāiestata jums.
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

Pirkšanas pasūtījumi tiek sagatavoti programmatūrā Finance and Operations. Kad pirkšanas pasūtījuma statuss ir **Apstiprināts**, jūs to sūtat kreditoram, izmantojot darbību **Sūtīt apstiprināšanai** lapā **Pirkšanas pasūtījums**. Pirkšanas pasūtījuma statuss mainās uz **Tiek pārskatīts ārēji**. Pēc pirkšanas pasūtījuma nosūtīšanas kreditors to var redzēt kreditoru sadarbības interfeisa lapā **Pārskatāmie pirkšanas pasūtījumi**. Kreditors pasūtījumu var pieņemt, noraidīt to vai ierosināt tā izmaiņas. Kreditors var arī pievienot komentārus, lai darītu zināmu informāciju, piemēram, PO izmaiņas. Ja vēlaties pievērst kreditora uzmanību jaunam PP, var izmantot arī drukas pārvaldības sistēmu, lai nosūtītu PP pa e-pastu.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Kreditora veikta pirkšanas pasūtījuma apstiprināšana un pieņemšana

Kad kreditors ir pieņēmis kādu pirkšanas pasūtījumu, šis pirkšanas pasūtījums var tikt akceptēts automātiski, vai var būt nepieciešams to akceptēt manuāli. Tas ir atkarīgs no tā, vai lauks **Kreditora aktivizēšana** ir iestatīts uz **Aktīvs (PP tiek automātiski apstiprināts)** vai uz **Aktīvs (PP netiek automātiski apstiprināts)** šim kreditoram.  

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
<td>Kreditors <strong>pieņem</strong> pasūtījumu. Programmatūra Finance and Operations ir konfigurēta automātiski apstiprināt pirkšanas pasūtījumus, kad kreditors tos pieņem.</td>

<td>Pasūtījuma statuss tiek atjaunināts uz <strong>Akceptēts</strong>. Ja kaut kas liedz šo pasūtījumu atjaunināt, tad kreditora atbilde joprojām tiek ierakstīta kā <strong>Pieņemts</strong>, bet pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>. 

Kreditoram nosūtītais pirkšanas pasūtījums ar statusu **Tiek pārskatīts ārēji** tiek atjaunināts ar apstiprinātajiem piegādes datumiem rindās. Šis atjauninājums iniciē jaunu versiju, kas tiks automātiski atjaunināta uz statusu **Apstiprināts**. Kad pirkšanas pasūtījums būs apstiprināts, tas tiks rādīts kreditora sadarbības interfeisā.</td>
</tr>
<tr class="odd">
<td>Kreditors <strong>pieņem</strong> pasūtījumu. Programmatūra Finance and Operations nav konfigurēta automātiski apstiprināt pirkšanas pasūtījumus, kad kreditors tos pieņem.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Pieņemts</strong>, bet pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>.

Kreditoram nosūtītais pirkšanas pasūtījums ar statusu **Tiek pārskatīts ārēji** tiek atjaunināts ar apstiprinātajiem piegādes datumiem rindās. Šis atjauninājums iniciē jaunu versiju, kas tiks iestatīta uz statusu **Tiek pārskatīts ārēji**. Pēc tam varēsit manuāli apstiprināt pirkšanas pasūtījumu.</td>

</tr>
<tr class="even">
<td>Kreditors <strong>noraida</strong> pasūtījumu.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Noraidīts</strong>, un PP joprojām paliek statuss <strong>Tiek pārskatīts ārēji</strong>. Noraidījums tiek saņemts kopā ar kreditora piezīmi.</td>
</tr>
<tr class="odd">
<td>Kreditors <strong>pieņem pasūtījumu ar izmaiņām</strong>. Izmaiņas tiek ierosinātas rindas līmenī. Iespējams pieņemt vai noraidīt atsevišķas rindas. Tostarp ir iespējamas citas tālāk uzskaitītās izmaiņas.
<ul>
<li>Datumu vai daudzumu maiņa.</li>
<li>Rindu sadalīšana dažādiem piegādes datumiem vai daudzumiem.</li>
<li>Kāda krājuma aizstāšana.</li>
</ul>
Kreditors nevar mainīt preces informāciju un maksas. Ierosinājumus par to izmaiņām var veikt, izmantojot piezīmes.</td>
<td>Kreditora atbilde tiek ierakstīta kā <strong>Pieņemts ar izmaiņām</strong>, un pirkšanas pasūtījuma statuss joprojām ir <strong>Tiek pārskatīts ārēji</strong>. Statusi norāda, kādu tipu izmaiņas iesaka kreditors. Lai iegūtu informāciju par izmaiņu automātisko patēriņu, skatiet tālāk esošo sadaļu par to, kā atjaunināt pirkšanas pasūtījumu, kad kreditors iesaka izmaiņas. </td>
</tr>
</tbody>
</table>

Varat izmantot darbvietu **Pirkšanas pasūtījuma** **sagatavošana**, lai uzraudzītu, uz kuriem pirkšanas pasūtījumiem kreditors ir atbildējis. Šajā darbvietā ietilpst divi tālāk norādītie saraksti, kuros ir pirkšanas pasūtījumi ar statusu **Tiek pārskatīts ārēji**.

-   Tiek pārskatīts ārēji, ir jāveic darbība.
-   Tiek pārskatīts ārēji, gaida kreditora atbildi.

### <a name="changing-a-po"></a>Pirkšanas pasūtījuma maiņa

Lai mainītu pirkšanas pasūtījumu, uz kuru jau ir atbildēts, jums kreditoram ir jānosūta jauna pirkšanas pasūtījuma versija. Jaunam PP ir versijas sufikss, lai norādītu, ka tas ir iepriekš nosūtīta PP mainīta versija. Lapā **Pirkšanas pasūtījuma kreditora apstiprinājumu vēsture** jūs un jūsu kreditori var izsekot katra pasūtījuma vēsturei. Iepriekš apstiprinātā pirkšanas pasūtījuma versija saglabājas apstiprināto PP sarakstā, līdz tiek apstiprināts jaunais PP.

### <a name="cancelling-a-po"></a>Pirkšanas pasūtījumu atcelšana

Kad atceļat kādu pirkšanas pasūtījumu, tā statuss tiek mainīts uz **Apstiprināts**. Jums ir jāsūta PP atpakaļ kreditoram, izmantojot kreditoru portālu, lai tas varētu apstiprināt vai noraidīt atcelšanu. Kad atcelšana ir apstiprināta, šis pirkšanas pasūtījums kreditora akceptēto pirkšanas pasūtījumu sarakstā tiek rādīts kā **Atcelts**.

### <a name="adding-attachments-to-a-po"></a>Pielikumu pievienošana pirkšanas pasūtījumam

Pirkšanas pasūtījumam varat pievienot pielikumus, piemēram, failus, attēlus un piezīmes, izmantojot dokumentu pārvaldības sistēmu. Tipa **Ārējs** pielikumi ir redzami kreditoram, kad sūtat pirkšanas pasūtījumu.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Pirkšanas pasūtījuma atjaunināšana, kad kreditors iesaka izmaiņas
Ja kreditors ir atbildējis uz pirkšanas pasūtījumu un ieteicis izmaiņas, nākamā darbība ir atbildes apstrāde.
Darbvietas **Pirkšanas pasūtījumu sagatavošanas darbvieta** sarakstā Tiek pārskatīts ārēji, ir jāveic darbība varat identificēt pirkšanas pasūtījumu, uz kuru kreditors atbildēja kā pieņemtu ar izmaiņām. Sarakstā Tiek pārskatīts ārēji, ir jāveic darbība varat arī pāriet uz kreditora atbildi. Atbildē kreditors var mainīt tālāk norādīto informāciju virsrakstā.
 
-   Kreditora dokumenta atsauce
-   Piegādes veids
-   Piegādes nosacījumi
-   Apstiprinātais piegādes datums

Kreditors var arī pievienot piezīmi vai pielikumu

Rindās kreditors var mainīt daudzumu un piegādes datumus, pievienot piezīmes un pielikumus, noraidīt rindu, aizstāt rindu ar citu preci, kas ir ievadīta kā teksts, un sadalīt rindu vairākās piegādēs. Atkarībā no tā, kuras izmaiņas ir ieteicis kreditors, rindas statusam būs dažādas tālāk norādītās vērtības.
    
-   **Pieņemts ar izmaiņām**
-   **Noraidīts**
-   **Aizstāts** Šajā gadījumā tiks pievienota papildu rinda ar statusu **Aizstājējs**.
-   **Apstiprināts** Sadalīts grafikā Šajā gadījumā tiks pievienotas papildu rindas ar statusu **Grafika rindas**.

Ja rinda ir bez izmaiņām, rindas statuss ir **Pieņemts**.

Atbildē varat skatīt iepriekš minētos rindas statusus, kas norāda, kādu tipu izmaiņas ir veicis kreditors. Turklāt visi mainītie lauki tiek rādīti treknrakstā, lai palīdzētu jums identificēt izmaiņas.

Pirkšanas pasūtījumu var atjaunināt, noklikšķinot uz darbības **Apstrādāt PP atjauninājumu** atbildē vai atsevišķi katrā attiecīgajā rindā. Indikators **Vai PP atjauninājums ir apstrādāts?** virsrakstā un rindās ļauj redzēt, vai sistēma ir apstrādājusi virsrakstu vai rindas, lai pirkšanas pasūtījumu atjauninātu ar jebkurām iespējamajām izmaiņām no atbildes. Procesu **Apstrādāt PP atjauninājumu** var palaist tikai vienreiz katram virsrakstam vai rindai.

Pirkšanas pasūtījumā nevar atjaunināt visas ieteiktās izmaiņas. Pirkšanas pasūtījumā automātiski var veikt tikai atjauninājumus virsrakstā, kā arī datumu un daudzumu atjauninājumus rindās. Lai veiktu citas izmaiņas, jums ir manuāli jāatjaunina pirkšanas pasūtījums. Šajā gadījumā indikators **Vai PP atjauninājums ir apstrādāts?** rāda **Manuāls atjauninājums**. Piemērs manuāli apstrādājamām izmaiņām ir situācija, kurā kreditors iesaka sadalīt rindu grafikā.

Rindai ar statusu **Pieņemts** būs apstiprināts piegādes datums, kas pirkšanas pasūtījumā tiks atjaunināts, kad izpildīsit procesu **Apstrādāt PP atjauninājumu**. Piezīmes un pielikumi netiks automātiski pārsūtīti uz pašreizējo pirkšanas pasūtījumu. Ņemiet vērā, ka, atjauninot pašreizējo pirkšanas pasūtījumu, izmantojot darbību **Apstrādāt PP atjauninājumu**, tirdzniecības līgumi netiks atkārtoti novērtēti pirkšanas pasūtījuma rindās.


## <a name="po-statuses-and-versions"></a>Pirkšanas pasūtījumu statusi un versijas
Šajā sadaļā ir aprakstīti dažādie statusi, kas var būt pirkšanas pasūtījumam līdz tā apstiprināšanas brīdim. Tajā ir arī aprakstīts, kurā brīdī jaunās pirkšanas pasūtījuma versijas ir pieejamas kreditoram. Process atšķiras atkarībā no tā, vai pirkšanas pasūtījumiem izmantojat izmaiņu pārvaldību. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versijas un statusi, ja nelietojat izmaiņu pārvaldību

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Darbība**                                                               | **Statuss un versija**                                                                                                                                       |
| Pirkšanas pasūtījuma sākotnējā versija tiek izveidota programmatūrā Finance and Operations. | Statuss ir **Apstiprināts**.                                                                                                                                  |
| PP tiek nosūtīts kreditoram.                                            | Versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                          |
| Kreditors nosūta atbildi **Pieņemts ar izmaiņām**.                  | Statuss joprojām ir **Tiek pārskatīts ārēji**.                                                                                                                  |
| Jūs veicat izmaiņas pēc kreditora pieprasījuma.                  | Statuss tiek mainīts uz **Apstiprināts**.                                                                                                                        |
| Jūs PP jauno versiju nosūtāt kreditoram.                        | Jauna versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                      |
| Kreditors pieņem PP jauno versiju.                            | Statuss joprojām ir **Tiek pārskatīts ārēji**, ja vien kreditora konts nav konfigurēts pirkšanas pasūtījumu automātiski iestatīt uz **Akceptēts**, kad kreditors to pieņem. |


Kreditoriem nav jāapstiprina pirkšanas pasūtījums, izmantojot kreditoru sadarbības interfeisu. Tie var arī nosūtīt e-pasta ziņojumu vai informēt par PP pieņemšanu, izmantojot citus kanālus. Pēc tam pasūtījumu varat apstiprināt manuāli programmatūrā Finance and Operations. Šajā gadījumā saņemsit brīdinājumu par pasūtījuma apstiprināšanu arī tad, ja nebūs saņemta atbilde no kreditora. Pēc tam PP tiek parādīts apstiprināšanas vēsturē kā atvērts akceptēts pasūtījums, kuram nav atbilžu. Kreditoram vairs nav iespējas apstiprināt vai noraidīt šo PP.  


>[!NOTE]
>Pirkšanas pasūtījuma versija, kas ir pieejama citiem Dynamics 365 for Finance and Operations procesiem, vienmēr ir jaunākā versija, pat ja šī versija vēl nav reģistrēta kreditoru sadarbības interfeisā.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versijas un statusi, ja lietojat izmaiņu pārvaldību

Ja pirkšanas pasūtījumiem ir iespējota izmaiņu pārvaldība, tad pirkšanas pasūtījumiem tiek veikta apstiprināšanas darbplūsma, lai sasniegtu statusu **Apstiprināts**. Šis process kreditoram nav redzams.  

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP, kad ir aktivizēta izmaiņu pārvaldība. Versija tiek reģistrēta, kad PP tiek apstiprināts, nevis kad PP tiek nosūtīts kreditoram vai akceptēts.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Darbība**                                                                                                    | **Statuss un versija**                                                                                                                                                                                                                                                                                                                                                                      |
| Pirkšanas pasūtījuma sākotnējā versija tiek izveidota programmatūrā Finance and Operations.                                      | Statuss ir **Melnraksts**.                                                                                                                                                                                                                                                                                                                                                                    |

| Pirkšanas pasūtījums tiek iesniegts apstiprināšanas procesam. (Apstiprināšanas process ir iekšējs process, kurā kreditors nav iesaistīts.) | Ja pirkšanas pasūtījums apstiprināšanas procesa laikā netiek noraidīts, statuss mainās no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**. Apstiprināts PP tiek reģistrēts kā versija.                                                                                                                                                                                                                     | | Pirkšanas pasūtījums tiek nosūtīts kreditoram                                                                                  | Versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                                                                                                                                                                                                                                                       | | Jūs veicat dažas kreditora pieprasītās izmaiņas manuāli vai izmantojot darbību atbildē, lai atjauninātu pirkšanas pasūtījumu.                                                       | Statuss tiek mainīts atpakaļ uz **Melnraksts**.                                                                                                                                                                                                                                                                                                                                                    | | Pirkšanas pasūtījums tiek atkārtoti iesniegts apstiprināšanas procesam.                                                            | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja pirkšanas pasūtījums netiek noraidīts apstiprināšanas procesa laikā. Ja vēlaties, sistēmu var konfigurēt tā, lai noteiktu lauku izmaiņām nebūtu nepieciešams atkārtots apstiprinājums. Šajā gadījumā statuss vispirms tiek mainīts uz **Melnraksts** un pēc tam tiek automātiski atjaunināts uz **Apstiprināts**. Apstiprinātais PP tiek reģistrēts kā jauna versija. | | Jūs PP jauno versiju nosūtāt kreditoram.                                                             | Jaunā versija tiek reģistrēta kreditoru sadarbības interfeisā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                                                                                                                                                                                                                                                   | | Kreditors apstiprina jauno pirkšanas pasūtījuma versiju.                                                                | Statuss tiek mainīts uz **Apstiprināts** automātiski vai saņemot atbildi no kreditora un pēc tam apstiprinot pirkšanas pasūtījumu.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Kopīgot informāciju par sūtījuma krājumiem
Ja izmantojat sūtījuma krājumus, tad kreditori var izmantot kreditoru sadarbības interfeisu, lai skatītu informāciju tālāk norādītajās lapās.

-   **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi** — pirkšanas pasūtījumi par sūtījuma krājumiem tiek ģenerēti, kad krājumu īpašumtiesības mainās no kreditora uz jūsu uzņēmumu. Tajā pašā laikā tiek grāmatota preču ieejas plūsma. Šie sūtījuma pirkšanas pasūtījumi tiek rādīti tikai lapā **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi**. Tie nav iekļauti moduļa **Kreditoru sadarbība** lapā **Visi akceptētie pirkšanas pasūtījumi**.
-   **No sūtījuma krājumiem saņemtās preces** — šajā lapā ir uzskaitītas visas transakcijas, kur preces īpašumtiesības no kreditora tiek nodotas jūsu uzņēmumam. Kreditori var izmantot šo informāciju, lai debitoram izrakstītu rēķinu.
-   **Rīcībā esošie sūtījuma krājumi** — šajā lapā tiek rādīti kreditoram piederošie rīcībā esošie sūtījuma krājumi, kas ir saņemti jūsu noliktavā.





