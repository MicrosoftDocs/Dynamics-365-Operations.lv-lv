---
title: Noklusējuma debitora izveide
description: Šajā tēmā aprakstīts, kā izveidot noklusējuma klientu, kuru lietot, veidojot kanālu risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477904"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="abc34-103">Noklusējuma debitora izveide</span><span class="sxs-lookup"><span data-stu-id="abc34-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abc34-104">Šajā tēmā aprakstīts, kā izveidot noklusējuma klientu, kuru lietot, veidojot kanālu risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="abc34-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="abc34-105">Veidojot kanālu, būs jānorāda noklusējuma debitors.</span><span class="sxs-lookup"><span data-stu-id="abc34-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="abc34-106">Noklusējuma debitoru var viegli izveidot, vispirms izveidojot debitoru grupu un debitoru adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="abc34-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="abc34-107">Debitoru grupas izveidošana</span><span class="sxs-lookup"><span data-stu-id="abc34-107">Create a customer group</span></span>

<span data-ttu-id="abc34-108">Ja debitoru grupas vēl nepastāv, varat to izveidot.</span><span class="sxs-lookup"><span data-stu-id="abc34-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="abc34-109">Iespējams izveidot grupas, kas pārstāv dažādas debitoru grupas, piemēram, vairumtirdzniecību, mazumtirdzniecību, inbternetu, darbiniekus u. tml.</span><span class="sxs-lookup"><span data-stu-id="abc34-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="abc34-110">Lai izveidotu debitoru grupu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="abc34-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="abc34-111">Navigācijas rūtī ejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Debitori \> Debitoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="abc34-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="abc34-112">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="abc34-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="abc34-113">Lodziņā **Debitoru grupa** ievadiet debitoru grupas ID.</span><span class="sxs-lookup"><span data-stu-id="abc34-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="abc34-114">Lodziņā **Apraksts** ievadiet atbilstošu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="abc34-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="abc34-115">Lodziņā **Apmaksas nosacījumi** ievadiet atbilstošu vērtību.</span><span class="sxs-lookup"><span data-stu-id="abc34-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="abc34-116">Ievadiet atbilstošu vērtību lodziņā **Laiks no rēķina apmaksas datuma līdz maksājuma datumam**.</span><span class="sxs-lookup"><span data-stu-id="abc34-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="abc34-117">Lodziņā **Noklusējuma nodokļu grupa** ievadiet nodokļu grupu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="abc34-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="abc34-118">Atlasiet izvēles rūtiņu **Cenā iekļauts PVN**, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="abc34-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="abc34-119">Lodziņā **Noklusējuma norakstīšanas iemesls** ievadiet atbilstošu vērtību, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="abc34-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="abc34-120">Tālāk redzamajā attēlā ir parādītas vairākas konfigurētās debitoru grupas.</span><span class="sxs-lookup"><span data-stu-id="abc34-120">The following image shows several configured customer groups.</span></span>

