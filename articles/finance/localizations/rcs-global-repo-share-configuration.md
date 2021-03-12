---
title: Elektronisko pārskatu konfigurāciju koplietošana RCS/globālā repozitorija ar ārējām organizācijām
description: Šajā tēmā skaidrots, kā koplietot elektronisko pārskatu (ER) konfigurācijas Microsoft Regulatory Configuration Services (RCS)/globālā repozitorijā tieši ar ārējām organizācijām.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0973d36a8fddd16d02776ac6567d424ac6ebc3ae
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994315"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="0b7fa-103">Koplietot elektronisko pārskatu (ER) konfigurācijas Regulatory Configuration Services (RCS) globālā repozitorijā tieši ar ārējām organizācijām</span><span class="sxs-lookup"><span data-stu-id="0b7fa-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b7fa-104">Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai koplietotu elektroniskos pārskatu (ER) konfigurācijas un pēc tam publicētu tās ārējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="0b7fa-105">Tālāk sniegtajos procedūru aprakstos ir paskaidrots kā RCS lietotājs var dalīties ar ER konfigurācijas versiju, kas ir konfigurēta kā RCS instance ar ārēju organizāciju.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="0b7fa-106">Lai varētu veikt šīs procedūras, ir jāizpilda šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="0b7fa-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="0b7fa-107">Piekļūstiet RCS instancei.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-107">Access an RCS instance.</span></span>
- <span data-ttu-id="0b7fa-108">Izveidojiet aktīvu konfigurācijas nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-108">Create an active configuration provider.</span></span> <span data-ttu-id="0b7fa-109">Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0b7fa-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="0b7fa-110">Izveidojiet un augšupielādējiet jaunu ER konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="0b7fa-111">Papildinformāciju skatiet šeit: [Jauna elektroniskā pārskata (ER) konfigurācijas versijas izveide un augšupielāde](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="0b7fa-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="0b7fa-112">Jums ir arī jāpārliecinās, ka RCS vide ir nodrošināta jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="0b7fa-113">Programmā Finance and Operations dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektroniskie pārskat**.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0b7fa-114">Ja jūsu uzņēmumā nav nodrošināta neviena RCS vide, atlasiet **Regulatory services — Configuration external** un pēc tam izpildiet norādījumus, lai tādu nodrošinātu.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="0b7fa-115">Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapas vietrādi URL, lai piekļūtu tai, atlasot pierakstīšanās opciju.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="0b7fa-116">Pārbaudiet konfigurāciju, ko vēlaties koplietot</span><span class="sxs-lookup"><span data-stu-id="0b7fa-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="0b7fa-117">Sekojiet šiem soļiem, lai pārbaudītu, vai konfigurācija, kuru vēlaties koplietot, jau ir augšupielādēta globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="0b7fa-118">**Elektroniskā pārskata** darbvietā atlasiet **Repozitoriji** jūsu konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigurācijas nodrošinātāji](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="0b7fa-120">Atlasiet **Globālais repozitorijs** \> **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="0b7fa-121">Meklējiet konfigurāciju, ko vēlaties koplietot.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="0b7fa-122">Varat izmantot filtra lauku, lai sašaurinātu meklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="0b7fa-123">Ja jūs nevarat atrast konfigurāciju globālajā repozitorijā, sekojiet soļiem, lai [izveidotu un augšupielādētu jaunu elektronisko pārskatu (ER) konfigurācijas versiju](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="0b7fa-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="0b7fa-124">ER konfigurāciju koplietošana ar ārējām organizācijām</span><span class="sxs-lookup"><span data-stu-id="0b7fa-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="0b7fa-125">Kad konfigurācijas nodrošinātājs ir izveidojis konfigurāciju, to var tieši koplietot ar ārējām organizācijām, izmantojot **Kopīgots ar** kopsavilkuma lapā **globālās konfigurācijas repozitorijs**.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="0b7fa-126">**Elektroniskā pārskata** darbvietā atlasiet **Repozitoriji** jūsu konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="0b7fa-127">Atlasiet **Globālais repozitorijs** \> **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="0b7fa-128">Atlasiet konfigurāciju, ko vēlaties koplietot.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="0b7fa-129">Kopsavilkuma cilnē **Kopīgots ar** atlasiet **Organizācija**.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Koplietots izmantojot kopsavilkuma cilni](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="0b7fa-131">Dialoglodziņā ievadiet ārējās organizācijas domēna nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Koplietošanas konfigurācijas versija ar ārējo organizācijas dialoglodziņu](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="0b7fa-133">Konfigurācija tiek koplietota ar ārējo organizāciju un ir pieejama šai organizācijai globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="0b7fa-134">No turienes to var importēt organizācijas RCS instancē vai tās programmas Finance and Operations instancēs.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="0b7fa-135">Lai atceltu konfigurāciju, kas iepriekš bijusi koplietota ar ārēju organizāciju, atlasiet konfigurāciju un noklikšķiniet uz **pārtraukt koplietošanu** un pēc tam atlasiet **Labi**</span><span class="sxs-lookup"><span data-stu-id="0b7fa-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
