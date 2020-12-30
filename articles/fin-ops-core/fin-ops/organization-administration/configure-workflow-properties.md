---
title: Konfigurēt darbplūsmas rekvizītus
description: Šajā tēmā ir paskaidrots, kā konfigurēt dažādus darbplūsmas rekvizītus.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693286"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="f56a7-103">Konfigurēt darbplūsmas rekvizītus</span><span class="sxs-lookup"><span data-stu-id="f56a7-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f56a7-104">Šajā tēmā ir paskaidrots, kā konfigurēt dažādus darbplūsmas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="f56a7-105">Lai konfigurētu darbplūsmas rekvizītus, atveriet darbplūsmu, izmantojot darbplūsmas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="f56a7-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="f56a7-106">Noklikšķiniet uz darbplūsmas redaktora audekla un pēc tam noklikšķiniet uz vienuma **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f56a7-107">Varat izmantot tālāk aprakstītās procedūras, lai konfigurētu dažādus darbplūsmas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="f56a7-108">Darbplūsmas nosaukums</span><span class="sxs-lookup"><span data-stu-id="f56a7-108">Name the workflow</span></span>

<span data-ttu-id="f56a7-109">Veiciet šādas darbības, lai ievadītu darbplūsmas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="f56a7-110">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56a7-111">Laukā **Nosaukums** ievadiet darbplūsmas unikālo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="f56a7-112">Piemēram, izveidojot pirkuma pieprasījuma darbplūsmu katrai valstij/reģionam, kurā strādājat, varat nosaukt pirkšanas pieprasījuma darbplūsmu **Pirkuma pieprasījumi Dānija** vai **Pirkuma pieprasījumi Spānija**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="f56a7-113">Norādiet darbplūsmas īpašnieku</span><span class="sxs-lookup"><span data-stu-id="f56a7-113">Specify the workflow owner</span></span>

<span data-ttu-id="f56a7-114">Darbplūsmas īpašnieks ir persona, kura pārvalda un uztur attiecīgo darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="f56a7-115">Veiciet šīs darbības, lai norādītu darbplūsmas īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="f56a7-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="f56a7-116">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56a7-117">Sarakstā **Īpašnieks** izvēlieties tās personas vārdu, kura pārvaldīs darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="f56a7-118">E-pasta veidnes atlasīšana</span><span class="sxs-lookup"><span data-stu-id="f56a7-118">Select an email template</span></span>

<span data-ttu-id="f56a7-119">Veiciet šīs darbības, lai atlasītu e-pasta veidni, kas tiek izmantota, lai ģenerētu ziņojumus par darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="f56a7-120">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56a7-121">Sarakstā **E-pasta veidne darbplūsmas paziņojumiem** atlasiet veidni.</span><span class="sxs-lookup"><span data-stu-id="f56a7-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="f56a7-122">Ievadiet instrukcijas lietotājam</span><span class="sxs-lookup"><span data-stu-id="f56a7-122">Enter instructions for users</span></span>

<span data-ttu-id="f56a7-123">Varat sniegt informāciju lietotājiem, kuri iesniedz dokumentus apstrādei un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="f56a7-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="f56a7-124">Šie lietotāji tiek saukti arī par *veidotājiem*.</span><span class="sxs-lookup"><span data-stu-id="f56a7-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="f56a7-125">Piemēram, jūs veidojat pirkuma pieprasījumu darbplūsmu un ievadāt instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="f56a7-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="f56a7-126">Šīs instrukcijas varēs skatīt lietotāji, kuri ievada pirkuma pieprasījumus lapā **Pirkuma pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="f56a7-127">Lai skatītu instrukcijas, veidotājs noklikšķina uz ikonas darbplūsmas ziņojumu joslā.</span><span class="sxs-lookup"><span data-stu-id="f56a7-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="f56a7-128">Veiciet šīs darbības, lai ievadītu instrukcijas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="f56a7-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="f56a7-129">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56a7-130">Laukā **Iesniegšanas instrukcijas** ievadiet instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="f56a7-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="f56a7-131">Lai personalizētu instrukcijas, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="f56a7-132">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="f56a7-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="f56a7-133">Lai ievietotu vietturi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="f56a7-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="f56a7-134">Noklikšķiniet uz lauka **Iesniegšanas instrukcijas**, lai norādītu, kur vēlaties ievietot vietturi.</span><span class="sxs-lookup"><span data-stu-id="f56a7-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f56a7-135">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f56a7-136">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="f56a7-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f56a7-137">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-137">Click **Insert**.</span></span>

