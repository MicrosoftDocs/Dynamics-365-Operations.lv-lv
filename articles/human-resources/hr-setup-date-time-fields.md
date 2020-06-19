---
title: Izprotiet datuma un laika laukus
description: Saprast, ko sagaidīt, izmantojot laukus Datums un Laiks programmā Microsoft Dynamics 365 Human Resources. Iegūstiet skaidrību par to, ko sagaidīt, mijiedarbojoties ar datuma un laika datiem personāla vadības veidlapā, ārējā avotā vai Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be1e28d0b842184ce3c4f7bd9748f5e76ac67489
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430099"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="c452e-104">Izprotiet datuma un laika laukus</span><span class="sxs-lookup"><span data-stu-id="c452e-104">Understand Date and Time fields</span></span>

<span data-ttu-id="c452e-105">**Datuma un laika** lauki ir pamatjēdzieni programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c452e-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c452e-106">Ir svarīgi saprast, kā strādāt ar **Datuma un laika** datiem Dynamics 365 Human Resources veidlapās, Common Data Service un ārējos avotos.</span><span class="sxs-lookup"><span data-stu-id="c452e-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="c452e-107">Izprast atšķirību starp datuma un datuma un laika lauku datu veidiem</span><span class="sxs-lookup"><span data-stu-id="c452e-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="c452e-108">**Datuma un laika** lauki ietver informāciju par laika joslu, bet **Datuma** lauki to neietver.</span><span class="sxs-lookup"><span data-stu-id="c452e-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="c452e-109">**Datuma** lauki rāda vienu un to pašu informāciju jebkurā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="c452e-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="c452e-110">Kad ievadāt datumu datumu laukā **Datums** programma Human Resources ieraksta šo pašu datumu datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="c452e-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="c452e-111">Parādot datus laukā **Datums un laiks**, programma Human Resources pielāgo datumu un laiku, pamatojoties uz lietotāja laika zonu, kas iestatīta veidlapā **Lietotāja opcijas** (**Kopīgi > Iestatīšana > Lietotāja opcijas**).</span><span class="sxs-lookup"><span data-stu-id="c452e-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="c452e-112">Datuma un laika informācija, ko ievadāt laukā, var nebūt vienāda ar datu bāzē ierakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="c452e-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="c452e-113">[![Lietotāja opciju veidlapa](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="c452e-114">Izpratne par Datuma un laika laukiem veidlapās</span><span class="sxs-lookup"><span data-stu-id="c452e-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="c452e-115">Ievadot datus **Datuma un laika** laukā, ekrānā parādītie dati nav tādi paši kā dati, kas tiek glabāti datu bāzē, ja lietotāja laika josla nav iestatīta uz koordinēto pasaules laiku (UTC).</span><span class="sxs-lookup"><span data-stu-id="c452e-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c452e-116">Dati **Datuma un laika** laukos vienmēr tiek glabāti kā UTC.</span><span class="sxs-lookup"><span data-stu-id="c452e-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="c452e-117">[![Darbinieka veidlapa](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="c452e-118">Izpratne par Datuma un laika laukiem datu bāzē</span><span class="sxs-lookup"><span data-stu-id="c452e-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="c452e-119">Kad programma Human Resources ieraksta **Datuma un laika** vērtību datu bāzē, tā saglabā datus UTC.</span><span class="sxs-lookup"><span data-stu-id="c452e-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="c452e-120">Tas ļauj lietotājiem skatīt visus **Datuma un laika** datus attiecībā pret laika joslu, kas definēta to lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="c452e-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="c452e-121">Iepriekšminētajā piemērā sākuma laiks ir laika punkts, nevis konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="c452e-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="c452e-122">Mainot lietotājā reģistrēto laika joslu no GMT + 12:00 uz GMT UTC, tas pats tikko izveidotais ieraksts rāda 04/30/2019 12:00:00, nevis 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="c452e-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="c452e-123">Zemāk minētajā piemērā darbinieku 000724 nodarbinātība kļūst aktīva tajā pašā laikā neatkarīgi no laika zonas.</span><span class="sxs-lookup"><span data-stu-id="c452e-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="c452e-124">Darbinieks būs aktīvs 04/30/2019 GMT laika joslā, kas ir tad pat kad 05/01/2019 GMT + 12:00 laika zonā.</span><span class="sxs-lookup"><span data-stu-id="c452e-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="c452e-125">Abi attiecas uz vienu un to pašu punktu laikā, nevis konkrētu datumu.</span><span class="sxs-lookup"><span data-stu-id="c452e-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="c452e-126">[![Darbinieka veidlapa](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="c452e-127">Datuma un laika dati Datu pārvaldības struktūrā, Excel, Common Data Service un Power BI</span><span class="sxs-lookup"><span data-stu-id="c452e-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="c452e-128">Datu pārvaldības struktūra, Excel pievienojumprogramma, Common Data Service un Power BI ziņošana ir paredzēta, lai mijiedarbotos ar datiem tieši datu bāzes līmenī.</span><span class="sxs-lookup"><span data-stu-id="c452e-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="c452e-129">Tā kā nav klienta, lai koriģētu **Datuma un laika** datus uz lietotāja laika joslu, visas **Datuma un laika** vērtības ir UTC, kas var izraisīt dažus kļūdainus pieņēmumus, ievadot vai skatot datus.</span><span class="sxs-lookup"><span data-stu-id="c452e-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="c452e-130">**Datuma un laika** dati, kas tiek iesniegti, izmantojot DMF, Excel vai Common Data Service, datu bāze pieņem, ka tie ir UTC.</span><span class="sxs-lookup"><span data-stu-id="c452e-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="c452e-131">Tas var izraisīt pārpratumus, ja iesniegtā **Datuma un laika** vērtība netiek rādīta kā paredzēts, jo lietotājam, kurš skata datus, nav iestatīta lietotāja laika josla uz UTC.</span><span class="sxs-lookup"><span data-stu-id="c452e-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="c452e-132">Tas pats var notikt pretēji, kad dati tiek eksportēti.</span><span class="sxs-lookup"><span data-stu-id="c452e-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="c452e-133">**Datuma un laika** dati eksportētajā DMF elementā var atšķirties no tiem, kas tiek parādīti Dynamics klientā.</span><span class="sxs-lookup"><span data-stu-id="c452e-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="c452e-134">Lietojot ārējos avotus, piemēram, DMF, lai skatītu vai autorizētu datus, ir svarīgi paturēt prātā, ka pēc noklusējuma tiek uzskatīts, ka **Datuma un laika** vērtības ir UTC neatkarīgi no lietotāja datora laika joslas vai to pašreizējā lietotāja laika joslas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="c452e-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="c452e-135">Viena un tā paša ieraksta piemēri, kas tiek rādīti dažādos preču apgabalos</span><span class="sxs-lookup"><span data-stu-id="c452e-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="c452e-136">**Programma Human Resources ar lietotāja laika joslu iestatītu uz UTC**</span><span class="sxs-lookup"><span data-stu-id="c452e-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="c452e-137">[![Darbinieka veidlapa](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="c452e-138">**Programma Human Resources ar lietotāja laika joslu iestatītu uz GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="c452e-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="c452e-139">[![Darbinieka veidlapa](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="c452e-140">**Excel, izmantojot OData**</span><span class="sxs-lookup"><span data-stu-id="c452e-140">**Excel Via OData**</span></span>

<span data-ttu-id="c452e-141">[![Excel, izmantojot OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="c452e-142">**DMF sagatavošana**</span><span class="sxs-lookup"><span data-stu-id="c452e-142">**DMF Staging**</span></span>

<span data-ttu-id="c452e-143">[![DMF sagatavošana](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="c452e-144">**DMF eksportēšana**</span><span class="sxs-lookup"><span data-stu-id="c452e-144">**DMF Export**</span></span>

<span data-ttu-id="c452e-145">[![DMF sagatavošana](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="c452e-146">**Excel, izmantojot Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="c452e-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="c452e-147">[![Excel, izmantojot Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="c452e-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="c452e-148">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="c452e-148">See also</span></span>

[<span data-ttu-id="c452e-149">IDatuma un laika dati</span><span class="sxs-lookup"><span data-stu-id="c452e-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="c452e-150">Lietotāja izvēlētās laika joslas</span><span class="sxs-lookup"><span data-stu-id="c452e-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
