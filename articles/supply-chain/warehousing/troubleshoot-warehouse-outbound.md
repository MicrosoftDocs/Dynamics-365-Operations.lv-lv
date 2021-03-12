---
title: Izejošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645457"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="5025d-103">Izejošo noliktavas operāciju problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="5025d-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5025d-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5025d-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="5025d-105">Tiek parādīts šāds kļūdas ziņojums: "Pārdošanas pasūtījumu nevarēja izlaist."</span><span class="sxs-lookup"><span data-stu-id="5025d-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5025d-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5025d-106">Issue description</span></span>

<span data-ttu-id="5025d-107">Šī problēma var rasties vairāku iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="5025d-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="5025d-108">Piemēram, pasūtījums ir kredīta pārvaldības aizturēšana, un nevienu sūtījumu nevar izveidot, kamēr nav ievadīta derīga pasta adrese visām pārdošanas rindām, kas ir saistītas ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5025d-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="5025d-109">Pretējā gadījumā ir paredzēta pasūtījuma aizturēšana, kas jāadresē, lai pasūtījumu varētu nodot izpildei noliktavā.</span><span class="sxs-lookup"><span data-stu-id="5025d-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="5025d-110">Šis aizturējums var būt specifisks pasūtījumam, vai tas var būt klienta kontā.</span><span class="sxs-lookup"><span data-stu-id="5025d-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5025d-111">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5025d-111">Issue resolution</span></span>

<span data-ttu-id="5025d-112">Pievienojiet vai atjauniniet adresi pārdošanas pasūtījumā un pasūtījuma rindās un pēc tam izlaidiet pasūtījumu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5025d-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="5025d-113">Pasūtījumus var izlaist noliktavā tikai tad, ja tiem ir derīga piegādes adrese (katram adreses formāta iestatījumam **Organizācijas administrēšanas** modulī).</span><span class="sxs-lookup"><span data-stu-id="5025d-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="5025d-114">Izmeklējiet pasūtījuma aizturēšanu un risināt šos jautājumus.</span><span class="sxs-lookup"><span data-stu-id="5025d-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="5025d-115">Pēc tam noņemiet aizturēšanu no pasūtījuma vai klienta un izlaidiet pasūtījumu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5025d-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="5025d-116">Tiek saņemts šāds ziņojums: "Sūtījums kravai 1% ir apstiprināts."</span><span class="sxs-lookup"><span data-stu-id="5025d-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="5025d-117">Tomēr neviena rinda netiek grāmatota.</span><span class="sxs-lookup"><span data-stu-id="5025d-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5025d-118">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5025d-118">Issue description</span></span>

<span data-ttu-id="5025d-119">Sūtījums tika apstiprināts kravā, bet nav notikusi grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="5025d-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5025d-120">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5025d-120">Issue resolution</span></span>

<span data-ttu-id="5025d-121">Sūtījuma apstiprināšana neietekmē grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="5025d-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="5025d-122">Tas tikai atjaunina sūtījuma un kravas statusu.</span><span class="sxs-lookup"><span data-stu-id="5025d-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="5025d-123">Grāmatošanai jābūt atsevišķā procesā.</span><span class="sxs-lookup"><span data-stu-id="5025d-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="5025d-124">Tiek parādīts šāds kļūdas ziņojums: "Tieša nosūtīšana nevar apstrādāt noliktavas 1%, jo tajā ir iespējota noliktavas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="5025d-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="5025d-125">Lūdzu, norādiet citu noliktavu, kas nav iespējota noliktavas pārvaldībai."</span><span class="sxs-lookup"><span data-stu-id="5025d-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5025d-126">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5025d-126">Issue description</span></span>

<span data-ttu-id="5025d-127">Krājums tiek pievienots pārdošanas rindai tiešajai piegādei no noliktavas, kas ir aktivizēta noliktavas pārvaldībai (WMS).</span><span class="sxs-lookup"><span data-stu-id="5025d-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="5025d-128">Šis kļūdas ziņojums tiek parādīts, atjauninot pārdošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="5025d-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="5025d-129">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5025d-129">Issue resolution</span></span>

<span data-ttu-id="5025d-130">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="5025d-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="5025d-131">Pašlaik WMS neatbalsta tiešo piegādi.</span><span class="sxs-lookup"><span data-stu-id="5025d-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="5025d-132">Tāpēc, lai izmantotu tiešo piegādi, jāatlasa WMS krājums un noliktava.</span><span class="sxs-lookup"><span data-stu-id="5025d-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>