---
title: Izmaksu elementu izveide
description: Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba36e8d2c5b1fc1df6e63e5eef20c465cbd0b693086eece4079ae2216d2c156e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762392"
---
# <a name="create-cost-elements"></a>Izmaksu elementu izveide 

[!include [banner](../../includes/banner.md)]

Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos. Šajā procedūrā ir izskaidrots, kā izveidot izmaksu elementu, importējot galvenos kontus un izmantojot datu savienojumu. Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF. Šī procedūra ir paredzēta kā izmaksu uzskaites līdzeklis, kas tika pievienots Dynamics 365 for Operations versijai 1611.


## <a name="create-new-cost-elements"></a>Izveidot jaunus izmaksu elementus
1. Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu elementa dimensijas.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.
5. Apraksta laukā ierakstiet vērtību.
6. Noklikšķiniet uz Saglabāt.

## <a name="configure-the-data-connector"></a>Konfigurēt datu savienotāju
1. Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.
2. Ievadiet vai atlasiet vērtību laukā Kontu plāns.
    * Atlasiet Koplietots, lai izmantotu koplietojamo kontu plānu.  
3. Noklikšķiniet uz Jauns.
4. Sarakstā atzīmējiet atlasīto rindu.
    * Varat izmantot filtrus, lai atlasītu kontus, kas atbilst jūsu kritērijiem.  
5. Ievadiet vai atlasiet vērtību laukā No galvenā konta.
6. Ievadiet vai atlasiet vērtību laukā Uz galveno kontu.
7. Noklikšķiniet uz OK.

## <a name="import-main-accounts"></a>Importēt galvenos kontus
1. Noklikšķiniet uz Importēt dimensiju elementus.
    * Galvenie konti tiks importēti izmaksu uzskaitē un izmantoti kā izmaksu elementi.  
2. Noklikšķiniet uz OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Skatīt importētos kontus kā izmaksu elementus
1. Noklikšķiniet uz Skatīt dimensijas elementus.
    * Skatiet importētos virsgrāmatas kontus kā izmaksu elementus, uz kuriem var aizplūst izmaksas jūsu uzņēmumā.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]