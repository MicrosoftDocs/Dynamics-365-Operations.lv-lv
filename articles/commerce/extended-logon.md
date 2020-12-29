---
title: Paplašinātās pieteikšanās funkcionalitātes iestatīšana pārdošanas punktiem MPOS un Cloud POS
description: Šajā tēmā ir aprakstītas Cloud POS un Retail Modern POS (MPOS) paplašinātās pieteikšanās iestatīšanas iespējas.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 79878e2ffbf219f77f378997c277ced8bb41598c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414006"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="399bb-103">Paplašinātās pieteikšanās funkcionalitātes iestatīšana MPOS un Cloud POS</span><span class="sxs-lookup"><span data-stu-id="399bb-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="399bb-104">Šajā tēmā ir aprakstītas Cloud POS un Retail Modern POS (MPOS) paplašinātās pieteikšanās iestatīšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="399bb-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="399bb-105">Paplašinātās pieteikšanās iestatīšana</span><span class="sxs-lookup"><span data-stu-id="399bb-105">Setting up extended logon</span></span>

<span data-ttu-id="399bb-106">Svītrkoda masku iestatījumi ir pieejami, izmantojot šādu ceļu: **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatījumi** &gt; **POS iestatījumi** &gt; **POS profili** &gt; **Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="399bb-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="399bb-107">Kopsavilkuma cilnē **Funkcijas** ir iekļautas tālāk norādītās opcijas, kas ir saistītas ar paplašināto pieteikšanos.</span><span class="sxs-lookup"><span data-stu-id="399bb-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="399bb-108">Personāla pieteikšanās ar svītrkodu</span><span class="sxs-lookup"><span data-stu-id="399bb-108">Staff bar code logon</span></span>

<span data-ttu-id="399bb-109">Ja ir iespējota opcija **Personāla pieteikšanās ar svītrkodu**, darbinieki, kuru pārdošanas punkta (POS) akreditācijas datiem ir piešķirtas paplašinātās pieteikšanās tiesības, var pieteikties, izmantojot svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="399bb-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="399bb-110">Darbinieku pieteikumam ar svītrkodu nepieciešama parole</span><span class="sxs-lookup"><span data-stu-id="399bb-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="399bb-111">Ja ir iespējota opcija **Personāla pieteikšanās ar svītrkodu jāpapildina ar paroli**, personāla pieteikšanās ar svītrkodu laikā tiek atlasīts tikai tas darbinieks, kam ir piešķirtas paplašinātās pieteikšanās tiesības, kas tiek apliecinātas.</span><span class="sxs-lookup"><span data-stu-id="399bb-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="399bb-112">Ja šī opcija ir iespējota, darbiniekiem tomēr jāievada parole.</span><span class="sxs-lookup"><span data-stu-id="399bb-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="399bb-113">Personāla pieteikšanās ar karti</span><span class="sxs-lookup"><span data-stu-id="399bb-113">Staff card logon</span></span>

<span data-ttu-id="399bb-114">Ja ir iespējota opcija **Personāla pieteikšanās ar karti**, darbinieki, kuru POS akreditācijas datos ir piešķirtas paplašinātās pieteikšanās tiesības, var pieteikties, izmantojot magnētisko karti.</span><span class="sxs-lookup"><span data-stu-id="399bb-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="399bb-115">Darbinieku pieteikumam ar karti nepieciešama parole</span><span class="sxs-lookup"><span data-stu-id="399bb-115">Staff card logon requires password</span></span>

<span data-ttu-id="399bb-116">Ja ir iespējota opcija **Personāla pieteikšanās ar karti jāpapildina ar paroli**, kad personāls piesakās, izmantojot karti, tiek atlasīts tikai tas darbinieks, kam ir piešķirtas paplašinātās pieteikšanās tiesības, kas tiek apliecinātas.</span><span class="sxs-lookup"><span data-stu-id="399bb-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="399bb-117">Ja šī opcija ir iespējota, darbiniekiem tomēr jāievada parole.</span><span class="sxs-lookup"><span data-stu-id="399bb-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="399bb-118">Paplašinātās pieteikšanās tiesību piešķiršana</span><span class="sxs-lookup"><span data-stu-id="399bb-118">Assigning an extended logon</span></span>

