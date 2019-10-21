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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182029"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organizācijas hierarhija Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju. Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.

Lai gan Common Data Service nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi. Kā daļa no Common Data Service integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Common Data Service.

## <a name="data-flow"></a>Datu plūsmas

Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Common Data Service arī turpmāk būs organizācijas hierarhija. Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Common Data Service informatīviem un paplašināmības mērķiem. Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Common Data Service kā vienvirziena datu plūsma no Finance and Operations programmām uz Common Data Service.

![Arhitektūras attēls](media/dual-write-data-flow.png)

## <a name="templates"></a>Veidnes

Organizācijas hierarhijas elementu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Iekšējais organizācijas hierarhijas nolūks

Šī veidne nodrošina organizācijas hierarhijas nolūka elementa vienvirziena sinhronizāciju no Finance and Operations uz citām Dynamics 365 programmām.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Iekšējais organizācijas hierarhijas veids

Šī veidne nodrošina organizācijas hierarhijas veida elementa vienvirziena sinhronizāciju no Finance and Operations uz citām Dynamics 365 programmām.

<!-- ![architecture image](media/dual-write-type.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NOSAUKUMS | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Iekšējā organizācijas hierarhija

Šī veidne nodrošina organizācijas hierarhijas publicētā elementa vienvirziena sinhronizāciju no Finance and Operations uz citām Dynamics 365 programmām.

<!-- ![architecture image](media/dual-write-organization.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Iekšējā organizācija

Iekšējās organizācijas informācija Common Data Service tiek iegūta no diviem — **pārvaldības struktūrvienība** un **juridiska persona**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Pārvaldības struktūrvienība

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NOSAUKUMS | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Juridiska persona

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NOSAUKUMS | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
nav | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Uzņēmums

Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![architecture image](media/dual-write-company.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NOSAUKUMS | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
