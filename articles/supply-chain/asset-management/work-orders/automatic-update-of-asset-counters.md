---
title: Līdzekļu skaitītāju automātiska atjaunināšana
description: Šajā tēmā aprakstīta automātiska līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9911d5b96bb58b5def3e7dfee0f36826d99f6ba1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263690"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="f7801-103">Pamatlīdzekļu skaitītāju automātiska atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="f7801-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7801-104">Papildinformāciju par līdzekļu skaitītāju manuālu reģistrāciju skatiet tēmā [Līdzekļu skaitītāju manuāla atjaunināšana](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="f7801-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="f7801-105">Informāciju par to, kā iestatīt līdzekļu skaitītājus, skatiet tēmā [Skaitītāji](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="f7801-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="f7801-106">Skaitītāju vērtības var arī automātiski atjaunināt no produktu reģistrācijas, balstoties uz ražošanas stundām vai ražoto daudzumu (proti, daudzumu, kas ir saražots).</span><span class="sxs-lookup"><span data-stu-id="f7801-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="f7801-107">Šis atjauninājums tiek veikts lapā **Atjaunināt līdzekļu skaitītājus**.</span><span class="sxs-lookup"><span data-stu-id="f7801-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="f7801-108">Var atjaunināt vienu vai vairākus līdzekļus, iestatot vienu parametru **Datums no**.</span><span class="sxs-lookup"><span data-stu-id="f7801-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="f7801-109">Šis parametrs norāda ražošanas reģistrāciju sākuma datumu (ražošanas stundas vai ražošanas daudzumu).</span><span class="sxs-lookup"><span data-stu-id="f7801-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="f7801-110">Citiem vārdiem sakot, tas norāda datumu, no kura ir jāatjaunina skaitītāja vērtības.</span><span class="sxs-lookup"><span data-stu-id="f7801-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="f7801-111">Visi līdzekļi, kas saistīti ar resursu *un* kam ir līdzekļu skaitītāji, kas iestatīti atjaunošanai, balstoties uz ražošanas stundām vai saražoto daudzumu, tiks iekļauti automātiskā atjauninājumā.</span><span class="sxs-lookup"><span data-stu-id="f7801-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="f7801-112">Tiks izveidotas jaunas skaitītāja vērtības.</span><span class="sxs-lookup"><span data-stu-id="f7801-112">New counter values will be created.</span></span>

<span data-ttu-id="f7801-113">Skaitītājiem, kas balstās uz saražoto daudzumu, skaits ietver gan derīgo, gan brāķa daudzumu, kas ir reģistrēts.</span><span class="sxs-lookup"><span data-stu-id="f7801-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="f7801-114">Ja saražotā daudzuma reģistrācijai lietotā vienība atšķiras no skaitītajā izmantotās vienības, daudzums tiek pārveidots, lai atbilstu skaitītāja vienībai.</span><span class="sxs-lookup"><span data-stu-id="f7801-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="f7801-115">Kā minēts iepriekš, automātisko skaitītāju vērtības var arī atjaunināt no produktu reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="f7801-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="f7801-116">Tādēļ līdzeklim, kam vēlaties automātiski atjaunināt skaitītājus, jābūt saistītam ar resursu (mašīnu).</span><span class="sxs-lookup"><span data-stu-id="f7801-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="f7801-117">Kad saražotie daudzumi vai ražošanas stundas reģistrētas resursam, varat atjaunināt saistītos līdzekļu skaitītājus.</span><span class="sxs-lookup"><span data-stu-id="f7801-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="f7801-118">Atlasiet **Līdzekļu pārvaldība** > **Periodiski** > **Līdzekļi** > **Līdzekļu skaitītāju atjaunināšana**.</span><span class="sxs-lookup"><span data-stu-id="f7801-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="f7801-119">Laukā **No datums** atlasiet automātiskā atjauninājuma sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="f7801-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="f7801-120">Datums šajā laukā ir "notiek darbs" datums no **Maršruta darījumi** (**Ražošanas kontrole** > **Pieprasījumi un atskaites** > **Ražošana** > **Maršruta darījumi** > **Fiziskais datums** laukā).</span><span class="sxs-lookup"><span data-stu-id="f7801-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="f7801-121">Kopsavilkuma cilnē **Iekļaujamie ieraksti** varat atlasīt konkrētus līdzekļus, līdzekļu veidus vai resursus automātiskai atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="f7801-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="f7801-122">Atlasiet **Filtrēt** un veiciet atbilstošās atlases.</span><span class="sxs-lookup"><span data-stu-id="f7801-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="f7801-123">Ātrajā cilnē **Palaist fonā** jūs varat pēc vajadzības uzstādīt automātisko atjauninājumu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="f7801-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="f7801-124">Attēlā zemāk ir parādīts dialoglodziņš **Atjaunināt līdzekļu skaitītājus**.</span><span class="sxs-lookup"><span data-stu-id="f7801-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![1. attēls](media/12-work-orders.png)

5. <span data-ttu-id="f7801-126">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f7801-126">Select **OK**.</span></span> 

<span data-ttu-id="f7801-127">Pēc automātiskās līdzekļu skaitītāja atjaunināšanas varat apskatīt skaitītāja reģistrācijas, kas saistītas ar līdzekli lapā **Līdzekļu skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="f7801-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="f7801-128">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi**, atlasiet līdzekli un pēc tam darbību rūts cilnas **Līdzeklis** grupā **Profilaktiski** atlasiet **Skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="f7801-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="f7801-129">Lapā **Līdzekļu apkopotā vērtība** ir pārskats par jaunāko reģistrāciju, kas veikta visiem skaitītāju veidiem visiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="f7801-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="f7801-130">Atlasiet **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu apkopotā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="f7801-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="f7801-131">Šī lapa ir līdzīga lapai **Līdzekļu skaitītāji**, taču jūs nevarat pievienot vai rediģēt reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="f7801-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="f7801-132">Tā ir tikai pārskatam.</span><span class="sxs-lookup"><span data-stu-id="f7801-132">It's for overview only.</span></span>

<span data-ttu-id="f7801-133">Attēlā zemāk ir parādīta lapa **Līdzekļu apkopotā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="f7801-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![2. attēls](media/13-work-orders.png)

<span data-ttu-id="f7801-135">Ņemiet vērā šādus punktus:</span><span class="sxs-lookup"><span data-stu-id="f7801-135">Note the following points:</span></span>

- <span data-ttu-id="f7801-136">Joprojām varat veidot manuālas skaitītāja vērtības reģistrācijas skaitītāju veidiem, kas tiek automātiski atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="f7801-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="f7801-137">Papildinformāciju skatiet sadaļā [Manuāla līdzekļu skaitītāju atjaunināšana](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="f7801-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="f7801-138">Varat iestatīt skaitītājus, kas ir saistīti ar citu skaitītāju.</span><span class="sxs-lookup"><span data-stu-id="f7801-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="f7801-139">Šādā gadījumā, atjauninot skaitītāju, vienlaikus automātiski tiek atjaunināti saistītie skaitītāji.</span><span class="sxs-lookup"><span data-stu-id="f7801-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="f7801-140">Papildinformāciju par to, kā iestatīt saistītos skaitītājus, skatiet tēmā [Skaitītāji](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="f7801-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]