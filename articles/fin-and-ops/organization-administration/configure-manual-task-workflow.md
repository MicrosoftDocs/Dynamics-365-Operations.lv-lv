---
title: "Konfigurēt manuālu uzdevumu darbplūsmā"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt manuāla uzdevuma rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8cda2ea6e75b3d33160599cc4334a7b4d2612815
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="configure-a-manual-task-in-a-workflow"></a><span data-ttu-id="923b9-103">Konfigurēt manuālu uzdevumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="923b9-103">Configure a manual task in a workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="923b9-104">Šajā tēmā ir paskaidrots, kā konfigurēt manuāla uzdevuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="923b9-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="923b9-105">Lai konfigurētu manuālu uzdevumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz uzdevuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="923b9-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="923b9-106">Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu manuālā uzdevuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="923b9-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="923b9-107">Nosaukuma piešķiršana uzdevumam</span><span class="sxs-lookup"><span data-stu-id="923b9-107">Name the task</span></span>
<span data-ttu-id="923b9-108">Izpildiet tālākos norādījumus, lai ievadītu manuālā uzdevuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-108">Follow these steps to enter a name for the manual task.</span></span>

1.  <span data-ttu-id="923b9-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="923b9-110">Laukā **Nosaukums** uzdevumam ievadiet unikālu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="923b9-111">Ievadiet tēmas rindu un instrukcijas</span><span class="sxs-lookup"><span data-stu-id="923b9-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="923b9-112">Jums jānorāda tēmas rinda un instrukcijas lietotājiem, kuri piešķirti šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="923b9-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="923b9-113">Piemēram, ja konfigurējat pirkšanas pieprasījumu uzdevumu, attiecīgajam uzdevumam piešķirtais lietotājs redz tēmas rindu un instrukcijas lapā **Pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="923b9-114">Tēmas rinda tiek parādīta lapā esošajā ziņojumu joslā.</span><span class="sxs-lookup"><span data-stu-id="923b9-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="923b9-115">Lietotājs var noklikšķināt uz ziņojumu joslā redzamās ikonas, lai skatītu instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="923b9-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="923b9-116">Veiciet šīs darbības, lai ievadītu tēmas rindu un instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="923b9-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="923b9-117">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="923b9-118">Laukā **Darbplūsmas elementa tēma** ievadiet tēmas rindu.</span><span class="sxs-lookup"><span data-stu-id="923b9-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="923b9-119">Lai personalizētu tēmas rindu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="923b9-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="923b9-120">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad tēmas rinda tiks parādīta lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="923b9-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="923b9-121">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="923b9-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="923b9-122">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="923b9-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="923b9-123">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="923b9-124">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="923b9-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="923b9-125">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="923b9-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="923b9-126">Lai pievienotu tēmas rindas tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="923b9-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="923b9-127">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="923b9-128">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="923b9-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="923b9-129">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="923b9-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="923b9-130">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="923b9-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="923b9-131">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 3. darbībā.</span><span class="sxs-lookup"><span data-stu-id="923b9-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="923b9-132">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="923b9-132">Click **Close**.</span></span>

