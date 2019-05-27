---
title: Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi
description: Šajā rakstā ir aprakstīts, kā izslēgt novirzes punktus no vēsturiskajiem datiem, kas tiek izmantoti, lai aprēķinātu pieprasījuma apjoma prognozi. Izslēdzot novirzes punktus, jūs varat uzlabot prognozes precizitāti.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce8ebaf32b30c57b307f0d8799660ba6b42365a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543518"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="67382-104">Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi</span><span class="sxs-lookup"><span data-stu-id="67382-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67382-105">Šajā rakstā ir aprakstīts, kā izslēgt novirzes punktus no vēsturiskajiem datiem, kas tiek izmantoti, lai aprēķinātu pieprasījuma apjoma prognozi.</span><span class="sxs-lookup"><span data-stu-id="67382-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="67382-106">Izslēdzot novirzes punktus, jūs varat uzlabot prognozes precizitāti.</span><span class="sxs-lookup"><span data-stu-id="67382-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="67382-107">Varat izslēgt novirzes punktus, lai uzlabotu prognozes precizitāti.</span><span class="sxs-lookup"><span data-stu-id="67382-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="67382-108">Šis uzdevums nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="67382-108">This is an optional task.</span></span> <span data-ttu-id="67382-109">Tālāk ir sniegts šī procesa apskats.</span><span class="sxs-lookup"><span data-stu-id="67382-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="67382-110">Noklikšķiniet uz **Vispārējā plānošana** &gt; **Iestatījumi** &gt; **Pieprasījuma prognozēšana** &gt; **Nepiederošas personas noņemšana**, lai atvērtu lapu **Nepiederošas personas noņemšana**, kurā varat izmantot vaicājumu, lai atlasītu izslēdzamās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="67382-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="67382-111">Atlasiet uzņēmumu, uz kuru attiecas šis vaicājums, un pēc tam ievadiet nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="67382-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="67382-112">Lauks **Vaicājuma datums** automātiski tiek iestatīts uz pašreizējo datumu.</span><span class="sxs-lookup"><span data-stu-id="67382-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="67382-113">Atzīmējiet izvēles rūtiņu **Aktīvs**, lai no vēsturiskajiem datiem izslēgtu transakcijas, ko šis vaicājums atrod.</span><span class="sxs-lookup"><span data-stu-id="67382-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="67382-114">Šis iestatījums stāsies spēkā pēc bāzlīnijas prognozes izveides.</span><span class="sxs-lookup"><span data-stu-id="67382-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="67382-115">Lapā **Novirzes punktu noņemšanas vaicājums** varat pievienot, noņemt un atlasīt kritērijus, kas definē, kuras transakcijas tiks izslēgtas, kad tiek aprēķināta bāzlīnijas prognoze.</span><span class="sxs-lookup"><span data-stu-id="67382-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="67382-116">Piemēram, atlasiet noteiktu krājumu vai pasūtījuma transakciju, ko izslēgt.</span><span class="sxs-lookup"><span data-stu-id="67382-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="67382-117">Noklikšķiniet uz **Rādīt transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="67382-117">Click **Display transactions**.</span></span> <span data-ttu-id="67382-118">Lapā **Novirzes punktu transakcijas** ir uzskaitītas transakcijas, kas atbilst kritērijiem, kurus definējāt vaicājumā, un kas tiks izslēgtas no vēsturiskajiem datiem, kad tiek aprēķināta pieprasījuma apjoma prognoze.</span><span class="sxs-lookup"><span data-stu-id="67382-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="67382-119">**Piezīme.** Varat arī izveidot vaicājumu, kas ir balstīts uz esošu vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="67382-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="67382-120">Atlasiet vaicājumu, ko vēlaties kopēt, un pēc tam noklikšķiniet uz **Dublēt**.</span><span class="sxs-lookup"><span data-stu-id="67382-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="67382-121">Laukā **Vaicājuma datums** tiek identificēta versija.</span><span class="sxs-lookup"><span data-stu-id="67382-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="67382-122">Šo vaicājumu var lietot tādu, kāds tas ir, vai varat noklikšķināt uz **Rediģēt vaicājumu**, lai modificētu kritērijus.</span><span class="sxs-lookup"><span data-stu-id="67382-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="67382-123">Pēc izvēles varat modificēt jaunā vaicājuma nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="67382-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="67382-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="67382-124">Additional resources</span></span>
--------

[<span data-ttu-id="67382-125">Ievads par pieprasījuma prognozēšanu</span><span class="sxs-lookup"><span data-stu-id="67382-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="67382-126">Prognozes precizitātes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="67382-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)



