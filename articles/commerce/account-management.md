---
title: Konta pārvaldības lapas un moduļi
description: Šajā tēmā aplūkotas konta pārvaldības lapas un moduļi risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206635"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="f644a-103">Konta pārvaldības lapas un moduļi</span><span class="sxs-lookup"><span data-stu-id="f644a-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f644a-104">Šajā tēmā aplūkotas konta pārvaldības lapas un moduļi risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f644a-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f644a-105">Konta pārvaldība attiecas uz lapu grupu, kas tiek izmantota, lai pārvaldītu ar lietotāja konta saistīto informāciju programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f644a-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f644a-106">Konta pārvaldības lapās ir ietverta konta pārvaldības mērķlapa, lietotāja profila lapa, lietotāja adreses lapa, pasūtījuma vēstures lapa, pasūtījuma informācijas lapa, lojalitātes programmas lapa un vēlmju saraksta lapa.</span><span class="sxs-lookup"><span data-stu-id="f644a-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="f644a-107">Konta pārvaldības mērķlapa</span><span class="sxs-lookup"><span data-stu-id="f644a-107">Account management landing page</span></span>

<span data-ttu-id="f644a-108">Konta pārvaldības mērķlapā tiek izmantoti šādi moduļi.</span><span class="sxs-lookup"><span data-stu-id="f644a-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="f644a-109">**Konteiners** — visas konta pārvaldības izvietošanas lapas moduļi jāievieto konteinerā.</span><span class="sxs-lookup"><span data-stu-id="f644a-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="f644a-110">**Konta sveiciena elements** — šis modulis tiek izmantots, lai nodrošinātu sveiciena ziņojumu konta pārvaldības lapā.</span><span class="sxs-lookup"><span data-stu-id="f644a-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="f644a-111">Tas ietver galvenes rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="f644a-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="f644a-112">**Konta vispārīgais elements** — šis modulis var tikt izmantots, lai nodrošinātu pozīcijas un saites uz kontu pārvaldības lapām, piemēram, lapas “Pasūtījumu vēsture” vai “Mans profils”.</span><span class="sxs-lookup"><span data-stu-id="f644a-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="f644a-113">Vispārīgo mozaīkas moduli var izmantot, lai konfigurētu mozaīku jebkurai lapai.</span><span class="sxs-lookup"><span data-stu-id="f644a-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="f644a-114">Fabrikam šis modulis tiek izmantots lapas “Pasūtījumu vēsture” un “Mans profils” saitēm konta pārvaldības izvietošanas lapā.</span><span class="sxs-lookup"><span data-stu-id="f644a-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="f644a-115">**Konta vēlmju elements** — šis modulis tiek izmantots, lai sniegtu elementu kopsavilkumu klienta vēlmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f644a-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="f644a-116">Piemēram, tas var norādīt: “Jūsu vēlmju sarakstā ir 10 elementi.”</span><span class="sxs-lookup"><span data-stu-id="f644a-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="f644a-117">Tajā ir iekļauti rekvizīti virsrakstam un saitei “Skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="f644a-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="f644a-118">Saite “Skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz vēlmju saraksta lapu.</span><span class="sxs-lookup"><span data-stu-id="f644a-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="f644a-119">**Konta adreses elements** — šis modulis tiek izmantots, lai sniegtu lietotāja adrešu kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="f644a-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="f644a-120">Piemēram, tas var norādīt: “Jūsu kontam ir pievienotas 2 adreses.”</span><span class="sxs-lookup"><span data-stu-id="f644a-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="f644a-121">Tajā ir iekļauti rekvizīti virsrakstam un saitei “Skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="f644a-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="f644a-122">Saite “Skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja adreses lapu.</span><span class="sxs-lookup"><span data-stu-id="f644a-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="f644a-123">**Konta lojalitātes programmas elements** — šis modulis tiek izmantots, lai parādītu un izveidotu saiti ar informāciju par lojalitātes programmu.</span><span class="sxs-lookup"><span data-stu-id="f644a-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="f644a-124">Šim elementam ir divi stāvokļi: viens stāvoklis rāda saites, lai pievienotos lojalitātes programmai, ja lietotājs jau nav dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="f644a-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="f644a-125">Otrs stāvoklis rāda saites, lai skatītu lojalitātes programmas informācijas lapu, kad lietotājs jau ir dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="f644a-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="f644a-126">Rekvizītos ietilpst galvene, saite “Reģistrēšanās” un saite “Skatīt lojalitātes programmas”.</span><span class="sxs-lookup"><span data-stu-id="f644a-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="f644a-127">Saite “Skatīt lojalitāti” ir jākonfigurē novirzīšanai uz lojalitātes programmas lapu.</span><span class="sxs-lookup"><span data-stu-id="f644a-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="f644a-128">Saite “Pierakstīšanās” ir jākonfigurē novirzīšanai uz lapu, kur lietotāji var pievienoties lojalitātes programmai.</span><span class="sxs-lookup"><span data-stu-id="f644a-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="f644a-129">Pasūtījumu vēstures lapa</span><span class="sxs-lookup"><span data-stu-id="f644a-129">Order history page</span></span>

