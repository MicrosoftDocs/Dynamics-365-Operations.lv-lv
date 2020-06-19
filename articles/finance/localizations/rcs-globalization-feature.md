---
title: Regulatory Configuration Services (RCS) — globalizācijas līdzekļi
description: Šajā tēmā ir paskaidrots, kā izmantot Microsoft Regulatory Configuration Services (RCS) un globālo repozitāriju, lai izveidotu un lieto globalizācijas līdzekļus.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 97206552616b248f88e516fea08b3f059257e8d1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3432051"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="069d9-103">Regulatory Configuration Services (RCS) — globalizācijas līdzekļi</span><span class="sxs-lookup"><span data-stu-id="069d9-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="069d9-104">Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai izveidotu globalizācijas līdzekli, ko var izmantot globalizācijas pakalpojumos, piemēram, e-rēķina pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="069d9-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="069d9-105">RCS ļauj veikt tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="069d9-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="069d9-106">Definēt līdzekļa saistītos komponentus.</span><span class="sxs-lookup"><span data-stu-id="069d9-106">Define related components of a feature.</span></span>
- <span data-ttu-id="069d9-107">Pārvaldīt līdzekļa dzīves ciklu, izmantojot līdzekļa statusu.</span><span class="sxs-lookup"><span data-stu-id="069d9-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="069d9-108">Padarīt līdzekli pieejamu definētām vidēm.</span><span class="sxs-lookup"><span data-stu-id="069d9-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="069d9-109">Koplietot līdzekli ar citām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="069d9-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="069d9-110">Tālāk minētajās procedūrās ir izskaidrots, kā lietotājs RCS var pievienot globalizācijas līdzekli un saistītos komponentus, atjaunināt līdzekļa statusu un padarīt šo līdzekli pieejamu, lai to varētu izmantot globalizācijas pakalpojumos.</span><span class="sxs-lookup"><span data-stu-id="069d9-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="069d9-111">Pirms procedūru pabeigšanas ir jāveic darbības, kas saistītas ar tālāk minētajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="069d9-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="069d9-112">Piekļūšana RCS instancei.</span><span class="sxs-lookup"><span data-stu-id="069d9-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="069d9-113">Konfigurācijas nodrošinātāja izveide un aktivizēšana.</span><span class="sxs-lookup"><span data-stu-id="069d9-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="069d9-114">Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="069d9-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="069d9-115">Savā programmas Finance and Operations instancē veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="069d9-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="069d9-116">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="069d9-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="069d9-117">Ja jūsu uzņēmumā nav nodrošināta neviena RCS vide, atlasiet **Regulatory services — Configuration** un izpildiet norādījumus, lai tādu nodrošinātu.</span><span class="sxs-lookup"><span data-stu-id="069d9-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="069d9-118">Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapas vietrādi URL, lai piekļūtu videi, atlasot pierakstīšanās opciju.</span><span class="sxs-lookup"><span data-stu-id="069d9-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="069d9-119">Globalizācijas līdzekļu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="069d9-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="069d9-120">Savā RCS instancē atlasiet elementu **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="069d9-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="069d9-121">Darbvietā **Līdzekļu pārvaldība** sarakstā atlasiet **Globalizācijas līdzekļi** un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="069d9-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globalizācijas līdzekļi līdzekļu pārvaldībā](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="069d9-123">Globalizācijas līdzekļi</span><span class="sxs-lookup"><span data-stu-id="069d9-123">Globalization features</span></span>

<span data-ttu-id="069d9-124">Lai izmantotu globalizācijas līdzekli, vispirms tas ir jāimportē no globālā repozitorija un jāizveido tā sava versija.</span><span class="sxs-lookup"><span data-stu-id="069d9-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="069d9-125">Ir divi veidi, kā pievienot globalizācijas līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="069d9-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="069d9-126">Pievienot atvasinātu līdzekli, kas ir balstīts uz esošu līdzekli, kurš ir publicēts vai koplietots.</span><span class="sxs-lookup"><span data-stu-id="069d9-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="069d9-127">Pievienot jaunu līdzekli, ko esat izveidojis pilnībā izveidojis pats.</span><span class="sxs-lookup"><span data-stu-id="069d9-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="069d9-128">Piekļuve globalizācijas līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="069d9-128">Access Globalization features</span></span>

