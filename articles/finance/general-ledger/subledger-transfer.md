---
title: Pārsūtīt apakšgrāmatu uz Virsgrāmatu
description: Šajā tēmā ir aprakstītas Microsoft Dynamics 365 Finance iespējas, kas saistītas ar apakšgrāmatas pārvirzīšanu virsgrāmatā.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897508"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="756ca-103">Pārsūtīt apakšgrāmatu uz Virsgrāmatu</span><span class="sxs-lookup"><span data-stu-id="756ca-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="756ca-104">Šajā tēmā ir aprakstītas Microsoft Dynamics 365 Finance iespējas, kas attiecas uz apakšgrāmatas žurnāla ierakstu partiju pārsūtīšanas kārtulām.</span><span class="sxs-lookup"><span data-stu-id="756ca-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="756ca-105">Versijā 8.1 tika veiktas izmaiņas, lai varētu pārsūtīt kārtulas, kas novecināja **sinhrono** opciju.</span><span class="sxs-lookup"><span data-stu-id="756ca-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="756ca-106">Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi programmai Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="756ca-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="756ca-107">Apakšgrāmatas partiju pārsūtīšanai ir pieejamas šādas opcijas.</span><span class="sxs-lookup"><span data-stu-id="756ca-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="756ca-108">Asinhrons — šī opcija nekavējoties plāno apakšgrāmatas uzskaites ierakstu pārsūtīšanu uz Virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="756ca-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="756ca-109">Virsgrāmatas dokuments tiks ierakstīts, tiklīdz būs brīvi resursi, lai apstrādātu šo pieprasījumu serverī.</span><span class="sxs-lookup"><span data-stu-id="756ca-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="756ca-110">Plānotā partija — šī opcija pievienos apakšgrāmatas uzskaites ierakstus, kas tiek pārsūtīti uz apstrādes rindu virsgrāmatā, kur ieraksti tiek apstrādāti pasūtījuma saņemšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="756ca-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="756ca-111">Virsgrāmatas dokuments tiks ierakstīts plānotajā laikā, ja būs brīvi resursi, lai apstrādātu šo pakešuzdevumu serverī.</span><span class="sxs-lookup"><span data-stu-id="756ca-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="756ca-112">Versijā 10.0.8 tika veikti uzlabojumi, lai uzlabotu asinhronās opcijas veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="756ca-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="756ca-113">Šis līdzeklis ir iespējots zem līdzekļa nosaukuma **Apakšgrāmatas pārsūtīšana uz Virsgrāmatas veiktspējas optimizāciju**.</span><span class="sxs-lookup"><span data-stu-id="756ca-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="756ca-114">Šī funkcionalitāte uzlabo datu pārsūtīšanu no apakšgrāmatas uz virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="756ca-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="756ca-115">Tas ļauj procesam būt efektīvākam, un tas grupē kopā mazāku darbību kopas, ko pārsūtīt.</span><span class="sxs-lookup"><span data-stu-id="756ca-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="756ca-116">Tas ļauj efektīvāk izmantot pakešu serveri.</span><span class="sxs-lookup"><span data-stu-id="756ca-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="756ca-117">Šai funkcionalitātei nepieciešams, ka pakešu serveris ir iestatīts, tiešsaistē un funkcionējošs, lai asinhronās pārsūtīšanas opcija darbotos.</span><span class="sxs-lookup"><span data-stu-id="756ca-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]