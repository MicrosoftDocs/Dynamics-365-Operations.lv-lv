---
title: Organizācijas hierarhija Dataverse
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Dataverse
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 30826bf69525a85bede6ec0b64ec1a579aea26a0a6c487583739ad3fcb787a28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769249"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizācijas hierarhija Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju. Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.

Lai gan Dataverse nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi. Kā daļa no Dataverse integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Dataverse.

## <a name="data-flow"></a>Datu plūsmas

Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Dataverse arī turpmāk būs organizācijas hierarhija. Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Dataverse informatīviem un paplašināmības mērķiem. Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Dataverse kā vienvirziena datu plūsma no Finance and Operations programmām uz Dataverse.

![Arhitektūras attēls.](media/dual-write-data-flow.png)

Organizācijas hierarhijas tabulu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Dataverse.

## <a name="templates"></a>Veidnes

Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas. Kā redzams šajā tabulā, tiek izveidota tabulas karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.

Finance and Operations programmas | Customer engagement programmas     | Apraksts
-----------------------|--------------------------------|---
[Juridiskas personas](mapping-reference.md#102) | cdm_companies | Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju.
[Juridiskas personas](mapping-reference.md#142) | msdyn_internalorganizations |
[Pārvaldības struktūrvienība](mapping-reference.md#143) | msdyn_internalorganizations |
[Organizācijas hierarhija — publicēta](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Šī veidne nodrošina organizācijas hierarhijas publicētās tabulas vienvirziena sinhronizāciju.
[Organizācijas hierarhijas nolūki](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Šī veidne nodrošina organizācijas hierarhijas mērķa tabulas vienvirziena sinhronizāciju.
[Organizācijas hierarhijas tips](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Šī veidne nodrošina organizācijas hierarhijas veida tabulas vienvirziena sinhronizāciju.

## <a name="internal-organization"></a>Iekšējā organizācija

Iekšējās organizācijas informācija Dataverse tiek iegūta no divām tabulām — **Pārvaldības struktūrvienība** un **Juridiska persona**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
