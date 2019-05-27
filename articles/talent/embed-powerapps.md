---
title: PowerApps pr. iegulš. Core HR
description: Šajā tēmā izskaidrots, kā atrisināt problēmu, kad PowerApps izvēlnes elements netiek rādīts sistēmas administrēšanas modulī.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e3b20e1d0a873c32b8f6f5e28f786febf62db355
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518604"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="582a0-103">PowerApps pr. iegulš. Core HR</span><span class="sxs-lookup"><span data-stu-id="582a0-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="582a0-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="582a0-104">**Issue**</span></span>

<span data-ttu-id="582a0-105">**PowerApps** izvēlnes elements netiek rādīts modulī **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="582a0-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="582a0-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="582a0-106">**Cause**</span></span>

<span data-ttu-id="582a0-107">Ir mainīts lietotāja interfeisa (UI) noformējums, un pakalpojums Microsoft PowerApps tagad ir ietverts standarta personalizācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="582a0-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="582a0-108">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="582a0-108">**Resolution**</span></span>

<span data-ttu-id="582a0-109">Ir mainīts veids, kā PowerApps programmas tiek iegultas.</span><span class="sxs-lookup"><span data-stu-id="582a0-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="582a0-110">PowerApps progr. tagad pievieno, lietojot personal. modeli.</span><span class="sxs-lookup"><span data-stu-id="582a0-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="582a0-111">Varat pievienot PowerApps programmas gandrīz visās Microsoft Dynamics 365 for Talent lapās.</span><span class="sxs-lookup"><span data-stu-id="582a0-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="582a0-112">Inf. par to, kā programmā Talent iegult PowerApps progr., sk. [PowerApps progr. ieg](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="582a0-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="582a0-113">Visiem PowerApps klientiem, kas veica progr. iegulš. pirms izm., ir jābūt jauninātiem uz jauno modeli.</span><span class="sxs-lookup"><span data-stu-id="582a0-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="582a0-114">Poga **PowerApps** ir gandrīz visu Talent lapu augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="582a0-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="582a0-115">Šo pogu var lietot, lai ievietotu PowerApps progr.</span><span class="sxs-lookup"><span data-stu-id="582a0-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="582a0-116">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="582a0-116">Here is an example.</span></span>

1. <span data-ttu-id="582a0-117">Dod. uz **Person. pārvald. \> Saites \> Nodarbin. \> Darbin**.</span><span class="sxs-lookup"><span data-stu-id="582a0-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="582a0-118">Atlasiet pogu **PowerApps** un tad atlasiet **Ievietot PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="582a0-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps poga](media/png.png)

3. <span data-ttu-id="582a0-120">Aizpildiet laukus dialoglodziņā **Ievietot PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="582a0-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogl. Ievietot PowerApp](media/insert-powerapp.png)

<span data-ttu-id="582a0-122">Vai arī veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="582a0-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="582a0-123">Lapas darbību rūts cilnes **Opcijas** grupā **Personalizēt** atlasiet **Personalizēt šo veidlapu**.</span><span class="sxs-lookup"><span data-stu-id="582a0-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Personalizēt grupu cilnē Opcijas](media/options.png)

    <span data-ttu-id="582a0-125">Tiek parādīta personaliz. rīkjosla.</span><span class="sxs-lookup"><span data-stu-id="582a0-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="582a0-126">Rīkjoslā atlasiet **Ievietot \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="582a0-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![PowerApps progr. ievietošana, lietojot personaliz. rīkjoslu](media/powerapp-bar.png)
