---
title: Uzturēšanas pieprasījumu dzīves cikla stāvokļi
description: Šajā tēmā ir aprakstīts, kā iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ece0fc1121211706350d804fec59e72ef08282fcba4e65f557a510834738b11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743678"
---
# <a name="maintenance-request-lifecycle-states"></a>Uzturēšanas pieprasījumu dzīves cikla stāvokļi

[!include [banner](../../includes/banner.md)]

 


Uzturēšanas pieprasījumadzīves cikla stāvokļi nosaka posmus, kuriem pieprasījums var iet cauri. Piemēri ietver **Izveidots**, **Aktīvs** un **Pabeigts**. Kad uzturēšanas pieprasījums tiek pārvērsts par darba pasūtījumu, uzturēšanas pieprasījuma dzīves cikla stāvoklis ir jāatjaunina uz **Pabeigts** vai **Aizvērts**, lai norādītu, ka uzturēšanas pieprasījums vairs nav aktīvs. Saraksta lapā **Visi uzturēšanas pieprasījumi** varat skatīt visus uzturēšanas pieprasījumus neatkarīgi no to dzīves cikla stāvokļa.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla stāvokļi**.
2. Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla stāvokli.
3. Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.

    Kopsavilkuma cilnes **Detalizēta informācija** laukā **Dzīves cikla modeļi** ir parādīts to uzturēšanas pieprasījumu dzīves cikla modeļu skaits, kuri izmanto dzīves cikla stāvokli.

5. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Aktīvs** uz **Jā**, ja uzturēšanas pieprasījumam ir jābūt aktīvam, kamēr tas atrodas šajā dzīves cikla stāvoklī.
6. Iestatiet opciju **Iestatīt faktisko beigu datumu** uz **Jā**, ja faktiskais beigu datums un laiks ir automātiski jāievada uzturēšanas pieprasījumā, kas ir šajā dzīves cikla stāvoklī.
7. Iestatiet opciju **Izveidot darba pasūtījumu** uz **Jā**, ja darba pasūtījumu var izveidot no uzturēšanas pieprasījuma, kas ir šajā dzīves cikla stāvoklī.
8. Iestatiet opciju **Dzēst** uz **Jā**, ja uzturēšanas pieprasījumu var dzēst, kamēr tas atrodas šajā dzīves cikla stāvoklī.
9. Kopsavilkuma cilnē **Atjaunināt** opcijas **Ienākošie** un **Izejošie** sadaļā **Līdzeklis** ir būtiskas, lietojot noliktavas labošanu. Iestatiet atbilstošo opciju uz **Jā**, ja līdzekļu, kas atlasīti uzturēšanas pieprasījumā, līdzekļa dzīves cikla stāvoklis ir automātiski jāatjaunina uz **Ienākošie** vai **Izejošie**, kad šī uzturēšanas pieprasījuma dzīves cikla stāvoklis ir iestatīts uz **Ienākošie** vai **Izejošie**.

Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla stāvokļi** piemērs.

![Uzturēšanas pieprasījumu dzīves cikla stāvokļu lapa.](media/02-setup-for-requests.png)

> [!NOTE]
> Uzturēšanas pieprasījuma dzīves cikla stāvokļi, dzīves cikla stāvokļa grupas un veidi ir saistīti ar darba pasūtījuma dzīves cikla stāvokļiem, dzīves cikla stāvokļa grupām un veidiem, un tiek lietoti tādā pašā veidā. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Uzturēšanas pieprasījuma dzīves cikla modeļu iestatīšana

Kad esat izveidojis dzīves cikla stāvokļus, kas nepieciešami uzturēšanas pieprasījumiem, tos var iedalīt cikla stāvokļa grupās vai dzīves cikla modeļos. Uzturēšanas pieprasījuma dzīves cikla modeļi tiek lietoti, lai izveidotu plūsmu, ko var izmantot dažādiem uzturēšanas pieprasījumu veidiem. Jāizveido vismaz viens standarta uzturēšanas pieprasījuma dzīves cikla modelis.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla modeļi**.
2. Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla modeli.
3. Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.

    Kopsavilkuma cilnē **Detalizēta informācija** laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti šajā līdzekļa dzīves cikla modelī. Laukā **Uzturēšanas pieprasījumu veidi** ir parādīts to uzturēšanas pieprasījumu veidu skaits, kuri izmanto šo dzīves cikla modeli.

5. Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet dzīves cikla stāvokļus, kuri būtu jāiekļauj dzīves cikla modelī:

    - Lai dzīves cikla modelim pievienotu dzīves cikla stāvokli, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi.](media/03-setup-for-requests.png) Lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
    - Lai iekļautu visus pieejamos dzīves cikla stāvokļus dzīves cikla modelī, atlasiet pogu **Atlasīt visus pieejamos dzīves cikla stāvokļus** ![Atlasīt visus pieejamos dzīves cikla stāvokļus.](media/04-setup-for-requests.png). Visi dzīves cikla stāvokļi tiek pārvietoti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
    - Lai no dzīves cikla modeļa noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogu ![Bultiņa pa kreisi.](media/05-setup-for-requests.png) Lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.

6. Kopsavilkuma cilnē **Vispārīgi** lauki sadaļā **Atjauninājumi** ir būtiski, ja izmantojat labošanu noliktavā.

    - Lauka **Saņemtā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek saņemti labošanai noliktavā.
    - Laukā **Piegādātā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek atgriezti pēc remonta.

Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla modeļi** piemērs.

![Uzturēšanas dzīves cikla modeļu lapa.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]