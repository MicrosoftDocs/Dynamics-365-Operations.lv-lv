---
title: Aprēķina pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812682"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="16a50-103">Aprēķina pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="16a50-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16a50-104">Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="16a50-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="16a50-105">Tajā parādīts, kā varat izveidot loģisko izteiksmi, izmantojot operatoru "Ja", lai iestatītu skaļruņa augstumu "10" baltiem skaļruņiem un "15" skaļruņiem ar citu korpusa apdari.</span><span class="sxs-lookup"><span data-stu-id="16a50-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="16a50-106">Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="16a50-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="16a50-107">Aprēķina pievienošana</span><span class="sxs-lookup"><span data-stu-id="16a50-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="16a50-108">Aprēķina izteiksmes izveide</span><span class="sxs-lookup"><span data-stu-id="16a50-108">Create calculation expression</span></span>
1. <span data-ttu-id="16a50-109">Noklikšķiniet uz Rediģēt izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="16a50-109">Click Edit expression.</span></span>
2. <span data-ttu-id="16a50-110">Laukā ConstraintBody ievadiet "Ja[CabinetFinish=="Balts", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="16a50-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="16a50-111">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="16a50-111">Click Validate.</span></span>
4. <span data-ttu-id="16a50-112">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="16a50-112">Click Close.</span></span>
5. <span data-ttu-id="16a50-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="16a50-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]