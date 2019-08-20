---
title: 'Izmaksu objektu izveide  '
description: Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot Dynamics 365 for Finance and Operations Enterprise edition izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.
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
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841253"
---
# <a name="create-cost-objects"></a><span data-ttu-id="e9af9-103">Izmaksu objektu izveide  </span><span class="sxs-lookup"><span data-stu-id="e9af9-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9af9-104">Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot Dynamics 365 for Finance and Operations Enterprise edition izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="e9af9-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="e9af9-105">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="e9af9-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="e9af9-106">Šī procedūra ir paredzēta kā izmaksu uzskaites līdzeklis, kas tika pievienots Dynamics 365 for Operations versijai 1611.</span><span class="sxs-lookup"><span data-stu-id="e9af9-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="e9af9-107">Izveidot jaunus izmaksu objektus</span><span class="sxs-lookup"><span data-stu-id="e9af9-107">Create new cost objects</span></span>
1. <span data-ttu-id="e9af9-108">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e9af9-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="e9af9-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9af9-109">Click New.</span></span>
3. <span data-ttu-id="e9af9-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9af9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e9af9-111">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="e9af9-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="e9af9-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9af9-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e9af9-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e9af9-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="e9af9-114">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="e9af9-114">Configure the data connector</span></span>
1. <span data-ttu-id="e9af9-115">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="e9af9-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="e9af9-116">Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="e9af9-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="e9af9-117">Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="e9af9-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="e9af9-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e9af9-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="e9af9-119">Importēt izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="e9af9-119">Import cost centers</span></span>
1. <span data-ttu-id="e9af9-120">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="e9af9-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="e9af9-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e9af9-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="e9af9-122">Skatīt importēto izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="e9af9-122">View the imported cost centers</span></span>
1. <span data-ttu-id="e9af9-123">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="e9af9-123">Click View dimension members.</span></span>

