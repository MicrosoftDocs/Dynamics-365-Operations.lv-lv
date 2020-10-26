---
title: Programma Human Resources programmā Teams
description: Šī tēma iepazīstina jūs ar programmu Microsoft Dynamics 365 Human Resources sadaļā Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 51f04e553da822c4e09d31bcd72c71b674ad1f1b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930021"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="181ea-103">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="181ea-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="181ea-104">Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj darbiniekiem ātri pieprasīt prombūtni un skatīt savu laiku ārpusbilances informāciju Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="181ea-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="181ea-105">Darbinieki var sazināties ar botu, lai pieprasītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="181ea-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="181ea-106">Cilne **Brīvais laiks** sniedz detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="181ea-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="181ea-107">Turklāt darbinieki var nosūtīt personām informāciju par gaidāmo prombūtni grupās un tērzēšanas sarunās ārpus personāla vadības lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="181ea-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams atstāj programmu botu](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams atstāj programmas cilni Brīvais laiks](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources programmas atvaļinājuma pieprasījuma karte](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="181ea-111">Instalēt un iestatīt</span><span class="sxs-lookup"><span data-stu-id="181ea-111">Install and setup</span></span>

<span data-ttu-id="181ea-112">Human Resources programmu varat atrast Teams veikalā.</span><span class="sxs-lookup"><span data-stu-id="181ea-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="181ea-113">Informāciju par programmas Teams instalēšanu skatiet sadaļā [Pārvaldīt atvaļinājumu pieprasījumus programmā Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="181ea-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="181ea-114">Lai iegūtu informāciju par programmu atļauju pārvaldību programmā Teams, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="181ea-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="181ea-115">Iespējot paziņojumus programmai Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="181ea-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="181ea-116">Ja vēlaties, lai lietotāji saņemtu paziņojumus par atvaļinājumu pieprasījumiem programmā Teams, paziņojumi ir jāiespējo programmā Human Resources.</span><span class="sxs-lookup"><span data-stu-id="181ea-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="181ea-117">Paziņojumus saņems tikai tie lietotāji, kuri ir pieteikušies Teams un izmanto Human Resources Teams programmu.</span><span class="sxs-lookup"><span data-stu-id="181ea-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="181ea-118">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="181ea-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="181ea-119">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="181ea-119">Select **Links**.</span></span>

3. <span data-ttu-id="181ea-120">Sadaļā **Iestatīšana** atlasiet **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="181ea-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="181ea-121">Cilnē **Vispārīgi** iestatiet **Iespējot paziņojumus Teams programmai** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="181ea-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivizējiet Teams programmas paziņojumus Sistēmas parametros](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="181ea-123">Lai ieslēgtu Teams paziņojumus visiem lietotājiem, uzvednē atlasiet **Jā** .</span><span class="sxs-lookup"><span data-stu-id="181ea-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Iespējojiet Teams paziņojumus visiem lietotājiem](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="181ea-125">Ieslēdziet vai izslēdziet Teams paziņojumus atsevišķiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="181ea-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="181ea-126">Pēc tam, kad esat iespējojis paziņojumus Human Resources Teams programmai, varat ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="181ea-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="181ea-127">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="181ea-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="181ea-128">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="181ea-128">Select **Links**.</span></span>

3. <span data-ttu-id="181ea-129">Sadaļā **Lietotāji** atlasiet **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="181ea-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="181ea-130">Atlasiet cilni **Darbplūsma** .</span><span class="sxs-lookup"><span data-stu-id="181ea-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="181ea-131">Iestatiet opciju **Iespējot paziņojumus programmai Teams** uz **Jā** , lai lietotājam iespējotu paziņojumus, vai uz **Nē**, lai atspējotu paziņojumus lietotājam.</span><span class="sxs-lookup"><span data-stu-id="181ea-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Iespējojiet Teams programmas paziņojumus cilnē Lietotāju opciju darbplūsma](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="181ea-133">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="181ea-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="181ea-134">Zināmās problēmas</span><span class="sxs-lookup"><span data-stu-id="181ea-134">Known issues</span></span>

| <span data-ttu-id="181ea-135">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="181ea-135">Issue</span></span> | <span data-ttu-id="181ea-136">Statuss</span><span class="sxs-lookup"><span data-stu-id="181ea-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="181ea-137">Horizontālā ritināšana nedarbojas Android tālruņos</span><span class="sxs-lookup"><span data-stu-id="181ea-137">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="181ea-138">Horizontālā ritināšana nav problēma iOS vai galddatora ierīcēs.</span><span class="sxs-lookup"><span data-stu-id="181ea-138">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="181ea-139">Mēs strādājam pie risinājuma Android.</span><span class="sxs-lookup"><span data-stu-id="181ea-139">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="181ea-140">Bilance nav pareiza, iesniedzot prombūtni nākotnes datumam.</span><span class="sxs-lookup"><span data-stu-id="181ea-140">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="181ea-141">Videoklips vēl nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="181ea-141">Forecasting isn't yet available.</span></span> <span data-ttu-id="181ea-142">Parādās pašreizējā datuma bilance.</span><span class="sxs-lookup"><span data-stu-id="181ea-142">The balance displays for the current date.</span></span> |
| <span data-ttu-id="181ea-143">Nevar atcelt **Pārskatā** pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="181ea-143">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="181ea-144">Šī funkcionalitāte pašlaik netiek atbalstīta, un tā tiks pievienota nākošajā laidienā.</span><span class="sxs-lookup"><span data-stu-id="181ea-144">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="181ea-145">Bilances informācija tiek aprēķināta no šodienas.</span><span class="sxs-lookup"><span data-stu-id="181ea-145">Balance information is calculated as of today.</span></span> | <span data-ttu-id="181ea-146">Sistēma pašlaik neparāda uzkrājumu perioda bilances, pat ja tās ir konfigurētas atvaļinājumu un prombūtnes parametros.</span><span class="sxs-lookup"><span data-stu-id="181ea-146">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="181ea-147">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="181ea-147">Troubleshooting</span></span>

<span data-ttu-id="181ea-148">Ja lietotājam rodas problēmas, pierakstoties vai izmantojot personāla vadības lietojumprogrammu Teams, izmēģiniet šīs problēmu novēršanas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="181ea-148">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="181ea-149">Ja pēc problēmu novēršanas problēmas joprojām pastāv, sazinieties ar atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="181ea-149">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="181ea-150">Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="181ea-150">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="181ea-151">Nevar pierakstīties personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="181ea-151">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="181ea-152">Ja lietotājs sazinās ar jums, jo viņš nevar pierakstīties lietojumprogrammā, pārbaudiet, vai lietotājam ir saistītais darbinieka ieraksts personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="181ea-152">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="181ea-153">Kļūda, apstiprinot atvaļinājumu pieprasījumus personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="181ea-153">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="181ea-154">Ja lietotājs saņem kļūdas ziņojumu, mēģinot apstiprināt atvaļinājumu pieprasījumus lietojumprogrammā Teams, veiciet tālāk norādītos problēmu novēršanas pasākumus:</span><span class="sxs-lookup"><span data-stu-id="181ea-154">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="181ea-155">Pārbaudiet, vai lietotāja Teams konts ir tas pats, ko lietotājs izmanto, lai piekļūtu personāla vadībai.</span><span class="sxs-lookup"><span data-stu-id="181ea-155">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="181ea-156">Pārbaudiet, vai lietotājs ir derīgs pieprasījuma apstiprinātājs, pārbaudot darbplūsmas iestatījumus atvaļinājumu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="181ea-156">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="181ea-157">Papildinformāciju par atvaļinājumu pieprasījumu darbplūsmām skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="181ea-157">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="181ea-158">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="181ea-158">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="181ea-159">Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)</span><span class="sxs-lookup"><span data-stu-id="181ea-159">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="181ea-160">Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku.</span><span class="sxs-lookup"><span data-stu-id="181ea-160">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="181ea-161">Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS).</span><span class="sxs-lookup"><span data-stu-id="181ea-161">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="181ea-162">Lasīt vairāk par LUIS [šeit](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="181ea-162">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="181ea-163">LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso).</span><span class="sxs-lookup"><span data-stu-id="181ea-163">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="181ea-164">Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="181ea-164">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="181ea-165">Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="181ea-165">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="181ea-166">LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="181ea-166">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="181ea-167">Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru.</span><span class="sxs-lookup"><span data-stu-id="181ea-167">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="181ea-168">Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā.</span><span class="sxs-lookup"><span data-stu-id="181ea-168">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="181ea-169">Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="181ea-169">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="181ea-170">Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="181ea-170">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="181ea-171">Microsoft Teams, Azure Event Grid un Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="181ea-171">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="181ea-172">Izmantojot programmu Dynamics 365 Human Resources risinājumā Microsoft Teams, noteikti klienta dati var ieplūst ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="181ea-172">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="181ea-173">Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="181ea-173">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="181ea-174">Šos datus var uzglabāt Microsoft Azure Event Grid līdz 24 stundām un tie tiks apstrādāti Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="181ea-174">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="181ea-175">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="181ea-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="181ea-176">Sarunājoties ar botu Human Resources programmā, sarunas saturs var tikt saglabāts Azure Cosmos DB un pārsūtīts uz Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="181ea-176">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="181ea-177">Šie dati var tikt glabāti Azure Cosmos DB līdz 24 stundām un tos var apstrādāt ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="181ea-177">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="181ea-178">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="181ea-178">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="181ea-179">Lai ierobežotu piekļuvi Human Resources programmai Microsoft Teams jūsu organizācijā vai lietotājiem jūsu organizācijā, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="181ea-179">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="181ea-180">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="181ea-180">See also</span></span> 

[<span data-ttu-id="181ea-181">Lejupielāde un instalēšana Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="181ea-181">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="181ea-182">Microsoft Teams palīdzības centrs</span><span class="sxs-lookup"><span data-stu-id="181ea-182">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="181ea-183">Atvaļinājumu pieprasījumu pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="181ea-183">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

