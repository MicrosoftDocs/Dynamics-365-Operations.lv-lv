---
title: Ienākošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250886"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="8575f-103">Ienākošo noliktavas operāciju problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="8575f-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8575f-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8575f-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="8575f-105">Tiek parādīts šāds kļūdas ziņojums: "Kvalitātes pasūtījums %1 ir ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="8575f-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="8575f-106">Klastera profilu nevarēja atrast, lūdzu, pārbaudiet savu konfigurāciju."</span><span class="sxs-lookup"><span data-stu-id="8575f-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8575f-107">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8575f-107">Issue description</span></span>

<span data-ttu-id="8575f-108">Šis kļūdas ziņojums ir saistīts ar saņemšanas procesu, kurā ir ieslēgta kvalitātes pārvaldība (QMS).</span><span class="sxs-lookup"><span data-stu-id="8575f-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="8575f-109">Atkarībā no konfigurācijas jūsu vidē papildu detaļas par transakciju, kas ģenerē kļūdas ziņojumu, var palīdzēt novērst šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="8575f-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8575f-110">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8575f-110">Issue resolution</span></span>

<span data-ttu-id="8575f-111">Vispirms pārskatiet [klastera izdošanas](set-up-cluster-picking.md) iestatījumu un pārliecinieties, ka klasteru profili ir pareizi iestatīti.</span><span class="sxs-lookup"><span data-stu-id="8575f-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="8575f-112">Klastera izdošanai nevar izmantot mobilās ierīces izvēlnes vienumu, ja vien nav iestatīti klasteru profili.</span><span class="sxs-lookup"><span data-stu-id="8575f-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="8575f-113">Atkarībā no jūsu vides, iespējams, būs jāpārskata arī citas saistītās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="8575f-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="8575f-114">Jauktā numura zīmes saņemšana nestrādā nevienam izvietojuma kodam, izņemot Kredītu.</span><span class="sxs-lookup"><span data-stu-id="8575f-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8575f-115">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8575f-115">Issue description</span></span>

<span data-ttu-id="8575f-116">Kad **Darbības** lauks izvietojuma kodam ir iestatīts kā *Kredīts* vai *Brāķis*, varat izmantot tikai [Jaukto numura zīmes saņemšanas](mixed-license-plate-receiving.md) izvēlnes elementu, lai apstrādātu atgrieztos krājumus.</span><span class="sxs-lookup"><span data-stu-id="8575f-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8575f-117">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8575f-117">Issue resolution</span></span>

<span data-ttu-id="8575f-118">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="8575f-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="8575f-119">Pašlaik tikai [izvietojuma kodi](../service-management/set-up-disposition-codes.md), kuros **Darbības** lauks ir iestatīts kā *Kredīts* vai *Brāķis*, tiek atbalstīts jauktai numura zīmes saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="8575f-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="8575f-120">Palaižot atjaunināt produktu ieejas plūsmas periodisko uzdevumu, neapstiprinātie pirkšanas pasūtījumi tiek apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="8575f-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8575f-121">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8575f-121">Issue description</span></span>

<span data-ttu-id="8575f-122">Pēc tam, kad esat palaidis *Atjaunināt preču ieejas plūsmu* periodisko uzdevumu, sistēma automātiski apstiprina neapstiprinātos pirkšanas pasūtījumus, kuriem ir krājuma darbības statuss *Reģistrēts*.</span><span class="sxs-lookup"><span data-stu-id="8575f-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8575f-123">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8575f-123">Issue resolution</span></span>

<span data-ttu-id="8575f-124">Jauna ienākošo kravu apstrādes funkcija *Pārsniedzot kravas daudzumu* izlabo šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="8575f-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="8575f-125">Lai ieslēgtu šo funkciju, dodieties uz [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet tālāk norādītos līdzekļus (minētajā secībā):</span><span class="sxs-lookup"><span data-stu-id="8575f-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="8575f-126">Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu</span><span class="sxs-lookup"><span data-stu-id="8575f-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="8575f-127">Noslodzes daudzumu pārmērīga saņemšana</span><span class="sxs-lookup"><span data-stu-id="8575f-127">Over receipt of load quantities</span></span>

<span data-ttu-id="8575f-128">Lai iegūtu papildu informāciju, skatiet [Reģistrēto preču daudzumu grāmatošana uz pirkšanas pasūtījumiem](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="8575f-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]