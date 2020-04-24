---
title: Jauktas noliktavas vienības saņemšana
description: Šajā tēmā ir aprakstīts, kā lietot jauktas noliktavas vienības saņemšanu, lai reģistrētu un izveidotu darbu vairākiem krājumiem, izmantojot mobilo ierīci.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215773"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="12043-103">Jauktas noliktavas vienības saņemšana</span><span class="sxs-lookup"><span data-stu-id="12043-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12043-104">Jauktas noliktavas vienības saņemšana jums ļauj izveidot noliktavas vienību, kas sastāv no vairākiem krājumiem, pirms reģistrējat un izveidojat izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="12043-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="12043-105">Noliktavas vienība, kas sastāv no vairākiem krājumiem, saņemšanas dokā nav jāsadala, lai jūs varētu reģistrēt katru krājumu.</span><span class="sxs-lookup"><span data-stu-id="12043-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="12043-106">Ja pirmdokumenta rindu identificēšanai izmantojat ar krājumu saistītu plūsmu, krājuma kontrolē varat skenēt svītrkodus.</span><span class="sxs-lookup"><span data-stu-id="12043-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="12043-107">Ja šim svītrkodam ir konfigurēts daudzums un mērvienība (unit of measure — UOM), tad krājums un daudzums tiek automātiski pievienots jauktajai noliktavas vienībai, un jūs tiekat pārcelts atpakaļ ekrānā, lai skenētu citu krājumu.</span><span class="sxs-lookup"><span data-stu-id="12043-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="12043-108">Šādi jūs varat ātri skenēt visus krājumus un nav nepieciešams apstiprināt katru darbību.</span><span class="sxs-lookup"><span data-stu-id="12043-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="12043-109">Jauktas noliktavas vienības saņemšana plūsmā varat parādīt sarakstu ar krājumiem, kas jau ir ieskenēti šai noliktavas vienībai, un no šejienes varat modificēt vai labot krājuma daudzumu.</span><span class="sxs-lookup"><span data-stu-id="12043-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="12043-110">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="12043-110">Where it applies</span></span>

<span data-ttu-id="12043-111">Jauktās noliktavas vienības saņemšana ir mobilās ierīces saņemšanas plūsma, kas paredzēta, lai vienlaicīgi reģistrētu un izveidotu darbu vairākām rindām/krājumiem.</span><span class="sxs-lookup"><span data-stu-id="12043-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="12043-112">Tas noder, ja saņemat ienākošas noliktavas vienības ar vairākiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="12043-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="12043-113">Kā iestatīt jaukto noliktavas vienību saņemšanu</span><span class="sxs-lookup"><span data-stu-id="12043-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="12043-114">Jauktās noliktavas vienības saņemšana tiek iestatīta kā mobilās ierīces izvēlnes vienums.</span><span class="sxs-lookup"><span data-stu-id="12043-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="12043-115">Ir jāizveido jauns izvēlnes vienums ar režīma darbu, kas neizmanto pastāvošu darbu, bet izmanto vienu no tālāk norādītajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="12043-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="12043-116">Jauktas noliktavas vienības saņemšana</span><span class="sxs-lookup"><span data-stu-id="12043-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="12043-117">Jaukto noliktavas vienību saņemšana un izvietošana</span><span class="sxs-lookup"><span data-stu-id="12043-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="12043-118">Pirmdokumenta rindu identificēšanas opcijas ir pirkšanas pasūtījuma krājums, pirkšanas pasūtījuma rinda, atgriešanas pasūtījums, pārsūtīšanas pasūtījuma krājums un pārsūtīšanas pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="12043-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="12043-119">Šīs opcijas varat mainīt saņemšanas secību atsevišķā noliktavas vienībā.</span><span class="sxs-lookup"><span data-stu-id="12043-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="12043-120">Pēdējā opcija ir pēc kravas krājuma.</span><span class="sxs-lookup"><span data-stu-id="12043-120">The last option is by load item.</span></span> <span data-ttu-id="12043-121">Var pievienot vairākus krājumus vienai noliktavas vienībai, bet nevar pārslēgties starp vairākām kravām.</span><span class="sxs-lookup"><span data-stu-id="12043-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
