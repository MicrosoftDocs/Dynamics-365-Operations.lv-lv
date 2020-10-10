---
title: Jauns dokumentu lietotāja interfeiss biznesa dokumentu pārvaldībā
description: Šajā tēmā ir sniegta informācija par to, kā izmantot jauno dokumentu lietotāja interfeisu (UI) elektroniskā pārskata (ER) struktūras biznesa dokumentu pārvaldības līdzeklī.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 015b595f85397fc1cf2c0368814ddc0369176f82
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893199"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="3e79d-103">Jauns dokumentu lietotāja interfeiss biznesa dokumentu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="3e79d-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e79d-104">Biznesa dokumentu pārvaldība ļauj biznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft 365 vai atbilstošu Microsoft Office darbvirsmas lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="3e79d-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="3e79d-105">Rediģējumi var ietvert dizaina izmaiņas vai jaunas izvietošanas, vai arī lietotāji var pievienot vietturus, lai iekļautu papildu datus, nemainot pirmkodu.</span><span class="sxs-lookup"><span data-stu-id="3e79d-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="3e79d-106">Papildinformāciju par to, kā strādāt ar biznesa dokumentu pārvaldību, skatiet [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="3e79d-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="3e79d-107">Jaunais dokumentu lietotāja interfeiss (UI) ir saprotamāks un ērtāk lietojams.</span><span class="sxs-lookup"><span data-stu-id="3e79d-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="3e79d-108">**Biznesa dokumenta** apgabals parāda tikai tās veidnes, kas ir pieejamas pašreizējam nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="3e79d-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="3e79d-109">Poga **Jauns dokuments** ļauj lietotājiem izveidot un rediģēt veidni elektroniskā pārskata (ER) formāta konfigurācijā, kas pieder citam nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="3e79d-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="3e79d-110">Šīs tēmas piemērā nodrošinātājs ir Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e79d-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="3e79d-111">Nodrošināt jauno dokumentu lietotāja interfeisa pieejamību biznesa dokumentu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="3e79d-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="3e79d-112">Lai biznesa dokumentu pārvaldībā sāktu izmantot jauno dokumentu lietotāja interfeisu, jāieslēdz līdzeklis **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai** darbvietā **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="3e79d-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="3e79d-113">Lai ieslēgtu šo līdzekli visām juridiskajām personām, veiciet tālak norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="3e79d-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="3e79d-114">Darbvietas **Lïdzekĺu pārvaldība** cilnē **Jauns** atlasiet sarakstā līdzekli **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**.</span><span class="sxs-lookup"><span data-stu-id="3e79d-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="3e79d-115">Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="3e79d-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="3e79d-116">Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="3e79d-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="3e79d-117">Citiem nodrošinātājiem piederošu veidņu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="3e79d-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="3e79d-118">Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.</span><span class="sxs-lookup"><span data-stu-id="3e79d-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="3e79d-120">Dialoglodziņā atlasiet dokumentu, kas jālieto kā veidne, un pēc tam atlasiet **Izveidot dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="3e79d-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialoglodziņš biznesa dokumenti](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="3e79d-122">Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="3e79d-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="3e79d-123">Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="3e79d-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="3e79d-124">Šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija ietvers rediģēto veidni un tiks izmantota šī ER formāta izmantošanai pašreizējam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="3e79d-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="3e79d-125">Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="3e79d-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="3e79d-126">Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.</span><span class="sxs-lookup"><span data-stu-id="3e79d-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="3e79d-127">Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="3e79d-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="3e79d-128">Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.</span><span class="sxs-lookup"><span data-stu-id="3e79d-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialoglodziņš Dokumenta izveide](./media/BDM_overview_new_template3.png)

<span data-ttu-id="3e79d-130">Pogu **Jauns dokuments** lieto, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, kas pieder citam nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="3e79d-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="3e79d-131">Šajā piemērā nodrošinātājs ir Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e79d-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="3e79d-132">Atlasot **Jauns dokuments**, jūs varat rezēt visas veidnes, kas pieder pašreizējiem un citiem nodrošinātājiem.</span><span class="sxs-lookup"><span data-stu-id="3e79d-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="3e79d-133">Pēc veidnes atlasīšanas tā ir atvērta rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="3e79d-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="3e79d-134">Rediģētā veidne būs saglabāta jaunā ER formāta konfigurācijā, kas ģenerēta automātiski.</span><span class="sxs-lookup"><span data-stu-id="3e79d-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="3e79d-135">Plašāku informāciju skatiet [Biznesa dokumentu pārvaldības apskatā](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="3e79d-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
