---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d3f1fba05d944e78e4595018d190c3dc41e076
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907915"
---
# <a name="create-new-users"></a><span data-ttu-id="5db46-103">Jaunu lietotāju izveide</span><span class="sxs-lookup"><span data-stu-id="5db46-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5db46-104">Pirms varat piekļūt Finance and Operations programmām, vispirms jums jābūt pievienotam lapai **Lietotāji** (**Sistēmas administrēšana \> Lietotāji \> Lietotāji**).</span><span class="sxs-lookup"><span data-stu-id="5db46-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="5db46-105">Lietotāji ietver jūsu organizācijas iekšējos darbiniekus vai ārējos debitorus un kreditorus.</span><span class="sxs-lookup"><span data-stu-id="5db46-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="5db46-106">Lietotājus var manuāli importēt vai pievienot.</span><span class="sxs-lookup"><span data-stu-id="5db46-106">Users can be imported or added manually.</span></span> <span data-ttu-id="5db46-107">Visiem lietotājiem jābūt korekti licencētiem atbilstošai lietošanai.</span><span class="sxs-lookup"><span data-stu-id="5db46-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="5db46-108">Papildinformāciju par to, kā pirkt un licencēt Finance and Operations lietojumprogrammas, skatiet [Microsoft Dynamics 365 licencēšanas rokasgrāmatā](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="5db46-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="5db46-109">Piešķiriet licenci lietotājam</span><span class="sxs-lookup"><span data-stu-id="5db46-109">Assign a license to a user</span></span>
<span data-ttu-id="5db46-110">Sistēmas administratori var [piešķirt licences lietotājiem](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 administrēšanas centrā](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="5db46-110">System admins can [assign licenses to users](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="5db46-111">Ārēja lietotāja pievienošana Azure AD un licences piešķiršana</span><span class="sxs-lookup"><span data-stu-id="5db46-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="5db46-112">Ārējiem lietotājiem jābūt norādītiem savā nomnieka direktorijā (Azure Active Directory (Azure AD)), lai tiem varētu piešķirt licences.</span><span class="sxs-lookup"><span data-stu-id="5db46-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="5db46-113">Šie ārējie lietotāji jāpievieno nomniekam Azure AD kā vieslietotāji un pēc tam jāpiešķir atbilstošās licences.</span><span class="sxs-lookup"><span data-stu-id="5db46-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="5db46-114">Finance and Operations programmām ir prasība, ka viesa lietotāja uzņēmumam ir jāizmanto Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5db46-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="5db46-115">Papildinformāciju skatiet [Pievienot Azure Active Directory B2B sadarbības lietotājus Azure portālā](/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="5db46-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="5db46-116">Jaunu lietotāju importēšana no Azure AD</span><span class="sxs-lookup"><span data-stu-id="5db46-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="5db46-117">Dodieties uz **Sistēmas administrēšana** \> **Lietotāji** \> **Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="5db46-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="5db46-118">Darbību rūtī atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="5db46-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="5db46-119">Atlasiet importējamos lietotājus.</span><span class="sxs-lookup"><span data-stu-id="5db46-119">Select the users to be imported.</span></span> <span data-ttu-id="5db46-120">Sarakstā ir iekļauti Azure AD lietotāji, kas pašlaik nav šīs vides lietotāji.</span><span class="sxs-lookup"><span data-stu-id="5db46-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="5db46-121">Atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="5db46-121">Select **Import users**.</span></span>
5. <span data-ttu-id="5db46-122">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="5db46-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="5db46-123">Lauka **Uzņēmums** vērtība tiks iestatīta, pamatojoties uz pašreizējo sesijas uzņēmumu administratoram. Pēc importēšanas jums jāpiešķir lomas un organizācijas pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="5db46-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="5db46-124">Plašāku informāciju skatiet [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="5db46-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="5db46-125">Ar nosacījumiem tas var būt pieprasīts arī, lai saistītu lietotāju ar **Personu** un atjauninātu lietotāja opcijas, piemēram, valodu.</span><span class="sxs-lookup"><span data-stu-id="5db46-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="5db46-126">Manuāli pievienot jaunu lietotāju</span><span class="sxs-lookup"><span data-stu-id="5db46-126">Manually add a new user</span></span>
1. <span data-ttu-id="5db46-127">Dodieties uz **Sistēmas administrēšana** \> **Lietotāji** \> **Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="5db46-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="5db46-128">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5db46-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="5db46-129">Laukā **Lietotāja ID** ievadiet lietotāja unikālu identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="5db46-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="5db46-130">Laukā **Lietotāja vārds** ievadiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="5db46-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="5db46-131">Laukā **Nodrošinātājs**:</span><span class="sxs-lookup"><span data-stu-id="5db46-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="5db46-132">Iekšējiem lietotājiem izmantojiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="5db46-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="5db46-133">Piemēram, Azure AD nomnieka prefikss https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="5db46-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="5db46-134">Kontiem, kasAzure AD nav lietotāji, piemēram, Service-2-Service, ievadiet pamatteksta vērtību.</span><span class="sxs-lookup"><span data-stu-id="5db46-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="5db46-135">Piemēram, NA.</span><span class="sxs-lookup"><span data-stu-id="5db46-135">For example, NA.</span></span> <span data-ttu-id="5db46-136">Šī vērtība palīdzēs izvairīties no nepareiziem autentifikācijas izsaukumi, kas var izraisīt kļūdas, ja tiek izmantota derīga identitātes nodrošinātāja vērtība.</span><span class="sxs-lookup"><span data-stu-id="5db46-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="5db46-137">Ārējiem vai viesa lietotājiem pievienojiet viņu Azure AD nomnieka vārdu pēc https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="5db46-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="5db46-138">Laukā **E-pasts** ievadiet pilnu lietotāja e-pasta/lietotāja principa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5db46-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="5db46-139">Laukā **Uzņēmums** atlasiet noklusējuma starta uzņēmumu lietotājam.</span><span class="sxs-lookup"><span data-stu-id="5db46-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="5db46-140">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5db46-140">Select **Save**.</span></span>

<span data-ttu-id="5db46-141">Identitātes nodrošinātāja un telemetrijas ID vērtības tiks atjauninātas, pamatojoties uz [Microsoft grafika](/graph/overview) izsaukumu, saglabājot lietotāja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5db46-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="5db46-142">Telemetrijas ID ir balstīts uz lietotāja objekta ID/drošības identifikatoru (SID) Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5db46-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="5db46-143">Pēc lietotāja pievienošanas jums jāpiešķir lomas un organizācijas pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="5db46-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="5db46-144">Plašāku informāciju skatiet [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="5db46-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="5db46-145">Ar nosacījumiem tas var būt pieprasīts arī, lai saistītu lietotāju ar **Personu** un atjauninātu **Lietotāja opcijas**, piemēram, valodu.</span><span class="sxs-lookup"><span data-stu-id="5db46-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="5db46-146">Lietotāja ID maiņa</span><span class="sxs-lookup"><span data-stu-id="5db46-146">Change a user ID</span></span>
<span data-ttu-id="5db46-147">Lai mainītu lietotāja ID, datu bāzē ir jāpārdēvē atslēga.</span><span class="sxs-lookup"><span data-stu-id="5db46-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="5db46-148">Ja, izmantojot šo procedūru, maināt lietotāja ID, visi saistītie lietotāja iestatījumi tiek modificēti tā, lai izmantotu jauno lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="5db46-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="5db46-149">Piemēram, lietojuma informācija tabulā **SysLastValue** tiek atjaunināta uz jauno lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="5db46-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="5db46-150">Lietotāja ID ir primārā lietotāja informācijas tabulas atslēga.</span><span class="sxs-lookup"><span data-stu-id="5db46-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="5db46-151">Primārās atslēgas pārdēvēšana var aizņemt kādu laiku esošiem lietotājiem, jo visas atsauces uz atslēgu arī tiek atjauninātas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="5db46-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="5db46-152">Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="5db46-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="5db46-153">Sarakstā atlasiet lietotāju un atlasiet **Opcijas\> Informācija par ierakstu**.</span><span class="sxs-lookup"><span data-stu-id="5db46-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="5db46-154">Atlasiet **Pārdēvēt**.</span><span class="sxs-lookup"><span data-stu-id="5db46-154">Select **Rename**.</span></span>
4. <span data-ttu-id="5db46-155">Ievadiet jaunu Lietotāja ID unikālo vērtību, tad atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5db46-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="5db46-156">Lai apstiprinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5db46-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5db46-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5db46-157">Additional resources</span></span>

<span data-ttu-id="5db46-158">Papildinformāciju par B2B lietotāju implementēšanu skatiet [sadaļā "Eksportēt B2B lietotājus uz Azure AD](../implement-b2b.md).</span><span class="sxs-lookup"><span data-stu-id="5db46-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="5db46-159">Informāciju par iepriekškonfigurētiem sistēmas kontiem skatiet [Iepriekš konfigurētos sistēmas kontus](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="5db46-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]