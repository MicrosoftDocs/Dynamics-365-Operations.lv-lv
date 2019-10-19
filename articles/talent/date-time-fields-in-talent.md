---
title: Darbs ar datumu un laiku programmā Microsoft Dynamics 365 Talent
description: Saprast, ko sagaidīt, izmantojot laukus Datums un Laiks programmā Microsoft Dynamics 365 Talent. Iegūstiet skaidrību par to, ko sagaidīt, mijiedarbojoties ar datuma un laika datiem veidlapā Talent, ārējā avotā vai Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
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
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a1d1a47bfe6bd58b1e1a0d4d46c2133f3bf48ad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2007971"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="6ddcc-104">Datuma un laika lauki programmā Talent</span><span class="sxs-lookup"><span data-stu-id="6ddcc-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ddcc-105">**Datuma un laika** lauki ir pamatjēdzieni programmā Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Talent.</span></span> <span data-ttu-id="6ddcc-106">Ir svarīgi saprast, kā strādāt ar **Datuma un laika** datiem Dynamics 365 veidlapā, Common Data Service un ārējos avotos.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="6ddcc-107">Izprast atšķirību starp datuma un datuma un laika lauku datu veidiem</span><span class="sxs-lookup"><span data-stu-id="6ddcc-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="6ddcc-108">**Datuma un laika** lauki ietver informāciju par laika joslu, bet **Datuma** lauki to neietver.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="6ddcc-109">**Datuma** lauki rāda vienu un to pašu informāciju jebkurā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="6ddcc-110">Kad ievadāt datumu datumu laukā **Datums** programma Talent ieraksta šo pašu datumu datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="6ddcc-111">Parādot datus laukā **Datums un laiks**, programma Talent pielāgo datumu un laiku, pamatojoties uz lietotāja laika zonu, kas iestatīta veidlapā **Lietotāja opcijas** (**Kopīgi > Iestatīšana > Lietotāja opcijas**).</span><span class="sxs-lookup"><span data-stu-id="6ddcc-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="6ddcc-112">Datuma un laika informācija, ko ievadāt laukā, var nebūt vienāda ar datu bāzē ierakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="6ddcc-113">[![Lietotāja opciju veidlapa](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="6ddcc-114">Izpratne par Datuma un laika laukiem veidlapās</span><span class="sxs-lookup"><span data-stu-id="6ddcc-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="6ddcc-115">Ievadot datus **Datuma un laika** laukā, ekrānā parādītie dati nav tādi paši kā dati, kas tiek glabāti datu bāzē, ja lietotāja laika josla nav iestatīta uz koordinēto pasaules laiku (UTC).</span><span class="sxs-lookup"><span data-stu-id="6ddcc-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="6ddcc-116">Dati **Datuma un laika** laukos vienmēr tiek glabāti kā UTC.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="6ddcc-117">[![Darbinieka veidlapa](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="6ddcc-118">Izpratne par Datuma un laika laukiem datu bāzē</span><span class="sxs-lookup"><span data-stu-id="6ddcc-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="6ddcc-119">Kad Programma Talent ieraksta **Datuma un laika** vērtību datu bāzē, tā saglabā datus UTC.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="6ddcc-120">Tas ļauj lietotājiem skatīt visus **Datuma un laika** datus attiecībā pret laika joslu, kas definēta to lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="6ddcc-121">Iepriekšminētajā piemērā sākuma laiks ir laika punkts, nevis konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="6ddcc-122">Mainot lietotājā reģistrēto laika joslu no GMT + 12:00 uz GMT UTC, tas pats tikko izveidotais ieraksts rāda 04/30/2019 12:00:00, nevis 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="6ddcc-123">Zemāk minētajā piemērā darbinieku 000724 nodarbinātība kļūst aktīva tajā pašā laikā neatkarīgi no laika zonas.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="6ddcc-124">Darbinieks būs aktīvs 04/30/2019 GMT laika joslā, kas ir tad pat kad 05/01/2019 GMT + 12:00 laika zonā.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="6ddcc-125">Abi attiecas uz vienu un to pašu punktu laikā, nevis konkrētu datumu.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="6ddcc-126">[![Darbinieka veidlapa](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="6ddcc-127">Datuma un laika dati Datu pārvaldības struktūrā, Excel, Common Data Service un Power BI</span><span class="sxs-lookup"><span data-stu-id="6ddcc-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="6ddcc-128">Datu pārvaldības struktūra, Excel pievienojumprogramma, Common Data Service un Power BI ziņošana ir paredzēta, lai mijiedarbotos ar datiem tieši datu bāzes līmenī.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="6ddcc-129">Tā kā nav klienta, lai koriģētu **Datuma un laika** datus uz lietotāja laika joslu, visas **Datuma un laika** vērtības ir UTC, kas var izraisīt dažus kļūdainus pieņēmumus, ievadot vai skatot datus.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="6ddcc-130">**Datuma un laika** dati, kas tiek iesniegti, izmantojot DMF, Excel vai Common Data Service, datu bāze pieņem, ka tie ir UTC.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="6ddcc-131">Tas var izraisīt pārpratumus, ja iesniegtā **Datuma un laika** vērtība netiek rādīta kā paredzēts, jo lietotājam, kurš skata datus, nav iestatīta lietotāja laika josla uz UTC.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="6ddcc-132">Tas pats var notikt pretēji, kad dati tiek eksportēti.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="6ddcc-133">**Datuma un laika** dati eksportētajā DMF elementā var atšķirties no tiem, kas tiek parādīti Dynamics klientā.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="6ddcc-134">Lietojot ārējos avotus, piemēram, DMF, lai skatītu vai autorizētu datus, ir svarīgi paturēt prātā, ka pēc noklusējuma tiek uzskatīts, ka **Datuma un laika** vērtības ir UTC neatkarīgi no lietotāja datora laika joslas vai to pašreizējā lietotāja laika joslas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="6ddcc-135">Viena un tā paša ieraksta piemēri, kas tiek rādīti dažādos preču apgabalos</span><span class="sxs-lookup"><span data-stu-id="6ddcc-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="6ddcc-136">**Programma Talent ar lietotāja laika joslu iestatītu uz UTC**</span><span class="sxs-lookup"><span data-stu-id="6ddcc-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="6ddcc-137">[![Darbinieka veidlapa](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="6ddcc-138">**Programma Talent ar lietotāja laika joslu iestatītu uz GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="6ddcc-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="6ddcc-139">[![Darbinieka veidlapa](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="6ddcc-140">**Excel, izmantojot OData**</span><span class="sxs-lookup"><span data-stu-id="6ddcc-140">**Excel Via OData**</span></span>

<span data-ttu-id="6ddcc-141">[![Excel, izmantojot OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="6ddcc-142">**DMF sagatavošana**</span><span class="sxs-lookup"><span data-stu-id="6ddcc-142">**DMF Staging**</span></span>

<span data-ttu-id="6ddcc-143">[![DMF sagatavošana](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="6ddcc-144">**DMF eksportēšana**</span><span class="sxs-lookup"><span data-stu-id="6ddcc-144">**DMF Export**</span></span>

<span data-ttu-id="6ddcc-145">[![DMF sagatavošana](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="6ddcc-146">**Excel, izmantojot Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="6ddcc-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="6ddcc-147">[![Excel, izmantojot Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="6ddcc-148">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="6ddcc-148">See also</span></span>

[<span data-ttu-id="6ddcc-149">IDatuma un laika dati</span><span class="sxs-lookup"><span data-stu-id="6ddcc-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="6ddcc-150">Lietotāja izvēlētās laika joslas</span><span class="sxs-lookup"><span data-stu-id="6ddcc-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
