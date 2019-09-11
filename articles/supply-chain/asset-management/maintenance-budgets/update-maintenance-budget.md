---
title: Uzturēšanas budžeta atjaunināšana
description: Šajā tēmā ir paskaidrots, kā atjaunināt uzturēšanas budžetu programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 486782968816cc585d9cf2d753f32e82f85e4f7e
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874789"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="8aeae-103">Uzturēšanas budžeta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="8aeae-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8aeae-104">Lapa **Uzturēšanas budžeta rindas** parāda visas budžeta rindas, kas ir izveidotas budžetā, kas ir atlasīts lapā **Uzturēšanas budžeti**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="8aeae-105">(Vairāk informācijas skatiet sadaļā [Uzturēšanas budžetu izveide](create-maintenance-budget.md).) Jūs varat pārrēķināt un pielāgot uzturēšanas budžeta rindas, līdz tiek apstiprināts uzturēšanas budžets.</span><span class="sxs-lookup"><span data-stu-id="8aeae-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="8aeae-106">Kad budžeta periods ir pagājis un izmaksas ir ievietotas līdzekļu pārvaldībā, varat atjaunināt budžeta rindas ar faktiskajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="8aeae-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="8aeae-107">Uzturēšanas budžeta pārrēķināšana</span><span class="sxs-lookup"><span data-stu-id="8aeae-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="8aeae-108">Jūs varat pārrēķināt uzturēšanas budžetu lapā **Uzturēšanas budžeta rindas**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="8aeae-109">Pārrēķinot uzturēšanas budžetu, esošās budžeta rindas tiek izdzēstas un tiek veikts jauns aprēķins.</span><span class="sxs-lookup"><span data-stu-id="8aeae-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="8aeae-110">Lapā **Uzturēšanas budžeta rindas** atlasiet **Pārrēķināt**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="8aeae-111">Dialoglodziņā **Pārrēķināt budžetu** veiciet nepieciešamās izmaiņas jaunajam aprēķinam un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="8aeae-112">Atbilstoši iestatītajām vērtībām tiek izveidotas jaunas budžeta rindas.</span><span class="sxs-lookup"><span data-stu-id="8aeae-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="8aeae-113">Budžeta rindu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="8aeae-113">Adjust budget lines</span></span>

<span data-ttu-id="8aeae-114">Tā vietā, lai pārrēķinātu visu uzturēšanas budžetu, varat pielāgot atlasītās rindas, kas saistītas ar budžeta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="8aeae-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="8aeae-115">Lapā **Uzturēšanas budžeta rindas** atlasiet rindas, lai tām atjauninātu budžeta izmaksas.</span><span class="sxs-lookup"><span data-stu-id="8aeae-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="8aeae-116">Atlasiet **Pielāgot**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="8aeae-117">Lai atlasītajām rindām pievienotu summu, atlasiet dialoglodziņu **Pievienot izmaksas** un tad ievadiet vērtību laukā **Pievienot vērtību**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="8aeae-118">Lai reizinātu budžeta izmaksas atlasītajās budžeta rindās ar koeficientu, atlasiet dialoglodziņu **Reizināt izmaksas** un ievadiet koeficientu laukā **Reizināšanas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="8aeae-119">Piemēram, ja jūs ievadāt vērtību **1,2** laukā **Reizināšanas vērtība**, jūs palielināt budžeta izmaksas izvēlētajām rindām par 20 procentiem.</span><span class="sxs-lookup"><span data-stu-id="8aeae-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="8aeae-120">Ja jūs ievadāt vērtību **0,7**, jūs samazināt budžeta izmaksas izvēlētajām rindām par 30 procentiem.</span><span class="sxs-lookup"><span data-stu-id="8aeae-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="8aeae-121">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-121">Select **OK**.</span></span>

<span data-ttu-id="8aeae-122">Atlasītās budžeta rindas tiek atjauninātas atbilstoši vērtībām, kuras iestatījāt 3. vai 4. darbībā.</span><span class="sxs-lookup"><span data-stu-id="8aeae-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="8aeae-123">Faktisko izmaksu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="8aeae-123">Update actual costs</span></span>

<span data-ttu-id="8aeae-124">Kad datumi budžeta rindās ir pagājuši un faktiskās izmaksas ir publicētas līdzekļu pārvaldībā, varat atjaunināt uzturēšanas budžeta faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="8aeae-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="8aeae-125">Lapā **Uzturēšanas budžeta rindas** atlasiet **Atjaunināt izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="8aeae-126">Dialoglodziņā **Aprēķināt faktiskās izmaksas** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8aeae-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="8aeae-127">Lauki **Faktiskās izmaksas** budžeta pozīcijās tiek atjaunināti, ja ir publicētas faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="8aeae-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="8aeae-128">Jaunas budžeta rindas var tikt izveidotas, ja kopš budžeta izveidošanas ir izveidoti jauni līdzekļu veidi un ja šie līdzekļu veidi ir izmantoti līdzekļiem, kuriem ir izveidoti darba pasūtījumi un par kuriem ir publicētas saistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="8aeae-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="8aeae-129">Jaunās budžeta rindas parāda tikai faktiskās izmaksas, jo tām netika aprēķinātas budžeta izmaksas.</span><span class="sxs-lookup"><span data-stu-id="8aeae-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="8aeae-130">Lai skatītu pārskatu par faktiskajām izmaksām, kas sadalītas profilaktiskajās, koriģējošajās un ieguldījumu izmaksās, lapā **Līdzekļu izmaksu kontrole** varat veikt aprēķinus par to pašu periodu.</span><span class="sxs-lookup"><span data-stu-id="8aeae-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="8aeae-131">Budžeta rindu manuāla pievienošana</span><span class="sxs-lookup"><span data-stu-id="8aeae-131">Manually add budget lines</span></span>

<span data-ttu-id="8aeae-132">Lapā **Uzturēšanas budžeta rindas** jūs varat manuāli pievienot jaunu budžeta rindu, atlasot **Jauns** un tad veicot nepieciešamās atlases rindā.</span><span class="sxs-lookup"><span data-stu-id="8aeae-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="8aeae-133">Šeit ir daži situāciju piemēri, kad šī pieeja varētu būt noderīga.</span><span class="sxs-lookup"><span data-stu-id="8aeae-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="8aeae-134">Jūs zināt, ka dažu līdzekļu atjaunošana pašlaik ir plānošanas posmā, bet saistītie uzdevumi vēl nav izveidoti līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="8aeae-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="8aeae-135">Tomēr jūs vēlaties, lai šo uzdevumu budžeta izmaksas tiktu iekļautas uzturēšanas budžetā.</span><span class="sxs-lookup"><span data-stu-id="8aeae-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="8aeae-136">Kopš budžeta uzturēšanas budžeta sastādīšanas ir izveidoti jauni līdzekļi vai līdzekļu veidi, taču šiem līdzekļiem vai līdzekļu veidiem vēl nav izveidoti uzturēšanas plāni.</span><span class="sxs-lookup"><span data-stu-id="8aeae-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="8aeae-137">Tomēr jūs vēlaties, lai šo līdzekļu veidu budžeta izmaksas tiktu iekļautas uzturēšanas budžetā.</span><span class="sxs-lookup"><span data-stu-id="8aeae-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
