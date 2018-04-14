---
title: Pakalpojumu objekti
description: "Pakalpojumu objekti ir klienta līdzekļi un preces, kurām jūs varat veikt pakalpojumu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0f7b63393085858c5ff4c64ebdf5d64b3c3ccdef
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="service-objects"></a><span data-ttu-id="6a05e-103">Pakalpojumu objekti</span><span class="sxs-lookup"><span data-stu-id="6a05e-103">Service objects</span></span> 

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6a05e-104">Pakalpojumu objekti ir klienta līdzekļi un preces, kurām jūs varat veikt pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="6a05e-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="6a05e-105">Atkarībā no sniegtā pakalpojuma tipa, objekti var būt materiāli vai nemateriāli:</span><span class="sxs-lookup"><span data-stu-id="6a05e-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="6a05e-106">Taustāmie objekti ir lietas, piem., mašīnas vai ēkas, kurām variet veikt fiziskas apkalpošanas uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="6a05e-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="6a05e-107">Materiāls pakalpojuma objekts var būt arī krājuma vienība, kuru izveidojat veidlapā Nodoto preču papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="6a05e-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="6a05e-108">Atkarībā no krājumu dimensijas grupas, kuras pievienojat prece, varat radīt pakalpojuma objektu, kura detalizācijas līmenī ir iekļauts preces sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="6a05e-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="6a05e-109">Tas ir noderīgi, ja ir jāizseko konkrēta prece, kuru pārstāv pakalpojuma objekts.</span><span class="sxs-lookup"><span data-stu-id="6a05e-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="6a05e-110">Materiāls pakalpojuma objekts var būt arī prece, kura ir netieši saistīta ar kompānijas tiešo produkciju vai piegādes ķēdi.</span><span class="sxs-lookup"><span data-stu-id="6a05e-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="6a05e-111">Piemēram, rīku komplekts, kas tiek izmantots remontdarbiem, pakalpojuma pasūtījumā var būt, piemēram, pakalpojuma objekts, kas nav iekļauts krājumos.</span><span class="sxs-lookup"><span data-stu-id="6a05e-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="6a05e-112">Šajā gadījumā tas netiek reģistrēts kā krājuma vienība.</span><span class="sxs-lookup"><span data-stu-id="6a05e-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="6a05e-113">Nemateriāli objekti ir abstraktas lietas, piemēram konti komplekts vai juridisks dokuments, kurā varat izpildīt pakalpojuma uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="6a05e-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="6a05e-114">Nemateriāla pakalpojuma objekta paraugs</span><span class="sxs-lookup"><span data-stu-id="6a05e-114">Example of an intangible service object</span></span>

<span data-ttu-id="6a05e-115">Uzņēmums A uztur finanšu ierakstus vairākiem maziem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="6a05e-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="6a05e-116">Viens no kompānijas A klientiem ir vietējā futbola komanda, kurai kompānija A reizi nedēļā veic grāmatvedības darbus un ikgadēja kluba kontu revīziju.</span><span class="sxs-lookup"><span data-stu-id="6a05e-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="6a05e-117">Kluba konti ir iestatīti veidlapā Pakalpojumu objekti un noteikti kā pakalpojumu līguma objekts.</span><span class="sxs-lookup"><span data-stu-id="6a05e-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="6a05e-118">Pastāv divas objekta pakalpojumu līgumu līnijas.</span><span class="sxs-lookup"><span data-stu-id="6a05e-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="6a05e-119">1. līnija ir iknedēļas grāmatvedība ar līnijai piešķirto nedēļas intervālu, un 2. līnija ir ikgadēja revīzija ar tai piešķirto gada intervālu.</span><span class="sxs-lookup"><span data-stu-id="6a05e-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a05e-120">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="6a05e-120">Related topics</span></span>

[<span data-ttu-id="6a05e-121">Pakalpojumu objektu izveide</span><span class="sxs-lookup"><span data-stu-id="6a05e-121">Create service objects</span></span>](create-service-objects.md)


