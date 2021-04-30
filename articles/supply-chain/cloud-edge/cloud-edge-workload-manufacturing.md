---
title: Ražošanas izpildes darba slodzes mākoņas un malas mēroga vienībām
description: Šajā tēmā aprakstīts, kā ražošanas izpildes darba slodzes darbojas ar mākoņa un malas mēroga vienībām.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a6d6979093c67d2d89b88678712f4c0205c63194
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899099"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Ražošanas izpildes darba slodzes mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ražošanas izpildes darba slodze ir pieejama priekšskatījumā šajā brīdī.
> Dažas biznesa funkcionalitātes netiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas.

Ražošanas izpildē mēroga vienības nodrošina šādas iespējas:

- Iekārtu operatori un ražotnes uzraudzības iestādes var piekļūt operāciju ražošanas plānam.
- Iekārtu operatori var uzturēt plāna atjaunināšanu, izpildot diskrētus un procesa ražošanas darbus.
- Ražotnes vadītājs var koriģēt darbības plānu.
- Darbinieki var piekļūt ierašanās un aiziešanas reģistrācijas laikam un apmeklējumam, lai nodrošinātu pareizu darbinieka algas aprēķinu.

Šajā tēmā aprakstīts, kā ražošanas izpildes darba slodzes darbojas ar mākoņa un malas mēroga vienībām.

## <a name="the-manufacturing-lifecycle"></a>Ražošanas cikls

Kā parādīts sekojošajā attēlā, ražošanas cikls ir sadalīts trīs fāzēs: *Plānošana*, *Izpilde* un *Pabeigšana*.

[![Ražošanas izpildes fāzes, kad tiek izmantota viena vide](media/mes-phases.png "Ražošanas izpildes fāzes, kad tiek izmantotas viena vide")](media/mes-phases-large.png)

Fāzē _Plānošana_ ietver produkta definīciju, plānošanu, pasūtījuma izveidi un plānošanu un izlaišanu. Izlaišanas darbība norāda pāreju no fāzes _Plānošana_ uz fāzi _Izpilde_. Kad ražošanas pasūtījums tiek izlaists, ražošanas pasūtījuma darbi būs redzami ražotnē un gatavi izpildei.

Kad ražošanas darbs ir atzīmēts kā pabeigts, tas tiek pārvietots no fāzes _Izpilde_ uz fāzi _Pabeigšana_. Fāzē _Pabeigšana_ reģistrācijas no fāzes *Izpilde* tiek veiktas, izmantojot apstiprinājuma darbplūsmu, kur tās tiek aprēķinātas, apstiprinātas un pārsūtītas. Šajā brīdī ražošanas pasūtījums ir pabeigts. Tāpēc tiek ģenerēts darbinieku apmaksas pamats.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Izpildes fāzes sadalīšana atsevišķā darba slodzē

Kā redzams ilustrācijā, kad tiek izmantotas mēroga vienības, fāze _Izpilde_ tiek sadalīta kā atsevišķa darba slodze.

[![Ražošanas izpildes fāzes, kad tiek izmantotas mēroga vienības](media/mes-phases-workloads.png "Ražošanas izpildes fāzes, kad tiek izmantotas mēroga vienības")](media/mes-phases-workloads-large.png)

Tagad modelis pāriet no viena gadījuma instalācijas modeļa uz modeli, kura pamatā ir centrmezgls un mēroga vienības. Fāzes _Plānošana_ un _Pabeigšana_ tiek izpildītas kā biroja operācijas, un ražošanas izpildes darba slodze darbojas uz mēroga vienībām. Dati tiek pārsūtīti asinhroni starp centrmezglu un mēroga vienībām.

Kad ražošanas pasūtījums tiek izlaists centrmezglā, visi dati, kas nepieciešami ražošanas darbu apstrādei, tiek pārsūtīti uz mēroga vienību. Šie dati ietver ražošanas pasūtījumus, ražošanas maršrutus, materiālu komplektus un produktus. Dati, kas nav saistīti ar ražošanas pasūtījumu (piemēram, netiešās aktivitātes, kavējumu kodi un ražošanas parametri), arī tiek pārsūtīti no centrmezgla uz mēroga vienību. Parasti dati, kas rodas no centrmezgla un kas tiek pārsūtīti uz mēroga vienību, var tikt izveidoti vai atjaunināti tikai centrmezglā. Piemēram, jaunu kavējuma kodu vai netiešo aktivitāti nevar izveidot mēroga vienībās,&mdash;tos var izmantot tikai reģistrācijai. Reģistrācijas, kas veiktas mēroga vienībās izpildes laikā, pēc tam tiek pārsūtītas uz centrmezglu, kur tiek apstrādāti laika un klātbūtnes apstiprinājums, krājumi un finanšu atjauninājumi.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Ražošanas izpildes uzdevumi, kurus var izpildīt darba slodzēm

Tālāk norādītos ražošanas izpildes uzdevumus pašlaik var palaist darba noslodzēm, kad tiek izmantotas mēroga vienības:

