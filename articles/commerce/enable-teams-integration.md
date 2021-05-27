---
title: Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju
description: Šajā tēmā ir aprakstīts, kā aktivizēt Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.
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
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019839"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="cc973-103">Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="cc973-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc973-104">Šajā tēmā ir aprakstīts, kā aktivizēt Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.</span><span class="sxs-lookup"><span data-stu-id="cc973-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="cc973-105">Lai nodrošinātu Teams ar informāciju no Dynamics 365 Commerce un sinhronizētu uzdevumu pārvaldības līdzekļus starp Teams un pārdošanas punkta (POS) programmu, ir jāiespējo integrācijas līdzekļi programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cc973-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="cc973-106">Iespējojot Teams integrāciju, jūs atļaujat koplietot datus ar brigādes grupām.</span><span class="sxs-lookup"><span data-stu-id="cc973-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="cc973-107">Dati, kas tiek koplietoti ar Teams, var atrasties citā valstī, nevis jūsu Commerce datos, un uz tiem var būt attiecas atšķirīgi saskaņotības standarti.</span><span class="sxs-lookup"><span data-stu-id="cc973-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="cc973-108">Papildinformāciju par šīm izmaiņām skatiet sadaļā [Microsoft drošības kontroles centrs](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="cc973-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="cc973-109">Papildinformāciju par Microsoft konfidencialitātes politikām skatiet [Microsoft Konfidencialitātes paziņojums](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="cc973-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="cc973-110">Iespējot Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="cc973-110">Enable Teams integration</span></span>

<span data-ttu-id="cc973-111">Lai iespējotu Microsoft Teams integrāciju ar commerce, jums Azure portālā ir jāreģistrē programma Teams ar savu nomnieku.</span><span class="sxs-lookup"><span data-stu-id="cc973-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="cc973-112">Lai reģistrētu programmu Teams savam nomniekam Azure portālā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="cc973-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="cc973-113">Veiciet norādītās darbības sadaļā [Ātrais starts: reģistrējiet programmu Microsoft identitātes platformā](/azure/active-directory/develop/quickstart-register-app), lai reģistrētu programmu Teams kopā ar nomnieku Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="cc973-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="cc973-114">Kopējiet **Programmas (klienta) ID** vērtību no reģistrētās programmas **Pārskata** lapas.</span><span class="sxs-lookup"><span data-stu-id="cc973-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="cc973-115">Šī vērtība tiks izmantota, lai iespējotu Teams integrāciju programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cc973-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="cc973-116">Kopējiet sertifikāta vērtību, kas tika ievadīta, kad [pievienojāt sertifikātu](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) 1. solī.</span><span class="sxs-lookup"><span data-stu-id="cc973-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="cc973-117">Sertifikāts tiek saukts arī par publisko atslēgu vai programmas atslēgu.</span><span class="sxs-lookup"><span data-stu-id="cc973-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="cc973-118">Šī vērtība tiks izmantota, lai iespējotu Teams integrāciju programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cc973-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="cc973-119">Lai iespējotu Teams integrāciju Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="cc973-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cc973-120">Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="cc973-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="cc973-121">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="cc973-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="cc973-122">Iestatiet opciju **Iespējot Microsoft Teams integrāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="cc973-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="cc973-123">Laukos **Programmas ID** un **Programmas atslēga** ievadiet vērtības, ko ieguvāt, kad Azure portālā reģistrējāt programmu Teams.</span><span class="sxs-lookup"><span data-stu-id="cc973-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="cc973-124">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc973-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="cc973-125">Šajā attēlā parādīts Teams integration konfigurācijas piemērs Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cc973-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Grupu integrācijas konfigurācija programmā Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="cc973-127">Atspējot Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="cc973-127">Disable Teams integration</span></span>

<span data-ttu-id="cc973-128">Lai atspējotu Microsoft Teams integrāciju Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="cc973-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cc973-129">Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="cc973-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="cc973-130">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="cc973-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="cc973-131">Iestatiet opciju **Iespējot Microsoft Teams integrāciju** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="cc973-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="cc973-132">Notīriet vērtības no laukiem **Programmas ID** un **Programmas atslēga**.</span><span class="sxs-lookup"><span data-stu-id="cc973-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="cc973-133">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc973-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc973-134">Pēc brigādes integrācijas programmas Commerce deaktivizēšanas POS termināļi vairs nerādīs uzdevumus, kas publicēti no programmas Teams.</span><span class="sxs-lookup"><span data-stu-id="cc973-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc973-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cc973-135">Additional resources</span></span>

[<span data-ttu-id="cc973-136">Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="cc973-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="cc973-137">Nodrošināt Microsoft Teams no Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cc973-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="cc973-138">Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="cc973-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="cc973-139">Lietotāju lomu pārvaldība Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cc973-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="cc973-140">Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cc973-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="cc973-141">Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ</span><span class="sxs-lookup"><span data-stu-id="cc973-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)