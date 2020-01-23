---
title: Power Apps programmu iegulšana Dynamics 365 — Core HR
description: Šajā tēmā izskaidrots, kā atrisināt problēmu, kad Microsoft Power Apps izvēlnes elements netiek rādīts sistēmas administrēšanas modulī.
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
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898716"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="5cfe2-103">Power Apps programmu iegulšana Dynamics 365 — Core HR</span><span class="sxs-lookup"><span data-stu-id="5cfe2-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

<span data-ttu-id="5cfe2-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="5cfe2-104">**Issue**</span></span>

<span data-ttu-id="5cfe2-105">**Power Apps** izvēlnes elements netiek rādīts modulī **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="5cfe2-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="5cfe2-106">**Cause**</span></span>

<span data-ttu-id="5cfe2-107">Ir mainīts lietotāja interfeisa (UI) noformējums, un pakalpojums Microsoft Power Apps tagad ir ietverts standarta personalizācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="5cfe2-108">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="5cfe2-108">**Resolution**</span></span>

<span data-ttu-id="5cfe2-109">Ir mainīts veids, kā Power Apps tiek iegultas.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="5cfe2-110">Power Apps tagad pievieno, lietojot personalizācijas modeli.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="5cfe2-111">Varat pievienot Power Apps gandrīz visās Microsoft Dynamics 365 Talent lapās.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="5cfe2-112">Informāciju par to, kā iegult Power Apps programmā Talent, skatiet tēmā [Iegult Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="5cfe2-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="5cfe2-113">Visiem Power Apps klientiem, kas veica programmu iegulšanu pirms izmaiņām, ir jābūt jauninātiem uz jauno modeli.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="5cfe2-114">Poga **Power Apps** ir gandrīz visu Talent lapu augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="5cfe2-115">Šo pogu var lietot, lai ievietotu Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="5cfe2-116">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-116">Here is an example.</span></span>

1. <span data-ttu-id="5cfe2-117">Dod. uz **Person. pārvald. \> Saites \> Nodarbin. \> Darbin**.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="5cfe2-118">Atlasiet pogu **Power Apps** un tad atlasiet **Ievietot PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps poga](media/png.png)

3. <span data-ttu-id="5cfe2-120">Aizpildiet laukus dialoglodziņā **Ievietot PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogl. Ievietot PowerApp](media/insert-powerapp.png)

<span data-ttu-id="5cfe2-122">Vai arī veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="5cfe2-123">Lapas darbību rūts cilnes **Opcijas** grupā **Personalizēt** atlasiet **Personalizēt šo veidlapu**.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Personalizēt grupu cilnē Opcijas](media/options.png)

    <span data-ttu-id="5cfe2-125">Tiek parādīta personaliz. rīkjosla.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="5cfe2-126">Rīkjoslā atlasiet **Ievietot \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="5cfe2-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Power Apps programmas ievietošana, lietojot personalizēšanas rīkjoslu](media/powerapp-bar.png)
