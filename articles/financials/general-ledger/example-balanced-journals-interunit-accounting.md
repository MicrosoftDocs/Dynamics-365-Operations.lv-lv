---
title: "Saskaņoti starpvienību uzskaites žurnāli"
description: "Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="ec8a6-103">Saskaņoti starpvienību uzskaites žurnāli</span><span class="sxs-lookup"><span data-stu-id="ec8a6-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ec8a6-104">Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana.</span><span class="sxs-lookup"><span data-stu-id="ec8a6-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="ec8a6-105">Ja konta ieraksti nav saskaņoti finanšu dimensijas vērtību līmenī, tiek automātiski izveidoti papildu kona ieraksti, lai saskaņotu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="ec8a6-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="ec8a6-106">Šie konta ieraksti izmanto grāmatošanas tipus **Starpvienību uzskaite — debets** un **Starpvienību uzskaite — kredīts** lapā **Automātisko darījumu konti**, lai noteiktu galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="ec8a6-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="ec8a6-107">Piemēram, kā saskaņošanas finanšu dimensija tiek atlasīta dimensija Filiāle, kas ir otrais virsgrāmatas konta segments, un tiks izveidoti tālāk norādītie uzskaites ieraksti.</span><span class="sxs-lookup"><span data-stu-id="ec8a6-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="ec8a6-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="ec8a6-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="ec8a6-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-109">100.00 DR</span></span> |
| <span data-ttu-id="ec8a6-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="ec8a6-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="ec8a6-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-111">100.00 DR</span></span> |
| <span data-ttu-id="ec8a6-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="ec8a6-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="ec8a6-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-113">200.00 CR</span></span> |

<span data-ttu-id="ec8a6-114">Šādā gadījumā tiek noteiktas tālāk norādītās bilances.</span><span class="sxs-lookup"><span data-stu-id="ec8a6-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="ec8a6-115">Filiālei MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="ec8a6-116">Filiālei NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="ec8a6-117">Tāpēc tiek automātiski izveidoti tālāk norādītie uzskaites ieraksti, lai saskaņotu žurnālu finanšu dimensijas vērtību līmenī.</span><span class="sxs-lookup"><span data-stu-id="ec8a6-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="ec8a6-118">(Starpvienību debets) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="ec8a6-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="ec8a6-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-119">100.00 DR</span></span> |
| <span data-ttu-id="ec8a6-120">(Starpvienību kredīts) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="ec8a6-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="ec8a6-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="ec8a6-121">100.00 CR</span></span> |






