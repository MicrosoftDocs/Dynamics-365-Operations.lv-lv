---
title: Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920885"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="4be62-103">Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="4be62-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4be62-104">Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="4be62-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="4be62-105">Tajā parādīts, kā varat noteikt, ka skaļrunim nepieciešama stūru aizsardzība, ja lietotājs ir atlasījis metāla priekšējo režģi.</span><span class="sxs-lookup"><span data-stu-id="4be62-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="4be62-106">Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="4be62-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="4be62-107">Izteiksmes ierobežojuma izveide</span><span class="sxs-lookup"><span data-stu-id="4be62-107">Create an expression constraint</span></span>

1. <span data-ttu-id="4be62-108">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="4be62-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="4be62-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4be62-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4be62-110">Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa modelis.</span><span class="sxs-lookup"><span data-stu-id="4be62-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="4be62-111">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4be62-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="4be62-112">Izvērsiet sadaļu **Ierobežojumi**.</span><span class="sxs-lookup"><span data-stu-id="4be62-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="4be62-113">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4be62-113">Select **Add**.</span></span>
7. <span data-ttu-id="4be62-114">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="4be62-114">Select **Create**.</span></span>
8. <span data-ttu-id="4be62-115">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4be62-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="4be62-116">Ievadīt izteiksmi</span><span class="sxs-lookup"><span data-stu-id="4be62-116">Enter expression</span></span>

1. <span data-ttu-id="4be62-117">Atlasiet **Rediģēt izteiksmi**.</span><span class="sxs-lookup"><span data-stu-id="4be62-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="4be62-118">Šajā posmā atbloķējot lietotāja interfeisu uzdevuma ierakstīšanu, varat izmantot IntelliSense un simbolu sarakstu, lai izveidotu ierobežojumu izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="4be62-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="4be62-119">Laukā **ConstraintBody** ievadiet "Nozīmē[FrontGrill=="Metāls", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="4be62-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="4be62-120">Šī izteiksmes loģika nosaka: ja priekšējais režģis ir metāls, tad jāatlasa stūru aizsardzības opcija.</span><span class="sxs-lookup"><span data-stu-id="4be62-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="4be62-121">Atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="4be62-121">Select **Validate**.</span></span>
    * <span data-ttu-id="4be62-122">Apstiprināšanas funkcija apstrādā ierobežojuma izteiksmi un pārbauda sintakses kļūdas.</span><span class="sxs-lookup"><span data-stu-id="4be62-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="4be62-123">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="4be62-123">Select **Close**.</span></span>
5. <span data-ttu-id="4be62-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4be62-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]