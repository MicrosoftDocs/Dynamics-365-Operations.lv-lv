---
title: Ikmēneša žurnāla ierakstu izveidošana partijā
description: Šajā tēmā paskaidrots, kā izveidot žurnāla ierakstus partijā, lai palīdzētu uzlabot efektivitāti, ierakstot ikmēneša nomas izdevumus.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881208"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="6990f-103">Ikmēneša žurnāla ierakstu izveidošana partijā</span><span class="sxs-lookup"><span data-stu-id="6990f-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6990f-104">Šajā tēmā paskaidrots, kā izveidot žurnāla ierakstus partijā, lai palīdzētu uzlabot efektivitāti, ierakstot ikmēneša nomas izdevumus.</span><span class="sxs-lookup"><span data-stu-id="6990f-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="6990f-105">Partiju apstrādi var izmantot, lai izveidotu žurnāla ierakstus no vairākiem grafikiem.</span><span class="sxs-lookup"><span data-stu-id="6990f-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="6990f-106">Šajos žurnāla ierakstos var iekļaut nomas maksājumus, saistību amortizāciju, līdzekļa lietošanas tiesību (LLT) amortizāciju un izpildes izmaksas.</span><span class="sxs-lookup"><span data-stu-id="6990f-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="6990f-107">Varat arī izmantot partiju apstrādi, lai vienlaicīgi veiktu vairāku nomu sākotnējo atzīšanu, vai arī veidotu pārejas korekcijas vairākām nomām vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="6990f-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="6990f-108">Lai iestatītu partijas darbu vai apstrādātu vairāku nomu maksājumu rēķinus, nolietojumu vai procentus, dodieties uz **Līdzekļu noma \> Periodiski \> Partiju žurnāla izveide**.</span><span class="sxs-lookup"><span data-stu-id="6990f-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="6990f-109">Parādītajā dialoglodziņā varat atlasīt grafiku, no kura ir jāizveido žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="6990f-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="6990f-110">Var arī norādīt, vai partiju apstrāde ir jāizpilda noteiktiem elementiem, nomas grupām vai nomas grāmatām.</span><span class="sxs-lookup"><span data-stu-id="6990f-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="6990f-111">Turpmākie darījumi, piemēram, saistību amortizācijas grafiki, maksājumi, nolietojums un izdevumi, tiks grāmatoti tikai pēc tam, kad tiks grāmatota atbilstošās nomas sākotnējā atzīšana.</span><span class="sxs-lookup"><span data-stu-id="6990f-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="6990f-112">Žurnāla ieraksti tiek izveidoti, bet tie netiks grāmatoti, līdz atlasīsiet komandu **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="6990f-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
