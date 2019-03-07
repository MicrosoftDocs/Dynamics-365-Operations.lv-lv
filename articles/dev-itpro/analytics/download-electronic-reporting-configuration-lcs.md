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
ms.openlocfilehash: 8686d2639a3ab7f2e79944cc5eed51571d463261
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "315755"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="5ca8f-103">Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="5ca8f-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ca8f-104">Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5ca8f-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="5ca8f-105">Šajā apmācībā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (ER) konfigurāciju jaunāko versiju no portāla Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5ca8f-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="5ca8f-106">Pierakstieties programmatūrā Dynamics 365 for Finance and Operations, izmantojot kādu no tālāk norādītajām lomām.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-106">Sign in to Finance and Operations by using one of the following roles:</span></span>

    - <span data-ttu-id="5ca8f-107">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="5ca8f-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="5ca8f-108">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="5ca8f-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5ca8f-109">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="5ca8f-109">System administrator</span></span>

2. <span data-ttu-id="5ca8f-110">Dodieties uz **Organizācijas administrēšana** &gt; **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="5ca8f-111">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="5ca8f-112">Elementā **Microsoft** noklikšķiniet uz **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="5ca8f-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="5ca8f-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="5ca8f-114">Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="5ca8f-115">Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="5ca8f-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="5ca8f-116">Noklikšķiniet uz **Pievienot**, lai pievienotu jaunu repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="5ca8f-117">Atlasiet **LCS** kā repozitorija tipu.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="5ca8f-118">Noklikšķiniet uz **Izveidot repozitoriju**.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="5ca8f-119">Ja tiek pieprasīts, izpildiet autorizācijas norādījumus.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="5ca8f-120">Ievadiet repozitorija nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="5ca8f-121">Noklikšķiniet uz **Labi**, lai apstiprinātu jauno repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="5ca8f-122">Režģī atlasiet jauno repozitoriju ar tipu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="5ca8f-123">Noklikšķiniet uz **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="5ca8f-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="5ca8f-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="5ca8f-125">Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="5ca8f-126">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="5ca8f-127">Noklikšķiniet uz **Importēt**, lai lejupielādētu atlasīto versiju no pakalpojuma LCS uz pašreizējo programmatūras Dynamics 365 for Finance and Operations instanci.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ca8f-128">Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā programmatūras Dynamics 365 for Finance and Operations instancē.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span>

    <span data-ttu-id="5ca8f-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="5ca8f-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5ca8f-130">Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="5ca8f-131">Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="5ca8f-132">Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="5ca8f-133">Plašāku informāciju skatiet ar šo tēmu saistīto rakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ca8f-134">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5ca8f-134">Additional resources</span></span>

[<span data-ttu-id="5ca8f-135">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="5ca8f-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)
