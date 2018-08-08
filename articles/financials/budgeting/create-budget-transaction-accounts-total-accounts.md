---
title: "Budžeta formas transakciju kontu un kopsummas kontu izveide"
description: "Šajā rakstā ir sniegts pārskats par budžetu veidošanas procesu, pamatojoties uz kopsummu kontiem. Tajā ir arī paskaidrots, kā kopsummu kontiem ieslēgt budžeta kontroli, ja ir nepieciešama budžeta kontrole."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6129a5431cba22ea656e4d6f473a4e93a81131ea
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="5dc1e-104">Budžeta formas transakciju kontu un kopsummas kontu izveide</span><span class="sxs-lookup"><span data-stu-id="5dc1e-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dc1e-105">Šajā rakstā ir sniegts pārskats par budžetu veidošanas procesu, pamatojoties uz kopsummu kontiem.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="5dc1e-106">Tajā ir arī paskaidrots, kā kopsummu kontiem ieslēgt budžeta kontroli, ja ir nepieciešama budžeta kontrole.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="5dc1e-107">Izmantojot budžeta plānu un budžeta reģistra ieraksta dokumentus, var budžetēt galvenos kontus, kam galvenā konta veids ir **Kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="5dc1e-108">Faktiskās izmaksas var grāmatot tikai transakciju galvenajos kontos.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="5dc1e-109">Periodiskajam procesam **Budžeta plāna ģenerēšana no virsgrāmatas** cilnē **Avots** kā kritēriju var norādīt galvenā konta veidu **Kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="5dc1e-110">Šādā gadījumā visi kopsummu galvenie konti tiks iekļauti mērķa budžeta plānā un summa būs vienāda ar atlasīto galveno kontu kopsummu.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="5dc1e-111">Varat aktivizēt budžeta kontroli galvenajiem kontiem ar veidu **Kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="5dc1e-112">Šī funkcionalitāte tiek atbalstīta, izmantojot budžeta grupas.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="5dc1e-113">Katram kopsummu galvenajam kontam budžets, kas jākontrolē attiecībā uz budžeta grupu, ir jāizveido lapā **Budžeta kontroles konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="5dc1e-114">Jūsu norādītajos kritērijos ir jāietilpst kopsummu galvenajam kontam un kontu diapazonam.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="5dc1e-115">Lai paātrinātu budžeta grupu izveides procesu, varat izmantot budžeta kontroles grupu datu elementu.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="5dc1e-116">Ja budžets tiek izmantots pārskatā, piemēram, finanšu pārskatā, kopsummu konta budžeta summa sastāv no:</span><span class="sxs-lookup"><span data-stu-id="5dc1e-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="5dc1e-117">budžetiem, kas izveidoti no katra transakcijas virsgrāmatas konta kopsummu intervālā;</span><span class="sxs-lookup"><span data-stu-id="5dc1e-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="5dc1e-118">budžeta kopsummas, kas ievadīta tieši kopsummas kontā.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="5dc1e-119">Tas ļauj izveidot atsevišķus budžetus visnozīmīgākajiem transakciju kontiem kopsummu konta intervālā un pievienot atlikušo budžeta daudzumu kopsummas kontam.</span><span class="sxs-lookup"><span data-stu-id="5dc1e-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




