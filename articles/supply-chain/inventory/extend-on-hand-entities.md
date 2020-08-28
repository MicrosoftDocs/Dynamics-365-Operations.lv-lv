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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: e276348a63bfdb9e712c0ea86e6c2a68c50872c0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665408"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="53886-103">Paplašināt krājumu rīcībā esošos datu elementus</span><span class="sxs-lookup"><span data-stu-id="53886-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53886-104">Microsoft Dynamics 365 Supply Chain Management nodrošina [paplašināmības](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) līdzekļus, kas ļauj jums [pievienot laukus tabulām, izmantojot paplašinājumu](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span><span class="sxs-lookup"><span data-stu-id="53886-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="53886-105">Šī tēma sniedz piemēru, kas parāda, kā pievienot paplašinātos laukus `INVENTORSITEONHANDENTITY` un `INVENTWAREHOUSEONHANDENTITY` skatiem, lai rīcībā esošo krājumu datu subjektu iespējas varētu strādāt ar paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="53886-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="53886-106">Papildu informāciju par datu elementiem skatiet [datu pārvaldības pārskatā](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="53886-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="53886-107">Šeit ir saraksts ar dažām rīcībā esošo krājumu datu vienībām:</span><span class="sxs-lookup"><span data-stu-id="53886-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="53886-108">Rīcībā esošie krājumi pēc vietas</span><span class="sxs-lookup"><span data-stu-id="53886-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="53886-109">Rīcībā esošie krājumi pēc vietas V2</span><span class="sxs-lookup"><span data-stu-id="53886-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="53886-110">Rīcībā esošie krājumi pēc noliktavas</span><span class="sxs-lookup"><span data-stu-id="53886-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="53886-111">Rīcībā esošie krājumi pēc noliktavas v2</span><span class="sxs-lookup"><span data-stu-id="53886-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="53886-112">Pēc lauku pievienošanas tabulām, kas tiek izmantotas `inventSiteOnHandView` skatā, ir jāsinhronizē programma, lai paplašinājumi tiktu pareizi atpazīti.</span><span class="sxs-lookup"><span data-stu-id="53886-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="53886-113">Paplašiniet `InventSiteOnHandView` skatu, pievienojot paplašinājuma lauku.</span><span class="sxs-lookup"><span data-stu-id="53886-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="53886-114">Paplašiniet `InventSiteOnHandAggregatedView` skatu ar paplašinājuma laukiem.</span><span class="sxs-lookup"><span data-stu-id="53886-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="53886-115">Paplašiniet `InventSiteOnHandAggregatedViewBuilder` viewBuilder klasi, modificējot `getExtensionFields()` metodi.</span><span class="sxs-lookup"><span data-stu-id="53886-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="53886-116">Šādā veidā, kad viewBuilder sinhronizācija tiek palaista, varat kartēt vecos skatu laukus jaunos skatījuma laukos.</span><span class="sxs-lookup"><span data-stu-id="53886-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="53886-117">Piemēram, `InventTable` tabulai ir pievienoti šādi četri lauki, izmantojot paplašinājumu:</span><span class="sxs-lookup"><span data-stu-id="53886-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="53886-118">Pielāgots lauks 1</span><span class="sxs-lookup"><span data-stu-id="53886-118">Custom field 1</span></span>
- <span data-ttu-id="53886-119">Pielāgots lauks 2</span><span class="sxs-lookup"><span data-stu-id="53886-119">Custom field 2</span></span>
- <span data-ttu-id="53886-120">Pielāgots lauks 3</span><span class="sxs-lookup"><span data-stu-id="53886-120">Custom field 3</span></span>
- <span data-ttu-id="53886-121">Pielāgots lauks 4</span><span class="sxs-lookup"><span data-stu-id="53886-121">Custom field 4</span></span>

<span data-ttu-id="53886-122">Šādā gadījumā `getExtensionFields()` metode ir jāmodificē tālāk aprakstītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="53886-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

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

<span data-ttu-id="53886-123">Kad šīs darbības ir izpildītas, varat paplašināt rīcībā esošos krājumus pēc vietas un rīcībā esošos krājumus pēc noliktavas datu subjektiem, pievienojot jaunos laukus.</span><span class="sxs-lookup"><span data-stu-id="53886-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="53886-124">Šādā veidā tiek nodrošināts, ka paplašinātie lauki tiek atpazīti un iekļauti datu migrācijas, kas izmanto šos datu elementus, laikā.</span><span class="sxs-lookup"><span data-stu-id="53886-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
