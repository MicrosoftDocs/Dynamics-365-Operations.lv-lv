---
title: Izprotiet datuma un laika laukus
description: Saprast, ko sagaidīt, izmantojot laukus Datums un Laiks programmā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a8bc27bb4560b4a15aef483ff465c4b943bf02b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889888"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="e6dc6-103">Informācija par datuma un laika laukiem</span><span class="sxs-lookup"><span data-stu-id="e6dc6-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e6dc6-104">**Datuma un laika** lauki ir pamatjēdzieni programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e6dc6-105">Ir svarīgi saprast, kā strādāt ar **Datuma un laika** datiem veidlapās, Dataverse un ārējos avotos.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="e6dc6-106">Izprast atšķirību starp datuma un datuma un laika lauku datu veidiem</span><span class="sxs-lookup"><span data-stu-id="e6dc6-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="e6dc6-107">**Datuma un laika** lauki ietver informāciju par laika joslu, bet **Datuma** lauki to neietver.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="e6dc6-108">**Datuma** lauki rāda vienu un to pašu informāciju jebkurā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="e6dc6-109">Kad ievadāt datumu datumu laukā **Datums** programma Human Resources ieraksta šo pašu datumu datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="e6dc6-110">Parādot datus laukā **Datums un laiks**, programma Human Resources pielāgo datumu un laiku, pamatojoties uz lietotāja laika zonu, kas iestatīta veidlapā **Lietotāja opcijas** (**Kopīgi > Iestatīšana > Lietotāja opcijas**).</span><span class="sxs-lookup"><span data-stu-id="e6dc6-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="e6dc6-111">Datuma un laika informācija, ko ievadāt laukā, var nebūt vienāda ar datu bāzē ierakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="e6dc6-112">[![Lietotāja opciju veidlapa](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="e6dc6-113">Izpratne par Datuma un laika laukiem veidlapās</span><span class="sxs-lookup"><span data-stu-id="e6dc6-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="e6dc6-114">**Datuma un laika** ekrānā parādītie dati nav tādi paši kā dati, kas tiek glabāti datu bāzē, ja lietotāja laika josla nav iestatīta uz koordinēto pasaules laiku (UTC).</span><span class="sxs-lookup"><span data-stu-id="e6dc6-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e6dc6-115">Dati **Datuma un laika** laukos vienmēr tiek glabāti kā UTC.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="e6dc6-116">[![Darbinieka veidlapa UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="e6dc6-117">Izpratne par Datuma un laika laukiem datu bāzē</span><span class="sxs-lookup"><span data-stu-id="e6dc6-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="e6dc6-118">Kad programma Human Resources ieraksta **Datuma un laika** vērtību datu bāzē, tā saglabā datus UTC.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="e6dc6-119">Tas ļauj lietotājiem skatīt visus **Datuma un laika** datus attiecībā pret laika joslu, kas definēta to lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="e6dc6-120">Iepriekšminētajā piemērā sākuma laiks ir laika punkts, nevis konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="e6dc6-121">Mainot lietotājā reģistrēto laika joslu no GMT + 12:00 uz GMT UTC, tas pats ieraksts rāda 04/30/2019 12:00:00, nevis 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="e6dc6-122">Zemāk minētajā piemērā darbinieku 000724 nodarbinātība kļūst aktīva tajā pašā laikā neatkarīgi no laika zonas.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="e6dc6-123">Darbinieks būs aktīvs 04/30/2019 GMT laika joslā, kas ir tad pat kad 05/01/2019 GMT + 12:00 laika zonā.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="e6dc6-124">Abi attiecas uz vienu un to pašu punktu laikā, nevis konkrētu datumu.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="e6dc6-125">[![Darbinieka veidlapa GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="e6dc6-126">Datuma un laika dati Datu pārvaldības struktūrā, Excel, Dataverse un Power BI</span><span class="sxs-lookup"><span data-stu-id="e6dc6-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="e6dc6-127">Datu pārvaldības struktūra, Excel pievienojumprogramma, Dataverse un Power BI ziņošana ir paredzēta, lai mijiedarbotos ar datiem tieši datu bāzes līmenī.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="e6dc6-128">Tā kā nav klienta, lai koriģētu **Datuma un laika** datus uz lietotāja laika joslu, visas **Datuma un laika** vērtības ir UTC, kas var izraisīt dažus kļūdainus pieņēmumus, ievadot vai skatot datus.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="e6dc6-129">**Datuma un laika** dati, kas tiek iesniegti, izmantojot DMF, Excel vai Dataverse, datu bāze pieņem, ka tie ir UTC.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="e6dc6-130">Tas var izraisīt pārpratumus, ja iesniegtā **Datuma un laika** vērtība netiek rādīta kā paredzēts, jo lietotājam, kurš skata datus, nav iestatīta lietotāja laika josla uz UTC.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="e6dc6-131">Tas pats var notikt pretēji, kad dati tiek eksportēti.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="e6dc6-132">**Datuma un laika** dati eksportētajā DMF elementā var atšķirties no tiem, kas tiek parādīti Dynamics klientā.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="e6dc6-133">Lietojot ārējos avotus, piemēram, DMF, lai skatītu vai autorizētu datus, jāpatur prātā, ka pēc noklusējuma tiek uzskatīts, ka **Datuma un laika** vērtības ir UTC neatkarīgi no lietotāja datora laika joslas vai to pašreizējā lietotāja laika joslas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="e6dc6-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="e6dc6-134">Viena un tā paša ieraksta piemēri, kas tiek rādīti dažādos preču apgabalos</span><span class="sxs-lookup"><span data-stu-id="e6dc6-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="e6dc6-135">**Programma Human Resources ar lietotāja laika joslu iestatītu uz UTC**</span><span class="sxs-lookup"><span data-stu-id="e6dc6-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="e6dc6-136">[![Darbinieka veidlapa, kas iestatīta uz UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="e6dc6-137">**Programma Human Resources ar lietotāja laika joslu iestatītu uz GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="e6dc6-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="e6dc6-138">[![Darbinieka veidlapa, kas iestatīta uz GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="e6dc6-139">**Excel, izmantojot OData**</span><span class="sxs-lookup"><span data-stu-id="e6dc6-139">**Excel Via OData**</span></span>

<span data-ttu-id="e6dc6-140">[![Excel, izmantojot OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="e6dc6-141">**DMF sagatavošana**</span><span class="sxs-lookup"><span data-stu-id="e6dc6-141">**DMF Staging**</span></span>

<span data-ttu-id="e6dc6-142">[![DMF sagatavošana](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="e6dc6-143">**DMF eksportēšana**</span><span class="sxs-lookup"><span data-stu-id="e6dc6-143">**DMF Export**</span></span>

<span data-ttu-id="e6dc6-144">[![DMF eksports](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="e6dc6-145">**Excel, izmantojot Dataverse**</span><span class="sxs-lookup"><span data-stu-id="e6dc6-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="e6dc6-146">[![Excel, izmantojot Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="e6dc6-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="e6dc6-147">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="e6dc6-147">See also</span></span>

[<span data-ttu-id="e6dc6-148">IDatuma un laika dati</span><span class="sxs-lookup"><span data-stu-id="e6dc6-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="e6dc6-149">Lietotāja izvēlētās laika joslas</span><span class="sxs-lookup"><span data-stu-id="e6dc6-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]