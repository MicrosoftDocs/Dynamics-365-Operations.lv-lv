---
title: Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām
description: Šajā tēmā ir aprakstīts, kā izveidot organizāciju hierarhiju modelēšanu bizness-biznesam (B2B) organizācijām.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035935"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="40019-103">Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām</span><span class="sxs-lookup"><span data-stu-id="40019-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40019-104">Šajā tēmā ir aprakstīts, kā izveidot organizāciju hierarhiju modelēšanu bizness-biznesam (B2B) organizācijām Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40019-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="40019-105">Programmā Commerce Headquarters biznesa partneru organizācijas tiek pārstāvētas ar klientu un klientu hierarhiju entītijām.</span><span class="sxs-lookup"><span data-stu-id="40019-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="40019-106">Biznesa partnera organizācija un tās lietotāji tiek attēloti kā klienti, un klientu hierarhijas tiek izmantotas, lai saistītu šos klientus vienu ar otru.</span><span class="sxs-lookup"><span data-stu-id="40019-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="40019-107">Kad biznesa partnera pieprasījums pievienoties B2B e-komercijas vietnei ir apstiprināts, tiek veiktas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="40019-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="40019-108">Sistēmā tiek izveidoti divi jauni klientu ieraksti: **Organizācijas tipa** klienta ieraksts biznesa partnera organizācijai un **Personas tipa** klienta ieraksts pieprasītājam (kas ir biznesa partneris, kurš iesniedza pieprasījumu).</span><span class="sxs-lookup"><span data-stu-id="40019-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="40019-109">Klientu hierarhijā tiek izveidots jauns ieraksts sadaļā **Klients \> Klientu hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="40019-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="40019-110">Šim ierakstam ir šādi virsraksta rekvizīti:</span><span class="sxs-lookup"><span data-stu-id="40019-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="40019-111">**Klientu hierarhijas ID** – unikāls klientu hierarhijas ID.</span><span class="sxs-lookup"><span data-stu-id="40019-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="40019-112">Šis ID izmanto numuru sēriju, kas ir definēta Commerce koplietotajos parametros programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="40019-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="40019-113">**Nosaukums** – biznesa partnera organizācijas nosaukums, kā norādīts uzņēmuma pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="40019-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="40019-114">**Mērķis** – šis rekvizīts ir iestatīts uz iepriekš definētu vērtību **B2B organizācijai**.</span><span class="sxs-lookup"><span data-stu-id="40019-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="40019-115">**Organizācija** – biznesa partnera klienta ID.</span><span class="sxs-lookup"><span data-stu-id="40019-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="40019-116">Šeit ir detalizēta informācija par klientu hierarhijas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="40019-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="40019-117">Pieprasītāja klienta ieraksts ir saistīts ar klientu hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="40019-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="40019-118">Administratora loma ir saistīta ar pieprasītāju.</span><span class="sxs-lookup"><span data-stu-id="40019-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="40019-119">Kad administrators pievieno vairāk lietotāju biznesa partnera organizācijai B2B vietnē, programmā Commerce Headquarters tiek izveidots jauns klienta ieraksts katram lietotājam.</span><span class="sxs-lookup"><span data-stu-id="40019-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="40019-120">Šis klienta ieraksts tiek pievienots arī atbilstošajam biznesa partnera klientu hierarhijas ierakstam, un tam ir “lietotāja” loma.</span><span class="sxs-lookup"><span data-stu-id="40019-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="40019-121">Vairumā gadījumu visu hierarhijā esošo klientu ierakstiem ir jāatbilst attiecīgajām rekvizītu vērtībām.</span><span class="sxs-lookup"><span data-stu-id="40019-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="40019-122">Piemēram, tā kā visiem biznesa partneru lietotājiem ir jāsaņem līdzīgas preču cenas, to cenu grupai un saistītajām konfigurācijām ir jāatbilst.</span><span class="sxs-lookup"><span data-stu-id="40019-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="40019-123">Tomēr sistēma šo konsekvenci neievieš.</span><span class="sxs-lookup"><span data-stu-id="40019-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="40019-124">Tāpēc attiecīgie Commerce Headquarters lietotāji ir atbildīgi nodrošināt, ka rekvizītu vērtības un konfigurācijas atbilst visiem attiecīgās hierarhijas klientiem.</span><span class="sxs-lookup"><span data-stu-id="40019-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="40019-125">Commerce Headquarters lietotāji var skatīt rekvizītu vērtības visiem klientu ierakstiem hierarhijā blakus izvietotajā skatā.</span><span class="sxs-lookup"><span data-stu-id="40019-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="40019-126">Atlasiet atbilstošā klienta ieraksta rekvizītus, nolaižamajā izvēlnē atlasot ciļņu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="40019-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="40019-127">Lietotāji var tieši skatīt un rediģēt rekvizītu vērtības no šī skata.</span><span class="sxs-lookup"><span data-stu-id="40019-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="40019-128">Vai arī, ja vēlaties lietot visas administratora klienta ieraksta vērtības visiem lietotāja klientu ierakstiem, atlasiet **Pārlabot** klientu hierarhiju informācijā.</span><span class="sxs-lookup"><span data-stu-id="40019-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40019-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="40019-129">Additional resources</span></span>

[<span data-ttu-id="40019-130">B2B e-komercijas vietnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="40019-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="40019-131">Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="40019-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="40019-132">Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="40019-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="40019-133">Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="40019-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)
