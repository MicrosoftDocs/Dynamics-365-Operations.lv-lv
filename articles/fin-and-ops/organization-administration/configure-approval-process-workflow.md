---
title: "Apstiprināšanas procesu konfigurēšana darbplūsmā"
description: "Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 212e9c32c7bb22b0ee0450e04b4090c540df7b54
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="4a7ed-103">Apstiprināšanas procesu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="4a7ed-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a7ed-104">Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="4a7ed-105">Lai konfigurētu apstiprināšanas procesu, darbplūsmas redaktorā ar peles labo pogu noklikšķiniet uz apstiprināšanas elementa un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="4a7ed-106">Nosaukuma piešķiršana apstiprināšanas procesam</span><span class="sxs-lookup"><span data-stu-id="4a7ed-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="4a7ed-107">Veiciet šīs darbības, lai ievadītu apstiprināšanas procesa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="4a7ed-108">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="4a7ed-109">Laukā **Nosaukums** ievadiet unikālu apstiprināšanas procesa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="4a7ed-110">Norādiet, kad sistēma automātiski veic darbību ar dokumentu</span><span class="sxs-lookup"><span data-stu-id="4a7ed-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="4a7ed-111">Varat konfigurēt, lai sistēma automātiski rīkotos ar dokumentu, ja ir izpildīti konkrēti nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="4a7ed-112">Piemēram, sistēma var apstiprināt izdevumu pārskatus, kuros kopējās summas ir mazākas par USD 100.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="4a7ed-113">Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="4a7ed-114">Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="4a7ed-115">Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="4a7ed-116">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="4a7ed-117">Ievadīt nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-117">Enter a condition.</span></span>
5.  <span data-ttu-id="4a7ed-118">Ja nepieciešams, ievadiet papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="4a7ed-119">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="4a7ed-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="4a7ed-120">Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="4a7ed-121">Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="4a7ed-122">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-122">Click **Test**.</span></span> <span data-ttu-id="4a7ed-123">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="4a7ed-124">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos formā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="4a7ed-125">Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="4a7ed-126">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="4a7ed-126">Specify when notifications are sent</span></span>
<span data-ttu-id="4a7ed-127">Varat lietotājiem nosūtīt paziņojumus, kad dokuments ir apstiprināts, noraidīts, deleģēts vai eskalēts vai kad ir pieprasītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="4a7ed-128">Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="4a7ed-129">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="4a7ed-130">Atzīmējiet izvēles rūtiņu pie notikumiem, lai sūtītu paziņojumus par:</span><span class="sxs-lookup"><span data-stu-id="4a7ed-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="4a7ed-131">**Deleģēt** — ja dokuments ir piešķirts citam lietotājam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="4a7ed-132">**Eskalēt** — ja piešķirtais lietotājs nav veicis darbību ar dokumentu atvēlētajā laika.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="4a7ed-133">**Apstiprināt** — ja dokuments ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="4a7ed-134">**Noraidīt** — ja dokuments ir noraidīts.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="4a7ed-135">**Pieprasīt izmaiņas** — ja piešķirtais lietotājs ir pieprasījis izmaiņas iesniegtajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="4a7ed-136">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="4a7ed-137">Noklikšķiniet uz cilnes **Paziņojuma teksts**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="4a7ed-138">Tekstlodziņā ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="4a7ed-139">Lai personalizētu tekstu, varat ievietot vietturus, kas tiks nomainīti ar attiecīgajiem datiem, kad tie tiks parādīti lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="4a7ed-140">Lai ievietotu vietturi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="4a7ed-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="4a7ed-141">Noklikšķiniet tekstlodziņā tajā atrašanās vietā, kur vēlaties ievietot vietturi.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="4a7ed-142">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="4a7ed-143">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="4a7ed-144">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="4a7ed-145">Lai pievienotu paziņojuma tulkojumus, noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="4a7ed-146">Parādītajā formā veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="4a7ed-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="4a7ed-147">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="4a7ed-148">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="4a7ed-149">Tekstlodziņā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="4a7ed-150">Lai personalizētu tekstu, ievietojiet vietturus.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="4a7ed-151">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-151">Click **Close**.</span></span>

