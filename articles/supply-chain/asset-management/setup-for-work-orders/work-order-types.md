---
title: Darba pasūtījumu veidi
description: Šajā rakstā skaidroti darba pasūtījumu veidi Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12745960f903ebc14208f2c8a01f076ed27a38d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891181"
---
# <a name="work-order-types"></a>Darba pasūtījumu veidi

[!include [banner](../../includes/banner.md)]

 

Darba pasūtījumu veidi tiek izmantoti, lai kategorizētu darba pasūtījumus. Piemēram, jums var būt darba pasūtījumi, kas saistīti ar profilaktisko uzturēšanu vai koriģējošo uzturēšanu.

Darba pasūtījuma veids definē piederību darba pasūtījuma dzīves cikla modelim. Darba pasūtījuma dzīves cikla modelis definē darba pasūtījuma dzīves cikla stāvokļus, kurus var iestatīt darba pasūtījumā. (Darba pasūtījumu dzīves cikla stāvokļu piemēri ir **Izveidots**, **Apstrādē** un **Pabeigts**.)

Lai iegūtu vairāk informācijas par darba pasūtījumu dzīves cikla stāvokļiem un projekta posmiem, skatiet sadaļu [Darba pasūtījuma dzīves cikla stāvokļi](work-order-lifecycle-states.md).

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Darba pasūtījumu veidi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu darba pasūtījuma veidu.
3. Laukā **Darba pasūtījuma veids** ievadiet darba pasūtījuma veida ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.
5. Atlasiet dzīves cikla modeli laukā **Darba pasūtījuma dzīves cikla modelis**.
5. Iestatiet opciju **Viens uzturēšanas speciālists** uz **Jā**, ja visiem darba pasūtījumu uzdevumiem, kas saistīti ar šī veida darba pasūtījumu, ir jābūt plānotiem vienam uzturēšanas speciālistam.
6. Laukā **Izmaksu veids** atlasiet **Labojošs**, **Profilaktisks** vai **Investīciju** pēc atbilstības. Visiem darba pasūtījuma uzdevumiem darba pasūtījumā jābūt ar vienādu izmaksu veidu.
7. Sadaļā **Obligāts** iestatiet atbilstošās opcijas uz **Jā**, lai norādītu, kura ar defektu vai uzturēšanas dīkstāvi saistītā informācija tiek pievienota šī veida darba pasūtījumam.

    > [!NOTE]
    > Opcijas sadaļā **Obligāts** ir saistītas ar opcijām kopsavilkuma cilnē **Validēt** lapā **Darba pasūtījuma dzīves cikla stāvokļi** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Dzīves cikla stāvokļi**).

8. Atlasiet **Saglabāt**.

![Darba pasūtījumu veidi.](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]