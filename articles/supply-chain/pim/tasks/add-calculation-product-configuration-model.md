---
title: Aprēķina pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "343171"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Aprēķina pievienošana preces konfigurācijas modelim

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu. Tajā parādīts, kā varat izveidot loģisko izteiksmi, izmantojot operatoru "Ja", lai iestatītu skaļruņa augstumu "10" baltiem skaļruņiem un "15" skaļruņiem ar citu korpusa apdari. Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.


## <a name="add-a-calculation"></a>Aprēķina pievienošana

## <a name="create-calculation-expression"></a>Aprēķina izteiksmes izveide
1. Noklikšķiniet uz Rediģēt izteiksmi.
2. Laukā ConstraintBody ievadiet "Ja[CabinetFinish=="Balts", 10, 15]".
3. Noklikšķiniet uz Pārbaudīt.
4. Noklikšķiniet uz Aizvērt.
5. Noklikšķiniet uz OK.

