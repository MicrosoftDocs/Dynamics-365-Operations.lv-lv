---
title: Procesu automatizācija
description: Šī tēma sniedz detalizētu informāciju par to, kā procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508189"
---
# <a name="process-automation"></a><span data-ttu-id="299fb-103">Procesu automatizācija</span><span class="sxs-lookup"><span data-stu-id="299fb-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="299fb-104">Procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.</span><span class="sxs-lookup"><span data-stu-id="299fb-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="299fb-105">Ieplānotā darba atjauninātais kalendāra skats ļauj lietotājiem skatīt un rīkoties ar plānoto un pabeigto darbu.</span><span class="sxs-lookup"><span data-stu-id="299fb-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="299fb-106">Administrācija</span><span class="sxs-lookup"><span data-stu-id="299fb-106">Administration</span></span>

<span data-ttu-id="299fb-107">Centrālā administrēšanas lapa visu procesu automatizācijām ir atrodama Sistēmas administrēšanas modulī, kas atrodas izvēlnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="299fb-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="299fb-108">Šajā lapā tiks uzskaitīti visi automatizētie procesi (sērijas), kas ir iestatīti sistēmā.</span><span class="sxs-lookup"><span data-stu-id="299fb-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="299fb-109">Tas arī ļaus jums pievienot jaunu procesu automatizācijas tieši no šīs lapas.</span><span class="sxs-lookup"><span data-stu-id="299fb-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="299fb-110">Pēc sērijas iestatīšanas varat pārvaldīt katru šī saraksta sēriju.</span><span class="sxs-lookup"><span data-stu-id="299fb-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="299fb-111">Varat izvēlēties rediģēt visu sēriju, dzēst to, skatīt visus gadījumus saraksta skatā vai atspējot sēriju, ja vēlaties pauzēt plānoto darbu laika periodā.</span><span class="sxs-lookup"><span data-stu-id="299fb-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="299fb-112">Kalendāra skats</span><span class="sxs-lookup"><span data-stu-id="299fb-112">Calendar view</span></span> 
<span data-ttu-id="299fb-113">Viens no procesa automatizācijas galvenajiem ieguvumiem ir iespēja redzēt plānoto darbu vienkāršā kalendāra skatā.</span><span class="sxs-lookup"><span data-stu-id="299fb-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="299fb-114">Šis skats ļauj jums skatīt darbu nedēļas laikā.</span><span class="sxs-lookup"><span data-stu-id="299fb-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="299fb-115">Šis skats tiks rādīts **Procesa automatizācijas** lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="299fb-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="299fb-116">Tas tiks aizpildīts ar atlasītās sērijas ieplānoto darbu.</span><span class="sxs-lookup"><span data-stu-id="299fb-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="299fb-117">[![Procesu automatizācijas kalendārs](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="299fb-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="299fb-118">Gadījumu izmaiņas</span><span class="sxs-lookup"><span data-stu-id="299fb-118">Occurrence changes</span></span>
<span data-ttu-id="299fb-119">Katru gadījumu var modificēt, neietekmējot ar tām izveidoto sēriju definētos citus gadījumus.</span><span class="sxs-lookup"><span data-stu-id="299fb-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="299fb-120">Ieplānotā darba gadījumus var rediģēt no kalendāra skata, atlasot pogu **Skatīt/rediģēt** un atlasot **Gadījums**.</span><span class="sxs-lookup"><span data-stu-id="299fb-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="299fb-121">Tas ļauj jums piekļūt visiem iestatījumiem, kas sākotnēji tika parādīti sēriju iestatīšanas vednī, un sniedz iespēju atlasītajam gadījumam veikt vienreizējas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="299fb-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="299fb-122">Ieplānotā darba gadījumu var izslēgt arī, atlasot pogu **Atspējot** no kalendāra skata.</span><span class="sxs-lookup"><span data-stu-id="299fb-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="299fb-123">Izstrādātāja dokumentācija</span><span class="sxs-lookup"><span data-stu-id="299fb-123">Developer documentation</span></span> 
<span data-ttu-id="299fb-124">Izstrādātāja dokumentācija pašlaik tiek rakstīta, lai izstrādātājiem ļautu paplašināt procesu automatizācijas struktūru.</span><span class="sxs-lookup"><span data-stu-id="299fb-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="299fb-125">Šī dokumentācija sniegs informāciju par to, kā varat izveidot pielāgotus procesus, kas ir nepieciešami, lai palaistu pakešu serveris, kas paredzēts procesu automatizācijas vednim, un automātiski tiek rādīti kalendāra skatā.</span><span class="sxs-lookup"><span data-stu-id="299fb-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
