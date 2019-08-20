---
title: Līdzekļu mēri
description: Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu mēru tipus.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783441"
---
# <a name="asset-measures"></a><span data-ttu-id="8b89d-103">Līdzekļu mēri</span><span class="sxs-lookup"><span data-stu-id="8b89d-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8b89d-104">Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu mēru tipus.</span><span class="sxs-lookup"><span data-stu-id="8b89d-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="8b89d-105">Līdzekļu mēru tipi tiek izmantoti, lai veiktu līdzekļu mērījumu reģistrācijas, piemēram, attiecībā uz ražošanas stundu skaitu vai līdzeklim saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="8b89d-106">Līdzekļu tipi ir saistīti ar līdzekļu mēru tipiem.</span><span class="sxs-lookup"><span data-stu-id="8b89d-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="8b89d-107">Tas nozīmē, ka līdzekļa mēru var izmantot līdzeklim tikai tad, ja līdzekļa mērs ir iestatīts līdzekļa tipam, kas izmantots līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="8b89d-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="8b89d-108">Pirms varat veikt mērījumu reģistrācijas līdzekļiem, izveidojiet līdzekļu mēru tipus, kurus vēlaties izmantot **Skaitītājos**.</span><span class="sxs-lookup"><span data-stu-id="8b89d-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="8b89d-109">Pēc tam varat izveidot mērījumu reģistrācijas līdzekļiem **Līdzekļu mēros**.</span><span class="sxs-lookup"><span data-stu-id="8b89d-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="8b89d-110">Līdzekļu mērus var izmantot uzturēšanas plāniem.</span><span class="sxs-lookup"><span data-stu-id="8b89d-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="8b89d-111">Uzturēšanas plāna rinda var būt ar tipu "Skaitītājs", piemēram, attiecībā uz ražošanas stundu skaitu vai saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="8b89d-112">Līdzekļu mērījumu reģistrāciju var atjaunināt manuāli vai automātiski, pamatojoties uz ražošanas laiku vai saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="8b89d-113">Līdzekļa mēru var iestatīt, lai izmantotu vienu no trim atjaunināšanas metodēm (kas atlasītas laukā **Atjaunināt** sadaļā **Skaitītāji**):</span><span class="sxs-lookup"><span data-stu-id="8b89d-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="8b89d-114">Manuāli — līdzekļu mērījumu vērtības ir jāreģistrē manuāli.</span><span class="sxs-lookup"><span data-stu-id="8b89d-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="8b89d-115">Ražošanas stundas — skaitītājs tiek automātiski atjaunināts, pamatojoties uz ražošanas stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="8b89d-116">Ražošanas daudzums — skaitītājs tiek automātiski atjaunināts, pamatojoties uz saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="8b89d-117">Ja tiek izmantots saražotais daudzums, *visi* reģistrētie krājumi tiek iekļauti mērījumu reģistrācijā — labais daudzums, kā arī kļūdu daudzums.</span><span class="sxs-lookup"><span data-stu-id="8b89d-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="8b89d-118">Ja nepieciešams, vienmēr ir iespējams veikt manuālas līdzekļu mērījumu reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="8b89d-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="8b89d-119">Skaitītāju tipu izveide līdzekļu skaitītāju reģistrācijām</span><span class="sxs-lookup"><span data-stu-id="8b89d-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="8b89d-120">Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu tipi** > **Skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="8b89d-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="8b89d-121">Atlasiet **Jauns**, lai izveidotu jaunu līdzekļa mēra tipu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="8b89d-122">Ievadiet ID laukā **Skaitītājs**, bet laukā **Nosaukums** — skaitītāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="8b89d-123">Kopsavilkuma cilnē **Vispārīgi** atlasiet mērvienību laukā **Vienība**.</span><span class="sxs-lookup"><span data-stu-id="8b89d-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="8b89d-124">Laukā **Atjaunināt** atlasiet atjaunināšanas metodi, kas jāizmanto līdzekļa mēram.</span><span class="sxs-lookup"><span data-stu-id="8b89d-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="8b89d-125">Atlasiet "Jā" pārslēgšanas pogā **Mantotās skaitītāja vērtības**, ja pakārtotajiem līdzekļiem līdzekļu struktūrā automātiski jāmanto līdzekļa mēra reģistrācijas, kas veiktas primārajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="8b89d-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="8b89d-126">Laukā **Apkopotā kopsumma** atlasiet summēšanas metodi, kas jāizmanto līdzekļa mērā, izmantojot šo līdzekļa mēra tipu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="8b89d-127">"Summa" ir standarta atlase, ko izmanto, lai pastāvīgi pievienotu reģistrētās vērtības kopējai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="8b89d-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="8b89d-128">"Vidējo" var izmantot, ja līdzekļa mērs ir iestatīts, lai uzraudzītu sliekšņvērtību, piemēram, attiecībā uz temperatūru, vibrāciju vai aktīva nolietojumu un nodilumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="8b89d-129">Laukā **Novirze virs** ievadiet augšējo līmeni procentos, lai pārbaudītu, vai manuālās līdzekļu mēru reģistrācijas ir paredzētajā diapazonā.</span><span class="sxs-lookup"><span data-stu-id="8b89d-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="8b89d-130">Pārbaude ir balstīta uz esošo līdzekļu mēru reģistrāciju lineāru pieaugumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="8b89d-131">Laukā **Novirze zem** ievadiet apakšējo līmeni procentos, lai pārbaudītu, vai manuālās līdzekļu mēru reģistrācijas ir paredzētajā diapazonā.</span><span class="sxs-lookup"><span data-stu-id="8b89d-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="8b89d-132">Pārbaude ir balstīta uz esošo līdzekļu mēru reģistrāciju lineāru samazinājumu.</span><span class="sxs-lookup"><span data-stu-id="8b89d-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="8b89d-133">Laukā **Tips** atlasiet ziņojuma tipu (informācija, brīdinājums, kļūda), kas jāparāda, ja, veicot manuālas līdzekļu mēru reģistrācijas, rodas novirzes ārpus noteiktā diapazona.</span><span class="sxs-lookup"><span data-stu-id="8b89d-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="8b89d-134">Kopsavilkuma cilnē **Līdzekļu tipi** pievienojiet līdzekļu tipus, kuriem būtu jāspēj izmantot līdzekļa mēru.</span><span class="sxs-lookup"><span data-stu-id="8b89d-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="8b89d-135">Kopsavilkuma cilnē **Saistītie līdzekļa mēri** pievienojiet līdzekļa mērus, kurus vēlaties atjaunināt automātiski, kad tiek atjaunināts šis līdzekļa mērs.</span><span class="sxs-lookup"><span data-stu-id="8b89d-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="8b89d-136">Saistītais līdzekļa mērs tiek automātiski atjaunināts tikai tad, ja saistītajam līdzekļa mēram līdzekļa mēra iestatījumos ir līdzekļa tips, ar kuru tas ir saistīts.</span><span class="sxs-lookup"><span data-stu-id="8b89d-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="8b89d-137">Piemēram: jūs iestatāt līdzekļa mēru "Ražošanas stundām" un pievienojat līdzekļa tipu "Kravas automašīnas dzinējs".</span><span class="sxs-lookup"><span data-stu-id="8b89d-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="8b89d-138">Kad šis līdzeklis tiek atjaunināts, atjaunināts tiek arī saistītais skaitītājs "Benzīns" ar tādām pašām aktīva mēra vērtībām.</span><span class="sxs-lookup"><span data-stu-id="8b89d-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="8b89d-139">Iestatījumi **Skaitītājos** ietver iestatījumu "Stundas".</span><span class="sxs-lookup"><span data-stu-id="8b89d-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="8b89d-140">Lai nodrošinātu līdzekļa mēru saistību, arī līdzekļa mērā "Benzīns" līdzekļa tips "Kravas automašīnas dzinējs" ir jāpievieno kopsavilkuma cilnei **Līdzekļu tipi**.</span><span class="sxs-lookup"><span data-stu-id="8b89d-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="8b89d-141">Piemēru par Stundu un Benzīna līdzekļu mēriem skatiet ekrānuzņēmumos zemāk.</span><span class="sxs-lookup"><span data-stu-id="8b89d-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="8b89d-142">Kad līdzekļu tipi tiek pievienoti līdzekļa mēra tipam **Skaitītājos**, šī līdzekļa mērs tiek automātiski pievienots līdzekļu tipiem kopsavilkuma cilnē **Skaitītāji**[Aktīvu tipos](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="8b89d-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![1. attēls](media/071-setup-for-objects.png)


