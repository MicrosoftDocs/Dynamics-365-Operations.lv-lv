---
title: Darba laika kalendāra izveide
description: Definējiet darba laika kalendāru, brīvdienas un ārpusdarba laikus pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc209b62836011b18362f78b63cdd3fcda884dc3
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198031"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="5352c-103">Darba laika kalendāra izveide</span><span class="sxs-lookup"><span data-stu-id="5352c-103">Create a working time calendar</span></span>

<span data-ttu-id="5352c-104">Darba laika kalendārs programmā Dynamics 365 Human Resources rāda dienas un stundas, kuras darbinieki strādā jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="5352c-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="5352c-105">Kad darbinieks iesniedz brīvā laika pieprasījumu, viņiem nav jāraizējas par brīvdienām un slēgšanu.</span><span class="sxs-lookup"><span data-stu-id="5352c-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="5352c-106">Lai racionalizētu brīvā laika pieprasījumus, konfigurējiet šos elementus savai organizācijai:</span><span class="sxs-lookup"><span data-stu-id="5352c-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="5352c-107">Darba laika kalendārs</span><span class="sxs-lookup"><span data-stu-id="5352c-107">Working time calendar</span></span>
- <span data-ttu-id="5352c-108">Brīvdienas un slēgšana</span><span class="sxs-lookup"><span data-stu-id="5352c-108">Holidays and closures</span></span>
- <span data-ttu-id="5352c-109">Nestrādājamais laiks</span><span class="sxs-lookup"><span data-stu-id="5352c-109">Non-work time</span></span>

<span data-ttu-id="5352c-110">Varat pievienot pēdējos divus elementus, kad iestatāt darba laika kalendāru.</span><span class="sxs-lookup"><span data-stu-id="5352c-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="5352c-111">Varat arī tos konfigurēt vai atjaunināt atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="5352c-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="5352c-112">Darba laika kalendāra iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5352c-112">Set up a working time calendar</span></span>

<span data-ttu-id="5352c-113">Iestatiet vismaz vienu darba laika kalendāru, kas rāda darbības dienas un stundas.</span><span class="sxs-lookup"><span data-stu-id="5352c-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="5352c-114">Ja jums ir atrašanās vietas vairākās valstīs un reģionos, iespējams, vēlēsities iestatīt darba laika kalendāru katram apgabalam.</span><span class="sxs-lookup"><span data-stu-id="5352c-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="5352c-115">Lapā **Organizācijas administrēšana** atlasiet **Kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="5352c-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="5352c-116">Atlasiet **Jauns** un ievadiet sava kalendāra nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5352c-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="5352c-117">Sadaļā **Ģenerēšanas opcijas** atlasiet savas organizācijas darba dienas un ievadiet darba laikus.</span><span class="sxs-lookup"><span data-stu-id="5352c-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="5352c-118">Lai pievienotu atvaļinājumu vai slēgšanu, atlasiet pogu **Pievienot** blakus **Brīvdienas un slēgšana**.</span><span class="sxs-lookup"><span data-stu-id="5352c-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="5352c-119">Lai pievienotu nestrādājamo laiku, piemēram, pusdienas vai pārtraukumus, atlasiet **Pievienot** sadaļā **Nestrādājamais laiks** un ievadiet nosaukumu un laika diapazonu.</span><span class="sxs-lookup"><span data-stu-id="5352c-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="5352c-120">Sadaļā **Dienas** atlasiet **Ģenerēt**, lai ģenerētu dienas kalendārā.</span><span class="sxs-lookup"><span data-stu-id="5352c-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="5352c-121">Ievadiet datumu diapazonu savam kalendāram un atlasiet **Ģenerēt dienas**.</span><span class="sxs-lookup"><span data-stu-id="5352c-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="5352c-122">Lai pievienotu darba grafikus, sadaļā **Darba grafiks** atlasiet **Pievienot** un pēc tam ievadiet laiku katram darba grafikam.</span><span class="sxs-lookup"><span data-stu-id="5352c-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="5352c-123">Brīvdienu un slēgšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5352c-123">Configure holidays and closures</span></span>

<span data-ttu-id="5352c-124">Brīvdienas un slēgšanu var pievienot vai mainīt atsevišķi no darba laika kalendāra.</span><span class="sxs-lookup"><span data-stu-id="5352c-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="5352c-125">Lapā **Organizācijas administrēšana** atlasiet **Brīvdienas un slēgšana**.</span><span class="sxs-lookup"><span data-stu-id="5352c-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="5352c-126">Atlasiet **Jauns** un ievadiet brīvdienas vai slēgšanas nosaukumu un datumu.</span><span class="sxs-lookup"><span data-stu-id="5352c-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="5352c-127">Nestrādājamā laika konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5352c-127">Configure non-work time</span></span>

<span data-ttu-id="5352c-128">Nestrādājamo laiku var pievienot vai mainīt atsevišķi no darba laika kalendāra.</span><span class="sxs-lookup"><span data-stu-id="5352c-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="5352c-129">Lapā **Organizācijas administrēšana** atlasiet **Nestrādājamais laiks**.</span><span class="sxs-lookup"><span data-stu-id="5352c-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="5352c-130">Atlasiet **Jauns** un ievadiet nestrādājamā laika nosaukumu un laika diapazonu.</span><span class="sxs-lookup"><span data-stu-id="5352c-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="5352c-131">Ja esat iespējojis atvaļinājumu un prombūtnes bankas brīvdienu labošanas priekšskatījuma līdzekli, Human Resources izmanto brīvdienas un slēgšanas datumus, lai noteiktu dienu skaitu, kas jāpielāgo darbiniekiem, kas reģistrēti kalendārā.</span><span class="sxs-lookup"><span data-stu-id="5352c-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="5352c-132">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="5352c-132">See also</span></span>

- [<span data-ttu-id="5352c-133">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="5352c-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="5352c-134">Atvaļinājumu un prombūtnes veidu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5352c-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
