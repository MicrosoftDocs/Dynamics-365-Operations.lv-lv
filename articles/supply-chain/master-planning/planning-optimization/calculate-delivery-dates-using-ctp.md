---
title: Pārdošanas pasūtījuma piegādes datumus aprēķināšana, izmantojot CTP
description: Funkcionalitāte Pieejama uz solīšanai (CTP) ļauj debitoriem sniegt reālus datumus, kad varat apsolīt noteiktas preces. Šajā rakstā ir aprakstīts, kā iestatīt un izmantot CTP katrai plānošanas programma (Plānošanas optimizācija un novecojusi vispārējās plānošanas programma).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 4a3b8ba89d9fb224026cf32cad89d7f28321ee79
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741208"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Pārdošanas pasūtījuma piegādes datumus aprēķināšana, izmantojot CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->
<!-- KFN: Split into two topics, one for PO and one for classic. -->

Funkcionalitāte Pieejama uz solīšanai (CTP) ļauj debitoriem sniegt reālus datumus, kad varat apsolīt noteiktas preces. Katrai pārdošanas rindai var norādīt datumu, ņemot vērā esošos rīcībā esošos krājumus, ražošanas noslodzi un transportēšanas laikus.

CTP paplašina funkcionalitāti Pieejams solīšanai [(ATP), ņemot vērā noslodzes](../../sales-marketing/delivery-dates-available-promise-calculations.md) informāciju. Kamēr ATP ņem vērā tikai materiālu pieejamību un pieņem neierobežotas noslodzes resursus, CTP ņem vērā gan materiālu, gan noslodzes pieejamību. Tādējādi tas nodrošina reālāku attēlu, vai pieprasījumu var apmierināt noteiktā laika posmā.

CTP darbojas nedaudz atšķirīgi, atkarībā no izmantotās vispārējās plānošanas programmas (Optimizācijas plānošana vai novecojusi vispārējās plānošanas programma). Šajā rakstā ir aprakstīts, kā to iestatīt katrai programma. CTP plānošanas optimizēšanai pašlaik atbalsta tikai to CTP scenāriju apakškopu, kurus atbalsta novecojusi vispārējās plānošanas programma.

## <a name="turn-on-ctp-for-planning-optimization"></a>Ieslēgt CTP plānošanas optimizēšanai

Vienmēr ir pieejama novecojusī vispārējās plānošanas programmas CTP. Tomēr, ja vēlaties izmantot CTP plānošanas optimizēšanai, sistēmai ir jābūt ieslēgtai. Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Vispārējā plānošana*
- **Līdzekļa nosaukums:** *(priekšskatījums) CTP plānošanas optimizēšanai*

## <a name="how-ctp-compares-to-atp"></a>Kā CTP salīdzina ar ATP

CTP un ATP ir līdzīgi, bet CTP bieži var sniegt precīzāku rezultātu, kā redzams šajā piemērā.

Krājums A ir krājums, kas veidots no krājumiem B un C, un rīcībā esošo krājumu daudzums A ir 0 (nulle). Ja veic ATP pārbaudi, kas apsver tikai materiālus, ATP daudzums arī būs 0 (nulle). Tomēr, ja veiksiet CTP pārbaudi, sistēma pārbauda krājumu B un C pieejamību, pārbaudiet resursus, kas nepieciešami to saglabāšanai A krājumam, un aprēķinās, cik no A krājumiem var tikt veikts. Turklāt CTP aprēķins var pārbaudīt resursus un materiālus, kas nepieciešami, lai izveidotu vairāk krājumu B un C, un izmantot tos, lai padarītu vairāk krājumu A.

CTP aprēķins, kas ņem vērā gan materiālus, gan resursus, var parādīt lielāku daudzumu nekā aprēķins, kas pārbauda tikai materiālus, īpaši, ja atzīmētais krājums ir salikšana pasūtījumā. Citiem vārdiem sakot, CTP funkcionalitāte ir balstīta uz izvēršanas funkciju, un to var palaist izvēlētajai pārdošanas pasūtījuma rindai, lai aprēķinātu paredzamo piegādes datumu.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Kā CTP atšķiras atkarībā no izmantotās vispārējās plānošanas programmas

