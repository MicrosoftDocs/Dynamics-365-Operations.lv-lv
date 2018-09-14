--- 
title: 'Izmaksu objektu izveide  '
description: "Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot Dynamics 365 for Finance and Operations Enterprise edition izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="dc3d6-103">Izmaksu objektu izveide  </span><span class="sxs-lookup"><span data-stu-id="dc3d6-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc3d6-104">Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot Dynamics 365 for Finance and Operations Enterprise edition izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="dc3d6-105">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="dc3d6-106">Šī procedūra ir paredzēta līdzeklim Izmaksu uzskaite, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="dc3d6-107">Izveidot jaunus izmaksu objektus</span><span class="sxs-lookup"><span data-stu-id="dc3d6-107">Create new cost objects</span></span>
1. <span data-ttu-id="dc3d6-108">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="dc3d6-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-109">Click New.</span></span>
3. <span data-ttu-id="dc3d6-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dc3d6-111">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="dc3d6-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="dc3d6-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="dc3d6-114">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="dc3d6-114">Configure the data connector</span></span>
1. <span data-ttu-id="dc3d6-115">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="dc3d6-116">Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="dc3d6-117">Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="dc3d6-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="dc3d6-119">Importēt izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="dc3d6-119">Import cost centers</span></span>
1. <span data-ttu-id="dc3d6-120">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="dc3d6-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="dc3d6-122">Skatīt importēto izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="dc3d6-122">View the imported cost centers</span></span>
1. <span data-ttu-id="dc3d6-123">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-123">Click View dimension members.</span></span>


