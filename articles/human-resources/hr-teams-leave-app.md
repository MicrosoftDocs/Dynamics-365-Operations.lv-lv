---
title: Atvaļinājuma pieprasījumu pārvaldība programmā Teams
description: Šajā tēmā parādīts, kā pieprasīt prombūtni Dynamics 365 Human Resources programmā Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3929997"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="73f7e-103">Atvaļinājuma pieprasījumu pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="73f7e-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="73f7e-104">Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj ātri pieprasīt prombūtni un skatīt savas prombūtnes bilances informāciju Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="73f7e-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="73f7e-105">Varat mijiedarboties ar botu, lai pieprasītu informāciju un sāktu atvaļinājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="73f7e-106">Cilne **Brīvais laiks** sniedz detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="73f7e-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="73f7e-107">Turklāt varat nosūtīt personām informāciju par gaidāmo prombūtni grupās un tērzēšanā ārpus Human Resources programmas.</span><span class="sxs-lookup"><span data-stu-id="73f7e-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="73f7e-108">Programmas instalēšana</span><span class="sxs-lookup"><span data-stu-id="73f7e-108">Install the app</span></span>

<span data-ttu-id="73f7e-109">Human Resources programmu varat atrast Teams veikalā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="73f7e-110">Sadaļā Microsoft Teams atlasiet daudzpunkti.</span><span class="sxs-lookup"><span data-stu-id="73f7e-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams atstāj programmas daudzpunkti](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="73f7e-112">Meklējiet Dynamics 365 Human Resources un pēc tam atlasiet elementu **Personāla vadība**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams atstāj programmas elementu personāla vadība](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="73f7e-114">Atlasiet pogu **Pievienot**, lai instalētu programmu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams atstāj programmas instalēšanu](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="73f7e-116">Ja programma jūs automātiski nepieraksta, atlasiet cilni **Iestatījumi**, lai pierakstītos.</span><span class="sxs-lookup"><span data-stu-id="73f7e-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams atstāj programmas cilni Iestatījumi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="73f7e-118">Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus.</span><span class="sxs-lookup"><span data-stu-id="73f7e-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="73f7e-119">Ja jums ir piekļuve vairāk nekā vienai Human Resources instancei, varat atlasīt, ar kuru vidi vēlaties veidot savienojumu, cilnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="73f7e-120">Programma tagad atbalsta Sistēmas administratora drošības lomu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="73f7e-121">Bota izmantošana</span><span class="sxs-lookup"><span data-stu-id="73f7e-121">Use the bot</span></span>

