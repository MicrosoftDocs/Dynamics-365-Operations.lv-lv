---
title: Inventory Visibility atbalsts WMS krājumiem
description: Šajā rakstā ir aprakstīts krājumu redzamības atbalsts krājumiem, kas ir iespējoti noliktavas pārvaldības procesiem (WMS krājumiem).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066616"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Inventory Visibility atbalsts WMS krājumiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts krājumu redzamības atbalsts krājumiem, kas ir iespējoti noliktavas pārvaldības procesiem (WMS). Funkcija, kas pievieno šo iespēju krājumu redzamībai, tiek nosaukta kā Uzlabots *WMS*.

## <a name="wms-items"></a>WMS krājumi

WMS krājums ir krājums, kas ir iespējots WMS un apstrādāts noliktavā, kas arī ir iespējota WMS.

Papildinformāciju par WMS un noliktavas **pārvaldības moduli** Microsoft Dynamics 365 Supply Chain Management skatiet noliktavas [pārvaldības pārskatā](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Funkcionalitātes tvērums

Krājumu redzamības papildu WMS līdzeklis vērsts uz rīcībā esošo krājumu daudzuma aprēķiniem, kas balstīti uz rīcībā esošiem vaicājumiem. Šis līdzeklis nav paredzēts, lai ļautu izmantot krājumu redzamību, lai vispārīgi pārvaldītu noliktavas apstrādes darbības. Krājumu redzamība pakļauj lietotājiem noliktavas raksturīgās koncepcijas. Šeit sniegti daži šo koncepciju piemēri:

- Rezervāciju hierarhija
- Vai krājums vai noliktava ir iespējota WMS
- Vienību secību grupas ID
- Noliktavai specifiskie procesi, piemēram, kravas, kravas, kopumi un darbs

Krājumu redzamība pieņem šo informāciju, balstoties uz datiem, kas tiek sūtīti no Piegādes ķēžu pārvaldības. WMS specifiskie dati (citiem vārdiem, no tabulas `WHSInventReserve`) nav redzami lietotājiem.

Kad krājumu redzamībai izmantojat papildu WMS līdzekli, visi vaicājuma rezultāti būs identiski rezultātiem, kas iegūti vaicājumos, kuri tiek veikti tieši Piegādes ķēžu pārvaldībā. Tomēr tie nebūs identiski to vaicājumu rezultātiem, kas veikti, izmantojot mobilo programmu Noliktavas pārvaldība, jo mobilā programma izmanto nedaudz citu aprēķina loģiku.

## <a name="when-to-use-the-feature"></a>Kad izmantot šo līdzekli

Krājumu redzamībai ieteicams izmantot papildu WMS līdzekli scenārijos, kuros ir spēkā visi šie nosacījumi:

- Jūs sinhronizējat Piegādes ķēdes pārvaldības datus ar krājumu redzamību.
- Jūs izmantojat WMS piegādes ķēžu pārvaldībā.
- Lietotāji veic rezervācijas WMS krājumiem līmeņos, kas nav noliktavas līmenī (piemēram, jo izmantojat noliktavas darbu).

Citos scenārijos rīcībā esošo vaicājumu rezultāti būs tādi paši, neatkarīgi no tā, vai ir iespējota krājumu redzamības funkcija Uzlabotais WMS. Turklāt veiktspēja būs labāka, ja šajā scenārijā šo līdzekli neiespējosiet, jo ir mazāk aprēķinu un tiek mazāk papildu atbalsta.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Iespējot papildu WMS līdzekli krājumu redzamībai

Lai iespējotu papildu WMS līdzekli krājumu redzamībai, sekojiet šiem soļiem.

1. Piesakieties Piegādes ķēžu pārvaldībā kā administrators.
1. Atveriet līdzekļu [pārvaldības darbvietu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet šādas funkcijas šādā secībā:

    1. *Pievienojumprogrammas Krājumu redzamība integrācija*
    1. *Iespējot noliktavas preces krājumu redzamības pakalpojumā*

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Krājumu un noliktavas pārvaldības parametri**.
1. Cilnē Iespējot **WMS vienumus** iestatiet opciju Iespējot **WMS krājumus** uz *Jā*.
1. Pierakstieties programmā Power Apps.
1. Atveriet konfigurācijas **lapu** un pēc tam cilnē Funkciju **pārvaldība** grieziet funkciju *AdvancedWHS*.
1. Piegādes ķēdes pārvaldībā dodieties uz krājumu pārvaldības **periodisko \> uzdevumu krājumu \> redzamības integrāciju**.
1. Darbību rūtī atlasiet Atspējot, lai **uz laiku** atspējotu krājumu redzamību.
1. Darbību rūtī atlasiet Iespējot **, lai** atkārtoti aktivizētu krājumu redzamību. Pievienojumprogramma ir pārlādēta, un tagad ir aktivizēta jaunā funkcija. Ar WMS saistītie dati sāk darboties sinhronizēti ar krājumu redzamību.

## <a name="query-on-hand-quantities-of-wms-items"></a>Vaicāt rīcībā esošos WMS krājumu daudzumus

Lai vaicātu WMS krājumiem, [izmantojiet to pašu programmas programmēšanas interfeisu (API) un ziņojumu sintaksi](inventory-visibility-api.md), kas tiek lietota krājumiem, kas nav WMS. Nav jānorāda, vai krājums ir WMS krājums vai krājums, kas nav WMS krājums. Krājumu redzamība automātiski izšķir krājumus, pamatojoties uz saglabātajiem datiem.

WMS krājumu vaicājumu rezultāti pamatā ir tādi paši kā rezultāti krājumiem, kas nav WMS. Vienīgā atšķirība ir tā, ka šādi fiziskie pasākumi no `fno` datu avota tiek aprēķināti, pamatojoties uz WMS loģiku Piegādes ķēžu pārvaldībā:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Visi citi fiziskie pasākumi tiek aprēķināti tāpat, kā krājumu redzamības līdzeklis Uzlabotais WMS.

Lai iegūtu sīkāku informāciju par to, kā darbojas WMS krājumu rīcībā esošie aprēķini, [skatiet krājumu rezervācijas noliktavas pārvaldības rakstā](https://www.microsoft.com/download/details.aspx?id=43284).

Datu elementi, kas tiek eksportēti Dataverse, vēl nevar atjaunināt WMS krājumu daudzumu. Datu elementi rādītie daudzumi ir pareizi gan krājumiem, kas nav WMS, gan daudzumiem, kurus neietekmē WMS loģika (t.i., `AvailPhysical` apjomi izņemot`AvailOrdered`, `ReservPhysical``ReservOrdered``fno` un datu avots).

WMS krājumu daudzumu izmaiņas, kas tiek glabātas Piegādes ķēdes pārvaldības datu avotā, ir aizliegtas. Attiecībā uz citām krājumu redzamības funkcijām šis ierobežojums tiek ieviests, lai palīdzētu novērst konfliktus.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Vieglās rezervācijas WMS krājumiem krājumu redzamība

Parasti tiek atbalstītas [vieglās rezervācijas](inventory-visibility-reservations.md) WMS krājumiem. Ar WMS saistītos fiziskos krājumus var iekļaut vieglās rezervēšanas aprēķinos. 

Zināmā ierobežojumā rezervācijas *aprēķināšanai pieejamais* ierobežojums pašlaik netiek atbalstīts WMS krājumiem. Tāpēc, ja virs pašreizējām dimensijām ir rezervēšana, kas notiek viegli, *rezervēšanai pieejamais* aprēķins nav pareizs. Vieglās rezervācijas netiks ietekmētas, ja **vieglās rezervēšanas API** ir atspējota [opcijaCheckAvailForReserv](inventory-visibility-api.md#create-one-reservation-event).

Šis ierobežojums attiecas arī uz funkcijām un pielāgojumiem, kas balstīti uz vieglās rezervēšanas (piemēram, sadalījuma).

## <a name="calculate-available-to-promise-quantities"></a>Aprēķināt pieejamos daudzumus solīšanai

WMS krājumiem [risinājums pilnībā atbalsta pieejamo](inventory-visibility-available-to-promise.md) solīšanai (ATP). Varat definēt ATP aprēķinus, neņemot vērā WMS raksturīgās detaļas.
