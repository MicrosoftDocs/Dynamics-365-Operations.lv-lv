---
title: Manuālu lēmumu konfigurēšana darbplūsmā
description: Šajā tēmā ir paskaidrots, kā konfigurēt manuāla lēmuma rekvizītus.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d351facbce02355ddb4bdf91d43d9df561e4f3b5
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798857"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="8c4e9-103">Manuālu lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="8c4e9-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c4e9-104">Šajā tēmā ir paskaidrots, kā konfigurēt manuāla lēmuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="8c4e9-105">Lai konfigurētu manuālu lēmumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz manuālā lēmuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8c4e9-106">Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu manuālā lēmuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="8c4e9-107">Lēmuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="8c4e9-107">Name the decision</span></span>

<span data-ttu-id="8c4e9-108">Izpildiet tālākos norādījumus, lai ievadītu manuālā lēmuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="8c4e9-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8c4e9-110">Laukā **Nosaukums** ievadiet unikālu manuālā lēmuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="8c4e9-111">Ievadiet tēmas rindu un instrukcijas</span><span class="sxs-lookup"><span data-stu-id="8c4e9-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="8c4e9-112">Jums jānorāda temata rinda un instrukcijas lietotājiem, kas piešķirti manuālajam lēmumam.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="8c4e9-113">Piemēram, ja konfigurējat pirkšanas pieprasījumu lēmumu, attiecīgajam lēmumam piešķirtais lietotājs redz tēmas rindu un instrukcijas lapā **Pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="8c4e9-114">Tēmas rinda tiek parādīta lapā esošajā ziņojumu joslā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="8c4e9-115">Lietotājs var noklikšķināt uz ziņojumu joslā redzamās ikonas, lai skatītu instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="8c4e9-116">Veiciet šīs darbības, lai ievadītu tēmas rindu un instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="8c4e9-117">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8c4e9-118">Cilnes **Instrukcijas** laukā **Darbplūsmas elementa tēma** ievadiet tēmas rindu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="8c4e9-119">Lai personalizētu tēmas rindu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="8c4e9-120">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad tēmas rinda tiks parādīta lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="8c4e9-121">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8c4e9-122">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8c4e9-123">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8c4e9-124">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8c4e9-125">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-125">Click **Insert**.</span></span>

4. <span data-ttu-id="8c4e9-126">Lai pievienotu tēmas rindas tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="8c4e9-127">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c4e9-128">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c4e9-129">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c4e9-130">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c4e9-131">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 3. darbībā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="8c4e9-132">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-132">Click **Close**.</span></span>

5. <span data-ttu-id="8c4e9-133">Laukā **Darbplūsmas elementa instrukcijas** ievadiet instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="8c4e9-134">Lai personalizētu instrukcijas, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="8c4e9-135">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="8c4e9-136">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8c4e9-137">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8c4e9-138">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8c4e9-139">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8c4e9-140">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-140">Click **Insert**.</span></span>

7. <span data-ttu-id="8c4e9-141">Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="8c4e9-142">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c4e9-143">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c4e9-144">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c4e9-145">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c4e9-146">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 6. darbībā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="8c4e9-147">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="8c4e9-148">Norādiet iespējamos lēmuma iznākumus</span><span class="sxs-lookup"><span data-stu-id="8c4e9-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="8c4e9-149">Parasti, ja dokuments tiek piešķirts lēmumu pieņēmējam, tam tiek uzdots jautājums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="8c4e9-150">Atbilde uz šo jautājumu parasti ir **Jā** vai **Nē**, vai **Patiess** vai **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="8c4e9-151">Veiciet šīs darbības, lai norādītu iespējamos manuālā lēmuma iznākumus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="8c4e9-152">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8c4e9-153">Cilnes **Iznākumi** laukā **1. iznākums** ievadiet iznākuma nosaukumu vai opciju.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="8c4e9-154">Lai pievienotu iznākuma tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="8c4e9-155">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c4e9-156">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c4e9-157">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c4e9-158">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c4e9-159">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-159">Click **Close**.</span></span>

4. <span data-ttu-id="8c4e9-160">Laukā **2. iznākums** ievadiet iznākuma nosaukumu vai opciju.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="8c4e9-161">Lai pievienotu iznākuma tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="8c4e9-162">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c4e9-163">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c4e9-164">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c4e9-165">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c4e9-166">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="8c4e9-167">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="8c4e9-167">Specify when notifications are sent</span></span>

