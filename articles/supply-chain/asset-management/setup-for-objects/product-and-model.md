---
title: Līdzekļa ražotāji un modeļi
description: Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu ražotājus un saistītos modeļus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1eca3112b95bc7d1a049f101fc1d461272a63aa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022260"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="f008c-103">Līdzekļa ražotāji un modeļi</span><span class="sxs-lookup"><span data-stu-id="f008c-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f008c-104">Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu ražotājus un saistītos modeļus Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="f008c-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="f008c-105">Modeļi var būt saistīti ar līdzekļu veidiem.</span><span class="sxs-lookup"><span data-stu-id="f008c-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="f008c-106">Preču–modeļa attiecību iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f008c-106">Set up product-model relations</span></span>

1. <span data-ttu-id="f008c-107">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Ražotājs un modelis**.</span><span class="sxs-lookup"><span data-stu-id="f008c-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="f008c-108">Atlasiet **Jauns**, lai izveidotu jaunu preci.</span><span class="sxs-lookup"><span data-stu-id="f008c-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="f008c-109">Laukā **Ražotājs** ievadiet līdzekļa ražotāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f008c-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="f008c-110">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="f008c-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f008c-111">Kopsavilkuma cilnē **Modeļi** atlasiet **Pievienot**, lai izveidotu līdzekļu modeli, kam jābūt saistītam ar līdzekļa ražotāju.</span><span class="sxs-lookup"><span data-stu-id="f008c-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="f008c-112">Laukā **Modelis** ievadiet līdzekļa modeļa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f008c-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="f008c-113">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="f008c-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="f008c-114">Laukā **Līdzekļa veids** atlasiet līdzekļa veidutipu, ar kuru jābūt saistītam ražotāja modelim.</span><span class="sxs-lookup"><span data-stu-id="f008c-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f008c-115">Varat arī iestatīt attiecības līdzekļu veidiem, ražotājiem un modeļiem uzmeklēšā **Līdzekļu veidi**.</span><span class="sxs-lookup"><span data-stu-id="f008c-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="f008c-116">Papildinformāciju skatiet nodaļā [Līdzekļa veidi](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="f008c-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="f008c-117">Kopsavilkuma cilnē **Detalizēta informācija** lauks **Modeļi** rāda to līdzekļu modeļu skaitu, kas iestatīti atlasītajam līdzekļu ražotājam.</span><span class="sxs-lookup"><span data-stu-id="f008c-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="f008c-118">Laukā **Līdzekļi** ir parādīts to līdzekļu skaits, kas izmanto atlasīto ražotāju.</span><span class="sxs-lookup"><span data-stu-id="f008c-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="f008c-119">Laukā **Līdzekļi** ir parādīts to objektu skaits, kas izmanto atlasīto ražotāja modeli.</span><span class="sxs-lookup"><span data-stu-id="f008c-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="f008c-120">Līdzekļa veidam var nebūt līdzekļa ražotāja modeļa attiecības, bet tas var būt saistīts ar vienu līdzekļa ražotāja modeli vai tas var būt saistīts ar vairākiem līdzekļu ražotāju modeļiem.</span><span class="sxs-lookup"><span data-stu-id="f008c-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="f008c-121">Ja līdzekļa veids ir saistīts vismaz ar vienu ražotāja modeli, tad tajās līdzekļu pārvaldības lapās, kurās var izveidot līdzekļu veida, ražotāja un modeļa kombinācijas, var atlasīt tikai tās kombinācijas, kas ir iestatītas uzmeklēšanā **Ražotāja modelis**.</span><span class="sxs-lookup"><span data-stu-id="f008c-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="f008c-122">Šīs lapas ietver **Visi līdzekļi**, **Līdzekļu pakalpojumu līmeņi**, **Darba veidu noklusējumi** un **Uzturēšanas budžeta rindas**.</span><span class="sxs-lookup"><span data-stu-id="f008c-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="f008c-123">Ja daži līdzekļu veidi nav saistīti ne ar vienu ražotāja modeli, lapās tiek rādīti tikai tie līdzekļu veidi un ražotāju modeļi, kuriem nav attiecību ar līdzekļu veidiem.</span><span class="sxs-lookup"><span data-stu-id="f008c-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="f008c-124">Ražotāja un modeļa atlasīšana objektā</span><span class="sxs-lookup"><span data-stu-id="f008c-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="f008c-125">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="f008c-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="f008c-126">Kolonnā **Līdzeklis** atlasiet saiti līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="f008c-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="f008c-127">Tiek atvērta lapa **Detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="f008c-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="f008c-128">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f008c-128">Select **Edit**.</span></span>
4. <span data-ttu-id="f008c-129">Kopsavilkuma cilnē **Vispārīgi** atlasiet vērtības laukos **Ražotājs** un **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="f008c-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
