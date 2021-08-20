---
title: Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem
description: Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fada426b03aa8a908c3351932a288c911cb8c60fa13ccbfbfd0ceed232759a88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736044"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem

[!include [banner](../../includes/banner.md)]

Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai. Šo uzdevumu parasti veic preces noformētājs.


## <a name="create-a-product-number-nomenclature"></a>Izveidot preces numura nomenklatūru

1. Dodieties uz **Preču informācijas pārvaldība \> Iestātījums \> Produktu nomenklatūra**.
1. Atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet nomenklatūras nosaukumu, kas palīdz identificēt mērķa produkta izmēru grupu, piemēram, `ColorSize`.
1. Laukā **Apraksts** ierakstiet kādu vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Galvenā produkta** numuru.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Krāsa**.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Izmērs**.
1. Aizvērt lapu.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Piešķirt nomenklatūru preces šablonam

1. Atlasiet **Produkta izmēru grupas**.
2. Atlasiet grupu **Izmēra-krāsas produkta izmērs**.
3. Atlasiet **Rediģēt**.
4. Atlasiet **Jā** laukā **Izmantot nomenklatūru**.
5. Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.
6. Aizvērt lapu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]