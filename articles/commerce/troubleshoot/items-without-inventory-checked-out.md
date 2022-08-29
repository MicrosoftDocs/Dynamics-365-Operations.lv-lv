---
title: Vienības bez krājumiem var izrakstīt
description: Šajā rakstā ir sniegtas traucējummeklēšanas norādes, kas var palīdzēt, kad debitori var pievienot saviem grozam krājumus ārpus rezervēm un turpināt paņemšanu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282739"
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
