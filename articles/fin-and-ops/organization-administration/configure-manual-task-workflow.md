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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 98e25e1a132f0767b9c58334f177845c222c3863
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a><span data-ttu-id="00543-103">Konfigurēt manuālu uzdevumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="00543-103">Configure a manual task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="00543-104">Šajā tēmā ir paskaidrots, kā konfigurēt manuāla uzdevuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="00543-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="00543-105">Lai konfigurētu manuālu uzdevumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz uzdevuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="00543-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="00543-106">Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu manuālā uzdevuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="00543-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="00543-107">Nosaukuma piešķiršana uzdevumam</span><span class="sxs-lookup"><span data-stu-id="00543-107">Name the task</span></span>
<span data-ttu-id="00543-108">Izpildiet tālākos norādījumus, lai ievadītu manuālā uzdevuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="00543-108">Follow these steps to enter a name for the manual task.</span></span>

1.  <span data-ttu-id="00543-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="00543-110">Laukā **Nosaukums** uzdevumam ievadiet unikālu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="00543-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="00543-111">Ievadiet tēmas rindu un instrukcijas</span><span class="sxs-lookup"><span data-stu-id="00543-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="00543-112">Jums jānorāda tēmas rinda un instrukcijas lietotājiem, kuri piešķirti šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="00543-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="00543-113">Piemēram, ja konfigurējat pirkšanas pieprasījumu uzdevumu, attiecīgajam uzdevumam piešķirtais lietotājs redz tēmas rindu un instrukcijas lapā **Pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="00543-114">Tēmas rinda tiek parādīta lapā esošajā ziņojumu joslā.</span><span class="sxs-lookup"><span data-stu-id="00543-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="00543-115">Lietotājs var noklikšķināt uz ziņojumu joslā redzamās ikonas, lai skatītu instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="00543-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="00543-116">Veiciet šīs darbības, lai ievadītu tēmas rindu un instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="00543-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="00543-117">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="00543-118">Laukā **Darbplūsmas elementa tēma** ievadiet tēmas rindu.</span><span class="sxs-lookup"><span data-stu-id="00543-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="00543-119">Lai personalizētu tēmas rindu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="00543-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="00543-120">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad tēmas rinda tiks parādīta lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="00543-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="00543-121">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="00543-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="00543-122">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="00543-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="00543-123">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="00543-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="00543-124">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="00543-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="00543-125">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="00543-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="00543-126">Lai pievienotu tēmas rindas tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="00543-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="00543-127">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="00543-128">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="00543-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="00543-129">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="00543-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="00543-130">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="00543-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="00543-131">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 3. darbībā.</span><span class="sxs-lookup"><span data-stu-id="00543-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="00543-132">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="00543-132">Click **Close**.</span></span>

