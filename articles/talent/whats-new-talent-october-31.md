---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 31. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "858794"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="bbc6c-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 31. oktobris)</span><span class="sxs-lookup"><span data-stu-id="bbc6c-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bbc6c-104">**Būvējums 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="bbc6c-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="bbc6c-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="bbc6c-106">Saišu izveidošana no Talent uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bbc6c-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="bbc6c-107">Šī jaunā navigācijas funkcionalitāte ļauj jums izveidot saiti no Talent uz Finance and Operations, nodrošinot tiešu navigāciju Finance and Operations lapās.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="bbc6c-108">Kad saites ir konfigurētas, varat norādīt saites nosaukumu un grupu, norādīt vietu, kur saitei būtu jābūt redzamai programmā Talent, ka arī mērķa lapu, ko atvērt programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="bbc6c-109">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="bbc6c-109">Coming soon</span></span>
<span data-ttu-id="bbc6c-110">Nākotnē tiks pievienots lauka konteksts, lai ļautu tieši pāriet uz atbilstošajiem ierakstiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="bbc6c-111">Piemēram, varat izmantot vienumu **Saite uz lauku**, lai sniegtu kontekstu pāriešanai tieši uz noteiktu darbinieku vai amatu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="bbc6c-112">Mērķa sistēmu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bbc6c-112">Configure target systems</span></span>

<span data-ttu-id="bbc6c-113">Programmā Talent sistēmas administratori var definēt saites, kas tiks rādītas dažādās sistēmas administrēšanas darbvietas vietās.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="bbc6c-114">Daļa no konfigurācijas ir Finance and Operations vides, uz kurām jūs vēlētos pāriet, un tās ir jānorāda kā šādu saišu “mērķis”.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="bbc6c-115">To var izdarīt, piešķirot mērķa sistēmai nosaukumu un norādot Finance and Operations vides vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="bbc6c-116">Lūk, piemērs Finance and Operations vietrādim URL, ko jūs norādītu: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="bbc6c-117">Kad esat konfigurējis mērķa sistēmu, varat definēt savas saites.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="bbc6c-118">Saišu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bbc6c-118">Configure links</span></span>

<span data-ttu-id="bbc6c-119">Katrai izveidotajai saitei ir definēta tālāk norādītā informācija.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="bbc6c-120">Saite —-saites nosaukums, izmantots vienīgi identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="bbc6c-121">Iespējot šo saiti — iestatiet uz **Jā**, ja vēlaties šo saiti rādīt programmas Talent lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="bbc6c-122">Parādāmais nosaukums — definējiet nosaukumu, kas būs redzams kā saite uz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="bbc6c-123">Šie dati pašlaik nav tulkoti.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="bbc6c-124">Rādīt saiti formā — izvēlēties, kurā lapā vēlaties rādīt šo saiti.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="bbc6c-125">Grupa — grupas nav obligātas, taču, ja vēlaties kārtot savas saites, izmantojot grupas, atlasiet esošu grupu vai izveidojiet jaunu, izmantojot lauku **Grupas**.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="bbc6c-126">Mērķa sistēma — atlasiet mērķa sistēmu, kas tika izveidota, izmantojot opciju **Konfigurēt mērķa sistēmu**.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="bbc6c-127">Šī būs Finance and Operations vide, kas tiks izmantota, kad šo saiti lietosiet navigēšanai.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="bbc6c-128">Lietotāja pašreizējais uzņēmums — atlasiet **Jā**, ja vēlaties izmantot lietotāja pašreizējā uzņēmuma kontekstu, kad notiek navigēšana uz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="bbc6c-129">Ja ir atlasīta vērtība **Nē**, varat atlasīt izmantojamo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="bbc6c-130">Mērķa izvēlnes vienums — ievadiet izvēlnes vienumu no Finance and Operations, kas saitei būtu jāizmanto navigēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="bbc6c-131">Ir pieejami izvēlnes vienumi, uz kuriem varat pāriet tieši.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="bbc6c-132">Lai atrastu nepieciešamo izvēlnes vienumu, atveriet programmu Finance and Operations un atveriet lapu, kas ir navigācijas mērķis.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="bbc6c-133">Kopējiet izvēlnes vienumu no vietrāža URL.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="bbc6c-134">Piemēram, ja vēlaties, lai saite jūs pārceltu uz darbinieku sarakstu programmā Finance and Operations, ievadiet vērtību, kas vietrādī URL ir redzama aiz “&mi”.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="bbc6c-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="bbc6c-136">Izvēlnes vienums pāriešanai uz darbinieku saraksta lapu šajā piemērā ir: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="bbc6c-137">Saite uz datu avotu — atlasiet datu avotu, uz kuru šī saite atsaucas.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="bbc6c-138">Ir pieejami visbiežāk izmantotie avoti, piemēram, **Nodarbinātais** un **Amats**.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="bbc6c-139">Saite uz lauku — (drīzumā) šī lauka atlasīšana ļaus tieši pāriet no atsevišķa ieraksta programmā Talent uz atsevišķu ierakstu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="bbc6c-140">Piekļuve saitēm</span><span class="sxs-lookup"><span data-stu-id="bbc6c-140">Access to links</span></span>