4. <span data-ttu-id="f56a7-138">Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="f56a7-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="f56a7-139">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="f56a7-140">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f56a7-141">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="f56a7-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="f56a7-142">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f56a7-143">Lai personalizētu tekstu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="f56a7-144">Instrukcijas par to, kā ievadīt vietturi, skatiet 3. darbībā.</span><span class="sxs-lookup"><span data-stu-id="f56a7-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="f56a7-145">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="f56a7-146">Norādiet, kad šī darbplūsma tiek izmantota aktivizēšanas nosacījumos</span><span class="sxs-lookup"><span data-stu-id="f56a7-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="f56a7-147">Varat izveidot vairākas darbplūsmas, kuru pamatā ir tas pats darbplūsmas tips.</span><span class="sxs-lookup"><span data-stu-id="f56a7-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="f56a7-148">Ja vairāku darbplūsmu pamatā ir tas pats tips, nepieciešams norādīt, kad katra darbplūsma tiek izmantota, izmantojot aktivizēšanas nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="f56a7-149">Ja aktivizēšanas nosacījumi nav izpildīti, tiek izmantota noklusējuma darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="f56a7-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="f56a7-150">Tāpat, ja darbplūsmas tipam ir definēta tikai viena darbplūsmas konfigurācija, šī darbplūsmas konfigurācija tiks izmantota neatkarīgi no aktivizēšanas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="f56a7-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="f56a7-151">Piemēram, varat izveidot pirkuma pieprasījuma darbplūsmu katrai valstij/reģionam, kurā strādājat, piemēram, Pirkuma pieprasījumi Dānija un Pirkuma pieprasījumi Spānija ar sekojošajiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="f56a7-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="f56a7-152">Pirkuma pieprasījumi Dānija — tiek izmantota, ja: valsts/reģions = DK</span><span class="sxs-lookup"><span data-stu-id="f56a7-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="f56a7-153">Pirkuma pieprasījumi Spānija — tiek izmantota, ja: valsts/reģions = ES</span><span class="sxs-lookup"><span data-stu-id="f56a7-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="f56a7-154">Veiciet šīs darbības, lai norādītu, kad tiek izmantota konfigurētā darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="f56a7-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="f56a7-155">Kreisajā rūtī noklikšķiniet uz **Aktivizēšana**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="f56a7-156">Atzīmējiet izvēles rūtiņu **Iestatīt nosacījumus šīs darbplūsmas izpildei**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="f56a7-157">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="f56a7-158">Ievadiet nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-158">Enter a condition.</span></span>
5. <span data-ttu-id="f56a7-159">Ievadiet visus nepieciešamos papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="f56a7-160">Izpildiet darbplūsmu ar dažiem mērķa ierakstiem, lai pārbaudītu, vai nosacījums ir pareizi iekļauts un izslēdz ierakstus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f56a7-161">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="f56a7-161">Specify when notifications are sent</span></span>

