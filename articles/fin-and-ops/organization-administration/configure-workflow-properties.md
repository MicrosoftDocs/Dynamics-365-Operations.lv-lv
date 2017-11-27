---
title: "Konfigurēt darbplūsmas rekvizītus"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt dažādus darbplūsmas rekvizītus."
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
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c24f6555508272b65aeb81c5a16a0bd2407f1b4
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="configure-the-properties-of-a-workflow"></a><span data-ttu-id="89a64-103">Konfigurēt darbplūsmas rekvizītus</span><span class="sxs-lookup"><span data-stu-id="89a64-103">Configure the properties of a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89a64-104">Šajā tēmā ir paskaidrots, kā konfigurēt dažādus darbplūsmas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="89a64-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="89a64-105">Lai konfigurētu darbplūsmas rekvizītus, atveriet darbplūsmu, izmantojot darbplūsmas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="89a64-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="89a64-106">Noklikšķiniet uz darbplūsmas redaktora audekla un pēc tam noklikšķiniet uz vienuma **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="89a64-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="89a64-107">Varat izmantot tālāk aprakstītās procedūras, lai konfigurētu dažādus darbplūsmas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="89a64-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="89a64-108">Darbplūsmas nosaukums</span><span class="sxs-lookup"><span data-stu-id="89a64-108">Name the workflow</span></span>
<span data-ttu-id="89a64-109">Veiciet šādas darbības, lai ievadītu darbplūsmas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="89a64-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="89a64-110">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="89a64-111">Laukā **Nosaukums** ievadiet darbplūsmas unikālo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="89a64-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="89a64-112">Piemēram, izveidojot pirkuma pieprasījuma darbplūsmu katrai valstij/reģionam, kurā strādājat, varat nosaukt pirkšanas pieprasījuma darbplūsmu **Pirkuma pieprasījumi Dānija** vai **Pirkuma pieprasījumi Spānija**.</span><span class="sxs-lookup"><span data-stu-id="89a64-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="89a64-113">Norādiet darbplūsmas īpašnieku</span><span class="sxs-lookup"><span data-stu-id="89a64-113">Specify the workflow owner</span></span>
<span data-ttu-id="89a64-114">Darbplūsmas īpašnieks ir persona, kura pārvalda un uztur attiecīgo darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="89a64-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="89a64-115">Veiciet šīs darbības, lai norādītu darbplūsmas īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="89a64-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="89a64-116">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="89a64-117">Sarakstā **Īpašnieks** izvēlieties tās personas vārdu, kura pārvaldīs darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="89a64-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="89a64-118">E-pasta veidnes atlasīšana</span><span class="sxs-lookup"><span data-stu-id="89a64-118">Select an email template</span></span>
<span data-ttu-id="89a64-119">Veiciet šīs darbības, lai atlasītu e-pasta veidni, kas tiek izmantota, lai ģenerētu ziņojumus par darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="89a64-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="89a64-120">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="89a64-121">Sarakstā **E-pasta veidne darbplūsmas paziņojumiem** atlasiet veidni.</span><span class="sxs-lookup"><span data-stu-id="89a64-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="89a64-122">Ievadiet instrukcijas lietotājam</span><span class="sxs-lookup"><span data-stu-id="89a64-122">Enter instructions for users</span></span>
<span data-ttu-id="89a64-123">Varat sniegt informāciju lietotājiem, kuri iesniedz dokumentus apstrādei un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="89a64-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="89a64-124">Šie lietotāji tiek saukti arī par *veidotājiem*.</span><span class="sxs-lookup"><span data-stu-id="89a64-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="89a64-125">Piemēram, jūs veidojat pirkuma pieprasījumu darbplūsmu un ievadāt instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="89a64-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="89a64-126">Šīs instrukcijas varēs skatīt lietotāji, kuri ievada pirkuma pieprasījumus lapā **Pirkuma pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="89a64-127">Lai skatītu instrukcijas, veidotājs noklikšķina uz ikonas darbplūsmas ziņojumu joslā.</span><span class="sxs-lookup"><span data-stu-id="89a64-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="89a64-128">Veiciet šīs darbības, lai ievadītu instrukcijas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="89a64-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="89a64-129">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="89a64-130">Laukā **Iesniegšanas instrukcijas** ievadiet instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="89a64-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="89a64-131">Lai personalizētu instrukcijas, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="89a64-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="89a64-132">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="89a64-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="89a64-133">Lai ievietotu vietturi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="89a64-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="89a64-134">Noklikšķiniet uz lauka **Iesniegšanas instrukcijas**, lai norādītu, kur vēlaties ievietot vietturi.</span><span class="sxs-lookup"><span data-stu-id="89a64-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="89a64-135">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="89a64-136">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="89a64-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="89a64-137">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="89a64-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="89a64-138">Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="89a64-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="89a64-139">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="89a64-140">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="89a64-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="89a64-141">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="89a64-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="89a64-142">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="89a64-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="89a64-143">Lai personalizētu tekstu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="89a64-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="89a64-144">Instrukcijas par to, kā ievadīt vietturi, skatiet 3. darbībā.</span><span class="sxs-lookup"><span data-stu-id="89a64-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="89a64-145">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="89a64-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="89a64-146">Norādiet, kad tiek izmantota šī darbplūsma</span><span class="sxs-lookup"><span data-stu-id="89a64-146">Specify when this workflow is used</span></span>
<span data-ttu-id="89a64-147">Varat izveidot vairākas darbplūsmas, kuru pamatā ir tas pats tips.</span><span class="sxs-lookup"><span data-stu-id="89a64-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="89a64-148">Piemēram, varat izveidot pirkuma pieprasījuma darbplūsmu katrai valstij/reģionam, kurā strādājat, piemēram, Pirkuma pieprasījumi Dānija un Pirkuma pieprasījumi Spānija.</span><span class="sxs-lookup"><span data-stu-id="89a64-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="89a64-149">Ja vairāku darbplūsmu pamatā ir tas pats tips, nepieciešams norādīt, kad katra darbplūsma tiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="89a64-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="89a64-150">Iepriekšējā piemērā norādiet šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="89a64-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="89a64-151">Pirkuma pieprasījumi Dānija — tiek izmantota, ja: valsts/reģions = DK</span><span class="sxs-lookup"><span data-stu-id="89a64-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="89a64-152">Pirkuma pieprasījumi Spānija — tiek izmantota, ja: valsts/reģions = ES</span><span class="sxs-lookup"><span data-stu-id="89a64-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="89a64-153">Veiciet šīs darbības, lai norādītu, kad tiek izmantota konfigurētā darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="89a64-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="89a64-154">Kreisajā rūtī noklikšķiniet uz **Aktivizēšana**.</span><span class="sxs-lookup"><span data-stu-id="89a64-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="89a64-155">Atzīmējiet izvēles rūtiņu **Iestatīt nosacījumus šīs darbplūsmas izpildei**.</span><span class="sxs-lookup"><span data-stu-id="89a64-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="89a64-156">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="89a64-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="89a64-157">Ievadīt nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="89a64-157">Enter a condition.</span></span>
5.  <span data-ttu-id="89a64-158">Ievadiet visus nepieciešamos papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="89a64-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="89a64-159">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi iestatīti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="89a64-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="89a64-160">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="89a64-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="89a64-161">Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="89a64-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="89a64-162">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="89a64-162">Click **Test**.</span></span> <span data-ttu-id="89a64-163">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="89a64-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="89a64-164">Piemēram, ja veidojat pirkuma pieprasījumu darbplūsmu Spānijai, lapas apgabalā **Pārbaudīt nosacījumu** tiek parādīts pirkšanas pieprasījumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="89a64-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="89a64-165">Noklikšķinot uz **Pārbaudīt**, sistēma izvērtēs izvēlētos pirkuma pieprasījumus, lai noteiktu, vai valsts/reģions ir ES.</span><span class="sxs-lookup"><span data-stu-id="89a64-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="89a64-166">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="89a64-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="89a64-167">Norādīt, kad tiek sūtīti paziņojumi</span><span class="sxs-lookup"><span data-stu-id="89a64-167">Specify when notifications are sent</span></span>
<span data-ttu-id="89a64-168">Kad dokuments iesniegts apstrādei, tiek izveidota darbplūsmas instance.</span><span class="sxs-lookup"><span data-stu-id="89a64-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="89a64-169">Varat nosūtīt paziņojumus lietotājiem, ja darbplūsmas instances, kuru pamatā ir attiecīgā darbplūsmā, ir sāktas, pabeigtas, pārtraukas vai apturētas kļūdas dēļ.</span><span class="sxs-lookup"><span data-stu-id="89a64-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="89a64-170">Veiciet šīs darbības, lai norādītu, kad tiek nosūtīti paziņojumi.</span><span class="sxs-lookup"><span data-stu-id="89a64-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="89a64-171">Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="89a64-172">Atzīmējiet izvēles rūtiņu katram notikumam, kam vajadzētu izraisīt paziņojumus:</span><span class="sxs-lookup"><span data-stu-id="89a64-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="89a64-173">**Sākts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek sākta.</span><span class="sxs-lookup"><span data-stu-id="89a64-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="89a64-174">**Apturēts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek apturēta kļūdas dēļ.</span><span class="sxs-lookup"><span data-stu-id="89a64-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="89a64-175">**Pabeigts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek pabeigta.</span><span class="sxs-lookup"><span data-stu-id="89a64-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="89a64-176">**Neatkopjama** — nosūtīt paziņojumus, kad darbplūsmas instance tiek apturēta neatkopjamas kļūdas dēļ.</span><span class="sxs-lookup"><span data-stu-id="89a64-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="89a64-177">**Pārtraukts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek pārtraukta.</span><span class="sxs-lookup"><span data-stu-id="89a64-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="89a64-178">Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="89a64-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="89a64-179">Cilnē **Paziņojuma teksts** ievadiet paziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="89a64-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="89a64-180">Lai personalizētu tekstu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="89a64-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="89a64-181">Vietturi tiks aizvietoti ar atbilstošiem datiem, kad teksts tiks parādīts lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="89a64-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="89a64-182">Lai ievietotu vietturi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="89a64-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="89a64-183">Noklikšķiniet uz lauka, lai norādītu, kur vietturim jāparādās.</span><span class="sxs-lookup"><span data-stu-id="89a64-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="89a64-184">Noklikšķiniet uz **Ievietot vietturi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="89a64-185">Parādītajā sarakstā atlasiet vietturi, kuru ievietot.</span><span class="sxs-lookup"><span data-stu-id="89a64-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="89a64-186">Noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="89a64-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="89a64-187">Lai pievienotu teksta tulkojumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="89a64-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="89a64-188">Noklikšķiniet uz **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="89a64-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="89a64-189">Parādītajā lapā noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="89a64-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="89a64-190">Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.</span><span class="sxs-lookup"><span data-stu-id="89a64-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="89a64-191">Laukā **Tulkotais teksts** ievadiet tekstu.</span><span class="sxs-lookup"><span data-stu-id="89a64-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="89a64-192">Lai personalizētu tekstu, var ievadīt vietturus.</span><span class="sxs-lookup"><span data-stu-id="89a64-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="89a64-193">Instrukcijas par to, kā ievadīt vietturi, skatiet 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="89a64-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="89a64-194">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="89a64-194">Click **Close**.</span></span>

