---
title: Organizācijas hierarhija Common Data Service
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Common Data Service
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000738"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organizācijas hierarhija Common Data Service

[!include [banner](../../includes/banner.md)]

Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju. Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.

Lai gan Common Data Service nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi. Kā daļa no Common Data Service integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Common Data Service.

## <a name="data-flow"></a>Datu plūsmas

Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Common Data Service arī turpmāk būs organizācijas hierarhija. Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Common Data Service informatīviem un paplašināmības mērķiem. Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Common Data Service kā vienvirziena datu plūsma no Finance and Operations programmām uz Common Data Service.

![Arhitektūras attēls](media/dual-write-data-flow.png)

Organizācijas hierarhijas elementu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Common Data Service.

## <a name="templates"></a>Veidnes

Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas. Kā redzams šajā tabulā, tiek izveidota elementa karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.

Finance and Operations programmas | Citas Dynamics 365 programmas | apraksts
-----------------------|--------------------------------|---
Organizācijas hierarhijas nolūki | msdyn_internalorganizationhierarchypurposes | Šī veidne nodrošina organizācijas hierarhijas mērķa elementa vienvirziena sinhronizāciju.
Organizācijas hierarhijas tips | msdyn_internalorganizationhierarchytypes | Šī veidne nodrošina organizācijas hierarhijas veida elementa vienvirziena sinhronizāciju.
Organizācijas hierarhija — publicētā | msdyn_internalorganizationhierarchies | Šī veidne nodrošina organizācijas hierarhijas publicētā elementa vienvirziena sinhronizāciju.
Pārvaldības struktūrvienība | msdyn_internalorganizations |
Juridiskas personas | msdyn_internalorganizations |
Juridiskas personas | cdm_companies | Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Iekšējā organizācija

Iekšējās organizācijas informācija Common Data Service tiek iegūta no diviem — **pārvaldības struktūrvienība** un **juridiska persona**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