<span data-ttu-id="8c4e9-168">Varat nosūtīt lietotājiem paziņojumus, ja lēmums ir pieņemts, deleģēts vai eskalēts.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="8c4e9-169">Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="8c4e9-170">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="8c4e9-171">Atzīmējiet izvēles rūtiņu pie notikumiem, par kuriem tiek sūtīti paziņojumi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="8c4e9-172">**\[1. izvēle\]**  — piešķirtais lietotājs ir atlasījis vienumu **\[1. izvēle\]**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="8c4e9-173">**\[2. izvēle\]**  — piešķirtais lietotājs ir atlasījis vienumu **\[2. izvēle\]**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="8c4e9-174">**Deleģēt**— piešķirtais lietotājs lēmumu ir piešķīris citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="8c4e9-175">**Eskalēt** — piešķirtais lietotājs nav pieņēmis lēmumu atvēlētajā laikā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="8c4e9-176">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="8c4e9-177">Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="8c4e9-178">Lai personalizētu paziņojumu, varat ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="8c4e9-179">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad paziņojums tiks parādīts lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="8c4e9-180">Veiciet šīs darbības, lai ievietotu vietturi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8c4e9-181">Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8c4e9-182">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8c4e9-183">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8c4e9-184">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-184">Click **Insert**.</span></span>

6. <span data-ttu-id="8c4e9-185">Lai pievienotu paziņojuma tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="8c4e9-186">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c4e9-187">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c4e9-188">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c4e9-189">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c4e9-190">Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="8c4e9-191">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-191">Click **Close**.</span></span>

7. <span data-ttu-id="8c4e9-192">Cilnē **Adresāts** norādiet personu, kurai paziņojumi tiek nosūtīti.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="8c4e9-193">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 8. darbību.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8c4e9-194">Opcija</span><span class="sxs-lookup"><span data-stu-id="8c4e9-194">Option</span></span></th>
    <th><span data-ttu-id="8c4e9-195">Paziņojuma adresāti</span><span class="sxs-lookup"><span data-stu-id="8c4e9-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="8c4e9-196">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="8c4e9-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8c4e9-197">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="8c4e9-197">Participant</span></span></td>
    <td><span data-ttu-id="8c4e9-198">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="8c4e9-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-199">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="8c4e9-200">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-201">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="8c4e9-201">Workflow user</span></span></td>
    <td><span data-ttu-id="8c4e9-202">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="8c4e9-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8c4e9-203">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-204">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="8c4e9-204">User</span></span></td>
    <td><span data-ttu-id="8c4e9-205">Īpaši lietotāji</span><span class="sxs-lookup"><span data-stu-id="8c4e9-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-206">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8c4e9-207">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8c4e9-208">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="8c4e9-209">Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="8c4e9-210">Lēmuma piešķiršana</span><span class="sxs-lookup"><span data-stu-id="8c4e9-210">Assign a decision</span></span>

