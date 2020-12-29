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
ms.openlocfilehash: e714be06984f399235f0799ef077a92deae64d9e
ms.sourcegitcommit: b0aa724a18ab1fbb5a62925f048c54b2c676ebf4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2020
ms.locfileid: "4476081"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="7a5ff-103">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="7a5ff-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7a5ff-104">Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj darbiniekiem ātri pieprasīt prombūtni un skatīt savu laiku ārpusbilances informāciju Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="7a5ff-105">Darbinieki var sazināties ar botu, lai pieprasītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="7a5ff-106">Cilne **Brīvais laiks** sniedz detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="7a5ff-107">Turklāt darbinieki var nosūtīt personām informāciju par gaidāmo prombūtni grupās un tērzēšanas sarunās ārpus personāla vadības lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams atstāj programmu botu](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams atstāj programmas cilni Brīvais laiks](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources programmas atvaļinājuma pieprasījuma karte](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="7a5ff-111">Instalēt un iestatīt</span><span class="sxs-lookup"><span data-stu-id="7a5ff-111">Install and setup</span></span>

<span data-ttu-id="7a5ff-112">Human Resources programmu varat atrast Teams veikalā.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="7a5ff-113">Informāciju par programmas Teams instalēšanu skatiet sadaļā [Pārvaldīt atvaļinājumu pieprasījumus programmā Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="7a5ff-114">Lai iegūtu informāciju par programmu atļauju pārvaldību programmā Teams, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="7a5ff-115">Iespējot paziņojumus programmai Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="7a5ff-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="7a5ff-116">Ja vēlaties, lai lietotāji saņemtu paziņojumus par atvaļinājumu pieprasījumiem programmā Teams, paziņojumi ir jāiespējo programmā Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="7a5ff-117">Paziņojumus saņems tikai tie lietotāji, kuri ir pieteikušies Teams un izmanto Human Resources Teams programmu.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="7a5ff-118">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7a5ff-119">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-119">Select **Links**.</span></span>

3. <span data-ttu-id="7a5ff-120">Sadaļā **Iestatīšana** atlasiet **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="7a5ff-121">Cilnē **Vispārīgi** iestatiet **Iespējot paziņojumus Teams programmai** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivizējiet Teams programmas paziņojumus Sistēmas parametros](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="7a5ff-123">Lai ieslēgtu Teams paziņojumus visiem lietotājiem, uzvednē atlasiet **Jā** .</span><span class="sxs-lookup"><span data-stu-id="7a5ff-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Iespējojiet Teams paziņojumus visiem lietotājiem](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="7a5ff-125">Ieslēdziet vai izslēdziet Teams paziņojumus atsevišķiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="7a5ff-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="7a5ff-126">Pēc tam, kad esat iespējojis paziņojumus Human Resources Teams programmai, varat ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="7a5ff-127">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7a5ff-128">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-128">Select **Links**.</span></span>

3. <span data-ttu-id="7a5ff-129">Sadaļā **Lietotāji** atlasiet **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="7a5ff-130">Atlasiet cilni **Darbplūsma** .</span><span class="sxs-lookup"><span data-stu-id="7a5ff-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="7a5ff-131">Iestatiet opciju **Iespējot paziņojumus programmai Teams** uz **Jā** , lai lietotājam iespējotu paziņojumus, vai uz **Nē**, lai atspējotu paziņojumus lietotājam.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Iespējojiet Teams programmas paziņojumus cilnē Lietotāju opciju darbplūsma](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="7a5ff-133">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="7a5ff-134">Zināmās problēmas</span><span class="sxs-lookup"><span data-stu-id="7a5ff-134">Known issues</span></span>

| <span data-ttu-id="7a5ff-135">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="7a5ff-135">Issue</span></span> | <span data-ttu-id="7a5ff-136">Statuss</span><span class="sxs-lookup"><span data-stu-id="7a5ff-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="7a5ff-137">Bilance nav pareiza, iesniedzot prombūtni nākotnes datumam.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-137">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="7a5ff-138">Videoklips vēl nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-138">Forecasting isn't yet available.</span></span> <span data-ttu-id="7a5ff-139">Parādās pašreizējā datuma bilance.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-139">The balance displays for the current date.</span></span> |
| <span data-ttu-id="7a5ff-140">Nevar atcelt **Pārskatā** pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-140">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="7a5ff-141">Šī funkcionalitāte pašlaik netiek atbalstīta, un tā tiks pievienota nākošajā laidienā.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-141">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="7a5ff-142">Bilances informācija tiek aprēķināta no šodienas.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-142">Balance information is calculated as of today.</span></span> | <span data-ttu-id="7a5ff-143">Sistēma pašlaik neparāda uzkrājumu perioda bilances, pat ja tās ir konfigurētas atvaļinājumu un prombūtnes parametros.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-143">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="7a5ff-144">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="7a5ff-144">Troubleshooting</span></span>

<span data-ttu-id="7a5ff-145">Ja lietotājam rodas problēmas, pierakstoties vai izmantojot personāla vadības lietojumprogrammu Teams, izmēģiniet šīs problēmu novēršanas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-145">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="7a5ff-146">Ja pēc problēmu novēršanas problēmas joprojām pastāv, sazinieties ar atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-146">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="7a5ff-147">Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-147">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="7a5ff-148">Nevar pierakstīties personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="7a5ff-148">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="7a5ff-149">Ja lietotājs sazinās ar jums, jo viņš nevar pierakstīties lietojumprogrammā, pārbaudiet, vai lietotājam ir saistītais darbinieka ieraksts personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-149">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="7a5ff-150">Kļūda, apstiprinot atvaļinājumu pieprasījumus personāla vadības lietojumprogrammā Teams</span><span class="sxs-lookup"><span data-stu-id="7a5ff-150">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="7a5ff-151">Ja lietotājs saņem kļūdas ziņojumu, mēģinot apstiprināt atvaļinājumu pieprasījumus lietojumprogrammā Teams, veiciet tālāk norādītos problēmu novēršanas pasākumus:</span><span class="sxs-lookup"><span data-stu-id="7a5ff-151">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="7a5ff-152">Pārbaudiet, vai lietotāja Teams konts ir tas pats, ko lietotājs izmanto, lai piekļūtu personāla vadībai.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-152">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="7a5ff-153">Pārbaudiet, vai lietotājs ir derīgs pieprasījuma apstiprinātājs, pārbaudot darbplūsmas iestatījumus atvaļinājumu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-153">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="7a5ff-154">Papildinformāciju par atvaļinājumu pieprasījumu darbplūsmām skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-154">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="7a5ff-155">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="7a5ff-155">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="7a5ff-156">Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)</span><span class="sxs-lookup"><span data-stu-id="7a5ff-156">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="7a5ff-157">Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-157">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="7a5ff-158">Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-158">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="7a5ff-159">Lasīt vairāk par LUIS [šeit](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-159">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="7a5ff-160">LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-160">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="7a5ff-161">Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-161">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="7a5ff-162">Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-162">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="7a5ff-163">LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-163">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7a5ff-164">Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-164">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="7a5ff-165">Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-165">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="7a5ff-166">Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-166">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="7a5ff-167">Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-167">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="7a5ff-168">Microsoft Teams, Azure Event Grid un Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7a5ff-168">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="7a5ff-169">Izmantojot programmu Dynamics 365 Human Resources risinājumā Microsoft Teams, noteikti klienta dati var ieplūst ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-169">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="7a5ff-170">Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-170">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="7a5ff-171">Šos datus var uzglabāt Microsoft Azure Event Grid līdz 24 stundām un tie tiks apstrādāti Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-171">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="7a5ff-172">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-172">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="7a5ff-173">Sarunājoties ar botu Human Resources programmā, sarunas saturs var tikt saglabāts Azure Cosmos DB un pārsūtīts uz Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-173">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="7a5ff-174">Šie dati var tikt glabāti Azure Cosmos DB līdz 24 stundām un tos var apstrādāt ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="7a5ff-174">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="7a5ff-175">Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="7a5ff-176">Lai ierobežotu piekļuvi Human Resources programmai Microsoft Teams jūsu organizācijā vai lietotājiem jūsu organizācijā, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="7a5ff-176">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="7a5ff-177">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="7a5ff-177">See also</span></span> 

[<span data-ttu-id="7a5ff-178">Lejupielāde un instalēšana Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7a5ff-178">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="7a5ff-179">Microsoft Teams palīdzības centrs</span><span class="sxs-lookup"><span data-stu-id="7a5ff-179">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="7a5ff-180">Atvaļinājumu pieprasījumu pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="7a5ff-180">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

