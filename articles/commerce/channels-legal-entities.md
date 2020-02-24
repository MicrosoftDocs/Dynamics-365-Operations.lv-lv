---
title: Izveidot juridiskās personas
description: Šajā tēmā ir aprakstīts, kā izveidot juridiskas personas programmā Microsoft Dynamics 365 Commerce, kas jāveido un jākonfigurē pirms kanālu izveides.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002408"
---
# <a name="create-legal-entities"></a><span data-ttu-id="ca9db-103">Izveidot juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="ca9db-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ca9db-104">Šajā tēmā ir aprakstīts, kā izveidot juridiskas personas programmā Microsoft Dynamics 365 Commerce, kas jāveido un jākonfigurē pirms kanālu izveides.</span><span class="sxs-lookup"><span data-stu-id="ca9db-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="ca9db-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ca9db-105">Overview</span></span>

<span data-ttu-id="ca9db-106">Juridiskā persona ir organizācija, kurai ir reģistrēta vai likumā noteikta juridiskā struktūra.</span><span class="sxs-lookup"><span data-stu-id="ca9db-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="ca9db-107">Juridiskas personas var noslēgt juridiskos līgumus, un tām ir nepieciešams sagatavot pārskatus, lai ziņotu par savu veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="ca9db-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="ca9db-108">Uzņēmums ir juridiskas personas veids.</span><span class="sxs-lookup"><span data-stu-id="ca9db-108">A company is a type of legal entity.</span></span> <span data-ttu-id="ca9db-109">Pašlaik uzņēmums ir vienīgais juridiskas personas veids, ko varat izveidot, un katra juridiska persona ir saistīta ar uzņēmuma ID.</span><span class="sxs-lookup"><span data-stu-id="ca9db-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="ca9db-110">Šī saistība pastāv, jo daži programmas funkcionālie apgabali izmanto uzņēmuma ID vai *DataAreaId* savos datu modeļos.</span><span class="sxs-lookup"><span data-stu-id="ca9db-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="ca9db-111">Šajos funkcionālos apgabalos uzņēmumi tiek izmantoti kā datu drošības robeža.</span><span class="sxs-lookup"><span data-stu-id="ca9db-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="ca9db-112">Lietotāji var piekļūt tikai tā uzņēmuma datiem, kurš ir pašlaik pieteicies sistēmā.</span><span class="sxs-lookup"><span data-stu-id="ca9db-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="ca9db-113">Veidojot kanālu, jānorāda, kurai juridiskajai personai pieder kanāls.</span><span class="sxs-lookup"><span data-stu-id="ca9db-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="ca9db-114">Izveidot jaunu juridisko personu</span><span class="sxs-lookup"><span data-stu-id="ca9db-114">Create a new legal entity</span></span>

<span data-ttu-id="ca9db-115">Lai izveidotu jaunu juridisko personu programmā Dynamics 365 Commerce, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ca9db-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ca9db-116">Navigācijas rūtī pārejiet uz **Moduļi \> Headquarters iestatīšana \> Juridiskās personas**.</span><span class="sxs-lookup"><span data-stu-id="ca9db-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="ca9db-117">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ca9db-117">On the action pane, select **New**.</span></span> <span data-ttu-id="ca9db-118">Labajā pusē tiek parādīta rūts **Jaunā juridiskā persona**.</span><span class="sxs-lookup"><span data-stu-id="ca9db-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="ca9db-119">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca9db-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="ca9db-120">Laukā **Uzņēmums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca9db-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="ca9db-121">Laukā **Valsts/reģions** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca9db-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="ca9db-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ca9db-122">Select **OK**.</span></span> 

   ![Juridiskās personas izveide](media/legal-entities.png)

1. <span data-ttu-id="ca9db-124">Sadaļā **Vispārīgi** sniedziet šādu vispārīgo informāciju par juridisko personu:</span><span class="sxs-lookup"><span data-stu-id="ca9db-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="ca9db-125">Ievadiet meklēšanas nosaukumu, ja ir nepieciešams meklēšanas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="ca9db-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="ca9db-126">Meklēšanas nosaukums ir alternatīvs nosaukums, ko var lietot šīs juridiskās personas meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="ca9db-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="ca9db-127">Atlasiet, vai šī juridiskā persona tiek izmantota kā konsolidēšanas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="ca9db-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="ca9db-128">Atlasiet, vai šī juridiskā persona tiek izmantota kā korekcijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="ca9db-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="ca9db-129">Atlasiet elementam **noklusējuma valodu**.</span><span class="sxs-lookup"><span data-stu-id="ca9db-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="ca9db-130">Izvēlieties **laika joslu** elementam.</span><span class="sxs-lookup"><span data-stu-id="ca9db-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="ca9db-131">Sadaļā **Adreses** atlasiet **Rediģēt**, lai ierakstītu informāciju par adresi, piemēram, ielas nosaukumu un numuru, pasta indeksu un pilsētu.</span><span class="sxs-lookup"><span data-stu-id="ca9db-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="ca9db-132">Sadaļā **Kontaktinformācija** ievadiet informāciju par komunikācijas veidiem, piemēram, e-pasta adreses, URL un tālruņa numurus.</span><span class="sxs-lookup"><span data-stu-id="ca9db-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="ca9db-133">Sadaļā **Likumā noteiktie pārskati** ievadiet reģistrācijas numurus, kas tiek lietoti ar likumu noteikto atskaišu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="ca9db-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="ca9db-134">Sadaļā **Reģistrācijas numuri** ievadiet juridiskās personas prasīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="ca9db-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="ca9db-135">Sadaļā **Bankas konta informācija** ievadiet juridiskās personas bankas kontus un reģistrācijas numurus.</span><span class="sxs-lookup"><span data-stu-id="ca9db-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="ca9db-136">Sadaļā **Ārējā tirdzniecība un loģistika** ievadiet juridiskās personas piegādes informāciju.</span><span class="sxs-lookup"><span data-stu-id="ca9db-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="ca9db-137">Sadaļā **Numuru sērijas** varat apskatīt numuru sērijas, kas ir saistītas ar šo juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="ca9db-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="ca9db-138">Lai sāktu, šis lauks būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="ca9db-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="ca9db-139">Sadaļā **Informācijas paneļa attēls** skatiet vai mainiet logotipu un informācijas paneļa attēlu, kas ir saistīti ar juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="ca9db-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="ca9db-140">Sadaļā **Nodokļa reģistrācija** ievadiet reģistrācijas numurus, kas tiek izmantoti, atskaitoties nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="ca9db-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="ca9db-141">Sadaļā **Nodoklis 1099** ievadiet 1099 informāciju par juridisko iestādi.</span><span class="sxs-lookup"><span data-stu-id="ca9db-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="ca9db-142">Sadaļā **Nodokļu informācija** ievadiet nodokļu informāciju par juridisko iestādi.</span><span class="sxs-lookup"><span data-stu-id="ca9db-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="ca9db-143">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ca9db-143">Select **Save**.</span></span>

<span data-ttu-id="ca9db-144">Tālāk redzamajā attēlā parādīts juridiskas personas informācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="ca9db-144">The following image shows details of an example legal entity.</span></span>

![Juridiskās personas vispārīgā sadaļa](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="ca9db-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ca9db-146">Additional resources</span></span>

[<span data-ttu-id="ca9db-147">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="ca9db-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ca9db-148">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="ca9db-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ca9db-149">Organizācijas hierarhijas</span><span class="sxs-lookup"><span data-stu-id="ca9db-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="ca9db-150">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="ca9db-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ca9db-151">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="ca9db-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
