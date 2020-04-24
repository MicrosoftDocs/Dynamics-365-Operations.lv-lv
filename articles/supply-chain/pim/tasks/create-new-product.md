---
title: Jaunas preces izveide
description: Šajā tēmā ir aprakstīts, kā izveidot jaunu koplietojamu preci.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bf15359e085b541407bb49c266f7d9505893e25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203714"
---
# <a name="create-a-new-product"></a><span data-ttu-id="788ab-103">Jaunas preces izveide</span><span class="sxs-lookup"><span data-stu-id="788ab-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="788ab-104">Šajā tēmā ir aprakstīts, kā izveidot jaunu koplietojamu preci.</span><span class="sxs-lookup"><span data-stu-id="788ab-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="788ab-105">To parasti veic preču noformētājs.</span><span class="sxs-lookup"><span data-stu-id="788ab-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="788ab-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="788ab-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="788ab-107">Preces izveide</span><span class="sxs-lookup"><span data-stu-id="788ab-107">Create a product</span></span>
1. <span data-ttu-id="788ab-108">Navigācijas rūtī dodieties uz **Moduļi > Preču informācijas pārvaldība > Preces > Preces**.</span><span class="sxs-lookup"><span data-stu-id="788ab-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="788ab-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="788ab-109">Select **New**.</span></span>
3. <span data-ttu-id="788ab-110">Laukā **Preces numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="788ab-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="788ab-111">Ja nav iestatīta numuru sērija preces numuram, tas ir jāievada manuāli.</span><span class="sxs-lookup"><span data-stu-id="788ab-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="788ab-112">Laukā **Preces nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="788ab-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="788ab-113">Preces nosaukuma noklusējuma vērtība ir meklēšanas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="788ab-113">The product name defaults to the search name.</span></span> <span data-ttu-id="788ab-114">Ja nepieciešams, varat to izmainīt.</span><span class="sxs-lookup"><span data-stu-id="788ab-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="788ab-115">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="788ab-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="788ab-116">Iestatīt dimensiju grupas</span><span class="sxs-lookup"><span data-stu-id="788ab-116">Set up dimension groups</span></span>
1. <span data-ttu-id="788ab-117">Atlasiet **Dimensiju grupas**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="788ab-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="788ab-118">Laukā **Noliktavas dimensiju grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="788ab-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="788ab-119">Noliktavas dimensijas grupa nosaka, kuras noliktavas dimensijas ir jāievada katrai transakcijai attiecīgajai precei un kā tā tiks izsekota krājumos.</span><span class="sxs-lookup"><span data-stu-id="788ab-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="788ab-120">Laukā **Izsekošanas dimensiju grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="788ab-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="788ab-121">Izsekošanas dimensijas grupa nosaka, kuras izsekošanas dimensijas ir jāievada katrai transakcijai attiecīgajai precei un kā tā tiks apstrādāta krājumos.</span><span class="sxs-lookup"><span data-stu-id="788ab-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="788ab-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="788ab-122">Select **OK**.</span></span>