1. <span data-ttu-id="069d9-129">Pārliecinieties, ka līdzeklis **Globalizācijas līdzekļi** ir ieslēgts līdzekļu pārvaldībā, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="069d9-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="069d9-130">Atveriet jauno darbvietu **Globalizācijas līdzekļi** un pēc tam sadaļā **Līdzekļi** atlasiet elementu **e-rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="069d9-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Globālo līdzekļu darbvieta](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="069d9-132">Tiek atvērta lapa **Elektroniskās rēķinu izrakstīšanas līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="069d9-132">The **e-Invoicing Features** page is opened.</span></span>

    ![E-rēķinu izrakstīšanas līdzekļu lapa](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="069d9-134">Atvasināta globalizācijas līdzekļa pievienošana</span><span class="sxs-lookup"><span data-stu-id="069d9-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="069d9-135">Varat pievienot jaunu globalizācijas līdzekli, atvasinot to no esoša līdzekļa, kas ir publicēts vai koplietots.</span><span class="sxs-lookup"><span data-stu-id="069d9-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="069d9-136">Atlasiet **Importēt**, lai atvērtu lapu **Importēšanas līdzeklis no globālā repozitorija**.</span><span class="sxs-lookup"><span data-stu-id="069d9-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Līdzekļa importēšana no globālā repozitorija lapas](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="069d9-138">Atlasiet **Sinhronizēt**, lai iegūtu jaunākos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="069d9-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="069d9-139">Sinhronizētajā sarakstā ir iekļauti līdzekļi, kas ir pieejami tāpēc, ka tos ir publicējusi korporācija Microsoft, vai arī tie tikuši koplietoti ar citu konfigurācijas nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="069d9-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Līdzekļu sinhronizētais saraksts](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="069d9-141">Sarakstā atlasiet importējamos līdzekļus un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="069d9-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="069d9-142">Jūs saņemsit ziņojumu, kad atlasītie līdzekļi ir sekmīgi importēti.</span><span class="sxs-lookup"><span data-stu-id="069d9-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Ziņojums par sekmīgu importēšanu](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="069d9-144">Atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Pamatojoties uz esošu versiju**.</span><span class="sxs-lookup"><span data-stu-id="069d9-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="069d9-145">Ievadiet līdzekļa nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="069d9-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="069d9-146">Pieejamo līdzekļu sarakstā atlasiet līdzekļa pamatversiju un pēc tam atlasiet **Izveidot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="069d9-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Atvasināta līdzekļa pievienošana](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="069d9-148">Pievienotais līdzeklis ir izveidots, un tam ir statuss **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="069d9-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Atvasinātais līdzeklis, kam ir melnraksta statuss](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="069d9-150">Pārskatiet līdzekļa komponentus, lai noteiktu, vai ir nepieciešami atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="069d9-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="069d9-151">Pārskatiet konfigurācijas, ja ir jāpielāgo elektronisko pārskatu (ER) formāti un to saistījums ar formāta kartējumiem līdzekļa versijai.</span><span class="sxs-lookup"><span data-stu-id="069d9-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="069d9-152">Pārskatiet iestatījumus gadījumā, ja līdzekļa versijai ir jāpielāgo cilne **Darbības**, cilne **Piemērojamības kārtulas** vai cilne **Mainīgie**.</span><span class="sxs-lookup"><span data-stu-id="069d9-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="069d9-153">Cilnē **Versijas** atlasiet datumu **Spēkā no** un ievadiet aprakstu, ja lauks **Apraksts** ir tukšs.</span><span class="sxs-lookup"><span data-stu-id="069d9-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="069d9-154">Atlasiet **Mainīt statusu**, lai pabeigtu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="069d9-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="069d9-155">Pabeigtos līdzekļus var padarīt pieejamus noteiktai videi, lai tos varētu izmantot globalizācijas pakalpojumos, vai arī tos var publicēt globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="069d9-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="069d9-156">Līdzekļi, kuriem ir vērtība **Līdzekļa versijas statuss** sadaļā **Publicēts**, var tikt koplietoti ar ārējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="069d9-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="069d9-157">Jauna globalizācijas līdzekļa pievienošana</span><span class="sxs-lookup"><span data-stu-id="069d9-157">Add a new Globalization feature</span></span>

<span data-ttu-id="069d9-158">Varat pievienot jaunu globalizācijas līdzekli, izveidojot to pilnībā pats.</span><span class="sxs-lookup"><span data-stu-id="069d9-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="069d9-159">Lapā **Importēt no globālā repozitorija** atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Jauns līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="069d9-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="069d9-160">Ievadiet līdzekļa nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="069d9-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="069d9-161">Atlasiet **Izveidot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="069d9-161">Select **Create feature**.</span></span>

    ![Jauna līdzekļa pievienošana](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="069d9-163">Cilnē **Versijas** atlasiet datumu **Spēkā no** un pēc tam atlasiet **Mainīt statusu**, lai pabeigtu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="069d9-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="069d9-164">Pabeigtos līdzekļus var padarīt pieejamus noteiktai videi, lai tos varētu izmantot globalizācijas pakalpojumos, vai arī tos var publicēt globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="069d9-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="069d9-165">Līdzekļi, kuriem ir vērtība **Līdzekļa versijas statuss** sadaļā **Publicēts**, var tikt koplietoti ar ārējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="069d9-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="069d9-166">Līdzekļu komponentu pārskats</span><span class="sxs-lookup"><span data-stu-id="069d9-166">Feature component overview</span></span>

<span data-ttu-id="069d9-167">Globalizācijas līdzekļiem ir vairāki komponenti.</span><span class="sxs-lookup"><span data-stu-id="069d9-167">Globalization features have several components:</span></span>

- <span data-ttu-id="069d9-168">**Versija** — šis komponents atbalsta līdzekļu dzīves cikla pārvaldību un ļauj lietotājiem pārvaldīt statusu dažādām līdzekļa versijām.</span><span class="sxs-lookup"><span data-stu-id="069d9-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="069d9-169">**Konfigurācijas** — šis komponents ļauj lietotājiem pārvaldīt, skatīt un rediģēt saistītos ER formātus un formatēt kartējumus.</span><span class="sxs-lookup"><span data-stu-id="069d9-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="069d9-170">**Iestatījumi** — šis komponents ļauj globalizācijas pakalpojumu lietotājiem, piemēram, e-rēķinu pakalpojumam, pārvaldīt saistītā līdzekļa versijas iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="069d9-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="069d9-171">Tādēļ tas atbalsta elastīgu komunikācijas uzbūvi un atbildes noteikumus.</span><span class="sxs-lookup"><span data-stu-id="069d9-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="069d9-172">**Vide** — šis komponents ļauj globalizācijas pakalpojumu lietotājiem, piemēram, e-rēķinu izsniegšanas pakalpojumam, pārvaldīt vidi, kurā tiek izmantots līdzekļu versijas iestatījums, un piešķirt autorizāciju lietotājiem, kuriem tai būs piekļuve.</span><span class="sxs-lookup"><span data-stu-id="069d9-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="069d9-173">**Organizācijas** — šis komponents ļauj lietotājiem koplietot šo līdzekli ar ārējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="069d9-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="069d9-174">Līdzekļu komponentu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="069d9-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="069d9-175">Versija un statuss</span><span class="sxs-lookup"><span data-stu-id="069d9-175">Version and status</span></span>

<span data-ttu-id="069d9-176">Versija tiek izmantota, lai pārvaldītu globalizācijas līdzekļa dzīves ciklu.</span><span class="sxs-lookup"><span data-stu-id="069d9-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="069d9-177">Statusu var mainīt cilnes **Versija** laukā **Statuss**. Ir pieejami tālāk minētie statusi.</span><span class="sxs-lookup"><span data-stu-id="069d9-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="069d9-178">**Melnraksts** — līdzekli var rediģēt tikai tad, ja tas ir šajā statusā.</span><span class="sxs-lookup"><span data-stu-id="069d9-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="069d9-179">**Pabeigts** — līdzeklis un visi saistītie komponenti ir finalizēti (pabeigti), un tos nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="069d9-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="069d9-180">**Publicēts** — līdzeklis un visi saistītie komponenti ir publicēti globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="069d9-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="069d9-181">**Koplietots** — līdzeklis un visi saistītie komponenti ir koplietoti ar ārējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="069d9-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="069d9-182">**Iespējots** — līdzeklis un visi saistītie komponenti ir iespējoti izmantošanai globalizācijas pakalpojumā, piemēram, e-rēķinu izrakstīšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="069d9-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="069d9-183">Līdzekļi ir secīgi jāpārvieto, izmantojot dažus no šiem statusiem.</span><span class="sxs-lookup"><span data-stu-id="069d9-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="069d9-184">Tāpēc ne katrs statuss var būt pieejams visos dzīves cikla posmos.</span><span class="sxs-lookup"><span data-stu-id="069d9-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="069d9-185">Konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="069d9-185">Configurations</span></span>

<span data-ttu-id="069d9-186">Konfigurēšanai ir pieejamas tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="069d9-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="069d9-187">**Skatīt** — skatīt pakārtoto līdzekļu konfigurācijas, kurām nav nepieciešams atjauninājums.</span><span class="sxs-lookup"><span data-stu-id="069d9-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="069d9-188">**Rediģēt** — izveidojiet atlasītās konfigurācijas melnraksta versiju, lai varētu rediģēt formātu vai formatēt kartējumu formāta noformētājā.</span><span class="sxs-lookup"><span data-stu-id="069d9-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="069d9-189">**Dzēst** — dzēst atlasīto konfigurāciju no līdzekļa.</span><span class="sxs-lookup"><span data-stu-id="069d9-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="069d9-190">**Pārskatīt** — pārskatīt līdzekli.</span><span class="sxs-lookup"><span data-stu-id="069d9-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="069d9-191">Papildinformāciju skatiet šīs tēmas nākamajā sadaļā [Atvasināto globalizācijas līdzekļu pārskatīšana](#rebase).</span><span class="sxs-lookup"><span data-stu-id="069d9-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="069d9-192">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="069d9-192">Setups</span></span>

<span data-ttu-id="069d9-193">Līdzekļa iestatīšanai ir pieejamas tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="069d9-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="069d9-194">**Pievienot** — izveidot jaunu līdzekļa iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="069d9-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="069d9-195">Šo līdzekļa iestatījumu var atvasināt no esoša līdzekļu iestatījuma vai izveidot to no nulles.</span><span class="sxs-lookup"><span data-stu-id="069d9-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="069d9-196">**Dzēst** — dzēst atlasīto līdzekļa iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="069d9-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="069d9-197">**Skatīt** — skatīt pakārtoto līdzekļa iestatījumu, kam nav nepieciešamas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="069d9-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="069d9-198">**Rediģēt** — izveidot, dzēst vai modificēt līdzekļa iestatījuma trīs galveno komponentu atribūtus.</span><span class="sxs-lookup"><span data-stu-id="069d9-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="069d9-199">Darbības un to parametri</span><span class="sxs-lookup"><span data-stu-id="069d9-199">Actions and their parameters</span></span>
    - <span data-ttu-id="069d9-200">Piemērojamības kārtulas</span><span class="sxs-lookup"><span data-stu-id="069d9-200">Applicability rules</span></span>
    - <span data-ttu-id="069d9-201">Mainīgie</span><span class="sxs-lookup"><span data-stu-id="069d9-201">Variables</span></span>

![Līdzekļa versijas iestatīšanas lapa](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="069d9-203">Vides</span><span class="sxs-lookup"><span data-stu-id="069d9-203">Environments</span></span>

<span data-ttu-id="069d9-204">Vidēm ir pieejamas tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="069d9-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="069d9-205">**Iespējot** — atlasītajai līdzekļa versijai atlasiet publicēto vidi un atlasiet datumu **Spēkā no**, kad tam jābūt pieejamam.</span><span class="sxs-lookup"><span data-stu-id="069d9-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="069d9-206">Papildinformāciju skatiet šīs tēmas nākamajā sadaļā [Vižu konfigurēšana iespējošanai](#configureenvironment).</span><span class="sxs-lookup"><span data-stu-id="069d9-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="069d9-207">**Atcelt** — noņemt vidi līdzekļa iestatījumam.</span><span class="sxs-lookup"><span data-stu-id="069d9-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="069d9-208">Organizācijas</span><span class="sxs-lookup"><span data-stu-id="069d9-208">Organizations</span></span>

<span data-ttu-id="069d9-209">Izpildiet tālāk minētās darbības, lai koplietotu globalizācijas līdzekli ar ārēju organizāciju.</span><span class="sxs-lookup"><span data-stu-id="069d9-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="069d9-210">Lapā **e-rēķina līdzekļi** atlasiet līdzekli un līdzekļa versiju, kuru koplietot.</span><span class="sxs-lookup"><span data-stu-id="069d9-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="069d9-211">Cilnē **Organizācijas** atlasiet **Koplietot ar** un pēc tam nolaižamajā dialoglodziņā ievadiet organizācijas domēna nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="069d9-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="069d9-212">Atlasiet **Koplietot**.</span><span class="sxs-lookup"><span data-stu-id="069d9-212">Select **Share**.</span></span>

    ![Līdzekļa koplietošana ar organizāciju](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="069d9-214">Līdzeklis tiek koplietots ar atlasīto organizāciju un ir pieejams šai organizācijai globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="069d9-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="069d9-215">No turienes līdzekli var importēt RCS organizācijas instancē vai Dynamics 365 Finance tā, lai to varētu izmantot.</span><span class="sxs-lookup"><span data-stu-id="069d9-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="069d9-216">Atvasināto globalizācijas līdzekļu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="069d9-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="069d9-217">Atvasināto globalizācijas līdzekli varat pārskatīt uz jaunu vai atjauninātu bāzes līdzekļu versiju.</span><span class="sxs-lookup"><span data-stu-id="069d9-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="069d9-218">Šādā veidā izmaiņas, kas notikušas bāzes versijā, var tikt automātiski atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="069d9-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="069d9-219">Atjaunināto bāzes līdzekļa versiju izveido sākotnējais konfigurācijas nodrošinātājs, un tā tiek publicēta vai koplietota.</span><span class="sxs-lookup"><span data-stu-id="069d9-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Atjauninātā bāzes līdzekļa versija](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="069d9-221">Piemēram, ja vēlaties pārskatīt jūsu izveidotā līdzekļa atvasināto versiju, vispirms iegūstiet līdzekļa jaunāko versiju, importējot to no globālā repozitorija.</span><span class="sxs-lookup"><span data-stu-id="069d9-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="069d9-222">Lapā **e-rēķina līdzekļi** atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="069d9-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="069d9-223">Atlasiet **Sinhronizēt**, lai iegūtu jaunākos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="069d9-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="069d9-224">Līdzekļu sarakstā atlasiet importējamos līdzekļus un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="069d9-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Līdzekļa jaunākās versijas importēšana](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="069d9-226">Līdzekļu sarakstā atlasiet līdzekli, kas jāpārskata.</span><span class="sxs-lookup"><span data-stu-id="069d9-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="069d9-227">Cilnē **Versija** atlasiet **Jauns**, lai izveidotu melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="069d9-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Izveidota jauna melnraksta versija](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="069d9-229">Atlasiet **Pārskatīt**.</span><span class="sxs-lookup"><span data-stu-id="069d9-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="069d9-230">Dialoglodziņā **Pārskatīt** atlasiet jaunāko līdzekļa versiju, uz kuru to pārveidot.</span><span class="sxs-lookup"><span data-stu-id="069d9-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Dialoglodziņš Pārskatīt](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="069d9-232">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="069d9-232">Select **OK**.</span></span>
9. <span data-ttu-id="069d9-233">Pārskatiet līdzekļa komponentus un veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="069d9-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="069d9-234">Atlasiet **Mainīt statusu**, lai pabeigtu pārskatīto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="069d9-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="069d9-235">Kad pārskatīšana ir pabeigta, varat veikt papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="069d9-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="069d9-236">Piemēram, varat publicēt līdzekli un padarīt to pieejamu izmantošanai globalizācijas pakalpojumos.</span><span class="sxs-lookup"><span data-stu-id="069d9-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Līdzekļa statuss atjaunināts uz Pabeigts](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="069d9-238">Vižu konfigurēšana globalizācijas līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="069d9-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="069d9-239">Globalizācijas pakalpojumu lietotāji var pārvaldīt vidi, lai iestatītu globalizācijas līdzekli un piešķirtu autorizāciju citiem lietotājiem, kuriem tam būs piekļuve.</span><span class="sxs-lookup"><span data-stu-id="069d9-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="069d9-240">Darbvietā **Globalizācijas līdzekļi** zem **Vides** atlasiet elementu **e-rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="069d9-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Globalizācijas līdzekļu darbvieta](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="069d9-242">Atlasiet **Key Vault parametrus** un pēc tam atlasiet **Jauns**, lai izveidotu Azure Key Vault noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="069d9-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="069d9-243">Ievadiet Key Vault aprakstu un pēc tam laukā **Key Vault URI** ievadiet vietrādi URL, kas identificē Key Vault resursu Azure.</span><span class="sxs-lookup"><span data-stu-id="069d9-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="069d9-244">Kopsavilkuma cilnē **Sertifikāti** atlasiet **Pievienot**, lai pievienotu sertifikātu, un ievadiet katra sertifikāta nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="069d9-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Sertifikāts pievienots](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="069d9-246">Atlasiet **Jauns**, lai izveidotu jaunu vidi.</span><span class="sxs-lookup"><span data-stu-id="069d9-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="069d9-247">Ievadiet krātuvei nepieciešamo nosaukumu, aprakstu un koplietojamo piekļuves paraksta marķieri.</span><span class="sxs-lookup"><span data-stu-id="069d9-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="069d9-248">Kopsavilkuma cilnā **Lietotāji** atlasiet **Jauns**, lai pievienotu lietotāju, kuram būs atļauja piekļūt šai videi.</span><span class="sxs-lookup"><span data-stu-id="069d9-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="069d9-249">Ievadiet lietotāja ID un e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="069d9-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="069d9-250">Atkārtojiet 7. un 8. darbību, lai pievienotu vairāk lietotāju.</span><span class="sxs-lookup"><span data-stu-id="069d9-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="069d9-251">Atlasiet **Publicēt**, lai publicētu vidi.</span><span class="sxs-lookup"><span data-stu-id="069d9-251">Select **Publish** to publish the environment.</span></span>

    ![Publicētā vide](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
