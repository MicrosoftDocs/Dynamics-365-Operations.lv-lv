---
title: Izmaksu objektu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810058"
---
# <a name="create-cost-objects"></a>Izmaksu objektu izveide 

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju. Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF. 


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]