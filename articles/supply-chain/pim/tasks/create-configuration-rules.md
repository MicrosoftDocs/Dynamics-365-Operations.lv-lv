---
title: Konfigurācijas kārtulu izveide
description: Ar šo procedūru tiek izveidoti konfigurācijas noteikumi, kurus var izmantot konfigurācijai atbilstoši dimensijām, lai ieviestu vai novērstu noteiktas MK rindu kombinācijas.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c53ea2eea7dfe3c02d1b21964decc6630d3a41cf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208275"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="b0dd0-103">Konfigurācijas kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="b0dd0-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0dd0-104">Ar šo procedūru tiek izveidoti konfigurācijas noteikumi, kurus var izmantot konfigurācijai atbilstoši dimensijām, lai ieviestu vai novērstu noteiktas MK rindu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="b0dd0-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b0dd0-106">Šī ir septītā procedūra no astoņām, kurā ir skaidrots, kā veidot kombinācijas konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="b0dd0-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Materiālu komplekti un formulas > Materiālu komplekti.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="b0dd0-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b0dd0-109">Atrodiet un atlasiet MK konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="b0dd0-110">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="b0dd0-111">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-111">Click Change view.</span></span>
5. <span data-ttu-id="b0dd0-112">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-112">Click Header view.</span></span>
    * <span data-ttu-id="b0dd0-113">Atveriet virsraksta skatu, lai piekļūtu kopsavilkuma cilnei Konfigurācijas maršruts.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="b0dd0-114">Izvērsiet vai sakļaujiet sadaļu Konfigurācijas maršruts.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="b0dd0-115">Kopsavilkuma cilnei Konfigurācijas maršruts jābūt izvērstā režīmā.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="b0dd0-116">Noklikšķiniet uz Konfigurācijas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="b0dd0-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-117">Click New.</span></span>
9. <span data-ttu-id="b0dd0-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="b0dd0-119">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b0dd0-120">Tiek rādīti krājumi pašreizējā konfigurācijas grupā.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="b0dd0-121">Atlasiet to, kas atspoguļo nosacījumu kārtulā.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="b0dd0-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b0dd0-123">Atlasiet opciju laukā Metode.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="b0dd0-124">Ir iespējams piemērot krājuma atlasi vai atcelt krājuma atlasi no citas konfigurācijas grupas.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="b0dd0-125">Laukā Atvasinātā grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b0dd0-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b0dd0-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0dd0-128">Atlasiet vēlamo konfigurācijas grupu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="b0dd0-129">Laukā Atvasinātā krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b0dd0-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0dd0-131">Atlasiet krājuma kodu, kas tiks atlasīts vai kura atlase tika noņemta atkarībā no izvēlētās metodes.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="b0dd0-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b0dd0-132">Close the page.</span></span>