5.  <span data-ttu-id="923b9-133">Laukā **Darbplūsmas elementa instrukcijas** ievadiet instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="923b9-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="923b9-134">Lai personalizētu instrukcijas, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="923b9-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="923b9-135">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="923b9-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="923b9-136">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="923b9-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="923b9-137">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="923b9-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="923b9-138">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="923b9-139">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="923b9-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="923b9-140">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="923b9-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="923b9-141">Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="923b9-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="923b9-142">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="923b9-143">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="923b9-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="923b9-144">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="923b9-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="923b9-145">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="923b9-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="923b9-146">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 6. darbībā.</span><span class="sxs-lookup"><span data-stu-id="923b9-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="923b9-147">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="923b9-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="923b9-148">Uzdevuma piešķiršana</span><span class="sxs-lookup"><span data-stu-id="923b9-148">Assign the task</span></span>
<span data-ttu-id="923b9-149">Veiciet šīs darbības, lai norādītu personu, kurai jāpiešķir manuālais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1.  <span data-ttu-id="923b9-150">Kreisajā rūtī noklikšķiniet uz **Piešķire**.</span><span class="sxs-lookup"><span data-stu-id="923b9-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="923b9-151">Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 3. darbību.</span><span class="sxs-lookup"><span data-stu-id="923b9-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="923b9-152">Opcija</span><span class="sxs-lookup"><span data-stu-id="923b9-152">Option</span></span></th>
    <th><span data-ttu-id="923b9-153">Lietotāji, kuriem ir piešķirts uzdevums</span><span class="sxs-lookup"><span data-stu-id="923b9-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="923b9-154">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="923b9-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="923b9-155">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="923b9-155">Participant</span></span></td>
    <td><span data-ttu-id="923b9-156">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="923b9-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-157">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai piešķirt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="923b9-158">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai piešķirt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="923b9-159">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="923b9-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="923b9-160">Lietotāji īpašā organizācijas hierarhijā</span><span class="sxs-lookup"><span data-stu-id="923b9-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-161">Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram piešķirt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="923b9-162">Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons.</span><span class="sxs-lookup"><span data-stu-id="923b9-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="923b9-163">Šie vārdi norāda, kuriem lietotājiem var piešķirt attiecīgo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="923b9-164">Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas:</span><span class="sxs-lookup"><span data-stu-id="923b9-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="923b9-165">Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="923b9-166">Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="923b9-167">Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="923b9-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="923b9-168">Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem uzdevums jāpiešķir:</span><span class="sxs-lookup"><span data-stu-id="923b9-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="923b9-169"><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — uzdevums tiek piešķirts visiem diapazonā esošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="923b9-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="923b9-170"><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — uzdevums tiek piešķirts tikai pēdējam lietotājam diapazonā.</span><span class="sxs-lookup"><span data-stu-id="923b9-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="923b9-171"><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — uzdevums netiek piešķirts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="923b9-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="923b9-172">Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="923b9-173">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="923b9-173">Workflow user</span></span></td>
    <td><span data-ttu-id="923b9-174">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="923b9-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="923b9-175">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="923b9-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="923b9-176">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="923b9-176">User</span></span></td>
    <td><span data-ttu-id="923b9-177">Noteikti Microsoft Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="923b9-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-178">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="923b9-179">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="923b9-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="923b9-180">Atlasiet lietotājus, kuriem piešķirt uzdevumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="923b9-181">Rinda</span><span class="sxs-lookup"><span data-stu-id="923b9-181">Queue</span></span></td>
    <td><span data-ttu-id="923b9-182">Darba vienumu rinda</span><span class="sxs-lookup"><span data-stu-id="923b9-182">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-183">Pēc tam, kad ir atlasīts vienums <strong>Rinda</strong>, noklikšķiniet uz cilnes <strong>Balstīts uz rindu</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="923b9-184">Lai uzdevumu piešķirtu noteiktai rindai, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="923b9-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="923b9-185">Sarakstā <strong>Rindas tips</strong> atlasiet <strong>Darba vienumu rindas</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="923b9-186">Sarakstā <strong>Rindas nosaukums</strong> atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="923b9-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="923b9-187">Ja konkrētam nosacījumam jānosaka, kurai rindai uzdevums tiek piešķirts, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="923b9-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="923b9-188">Sarakstā <strong>Rindas tips</strong> atlasiet <strong>Nosacījuma darba vienumu rindas</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="923b9-189">Sarakstā <strong>Rindas nosaukums</strong> atlasiet <strong>Nosacījumu rinda</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="923b9-190">
    <strong>Piezīme.</strong> Šī opcija tiek izmantota tikai dažām darbplūsmām, piemēram, Pieteikumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="923b9-190">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="923b9-191">Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pabeigtu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="923b9-192">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="923b9-192">Select one of the following options:</span></span>
    -   <span data-ttu-id="923b9-193">**Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="923b9-194">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="923b9-195">**Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="923b9-196">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="923b9-197">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="923b9-198">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="923b9-199">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigtu uzdevumu līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="923b9-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="923b9-200">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="923b9-201">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigt uzdevumu līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="923b9-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="923b9-202">Ja lietotājs nepabeidz uzdevumu atvēlētajā laikā, uzdevums ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="923b9-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="923b9-203">Nokavētu uzdevumu var eskalēt, pamatojoties uz opcijām, kas ir atlasītas lapas apgabalā **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="923b9-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="923b9-204">Norādiet, kas notiek, ja uzdevums nokavēts</span><span class="sxs-lookup"><span data-stu-id="923b9-204">Specify what happens when the task is overdue</span></span>
