---
title: Organizācijas hierarhija Dataverse
description: Šajā rakstā aprakstīta organizācijas datu integrācija starp finanšu un operāciju programmām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289052"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizācijas hierarhija Dataverse

[!include [banner](../../includes/banner.md)]



Tā kā Dynamics 365 Finanses ir finanšu sistēma, *organizācija* ir galvenā koncepcija un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju. Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.

Lai gan Dataverse nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi. Kā daļa no Dataverse integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Dataverse.

## <a name="data-flow"></a>Datu plūsmas

Biznesa izmaiņas, kas sastāv no finanšu un operāciju Dataverse programmām un turpinās organizācijas hierarhiju. Šī organizācijas hierarhija ir veidota uz finanšu un operāciju programmām, bet tā Dataverse ir atklāta informatīvās un paplašināmības nolūkos. Šajā attēlā redzama organizācijas hierarhijas informācija, kas Dataverse ir atklāta kā vienvirziena datu plūsma no finanšu un operāciju programmām uz Dataverse.

![Arhitektūras attēls.](media/dual-write-data-flow.png)

Organizācijas hierarhijas tabulas kartes ir pieejamas datu vienvirziena sinhronizācijai no finanšu un operāciju programmām uz Dataverse.

## <a name="templates"></a>Veidnes

Organizācija ir cilvēku grupa, kas strādā kopā, lai nodrošinātu biznesa procesu vai sasniegtu mērķi. Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu. Varat definēt šādus iekšējo organizāciju veidus: juridiskas personas, pārvaldības struktūrvienības un darba grupas. Kā redzams šajā tabulā, tiek izveidota tabulu karšu kolekcija, lai sinhronizētu juridiskās personas, pārvaldības struktūrvienības un saistīto orgorizācijas hierarhijas informāciju.

Finance and Operations programmas | Customer engagement programmas     | Apraksts
-----------------------|--------------------------------|---
[Juridiskas personas](mapping-reference.md#102) | cdm_companies | 
[Juridiskas personas](mapping-reference.md#142) | msdyn_internalorganizations |
[Pārvaldības struktūrvienība](mapping-reference.md#143) | msdyn_internalorganizations |
[Organizācijas hierarhija — publicēta](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Šī veidne nodrošina organizācijas hierarhijas publicētās tabulas vienvirziena sinhronizāciju.
[Organizācijas hierarhijas nolūki](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Šī veidne nodrošina organizācijas hierarhijas mērķa tabulas vienvirziena sinhronizāciju.
[Organizācijas hierarhijas tips](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Šī veidne nodrošina organizācijas hierarhijas veida tabulas vienvirziena sinhronizāciju.

## <a name="internal-organization"></a>Iekšējā organizācija

Iekšējās organizācijas informācija Dataverse tiek iegūta no divām tabulām — **Pārvaldības struktūrvienība** un **Juridiska persona**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

