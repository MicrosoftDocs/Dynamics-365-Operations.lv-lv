---
title: "Risinātāja stratēģija preces konfigurācijai"
description: "Šajā tēmā ir aprakstīts, kā varat izmantot risinātāja stratēģiju, lai uzlabotu preču konfigurāciju."
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4544128e580b30b14a6236a9a6147ff0a8641d72
ms.contentlocale: lv-lv
ms.lasthandoff: 02/07/2018

---

# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="82956-103">Risinātāja stratēģija preces konfigurācijai</span><span class="sxs-lookup"><span data-stu-id="82956-103">Solver strategy for product configuration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82956-104">Šajā tēmā ir aprakstīts, kā varat izmantot risinātāja stratēģiju, lai uzlabotu preču konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="82956-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="82956-105">Risinātāja stratēģiju koncepcija pirmoreiz tika ieviesta Microsoft Dynamics AX 2012 R2 7. kumulatīvajā atjauninājumā (CU7).</span><span class="sxs-lookup"><span data-stu-id="82956-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="82956-106">Tā tika paplašināta Microsoft Dynamics AX 2012 R3 8. kumulatīvajā atjauninājumā (CU8) un risinājumā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.</span><span class="sxs-lookup"><span data-stu-id="82956-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="82956-107">Risinātāja stratēģijas koncepcijā tagad ir ietvertas tālāk norādītās stratēģijas.</span><span class="sxs-lookup"><span data-stu-id="82956-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="82956-108">Noklusētā vērtība</span><span class="sxs-lookup"><span data-stu-id="82956-108">Default</span></span>
- <span data-ttu-id="82956-109">Vispirms domēni ar minimālu vērtību skaitu</span><span class="sxs-lookup"><span data-stu-id="82956-109">Minimal domains first</span></span>
- <span data-ttu-id="82956-110">No augšas uz leju</span><span class="sxs-lookup"><span data-stu-id="82956-110">Top-down</span></span>
- <span data-ttu-id="82956-111">Z3</span><span class="sxs-lookup"><span data-stu-id="82956-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="82956-112">Risinātāja stratēģija</span><span class="sxs-lookup"><span data-stu-id="82956-112">Solver strategy</span></span> 

