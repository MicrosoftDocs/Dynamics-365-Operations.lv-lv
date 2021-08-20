---
title: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
description: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760928"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Nevar apstiprināt sūtījumu, jo nav izdoti krājumi

Kļūdas kods: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Daļa noslodzei %1 nepieciešamo krājumu vēl nav izdoti un pārvietoti uz galīgo nosūtīšanas novietojumu.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Kravu vai sūtījumu nevar apstiprināt tās pašreizējā stāvoklī, jo var pastāvēt viens no tālāk norādītajiem nosacījumiem:

- Saistītais darbs vēl nav izdots un pārvietots uz beigu nosūtīšanas vietu.
- Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.
- Izmantojot kopuma veidnes konteinerizāciju, novietojuma direktīva tika konfigurēta ar iepakošanas vietu kā galīgo nosūtīšanas vietu.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.
- Atceliet darba ID, kas izveidoti ar iepakošanas novietojumu kā galīgās nosūtīšanas vietu, pārkonfigurējiet novietojuma direktīvu un atkārtoti ielādējiet kravu.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt

Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.
1. Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Atceliet darba ID, kas izveidoti ar iepakošanas novietojumu kā galīgās nosūtīšanas vietu, pārkonfigurējiet novietojuma direktīvu un atkārtoti ielādējiet kravu

Izmantojiet šo procedūru, lai atceltu darba ID, kuru iepakošanas vieta ir galīgā izvietošanas vieta ar automatizētu konteinerizēšanu.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Tiek atvērts dialogs **Atcelt darbu**. Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt. Atlasītā darba ID vērtībai **Darba statuss** jābūt *Atvērts*, *Procesā*, *Atcelts*, *Apvienots* vai *Slēgts*.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.
1. Pēc nepieciešamības, atkārtojiet šo procedūru pārējiem darba ID.

Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).

Izmantojiet šo procedūru, lai pārkonfigurētu novietojuma direktīvu, jo, iestatot kopuma veidni, iepakošanas vieta netiks izmantota kā galīgā nosūtīšanas vieta.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.
1. Atlasiet novietojuma direktīvu, ko izmantojat automatizētai konteinerizēšanai.
1. Kopsavilkuma cilnes rīkjoslā **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialogā cilnē **Diapazons** atrodiet rindu, kur **Lauks** ir iestatīts uz *Novietojuma profils*, un pārbaudiet, vai laukā **Kritēriji** rindai nav iestatīts novietojuma profils ar **Novietojuma veidu** *Iepakojums*. Koriģēt lauku **Kritēriji**, lai labotu pēdējo izvietošanas novietojumu.

Izmantojiet šo procedūru, lai atkārtoti ielādētu kravu un izveidotu darba ID ar pareizo galīgo nosūtīšanas vietu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Sadaļā **Kravas** atrodiet kravu, kas ir jāizlaiž.
1. Sadaļas **Kravas** rīkjoslā atlasiet opciju **Pārvietot \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto kravu uz noliktavu.
1. Pēc nepieciešamības, atkārtojiet šo procedūru pārējam kravām.
