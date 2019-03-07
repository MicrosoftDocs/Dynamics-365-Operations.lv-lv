---
title: Rīcībā esošo krājumu izmaksu vērtību koriģēšana
description: Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "335167"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="83c18-103">Rīcībā esošo krājumu izmaksu vērtību koriģēšana</span><span class="sxs-lookup"><span data-stu-id="83c18-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83c18-104">Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību.</span><span class="sxs-lookup"><span data-stu-id="83c18-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="83c18-105">Lapu **Rīcībā esošo krājumu koriģēšana** var izmantot, lai koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību pēc krājumu slēgšanas procesa palaišanas.</span><span class="sxs-lookup"><span data-stu-id="83c18-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="83c18-106">**Piezīme.** Lai atvērtu lapu **Rīcībā esošo krājumu koriģēšana**, lapā **Slēgšana un koriģēšana** atlasiet pabeigta krājuma slēgšanas procesa ierakstu un pēc tam noklikšķiniet uz **Korekcija** &gt; **Rīcībā esošs**.</span><span class="sxs-lookup"><span data-stu-id="83c18-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="83c18-107">**Piemērs.** Februārī jums ir šādas transakcijas:</span><span class="sxs-lookup"><span data-stu-id="83c18-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="83c18-108">1. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 2 un izmaksām ar summu 10,00 USD;</span><span class="sxs-lookup"><span data-stu-id="83c18-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="83c18-109">5. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 1 un izmaksām ar summu 13,00 USD;</span><span class="sxs-lookup"><span data-stu-id="83c18-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="83c18-110">19. februāris: krājumu finanšu izejas plūsma daudzumam ar vērtību 1 un kārtējām vidējām izmaksām ar summu 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="83c18-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="83c18-111">Šim krājumam bija iestatīts krājumu modelis “pirmais iekšā, pirmais ārā” (first in, first out – FIFO), un krājuma slēgšana notika 28. februārī.</span><span class="sxs-lookup"><span data-stu-id="83c18-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="83c18-112">Finanšu izejas plūsmas transakcija 11,00 USD apjomā tiks nokārtota pret 1. februāra krājumu ieejas plūsmu, un tiks veikta korekcija 1,00 USD apjomā.</span><span class="sxs-lookup"><span data-stu-id="83c18-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="83c18-113">Atvērto krājumu daudzumi būs redzami šādās krājumu ieejas plūsmās:</span><span class="sxs-lookup"><span data-stu-id="83c18-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="83c18-114">1. februāris: daudzums ar vērtību 1 un izmaksas ar summu 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="83c18-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="83c18-115">5. februāris: daudzums ar vērtību 1 un izmaksas ar summu 13,00 USD.</span><span class="sxs-lookup"><span data-stu-id="83c18-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="83c18-116">Lai šiem diviem krājumiem iestatītu izmaksas USD 15,00 apjomā, izmantojiet rīcībā esošās korekcijas opciju, lai koriģētu atvērtos rīcībā esošos daudzumus no pēdējā krājumu aizvēršanas perioda.</span><span class="sxs-lookup"><span data-stu-id="83c18-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="83c18-117">**Piezīme.** Rīcībā esošās korekcijas transakcijas grāmatošanas datums būs pēdējās krājumu slēgšanas datums.</span><span class="sxs-lookup"><span data-stu-id="83c18-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="83c18-118">Šo datumu nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="83c18-118">This date can't be modified.</span></span>
