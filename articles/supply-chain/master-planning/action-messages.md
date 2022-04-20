---
title: Darbību ziņojumi
description: Darbības ziņojums ir sistēmas izveidots priekšlikums mainīt esošu plānotu vai apstiprinātu pasūtījumu.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570259"
---
# <a name="action-messages"></a>Darbību ziņojumi

[!include [banner](../includes/banner.md)]

Darbības ziņojums ir sistēmas izveidots priekšlikums, lai mainītu esošo plānoto, apstiprināto vai apstiprināto pasūtījumu.

Darbību ziņojumus ģenerē vispārējās plānošanas aprēķins, reaģējot uz prasību izmaiņām. Piemēram, nosūtīšanas datums vai daudzums tiek mainīts pārdošanas pasūtījumā pēc tam, kad pirkšanas pasūtījums jau ir izveidots, lai izpildītu šī pārdošanas pasūtījuma pieprasījumu. Šajā gadījumā vispārējās plānošanas aprēķins ģenerē vienu vai vairākus darbības ziņojumus, kas iesaka atjaunināt pirkšanas pasūtījumu. Jūs izlemjat, vai veikt ierosinātās izmaiņas.

Varat iestatīt veidu, kā ziņojumi tiek aprēķināti seguma grupai, kuru piesaistāt krājumam.

## <a name="select-action-messages"></a>Darbību ziņojumu atlasīšana

Lapā **Seguma grupas** varat atlasīt darbību ziņojumus, kurus vēlaties, lai sistēma ģenerē, kā arī atlasīt, uz kurām vajadzību grupām vai elementiem šie ziņojumi attiecas. Šajā tabulā uzskaitīti atlasītie darbību ziņojumi.

| Ziņojums | Apraksts |
|---|---|
| Paātrināt | Sistēma ģenerēs darbību ziņojumus, jo tie ir nepieciešami, lai pārvietotu pasūtījumus uz agrāku datumu. Laukā **Avansa uzcenojums** var norādīt maksimālo dienu skaitu, kas var būt starp ieejas plūsmu un izdošanu bez iepriekšējas darbības. |
| Atlikt | Sistēma ģenerēs darbību ziņojumus, jo tie ir nepieciešami, lai pasūtījumus pārvietotu uz vēlāku datumu. Laukā **Atliktais** uzcenojums varat norādīt maksimālo dienu skaitu, kas var būt starp ieejas un izejas plūsmu, bez atlikšanas darbības. |
| Samazināt | Sistēma ģenerēs darbības ziņojumus, kad ražošanas pasūtījumi, pirkšanas pasūtījumi un citas saņemšanas darbības ir jāsamazina, lai novērstu liekus krājumu līmeņus. |
| Pieaugums | Sistēma ģenerēs darbības ziņojumus, kad ražošanas pasūtījumi, pirkšanas pasūtījumi un citas saņemšanas darbības ir jāpalielina, lai novērstu krājumu iztrūkumus. |
| Atvasinātās darbības | Darbības ziņojumi, kas izveidoti saņemšanas darbībām, tiks izplatīti visām atvasinātajām prasībām, un nepieciešamie darbību ziņojumi tiek ģenerēti saņemšanas darbībām, kas atbilst šīm prasībām. |

Tālāk sadaļās ir sniegtas dažas detalizētas scenārijus.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Palielināt un samazināt darbības ar preču noklusējuma pasūtījuma daudzumiem

Lapā Noklusējuma **pasūtījuma iestatījumi** krājumam var iestatīt minimālo pasūtījuma daudzumu, maksimālo pasūtījuma daudzumu un vairākas vērtības. Pēc tam sistēma šos iestatījumus ņem vērā, kad tā iesaka darbības, lai nodrošinātu, ka ieteikumi nekad neraisīs undersupply.

Piemēram, jums ir krājums, kas savā Noklusējuma pasūtījuma iestatījumu lapā **ir šāds** iestatījums:

- **Minimālais pasūtījumu daudzums:** *0*
- **Maksimālais pasūtījuma daudzums:** *90*
- **Daudzkārtīgi:** *20*

