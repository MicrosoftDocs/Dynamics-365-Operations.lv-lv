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
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113809"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="0070a-103">E-pasta paziņojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0070a-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0070a-104">Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0070a-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0070a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="0070a-105">Overview</span></span>

<span data-ttu-id="0070a-106">Pirms kanālu izveides jums vajadzēs iestatīt profilu, lai nodrošinātu, ka dažādiem notikumiem, piemēram, pasūtījuma izveidei, pasūtījuma nosūtīšanas statusam un maksājuma kļūmei, var nosūtīt e-pasta paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="0070a-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="0070a-107">Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="0070a-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="0070a-108">E-pasta paziņojumu profila izveide</span><span class="sxs-lookup"><span data-stu-id="0070a-108">Create an email notification profile</span></span>

<span data-ttu-id="0070a-109">Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0070a-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="0070a-110">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \>Komercijas e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="0070a-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="0070a-111">Darbību rūtī noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0070a-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="0070a-112">Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="0070a-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="0070a-113">Ievadiet atbilstošu aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0070a-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="0070a-114">Iestatiet slēdzi **Aktīvs** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0070a-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="0070a-115">E-pasta veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="0070a-115">Create an email template</span></span>

<span data-ttu-id="0070a-116">Lai varētu izveidot e-pasta paziņojumu, jāizveido organizācijas e-pasta veidne, kurā iekļauta sūtītāju e-pasta informācija un e-pasta veidne.</span><span class="sxs-lookup"><span data-stu-id="0070a-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="0070a-117">Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0070a-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="0070a-118">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Organizāciju e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="0070a-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="0070a-119">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0070a-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="0070a-120">Laukā **E-pasta ID** ievadiet ID, lai palīdzētu identificēt šo veidni.</span><span class="sxs-lookup"><span data-stu-id="0070a-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="0070a-121">Laukā **Sūtītāja nosaukums** ievadiet sūtītāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0070a-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="0070a-122">Ievadiet jēgpilnu aprakstu laukā **Epasta apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0070a-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="0070a-123">Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāju e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="0070a-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="0070a-124">Sadaļā **Vispārīgi** aizpildiet visu izvēles informāciju (piemēram, e-pasta prioritāte).</span><span class="sxs-lookup"><span data-stu-id="0070a-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="0070a-125">Paplašiniet sadaļu **E-pasta ziņojuma saturs** un atlasiet **Jauns**, lai izveidotu veidnes saturu.</span><span class="sxs-lookup"><span data-stu-id="0070a-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="0070a-126">Katram satura vienumam atlasiet valodu un norādiet e-pasta tēmas rindu.</span><span class="sxs-lookup"><span data-stu-id="0070a-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="0070a-127">Ja e-pasta ziņojumā būs pamatteksts, pārliecinieties, ir atzīmēta izvēles rūtiņa **Ir pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="0070a-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="0070a-128">Darbības rūtī atlasiet **E-pasta ziņojums**, lai nodrošinātu e-pasta pamatteksta veidni.</span><span class="sxs-lookup"><span data-stu-id="0070a-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="0070a-129">Tālāk redzamajā attēlā parādīti daži e-pasta veidnes iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="0070a-129">The following image shows some example email template settings.</span></span>

![E-pasta veidņu iestatījumi](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="0070a-131">E-pasta notikuma izveide</span><span class="sxs-lookup"><span data-stu-id="0070a-131">Create an email event</span></span>

<span data-ttu-id="0070a-132">Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0070a-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="0070a-133">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \>Komercijas e-pasta paziņojumu profils**.</span><span class="sxs-lookup"><span data-stu-id="0070a-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="0070a-134">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0070a-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="0070a-135">**E-pasta ID** nolaižamajā sarakstā atlasiet e-pasta veidni.</span><span class="sxs-lookup"><span data-stu-id="0070a-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="0070a-136">Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.</span><span class="sxs-lookup"><span data-stu-id="0070a-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="0070a-137">Atzīmējiet izvēles rūtiņu **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="0070a-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="0070a-138">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0070a-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="0070a-139">Tālāk redzamajā attēlā parādīti daži notikuma paziņojumu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="0070a-139">The following image shows some example event notification settings.</span></span>

![Notikuma paziņojuma iestatījumi](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="0070a-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0070a-141">Additional resources</span></span>

[<span data-ttu-id="0070a-142">E-pasta konfigurēšana un sūtīšana</span><span class="sxs-lookup"><span data-stu-id="0070a-142">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="0070a-143">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="0070a-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="0070a-144">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="0070a-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="0070a-145">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="0070a-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
