---
title: Noliktavas darba politikas
description: "Versijā Microsoft Dynamics AX 7.0.1 (2016. gada maija atjauninājums) ir ieviesta jauna noliktavas darba politika. Šī darba politika kontrolē to, vai ražošanā noliktavas procesiem tiek izveidots noliktavas darbs."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 5660e5c8e3329564fc4262b5ad4f2547347bbb1a
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-work-policies"></a>Noliktavas darba politikas

Versijā Microsoft Dynamics AX 7.0.1 (2016. gada maija atjauninājums) ir ieviesta jauna noliktavas darba politika. Šī darba politika kontrolē to, vai ražošanā noliktavas procesiem tiek izveidots noliktavas darbs.

Šī darba politika kontrolē to, vai ražošanā noliktavas procesiem tiek izveidots noliktavas darbs. Šo darba politiku varat iestatīt, izmantojot kombināciju no vienumiem **darba pasūtījuma veidi**, **krājumu novietojums** un **prece**. Piemēram, produkta L0101 tiek ziņota kā pabeigta izvades vietu 001. Vēlāk pabeigta prece tiek patērēts citā ražošanas pasūtījumā izvades vietā 001. Šajā gadījumā var iestatīt darba politiku, lai neļautu gatavās produkcijas izvietošanas darbā tiek veidota, ziņojot produkta L0101 pabeigšanu izvades vietu 001. Darba politika ir atsevišķs elements, ko var aprakstīt ar tālāk norādīto informāciju.

-   **Darba politikas nosaukums **(darba politikas unikālais identifikators)
-   **Darba pasūtījumu veidi **un** Darba izveidošanas metode**
-   **Krājumu vietas**
-   **preces.**

## <a name="work-order-types"></a>Darba pasūtījumu veidi
Varat atlasīt no tālāk uzskaitītajiem darba pasūtījumu veidiem.

-   Pabeigto preču izvietošana
-   Līdzproduktu un blakusproduktu izvietošana
-   Izejmateriālu izdošana

Laukam **Darba izveidošanas metode** vērtība ir **Nekad**. Šī vērtība norāda, ka šī darba politika atlasītajam darba pasūtījuma veidam neļaus izveidot noliktavas darbu.

## <a name="inventory-locations"></a>Krājumu vietas
Varat atlasīt novietojumu, uz kuru attiecas šī darba politika. Ja darba politikai nav piesaistīts neviens novietojums, tad šī darba politika netiek lietota nevienam procesam. Lapā **Novietojumi** varat arī atlasīt vai atcelt konkrēta novietojuma atlasi darba politikai.

## <a name="products"></a>Preces
Varat atlasīt preci, uz kuru attiecas šī darba politika. Darba politiku varat lietot visām precēm vai atlasītām precēm.

## <a name="example"></a>Piemērs
Nākamajā piemērā ir divi ražošanas pasūtījumi, PRD-001 un PRD-00*2*. Ražošanas pasūtījumā PRD-001 ir operācija ar nosaukumu **Montāža**, kur prece SC1 tiek ziņota kā pabeigta uz novietojumu O1. Ražošanas pasūtījumā PRD-002 ir operācija ar nosaukumu **Krāsošana**, un tas patērē preci SC1 no novietojuma O1. Ražošanas pasūtījums PRD-002 patērē arī izejmateriālu RM1 no novietojuma O1. Izejmateriāls RM1 tiek glabāts noliktavas novietojumā BULK-001 un ar noliktavas darbu izejmateriālu izdošanai tiks izdots uz novietojumu O1. Izdošanas darbs tiek ģenerēts, kad tiek izlaista ražošana PRD-002. 