Ja ir pieprasījums daudzumam 60 no šī krājuma, vispārējā plānošana izveidos plānoto pirkšanas pasūtījumu daudzumam 60. Ja pieprasījums tiek palielināts par 30, vispārējais plāns ieteiks palielinājumu par 40, jo tas ievēros 20 dalāmo un nekad neraisīs nejaukošanu.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Darbību ziņojumi pasūtījumiem, kas saistīti ar drošības krājumu

Darbību ziņojumi pasūtījumiem, kas nodrošina drošības krājumu, nekad neteiks samazināt daudzumu zem daudzuma, kas ir nepieciešams drošības rezervēm. Citiem vārdiem sakot, ja ir pasūtījums, kas nodrošina drošības rezervi un debitora pieprasījumu, un pieprasījums ir samazināts vai atcelts, vispārējais plāns ieteiks samazināt plānoto pasūtījumu par samazinātu pieprasījumu. Tomēr tā nekad nepiedāvās vērtību, kas ir zemāka nekā nepieciešamais drošības rezerve.

Sistēma nepiedāvās izpildes darbības drošības krājumu piegādei, jo ir pieņemts, ka drošības rezerve ir jāpiegādā nepieciešamajā laikā un pieprasītajā datumā.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Avansa un atliktās ar MK saistītās darbības

Darbības, kas saistītas ar materiālu komplektu (MK) komponentiem, jālieto pirms to pamatelementu darbībām, jo var tikt ietekmēti turpmāki pasūtījumi, kas saistīti ar augstāka līmeņa MK. Pēc tam vēlreiz jāpalaiž vispārējā plānošana, lai pārrēķinātu un ieteiktu atbilstošas darbības.

Piemēram, jums ir šāda situācija:

- Beigu labajam *FG* ar ražošanas *tipu* ir MK, kas ietver izejmateriālu *RM*.
- Šodienas datums ir 21. janvāris.
- Pastāv, izpildei nodots FG ražošanas pasūtījums *ir* ieplānots 25. janvārī.
- Lai atbalstītu esošo ražošanas pasūtījumu, vispārējā plānošana ir izveidojusi plānotu pirkšanas pasūtījumu nepieciešamajam izejmateriālu *RM*. Šī pasūtījuma vajadzības datums ir 25. janvāris.
- Šodien ir izveidots jauns *FG pārdošanas* pasūtījums. Tā vajadzības datums ir šodiena (21. janvāris).
- 21. janvāris ir slēgts piegādei *RM* kalendārā, bet 22. janvāris ir atvērts.

Kad tiek veikta vispārējā plānošana, tā ģenerē uzlabotus darbību ziņojumus, kas ieteiktu iepriekš plānotās ražošanas pārvietošanu, lai varētu izpildīt šodienas pasūtījumu.

- Lai atbilstu jaunajam pieprasījumam, tas iesaka pārvietot ražošanas pasūtījumu *uz FG* līdz 21. janvārim. (Ņemot vērā slēgto datumu šim datumam, tas sniedz šādu ieteikumu. *Rm*.)
- Tā *kā* ražošanas pasūtījumam joprojām nepieciešams RM, ieteicams arī pārvietot uz augšu plānoto pirkšanas pasūtījumu. Tomēr šoreiz tas pārbauda *RM* kalendāru. Tāpēc tas iesaka pārvietot plānoto pirkšanas pasūtījumu uz RM *uz* 22. janvāri (jo 21. janvāris ir slēgts).

Kā redzams, pieprasītais izejmateriāls *RM tagad* nokavēs plānoto FG *ražošanu*. Tāpēc jums vispirms ir jāpiemēro avansa darbība plānotajam pirkšanas pasūtījumam RM *un* pēc tam vēlreiz jāpalaiž galvenā plānošana. Šajā brīdī vispārējā plānošana ģenerēs jaunu darbības ziņojumu, kas iesaka pārvietot FG *ražošanas* pasūtījumu uz 22. janvāri.
