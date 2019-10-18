---
title: Apstiprināšanas procesu konfigurēšana darbplūsmā
description: Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus.
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
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09d09464eae932bf9caf4f2ea38cbbb3b4f0162
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190216"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="b29f9-103">Apstiprināšanas procesu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="b29f9-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b29f9-104">Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="b29f9-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="b29f9-105">Lai konfigurētu apstiprināšanas procesu, darbplūsmas redaktorā ar peles labo pogu noklikšķiniet uz apstiprināšanas elementa un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="b29f9-106">Nosaukuma piešķiršana apstiprināšanas procesam</span><span class="sxs-lookup"><span data-stu-id="b29f9-106">Name the approval process</span></span>

<span data-ttu-id="b29f9-107">Veiciet šīs darbības, lai ievadītu apstiprināšanas procesa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="b29f9-108">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b29f9-109">Laukā **Nosaukums** ievadiet unikālu apstiprināšanas procesa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="b29f9-110">Norādiet, kad sistēma automātiski veic darbību ar dokumentu</span><span class="sxs-lookup"><span data-stu-id="b29f9-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="b29f9-111">Varat konfigurēt, lai sistēma automātiski rīkotos ar dokumentu, ja ir izpildīti konkrēti nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="b29f9-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="b29f9-112">Piemēram, sistēma var apstiprināt izdevumu pārskatus, kuros kopējās summas ir mazākas par USD 100.</span><span class="sxs-lookup"><span data-stu-id="b29f9-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="b29f9-113">Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="b29f9-114">Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="b29f9-115">Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="b29f9-116">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="b29f9-117">Ievadīt nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-117">Enter a condition.</span></span>
5. <span data-ttu-id="b29f9-118">Ja nepieciešams, ievadiet papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="b29f9-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="b29f9-119">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="b29f9-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="b29f9-120">Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="b29f9-121">Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="b29f9-122">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-122">Click **Test**.</span></span> <span data-ttu-id="b29f9-123">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="b29f9-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="b29f9-124">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos formā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="b29f9-125">Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="b29f9-126">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="b29f9-126">Specify when notifications are sent</span></span>

<span data-ttu-id="b29f9-127">Varat lietotājiem nosūtīt paziņojumus, kad dokuments ir apstiprināts, noraidīts, deleģēts vai eskalēts vai kad ir pieprasītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b29f9-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="b29f9-128">Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.</span><span class="sxs-lookup"><span data-stu-id="b29f9-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="b29f9-129">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="b29f9-130">Atzīmējiet izvēles rūtiņu pie notikumiem, lai sūtītu paziņojumus par:</span><span class="sxs-lookup"><span data-stu-id="b29f9-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="b29f9-131">**Deleģēt** — ja dokuments ir piešķirts citam lietotājam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="b29f9-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="b29f9-132">**Eskalēt** — ja piešķirtais lietotājs nav veicis darbību ar dokumentu atvēlētajā laika.</span><span class="sxs-lookup"><span data-stu-id="b29f9-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="b29f9-133">**Apstiprināt** — ja dokuments ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="b29f9-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="b29f9-134">**Noraidīt** — ja dokuments ir noraidīts.</span><span class="sxs-lookup"><span data-stu-id="b29f9-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="b29f9-135">**Pieprasīt izmaiņas** — ja piešķirtais lietotājs ir pieprasījis izmaiņas iesniegtajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="b29f9-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="b29f9-136">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="b29f9-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="b29f9-137">Noklikšķiniet uz cilnes **Paziņojuma teksts**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="b29f9-138">Tekstlodziņā ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="b29f9-139">Lai personalizētu tekstu, varat ievietot vietturus, kas tiks nomainīti ar attiecīgajiem datiem, kad tie tiks parādīti lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="b29f9-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="b29f9-140">Lai ievietotu vietturi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="b29f9-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="b29f9-141">Noklikšķiniet tekstlodziņā tajā atrašanās vietā, kur vēlaties ievietot vietturi.</span><span class="sxs-lookup"><span data-stu-id="b29f9-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="b29f9-142">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="b29f9-143">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="b29f9-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="b29f9-144">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-144">Click **Insert**.</span></span>