5.  <span data-ttu-id="00543-133">Laukā **Darbplūsmas elementa instrukcijas** ievadiet instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="00543-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="00543-134">Lai personalizētu instrukcijas, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="00543-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="00543-135">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="00543-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="00543-136">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="00543-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="00543-137">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="00543-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="00543-138">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="00543-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="00543-139">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="00543-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="00543-140">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="00543-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="00543-141">Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="00543-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="00543-142">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="00543-143">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="00543-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="00543-144">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="00543-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="00543-145">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="00543-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="00543-146">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 6. darbībā.</span><span class="sxs-lookup"><span data-stu-id="00543-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="00543-147">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="00543-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="00543-148">Uzdevuma piešķiršana</span><span class="sxs-lookup"><span data-stu-id="00543-148">Assign the task</span></span>
<span data-ttu-id="00543-149">Veiciet šīs darbības, lai norādītu personu, kurai jāpiešķir manuālais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1.  <span data-ttu-id="00543-150">Kreisajā rūtī noklikšķiniet uz **Piešķire**.</span><span class="sxs-lookup"><span data-stu-id="00543-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="00543-151">Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 3. darbību.</span><span class="sxs-lookup"><span data-stu-id="00543-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="00543-152">Opcija</span><span class="sxs-lookup"><span data-stu-id="00543-152">Option</span></span></th>
    <th><span data-ttu-id="00543-153">Lietotāji, kuriem ir piešķirts uzdevums</span><span class="sxs-lookup"><span data-stu-id="00543-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="00543-154">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="00543-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="00543-155">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="00543-155">Participant</span></span></td>
    <td><span data-ttu-id="00543-156">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="00543-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-157">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai piešķirt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="00543-158">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai piešķirt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="00543-159">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="00543-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="00543-160">Lietotāji īpašā organizācijas hierarhijā</span><span class="sxs-lookup"><span data-stu-id="00543-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-161">Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram piešķirt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="00543-162">Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons.</span><span class="sxs-lookup"><span data-stu-id="00543-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="00543-163">Šie vārdi norāda, kuriem lietotājiem var piešķirt attiecīgo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="00543-164">Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas:</span><span class="sxs-lookup"><span data-stu-id="00543-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="00543-165">Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="00543-166">Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="00543-167">Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="00543-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="00543-168">Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem uzdevums jāpiešķir:</span><span class="sxs-lookup"><span data-stu-id="00543-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="00543-169"><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — uzdevums tiek piešķirts visiem diapazonā esošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="00543-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="00543-170"><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — uzdevums tiek piešķirts tikai pēdējam lietotājam diapazonā.</span><span class="sxs-lookup"><span data-stu-id="00543-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="00543-171"><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — uzdevums netiek piešķirts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="00543-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="00543-172">Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="00543-173">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="00543-173">Workflow user</span></span></td>
    <td><span data-ttu-id="00543-174">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="00543-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="00543-175">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="00543-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="00543-176">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="00543-176">User</span></span></td>
    <td><span data-ttu-id="00543-177">Noteikti Microsoft Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="00543-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-178">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="00543-179">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="00543-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="00543-180">Atlasiet lietotājus, kuriem piešķirt uzdevumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="00543-181">Rinda</span><span class="sxs-lookup"><span data-stu-id="00543-181">Queue</span></span></td>
    <td><span data-ttu-id="00543-182">Darba vienumu rinda</span><span class="sxs-lookup"><span data-stu-id="00543-182">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-183">Pēc tam, kad ir atlasīts vienums <strong>Rinda</strong>, noklikšķiniet uz cilnes <strong>Balstīts uz rindu</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="00543-184">Lai uzdevumu piešķirtu noteiktai rindai, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="00543-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="00543-185">Sarakstā <strong>Rindas tips</strong> atlasiet <strong>Darba vienumu rindas</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="00543-186">Sarakstā <strong>Rindas nosaukums</strong> atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="00543-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="00543-187">Ja konkrētam nosacījumam jānosaka, kurai rindai uzdevums tiek piešķirts, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="00543-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="00543-188">Sarakstā <strong>Rindas tips</strong> atlasiet <strong>Nosacījuma darba vienumu rindas</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="00543-189">Sarakstā <strong>Rindas nosaukums</strong> atlasiet <strong>Nosacījumu rinda</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="00543-190">
    <strong>Piezīme.</strong> Šī opcija tiek izmantota tikai dažām darbplūsmām, piemēram, Pieteikumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="00543-190">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="00543-191">Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pabeigtu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="00543-192">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="00543-192">Select one of the following options:</span></span>
    -   <span data-ttu-id="00543-193">**Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="00543-194">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="00543-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="00543-195">**Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="00543-196">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="00543-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="00543-197">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="00543-198">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="00543-199">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigtu uzdevumu līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="00543-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="00543-200">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="00543-201">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigt uzdevumu līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="00543-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="00543-202">Ja lietotājs nepabeidz uzdevumu atvēlētajā laikā, uzdevums ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="00543-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="00543-203">Nokavētu uzdevumu var eskalēt, pamatojoties uz opcijām, kas ir atlasītas lapas apgabalā **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="00543-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="00543-204">Norādiet, kas notiek, ja uzdevums nokavēts</span><span class="sxs-lookup"><span data-stu-id="00543-204">Specify what happens when the task is overdue</span></span>
