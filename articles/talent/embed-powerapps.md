---
title: PowerApps programmu iegulšana Dynamics 365 — Core HR
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
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551007"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="89771-103">PowerApps programmu iegulšana Dynamics 365 — Core HR</span><span class="sxs-lookup"><span data-stu-id="89771-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89771-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="89771-104">**Issue**</span></span>

<span data-ttu-id="89771-105">**PowerApps** izvēlnes elements netiek rādīts modulī **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="89771-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="89771-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="89771-106">**Cause**</span></span>

<span data-ttu-id="89771-107">Ir mainīts lietotāja interfeisa (UI) noformējums, un pakalpojums Microsoft PowerApps tagad ir ietverts standarta personalizācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="89771-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="89771-108">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="89771-108">**Resolution**</span></span>

<span data-ttu-id="89771-109">Ir mainīts veids, kā PowerApps programmas tiek iegultas.</span><span class="sxs-lookup"><span data-stu-id="89771-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="89771-110">PowerApps programmas tagad pievieno, lietojot personalizācijas modeli.</span><span class="sxs-lookup"><span data-stu-id="89771-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="89771-111">Varat pievienot PowerApps programmas gandrīz visās Microsoft Dynamics 365 Talent lapās.</span><span class="sxs-lookup"><span data-stu-id="89771-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="89771-112">Informāciju par to, kā programmā Talent iegult PowerApps programmas, skatiet [Iegult PowerApps programmas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="89771-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="89771-113">Visiem PowerApps klientiem, kas veica programmu iegulšanu pirms izmaiņām, ir jābūt jauninātiem uz jauno modeli.</span><span class="sxs-lookup"><span data-stu-id="89771-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="89771-114">Poga **PowerApps** ir gandrīz visu Talent lapu augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="89771-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="89771-115">Šo pogu var lietot, lai ievietotu PowerApps programmu.</span><span class="sxs-lookup"><span data-stu-id="89771-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="89771-116">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="89771-116">Here is an example.</span></span>

1. <span data-ttu-id="89771-117">Dod. uz **Person. pārvald. \> Saites \> Nodarbin. \> Darbin**.</span><span class="sxs-lookup"><span data-stu-id="89771-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="89771-118">Atlasiet pogu **PowerApps** un tad atlasiet **Ievietot PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="89771-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps poga](media/png.png)

3. <span data-ttu-id="89771-120">Aizpildiet laukus dialoglodziņā **Ievietot PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="89771-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogl. Ievietot PowerApp](media/insert-powerapp.png)

<span data-ttu-id="89771-122">Vai arī veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="89771-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="89771-123">Lapas darbību rūts cilnes **Opcijas** grupā **Personalizēt** atlasiet **Personalizēt šo veidlapu**.</span><span class="sxs-lookup"><span data-stu-id="89771-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Personalizēt grupu cilnē Opcijas](media/options.png)

    <span data-ttu-id="89771-125">Tiek parādīta personaliz. rīkjosla.</span><span class="sxs-lookup"><span data-stu-id="89771-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="89771-126">Rīkjoslā atlasiet **Ievietot \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="89771-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![PowerApps programmas ievietošana, lietojot personalizēšanas rīkjoslu](media/powerapp-bar.png)
