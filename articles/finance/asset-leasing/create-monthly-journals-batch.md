---
title: Ikmēneša žurnāla ierakstu izveidošana partijā
description: Šajā tēmā paskaidrots, kā izveidot žurnāla ierakstus partijā, lai palīdzētu uzlabot efektivitāti, ierakstot ikmēneša nomas izdevumus.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f46f289c58c32c535dd20fb510cf2812625c49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971332"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="01880-103">Ikmēneša žurnāla ierakstu izveidošana partijā</span><span class="sxs-lookup"><span data-stu-id="01880-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01880-104">Šajā tēmā paskaidrots, kā izveidot žurnāla ierakstus partijā, lai palīdzētu uzlabot efektivitāti, ierakstot ikmēneša nomas izdevumus.</span><span class="sxs-lookup"><span data-stu-id="01880-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="01880-105">Partiju apstrādi var izmantot, lai izveidotu žurnāla ierakstus no vairākiem grafikiem.</span><span class="sxs-lookup"><span data-stu-id="01880-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="01880-106">Šajos žurnāla ierakstos var iekļaut nomas maksājumus, saistību amortizāciju, līdzekļa lietošanas tiesību (LLT) amortizāciju un izpildes izmaksas.</span><span class="sxs-lookup"><span data-stu-id="01880-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="01880-107">Varat arī izmantot partiju apstrādi, lai vienlaicīgi veiktu vairāku nomu sākotnējo atzīšanu, vai arī veidotu pārejas korekcijas vairākām nomām vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="01880-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="01880-108">Lai iestatītu partijas darbu vai apstrādātu vairāku nomu maksājumu rēķinus, nolietojumu vai procentus, dodieties uz **Līdzekļu noma \> Periodiski \> Partiju žurnāla izveide**.</span><span class="sxs-lookup"><span data-stu-id="01880-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="01880-109">Parādītajā dialoglodziņā varat atlasīt grafiku, no kura ir jāizveido žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="01880-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="01880-110">Var arī norādīt, vai partiju apstrāde ir jāizpilda noteiktiem elementiem, nomas grupām vai nomas grāmatām.</span><span class="sxs-lookup"><span data-stu-id="01880-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="01880-111">Turpmākie darījumi, piemēram, saistību amortizācijas grafiki, maksājumi, nolietojums un izdevumi, tiks grāmatoti tikai pēc tam, kad tiks grāmatota atbilstošās nomas sākotnējā atzīšana.</span><span class="sxs-lookup"><span data-stu-id="01880-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="01880-112">Žurnāla ieraksti tiek izveidoti, bet tie netiks grāmatoti, līdz atlasīsiet komandu **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="01880-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>