<span data-ttu-id="f644a-130">Pasūtījumu vēstures lapā tiek izmantots pasūtījuma vēstures modulis, lai parādītu visus pēdējos lietotāja veiktos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="f644a-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="f644a-131">Pasūtījumu informācijas lapa</span><span class="sxs-lookup"><span data-stu-id="f644a-131">Order details page</span></span>

<span data-ttu-id="f644a-132">Pasūtījumu informācijas lapa sniedz detalizētu informāciju par katru pasūtījumu, un tai var piekļūt no pasūtījumu vēstures lapas.</span><span class="sxs-lookup"><span data-stu-id="f644a-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="f644a-133">Tā izmanto pasūtījuma informācijas moduli, kas pieprasa pārdošanas ID vai transakcijas ID, lai izgūtu pasūtījuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="f644a-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="f644a-134">Lietotāja profila lapa</span><span class="sxs-lookup"><span data-stu-id="f644a-134">User profile page</span></span>

<span data-ttu-id="f644a-135">Lietotāja profila lapā tiek rādīta lietotāja konta informācija, piemēram, lietotāja vārds un e-pasta adrese.</span><span class="sxs-lookup"><span data-stu-id="f644a-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="f644a-136">Tā izmanto lietotāja profila informāciju un lietotāja profila rediģēšanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="f644a-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="f644a-137">Lai gan e-pasta adresi nevar noņemt, to var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f644a-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="f644a-138">Lietotāja profila lapā tiek rādītas arī lietotāja preferences, kas ļauj lietotājam piedalīties vai atteikties no noteiktām funkcijām, piemēram, ieteikumu sarakstu personalizēšanas.</span><span class="sxs-lookup"><span data-stu-id="f644a-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="f644a-139">Lietotāja adreses lapa</span><span class="sxs-lookup"><span data-stu-id="f644a-139">User address page</span></span>

<span data-ttu-id="f644a-140">Lietotāja adreses lapā tiek parādīts to adrešu saraksts, kuras ir saistītas ar lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="f644a-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="f644a-141">Lietotājs vai nu sniedzis šīs adreses norēķināšanās laikā, vai arī tās tieši pievienojis šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="f644a-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="f644a-142">Lietotāja adreses modulis tiek izmantots, lai pievienotu un rediģētu adreses, iestatītu primāro adresi un atveidotu esošās adreses lapā.</span><span class="sxs-lookup"><span data-stu-id="f644a-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="f644a-143">Vēlmju saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="f644a-143">Wish list page</span></span>

<span data-ttu-id="f644a-144">Vēlmju saraksta lapā ir redzami elementi, kas tika pievienoti klienta vēlmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f644a-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="f644a-145">Tā izmanto vēlmju saraksta moduli, lai atveidotu vēlmju saraksta elementus.</span><span class="sxs-lookup"><span data-stu-id="f644a-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="f644a-146">Lojalitātes lapa</span><span class="sxs-lookup"><span data-stu-id="f644a-146">Loyalty page</span></span>

<span data-ttu-id="f644a-147">Izmantojot lojalitātes programmas lapu, klienti var skatīt informāciju par savu lojalitātes programmu, ja viņi jau ir dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="f644a-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="f644a-148">Viņi var arī skatīt punktus, ko nopelnījuši un izpirkuši pēdējās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="f644a-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="f644a-149">Lapa izmanto lojalitātes programmas informācijas moduli, lai parādītu lojalitātes programmas detaļas.</span><span class="sxs-lookup"><span data-stu-id="f644a-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="f644a-150">Lai pievienotos lojalitātes programmai, mārketinga lapu var izveidot, izmantojot lojalitātes programmas pierakstīšanās un lojalitātes programmas moduļus.</span><span class="sxs-lookup"><span data-stu-id="f644a-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="f644a-151">Ja lietotājs nav lojalitātes programmas dalībnieks, šie moduļi ļaus lietotājam reģistrēties.</span><span class="sxs-lookup"><span data-stu-id="f644a-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f644a-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f644a-152">Additional resources</span></span>

[<span data-ttu-id="f644a-153">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="f644a-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f644a-154">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="f644a-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f644a-155">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="f644a-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f644a-156">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="f644a-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f644a-157">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="f644a-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f644a-158">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="f644a-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f644a-159">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="f644a-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f644a-160">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="f644a-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]