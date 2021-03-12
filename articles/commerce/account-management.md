---
title: Konta pārvaldības lapas un moduļi
description: Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c465b8883438eee886b177274bf89ddb86aa00b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980560"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="53047-103">Konta pārvaldības lapas un moduļi</span><span class="sxs-lookup"><span data-stu-id="53047-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53047-104">Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="53047-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="53047-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="53047-105">Overview</span></span>

<span data-ttu-id="53047-106">Konta pārvaldība attiecas uz lapu grupu, kas tiek izmantota, lai pārvaldītu ar lietotāja konta saistīto informāciju programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="53047-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="53047-107">Konta pārvaldības lapās ir ietverta konta pārvaldības mērķlapa, lietotāja profila lapa, lietotāja adreses lapa, pasūtījuma vēstures lapa, pasūtījuma informācijas lapa, lojalitātes programmas lapa un vēlmju saraksta lapa.</span><span class="sxs-lookup"><span data-stu-id="53047-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="53047-108">Konta pārvaldības mērķlapa</span><span class="sxs-lookup"><span data-stu-id="53047-108">Account management landing page</span></span>

<span data-ttu-id="53047-109">Konta pārvaldības mērķlapā tiek izmantoti šādi moduļi.</span><span class="sxs-lookup"><span data-stu-id="53047-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="53047-110">**Konteiners** — visas konta pārvaldības izvietošanas lapas moduļi jāievieto konteinerā.</span><span class="sxs-lookup"><span data-stu-id="53047-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="53047-111">**Konta sveiciena elements** — šis modulis tiek izmantots, lai nodrošinātu sveiciena ziņojumu konta pārvaldības lapā.</span><span class="sxs-lookup"><span data-stu-id="53047-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="53047-112">Tas ietver galvenes rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="53047-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="53047-113">**Konta vispārīgais elements** — šis modulis var tikt izmantots, lai nodrošinātu pozīcijas un saites uz kontu pārvaldības lapām, piemēram, lapas “Pasūtījumu vēsture” vai “Mans profils”.</span><span class="sxs-lookup"><span data-stu-id="53047-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="53047-114">Vispārīgo mozaīkas moduli var izmantot, lai konfigurētu mozaīku jebkurai lapai.</span><span class="sxs-lookup"><span data-stu-id="53047-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="53047-115">Fabrikam šis modulis tiek izmantots lapas “Pasūtījumu vēsture” un “Mans profils” saitēm konta pārvaldības izvietošanas lapā.</span><span class="sxs-lookup"><span data-stu-id="53047-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="53047-116">**Konta vēlmju elements** — šis modulis tiek izmantots, lai sniegtu elementu kopsavilkumu klienta vēlmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="53047-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="53047-117">Piemēram, tas var norādīt: “Jūsu vēlmju sarakstā ir 10 elementi.”</span><span class="sxs-lookup"><span data-stu-id="53047-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="53047-118">Tajā ir iekļauti rekvizīti virsrakstam un saitei “Skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="53047-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="53047-119">Saite “Skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz vēlmju saraksta lapu.</span><span class="sxs-lookup"><span data-stu-id="53047-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="53047-120">**Konta adreses elements** — šis modulis tiek izmantots, lai sniegtu lietotāja adrešu kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="53047-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="53047-121">Piemēram, tas var norādīt: “Jūsu kontam ir pievienotas 2 adreses.”</span><span class="sxs-lookup"><span data-stu-id="53047-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="53047-122">Tajā ir iekļauti rekvizīti virsrakstam un saitei “Skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="53047-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="53047-123">Saite “Skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja adreses lapu.</span><span class="sxs-lookup"><span data-stu-id="53047-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="53047-124">**Konta lojalitātes programmas elements** — šis modulis tiek izmantots, lai parādītu un izveidotu saiti ar informāciju par lojalitātes programmu.</span><span class="sxs-lookup"><span data-stu-id="53047-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="53047-125">Šim elementam ir divi stāvokļi: viens stāvoklis rāda saites, lai pievienotos lojalitātes programmai, ja lietotājs jau nav dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="53047-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="53047-126">Otrs stāvoklis rāda saites, lai skatītu lojalitātes programmas informācijas lapu, kad lietotājs jau ir dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="53047-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="53047-127">Rekvizītos ietilpst galvene, saite “Reģistrēšanās” un saite “Skatīt lojalitātes programmas”.</span><span class="sxs-lookup"><span data-stu-id="53047-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="53047-128">Saite “Skatīt lojalitāti” ir jākonfigurē novirzīšanai uz lojalitātes programmas lapu.</span><span class="sxs-lookup"><span data-stu-id="53047-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="53047-129">Saite “Pierakstīšanās” ir jākonfigurē novirzīšanai uz lapu, kur lietotāji var pievienoties lojalitātes programmai.</span><span class="sxs-lookup"><span data-stu-id="53047-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="53047-130">Pasūtījumu vēstures lapa</span><span class="sxs-lookup"><span data-stu-id="53047-130">Order history page</span></span>

