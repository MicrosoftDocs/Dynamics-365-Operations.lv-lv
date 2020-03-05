---
title: Iestatīt apmācību kursus
description: Personāla vadības administratori un vadītāji var izmantot šos kursu līdzekļus, lai uzturētu informāciju par darbiniekiem piedāvāto apmācību.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c3c23ab6fca3f97fbca9edfe83c656e7ca8a2800
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009797"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="ed102-103">Iestatīt apmācību kursus</span><span class="sxs-lookup"><span data-stu-id="ed102-103">Set up training courses</span></span>

<span data-ttu-id="ed102-104">Personāla vadības administratori un vadītāji var izmantot šos kursu līdzekļus, lai uzturētu informāciju par darbiniekiem piedāvāto apmācību.</span><span class="sxs-lookup"><span data-stu-id="ed102-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="ed102-105">Priekšnoteikumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ed102-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="ed102-106">Pirms veidojat kursus, ir nepieciešama un ir jāiestata tālāk norādītā informācija.</span><span class="sxs-lookup"><span data-stu-id="ed102-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="ed102-107">**Kursu tipi**</span><span class="sxs-lookup"><span data-stu-id="ed102-107">**Course types**</span></span>

<span data-ttu-id="ed102-108">Tālāk minēta izvēles informācija, ko var norādīt kursiem.</span><span class="sxs-lookup"><span data-stu-id="ed102-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="ed102-109">Ja zināt, ka ievadīsiet šo informāciju kursiem, jums jāiestata šī informācija pirms kursu ierakstu izveidošanas.</span><span class="sxs-lookup"><span data-stu-id="ed102-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="ed102-110">**Klases grupas**</span><span class="sxs-lookup"><span data-stu-id="ed102-110">**Classroom groups**</span></span>
-   <span data-ttu-id="ed102-111">**Kursu grupas**</span><span class="sxs-lookup"><span data-stu-id="ed102-111">**Course groups**</span></span>
-   <span data-ttu-id="ed102-112">**Kursu atrašanās vietas**</span><span class="sxs-lookup"><span data-stu-id="ed102-112">**Course locations**</span></span>
-   <span data-ttu-id="ed102-113">**Klases telpas**</span><span class="sxs-lookup"><span data-stu-id="ed102-113">**Classrooms**</span></span>
-   <span data-ttu-id="ed102-114">**Instruktori**</span><span class="sxs-lookup"><span data-stu-id="ed102-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="ed102-115">Kursu tipi</span><span class="sxs-lookup"><span data-stu-id="ed102-115">Course types</span></span>
<span data-ttu-id="ed102-116">Kursu tipus var izmantot, lai kategorizētu kursus atbilstoši to struktūrai vai saturam.</span><span class="sxs-lookup"><span data-stu-id="ed102-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="ed102-117">Kursu tipus varat izveidot lapā **Kursu tipi**.</span><span class="sxs-lookup"><span data-stu-id="ed102-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="ed102-118">Veidojot kursu ierakstu, ir jāatlasa kursu veids.</span><span class="sxs-lookup"><span data-stu-id="ed102-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="ed102-119">Kursu iestatīšanas veids</span><span class="sxs-lookup"><span data-stu-id="ed102-119">Course setup type</span></span>
<span data-ttu-id="ed102-120">Tālāk esošajā tabulā uzskaitīti trīs kursu iestatījumu veidi.</span><span class="sxs-lookup"><span data-stu-id="ed102-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="ed102-121">Iestatījumu veidi nosaka kursu struktūru.</span><span class="sxs-lookup"><span data-stu-id="ed102-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ed102-122">Iestatījumu veidi</span><span class="sxs-lookup"><span data-stu-id="ed102-122">Setup type</span></span></th>
<th><span data-ttu-id="ed102-123">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ed102-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed102-124"><strong>Standarta</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="ed102-125">Atlasiet šo veidu kursiem, kam nav ikdienas darba kārtības.</span><span class="sxs-lookup"><span data-stu-id="ed102-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="ed102-126">Šis ir noklusētais iestatījumu veids, veidojot jaunus kursus.</span><span class="sxs-lookup"><span data-stu-id="ed102-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed102-127"><strong>Darba kārtība</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="ed102-128">Atlasiet šo veidu, lai plānotu katras kursa dienas detalizēto informāciju tādam kursam, kas notiek vairākas dienas.</span><span class="sxs-lookup"><span data-stu-id="ed102-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed102-129"><strong>Darba kārtībā + sesija</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="ed102-130">Atlasiet šo veidu sarežģītākiem kursiem.</span><span class="sxs-lookup"><span data-stu-id="ed102-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="ed102-131">Piemēram, kursu darba kārtību var sadalīt tēmās un sesijās.</span><span class="sxs-lookup"><span data-stu-id="ed102-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="ed102-132"><strong>Tēma</strong> — tēmas ir kursu specifiskās jomas.</span><span class="sxs-lookup"><span data-stu-id="ed102-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="ed102-133"><strong>Sesijas</strong> — tēmas ir sīkāk sadalītas sesijās, un sesijas palīdz identificēt tēmai specifiskos procesus vai metodes.</span><span class="sxs-lookup"><span data-stu-id="ed102-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="ed102-134">Kursu uzdevumi</span><span class="sxs-lookup"><span data-stu-id="ed102-134">Course tasks</span></span>
<span data-ttu-id="ed102-135">Katram kursam var izpildīt šādus uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="ed102-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="ed102-136">Reģistrēt dalībniekus</span><span class="sxs-lookup"><span data-stu-id="ed102-136">Register participants</span></span>
- <span data-ttu-id="ed102-137">Norādīt reģistrācijas termiņu</span><span class="sxs-lookup"><span data-stu-id="ed102-137">Specify a registration deadline</span></span>
- <span data-ttu-id="ed102-138">Definēt minimālo un maksimālo dalībnieku skaitu</span><span class="sxs-lookup"><span data-stu-id="ed102-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="ed102-139">Piešķirt kursa atrašanās vietu un mācību telpu</span><span class="sxs-lookup"><span data-stu-id="ed102-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="ed102-140">Kursu dalībniekiem ieteikt viesnīcas</span><span class="sxs-lookup"><span data-stu-id="ed102-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="ed102-141">Veidot kursa aprakstu, ko pēc tam varat reklamēt darbinieku pašapkalpošanās pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="ed102-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="ed102-142">**Piezīme.** Kursu varat dzēst tikai tad, ja tam neviens nav reģistrējies.</span><span class="sxs-lookup"><span data-stu-id="ed102-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="ed102-143">Kursu statusi</span><span class="sxs-lookup"><span data-stu-id="ed102-143">Course statuses</span></span>
<span data-ttu-id="ed102-144">Tālāk esošajā tabulā uzskaitīti iespējamie kursu statusi un darbības, kuras varat pabeigt, kad kursam ir specifisks statuss.</span><span class="sxs-lookup"><span data-stu-id="ed102-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ed102-145">Statuss</span><span class="sxs-lookup"><span data-stu-id="ed102-145">Status</span></span></th>
<th><span data-ttu-id="ed102-146">Darbības</span><span class="sxs-lookup"><span data-stu-id="ed102-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed102-147"><strong>Izveidots</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="ed102-148">Ievadiet un modificējiet kursu informāciju.</span><span class="sxs-lookup"><span data-stu-id="ed102-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="ed102-149">Kursu statusu mainiet uz <strong>Atvērts</strong>, lai darbinieki varētu reģistrēties šim kursam.</span><span class="sxs-lookup"><span data-stu-id="ed102-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed102-150"><strong>Atvērts</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="ed102-151">Reģistrējiet dalībniekus kursiem.</span><span class="sxs-lookup"><span data-stu-id="ed102-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="ed102-152">Dzēsiet kursu dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="ed102-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="ed102-153">Apstipriniet kursu dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="ed102-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="ed102-154">Mainiet kursa statusu uz <strong>Slēgts</strong> vai <strong>Atcelts</strong>.</span><span class="sxs-lookup"><span data-stu-id="ed102-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="ed102-155">Plānojiet anketas darbiniekiem, kuru statuss ir <strong>Apstiprināts</strong>.</span><span class="sxs-lookup"><span data-stu-id="ed102-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed102-156"><strong>Slēgts</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="ed102-157">Kursus var atvērt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="ed102-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed102-158"><strong>Atcelts</strong></span><span class="sxs-lookup"><span data-stu-id="ed102-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="ed102-159">Kursus var atvērt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="ed102-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="ed102-160">Kursu dalībnieki</span><span class="sxs-lookup"><span data-stu-id="ed102-160">Course participants</span></span>
<span data-ttu-id="ed102-161">Kursu dalībnieki ir darbinieki, kuri piedalās apmācības kursos vai notikumā.</span><span class="sxs-lookup"><span data-stu-id="ed102-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="ed102-162">Dalībniekus var reģistrēt tikai atvērtiem kursiem.</span><span class="sxs-lookup"><span data-stu-id="ed102-162">You can only register participants for open courses.</span></span> <span data-ttu-id="ed102-163">Minimālais un maksimālais dalībnieku skaits, ko varat reģistrēt vienam kursam, ir noteikts kopsavilkuma cilnē **Vispārīgi**, lapā **Kursi**.</span><span class="sxs-lookup"><span data-stu-id="ed102-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="ed102-164">Darbplūsma</span><span class="sxs-lookup"><span data-stu-id="ed102-164">Workflow</span></span>
--------

<span data-ttu-id="ed102-165">Darbinieki, kuri kursam ir reģistrējušies, izmantojot lapu **Darbinieku pašapkalpošanās**, savu reģistrāciju var maršrutēt apstiprināšanai caur darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="ed102-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="ed102-166">Darbplūsmu kursam varat piešķirt kopsavilkuma cilnē **Vispārīgi**, lapā **Kursi**.</span><span class="sxs-lookup"><span data-stu-id="ed102-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>




