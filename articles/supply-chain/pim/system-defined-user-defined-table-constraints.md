---
title: Sistēmas definēti un lietotāja definēti tabulas ierobežojumi
description: Šajā rakstā ir aprakstīti lietotāja un sistēmas definēta preces konfigurācijas modeļa komponentu tabulas divi ierobežojumu veidi. Tabulas ierobežojumi attiecas uz atļauto atribūtu kombināciju matricām, kur katra rinda nosaka vienu iespējamo atribūta vērtību kopu.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 120ffe8e64629d0f99ac036d6ae6a933575903e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987158"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Sistēmas definēti un lietotāja definēti tabulas ierobežojumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti lietotāja un sistēmas definēta preces konfigurācijas modeļa komponentu tabulas divi ierobežojumu veidi. Tabulas ierobežojumi attiecas uz atļauto atribūtu kombināciju matricām, kur katra rinda nosaka vienu iespējamo atribūta vērtību kopu.

Tabulas ierobežojumi attiecas uz to atribūtu kombināciju matricām, kas atļauti komponentiem preču konfigurēšanas modelī. Katra tabulas rinda nosaka vienu iespējamo atribūtu vērtību kopu. Preču konfigurēšanas modelī ir iespējams noteikt divu veidu ierobežojumus.

-   **Izteiksmes ierobežojums** — izveidojiet izteiksmi, kas nosaka attiecības starp atribūtiem, lai nodrošinātu, ka preces konfigurācijas laikā var atlasīt tikai saderīgas vērtības.
-   **Tabulas ierobežojums** — izveidot tabulu, kas definē visas kombinācijas, kas atļautas norādītajai atribūtu kopai. Ir pieejami divu veidu tabulas ierobežojumi: lietotāja definēti tabulas ierobežojumi un sistēmas definēti tabulas ierobežojumi.

Šajā rakstā aprakstīti lietotāja definēti un sistēmas definēti tabulas ierobežojumi komponentiem preces konfigurācijas modelī.

## <a name="user-defined-table-constraints"></a>Lietotāja definēti tabulas ierobežojumi
Lietotāja definēts tabulas ierobežojums ir matricas veids, ko izmanto, lai aprakstītu tādu atribūtu vērtību kombināciju kopas, ko definē atribūtu veidi. Piemēram, ja ražojat skaļruņus, lietotāja definētā tabulas ierobežojumā varat iekļaut korpusa apdares kolonnas un priekšējo režģi. Korpusa apdares atribūta veidam ir četras vērtības, bet priekšējā režģa atribūta veidam — trīs vērtības. Tādēļ, ja ierobežojumi netiek izmantoti, ir iespējamas 4 × 3 = 12 kombinācijas. Tomēr šajā piemērā ir atļautas tikai sešas kombinācijas, kā parādīts nākamajā tabulā. Šī Informācija tiek parādīta lapas **Rediģēt tabulas ierobežojumu** cilnē **Atļautās kombinācijas**.

| Korpusa apdare | Priekšējais režģis |
|----------------|-------------|
| melna          | melna       |
| melna          | Metāla       |
| Ozola            | melna       |
| Rožkoka       | Balta       |
| Balta          | melna       |
| Balta          | Balta       |

Lietotāja definētos tabulas ierobežojumus nosaka ar statisku tabulu ievadi, kas darbojas tādā pašā veidā, kā izteiksmes ierobežojums. Izmantojot lietotāja definētu tabulas ierobežojumu, tabulas parasti ir vieglāk izveidot, izprast un uzturēt, nekā garus izteiksmes ierobežojumus.

## <a name="system-defined-table-constraints"></a>Sistēmas definēti tabulas ierobežojumi
Sistēmas definēts tabulas ierobežojums izveido dinamisku kartēšanu starp atribūta veidu un lauku tabulā. Ja sistēmas definētu tabulas ierobežojumu iekļauj preces konfigurācijas modelī, kartēšana nodrošina, ka tiks paradīti nevis atribūta veida vērtības, bet gan tabulas dati. Rezultātā tiek iegūts dinamisks ierobežojums, jo tabulas saturu var modificēt (piemēram, izmantojot citus moduļus).  

Izveidojot sistēmas definētu tabulas ierobežojumu, atlasiet tabulu, ja vēlaties papildus definēt izmantojamu vaicājumu, un pēc tam piesaistiet atribūtu veidus atlasītās tabulas laukiem. Lauku veidiem jāatbilst atribūtu veidiem.  

Pirms tabulas ierobežojumu var izmantot preces konfigurācijas modelī, tabulas ierobežojums jāiekļauj ierobežojumā vienā no modeļu komponentiem. Procedūra paredzēta, lai izveidotu jaunu ierobežojumu, atlasītu tabulas ierobežojuma veidu, un pēc tam atlasītu tabulas lietojamo ierobežojuma definīciju. Visbeidzot visi tabulas ierobežojuma lauki jākartē uz atribūtiem preces konfigurācijas modelī.

<a name="additional-resources"></a>Papildu resursi
--------

[Pārskats par preču konfigurācijas modeļiem](product-configuration-models.md)



