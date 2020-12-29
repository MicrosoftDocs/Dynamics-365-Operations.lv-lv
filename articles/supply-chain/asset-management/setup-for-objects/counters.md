---
title: Līdzekļu mēri
description: Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu mēru tipus.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432886"
---
# <a name="counters"></a><span data-ttu-id="3288d-103">Skaitītāji</span><span class="sxs-lookup"><span data-stu-id="3288d-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3288d-104">Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu skaitītāju veidus.</span><span class="sxs-lookup"><span data-stu-id="3288d-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="3288d-105">Skaitītāju veidi tiek izmantoti, lai veiktu līdzekļu skaitītāju reģistrācijas, piemēram, attiecībā uz ražošanas stundu skaitu vai līdzeklim saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="3288d-106">Līdzekļu veidi ir saistīti ar skaitītāju veidiem.</span><span class="sxs-lookup"><span data-stu-id="3288d-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="3288d-107">Tas nozīmē, ka skaitītāju var izmantot līdzeklim tikai tad, ja skaitītājs ir iestatīts līdzekļa veidam, kas izmantots līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="3288d-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="3288d-108">Pirms varat veikt skaitītāju reģistrācijas līdzekļiem, izveidojiet skaitītāju veidus, kurus vēlaties izmantot **Skaitītājos**.</span><span class="sxs-lookup"><span data-stu-id="3288d-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="3288d-109">Pēc tam varat izveidot skaitītāju reģistrācijas līdzekļiem **Skaitītājos**.</span><span class="sxs-lookup"><span data-stu-id="3288d-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="3288d-110">Skaitītājus var izmantot uzturēšanas plāniem.</span><span class="sxs-lookup"><span data-stu-id="3288d-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="3288d-111">Uzturēšanas plāna rinda var būt ar tipu "Skaitītājs", piemēram, attiecībā uz ražošanas stundu skaitu vai saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="3288d-112">Skaitītāju reģistrāciju var atjaunināt manuāli vai automātiski, pamatojoties uz ražošanas laiku vai saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="3288d-113">Skaitītāju var iestatīt, lai izmantotu vienu no trim atjaunināšanas metodēm (kas atlasītas laukā **Atjaunināt** sadaļā **Skaitītāji**):</span><span class="sxs-lookup"><span data-stu-id="3288d-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="3288d-114">Manuāli — skaitītāja vērtības ir jāreģistrē manuāli.</span><span class="sxs-lookup"><span data-stu-id="3288d-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="3288d-115">Ražošanas stundas — skaitītājs tiek automātiski atjaunināts, pamatojoties uz ražošanas stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="3288d-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="3288d-116">Ražošanas daudzums — skaitītājs tiek automātiski atjaunināts, pamatojoties uz saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="3288d-117">Ja tiek izmantots saražotais daudzums, *visi* reģistrētie krājumi tiek iekļauti skaitītāju reģistrācijā — labais daudzums, kā arī kļūdu daudzums.</span><span class="sxs-lookup"><span data-stu-id="3288d-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="3288d-118">Ja nepieciešams, vienmēr ir iespējams veikt manuālas skaitītāju reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="3288d-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="3288d-119">Skaitītāju tipu izveide līdzekļu skaitītāju reģistrācijām</span><span class="sxs-lookup"><span data-stu-id="3288d-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="3288d-120">Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu tipi** > **Skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="3288d-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="3288d-121">Atlasiet **Jauns**, lai izveidotu jaunu skaitītāja veidu.</span><span class="sxs-lookup"><span data-stu-id="3288d-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="3288d-122">Ievadiet ID laukā **Skaitītājs**, bet laukā **Nosaukums** — skaitītāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="3288d-123">Kopsavilkuma cilnē **Vispārīgi** atlasiet skaitītāja vienību laukā **Vienība**.</span><span class="sxs-lookup"><span data-stu-id="3288d-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="3288d-124">Laukā **Atjaunināt** atlasiet atjaunināšanas metodi, kas jāizmanto līdzekļa skaitītājam.</span><span class="sxs-lookup"><span data-stu-id="3288d-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="3288d-125">Atlasiet "Jā" pārslēgšanas pogā **Mantotās skaitītāja vērtības**, ja pakārtotajiem līdzekļiem līdzekļu struktūrā automātiski jāmanto skaitītāja reģistrācijas, kas veiktas primārajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="3288d-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="3288d-126">Laukā **Apkopotā kopsumma** atlasiet summēšanas metodi, kas jāizmanto skaitītājā, izmantojot šo skaitītāja veidu.</span><span class="sxs-lookup"><span data-stu-id="3288d-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="3288d-127">"Summa" ir standarta atlase, ko izmanto, lai pastāvīgi pievienotu reģistrētās vērtības kopējai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="3288d-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="3288d-128">"Vidējo" var izmantot, ja skaitītājs ir iestatīts, lai uzraudzītu sliekšņvērtību, piemēram, attiecībā uz temperatūru, vibrāciju vai aktīva nolietojumu un nodilumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="3288d-129">Laukā **Novirze virs** ievadiet augšējo līmeni procentos, lai pārbaudītu, vai manuālās skaitītāja reģistrācijas ir paredzētajā diapazonā.</span><span class="sxs-lookup"><span data-stu-id="3288d-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="3288d-130">Pārbaude ir balstīta uz esošo skaitītāju reģistrāciju lineāru pieaugumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="3288d-131">Laukā **Novirze zem** ievadiet apakšējo līmeni procentos, lai pārbaudītu, vai manuālās skaitītāja reģistrācijas ir paredzētajā diapazonā.</span><span class="sxs-lookup"><span data-stu-id="3288d-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="3288d-132">Pārbaude ir balstīta uz esošo skaitītāju reģistrāciju lineāru samazinājumu.</span><span class="sxs-lookup"><span data-stu-id="3288d-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="3288d-133">Laukā **Tips** atlasiet ziņojuma tipu (informācija, brīdinājums, kļūda), kas jāparāda, ja, veicot manuālas skaitītāju reģistrācijas, rodas novirzes ārpus noteiktā diapazona.</span><span class="sxs-lookup"><span data-stu-id="3288d-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="3288d-134">Kopsavilkuma cilnē **Līdzekļu tipi** pievienojiet līdzekļu tipus, kuriem būtu jāspēj izmantot skaitītāju.</span><span class="sxs-lookup"><span data-stu-id="3288d-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="3288d-135">Kopsavilkuma cilnē **Saistītie skaitītāji** pievienojiet skaitītājus, kurus vēlaties atjaunināt automātiski, kad tiek atjaunināts šis skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="3288d-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="3288d-136">Saistītais skaitītājs tiek automātiski atjaunināts tikai tad, ja saistītajam skaitītājam skaitītāja iestatījumos ir līdzekļa veids, ar kuru tas ir saistīts.</span><span class="sxs-lookup"><span data-stu-id="3288d-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="3288d-137">Piemēram: jūs iestatāt skaitītāju "Ražošanas stundām" un pievienojat līdzekļa veidu "Kravas automašīnas dzinējs".</span><span class="sxs-lookup"><span data-stu-id="3288d-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="3288d-138">Kad šis skaitītājs tiek atjaunināts, atjaunināts tiek arī saistītais skaitītājs "Benzīns" ar tādām pašām skaitītāja vērtībām.</span><span class="sxs-lookup"><span data-stu-id="3288d-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="3288d-139">Iestatījumi **Skaitītājos** ietver iestatījumu "Stundas".</span><span class="sxs-lookup"><span data-stu-id="3288d-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="3288d-140">Lai nodrošinātu skaitītāju saistību, arī skaitītājā "Benzīns" līdzekļa veids "Kravas automašīnas dzinējs" ir jāpievieno kopsavilkuma cilnei **Līdzekļu veidi**.</span><span class="sxs-lookup"><span data-stu-id="3288d-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="3288d-141">Piemēru par Stundu un Benzīna skaitītājiem skatiet ekrānuzņēmumos zemāk.</span><span class="sxs-lookup"><span data-stu-id="3288d-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="3288d-142">Kad līdzekļu veidi tiek pievienoti skaitītāja veidam **Skaitītājos**, šis skaitītājs tiek automātiski pievienots līdzekļu veidiem kopsavilkuma cilnē **Skaitītāji** [Līdzekļu veidi](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="3288d-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![1. attēls](media/071-setup-for-objects.png)