7. <span data-ttu-id="b29f9-145">Lai pievienotu paziņojuma tulkojumus, noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="b29f9-146">Parādītajā formā veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="b29f9-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="b29f9-147">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-147">Click **Add**.</span></span>
    2. <span data-ttu-id="b29f9-148">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="b29f9-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="b29f9-149">Tekstlodziņā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="b29f9-150">Lai personalizētu tekstu, ievietojiet vietturus.</span><span class="sxs-lookup"><span data-stu-id="b29f9-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="b29f9-151">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-151">Click **Close**.</span></span>

8. <span data-ttu-id="b29f9-152">Noklikšķiniet uz cilnes **Saņēmējs**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="b29f9-153">Norādīt, kam tiek sūtīti paziņojumi.</span><span class="sxs-lookup"><span data-stu-id="b29f9-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="b29f9-154">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 10. darbību.</span><span class="sxs-lookup"><span data-stu-id="b29f9-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="b29f9-155">Opcija</span><span class="sxs-lookup"><span data-stu-id="b29f9-155">Option</span></span></th>
    <th><span data-ttu-id="b29f9-156">Paziņojuma adresāti</span><span class="sxs-lookup"><span data-stu-id="b29f9-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="b29f9-157">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="b29f9-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="b29f9-158"><strong>Dalībnieks</strong></span><span class="sxs-lookup"><span data-stu-id="b29f9-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="b29f9-159">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="b29f9-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="b29f9-160">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, noklikšķiniet uz cilnes <strong>Pēc lomas</strong>.</span><span class="sxs-lookup"><span data-stu-id="b29f9-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="b29f9-161">Sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas vai lomas veidu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="b29f9-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="b29f9-162">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="b29f9-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="b29f9-163"><strong>Darbplūsmas lietotājs</strong></span><span class="sxs-lookup"><span data-stu-id="b29f9-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="b29f9-164">Lietotāji, kuri piedalās pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="b29f9-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="b29f9-165">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, noklikšķiniet uz cilnes <strong>Darbplūsmas lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="b29f9-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="b29f9-166">Sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="b29f9-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="b29f9-167"><strong>Lietotājs</strong></span><span class="sxs-lookup"><span data-stu-id="b29f9-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="b29f9-168">Īpaši lietotāji</span><span class="sxs-lookup"><span data-stu-id="b29f9-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="b29f9-169">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="b29f9-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="b29f9-170">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="b29f9-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="b29f9-171">Atkārtojiet 3.–9. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="b29f9-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="b29f9-172"> Norādiet pēdējo apstiprinātāju</span><span class="sxs-lookup"><span data-stu-id="b29f9-172">Specify a final approver</span></span>

<span data-ttu-id="b29f9-173">Varat apzīmēt pēdējo apstiprinātāju scenārijiem, kuros apstiprinātājs ir persona, kas iesniegusi dokumentu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="b29f9-173">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="b29f9-174">Lai norādītu galīgo apstiprinātāju, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="b29f9-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="b29f9-175">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-175">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="b29f9-176">Atzīmējiet izvēles rūtiņu **Izmantot galīgo apstiprinātāju**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-176">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="b29f9-177">Sarakstā atlasiet lietotāju, kurš būs galīgais apstiprinātājs.</span><span class="sxs-lookup"><span data-stu-id="b29f9-177">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="b29f9-178">Laika robežas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b29f9-178">Set a time limit</span></span>

