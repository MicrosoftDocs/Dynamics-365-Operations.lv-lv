---
title: Ienākošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920991"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="4e1ea-103">Ienākošo noliktavas operāciju problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="4e1ea-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e1ea-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="4e1ea-105">Tiek parādīts šāds kļūdas ziņojums: "Kvalitātes pasūtījums %1 ir ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="4e1ea-106">Klastera profilu nevarēja atrast, lūdzu, pārbaudiet savu konfigurāciju."</span><span class="sxs-lookup"><span data-stu-id="4e1ea-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e1ea-107">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="4e1ea-107">Issue description</span></span>

<span data-ttu-id="4e1ea-108">Šis kļūdas ziņojums ir saistīts ar saņemšanas procesu, kurā ir ieslēgta kvalitātes pārvaldība (QMS).</span><span class="sxs-lookup"><span data-stu-id="4e1ea-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="4e1ea-109">Atkarībā no konfigurācijas jūsu vidē papildu detaļas par transakciju, kas ģenerē kļūdas ziņojumu, var palīdzēt novērst šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e1ea-110">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="4e1ea-110">Issue resolution</span></span>

<span data-ttu-id="4e1ea-111">Vispirms pārskatiet [klastera izdošanas](set-up-cluster-picking.md) iestatījumu un pārliecinieties, ka klasteru profili ir pareizi iestatīti.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="4e1ea-112">Klastera izdošanai nevar izmantot mobilās ierīces izvēlnes vienumu, ja vien nav iestatīti klasteru profili.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="4e1ea-113">Atkarībā no jūsu vides, iespējams, būs jāpārskata arī citas saistītās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="4e1ea-114">Jauktā numura zīmes saņemšana nestrādā nevienam izvietojuma kodam, izņemot Kredītu.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e1ea-115">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="4e1ea-115">Issue description</span></span>

<span data-ttu-id="4e1ea-116">Kad **Darbības** lauks izvietojuma kodam ir iestatīts kā *Kredīts* vai *Brāķis*, varat izmantot tikai [Jaukto numura zīmes saņemšanas](mixed-license-plate-receiving.md) izvēlnes elementu, lai apstrādātu atgrieztos krājumus.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e1ea-117">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="4e1ea-117">Issue resolution</span></span>

<span data-ttu-id="4e1ea-118">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="4e1ea-119">Pašlaik tikai [izvietojuma kodi](../service-management/set-up-disposition-codes.md), kuros **Darbības** lauks ir iestatīts kā *Kredīts* vai *Brāķis*, tiek atbalstīts jauktai numura zīmes saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="4e1ea-120">Palaižot atjaunināt produktu ieejas plūsmas periodisko uzdevumu, neapstiprinātie pirkšanas pasūtījumi tiek apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e1ea-121">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="4e1ea-121">Issue description</span></span>

<span data-ttu-id="4e1ea-122">Pēc tam, kad esat palaidis *Atjaunināt preču ieejas plūsmu* periodisko uzdevumu, sistēma automātiski apstiprina neapstiprinātos pirkšanas pasūtījumus, kuriem ir krājuma darbības statuss *Reģistrēts*.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e1ea-123">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="4e1ea-123">Issue resolution</span></span>

<span data-ttu-id="4e1ea-124">Jauna ienākošo kravu apstrādes funkcija *Pārsniedzot kravas daudzumu* izlabo šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="4e1ea-125">Lai ieslēgtu šo funkciju, dodieties uz darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet tālāk norādītos līdzekļus (minētajā secībā):</span><span class="sxs-lookup"><span data-stu-id="4e1ea-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="4e1ea-126">Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu</span><span class="sxs-lookup"><span data-stu-id="4e1ea-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="4e1ea-127">Noslodzes daudzumu pārmērīga saņemšana</span><span class="sxs-lookup"><span data-stu-id="4e1ea-127">Over receipt of load quantities</span></span>

<span data-ttu-id="4e1ea-128">Lai iegūtu papildu informāciju, skatiet [Reģistrēto preču daudzumu grāmatošana uz pirkšanas pasūtījumiem](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="4e1ea-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="4e1ea-129">Kad reģistrēju ienākošos pasūtījumus, es saņemu šādu kļūdas ziņojumu: "Daudzums nav derīgs."</span><span class="sxs-lookup"><span data-stu-id="4e1ea-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e1ea-130">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="4e1ea-130">Issue description</span></span>

<span data-ttu-id="4e1ea-131">Ja **Numura zīmes grupēšanas politikas** lauks ir iestatīts uz *Lietotājs, kas ir definēts* mobilās ierīces izvēlnes elementam, kas tiek izmantots ienākošo pasūtījumu reģistrēšanai, saņemat kļūdas ziņojumu ("Daudzums nav derīgs"), un reģistrāciju nevar pabeigt.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="4e1ea-132">Izsniegšanas iemesls</span><span class="sxs-lookup"><span data-stu-id="4e1ea-132">Issue cause</span></span>

<span data-ttu-id="4e1ea-133">Ja *Lietotājs, kas ir definēts* tiek izmantots kā numura zīmi grupēšanas politika, sistēma ienākošos krājumus sadala atsevišķās numura vienībai, kā norādīts vienību secību grupā.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="4e1ea-134">Ja partijas vai sērijas numuri tiek izmantoti saņemtā krājuma izsekošanai, katras partijas vai sērijas daudzumi ir jānorāda uz reģistrēto numura zīmi.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="4e1ea-135">Ja numura zīmei norādītais daudzums pārsniedz daudzumu, kas joprojām ir jāsaņem saskaņā ar pašreizējām dimensijām, saņemat kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e1ea-136">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="4e1ea-136">Issue resolution</span></span>

<span data-ttu-id="4e1ea-137">Kad reģistrējiet krājumu, izmantojot mobilās ierīces izvēlnes vienumu, kura **Numura zīmi grupēšanas politikas** lauks ir iestatīts uz *Lietotājs, kas ir definēts*, sistēmai var būt nepieciešams apstiprināt vai ievadīt numura zīmi numurus, partijas numurus vai sērijas numurus.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="4e1ea-138">Numura zīmes apstiprināšanas lapā sistēma parādīs daudzumu, kas ir piešķirts pašreizējai numura zīmei.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="4e1ea-139">Partijas vai sērijas apstiprinājuma lapās sistēma rādīs daudzumu, kas ir jāsaņem pašreizējā numura zīmi.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="4e1ea-140">Šeit tiks iekļauts arī lauks, kur varat ievadīt daudzumu, ko reģistrēt numura zīmes un paketes vai sērijas numura kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="4e1ea-141">Šajā gadījumā pārliecinieties, ka numura zīmei reģistrētais daudzums nepārsniedz daudzumu, kas joprojām ir jāsaņem.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="4e1ea-142">Ja saņemšanas pasūtījuma reģistrācijā tiek ģenerēts pārāk daudz numura zīmju, **Numura zīmes grupēšanas politikas** lauka vērtību var mainīt uz *Numura zīmes grupēšanu*, krājumam var piešķirt jaunu vienību secību grupu vai vienību secību grupas opciju **Numura zīmju grupai** var deaktivizēt.</span><span class="sxs-lookup"><span data-stu-id="4e1ea-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