<span data-ttu-id="53047-131">Pasūtījumu vēstures lapā tiek izmantots pasūtījuma vēstures modulis, lai parādītu visus pēdējos lietotāja veiktos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="53047-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="53047-132">Pasūtījumu informācijas lapa</span><span class="sxs-lookup"><span data-stu-id="53047-132">Order details page</span></span>

<span data-ttu-id="53047-133">Pasūtījumu informācijas lapa sniedz detalizētu informāciju par katru pasūtījumu, un tai var piekļūt no pasūtījumu vēstures lapas.</span><span class="sxs-lookup"><span data-stu-id="53047-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="53047-134">Tā izmanto pasūtījuma informācijas moduli, kas pieprasa pārdošanas ID vai transakcijas ID, lai izgūtu pasūtījuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="53047-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="53047-135">Lietotāja profila lapa</span><span class="sxs-lookup"><span data-stu-id="53047-135">User profile page</span></span>

<span data-ttu-id="53047-136">Lietotāja profila lapā tiek rādīta lietotāja konta informācija, piemēram, lietotāja vārds un e-pasta adrese.</span><span class="sxs-lookup"><span data-stu-id="53047-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="53047-137">Tā izmanto lietotāja profila informāciju un lietotāja profila rediģēšanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="53047-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="53047-138">Lai gan e-pasta adresi nevar noņemt, to var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="53047-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="53047-139">Lietotāja profila lapā tiek rādītas arī lietotāja preferences, kas ļauj lietotājam piedalīties vai atteikties no noteiktām funkcijām, piemēram, ieteikumu sarakstu personalizēšanas.</span><span class="sxs-lookup"><span data-stu-id="53047-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="53047-140">Lietotāja adreses lapa</span><span class="sxs-lookup"><span data-stu-id="53047-140">User address page</span></span>

<span data-ttu-id="53047-141">Lietotāja adreses lapā tiek parādīts to adrešu saraksts, kuras ir saistītas ar lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="53047-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="53047-142">Lietotājs vai nu sniedzis šīs adreses norēķināšanās laikā, vai arī tās tieši pievienojis šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="53047-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="53047-143">Lietotāja adreses modulis tiek izmantots, lai pievienotu un rediģētu adreses, iestatītu primāro adresi un atveidotu esošās adreses lapā.</span><span class="sxs-lookup"><span data-stu-id="53047-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="53047-144">Vēlmju saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="53047-144">Wish list page</span></span>

<span data-ttu-id="53047-145">Vēlmju saraksta lapā ir redzami elementi, kas tika pievienoti klienta vēlmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="53047-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="53047-146">Tā izmanto vēlmju saraksta moduli, lai atveidotu vēlmju saraksta elementus.</span><span class="sxs-lookup"><span data-stu-id="53047-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="53047-147">Lojalitātes lapa</span><span class="sxs-lookup"><span data-stu-id="53047-147">Loyalty page</span></span>

<span data-ttu-id="53047-148">Izmantojot lojalitātes programmas lapu, klienti var skatīt informāciju par savu lojalitātes programmu, ja viņi jau ir dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="53047-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="53047-149">Viņi var arī skatīt punktus, ko nopelnījuši un izpirkuši pēdējās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="53047-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="53047-150">Lapa izmanto lojalitātes programmas informācijas moduli, lai parādītu lojalitātes programmas detaļas.</span><span class="sxs-lookup"><span data-stu-id="53047-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="53047-151">Lai pievienotos lojalitātes programmai, mārketinga lapu var izveidot, izmantojot lojalitātes programmas pierakstīšanās un lojalitātes programmas moduļus.</span><span class="sxs-lookup"><span data-stu-id="53047-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="53047-152">Ja lietotājs nav lojalitātes programmas dalībnieks, šie moduļi ļaus lietotājam reģistrēties.</span><span class="sxs-lookup"><span data-stu-id="53047-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53047-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="53047-153">Additional resources</span></span>

[<span data-ttu-id="53047-154">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="53047-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="53047-155">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="53047-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="53047-156">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="53047-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="53047-157">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="53047-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="53047-158">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="53047-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="53047-159">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="53047-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="53047-160">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="53047-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="53047-161">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="53047-161">Footer module</span></span>](author-footer-module.md)
