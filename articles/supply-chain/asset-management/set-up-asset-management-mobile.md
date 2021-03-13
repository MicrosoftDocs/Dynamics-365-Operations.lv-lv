---
title: Līdzekļu pārvaldības darbvietas izmantošana
description: Šajā tēmā ir aprakstīts, kā iestatīt Microsoft Dynamics 365 Supply Chain Management un Finance and Operations (Dynamics 365) mobile programmu, lai palaistu Līdzekļu pārvaldības mobilo darbvietu, kuru darbinieki var izmantot, lai veiktu līdzekļu pārvaldības uzdevumus.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9c2410c50b5d289792e2cc364674e1e093653590
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033219"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="5357e-103">Līdzekļu pārvaldības darbvietas izmantošana</span><span class="sxs-lookup"><span data-stu-id="5357e-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5357e-104">Šajā tēmā ir aprakstīts, kā iestatīt Microsoft Dynamics 365 Supply Chain Management un Finance and Operations (Dynamics 365) mobile programmu, lai palaistu **Līdzekļu pārvaldības** mobilo darbvietu, kuru darbinieki var izmantot, lai veiktu līdzekļu pārvaldības uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="5357e-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="5357e-105">Iestatīt uzturēsanas darbinieku lietotājus Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5357e-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="5357e-106">Katram lietotājam, kam ir nepieciešama piekļuve **Līdzekļu pārvaldības** mobilajai darbvietai, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="5357e-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="5357e-107">Supply Chain Management dodieties uz **Cilvēkresursi \> Darbinieki** un pārliecinieties, vai lietotājam, kuru vēlaties iestatīt,pastāv darbinieka ieraksts.</span><span class="sxs-lookup"><span data-stu-id="5357e-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="5357e-108">Izveidojiet jaunu darbinieka ierakstu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="5357e-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="5357e-109">Dodieties uz sadaļu **Līdzekļu pārvaldība \> Iestatījumi \> Darbinieki \> Darbinieki** un pārliecinieties, vai iepriekšējā darbībā identificētais (vai izveidotais) darbinieka ieraksts ir kartēts uz darbinieka uzturēšanas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5357e-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="5357e-110">Izveidojiet jaunu darbinieka uzturēšanas ierakstu pēc vajadzības un iestatiet lauku **Darbinieks** uz darbinieka ierakstu no iepriekšējā soļa.</span><span class="sxs-lookup"><span data-stu-id="5357e-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="5357e-111">Dodieties uz sadaļu **Līdzekļu pārvaldība \> Iestatījumi \> Darbinieki \> Uzturēšanas darbinieku grupas** un pārliecinieties, vai iepriekšējā darbībā identificētais (vai izveidotais) darbinieka ieraksts pieder darbinieka uzturēšanas ierakstam.</span><span class="sxs-lookup"><span data-stu-id="5357e-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="5357e-112">Dodieties uz **Sistēmas administrēšana \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="5357e-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="5357e-113">Režģī atlasiet atbilstošo lietotāju.</span><span class="sxs-lookup"><span data-stu-id="5357e-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="5357e-114">Kopsavilkuma cilnē **Lietotāja informācija** iestatiet lauku **Persona** uz darbinieka kontu, kuru vēlaties saistīt ar pašreizējo lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="5357e-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="5357e-115">Šim darbinieka kontam jābūt darbinieka ierakstam, ko 1. solī identificējāt (vai izveidojāt) un kartēts uz darbinieka uzturēšanas ierakstu 2. solī.</span><span class="sxs-lookup"><span data-stu-id="5357e-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="5357e-116">Lietotāju atļaujas un drošības lomas attiecas uz **Līdzekļu pārvaldības** mobilās darbvietas funkcijām, tāpat kā uz Supply Chain Management lietotāja interfeisa funkcijām.</span><span class="sxs-lookup"><span data-stu-id="5357e-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="5357e-117">Tāpēc katram lietotājam, kuru iestatāt, lai piekļūtu **Līdzekļu pārvaldības** mobilajai darbvietai, jābūt drošības lomām, kurām ir nepieciešamas veikt līdzīgas operācijas tieši Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5357e-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="5357e-118">Līdzekļu pārvaldības mobilās darbvietas publicēšana</span><span class="sxs-lookup"><span data-stu-id="5357e-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="5357e-119">Lai līdzekļu pārvaldības līdzekļi būtu pieejami mobilajā programmā Finance and Operations (Dynamics 365), publicējiet **Līdzekļu pārvaldības** mobilo darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5357e-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="5357e-120">Supply Chain Management atlasiet pogu **Iestatījumi** (ātrumkārbas simbols augšējā labajā stūrī) un izvēlnē atlasiet **Mobilā programma**.</span><span class="sxs-lookup"><span data-stu-id="5357e-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="5357e-121">Dialoglodziņā **Pārvaldīt mobilo programmu** atrodiet elementu **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="5357e-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="5357e-122">Ja tajā ir teksts "Metadatos - nav publicēti", darbalauks vēl nav publicēts.</span><span class="sxs-lookup"><span data-stu-id="5357e-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="5357e-123">Ja tajā ir teksts "Metadatos - publicēts", darbvieta jau ir publicēta, un jūš varat izlaist šīs procedūras atlikušo daļu.</span><span class="sxs-lookup"><span data-stu-id="5357e-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="5357e-124">![Pārvaldīt mobilās programmas dialoglodziņu](media/mobile-workspaces.png "Pārvaldīt mobilās programmas dialoglodziņu")</span><span class="sxs-lookup"><span data-stu-id="5357e-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="5357e-125">Atlasiet elementu **Līdzekļu pārvaldība** un pēc tam rīkjoslā atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="5357e-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="5357e-126">Pēc dažām sekundēm jums jāsaņem paziņojums par to, ka darbvietas publicēšana ir veiksmīgi pabeigta.</span><span class="sxs-lookup"><span data-stu-id="5357e-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="5357e-127">Turklāt elementa tekstam jāmainās uz "Metadatos — publicēts."</span><span class="sxs-lookup"><span data-stu-id="5357e-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="5357e-128">Instalējiet un iestatiet Finance and Operations (Dynamics 365) mobilo programmu</span><span class="sxs-lookup"><span data-stu-id="5357e-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="5357e-129">Lai mobilajā ierīcē instalētu **Microsoft Finance and Operations (Dynamics 365) programmu**, dodieties uz vienu no tālāk minētajiem programmu veikaliem:</span><span class="sxs-lookup"><span data-stu-id="5357e-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="5357e-130">Google Android ierīcēm</span><span class="sxs-lookup"><span data-stu-id="5357e-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="5357e-131">Apple iOS ierīcēm</span><span class="sxs-lookup"><span data-stu-id="5357e-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="5357e-132">Atveriet Finance and Operations (Dynamics 365) programmu.</span><span class="sxs-lookup"><span data-stu-id="5357e-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="5357e-133">Jāparādās pierakstīšanās lapai.</span><span class="sxs-lookup"><span data-stu-id="5357e-133">The sign-in page should appear.</span></span> <span data-ttu-id="5357e-134">**Pieteikšanās** laukā ievadiet Supply Chain Management URL vai atlasiet neseno URL sarakstā **Jaunākās vides** un pēc tam nospiediet **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="5357e-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="5357e-135">![Pierakstīšanās lapa](media/mobile-app-sign-in.png "Pierakstīšanās lapa")</span><span class="sxs-lookup"><span data-stu-id="5357e-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="5357e-136">Ja tiek piedāvāts apstiprināt savienojumu, atzīmējiet izvēles rūtiņu **Es saprotu** un pēc tam nospiediet taustiņu **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="5357e-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="5357e-137">Lapā **Konta izvēle** izmantojiet Microsoft kontu, lai pieteiktos mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="5357e-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="5357e-138">Tiek atvērta lapa **Darbvietas**.</span><span class="sxs-lookup"><span data-stu-id="5357e-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="5357e-139">Tas uzskaita katru mobilo darbvietu, ko publicējusi jūsu Supply Chain Management instance.</span><span class="sxs-lookup"><span data-stu-id="5357e-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="5357e-140">![Darbvietu saraksts](media/mobile-app-workspaces.png "Darbvietu saraksts")</span><span class="sxs-lookup"><span data-stu-id="5357e-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="5357e-141">Ja jāmaina juridiskā persona (uzņēmums), augšējā kreisajā stūrī klikšķiniet pogu Izvēlne (dažreiz tiek saukta par hamburgera pogu) un pēc tam nospiediet **Mainīt uzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="5357e-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="5357e-142">![Juridiskās personas maiņa](media/mobile-app-change-comp.png "Juridiskās personas maiņa")</span><span class="sxs-lookup"><span data-stu-id="5357e-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="5357e-143">Lapā **Darbvietas** atlasiet darbvietu, ar kuru vēlaties strādāt, lai to atvērtu.</span><span class="sxs-lookup"><span data-stu-id="5357e-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="5357e-144">![Līdzekļu pārvaldības mobilā darbvieta](media/mobile-app-asset-workspace.png "Līdzekļu pārvaldības mobilā darbvieta")</span><span class="sxs-lookup"><span data-stu-id="5357e-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="5357e-145">Darbs ar Līdzekļu pārvaldības mobilo darbvietu</span><span class="sxs-lookup"><span data-stu-id="5357e-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="5357e-146">Papildinformāciju par to, kā strādāt ar **Līdzekļu pārvaldības** mobilo darbvietu, skatiet sadaļā [Līdzekļu pārvaldības mobilās darbvietas izmantošana](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="5357e-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="5357e-147">Papildinformāciju par Finance and Operations (Dynamics 365) mobilo programmu skatiet [mobilās programmas sākumlapā](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="5357e-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>
