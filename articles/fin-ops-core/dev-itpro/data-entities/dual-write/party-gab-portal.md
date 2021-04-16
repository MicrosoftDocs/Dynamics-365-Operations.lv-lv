---
title: Power Portal izmantošana kopā ar pušu datu modeli
description: Šajā tēmā aprakstītas izmaiņas Power Portal tīmekļa lomās, kas ir veiktas, jo puses datu modelis ir dubultrakstīšanā.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833094"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Power Portal izmantošana kopā ar pušu datu modeli

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Dubultās rakstīšanas lietojumprogrammas orhestrācijas risinājuma versijā 2.0.999.0 un jaunākās ir iekļautas datu modeļa izmaiņas pušu un globālajā adrešu grāmatā tabulām Konts un Kontaktpersona. Izmaiņas ļauj attiecības daudzi pret daudziem, kas atbalsta detalizētus biznesa scenārijus. Šīs izmaiņas neatbalsta portāla tīmekļa lomas, tostarp klientu portāls, kas tiek piegādāts ārpus saraksta vai kas pastāv vidē pirms dubultrakstīšanas instalēšanas. Lai tīmekļa lomas darbotos kā paredzēts, ir jāizveido jaunas tīmekļa lomas, izmantojot jauno datu modeli. 

Kopumā tabulu mijiedarbības veids ir mainījies, bet tabulas atļaujas debitora portālā nav mainītas. Šajā tēmā skaidrots, kā izveidot jaunas tīmekļa lomas, kas darbojas ar jauno uzlaboto datu modeli.

Šajā diagrammā parādītas tabulas attiecības **bez** puses un globālās adrešu grāmatas datu modeļa:

   ![bez puses modeļa](media/without-party-model.PNG)

Šajā diagrammā parādītas tabulas attiecības **ar** puses un globālās adrešu grāmatas datu modeli:

   ![ar puses modeļi](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Izveidot jaunu tabulas atļauju

Lai izveidotu šīs jaunās tabulas atļaujas, rīkojieties šādi:

1. Pieteikties [Power Apps](https://make.powerapps.com) un doties uz jūsu programmām.
2. Atlasiet savu portāla pārvaldības programmu.
3. Līdzjoslā atlasiet **Drošība > Tabulas atļaujas**.

    Jums ir jāizveido trīs jaunas atļaujas:

    + Savienojums kontaktpesona ar pusi
    + Savienojums puse ar kontu
    + Savienojums konts ar pasūtījumu

4. Izveidojiet un saglabājiet jaunu atļauju savienojumam kontaktpersona ar pusi, iestatot šādus parametrus:

    + **Nosaukums**: savienojums puse ar kontu (vai jūsu izvēle)
    + **Tabulas nosaukums**: msdyn_contactforparty
    + **Tīmekļa vietne**: Debitoru portāls
    + **Tvērums**: kontaktpersona
    + **Privilēģijas**: atlasīt visu
    + **Tīmekļa lomas**: autentificētie lietotāji, debitora pārstāvis (vai jūsu izvēle)

5. Izveidojiet un saglabājiet jaunu atļauju savienojumam puse ar kontu, iestatot šādus parametrus:

    + **Nosaukums**: savienojums puse ar kontu (vai jūsu izvēle)
    + **Tabulas nosaukums**: konts
    + **Tīmekļa vietne**: Debitoru portāls
    + **Tvērums**: pamatelements
    + **Privilēģijas**: atlasīt visu
    + **Vecāktabavas atļauja**: savienojumam kontaktpersona ar pusi

6. Izveidojiet un saglabājiet jaunu atļauju savienojumam konts ar pasūtījumu, iestatot šādus parametrus:

    + **Nosaukums**: savienojums konts ar pasūtījumu (vai jūsu izvēle)
    + **Tabulas nosaukums**: pārdošanas pasūtījums
    + **Tīmekļa vietne**: Debitoru portāls
    + **Tvērums**: pamatelements
    + **Privilēģijas**: atlasīt visu
    + **Vecāktabavas atļauja**: savienojumam puse ar kontu

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
