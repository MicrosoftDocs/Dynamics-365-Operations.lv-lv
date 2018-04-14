--- 
title: 'Izmaksu objektu izveide  '
description: "Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot programmas Dynamics 365 for Finance and Operations izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e469fc30d649aac0c544b6de9e17fd173f3ce497
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="df18d-103">Izmaksu objektu izveide  </span><span class="sxs-lookup"><span data-stu-id="df18d-103">Create cost objects</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df18d-104">Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot programmas Dynamics 365 for Finance and Operations izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="df18d-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="df18d-105">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="df18d-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="df18d-106">Šī procedūra ir paredzēta līdzeklim Izmaksu uzskaite, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="df18d-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="df18d-107">Izveidot jaunus izmaksu objektus</span><span class="sxs-lookup"><span data-stu-id="df18d-107">Create new cost objects</span></span>
1. <span data-ttu-id="df18d-108">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="df18d-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="df18d-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="df18d-109">Click New.</span></span>
3. <span data-ttu-id="df18d-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="df18d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="df18d-111">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="df18d-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="df18d-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="df18d-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="df18d-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="df18d-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="df18d-114">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="df18d-114">Configure the data connector</span></span>
1. <span data-ttu-id="df18d-115">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="df18d-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="df18d-116">Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="df18d-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="df18d-117">Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="df18d-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="df18d-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="df18d-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="df18d-119">Importēt izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="df18d-119">Import cost centers</span></span>
1. <span data-ttu-id="df18d-120">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="df18d-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="df18d-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="df18d-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="df18d-122">Skatīt importēto izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="df18d-122">View the imported cost centers</span></span>
1. <span data-ttu-id="df18d-123">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="df18d-123">Click View dimension members.</span></span>