<span data-ttu-id="00543-205">Ja lietotājs nepabeidz manuālo uzdevumu atvēlētajā laikā, uzdevums ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="00543-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="00543-206">Uzdevumu, kas ir nokavēts, var eskalēt vai automātiski piešķirt citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="00543-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="00543-207">Veiciet šīs darbības, lai eskalētu uzdevumu, ja tas ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="00543-207">Follow these steps to escalate the task if it's overdue.</span></span>

1.  <span data-ttu-id="00543-208">Kreisajā rūtī noklikšķiniet uz **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="00543-208">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="00543-209">Atzīmējiet izvēles rūtiņu **Izmantot eskalācijas ceļu**, lai izveidotu eskalācijas ceļu.</span><span class="sxs-lookup"><span data-stu-id="00543-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="00543-210">Sistēma automātiski piešķirs uzdevumu lietotājiem, kuri ir norādīti eskalācijas ceļā.</span><span class="sxs-lookup"><span data-stu-id="00543-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="00543-211">Piemēram, šajā tabulā ir attēlots eskalācijas ceļš.</span><span class="sxs-lookup"><span data-stu-id="00543-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="00543-212">Secība</span><span class="sxs-lookup"><span data-stu-id="00543-212">Sequence</span></span> | <span data-ttu-id="00543-213">Eskalācijas ceļš</span><span class="sxs-lookup"><span data-stu-id="00543-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="00543-214">1</span><span class="sxs-lookup"><span data-stu-id="00543-214">1</span></span>        | <span data-ttu-id="00543-215">Piešķirt: Lindai</span><span class="sxs-lookup"><span data-stu-id="00543-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="00543-216">2</span><span class="sxs-lookup"><span data-stu-id="00543-216">2</span></span>        | <span data-ttu-id="00543-217">Piešķirt: Zanei</span><span class="sxs-lookup"><span data-stu-id="00543-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="00543-218">3</span><span class="sxs-lookup"><span data-stu-id="00543-218">3</span></span>        | <span data-ttu-id="00543-219">Pēdējā darbība: noraidīt</span><span class="sxs-lookup"><span data-stu-id="00543-219">Final action: Reject</span></span> |

    <span data-ttu-id="00543-220">Šajā piemērā sistēma piešķir nokavēto uzdevumu Lindai.</span><span class="sxs-lookup"><span data-stu-id="00543-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="00543-221">Ja Linda nepabeidz uzdevumu atvēlētajā laikā, sistēma piešķir uzdevumu Zanei.</span><span class="sxs-lookup"><span data-stu-id="00543-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="00543-222">Ja Zane nepabeidz uzdevumu atvēlētajā laikā, sistēma noraida dokumentu, kas tika iesniegts apstrādei.</span><span class="sxs-lookup"><span data-stu-id="00543-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>
