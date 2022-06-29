---
title: Darba pasūtījumu izveide no uzturēšanas pieprasījumiem
description: Šajā rakstā skaidrots, kā izveidot darba pasūtījumu no uzturēšanas pieprasījuma Līdzekļu pārvaldībā.
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
ms.openlocfilehash: bb54ec3466086afbd87a023a40e346a6a3464c98
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017179"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Darba pasūtījumu izveide no uzturēšanas pieprasījumiem

[!include [banner](../../includes/banner.md)]

 


Pēc uzturēšanas pieprasījumu izveides tos var viegli pārvērst par darba pasūtījumiem. Šajā rakstā aprakstīts ātrākais veids, kā strādāt ar uzturēšanas pieprasījumiem, vienlaicīgi atjaunināt vairākus uzturēšanas pieprasījumus un pēc tam izveidot darba pasūtījumu vairākiem uzturēšanas pieprasījumiem. Lapā **Aktīvie uzturēšanas pieprasījumi** vai **Mania funkcionālā novietojuma uzturēšanas pieprasījumi** varat vienlaikus strādāt ar vienu uzturēšanas pieprasījumu un pārveidot vienu uzturēšanas pieprasījumu par darba pasūtījumu.

> [!NOTE]
> Katru uzturēšanas pieprasījumu var saistīt tikai ar vienu darba pasūtījumu. Taču vienā darba pasūtījumā var iekļaut vairākus uzturēšanas pieprasījumus pat tad, ja uzturēšanas pieprasījumiem ir dažādi līdzekļi.

1. Atlasiet Līdzekļu **pārvaldības uzturēšanas** \> **pieprasījumus** \> **visiem uzturēšanas pieprasījumiem**.
2. Pirms jūs varat izveidot darba pasūtījumu no uzturēšanas pieprasījumiem, ir jāatlasa vismaz uzturēšanas darba veids uzturēšanas pieprasījumiem, kā arī uzturēšanas darba veida variants un tirdzniecība, ja šī informācija ir svarīga. Režģa skatā varat viegli atjaunināt informāciju par uzturēšanas pieprasījumu.
3. Kad esat gatavs izveidot darba pasūtījumu, atlasiet uzturēšanas pieprasījumus, ko tajā iekļaut.

    - Ja atlasāt vairākus uzturēšanas pieprasījumus, kas ir jāpārvērš par darba pasūtījumu, tad gan lauks **Līdzeklis**, gan lauks **Uzturēšanas darba veids** ir jāiestata pirms darba pasūtījuma izveides.
    - Ja atlasāt vienu uzturēšanas pieprasījumu, kas jāpārvērš par darba pasūtījumu, pirms darba pasūtījuma izveides ir jāiestata tikai lauks **Līdzeklis**. Tomēr, izveidojot darba pasūtījumu, varat atlasīt uzturēšanas darba veidu (un saistīto uzturēšanas darba veida variantu un tirdzniecību, ja šī informācija ir svarīga) dialoglodziņā **Izveidot darba pasūtījumu**.

4. Atlasiet **Darba pasūtījums**.
5. Dialoglodziņā **Izveidot darba pasūtījumu** iestatiet laukus un pēc tam atlasiet **Labi**.

    Ziņojumu josla var paziņot, ka ir izveidots jauns darba pasūtījums.

    Turklāt, izveidojot darba pasūtījumu, kas ir balstīts uz uzturēšanas pieprasījumu, ja ar uzturēšanas pieprasījumu saistītais līdzeklis ir ietverts garantijas līgumā, ziņojumu josla paziņo par garantijas līgumu.

6. Atlasiet **Līdzekļu pārvaldības** \> **darbs pasūtījumus** \> **visiem darba** pasūtījumiem un atveriet jauno darba pasūtījumu.

    ![Atvērt jaunu darba pasūtījumu.](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]