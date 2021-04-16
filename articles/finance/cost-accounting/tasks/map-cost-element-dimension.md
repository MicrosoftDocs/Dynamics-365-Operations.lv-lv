---
title: Izmaksu elementa dimensijas kartēšana
description: Izmaksu kontrolieris var izmantot šo procedūru, lai kartētu izmaksu elementa dimensiju uz izmaksu elementu dimensiju MXMF juridiskajā personā.
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 845ab27a09905f42c905f9018f9f176a64f8785a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841049"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="1ecae-103">Izmaksu elementa dimensijas kartēšana</span><span class="sxs-lookup"><span data-stu-id="1ecae-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ecae-104">Izmaksu kontrolieris var izmantot šo procedūru, lai kartētu izmaksu elementa dimensiju uz izmaksu elementu dimensiju MXMF juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="1ecae-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="1ecae-105">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="1ecae-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="1ecae-106">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu elementa dimensijas.</span><span class="sxs-lookup"><span data-stu-id="1ecae-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="1ecae-107">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ecae-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1ecae-108">Šim piemēram atlasiet Izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="1ecae-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="1ecae-109">Noklikšķiniet uz Dimensiju kartējumi.</span><span class="sxs-lookup"><span data-stu-id="1ecae-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="1ecae-110">Noklikšķiniet uz Konfigurēt kartējumus no šīs dimensijas.</span><span class="sxs-lookup"><span data-stu-id="1ecae-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="1ecae-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1ecae-111">Click New.</span></span>
6. <span data-ttu-id="1ecae-112">Laukā Uz dimensiju ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ecae-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="1ecae-113">Šim piemēram atlasiet MXMF izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="1ecae-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="1ecae-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1ecae-114">Click New.</span></span>
8. <span data-ttu-id="1ecae-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1ecae-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="1ecae-116">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ecae-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ecae-117">Šim piemēram atlasiet dimensijas elementu 606400 Tālrunis & Faksa izdevumi.</span><span class="sxs-lookup"><span data-stu-id="1ecae-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="1ecae-118">Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ecae-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ecae-119">Šim piemēram atlasiet dimensijas elementu 6001004 Telefono.</span><span class="sxs-lookup"><span data-stu-id="1ecae-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="1ecae-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1ecae-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]