<span data-ttu-id="399bb-119">Pēc noklusējuma paplašinātās pieteikšanās tiesības strādniekiem var piešķirt tikai vadītāji.</span><span class="sxs-lookup"><span data-stu-id="399bb-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="399bb-120">Lai piešķirtu paplašināto pieteikšanos, pārdošanas punktā (POS) dodieties uz **Paplašinātā pieteikšanās**.</span><span class="sxs-lookup"><span data-stu-id="399bb-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="399bb-121">Pēc tam meklējiet nodarbināto, meklēšanas laukā ievadot viņa vai viņas operatora ID.</span><span class="sxs-lookup"><span data-stu-id="399bb-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="399bb-122">Atlasiet strādnieka vārdu un pēc tam noklikšķiniet uz **Piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="399bb-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="399bb-123">Nākamajā lapā nolasiet vai skenējiet paplašinātās pieteikšanās karti, lai piešķirtu to strādniekam.</span><span class="sxs-lookup"><span data-stu-id="399bb-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="399bb-124">Ja kartes nolasīšana vai skenēšana ir sekmīga, aktivizēta tiek poga **Labi**.</span><span class="sxs-lookup"><span data-stu-id="399bb-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="399bb-125">Noklikšķiniet uz **Labi**, lai saglabātu darbinieka paplašinātās pieteikšanās tiesības.</span><span class="sxs-lookup"><span data-stu-id="399bb-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="399bb-126">Paplašinātās pieteikšanās tiesību dzēšana</span><span class="sxs-lookup"><span data-stu-id="399bb-126">Deleting an extended logon</span></span>

<span data-ttu-id="399bb-127">Lai dzēstu darbiniekam piešķirtās paplašinātās pieteikšanās tiesības, izmantojiet darbību **Paplašinātā pieteikšanās** un meklējiet darbinieku.</span><span class="sxs-lookup"><span data-stu-id="399bb-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="399bb-128">Atlasiet darbinieka vārdu un pēc tam noklikšķiniet uz **Noņemt piešķirtās tiesības**.</span><span class="sxs-lookup"><span data-stu-id="399bb-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="399bb-129">Visi ar šo lietotāju saistītie paplašinātās pieteikšanās akreditācijas dati tiek noņemti.</span><span class="sxs-lookup"><span data-stu-id="399bb-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="399bb-130">Paplašinātās pieteikšanās tiesību paplašināšana</span><span class="sxs-lookup"><span data-stu-id="399bb-130">Extending extended logon</span></span>

<span data-ttu-id="399bb-131">Pieteikšanās pakalpojumu var paplašināt, lai atbalstītu papildu paplašinātās pieteikšanās ierīces, piemēra, plaukstas skenerus.</span><span class="sxs-lookup"><span data-stu-id="399bb-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="399bb-132">Lai iegūtu papildinformāciju, skatiet POS dokumentāciju par paplašināšanas iespējām.</span><span class="sxs-lookup"><span data-stu-id="399bb-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="399bb-133">Paplašinātās pieteikšanās tiesību izmantošana</span><span class="sxs-lookup"><span data-stu-id="399bb-133">Using extended logon</span></span>

<span data-ttu-id="399bb-134">Ja paplašinātā pieteikšanās opcija ir konfigurēta un darbiniekam ir piešķirts svītrkods un magnētiskā karte, darbiniekam ir tikai jānolasa vai jānoskenē karte, kamēr ir atvērta POS pieteikšanās lapa.</span><span class="sxs-lookup"><span data-stu-id="399bb-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="399bb-135">Ja pirms pieteikšanās turpināšanas ir jāievada arī parole, darbiniekam tiek parādīta uzvedne ievadīt savu parole.</span><span class="sxs-lookup"><span data-stu-id="399bb-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>
