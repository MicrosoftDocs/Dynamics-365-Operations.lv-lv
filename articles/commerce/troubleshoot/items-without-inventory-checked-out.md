---
title: Vienības bez krājumiem var izrakstīt
description: Šajā rakstā ir sniegtas traucējummeklēšanas norādes, kas var palīdzēt, kad debitori var pievienot saviem grozam krājumus ārpus rezervēm un turpināt paņemšanu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 24400953d2a17384be8ab3000aa829bf2bcb7192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877189"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Vienības bez krājumiem var izrakstīt

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegtas traucējummeklēšanas norādes, kas var palīdzēt, kad debitori var pievienot saviem grozam krājumus ārpus rezervēm un turpināt paņemšanu.

## <a name="description"></a>Apraksts

Lietotāji var pievienot preci savam grozam, pat ja veikalā nav rīcībā esošu krājumu un tad pāriet uz apmaksas lapu.

## <a name="resolution"></a>Novēršana

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Iespējot rekvizītu Rādīt Nav noliktavā kļūdas Commerce vietnes veidotājā

Lai iespējotu rekvizītu **Rādīt Nav noliktavā kļūdas** Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Atlasiet vietni, pie kuras strādājat.
1. Kreisās puses navigācijā atlasiet **Lapas**.
1. Atlasiet **CartPage**, lai to atvērtu.
1. Atlasiet slotu **1. grozs**, atlasiet **Rediģēt** un pēc tam rekvizītu rūtī atzīmējiet izvēles rūtiņu **Rādīt Nav noliktavā kļūdas**.
1. Saglabājiet un publicējiet lapu.

## <a name="additional-resources"></a>Papildu resursi

[Krājumu iestatījumu lietošana](../inventory-settings.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](../calculated-inventory-retail-channels.md)

[Krājumu buferu un krājumu līmeņu konfigurēšana](../inventory-buffers-levels.md)
