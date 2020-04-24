---
title: Iespējot Azure Active Directory autentifikāciju, lai pierakstītos POS
description: Šajā tēmā paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) pierakstīšanās pieredzi, lai tā izmantotu Azure Active Directory autentifikāciju.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248944"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="8e29f-103">Iespējot Azure Active Directory autentifikāciju, lai pierakstītos POS</span><span class="sxs-lookup"><span data-stu-id="8e29f-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="8e29f-104">Daudzi klienti, kuri lieto Microsoft Dynamics 365 Commerce, izmanto arī citus Microsoft mākoņpakalpojumu pakalpojumus, un viņi var izmantot Azure Active Directory (Azure AD), lai pārvaldītu lietotāju akreditācijas datus šiem pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="8e29f-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="8e29f-105">Šādos gadījumos klienti varētu vēlēties izmantot vienu un to pašu Azure AD kontu dažādās lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="8e29f-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="8e29f-106">Šajā tēmā paskaidrots, kā konfigurēt Commerce pārdošanas punkta (POS) pierakstīšanās pieredzi, lai izmantotu Azure AD autentifikāciju.</span><span class="sxs-lookup"><span data-stu-id="8e29f-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="8e29f-107">Azure AD autentifikācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8e29f-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="8e29f-108">Lai padarītu Azure AD pieejamu kā autentifikācijas metodi POS pierakstīšanās sistēmai veikalā, ir jākonfigurē veikala funkcionalitātes profila iestatījumi un pēc tam šie iestatījumi jāpiemēro POS klientiem.</span><span class="sxs-lookup"><span data-stu-id="8e29f-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="8e29f-109">Lai konfigurētu funkcionalitātes profilu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8e29f-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="8e29f-110">Dodieties uz sadaļu **Retail un Commerce** \> **Kanāla iestatīšana** \> **POS iestatīšana** \> **POS profili** \> **Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="8e29f-111">Atlasiet maināmo funkcionalitātes profilu.</span><span class="sxs-lookup"><span data-stu-id="8e29f-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="8e29f-112">Kopsavilkuma cilnes **Funkcijas** sadaļā **POS personāla pieteikšanās** mainiet lauka **Pieteikšanās autentifikācijas metodes** vērtību no **Personāla ID un parole** uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="8e29f-113">Pēc noklusējuma visi funkcionalitātes profili izmanto vērtību **Personāla ID un parole** kā POS autentifikācijas metodi.</span><span class="sxs-lookup"><span data-stu-id="8e29f-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="8e29f-114">Tāpēc ir jāmaina lauka **Pieteikšanās autentifikācijas metode** vērtība, ja vēlaties lietot Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8e29f-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="8e29f-115">Visus mazumtirdzniecības veikalus, kas ir saistīti ar izvēlēto funkcionalitātes profilu, ietekmēs šīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="8e29f-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="8e29f-116">Lai piemērotu iestatījumus POS klientiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="8e29f-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="8e29f-117">Pārejiet uz **Retail un Commerce** \> **Retail un Commerce IT** \> **Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="8e29f-118">Palaidiet sadales grafiku **1070** (**Kanāla konfigurācija**).</span><span class="sxs-lookup"><span data-stu-id="8e29f-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="8e29f-119">Azure AD autentifikācijai ir nepieciešams interneta savienojums.</span><span class="sxs-lookup"><span data-stu-id="8e29f-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="8e29f-120">Tā nedarbosies, ja POS būs bezsaistes režīmā.</span><span class="sxs-lookup"><span data-stu-id="8e29f-120">It won't work when POS is in offline mode.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="8e29f-121">Saistīt Azure AD kontu ar darbinieku</span><span class="sxs-lookup"><span data-stu-id="8e29f-121">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="8e29f-122">Pirms veikala darbinieks var izmantot Azure AD kontu, lai pieteiktos POS programmā, Azure AD kontam jābūt saistītam ar šo darbinieku.</span><span class="sxs-lookup"><span data-stu-id="8e29f-122">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="8e29f-123">Lai saistītu Azure AD kontu ar darbinieku, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8e29f-123">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="8e29f-124">Dodieties uz **Retail un Commerce** \> **Darbinieki** \> **Nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-124">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="8e29f-125">Atveriet darbinieka detalizētas informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="8e29f-125">Open the details page for a worker.</span></span>
1. <span data-ttu-id="8e29f-126">Darbību rūts cilnē **Commerce** grupā **Ārējā identitāte** atlasiet **Saistīt esošo identitāti**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-126">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="8e29f-127">Dialoglodziņā **Izmantot esošo ārējo identitāti** atlasiet opciju **Meklēt, izmantojot e-pastu**, ievadiet Azure AD e-pasta adresi un pēc tam atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-127">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="8e29f-128">Atlasiet Azure AD kontu, kas tiek atgriezts, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-128">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="8e29f-129">Darbinieka detalizētas informācijas lapas cilnē **Commerce** tiks ievadīti lauki **Aizstājvārds**, **UPN** un **Ārējais apakšidentifikators**.</span><span class="sxs-lookup"><span data-stu-id="8e29f-129">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e29f-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8e29f-130">Additional resources</span></span>

[<span data-ttu-id="8e29f-131">Paplašinātās pieteikšanās funkcionalitātes iestatīšana MPOS un Cloud POS</span><span class="sxs-lookup"><span data-stu-id="8e29f-131">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="8e29f-132">Izveidot mazumtirdzniecības funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="8e29f-132">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="8e29f-133"> Nodarbinātā konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8e29f-133">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
