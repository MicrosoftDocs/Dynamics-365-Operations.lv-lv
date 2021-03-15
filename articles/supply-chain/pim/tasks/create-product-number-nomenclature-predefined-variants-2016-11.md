---
title: Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem
description: Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007545"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem

[!include [banner](../../includes/banner.md)]

Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai. Šo uzdevumu parasti veic preces noformētājs.


## <a name="create-a-product-number-nomenclature"></a>Izveidot preces numura nomenklatūru
1. Atlasiet **Produkta varianta modeļa definīcija**.
2. Atlasiet **Produkta nomenklatūra**.
3. Atlasiet **Jauns**.
4. Laukā **Nosaukums** ievadiet nomenklatūras nosaukumu, kas palīdz identificēt mērķa produkta izmēru grupu, piemēram, `ColorSize`.
5. Laukā **Apraksts** ierakstiet kādu vērtību.
6. Atlasiet **Pievienot**.
7. Atlasiet **Galvenā produkta** numuru.
8. Atlasiet **Pievienot**.
9. Atlasiet **Pastāvīgais teksts**.
10. Laukā **Teksts** ierakstiet vērtību.
11. Atlasiet **Pievienot**.
12. Atlasiet **Krāsa**.
13. Atlasiet **Pievienot**.
14. Atlasiet **Pastāvīgais teksts**.
15. Laukā **Teksts** ierakstiet vērtību.
16. Atlasiet **Pievienot**.
17. Atlasiet **Izmērs**.
18. Aizvērt lapu.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Piešķirt nomenklatūru preces šablonam
1. Atlasiet **Produkta izmēru grupas**.
2. Atlasiet grupu **Izmēra-krāsas produkta izmērs**.
3. Atlasiet **Rediģēt**.
4. Atlasiet **Jā** laukā **Izmantot nomenklatūru**.
5. Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.
6. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]