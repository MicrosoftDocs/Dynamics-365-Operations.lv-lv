---
title: Nomas grupas izveide
description: Šajā rakstā ir izskaidrots, kā iestatīt nomas grupas. Nomas grupas ir vajadzīgas, lai izveidotu jaunas nomas.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd1a6f61346233bf205657917c65fccd82167f7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895027"
---
# <a name="create-a-lease-group"></a>Nomas grupas izveide

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt nomas grupas. Nomas grupas ir vajadzīgas, lai izveidotu jaunas nomas. Nomas grāmatas ir saistītas ar katru nomas grupu. Nomas grāmatas nosaka noklusējuma grāmatas, kas jāizveido katrai nomai. Varat piešķirt konkrētus kontus nomas grupai lapā **Nomas grāmatošanas parametri**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Nomas grāmatas izveide un nomas grupas pievienošana

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grupas**.
2. Lai pievienotu nomas grupu, darbību rūtī atlasiet **Jauns**. Režģim tiek pievienota rinda.
3. Jaunās rindas laukā **Nomas grupa** ievadiet vērtību.
4. Laukā **Apraksts** ievadiet kādu vērtību.

Tikko ievadītā informācija tiek pievienota laukam **Nomas grupa** lapā **Pievienot nomu**.

## <a name="associate-a-book-with-a-lease-group"></a>Grāmatas saistīšana ar nomas grupu

Pēc nomas grupu izveides varat piešķirt grāmatas katrai grupai. Izveidojot nomu un piešķirot to nomas grupai, sistēma izveido grafiku kopu katrai grāmatai, kas saistīta ar nomas grupu.

> [!NOTE]
> Grāmatas ir jāiestata pirms tās var piešķirt nomas grupai.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grupa**.
2. Atlasiet nomas grupu un pēc tam atlasiet **Grāmatas**.
3. Atlasiet **Jauns** un pēc tam laukā **Grāmatas veids** atlasiet grāmatu, ko piešķirt nomas grupai. Nomas grupai varat piešķirt vairākas grāmatas, ja noma jāuzskaita dažādos veidos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