<span data-ttu-id="923b9-205">Ja lietotājs nepabeidz manuālo uzdevumu atvēlētajā laikā, uzdevums ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="923b9-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="923b9-206">Uzdevumu, kas ir nokavēts, var eskalēt vai automātiski piešķirt citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="923b9-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="923b9-207">Veiciet šīs darbības, lai eskalētu uzdevumu, ja tas ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="923b9-207">Follow these steps to escalate the task if it's overdue.</span></span>

1.  <span data-ttu-id="923b9-208">Kreisajā rūtī noklikšķiniet uz **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="923b9-208">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="923b9-209">Atzīmējiet izvēles rūtiņu **Izmantot eskalācijas ceļu**, lai izveidotu eskalācijas ceļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="923b9-210">Sistēma automātiski piešķirs uzdevumu lietotājiem, kuri ir norādīti eskalācijas ceļā.</span><span class="sxs-lookup"><span data-stu-id="923b9-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="923b9-211">Piemēram, šajā tabulā ir attēlots eskalācijas ceļš.</span><span class="sxs-lookup"><span data-stu-id="923b9-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="923b9-212">Secība</span><span class="sxs-lookup"><span data-stu-id="923b9-212">Sequence</span></span> | <span data-ttu-id="923b9-213">Eskalācijas ceļš</span><span class="sxs-lookup"><span data-stu-id="923b9-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="923b9-214">1</span><span class="sxs-lookup"><span data-stu-id="923b9-214">1</span></span>        | <span data-ttu-id="923b9-215">Piešķirt: Lindai</span><span class="sxs-lookup"><span data-stu-id="923b9-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="923b9-216">2</span><span class="sxs-lookup"><span data-stu-id="923b9-216">2</span></span>        | <span data-ttu-id="923b9-217">Piešķirt: Zanei</span><span class="sxs-lookup"><span data-stu-id="923b9-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="923b9-218">3</span><span class="sxs-lookup"><span data-stu-id="923b9-218">3</span></span>        | <span data-ttu-id="923b9-219">Pēdējā darbība: noraidīt</span><span class="sxs-lookup"><span data-stu-id="923b9-219">Final action: Reject</span></span> |

    <span data-ttu-id="923b9-220">Šajā piemērā sistēma piešķir nokavēto uzdevumu Lindai.</span><span class="sxs-lookup"><span data-stu-id="923b9-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="923b9-221">Ja Linda nepabeidz uzdevumu atvēlētajā laikā, sistēma piešķir uzdevumu Zanei.</span><span class="sxs-lookup"><span data-stu-id="923b9-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="923b9-222">Ja Zane nepabeidz uzdevumu atvēlētajā laikā, sistēma noraida dokumentu, kas tika iesniegts apstrādei.</span><span class="sxs-lookup"><span data-stu-id="923b9-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>
