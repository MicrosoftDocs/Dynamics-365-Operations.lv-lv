---
title: Izveidot juridiskās personas
description: Šajā tēmā aprakstīts, kā izveidot juridisku personu risinājumā Microsoft Dynamics 365 Commerce, kas jāizveido un jākonfigurē pirms kanālu izveides.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800619"
---
# <a name="create-legal-entities"></a><span data-ttu-id="4050d-103">Izveidot juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="4050d-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4050d-104">Šajā tēmā aprakstīts, kā izveidot juridisku personu risinājumā Microsoft Dynamics 365 Commerce, kas jāizveido un jākonfigurē pirms kanālu izveides.</span><span class="sxs-lookup"><span data-stu-id="4050d-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="4050d-105">Juridiskā persona ir organizācija, kurai ir reģistrēta vai likumā noteikta juridiskā struktūra.</span><span class="sxs-lookup"><span data-stu-id="4050d-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="4050d-106">Juridiskas personas var noslēgt juridiskos līgumus, un tām ir nepieciešams sagatavot pārskatus, lai ziņotu par savu veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="4050d-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="4050d-107">Uzņēmums ir juridiskas personas veids.</span><span class="sxs-lookup"><span data-stu-id="4050d-107">A company is a type of legal entity.</span></span> <span data-ttu-id="4050d-108">Pašlaik uzņēmums ir vienīgais juridiskas personas veids, ko varat izveidot, un katra juridiska persona ir saistīta ar uzņēmuma ID.</span><span class="sxs-lookup"><span data-stu-id="4050d-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="4050d-109">Šī saistība pastāv, jo daži programmas funkcionālie apgabali izmanto uzņēmuma ID vai *DataAreaId* savos datu modeļos.</span><span class="sxs-lookup"><span data-stu-id="4050d-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="4050d-110">Šajos funkcionālos apgabalos uzņēmumi tiek izmantoti kā datu drošības robeža.</span><span class="sxs-lookup"><span data-stu-id="4050d-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="4050d-111">Lietotāji var piekļūt tikai tā uzņēmuma datiem, kurš ir pašlaik pieteicies sistēmā.</span><span class="sxs-lookup"><span data-stu-id="4050d-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="4050d-112">Veidojot kanālu, jānorāda, kurai juridiskajai personai pieder kanāls.</span><span class="sxs-lookup"><span data-stu-id="4050d-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="4050d-113">Izveidot jaunu juridisko personu</span><span class="sxs-lookup"><span data-stu-id="4050d-113">Create a new legal entity</span></span>

<span data-ttu-id="4050d-114">Lai izveidotu jaunu juridisko personu programmā Dynamics 365 Commerce, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4050d-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4050d-115">Navigācijas rūtī pārejiet uz  **Moduļi \> Headquarters iestatīšana \> Juridiskās personas**.</span><span class="sxs-lookup"><span data-stu-id="4050d-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="4050d-116">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4050d-116">On the action pane, select **New**.</span></span> <span data-ttu-id="4050d-117">Labajā pusē tiek parādīta rūts **Jaunā juridiskā persona**.</span><span class="sxs-lookup"><span data-stu-id="4050d-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="4050d-118">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4050d-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="4050d-119">Laukā **Uzņēmums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4050d-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="4050d-120">Laukā **Valsts/reģions** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4050d-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="4050d-121">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4050d-121">Select **OK**.</span></span> 

   ![Juridiskās personas izveide](media/legal-entities.png)

1. <span data-ttu-id="4050d-123">Sadaļā **Vispārīgi** sniedziet šādu vispārīgo informāciju par juridisko personu:</span><span class="sxs-lookup"><span data-stu-id="4050d-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="4050d-124">Ievadiet meklēšanas nosaukumu, ja ir nepieciešams meklēšanas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="4050d-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="4050d-125">Meklēšanas nosaukums ir alternatīvs nosaukums, ko var lietot šīs juridiskās personas meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="4050d-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="4050d-126">Atlasiet, vai šī juridiskā persona tiek izmantota kā konsolidēšanas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="4050d-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="4050d-127">Atlasiet, vai šī juridiskā persona tiek izmantota kā korekcijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="4050d-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="4050d-128">Atlasiet elementam **noklusējuma valodu**.</span><span class="sxs-lookup"><span data-stu-id="4050d-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="4050d-129">Izvēlieties **laika joslu** elementam.</span><span class="sxs-lookup"><span data-stu-id="4050d-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="4050d-130">Sadaļā **Adreses** atlasiet **Rediģēt**, lai ierakstītu informāciju par adresi, piemēram, ielas nosaukumu un numuru, pasta indeksu un pilsētu.</span><span class="sxs-lookup"><span data-stu-id="4050d-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="4050d-131">Sadaļā **Kontaktinformācija** ievadiet informāciju par komunikācijas veidiem, piemēram, e-pasta adreses, URL un tālruņa numurus.</span><span class="sxs-lookup"><span data-stu-id="4050d-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="4050d-132">Sadaļā **Likumā noteiktie pārskati** ievadiet reģistrācijas numurus, kas tiek lietoti ar likumu noteikto atskaišu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="4050d-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="4050d-133">Sadaļā **Reģistrācijas numuri** ievadiet juridiskās personas prasīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="4050d-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="4050d-134">Sadaļā **Bankas konta informācija** ievadiet juridiskās personas bankas kontus un reģistrācijas numurus.</span><span class="sxs-lookup"><span data-stu-id="4050d-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="4050d-135">Sadaļā **Ārējā tirdzniecība un loģistika** ievadiet juridiskās personas piegādes informāciju.</span><span class="sxs-lookup"><span data-stu-id="4050d-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="4050d-136">Sadaļā **Numuru sērijas** varat apskatīt numuru sērijas, kas ir saistītas ar šo juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="4050d-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="4050d-137">Lai sāktu, šis lauks būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="4050d-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="4050d-138">Sadaļā **Informācijas paneļa attēls** skatiet vai mainiet logotipu un informācijas paneļa attēlu, kas ir saistīti ar juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="4050d-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="4050d-139">Sadaļā **Nodokļa reģistrācija** ievadiet reģistrācijas numurus, kas tiek izmantoti, atskaitoties nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="4050d-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="4050d-140">Sadaļā **Nodoklis 1099** ievadiet 1099 informāciju par juridisko iestādi.</span><span class="sxs-lookup"><span data-stu-id="4050d-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="4050d-141">Sadaļā **Nodokļu informācija** ievadiet nodokļu informāciju par juridisko iestādi.</span><span class="sxs-lookup"><span data-stu-id="4050d-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="4050d-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4050d-142">Select **Save**.</span></span>

<span data-ttu-id="4050d-143">Tālāk redzamajā attēlā parādīts juridiskas personas informācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="4050d-143">The following image shows details of an example legal entity.</span></span>

![Juridiskās personas vispārīgā sadaļa](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="4050d-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4050d-145">Additional resources</span></span>

[<span data-ttu-id="4050d-146">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="4050d-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="4050d-147">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="4050d-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="4050d-148">Organizācijas hierarhijas</span><span class="sxs-lookup"><span data-stu-id="4050d-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="4050d-149">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="4050d-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4050d-150">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4050d-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
