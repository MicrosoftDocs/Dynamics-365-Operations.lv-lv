---
title: Microsoft Teams nodrošināšana no Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīts, kā nodrošināt Microsoft Teams, izmantojot organizācijas Dynamics 365 Commerce datus.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908908"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="e0b16-103">Microsoft Teams nodrošināšana no Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e0b16-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e0b16-104">Šajā tēmā ir aprakstīts, kā nodrošināt Microsoft Teams, izmantojot organizācijas Dynamics 365 Commerce datus.</span><span class="sxs-lookup"><span data-stu-id="e0b16-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e0b16-105">Dynamics 365 Commerce piedāvā ērtu veidu, kā nodrošināt Teams, ja vēl neesat iestatījis grupas saviem mazumtirdzniecības veikaliem.</span><span class="sxs-lookup"><span data-stu-id="e0b16-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="e0b16-106">Izmantojot pareizi definētas informācijas priekšrocības no Commerce, ko vēlaties izmantot programmā Teams, varat palīdzēt veikala darbiniekiem sākt darbu Teams.</span><span class="sxs-lookup"><span data-stu-id="e0b16-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="e0b16-107">Šajā informācijā ir iekļauta organizācijas hierarhija, veikalu nosaukumi, darbinieku informācija un Azure Active Directory (Azure AD) konti.</span><span class="sxs-lookup"><span data-stu-id="e0b16-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="e0b16-108">Teams nodrošinājuma procesam ir divas galvenās darbības:</span><span class="sxs-lookup"><span data-stu-id="e0b16-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="e0b16-109">Programmā Teams izveidojiet grupu katram mazumtirdzniecības veikalam un pievienojiet veikala darbiniekus kā atbilstošās grupas dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="e0b16-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="e0b16-110">Ja darbinieks ir saistīts ar vairāk nekā vienu mazumtirdzniecības veikalu, šo faktu atspoguļos grupas dalība.</span><span class="sxs-lookup"><span data-stu-id="e0b16-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="e0b16-111">Tiks izveidota sakaru grupa, kurā iekļauti reģionālie vadītāji kā dalībnieki, lai palīdzētu publicēt uzdevumus no Teams.</span><span class="sxs-lookup"><span data-stu-id="e0b16-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="e0b16-112">Augšupielādējiet organizācijas hierarhiju no Commerce uz Teams.</span><span class="sxs-lookup"><span data-stu-id="e0b16-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="e0b16-113">Nodrošināt Teams Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="e0b16-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="e0b16-114">Pirms Microsoft Teams nodrošināšanas izpildiet šos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="e0b16-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="e0b16-115">Apstipriniet, ka visi reģionālie vadītāji ir pazinuši sakaru vadītājus.</span><span class="sxs-lookup"><span data-stu-id="e0b16-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="e0b16-116">Apstipriniet, ka katra veikala vadītāja un darbinieka Azure konts ir saistīts ar šī vadītāja vai darbinieka darbinieka ierakstu programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="e0b16-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="e0b16-117">Lai nodrošinātu programmu Teams komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e0b16-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e0b16-118">Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="e0b16-119">Darbību rūtī atlasiet **Grupu nodrošināšana**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="e0b16-120">Ir izveidots pakešuzdevums ar nosaukumu **Grupu nodrošināšana**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="e0b16-121">Dodieties uz **Sistēmas administrēšana \> Uzziņas \> Pakešdarbi** un atrodiet pēdējo darbu ar aprakstu **Teams nodrošināšana**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="e0b16-122">Uzgaidiet, kamēr šis darbs tiks pabeigts.</span><span class="sxs-lookup"><span data-stu-id="e0b16-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="e0b16-123">Ja neviens no jūsu reģionālajiem vadītājiem, veikalu vadītājiem un veikala darbiniekiem nav saistīts ar brigādes licenci, varat saņemt šādu kļūdas ziņojumu: "Neizdevās izgūt lietotājam atbildīgās sku kategorijas."</span><span class="sxs-lookup"><span data-stu-id="e0b16-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="e0b16-124">Lai labotu problēmu, darbību rūtī atlasiet **Sinhronizēt grupas un dalībniekus**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="e0b16-125">Pārbaudīt Teams nodrošinājumu Teams administrēšanas centrā</span><span class="sxs-lookup"><span data-stu-id="e0b16-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="e0b16-126">Lai apstiprinātu Microsoft Teams nodrošināšanu Microsoft Teams administrēšanas centrā, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="e0b16-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="e0b16-127">Dodieties uz [Teams administrēšanas centru](https://admin.teams.microsoft.com/) un piesakieties kā sava e-komercijas nomnieka administrators.</span><span class="sxs-lookup"><span data-stu-id="e0b16-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="e0b16-128">Kreisajā navigācijas rūtī atlasiet **Teams**, lai to izvērstu, un pēc tam atlasiet **Pārvaldīt grupas**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="e0b16-129">Pārliecinieties, vai katram Commerce mazumtirdzniecības veikalam ir izveidota viena grupa.</span><span class="sxs-lookup"><span data-stu-id="e0b16-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="e0b16-130">Atlasiet grupu un apstipriniet, ka veikala darbinieki ir tai pievienoti kā dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="e0b16-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="e0b16-131">Kreisajā navigācijas rūtī atlasiet **Lietotāji** un apstipriniet, ka visi veikala darbinieki visos veikalos ir pievienoti kā lietotāji.</span><span class="sxs-lookup"><span data-stu-id="e0b16-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="e0b16-132">Šajā attēlā parādīts **Grupu pārvaldības** lapas piemērs Teams administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="e0b16-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Grupu pārvaldības lapas piemērs Grupu administrēšanas centrā](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="e0b16-134">Augšupielādējiet organizācijas hierarhiju no Commerce uz Teams</span><span class="sxs-lookup"><span data-stu-id="e0b16-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="e0b16-135">Commerce organizācijas hierarhiju var izmantot, lai publicētu uzdevumus visos vai atlasītajiem Microsoft Teams veikaliem, kas izmanto vienādu hierarhijas struktūru.</span><span class="sxs-lookup"><span data-stu-id="e0b16-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="e0b16-136">Lai augšupielādētu Commerce organizācijas hierarhiju uz Teams, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e0b16-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="e0b16-137">Dodieties uz **Mazumtirdzniecība un komercija \> Kanālu iestatījumi \> Microsoft Teams integrācijas konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="e0b16-138">Atlasiet **Lejupielādes mērķa hierarhija** un pēc tam atlasiet **Mazumtirdzniecības veikali pēc reģiona**, lai lejupielādētu komatatdalīto vērtību (CSV) failu organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="e0b16-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="e0b16-139">Instalējiet Microsoft Teams PowerShell moduli, izpildot norādītās darbības sadaļā [Microsoft Teams Power Shell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="e0b16-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="e0b16-140">Kad tiek parādīta uzvedne Teams PowerShell logā, piesakieties, nomniekam izmantojot Azure AD administratora kontu.</span><span class="sxs-lookup"><span data-stu-id="e0b16-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="e0b16-141">Sekojiet soļiem sadaļā [Iestatīt savas grupas mērķa hierarhiju](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy), lai augšupielādētu CSV failu mērķa hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="e0b16-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="e0b16-142">Pārbaudiet, vai organizācijas hierarhija tika augšupielādēta Teams</span><span class="sxs-lookup"><span data-stu-id="e0b16-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="e0b16-143">Pārbaudiet, vai organizācijas hierarhija tika augšupielādēta Microsoft Teams, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="e0b16-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="e0b16-144">Piesakieties Teams kā saziņas pārvaldītājs.</span><span class="sxs-lookup"><span data-stu-id="e0b16-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="e0b16-145">Navigācijas rūtī pa kreisi atlasiet **Uzdevumi pēc plānotāja**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="e0b16-146">Cilnē **Publicētie saraksti** izveidojiet jaunu sarakstu, kam ir fiktīvs uzdevums.</span><span class="sxs-lookup"><span data-stu-id="e0b16-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="e0b16-147">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e0b16-147">Select **Publish**.</span></span> <span data-ttu-id="e0b16-148">Organizācijas hierarhijai ir jābūt parādītai dialoglodziņā **Atlasīt, kas tiks publicēts**, kā parādīts piemērā šajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="e0b16-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Organizācijas hierarhijas piemērs dialoglodziņā Atlasīt, kas tiks publicēts](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="e0b16-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e0b16-150">Additional resources</span></span>

[<span data-ttu-id="e0b16-151">Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="e0b16-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="e0b16-152">Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="e0b16-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="e0b16-153">Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="e0b16-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="e0b16-154">Lietotāju lomu pārvaldība Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e0b16-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="e0b16-155">Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e0b16-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="e0b16-156">Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ</span><span class="sxs-lookup"><span data-stu-id="e0b16-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
