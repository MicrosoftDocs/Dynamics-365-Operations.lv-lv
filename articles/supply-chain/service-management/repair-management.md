---
title: Labošanas pārvaldība
description: Sistemātiski sagrupējiet problēmas, lai palīdzētu ar ieteiktiem risinājumiem, kas bijuši veiksmīgi iepriekš.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d0c6ee65713af86378ada79075f969a41f1c0ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836018"
---
# <a name="repair-management"></a><span data-ttu-id="c08d3-103">Labošanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="c08d3-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c08d3-104">Labošanas pārvaldībai varat sistemātiski grupēt problēmas.</span><span class="sxs-lookup"><span data-stu-id="c08d3-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="c08d3-105">Tas tiek darīts, lai palīdzētu ar ieteiktiem risinājumiem, kas bijuši veiksmīgi iepriekš.</span><span class="sxs-lookup"><span data-stu-id="c08d3-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="c08d3-106">Iestatiet simptomu, diagnozes un atrises iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c08d3-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="c08d3-107">Tos visus vēlāk var pielietot gadījumā, ja labošanai saņemat līdzīgu krājumu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="c08d3-108">Varat arī iestatīt labošanas posmus, kuri ļauj sekot labošanas gaitai.</span><span class="sxs-lookup"><span data-stu-id="c08d3-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="c08d3-109">Labošanas pārvaldības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c08d3-109">Setting up repair management</span></span>

<span data-ttu-id="c08d3-110">Izmantojiet šīs iestatīšanas veidlapas, lai ievadītu informāciju, kas tiks izmantota, lai norādītu labošanai simptomus, diagnozi un atrisinājumu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="c08d3-111">**Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="c08d3-112">**Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Simptomu apgabali**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="c08d3-113">**Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Diagnozes apgabali**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="c08d3-114">**Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Atrisinājumi**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="c08d3-115">**Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Labošanas posmi**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="c08d3-116">Simptomi un nosacījumi</span><span class="sxs-lookup"><span data-stu-id="c08d3-116">Symptoms and conditions</span></span>

<span data-ttu-id="c08d3-117">Simptomi ir tas, kā klients raksturo problēmu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="c08d3-118">Simptomos iekļauti klienta novērojumi, kas norāda uz remonta nepieciešamību.</span><span class="sxs-lookup"><span data-stu-id="c08d3-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="c08d3-119">Varat iestatīt simptomu apgabalus, simptomu kodus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="c08d3-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="c08d3-120">Simptomu apgabals attiecas uz kļūmes jomu, un simptomu kods attiecas uz kļūmes simptomu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="c08d3-121">Nosacījumi apraksta situāciju vai vidi situāciju problēmas rašanās brīdī.</span><span class="sxs-lookup"><span data-stu-id="c08d3-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="c08d3-122">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="c08d3-122">**Example**</span></span>

<span data-ttu-id="c08d3-123">Remontam tiek nodots dators cietā diska kļūmes dēļ pēc ilgstoša lietošanas perioda.</span><span class="sxs-lookup"><span data-stu-id="c08d3-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="c08d3-124">Cietā diska kļūmes rezultātā tiek parādīta zilā ekrāna kļūda.</span><span class="sxs-lookup"><span data-stu-id="c08d3-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="c08d3-125">Tehniķis, kurš pieņem datoru, ievada šādus simptomus un nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="c08d3-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="c08d3-126">Simptomu apgabals ir cietais disks</span><span class="sxs-lookup"><span data-stu-id="c08d3-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="c08d3-127">Simptomu kods ir zilā ekrāna kļūda</span><span class="sxs-lookup"><span data-stu-id="c08d3-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="c08d3-128">Nosacījums ir tāds, ka rodas cietā diska kļūme pēc ilgstoša lietošanas perioda.</span><span class="sxs-lookup"><span data-stu-id="c08d3-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="c08d3-129">Diagnoze un atrises</span><span class="sxs-lookup"><span data-stu-id="c08d3-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="c08d3-130">Diagnozes un atrises lauki ir pārskati no remonta perspektīvas.</span><span class="sxs-lookup"><span data-stu-id="c08d3-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="c08d3-131">Šie ir soļi, ko tehniķis veic problēmas izpētes laikā.</span><span class="sxs-lookup"><span data-stu-id="c08d3-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="c08d3-132">Diagnozes apgabals sedz darbību, kas jāveic problēmas risināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="c08d3-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="c08d3-133">Diagnozes kods ir veids, kā problēma tiek apstrādāta, atrise var būt tāda, ka vienība tiek salabota, nomainīta vai klients atceļ pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="c08d3-134">Piemēram, ja dators tiek salabots, diagnozes apgabals varētu būt “bojāta detaļa”, diagnozes kods varētu būt “uzstādīta jauna videokarte”, bet atrisinājums varētu būt “nomainīts”.</span><span class="sxs-lookup"><span data-stu-id="c08d3-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="c08d3-135">Remonta pakāpes</span><span class="sxs-lookup"><span data-stu-id="c08d3-135">Repair stages</span></span>

