---
title: Vienības bez krājumiem var izrakstīt
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad debitori var pievienot savam grozam krājumus, kas nav noliktavā, un turpināt apmaksu.
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018462"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Vienības bez krājumiem var izrakstīt

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad debitori var pievienot savam grozam krājumus, kas nav noliktavā, un turpināt apmaksu.

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
