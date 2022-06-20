---
title: Inventory Visibility atbalsts WHS krājumiem
description: Šajā dokumentā ir aprakstīts krājumu redzamības atbalsts krājumiem, kas ir iespējoti papildu noliktavas procesiem (WHS krājumiem).
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
ms.openlocfilehash: ec2254d6cf203216acea88fdfb54ad491abdeb49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895675"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Inventory Visibility atbalsts WHS krājumiem

[!include [banner](../includes/banner.md)]

Šajā dokumentā ir aprakstīts krājumu redzamības atbalsts krājumiem, kas ir iespējoti papildu noliktavas procesiem (WHS krājumiem). Funkcija, kas pievieno šo iespēju krājumu redzamībai, tiek nosaukta kā Uzlabotā *WHS*.

## <a name="whs-items"></a>WHS krājumi

WHS krājums ir krājums, kas ir iespējots papildu noliktavas procesiem (WHS) un apstrādāts noliktavā, kas arī ir iespējota whS.

Papildinformāciju par WHS un noliktavas **vadības moduli** programmā Microsoft Dynamics 365 Supply Chain Management skatiet noliktavas [pārvaldības pārskatā](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Funkcionalitātes tvērums

Krājumu redzamības papildu līdzeklis WHS vērsts uz rīcībā esošo daudzumu aprēķiniem, kas balstīti uz rīcībā esošiem vaicājumiem. Šis līdzeklis nav paredzēts, lai ļautu izmantot krājumu redzamību, lai vispārīgi pārvaldītu noliktavas apstrādes darbības. Krājumu redzamība pakļauj lietotājiem noliktavas raksturīgās koncepcijas. Šeit sniegti daži šo koncepciju piemēri:

- Rezervāciju hierarhija
- Vai krājums vai noliktava ir iespējota, ja izmanto noliktavas pārvaldības procesu
- Vienību secību grupas ID
- Noliktavai specifiskie procesi, piemēram, kravas, kravas, kopumi un darbs

Krājumu redzamība pieņem šo informāciju, balstoties uz datiem, kas tiek sūtīti no Piegādes ķēžu pārvaldības. WHS specifiskie dati (citiem vārdiem, no tabulas `WHSInventReserve`) lietotājiem nav redzami.

Izmantojot uzlaboto WHS līdzekli krājumu redzamībai, visi vaicājuma rezultāti būs identiski rezultātiem, kas iegūti no vaicājumiem, kas tiek veikti tieši Piegādes ķēžu pārvaldībā. Tomēr tie nebūs identiski to vaicājumu rezultātiem, kas veikti, izmantojot mobilo programmu Noliktavas pārvaldība, jo mobilā programma izmanto nedaudz citu aprēķina loģiku.

## <a name="when-to-use-the-feature"></a>Kad izmantot šo līdzekli

Krājumu redzamībai ieteicams izmantot līdzekli Uzlabotā WHS gadījumos, kuros ir spēkā visi šie nosacījumi:

- Jūs sinhronizējat Piegādes ķēdes pārvaldības datus ar krājumu redzamību.
- Jūs izmantojat WHS piegādes ķēžu pārvaldībā.
- Lietotāji veic rezervācijas WHS krājumiem citos līmeņos, nevis noliktavas līmenī (piemēram, ja izmantojat noliktavas darbu).

Citos scenārijos rīcībā esošo vaicājumu rezultāti būs tādi paši, neatkarīgi no tā, vai ir iespējota krājumu redzamības papildu WHS funkcija. Turklāt veiktspēja būs labāka, ja šajā scenārijā šo līdzekli neiespējosiet, jo ir mazāk aprēķinu un tiek mazāk papildu atbalsta.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Iespējojiet papildu WHS līdzekli krājumu redzamībai

Lai iespējotu uzlaboto WHS līdzekli krājumu redzamībai, izpildiet šīs darbības.

1. Piesakieties Piegādes ķēžu pārvaldībā kā administrators.
1. Atveriet līdzekļu [pārvaldības darbvietu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet šādas funkcijas šādā secībā:

    1. *Pievienojumprogrammas Krājumu redzamība integrācija*
    1. *Iespējot noliktavas preces krājumu redzamības pakalpojumā*

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Krājumu un noliktavas pārvaldības parametri**.
1. Cilnē Iespējot **WHS krājumus** iestatiet opciju Iespējot **WHS krājumus** uz *Jā*.
1. Pierakstieties programmā Power Apps.
1. Atveriet konfigurācijas **lapu** un pēc tam cilnē Funkciju **pārvaldība** grieziet funkciju *AdvancedWHS*.
1. Piegādes ķēdes pārvaldībā dodieties uz krājumu pārvaldības **periodisko \> uzdevumu krājumu \> redzamības integrāciju**.
1. Darbību rūtī atlasiet Atspējot, lai **uz laiku** atspējotu krājumu redzamību.
1. Darbību rūtī atlasiet Iespējot **, lai** atkārtoti aktivizētu krājumu redzamību. Pievienojumprogramma ir pārlādēta, un tagad ir aktivizēta jaunā funkcija. Ar WHS saistītie dati tiek sākti sinhronizēt ar krājumu redzamību.

## <a name="query-on-hand-quantities-of-whs-items"></a>Vaicāt rīcībā esošos WHS krājumu daudzumus

Lai vaicātu WHS krājumiem, izmantojiet [to pašu programmas programmēšanas interfeisu (API)](inventory-visibility-api.md) un ziņojumu sintaksi, kas tiek izmantota krājumiem, kas nav WHS. Nav jānorāda, vai krājums ir WHS krājums vai whS krājums. Krājumu redzamība automātiski izšķir krājumus, pamatojoties uz saglabātajiem datiem.

WhS krājumu vaicājumu rezultāti pamatā ir tādi paši kā to krājumu rezultāti, kas nav WHS krājumi. Vienīgā atšķirība ir tā, ka šādi fiziskie pasākumi no `fno` datu avota tiek aprēķināti, pamatojoties uz WHS loģiku piegādes ķēžu pārvaldībā:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Visi citi fiziskie pasākumi tiek aprēķināti tāpat, kā krājumu redzamības papildu WHS funkcija.

Papildinformāciju par to, kā whS krājumu rīcībā esošo krājumu rīcībā esošo krājumu aprēķini darbojas, [skatiet noliktavas pārvaldības](https://www.microsoft.com/download/details.aspx?id=43284) darba lapas sadaļā Rezervācijas.

Datu elementi, kas tiek eksportēti Dataverse, vēl nevar atjaunināt WHS krājumu daudzumus. Datu elementi rādītie daudzumi ir pareizi gan krājumiem, kas nav WHS, gan daudzumiem, kurus neietekmē WHS loģika (t.i., `AvailPhysical``AvailOrdered` apjomi izņemot, `ReservPhysical``ReservOrdered``fno` un datu avotā).

To WHS krājumu daudzumu izmaiņas, kas tiek glabāti piegādes ķēdes pārvaldības datu avotā, ir aizliegtas. Attiecībā uz citām krājumu redzamības funkcijām šis ierobežojums tiek ieviests, lai palīdzētu novērst konfliktus.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Vieglās rezervācijas WHS krājumiem krājumu redzamība

Noliktavas krājumu [vieglās rezervācijas](inventory-visibility-reservations.md) parasti tiek atbalstītas. Ar WHS saistītos fiziskos pasākumus var iekļaut vieglās rezervēšanas aprēķinos. 

Zināmā ierobežojumā rezervēšanas *aprēķināšanai pieejamais* daudzums pašlaik netiek atbalstīts WHS krājumiem. Tāpēc, ja virs pašreizējām dimensijām ir rezervēšana, kas notiek viegli, *rezervēšanai pieejamais* aprēķins nav pareizs. Vieglās rezervācijas netiks ietekmētas, ja **vieglās rezervēšanas API** ir atspējota [opcijaCheckAvailForReserv](inventory-visibility-api.md#create-one-reservation-event).

Šis ierobežojums attiecas arī uz funkcijām un pielāgojumiem, kas balstīti uz vieglās rezervēšanas (piemēram, sadalījuma).

## <a name="calculate-available-to-promise-quantities"></a>Aprēķināt pieejamos daudzumus solīšanai

Risinājums pilnībā atbalsta solīšanai [(ATP)](inventory-visibility-available-to-promise.md) WHS krājumiem. Varat definēt ATP aprēķinus, neveicot attiecībā uz WHS raksturīgām detaļām.
