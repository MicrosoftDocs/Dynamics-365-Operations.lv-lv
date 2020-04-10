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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f8fcfdafb2d5fb5a4d4800221fabf4b2111f86
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150267"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Aprēķina pievienošana preces konfigurācijas modelim

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu. Tajā parādīts, kā varat izveidot loģisko izteiksmi, izmantojot operatoru "Ja", lai iestatītu skaļruņa augstumu "10" baltiem skaļruņiem un "15" skaļruņiem ar citu korpusa apdari. Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.


## <a name="add-a-calculation"></a>Aprēķina pievienošana

## <a name="create-calculation-expression"></a>Aprēķina izteiksmes izveide
1. Noklikšķiniet uz Rediģēt izteiksmi.
2. Laukā ConstraintBody ievadiet "Ja[CabinetFinish=="Balts", 10, 15]".
3. Noklikšķiniet uz Pārbaudīt.
4. Noklikšķiniet uz Aizvērt.
5. Noklikšķiniet uz OK.