3.  <span data-ttu-id="923b9-223">Lai pievienotu lietotāju eskalācijas ceļam, noklikšķiniet uz **Pievienot eskalāciju**.</span><span class="sxs-lookup"><span data-stu-id="923b9-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="923b9-224">Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 4. darbību.</span><span class="sxs-lookup"><span data-stu-id="923b9-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="923b9-225">Opcija</span><span class="sxs-lookup"><span data-stu-id="923b9-225">Option</span></span></th>
    <th><span data-ttu-id="923b9-226">Lietotāji, kuriem tiek eskalēts uzdevums</span><span class="sxs-lookup"><span data-stu-id="923b9-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="923b9-227">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="923b9-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="923b9-228">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="923b9-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="923b9-229">Lietotāji īpašā organizācijas hierarhijā</span><span class="sxs-lookup"><span data-stu-id="923b9-229">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-230">Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram eskalēt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="923b9-231">Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons.</span><span class="sxs-lookup"><span data-stu-id="923b9-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="923b9-232">Šie vārdi norāda, kuriem lietotājiem var eskalēt attiecīgo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="923b9-233">Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas:</span><span class="sxs-lookup"><span data-stu-id="923b9-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="923b9-234">Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="923b9-235">Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="923b9-236">Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="923b9-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="923b9-237">Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem uzdevums jāeskalē:</span><span class="sxs-lookup"><span data-stu-id="923b9-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="923b9-238"><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — uzdevums tiek eskalēts visiem diapazonā esošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="923b9-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="923b9-239"><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — uzdevums tiek eskalēts tikai pēdējam lietotājam diapazonā.</span><span class="sxs-lookup"><span data-stu-id="923b9-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="923b9-240"><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — šis uzdevums netiek eskalēts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="923b9-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="923b9-241">Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="923b9-242">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="923b9-242">Workflow user</span></span></td>
    <td><span data-ttu-id="923b9-243">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="923b9-243">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="923b9-244">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="923b9-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="923b9-245">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="923b9-245">User</span></span></td>
    <td><span data-ttu-id="923b9-246">Noteikti Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="923b9-246">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-247">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="923b9-248">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="923b9-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="923b9-249">Atlasiet lietotājus, kuriem eskalēt uzdevumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="923b9-250">Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pabeigtu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="923b9-251">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="923b9-251">Select one of the following options:</span></span>
    -   <span data-ttu-id="923b9-252">**Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="923b9-253">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="923b9-254">**Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="923b9-255">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="923b9-256">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="923b9-257">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="923b9-258">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigtu uzdevumu līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="923b9-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="923b9-259">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="923b9-260">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigt uzdevumu līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="923b9-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="923b9-261">Atkārtojiet 3.–4. darbību katram lietotājam, kurš jāpievieno eskalācijas ceļam.</span><span class="sxs-lookup"><span data-stu-id="923b9-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="923b9-262">Jūs varat mainīt lietotāju secību.</span><span class="sxs-lookup"><span data-stu-id="923b9-262">You can change the order of the users.</span></span>
6.  <span data-ttu-id="923b9-263">Ja eskalācijas ceļā norādītie lietotāji nepabeidz uzdevumu atvēlētajā laikā, sistēma veic darbību ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="923b9-264">Lai norādītu darbību, ko sistēma veic, atlasiet rindu **Darbība** un pēc tam cilnē **Beigu darbība** atlasiet darbību.</span><span class="sxs-lookup"><span data-stu-id="923b9-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="923b9-265">Norādiet, kad sistēma automātiski veic darbību ar uzdevumu</span><span class="sxs-lookup"><span data-stu-id="923b9-265">Specify when the system automatically acts on the task</span></span>
<span data-ttu-id="923b9-266">Varat konfigurēt sistēmu, lai tā veiktu darbību ar manuālu uzdevumu, ja tiek izpildīti konkrēti nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="923b9-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="923b9-267">Piemēram, uzdevumam ir nepieciešams, lai nodaļas Izdevumu atskaites dalībnieks pārskatītu čekus, kas ir iesniegti kopā ar izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="923b9-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="923b9-268">Saskaņā ar uzņēmuma politiku, šis uzdevums ir jāveic, ja izdevumu pārskata kopsumma ir lielāka par 100 USD.</span><span class="sxs-lookup"><span data-stu-id="923b9-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="923b9-269">Šādā scenārijā varat konfigurēt sistēmu, lai tā automātiski atzīmētu uzdevumu kā **Pabeigts**, ja kopsumma ir mazāka par 100.</span><span class="sxs-lookup"><span data-stu-id="923b9-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="923b9-270">Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar manuālo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1.  <span data-ttu-id="923b9-271">Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="923b9-271">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="923b9-272">Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="923b9-272">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="923b9-273">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="923b9-273">Click **Add condition**.</span></span>
4.  <span data-ttu-id="923b9-274">Ievadīt nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-274">Enter a condition.</span></span>
5.  <span data-ttu-id="923b9-275">Ievadiet visus nepieciešamos papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="923b9-275">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="923b9-276">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="923b9-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="923b9-277">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="923b9-277">Click **Test**.</span></span>
    2.  <span data-ttu-id="923b9-278">Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="923b9-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="923b9-279">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="923b9-279">Click **Test**.</span></span> <span data-ttu-id="923b9-280">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="923b9-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="923b9-281">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="923b9-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7.  <span data-ttu-id="923b9-282">Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="923b9-283">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="923b9-283">Specify when notifications are sent</span></span>
