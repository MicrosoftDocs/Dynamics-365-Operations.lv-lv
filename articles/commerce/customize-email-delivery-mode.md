---
title: Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida
description: Šajā tēmā aprakstīts, kā iestatīt pielāgotas e-pasta veidnes konkrētiem paziņojumu veidiem un piegādes veidiem risinājumā Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 411e694b33e0443a336f6a8cdad78714630e4bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799377"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="d1a4e-103">Darbību e-pasta ziņojumu pielāgošana pēc piegādes veida</span><span class="sxs-lookup"><span data-stu-id="d1a4e-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1a4e-104">Šajā tēmā aprakstīts, kā iestatīt pielāgotas e-pasta veidnes konkrētiem paziņojumu veidiem un piegādes veidiem risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d1a4e-105">Transakciju e-pasta vēstules tagad var tikt pielāgotas kombinācijai no paziņojuma veida (piemēram, **Pasūtījums izveidots**, **Pasūtījums iepakots** vai **Pasūtījumam ir izrakstīts rēķins**) un piegādes veida (piemēram, pa nakti, savākšana no veikala vai savākšana ietves malā).</span><span class="sxs-lookup"><span data-stu-id="d1a4e-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="d1a4e-106">Pielāgoti transakciju e-pasta ziņojumi ļauj mazumtirgotājiem nodrošināt saviem klientiem pasūtījumu izpildi, kas ir pielāgota pasūtījuma piegādes veidam.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="d1a4e-107">Piemēram, "pasūtījums iepakots" notikums var tikt pielāgots, lai tas nodrošinātu saņemšanas ietves malā instrukcijas debitoriem, kuri izvēlas savākšanu ietves malā.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="d1a4e-108">Tā var arī sniegt informāciju par pārvadājumu pārvadātāju un piegādi klientiem, kuri izvēlas nosūtīt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="d1a4e-109">Lai izmantotu funkcionalitāti pielāgotajiem transakciju e-pastiem, vispirms ir jāieslēdz līdzeklis **Transakciju e-pasta veidņu pielāgošana pēc piegādes veida**, dodoties uz **Darbvietas \> Līdzekļu pārvaldība** programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="d1a4e-110">E-pasta ziņojumus var pielāgot pēc piegādes veida šādos paziņojuma tipos:</span><span class="sxs-lookup"><span data-stu-id="d1a4e-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="d1a4e-111">**Pasūtījuma atcelšana** — Šis e-pasta paziņojuma tips ir jauns.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="d1a4e-112">**Pasūtījums izveidots**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-112">**Order created**</span></span>
- <span data-ttu-id="d1a4e-113">**Pasūtījums apstiprināts**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-113">**Order confirmed**</span></span>
- <span data-ttu-id="d1a4e-114">**Pasūtījumam ir izrakstīts rēķins** — Šis e-pasta paziņojuma tips ir jauns.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="d1a4e-115">To var izmantot, paziņojuma tipa **Pasūtījuma nosūtīts** vietā, kas nosūtīs paziņojumu jebkuram rēķina notikumam, kuram ir nosūtīšanas piegādes veids (nevis saņemšanas, izpildes vai elektroniskais piegādes veids).</span><span class="sxs-lookup"><span data-stu-id="d1a4e-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="d1a4e-116">**Pasūtījums saņemts**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-116">**Order picked**</span></span>
- <span data-ttu-id="d1a4e-117">**Pasūtījums iepakots**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-117">**Order packed**</span></span>
- <span data-ttu-id="d1a4e-118">**Pasūtījums sagatavots savākšanai** – šo paziņojuma tipu var pielāgot piegādes veidam tikai tad, ja ir ieslēgts līdzeklis **Vairāku saņemšanas piegādes režīmu atbalsts**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="d1a4e-119">Šādā gadījumā šis paziņojuma tips ir funkcionāli līdzvērtīgs paziņojuma tipam **Pasūtījuma iepakots**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="d1a4e-120">**Maksājums neizdevās**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-120">**Payment failed**</span></span>
- <span data-ttu-id="d1a4e-121">**Izveidots aizstāšanas pasūtījums**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="d1a4e-122">Konfigurēt e-pasta veidnes noteiktiem piegādes veidiem</span><span class="sxs-lookup"><span data-stu-id="d1a4e-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="d1a4e-123">Šai procedūrai pieņēmums ir tāds, ka jūs jau esat izveidojis jaunas, pielāgotas e-pasta veidnes un pievienojis tās lapai **Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="d1a4e-124">Informāciju par e-pasta veidņu izveidi un augšupielādi skatiet [E-pasta veidņu izveide transakciju notikumiem](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="d1a4e-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="d1a4e-125">Lai konfigurētu e-pasta veidnes noteiktiem piegādes veidiem programmā Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d1a4e-126">Dodieties uz **Komercijas e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d1a4e-127">Sadaļā **Mazumtirdzniecības notikumu paziņojumu iestatījumi** atlasiet esošu paziņojuma tipu.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="d1a4e-128">Kamēr paziņojuma tips joprojām ir atlasīts, izvēlieties **Konfigurēt piegādes veidus**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="d1a4e-129">Dialoglodziņā **Piegādes veidi** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="d1a4e-130">Jaunajā rindā, laukā **Piegādes veids** atlasiet piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="d1a4e-131">Laukā **E-pasta ID** atlasiet e-pasta veidni, ko kartēt uz piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="d1a4e-132">Atzīmējiet izvēles rūtiņu **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="d1a4e-133">Atkārtojiet 4. un 7. soli, lai pievienotu citus piegādes veidus.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="d1a4e-134">Pēc pabeigšanas atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="d1a4e-135">Kad pārdošanas pasūtījuma rindās ir vairāk nekā viens piegādes veids, tiks izmantota noklusējuma veidne.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="d1a4e-136">Noklusējuma veidne ir veidne, kas ir kartēta paziņojuma veidam lapā **Komercijas e-pasta paziņojuma profils**.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="d1a4e-137">Ja pārdošanas pasūtījumam ir piegādes veids, kas nav konfigurēts pielāgotai e-pasta veidnei, tiks izmantota noklusējuma e-pasta veidne.</span><span class="sxs-lookup"><span data-stu-id="d1a4e-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1a4e-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d1a4e-138">Additional resources</span></span>

[<span data-ttu-id="d1a4e-139">Zvanu centra pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="d1a4e-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="d1a4e-140">Piegādes veida mainīšana programmā POS</span><span class="sxs-lookup"><span data-stu-id="d1a4e-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]