<span data-ttu-id="82956-113">Preces konfigurācijas modeli var formulēt kā [ierobežojuma apmierinātības problēmu (CSP — Constraint Satisfaction Problem)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span><span class="sxs-lookup"><span data-stu-id="82956-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="82956-114">Microsoft Solver Foundation (MSF) nodrošina divu veidu risinātāja stratēģijas CSP gadījumu atrisināšanai, ko var izmantot no preču konfigurācijas modeļiem.</span><span class="sxs-lookup"><span data-stu-id="82956-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="82956-115">Šo risinātāja stratēģiju pamatā ir [heiristika](https://techterms.com/definition/heuristic), ko izmanto, lai noteiktu secību, kādā problēmas risināšanas laikā tiek ņemti vērā CSP gadījumu mainīgie.</span><span class="sxs-lookup"><span data-stu-id="82956-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="82956-116">Heiristika var ievērojami ietekmēt veiktspēju, kad tiek risināta problēma vai problēmu klase.</span><span class="sxs-lookup"><span data-stu-id="82956-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="82956-117">Programmā Finance and Operations preču konfigurācijas modeļu risinātāja stratēģija nosaka, kurš risinātājs tiek izmantots heiristikai.</span><span class="sxs-lookup"><span data-stu-id="82956-117">In Finance and Operations, the solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="82956-118">Stratēģijas **Noklusējuma**, **Vispirms domēni ar minimālu vērtību skaitu** un **No augšas uz leju** izmanto divus MSF risinātājus, savukārt stratēģija **Z3** izmanto Z3 risinātāju.</span><span class="sxs-lookup"><span data-stu-id="82956-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="82956-119">Reālu debitoru ieviešanas gadījumu pētījumi liecina, ka, mainot preces konfigurācijas modeļa risinātāja stratēģiju, reakcijas laiks var tikt samazināts no minūtēm līdz milisekundēm.</span><span class="sxs-lookup"><span data-stu-id="82956-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="82956-120">Tādēļ ir vērts izmēģināt dažādas risinātāja stratēģijas, lai atrastu visefektīvāko stratēģiju savam preces konfigurācijas modelim.</span><span class="sxs-lookup"><span data-stu-id="82956-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="82956-121">Risinātāja stratēģijas iestatījumu maiņa</span><span class="sxs-lookup"><span data-stu-id="82956-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="82956-122">Lai mainītu risinātāja stratēģiju, lapas **Preču konfigurācijas modeļi** darbību rūtī atlasiet vienumu **Modeļa rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="82956-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="82956-123">Pēc tam dialoglodziņā **Rediģēt detalizētu informāciju par modeli** atlasiet risinātāja stratēģiju.</span><span class="sxs-lookup"><span data-stu-id="82956-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="82956-124">[![Risinātāja stratēģijas maiņa](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="82956-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="82956-125">Pašlaik nav loģikas, kas automātiski nosaka, kura risinātāja stratēģija ir visefektīvākā stratēģija preces konfigurācijai, kuras pamatā ir ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="82956-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="82956-126">Tādēļ jums risinātāja stratēģijas jāizmēģina pa vienai.</span><span class="sxs-lookup"><span data-stu-id="82956-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="82956-127">Tālāk esošajā tabulā sniegti ieteikumi par risinātāja stratēģijas izmantošanu dažādos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="82956-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="82956-128">Risinātāja stratēģija</span><span class="sxs-lookup"><span data-stu-id="82956-128">Solver strategy</span></span>      | <span data-ttu-id="82956-129">Stratēģijas izmantošana šajā scenārijā</span><span class="sxs-lookup"><span data-stu-id="82956-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="82956-130">Noklusētā vērtība</span><span class="sxs-lookup"><span data-stu-id="82956-130">Default</span></span>              | <span data-ttu-id="82956-131">Stratēģija **Noklusējuma** ir optimizēta tādu modeļu risināšanai, kuru pamatā ir tabulas ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="82956-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="82956-132">Debitoru ieviešanas gadījumu pētījumi liecina, ka šī stratēģija ir visefektīvākā stratēģija scenārijos, kuros plaši tiek izmantoti tabulas ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="82956-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="82956-133">Vispirms domēns ar minimālu vērtību skaitu</span><span class="sxs-lookup"><span data-stu-id="82956-133">Minimal domain first</span></span> | <span data-ttu-id="82956-134">Stratēģijas **Vispirms domēns ar minimālu vērtību skaitu** un **No augšas uz leju** ir cieši saistītas.</span><span class="sxs-lookup"><span data-stu-id="82956-134">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="82956-135">Debitoru ieviešanas gadījumu pētījumi liecina, ka stratēģija **No augšas uz leju**, kas tika ieviesta 8. kumulatīvajā atjauninājumā, pārspēj stratēģiju **Vispirms domēns ar minimālu vērtību skaitu**.</span><span class="sxs-lookup"><span data-stu-id="82956-135">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="82956-136">Tomēr stratēģija **Vispirms domēns ar minimālu vērtību skaitu** ir saglabāta produktā atpakaļsaderības nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="82956-136">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="82956-137">Pierādīts, ka abas šīs risinātāja stratēģijas efektīvāk risina modeļus, kas satur vairākas aritmētiskas izteiksmes bez tabulas ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="82956-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="82956-138">Taču dažos gadījumos stratēģija **Noklusējuma** pārspēj abas šīs stratēģijas.</span><span class="sxs-lookup"><span data-stu-id="82956-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="82956-139">Tādēļ izmēģiniet katru stratēģiju.</span><span class="sxs-lookup"><span data-stu-id="82956-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="82956-140">No augšas uz leju</span><span class="sxs-lookup"><span data-stu-id="82956-140">Top-down</span></span>             | <span data-ttu-id="82956-141">Stratēģijas **Vispirms domēns ar minimālu vērtību skaitu** un **No augšas uz leju** ir cieši saistītas.</span><span class="sxs-lookup"><span data-stu-id="82956-141">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="82956-142">Debitoru ieviešanas gadījumu pētījumi liecina, ka stratēģija **No augšas uz leju**, kas tika ieviesta 8. kumulatīvajā atjauninājumā, pārspēj stratēģiju **Vispirms domēns ar minimālu vērtību skaitu**.</span><span class="sxs-lookup"><span data-stu-id="82956-142">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="82956-143">Tomēr stratēģija **Vispirms domēns ar minimālu vērtību skaitu** ir saglabāta produktā atpakaļsaderības nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="82956-143">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="82956-144">Pierādīts, ka abas šīs risinātāja stratēģijas efektīvāk risina modeļus, kas satur vairākas aritmētiskas izteiksmes bez tabulas ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="82956-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="82956-145">Taču dažos gadījumos stratēģija **Noklusējuma** pārspēj abas šīs stratēģijas.</span><span class="sxs-lookup"><span data-stu-id="82956-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="82956-146">Tādēļ izmēģiniet katru stratēģiju.</span><span class="sxs-lookup"><span data-stu-id="82956-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="82956-147">Z3</span><span class="sxs-lookup"><span data-stu-id="82956-147">Z3</span></span>                   | <span data-ttu-id="82956-148">Kā noklusējuma risinātāja stratēģiju ieteicams izmantot stratēģiju **Z3**.</span><span class="sxs-lookup"><span data-stu-id="82956-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="82956-149">Ja uztraucaties par veiktspēju un mērogojamību, varat izvērtēt pārējās stratēģijas.</span><span class="sxs-lookup"><span data-stu-id="82956-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="82956-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="82956-150">Additional resources</span></span>

[<span data-ttu-id="82956-151">Preces konfigurācijas modeļa veidošana</span><span class="sxs-lookup"><span data-stu-id="82956-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="82956-152">Heiristika</span><span class="sxs-lookup"><span data-stu-id="82956-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="82956-153">Ierobežojuma apmierinātības problēma</span><span class="sxs-lookup"><span data-stu-id="82956-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)
