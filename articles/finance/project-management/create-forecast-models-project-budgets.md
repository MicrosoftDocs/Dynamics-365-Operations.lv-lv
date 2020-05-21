---
title: Izveidot prognozes modeļus projekta budžetiem
description: Šajā tēmā aprakstīts, kā izveidot prognozes modeli atlikušajiem budžetiem.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321783"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="6f547-103">Izveidot prognozes modeļus projekta budžetiem</span><span class="sxs-lookup"><span data-stu-id="6f547-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f547-104">Šajā tēmā aprakstīts, kā izveidot prognozes modeli atlikušajiem budžetiem.</span><span class="sxs-lookup"><span data-stu-id="6f547-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="6f547-105">Projekts, kas ir pakļauts budžeta kontrolei, izmanto divu veidu budžetus: sākotnējo un atlikušo.</span><span class="sxs-lookup"><span data-stu-id="6f547-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="6f547-106">Veidojot projekta budžetu, ir jānorāda sākotnējā un atlikušā budžeta prognozes modeļi, kas izveidoti **Prognozes modeļi** lapā.</span><span class="sxs-lookup"><span data-stu-id="6f547-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="6f547-107">Uz norādītajiem modeļiem pamatotie projekta budžeti tiek veidoti, kad apstiprināt projekta budžetu.</span><span class="sxs-lookup"><span data-stu-id="6f547-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="6f547-108">Budžeta modelim, kuru izmanto budžeta kontrolei, nevar būt apakšmodeļu vai izmantot kā apakšmodeli.</span><span class="sxs-lookup"><span data-stu-id="6f547-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="6f547-109">Atlasiet **Projektu pārvaldība un uzskaite** > **Iestatījumi** > **Prognozes**  > **Prognožu modeļi**.</span><span class="sxs-lookup"><span data-stu-id="6f547-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="6f547-110">Atlasiet **Jauns**, lai izveidotu jaunu prognozes modeli, un pēc tam ierakstiet modeļa ID numuru un jaunā modeļa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6f547-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="6f547-111">Iestatiet opciju **Apturēts** uz **Jā**, lai nepieļautu izmaiņas prognožu modeļa rindās.</span><span class="sxs-lookup"><span data-stu-id="6f547-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="6f547-112">Ja prognozes rindām, ar kurām modelis ir saistīts, ir jāģenerē naudas plūsmas prognozes virsgrāmatā, iestatiet **iekļaut skaidras naudas plūsmas prognozes** uz **Jā.**</span><span class="sxs-lookup"><span data-stu-id="6f547-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="6f547-113">Lai lietotu projekta datumu kā rēķina datumu, iestatiet **Prognozes rēķina datumu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6f547-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="6f547-114">Laukā **Budžeta veids** atlasiet vienu no šādiem modeļa veidiem:</span><span class="sxs-lookup"><span data-stu-id="6f547-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="6f547-115">**Sākotnējais budžets**: izmantojiet sākotnējā budžeta summas, kas tiek izpildītas, kad sākotnējais budžets ir izveidots un apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="6f547-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="6f547-116">**Atlikušais budžets**: izmantojiet atlikušā budžeta summas projekta dzīves cikla laikā.</span><span class="sxs-lookup"><span data-stu-id="6f547-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="6f547-117">Šī budžeta modeļa bilances tiek samazinātas ar faktiskajiem darījumiem un palielinātas vai samazinātas ar budžeta pārskatījumiem.</span><span class="sxs-lookup"><span data-stu-id="6f547-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="6f547-118">**Pārnešana**: izmantojiet pārnestā budžeta summas šim projektam.</span><span class="sxs-lookup"><span data-stu-id="6f547-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="6f547-119">Pārnešana ir neobligāts process, ko var palaist, lai neizmantotās budžeta summas pārsūtītu no viena finanšu gada uz citu.</span><span class="sxs-lookup"><span data-stu-id="6f547-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="6f547-120">Iestatiet sekojošās opcijas, kā nepieciešams:</span><span class="sxs-lookup"><span data-stu-id="6f547-120">Set the following options as required:</span></span>

   - <span data-ttu-id="6f547-121">Iespējojiet **Prognozes rēķina datumu**, lai lietotu projekta datumu kā rēķina datumu.</span><span class="sxs-lookup"><span data-stu-id="6f547-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="6f547-122">Iespējojiet **Prognoze ar NP** uz prognozi, pamatojoties uz nepabeigto darbu (NP), un pēc tam atlasiet NP veidu.</span><span class="sxs-lookup"><span data-stu-id="6f547-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="6f547-123">Noklusējuma **Budžeta veidu** var paturēt kā **Neviens** vai ievadīt jaunu veidu.</span><span class="sxs-lookup"><span data-stu-id="6f547-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="6f547-124">Pēc ieraksta maiņas budžeta veidu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="6f547-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="6f547-125">Mainot noklusējuma budžeta veidu, visas citas opcijas vairs nebūs pieejamas atjauninājumiem un šo budžeta modeli nevar izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="6f547-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

