---
title: Konfigurēt Human Resources parametrus
description: Šajā rakstā ir paskaidrots, kā iestatīt uzņēmumam raksturīgus parametrus programmā Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10f3c62925f6b951f88b990cb8b103dde54c27d1
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2021
ms.locfileid: "5502944"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="7723e-103">Konfigurēt Human Resources parametrus</span><span class="sxs-lookup"><span data-stu-id="7723e-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7723e-104">Dažu cilvēkresursu parametru iestatījumi tiek koplietoti uzņēmumu starpā, savukārt citu parametru iestatījumi ir raksturīgi noteiktam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="7723e-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="7723e-105">Šajā rakstā ir paskaidrots, kā iestatīt uzņēmumam raksturīgus cilvēkresursu parametrus.</span><span class="sxs-lookup"><span data-stu-id="7723e-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="7723e-106">Divas lapas tiek izmantotas, lai iestatītu cilvēkresursu parametrus.</span><span class="sxs-lookup"><span data-stu-id="7723e-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="7723e-107">Parametriem, kas ir kopīgi visiem uzņēmumiem, izmanto lapu **Personāla vadības kopīgie parametri**.</span><span class="sxs-lookup"><span data-stu-id="7723e-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="7723e-108">Parametriem, kas ir specifiski uzņēmumam (citiem vārdiem sakot, iestatījumi attiecas uz vienu uzņēmumu), izmanto lapu **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="7723e-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Dodieties uz Cilvēkresursu parametri](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="7723e-110">Lapā **Personāla vadības parametri** iestatījumi ir sadalīti sešās cilnēs:</span><span class="sxs-lookup"><span data-stu-id="7723e-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="7723e-111">**Vispārējā daļa**</span><span class="sxs-lookup"><span data-stu-id="7723e-111">**General**</span></span>
- <span data-ttu-id="7723e-112">**Personāla atlase** (šī cilne nav iekļauta programmā Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="7723e-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="7723e-113">**Kompensācija**</span><span class="sxs-lookup"><span data-stu-id="7723e-113">**Compensation**</span></span>
- <span data-ttu-id="7723e-114">**Numuru sērijas**</span><span class="sxs-lookup"><span data-stu-id="7723e-114">**Number sequences**</span></span>
- <span data-ttu-id="7723e-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="7723e-115">**FMLA**</span></span>
- <span data-ttu-id="7723e-116">**Darbinieku patstāvīgi izmantojamais pakalpojums**</span><span class="sxs-lookup"><span data-stu-id="7723e-116">**Employee self service**</span></span>
- <span data-ttu-id="7723e-117">**Vadītāja pašapkalpošanās**</span><span class="sxs-lookup"><span data-stu-id="7723e-117">**Manager self service**</span></span>
- <span data-ttu-id="7723e-118">**Atvieglojumu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="7723e-118">**Benefits management**</span></span>
- <span data-ttu-id="7723e-119">**Atvaļinājumi un kavējumi**</span><span class="sxs-lookup"><span data-stu-id="7723e-119">**Leave and absence**</span></span>
- <span data-ttu-id="7723e-120">**Maksājuma metodes**</span><span class="sxs-lookup"><span data-stu-id="7723e-120">**Payment methods**</span></span>

<span data-ttu-id="7723e-121">Katra cilne ietver informāciju, kas attiecas uz vienu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="7723e-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="7723e-122">Vispārējā daļa</span><span class="sxs-lookup"><span data-stu-id="7723e-122">General</span></span>

<span data-ttu-id="7723e-123">Iestatījumi lapā **Vispārīgi** nosaka informācijas parādīšanos par kavējumu, traumu un slimību un jaunām pieņemšanām darbā.</span><span class="sxs-lookup"><span data-stu-id="7723e-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="7723e-124">Šīs cilnes iestatījumi definē arī dažus noklusējuma ierakstus, kas parādās darba laikā.</span><span class="sxs-lookup"><span data-stu-id="7723e-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="7723e-125">It īpaši šī cilne ļauj:</span><span class="sxs-lookup"><span data-stu-id="7723e-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="7723e-126">Atlasiet krāsu, kuru piemērot atvērtajām kavējumu transakcijām</span><span class="sxs-lookup"><span data-stu-id="7723e-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="7723e-127">Norādīt stilu lapu, kas jāizmanto pārskatiem</span><span class="sxs-lookup"><span data-stu-id="7723e-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="7723e-128">Iespējot integrāciju starp apmācību kursiem un prombūtnes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="7723e-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="7723e-129">Atlasiet kavējuma kodu, kas tiek izmantots šīs integrācijas kontrolei.</span><span class="sxs-lookup"><span data-stu-id="7723e-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="7723e-130">Norādiet, cik ilgi uzturēt traumas vai slimības gadījumu incidentus.</span><span class="sxs-lookup"><span data-stu-id="7723e-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="7723e-131">Norādiet noklusēto identifikācijas numuru, kas tiek rādīts, pieņemot darbā jaunu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="7723e-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Cilne Vispārīgi](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="7723e-133">Personāla atlase</span><span class="sxs-lookup"><span data-stu-id="7723e-133">Recruitment</span></span>

<span data-ttu-id="7723e-134">Iestatījumi cilnē **Personāla atlase** definē dokumentu tipus, kas tiek izmantoti sarakstei, kas tiek automātiski nosūtīta kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="7723e-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="7723e-135">Varat arī norādīt personāla atlases projektu, ko izmanto neapstiprināto pieteikumu saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="7723e-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="7723e-136">Periods, kas tiek noteiks personāla atlases projekta vecumstruktūrai, nosaka personāla atlases projektus, kas iekļauti elementā **Vecumstruktūras projekti** darbvietā **Personāla atlases pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="7723e-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="7723e-137">Periods, kas noteikts brīdinājumam par pieteikuma iesniegšanas termiņu, tiek izmantots, lai parādītu personāla atlases projektus, kuriem tuvojas pieteikumu iesniegšanas termiņš elementā **Tuvojas pieteikuma iesniegšanas beigu termiņš** darbvirsmā **Personāla atlase**.</span><span class="sxs-lookup"><span data-stu-id="7723e-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="7723e-138">Papildinformāciju par pieņemšanu darbā skatiet [Personāla atlases kandidāti](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="7723e-139">Kompensācija</span><span class="sxs-lookup"><span data-stu-id="7723e-139">Compensation</span></span>

<span data-ttu-id="7723e-140">Iestatījumi cilnē **Atlīdzība** definē, vai lietotājiem ir jāapstiprina, ka viņi vēlas saglabāt informāciju fiksēto vai mainīgo atlīdzību plānam programmā Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7723e-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="7723e-141">Ja atzīmējat izvēles rūtiņu **Iespējot saglabāšanas pārbaudi**, ikreiz, kad lietotāji aizver ar atlīdzību saistītu lapu, viņi saņem ziņojumu ar jautājumu, vai viņi vēlas saglabāt ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7723e-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="7723e-142">Dažas Atlīdzības pārvaldības lapas neļauj lietotājiem dzēst informāciju.</span><span class="sxs-lookup"><span data-stu-id="7723e-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="7723e-143">Tāpēc prasot lietotājiem apstiprināt, ka viņi vēlas saglabāt informāciju, var ierobežot informācijas daudzumu, kas tiek saglabāts un ko nevar izdzēst vēlāk.</span><span class="sxs-lookup"><span data-stu-id="7723e-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="7723e-144">Ja izvēles rūtiņa **Iespējot saglabāšanas pārbaudi** ir notīrīta, ieraksti tiek vienmēr saglabāti nekavējoties, iespējams pirms lietotājs ir gatavs.</span><span class="sxs-lookup"><span data-stu-id="7723e-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="7723e-145">Ja jūs izmantojat veiktspējas pārvaldību, cilne **Atlīdzība** ļauj jums izvēlēties vērtēšanas modeli, ko veiktspējas vērtēšanas laikā lietot modeļa, kas piešķirts atlīdzības plāniem, vietā.</span><span class="sxs-lookup"><span data-stu-id="7723e-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="7723e-146">Cilvēkresursu sadaļā varat lietot cilni **Atlīdzība**, lai izvēlētos ierobežot piekļuvi atlīdzības plāniem un iestatīt noklusējuma valūtu.</span><span class="sxs-lookup"><span data-stu-id="7723e-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="7723e-147">Papildinformāciju par atlīdzību skatiet [Atlīdzības plānu pārskats](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Kompensāciju cilne](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="7723e-149">Numuru sērijas</span><span class="sxs-lookup"><span data-stu-id="7723e-149">Number sequences</span></span>

<span data-ttu-id="7723e-150">Iestatījumi cilnē **Numuru sērija** nosaka secības, ko izmanto, lai personāla vadības krājumiem automātiski piešķirtu ID, piemēram:</span><span class="sxs-lookup"><span data-stu-id="7723e-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="7723e-151">Programmas</span><span class="sxs-lookup"><span data-stu-id="7723e-151">Applications</span></span>
- <span data-ttu-id="7723e-152">Kavējumu reģistrācija</span><span class="sxs-lookup"><span data-stu-id="7723e-152">Absence registrations</span></span>
- <span data-ttu-id="7723e-153">Atlīdzības procesa rezultāti</span><span class="sxs-lookup"><span data-stu-id="7723e-153">Compensation process results</span></span>
- <span data-ttu-id="7723e-154">Lietu numuri</span><span class="sxs-lookup"><span data-stu-id="7723e-154">Case numbers</span></span>
- <span data-ttu-id="7723e-155">Kursi</span><span class="sxs-lookup"><span data-stu-id="7723e-155">Courses</span></span>
- <span data-ttu-id="7723e-156">Kursu darba kārtība</span><span class="sxs-lookup"><span data-stu-id="7723e-156">Course agendas</span></span>

<span data-ttu-id="7723e-157">Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas** (atlasiet uz **Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**).</span><span class="sxs-lookup"><span data-stu-id="7723e-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="7723e-158">Plašāku informāciju par numuru secību skatiet [Numuru sērijas pārskats](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7723e-158">For more information, see [Number sequences overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="7723e-159">Nostrādāto stundu skaits nedrīkst pārsniegt 1250 un nodarbinātības garums nedrīkst pārsniegt 12 mēnešus.</span><span class="sxs-lookup"><span data-stu-id="7723e-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="7723e-160">Šīs maksimālās vērtības ir saskaņā ar federālo likumu Amerikas Savienotajās Valstīs.</span><span class="sxs-lookup"><span data-stu-id="7723e-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Cilne Numuru sērijas](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="7723e-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="7723e-162">FMLA</span></span>

<span data-ttu-id="7723e-163">Cilnē FMLA iestatiet FMLA piemērotības prasības un FMLA pilnvaru stundas.</span><span class="sxs-lookup"><span data-stu-id="7723e-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="7723e-164">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes parametru konfigurēšana](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![Cilne FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="7723e-166">Darbinieku patstāvīgi izmantojamais pakalpojums</span><span class="sxs-lookup"><span data-stu-id="7723e-166">Employee self service</span></span>

<span data-ttu-id="7723e-167">Iestatījumi cilnē **Darbinieku pašapkalpošanās** ietekmē to, kā darbiniekiem parādās darbinieku pašapkalpošanās.</span><span class="sxs-lookup"><span data-stu-id="7723e-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="7723e-168">Šajā cilnē var:</span><span class="sxs-lookup"><span data-stu-id="7723e-168">On this tab, you can:</span></span>

- <span data-ttu-id="7723e-169">Darbinieka patstāvīgi izmantojamas darbvietas nosaukuma ievade</span><span class="sxs-lookup"><span data-stu-id="7723e-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="7723e-170">Atlasīt, kuru informāciju vadītājs var ievadīt darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="7723e-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="7723e-171">Pievienot darbiniekiem noderīgas saites</span><span class="sxs-lookup"><span data-stu-id="7723e-171">Add useful links for employees</span></span>
- <span data-ttu-id="7723e-172">Ierobežot darbinieku kontaktinformācijas pievienošanu vai rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="7723e-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="7723e-173">Papildinformāciju skatiet sadaļā [Personas informācijas rediģēšanas](hr-employee-self-service-restrict-editing.md)ierobežošana.</span><span class="sxs-lookup"><span data-stu-id="7723e-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="7723e-174">Papildinformāciju par Darbinieku pašapkalpošanās iestatīšanu skatiet pārskatā [Darbinieku un Pārvaldnieka pašapkalpošanās](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Darbinieku pašapkalpošanās cilne](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="7723e-176">Vadītāja pašapkalpošanās</span><span class="sxs-lookup"><span data-stu-id="7723e-176">Manager self service</span></span>

<span data-ttu-id="7723e-177">**Vadītāja pašapkalpošanās** cilnes iestatījumi ietekmē, ko vadītāji redz Vadītāju pašapkalpošanās programmā.</span><span class="sxs-lookup"><span data-stu-id="7723e-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="7723e-178">Šajā cilnē varat konfigurēt šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="7723e-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="7723e-179">Ierakstu, kuru skaits beidzas, diapazons</span><span class="sxs-lookup"><span data-stu-id="7723e-179">The range for expiring records</span></span>
- <span data-ttu-id="7723e-180">Informācijas pārvaldnieki var skatīt ierakstus, kuru termiņš beidzas</span><span class="sxs-lookup"><span data-stu-id="7723e-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="7723e-181">Vai vadītāji var skatīt atvērtās pozīcijas paplašinātiem pārskatiem</span><span class="sxs-lookup"><span data-stu-id="7723e-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="7723e-182">Izejas darbinieku skatījumi</span><span class="sxs-lookup"><span data-stu-id="7723e-182">Views of exiting workers</span></span>
- <span data-ttu-id="7723e-183">Noderīgas saites vadītājiem</span><span class="sxs-lookup"><span data-stu-id="7723e-183">Useful links for managers</span></span>

<span data-ttu-id="7723e-184">Papildinformāciju par Darbinieku pašapkalpošanās iestatīšanu skatiet [Darbinieku un Vadītāja pašapkalpošanās pārskats](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Vadītāja pašapkalpošanās cilne](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="7723e-186">Atvieglojumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="7723e-186">Benefits management</span></span>

<span data-ttu-id="7723e-187">Cilnē Atvieglojumu pārvaldība varat konfigurēt e-pasta opcijas atvieglojumu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="7723e-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="7723e-188">Papildinformāciju par atvieglojumu pārvaldības iestatīšanu un izmantošanu skatiet [Atvieglojumu pārvaldības pārskats](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Cilne Atvieglojumu pārvaldība](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="7723e-190">Atvaļinājumi un kavējumi</span><span class="sxs-lookup"><span data-stu-id="7723e-190">Leave and absence</span></span>

<span data-ttu-id="7723e-191">Papildinformāciju par atvaļinājumu un kavējumu pārskatu skatiet tēmā [Atvaļinājumu un kavējumu pārskats](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="7723e-192">Maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="7723e-192">Payment methods</span></span>

<span data-ttu-id="7723e-193">Cilnē **Maksājuma metodes** varat atlasīt maksājumu metodes, ko atbalsta jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="7723e-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="7723e-194">Papildinformāciju par atlīdzību konfigurēšanu skatiet [Atlīdzības plānu pārskats](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7723e-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Cilne Maksājuma metodes](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]