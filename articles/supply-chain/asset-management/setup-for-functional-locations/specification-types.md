---
title: Uzturēšanas atribūtu veidi
description: Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot atribūtu veidus.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783426"
---
# <a name="maintenance-attribute-types"></a>Uzturēšanas atribūtu veidi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot atribūtu veidus. Atribūti tiek izmantoti, lai aprakstītu dažādu elementu īpašības. Varat iestatīt atribūtus tālāk norādītajos elementos.

- [Funkcionālo novietojumu veidi](../setup-for-functional-locations/functional-location-types.md)
- [Funkcionālie novietojumi](../functional-locations/create-functional-locations.md)
- [Līdzekļu veidi](../setup-for-objects/object-types.md)
- Pamatlīdzekļu tabula

Atribūti, kurus var iestatīt, atšķiras atkarībā no elementa. Piemēram, funkcionālajam novietojumam var iestatīt atribūtus atrašanās vietas konfigurācijai un fiziskajam lielumam. Līdzekļa veidam vai līdzeklim var iestatīt dzinēja tilpuma, enerģijas patēriņa un maksimālās noslodzes atribūtus atšķirīgos apstākļos.

## <a name="create-attribute-types"></a>Izveidot atribūta veidu

Varat izveidot savus atribūtu veidus. Turklāt varat pārsūtīt preces dimensijas no programmas Microsoft Dynamics 365 for Finance and Operations uz lapu **Atribūtu veidi**.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Atribūtu veidi**.
2. Pirmo reizi iestatot atribūtu veidus, atlasiet **Izveidot preces dimensijas**, lai automātiski pārsūtītu standarta Finance and Operations preču dimensijas.
3. Atlasiet **Jauns**, lai izveidotu jaunu atribūta veidu.
4. Laukā **Atribūta veids** ievadiet atribūta veida nosaukumu.
5. Ievadiet aprakstu laukā **Apraksts**.
6. Laukā **Vienība** pēc vajadzības atlasiet atbilstošo atribūta vienību.
7. Laukā **Datu veids** atlasiet vienības datu veidu.
8. Ja kā datu veidu atlasījāt **Virkne**, veiciet tālāk norādītās darbības, lai izveidotu atribūta veida vērtības.

    1. Atlasiet atribūta veidu un pēc tam atlasiet **Vērtības**.
    2. Laukā **Atribūta vērtības** atlasiet **Jauns**.
    3. Laukā **Atribūta veids** atlasiet atribūta veidu (dimensiju).
    4. Laukā **Vērtība** ievadiet saistīto vērtību.
    5. Ievadiet aprakstu laukā **Apraksts**.
    6. Saglabājiet ierakstu.
    7. Atgriezieties lapā **Atribūtu veidi**.

9. Saglabājiet ierakstu.

    Laukā **Funkcionālie novietojumi** ir norādīts to funkcionālo novietojumu skaits, kuri izmanto atribūta veidu. Laukā **Līdzekļu veidi** ir parādīts to līdzekļu veidu skaits, kuri to izmanto.