![Debitoru grupas](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="abc34-122">Jaunas debitoru adrešu grāmatas izveide</span><span class="sxs-lookup"><span data-stu-id="abc34-122">Create a customer address book</span></span>

<span data-ttu-id="abc34-123">Debitoram jābūt saistītam ar adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="abc34-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="abc34-124">Ja tā vēl nav izveidota, tā jāizveido.</span><span class="sxs-lookup"><span data-stu-id="abc34-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="abc34-125">Lai izveidotu debitoru grupas adrešu grāmatu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="abc34-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="abc34-126">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Adrešu grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="abc34-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="abc34-127">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="abc34-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="abc34-128">Lodziņā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="abc34-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="abc34-129">Lodziņā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="abc34-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="abc34-130">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="abc34-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="abc34-131">Tālāk redzamajā attēlā ir parādīts adresu gramatas piemērs.</span><span class="sxs-lookup"><span data-stu-id="abc34-131">The following image shows an example address book.</span></span>

![Adrešu grāmata](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="abc34-133">Noklusējuma debitora izveide</span><span class="sxs-lookup"><span data-stu-id="abc34-133">Create a default customer</span></span>

<span data-ttu-id="abc34-134">Lai izveidotu noklusējuma debitoru, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="abc34-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="abc34-135">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Debitori \> Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="abc34-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="abc34-136">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="abc34-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="abc34-137">Nolaižamajā sarakstā **Tips** atlasiet "Persona".</span><span class="sxs-lookup"><span data-stu-id="abc34-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="abc34-138">Nolaižamajā sarakstā **Debitora konts** atlasiet vai ievadiet konta numuru (piemēram, "100001").</span><span class="sxs-lookup"><span data-stu-id="abc34-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="abc34-139">Nolaižamajā sarakstā **Vārds** atlasiet vai ievadiet vārdu (piemēram, "Noklusējums").</span><span class="sxs-lookup"><span data-stu-id="abc34-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="abc34-140">Nolaižamajā sarakstā **Otrais vārds** atlasiet vai ievadiet vārdu (piemēram, "Mazumtirdzniecība").</span><span class="sxs-lookup"><span data-stu-id="abc34-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="abc34-141">Nolaižamajā sarakstā **Uzvārds** atlasiet vai ievadiet vārdu (piemēram, "Debitors").</span><span class="sxs-lookup"><span data-stu-id="abc34-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="abc34-142">Nolaižamajā sarakstā **Valūta** atlasiet vai ievadiet valūtu (piemēram, "USD").</span><span class="sxs-lookup"><span data-stu-id="abc34-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="abc34-143">Nolaižamajā sarakstā **Valūta** atlasiet iepriekš izveidoto debitoru grupu.</span><span class="sxs-lookup"><span data-stu-id="abc34-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="abc34-144">Nolaižamajā srakstā **Adrešu grāmatas**  atlasiet esošu debitoru adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="abc34-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="abc34-145">Atlasiet **Saglabāt**, lai saglabātu un atgrieztos debitoru detalizētās informācijas ekrānā pēc jauna debitora.</span><span class="sxs-lookup"><span data-stu-id="abc34-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="abc34-146">Noklusējuma debitoram adrese nav jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="abc34-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="abc34-147">Tālāk redzamajā attēlā parādīts debitoru izveides piemērs.</span><span class="sxs-lookup"><span data-stu-id="abc34-147">The following image shows an example of customer creation.</span></span>

![Noklusējuma debitora izveide](media/default-customer-creation.png)

<span data-ttu-id="abc34-149">Tālāk redzamajā attēlā parādīta noklusējuma debitora konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="abc34-149">The following image shows a default customer configuration.</span></span>

![Debitora konfigurācijas paraugs](media/default-customer-configuration1.png)

<span data-ttu-id="abc34-151">Lielākā daļa noklusējuma vērtību debitora detalizētās informācijas ekrānā var palikt, bet ir divas vērtības ir jāmaina.</span><span class="sxs-lookup"><span data-stu-id="abc34-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="abc34-152">Debitoru detalizētas informācijas ekrānā izvērsiet **Pārdošanas pasūtījuma noklusējumi**.</span><span class="sxs-lookup"><span data-stu-id="abc34-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="abc34-153">Nolaižamajā sarakstā **Vieta** atlasiet vai ievadiet iepriekš konfigurētu vietu.</span><span class="sxs-lookup"><span data-stu-id="abc34-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="abc34-154">Nolaižamajā sarakstā **Noliktava** atlasiet vai ievadiet iepriekš konfigurētu noliktavu.</span><span class="sxs-lookup"><span data-stu-id="abc34-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="abc34-155">Tālāk redzamajā attēlā parādīts debitoru konfigurācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="abc34-155">The following image shows an example customer configuration.</span></span>

![Debitora konfigurācijas piemērs](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="abc34-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="abc34-157">Additional resources</span></span>

[<span data-ttu-id="abc34-158">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="abc34-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="abc34-159">Uzstādīt kanālu priekšnosacījumus</span><span class="sxs-lookup"><span data-stu-id="abc34-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