Šajā tabulā ir apkopotas atšķirības starp CTP optimizāciju plānošanu un CTP novecojušu vispārējās plānošanas programmu.

| Elements | Plānošanas optimizācija | Novecojusi vispārējās plānošanas programma |
|---|---|---|
| **Piegādes datuma kontroles** iestatījumi pasūtījumiem, pasūtījuma rindām un precēm | *CTP plānošanas optimizācijai* | *Ctp* |
| Aprēķina laiks | Aprēķināšana tiek izraisīta, palaižot dinamisko plānu kā ieplānotu uzdevumu. | Aprēķins nekavējoties tiek parādīts katru reizi, kad ievadāt vai atjaunināsiet pārdošanas pasūtījuma rindu. |
| **CTP plānošanas optimizācijas statusa** lauka vērtībai | <p>Vērtība Nav gatava *tiek parādīta* pasūtījumiem un pasūtījumu rindām, kur dinamiskais plāns nav palaists kopš pasūtījumu un rindu izveides vai pēdējās atjaunināšanas.</p><p>Gatavības vērtība *tiek parādīta* pasūtījumiem un rindām, kur CTP ir izmantots, lai aprēķinātu apstiprinātos piegādes datumus, palaižot dinamisko plānu.</p> | Vienmēr tiek rādīta *vērtība* Gatavs. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a> Iestatīt noklusējuma piegādes datuma kontroles metodes

Sistēma var izmantot jebkuru no vairākām metodēm, lai aprēķinātu piegādes datuma novērtējumu katram pasūtījumam un pasūtījuma rindai. Jāiestata piegādes datuma kontroles metode, ko vēlaties visbiežāk izmantot kā globālo noklusējuma metodi. Katrai precei var iestatīt arī individuālas ignorēšanas. Vēlāk varēsit pārrakstīt noklusētās metodes katram pasūtījumam un/vai pasūtījuma rindai pēc to pieprasīšanas.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a> Iestatīt globālo noklusējuma piegādes datuma kontroli

Noklusējuma piegādes datuma kontroles metode tiks lietota visām jaunajām pasūtījuma rindām, kur nav lietota ignorēšana. Lai atlasītu vienu, sekojiet šiem soļiem.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
1. **Cilnē Kravas** kopsavilkuma **cilnē** Piegādes kontrole, **laukā Piegādes datuma** kontrole atlasiet metodi, kuru vēlaties izmantot kā noklusējuma metodi savam uzņēmumam:

    - *Nav* – neaprēķina piegādes datumus.
    - *Pārdošanas izpildes laiks* – pārdošanas izpildes laiks ir laiks starp pārdošanas pasūtījuma izveidošanu un krājumu nosūtīšanu. Piegādes datuma aprēķina pamatā ir noklusējuma dienu skaits, kā arī nav apsvērta krājumu pieejamība, zināms pieprasījums vai plānota piegāde.
    - *ATP* – ATP ir daudzums krājumam, kas ir pieejams un to var solīt debitoram noteiktā datumā. ATP aprēķinā tiek iekļauti nesaistītie krājumi, izpildes laiki, plānotās ieejas plūsmas un izejas plūsmas.
    - *ATP + Izejas* plūsmas rezerve – nosūtīšanas datums ir vienāds ar ATP datumu plus krājuma izejas plūsmas rezervi. Izejas plūsmas rezerve ir laiks, kas ir nepieciešams, lai krājumus sagatavotu sūtīšanai.
    - *CTP* - izmantojiet CTP aprēķinu, ko nodrošina novecojusi vispārējās plānošanas programma. Ja izmantojat plānošanas optimizāciju, *nav atļauta CTP* piegādes datuma kontroles metode, un, ja tā ir atlasīta, aprēķina izpildes laikā rodas kļūda.
    - *CTP plānošanas optimizēšanai* - izmantojiet CTP aprēķinu, ko nodrošina plānošanas optimizācija. Šī opcija stāsies spēkā tikai tad, ja izmantojat novecojušu vispārējās plānošanas programmu.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Iestatīt piegādes datuma kontroles ignorēšanu atsevišķām precēm

