---
title: Izmaksu elementu izveide
description: Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779694"
---
# <a name="create-cost-elements"></a>Izmaksu elementu izveide 

[!include [banner](../../includes/banner.md)]

Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos. Šajā procedūrā ir izskaidrots, kā izveidot izmaksu elementu, importējot galvenos kontus un izmantojot datu savienojumu. Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF. Šī procedūra ir paredzēta kā izmaksu uzskaites līdzeklis, kas tika pievienots Dynamics 365 for Operations versijai 1611.


## <a name="create-new-cost-elements"></a>Izveidot jaunus izmaksu elementus
1. Pārejiet uz sadaļu **Izmaksu uzskaite > Dimensijas > Izmaksu elementu dimensijas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. **Laukā Datu savienotājs dimensiju elementiem** ievadiet vai atlasiet vērtību.
5. Laukā **Apraksts** ierakstiet kādu vērtību.
6. Noklikšķiniet uz **Saglabāt**.

## <a name="configure-the-data-connector"></a>Konfigurēt datu savienotāju
1. Noklikšķiniet uz **Konfigurēt dimensijas elementa nodrošinātāju**.
2. Laukā **Kontu** plāns ievadiet vai atlasiet vērtību.
    * Atlasiet **Koplietots**, lai izmantotu koplietojamo kontu plānu.  
3. Klikšķiniet **Jauns**.
4. Sarakstā atzīmējiet atlasīto rindu.
    * Varat izmantot filtrus, lai atlasītu kontus, kas atbilst jūsu kritērijiem.  
5. **Laukā No galvenā konta** ievadiet vai atlasiet vērtību.
6. **Laukā Galvenais konts** ievadiet vai atlasiet vērtību.
7. Noklikšķiniet uz **Labi**.

## <a name="import-main-accounts"></a>Importēt galvenos kontus
1. Noklikšķiniet uz **Importēt dimensijas elementus**.
    * Galvenie konti tiks importēti izmaksu uzskaitē un izmantoti kā izmaksu elementi.  
2. Noklikšķiniet uz **Labi**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Skatīt importētos kontus kā izmaksu elementus
1. Noklikšķiniet uz **Skatīt dimensijas elementus**.
    * Skatiet importētos virsgrāmatas kontus kā izmaksu elementus, uz kuriem var aizplūst izmaksas jūsu uzņēmumā.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
