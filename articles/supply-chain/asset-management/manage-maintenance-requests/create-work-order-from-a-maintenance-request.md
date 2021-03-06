---
title: Darba pasūtījumu izveide no uzturēšanas pieprasījumiem
description: Šajā tēmā izskaidrots, kā izveidot darba pasūtījumu Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c360985509f8f1379ed4a9bd17b95f2d8c85340e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808596"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Darba pasūtījumu izveide no uzturēšanas pieprasījumiem

[!include [banner](../../includes/banner.md)]

 


Pēc uzturēšanas pieprasījumu izveides tos var viegli pārvērst par darba pasūtījumiem. Šajā tēmā aprakstīts ātrākais veids, kā strādāt ar uzturēšanas pieprasījumiem, vienlaicīgi atjaunināt vairākus uzturēšanas pieprasījumus un pēc tam vienlaicīgi izveidot darba pasūtījumu vairākiem uzturēšanas pieprasījumiem. Lapā **Aktīvie uzturēšanas pieprasījumi** vai **Mania funkcionālā novietojuma uzturēšanas pieprasījumi** varat vienlaikus strādāt ar vienu uzturēšanas pieprasījumu un pārveidot vienu uzturēšanas pieprasījumu par darba pasūtījumu.

> [!NOTE]
> Katru uzturēšanas pieprasījumu var saistīt tikai ar vienu darba pasūtījumu. Taču vienā darba pasūtījumā var iekļaut vairākus uzturēšanas pieprasījumus pat tad, ja uzturēšanas pieprasījumiem ir dažādi līdzekļi.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi**.
2. Pirms jūs varat izveidot darba pasūtījumu no uzturēšanas pieprasījumiem, ir jāatlasa vismaz uzturēšanas darba veids uzturēšanas pieprasījumiem, kā arī uzturēšanas darba veida variants un tirdzniecība, ja šī informācija ir svarīga. Režģa skatā varat viegli atjaunināt informāciju par uzturēšanas pieprasījumu.
3. Kad esat gatavs izveidot darba pasūtījumu, atlasiet uzturēšanas pieprasījumus, ko tajā iekļaut.

    - Ja atlasāt vairākus uzturēšanas pieprasījumus, kas ir jāpārvērš par darba pasūtījumu, tad gan lauks **Līdzeklis**, gan lauks **Uzturēšanas darba veids** ir jāiestata pirms darba pasūtījuma izveides.
    - Ja atlasāt vienu uzturēšanas pieprasījumu, kas jāpārvērš par darba pasūtījumu, pirms darba pasūtījuma izveides ir jāiestata tikai lauks **Līdzeklis**. Tomēr, izveidojot darba pasūtījumu, varat atlasīt uzturēšanas darba veidu (un saistīto uzturēšanas darba veida variantu un tirdzniecību, ja šī informācija ir svarīga) dialoglodziņā **Izveidot darba pasūtījumu**.

4. Atlasiet **Darba pasūtījums**.
5. Dialoglodziņā **Izveidot darba pasūtījumu** iestatiet laukus un pēc tam atlasiet **Labi**.

    Ziņojumu josla var paziņot, ka ir izveidots jauns darba pasūtījums.

    Turklāt, izveidojot darba pasūtījumu, kas ir balstīts uz uzturēšanas pieprasījumu, ja ar uzturēšanas pieprasījumu saistītais līdzeklis ir ietverts garantijas līgumā, ziņojumu josla paziņo par garantijas līgumu.

6. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Darba pasūtījumi** \> **Visi darba pasūtījumi** un atveriet jauno darba pasūtījumu.

    ![Atvērt jaunu darba pasūtījumu](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]