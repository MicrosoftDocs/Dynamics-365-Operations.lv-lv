---
title: Elektronisko pārskatu konfigurāciju izveide pakalpojumā RCS un to augšupielāde globālajā repozitorijā
description: Šajā tēmā skaidrots, kā izveidot elektronisko pārskatu (ER) konfigurāciju Microsoft Regulatory Configuration Services (RCS) un augšupielādēt to globālajā repozitorijā.
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a138fd4b525077f12f6575f4b10f682728b71203
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838723"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="7885d-103">ER konfigurāciju izveide Regulatory Configuration Services (RCS) un to augšupielāde globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="7885d-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7885d-104">Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai veidotu elektroniska pārskata (ER) konfigurācijas un publicētu tās, lai tās varētu izmantot jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="7885d-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="7885d-105">Tālāk aprakstītajās procedūrās ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot atvasinātu Elektroniskā pārskata (EK) versiju, kas ir konfigurēta RCS instancē, un pēc tam augšupielādēt atvasināto konfigurāciju globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="7885d-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="7885d-106">Lai varētu veikt šīs procedūras, ir jāizpilda šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="7885d-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="7885d-107">Piekļūstiet RCS instancei.</span><span class="sxs-lookup"><span data-stu-id="7885d-107">Access an RCS instance.</span></span>
- <span data-ttu-id="7885d-108">Izveidojiet aktīvu konfigurācijas nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="7885d-108">Create an active configuration provider.</span></span> <span data-ttu-id="7885d-109">Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7885d-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="7885d-110">Jums ir arī jāpārliecinās, ka RCS vide ir nodrošināta jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="7885d-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="7885d-111">Programmā Finance and Operations dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektroniskie pārskat**.</span><span class="sxs-lookup"><span data-stu-id="7885d-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7885d-112">Ja jūsu uzņēmumā nav nodrošināta neviena RCS vide, atlasiet **Regulatory services — Configuration external** un pēc tam izpildiet norādījumus, lai tādu nodrošinātu.</span><span class="sxs-lookup"><span data-stu-id="7885d-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="7885d-113">Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapas vietrādi URL, lai piekļūtu tai, atlasot pierakstīšanās opciju.</span><span class="sxs-lookup"><span data-stu-id="7885d-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="7885d-114">Izveidot atvasinātu konfigurācijas versiju RCS</span><span class="sxs-lookup"><span data-stu-id="7885d-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="7885d-115">Darbvietas **Elektroniskajā pārskatā** pārbaudiet, vai jūsu organizācijai ir aktīvs konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="7885d-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="7885d-116">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="7885d-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7885d-117">Atlasiet konfigurāciju, no kuras vēlaties atvasināt jauno versiju.</span><span class="sxs-lookup"><span data-stu-id="7885d-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="7885d-118">Varat izmantot filtra lauku virs koka skata, lai sašaurinātu meklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7885d-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="7885d-119">Atlasiet **Izveidot konfigurāciju** \> **Atvasināt no nosaukuma**.</span><span class="sxs-lookup"><span data-stu-id="7885d-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="7885d-120">Ievadiet nosaukumu un aprakstu un pēc tam atlasiet **Izveidot konfigurāciju**, lai izveidotu jaunu atvasinātu versiju.</span><span class="sxs-lookup"><span data-stu-id="7885d-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="7885d-121">Atlasiet tikko atvasināto konfigurāciju, pievienojiet versijas aprakstu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7885d-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="7885d-122">Konfigurācijas statuss ir nomainīts uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="7885d-122">The status of the configuration to is changed to **Completed**.</span></span>

![Jauna konfigurācijas versija RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="7885d-124">Kad konfigurācijas statuss ir mainīts, var tikt parādīts pārbaudes kļūdas ziņojums, kas saistīts ar savienotajām lietojumprogrammām.</span><span class="sxs-lookup"><span data-stu-id="7885d-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="7885d-125">Lai izslēgtu pārbaudi, cilnes **Konfigurācijas** darbību rūtī atlasiet **Lietotāja parametri** un pēc tam opciju **Izlaist validāciju konfigurācijas statusa maiņai un pārbāzei** iestatītu uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="7885d-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="7885d-126">Konfigurācijas augšupielāde globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="7885d-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="7885d-127">Lai koplietotu jaunu vai atvasinātu konfigurāciju ar savu organizāciju, varat to augšupielādēt globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="7885d-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="7885d-128">Atlasiet konfigurācijas pabeigtu versiju un pēc tam atlasiet **Augšupielādēt repozitorijā**.</span><span class="sxs-lookup"><span data-stu-id="7885d-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="7885d-129">Atlasiet opciju **Globāli (Microsoft)** un pēc tam atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="7885d-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Augšupielādēt repozitorija opcijās](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="7885d-131">Apstiprinājuma ziņojuma lodziņā atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7885d-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="7885d-132">Atjauniniet versijas aprakstu pēc nepieciešamības un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7885d-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="7885d-133">Konfigurācijas statuss ir atjaunināts uz **Kopīgot**, un konfigurācija ir augšupielādēta globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="7885d-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="7885d-134">No turienes ar to var strādāt šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="7885d-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="7885d-135">Importējiet to savā Dynamics 365 instancē.</span><span class="sxs-lookup"><span data-stu-id="7885d-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="7885d-136">Papildinformāciju skatiet [(ER) Konfigurāciju importēšana no RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="7885d-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="7885d-137">Koplietot to ar trešo pusi vai ārēju organizāciju, skatiet [RCS Koplietot elektronisko pārskatu (ER) konfigurācijas ar ārējām organizācijām](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="7885d-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Atvasinātā Intrastat Contoso konfigurācijas versija globālajā krātuvē](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="7885d-139">Konfigurācijas dzēšana no globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="7885d-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="7885d-140">Lai dzēstu jūsu organizācijas izveidoto konfigurāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7885d-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="7885d-141">**Elektroniskā pārskata** darbvietā pārbaudiet, vai jūsu konfigurācijas nodrošinātājs ir **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="7885d-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="7885d-142">Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7885d-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="7885d-143">Aktīvajam konfigurācijas nodrošinātājam atlasiet **repozitoriju**.</span><span class="sxs-lookup"><span data-stu-id="7885d-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="7885d-144">Atlasiet repozitorija veidu **Globāls** un atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="7885d-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="7885d-145">Kopsavilkuma cilnē **Filtrs** atrodiet konfigurāciju, ko vēlaties dzēst, izmantojot funkciju **Filtrs**.</span><span class="sxs-lookup"><span data-stu-id="7885d-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="7885d-146">Kopsavilkuma cilnē **Versija** atlasiet konfigurācijas versiju, ko vēlaties dzēst, un pēc tam atlasiet **Dzēst**:</span><span class="sxs-lookup"><span data-stu-id="7885d-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Konfigurācijas dzēšana no globālā repozitorija](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="7885d-148">Apstiprinājuma ziņojuma lodziņā atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7885d-148">In the confirmation message box, select **Yes**.</span></span>

    ![Konfigurācijas versijas dzēšanas apstiprinājuma ziņojums](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="7885d-150">Konfigurācijas versija tiek dzēsta un tiek parādīts apstiprinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="7885d-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="7885d-151">Konfigurācijas var dzēst tikai konfigurāciju nodrošinātājs, kas tās izveidoja.</span><span class="sxs-lookup"><span data-stu-id="7885d-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="7885d-152">Ja konfigurācija ir koplietota ar citu organizāciju, tad pirms tās dzēšanas, konfigurācijas koplietošana ir jāatceļ.</span><span class="sxs-lookup"><span data-stu-id="7885d-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]