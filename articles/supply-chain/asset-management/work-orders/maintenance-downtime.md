---
title: Darba pasūtījumu dīkstāve uzturēšanas dēļ
description: Šajā tēmā aprakstīts, kā izveidot dīkstāve uzturēšanas dēļ reģistrācijas līdzeklī, kas ir atlasīts darba pasūtījumā.
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
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020915"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="f29b4-103">Darba pasūtījumu dīkstāve uzturēšanas dēļ</span><span class="sxs-lookup"><span data-stu-id="f29b4-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="f29b4-104">Jūs varat izveidot dīkstāve uzturēšanas dēļ reģistrācijas līdzeklī, kas ir atlasīts darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="f29b4-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="f29b4-105">Šī iespēja ir noderīga, ja vēlaties reģistrēt dīkstāve uzturēšanas dēļ vienā vai vairākās iekārtās ražošanas zonā.</span><span class="sxs-lookup"><span data-stu-id="f29b4-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="f29b4-106">Vispirms jūs izveidojat dīkstāves uzturēšanas dēļ pamatojuma kodus, kurus vēlaties izmantot, piemēram, **Sadalījums** vai **Plānota pārtraukšana**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="f29b4-107">Šī darbība tiek veikta lapā **Dīkstāves uzturēšanas dēļ pamatojuma kodi**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="f29b4-108">Pēc tam jūs varat izveidot reģistrācijas dīkstāves uzturēšanas dēļ lapā **Dīkstāve uzturēšanas dēļ** un pievienot atbilstošos dīkstāve uzturēšanas dēļ pamatojuma kodus.</span><span class="sxs-lookup"><span data-stu-id="f29b4-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="f29b4-109">Dīkstāves uzturēšanas dēļ iemeslu kodu izveide</span><span class="sxs-lookup"><span data-stu-id="f29b4-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="f29b4-110">Atlasiet **Līdzekļu pārvaldība** > **Uzstādījums** > **Darba pasūtījumi** > **Dīkstāves uzturēšanas dēļ pamatojuma kodi**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="f29b4-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-111">Select **New**.</span></span>

3. <span data-ttu-id="f29b4-112">Laukā **Dīkstāve uzturēšanas dēļ pamatojuma kods** ievadiet ID dīkstāve uzturēšanas dēļ pamatojuma kodam.</span><span class="sxs-lookup"><span data-stu-id="f29b4-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="f29b4-113">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f29b4-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="f29b4-114">Atzīmējiet izvēles rūtiņu **KPI iekļaut**, ja pamatojuma kods ir jāietver pamatlīdzekļa izpildes pamatrādītāja (key performance indicators - KPIs) aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="f29b4-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="f29b4-115">Kopumā plānotajiem ražošanas pārtraukumiem nevajadzētu tikt iekļautiem KPI aprēķinos, tāpēc ka tiem nav ietekmes uz sagaidāmo sniegumu.</span><span class="sxs-lookup"><span data-stu-id="f29b4-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="f29b4-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-116">Select **Save**.</span></span>

<span data-ttu-id="f29b4-117">Šajā attēlā ir parādīts lapas **Dīkstāves uzturēšanas dēļ pamatojuma kodi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="f29b4-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![1. attēls](media/15-work-orders.png)

<span data-ttu-id="f29b4-119">Pēc tam, kad esat izveidojis dīkstāves uzturēšanas dēļ iemeslu kodus, kurus vēlaties izmantot, jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas darba pasūtījumiem un līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="f29b4-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="f29b4-120">Dīkstāves uzturēšanas dēļ reģistrāciju izveide</span><span class="sxs-lookup"><span data-stu-id="f29b4-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="f29b4-121">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f29b4-122">Atlasiet darba pasūtījumu un pēc tam cilnē **Darba pasūtījums** grupā **Līdzeklis** atlasiet **Dīkstāve uzturēšanas dēļ**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="f29b4-123">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-123">Select **New**.</span></span>

4. <span data-ttu-id="f29b4-124">Laukos **No** un **Uz** ievadiet dīkstāves uzturēšanas dēļ reģistrācijas laiku un datumu.</span><span class="sxs-lookup"><span data-stu-id="f29b4-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="f29b4-125">Atstājot lauku **Uz**, ilgums stundās tiek automātiski ievietots laukā **Ilgums**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="f29b4-126">Laukā **Dīkstāves uzturēšanas dēļ iemeslu kods** atlasiet iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="f29b4-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="f29b4-127">Atkārtojiet 3. līdz 5. soli, lai pievienotu vairāk reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="f29b4-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="f29b4-128">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-128">Select **Save**.</span></span>

<span data-ttu-id="f29b4-129">Attēlā tālāk parādīts dīkstāve uzturēšanas dēļ reģistrācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="f29b4-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![2. attēls](media/16-work-orders.png)

<span data-ttu-id="f29b4-131">Kalendārs, kuru izmanto, lai aprēķinātu dīkstāves uzturēšanas dēļ reģistrāciju, ir atkarīgs no jūsu līdzekļu un parametru uzstādījumu izvēles.</span><span class="sxs-lookup"><span data-stu-id="f29b4-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="f29b4-132">Ja sadaļā **Resurss** kopsavilkuma cilnē **Fiksētais līdzeklis** lapā **Visi līdzekļi** ir atlasīts resurss, tiek izmantots kalendārs, kas ir uzstādīts saistītajai resursu grupai, kā parādīts šajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="f29b4-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![3. attēls](media/17-work-orders.png)

<span data-ttu-id="f29b4-134">Ja līdzeklim nav atlasīts neviens resurss, tiek izmantots standarta kalendārs, kas ir atlasīts lapā **Līdzekļu pārvaldības parametri**, kā uzrādīts šajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="f29b4-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![4. attēls](media/18-work-orders.png)

<span data-ttu-id="f29b4-136">Lai redzētu pārskatu par visām dīkstāves uzturēšanas dēļ reģistrācijām, noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Dīkstāve uzturēšanas dēļ**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="f29b4-137">Visi kalendāri, izmantoti modulī **Līdzekļu pārvaldība**, tiek iestatīti **Organizācijas administrēšana** > **Uzstādīšana** > **Kalendāri** > **Kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="f29b4-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