- Ierašanās, pieteikšanās, ierašanās un kavējums
- Sākt darbu
- Komplekta darbi
- Pārskata norise
- Ziņot par lūžņiem
- Netiešā aktivitāte
- Pārtraukums

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Darbs ar ražošanas izpildes darba slodzēm centrmezglā

Parasti procesi, kas ir nepieciešami ražošanas izpildes darba slodzēm, tiek palaisti automātiski, lai pēc nepieciešamības uzturētu centrmezglu un visas mēroga vienības sinhronizācijā. Tomēr, ja rodas problēmas, varat manuāli aktivizēt neapstrādāto reģistrāciju apstrādi, kas tiek saņemta no darba slodzēm un/vai pārbaudīt reģistrācijas apstrādes žurnālu.

### <a name="manually-process-raw-registrations"></a>Apstrādāt neapstrādātās reģistrācijas manuāli

Pakalpojumā Supply Chain Management pakešuzdevums tiek palaists automātiski, lai apstrādātu visas reģistrācijas, kas saņemtas no darba slodzēm. Šis darbs izveido vajadzīgos ražošanas žurnālus un reģistrācijas žurnāla ierakstus, kad reģistrācija tiek apstrādāta pabeigtam darbam uz darba slodzes.

Lai gan darbs parasti tiek palaists automātiski, to var palaist manuāli jebkurā laikā, piesakoties centrmezglā un dodoties uz **Ražošanas kontrole \> Periodiskie uzdevumie \> Biroja darba slodzes pārvaldība \> Apstrādāt neapstrādātās reģistrācijas**.

### <a name="check-the-raw-registration-processing-log"></a>Pārbaudīt neapstrādāto reģistrāciju apstrādes žurnālu

Lai pārskatītu reģistrācijas apstrādes žurnālu, piesakieties centrmezglam un dodieties uz **Ražošanas kontrole \> Periodiskie uzdevumi \> Biroja darba slodzes pārvaldība \> Neapstrādāto reģistrāciju apstrādes žurnāls**. Lapa **Neapstrādāto reģistrāciju apstrādes žurnāls** rāda apstrādāto neapstrādāto reģistrāciju sarakstu un katras reģistrācijas statusu.

![Neapstrādāto reģistrāciju apstrādes žurnāla lapa](media/mes-processing-log.png "Neapstrādāto reģistrāciju apstrādes žurnāla lapa")

Jūs varat strādāt ar jebkuru reģistrāciju sarakstā, atlasot to un pēc tam atlasot vienu no šīm pogām darbības rūtī:

- **Apstrādāt** – manuāli apstrādāt atlasīto reģistrāciju. Šī darbība var būt noderīga, ja darbs _Apstrādāt neapstrādātu reģistrāciju_ nav palaists vai arī tas neizdevās.
- **Atcelt** – atcelt atlasīto reģistrāciju.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Darbs ar ražošanas izpildes darba slodzēm mēroga vienībā

Parasti procesi, kas ir nepieciešami ražošanas izpildes darba slodzēm, tiek palaisti automātiski, lai pēc nepieciešamības uzturētu centrmezglu un visas mēroga vienības sinhronizācijā. Tomēr, ja rodas problēmas, varat pārbaudīt to pasūtījumu vēsturi, kas ir apstrādāti apjoma vienībās, vai manuāli palaist darbu _Ražošanas centrmezgls mēroga vienību ziņojuma procesoram_.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Skatīt to ražošanas darbu vēsturi, kas ir apstrādāti mēroga vienībās

Lai pārskatītu to ražošanas darbu vēsturi, kas ir apstrādāti mēroga vienībās, piesakieties apjoma mērvienību iekārtā un dodieties uz **Ražošanas kontrole \> Periodiskie uzdevumi \> Biroja darba slodzes pērvaldība \> Ražošanas darbu apstrādes vēsture**. Lapā **Ražošanas darbu apstrādes vēsture** tiek parādīta ražošanas pasūtījumu apstrādes vēsture mēroga vienībā. Jūs varat strādāt ar jebkuru ražošanas pasūtījumu sarakstā, atlasot to un pēc tam atlasot vienu no šīm pogām darbības rūtī:

- **Apstrādāt** – manuāli apstrādāt atlasīto ražošanas pasūtījumu.
- **Atcelt** – atcelt atlasīto ražošanas pasūtījumu.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Ražošanas centrmezgls mēroga vienības ziņojuma procesora darbām

Darbs _Ražošanas centrmezgls mēroga vienības ziņojuma procesoram_ apstrādā datus no centrmezgla uz mēroga vienību. Šis darbs tiek automātiski sākts, kad tiek izvietota ražošanas izpildes darba slodze. Tomēr to var palaist manuāli jebkurā laikā, pārejot uz **Ražošanas kontrole \> Periodiskie uzdevumi \> Biroja darba slodzes pārvadība \> Ražošanas centrmezgls mēroga vienības ziņojuma procesoram**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
