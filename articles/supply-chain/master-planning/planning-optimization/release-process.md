---
title: Plānošanas optimizācijas izlaišanas process un izlaišanas vēsture
description: Šajā rakstā ir sniegta informācija par izlaišanas procesu un izlaišanas vēsturi optimizācijas plānošanai.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682565"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Plānošanas optimizācijas izlaišanas process un izlaišanas vēsture

[!include [banner](../../includes/banner.md)]

Microsoft atjaunina plānošanas optimizāciju ik mēnesi. Tomēr, ņemot vērā biznesa prasības, reizēm tiek izlaisti papildu atjauninājumi starp plānotajiem laidieniem.

Katrs laidiens tiek publicēts atsevišķos reģionos, kuros ir pieejama plānošanas optimizācija. Šis process parasti ilgst trīs dienas.

Kamēr tiek atjaunināta plānošanas optimizācija, vispārējā plānošana var tikt palaista lēnāk nekā parasti.

Vides, kas izmanto plānošanas optimizāciju, automātiski saņem jaunāko laidienu. Nav nepieciešama lietotāja darbība: pakalpojums tiek atjaunināts automātiski. Tomēr neviena pārrāvuma maiņas funkcionalitāte nekad netiek automātiski virzīta uz vidēm. Pēc noklusējuma visas izmaiņas, kas tiek uzskatītas par pārrāvumu, ir izslēgtas, un tās ir skaidri jāieslēdz, izmantojot [līdzekļu pārvaldību](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tāpēc šīs izmaiņas neparādīsies vidēs, līdz tās netiks iespējotas.

Tā kā paziņojumi netiek rādīti, kad jūsu vidē tiek atjaunināta plānošanas optimizācija, varat pārskatīt piezīmes par izlaišanu nākamajā tabulā, lai noteiktu, kad izmaiņas tika izlaistas un kādas funkcijas tās ieviesa. Šajā tabulā ir norādītas izmaiņas, kas tika izlaistas optimizācijas plānošanai, neatkarīgi no tā, vai šīs izmaiņas ir saistītas ar līdzekli no līdzekļu pārvaldības un izpildes datumu.

| Izmaiņas | Līdzekļu pārvaldības informācija | Izlaišanas datumi |
|---|---|---|
| <p>[Partijas atgriešanas kodi](../../inventory/batch-disposition-codes.md)</p><p>Iekļaut vispārējos plānos rīcībā esošos krājumus un krājumu darbību parametrus</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi</p> | Līdzekļu pārvaldība nav nepieciešama | 2022. gada 10.-14. oktobris |
| <p>[Resursu plānošana ar ierobežotu noslodzi](finite-capacity.md)</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi</p> | Līdzekļu pārvaldība nav nepieciešama | 2022. gada 19. septembris |
| Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi | Līdzekļu pārvaldība nav nepieciešama | 2022. gada 29. augusts - 3. septembris |
| <p>[Centralizēta kalendāra uzturēšana](../supply-chain-calendars-master-planning.md)</p><p>[Ieteikumi esošo piedāvājumu optimizēšana](../action-messages.md)</p><p>[Apakšlīgumu slēgšanas atbalsts](../../production-control/manage-subcontract-work-production.md)</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi</p> | Līdzekļu pārvaldība nav nepieciešama | 2022. gada 7.-11. marts |
| Ražošanas pasūtījumu prioritāšu atbalsta plānošana | Pieejama versijā 10.0.25 kā daļa no funkcijas ar nosaukumu Prioritātes *vadīts MRP atbalsts optimizācijas plānošanai*. | 2021. gada 12. novembris |
| Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi | Līdzekļu pārvaldība nav nepieciešama | 2021. gada 12. novembris |
| <p>Atbalstīt apstrādes laika aprēķina formulas, ražošanas maršrutu ar pārklāšanos un ražošanas operāciju skaitu prasību darījumos</p><p>Uzlaboti kļūdu ziņojumi ražošanas plānošanai, kas saistīti ar taimautu, noslodzi, noslodzi un ciklisko maršrutu</p><p>Uzlabota konsekvence, aprēķinot saņemšanas datumus un izdošanas datumus gan plānotajiem, gan apstiprinātajiem pasūtījumiem</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi</p> | Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai* | 2021. gada 22. oktobris |
| <p>Atbalstīt, ņemot vērā brāķa procentus, apstrādes laika aprēķinā</p><p>Atbalstu operācijas numura un materiālu izmantošanai plānošanas laikā</p> | Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai* | 2021. gada 5.-7. oktobris |
| <p>Atbalstu ražošanas maršruta darbu tipiem: rinda **pirms**, gaidīšanas **pēc** un transportēšanas **laiks**</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi</p> | Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai* | 2021. gada 25. septembris |
| <p>Vispārējo plānu atbalsts plānošanas metodei **, kas iestatīta** uz *Operāciju plānošana*</p><p>Maršruta grupu **lapā ņemot** vērā iestatījumus **aktivizēšanai**, **darba** **·** **laikam un Noslodzei izvēles rūtiņas rindām ar tipu Maršruts/darbs ar** iestatījumu *vai* Procesu *·* </p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi</p> | <p>Operāciju plānošana ir pieejama līdzekļu pārvaldībā versijā 10.0.20</p><p>Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai*</p> | 2021. gada 9.—17. septembris |
| Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi | Līdzekļu pārvaldība nav nepieciešama | 2021. gada 25.—30. augusts |
| <p>Pievienotais **Izpildes laika** lauks plānotajiem pasūtījumiem.</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi.</p> | Līdzekļu pārvaldība nav nepieciešama | 2021. gada 12.—17. augusts |
| <p>Pievienotais resursu tipa prasības neierobežotas noslodzes plānošanai</p><p>Uzlabota resursu efektivitāte un kalendāra efektivitāte neierobežotas noslodzes plānošanai</p><p>Papildinformāciju skatiet sadaļā Plānošana [ar neierobežotu noslodzi](infinite-capacity-planning.md)</p> | <p>Pieejams līdzekļu pārvaldībā no versijas 10.0.20</p><p>Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai*</p> | 2021. gada 6.—12. jūlijs |
| Vispārējie kvalitātes uzlabojumi | Līdzekļu pārvaldība nav nepieciešama | 2021. gada 6.—12. jūlijs |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