8.  <span data-ttu-id="4a7ed-152">Noklikšķiniet uz cilnes **Saņēmējs**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="4a7ed-153">Norādīt, kam tiek sūtīti paziņojumi.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="4a7ed-154">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 10. darbību.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="4a7ed-155">Opcija</span><span class="sxs-lookup"><span data-stu-id="4a7ed-155">Option</span></span></th>
    <th><span data-ttu-id="4a7ed-156">Paziņojuma adresāti</span><span class="sxs-lookup"><span data-stu-id="4a7ed-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="4a7ed-157">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="4a7ed-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="4a7ed-158"><strong>Dalībnieks</strong></span><span class="sxs-lookup"><span data-stu-id="4a7ed-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="4a7ed-159">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="4a7ed-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4a7ed-160">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, noklikšķiniet uz cilnes <strong>Pēc lomas</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="4a7ed-161">Sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas vai lomas veidu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="4a7ed-162">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="4a7ed-163"><strong>Darbplūsmas lietotājs</strong></span><span class="sxs-lookup"><span data-stu-id="4a7ed-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="4a7ed-164">Lietotāji, kuri piedalās pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="4a7ed-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4a7ed-165">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, noklikšķiniet uz cilnes <strong>Darbplūsmas lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="4a7ed-166">Sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="4a7ed-167"><strong>Lietotājs</strong></span><span class="sxs-lookup"><span data-stu-id="4a7ed-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="4a7ed-168">Noteikti Microsoft Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="4a7ed-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4a7ed-169">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="4a7ed-170"><strong>Pieejamie lietotāji</strong>: sarakstā ir ietverti visi Microsoft Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="4a7ed-171">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>:.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="4a7ed-172">Atkārtojiet 3.–9. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="4a7ed-173"> Norādiet pēdējo apstiprinātāju</span><span class="sxs-lookup"><span data-stu-id="4a7ed-173">Specify a final approver</span></span>
<span data-ttu-id="4a7ed-174">Varat apzīmēt pēdējo apstiprinātāju scenārijiem, kuros apstiprinātājs ir persona, kas iesniegusi dokumentu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="4a7ed-175">Lai norādītu galīgo apstiprinātāju, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="4a7ed-176">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="4a7ed-177">Atzīmējiet izvēles rūtiņu **Izmantot galīgo apstiprinātāju**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="4a7ed-178">Sarakstā atlasiet lietotāju, kurš būs galīgais apstiprinātājs.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="4a7ed-179">Laika robežas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4a7ed-179">Set a time limit</span></span>
<span data-ttu-id="4a7ed-180">Veiciet šīs darbības, ja apstiprināšanas process ir jāpabeidz noteiktā laikā.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

| <span data-ttu-id="4a7ed-181">**Piezīme**</span><span class="sxs-lookup"><span data-stu-id="4a7ed-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7ed-182">Šajās darbībās izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas katra apstiprināšanas soļa apgabalā **Piešķire** un **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="4a7ed-183">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="4a7ed-184">Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas** **elementa** laika ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="4a7ed-185">Laukā **Ilgums** norādiet, kad apstiprināšanas process ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="4a7ed-186">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="4a7ed-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="4a7ed-187">**Stundas** — ievadiet stundu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="4a7ed-188">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="4a7ed-189">**Dienas** — ievadiet dienu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="4a7ed-190">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="4a7ed-191">**Nedēļas** — ievadiet nedēļu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="4a7ed-192">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz apstiprināšanas process.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="4a7ed-193">Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="4a7ed-194">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz apstiprināšanas process.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="4a7ed-195">Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="4a7ed-196">Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="4a7ed-197">Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="4a7ed-198">Norādiet, kuras darbības ir pieejamas lietotājam</span><span class="sxs-lookup"><span data-stu-id="4a7ed-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="4a7ed-199">Kad dokuments ir piešķirts lietotājam apstiprināšanai, lietotājam ar šo dokumentu jārīkojas.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="4a7ed-200">Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar iesniegto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="4a7ed-201">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="4a7ed-202">Atzīmējiet izvēles rūtiņu **Apstiprināt**, ja lietotājs var apstiprināt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="4a7ed-203">Atzīmējiet izvēles rūtiņu **Noraidīt**, ja lietotājs var noraidīt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="4a7ed-204">Atzīmējiet izvēles rūtiņu **Pieprasīt izmaiņas**, ja lietotājs var pieprasīt izmaiņas dokumentā.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="4a7ed-205">Atzīmējiet izvēles rūtiņu **Deleģēt**, ja lietotājs var piešķirt dokumentu citam lietotājam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="4a7ed-206">**Piezīme**. Izvēles rūtiņa **Iespējot darbības no darbu saraksta uzņēmuma portālā** ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="4a7ed-207"> Apstiprinājuma darbību konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="4a7ed-207">Configure the approval steps</span></span>
<span data-ttu-id="4a7ed-208">Apstiprināšanas process sastāv no apstiprināšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="4a7ed-209">Veiciet šādu procedūru, lai pievienotu darbības apstiprināšanas procesam un konfigurētu darbības.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="4a7ed-210">Darbplūsmas redaktorā veiciet dubultklikšķi uz apstiprināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="4a7ed-211">Darbplūsmas redaktorā tiek parādītas apstiprināšanas procesa darbības.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="4a7ed-212">Lai pievienotu apstiprināšanas darbību, velciet darbību no apgabala **Darbplūsmas elementi** uz audekla.</span><span class="sxs-lookup"><span data-stu-id="4a7ed-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="4a7ed-213">Lai konfigurētu apstiprināšanas darbību, skatiet sadaļu [Apstiprinājuma darbības konfigurēšana](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="4a7ed-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






