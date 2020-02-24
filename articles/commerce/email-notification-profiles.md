---
title: E-pasta paziņojumu iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: feb28b9c801786f63282c4189d3eeb6d53ed07e1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003146"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="e177c-103">E-pasta paziņojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e177c-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e177c-104">Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e177c-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e177c-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e177c-105">Overview</span></span>

<span data-ttu-id="e177c-106">Pirms kanālu izveides jums vajadzēs iestatīt profilu, lai nodrošinātu, ka dažādiem notikumiem, piemēram, pasūtījuma izveidei, pasūtījuma nosūtīšanas statusam un maksājuma kļūmei, var nosūtīt e-pasta paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="e177c-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="e177c-107">Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span><span class="sxs-lookup"><span data-stu-id="e177c-107">For additional email configuration information, see [Configure and send email](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="e177c-108">E-pasta paziņojumu profila izveide</span><span class="sxs-lookup"><span data-stu-id="e177c-108">Create an email notification profile</span></span>

<span data-ttu-id="e177c-109">Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e177c-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="e177c-110">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Mazumtirdzniecības e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="e177c-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="e177c-111">Darbību rūtī noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e177c-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="e177c-112">Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="e177c-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="e177c-113">Ievadiet atbilstošu aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e177c-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="e177c-114">Iestatiet slēdzi **Aktīvs** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e177c-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="e177c-115">E-pasta veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="e177c-115">Create an email template</span></span>

<span data-ttu-id="e177c-116">Lai varētu izveidot e-pasta paziņojumu, jāizveido organizācijas e-pasta veidne, kurā iekļauta sūtītāju e-pasta informācija un e-pasta veidne.</span><span class="sxs-lookup"><span data-stu-id="e177c-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="e177c-117">Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e177c-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="e177c-118">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Organizāciju e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="e177c-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="e177c-119">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e177c-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e177c-120">Laukā **E-pasta ID** ievadiet ID, lai palīdzētu identificēt šo veidni.</span><span class="sxs-lookup"><span data-stu-id="e177c-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="e177c-121">Laukā **Sūtītāja nosaukums** ievadiet sūtītāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e177c-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="e177c-122">Ievadiet jēgpilnu aprakstu laukā **Epasta apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e177c-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="e177c-123">Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāju e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="e177c-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="e177c-124">Sadaļā **Vispārīgi** aizpildiet visu izvēles informāciju (piemēram, e-pasta prioritāte).</span><span class="sxs-lookup"><span data-stu-id="e177c-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="e177c-125">Paplašiniet sadaļu **E-pasta ziņojuma saturs** un atlasiet **Jauns**, lai izveidotu veidnes saturu.</span><span class="sxs-lookup"><span data-stu-id="e177c-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="e177c-126">Katram satura vienumam atlasiet valodu un norādiet e-pasta tēmas rindu.</span><span class="sxs-lookup"><span data-stu-id="e177c-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="e177c-127">Ja e-pasta ziņojumā būs pamatteksts, pārliecinieties, ir atzīmēta izvēles rūtiņa **Ir pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="e177c-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="e177c-128">Darbības rūtī atlasiet **E-pasta ziņojums**, lai nodrošinātu e-pasta pamatteksta veidni.</span><span class="sxs-lookup"><span data-stu-id="e177c-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="e177c-129">Tālāk redzamajā attēlā parādīti daži e-pasta veidnes iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="e177c-129">The following image shows some example email template settings.</span></span>

![E-pasta veidņu iestatījumi](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="e177c-131">E-pasta notikuma izveide</span><span class="sxs-lookup"><span data-stu-id="e177c-131">Create an email event</span></span>

<span data-ttu-id="e177c-132">Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e177c-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="e177c-133">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Mazumtirdzniecības e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="e177c-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="e177c-134">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e177c-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="e177c-135">**E-pasta ID** nolaižamajā sarakstā atlasiet e-pasta veidni.</span><span class="sxs-lookup"><span data-stu-id="e177c-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="e177c-136">Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.</span><span class="sxs-lookup"><span data-stu-id="e177c-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="e177c-137">Atzīmējiet izvēles rūtiņu **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="e177c-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="e177c-138">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e177c-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e177c-139">Tālāk redzamajā attēlā parādīti daži mazumtirdzniecības notikuma paziņojumu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="e177c-139">The following image shows some example retail event notification settings.</span></span>

![Mazumtirdzniecības notikuma paziņojuma iestatījumi](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="e177c-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e177c-141">Additional resources</span></span>

[<span data-ttu-id="e177c-142">E-pasta konfigurēšana un sūtīšana</span><span class="sxs-lookup"><span data-stu-id="e177c-142">Configure and send email</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[<span data-ttu-id="e177c-143">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="e177c-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e177c-144">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="e177c-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="e177c-145">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="e177c-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
