---
title: Pievienošanas ceļvežu un veidņu rediģēšana programmā Dynamics 365 Talent - Onboard
description: Šajā tēmā ir paskaidrots, kā pievienot darbības un citu informāciju pievienošanas ceļvežiem un veidnēm programmā Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7803c7cd2c58b8544d2c8dd711c295d6882f9fca
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010802"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="491db-103">Pievienošanas ceļvežu un veidņu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="491db-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="491db-104">Kad esat izveidojis pievienošanas ceļvedi vai veidni programmā Microsoft Dynamics 365 Talent: Onboard, jums jāpievieno ievads, darbības, kontaktpersonas un resursi.</span><span class="sxs-lookup"><span data-stu-id="491db-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="491db-105">Onboard ļauj iekļaut bagātīgu saturu jūsu pārvietošanas ceļvežiem, tostarp:</span><span class="sxs-lookup"><span data-stu-id="491db-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="491db-106">YouTube videoklipus</span><span class="sxs-lookup"><span data-stu-id="491db-106">YouTube videos</span></span>
- <span data-ttu-id="491db-107">Microsoft Sway prezentācijas</span><span class="sxs-lookup"><span data-stu-id="491db-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="491db-108">Microsoft PowerApps programmas</span><span class="sxs-lookup"><span data-stu-id="491db-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="491db-109">Microsoft Stream videoklipus</span><span class="sxs-lookup"><span data-stu-id="491db-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="491db-110">Microsoft Forms veidlapas</span><span class="sxs-lookup"><span data-stu-id="491db-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="491db-111">Iframe, kurā iekļauts tīmekļa saturs</span><span class="sxs-lookup"><span data-stu-id="491db-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="491db-112">No veidnes importēto ievadu vai darbību rediģēšana</span><span class="sxs-lookup"><span data-stu-id="491db-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="491db-113">Ja izveidojat pievienošanas ceļvedi no veidnes vai importējat darbības no vienas veidnes uz citu, uz importētajām darbībām pamanīsit pogu **Slēdzene**.</span><span class="sxs-lookup"><span data-stu-id="491db-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="491db-114">Tās sauc par *pārvaldītām darbībām*.</span><span class="sxs-lookup"><span data-stu-id="491db-114">These are called *managed activities*.</span></span>

