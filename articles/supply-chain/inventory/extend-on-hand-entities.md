---
title: Paplašināt krājumu rīcībā esošos datu elementus
description: Šajā rakstā sniegts piemērs, kā pievienot paplašinātus laukus skatā INVENTORSITEONHANDENTITY un INVENTWAREDALEONHANDENTITY, lai rīcībā esošo datu entītiju iespējas varētu strādāt ar paplašinājumiem.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906042"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Paplašināt krājumu rīcībā esošos datu elementus

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management nodrošina [paplašināmības](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) līdzekļus, kas ļauj jums [pievienot laukus tabulām, izmantojot paplašinājumu](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Šajā rakstā sniegts piemērs `INVENTORSITEONHANDENTITY``INVENTWAREHOUSEONHANDENTITY`, kurā parādīts, kā pievienot paplašinātus laukus un skatus, lai rīcībā esošo krājumu datu entītiju iespējas varētu strādāt ar paplašinājumiem. Papildu informāciju par datu elementiem skatiet [datu pārvaldības pārskatā](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Šeit ir saraksts ar dažām rīcībā esošo krājumu datu vienībām:
>
> - Rīcībā esošie krājumi pēc vietas
> - Rīcībā esošie krājumi pēc vietas V2
> - Rīcībā esošie krājumi pēc noliktavas
> - Rīcībā esošie krājumi pēc noliktavas v2

Pēc lauku pievienošanas tabulām, kas tiek izmantotas `inventSiteOnHandView` skatā, ir jāsinhronizē programma, lai paplašinājumi tiktu pareizi atpazīti.

1. Paplašiniet `InventSiteOnHandView` skatu, pievienojot paplašinājuma lauku.
1. Paplašiniet `InventSiteOnHandAggregatedView` skatu ar paplašinājuma laukiem.
1. Paplašiniet `InventSiteOnHandAggregatedViewBuilder` viewBuilder klasi, modificējot `getExtensionFields()` metodi. Šādā veidā, kad viewBuilder sinhronizācija tiek palaista, varat kartēt vecos skatu laukus jaunos skatījuma laukos.

Piemēram, `InventTable` tabulai ir pievienoti šādi četri lauki, izmantojot paplašinājumu:

- Pielāgots lauks 1
- Pielāgots lauks 2
- Pielāgots lauks 3
- Pielāgots lauks 4

Šādā gadījumā `getExtensionFields()` metode ir jāmodificē tālāk aprakstītajā veidā.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Kad šīs darbības ir izpildītas, varat paplašināt rīcībā esošos krājumus pēc vietas un rīcībā esošos krājumus pēc noliktavas datu subjektiem, pievienojot jaunos laukus. Šādā veidā tiek nodrošināts, ka paplašinātie lauki tiek atpazīti un iekļauti datu migrācijas, kas izmanto šos datu elementus, laikā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]