<span data-ttu-id="bbc6c-141">Sistēmas administratori redzēs jaunizveidotās saites uz definētām lapām pat tad, ja opcija **Iespējot šo saiti** būs ir iestatīta uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="bbc6c-142">Šo funkcionalitāti var izmantot saišu testēšanai pirms to rādīšanas citiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="bbc6c-143">Visas pārējās lomas konfigurētās saites varēs redzēt tikai pēc tam, kad opcija **Iespējot šo saiti** būs iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="bbc6c-144">Darbinieki, kam ir piekļuve lapām, kurās saites tiek rādītas, varēs piekļūt šīm saitēm.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="bbc6c-145">Lietotājiem var būt arī programmā Finance and Operations definētas drošības tiesības piekļūt lapām programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="bbc6c-146">Ja viņiem tādu nav, saites lietošanas laikā tiek parādīts drošības dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="bbc6c-147">Citas izmaiņas/labojumi</span><span class="sxs-lookup"><span data-stu-id="bbc6c-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="bbc6c-148">Amatus ar sākuma datumu nākotnē nevar piešķirt jaunam darbiniekam</span><span class="sxs-lookup"><span data-stu-id="bbc6c-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="bbc6c-149">Ir veiktas izmaiņas, lai ļautu darbiniekus piešķirt amatiem ar datumiem nākotnē.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="bbc6c-150">Var atlasīt amatus, kuru sākuma datumi ir nākotnē, un darbinieka piešķire tiek veikta, izpildot darbplūsmas saglabāšanu vai pabeigšanu (ja šī darbplūsma ir iespējota).</span><span class="sxs-lookup"><span data-stu-id="bbc6c-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="bbc6c-151">Jaunu darbinieku nevar piešķirt esošam amatam</span><span class="sxs-lookup"><span data-stu-id="bbc6c-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="bbc6c-152">Ir veiktas izmaiņas, tāpēc jauna darbinieka piešķiri tagad var piešķirt esošiem amatiem.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="bbc6c-153">Darba stāža datums/biroja vieta pazūd, kad nodarbinātības sākuma datums ir pagātnē un ieraksts tiek saglabāts</span><span class="sxs-lookup"><span data-stu-id="bbc6c-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="bbc6c-154">Ir veiktas izmaiņas, lai labotu vienumu **Darba stāža datums** un **Biroja vieta** redzamību, kad tiek saglabātas izmaiņas iepriekšējiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="bbc6c-155">Nodarbinātā lapā nevar ievadīt datus par nodarbinātību ar datumu nākotnē</span><span class="sxs-lookup"><span data-stu-id="bbc6c-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="bbc6c-156">Galvenajā nodarbināto lapā ir atspējoti nodarbinātības dati nodarbinātībai ar datumu nākotnē.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="bbc6c-157">Nodarbinātības datus var ievadīt, izmantojot lapas **Datumu pārvaldnieks**.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="bbc6c-158">Turpmākajos laidienos tiks ieviestas papildu izmaiņas, lai iespējotu nodarbinātības datu ievadīšanu tieši darbplūsmas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="bbc6c-159">Vērtības ValidFrom un ValidTo pievienošana elementam HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="bbc6c-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="bbc6c-160">Elements Datu pārvaldības struktūra (Data Management Framework — DMF) HcmPersonalContactPersonEntity ir atjaunināts, ietverot tajā datumus “derīgs no” un “derīgs līdz”, lai iespējotu noteiktus atvieglojumu ieviešanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="bbc6c-161">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="bbc6c-161">Known issue</span></span>
- <span data-ttu-id="bbc6c-162">**Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="bbc6c-163">**Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="bbc6c-164">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="bbc6c-165">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="bbc6c-165">(This issue will be fixed in the next platform update.)</span></span>
