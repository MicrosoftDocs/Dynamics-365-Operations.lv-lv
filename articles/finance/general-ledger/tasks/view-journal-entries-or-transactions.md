---
title: Žurnālu ierakstu vai transakciju skatīšana
description: Šajā procedūrā parādīts, kā izmantot Dokumentu darbību vaicājumu, lai meklētu žurnālu ierakstus vai darbības.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da5979067639834929d10c0a8c1e372b2235a7af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222075"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="4c9fe-103">Žurnālu ierakstu vai transakciju skatīšana</span><span class="sxs-lookup"><span data-stu-id="4c9fe-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c9fe-104">Šajā procedūrā parādīts, kā izmantot Dokumentu darbību vaicājumu, lai meklētu žurnālu ierakstus vai darbības.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="4c9fe-105">**Navigācijas rūtī dodieties uz > Moduļi > Virsgrāmata > Pieprasījumi un pārskati > Dokumentu darbības**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="4c9fe-106">Atlasiet lauku, kuram vēlaties definēt filtra kritērijus.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="4c9fe-107">Ievadiet jūsu filtra kritērijus atlasītajam laukam.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="4c9fe-108">Varat veikt filtrēšanu, izmantojot vienu vērtību vai diapazonu.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="4c9fe-109">Definējot diapazonu, pārliecinieties, ka tiek lietota pareiza sintakse.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="4c9fe-110">Vērtības jāatdala ar dubultu punktu (..).</span><span class="sxs-lookup"><span data-stu-id="4c9fe-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="4c9fe-111">Noklikšķiniet cilni **Savienojumi**, lai pievienotu papildu tabulas, kuras vēlaties filtrēt.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="4c9fe-112">Kokā atlasiet **Tabulas/Virsgrāmatas žurnāla ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="4c9fe-113">Noklikšķiniet **Pievienot savienojuma tabulu**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="4c9fe-114">Noklikšķiniet uz **Atcelt**, ja nevēlaties pievienot papildu tabulu.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="4c9fe-115">Noklikšķiniet uz cilnes **Diapazons**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="4c9fe-116">Lai palaistu vaicājumu, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="4c9fe-117">Darbību rūtī noklikšķiniet uz **Darbības izcelsme**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="4c9fe-118">Dažādas pogas par režģi var izmantot, lai izpētītu papildu informāciju par atlasīto dokumenta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="4c9fe-119">Dažas pogas var nebūt pieejamas, atkarībā no darījuma veida un darbības īpašībām.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="4c9fe-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-120">Close the page.</span></span>
12. <span data-ttu-id="4c9fe-121">Darbību rūtī noklikšķiniet uz **Oriģinālais dokuments**.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="4c9fe-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4c9fe-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]