---
title: 'Izmaksu objektu izveide  '
description: Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot Dynamics 365 for Finance and Operations Enterprise edition izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543775"
---
# <a name="create-cost-objects"></a>Izmaksu objektu izveide   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot Dynamics 365 for Finance and Operations Enterprise edition izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju. Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF. Šī procedūra ir paredzēta kā izmaksu uzskaites līdzeklis, kas tika pievienots Dynamics 365 for Operations versijai 1611.


## <a name="create-new-cost-objects"></a>Izveidot jaunus izmaksu objektus
1. Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu objektu dimensijas.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.
5. Apraksta laukā ierakstiet vērtību.
6. Noklikšķiniet uz Saglabāt.

## <a name="configure-the-data-connector"></a>Konfigurēt datu savienotāju
1. Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.
    * Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.  
2. Laukā Dimensijas nosaukums atlasiet opciju Izmaksu centrs.
3. Noklikšķiniet uz OK.

## <a name="import-cost-centers"></a>Importēt izmaksu centrus
1. Noklikšķiniet uz Importēt dimensiju elementus.
2. Noklikšķiniet uz OK.

## <a name="view-the-imported-cost-centers"></a>Skatīt importēto izmaksu centrus
1. Noklikšķiniet uz Skatīt dimensijas elementus.