3.  <span data-ttu-id="00543-223">Lai pievienotu lietotāju eskalācijas ceļam, noklikšķiniet uz **Pievienot eskalāciju**.</span><span class="sxs-lookup"><span data-stu-id="00543-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="00543-224">Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 4. darbību.</span><span class="sxs-lookup"><span data-stu-id="00543-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="00543-225">Opcija</span><span class="sxs-lookup"><span data-stu-id="00543-225">Option</span></span></th>
    <th><span data-ttu-id="00543-226">Lietotāji, kuriem tiek eskalēts uzdevums</span><span class="sxs-lookup"><span data-stu-id="00543-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="00543-227">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="00543-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="00543-228">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="00543-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="00543-229">Lietotāji īpašā organizācijas hierarhijā</span><span class="sxs-lookup"><span data-stu-id="00543-229">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-230">Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram eskalēt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="00543-231">Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons.</span><span class="sxs-lookup"><span data-stu-id="00543-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="00543-232">Šie vārdi norāda, kuriem lietotājiem var eskalēt attiecīgo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="00543-233">Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas:</span><span class="sxs-lookup"><span data-stu-id="00543-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="00543-234">Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="00543-235">Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="00543-236">Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="00543-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="00543-237">Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem uzdevums jāeskalē:</span><span class="sxs-lookup"><span data-stu-id="00543-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="00543-238"><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — uzdevums tiek eskalēts visiem diapazonā esošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="00543-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="00543-239"><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — uzdevums tiek eskalēts tikai pēdējam lietotājam diapazonā.</span><span class="sxs-lookup"><span data-stu-id="00543-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="00543-240"><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — šis uzdevums netiek eskalēts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="00543-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="00543-241">Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="00543-242">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="00543-242">Workflow user</span></span></td>
    <td><span data-ttu-id="00543-243">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="00543-243">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="00543-244">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="00543-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="00543-245">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="00543-245">User</span></span></td>
    <td><span data-ttu-id="00543-246">Noteikti Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="00543-246">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-247">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="00543-248">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="00543-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="00543-249">Atlasiet lietotājus, kuriem eskalēt uzdevumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="00543-250">Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pabeigtu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="00543-251">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="00543-251">Select one of the following options:</span></span>
    -   <span data-ttu-id="00543-252">**Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="00543-253">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="00543-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="00543-254">**Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="00543-255">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="00543-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="00543-256">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="00543-257">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="00543-258">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigtu uzdevumu līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="00543-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="00543-259">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="00543-260">Piemēram, iespējams, vēlēsities, lai lietotājs pabeigt uzdevumu līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="00543-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="00543-261">Atkārtojiet 3.–4. darbību katram lietotājam, kurš jāpievieno eskalācijas ceļam.</span><span class="sxs-lookup"><span data-stu-id="00543-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="00543-262">Jūs varat mainīt lietotāju secību.</span><span class="sxs-lookup"><span data-stu-id="00543-262">You can change the order of the users.</span></span>
6.  <span data-ttu-id="00543-263">Ja eskalācijas ceļā norādītie lietotāji nepabeidz uzdevumu atvēlētajā laikā, sistēma veic darbību ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="00543-264">Lai norādītu darbību, ko sistēma veic, atlasiet rindu **Darbība** un pēc tam cilnē **Beigu darbība** atlasiet darbību.</span><span class="sxs-lookup"><span data-stu-id="00543-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="00543-265">Norādiet, kad sistēma automātiski veic darbību ar uzdevumu</span><span class="sxs-lookup"><span data-stu-id="00543-265">Specify when the system automatically acts on the task</span></span>
<span data-ttu-id="00543-266">Varat konfigurēt sistēmu, lai tā veiktu darbību ar manuālu uzdevumu, ja tiek izpildīti konkrēti nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="00543-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="00543-267">Piemēram, uzdevumam ir nepieciešams, lai nodaļas Izdevumu atskaites dalībnieks pārskatītu čekus, kas ir iesniegti kopā ar izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="00543-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="00543-268">Saskaņā ar uzņēmuma politiku, šis uzdevums ir jāveic, ja izdevumu pārskata kopsumma ir lielāka par 100 USD.</span><span class="sxs-lookup"><span data-stu-id="00543-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="00543-269">Šādā scenārijā varat konfigurēt sistēmu, lai tā automātiski atzīmētu uzdevumu kā **Pabeigts**, ja kopsumma ir mazāka par 100.</span><span class="sxs-lookup"><span data-stu-id="00543-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="00543-270">Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar manuālo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1.  <span data-ttu-id="00543-271">Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="00543-271">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="00543-272">Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="00543-272">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="00543-273">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="00543-273">Click **Add condition**.</span></span>
4.  <span data-ttu-id="00543-274">Ievadīt nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="00543-274">Enter a condition.</span></span>
5.  <span data-ttu-id="00543-275">Ievadiet visus nepieciešamos papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="00543-275">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="00543-276">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="00543-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="00543-277">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="00543-277">Click **Test**.</span></span>
    2.  <span data-ttu-id="00543-278">Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="00543-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="00543-279">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="00543-279">Click **Test**.</span></span> <span data-ttu-id="00543-280">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="00543-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="00543-281">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="00543-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7.  <span data-ttu-id="00543-282">Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="00543-283">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="00543-283">Specify when notifications are sent</span></span>
