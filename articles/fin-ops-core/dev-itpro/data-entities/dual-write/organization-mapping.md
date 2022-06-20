---
title: Organizācijas hierarhija Dataverse
description: Šajā rakstā aprakstīta organizācijas datu integrācija starp Finanšu un operāciju programmām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4edaf5b9c50e9d8781ff703328ac786d71ee782
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884737"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizācijas hierarhija Dataverse

[!include [banner](../../includes/banner.md)]



Tā kā Dynamics 365 Finanses ir finanšu sistēma, *organizācija* ir galvenā koncepcija un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju. Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.

Lai gan Dataverse nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi. Kā daļa no Dataverse integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Dataverse.

## <a name="data-flow"></a>Datu plūsmas

Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Dataverse arī turpmāk būs organizācijas hierarhija. Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Dataverse informatīviem un paplašināmības mērķiem. Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Dataverse kā vienvirziena datu plūsma no Finance and Operations programmām uz Dataverse.

![Arhitektūras attēls.](media/dual-write-data-flow.png)

Organizācijas hierarhijas tabulas kartes ir pieejamas datu vienvirziena sinhronizācijai no Finanšu un operāciju programmām uz Dataverse.

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
