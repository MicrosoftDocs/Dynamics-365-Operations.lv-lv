---
title: Inventory Visibility atbalsts WMS krājumiem
description: Šajā rakstā ir aprakstīts krājumu redzamības atbalsts krājumiem, kas ir iespējoti noliktavas pārvaldības procesiem (WMS krājumiem).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762759"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Inventory Visibility atbalsts WMS krājumiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts krājumu redzamības atbalsts krājumiem, kas ir iespējoti noliktavas pārvaldības procesiem (WMS). Līdzeklis, kas pievieno šo iespēju krājumu redzamībai, tiek nosaukts par *Papildu WMS*.

## <a name="wms-items"></a>WMS vienumi

WMS krājums ir krājums, kas ir iespējots WMS un apstrādāts noliktavā, kurā ir iespējota arī WMS.

Papildinformāciju par WMS un **moduli Noliktavas pārvaldība** korporācijā Microsoft Dynamics 365 Supply Chain Management skatiet rakstā [Noliktavas pārvaldības pārskats](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Funkcijas darbības joma

Papildu WMS līdzeklis krājumu redzamībai koncentrējas uz rīcībā esošiem daudzuma aprēķiniem, kuru pamatā ir rīcībā esošie vaicājumi. Šis līdzeklis nav paredzēts, lai jūs varētu izmantot krājumu redzamību, lai pārvaldītu noliktavas apstrādes darbības kopumā. Krājumu redzamība neatklāj noliktavai raksturīgas koncepcijas tās lietotājiem. Šeit ir daži šo jēdzienu piemēri:

- Rezervāciju hierarhija
- Vai krājumam vai noliktavai ir iespējots WMS
- Vienību secību grupas ID
- Noliktavai raksturīgi procesi, piemēram, sūtījumi, kravas, viļņi un darbs

Krājumu redzamība izsecina šo informāciju, pamatojoties uz datiem, kas tiek nosūtīti no Supply Chain Management. WMS raksturīgie dati (citiem vārdiem sakot, dati no `WHSInventReserve` tabulas) lietotājiem nav redzami.

Ja krājumu redzamībai izmantojat uzlaboto WMS līdzekli, visi vaicājumu rezultāti būs identiski to vaicājumu rezultātiem, kas veikti tieši programmatūrā Supply Chain Management. Tomēr tie nebūs identiski to vaicājumu rezultātiem, kas veikti, izmantojot mobilo programmu Noliktavas pārvaldība, jo mobilā programma izmanto nedaudz atšķirīgu aprēķinu loģiku.

## <a name="when-to-use-the-feature"></a>Kad izmantot šo funkciju

WMS līdzekli krājumu redzamībai ieteicams izmantot scenārijos, kuros ir izpildīti visi šie nosacījumi:

- Jūs sinhronizējat Supply Chain Management datus ar krājumu redzamību.
- Jūs izmantojat WMS programmatūrā Supply Chain Management.
- Lietotāji rezervē WMS krājumus līmeņos, kas ir zemāki par noliktavas līmeni (piemēram, numura zīmes līmenī, jo jūs apstrādājat noliktavas darbu).

Citos scenārijos rīcībā esošo vaicājumu rezultāti būs vienādi neatkarīgi no tā, vai ir iespējots uzlabotais WMS līdzeklis krājumu redzamībai. Turklāt veiktspēja būs labāka, ja šajos scenārijos neiespējosit šo funkciju, jo ir mazāk aprēķinu un mazāk pieskaitāmo izmaksu.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>WMS līdzekļa iespējošana krājumu redzamībai

Lai iespējotu WMS līdzekli krājumu redzamībai, veiciet tālāk norādītās darbības.

1. Piesakieties Supply Chain Management kā administrators.
1. [Atveriet darbvietu Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet šādus līdzekļus šādā secībā:

    1. *Pievienojumprogrammas Krājumu redzamība integrācija*
    1. *Iespējot noliktavas preces krājumu redzamības pakalpojumā*

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Krājumu un noliktavas pārvaldības parametri**.
1. Cilnē Enable **WMS Items (Iespējot WMS vienumus) opcijai** Enable WMS Items (Iespējot WMS **vienumus**) iestatiet vērtību *Yes*.
1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. **Atveriet lapu Konfigurācija** un pēc tam **cilnē Līdzekļu pārvaldība** ieslēdziet *līdzekli AdvancedWHS*.
1. Sadaļā Supply Chain Management dodieties uz sadaļu **Krājumu pārvaldības \> periodisko uzdevumu \> krājumu redzamības integrācija**.
1. Darbību rūtī atlasiet **Atspējot**, lai īslaicīgi atspējotu krājumu redzamību.
1. Darbību rūtī atlasiet **Iespējot**, lai atkārtoti iespējotu krājumu redzamību. Pievienojumprogramma tiek atkārtoti ielādēta, un jaunā funkcija tagad ir iespējota. Ar WMS saistītie dati tiek sinhronizēti ar krājumu redzamību.

## <a name="query-on-hand-quantities-of-wms-items"></a>Vaicājiet rīcībā esošos WMS vienumu daudzumus

Lai vaicātu par WMS vienumiem, izmantojiet to pašu [lietojumprogrammu programmēšanas interfeisu (API) un ziņojumu sintaksi](inventory-visibility-api.md), ko izmantojat vienumiem, kas nav WMS vienumi. Jums nav jānorāda, vai vienums ir WMS vienums vai vienums, kas nav WMS. Krājumu redzamība automātiski atšķir vienumus, pamatojoties uz saglabātajiem datiem.

WMS vienumu vaicājumu rezultāti būtībā ir tādi paši kā rezultāti vienumiem, kas nav WMS vienumi. Vienīgā atšķirība ir tā, ka tālāk norādītie `fno` fiziskie mērījumi no datu avota tiek aprēķināti, pamatojoties uz WMS loģiku programmatūrā Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Visi pārējie fiziskie mēri tiek aprēķināti tieši tāpat, kā tie tiek aprēķināti, ja WMS līdzeklis krājumu redzamībai ir atspējots.

Detalizētu informāciju par to, kā darbojas rīcībā esošie WMS krājumu aprēķini, skatiet tehniskajā [dokumentā Rezervācijas noliktavas pārvaldībā](https://www.microsoft.com/download/details.aspx?id=43284).

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Rīcībā esošs saraksta skats un datu elements WMS vienumiem

Lapas **Krājumu redzamības kopsavilkuma** iepriekšēja ielāde nodrošina entītijas Rīcībā esošs indeksa *vaicājuma iepriekšējas ielādes rezultātu* skats. Atšķirībā no *entītijas Krājumu kopsavilkums*, *entītija Rīcībā esošie indeksa vaicājuma iepriekšējas ielādes rezultāti* nodrošina rīcībā esošo krājumu sarakstu precēm kopā ar atlasītajām dimensijām. Krājumu redzamība sinhronizē iepriekš ielādētos kopsavilkuma datus ik pēc 15 minūtēm.

Ja izmantojat krājumu redzamību ar WMS vienumiem un vēlaties skatīt rīcībā esošo WMS vienumu sarakstu, ieteicams iespējot *līdzekli Iepriekš ielādēt krājumu redzamības kopsavilkumu* (skatiet arī [Racionalizēta rīcībā esoša vaicājuma](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) iepriekšēja ielāde). Atbilstošais datu elements saglabā Dataverse vaicājuma iepriekšējās ielādes rezultātu, kas tiek atjaunināts ik pēc 15 minūtēm. Datu elementa nosaukums ir `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Entītija Dataverse ir tikai lasāma. Varat skatīt un eksportēt datus entītijās Krājumu redzamība, bet **nemodificēt tos**.

Izmaiņas WMS krājumu daudzumos, kas tiek glabāti Supply Chain Management datu avotā (`fno`), ir aizliegtas. Šī darbība atbilst citu krājumu redzamības līdzekļu darbībai. Šis ierobežojums tiek piemērots, lai palīdzētu novērst konfliktus.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS vienumu saderība citām funkcijām krājumu redzamības sadaļā

[Tiek atbalstītas WMS vienumu mīkstās rezervācijas](inventory-visibility-reservations.md) un [krājumu sadale](inventory-visibility-allocation.md). Ar WMS saistītos fiziskos mērus varat iekļaut nesaistošo rezervāciju un sadalījuma aprēķinos.

## <a name="calculate-available-to-promise-quantities"></a>Aprēķiniet solīšanai pieejamos daudzumus

Risinājums pilnībā atbalsta [pieejamo solījumu (ATP)](inventory-visibility-available-to-promise.md) WMS vienumiem. Varat definēt ATP aprēķinus, neuztraucoties par WMS specifisko informāciju.
