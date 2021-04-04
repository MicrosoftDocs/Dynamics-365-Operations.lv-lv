---
title: E-pasta paziņojumu iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555311"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="01bc2-103">E-pasta paziņojumu profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="01bc2-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01bc2-104">Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="01bc2-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="01bc2-105">Veidojot kanālus, varat iestatīt e-pasta paziņojuma profilu.</span><span class="sxs-lookup"><span data-stu-id="01bc2-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="01bc2-106">Šādā veidā e-pasta ziņojumi var tikt nosūtīti debitoriem par dažādiem darbību notikumiem, piemēram, pasūtījuma izveidi, pasūtījuma nosūtīšanas statusu un maksājuma kļūmi.</span><span class="sxs-lookup"><span data-stu-id="01bc2-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="01bc2-107">Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="01bc2-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="01bc2-108">E-pasta paziņojumu profila izveide</span><span class="sxs-lookup"><span data-stu-id="01bc2-108">Create an email notification profile</span></span>

<span data-ttu-id="01bc2-109">Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="01bc2-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="01bc2-110">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="01bc2-111">Darbību rūtī noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="01bc2-112">Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="01bc2-113">Ievadiet atbilstošu aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="01bc2-114">Iestatiet slēdzi **Aktīvs** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="01bc2-115">E-pasta veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="01bc2-115">Create an email template</span></span>

<span data-ttu-id="01bc2-116">Lai e-pasta paziņojuma tipu varētu iespējot, programmā Commerce Headquarters ir jāizveido organizācijas e-pasta veidne.</span><span class="sxs-lookup"><span data-stu-id="01bc2-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="01bc2-117">Šī veidne definē e-pasta tēmu, sūtītāju, noklusējuma valodu un e-pasta pamattekstu katrai valodai, ko vēlaties atbalstīt.</span><span class="sxs-lookup"><span data-stu-id="01bc2-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="01bc2-118">Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="01bc2-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="01bc2-119">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Organizāciju e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="01bc2-120">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="01bc2-121">Laukā **E-pasta ID** ievadiet ID, lai palīdzētu identificēt šo veidni.</span><span class="sxs-lookup"><span data-stu-id="01bc2-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="01bc2-122">Laukā **Sūtītāja nosaukums** ievadiet sūtītāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="01bc2-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="01bc2-123">Ievadiet jēgpilnu aprakstu laukā **Epasta apraksts**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="01bc2-124">Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāju e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="01bc2-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="01bc2-125">Sadaļā **Vispārīgi** atlasiet noklusējuma valodu e-pasta veidnei.</span><span class="sxs-lookup"><span data-stu-id="01bc2-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="01bc2-126">Noklusējuma valoda tiks lietota, ja norādītajai valodai nav lokalizētas veidnes.</span><span class="sxs-lookup"><span data-stu-id="01bc2-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="01bc2-127">Paplašiniet sadaļu **E-pasta ziņojuma saturs** un atlasiet **Jauns**, lai izveidotu veidnes saturu.</span><span class="sxs-lookup"><span data-stu-id="01bc2-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="01bc2-128">Katram satura vienumam atlasiet valodu un norādiet e-pasta tēmas rindu.</span><span class="sxs-lookup"><span data-stu-id="01bc2-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="01bc2-129">Ja e-pasta ziņojumā būs pamatteksts, pārliecinieties, ir atzīmēta izvēles rūtiņa **Ir pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="01bc2-130">Darbības rūtī atlasiet **E-pasta ziņojums**, lai nodrošinātu e-pasta pamatteksta veidni.</span><span class="sxs-lookup"><span data-stu-id="01bc2-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="01bc2-131">Tālāk redzamajā attēlā parādīti daži e-pasta veidnes iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="01bc2-131">The following image shows some example email template settings.</span></span>

![E-pasta veidņu iestatījumi](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="01bc2-133">E-pasta notikuma izveide</span><span class="sxs-lookup"><span data-stu-id="01bc2-133">Create an email event</span></span>

<span data-ttu-id="01bc2-134">Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="01bc2-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="01bc2-135">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="01bc2-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="01bc2-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="01bc2-137">**E-pasta ID** nolaižamajā sarakstā atlasiet e-pasta veidni.</span><span class="sxs-lookup"><span data-stu-id="01bc2-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="01bc2-138">Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="01bc2-139">Atzīmējiet izvēles rūtiņu **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="01bc2-140">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="01bc2-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="01bc2-141">Tālāk redzamajā attēlā parādīti daži notikuma paziņojumu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="01bc2-141">The following image shows some example event notification settings.</span></span>

![Notikuma paziņojuma iestatījumi](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="01bc2-143">Turpmākās darbības</span><span class="sxs-lookup"><span data-stu-id="01bc2-143">Next steps</span></span>

<span data-ttu-id="01bc2-144">Lai varētu nosūtīt e-pastus, ir jākonfigurē izejošais pasta pakalpojums un jāiestata pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="01bc2-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="01bc2-145">Papildinformāciju skatiet [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="01bc2-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="01bc2-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="01bc2-146">Additional resources</span></span>

[<span data-ttu-id="01bc2-147">E-pasta konfigurēšana un sūtīšana</span><span class="sxs-lookup"><span data-stu-id="01bc2-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="01bc2-148">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="01bc2-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="01bc2-149">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="01bc2-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="01bc2-150">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="01bc2-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
