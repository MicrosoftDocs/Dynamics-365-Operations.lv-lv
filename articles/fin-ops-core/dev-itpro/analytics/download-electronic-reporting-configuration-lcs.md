---
title: Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services
description: Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49785835ee2da911d7b8d1360e1c42f850f1153f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771497"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="be0d3-103">Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="be0d3-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be0d3-104">Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="be0d3-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="be0d3-105">Šajā apmācībā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (ER) konfigurāciju jaunāko versiju no portāla Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="be0d3-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="be0d3-106">Pierakstieties programmā, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="be0d3-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="be0d3-107">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="be0d3-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="be0d3-108">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="be0d3-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="be0d3-109">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="be0d3-109">System administrator</span></span>

2. <span data-ttu-id="be0d3-110">Dodieties uz **Organizācijas administrēšana** &gt; **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="be0d3-111">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="be0d3-112">Elementā **Microsoft** noklikšķiniet uz **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="be0d3-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="be0d3-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="be0d3-114">Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="be0d3-115">Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="be0d3-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="be0d3-116">Noklikšķiniet uz **Pievienot**, lai pievienotu jaunu repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="be0d3-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="be0d3-117">Atlasiet **LCS** kā repozitorija tipu.</span><span class="sxs-lookup"><span data-stu-id="be0d3-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="be0d3-118">Noklikšķiniet uz **Izveidot repozitoriju**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="be0d3-119">Ja tiek pieprasīts, izpildiet autorizācijas norādījumus.</span><span class="sxs-lookup"><span data-stu-id="be0d3-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="be0d3-120">Ievadiet repozitorija nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="be0d3-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="be0d3-121">Noklikšķiniet uz **Labi**, lai apstiprinātu jauno repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="be0d3-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="be0d3-122">Režģī atlasiet jauno repozitoriju ar tipu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="be0d3-123">Noklikšķiniet uz **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.</span><span class="sxs-lookup"><span data-stu-id="be0d3-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="be0d3-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="be0d3-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="be0d3-125">Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="be0d3-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="be0d3-126">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.</span><span class="sxs-lookup"><span data-stu-id="be0d3-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="be0d3-127">Noklikšķiniet uz **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo instanci.</span><span class="sxs-lookup"><span data-stu-id="be0d3-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="be0d3-128">Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā instancē.</span><span class="sxs-lookup"><span data-stu-id="be0d3-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="be0d3-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="be0d3-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="be0d3-130">Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas.</span><span class="sxs-lookup"><span data-stu-id="be0d3-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="be0d3-131">Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām.</span><span class="sxs-lookup"><span data-stu-id="be0d3-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="be0d3-132">Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="be0d3-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="be0d3-133">Plašāku informāciju skatiet ar šo tēmu saistīto rakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="be0d3-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be0d3-134">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="be0d3-134">Additional resources</span></span>

[<span data-ttu-id="be0d3-135">Elektronisko ziņojumu (ER) pārskats</span><span class="sxs-lookup"><span data-stu-id="be0d3-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
