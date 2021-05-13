---
title: Procesu automatizācija
description: Šī tēma sniedz detalizētu informāciju par to, kā procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920833"
---
# <a name="process-automation"></a><span data-ttu-id="5d61c-103">Procesu automatizācija</span><span class="sxs-lookup"><span data-stu-id="5d61c-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5d61c-104">Procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.</span><span class="sxs-lookup"><span data-stu-id="5d61c-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="5d61c-105">Ieplānotā darba atjauninātais kalendāra skats ļauj lietotājiem skatīt un rīkoties ar plānoto un pabeigto darbu.</span><span class="sxs-lookup"><span data-stu-id="5d61c-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="5d61c-106">Administrācija</span><span class="sxs-lookup"><span data-stu-id="5d61c-106">Administration</span></span>

<span data-ttu-id="5d61c-107">Centrālā administrēšanas lapa visu procesu automatizācijām ir atrodama Sistēmas administrēšanas modulī, kas atrodas izvēlnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d61c-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="5d61c-108">Šajā lapā tiks uzskaitīti visi automatizētie procesi (sērijas), kas ir iestatīti sistēmā.</span><span class="sxs-lookup"><span data-stu-id="5d61c-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="5d61c-109">Tas arī ļaus jums pievienot jaunu procesu automatizācijas tieši no šīs lapas.</span><span class="sxs-lookup"><span data-stu-id="5d61c-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="5d61c-110">Pēc sērijas iestatīšanas varat pārvaldīt katru šī saraksta sēriju.</span><span class="sxs-lookup"><span data-stu-id="5d61c-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="5d61c-111">Varat izvēlēties rediģēt visu sēriju, dzēst to, skatīt visus gadījumus saraksta skatā vai atspējot sēriju, ja vēlaties pauzēt plānoto darbu.</span><span class="sxs-lookup"><span data-stu-id="5d61c-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="5d61c-112">Visi procesi, kas ir atspējoti līdzekļu pārvaldībā, netiks rādīti, kad līdzeklis ir atspējots.</span><span class="sxs-lookup"><span data-stu-id="5d61c-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="5d61c-113">Turklāt procesu automatizācijas plānošanas programma neplāno nekādus gadījumus vai fona procesus atspējotam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="5d61c-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="5d61c-114">No jauna iespējojot šo līdzekli, visi ieplānotie gadījumi vai fona procesi pagātnē tiek nekavējoties palaisti.</span><span class="sxs-lookup"><span data-stu-id="5d61c-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="5d61c-115">Procesa automatizācijas plānošanas programma balstās uz sistēmas pakešuzdevuma **Procesa automatizācijas aptauju sistēmas darbs** palaišanu.</span><span class="sxs-lookup"><span data-stu-id="5d61c-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="5d61c-116">Darbs nekādā gadījumā nedrīkst tikt mainīts vai pārveidots.</span><span class="sxs-lookup"><span data-stu-id="5d61c-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="5d61c-117">Kalendāra skats</span><span class="sxs-lookup"><span data-stu-id="5d61c-117">Calendar view</span></span>

<span data-ttu-id="5d61c-118">Viens no procesa automatizācijas galvenajiem ieguvumiem ir iespēja redzēt plānoto darbu vienkāršā kalendāra skatā.</span><span class="sxs-lookup"><span data-stu-id="5d61c-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="5d61c-119">Šis skats ļauj jums skatīt darbu nedēļas laikā.</span><span class="sxs-lookup"><span data-stu-id="5d61c-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="5d61c-120">Šis skats tiks rādīts **Procesa automatizācijas** lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="5d61c-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="5d61c-121">Tas tiks aizpildīts ar atlasītās sērijas ieplānoto darbu.</span><span class="sxs-lookup"><span data-stu-id="5d61c-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="5d61c-122">[![Procesu automatizācijas kalendārs](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="5d61c-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="5d61c-123">Gadījumu izmaiņas</span><span class="sxs-lookup"><span data-stu-id="5d61c-123">Occurrence changes</span></span>

<span data-ttu-id="5d61c-124">Katru gadījumu var modificēt, neietekmējot ar tām izveidoto sēriju definētos citus gadījumus.</span><span class="sxs-lookup"><span data-stu-id="5d61c-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="5d61c-125">Ieplānotā darba gadījumus var rediģēt no kalendāra skata, atlasot pogu **Skatīt/rediģēt** un atlasot **Gadījums**.</span><span class="sxs-lookup"><span data-stu-id="5d61c-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="5d61c-126">Šī lapa ļauj jums piekļūt visiem iestatījumiem, kas sākotnēji tika parādīti sēriju iestatīšanas vednī, un sniedz iespēju atlasītajam gadījumam veikt vienreizējas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5d61c-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="5d61c-127">Ieplānotā darba gadījumu var izslēgt arī, atlasot pogu **Atspējot** no kalendāra skata.</span><span class="sxs-lookup"><span data-stu-id="5d61c-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="5d61c-128">Izstrādātāja dokumentācija</span><span class="sxs-lookup"><span data-stu-id="5d61c-128">Developer documentation</span></span>

<span data-ttu-id="5d61c-129">Procesu automatizācijas struktūra ļauj izstrādātājiem paplašināt procesu automatizācijas struktūru.</span><span class="sxs-lookup"><span data-stu-id="5d61c-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="5d61c-130">Šī [Procesu automatizācijas struktūras](../process-automation/process-automation-framework.md) dokumentācija sniedz informāciju par to, kā varat izveidot pielāgotus procesus, kas ir nepieciešami, lai palaistu pakešu serveri, kas paredzēts procesu automatizācijas vednim, un automātiski tiek rādīti kalendāra skatā.</span><span class="sxs-lookup"><span data-stu-id="5d61c-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
