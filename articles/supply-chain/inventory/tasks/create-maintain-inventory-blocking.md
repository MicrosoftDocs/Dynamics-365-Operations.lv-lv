---
title: Krājuma bloķēšanas izveide un uzturēšana
description: Šajā tēmā aprakstīts, kā izmantot krājumu aizturēšanu, lai novērstu fiziski rīcībā esošo krājumu rezervēšanu citos izejošajos pirmdokumentos.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956162"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="0791e-103">Krājuma bloķēšanas izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="0791e-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0791e-104">Šajā tēmā aprakstīts, kā izmantot krājumu aizturēšanu, lai novērstu fiziski rīcībā esošo krājumu rezervēšanu citos izejošajos pirmdokumentos.</span><span class="sxs-lookup"><span data-stu-id="0791e-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="0791e-105">Pirms sākat procedūras šajā tēmā, jābūt krājumam, kuram ir pieejami fiziski rīcībā esošie krājumi.</span><span class="sxs-lookup"><span data-stu-id="0791e-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="0791e-106">Bloķēt krājumus</span><span class="sxs-lookup"><span data-stu-id="0791e-106">Block inventory</span></span>

<span data-ttu-id="0791e-107">Lai izveidotu krājuma aizturēšanas ierakstu tā, ka krājumi tiek bloķēti, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="0791e-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="0791e-108">Dodieties uz **Krājumu vadība \> Periodiskie uzdevumi \> Krājumu aizturēšana**.</span><span class="sxs-lookup"><span data-stu-id="0791e-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="0791e-109">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0791e-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0791e-110">Jaunā aizturēšanas ieraksta virsrakstā iestatiet lauku **Krājuma numurs** precei, kuru vēlaties bloķēt, un ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="0791e-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="0791e-111">Kopsavilkuma cilnē **Vispārīgi** laukā **Daudzums** ievadiet bloķējamo vienumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="0791e-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="0791e-112">Kopsavilkuma cilnē **Krājumu dimensijas** norādiet vietu un noliktavu, kur krājumi, ko vēlaties bloķēt, pašlaik atrodas.</span><span class="sxs-lookup"><span data-stu-id="0791e-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="0791e-113">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0791e-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="0791e-114">Krājumu bloķēšanas nosacījumu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="0791e-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="0791e-115">Lai atjauninātu krājuma aizturēšanas ierakstu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="0791e-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="0791e-116">Dodieties uz **Krājumu vadība \> Periodiskie uzdevumi \> Krājumu aizturēšana**.</span><span class="sxs-lookup"><span data-stu-id="0791e-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="0791e-117">Saraksta rūtī atlasiet atbilstošo aizturēšanas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0791e-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="0791e-118">Pēc nepieciešamības rediģējiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0791e-118">Edit the record as required.</span></span> <span data-ttu-id="0791e-119">Piemēram, var mainīt lauka **Paredzamais datums** vērtību, lai norādītu, kad bloķētajiem krājumiem ir jābūt pieejamiem rezervācijai.</span><span class="sxs-lookup"><span data-stu-id="0791e-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="0791e-120">Ja ir atlasīta opcija **Plānotie ieņēmumi**, plānotajai transakcijai parādīsies datums.</span><span class="sxs-lookup"><span data-stu-id="0791e-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="0791e-121">(Opcija **Paredzamā saņemšana** tiek atlasīta pēc noklusējuma, manuāli veidojot aizturēšanas ierakstu.)</span><span class="sxs-lookup"><span data-stu-id="0791e-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="0791e-122">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0791e-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="0791e-123">Krājumu atbloķēšana</span><span class="sxs-lookup"><span data-stu-id="0791e-123">Unblock inventory</span></span>

<span data-ttu-id="0791e-124">Lai noņemtu krājuma aizturēšanas ierakstu tā, ka krājumi tiek atbloķēti, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="0791e-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="0791e-125">Dodieties uz **Krājumu vadība \> Periodiskie uzdevumi \> Krājumu aizturēšana**.</span><span class="sxs-lookup"><span data-stu-id="0791e-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="0791e-126">Saraksta rūtī atlasiet atbilstošo aizturēšanas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0791e-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="0791e-127">Darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="0791e-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="0791e-128">Tiek piedāvāts apstiprināt operāciju.</span><span class="sxs-lookup"><span data-stu-id="0791e-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="0791e-129">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0791e-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="0791e-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0791e-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
