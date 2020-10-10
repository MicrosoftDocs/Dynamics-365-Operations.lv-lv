---
title: Uzturēšanas budžetu izveide
description: Šajā tēmā ir paskaidrots, kā izveidot uzturēšanas budžetu programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2aaba8794bf0025f0449509752e4f197d3bf3db4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889701"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="0084e-103">Uzturēšanas budžetu izveide</span><span class="sxs-lookup"><span data-stu-id="0084e-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="0084e-104">Uzturēšanas budžeti tiek izmantoti, lai iegūtu pārskatu par profilaktiskās uzturēšanas izmaksām.</span><span class="sxs-lookup"><span data-stu-id="0084e-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="0084e-105">Budžeta rindas tiek aprēķinātas, balstoties uz uzturēšanas grafika rindām, kam ir paredzēts sākuma datums budžeta perioda laikā.</span><span class="sxs-lookup"><span data-stu-id="0084e-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="0084e-106">Uzturēšanas budžeti ir balstīti uz izmaksu veidiem, ko lieto programmā Asset Management: **Profilaktiskas**, **Labojošas** un **Ieguldījumi**.</span><span class="sxs-lookup"><span data-stu-id="0084e-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="0084e-107">Budžeta izmaksas ieguldījumu uzturēšanai ir iekļautas aktīvajiem līdzekļiem, kam aizvietošanas datums ir budžeta periodā un ir saistīta aizstāšanas vērtība.</span><span class="sxs-lookup"><span data-stu-id="0084e-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="0084e-108">Labojošas uzturēšanas budžeta izmaksas tiek iekļautas, ja pagātnes labošanas datums ir iekļauts budžeta aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0084e-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="0084e-109">Tādā gadījuma labošanas izmaksas no iepriekšējā perioda tiek aprēķinātas tam pašam nākotnes periodam, kam aprēķināts uzturēšanas budžetu.</span><span class="sxs-lookup"><span data-stu-id="0084e-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="0084e-110">Uzturēšanas budžeta izveide</span><span class="sxs-lookup"><span data-stu-id="0084e-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="0084e-111">Atlasiet **Līdzekļu pārvaldība** \> **Pieprasījumi** \> **Uzturēšanas budžets** \> **Budžets**.</span><span class="sxs-lookup"><span data-stu-id="0084e-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="0084e-112">Atlasiet **Izveidot budžetu**.</span><span class="sxs-lookup"><span data-stu-id="0084e-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="0084e-113">Laukā **Uzturēšanas budžets** ievadiet budžeta ID.</span><span class="sxs-lookup"><span data-stu-id="0084e-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="0084e-114">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0084e-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0084e-115">Kopsavilkuma cilnē **Periods** laukumā **Datums no** un **Datums līdz** ievadiet budžeta perioda sākuma un beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="0084e-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="0084e-116">Lai iekļautu labošanas budžeta izmaksas, kas aprēķinātas, balstoties uz faktiskajam izmaksām iepriekšējā periodā, laukā **Labošanas datums no** ievadiet sākuma datumu periodam, no kura ir jāiekļauj šīs izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0084e-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="0084e-117">Atkarībā no detalizācijas līmeņa budžetā iestatiet vajadzīgās opcijas kopsavilkuma cilnēs **Grupēt pēc**.</span><span class="sxs-lookup"><span data-stu-id="0084e-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="0084e-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0084e-118">Select **OK**.</span></span>
8. <span data-ttu-id="0084e-119">Atlasiet **Budžeta rindas** lapā **Uzturēšanas budžeta rindas**, kur varat skatīt visas budžeta rindas, kas ir izveidotas periodam.</span><span class="sxs-lookup"><span data-stu-id="0084e-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="0084e-120">Lai apstiprinātu budžetu, atlasiet to lapā **Uzturēšanas budžeti**, tad atlasiet **Apstiprināt**</span><span class="sxs-lookup"><span data-stu-id="0084e-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="0084e-121">Dialoglodziņā **Apstiprināt budžetu** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0084e-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="0084e-122">Jūsu vārds tiek ievadīts laukā **Apstiprināja** lapā **Uzturēšanas budžeti**.</span><span class="sxs-lookup"><span data-stu-id="0084e-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0084e-123">Kad esat apstiprinājis uzturēšanas budžetu, varat pārrēķināt vai precizēt saistītās rindas lapā **Uzturēšanas budžeta rindas**, ja vien pirms tam neesat noņēmis apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="0084e-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="0084e-124">Lai noņemtu uzturēšanas budžeta apstiprinājumu, atlasiet to lapā **Uzturēšanas budžeti**, tad atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="0084e-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="0084e-125">Dialoglodziņā **Apstiprināt budžetu** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0084e-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Uzturēšanas budžeti](media/01-maintenance-budgets.png)

<span data-ttu-id="0084e-127">Jūs varat arī izveidot jaunu uzturēšanas budžetu, kopējot esošu budžetu.</span><span class="sxs-lookup"><span data-stu-id="0084e-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="0084e-128">Kopējamo budžetu atlasiet lapā **Uzturēšanas budžeti**, tad atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="0084e-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="0084e-129">Šī pieeja ir noderīga, piemēram, ja esat izveidojis budžetu vienam mēnesim un vēlaties to kopēt citiem mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="0084e-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="0084e-130">Uzturēšanas budžetā tiek aprēķinātas tikai budžeta izmaksas, balstoties uz uzturēšanas grafika rindām.</span><span class="sxs-lookup"><span data-stu-id="0084e-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="0084e-131">Lai aprēķinātu faktiskās izmaksas tam pašam periodam, šo aprēķinu var veikt lapā **Līdzekļu izmaksu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="0084e-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
