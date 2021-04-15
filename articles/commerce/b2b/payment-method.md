---
title: Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs
description: Šajā tēmā ir aprakstīts, kā konfigurēt klienta konta maksājuma metodi bizness-biznesam (B2B) e-komercijas vietnēs.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799809"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="46b74-103">Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="46b74-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46b74-104">Šajā tēmā ir aprakstīts, kā konfigurēt klienta konta maksājuma metodi bizness-biznesam (B2B) e-komercijas vietnēs.</span><span class="sxs-lookup"><span data-stu-id="46b74-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="46b74-105">Mazumtirgotāji var pieņemt dažāda veida maksājumus apmaiņā pret pārdotajām precēm un pakalpojumiem e-komercijas kanālā.</span><span class="sxs-lookup"><span data-stu-id="46b74-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="46b74-106">Sistēmas iestatīšanas laikā programmā Microsoft Dynamics 365 Commerce ir jākonfigurē katrs maksājuma veids, ko pieņem mazumtirgotājs.</span><span class="sxs-lookup"><span data-stu-id="46b74-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="46b74-107">Klienta konta (vai “uz kredīta”) maksājuma metodei ir jābūt atbalsītai B2B e-komercijas vietnēs.</span><span class="sxs-lookup"><span data-stu-id="46b74-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="46b74-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="46b74-108">Prerequisites</span></span>

1. <span data-ttu-id="46b74-109">Pievienojiet klienta konta maksāšanas metodi komponentam Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b74-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="46b74-110">Saistiet klienta konta maksāšanas metodi ar e-komercijas kanālu.</span><span class="sxs-lookup"><span data-stu-id="46b74-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="46b74-111">Pārliecinieties, vai klientam ir iespējots **Atļaut uz kredīta**, komponentā Commerce Headquarters atverot **Retail un Commerce \> Klienti \> Visi klienti \> Maksājuma noklusējuma informācija**.</span><span class="sxs-lookup"><span data-stu-id="46b74-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="46b74-112">Kā arī pārliecinieties, vai **Kredīta limita** parametri ir iestatīti atbilstoši klientam, atverot **Retail un Commerce \> Klienti \> Visi klienti \> Kredīts un iekasēšana** komponentā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b74-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="46b74-113">Klienta konta maksājuma metodes iespējošana Commerce vietnes veidotājā</span><span class="sxs-lookup"><span data-stu-id="46b74-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="46b74-114">Lai iespējotu klienta konta maksājuma metodi Commerce vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46b74-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="46b74-115">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="46b74-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="46b74-116">Iestatiet rekvizītu **Iespējot klienta konta maksājumus** uz **Iespējot B2B klientiem**.</span><span class="sxs-lookup"><span data-stu-id="46b74-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="46b74-117">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="46b74-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="46b74-118">Jaunās vietnes iestatījumi stājas spēkā tikai pēc faila app.settings.json atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="46b74-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="46b74-119">Papildinformāciju skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="46b74-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="46b74-120">Klienta konta maksājuma metodes iespējošana B2B e-komercijas vietnes norēķināšanās lapā</span><span class="sxs-lookup"><span data-stu-id="46b74-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="46b74-121">Lai iespējotu klienta konta maksājuma metodes B2B e-komercijas vietnes norēķināšanās lapā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46b74-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="46b74-122">Commerce vietnes veidotājā atrodiet un rediģējiet norēķināšanās lapu vai fragmentu, kas satur B2B e-komercijas vietnes norēķināšanās moduli.</span><span class="sxs-lookup"><span data-stu-id="46b74-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="46b74-123">Slotā **Norēķināšanās sekcijas konteiners** atlasiet **Pievienot moduli** un pēc tam pievienojiet **Klienta konta maksājuma** moduli.</span><span class="sxs-lookup"><span data-stu-id="46b74-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="46b74-124">Novietojiet **Klienta konta maksājumu** moduli, atlasot daudzpunktes (**...**), un pēc nepieciešamības atlasot **Pārvietot uz augšu** vai **Pārvietot uz leju**.</span><span class="sxs-lookup"><span data-stu-id="46b74-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="46b74-125">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="46b74-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="46b74-126">Klienta konta maksājuma metodes iespējošanas un publicēšanas apstiprinājums</span><span class="sxs-lookup"><span data-stu-id="46b74-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="46b74-127">Lai apstiprinātu, vai klienta konta maksājuma metode ir iespējota, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46b74-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="46b74-128">Pierakstieties e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="46b74-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="46b74-129">Pievienojiet grozam preci.</span><span class="sxs-lookup"><span data-stu-id="46b74-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="46b74-130">Doties uz norēķināšanās lapu.</span><span class="sxs-lookup"><span data-stu-id="46b74-130">Go to the checkout page.</span></span> <span data-ttu-id="46b74-131">Jums vajadzētu redzēt jauno **Klienta konta** maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="46b74-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46b74-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="46b74-132">Additional resources</span></span>

[<span data-ttu-id="46b74-133">B2B e-komercijas vietnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="46b74-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="46b74-134">Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām</span><span class="sxs-lookup"><span data-stu-id="46b74-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="46b74-135">Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="46b74-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="46b74-136">Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="46b74-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="46b74-137">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="46b74-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]