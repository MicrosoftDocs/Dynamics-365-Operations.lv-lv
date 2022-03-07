---
title: Plānošanas optimizācijas izlaišanas process un izlaišanas vēsture
description: Šajā tēmā ir sniegta informācija par izlaišanas procesu un izlaišanas vēsturi optimizācijas plānošanai.
author: crytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1bf08fc75aa2c05b2f2974ee46ec16609505f696
ms.sourcegitcommit: b5f2d88ff4e0a234fa6b9ee33516425e54ff2c3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/21/2021
ms.locfileid: "7506787"
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
| <p>Pievienots atbalsts galvenajiem plāniem ar opciju **Plānošanas metode** iestatītu uz vērtību *Operāciju plānošana*.</p><p>Lapā **Maršrutu grupas** ievērojiet iestatījumus aizzīmes laukiem **Aktivizācija**, **Darba laiks** un **Veiktspēja** rindām ar **Maršrutēšanas/uzdevuma veidu** *Iestatīšana* vai *Process*. </p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi. | <p>Operāciju plānošana ir pieejama līdzekļu pārvaldībā no 10.0.20. versijas.</p><p>Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai*</p>  | 2021. gada 9.—17. septembris |
| Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi. | Līdzekļu pārvaldība nav nepieciešama. | 2021. gada 25.—30. augusts |
| <p>Pievienotais **Izpildes laika** lauks plānotajiem pasūtījumiem.</p><p>Vispārējie veiktspējas, kvalitātes un stabilitātes uzlabojumi.</p> | Līdzekļu pārvaldība nav nepieciešama. | 2021. gada 12.—17. augusts |
| <p>Pievienoto resursu tipa prasības neierobežotas noslodzes plānošanai.</p><p>Uzlaboto resursu efektivitāte un kalendāra efektivitāte neierobežotas noslodzes plānošanai.</p><p>Papildinformāciju skatiet sadaļā [Plānošana ar neierobežotu noslodzi](infinite-capacity-planning.md). | <p>Pieejama līdzekļu pārvaldībā no versijas 10.0.20.</p><p>Līdzekļa nosaukums: *Bezgalīga noslodzes plānošana plānošanas optimizācijai*</p> | 2021. gada 6.—12. jūlijs |
| Vispārējie kvalitātes uzlabojumi. | Līdzekļu pārvaldība nav nepieciešama. | 2021. gada 6.—12. jūlijs |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
