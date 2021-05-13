---
title: Preces numuru nomenklatūras izveide konfigurētiem preces variantiem
description: Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921015"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Preces numuru nomenklatūras izveide konfigurētiem preces variantiem

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam. Šajā procedūrā ir parādīts, kā jūs varat izveidot konfigurācijas nomenklatūru preces konfigurācijas modeļa komponentam. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Jauna preces numura nomenklatūra tiek piešķirta D0004 preces šablonam. Šo uzdevumu parasti veic preces noformētājs.

## <a name="create-a-product-number-nomenclature"></a>Izveidot preces numura nomenklatūru

1. Dodieties uz **Preču informācijas pārvaldība \> Iestātījums \> Produktu nomenklatūra**.
1. Atlasiet **Jauns**.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
1. Laukā **Apraksts** ierakstiet kādu vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Galvenā produkta numurs**.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasīt **Konfigurācija**.
1. Aizvērt lapu.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Piešķirt preces numura nomenklatūru preces šablonam

1. Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Produktu šabloni**.
1. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Preces numurs**, izmantojot vērtību 'D'.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Atlasiet **Rediģēt**.
1. Atlasiet *Jā* laukā **Izmantot nomenklatūru**.
1. Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.
1. Aizvērt lapu.
1. Aizvērt lapu.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Izveidot nomenklatūru preces konfigurācijas modeļa komponentam

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Atlasiet **Rediģēt**.
1. Atlasiet *Jā* laukā **Izmantot konfigurācijas nomenklatūru**.
1. Atlasiet **Pievienot**.
1. Atlasiet **Atribūta vērtība**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Atribūta vērtība**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Atribūta vērtība**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Atribūta vērtība**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Pastāvīgais teksts**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Teksts** ierakstiet vērtību.
1. Atlasiet **Pievienot**.
1. Atlasiet **Numuru sērijas vērtība**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Numuru sērija** ievadiet vai atlasiet kādu vērtību.
1. Aizvērt lapu.
1. Aizvērt lapu.
1. Aizvērt lapu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]