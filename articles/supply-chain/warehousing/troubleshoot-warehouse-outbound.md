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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993982"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="f1911-103">Izejošo noliktavas operāciju problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="f1911-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1911-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f1911-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="f1911-105">Tiek parādīts šāds kļūdas ziņojums: "Pārdošanas pasūtījumu nevarēja izlaist."</span><span class="sxs-lookup"><span data-stu-id="f1911-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f1911-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="f1911-106">Issue description</span></span>

<span data-ttu-id="f1911-107">Šī problēma var rasties vairāku iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="f1911-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="f1911-108">Piemēram, pasūtījums ir kredīta pārvaldības aizturēšana, un nevienu sūtījumu nevar izveidot, kamēr nav ievadīta derīga pasta adrese visām pārdošanas rindām, kas ir saistītas ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="f1911-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="f1911-109">Pretējā gadījumā ir paredzēta pasūtījuma aizturēšana, kas jāadresē, lai pasūtījumu varētu nodot izpildei noliktavā.</span><span class="sxs-lookup"><span data-stu-id="f1911-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="f1911-110">Šis aizturējums var būt specifisks pasūtījumam, vai tas var būt klienta kontā.</span><span class="sxs-lookup"><span data-stu-id="f1911-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f1911-111">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="f1911-111">Issue resolution</span></span>

<span data-ttu-id="f1911-112">Pievienojiet vai atjauniniet adresi pārdošanas pasūtījumā un pasūtījuma rindās un pēc tam izlaidiet pasūtījumu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="f1911-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="f1911-113">Pasūtījumus var izlaist noliktavā tikai tad, ja tiem ir derīga piegādes adrese (katram adreses formāta iestatījumam **Organizācijas administrēšanas** modulī).</span><span class="sxs-lookup"><span data-stu-id="f1911-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="f1911-114">Izmeklējiet pasūtījuma aizturēšanu un risināt šos jautājumus.</span><span class="sxs-lookup"><span data-stu-id="f1911-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="f1911-115">Pēc tam noņemiet aizturēšanu no pasūtījuma vai klienta un izlaidiet pasūtījumu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="f1911-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="f1911-116">Tiek saņemts šāds ziņojums: "Sūtījums kravai 1% ir apstiprināts."</span><span class="sxs-lookup"><span data-stu-id="f1911-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="f1911-117">Tomēr neviena rinda netiek grāmatota.</span><span class="sxs-lookup"><span data-stu-id="f1911-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f1911-118">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="f1911-118">Issue description</span></span>

<span data-ttu-id="f1911-119">Sūtījums tika apstiprināts kravā, bet nav notikusi grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="f1911-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f1911-120">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="f1911-120">Issue resolution</span></span>

<span data-ttu-id="f1911-121">Sūtījuma apstiprināšana neietekmē grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="f1911-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="f1911-122">Tas tikai atjaunina sūtījuma un kravas statusu.</span><span class="sxs-lookup"><span data-stu-id="f1911-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="f1911-123">Grāmatošanai jābūt atsevišķā procesā.</span><span class="sxs-lookup"><span data-stu-id="f1911-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="f1911-124">Tiek parādīts šāds kļūdas ziņojums: "Tieša nosūtīšana nevar apstrādāt noliktavas 1%, jo tajā ir iespējota noliktavas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="f1911-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="f1911-125">Lūdzu, norādiet citu noliktavu, kas nav iespējota noliktavas pārvaldībai."</span><span class="sxs-lookup"><span data-stu-id="f1911-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f1911-126">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="f1911-126">Issue description</span></span>

<span data-ttu-id="f1911-127">Krājums tiek pievienots pārdošanas rindai tiešajai piegādei no noliktavas, kas ir aktivizēta noliktavas pārvaldībai (WMS).</span><span class="sxs-lookup"><span data-stu-id="f1911-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="f1911-128">Šis kļūdas ziņojums tiek parādīts, atjauninot pārdošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="f1911-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="f1911-129">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="f1911-129">Issue resolution</span></span>

<span data-ttu-id="f1911-130">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="f1911-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f1911-131">Pašlaik WMS neatbalsta tiešo piegādi.</span><span class="sxs-lookup"><span data-stu-id="f1911-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="f1911-132">Tāpēc, lai izmantotu tiešo piegādi, jāatlasa WMS krājums un noliktava.</span><span class="sxs-lookup"><span data-stu-id="f1911-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
