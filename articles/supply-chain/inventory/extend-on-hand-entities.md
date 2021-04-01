---
title: Paplašināt krājumu rīcībā esošos datu elementus
description: Šī tēma sniedz piemēru, kas parāda, kā pievienot paplašinātos laukus INVENTORSITEONHANDENTITY un INVENTWAREHOUSEONHANDENTITY skatiem, lai rīcībā esošo krājumu datu subjektu iespējas varētu strādāt ar paplašinājumiem.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0f48e424a9ab3349d3c114ecbd01424005b9a9c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219345"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Paplašināt krājumu rīcībā esošos datu elementus

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management nodrošina [paplašināmības](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) līdzekļus, kas ļauj jums [pievienot laukus tabulām, izmantojot paplašinājumu](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Šī tēma sniedz piemēru, kas parāda, kā pievienot paplašinātos laukus `INVENTORSITEONHANDENTITY` un `INVENTWAREHOUSEONHANDENTITY` skatiem, lai rīcībā esošo krājumu datu subjektu iespējas varētu strādāt ar paplašinājumiem. Papildu informāciju par datu elementiem skatiet [datu pārvaldības pārskatā](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

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