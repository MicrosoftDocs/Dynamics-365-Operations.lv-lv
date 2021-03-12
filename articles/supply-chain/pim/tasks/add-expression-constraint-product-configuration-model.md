---
title: Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 411e20bd8631b70df981c5785f502693d5ba3705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987133"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="53fb2-103">Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="53fb2-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53fb2-104">Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="53fb2-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="53fb2-105">Tajā parādīts, kā varat noteikt, ka skaļrunim nepieciešama stūru aizsardzība, ja lietotājs ir atlasījis metāla priekšējo režģi.</span><span class="sxs-lookup"><span data-stu-id="53fb2-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="53fb2-106">Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="53fb2-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="53fb2-107">Izteiksmes ierobežojuma izveide</span><span class="sxs-lookup"><span data-stu-id="53fb2-107">Create an expression constraint</span></span>
1. <span data-ttu-id="53fb2-108">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="53fb2-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="53fb2-109">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="53fb2-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="53fb2-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="53fb2-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="53fb2-111">Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa modelis.</span><span class="sxs-lookup"><span data-stu-id="53fb2-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="53fb2-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="53fb2-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="53fb2-113">Izvērsiet sadaļu Ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="53fb2-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="53fb2-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="53fb2-114">Click Add.</span></span>
7. <span data-ttu-id="53fb2-115">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="53fb2-115">Click Create.</span></span>
8. <span data-ttu-id="53fb2-116">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53fb2-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="53fb2-117">Ievadīt izteiksmi</span><span class="sxs-lookup"><span data-stu-id="53fb2-117">Enter expression</span></span>
1. <span data-ttu-id="53fb2-118">Noklikšķiniet uz Rediģēt izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="53fb2-118">Click Edit expression.</span></span>
    * <span data-ttu-id="53fb2-119">Šajā posmā atbloķējot lietotāja interfeisu uzdevuma ierakstīšanu, varat izmantot IntelliSense un simbolu sarakstu, lai izveidotu ierobežojumu izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="53fb2-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="53fb2-120">Laukā ConstraintBody ievadiet "Nozīmē[FrontGrill=="Metāls", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="53fb2-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="53fb2-121">Šī izteiksmes loģika nosaka: ja priekšējais režģis ir metāls, tad jāatlasa stūru aizsardzības opcija.</span><span class="sxs-lookup"><span data-stu-id="53fb2-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="53fb2-122">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="53fb2-122">Click Validate.</span></span>
    * <span data-ttu-id="53fb2-123">Apstiprināšanas funkcija apstrādā ierobežojuma izteiksmi un pārbauda sintakses kļūdas.</span><span class="sxs-lookup"><span data-stu-id="53fb2-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="53fb2-124">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="53fb2-124">Click Close.</span></span>
5. <span data-ttu-id="53fb2-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="53fb2-125">Click OK.</span></span>

