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
# <a name="maintenance-attribute-types"></a><span data-ttu-id="b4f66-103">Uzturēšanas atribūtu veidi</span><span class="sxs-lookup"><span data-stu-id="b4f66-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b4f66-104">Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot atribūtu veidus.</span><span class="sxs-lookup"><span data-stu-id="b4f66-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="b4f66-105">Atribūti tiek izmantoti, lai aprakstītu dažādu elementu īpašības.</span><span class="sxs-lookup"><span data-stu-id="b4f66-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="b4f66-106">Varat iestatīt atribūtus tālāk norādītajos elementos.</span><span class="sxs-lookup"><span data-stu-id="b4f66-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="b4f66-107">Funkcionālo novietojumu veidi</span><span class="sxs-lookup"><span data-stu-id="b4f66-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="b4f66-108">Funkcionālie novietojumi</span><span class="sxs-lookup"><span data-stu-id="b4f66-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="b4f66-109">Līdzekļu veidi</span><span class="sxs-lookup"><span data-stu-id="b4f66-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="b4f66-110">Pamatlīdzekļu tabula</span><span class="sxs-lookup"><span data-stu-id="b4f66-110">Assets</span></span>

<span data-ttu-id="b4f66-111">Atribūti, kurus var iestatīt, atšķiras atkarībā no elementa.</span><span class="sxs-lookup"><span data-stu-id="b4f66-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="b4f66-112">Piemēram, funkcionālajam novietojumam var iestatīt atribūtus atrašanās vietas konfigurācijai un fiziskajam lielumam.</span><span class="sxs-lookup"><span data-stu-id="b4f66-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="b4f66-113">Līdzekļa veidam vai līdzeklim var iestatīt dzinēja tilpuma, enerģijas patēriņa un maksimālās noslodzes atribūtus atšķirīgos apstākļos.</span><span class="sxs-lookup"><span data-stu-id="b4f66-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="b4f66-114">Izveidot atribūta veidu</span><span class="sxs-lookup"><span data-stu-id="b4f66-114">Create attribute types</span></span>

<span data-ttu-id="b4f66-115">Varat izveidot savus atribūtu veidus.</span><span class="sxs-lookup"><span data-stu-id="b4f66-115">You can create your own attribute types.</span></span> <span data-ttu-id="b4f66-116">Turklāt varat pārsūtīt preces dimensijas no programmas Microsoft Dynamics 365 for Finance and Operations uz lapu **Atribūtu veidi**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-116">Additionally, you can transfer product dimensions from Microsoft Dynamics 365 for Finance and Operations to the **Attribute types** page.</span></span>

1. <span data-ttu-id="b4f66-117">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Atribūtu veidi**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="b4f66-118">Pirmo reizi iestatot atribūtu veidus, atlasiet **Izveidot preces dimensijas**, lai automātiski pārsūtītu standarta Finance and Operations preču dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b4f66-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard Finance and Operations product dimensions.</span></span>
3. <span data-ttu-id="b4f66-119">Atlasiet **Jauns**, lai izveidotu jaunu atribūta veidu.</span><span class="sxs-lookup"><span data-stu-id="b4f66-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="b4f66-120">Laukā **Atribūta veids** ievadiet atribūta veida nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b4f66-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="b4f66-121">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b4f66-122">Laukā **Vienība** pēc vajadzības atlasiet atbilstošo atribūta vienību.</span><span class="sxs-lookup"><span data-stu-id="b4f66-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="b4f66-123">Laukā **Datu veids** atlasiet vienības datu veidu.</span><span class="sxs-lookup"><span data-stu-id="b4f66-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="b4f66-124">Ja kā datu veidu atlasījāt **Virkne**, veiciet tālāk norādītās darbības, lai izveidotu atribūta veida vērtības.</span><span class="sxs-lookup"><span data-stu-id="b4f66-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="b4f66-125">Atlasiet atribūta veidu un pēc tam atlasiet **Vērtības**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="b4f66-126">Laukā **Atribūta vērtības** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="b4f66-127">Laukā **Atribūta veids** atlasiet atribūta veidu (dimensiju).</span><span class="sxs-lookup"><span data-stu-id="b4f66-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="b4f66-128">Laukā **Vērtība** ievadiet saistīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="b4f66-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="b4f66-129">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="b4f66-130">Saglabājiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b4f66-130">Save the record.</span></span>
    7. <span data-ttu-id="b4f66-131">Atgriezieties lapā **Atribūtu veidi**.</span><span class="sxs-lookup"><span data-stu-id="b4f66-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="b4f66-132">Saglabājiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b4f66-132">Save the record.</span></span>

    <span data-ttu-id="b4f66-133">Laukā **Funkcionālie novietojumi** ir norādīts to funkcionālo novietojumu skaits, kuri izmanto atribūta veidu.</span><span class="sxs-lookup"><span data-stu-id="b4f66-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="b4f66-134">Laukā **Līdzekļu veidi** ir parādīts to līdzekļu veidu skaits, kuri to izmanto.</span><span class="sxs-lookup"><span data-stu-id="b4f66-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