<span data-ttu-id="923b9-284">Varat lietotājiem nosūtīt paziņojumus, kad manuālais uzdevums ir deleģēts, eskalēts, pabeigts vai noraidīts vai kad ir pieprasītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="923b9-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="923b9-285">Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.</span><span class="sxs-lookup"><span data-stu-id="923b9-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="923b9-286">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-286">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="923b9-287">Atzīmējiet izvēles rūtiņu pie notikumiem, par kuriem tiek sūtīti paziņojumi:</span><span class="sxs-lookup"><span data-stu-id="923b9-287">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="923b9-288">**Deleģēt** — uzdevums ir piešķirts citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="923b9-288">**Delegate** – The task has been assigned to another user.</span></span>
    -   <span data-ttu-id="923b9-289">**Eskalēt** — piešķirtais lietotājs nav pabeidzis uzdevumu atvēlētajā laikā.</span><span class="sxs-lookup"><span data-stu-id="923b9-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    -   <span data-ttu-id="923b9-290">**Pabeigt** — piešķirtais lietotājs ir pabeidzis uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-290">**Complete** – The assigned user has completed the task.</span></span>
    -   <span data-ttu-id="923b9-291">**Noraidīt** — piešķirtais lietotājs ir noraidījis iesniegto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="923b9-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    -   <span data-ttu-id="923b9-292">**Pieprasīt izmaiņas** — piešķirtais lietotājs ir pieprasījis izmaiņas iesniegtajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="923b9-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3.  <span data-ttu-id="923b9-293">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="923b9-293">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="923b9-294">Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="923b9-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="923b9-295">Lai personalizētu paziņojumu, varat ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="923b9-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="923b9-296">Vietturi tiks aizvietoti ar atbilstošu informāciju, kad paziņojums tiks parādīts lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="923b9-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="923b9-297">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="923b9-297">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="923b9-298">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="923b9-298">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="923b9-299">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-299">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="923b9-300">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="923b9-300">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="923b9-301">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="923b9-301">Click **Insert**.</span></span>

6.  <span data-ttu-id="923b9-302">Lai pievienotu paziņojuma tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="923b9-302">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="923b9-303">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-303">Click **Translations**.</span></span>
    2.  <span data-ttu-id="923b9-304">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="923b9-304">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="923b9-305">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="923b9-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="923b9-306">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="923b9-306">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="923b9-307">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="923b9-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="923b9-308">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="923b9-308">Click **Close**.</span></span>

7.  <span data-ttu-id="923b9-309">Cilnē **Adresāts** norādiet personu, kurai paziņojumi tiek nosūtīti.</span><span class="sxs-lookup"><span data-stu-id="923b9-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="923b9-310">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 8. darbību.</span><span class="sxs-lookup"><span data-stu-id="923b9-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="923b9-311">Opcija</span><span class="sxs-lookup"><span data-stu-id="923b9-311">Option</span></span></th>
    <th><span data-ttu-id="923b9-312">Paziņojuma adresāti</span><span class="sxs-lookup"><span data-stu-id="923b9-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="923b9-313">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="923b9-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="923b9-314">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="923b9-314">Participant</span></span></td>
    <td><span data-ttu-id="923b9-315">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="923b9-315">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-316">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="923b9-317">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="923b9-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="923b9-318">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="923b9-318">Workflow user</span></span></td>
    <td><span data-ttu-id="923b9-319">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="923b9-319">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="923b9-320">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="923b9-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="923b9-321">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="923b9-321">User</span></span></td>
    <td><span data-ttu-id="923b9-322">Noteikti Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="923b9-322">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="923b9-323">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="923b9-324">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="923b9-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="923b9-325">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="923b9-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="923b9-326">Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="923b9-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="923b9-327">Laika robežas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="923b9-327">Set a time limit</span></span>