<span data-ttu-id="b29f9-179">Veiciet šīs darbības, ja apstiprināšanas process ir jāpabeidz noteiktā laikā.</span><span class="sxs-lookup"><span data-stu-id="b29f9-179">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="b29f9-180">Šajās darbībās izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas katra apstiprināšanas soļa apgabalā **Piešķire** un **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-180">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="b29f9-181">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-181">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="b29f9-182">Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas** **elementa** laika ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-182">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="b29f9-183">Laukā **Ilgums** norādiet, kad apstiprināšanas process ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="b29f9-183">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="b29f9-184">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="b29f9-184">Select one of the following options:</span></span>

    - <span data-ttu-id="b29f9-185">**Stundas** — ievadiet stundu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="b29f9-185">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="b29f9-186">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="b29f9-187">**Dienas** — ievadiet dienu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="b29f9-187">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="b29f9-188">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="b29f9-189">**Nedēļas** — ievadiet nedēļu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="b29f9-189">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="b29f9-190">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz apstiprināšanas process.</span><span class="sxs-lookup"><span data-stu-id="b29f9-190">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="b29f9-191">Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="b29f9-191">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="b29f9-192">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz apstiprināšanas process.</span><span class="sxs-lookup"><span data-stu-id="b29f9-192">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="b29f9-193">Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="b29f9-193">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="b29f9-194">Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-194">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="b29f9-195">Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.</span><span class="sxs-lookup"><span data-stu-id="b29f9-195">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="b29f9-196">Norādiet, kuras darbības ir pieejamas lietotājam</span><span class="sxs-lookup"><span data-stu-id="b29f9-196">Specify which actions are available to the user</span></span>

<span data-ttu-id="b29f9-197">Kad dokuments ir piešķirts lietotājam apstiprināšanai, lietotājam ar šo dokumentu jārīkojas.</span><span class="sxs-lookup"><span data-stu-id="b29f9-197">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="b29f9-198">Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar iesniegto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-198">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="b29f9-199">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-199">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="b29f9-200">Atzīmējiet izvēles rūtiņu **Apstiprināt**, ja lietotājs var apstiprināt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-200">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="b29f9-201">Atzīmējiet izvēles rūtiņu **Noraidīt**, ja lietotājs var noraidīt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b29f9-201">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="b29f9-202">Atzīmējiet izvēles rūtiņu **Pieprasīt izmaiņas**, ja lietotājs var pieprasīt izmaiņas dokumentā.</span><span class="sxs-lookup"><span data-stu-id="b29f9-202">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="b29f9-203">Atzīmējiet izvēles rūtiņu **Deleģēt**, ja lietotājs var piešķirt dokumentu citam lietotājam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="b29f9-203">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="b29f9-204">Izvēles rūtiņa **Iespējot darbības no darbu saraksta uzņēmuma portālā** ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="b29f9-204">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="b29f9-205"> Apstiprinājuma darbību konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b29f9-205">Configure the approval steps</span></span>

<span data-ttu-id="b29f9-206">Apstiprināšanas process sastāv no apstiprināšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="b29f9-206">An approval process consists of approval steps.</span></span> <span data-ttu-id="b29f9-207">Veiciet šādu procedūru, lai pievienotu darbības apstiprināšanas procesam un konfigurētu darbības.</span><span class="sxs-lookup"><span data-stu-id="b29f9-207">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="b29f9-208">Darbplūsmas redaktorā veiciet dubultklikšķi uz apstiprināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="b29f9-208">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="b29f9-209">Darbplūsmas redaktorā tiek parādītas apstiprināšanas procesa darbības.</span><span class="sxs-lookup"><span data-stu-id="b29f9-209">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="b29f9-210">Lai pievienotu apstiprināšanas darbību, velciet darbību no apgabala **Darbplūsmas elementi** uz audekla.</span><span class="sxs-lookup"><span data-stu-id="b29f9-210">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="b29f9-211">Lai konfigurētu apstiprināšanas darbību, skatiet sadaļu [Apstiprinājuma darbības konfigurēšana](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b29f9-211">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