<span data-ttu-id="491db-115">[![Pārvaldītās darbības](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="491db-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="491db-116">Atlasot pārvaldīto darbību, darbības augšdaļā var redzēt avota veidni.</span><span class="sxs-lookup"><span data-stu-id="491db-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="491db-117">[![Pārvaldītās darbības avots](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="491db-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="491db-118">Ja rediģējat darbību veidnē, Onboard pārbīdīs izmaiņas uz visām veidnēm un nenosūtītiem ceļvežiem, kuru pamatā ir šī veidne.</span><span class="sxs-lookup"><span data-stu-id="491db-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="491db-119">Ja atlasīsit nenosūtītu ceļvedi, kura pamatā ir rediģētā veidne, un pēc tam ceļvedī atlasīsit cilni **Darbības**, tiks parādīts paziņojums, ka jūsu ceļvedis ir mainījies.</span><span class="sxs-lookup"><span data-stu-id="491db-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="491db-120">Lai noraidītu paziņojumu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="491db-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="491db-121">[![Paziņojuma maiņa](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="491db-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="491db-122">Blakus atjauninātajām darbībām redzēsit melnu punktu.</span><span class="sxs-lookup"><span data-stu-id="491db-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="491db-123">[![Mainīta darbība](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="491db-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="491db-124">Pārvaldītās darbības nevar rediģēt ārpus oriģinālās veidnes, izņemot to, ka darbības labās puses sadaļā ir jāpievieno piešķīrējs, izpildes datums vai cita informācija.</span><span class="sxs-lookup"><span data-stu-id="491db-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="491db-125">Ja vēlaties rediģēt pārvaldīto darbību vai nevēlaties, lai darbība saņem atjauninājumus no veidnes, no kuras tie nākuši, atlasiet šīs darbības pogu **Slēdzene**.</span><span class="sxs-lookup"><span data-stu-id="491db-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="491db-126">Poga **Slēdzene** izzudīs.</span><span class="sxs-lookup"><span data-stu-id="491db-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="491db-127">Šo darbību vairs nepārvaldīs oriģinālā veidne, un tā vairs nesaņems atjauninājumus no minētās veidnes.</span><span class="sxs-lookup"><span data-stu-id="491db-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="491db-128">Atjauninājumi, ko veicat darbībai, neietekmē oriģinālo veidni.</span><span class="sxs-lookup"><span data-stu-id="491db-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="491db-129">Ja izdzēšat darbību no ceļveža un izbīdāt izmaiņas no šā ceļveža veidnes, aktivitāte ceļvedī paliks izdzēsta.</span><span class="sxs-lookup"><span data-stu-id="491db-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="491db-130">Veidnes nepārvalda kontaktpersonas un resursus.</span><span class="sxs-lookup"><span data-stu-id="491db-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="491db-131">Turklāt sadaļas netiek pārvaldītas, tādēļ, ja pievienojat vai rediģējat sadaļu veidnē, izmaiņas netiks izstumtas uz visiem ceļvežiem vai veidnēm, kas izmanto šo veidni.</span><span class="sxs-lookup"><span data-stu-id="491db-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="491db-132">Ja veidnei pievienojat jaunas darbības, jaunās darbības tiek virzītas uz ceļvežiem un veidnēm, kuru pamatā ir šī veidne, un jaunās darbības tiek parādītas augšpusē.</span><span class="sxs-lookup"><span data-stu-id="491db-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="491db-133">Darbību importēšana no citas veidnes</span><span class="sxs-lookup"><span data-stu-id="491db-133">Import activities from another template</span></span>

<span data-ttu-id="491db-134">Ceļvedī vai veidnē varat importēt darbības no vienas vai vairākām veidnēm.</span><span class="sxs-lookup"><span data-stu-id="491db-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="491db-135">Atlasiet ceļvedi vai veidni, kuru vēlaties rediģēt.</span><span class="sxs-lookup"><span data-stu-id="491db-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="491db-136">Atlasiet cilni **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="491db-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="491db-137">Atlasiet cilni **Importēt** sadaļā pa labi.</span><span class="sxs-lookup"><span data-stu-id="491db-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="491db-138">[![Darbību importēšana](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="491db-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="491db-139">Lai priekšskatītu uzdevumus jaunā cilnē jūsu pārlūkā, jebkurā veidnē atlasiet pogu **Atvērt jaunā cilnē**.</span><span class="sxs-lookup"><span data-stu-id="491db-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="491db-140">[![Darbību importēšana](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="491db-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="491db-141">Velciet un nometiet vajadzīgo veidni tajā vietā jūsu ceļveža veidnē, kur vēlaties, lai darbības tiktu rādītas.</span><span class="sxs-lookup"><span data-stu-id="491db-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="491db-142">Turpiniet rediģēt savu ceļvedi vai veidni.</span><span class="sxs-lookup"><span data-stu-id="491db-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="491db-143">Importētās darbības saturēs pogu **Slēdzene**, kas norāda, ka šīs darbības pārvalda veidne, no kuras jūs importējāt.</span><span class="sxs-lookup"><span data-stu-id="491db-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="491db-144">Veicot izmaiņas importētajā veidnē, šīs darbības atjauninās veidnē, uz kuru tās importējāt.</span><span class="sxs-lookup"><span data-stu-id="491db-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="491db-145">Tomēr izmaiņas netiks automātiski izstumtas uz visiem ceļvežiem, kas izveidoti no veidnes, uz kuru importējāt.</span><span class="sxs-lookup"><span data-stu-id="491db-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="491db-146">Izmaiņu no veidnes uz citām veidnēm vai ceļvežiem izstumšana</span><span class="sxs-lookup"><span data-stu-id="491db-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="491db-147">Rediģējot veidni, kas satur darbības, kuras tiek izmantotas citās veidnēs vai ceļvežos, jums ir jāstumj izmaiņas, ja vēlaties, lai tās parādītos citās veidnēs vai ceļvežos.</span><span class="sxs-lookup"><span data-stu-id="491db-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="491db-148">Ja neesat pārliecināts, vai veidnes darbības tiek izmantotas citās veidnēs vai ceļvežos, atlasiet cilni **Izmantots**, lai skatītu, kur šīs aktivitātes ir redzamas.</span><span class="sxs-lookup"><span data-stu-id="491db-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="491db-149">[![Skatīt ceļvežus un veidnes, kuros darbības tiek izmantotas](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="491db-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="491db-150">Lai izstumtu jūsu izmaiņas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="491db-150">To push your changes:</span></span>

1. <span data-ttu-id="491db-151">Saglabājiet izmaiņas, atlasot pogu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="491db-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="491db-152">Ja to nedarīsit, jums tiks lūgts saglabāt izmaiņas nākamajā darbībā.</span><span class="sxs-lookup"><span data-stu-id="491db-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="491db-153">Atlasiet **Izstumt šīs izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="491db-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="491db-154">Ievada pievienošana vai rediģēšana</span><span class="sxs-lookup"><span data-stu-id="491db-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="491db-155">Cilnē **Ievads** ievadiet ceļveža nosaukumu un sākuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="491db-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="491db-156">Lai izmantotu parauga tekstu, atlasiet **Lietot šo ziņojumu**.</span><span class="sxs-lookup"><span data-stu-id="491db-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="491db-157">[![Ievada cilne Onboard veidnē](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="491db-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="491db-158">Izmantojiet formatēšanas pogas, lai izsauktu nepieciešamo tekstu vai pievienotu attēlus vai saites.</span><span class="sxs-lookup"><span data-stu-id="491db-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="491db-159">Atlasiet **Saglabāt**, lai saglabātu veikto darbu.</span><span class="sxs-lookup"><span data-stu-id="491db-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="491db-160">Darbību pievienošana vai rediģēšana</span><span class="sxs-lookup"><span data-stu-id="491db-160">Add or edit activities</span></span>

1. <span data-ttu-id="491db-161">Cilnē **Darbības** velciet vienumus no labās puses uz rediģēšanas apgabalu.</span><span class="sxs-lookup"><span data-stu-id="491db-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="491db-162">Lai organizētu ceļvedi sadaļās, velciet vienumu **Jauna sadaļa** uz rediģēšanas apgabalu un ievadiet sadaļas nosaukumu un neobligātu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="491db-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="491db-163">Jaunas sadaļas pievienošana pievienošanas ceļvedim vai veidnei</span><span class="sxs-lookup"><span data-stu-id="491db-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="491db-164">Lai pabeigtu darbību pievienošanu nesen nolīgtajam darbiniekam, velciet vienumu **Jauna darbība** uz rediģēšanas apgabalu un ievadiet darbības nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="491db-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="491db-165">Jaunas darbības pievienošana pievienošanas ceļvedim vai veidnei</span><span class="sxs-lookup"><span data-stu-id="491db-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="491db-166">Bagātināta satura pievienošana savam pievienošanas cveļvedim</span><span class="sxs-lookup"><span data-stu-id="491db-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="491db-167">Lai pievienotu YouTube videoklipu, velciet **YouTube** vienumu uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un ievadiet YouTube videoklipa vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="491db-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="491db-168">Lai pievienotu Sway prezentāciju vai biļetenu, velciet vienumu **Sway** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un ievadiet Sway prezentācijas vai biļetena iegulto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="491db-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="491db-169">Lai pievienotu programmu PowerApps, velciet vienumu **PowerApps** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un vai nu atlasiet programmu PowerApps vai arī ievadiet programmas PowerApps ID.</span><span class="sxs-lookup"><span data-stu-id="491db-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="491db-170">Lai pievienotu Microsoft Stream videoklipu, velciet **Microsoft Stream** vienumu uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un ievadiet Microsoft Stream videoklipa vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="491db-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="491db-171">Lai pievienotu Microsoft Forms veidlapu, velciet vienumu **Microsoft Forms** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu, ievadiet Microsoft Forms veidlapas vietrādi URL un norādiet ekrāna laukuma lielumu.</span><span class="sxs-lookup"><span data-stu-id="491db-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="491db-172">Lai pievienotu iframe, kas ietver tīmekļa saturu, velciet vienumu **Tīmekļa saturs (iframe)** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu, ievadiet tīmekļa satura vietrādi URL un norādiet ekrāna laukuma lielumu.</span><span class="sxs-lookup"><span data-stu-id="491db-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="491db-173">Bagātināta satura pievienošana pievienošanas ceļvedim vai veidnei</span><span class="sxs-lookup"><span data-stu-id="491db-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="491db-174">Neobligāti: katras darbības labās puses apgabalā piešķiriet darbību konkrētai personai vai lomai, pievienojiet izpildes datumu un kontaktpersonu, un piešķiriet kategorijas krāsu.</span><span class="sxs-lookup"><span data-stu-id="491db-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="491db-175">Piešķirot darbību personai vai lomai, katrai personai tiek izveidots uzdevums.</span><span class="sxs-lookup"><span data-stu-id="491db-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="491db-176">Šis uzdevums tiek parādīts Onboard izvēlnē **Uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="491db-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="491db-177">[![Darbības piešķiršana pievienošanas ceļvedī vai veidnē](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="491db-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="491db-178">Atlasiet **Saglabāt**, lai saglabātu veikto darbu.</span><span class="sxs-lookup"><span data-stu-id="491db-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="491db-179">Lai izdzēstu darbību vai sadaļu, atlasiet pogu **Dzēst** (atkritnes simbols) darbības vai sadaļas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="491db-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="491db-180">Lai pārkārtotu darbības un sadaļas, velciet tās uz jaunu atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="491db-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="491db-181">Kontaktpersonu pievienošana vai rediģēšana</span><span class="sxs-lookup"><span data-stu-id="491db-181">Add or edit contacts</span></span>

<span data-ttu-id="491db-182">Varat pievienot kontaktpersonas, kas var palīdzēt jūsu nesen nolīgtajam darbiniekam gūt panākumus no pirmās dienas.</span><span class="sxs-lookup"><span data-stu-id="491db-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="491db-183">Šīs kontaktpersonas var būt darba devēji, grupas biedri, nolīgšanas palīgi, padomdevēji, administratori un IT atbalsta personāls.</span><span class="sxs-lookup"><span data-stu-id="491db-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="491db-184">Cilnē **Kontaktpersonas** atlasiet **Jauna kontaktpersona**.</span><span class="sxs-lookup"><span data-stu-id="491db-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="491db-185">Dialoglodziņā **Pievienot grupas dalībnieku** ievadiet kontaktpersonas vārdu vai e-pasta adresi, ievadiet īsu aprakstu, kurā paskaidrots, kā kontaktpersona var palīdzēt nesen nolīgtajam darbiniekam un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="491db-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="491db-186">Kontaktpersonu pievienošana pievienošanas ceļvedim vai veidnei</span><span class="sxs-lookup"><span data-stu-id="491db-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="491db-187">Vai arī varat atlasīt vienu vai vairākas kontaktpersonas sadaļā **Ieteikumi.**</span><span class="sxs-lookup"><span data-stu-id="491db-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="491db-188">Atlasiet **Saglabāt**, lai saglabātu veikto darbu.</span><span class="sxs-lookup"><span data-stu-id="491db-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="491db-189">Lai izdzēstu kontaktpersonu, atlasiet pogu **Dzēst** (atkritnes simbols) pa labi no kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="491db-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="491db-190">Lai rediģētu kontaktpersonu, atlasiet pogu **Rediģēt** (zīmuļa simbols) pa labi no kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="491db-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="491db-191">Resursu pievienošana vai rediģēana</span><span class="sxs-lookup"><span data-stu-id="491db-191">Add or edit resources</span></span>

<span data-ttu-id="491db-192">Varat pievienot noderīgus failus, kartes un saites jūsu pievienošanas ceļveža sadaļai **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="491db-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="491db-193">Cilnē **Resursi** atlasiet **Jauns resurss**.</span><span class="sxs-lookup"><span data-stu-id="491db-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="491db-194">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="491db-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="491db-195">Lai pievienotu failu, atlasiet cilni **Fails** un velciet failu uz norādīto apgabalu.</span><span class="sxs-lookup"><span data-stu-id="491db-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="491db-196">(Vai arī noklikšķiniet jebkurā vietā šajā apgabalā, lai pārlūkotu failu savā datorā, vai atlasiet **Pārlūkot OneDrive**.) Ievadiet faila nosaukumu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="491db-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="491db-197">Lai pievienotu saiti, atlasiet cilni **Saite**, ievadiet saites nosaukumu un adresi un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="491db-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="491db-198">Lai pievienotu karti, atlasiet cilni **Karte**, ievadiet kartes nosaukumu un adresi un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="491db-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="491db-199">Onboard ietvers jūsu norādītās adreses karti.</span><span class="sxs-lookup"><span data-stu-id="491db-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="491db-200">Resursa pievienošana pievienošanas ceļvedim vai veidnei</span><span class="sxs-lookup"><span data-stu-id="491db-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="491db-201">Atlasiet **Saglabāt**, lai saglabātu veikto darbu.</span><span class="sxs-lookup"><span data-stu-id="491db-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="491db-202">Lai izdzēstu resursu, atlasiet pogu **Dzēst** (atkritnes simbols) pa labi no resursa.</span><span class="sxs-lookup"><span data-stu-id="491db-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="491db-203">Lai rediģētu kontaktpersonu, atlasiet pogu **Rediģēt** (zīmuļa simbols) pa labi no resursa.</span><span class="sxs-lookup"><span data-stu-id="491db-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="491db-204">Nākamās darbības</span><span class="sxs-lookup"><span data-stu-id="491db-204">Next steps</span></span>

- [<span data-ttu-id="491db-205">Satura kopīgošana ar citiem ieguldītājiem</span><span class="sxs-lookup"><span data-stu-id="491db-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="491db-206">Uzdevumu un pievienoto darbinieku statusa skatīšana</span><span class="sxs-lookup"><span data-stu-id="491db-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="491db-207">Par pieņemšanu darbā atbildīgo grupu izveide Onboard</span><span class="sxs-lookup"><span data-stu-id="491db-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="491db-208">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="491db-208">See also</span></span>

- [<span data-ttu-id="491db-209">Programmas Onboard izmēģināšana vai iegāde</span><span class="sxs-lookup"><span data-stu-id="491db-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="491db-210">Jaunumi</span><span class="sxs-lookup"><span data-stu-id="491db-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="491db-211">Piezīmes par laidienu</span><span class="sxs-lookup"><span data-stu-id="491db-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="491db-212">Atbalsta saņemšana</span><span class="sxs-lookup"><span data-stu-id="491db-212">Get support</span></span>](./talent-support.md)
