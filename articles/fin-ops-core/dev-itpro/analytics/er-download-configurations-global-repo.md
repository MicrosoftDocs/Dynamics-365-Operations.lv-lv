---
title: Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija
description: Šajā tēmā paskaidrots, kā lejupielādēt elektronisko pārskatu (ER) konfigurācijas no konfigurācijas pakalpojuma globālā repozitorija.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c4f083163db72569d91825819a904319a0fe3123
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561906"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="68b7a-103">Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="68b7a-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68b7a-104">Šajā tēmā paskaidrots, kā lejupielādēt [Elektronisko pārskatu (ER) konfigurācijas](general-electronic-reporting.md#Configuration) no konfigurācijas pakalpojuma globālā repozitorija.</span><span class="sxs-lookup"><span data-stu-id="68b7a-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="68b7a-105">Plašāku informāciju skatiet [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, konfigurācijas pakalpojums](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="68b7a-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="68b7a-106">Atvērt konfigurācijas repozitoriju</span><span class="sxs-lookup"><span data-stu-id="68b7a-106">Open configurations repository</span></span>

1. <span data-ttu-id="68b7a-107">Pierakstieties programmā Dynamics 365 Finance, izmantojot vienu no tālāk minētajām lomām.</span><span class="sxs-lookup"><span data-stu-id="68b7a-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="68b7a-108">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="68b7a-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="68b7a-109">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="68b7a-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="68b7a-110">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="68b7a-110">System administrator</span></span>

2. <span data-ttu-id="68b7a-111">Pārejiet uz sadaļu **Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="68b7a-112">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="68b7a-113">Elementā **Microsoft** atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Elektronisko pārskatu darbvieta](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="68b7a-115">Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar veidu **Globāls**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="68b7a-116">Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="68b7a-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="68b7a-117">Atlasiet **Pievienot**, lai pievienotu jaunu repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="68b7a-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="68b7a-118">Atlasiet **Globāls** kā repozitorija veidu un pēc tam atlasiet **Izveidot repozitoriju**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="68b7a-119">Ja tiek pieprasīts, izpildiet autorizācijas norādījumus.</span><span class="sxs-lookup"><span data-stu-id="68b7a-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="68b7a-120">Ievadiet repozitorija nosaukumu un aprakstu un pēc tam atlasiet **Labi**, lai apstiprinātu jauno repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="68b7a-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="68b7a-121">Režģī atlasiet jauno repozitoriju ar veidu **Globāls**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="68b7a-122">Atlasiet **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.</span><span class="sxs-lookup"><span data-stu-id="68b7a-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Repozitoriju lapas konfigurēšana](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="68b7a-124">Vienas atsevišķas konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="68b7a-124">Import a single configuration</span></span>

1. <span data-ttu-id="68b7a-125">Lapā **Konfigurācijas repozirotiji** konfigurāciju kokā atlasiet vēlamo ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="68b7a-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="68b7a-126">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.</span><span class="sxs-lookup"><span data-stu-id="68b7a-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="68b7a-127">Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.</span><span class="sxs-lookup"><span data-stu-id="68b7a-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68b7a-128">Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="68b7a-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Konfigurācijas repozitorijas lapa.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="68b7a-130">Filtrēto konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="68b7a-130">Import filtered configurations</span></span>

1. <span data-ttu-id="68b7a-131">Lapā **Konfigurāciju repozitoriji** konfigurāciju kokā izvērsiet kopsavilkuma cilni **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="68b7a-132">Režģī **Tagi** pievienojiet visus nepieciešamos tagus.</span><span class="sxs-lookup"><span data-stu-id="68b7a-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="68b7a-133">Laukā **Valsts/reģiona piemērojamība** atlasiet attiecīgos valstu/reģionu kodus un pēc tam atlasiet **Lietot filtru**.</span><span class="sxs-lookup"><span data-stu-id="68b7a-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68b7a-134">Kopsavilkuma cilnes **Konfigurācijas** rāda visas konfigurācijas, kas atbilst norādītajiem atlases nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="68b7a-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="68b7a-135">Kopsavilkuma cilnē **Konfigurācijas** atlasiet **Importēt**, lai lejupielādētu filtrētās konfigurācijas no Globālā repozitorija uz pašreizējo instanci.</span><span class="sxs-lookup"><span data-stu-id="68b7a-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="68b7a-136">Kopsavilkuma cilnē **Konfigurācijas** atlasiet **Atiestatīt filtru**, lai notīrītu norādītos atlases nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="68b7a-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Konfigurācijas repozitorijas lapa.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="68b7a-138">Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas.</span><span class="sxs-lookup"><span data-stu-id="68b7a-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="68b7a-139">Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām.</span><span class="sxs-lookup"><span data-stu-id="68b7a-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="68b7a-140">Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="68b7a-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="68b7a-141">Plašāku informāciju skatiet ar šo tēmu saistīto resursu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="68b7a-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="68b7a-142">ER konfigurācijas var konfigurēt kā atkarīgas no citām konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="68b7a-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="68b7a-143">Tāpēc kopā ar izvēlēto konfigurāciju var automātiski importēt citas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="68b7a-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="68b7a-144">Plašāku informāciju par konfigurācijas atkarībām skatiet [Noteikt atkarību no ER konfigurācijām citos komponentos](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="68b7a-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68b7a-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="68b7a-145">Additional resources</span></span>

[<span data-ttu-id="68b7a-146">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="68b7a-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]