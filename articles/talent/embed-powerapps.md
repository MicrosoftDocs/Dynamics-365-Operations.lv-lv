---
title: Power Apps programmu iegulšana Dynamics 365 Human Resources
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017877"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="87ee3-103">Power Apps programmu iegulšana Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="87ee3-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="87ee3-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="87ee3-104">**Issue**</span></span>

<span data-ttu-id="87ee3-105">**Power Apps** izvēlnes elements netiek rādīts modulī **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="87ee3-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="87ee3-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="87ee3-106">**Cause**</span></span>

<span data-ttu-id="87ee3-107">Ir mainīts lietotāja interfeisa (UI) noformējums, un pakalpojums Microsoft Power Apps tagad ir ietverts standarta personalizācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="87ee3-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="87ee3-108">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="87ee3-108">**Resolution**</span></span>

<span data-ttu-id="87ee3-109">Ir mainīts veids, kā Power Apps tiek iegultas.</span><span class="sxs-lookup"><span data-stu-id="87ee3-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="87ee3-110">Power Apps tagad pievieno, lietojot personalizācijas modeli.</span><span class="sxs-lookup"><span data-stu-id="87ee3-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="87ee3-111">Varat pievienot Power Apps gandrīz visās Microsoft Dynamics 365 Talent lapās.</span><span class="sxs-lookup"><span data-stu-id="87ee3-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="87ee3-112">Informāciju par to, kā iegult Power Apps programmā Talent, skatiet tēmā [Iegult Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="87ee3-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="87ee3-113">Visiem Power Apps klientiem, kas veica programmu iegulšanu pirms izmaiņām, ir jābūt jauninātiem uz jauno modeli.</span><span class="sxs-lookup"><span data-stu-id="87ee3-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="87ee3-114">Poga **Power Apps** ir gandrīz visu Talent lapu augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="87ee3-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="87ee3-115">Šo pogu var lietot, lai ievietotu programmas.</span><span class="sxs-lookup"><span data-stu-id="87ee3-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="87ee3-116">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="87ee3-116">Here is an example.</span></span>

1. <span data-ttu-id="87ee3-117">Dod. uz **Person. pārvald. \> Saites \> Nodarbin. \> Darbin**.</span><span class="sxs-lookup"><span data-stu-id="87ee3-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="87ee3-118">Atlasiet pogu **Power Apps** un pēc tam atlasiet **Pievienot programmu no Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="87ee3-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps poga](media/png.png)

3. <span data-ttu-id="87ee3-120">Aizpildiet laukus dialoglodziņā **Pievienot programmu no Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="87ee3-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Programmas pievienošana no Power Apps dialoglodziņa](media/insert-powerapp.png)

<span data-ttu-id="87ee3-122">Vai arī veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="87ee3-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="87ee3-123">Lapas darbību rūts cilnes **Opcijas** grupā **Personalizēt** atlasiet **Personalizēt šo lapu**.</span><span class="sxs-lookup"><span data-stu-id="87ee3-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Personalizēt grupu cilnē Opcijas](media/options.png)

    <span data-ttu-id="87ee3-125">Tiek parādīta personaliz. rīkjosla.</span><span class="sxs-lookup"><span data-stu-id="87ee3-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="87ee3-126">Rīkjoslā noklikšķiniet uz opcijas **Pievienot programmu no Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="87ee3-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Programmas pievienošana no Power Apps, izmantojot personalizēšanas rīkjoslu](media/powerapp-bar.png)
