--- 
title: "Aprēķina pievienošana preces konfigurācijas modelim"
description: "Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Aprēķina pievienošana preces konfigurācijas modelim

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim pievienot jaunu aprēķinu. Tajā parādīts, kā varat izveidot loģisko izteiksmi, izmantojot operatoru "Ja", lai iestatītu skaļruņa augstumu "10" baltiem skaļruņiem un "15" skaļruņiem ar citu korpusa apdari. Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.


## <a name="add-a-calculation"></a>Aprēķina pievienošana

## <a name="create-calculation-expression"></a>Aprēķina izteiksmes izveide
1. Noklikšķiniet uz Rediģēt izteiksmi.
2. Laukā ConstraintBody ievadiet "Ja[CabinetFinish=="Balts", 10, 15]".
3. Noklikšķiniet uz Pārbaudīt.
4. Noklikšķiniet uz Aizvērt.
5. Noklikšķiniet uz OK.

