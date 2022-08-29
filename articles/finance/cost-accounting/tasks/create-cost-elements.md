---
title: Izmaksu elementu izveide
description: Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos.
author: kfend
ms.date: 08/29/2018
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
ms.openlocfilehash: 9ca826e54171a3dc3582dc5ceb716ac009d45674
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280726"
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