<span data-ttu-id="c08d3-136">Remonta pakāpes nosaka remonta procesa stāvokli.</span><span class="sxs-lookup"><span data-stu-id="c08d3-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="c08d3-137">Labošanas posmam ir beigu parametrs **Pabeigts**, kas norāda, ka labošanas rinda ir pabeigta un beigšanas datums un laiks ir ierakstīti.</span><span class="sxs-lookup"><span data-stu-id="c08d3-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="c08d3-138">Remonta pārvaldības pielietošana</span><span class="sxs-lookup"><span data-stu-id="c08d3-138">Applying repair management</span></span>

<span data-ttu-id="c08d3-139">Lai pielietotu remonta pārvaldību vienībai, vienībai jābūt iestatītam ar pakalpojumu objektu, kas ir saistībā ar pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="c08d3-140">No pakalpojuma pasūtījuma variet pēc tam izveidot remonta rindu ar informāciju par pašreizējo problēmu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="c08d3-141">remonta rindā definējiet labojamo pakalpojuma objektu un informāciju par simptomiem, diagnozi un izpildījumu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="c08d3-142">Variet arī izveidot piezīmi remonta rindai.</span><span class="sxs-lookup"><span data-stu-id="c08d3-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="c08d3-143">Variet izveidot arī remonta rindas katram remonta procesa solim.</span><span class="sxs-lookup"><span data-stu-id="c08d3-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="c08d3-144">Izveidojiet remonta rindu pakalpojuma pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="c08d3-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="c08d3-145">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="c08d3-146">Izvēlieties pakalpojuma pasūtījumu ar pakalpojuma objektu, ko nepieciešams izlabot.</span><span class="sxs-lookup"><span data-stu-id="c08d3-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="c08d3-147">Noklikšķiniet uz **Labot** \> **Labot rindas**, lai atvērtu veidlapu **Labot rindas**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="c08d3-148">Atlasiet **Jauns**, lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="c08d3-149">Izvēlieties pakalpojuma objektu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-149">Select a service object.</span></span> <span data-ttu-id="c08d3-150">Varat izvēlēties jebkuru objektu, kam pakalpojuma pasūtījumā iestatīta objekta relācija.</span><span class="sxs-lookup"><span data-stu-id="c08d3-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="c08d3-151">Izvēlieties jebkuru priekšiestatīto simptomu, diagnozes un izpildes vērtību, kas ir svarīga labošanas rindā un, ja nepieciešams, pēc tam klikšķiniet uz cilnes **Piezīme**, lai izveidotu piezīmi labošanas rindai.</span><span class="sxs-lookup"><span data-stu-id="c08d3-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="c08d3-152">Atlasiet **Saglabāt**, lai saglabātu jauno, laboto rindu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="c08d3-153">Veidlapas **Labošanas rindas** cilnē **Vispārīgi** lauks **Izveides datums un laiks** tiek atjaunināts ar saglabāšanas laiku.</span><span class="sxs-lookup"><span data-stu-id="c08d3-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="c08d3-154">Sekošana norisei un labošanas problēmu atrisināšana</span><span class="sxs-lookup"><span data-stu-id="c08d3-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="c08d3-155">Varat izvēlēties labošanas rindas posmus, lai sekotu labošanas gaitai.</span><span class="sxs-lookup"><span data-stu-id="c08d3-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="c08d3-156">Kad labošanas problēma ir atrisināta, varat aizvērt labošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="c08d3-157">Iestatiet tādu labošanas posmu, kuram ir iespējots rekvizīts **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="c08d3-158">Pašreizējais datums un laiks tiek reģistrēti rindā kā pabeigšanas laiks.</span><span class="sxs-lookup"><span data-stu-id="c08d3-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="c08d3-159">Aizveriet izlabotās problēmas remonta rindu</span><span class="sxs-lookup"><span data-stu-id="c08d3-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="c08d3-160">Atveriet veidlapu **Labošanas rindas**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="c08d3-161">Ievērojiet šajā tēmā iepriekš aprakstīto procedūru, lai izveidotu labošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="c08d3-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="c08d3-162">Izvēlieties remonta rindu ar remonta problēmu, ko vēlaties aizvērt.</span><span class="sxs-lookup"><span data-stu-id="c08d3-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="c08d3-163">Laukā **Labošanas posms** atlasiet posmu, kuram ir iespējots rekvizīts **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="c08d3-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]