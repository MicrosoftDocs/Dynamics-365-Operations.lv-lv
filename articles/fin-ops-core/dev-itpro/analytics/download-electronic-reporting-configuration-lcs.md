---
title: Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services
description: Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271187"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="f515e-103">Elektronisko pārskatu veidošanas konfigurācijas lejupielāde no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f515e-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f515e-104">Šajā tēmā ir paskaidrots, kā lejupielādēt jaunāko [Elektroniskās ziņošanas (Electronic reporting - ER) konfigurācijas](general-electronic-reporting.md#Configuration) versiju no [Koplietojamo līdzekļu bibliotēka](../lifecycle-services/asset-library.md) programmā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f515e-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f515e-105">LCS kā ER konfigurāciju glabāšanas repozitorija izmantošana ir [novecojusi](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="f515e-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="f515e-106">Papildinformāciju skatiet [Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="f515e-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="f515e-107">Pierakstieties programmā, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="f515e-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="f515e-108">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="f515e-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="f515e-109">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="f515e-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f515e-110">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="f515e-110">System administrator</span></span>

2. <span data-ttu-id="f515e-111">Dodieties uz **Organizācijas administrēšana** &gt; **Darbvietas** &gt; **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="f515e-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="f515e-112">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="f515e-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="f515e-113">Elementā **Microsoft** atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="f515e-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="f515e-114">[![Microsoft elements lokalizācijas konfigurāciju lapā](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="f515e-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="f515e-115">Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f515e-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="f515e-116">Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="f515e-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="f515e-117">Atlasiet **Pievienot**, lai pievienotu repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="f515e-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="f515e-118">Atlasiet **LCS** kā repozitorija tipu.</span><span class="sxs-lookup"><span data-stu-id="f515e-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="f515e-119">Atlasiet **Izveidot repozitoriju**.</span><span class="sxs-lookup"><span data-stu-id="f515e-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="f515e-120">Ja tiek parādīta uzvedne par autorizāciju, izpildiet ekrānā redzamos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="f515e-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="f515e-121">Ievadiet repozitorija nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f515e-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="f515e-122">Atlasiet **Labi**, lai apstiprinātu jauno repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f515e-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="f515e-123">Režģī atlasiet jauno repozitoriju ar tipu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f515e-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="f515e-124">Atlasiet **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.</span><span class="sxs-lookup"><span data-stu-id="f515e-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="f515e-125">[![Repozitoriju lapas konfigurēšana](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="f515e-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="f515e-126">Ja rodas problēmas, piekļūstot LCS repozitorijam, lai lejupielādētu konfigurāciju no koplietojamo līdzekļu bibliotēkas LCS, varat tai vietā lejupielādēt konfigurācijas no [Globālā krātuve](er-download-configurations-global-repo.md) .</span><span class="sxs-lookup"><span data-stu-id="f515e-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="f515e-127">Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="f515e-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="f515e-128">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.</span><span class="sxs-lookup"><span data-stu-id="f515e-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="f515e-129">Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo instanci.</span><span class="sxs-lookup"><span data-stu-id="f515e-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f515e-130">Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā instancē.</span><span class="sxs-lookup"><span data-stu-id="f515e-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="f515e-131">[![Konfigurācijas repozitorijas lapa.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="f515e-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="f515e-132">Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas.</span><span class="sxs-lookup"><span data-stu-id="f515e-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="f515e-133">Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām.</span><span class="sxs-lookup"><span data-stu-id="f515e-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="f515e-134">Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="f515e-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="f515e-135">Plašāku informāciju skatiet ar šo tēmu saistīto tēmu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f515e-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f515e-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f515e-136">Additional resources</span></span>

[<span data-ttu-id="f515e-137">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="f515e-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="f515e-138">Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="f515e-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
