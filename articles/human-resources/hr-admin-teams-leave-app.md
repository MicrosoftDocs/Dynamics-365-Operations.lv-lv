---
title: Programma Human Resources programmā Teams
description: Šī tēma iepazīstina jūs ar programmu Microsoft Dynamics 365 Human Resources sadaļā Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b44cee0574794ae4b3cfd1987934aa4933b46b2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803997"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="0be99-103">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="0be99-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0be99-104">Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj darbiniekiem ātri pieprasīt prombūtni un skatīt savu laiku ārpusbilances informāciju Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0be99-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="0be99-105">Darbinieki var sazināties ar botu, lai pieprasītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="0be99-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="0be99-106">Cilne **Brīvais laiks** sniedz detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="0be99-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="0be99-107">Turklāt darbinieki var nosūtīt personām informāciju par gaidāmo prombūtni grupās un tērzēšanas sarunās ārpus personāla vadības lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="0be99-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams atstāj programmu botu](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams atstāj programmas cilni Brīvais laiks](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources programmas atvaļinājuma pieprasījuma karte](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="0be99-111">Instalēt un iestatīt</span><span class="sxs-lookup"><span data-stu-id="0be99-111">Install and setup</span></span>

<span data-ttu-id="0be99-112">Dynamics 365 Human Resources programmu varat atrast Teams veikalā.</span><span class="sxs-lookup"><span data-stu-id="0be99-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="0be99-113">Informāciju par programmas Teams instalēšanu skatiet sadaļā [Pārvaldīt atvaļinājumu pieprasījumus programmā Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="0be99-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="0be99-114">Lai iegūtu informāciju par programmu atļauju pārvaldību programmā Teams, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="0be99-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="0be99-115">Ja vēlaties, lai lietotāji programmā skatītu atvaļinājumu un prombūtnes kalendāru, funkcionalitātes pārvaldībā aktivizējiet kalendāru **Atvaļinājums un kavējumi darba komandās**.</span><span class="sxs-lookup"><span data-stu-id="0be99-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="0be99-116">Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="0be99-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="0be99-117">Iespējot paziņojumus programmai Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="0be99-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="0be99-118">Ja vēlaties, lai lietotāji saņemtu paziņojumus par atvaļinājumu pieprasījumiem programmā Teams, paziņojumi ir jāiespējo programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0be99-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="0be99-119">Paziņojumus saņems tikai tie lietotāji, kuri ir pieteikušies Teams un izmanto Dynamics 365 Human Resources Teams programmu.</span><span class="sxs-lookup"><span data-stu-id="0be99-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="0be99-120">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="0be99-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="0be99-121">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="0be99-121">Select **Links**.</span></span>

3. <span data-ttu-id="0be99-122">Sadaļā **Iestatīšana** atlasiet **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="0be99-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="0be99-123">Cilnē **Vispārīgi** iestatiet **Iespējot paziņojumus Teams programmai** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0be99-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivizējiet Teams programmas paziņojumus Sistēmas parametros](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="0be99-125">Lai ieslēgtu Teams paziņojumus visiem lietotājiem, uzvednē atlasiet **Jā** .</span><span class="sxs-lookup"><span data-stu-id="0be99-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Iespējojiet Teams paziņojumus visiem lietotājiem](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="0be99-127">Ieslēdziet vai izslēdziet Teams paziņojumus atsevišķiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="0be99-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="0be99-128">Pēc tam, kad esat iespējojis paziņojumus Dynamics 365 Human Resources Teams programmai, varat ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="0be99-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="0be99-129">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="0be99-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="0be99-130">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="0be99-130">Select **Links**.</span></span>

3. <span data-ttu-id="0be99-131">Sadaļā **Lietotāji** atlasiet **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="0be99-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="0be99-132">Atlasiet cilni **Darbplūsma** .</span><span class="sxs-lookup"><span data-stu-id="0be99-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="0be99-133">Iestatiet opciju **Iespējot paziņojumus programmai Teams** uz **Jā** , lai lietotājam iespējotu paziņojumus, vai uz **Nē**, lai atspējotu paziņojumus lietotājam.</span><span class="sxs-lookup"><span data-stu-id="0be99-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Iespējojiet Teams programmas paziņojumus cilnē Lietotāju opciju darbplūsma](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="0be99-135">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0be99-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="0be99-136">Atbalstītās valodas</span><span class="sxs-lookup"><span data-stu-id="0be99-136">Supported languages</span></span>

<span data-ttu-id="0be99-137">Programma Dynamics 365 Human Resources lietotnē Teams atbalsta šādas valodas:</span><span class="sxs-lookup"><span data-stu-id="0be99-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="0be99-138">Atrašanās vietas ID</span><span class="sxs-lookup"><span data-stu-id="0be99-138">Locale ID</span></span> | <span data-ttu-id="0be99-139">Valoda</span><span class="sxs-lookup"><span data-stu-id="0be99-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="0be99-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="0be99-140">de-DE</span></span> | <span data-ttu-id="0be99-141">Vācu (Vācija)</span><span class="sxs-lookup"><span data-stu-id="0be99-141">German (Germany)</span></span> |
| <span data-ttu-id="0be99-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="0be99-142">es-ES</span></span> | <span data-ttu-id="0be99-143">Spāņu (Spānija)</span><span class="sxs-lookup"><span data-stu-id="0be99-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="0be99-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="0be99-144">es-MX</span></span> | <span data-ttu-id="0be99-145">Spāņu (Meksika)</span><span class="sxs-lookup"><span data-stu-id="0be99-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="0be99-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="0be99-146">fr-CA</span></span> | <span data-ttu-id="0be99-147">Franču (Kanāda)</span><span class="sxs-lookup"><span data-stu-id="0be99-147">French (Canada)</span></span> |
| <span data-ttu-id="0be99-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="0be99-148">fr-FR</span></span> | <span data-ttu-id="0be99-149">Franču (Francija)</span><span class="sxs-lookup"><span data-stu-id="0be99-149">French (France)</span></span> |
| <span data-ttu-id="0be99-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="0be99-150">it-IT</span></span> | <span data-ttu-id="0be99-151">Itāļu (Itālija)</span><span class="sxs-lookup"><span data-stu-id="0be99-151">Italian (Italy)</span></span> |
| <span data-ttu-id="0be99-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="0be99-152">nl-NL</span></span> | <span data-ttu-id="0be99-153">Holandiešu (Nīderlande)</span><span class="sxs-lookup"><span data-stu-id="0be99-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="0be99-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="0be99-154">pt-BR</span></span> | <span data-ttu-id="0be99-155">Portugāļu (Brazīlija)</span><span class="sxs-lookup"><span data-stu-id="0be99-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="0be99-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="0be99-156">tr-TR</span></span> | <span data-ttu-id="0be99-157">Turku (Turcija)</span><span class="sxs-lookup"><span data-stu-id="0be99-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="0be99-158">zh-(CN)</span><span class="sxs-lookup"><span data-stu-id="0be99-158">zh-CN</span></span> | <span data-ttu-id="0be99-159">Ķīniešu (vienkāršotā)</span><span class="sxs-lookup"><span data-stu-id="0be99-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="0be99-160">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="0be99-160">Notes</span></span>

<span data-ttu-id="0be99-161">Turpmākajiem laidieniem ir noslīdētas šādas darba vienības:</span><span class="sxs-lookup"><span data-stu-id="0be99-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="0be99-162">Darbplūsmas elements</span><span class="sxs-lookup"><span data-stu-id="0be99-162">Work item</span></span> | <span data-ttu-id="0be99-163">Statuss</span><span class="sxs-lookup"><span data-stu-id="0be99-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="0be99-164">Bilance nav pareiza, iesniedzot prombūtni nākotnes datumam.</span><span class="sxs-lookup"><span data-stu-id="0be99-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="0be99-165">Videoklips vēl nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="0be99-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="0be99-166">Parādās pašreizējā datuma bilance.</span><span class="sxs-lookup"><span data-stu-id="0be99-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="0be99-167">Nevar atcelt **Pārskatā** pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="0be99-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="0be99-168">Šī funkcionalitāte pašlaik netiek atbalstīta, un tā tiks pievienota nākošajā laidienā.</span><span class="sxs-lookup"><span data-stu-id="0be99-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="0be99-169">Bilances informācija tiek aprēķināta no šodienas.</span><span class="sxs-lookup"><span data-stu-id="0be99-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="0be99-170">Sistēma pašlaik neparāda uzkrājumu perioda bilances, pat ja tās ir konfigurētas atvaļinājumu un prombūtnes parametros.</span><span class="sxs-lookup"><span data-stu-id="0be99-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="0be99-171">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="0be99-171">Troubleshooting</span></span>

<span data-ttu-id="0be99-172">Ja lietotājam rodas problēmas, pierakstoties vai izmantojot personāla vadības lietojumprogrammu Teams, izmēģiniet šīs problēmu novēršanas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="0be99-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="0be99-173">Ja pēc problēmu novēršanas problēmas joprojām pastāv, sazinieties ar atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="0be99-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="0be99-174">Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="0be99-174">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="0be99-175">Nevar pierakstīties personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="0be99-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="0be99-176">Ja lietotājs sazinās ar jums, jo viņš nevar pierakstīties lietojumprogrammā, pārbaudiet, vai lietotājam ir saistītais darbinieka ieraksts personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="0be99-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="0be99-177">Kļūda, apstiprinot atvaļinājumu pieprasījumus personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="0be99-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="0be99-178">Ja lietotājs saņem kļūdas ziņojumu, mēģinot apstiprināt atvaļinājumu pieprasījumus lietojumprogrammā Teams, veiciet tālāk norādītos problēmu novēršanas pasākumus:</span><span class="sxs-lookup"><span data-stu-id="0be99-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="0be99-179">Pārbaudiet, vai lietotāja Teams konts ir tas pats, ko lietotājs izmanto, lai piekļūtu personāla vadībai.</span><span class="sxs-lookup"><span data-stu-id="0be99-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="0be99-180">Pārbaudiet, vai lietotājs ir derīgs pieprasījuma apstiprinātājs, pārbaudot darbplūsmas iestatījumus atvaļinājumu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="0be99-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="0be99-181">Papildinformāciju par atvaļinājumu pieprasījumu darbplūsmām skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="0be99-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0be99-182">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="0be99-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="0be99-183">Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)</span><span class="sxs-lookup"><span data-stu-id="0be99-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="0be99-184">Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku.</span><span class="sxs-lookup"><span data-stu-id="0be99-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="0be99-185">Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS).</span><span class="sxs-lookup"><span data-stu-id="0be99-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="0be99-186">Lasīt vairāk par LUIS [šeit](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="0be99-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="0be99-187">LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso).</span><span class="sxs-lookup"><span data-stu-id="0be99-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="0be99-188">Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="0be99-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="0be99-189">Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="0be99-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="0be99-190">LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0be99-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0be99-191">Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru.</span><span class="sxs-lookup"><span data-stu-id="0be99-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="0be99-192">Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā.</span><span class="sxs-lookup"><span data-stu-id="0be99-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="0be99-193">Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="0be99-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="0be99-194">Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="0be99-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="0be99-195">Microsoft Teams, Azure Event Grid un Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0be99-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="0be99-196">Izmantojot programmu Dynamics 365 Human Resources risinājumā Microsoft Teams, noteikti klienta dati var ieplūst ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="0be99-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="0be99-197">Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0be99-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="0be99-198">Šos datus var uzglabāt Microsoft Azure Event Grid līdz 24 stundām un tie tiks apstrādāti Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="0be99-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0be99-199">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="0be99-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="0be99-200">Sarunājoties ar botu Human Resources programmā, sarunas saturs var tikt saglabāts Azure Cosmos DB un pārsūtīts uz Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0be99-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="0be99-201">Šie dati var tikt glabāti Azure Cosmos DB līdz 24 stundām un tos var apstrādāt ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="0be99-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0be99-202">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="0be99-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="0be99-203">Lai ierobežotu piekļuvi Human Resources programmai Microsoft Teams jūsu organizācijā vai lietotājiem jūsu organizācijā, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="0be99-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="0be99-204">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="0be99-204">See also</span></span> 

[<span data-ttu-id="0be99-205">Lejupielāde un instalēšana Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0be99-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="0be99-206">Microsoft Teams palīdzības centrs</span><span class="sxs-lookup"><span data-stu-id="0be99-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="0be99-207">Atvaļinājumu pieprasījumu pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="0be99-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]