<span data-ttu-id="73f7e-122">Pēc programmas instalēšanas, tiek parādīts sveiciena ziņojums, informējot jūs par darbību veidiem, ko bots var veikt jūsu vārdā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams atstāj programmas bota sveiciena ziņojumu](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="73f7e-124">Pirmo reizi izmantojot botu, var būt nepieciešams pierakstīties.</span><span class="sxs-lookup"><span data-stu-id="73f7e-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="73f7e-125">Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus.</span><span class="sxs-lookup"><span data-stu-id="73f7e-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="73f7e-126">Varat lūgt botam:</span><span class="sxs-lookup"><span data-stu-id="73f7e-126">You can ask the bot to:</span></span>

- <span data-ttu-id="73f7e-127">Rādīt prombūtnes bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts.</span><span class="sxs-lookup"><span data-stu-id="73f7e-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams atstāj programmas bilances rādīšanu](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="73f7e-129">Rādīt papildu informāciju par konkrētu atvaļinājuma veidu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams atstāj programmas informācijas rādīšanu](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="73f7e-131">Izveidot atvaļinājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-131">Start a leave request for you.</span></span>

   ![Human Resources Teams atstāj programmas atvaļinājuma pieprasījumu](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="73f7e-133">Pēc atvaļinājuma pieprasījuma sākšanas varat pielāgot dienas tieši kartē.</span><span class="sxs-lookup"><span data-stu-id="73f7e-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teams atstāj programmas rediģēšanas pieprasījumu](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="73f7e-135">Kad esat pabeidzis ievadīt informāciju, atlasiet **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="73f7e-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="73f7e-136">Varat arī atlasīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="73f7e-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teams atstāj programmas pieprasījuma iesniegšanu](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="73f7e-138">Atvaļinājuma pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="73f7e-138">Manage your leave in Teams</span></span>

<span data-ttu-id="73f7e-139">Cilne **Brīvais laiks** ļauj skatīt:</span><span class="sxs-lookup"><span data-stu-id="73f7e-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="73f7e-140">Bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts</span><span class="sxs-lookup"><span data-stu-id="73f7e-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="73f7e-141">Gaidāmos atvaļinājuma pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="73f7e-141">Upcoming leave requests</span></span>

- <span data-ttu-id="73f7e-142">Prombūtnes pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="73f7e-142">Time-off requests</span></span>

- <span data-ttu-id="73f7e-143">Melnraksta atvaļinājuma pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="73f7e-143">Draft leave requests</span></span>

![Personāla vadība Teams atstāj programmas cilni Brīvais laiks](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="73f7e-145">Jauna pieprasījuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="73f7e-145">Create a new request</span></span>

1. <span data-ttu-id="73f7e-146">Lai izveidotu jaunu atvaļinājuma pieprasījumu, atlasiet **Jauns pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams atstāj programmas Jauns pieprasījums](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="73f7e-148">Ievadiet dienu vai dienas, kurās vēlaties ņemt pārtraukumu, un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams atstāj programmas pievienot prombūtni](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="73f7e-150">Ja piemērojams, ievadiet iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="73f7e-151">Ievadiet arī komentārus un pievienojiet pielikumus.</span><span class="sxs-lookup"><span data-stu-id="73f7e-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="73f7e-152">Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="73f7e-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="73f7e-153">Varat arī ierakstīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="73f7e-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="73f7e-154">Melnraksta pieprasījumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="73f7e-154">Manage draft requests</span></span>

1. <span data-ttu-id="73f7e-155">Atlasiet cilni **Melnraksti**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams atstāj programmas cilni Melnraksti](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="73f7e-157">Atlasiet zīmuli, lai rediģētu pieprasījumu, vai atlasiet atkritni, lai dzēstu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="73f7e-158">Veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="73f7e-158">Make any necessary changes.</span></span> <span data-ttu-id="73f7e-159">Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="73f7e-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="73f7e-160">Varat arī atlasīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="73f7e-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams atstāj programmas rediģēšanas melnraksts](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="73f7e-162">Atbildēt uz programmas Teams paziņojumiem</span><span class="sxs-lookup"><span data-stu-id="73f7e-162">Respond to Teams notifications</span></span>

<span data-ttu-id="73f7e-163">Kad jūs vai darbinieks, kuram jūs esat apstiprinātājs, iesniedz atvaļinājuma pieprasījumu, jums tiek nosūtīts paziņojums Teams risinājuma Human Resources programmā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="73f7e-164">Varat atlasīt paziņojumu, lai to skatītu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-164">You can select the notification to view it.</span></span> <span data-ttu-id="73f7e-165">Paziņojumi tiek rādīti arī **Tērzēšanas** zonā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="73f7e-166">Ja esat apstiprinātājs, varat izvēlēties **Apstiprināt** vai **Atteikt** paziņojumā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="73f7e-167">Var arī norādīt neobligātu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-167">You can also provide an optional message.</span></span>

![Atvaļinājuma pieprasījuma paziņojums Human Resources Teams programmā](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="73f7e-169">Sūtīt gaidāmās prombūtnes informāciju saviem kolēģiem</span><span class="sxs-lookup"><span data-stu-id="73f7e-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="73f7e-170">Pēc tam, kad esat instalējis Human Resources programmu Teams, varat vienkārši nosūtīt informāciju par jūsu gaidāmo prombūtni saviem kolēģiem grupās vai tērzēšanā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="73f7e-171">Programmas Teams grupā vai tērzēšanā atlasiet Human Resources pogu zem tērzēšanas loga.</span><span class="sxs-lookup"><span data-stu-id="73f7e-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources poga zem tērzēšanas loga](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="73f7e-173">Atlasiet atvaļinājuma pieprasījumu, kuru vēlaties kopīgot.</span><span class="sxs-lookup"><span data-stu-id="73f7e-173">Select the leave request you want to share.</span></span> <span data-ttu-id="73f7e-174">Ja vēlaties kopīgot melnraksta atvaļinājuma pieprasījumu, vispirms atlasiet **Melnraksti**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Atlasīt gaidāmā atvaļinājuma pieprasījumu koplietošanai](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="73f7e-176">Jūsu atvaļinājuma pieprasījums tiks parādīts tērzēšanā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-176">Your leave request will display in the chat.</span></span>

![Human Resources programmas atvaļinājuma pieprasījuma karte](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="73f7e-178">Ja esat kopīgojis melnraksta pieprasījumu, tas tiks parādīts kā melnraksts:</span><span class="sxs-lookup"><span data-stu-id="73f7e-178">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources programmas atvaļinājuma pieprasījuma kartes melnraksts](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="73f7e-180">Skatiet savas grupas atvaļinājuma kalendāru</span><span class="sxs-lookup"><span data-stu-id="73f7e-180">View your team's leave calendar</span></span>

<span data-ttu-id="73f7e-181">Ja esat vādītājs ar tiešajiem pārskatiem, varat apskatīt savas grupas apstiprināto un gaidošo brīvo laiku.</span><span class="sxs-lookup"><span data-stu-id="73f7e-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="73f7e-182">Programmā Human Resources risinājumā Teams atlasiet **Brīvais laiks**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="73f7e-183">Atlasiet **Grupas kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="73f7e-183">Select **Team calendar**.</span></span>

   ![Skatīt kalendāru programmā Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="73f7e-185">Kalendārā tiek rādīti jūsu tiešo pārskatu apstiprinātais un gaidošais brīvais laiks.</span><span class="sxs-lookup"><span data-stu-id="73f7e-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Brīvā laika kalendārs programmā Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="73f7e-187">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="73f7e-187">Troubleshooting</span></span>

<span data-ttu-id="73f7e-188">Ja jums rodas problēmas, pierakstoties vai izmantojot personāla vadības lietojumprogrammu Teams, izmēģiniet šīs problēmu novēršanas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="73f7e-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="73f7e-189">Ja pēc problēmu novēršanas problēmas joprojām pastāv, sazinieties ar atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="73f7e-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="73f7e-190">Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="73f7e-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="73f7e-191">Nevar pierakstīties personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="73f7e-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="73f7e-192">Ja nevarat pierakstīties lietojumprogrammā, iespējams, ka konts, kuru izmantojat, lai pierakstītos Microsoft Teams nav saistīts ar darbinieka ierakstu Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73f7e-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="73f7e-193">Sazinieties ar sistēmas administratoru, lai pārliecinātos, ka darbinieka ieraksts ir pareizi saistīts.</span><span class="sxs-lookup"><span data-stu-id="73f7e-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="73f7e-194">Kļūda, apstiprinot atvaļinājumu pieprasījumus personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="73f7e-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="73f7e-195">Ja jūs saņemat kļūdu, mēģinot apstiprināt atvaļinājumu pieprasījumus lietojumprogrammā Teams, veiciet tālāk norādītos problēmu novēršanas pasākumus:</span><span class="sxs-lookup"><span data-stu-id="73f7e-195">If you receive an error when you're trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="73f7e-196">Pārbaudiet, vai konts, kuru izmantojat, lai pierakstītos Microsoft Teams ir tas pats, ko izmantojat, lai piekļūtu Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73f7e-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="73f7e-197">Pārbaudiet, vai esat derīgs pieprasījuma apstiprinātājs, pārbaudot darbplūsmas iestatījumus atvaļinājumu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="73f7e-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="73f7e-198">Papildinformāciju par atvaļinājumu pieprasījumu darbplūsmām skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="73f7e-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="73f7e-199">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="73f7e-199">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="73f7e-200">Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)</span><span class="sxs-lookup"><span data-stu-id="73f7e-200">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="73f7e-201">Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku.</span><span class="sxs-lookup"><span data-stu-id="73f7e-201">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="73f7e-202">Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS).</span><span class="sxs-lookup"><span data-stu-id="73f7e-202">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="73f7e-203">Lasīt vairāk par LUIS [šeit](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="73f7e-203">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="73f7e-204">LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso).</span><span class="sxs-lookup"><span data-stu-id="73f7e-204">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="73f7e-205">Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="73f7e-205">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="73f7e-206">Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="73f7e-206">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="73f7e-207">LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73f7e-207">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="73f7e-208">Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru.</span><span class="sxs-lookup"><span data-stu-id="73f7e-208">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="73f7e-209">Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā.</span><span class="sxs-lookup"><span data-stu-id="73f7e-209">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="73f7e-210">Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="73f7e-210">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="73f7e-211">Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="73f7e-211">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="73f7e-212">Microsoft Teams, Azure Event Grid un Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="73f7e-212">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="73f7e-213">Izmantojot programmu Dynamics 365 Human Resources risinājumā Microsoft Teams, noteikti klienta dati var ieplūst ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="73f7e-213">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="73f7e-214">Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="73f7e-214">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="73f7e-215">Šos datus var uzglabāt Microsoft Azure Event Grid līdz 24 stundām un tie tiks apstrādāti Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="73f7e-215">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="73f7e-216">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="73f7e-216">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="73f7e-217">Sarunājoties ar botu Human Resources programmā, sarunas saturs var tikt saglabāts Azure Cosmos DB un pārsūtīts uz Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="73f7e-217">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="73f7e-218">Šie dati var tikt glabāti Azure Cosmos DB līdz 24 stundām un tos var apstrādāt ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="73f7e-218">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="73f7e-219">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="73f7e-219">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="73f7e-220">Lai ierobežotu piekļuvi Human Resources programmai Microsoft Teams jūsu organizācijā vai lietotājiem jūsu organizācijā, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="73f7e-220">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="73f7e-221">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="73f7e-221">See also</span></span>

[<span data-ttu-id="73f7e-222">Lejupielāde un instalēšana Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="73f7e-222">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="73f7e-223">Microsoft Teams palīdzības centrs</span><span class="sxs-lookup"><span data-stu-id="73f7e-223">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="73f7e-224">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="73f7e-224">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