<span data-ttu-id="8c4e9-211">Veiciet šīs darbības, lai norādītu personu, kurai jāpiešķir manuālais lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="8c4e9-212">Kreisajā rūtī noklikšķiniet uz **Piešķire**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="8c4e9-213">Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 3. darbību.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8c4e9-214">Opcija</span><span class="sxs-lookup"><span data-stu-id="8c4e9-214">Option</span></span></th>
    <th><span data-ttu-id="8c4e9-215">Lietotāji, kuriem ir piešķirts lēmums</span><span class="sxs-lookup"><span data-stu-id="8c4e9-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="8c4e9-216">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="8c4e9-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8c4e9-217">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="8c4e9-217">Participant</span></span></td>
    <td><span data-ttu-id="8c4e9-218">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="8c4e9-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-219">Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai piešķirt lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="8c4e9-220">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai piešķirt lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-221">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="8c4e9-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="8c4e9-222">Lietotāji īpašā organizācijas hierarhijā</span><span class="sxs-lookup"><span data-stu-id="8c4e9-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-223">Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram piešķirt lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="8c4e9-224">Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="8c4e9-225">Šie vārdi norāda, kuriem lietotājiem var piešķirt attiecīgo lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="8c4e9-226">Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="8c4e9-227">Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="8c4e9-228">Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="8c4e9-229">Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8c4e9-230">Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem lēmums jāpiešķir:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="8c4e9-231"><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — lēmums tiek piešķirts visiem diapazonā esošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="8c4e9-232"><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — lēmums tiek piešķirts tikai pēdējam lietotājam diapazonā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="8c4e9-233"><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — lēmums netiek piešķirts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="8c4e9-234">Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-235">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="8c4e9-235">Workflow user</span></span></td>
    <td><span data-ttu-id="8c4e9-236">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="8c4e9-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8c4e9-237">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-238">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="8c4e9-238">User</span></span></td>
    <td><span data-ttu-id="8c4e9-239">Īpaši lietotāji</span><span class="sxs-lookup"><span data-stu-id="8c4e9-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-240">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8c4e9-241">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8c4e9-242">Atlasiet lietotājus, kuriem piešķirt lēmumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="8c4e9-243">Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pieņemtu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="8c4e9-244">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-244">Select one of the following options:</span></span>

    - <span data-ttu-id="8c4e9-245">**Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="8c4e9-246">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c4e9-247">**Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="8c4e9-248">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c4e9-249">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="8c4e9-250">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="8c4e9-251">Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8c4e9-252">**Gadi** — izvēlieties dienu, nedēļu un mēnesi līdz kuram lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="8c4e9-253">Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="8c4e9-254">Ja lietotājs nepieņem lēmumu atvēlētajā laikā, lēmums ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="8c4e9-255">Nokavēts lēmums tiek eskalēts, pamatojoties uz opcijām, kas ir atlasītas lapas apgabalā **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="8c4e9-256">Norādiet, kas notiek, ja lēmums nokavēts</span><span class="sxs-lookup"><span data-stu-id="8c4e9-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="8c4e9-257">Ja lietotājs nepieņem lēmumu atvēlētajā laikā, lēmums ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="8c4e9-258">Lēmumu, kas ir nokavēts, var eskalēt vai automātiski piešķirt citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="8c4e9-259">Veiciet šīs darbības, lai eskalētu lēmumu, ja tas ir nokavēts.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="8c4e9-260">Kreisajā rūtī noklikšķiniet uz **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="8c4e9-261">Atzīmējiet izvēles rūtiņu **Izmantot eskalācijas ceļu**, lai izveidotu eskalācijas ceļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="8c4e9-262">Sistēma automātiski piešķirs lēmumu lietotājiem, kuri ir norādīti eskalācijas ceļā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="8c4e9-263">Piemēram, šajā tabulā ir attēlots eskalācijas ceļš.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="8c4e9-264">Secība</span><span class="sxs-lookup"><span data-stu-id="8c4e9-264">Sequence</span></span> | <span data-ttu-id="8c4e9-265">Eskalācijas ceļš</span><span class="sxs-lookup"><span data-stu-id="8c4e9-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="8c4e9-266">1.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-266">1</span></span>        | <span data-ttu-id="8c4e9-267">Piešķirt: Lindai</span><span class="sxs-lookup"><span data-stu-id="8c4e9-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="8c4e9-268">2.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-268">2</span></span>        | <span data-ttu-id="8c4e9-269">Piešķirt: Zanei</span><span class="sxs-lookup"><span data-stu-id="8c4e9-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="8c4e9-270">3.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-270">3</span></span>        | <span data-ttu-id="8c4e9-271">Gala darbība: \[1. izvēle\]</span><span class="sxs-lookup"><span data-stu-id="8c4e9-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="8c4e9-272">Šajā piemērā sistēma piešķir nokavēto lēmumu Lindai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="8c4e9-273">Ja Linda nepieņem lēmumu atvēlētajā laikā, sistēma piešķir lēmumu Zanei.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="8c4e9-274">Ja Zane nepieņem lēmumu atvēlētajā laikā, sistēma kā lēmumu atlasa vienumu **\[1. izvēle\]**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="8c4e9-275">Lai pievienotu lietotāju eskalācijas ceļam, noklikšķiniet uz **Pievienot eskalāciju**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="8c4e9-276">Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 4. darbību.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8c4e9-277">Opcija</span><span class="sxs-lookup"><span data-stu-id="8c4e9-277">Option</span></span></th>
    <th><span data-ttu-id="8c4e9-278">Lietotāji, kuriem tiek eskalēts lēmums</span><span class="sxs-lookup"><span data-stu-id="8c4e9-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="8c4e9-279">Papildu transakcijas</span><span class="sxs-lookup"><span data-stu-id="8c4e9-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8c4e9-280">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="8c4e9-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="8c4e9-281">Lietotāji īpašā organizācijas hierarhijā</span><span class="sxs-lookup"><span data-stu-id="8c4e9-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-282">Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, uz kuru eskalēt lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="8c4e9-283">Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="8c4e9-284">Šie vārdi norāda, kuriem lietotājiem var eskalēt lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="8c4e9-285">Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="8c4e9-286">Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="8c4e9-287">Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="8c4e9-288">Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8c4e9-289">Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem jāveic lēmuma eskalācija:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="8c4e9-290"><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — lēmums tiek eskalēts visiem diapazonā esošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="8c4e9-291"><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — lēmums tiek eskalēts tikai pēdējam lietotājam diapazonā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="8c4e9-292"><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — lēmums netiek eskalēts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="8c4e9-293">Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-294">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="8c4e9-294">Workflow user</span></span></td>
    <td><span data-ttu-id="8c4e9-295">Lietotāji pašreizējā darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="8c4e9-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8c4e9-296">Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c4e9-297">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="8c4e9-297">User</span></span></td>
    <td><span data-ttu-id="8c4e9-298">Īpaši lietotāji</span><span class="sxs-lookup"><span data-stu-id="8c4e9-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c4e9-299">Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8c4e9-300">Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8c4e9-301">Atlasiet lietotājus, kuriem eskalēt lēmumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="8c4e9-302">Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pieņemtu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="8c4e9-303">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-303">Select one of the following options:</span></span>

    - <span data-ttu-id="8c4e9-304">**Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="8c4e9-305">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c4e9-306">**Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="8c4e9-307">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c4e9-308">**Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="8c4e9-309">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="8c4e9-310">Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8c4e9-311">**Gadi** — izvēlieties dienu, nedēļu un mēnesi līdz kuram lietotājam ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="8c4e9-312">Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="8c4e9-313">Atkārtojiet 3.–4. darbību katram lietotājam, kurš jāpievieno eskalācijas ceļam.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="8c4e9-314">Jūs varat mainīt lietotāju secību.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="8c4e9-315">Ja eskalācijas ceļā norādītie lietotāji nepieņem lēmumu atvēlētajā laikā, sistēma pieņem lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="8c4e9-316">Lai norādītu opciju, ko sistēma izvēlas, atlasiet rindu **Darbība** un pēc tam cilnē **Beigu darbība** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="8c4e9-317">Laika robežas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8c4e9-317">Set a time limit</span></span>

