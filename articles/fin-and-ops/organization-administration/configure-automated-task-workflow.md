---
title: Automatizētu uzdevumu konfigurēšana darbplūsmā
description: Šajā tēmā ir paskaidrots, kā konfigurēt automatizēta uzdevuma rekvizītus.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a9f37228beedafa085987668d5c89b06c6c9d61
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "365113"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="aea1c-103">Automatizētu uzdevumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="aea1c-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aea1c-104">Šajā tēmā ir paskaidrots, kā konfigurēt automatizēta uzdevuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="aea1c-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="aea1c-105">Lai konfigurētu automatizētu uzdevumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz uzdevuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="aea1c-106">Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu automatizētā uzdevuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="aea1c-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="aea1c-107">Nosaukuma piešķiršana uzdevumam</span><span class="sxs-lookup"><span data-stu-id="aea1c-107">Name the task</span></span>

<span data-ttu-id="aea1c-108">Izpildiet tālākos norādījumus, lai ievadītu automatizētā uzdevuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="aea1c-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="aea1c-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="aea1c-110">Laukā **Nosaukums** uzdevumam ievadiet unikālu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="aea1c-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="aea1c-111">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="aea1c-111">Specify when notifications are sent</span></span>

<span data-ttu-id="aea1c-112">Varat nosūtīt lietotājiem paziņojumus, kad automatizētais uzdevums ir palaists vai atcelts.</span><span class="sxs-lookup"><span data-stu-id="aea1c-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="aea1c-113">Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.</span><span class="sxs-lookup"><span data-stu-id="aea1c-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="aea1c-114">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="aea1c-115">Atzīmējiet izvēles rūtiņu pie notikumiem, lai sūtītu paziņojumus par:</span><span class="sxs-lookup"><span data-stu-id="aea1c-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="aea1c-116">**Izpildi** — paziņojumi tiek nosūtīti, kad uzdevums ir palaists.</span><span class="sxs-lookup"><span data-stu-id="aea1c-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="aea1c-117">**Atcelšanu** — paziņojumi tiek nosūtīti, kad uzdevums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="aea1c-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="aea1c-118">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="aea1c-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="aea1c-119">Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="aea1c-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="aea1c-120">Lai personalizētu paziņojumu, varat ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="aea1c-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="aea1c-121">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad paziņojums tiks parādīts lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="aea1c-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="aea1c-122">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="aea1c-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="aea1c-123">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="aea1c-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="aea1c-124">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="aea1c-125">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="aea1c-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="aea1c-126">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-126">Click **Insert**.</span></span>

6. <span data-ttu-id="aea1c-127">Lai pievienotu paziņojuma tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="aea1c-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="aea1c-128">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="aea1c-129">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="aea1c-130">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="aea1c-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="aea1c-131">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="aea1c-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="aea1c-132">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="aea1c-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="aea1c-133">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="aea1c-133">Click **Close**.</span></span>

7. <span data-ttu-id="aea1c-134">Cilnē **Adresāts** norādiet personu, kurai paziņojumi tiek nosūtīti.</span><span class="sxs-lookup"><span data-stu-id="aea1c-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="aea1c-135">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 8. darbību.</span><span class="sxs-lookup"><span data-stu-id="aea1c-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="aea1c-136">Opcija</span><span class="sxs-lookup"><span data-stu-id="aea1c-136">Option</span></span></th>
    <th><span data-ttu-id="aea1c-137">Paziņojuma adresāti</span><span class="sxs-lookup"><span data-stu-id="aea1c-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="aea1c-138">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="aea1c-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="aea1c-139">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="aea1c-139">Participant</span></span></td>
    <td><span data-ttu-id="aea1c-140">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="aea1c-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="aea1c-141">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="aea1c-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="aea1c-142">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="aea1c-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="aea1c-143">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="aea1c-143">Workflow user</span></span></td>
    <td><span data-ttu-id="aea1c-144">Lietotāji, kuri piedalās pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="aea1c-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="aea1c-145">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="aea1c-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="aea1c-146">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="aea1c-146">User</span></span></td>
    <td><span data-ttu-id="aea1c-147">Īpaši Microsoft Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="aea1c-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="aea1c-148">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="aea1c-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="aea1c-149">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="aea1c-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="aea1c-150">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="aea1c-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="aea1c-151">Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="aea1c-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>
