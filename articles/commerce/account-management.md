---
title: Konta pārvaldības lapas un moduļi
description: Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885813"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="7620b-103">Konta pārvaldības lapas un moduļi</span><span class="sxs-lookup"><span data-stu-id="7620b-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7620b-104">Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7620b-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7620b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="7620b-105">Overview</span></span>

<span data-ttu-id="7620b-106">Konta pārvaldība attiecas uz lapu grupu, kas tiek izmantota, lai pārvaldītu ar lietotāja konta saistīto informāciju programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7620b-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7620b-107">Konta pārvaldības lapās ir ietverta konta pārvaldības mērķlapa, lietotāja profila lapa, lietotāja adreses lapa, pasūtījuma vēstures lapa, pasūtījuma informācijas lapa, lojalitātes programmas lapa un vēlmju saraksta lapa.</span><span class="sxs-lookup"><span data-stu-id="7620b-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="7620b-108">Konta pārvaldības mērķlapa</span><span class="sxs-lookup"><span data-stu-id="7620b-108">Account management landing page</span></span>

<span data-ttu-id="7620b-109">Konta pārvaldības mērķlapā tiek izmantoti šādi moduļi.</span><span class="sxs-lookup"><span data-stu-id="7620b-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="7620b-110">**Satura izvietojums** — šis modulis ir konteinera modulis, kas ietver visus moduļus konta pārvaldības mērķlapā.</span><span class="sxs-lookup"><span data-stu-id="7620b-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="7620b-111">**Konta sveiciena elements** — šis modulis tiek izmantots, lai nodrošinātu sveiciena ziņojumu konta pārvaldības lapā.</span><span class="sxs-lookup"><span data-stu-id="7620b-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="7620b-112">Tajā ir iekļauti virsraksta un elementa izmēra rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="7620b-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="7620b-113">Rekvizīts **Elementa izmērs** nosaka moduļa platumu satura izvietojuma modulī.</span><span class="sxs-lookup"><span data-stu-id="7620b-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="7620b-114">Vērtību diapazons ir no **1** līdz **12**, kur **12** ir pilns satura izvietošanas konteinera platums.</span><span class="sxs-lookup"><span data-stu-id="7620b-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="7620b-115">**Konta pasūtījuma izvietošanas elements** — šis modulis tiek izmantots, lai sniegtu kopsavilkumu par pasūtījumu skaitu, ko ievietoja lietotāja konts.</span><span class="sxs-lookup"><span data-stu-id="7620b-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="7620b-116">Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="7620b-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7620b-117">Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz pasūtījumu vēstures lapu.</span><span class="sxs-lookup"><span data-stu-id="7620b-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="7620b-118">**Konta profila novietojuma elements** — šis modulis tiek izmantots, lai sniegtu lietotāja profila kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="7620b-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="7620b-119">Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="7620b-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7620b-120">Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja profila lapu.</span><span class="sxs-lookup"><span data-stu-id="7620b-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="7620b-121">**Konta vēlmju elements** — šis modulis tiek izmantots, lai sniegtu elementu kopsavilkumu klienta vēlmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="7620b-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="7620b-122">Piemēram, tas var norādīt: “Jūsu vēlmju sarakstā ir 10 elementi.”</span><span class="sxs-lookup"><span data-stu-id="7620b-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="7620b-123">Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="7620b-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7620b-124">Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz vēlmju saraksta lapu.</span><span class="sxs-lookup"><span data-stu-id="7620b-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="7620b-125">**Konta adreses elements** — šis modulis tiek izmantots, lai sniegtu lietotāja adrešu kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="7620b-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="7620b-126">Piemēram, tas var norādīt: “Jūsu kontam ir pievienotas 2 adreses.”</span><span class="sxs-lookup"><span data-stu-id="7620b-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="7620b-127">Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”.</span><span class="sxs-lookup"><span data-stu-id="7620b-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7620b-128">Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja adreses lapu.</span><span class="sxs-lookup"><span data-stu-id="7620b-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="7620b-129">**Konta lojalitātes programmas elements** — šis modulis tiek izmantots, lai parādītu un izveidotu saiti ar informāciju par lojalitātes programmu.</span><span class="sxs-lookup"><span data-stu-id="7620b-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="7620b-130">Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram, saitei “skatīt detalizētu informāciju” un saitei “kļūt par dalībnieku”.</span><span class="sxs-lookup"><span data-stu-id="7620b-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="7620b-131">Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lojalitātes programmas lapu.</span><span class="sxs-lookup"><span data-stu-id="7620b-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="7620b-132">Saite “kļūt par dalībnieku” ir jākonfigurē novirzīšanai uz lapu, kur lietotāji var pievienoties lojalitātes programmai.</span><span class="sxs-lookup"><span data-stu-id="7620b-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="7620b-133">Pasūtījumu vēstures lapa</span><span class="sxs-lookup"><span data-stu-id="7620b-133">Order history page</span></span>

