---
title: Uzturēšanas atribūtu veidi
description: Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot atribūtu veidus.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b221e9168fc60b5927bb92de80bd6b9614ad591c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019808"
---
# <a name="maintenance-attribute-types"></a>Uzturēšanas atribūtu veidi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot atribūtu veidus. Atribūti tiek izmantoti, lai aprakstītu dažādu elementu īpašības. Varat iestatīt atribūtus tālāk norādītajos elementos.

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