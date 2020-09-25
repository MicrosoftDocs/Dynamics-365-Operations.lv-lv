---
title: Personāla vadības programma programmā Teams
description: Šī tēma iepazīstina jūs ar programmu Microsoft Dynamics 365 Human Resources sadaļā Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776312"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="bf8b5-103">Personāla vadības programma programmā Teams</span><span class="sxs-lookup"><span data-stu-id="bf8b5-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bf8b5-104">Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj darbiniekiem ātri pieprasīt prombūtni un skatīt savu laiku ārpusbilances informāciju Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="bf8b5-105">Darbinieki var sazināties ar botu, lai pieprasītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="bf8b5-106">Cilne **Laiks izslēgts** sniedz detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-106">The **Time off** tab provides more detailed information.</span></span>

![Personāla vadība Teams atstāj programmu botu](./media/hr-admin-teams-leave-app-bot.png)

![Personāla vadība Teams atstāj programmas cilni Laiks izslēgts](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="bf8b5-109">Instalēt un iestatīt</span><span class="sxs-lookup"><span data-stu-id="bf8b5-109">Install and setup</span></span>

<span data-ttu-id="bf8b5-110">Personāla vadības programmu varat atrast Teams veikalā.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="bf8b5-111">Informāciju par programmu grupu instalēšanu skatiet sadaļā [Pārvaldīt atvaļinājumu pieprasījumus komandās](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="bf8b5-112">Lai iegūtu informāciju par programmu atļauju pārvaldību grupās, skatiet sadaļu [programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="bf8b5-113">Iespējot paziņojumus programmai Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="bf8b5-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="bf8b5-114">Ja vēlaties, lai lietotāji saņemtu paziņojumus par atvaļinājumu pieprasījumiem programmā Teams, paziņojumi ir jāiespējo programmā Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="bf8b5-115">Paziņojumus saņems tikai tie lietotāji, kuri ir pieteikušies Teams un izmanto Human Resources Teams programmu.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="bf8b5-116">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="bf8b5-117">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-117">Select **Links**.</span></span>

3. <span data-ttu-id="bf8b5-118">Sadaļā **Iestatīšana** atlasiet **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="bf8b5-119">Cilnē **Vispārīgi** iestatiet **Iespējot paziņojumus Teams programmai** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivizējiet Teams programmas paziņojumus Sistēmas parametros](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="bf8b5-121">Lai ieslēgtu Teams paziņojumus visiem lietotājiem, uzvednē atlasiet **Jā** .</span><span class="sxs-lookup"><span data-stu-id="bf8b5-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Iespējojiet Teams paziņojumus visiem lietotājiem](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="bf8b5-123">Ieslēzdiet vai izslēdziet Teams paziņojumus atsevišķiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="bf8b5-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="bf8b5-124">Pēc tam, kad esat iespējojis paziņojumus Human Resources Teams programmai, varat ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="bf8b5-125">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="bf8b5-126">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-126">Select **Links**.</span></span>

3. <span data-ttu-id="bf8b5-127">Sadaļā **Lietotāji** atlasiet **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="bf8b5-128">Atlasiet cilni **Darbplūsma** .</span><span class="sxs-lookup"><span data-stu-id="bf8b5-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="bf8b5-129">Iestatiet opciju **Iespējot paziņojumus programmai Teams** uz **Jā** , lai lietotājam iespējotu paziņojumus, vai uz **Nē**, lai atspējotu paziņojumus lietotājam.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Iespējojiet Teams programmas paziņojumus cilnē Lietotāju opciju darbplūsma](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="bf8b5-131">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="bf8b5-132">Zināmās problēmas</span><span class="sxs-lookup"><span data-stu-id="bf8b5-132">Known issues</span></span>

| <span data-ttu-id="bf8b5-133">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="bf8b5-133">Issue</span></span> | <span data-ttu-id="bf8b5-134">Statuss</span><span class="sxs-lookup"><span data-stu-id="bf8b5-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="bf8b5-135">Horizontālā ritināšana nedarbojas Android tālruņos</span><span class="sxs-lookup"><span data-stu-id="bf8b5-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="bf8b5-136">Horizontālā ritināšana nav problēma iOS vai galddatora ierīcēs.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="bf8b5-137">Mēs strādājam pie risinājuma Android.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="bf8b5-138">Kļūda: radās problēma, meklējot vidi, ar kuru jāizveido savienojums.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="bf8b5-139">Šo kļūdu varat saņemt pat tad, ja esat pārliecinājies, ka lietotājs var piekļūt vienai vai vairākām Human Resources vidēm.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="bf8b5-140">Turklāt iespējams, ka neredzēsit visas paredzētās vides.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="bf8b5-141">Kamēr mēs novērsīsim šo problēmu, dzēsiet lietotāju un pēc tam importējiet to vēlreiz, lai atrisinātu problēmu.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="bf8b5-142">Bilance nav pareiza, iesniedzot prombūtni nākotnes datumam.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="bf8b5-143">Videoklips vēl nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="bf8b5-144">Parādās pašreizējā datuma bilance.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="bf8b5-145">Nevar atcelt **Pārskatā** pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="bf8b5-146">Šī funkcionalitāte pašlaik netiek atbalstīta, un tā tiks pievienota nākošajā laidienā.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="bf8b5-147">Bilances informācija tiek aprēķināta no šodienas.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="bf8b5-148">Sistēma pašlaik neparāda uzkrājumu perioda bilances, pat ja tās ir konfigurētas atvaļinājumu un prombūtnes parametros.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="bf8b5-149">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="bf8b5-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="bf8b5-150">Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)</span><span class="sxs-lookup"><span data-stu-id="bf8b5-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="bf8b5-151">Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="bf8b5-152">Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="bf8b5-153">Lasīt vairāk par LUIS [šeit](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="bf8b5-154">LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="bf8b5-155">Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="bf8b5-156">Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="bf8b5-157">LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bf8b5-158">Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="bf8b5-159">Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="bf8b5-160">Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="bf8b5-161">Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="bf8b5-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="bf8b5-162">Microsoft Azure Event Grid un Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bf8b5-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="bf8b5-163">Izmantojot paziņojumu līdzekli programmai Dynamics 365 Human Resources risinājumā Teams, noteikti klienta dati ieplūdīs ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="bf8b5-164">Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="bf8b5-165">Šos datus var uzglabāt līdz 24 stundām un apstrādāt Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="bf8b5-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf8b5-166">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bf8b5-166">See also</span></span> 

[<span data-ttu-id="bf8b5-167">Lejupielāde un instalēšana Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bf8b5-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="bf8b5-168">Microsoft Teams palīdzības centrs</span><span class="sxs-lookup"><span data-stu-id="bf8b5-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="bf8b5-169">Atvaļinājumu pieprasījumu pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="bf8b5-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