<span data-ttu-id="7620b-134">Pasūtījumu vēstures lapā tiek izmantots pasūtījuma vēstures modulis, lai parādītu visus pēdējos lietotāja veiktos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="7620b-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="7620b-135">Pasūtījumu informācijas lapa</span><span class="sxs-lookup"><span data-stu-id="7620b-135">Order details page</span></span>

<span data-ttu-id="7620b-136">Pasūtījumu informācijas lapa sniedz detalizētu informāciju par katru pasūtījumu, un tai var piekļūt no pasūtījumu vēstures lapas.</span><span class="sxs-lookup"><span data-stu-id="7620b-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="7620b-137">Tā izmanto pasūtījuma informācijas moduli, kas pieprasa pārdošanas ID vai transakcijas ID, lai izgūtu pasūtījuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="7620b-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="7620b-138">Lietotāja profila lapa</span><span class="sxs-lookup"><span data-stu-id="7620b-138">User profile page</span></span>

<span data-ttu-id="7620b-139">Lietotāja profila lapā tiek rādīta lietotāja konta informācija, piemēram, lietotāja vārds un e-pasta adrese.</span><span class="sxs-lookup"><span data-stu-id="7620b-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="7620b-140">Tā izmanto lietotāja profila moduli.</span><span class="sxs-lookup"><span data-stu-id="7620b-140">It uses the user profile module.</span></span> <span data-ttu-id="7620b-141">Lai gan e-pasta adresi nevar noņemt, to var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="7620b-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="7620b-142">Lietotāja profila lapā tiek rādītas arī lietotāja preferences, kas ļauj lietotājam piedalīties vai atteikties no noteiktām funkcijām, piemēram, ieteikumu sarakstu personalizēšanas.</span><span class="sxs-lookup"><span data-stu-id="7620b-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="7620b-143">Lietotāja adreses lapa</span><span class="sxs-lookup"><span data-stu-id="7620b-143">User address page</span></span>

<span data-ttu-id="7620b-144">Lietotāja adreses lapā tiek parādīts to adrešu saraksts, kuras ir saistītas ar lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="7620b-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="7620b-145">Lietotājs vai nu sniedzis šīs adreses norēķināšanās laikā, vai arī tās tieši pievienojis šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="7620b-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="7620b-146">Lietotāja adreses modulis tiek izmantots, lai pievienotu un rediģētu adreses, iestatītu primāro adresi un atveidotu esošās adreses lapā.</span><span class="sxs-lookup"><span data-stu-id="7620b-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="7620b-147">Vēlmju saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="7620b-147">Wish list page</span></span>

<span data-ttu-id="7620b-148">Vēlmju saraksta lapā ir redzami elementi, kas tika pievienoti klienta vēlmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="7620b-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="7620b-149">Tā izmanto vēlmju saraksta moduli, lai atveidotu vēlmju saraksta elementus.</span><span class="sxs-lookup"><span data-stu-id="7620b-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="7620b-150">Lojalitātes lapa</span><span class="sxs-lookup"><span data-stu-id="7620b-150">Loyalty page</span></span>

<span data-ttu-id="7620b-151">Izmantojot lojalitātes programmas lapu, klienti var pievienoties lojalitātes programmai vai, ja tie jau ir lojalitātes programmas dalībnieki, skatīt informāciju par savu programmu.</span><span class="sxs-lookup"><span data-stu-id="7620b-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="7620b-152">Viņi var arī skatīt punktus, ko nopelnījuši un izpirkuši pēdējās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="7620b-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7620b-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7620b-153">Additional resources</span></span>

[<span data-ttu-id="7620b-154">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="7620b-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7620b-155">Container modulis</span><span class="sxs-lookup"><span data-stu-id="7620b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7620b-156">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="7620b-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7620b-157">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="7620b-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7620b-158">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="7620b-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7620b-159">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="7620b-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7620b-160">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="7620b-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7620b-161">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="7620b-161">Footer module</span></span>](author-footer-module.md)
