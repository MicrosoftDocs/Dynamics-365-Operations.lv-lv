---
title: Izejošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 919b6f433db47f24adc9a474942557a1467d1f71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828182"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="6e572-103">Izejošo noliktavas operāciju problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="6e572-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e572-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6e572-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="6e572-105">Tiek parādīts šāds kļūdas ziņojums: "Pārdošanas pasūtījumu nevarēja izlaist."</span><span class="sxs-lookup"><span data-stu-id="6e572-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e572-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="6e572-106">Issue description</span></span>

<span data-ttu-id="6e572-107">Šī problēma var rasties vairāku iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="6e572-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="6e572-108">Piemēram, pasūtījums ir kredīta pārvaldības aizturēšana, un nevienu sūtījumu nevar izveidot, kamēr nav ievadīta derīga pasta adrese visām pārdošanas rindām, kas ir saistītas ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="6e572-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="6e572-109">Pretējā gadījumā ir paredzēta pasūtījuma aizturēšana, kas jāadresē, lai pasūtījumu varētu nodot izpildei noliktavā.</span><span class="sxs-lookup"><span data-stu-id="6e572-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="6e572-110">Šis aizturējums var būt specifisks pasūtījumam, vai tas var būt klienta kontā.</span><span class="sxs-lookup"><span data-stu-id="6e572-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e572-111">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="6e572-111">Issue resolution</span></span>

<span data-ttu-id="6e572-112">Pievienojiet vai atjauniniet adresi pārdošanas pasūtījumā un pasūtījuma rindās un pēc tam izlaidiet pasūtījumu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6e572-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="6e572-113">Pasūtījumus var izlaist noliktavā tikai tad, ja tiem ir derīga piegādes adrese (katram adreses formāta iestatījumam **Organizācijas administrēšanas** modulī).</span><span class="sxs-lookup"><span data-stu-id="6e572-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="6e572-114">Izmeklējiet pasūtījuma aizturēšanu un risināt šos jautājumus.</span><span class="sxs-lookup"><span data-stu-id="6e572-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="6e572-115">Pēc tam noņemiet aizturēšanu no pasūtījuma vai klienta un izlaidiet pasūtījumu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6e572-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="6e572-116">Tiek saņemts šāds ziņojums: "Sūtījums kravai 1% ir apstiprināts."</span><span class="sxs-lookup"><span data-stu-id="6e572-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="6e572-117">Tomēr neviena rinda netiek grāmatota.</span><span class="sxs-lookup"><span data-stu-id="6e572-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e572-118">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="6e572-118">Issue description</span></span>

<span data-ttu-id="6e572-119">Sūtījums tika apstiprināts kravā, bet nav notikusi grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="6e572-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e572-120">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="6e572-120">Issue resolution</span></span>

<span data-ttu-id="6e572-121">Sūtījuma apstiprināšana neietekmē grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="6e572-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="6e572-122">Tas tikai atjaunina sūtījuma un kravas statusu.</span><span class="sxs-lookup"><span data-stu-id="6e572-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="6e572-123">Grāmatošanai jābūt atsevišķā procesā.</span><span class="sxs-lookup"><span data-stu-id="6e572-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="6e572-124">Tiek parādīts šāds kļūdas ziņojums: "Tieša nosūtīšana nevar apstrādāt noliktavas 1%, jo tajā ir iespējota noliktavas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="6e572-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="6e572-125">Lūdzu, norādiet citu noliktavu, kas nav iespējota noliktavas pārvaldībai."</span><span class="sxs-lookup"><span data-stu-id="6e572-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e572-126">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="6e572-126">Issue description</span></span>

<span data-ttu-id="6e572-127">Krājums tiek pievienots pārdošanas rindai tiešajai piegādei no noliktavas, kas ir aktivizēta noliktavas pārvaldībai (WMS).</span><span class="sxs-lookup"><span data-stu-id="6e572-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="6e572-128">Šis kļūdas ziņojums tiek parādīts, atjauninot pārdošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="6e572-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="6e572-129">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="6e572-129">Issue resolution</span></span>

<span data-ttu-id="6e572-130">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="6e572-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="6e572-131">Pašlaik WMS neatbalsta tiešo piegādi.</span><span class="sxs-lookup"><span data-stu-id="6e572-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="6e572-132">Tāpēc, lai izmantotu tiešo piegādi, jāatlasa WMS krājums un noliktava.</span><span class="sxs-lookup"><span data-stu-id="6e572-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]