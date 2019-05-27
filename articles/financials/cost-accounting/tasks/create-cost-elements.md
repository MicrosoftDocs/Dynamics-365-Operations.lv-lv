---
title: 'Izmaksu elementu izveide  '
description: Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbaf4f7533d51d554d838e8e9e2aa05ca451298a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543799"
---
# <a name="create-cost-elements"></a>Izmaksu elementu izveide   

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

