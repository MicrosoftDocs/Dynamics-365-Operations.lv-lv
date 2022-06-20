---
title: Izsekot ienākošos reisus un pārvadāšanas konteinera ceļojumus
description: Šajā rakstā skaidrots, kā var izmantot ieešanas izsekošanas lapu, lai izsekotu jūsu reisu un pārvadāšanas konteineru transportēšanas progresu.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 17874f984945b27e036eafda841ec1fd95d345be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854360"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Izsekot ienākošos reisus un pārvadāšanas konteinera ceļojumus

[!include [banner](../../includes/banner.md)]

Lapa **Ienākošo sūtījumu izsekošana** ļauj izsekot savu reisu un pārvadāšanas konteineru transportēšanas progresu. Katru reisu un vilcienu sadala pēc *aktivitātēm*, kur katrai ir sava rinda lapā. Jūs variet izmantot šo lapu, lai skatītu un ievadītu paredzamos datumus un faktiskos datumus pēc darbības.

Parasti, atkarībā no [Izsekošanas kontroles centra iestatījumiem](delivery-information-setup.md#tracking-control-center), šīs aktivitātes automātiski rāda novērtēto beigu datumu galamērķī. Atkarībā no iestatījuma arī pēdējais datums parasti atjaunina piegādes datumu vai apstiprināto datumu pirkšanas pasūtījuma rindās. Pārsūtīšanas pasūtījuma rindām var iestatīt sistēmu, lai atjauninātu saņemšanas datumu.

Lai atvērtu **Ienākošo sūtījumu izsekošanas** lapu, dodieties uz sadaļu **Kopējās izmaksas \> Izsekošana \> Ienākošo sūtījumu izsekošana**.

## <a name="filter-the-activities-list"></a>Filtrēt aktivitāšu sarakstu

Jūs varat izmantot laukus **Reiss** un **Nosūtīšanas konteiners**, kas atrodas **Ienākošo sūtījumu izsekošanas** lapas augšpusē, lai filtrētu lapu tā, lai tā rādītu tikai aktivitātes, kas saistītas ar izvēlēto reisu un/vai nosūtīšanas konteineru.

## <a name="update-tracking-information"></a>Izsekošanas informācija atjaunināšana

Lai atjauninātu reisa vai ceļojuma grafiku, ievadiet pirmās aktivitātes sākuma datumu. Pēc tam tiek atjaunināts pēdējās aktivitātes novērtētais beigu datums. Iestatījums katrai ceļojuma veidnei [Izsekošanas kontroles centrā](delivery-information-setup.md#tracking-control-center) nosaka paredzamo izpildes laiku. Plānotie beigu datumi izmanto izpildes laiku no aktivitātes sākuma datuma. Pēc tam, kad ir reģistrēts faktiskais beigu datums, nākamās darbības sākuma datums tiek atjaunināts uz to pašu datumu, ar kuru tiek atjaunināts iepriekšējās darbības faktiskais beigu datums. Tiek atjaunināts faktiskais izpildes laiks, lai varētu veikt salīdzinājumu un analīzi. Papildu piezīmes var ievadīt laukā **Piezīme**.

Aktivitāšu secību režģī nosaka aktivitāšu secība attiecīgajā ceļojuma veidnē. Ja sekošanas kontrole mainās arī pievienotajā ceļojuma posmā, mainās arī izsekošanas kontrole.

Varat atjaunināt datumus visiem konteineriem, darbību rūtī atlasot **Atjaunināt sākuma datumu** vai **Atjaunināt faktisko beigu datumu**. Alternatīvi jūs varat ievadīt datumus katram sūtījuma konteineram. Šī pieeja ļauj lielāku elastīgumu, jo konteineri var tikt sadalīti vairāku ceļojumu vidē.

## <a name="buttons-on-the-action-pane"></a>Pogas darbību rūtī

Lai strādātu ar atlasīto izmaksu budžetu, varat izmantot pogas lapas **Ienākošo sūtījumu izsekošanas** darbību rūtī. Tālāk esošajā tabulā ir aprakstītas pieejamās opcijas.

| Poga | Apraksts |
|---|---|
| Labot | Rediģējiet reisa vai sūtījuma konteinera ceļojumu. |
| Jauna | Izveidojiet jaunu reisa vai sūtījuma konteinera ceļojumu. |
| Delete | Dzēsiet reisa vai sūtījuma konteinera ceļojumu. |
| Atjaunināt sākuma datumu | Atjauniniet aktivitātes sākuma datumu visiem reisa konteineriem. Kad noteiktas aktivitātes vai ceļojuma kājiņu sākuma datums ir atjaunināts, sekojošie plānotie sākuma datumi tiek atjaunināti, pamatojoties uz norādīto izpildes laiku. |
| Atjaunināt faktisko beigu datumu | Atjauniniet aktivitātes beigu datumu visiem reisa konteineriem. Kad noteiktas aktivitātes vai ceļojuma kājiņu beigu datums ir atjaunināts, sekojošie plānotie sākuma datumi tiek atjaunināti, pamatojoties uz norādīto izpildes laiku. |
| Pievienot aktivitātes | Manuāli pievienot reisam darbību. Piemēram, var pievienot fumigācijas aktivitāti. Papildinājums var izraisīt to, ka jāmaina apstiprinātais preču piegādes datums kuģim vai reisam. Kad aktivitāte ir pievienota ceļojumam, aprēķinātās dienas nav ievadītas līdz brīdim, kad ir atjaunināts ceļojuma kāja sākuma datums. |

## <a name="information-and-settings-on-the-overview-tab"></a>Informācija un iestatījumi cilnē Pārskats

Cilne **Pārskats** parāda visu darbību sarakstu, kas pieder lapas augšpusē atlasītajam reisam un/vai pārvadāšanas konteineram. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai darbībai.

| Lauks | Apraksts |
|---|---|
| Fāze | Aktivitātes kājas ID, kā to definēja ceļojuma veidne. |
| Piegādes veids | Plānotais aktivitātes piegādes veids. |
| Aktivitāte | Šis lauks parasti identificē ar darbību saistīto darbu vai uzdevumu. Tipiski piemēri ietver *Kuģošanas* un *Muitas kontrole*. |
| Apraksts | Garāks aktivitātes apraksts. |
| Sākuma datums | Šis lauks sākotnēji rāda aktivitātes paredzamo sākuma datumu. Tomēr pēc tam, kad ir ievadīts iepriekšējās aktivitātes faktiskais beigu datums, tas parāda faktisko sākuma datumu. Šis lauks tiek izmantots, lai noteiktu paredzamo beigu datumu, pamatojoties uz izpildes laiku. |
| Plānotais beigu datums | Šī lauka vērtība tiek aprēķināta, pamatojoties uz sākuma datumu un izpildes laiku. Parasti vērtību nerediģēsiet tieši. |
| Faktiskais pabeigšanas datums | Lietotājam ir jāatjaunina šis lauks pēc iespējas ātrāk pēc aktivitātes rašanās. Faktiskais izpildes laiks pēc tam tiek atjaunināts. |
| Aprēķināto dienu skaits | Paredzamais laiks (dienās), kas nepieciešams darbības pabeigšanai. |
| Faktiskās dienas | Faktiskais laiks (dienās), kas nepieciešams darbības pabeigšanai. |
| Piezīme | Izmantojiet šo lauku, lai pievienotu dažādas piezīmes un detalizētu informāciju par darbību. |

## <a name="information-and-settings-on-the-general-tab"></a>Informācija un iestatījumi cilnē Vispārīgi

Cilne **Vispārīgi** parāda informāciju par sadaļām, kas atlasītas cilnē **Pārskats**. Lai gan tas atkārto daļu no informācijas, kas parādās cilnē **Pārskats**, tajā iekļauta arī papildu informācija par izvēlēto kāju.
