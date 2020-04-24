---
title: Darba pasūtījumu veidi
description: Šajā tēmā ir paskaidroti darba pasūtījuma veidi līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 375b18a4bd37ddadecee03a01b3b2125f5cc8d0a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215428"
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

![Darba pasūtījumu veidi](media/16-setup-for-work-orders.png)
