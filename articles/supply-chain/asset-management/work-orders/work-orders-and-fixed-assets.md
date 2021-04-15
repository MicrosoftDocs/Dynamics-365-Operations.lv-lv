---
title: Darba pasūtījumi un pamatlīdzekļi
description: Šajā tēmā ir paskaidroti darba pasūtījumi un pamatlīdzekļi Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816728"
---
# <a name="work-orders-and-fixed-assets"></a>Darba pasūtījumi un pamatlīdzekļi

[!include [banner](../../includes/banner.md)]


Līdzekļu pārvaldībā līdzekļi var būt saistīti ar pamatlīdzekļiem, un šiem līdzekļiem varat izveidot darba pasūtījumus. Ja izmantojat šo funkcionalitāti, varat iegūt pilnīgu pārskatu par pamatlīdzekļiem, saistītajiem investīciju projektiem un izmaksām, kas reģistrētas ieguldījumu projektiem moduļos **Projekta pārvaldība un uzskaite** un **Pamatlīdzekļi** programmā Microsoft Dynamics 365 for Finance and Operations.

>[!NOTE]
>Lauks **Pamatlīdzekļa numurs** darba pasūtījuma uzdevuma projektā tiek aizpildīts tikai tad, ja darba pasūtījuma uzdevuma projektā kā projekta veids ir izvēlēts veids **Investīcijas**.

Attēlā ir parādīta saite starp investīciju projektu **Projekta vadības un uzskaites** modulī un darba pasūtījuma darba projektu.

![1. attēls](media/24-work-orders.png)

Šī procedūra apraksta relāciju starp līdzekļiem, darba pasūtījumiem, darba pasūtījuma uzdevuma projektiem un pamatlīdzekļiem.

1. Jūs izveidojat pamatlīdzeklim piesaistītu pamatlīdzekli.

![2. attēls](media/25-work-orders.png)

2. Kad iestatāt darba pasūtījuma veidus **Darba pasūtījumu veidi** lapā (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Darba pasūtījumu veidi**), jūs izveidojat darba pasūtījuma veidu ieguldījumu apstrādei. Skatiet arī sadaļu [Darba pasūtījumu veidi](../setup-for-work-orders/work-order-types.md).

![3. attēls](media/26-work-orders.png)

3. Kad iestatāt darba pasūtījuma projekta grupas cilnē **Projektu grupa** lapā **Darba pasūtījumu projektu iestatīšana** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana**), jūs izveidojat relāciju starp darba pasūtījuma veidu, kas tiek izmantots ieguldījumiem, un projekta grupu, kas izveidota ieguldījumiem **Projektu grupu** lapā modulī **Projekta pārvaldība un uzskaite** (**Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Projekta grupas**).

![4. attēls](media/27-work-orders.png)

4. Veidojot darba pasūtījumu, kas attiecas uz pamatlīdzekļu objektu, jūs izvēlaties darba pasūtījuma veidu, kas tiek izmantots ieguldījumu apstrādei, piemēram, **Investīcijas**.

5. Kad darba pasūtījums ir izveidots, ar to saistītais darba pasūtījuma veids tiek parādīts lapā **Visi darba pasūtījumi**.

![5. attēls](media/28-work-orders.png)

6. Kad darba pasūtījums ir izveidots, projekts, kas saistīts ar darba pasūtījumu, tiek izveidots lapā **Visi projekti** modulī **Projekta vadība un uzskaite** (**Projektu vadība un uzskaite** > **Projekti** > **Visi projekti**). Lai skatītu informāciju, kas saistīta ar projektu, atlasiet saiti laukā **Projekta ID** cilnē **Vispārīgi** kopsavilkuma cilnē **Rindas detaļas** detalizētajā skatā **Visi darba pasūtījumi** lapā **Līdzekļu pārvaldības** modulī (**Līdzekļu pārvaldība** > **Kopējais** > **Darba pasūtījumi** > **Visiem darba pasūtījumi**).

![6. attēls](media/29-work-orders.png)

7. Lai skatītu pārskatu par projektiem, kas saistīti ar pamatlīdzekļiem, atlasiet **Pamatlīdzekļi** > **Pamatlīdzekļi** > **Pamatlīdzekļi** un pēc tam laukā **Pamatlīdzekļa numurs** atlasiet saiti pamatlīdzeklim, lai atvērtu detaļu skatu. Paplašiniet **Saistīto informācijas** rūti lapas labajā pusē un atlasiet **Saistītie projekti** kopsavilkuma cilni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]