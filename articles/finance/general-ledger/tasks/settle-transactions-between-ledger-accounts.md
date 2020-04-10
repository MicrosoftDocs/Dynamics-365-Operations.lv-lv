---
title: Darbību segšana starp Virsgrāmatas kontiem
description: Šajā procedūrā parādīts, kā nosegt transakcijas starp Virsgrāmatas kontiem un atcelt Virsgrāmatas nosegšanu.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144678"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="f602e-103">Darbību segšana starp Virsgrāmatas kontiem</span><span class="sxs-lookup"><span data-stu-id="f602e-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f602e-104">Šajā procedūrā parādīts, kā nosegt transakcijas starp Virsgrāmatas kontiem un atcelt Virsgrāmatas nosegšanu.</span><span class="sxs-lookup"><span data-stu-id="f602e-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="f602e-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="f602e-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="f602e-106">Transakciju segšana starp Virsgrāmatas kontiem</span><span class="sxs-lookup"><span data-stu-id="f602e-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="f602e-107">Pārejiet uz sadaļu Virsgrāmata > Periodiskie uzdevumi > Virsgrāmatas darbību sasaistīšana.</span><span class="sxs-lookup"><span data-stu-id="f602e-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="f602e-108">Sarakstā atrodiet transakcijas, kuras vēlaties nosegt.</span><span class="sxs-lookup"><span data-stu-id="f602e-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="f602e-109">Summas bilancei jābūt vienādai ar nulli.</span><span class="sxs-lookup"><span data-stu-id="f602e-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="f602e-110">Noklikšķiniet uz Iekļaut.</span><span class="sxs-lookup"><span data-stu-id="f602e-110">Click Include.</span></span>
4. <span data-ttu-id="f602e-111">Noklikšķiniet uz Akceptēt.</span><span class="sxs-lookup"><span data-stu-id="f602e-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="f602e-112">Virsgrāmatas nosegšanas atcelšana</span><span class="sxs-lookup"><span data-stu-id="f602e-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="f602e-113">Pārejiet uz sadaļu Virsgrāmata > Uzziņas un atskaites > Apgrozījuma bilance.</span><span class="sxs-lookup"><span data-stu-id="f602e-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="f602e-114">Noklikšķiniet uz Parametri, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="f602e-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="f602e-115">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="f602e-115">Click Update.</span></span>
4. <span data-ttu-id="f602e-116">Sarakstā atrodiet kontu, kurā atrodas nosegta transakcija.</span><span class="sxs-lookup"><span data-stu-id="f602e-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="f602e-117">Noklikšķiniet uz Visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="f602e-117">Click All transactions.</span></span>
6. <span data-ttu-id="f602e-118">Izmantojiet filtru, lai viegli atrastu transakciju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f602e-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="f602e-119">Noklikšķiniet uz Virsgrāmatas darbību sasaistīšana.</span><span class="sxs-lookup"><span data-stu-id="f602e-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="f602e-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f602e-120">In the list, mark the selected row.</span></span>