<span data-ttu-id="00543-284">Varat lietotājiem nosūtīt paziņojumus, kad manuālais uzdevums ir deleģēts, eskalēts, pabeigts vai noraidīts vai kad ir pieprasītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="00543-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="00543-285">Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.</span><span class="sxs-lookup"><span data-stu-id="00543-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="00543-286">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-286">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="00543-287">Atzīmējiet izvēles rūtiņu pie notikumiem, par kuriem tiek sūtīti paziņojumi:</span><span class="sxs-lookup"><span data-stu-id="00543-287">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="00543-288">**Deleģēt** — uzdevums ir piešķirts citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="00543-288">**Delegate** – The task has been assigned to another user.</span></span>
    -   <span data-ttu-id="00543-289">**Eskalēt** — piešķirtais lietotājs nav pabeidzis uzdevumu atvēlētajā laikā.</span><span class="sxs-lookup"><span data-stu-id="00543-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    -   <span data-ttu-id="00543-290">**Pabeigt** — piešķirtais lietotājs ir pabeidzis uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-290">**Complete** – The assigned user has completed the task.</span></span>
    -   <span data-ttu-id="00543-291">**Noraidīt** — piešķirtais lietotājs ir noraidījis iesniegto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="00543-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    -   <span data-ttu-id="00543-292">**Pieprasīt izmaiņas** — piešķirtais lietotājs ir pieprasījis izmaiņas iesniegtajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="00543-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3.  <span data-ttu-id="00543-293">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="00543-293">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="00543-294">Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="00543-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="00543-295">Lai personalizētu paziņojumu, varat ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="00543-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="00543-296">Vietturi tiks aizvietoti ar atbilstošu informāciju, kad paziņojums tiks parādīts lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="00543-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="00543-297">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="00543-297">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="00543-298">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="00543-298">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="00543-299">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="00543-299">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="00543-300">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="00543-300">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="00543-301">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="00543-301">Click **Insert**.</span></span>

6.  <span data-ttu-id="00543-302">Lai pievienotu paziņojuma tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="00543-302">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="00543-303">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-303">Click **Translations**.</span></span>
    2.  <span data-ttu-id="00543-304">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="00543-304">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="00543-305">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="00543-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="00543-306">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="00543-306">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="00543-307">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="00543-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="00543-308">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="00543-308">Click **Close**.</span></span>

7.  <span data-ttu-id="00543-309">Cilnē **Adresāts** norādiet personu, kurai paziņojumi tiek nosūtīti.</span><span class="sxs-lookup"><span data-stu-id="00543-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="00543-310">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 8. darbību.</span><span class="sxs-lookup"><span data-stu-id="00543-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="00543-311">Opcija</span><span class="sxs-lookup"><span data-stu-id="00543-311">Option</span></span></th>
    <th><span data-ttu-id="00543-312">Paziņojuma adresāti</span><span class="sxs-lookup"><span data-stu-id="00543-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="00543-313">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="00543-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="00543-314">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="00543-314">Participant</span></span></td>
    <td><span data-ttu-id="00543-315">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="00543-315">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-316">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="00543-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="00543-317">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="00543-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="00543-318">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="00543-318">Workflow user</span></span></td>
    <td><span data-ttu-id="00543-319">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="00543-319">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="00543-320">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="00543-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="00543-321">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="00543-321">User</span></span></td>
    <td><span data-ttu-id="00543-322">Noteikti Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="00543-322">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="00543-323">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="00543-324">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="00543-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="00543-325">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="00543-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="00543-326">Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="00543-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="00543-327">Laika robežas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="00543-327">Set a time limit</span></span>
