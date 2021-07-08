---
title: Palaižot iebūvēto vispārējās plānošanas programmu, tiek parādīta kļūda
description: Palaižot novecojušo iebūvēto vispārējās plānošanas programmu, tiek parādīts kļūdas ziņojums.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294129"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="9a152-103">Palaižot iebūvēto vispārējās plānošanas programmu, tiek parādīta kļūda</span><span class="sxs-lookup"><span data-stu-id="9a152-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="9a152-104">Kļūdas kods: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="9a152-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="9a152-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="9a152-105">Symptoms</span></span>

<span data-ttu-id="9a152-106">Palaižot vispārējo plānošanu, izmantojot novecojušo iebūvēto vispārējās plānošanas programmu, tiek parādīts šāds kļūdas ziņojums:</span><span class="sxs-lookup"><span data-stu-id="9a152-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="9a152-107">Šis kļūdas ziņojums tiek parādīts, jo iebūvētā vispārējās plānošanas programma tika izmantota scenārijiem, ko atbalsta plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="9a152-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="9a152-108">Tagad jums vajadzētu migrēt uz plānošanas optimizāciju, jo pašreizējā iebūvētā vispārējā plānošana ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="9a152-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="9a152-109">Ievērojiet, ka šī vispārējās plānošanas izpilde tika pabeigta sekmīgi.</span><span class="sxs-lookup"><span data-stu-id="9a152-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="9a152-110">Ja jūsu migrācijai ir stipras atkarības no nepabeigtiem līdzekļiem, var tikt pieprasīta atkāpe no iebūvētās vispārējās plānošanas programmas ilgstošas izmantošanas.</span><span class="sxs-lookup"><span data-stu-id="9a152-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="9a152-111">Lūdzu, aizpildiet šo anketu, lai sāktu darbu, un, ja nepieciešams, pieprasiet izņēmumu no migrācijas uz plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="9a152-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="9a152-112">Plānošanas optimizācijas migrācijas un izņēmumu anketas</span><span class="sxs-lookup"><span data-stu-id="9a152-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="9a152-113">Iemesls</span><span class="sxs-lookup"><span data-stu-id="9a152-113">Cause</span></span>

<span data-ttu-id="9a152-114">Ja palaižat plānošanu un neizmantojat ražošanas kontroles līdzekļus, ir jāapsver iespēja migrēt uz Plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="9a152-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="9a152-115">Iebūvētā vispārējās plānošanas programma ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="9a152-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="9a152-116">Tāpēc, ja vēlaties turpināt to lietot, nesaņemot kļūdas ziņojumu, jums ir jāpiesakās, lai saņemtu izņēmumu no Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a152-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="9a152-117">Novēršana</span><span class="sxs-lookup"><span data-stu-id="9a152-117">Resolution</span></span>

<span data-ttu-id="9a152-118">Papildinformāciju par to, kā migrēt uz Plānošanas optimizāciju, vai kā pieteikties uz izņēmumu, lai varētu turpināt izmantot novecojušu iebūvēto plānošanas programmu, skatiet [Migrācija uz vispārējās plānošanas Plānošanas optimizāciju](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="9a152-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
