---
title: Aprēķina pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987058"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="187f9-103">Aprēķina pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="187f9-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="187f9-104">Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="187f9-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="187f9-105">Tajā parādīts, kā varat izveidot loģisko izteiksmi, izmantojot operatoru "Ja", lai iestatītu skaļruņa augstumu "10" baltiem skaļruņiem un "15" skaļruņiem ar citu korpusa apdari.</span><span class="sxs-lookup"><span data-stu-id="187f9-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="187f9-106">Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="187f9-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="187f9-107">Aprēķina pievienošana</span><span class="sxs-lookup"><span data-stu-id="187f9-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="187f9-108">Aprēķina izteiksmes izveide</span><span class="sxs-lookup"><span data-stu-id="187f9-108">Create calculation expression</span></span>
1. <span data-ttu-id="187f9-109">Noklikšķiniet uz Rediģēt izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="187f9-109">Click Edit expression.</span></span>
2. <span data-ttu-id="187f9-110">Laukā ConstraintBody ievadiet "Ja[CabinetFinish=="Balts", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="187f9-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="187f9-111">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="187f9-111">Click Validate.</span></span>
4. <span data-ttu-id="187f9-112">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="187f9-112">Click Close.</span></span>
5. <span data-ttu-id="187f9-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="187f9-113">Click OK.</span></span>