Varat piešķirt ignorēšanu noteiktām precēm, ja vēlaties izmantot piegādes datuma kontroles metodi, kas nav tā, kas iestatīta kā globālā noklusējuma metode.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci, ko vēlaties iestatīt.
1. Darbību rūts cilnē **Pārvaldīt krājumu** grupā **Pasūtījuma iestatījumi** atlasiet **Pasūtījuma noklusējuma iestatījumi**.
1. Lapā Noklusējuma **pasūtījuma iestatījumi** kopsavilkuma cilnē Pārdošanas **pasūtījums** iestatiet opciju Ignorēt **piegādes kontroli uz** *Jā*.
1. Laukā **Piegādes datuma** kontrole atlasiet metodi, ko izmantot atlasītajai precei. Ir pieejamas tās pašas opcijas, kas aprakstītas [sadaļā Iestatīt globālo piegādes](#global-default) datuma kontroli.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a> Plānot CTP optimizācijas aprēķinu plānošanai

Kad plānošanas optimizēšanai izmantojat CTP, ir jāpalaiž dinamiskais plāns, lai sistēma aktivizētu CTP aprēķinus, un pēc tam jāiestata apstiprinātie nosūtīšanas un saņemšanas datumi visiem atbilstošajiem pasūtījumiem. Plānā jāietver visi krājumi, kuriem ir nepieciešami nosūtīšanas un saņemšanas datumi. (Izmantojot CTP novecojušajiem vispārējās plānošanas programmas aprēķiniem, CTP aprēķini tiek nekavējoties veikti lokāli. Tādēļ nav jāpalaiž dinamiskais plāns, lai redzētu CTP rezultātus.)

Lai nodrošinātu, ka datumi visiem lietotājiem ir pieejami laikus, ieteicams iestatīt pakešuzdevumus, lai atbilstošos plānus palaistu periodiski. Piemēram, pakešuzdevums, kas iestatīts dinamiskā plāna palaišanai ik pēc 30 minūtēm, iestatīs apstiprināto nosūtīšanas un saņemšanas datumus ik pēc 30 minūtēm. Tādēļ lietotājiem, kas ievada un importē pasūtījumus, būs jāgaida ne vairāk kā 30 minūtes, lai iegūtu apstiprinātos nosūtīšanas un saņemšanas datumus.

Lai uzstādītu pakešuzdevumu regulārai plāna palaišanai dinamiskajā plānā, sekojiet šiem soļiem.

1. Doties uz vispārējās **plānošanas vispārējo \> plānošanu Palaist \> vispārējo \> plānošanu**.
1. Vispārējās plānošanas **dialoglodziņā** kopsavilkuma **cilnē** Parametri iestatiet vispārējā plāna lauku **uz dinamisko plānu,** kuru vēlaties palaist.
1. Kopsavilkuma cilnes **Fonā cilnē Palaist** iestatiet opciju Pakešapstrāde **uz** *Jā*.
1. Atlasiet **Periodiskums** un iestatiet grafiku pēc vajadzības.
1. Atlasiet **Labi,** lai saglabātu grafiku.
1. Atlasiet **Labi**, lai izveidotu pakešuzdevumu un aizvērtu dialoglodziņu.

## <a name="use-ctp-for-the-deprecated-master-planning-engine"></a>Izmantot CTP novecojusi vispārējās plānošanas programma

### <a name="create-a-new-order-by-using-ctp-for-the-deprecated-master-planning-engine"></a>Izveidot jaunu pasūtījumu, izmantojot CTP novecojusī vispārējās plānošanas programma

Katru reizi, kad pievienojat jaunu pārdošanas pasūtījumu vai pasūtījuma rindu, sistēma tam piešķir noklusējuma piegādes datuma kontroles metodi. Pasūtījuma virsraksts vienmēr sākas ar globālo noklusējuma metodi. Ja pasūtītam krājumam tiek piešķirta ignorēšana, jaunā pasūtījuma rinda izmantos šo ignorēšanu. Pretējā gadījumā jaunā pasūtījuma rinda izmantos arī globālo noklusējuma metodi. Tādēļ jums jāiestata noklusētās metodes tā, lai tās atbilstu piegādes datuma kontroles metodei, ko visbiežāk izmantojat. Pēc pasūtījuma izveides varat ignorēt noklusēto metodi pasūtījuma virsrakstā un/vai pasūtījuma rindas līmenī pēc savas pieprasīšanas. Papildinformāciju skatiet noklusējuma [piegādes datuma kontroles metožu iestatīšana un](#default-methods) Esošo [pārdošanas pasūtījumu mainīšana CTP izmantošanai](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-the-deprecated-master-planning-engine"></a>Skatīt apstiprinātos piegādes datumus, ja novecojusit vispārējās plānošanas programmas CTP

Ja izmantojat vispārējās plānošanas programmu, CTP aprēķini tiek piemēroti pasūtījumiem un/**·** *vai pasūtījumu rindām, kur piegādes datuma kontroles lauks ir iestatīts uz CTP.*

Pārdošanas rindām, kas izmanto CTP novecojušajām vispārējās plānošanas programmas lietojumprogrammām, sistēma automātiski iestata laukus Apstiprināts nosūtīšanas datums un **Apstiprināts** **saņemšanas** datums katru reizi, kad saglabājat pārdošanas rindu. Ja vēlāk pārdošanas rindā veiksiet atbilstošas izmaiņas (piemēram, izmainot tās daudzumu vai vietu), datumi nekavējoties tiks pārrēķināti.

- Lai skatītu apstiprinātos piegādes datumus pārdošanas pasūtījuma rindai, atveriet pārdošanas pasūtījumu un izvēlieties pārdošanas rindu. Pēc tam kopsavilkuma cilnē **Piegāde kopsavilkuma** cilnē Rindas informācija **pārskatiet** Apstiprinātā **nosūtīšanas datuma un** Apstiprinātā **saņemšanas datuma** vērtības.
- Lai skatītu apstiprinātos piegādes datumus visam pasūtījumam, atveriet pārdošanas pasūtījumu un atlasiet virsraksta **skatu**. Pēc tam kopsavilkuma cilnē Piegāde **pārskatiet** apstiprinātā nosūtīšanas **datuma un apstiprinātā** **saņemšanas datuma** vērtības.

## <a name="use-ctp-for-planning-optimization"></a>Izmantot CTP plānošanas optimizēšanai

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Izveidot jaunu pasūtījumu, izmantojot CTP plānošanas optimizēšanai

Katru reizi, kad pievienojat jaunu pārdošanas pasūtījumu vai pasūtījuma rindu, sistēma tam piešķir noklusējuma piegādes datuma kontroles metodi. Pasūtījuma virsraksts vienmēr sākas ar globālo noklusējuma metodi. Ja pasūtītam krājumam tiek piešķirta ignorēšana, jaunā pasūtījuma rinda izmantos šo ignorēšanu. Pretējā gadījumā jaunā pasūtījuma rinda izmantos arī globālo noklusējuma metodi. Tādēļ jums jāiestata noklusētās metodes tā, lai tās atbilstu piegādes datuma kontroles metodei, ko visbiežāk izmantojat. Pēc pasūtījuma izveides varat ignorēt noklusēto metodi pasūtījuma virsrakstā un/vai pasūtījuma rindas līmenī pēc savas pieprasīšanas. Papildinformāciju skatiet noklusējuma [piegādes datuma kontroles metožu iestatīšana un](#default-methods) Esošo [pārdošanas pasūtījumu mainīšana CTP izmantošanai](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Skatīt apstiprinātos piegādes datumus, izmantojot CTP plānošanas optimizēšanai

Ja izmantojat plānošanas optimizāciju, CTP aprēķini tiek piemēroti pasūtījumiem un/ **vai pasūtījuma rindām, kur piegādes datuma** *kontroles lauks ir iestatīts uz CTP plānošanas optimizēšanai*.

Pārdošanas rindām, kas izmanto CTP plānošanas optimizēšanai, **·** **lauki** Apstiprināts nosūtīšanas datums un Apstiprināts saņemšanas datums būs tukši līdz izpildīsit atbilstošo dinamisko plānu (parasti, izmantojot periodisko pakešuzdevumu). Pēc tam tās tiek iestatītas automātiski. Papildinformāciju skatiet Schedule [CTP optimizācijas aprēķinu plānošanai](#batch-job).

CTP **plānošanas optimizācijas statusa lauks** norāda, vai apstiprinātie datumi vēl ir aprēķināti katrai rindai, kas plānošanas optimizēšanai izmanto CTP. Laukā tiek parādīta vērtība *Nav* gatava rindām un pasūtījumiem, kur apstiprinātie piegādes datumi vēl nav aprēķināti vai vairs nav derīgi citu izmaiņu dēļ. Rāda vērtību Gatavs aprēķinātajām *rindām* un pasūtījumiem. Var skatīt statusu katrai rindai un visam pasūtījumam.

- Lai apskatītu pārdošanas pasūtījuma rindas statusu, atveriet pārdošanas pasūtījumu un izvēlieties pārdošanas rindu. Pēc tam kopsavilkuma **cilnē Piegāde kopsavilkuma** cilnē Rindas **informācija** **pārskatiet CTP optimizācijas statusa vērtības plānošanai.** Rindas **lauki Apstiprināts** nosūtīšanas **datums un** Apstiprinātais saņemšanas datums arī tiek rādīti šajā cilnē pēc to aprēķina.
- Lai skatītu visa pasūtījuma statusu, atveriet pārdošanas pasūtījumu un atlasiet virsraksta **skatu**. Tad kopsavilkuma cilnē Piegāde **pārskatiet** CTP, **lai iegūtu optimizācijas statusa vērtību** plānošanai. Pasūtījuma **apstiprinātais nosūtīšanas** **datums un** Apstiprinātais saņemšanas datums tiek rādīti arī šajā cilnē pēc to aprēķina.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Ja atjaunināt pārdošanas pasūtījuma rindu pēc CTP plānošanas optimizācijai ir aprēķinājusi tam apstiprinātos datumus, sistēma nod pastāvēs šos datumus līdz nākamajai atbilstošā dinamiskā plāna palaišanas reizei.
> - Ja rediģējat saistīto iestatījumu, kas var ietekmēt esošos apstiprinātos datumus (piemēram, mainot izpildes laikus, rezervācijas vai iezīmēšanas), notīriet atbilstīgo esošo pasūtījumu apstiprinātos datumus. Šīs darbības rezultātā katras atbilstošās rindas statuss tiks nomainīts uz Nav *gatavs*. Šīs izmaiņas savukārt izraisīs sistēmas apstiprināto datumu pārrēķināšanu nākamajā reizē, kad tas palaiž dinamisko plānu.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a> Mainīt esošos pārdošanas pasūtījumus, lai tie izmantotu CTP

Piegādes datuma kontroles **vērtību var mainīt** jebkuram atvērtam pasūtījumam jebkurā laikā. Vērtību var mainīt virsraksta līmenī un/vai katrai rindai pēc jūsu pieprasītā.

### <a name="change-to-ctp-at-the-order-header-level"></a>Mainīt uz CTP pasūtījuma virsraksta līmenī

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Lai mainītu pasūtījumu tā, ka tas izmanto CTP pasūtījuma virsraksta līmenī, sekojiet šiem soļiem.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atveriet pārdošanas pasūtījumu, kuru vēlaties iestatīt, vai izveidojiet jaunu.
1. Atlasiet **Virsrakstu**, lai atvērtu galvenes informāciju pārdošanas pasūtījuma **informācijas** lapā.
1. Kopsavilkuma cilnē **Piegāde** iestatiet piegādes **datuma kontroles** lauku uz vienu no šīm vērtībām atkarībā no izmantotās plānošanas programmas:

    - *CTP* - izmantojiet CTP aprēķinu, ko nodrošina novecojusi vispārējās plānošanas programma. Ja izmantojat plānošanas optimizāciju, *nav atļauta CTP* piegādes datuma kontroles metode. Tāpēc, atlasot šo vērtību, tiek parādīts kļūdas ziņojums, kad tiek palaists aprēķins.
    - *CTP plānošanas optimizēšanai* - izmantojiet CTP aprēķinu, ko nodrošina plānošanas optimizācija. Šis iestatījums stāsies spēkā tikai tad, ja izmantojat novecojušu vispārējās plānošanas programmu.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Atlasiet **Labi**, lai piemērotu izmaiņas.

### <a name="change-to-ctp-at-the-order-line-level"></a>Mainīt uz CTP pasūtījuma rindas līmenī

Ja izveidojat pasūtījuma rindu, izmantojot atšķirīgu piegādes datuma kontroles metodi, varat mainīt CTP jebkurā laikā. Rindas līmenī veiktās izmaiņas neietekmē nevienu citu rindu. Tomēr, tie var radīt vispārējas pasūtījuma piegādes datumu pārvietoties uz priekšu un atpakaļ, atkarībā no tā, kā mainās katra atjauninātā rindas aprēķina. <!-- KFM: Confirm this intro at next revision -->

Lai mainītu pasūtījumu tā, ka rindu līmenī tai tiek izmantots CTP, kam ir novecojusi vispārējās plānošanas programma, sekojiet šiem soļiem.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atveriet pārdošanas pasūtījumu, kuru vēlaties iestatīt, vai izveidojiet jaunu.
1. **Lapā Detalizēta informācija par** pārdošanas pasūtījumu **kopsavilkuma** cilnē Pārdošanas pasūtījuma rinda atlasiet pārdošanas pasūtījuma rindu, kuru vēlaties iestatīt.
1. **·** **·** **Kopsavilkuma** cilnē Rindas informācija cilnē Piegāde iestatiet lauku Piegādes datuma kontrole uz vienu no šīm vērtībām atkarībā no izmantotās plānošanas programmas:

    - *CTP* - izmantojiet CTP aprēķinu, ko nodrošina novecojusi vispārējās plānošanas programma. Ja izmantojat plānošanas optimizāciju, *nav atļauta CTP* piegādes datuma kontroles metode. Tāpēc, atlasot šo vērtību, tiek parādīts kļūdas ziņojums, kad tiek palaists aprēķins.
    - *CTP plānošanas optimizēšanai* - izmantojiet CTP aprēķinu, ko nodrošina plānošanas optimizācija. Šis iestatījums stāsies spēkā tikai tad, ja izmantojat novecojušu vispārējās plānošanas programmu.

    Tiek **atvērts dialoglodziņš Pieejamais nosūtīšanas** un saņemšanas datums un ir redzami pieejamie nosūtīšanas un saņemšanas datumi. Šis dialoglodziņš darbojas tāpat kā pasūtījuma rindās ar pasūtījuma virsrakstu, kā aprakstīts iepriekšējā sadaļā.

1. Darbību rūtī atlasiet **Saglabāt**.