<span data-ttu-id="00543-328">Veiciet šīs darbības, ja manuālais uzdevums ir jāpabeidz noteiktā laikā.</span><span class="sxs-lookup"><span data-stu-id="00543-328">Follow these steps if the manual task must be completed in a specific time.</span></span> 

<span data-ttu-id="00543-329">**Piezīme.** Šajā procedūrā izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas lapas apgabalos **Piešķire** un **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="00543-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="00543-330">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="00543-331">Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas elementa laika ierobežojumu**.</span><span class="sxs-lookup"><span data-stu-id="00543-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="00543-332">Laukā **Ilgums** norādiet, kad uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="00543-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="00543-333">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="00543-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="00543-334">**Stundas** — ievadiet stundu skaitu, kuru laikā uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="00543-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="00543-335">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="00543-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="00543-336">**Dienas** — ievadiet dienu skaitu, kuru laikā uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="00543-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="00543-337">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="00543-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="00543-338">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā uzdevums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="00543-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    -   <span data-ttu-id="00543-339">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="00543-340">Piemēram, iespējams, vēlēsieties, lai uzdevums tiktu pabeigts līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="00543-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="00543-341">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz uzdevums.</span><span class="sxs-lookup"><span data-stu-id="00543-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="00543-342">Piemēram, iespējams, vēlēsieties, lai uzdevums tiktu pabeigts līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="00543-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="00543-343">Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="00543-344">Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.</span><span class="sxs-lookup"><span data-stu-id="00543-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="00543-345">Norādiet, kuras darbības ir pieejamas lietotājam</span><span class="sxs-lookup"><span data-stu-id="00543-345">Specify which actions are available to the user</span></span>
<span data-ttu-id="00543-346">Kad manuālais uzdevums ir piešķirts lietotājam, lietotājam ir jāveic darbība ar šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="00543-347">Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="00543-347">Follow these steps to specify which actions the user can take on the task.</span></span> <span data-ttu-id="00543-348">**Piezīme.** Pieejamās darbības var atšķirties atkarībā no tā, kā uzdevums projektēts.</span><span class="sxs-lookup"><span data-stu-id="00543-348">**Note:** The actions that are available vary, depending on the design of the task.</span></span>

1.  <span data-ttu-id="00543-349">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="00543-349">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="00543-350">Atzīmējiet izvēles rūtiņu **Pabeigts**, lai lietotājs varētu atzīmēt šo uzdevumu, izmantojot vienumu **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="00543-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3.  <span data-ttu-id="00543-351">Atzīmējiet izvēles rūtiņu **Noraidīt**, lai lietotājs varētu noraidīt iesniegto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="00543-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4.  <span data-ttu-id="00543-352">Atzīmējiet izvēles rūtiņu **Pieprasīt izmaiņas**, lai lietotājs varētu pieprasīt izmaiņu veikšanu iesniegtajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="00543-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5.  <span data-ttu-id="00543-353">Atzīmējiet izvēles rūtiņu **Deleģēt**, lai lietotājs varētu piešķirt uzdevumu citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="00543-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6.  <span data-ttu-id="00543-354">Atzīmējiet izvēles rūtiņu **Piešķirt no jauna**, lai lietotājs varētu piešķirt no jauna uzdevumu citam lietotājam darba vienumu rindā.</span><span class="sxs-lookup"><span data-stu-id="00543-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7.  <span data-ttu-id="00543-355">Atzīmējiet izvēles rūtiņu **Nodot izpildei**, lai lietotājs varētu piešķirt no jauna uzdevumu darba vienumu rindā.</span><span class="sxs-lookup"><span data-stu-id="00543-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="00543-356">Pēc tam uzdevumu var pabeigt cits lietotājs.</span><span class="sxs-lookup"><span data-stu-id="00543-356">Another user can then complete the task.</span></span>





