---
title: Līdzekļu skaitītāju automātiska atjaunināšana
description: Šajā tēmā aprakstīta automātiska līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875784"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="150ed-103">Līdzekļu skaitītāju automātiska atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="150ed-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="150ed-104">Iepriekšējā nodaļā aprakstīta manuāla līdzekļu skaitītāju atjaunināšana.</span><span class="sxs-lookup"><span data-stu-id="150ed-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="150ed-105">Līdzekļu skaitītāju iestatīšana ir aprakstīta [Skaitītāji](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="150ed-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="150ed-106">Skaitītāju vērtības var arī automātiski atjaunināt no produktu reģistrācijas, balstoties uz ražošanas stundām vai ražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="150ed-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="150ed-107">Tas tiek darīts sadaļā **Atjaunināt līdzekļu skaitītājus**.</span><span class="sxs-lookup"><span data-stu-id="150ed-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="150ed-108">Var atjaunināt vienu vai vairākus līdzekļus, ievietojot vienu parametru **Datums no**.</span><span class="sxs-lookup"><span data-stu-id="150ed-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="150ed-109">Šis parametrs norāda ražošanas reģistrāciju sākuma datumu (stundas vai saražoto daudzumu), tas ir, sākuma datumu, no kura jāatjaunina skaitītāja vērtības.</span><span class="sxs-lookup"><span data-stu-id="150ed-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="150ed-110">Visi līdzekļi, kas saistīti ar resursu *un* kam ir līdzekļu skaitītāji, kas iestatīti atjaunošanai, balstoties uz saražoto daudzumu vai ražošanas stundām, tiks iekļauti automātiskā atjauninājumā, un tiks izveidotas jaunas skaitītāja vērtības.</span><span class="sxs-lookup"><span data-stu-id="150ed-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="150ed-111">Attiecībā uz skaitītājiem, kas balstīti uz ražošanas daudzumu, skaitā ir iekļauts reģistrēto labas kvalitātes preču un bojāto preču daudzums.</span><span class="sxs-lookup"><span data-stu-id="150ed-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="150ed-112">Ja saražotā daudzuma reģistrācijai lietotā vienība atšķiras no skaitītajā izmantotās vienības, daudzums tiek pārveidots, lai atbilstu skaitītāja vienībai.</span><span class="sxs-lookup"><span data-stu-id="150ed-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="150ed-113">Kā minēts iepriekš, automātisko skaitītāju vērtības var arī atjaunināt no produktu reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="150ed-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="150ed-114">Tādēļ līdzeklim, kam vēlaties automātiski atjaunināt skaitītājus, jābūt saistītam ar resursu (mašīnu).</span><span class="sxs-lookup"><span data-stu-id="150ed-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="150ed-115">Šie paskaidrojumi sniedz pārskatu par ražošanas pasūtījumu iestatīšanu un apstrādi (modulī **Ražošanas kontrole**), kas tiek izmantots kā pamats skaitītāju automātiskai atjaunināšanai modulī **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="150ed-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="150ed-116">Kad saražotie daudzumi vai ražošanas stundas reģistrētas resursam, varat atjaunināt saistītos līdzekļu skaitītājus.</span><span class="sxs-lookup"><span data-stu-id="150ed-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="150ed-117">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Līdzekļi** > **Līdzekļu skaitītāju atjaunināšana**.</span><span class="sxs-lookup"><span data-stu-id="150ed-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="150ed-118">Laukā **No datums** atlasiet automātiskā atjauninājuma sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="150ed-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="150ed-119">Datums šajā laukā ir "notiek darbs" datums no **Maršruta darījumi** (**Ražošanas kontrole** > **Pieprasījumi un atskaites** > **Ražošana** > **Maršruta darījumi** > **Fiziskais datums** laukā).</span><span class="sxs-lookup"><span data-stu-id="150ed-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="150ed-120">Ja vēlaties atlasīt konkrētus līdzekļus, līdzekļu veidus vai resursus automātiskam atjauninājumam, kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un atlasiet attiecīgi.</span><span class="sxs-lookup"><span data-stu-id="150ed-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="150ed-121">Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="150ed-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![1. attēls](media/12-work-orders.png)

5. <span data-ttu-id="150ed-123">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="150ed-123">Click **OK**.</span></span> <span data-ttu-id="150ed-124">Kad notikusi automātiska līdzekļu skaitītāja atjaunināšana, varat redzēt ar līdzekli saistītās skaitītāja reģistrācijas sadaļā **Līdzekļu skaitītāji** (**Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi** > Atlasīt līdzekli > **Skaitītāji** poga).</span><span class="sxs-lookup"><span data-stu-id="150ed-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="150ed-125">Sarakstā **Līdzekļu skaitītāju kopsummas** ir pārskats par jaunākajām reģistrācijām visiem skaitītāju veidiem visiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="150ed-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="150ed-126">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu apkopotā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="150ed-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="150ed-127">Skats ir ļoti līdzīgs **Līdzekļu skaitītājam**, bet jūs nevarat pievienot vai rediģēt reģistrācijas **Līdzekļu apkopotajā vērtībā**.</span><span class="sxs-lookup"><span data-stu-id="150ed-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="150ed-128">Tas ir tikai pārskatam.</span><span class="sxs-lookup"><span data-stu-id="150ed-128">It is for overview only.</span></span>

![2. attēls](media/13-work-orders.png)


- <span data-ttu-id="150ed-130">Joprojām ir iespējams veidot manuālas skaitītāja vērtības reģistrācijas skaitītāju veidiem, kas tiek automātiski atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="150ed-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="150ed-131">Skatiet sadaļu „Manuāla līdzekļu skaitītāju atjaunināšana”, kur ir vairāk informācijas.</span><span class="sxs-lookup"><span data-stu-id="150ed-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="150ed-132">Varat iestatīt skaitītājus, kas saistīti ar citu skaitītāju, kas nozīmē, ka, kad tiek atjaunināts skaitītājs, vienlaicīgi tiek automātiski atjaunināti saistītie skaitītāji.</span><span class="sxs-lookup"><span data-stu-id="150ed-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="150ed-133">Skatiet tēmu [Skaitītāji](../setup-for-objects/counters.md) attiecībā uz saistīto skaitītāju iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="150ed-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
