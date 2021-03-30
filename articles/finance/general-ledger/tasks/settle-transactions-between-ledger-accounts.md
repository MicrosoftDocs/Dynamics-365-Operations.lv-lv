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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222099"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="d8d37-103">Darbību segšana starp Virsgrāmatas kontiem</span><span class="sxs-lookup"><span data-stu-id="d8d37-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8d37-104">Šajā procedūrā parādīts, kā nosegt transakcijas starp Virsgrāmatas kontiem un atcelt Virsgrāmatas nosegšanu.</span><span class="sxs-lookup"><span data-stu-id="d8d37-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="d8d37-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="d8d37-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="d8d37-106">Transakciju segšana starp Virsgrāmatas kontiem</span><span class="sxs-lookup"><span data-stu-id="d8d37-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="d8d37-107">Pārejiet uz sadaļu Virsgrāmata > Periodiskie uzdevumi > Virsgrāmatas darbību sasaistīšana.</span><span class="sxs-lookup"><span data-stu-id="d8d37-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="d8d37-108">Sarakstā atrodiet transakcijas, kuras vēlaties nosegt.</span><span class="sxs-lookup"><span data-stu-id="d8d37-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="d8d37-109">Summas bilancei jābūt vienādai ar nulli.</span><span class="sxs-lookup"><span data-stu-id="d8d37-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="d8d37-110">Noklikšķiniet uz Iekļaut.</span><span class="sxs-lookup"><span data-stu-id="d8d37-110">Click Include.</span></span>
4. <span data-ttu-id="d8d37-111">Noklikšķiniet uz Akceptēt.</span><span class="sxs-lookup"><span data-stu-id="d8d37-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="d8d37-112">Virsgrāmatas nosegšanas atcelšana</span><span class="sxs-lookup"><span data-stu-id="d8d37-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="d8d37-113">Pārejiet uz sadaļu Virsgrāmata > Uzziņas un atskaites > Apgrozījuma bilance.</span><span class="sxs-lookup"><span data-stu-id="d8d37-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="d8d37-114">Noklikšķiniet uz Parametri, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="d8d37-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="d8d37-115">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="d8d37-115">Click Update.</span></span>
4. <span data-ttu-id="d8d37-116">Sarakstā atrodiet kontu, kurā atrodas nosegta transakcija.</span><span class="sxs-lookup"><span data-stu-id="d8d37-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="d8d37-117">Noklikšķiniet uz Visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="d8d37-117">Click All transactions.</span></span>
6. <span data-ttu-id="d8d37-118">Izmantojiet filtru, lai viegli atrastu transakciju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="d8d37-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="d8d37-119">Noklikšķiniet uz Virsgrāmatas darbību sasaistīšana.</span><span class="sxs-lookup"><span data-stu-id="d8d37-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="d8d37-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d8d37-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]