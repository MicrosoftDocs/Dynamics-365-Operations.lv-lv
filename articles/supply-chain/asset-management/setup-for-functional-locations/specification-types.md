---
title: Uzturēšanas atribūtu veidi
description: Šajā rakstā ir izskaidrots, kā izveidot atribūtu tipus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a0aca3ccf24505c064ad59f0adafb771056ba95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887665"
---
# <a name="maintenance-attribute-types"></a>Uzturēšanas atribūtu veidi

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā ir izskaidrots, kā izveidot atribūtu tipus Līdzekļu pārvaldībā. Atribūti tiek izmantoti, lai aprakstītu dažādu elementu īpašības. Varat iestatīt atribūtus tālāk norādītajos elementos:

- [Funkcionālo novietojumu tipi](../setup-for-functional-locations/functional-location-types.md)
- [Funkcionālo novietojumu izveide](../functional-locations/create-functional-locations.md)
- [Līdzekļu tipi](../setup-for-objects/object-types.md)
- Līdzekļi

Atribūti, kurus var iestatīt, atšķiras atkarībā no elementa. Piemēram, funkcionālajam novietojumam var iestatīt atribūtus atrašanās vietas konfigurācijai un fiziskajam lielumam. Līdzekļa veidam vai līdzeklim var iestatīt dzinēja tilpuma, enerģijas patēriņa un maksimālās noslodzes atribūtus atšķirīgos apstākļos.

## <a name="create-attribute-types"></a>Izveidot atribūta veidu

Varat izveidot savus atribūtu veidus. Turklāt varat pārsūtīt preces dimensijas uz lapu **Atribūtu veidi**.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Atribūtu veidi**.
2. Pirmo reizi iestatot atribūtu veidus, atlasiet **Izveidot preces dimensijas**, lai automātiski pārsūtītu standarta preču dimensijas.
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]