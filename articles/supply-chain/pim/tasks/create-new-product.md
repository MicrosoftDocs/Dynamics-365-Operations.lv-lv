---
title: Izveidot jaunu preci
description: Šajā uzdevumā ir aprakstīts, kā izveidot jaunu koplietojamu preci.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548420"
---
# <a name="create-a-new-product"></a>Izveidot jaunu preci

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumā ir aprakstīts, kā izveidot jaunu koplietojamu preci. To parasti veic preču noformētājs. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.

1. Dodieties uz Preču informācijas pārvaldība > Preces > Preces.

## <a name="create-a-product"></a>Preces izveide
1. Noklikšķiniet uz Jauns.
2. Laukā Preces numurs ierakstiet vērtību.
    * Ja nav iestatīta numuru sērija preces numuram, tas ir jāievada manuāli.  
3. Laukā Preces nosaukums ierakstiet kādu vērtību.
    * Preces nosaukuma noklusējuma vērtība ir meklēšanas nosaukums. Ja nepieciešams, varat to izmainīt.  
4. Noklikšķiniet uz OK.

## <a name="set-up-dimension-groups"></a>Iestatīt dimensiju grupas
1. Noklikšķiniet uz Dimensiju grupas, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.
    * Noliktavas dimensijas grupa nosaka, kuras noliktavas dimensijas ir jāievada katrai transakcijai attiecīgajai precei un kā tā tiks izsekota krājumos.  
3. Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.
    * Izsekošanas dimensijas grupa nosaka, kuras izsekošanas dimensijas ir jāievada katrai transakcijai attiecīgajai precei un kā tā tiks apstrādāta krājumos.  
4. Noklikšķiniet uz OK.

