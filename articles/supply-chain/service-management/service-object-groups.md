---
title: Pakalpojumu objektu grupas
description: "Objektu grupas ir noderīgas, ja pārskata izveides nolūkos vai statistikas nolūkos ir jāveic objektu datu sakārtošana vai filtrēšana."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: lv-lv
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="cd50d-103">Pakalpojumu objektu grupas</span><span class="sxs-lookup"><span data-stu-id="cd50d-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd50d-104">Objektu grupas ir noderīgas, ja pārskata izveides nolūkos vai statistikas nolūkos ir jāveic objektu datu sakārtošana vai filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="cd50d-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="cd50d-105">Piemēram, varat grupēt objektus pēc ģeogrāfiskās atrašanās vietas vai pēc tipa.</span><span class="sxs-lookup"><span data-stu-id="cd50d-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="cd50d-106">Grupēt pēc ģeogrāfiskās atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="cd50d-106">Group by geographical location</span></span>

<span data-ttu-id="cd50d-107">Varat izmantot šo grupēšanas metodi, lai norādītu dažādu jūsu uzņēmuma apkalpoto objektu atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="cd50d-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="cd50d-108">Objektu grupēšana pēc ģeogrāfiskās atrašanās vietas ir noderīga, ja ir jānorāda objekti, kuriem jūsu uzņēmums jau nodrošina pakalpojumus noteiktajā valstī/reģionā.</span><span class="sxs-lookup"><span data-stu-id="cd50d-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="cd50d-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="cd50d-109">Example</span></span>

<span data-ttu-id="cd50d-110">Klients no Beļģijas sazinās ar jūsu apkalpošanas centru un vēlas noslēgt pakalpojumu līgumu attiecībā uz objektu ABC.</span><span class="sxs-lookup"><span data-stu-id="cd50d-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="cd50d-111">Visiem Beļģijā apkalpotajiem objektiem esat pievienojis ģeogrāfiskās atrašanās vietas objektu grupu Beļģija.</span><span class="sxs-lookup"><span data-stu-id="cd50d-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="cd50d-112">Lietojot šo grupu kā filtru, varat ātri noskaidrot, vai jūsu programmā jau pastāv ieraksts par ABC objektu vai jums būs jāizveido šis ieraksts no jauna.</span><span class="sxs-lookup"><span data-stu-id="cd50d-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="cd50d-113">Grupēt pēc tipa</span><span class="sxs-lookup"><span data-stu-id="cd50d-113">Group by type</span></span>

<span data-ttu-id="cd50d-114">Šo grupēšanas metodi varat izmantot, lai parādītu, kuriem objektu tipiem jūsu uzņēmums nodrošina pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="cd50d-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="cd50d-115">Objektu grupēšana pēc tipiem var būt noderīga arī tajos gadījumos, ja, piemēram, programmā vēlaties izveidot jaunu objektu, pamatojoties uz lietojumprogrammā esošo objektu, vai arī objektu, kas ir līdzīgs jau esošajam objektam.</span><span class="sxs-lookup"><span data-stu-id="cd50d-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="cd50d-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="cd50d-116">Example</span></span>

<span data-ttu-id="cd50d-117">Klients sazinās ar jūsu apkalpošanas centru un vēlas noslēgt pakalpojumu līgumu attiecībā uz gaisa kondicionēšanas iekārtu HIJ.</span><span class="sxs-lookup"><span data-stu-id="cd50d-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="cd50d-118">Jums vēl nav ieraksta par šo iekārtu.</span><span class="sxs-lookup"><span data-stu-id="cd50d-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="cd50d-119">Tomēr esat iestatījis objektu grupu ar nosaukumu Gaisa kondicionētāji un pievienojis šo grupu visiem gaisa kondicionēšanas objektiem.</span><span class="sxs-lookup"><span data-stu-id="cd50d-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="cd50d-120">Tāpēc varat ātri sameklēt un identificēt visas pārējas gaisa kondicionēšanas iekārtas un izmantot šo objektu veidnēs esošo informāciju, lai izveidotu HIJ iekārtai paredzētas pakalpojumu līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="cd50d-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="cd50d-121">Šādi izmantojot objektu grupas, varat ātri iestatīt jaunus objektus un noteikt, kādi pakalpojuma uzdevumi ir jāveic šiem objektiem.</span><span class="sxs-lookup"><span data-stu-id="cd50d-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




