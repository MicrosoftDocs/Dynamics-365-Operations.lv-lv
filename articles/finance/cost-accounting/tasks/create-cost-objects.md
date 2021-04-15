---
title: Izmaksu objektu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810058"
---
# <a name="create-cost-objects"></a><span data-ttu-id="70d79-103">Izmaksu objektu izveide</span><span class="sxs-lookup"><span data-stu-id="70d79-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70d79-104">Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="70d79-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="70d79-105">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="70d79-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="70d79-106">Izveidot jaunus izmaksu objektus</span><span class="sxs-lookup"><span data-stu-id="70d79-106">Create new cost objects</span></span>
1. <span data-ttu-id="70d79-107">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="70d79-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="70d79-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="70d79-108">Click New.</span></span>
3. <span data-ttu-id="70d79-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="70d79-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="70d79-110">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="70d79-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="70d79-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="70d79-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="70d79-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="70d79-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="70d79-113">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="70d79-113">Configure the data connector</span></span>
1. <span data-ttu-id="70d79-114">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="70d79-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="70d79-115">Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="70d79-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="70d79-116">Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="70d79-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="70d79-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70d79-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="70d79-118">Importēt izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="70d79-118">Import cost centers</span></span>
1. <span data-ttu-id="70d79-119">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="70d79-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="70d79-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70d79-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="70d79-121">Skatīt importēto izmaksu centrus</span><span class="sxs-lookup"><span data-stu-id="70d79-121">View the imported cost centers</span></span>
1. <span data-ttu-id="70d79-122">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="70d79-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]