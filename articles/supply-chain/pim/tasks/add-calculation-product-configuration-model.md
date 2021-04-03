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
ms.openlocfilehash: 6e23d33c6911310cca6aac0df4589e909568a86a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258075"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]