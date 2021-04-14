---
title: Procesu automatizācija
description: Šī tēma sniedz detalizētu informāciju par to, kā procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.
author: RyanCCarlson2
ms.date: 08/12/2020
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
ms.openlocfilehash: 509decec3c3d3b598a2457cddba4896730480ec6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745929"
---
# <a name="process-automation"></a><span data-ttu-id="f34d6-103">Procesu automatizācija</span><span class="sxs-lookup"><span data-stu-id="f34d6-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f34d6-104">Procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.</span><span class="sxs-lookup"><span data-stu-id="f34d6-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="f34d6-105">Ieplānotā darba atjauninātais kalendāra skats ļauj lietotājiem skatīt un rīkoties ar plānoto un pabeigto darbu.</span><span class="sxs-lookup"><span data-stu-id="f34d6-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="f34d6-106">Administrācija</span><span class="sxs-lookup"><span data-stu-id="f34d6-106">Administration</span></span>

<span data-ttu-id="f34d6-107">Centrālā administrēšanas lapa visu procesu automatizācijām ir atrodama Sistēmas administrēšanas modulī, kas atrodas izvēlnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f34d6-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="f34d6-108">Šajā lapā tiks uzskaitīti visi automatizētie procesi (sērijas), kas ir iestatīti sistēmā.</span><span class="sxs-lookup"><span data-stu-id="f34d6-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="f34d6-109">Tas arī ļaus jums pievienot jaunu procesu automatizācijas tieši no šīs lapas.</span><span class="sxs-lookup"><span data-stu-id="f34d6-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="f34d6-110">Pēc sērijas iestatīšanas varat pārvaldīt katru šī saraksta sēriju.</span><span class="sxs-lookup"><span data-stu-id="f34d6-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="f34d6-111">Varat izvēlēties rediģēt visu sēriju, dzēst to, skatīt visus gadījumus saraksta skatā vai atspējot sēriju, ja vēlaties pauzēt plānoto darbu.</span><span class="sxs-lookup"><span data-stu-id="f34d6-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="f34d6-112">Visi procesi, kas ir atspējoti līdzekļu pārvaldībā, netiks rādīti, kad līdzeklis ir atspējots.</span><span class="sxs-lookup"><span data-stu-id="f34d6-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="f34d6-113">Turklāt procesu automatizācijas plānošanas programma neplāno nekādus gadījumus vai fona procesus atspējotam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="f34d6-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="f34d6-114">No jauna iespējojot šo līdzekli, visi ieplānotie gadījumi vai fona procesi pagātnē tiek nekavējoties palaisti.</span><span class="sxs-lookup"><span data-stu-id="f34d6-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="f34d6-115">Kalendāra skats</span><span class="sxs-lookup"><span data-stu-id="f34d6-115">Calendar view</span></span>

<span data-ttu-id="f34d6-116">Viens no procesa automatizācijas galvenajiem ieguvumiem ir iespēja redzēt plānoto darbu vienkāršā kalendāra skatā.</span><span class="sxs-lookup"><span data-stu-id="f34d6-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="f34d6-117">Šis skats ļauj jums skatīt darbu nedēļas laikā.</span><span class="sxs-lookup"><span data-stu-id="f34d6-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="f34d6-118">Šis skats tiks rādīts **Procesa automatizācijas** lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="f34d6-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="f34d6-119">Tas tiks aizpildīts ar atlasītās sērijas ieplānoto darbu.</span><span class="sxs-lookup"><span data-stu-id="f34d6-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="f34d6-120">[![Procesu automatizācijas kalendārs](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="f34d6-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="f34d6-121">Gadījumu izmaiņas</span><span class="sxs-lookup"><span data-stu-id="f34d6-121">Occurrence changes</span></span>

<span data-ttu-id="f34d6-122">Katru gadījumu var modificēt, neietekmējot ar tām izveidoto sēriju definētos citus gadījumus.</span><span class="sxs-lookup"><span data-stu-id="f34d6-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="f34d6-123">Ieplānotā darba gadījumus var rediģēt no kalendāra skata, atlasot pogu **Skatīt/rediģēt** un atlasot **Gadījums**.</span><span class="sxs-lookup"><span data-stu-id="f34d6-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="f34d6-124">Šī lapa ļauj jums piekļūt visiem iestatījumiem, kas sākotnēji tika parādīti sēriju iestatīšanas vednī, un sniedz iespēju atlasītajam gadījumam veikt vienreizējas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="f34d6-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="f34d6-125">Ieplānotā darba gadījumu var izslēgt arī, atlasot pogu **Atspējot** no kalendāra skata.</span><span class="sxs-lookup"><span data-stu-id="f34d6-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="f34d6-126">Izstrādātāja dokumentācija</span><span class="sxs-lookup"><span data-stu-id="f34d6-126">Developer documentation</span></span>

<span data-ttu-id="f34d6-127">Procesu automatizācijas struktūra ļauj izstrādātājiem paplašināt procesu automatizācijas struktūru.</span><span class="sxs-lookup"><span data-stu-id="f34d6-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="f34d6-128">Šī [Procesu automatizācijas struktūras](../process-automation/process-automation-framework.md) dokumentācija sniedz informāciju par to, kā varat izveidot pielāgotus procesus, kas ir nepieciešami, lai palaistu pakešu serveri, kas paredzēts procesu automatizācijas vednim, un automātiski tiek rādīti kalendāra skatā.</span><span class="sxs-lookup"><span data-stu-id="f34d6-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]