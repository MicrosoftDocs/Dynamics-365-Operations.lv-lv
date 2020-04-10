---
title: 'Izmaksu objektu izveide  '
description: Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142321"
---
# <a name="create-cost-objects"></a><span data-ttu-id="2b631-103">Izmaksu objektu izveide  </span><span class="sxs-lookup"><span data-stu-id="2b631-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b631-104">Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="2b631-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="2b631-105">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="2b631-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="2b631-106">Izveidot jaunus izmaksu objektus</span><span class="sxs-lookup"><span data-stu-id="2b631-106">Create new cost objects</span></span>
1. <span data-ttu-id="2b631-107">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="2b631-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="2b631-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2b631-108">Click New.</span></span>
3. <span data-ttu-id="2b631-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2b631-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2b631-110">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="2b631-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="2b631-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2b631-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2b631-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2b631-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="2b631-113">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="2b631-113">Configure the data connector</span></span>
1. <span data-ttu-id="2b631-114">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="2b631-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="2b631-115">Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="2b631-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="2b631-116">Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="2b631-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="2b631-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2b631-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="2b631-118">Importēt izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="2b631-118">Import cost centers</span></span>
1. <span data-ttu-id="2b631-119">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="2b631-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="2b631-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2b631-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="2b631-121">Skatīt importēto izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="2b631-121">View the imported cost centers</span></span>
1. <span data-ttu-id="2b631-122">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="2b631-122">Click View dimension members.</span></span>