<span data-ttu-id="923b9-328">Veiciet šīs darbības, ja manuālais uzdevums ir jāpabeidz noteiktā laikā.</span><span class="sxs-lookup"><span data-stu-id="923b9-328">Follow these steps if the manual task must be completed in a specific time.</span></span> 

<span data-ttu-id="923b9-329">**Piezīme.** Šajā procedūrā izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas lapas apgabalos **Piešķire** un **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="923b9-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="923b9-330">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="923b9-331">Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas elementa laika ierobežojumu**.</span><span class="sxs-lookup"><span data-stu-id="923b9-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="923b9-332">Laukā **Ilgums** norādiet, kad uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="923b9-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="923b9-333">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="923b9-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="923b9-334">**Stundas** — ievadiet stundu skaitu, kuru laikā uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="923b9-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="923b9-335">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="923b9-336">**Dienas** — ievadiet dienu skaitu, kuru laikā uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="923b9-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="923b9-337">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="923b9-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="923b9-338">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="923b9-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    -   <span data-ttu-id="923b9-339">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="923b9-340">Piemēram, iespējams, vēlēsieties, lai uzdevums tiktu pabeigts līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="923b9-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="923b9-341">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="923b9-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="923b9-342">Piemēram, iespējams, vēlēsieties, lai uzdevums tiktu pabeigts līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="923b9-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="923b9-343">Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="923b9-344">Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.</span><span class="sxs-lookup"><span data-stu-id="923b9-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="923b9-345">Norādiet, kuras darbības ir pieejamas lietotājam</span><span class="sxs-lookup"><span data-stu-id="923b9-345">Specify which actions are available to the user</span></span>
<span data-ttu-id="923b9-346">Kad manuālais uzdevums ir piešķirts lietotājam, lietotājam ir jāveic darbība ar šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="923b9-347">Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="923b9-347">Follow these steps to specify which actions the user can take on the task.</span></span> <span data-ttu-id="923b9-348">**Piezīme.** Pieejamās darbības var atšķirties atkarībā no tā, kā uzdevums projektēts.</span><span class="sxs-lookup"><span data-stu-id="923b9-348">**Note:** The actions that are available vary, depending on the design of the task.</span></span>

1.  <span data-ttu-id="923b9-349">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="923b9-349">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="923b9-350">Atzīmējiet izvēles rūtiņu **Pabeigts**, lai lietotājs varētu atzīmēt šo uzdevumu, izmantojot vienumu **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="923b9-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3.  <span data-ttu-id="923b9-351">Atzīmējiet izvēles rūtiņu **Noraidīt**, lai lietotājs varētu noraidīt iesniegto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="923b9-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4.  <span data-ttu-id="923b9-352">Atzīmējiet izvēles rūtiņu **Pieprasīt izmaiņas**, lai lietotājs varētu pieprasīt izmaiņu veikšanu iesniegtajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="923b9-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5.  <span data-ttu-id="923b9-353">Atzīmējiet izvēles rūtiņu **Deleģēt**, lai lietotājs varētu piešķirt uzdevumu citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="923b9-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6.  <span data-ttu-id="923b9-354">Atzīmējiet izvēles rūtiņu **Piešķirt no jauna**, lai lietotājs varētu piešķirt no jauna uzdevumu citam lietotājam darba vienumu rindā.</span><span class="sxs-lookup"><span data-stu-id="923b9-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7.  <span data-ttu-id="923b9-355">Atzīmējiet izvēles rūtiņu **Nodot izpildei**, lai lietotājs varētu piešķirt no jauna uzdevumu darba vienumu rindā.</span><span class="sxs-lookup"><span data-stu-id="923b9-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="923b9-356">Pēc tam uzdevumu var pabeigt cits lietotājs.</span><span class="sxs-lookup"><span data-stu-id="923b9-356">Another user can then complete the task.</span></span>





