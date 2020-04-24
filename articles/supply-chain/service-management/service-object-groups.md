---
title: Pakalpojumu objektu grupas
description: Objektu grupas ir noderīgas, ja pārskata izveides nolūkos vai statistikas nolūkos ir jāveic objektu datu sakārtošana vai filtrēšana.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca1ca177fe7048e5ff37a8058d00face4a8166f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215106"
---
# <a name="service-object-groups"></a><span data-ttu-id="9fa87-103">Pakalpojumu objektu grupas</span><span class="sxs-lookup"><span data-stu-id="9fa87-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fa87-104">Objektu grupas ir noderīgas, ja pārskata izveides nolūkos vai statistikas nolūkos ir jāveic objektu datu sakārtošana vai filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="9fa87-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="9fa87-105">Piemēram, varat grupēt objektus pēc ģeogrāfiskās atrašanās vietas vai pēc tipa.</span><span class="sxs-lookup"><span data-stu-id="9fa87-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="9fa87-106">Grupēt pēc ģeogrāfiskās atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="9fa87-106">Group by geographical location</span></span>

<span data-ttu-id="9fa87-107">Varat izmantot šo grupēšanas metodi, lai norādītu dažādu jūsu uzņēmuma apkalpoto objektu atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="9fa87-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="9fa87-108">Objektu grupēšana pēc ģeogrāfiskās atrašanās vietas ir noderīga, ja ir jānorāda objekti, kuriem jūsu uzņēmums jau nodrošina pakalpojumus noteiktajā valstī/reģionā.</span><span class="sxs-lookup"><span data-stu-id="9fa87-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="9fa87-109">Piemērs</span><span class="sxs-lookup"><span data-stu-id="9fa87-109">Example</span></span>

<span data-ttu-id="9fa87-110">Klients no Beļģijas sazinās ar jūsu apkalpošanas centru un vēlas noslēgt pakalpojumu līgumu attiecībā uz objektu ABC.</span><span class="sxs-lookup"><span data-stu-id="9fa87-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="9fa87-111">Visiem Beļģijā apkalpotajiem objektiem esat pievienojis ģeogrāfiskās atrašanās vietas objektu grupu Beļģija.</span><span class="sxs-lookup"><span data-stu-id="9fa87-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="9fa87-112">Lietojot šo grupu kā filtru, varat ātri noskaidrot, vai jūsu programmā jau pastāv ieraksts par ABC objektu vai jums būs jāizveido šis ieraksts no jauna.</span><span class="sxs-lookup"><span data-stu-id="9fa87-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="9fa87-113">Grupēt pēc tipa</span><span class="sxs-lookup"><span data-stu-id="9fa87-113">Group by type</span></span>

<span data-ttu-id="9fa87-114">Šo grupēšanas metodi varat izmantot, lai parādītu, kuriem objektu tipiem jūsu uzņēmums nodrošina pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="9fa87-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="9fa87-115">Objektu grupēšana pēc tipiem var būt noderīga arī tajos gadījumos, ja, piemēram, programmā vēlaties izveidot jaunu objektu, pamatojoties uz lietojumprogrammā esošo objektu, vai arī objektu, kas ir līdzīgs jau esošajam objektam.</span><span class="sxs-lookup"><span data-stu-id="9fa87-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="9fa87-116">Piemērs</span><span class="sxs-lookup"><span data-stu-id="9fa87-116">Example</span></span>

<span data-ttu-id="9fa87-117">Klients sazinās ar jūsu apkalpošanas centru un vēlas noslēgt pakalpojumu līgumu attiecībā uz gaisa kondicionēšanas iekārtu HIJ.</span><span class="sxs-lookup"><span data-stu-id="9fa87-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="9fa87-118">Jums vēl nav ieraksta par šo iekārtu.</span><span class="sxs-lookup"><span data-stu-id="9fa87-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="9fa87-119">Tomēr esat iestatījis objektu grupu ar nosaukumu Gaisa kondicionētāji un pievienojis šo grupu visiem gaisa kondicionēšanas objektiem.</span><span class="sxs-lookup"><span data-stu-id="9fa87-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="9fa87-120">Tāpēc varat ātri sameklēt un identificēt visas pārējas gaisa kondicionēšanas iekārtas un izmantot šo objektu veidnēs esošo informāciju, lai izveidotu HIJ iekārtai paredzētas pakalpojumu līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="9fa87-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="9fa87-121">Šādi izmantojot objektu grupas, varat ātri iestatīt jaunus objektus un noteikt, kādi pakalpojuma uzdevumi ir jāveic šiem objektiem.</span><span class="sxs-lookup"><span data-stu-id="9fa87-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="9fa87-122">Pakalpojumu objektu grupu izveide</span><span class="sxs-lookup"><span data-stu-id="9fa87-122">Create service object groups</span></span>

<span data-ttu-id="9fa87-123">Izveidojiet grupas, kurām varat piešķirt pakalpojumu objektus.</span><span class="sxs-lookup"><span data-stu-id="9fa87-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="9fa87-124">Pakalpojumu objekti ir krājumu vienības un citi produkti, saistībā ar kuriem tiek sniegti pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="9fa87-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="9fa87-125">Grupējot pakalpojumu objektus, var izveidot pārskatus par līdzīgiem un saistītiem pakalpojumu objektiem.</span><span class="sxs-lookup"><span data-stu-id="9fa87-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="9fa87-126">Piemēram, pakalpojumu objektu grupu ver veidot divi divi pakalpojumu objekti: viens pakalpojuma objekts ir komplekts un otrs pakalpojuma objekts ir komplekta instalēšanas pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="9fa87-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="9fa87-127">Lai izveidotu pakalpojumu objektu grupas, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="9fa87-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="9fa87-128">Noklikšķiniet uz **Pakalpojumu pārvaldība > Iestatīšana > Pakalpojumu objekti > Pakalpojumu objektu grupas**.</span><span class="sxs-lookup"><span data-stu-id="9fa87-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="9fa87-129">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu pakalpojuma objektu grupu.</span><span class="sxs-lookup"><span data-stu-id="9fa87-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="9fa87-130">Ievadiet pakalpojumu objekta grupai unikālu nosaukumu un, ja vēlaties, arī aprakstu.</span><span class="sxs-lookup"><span data-stu-id="9fa87-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="9fa87-131">Varat grupai piešķirt pakalpojumu objektus, izmantojot formu **Pakalpojumu objekti**.</span><span class="sxs-lookup"><span data-stu-id="9fa87-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="9fa87-132">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="9fa87-132">See also</span></span>

[<span data-ttu-id="9fa87-133">Pakalpojumu objektu izveide</span><span class="sxs-lookup"><span data-stu-id="9fa87-133">Create service objects</span></span>](create-service-objects.md)


