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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990771"
---
# <a name="create-cost-objects"></a><span data-ttu-id="14487-103">Izmaksu objektu izveide  </span><span class="sxs-lookup"><span data-stu-id="14487-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14487-104">Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="14487-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="14487-105">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="14487-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="14487-106">Izveidot jaunus izmaksu objektus</span><span class="sxs-lookup"><span data-stu-id="14487-106">Create new cost objects</span></span>
1. <span data-ttu-id="14487-107">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="14487-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="14487-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="14487-108">Click New.</span></span>
3. <span data-ttu-id="14487-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="14487-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="14487-110">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="14487-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="14487-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="14487-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="14487-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="14487-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="14487-113">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="14487-113">Configure the data connector</span></span>
1. <span data-ttu-id="14487-114">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="14487-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="14487-115">Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="14487-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="14487-116">Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="14487-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="14487-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="14487-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="14487-118">Importēt izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="14487-118">Import cost centers</span></span>
1. <span data-ttu-id="14487-119">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="14487-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="14487-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="14487-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="14487-121">Skatīt importēto izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="14487-121">View the imported cost centers</span></span>
1. <span data-ttu-id="14487-122">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="14487-122">Click View dimension members.</span></span>

