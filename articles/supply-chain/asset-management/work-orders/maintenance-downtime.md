---
title: Dīkstāve uzturēšanas dēļ
description: Šajā tēmā aprakstīta dīkstāve uzturēšanas dēļ programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918248"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="fd7f2-103">Dīkstāve uzturēšanas dēļ</span><span class="sxs-lookup"><span data-stu-id="fd7f2-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fd7f2-104">Jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas līdzeklī, kas atlasīts darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="fd7f2-105">Tas ir noderīgi, ja vēlaties reģistrēt dīkstāvi uzturēšanas dēļ vienā vai vairākās iekārtās ražošanas zonā.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="fd7f2-106">Vispirms jūs izveidojat dīkstāves uzturēšanas dēļ iemeslu kodus, kurus vēlaties izmantot, piemēram, salūšana vai plānota pārtraukšana.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="fd7f2-107">Tas tiek darīts sadaļā **Dīkstāves uzturēšanas dēļ iemeslu kodi**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="fd7f2-108">Pēc tam jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas sadaļā **Dīkstāve uzturēšanas dēļ** un pievienot atbilstošos iemeslu kodus.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="fd7f2-109">Dīkstāves uzturēšanas dēļ iemeslu kodu izveide</span><span class="sxs-lookup"><span data-stu-id="fd7f2-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="fd7f2-110">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādījums** > **Darba pasūtījumi** > **Dīkstāves uzturēšanas dēļ iemeslu kodi**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="fd7f2-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-111">Click **New**.</span></span>

3. <span data-ttu-id="fd7f2-112">Laukā **Dīkstāves uzturēšanas dēļ iemeslu kods** ievadiet ID.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="fd7f2-113">Laukā **Nosaukums** ievadiet iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="fd7f2-114">Atlasiet izvēles rūti **KPI ietver**, ja iemesla kodu ir jāiekļauj līdzekļa KPI aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="fd7f2-115">Kopumā plānotajiem ražošanas pārtraukumiem nevajadzētu tikt iekļautiem KPI aprēķinos, jo tiem nav ietekmes uz sagaidāmo sniegumu.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="fd7f2-116">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-116">Click **Save**.</span></span>

![1. attēls](media/15-work-orders.png)


<span data-ttu-id="fd7f2-118">Kad esat izveidojis dīkstāves uzturēšanas dēļ iemeslu kodus, kurus vēlaties izmantot, jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas darba pasūtījumiem un līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="fd7f2-119">Dīkstāves uzturēšanas dēļ reģistrāciju izveide</span><span class="sxs-lookup"><span data-stu-id="fd7f2-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="fd7f2-120">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="fd7f2-121">Atlasiet darba pasūtījumu un noklikšķiniet uz **Dīkstāve uzturēšanas dēļ**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="fd7f2-122">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-122">Click **New**.</span></span>

4. <span data-ttu-id="fd7f2-123">Ievadiet dīkstāves uzturēšanas dēļ reģistrācijas laiku un datumu laukos **No** un **Uz**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="fd7f2-124">Atstājot lauku **Uz**, ilgums stundās tiek automātiski ievietots laukā **Ilgums**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="fd7f2-125">Laukā **Dīkstāves uzturēšanas dēļ iemeslu kods** ievadiet iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="fd7f2-126">Ja vēlaties pievienot papildu reģistrācijas, atkārtojiet 3.–6. darbību.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="fd7f2-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-127">Click **Save**.</span></span>


![2. attēls](media/16-work-orders.png)


<span data-ttu-id="fd7f2-129">Kalendārs, kuru izmanto, lai aprēķinātu dīkstāves uzturēšanas dēļ reģistrāciju, ir atkarīgs no jūsu veiktās līdzekļu un parametru uzstādījumu izvēles.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="fd7f2-130">Ja sadaļā **Visi līdzekļi** > **Fiksētais līdzeklis** kopsavilkuma cilnē > laukā **Resurss** ir atlasīts resurss, tiek izmantots kalendāra uzstādījums saistītajai resursu grupai, kā parādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![3. attēls](media/17-work-orders.png)


<span data-ttu-id="fd7f2-132">Ja līdzeklim nav atlasīts neviens resurss, tiek izmantots standarta kalendārs, kas atlasīts sadaļā **Līdzekļu pārvaldības parametri**, kā uzrādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![4. attēls](media/18-work-orders.png)


<span data-ttu-id="fd7f2-134">Noklikšķiniet uz **Uzņēmuma līdzekļu pārvaldība** > **Pieprasījumi** > **Dīkstāve uzturēšanas dēļ**, lai redzētu pārskatu par visām dīkstāves uzturēšanas dēļ reģistrācijām.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="fd7f2-135">Visi kalendāri, kas tiek izmantoti modulī **Līdzekļu pārvaldība**, tiek iestatīti **Organizācijas administrēšana** > **Uzstādīšana** > **Kalendāri** > **Kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="fd7f2-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

