---
title: Papildinformāciju skatiet sadaļā Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju
description: Šajā tēmā ir uzskaitīti līdzekļi, kurus vēl neatbalsta plānošanas optimizācija un kuri nav norādīti lapā Optimizācijas plānošanas atbilstības analīze.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344958"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Papildinformāciju skatiet sadaļā Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju

[!include [banner](../../includes/banner.md)]

Optimizācijas optimizācijas rezultāti var atšķirties no iebūvētās vispārējās plānošanas programmas rezultātiem. To var izraisīt arī vēl nepabeigtas funkcijas. Šajā tēmā ir uzskaitīti līdzekļi, kurus vēl neatbalsta plānošanas optimizācija un kuri nav norādīti lapā **[Optimizācijas plānošanas atbilstības analīze](planning-optimization-fit-analysis.md)**.

| Funkcija | Pašreizējā funkcionalitāte plānošanas optimizācijā |
|---|---|
| Pieļaujamā svara preces | Pieļaujamā svara preces tiek uzskatītas par parastām precēm.|
| Paplašināmās dimensijas | Paplašināmās dimensijas plānotajiem pasūtījumiem ir tukšas, pat ja lapā **Noliktavas dimensiju grupas** vai **Izsekošanas dimensiju grupas** ir atzīmēta izvēles rūtiņa **Vajadzības plāns pēc dimensijas**. |
| Filtrētas ražošanas izpildes | Sīkāku informāciju skatiet [Ražošanas plānošana — filtri](production-planning.md#filters). |
| Prognožu plānošana | Budžeta plānošana netiek atbalstīta. Ieteicams izmantot vispārējo plānošanu, kur budžeta modelis ir piešķirts vispārējai plānam. |
| Plānoto pasūtījumu numuru secība | Plānoto pasūtījumu numuru sērijas netiek atbalstītas. Plānoto pasūtījumu numuri tiek ģenerēti pakalpojuma pusē. |
| Plānot plāna kopēšanu, dzēšanu un plāna versijas tīrīšanu | <p>Tālāk minētās preces ir atspējotas **Vispārējās plānošanas \> Vispārējās plānošanas \> Uzturēšanas plānu** navigācijas rūtī:</p><ul><li>Plāna kopija</li><li>Dzēst plānu</li><li>Ieplānot versijas tīrīšanu</li></ul> |
| Atgrieztie pasūtījumi | Atgriešanas pasūtījumi netiek izskatīti. |
| Ar plānošanu saistītās funkcijas | Papildinformāciju skatiet sadaļā [Plānošana ar neierobežotu noslodzi](infinite-capacity-planning.md#limitations). |
| Transportēšanas kalendārs | Vērtība lapā **Piegādes režīmi** kolonnā **Transportēšanas kalendārs** tiek ignorēta. |

## <a name="additional-resources"></a>Papildu resursi

- [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)
- [Parametri, kas netiek izmantoti plānošanas optimizācijai](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