<span data-ttu-id="8c4e9-318">Veiciet šīs darbības, ja lēmums ir jāpieņem noteiktā laikā.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="8c4e9-319">Šajā procedūrā izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas lapas apgabalos **Piešķire** un **Eskalācija**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="8c4e9-320">Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="8c4e9-321">Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas elementa laika ierobežojumu**.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="8c4e9-322">Laukā **Ilgums** norādiet, kad lēmums ir jāpieņem.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="8c4e9-323">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="8c4e9-323">Select one of the following options:</span></span>

    - <span data-ttu-id="8c4e9-324">**Stundas** — ievadiet stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="8c4e9-325">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c4e9-326">**Dienas** — ievadiet dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="8c4e9-327">Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c4e9-328">**Nedēļas** — ievadiet nedēļu skaitu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="8c4e9-329">**Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="8c4e9-330">Piemēram, iespējams, vēlēsities, lai lēmums tiktu pieņemts līdz mēneša trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8c4e9-331">**Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="8c4e9-332">Piemēram, iespējams, vēlēsities, lai lēmums tiktu pieņemts līdz decembra trešās nedēļas piektdienai.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="8c4e9-333">Ja laika ierobežojums ir pārsniegts, sistēma pieņems lēmumu.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="8c4e9-334">Sarakstā **Darbība** atlasiet opciju, kura sistēmai būtu jāizvēlas.</span><span class="sxs-lookup"><span data-stu-id="8c4e9-334">In the **Action** list, select the option that the system should select.</span></span>