7.  <span data-ttu-id="89a64-195">Cilnē **Adresāts** izmantojiet šādas opcijas, lai norādītu personas, kurām jāsaņem paziņojumi.</span><span class="sxs-lookup"><span data-stu-id="89a64-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89a64-196">Opcija</span><span class="sxs-lookup"><span data-stu-id="89a64-196">Option</span></span></th>
    <th><span data-ttu-id="89a64-197">Paziņojumi tiek nosūtīti šiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="89a64-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="89a64-198">Lai nosūtītu paziņojumus, rīkojieties šādi</span><span class="sxs-lookup"><span data-stu-id="89a64-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="89a64-199">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="89a64-199">Participant</span></span></td>
    <td><span data-ttu-id="89a64-200">Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</span><span class="sxs-lookup"><span data-stu-id="89a64-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="89a64-201">Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Dalībnieks</strong>.</span><span class="sxs-lookup"><span data-stu-id="89a64-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="89a64-202">Cilnē <strong>Pēc lomas</strong>, sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="89a64-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="89a64-203">Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="89a64-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="89a64-204">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="89a64-204">Workflow user</span></span></td>
    <td><span data-ttu-id="89a64-205">Lietotāji, kuri ir šīs darbplūsmas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="89a64-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="89a64-206">Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Darbplūsmas lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="89a64-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="89a64-207">Cilnē <strong>Darbplūsmas lietotājs</strong>, sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet šīs darbplūsmas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="89a64-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="89a64-208">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="89a64-208">User</span></span></td>
    <td><span data-ttu-id="89a64-209">Noteikti Dynamics 365 for Finance and Operations lietotāji</span><span class="sxs-lookup"><span data-stu-id="89a64-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="89a64-210">Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Lietotājs</strong>.</span><span class="sxs-lookup"><span data-stu-id="89a64-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="89a64-211">Cilnes <strong>Lietotājs</strong> sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji.</span><span class="sxs-lookup"><span data-stu-id="89a64-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="89a64-212">Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</span><span class="sxs-lookup"><span data-stu-id="89a64-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="89a64-213">Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="89a64-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="89a64-214">Ievadiet komentārus par attiecīgajā darbplūsmā veiktajām izmaiņām</span><span class="sxs-lookup"><span data-stu-id="89a64-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="89a64-215">Lai ievadītu komentārus par izmaiņām, ko veicāt šajā darbplūsmā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="89a64-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="89a64-216">Kreisajā rūtī noklikšķiniet uz **Piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="89a64-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="89a64-217">Laukā **Ievadīt komentārus par darbplūsmu** ievadiet savus komentārus.</span><span class="sxs-lookup"><span data-stu-id="89a64-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="89a64-218">Pārskatiet savus komentārus.</span><span class="sxs-lookup"><span data-stu-id="89a64-218">Review your comments.</span></span> <span data-ttu-id="89a64-219">Pēc komentāru pievienošanas tos nevar pārveidot.</span><span class="sxs-lookup"><span data-stu-id="89a64-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="89a64-220">Noklikšķiniet uz **Pievienot**, lai pievienotu jūsu komentārus apgabalā **Komentāru vēsture**.</span><span class="sxs-lookup"><span data-stu-id="89a64-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





