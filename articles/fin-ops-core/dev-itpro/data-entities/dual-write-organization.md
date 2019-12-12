---
title: Organizācijas hierarhija Common Data Service
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769664"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organizācijas hierarhija Common Data Service

[!include [banner](../includes/banner.md)]

Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju. Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.

Lai gan Common Data Service nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi. Kā daļa no Common Data Service integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Common Data Service.

## <a name="data-flow"></a>Datu plūsmas

Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Common Data Service arī turpmāk būs organizācijas hierarhija. Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Common Data Service informatīviem un paplašināmības mērķiem. Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Common Data Service kā vienvirziena datu plūsma no Finance and Operations programmām uz Common Data Service.

![Arhitektūras attēls](media/dual-write-data-flow.png)

## <a name="templates"></a>Veidnes

Organizācijas hierarhijas elementu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Common Data Service.

## <a name="templates"></a>Veidnes

Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas. Kā redzams šajā tabulā, tiek izveidota elementa karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.

Finance and Operations | Citas Dynamics 365 programmas | Apraksts
-----------------------|--------------------------------|---
Organizācijas hierarhijas nolūki | msdyn_internalorganizationhierarchypurposes | Šī veidne nodrošina organizācijas hierarhijas mērķa elementa vienvirziena sinhronizāciju.
Organizācijas hierarhijas tips | msdyn_internalorganizationhierarchytypes | Šī veidne nodrošina organizācijas hierarhijas veida elementa vienvirziena sinhronizāciju.
Organizācijas hierarhija — publicētā | msdyn_internalorganizationhierarchies | Šī veidne nodrošina organizācijas hierarhijas publicētā elementa vienvirziena sinhronizāciju.
Pārvaldības struktūrvienība | msdyn_internalorganizations | 
Juridiskas personas | msdyn_internalorganizations | 
Juridiskas personas | cdm_companies | Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju.


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Iekšējā organizācija

Iekšējās organizācijas informācija Common Data Service tiek iegūta no diviem — **pārvaldības struktūrvienība** un **juridiska persona**.

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]
