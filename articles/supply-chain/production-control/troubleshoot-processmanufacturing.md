---
title: Problēmu novēršana saistībā ar ražošanas procesu
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar ražošanas procesu.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 938820b6cd2bb470b440fea7b70124efc0faf7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824994"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="bf5eb-103">Problēmu novēršana saistībā ar ražošanas procesu</span><span class="sxs-lookup"><span data-stu-id="bf5eb-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="bf5eb-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar ražošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="bf5eb-105">Kad es izmantoju darba kartes ierīci, lai pārskatā sniegtu daļēju daudzumu, kas ir pēdējais darbs ražošanas pasūtījumā, visi iepriekšēji darbi, kuru statuss ir nepabeigts, tiek automātiski pabeigti.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="bf5eb-106">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-106">This behavior is by design.</span></span> <span data-ttu-id="bf5eb-107">Lapā **Ražošanas pasūtījuma noklusējumi** cilnē **Ziņot kā pabeigtus** ir opcija, kas tiek saukta par **Beigu zīmes maršrutu**.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="bf5eb-108">Ja šī tēma ir iestatīta uz *Jā*, maršruta kartes žurnāls tiek grāmatots, kad darbinieks izmanto darba kartes ierīci vai darba kartes termināli, lai ziņotu par pēdējo operāciju.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="bf5eb-109">Šis žurnāls atzīmē visas operācijas kā pabeigtas un beidz visus ražošanas darbus.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="bf5eb-110">Ja **Beigu zīmes maršruta** opcija ir iestatīta uz *Jā*, sistēma neņem vērā darbinieka izvēlēto darba statusu brīdī, kad viņš ziņoja par pēdējo operāciju.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="bf5eb-111">Sistēma arī neņem vērā, vai darbinieks ziņo par pilnīgu vai daļēju daudzumu.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="bf5eb-112">Kad es mēģinu veikt krājumu slēgšanu, tiek saņemts šāds brīdinājuma ziņojums: "nav reģistrēta atgriezeniskas izmaksu aprēķināšanas izpilde ar datumu %1, kas atbilst perioda beigām."</span><span class="sxs-lookup"><span data-stu-id="bf5eb-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="bf5eb-113">Laidienos pirms 10.0.13 izlaiduma, ja neizmantojat taupīgo ražošanas izmaksu plūsmu, krājuma slēgšanas laikā saņemat šādu kļūdainu brīdinājuma ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="bf5eb-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="bf5eb-114">Jūs gatavojaties izpildīt Krājumu slēgšanu ar datumu %1.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="bf5eb-115">Nav reģistrēta neviena Atgriezeniska izmaksu aprēķināšana ar datumu %1 salīdzināšanas perioda beigas.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="bf5eb-116">Lūdzu atceraties veikt Atgriezenisko izmaksu aprēķināšanu ar datumu %1 salīdzināšanas perioda beigas.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="bf5eb-117">Krājumu novērtējums, pārdoto preču izmaksas un novirzes Apakšgrāmatās vai Virsgrāmatā var nebūt pareizas, kamēr tās nav izpildītas.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="bf5eb-118">Šī problēma ir novērsta, 10.0.13 laidienā un jaunākos.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="bf5eb-119">Papildinformāciju skatiet [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="bf5eb-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]