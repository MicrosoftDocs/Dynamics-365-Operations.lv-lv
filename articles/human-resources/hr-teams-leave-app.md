---
title: Atvaļinājuma pieprasījumu pārvaldība programmā Teams
description: Šajā tēmā parādīts, kā pieprasīt prombūtni Dynamics 365 Human Resources programmā Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766764"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="a3f45-103">Atvaļinājuma pieprasījumu pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="a3f45-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a3f45-104">Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj ātri pieprasīt prombūtni un skatīt savas prombūtnes bilances informāciju Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a3f45-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="a3f45-105">Varat sazināties ar botu, lai pieprasītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="a3f45-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="a3f45-106">Cilne **Laiks izslēgts** sniedz detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="a3f45-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="a3f45-107">Programmas instalēšana</span><span class="sxs-lookup"><span data-stu-id="a3f45-107">Install the app</span></span>

<span data-ttu-id="a3f45-108">Personāla vadības programmu varat atrast Teams veikalā.</span><span class="sxs-lookup"><span data-stu-id="a3f45-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="a3f45-109">Sadaļā Microsoft Teams atlasiet daudzpunkti.</span><span class="sxs-lookup"><span data-stu-id="a3f45-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams atstāj programmas daudzpunkti](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="a3f45-111">Meklējiet Dynamics 365 Human Resources un pēc tam atlasiet elementu **Personāla vadība**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams atstāj programmas elementu personāla vadība](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="a3f45-113">Atlasiet pogu **Pievienot**, lai instalētu programmu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams atstāj programmas instalēšanu](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="a3f45-115">Ja programma jūs automātiski nepieraksta, atlasiet cilni **Iestatījumi**, lai pierakstītos.</span><span class="sxs-lookup"><span data-stu-id="a3f45-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams atstāj programmas cilni Iestatījumi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="a3f45-117">Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus.</span><span class="sxs-lookup"><span data-stu-id="a3f45-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="a3f45-118">Ja jums ir piekļuve vairāk nekā vienai Human Resources instancei, varat atlasīt, ar kuru vidi vēlaties veidot savienojumu, cilnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="a3f45-119">Programma pašlaik neatbalsta sistēmas administratora drošības lomu un tiks parādīts kļūdas ziņojumu, ja pierakstīsities ar sistēmas administratora kontu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="a3f45-120">Lai pierakstītos ar citu kontu, cilnē **Iestatījumi** atlasiet pogu **Kontu pārslēgšana** un pēc tam pierakstieties ar lietotāja kontu, kam nav sistēmas administratora privilēģiju.</span><span class="sxs-lookup"><span data-stu-id="a3f45-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="a3f45-121">Bota izmantošana</span><span class="sxs-lookup"><span data-stu-id="a3f45-121">Use the bot</span></span>

<span data-ttu-id="a3f45-122">Pēc programmas instalēšanas, tiek parādīts sveiciena ziņojums, informējot jūs par darbību veidiem, ko bots var veikt jūsu vārdā.</span><span class="sxs-lookup"><span data-stu-id="a3f45-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams atstāj programmas bota sveiciena ziņojumu](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="a3f45-124">Pirmo reizi izmantojot botu, var būt nepieciešams pierakstīties.</span><span class="sxs-lookup"><span data-stu-id="a3f45-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="a3f45-125">Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus.</span><span class="sxs-lookup"><span data-stu-id="a3f45-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="a3f45-126">Varat lūgt botam:</span><span class="sxs-lookup"><span data-stu-id="a3f45-126">You can ask the bot to:</span></span>

- <span data-ttu-id="a3f45-127">Rādīt prombūtnes bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts.</span><span class="sxs-lookup"><span data-stu-id="a3f45-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams atstāj programmas bilances rādīšanu](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="a3f45-129">Rādīt papildu informāciju par konkrētu atvaļinājuma veidu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams atstāj programmas informācijas rādīšanu](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="a3f45-131">Izveidot atvaļinājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-131">Start a leave request for you.</span></span>

   ![Human Resources Teams atstāj programmas atvaļinājuma pieprasījumu](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="a3f45-133">Pēc atvaļinājuma pieprasījuma sākšanas varat pielāgot dienas pa tieši kartē.</span><span class="sxs-lookup"><span data-stu-id="a3f45-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teams atstāj programmas rediģēšanas pieprasījumu](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="a3f45-135">Kad esat pabeidzis ievadīt informāciju, atlasiet **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="a3f45-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="a3f45-136">Varat arī atlasīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="a3f45-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teams atstāj programmas pieprasījuma iesniegšanu](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="a3f45-138">Atvaļinājuma pārvaldība programmā Teams</span><span class="sxs-lookup"><span data-stu-id="a3f45-138">Manage your leave in Teams</span></span>

<span data-ttu-id="a3f45-139">Cilne **Prombūtne** ļauj skatīt:</span><span class="sxs-lookup"><span data-stu-id="a3f45-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="a3f45-140">Bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts</span><span class="sxs-lookup"><span data-stu-id="a3f45-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="a3f45-141">Gaidāmos atvaļinājuma pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="a3f45-141">Upcoming leave requests</span></span>

- <span data-ttu-id="a3f45-142">Prombūtnes pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="a3f45-142">Time-off requests</span></span>

- <span data-ttu-id="a3f45-143">Melnraksta atvaļinājuma pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="a3f45-143">Draft leave requests</span></span>

![Personāla vadība Teams atstāj programmas cilni Laiks izslēgts](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="a3f45-145">Jauna pieprasījuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="a3f45-145">Create a new request</span></span>

1. <span data-ttu-id="a3f45-146">Lai izveidotu jaunu atvaļinājuma pieprasījumu, atlasiet **Jauns pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams atstāj programmas Jauns pieprasījums](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="a3f45-148">Ievadiet dienu vai dienas, kurās vēlaties ņemt pārtraukumu, un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams atstāj programmas pievienot prombūtni](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="a3f45-150">Ja piemērojams, ievadiet iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="a3f45-151">Ievadiet arī komentārus un pievienojiet pielikumus.</span><span class="sxs-lookup"><span data-stu-id="a3f45-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="a3f45-152">Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="a3f45-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a3f45-153">Varat arī ierakstīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="a3f45-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="a3f45-154">Melnraksta pieprasījumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="a3f45-154">Manage draft requests</span></span>

1. <span data-ttu-id="a3f45-155">Atlasiet cilni **Melnraksti**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams atstāj programmas cilni Melnraksti](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="a3f45-157">Atlasiet zīmuli, lai rediģētu pieprasījumu, vai atlasiet atkritni, lai dzēstu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="a3f45-158">Veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="a3f45-158">Make any necessary changes.</span></span> <span data-ttu-id="a3f45-159">Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="a3f45-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a3f45-160">Varat arī atlasīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="a3f45-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams atstāj programmas rediģēšanas melnraksts](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="a3f45-162">Teams paziņojumi</span><span class="sxs-lookup"><span data-stu-id="a3f45-162">Teams notifications</span></span>

<span data-ttu-id="a3f45-163">Kad jūs vai darbinieks, kuram jūs esat apstiprinātājs, iesniedz atvaļinājuma pieprasījumu, jums tiek nosūtīts paziņojums Teams risinājuma Human Resources programmā.</span><span class="sxs-lookup"><span data-stu-id="a3f45-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="a3f45-164">Varat atlasīt paziņojumu, lai to skatītu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-164">You can select the notification to view it.</span></span> <span data-ttu-id="a3f45-165">Paziņojumi tiek rādīti arī **Tērzēšanas** zonā.</span><span class="sxs-lookup"><span data-stu-id="a3f45-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="a3f45-166">Ja esat apstiprinātājs, varat izvēlēties **Apstiprināt** vai **Atteikt** paziņojumā.</span><span class="sxs-lookup"><span data-stu-id="a3f45-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="a3f45-167">Var arī norādīt neobligātu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="a3f45-167">You can also provide an optional message.</span></span>

![Atvaļinājuma pieprasījuma paziņojums Human Resources Teams programmā](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="a3f45-169">Skatiet savas grupas atvaļinājuma kalendāru</span><span class="sxs-lookup"><span data-stu-id="a3f45-169">View your team's leave calendar</span></span>

<span data-ttu-id="a3f45-170">Ja esat vādītājs ar tiešajiem pārskatiem, varat apskatīt savas grupas apstiprināto un gaidošo brīvo laiku.</span><span class="sxs-lookup"><span data-stu-id="a3f45-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="a3f45-171">Programmā Human Resources risinājumā Teams atlasiet **Brīvais laiks**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="a3f45-172">Atlasiet **Grupas kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="a3f45-172">Select **Team calendar**.</span></span>

   ![Skatīt kalendāru programmā Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="a3f45-174">Kalendārā tiek rādīti jūsu tiešo pārskatu apstiprinātais un gaidošais brīvais laiks.</span><span class="sxs-lookup"><span data-stu-id="a3f45-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Brīvā laika kalendārs programmā Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="a3f45-176">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="a3f45-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a3f45-177">Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)</span><span class="sxs-lookup"><span data-stu-id="a3f45-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a3f45-178">Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku.</span><span class="sxs-lookup"><span data-stu-id="a3f45-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a3f45-179">Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS).</span><span class="sxs-lookup"><span data-stu-id="a3f45-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a3f45-180">Lasīt vairāk par LUIS [šeit](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="a3f45-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a3f45-181">LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso).</span><span class="sxs-lookup"><span data-stu-id="a3f45-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a3f45-182">Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="a3f45-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a3f45-183">Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="a3f45-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a3f45-184">LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a3f45-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a3f45-185">Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru.</span><span class="sxs-lookup"><span data-stu-id="a3f45-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a3f45-186">Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā.</span><span class="sxs-lookup"><span data-stu-id="a3f45-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a3f45-187">Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="a3f45-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a3f45-188">Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a3f45-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="a3f45-189">Microsoft Azure Event Grid un Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a3f45-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="a3f45-190">Izmantojot paziņojumu līdzekli programmai Dynamics 365 Human Resources risinājumā Teams, noteikti klienta dati ieplūdīs ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="a3f45-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="a3f45-191">Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a3f45-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a3f45-192">Šos datus var uzglabāt līdz 24 stundām un apstrādāt Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="a3f45-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3f45-193">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="a3f45-193">See also</span></span>

[<span data-ttu-id="a3f45-194">Lejupielāde un instalēšana Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a3f45-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a3f45-195">Microsoft Teams palīdzības centrs</span><span class="sxs-lookup"><span data-stu-id="a3f45-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a3f45-196">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="a3f45-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
