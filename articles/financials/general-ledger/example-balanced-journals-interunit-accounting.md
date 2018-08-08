---
title: "Saskaņoti starpvienību uzskaites žurnāli"
description: "Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana."
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="330f5-103">Saskaņoti starpvienību uzskaites žurnāli</span><span class="sxs-lookup"><span data-stu-id="330f5-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="330f5-104">Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana.</span><span class="sxs-lookup"><span data-stu-id="330f5-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="330f5-105">Ja konta ieraksti nav saskaņoti finanšu dimensijas vērtību līmenī, tiek automātiski izveidoti papildu kona ieraksti, lai saskaņotu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="330f5-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="330f5-106">Šie konta ieraksti izmanto grāmatošanas tipus **Starpvienību uzskaite — debets** un **Starpvienību uzskaite — kredīts** lapā **Automātisko darījumu konti**, lai noteiktu galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="330f5-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="330f5-107">Piemēram, kā saskaņošanas finanšu dimensija tiek atlasīta dimensija Struktūrvienība, kas ir otrais virsgrāmatas konta segments, un tiks izveidoti tālāk norādītie uzskaites ieraksti.</span><span class="sxs-lookup"><span data-stu-id="330f5-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="330f5-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="330f5-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="330f5-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="330f5-109">100.00 DR</span></span> |
| <span data-ttu-id="330f5-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="330f5-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="330f5-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="330f5-111">100.00 DR</span></span> |
| <span data-ttu-id="330f5-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="330f5-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="330f5-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="330f5-113">200.00 CR</span></span> |

<span data-ttu-id="330f5-114">Šādā gadījumā tiek noteiktas tālāk norādītās bilances.</span><span class="sxs-lookup"><span data-stu-id="330f5-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="330f5-115">Struktūrvienībai MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="330f5-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="330f5-116">Struktūrvienībai NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="330f5-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="330f5-117">Tāpēc tiek automātiski izveidoti tālāk norādītie uzskaites ieraksti, lai saskaņotu žurnālu finanšu dimensijas vērtību līmenī.</span><span class="sxs-lookup"><span data-stu-id="330f5-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="330f5-118">(Starpvienību debets) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="330f5-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="330f5-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="330f5-119">100.00 DR</span></span> |
| <span data-ttu-id="330f5-120">(Starpvienību kredīts) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="330f5-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="330f5-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="330f5-121">100.00 CR</span></span> |