[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Kad plānojat konfigurēt noliktavas darba politiku šim scenārijam, ir jāņem vērā tālāk norādītā informācija.

-   Noliktavas darbs gatavo preču izvietošanai nav nepieciešams, kad preci SC1 ziņojat kā pabeigtu no ražošanas pasūtījuma PRD-001 uz novietojumu O1. Tas ir tādēļ, ka operācija **Krāsošana** ražošanas pasūtījumam PRD-002 preci SC1 patērē tajā pašā novietojumā.
-   Noliktavas darbs izejmateriālu izdošanai ir nepieciešams, lai izejmateriālu RM1 no noliktavas novietojumā BULK-001 pārvietotu uz novietojumu O1.

Šeit ir sniegts darba politikas piemērs, kuru varat iestatīt, pamatojoties uz šiem apsvērumiem.

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|**Work policy name**<br>                 |**Work order types**<br>                               |
| Nē, nolikšu 01'                    |-Pabeigta prece izvietota<br>                           |
|                                         |**Locations**<br>                                      |
|                                         |-O1   |                                               |
|                                         |**Products** <br>                                      |
|                                         |-SC1                                                  |

Nākamajās procedūrās ir sniegtas detalizētas instrukcijas par to, kā iestatīt noliktavas darba politiku šim scenārijam. Ir aprakstīts arī piemēra iestatījums, kurā redzams, kā ražošanas pasūtījumu ziņot kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības.

## <a name="set-up-a-warehouse-work-policy"></a>Iestatīt noliktavas darba politiku
Ne vienmēr noliktavas procesi ietver noliktavas darbu. Definējot darba politiku, jūs varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai preču kopai konkrētos novietojumos. Šīs procedūras izveidošanai tika izmantots demonstrācijas datu uzņēmums USMF. 

DARBĪBAS (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Dodieties uz Noliktavas vadība &gt; Iestatīšana &gt; Darbs &gt; Darba politikas.        |
| 2.  | Noklikšķiniet uz Jauns.                                                                 |
| 3.  | Darba politikas nosaukumu laukā ierakstiet 'Nav izvietošanas darbu'.                    |
| 4.  | Noklikšķiniet uz Saglabāt.                                                                |
| 5.  | Noklikšķiniet uz Pievienot.                                                                 |
| 6.  | Sarakstā atzīmējiet atlasīto rindu.                                        |
| 7.  | Darba pasūtījuma veida laukā atlasiet 'Pabeigto preču izvietošana'.            |
| 8.  | Noklikšķiniet uz Pievienot.                                                                 |
| 9.  | Sarakstā atzīmējiet atlasīto rindu.                                        |
| 10. | Darba pasūtījuma veida laukā atlasiet 'Līdzproduktu un blakusproduktu izvietošana'. |
| 11. | Izvērsiet sadaļu Krājumu atrašanās vietas.                                    |
| 12. | Noklikšķiniet uz Pievienot.                                                                 |
| 13. | Sarakstā atzīmējiet atlasīto rindu.                                        |
| 14. | Sarakstā Noliktava ievadiet '51'.                                         |
| 15. | Laukā Atrašanās vieta, ievadiet vai atlasiet '001'.                              |
| 16. | Izvērsiet sadaļu Preces.                                               |
| 17. | Laukā Preču atlase, atlasiet 'Atlasīts'.                         |
| 18. | Noklikšķiniet uz Pievienot.                                                                 |
| 19. | Sarakstā atzīmējiet atlasīto rindu.                                        |
| 20. | Laukā Krājuma kods ievadiet vai atlasiet 'L0101'.                         |
| 21. | Noklikšķiniet uz Saglabāt.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Ziņot ražošanas pasūtījumu kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības
Šajā procedūrā ir parādīts piemērs tam, kā ziņot kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības. Šim uzdevumam ir nepieciešama piemērojama darba politika. Iepriekšējā procedūrā ir parādīta darba politikas iestatīšana. 

DARBĪBAS (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Apakšuzdevums: iestatīt izvades novietojumu.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Dodieties uz Organizācijas administrēšana &gt; Resursi &gt; Resursu grupas.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Sarakstā atlasiet resursu grupu “5102”.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Noklikšķiniet uz Rediģēt.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Laukā Izvades noliktava ievadiet “51”.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Laukā Izvades vieta ievadiet “001”.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Novietojums 001 nav no numura zīmes atkarīgs novietojums. Novietojumu, kas nav atkarīgs no numura zīmes, var iestatīt tikai tad, ja attiecīgajam novietojumam ir piemērojama darba politika.</td>
</tr>
<tr>
<td colspan="3"><strong>Apakšuzdevums: izveidot ražošanas pasūtījumu un norādīt to kā pabeigtu.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Aizvērt lapu.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Doties uz Ražošanas kontrole &gt; Ražošanas pasūtījumi &gt; Visi ražošanas pasūtījumi.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Noklikšķiniet uz Jauns ražošanas pasūtījums.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Laukā Krājuma kods ievadiet “L0101”.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Noklikšķiniet uz Izveidot.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Darbību rūtī noklikšķiniet uz Ražošanas pasūtījums.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Noklikšķiniet uz Novērtējums.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Noklikšķiniet uz Labi.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Noklikšķiniet uz Sākt.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Noklikšķiniet uz cilnes Vispārīgie iestatījumi.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Laukā Automātisks MK patēriņš atlasiet "Nekad".</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Noklikšķiniet uz Labi.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Noklikšķiniet uz Ziņot kā pabeigtu.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Noklikšķiniet uz cilnes Vispārīgie iestatījumi.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Laukā Pieņemt kļūdu atlasiet vienumu Jā.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Noklikšķiniet uz Labi.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Darbību rūtī noklikšķiniet uz Noliktava.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Noklikšķiniet uz Detalizēta informācija par darbu.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Kad ražošanas pasūtījums tika norādīts kā pabeigts, netika ģenerēts darbs izvietošanai. Tas notiek tāpēc, ka ir definēta darba politika, kas neļauj ģenerēt darbu, kad produkts L0101 tiek norādīts kā pabeigts novietojumā 001.</td>
</tr>
</tbody>
</table>


