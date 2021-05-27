---
title: Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ
description: Šajā tēmā sniegtas atbildes uz bieži uzdotajiem jautājumiem par Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019474"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="67382-103">Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ</span><span class="sxs-lookup"><span data-stu-id="67382-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67382-104">Šajā tēmā sniegtas atbildes uz bieži uzdotajiem jautājumiem par Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.</span><span class="sxs-lookup"><span data-stu-id="67382-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="67382-105">Kurš veikalā kļūst par grupas īpašnieku, nodrošināt Teams no Commerce?</span><span class="sxs-lookup"><span data-stu-id="67382-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="67382-106">Visi veikala vadītāji automātiski tiek pievienoti atbilstošajai komandas grupai kā īpašnieki, lai tie varētu veikt tādas darbības kā privāta kanāla pievienošana un dalībnieku pievienošana vai dzēšana.</span><span class="sxs-lookup"><span data-stu-id="67382-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="67382-107">Kā programmā Commerce Headquarters darbiniekam piešķirt lomu "sakaru pārvaldnieks"?</span><span class="sxs-lookup"><span data-stu-id="67382-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="67382-108">Komunikācijas vadītāji var Microsoft Teams izveidot un publicēt uzdevumu sarakstus.</span><span class="sxs-lookup"><span data-stu-id="67382-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="67382-109">Organizācijas darbiniekiem, kuriem ir jākļūst par sakaru pārvaldniekiem, programmā Commerce headquarters ir jābūt piešķirtai lomai "Mazumtirdzniecības uzdevumu pārvaldnieks".</span><span class="sxs-lookup"><span data-stu-id="67382-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="67382-110">Lai piešķirtu mazumtirdzniecības uzdevumu pārvaldnieka lomu darbiniekam programmā Commerce Headquarters, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="67382-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="67382-111">Dodieties uz **Retail un Commerce \> Nodarbinātie \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="67382-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="67382-112">Atlasiet darbinieku.</span><span class="sxs-lookup"><span data-stu-id="67382-112">Select an employee.</span></span>
1. <span data-ttu-id="67382-113">Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**.</span><span class="sxs-lookup"><span data-stu-id="67382-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="67382-114">Dialoglodziņā lomu **Piešķirt lomas lietotājam** atlasiet lomu **Mazumtirdzniecības uzdevumu vadītājs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="67382-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="67382-115">Kā var izveidot noteiktu organizācijas hierarhiju, kurā veikt Microsoft Teams augšupielādi?</span><span class="sxs-lookup"><span data-stu-id="67382-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="67382-116">Programmā Commerce Headquarters katra organizācijas hierarhija ir saistīta ar vienu vai vairākiem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="67382-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="67382-117">Pārliecinieties, ka ar hierarhiju, kuru vēlaties nodrošināt Microsoft Teams ir saistīts ar **Mazumtirdzniecības pārskatu** mērķi, kā parādīts nākamajā piemēra attēlā.</span><span class="sxs-lookup"><span data-stu-id="67382-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Organizācijas hierarhijas nolūka piemērs programmā Commerce Headquarters](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="67382-119">Kā iespējot mazumtirdzniecības veikala darbinieku pieteik anos Commerce Point Of Sale (POS) izmantojot Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="67382-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="67382-120">Informāciju par to, kā konfigurēt Commerce POS pierakstīšanās pieredzi autentifikācijas lietošanai Azure AD, skatiet sadaļā [Iespējot Azure Active Directory, autentifikāciju, lai pierakstītos POS](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="67382-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="67382-121">Kā kartēt veikalus un atbilstošās grupas programmā Commerce Headquarters, ja mana organizācija jau ir izveidojusi Microsoft Teams grupas?</span><span class="sxs-lookup"><span data-stu-id="67382-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="67382-122">Informāciju par veikalu un grupu kartēšanu, ja pastāv iepriekšējas darba grupas, skatiet sadaļā Kartēt veikalus un atbilstošās darba grupas, ja uzņēmumā ir [iepriekš esošas darba grupas Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="67382-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="67382-123">Kā notīrīt Microsoft Graph API marķieri, kas saglabāts sesijas krātuvē?</span><span class="sxs-lookup"><span data-stu-id="67382-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="67382-124">Lietotājam, kurš ir pieteicies pārdošanas punktā (POS), izmantojot Azure Active Directory (Azure AD) kontu, ir jāizrakstās no POS vai jāaizver programma, lai notīrītu sesijas krātuvi.</span><span class="sxs-lookup"><span data-stu-id="67382-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="67382-125">Ieteicams ieteicams vienmēr saglabāt darbiniekus, kas bloķē POS termināli vai izrakstīties no sesijas, ja netiek izmantots terminālis.</span><span class="sxs-lookup"><span data-stu-id="67382-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="67382-126">Kas notiek, ja veikalā nav veikala pārvaldnieku?</span><span class="sxs-lookup"><span data-stu-id="67382-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="67382-127">Ja veikalam nav pārvaldnieku, veikalam vai Teams grupām netiks izveidota grupa.</span><span class="sxs-lookup"><span data-stu-id="67382-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="67382-128">Kas notiek, ja veikala vadītājs atstāj uzņēmumu?</span><span class="sxs-lookup"><span data-stu-id="67382-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="67382-129">Ikviens, kam ir īpašnieka loma, var pievienot jaunu veikala pārvaldnieku programmā Commerce Headquarters un nodrošināt Teams, lai jaunajam vadītājam būtu nepieciešamās grupas Teams privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="67382-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="67382-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="67382-130">Additional resources</span></span>

[<span data-ttu-id="67382-131">Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="67382-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="67382-132">Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="67382-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="67382-133">Nodrošināt Microsoft Teams no Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="67382-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="67382-134">Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="67382-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="67382-135">Lietotāju lomu pārvaldība Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="67382-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="67382-136">Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="67382-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