<span data-ttu-id="f56a7-162">Kad dokuments iesniegts apstrādei, tiek izveidota darbplūsmas instance.</span><span class="sxs-lookup"><span data-stu-id="f56a7-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="f56a7-163">Varat nosūtīt paziņojumus lietotājiem, ja darbplūsmas instances, kuru pamatā ir attiecīgā darbplūsmā, ir sāktas, pabeigtas, pārtraukas vai apturētas kļūdas dēļ.</span><span class="sxs-lookup"><span data-stu-id="f56a7-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="f56a7-164">Veiciet šīs darbības, lai norādītu, kad tiek nosūtīti paziņojumi.</span><span class="sxs-lookup"><span data-stu-id="f56a7-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="f56a7-165">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="f56a7-166">Atzīmējiet izvēles rūtiņu katram notikumam, kam vajadzētu izraisīt paziņojumus:</span><span class="sxs-lookup"><span data-stu-id="f56a7-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="f56a7-167">**Sākts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek sākta.</span><span class="sxs-lookup"><span data-stu-id="f56a7-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="f56a7-168">**Apturēts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek apturēta kļūdas dēļ.</span><span class="sxs-lookup"><span data-stu-id="f56a7-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="f56a7-169">**Pabeigts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek pabeigta.</span><span class="sxs-lookup"><span data-stu-id="f56a7-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="f56a7-170">**Neatkopjama** — nosūtīt paziņojumus, kad darbplūsmas instance tiek apturēta neatkopjamas kļūdas dēļ.</span><span class="sxs-lookup"><span data-stu-id="f56a7-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="f56a7-171">**Pārtraukts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek pārtraukta.</span><span class="sxs-lookup"><span data-stu-id="f56a7-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="f56a7-172">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="f56a7-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="f56a7-173">Cilnē **Paziņojuma teksts** ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="f56a7-174">Lai personalizētu tekstu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="f56a7-175">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad teksts tiks parādīts lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="f56a7-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="f56a7-176">Lai ievietotu vietturi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="f56a7-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="f56a7-177">Noklikšķiniet uz lauka, lai norādītu, kur vietturim jāparādās.</span><span class="sxs-lookup"><span data-stu-id="f56a7-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f56a7-178">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f56a7-179">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="f56a7-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f56a7-180">Klikšķiniet **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="f56a7-181">Bieži izmantots opcijas **Paziņojuma teksts** vietturis ir Last Notes: %Workflow.Last note%, kas parāda visus iepriekšējās darbības komentārus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="f56a7-182">Lai pievienotu teksta tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="f56a7-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="f56a7-183">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="f56a7-184">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="f56a7-185">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="f56a7-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="f56a7-186">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f56a7-187">Lai personalizētu tekstu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="f56a7-188">Instrukcijas par to, kā ievadīt vietturi, skatiet 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="f56a7-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="f56a7-189">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-189">Click **Close**.</span></span>

7. <span data-ttu-id="f56a7-190">Cilnē **Adresāts** izmantojiet šādas opcijas, lai norādītu personas, kurām jāsaņem paziņojumi.</span><span class="sxs-lookup"><span data-stu-id="f56a7-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f56a7-191">Opcija</span><span class="sxs-lookup"><span data-stu-id="f56a7-191">Option</span></span></th>
    <th><span data-ttu-id="f56a7-192">Paziņojumi tiek nosūtīti šiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="f56a7-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="f56a7-193">Lai nosūtītu paziņojumus, rīkojieties šādi</span><span class="sxs-lookup"><span data-stu-id="f56a7-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f56a7-194">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="f56a7-194">Participant</span></span></td>
    <td><span data-ttu-id="f56a7-195">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="f56a7-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f56a7-196">Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Dalībnieks</strong>.</span><span class="sxs-lookup"><span data-stu-id="f56a7-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="f56a7-197">Cilnē <strong>Pēc lomas</strong>, sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f56a7-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f56a7-198">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f56a7-199">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="f56a7-199">Workflow user</span></span></td>
    <td><span data-ttu-id="f56a7-200">Lietotāji, kuri ir šīs darbplūsmas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="f56a7-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f56a7-201">Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Darbplūsmas lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="f56a7-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="f56a7-202">Cilnē <strong>Darbplūsmas lietotājs</strong>, sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet šīs darbplūsmas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="f56a7-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f56a7-203">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="f56a7-203">User</span></span></td>
    <td><span data-ttu-id="f56a7-204">Īpaši lietotāji</span><span class="sxs-lookup"><span data-stu-id="f56a7-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f56a7-205">Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="f56a7-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="f56a7-206">Cilnē <strong>Lietotājs</strong>, sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji.</span><span class="sxs-lookup"><span data-stu-id="f56a7-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f56a7-207">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="f56a7-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="f56a7-208">Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="f56a7-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="f56a7-209">Ievadiet komentārus par attiecīgajā darbplūsmā veiktajām izmaiņām</span><span class="sxs-lookup"><span data-stu-id="f56a7-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="f56a7-210">Lai ievadītu komentārus par izmaiņām, ko veicāt šajā darbplūsmā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="f56a7-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="f56a7-211">Kreisajā rūtī noklikšķiniet uz **Piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="f56a7-212">Laukā **Ievadīt komentārus par darbplūsmu** ievadiet savus komentārus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="f56a7-213">Pārskatiet savus komentārus.</span><span class="sxs-lookup"><span data-stu-id="f56a7-213">Review your comments.</span></span> <span data-ttu-id="f56a7-214">Pēc komentāru pievienošanas tos nevar pārveidot.</span><span class="sxs-lookup"><span data-stu-id="f56a7-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="f56a7-215">Noklikšķiniet uz **Pievienot**, lai pievienotu jūsu komentārus apgabalā **Komentāru vēsture**.</span><span class="sxs-lookup"><span data-stu-id="f56a7-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
