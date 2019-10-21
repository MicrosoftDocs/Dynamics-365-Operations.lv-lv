---
title: Darba pasūtījumi un pamatlīdzekļi
description: Šajā tēmā ir paskaidroti darba pasūtījumi un pamatlīdzekļi līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250833"
---
# <a name="work-orders-and-fixed-assets"></a>Darba pasūtījumi un pamatlīdzekļi


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Līdzekļu pārvaldībā līdzekļi var būt saistīti ar pamatlīdzekļiem, un šiem līdzekļiem varat izveidot darba pasūtījumus. Ja izmantojat šo funkcionalitāti, varat iegūt pilnīgu pārskatu par pamatlīdzekļiem, saistītajiem investīciju projektiem un izmaksām, kas reģistrētas ieguldījumu projektiem moduļos **Projekta pārvaldība un uzskaite** un **Pamatlīdzekļi**.

>[!NOTE]
>Lauks **Pamatlīdzekļa numurs** darba pasūtījuma uzdevuma projektā tiek aizpildīts tikai tad, ja darba pasūtījuma uzdevuma projektā kā projekta veids ir izvēlēts veids “Investīcijas”.

![1. attēls](media/24-work-orders.png)

Šī procedūra apraksta relāciju starp līdzekļiem, darba pasūtījumiem, darba pasūtījuma uzdevuma projektiem un pamatlīdzekļiem.

1. Jūs izveidojat līdzekli, kas attiecas uz pamatlīdzekli, kā parādīts attēlā zemāk.

![2. attēls](media/25-work-orders.png)

2. Kad iestatāt darba pasūtījuma veidus (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Darba pasūtījumu veidi**), jūs izveidojat darba pasūtījuma veidu ieguldījumu apstrādei. Skatiet arī sadaļu [Darba pasūtījumu veidi](../setup-for-work-orders/work-order-types.md).

![3. attēls](media/26-work-orders.png)

3. Kad iestatāt darba pasūtījuma projekta grupas (saite **Līdzekļa pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana** > **Projekta gripa**), jūs izveidojat relāciju starp darba pasūtījuma veidu, kas tiek izmantots ieguldījumiem, un projekta grupu, kas izveidota ieguldījumiem modulī **Projekta pārvaldība un uzskaite** (**Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Projekta grupas**).

![4. attēls](media/27-work-orders.png)

4. Veidojot darba pasūtījumu, kas attiecas uz pamatlīdzekļu objektu, jūs izvēlaties darba pasūtījuma veidu, kas tiek izmantots ieguldījumu apstrādei, piemēram, “Investīcijas”.

5. Kad darba pasūtījums ir izveidots, ar to saistītais darba pasūtījuma veids tiek parādīts sadaļā **Visi darba pasūtījumi**.

![5. attēls](media/28-work-orders.png)

6. Kad darba pasūtījums ir izveidots, ar darba pasūtījumu saistīts projekts tiek izveidots sadaļā **Projekta pārvaldība un uzskaite** > **Visi projekti**. Jūs varat apskatīt ar projektu saistīto informāciju, noklikšķinot uz darba pasūtījuma saites **Projekta ID** (sadaļā **Līdzekļu pārvaldība** atveriet darba pasūtījumu sadaļā Detalizētas informācijas skats > **Rindas informācija** kopsavilkuma cilne > **Vispārīgi** cilnes lauks > **Projekta ID**).

![6. attēls](media/29-work-orders.png)

7. Sadaļā **Pamatlīdzekļi** jūs varat skatīt pārskatu par projektiem, kas saistīti ar pamatlīdzekli (**Pamatlīdzekļi** > **Pamatlīdzekļi** > **Pamatlīdzekļi** > noklikšķiniet uz pamatlīdzekļa laukā **Pamatlīdzekļa numurs** > skatiet saturu rūtī **Saistītā informācija** > sadaļā **Saistītie projekti**).

