---
title: Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "360582"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="c893a-103">Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="c893a-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c893a-104">Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="c893a-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="c893a-105">Tajā parādīts, kā varat noteikt, ka skaļrunim nepieciešama stūru aizsardzība, ja lietotājs ir atlasījis metāla priekšējo režģi.</span><span class="sxs-lookup"><span data-stu-id="c893a-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="c893a-106">Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="c893a-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="c893a-107">Izteiksmes ierobežojuma izveide</span><span class="sxs-lookup"><span data-stu-id="c893a-107">Create an expression constraint</span></span>
1. <span data-ttu-id="c893a-108">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="c893a-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c893a-109">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="c893a-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="c893a-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c893a-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c893a-111">Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa modelis.</span><span class="sxs-lookup"><span data-stu-id="c893a-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="c893a-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c893a-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c893a-113">Izvērsiet sadaļu Ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="c893a-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="c893a-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c893a-114">Click Add.</span></span>
7. <span data-ttu-id="c893a-115">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="c893a-115">Click Create.</span></span>
8. <span data-ttu-id="c893a-116">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c893a-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="c893a-117">Ievadīt izteiksmi</span><span class="sxs-lookup"><span data-stu-id="c893a-117">Enter expression</span></span>
1. <span data-ttu-id="c893a-118">Noklikšķiniet uz Rediģēt izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="c893a-118">Click Edit expression.</span></span>
    * <span data-ttu-id="c893a-119">Šajā posmā atbloķējot lietotāja interfeisu uzdevuma ierakstīšanu, varat izmantot IntelliSense un simbolu sarakstu, lai izveidotu ierobežojumu izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="c893a-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="c893a-120">Laukā ConstraintBody ievadiet "Nozīmē[FrontGrill=="Metāls", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="c893a-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="c893a-121">Šī izteiksmes loģika nosaka: ja priekšējais režģis ir metāls, tad jāatlasa stūru aizsardzības opcija.</span><span class="sxs-lookup"><span data-stu-id="c893a-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="c893a-122">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="c893a-122">Click Validate.</span></span>
    * <span data-ttu-id="c893a-123">Apstiprināšanas funkcija apstrādā ierobežojuma izteiksmi un pārbauda sintakses kļūdas.</span><span class="sxs-lookup"><span data-stu-id="c893a-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="c893a-124">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="c893a-124">Click Close.</span></span>
5. <span data-ttu-id="c893a-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c893a-125">Click OK.</span></span>

