---
title: Plānošanas optimizācijas neizmantotie parametri
description: Šajā tēmā ir uzskaitīti parametri, ko plānošanas optimizācija pašlaik neapsver tās darbības laikā.
author: ChristianRytt
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e1b4e6df2c514b55ec101c0edf22590041628
ms.sourcegitcommit: fcb1aa39e933216dea9e586b552bce6057f416a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2021
ms.locfileid: "7645762"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Plānošanas optimizācijas neizmantotie parametri

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir uzskaitīti parametri, ko plānošanas optimizācija pašlaik neapsver tās darbības laikā. Plānošanas pakalpojums var izlaist parametru, jo, piemēram, saistītā funkcionalitāte vēl nav atbalstīta. Alternatīvi parametrs, iespējams, ir novecojis funkcionālo izmaiņu dēļ.

Tālāk sadaļās ir norādīti parametri, ko Plānošnas optimizācija izmanto noteiktu lapu plānošanai. Tās arī skaidro, kāpēc katrs parametrs netiek izmantots.

## <a name="master-planning-parameters-page"></a>Vispārējās plānošanas parametru lapa

Plānošanas optimizācijā netiek lietoti parametri vai opcijas lapā **Vispārējās plānošanas parametri**:

- **Vispārīgi** cilne:

  - **Pašreizējais prognožu plāns** – gaida atbalstu *Progoze*.
  - **Pašreizējais statiskais vispārējais plāns** - gaida atbalstu *Kopēt statisko uz dinamisko plānu*.
  - **Pašreizējās dinamisks vispārējais plāns** - gaida atbalstu *Kopēt statisko uz dinamisko plānu*.
  - **Kopējiet pabeigto un atjaunināto statisko vispārējo plānu uz dinamisko vispārējo plānu** – gaida atbalstu *Kopēt statisko uz dinamisko plānu*.
  - **Aprēķināto kavējumu sākuma laiks** – gaida atbalstu *Aprēķinātie kavējumi*.
  - **Lietot dinamiskās negatīvās dienas** — Plānošanas optimizācija vienmēr izmanto pieeju *Dinamiskās negatīvās dienas*.
  - **Šīsdienas datumu kalendārs** - gaida atbalstu *Plānošana*.
  - **Kešatmiņas izmantošana** – Microsoft Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Uzdevumu skaits palīga uzdevumu komplektā** — Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Pirmsapstrāde: automātiski filtrēt pēc vienumiem ar tiešo pieprasījumu** — Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Pēcapstrāde: automātiski filtrēt pēc vienumiem ar tiešo pieprasījumu** — Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Pasūtījumu skaits apstiprināšanas komplektā** — Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Pavedienu skaits** — Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Plānošanas procesa taimauts minūtēs** — Azure abonementa konfigurācija apstrādā veiktspējas punktus.
  - **Sākuma laika plānošana** – gaida atbalstu *Plānošana*.

- **Plānoto pasūtījumu** cilne:

  - **Ieejas plūsmas laiks** – gaida atbalstu *Plānošana*.
  - **Ražošana** - gaida atbalstu *Plānošana*.
  - Lauki sadaļā **Projekts** – gaida atbalstu *Plānošana*.

## <a name="coverage-groups-page"></a>Vajadzības grupu lapa

Plānošanas optimizācijā netiek lietoti parametri vai opcijas lapā **Vajadzības grupas**:

- Kopsavilkuma cilne **Vispārīgi**.

  - **Pozitīvās dienas** – gaida atbalstu *Pozitīvas dienas*.
  - **Patērēt rīcībā esošos krājumus** - gaida atbalstu *Rīcībā esošo krājumu patēriņš*.
  - **Izmantojiet norādīto MK vai formulas versiju** – gaida atbalstu *Formulas versijas ar līdzproduktu/blakusproduktu*.
  - **Izmantojiet norādīto maršruta versiju** – gaida atbalstu *Pieprasījums ar noteiktām MK vai maršruta prasībām*.

- **Darbības** kopsavilkuma cilne:

  - **Darbības ziņojums** – gaida atbalstu *Darbības*.
  - **Darbības periods** – gaida atbalstu *Darbības*.
  - **Atlikšanas rezerve** - gaida atbalstu *Darbības*.
  - **Avansa rezerve** - gaida atbalstu *Darbības*.
  - **Pamata datums** – gaida atbalstu *Darbības*.
  - **Avanss** - gaida atbalstu *Darbības*.
  - **Atlikšana** - gaida atbalstu *Darbības*.
  - **Samazinājums** - gaida atbalstu *Darbības*.
  - **Palielinājums** - gaida atbalstu *Darbības*.
  - **Atvasinātas darbības** – gaida atbalstu *Darbības*.

- **Cits** kopsavilkuma cilne:

  - **Sasalšanas periods (dienas)** — Plānošanas optimizācijā nav plānots atbalsts *Sasalšanas periods*.
  - **MK izvēršanas periods (dienas)** – gaida atbalstu *Plānošana*.
  - **Noslodzes plānošanas periods (dienas)** – gaida atbalstu *Plānošana*.
  - **Apstiprinātais pieprasījuma periods (dienas)** – gaida atbalstu *Pieprasījums*.
  - **Prognožu plāna periods** – gaida atbalstu *Progoze*.

- **Aizkaves** kopsavilkuma cilne:

  - **Aprēķinātie kavējumi** – gaida atbalstu *Aprēķinātie kavējumi*.
  - **Aprēķināt kavējumu periodu (dienas)** – gaida atbalstu *Aprēķinātie kavējumi*.

## <a name="item-coverage-page"></a>Lapa Krājumu vajadzība

Plānošanas optimizācijā netiek lietoti parametri vai opcijas lapā **Krājumu vajadzība**:

- **Vispārīgi** cilne:

  - **Plānotā pasūtījuma tips** — plānošanas optimizācija neatbalsta *Kanban* opciju, gaida *Kanban* atbalstu.
  - **Sasalšanas periods (dienas)** — Plānošanas optimizācijā nav plānots atbalsts *Sasalšanas periods*.
  - **MK izvēršanas periods (dienas)** – gaida atbalstu *Plānošana*.
  - **Noslodzes plānošanas periods (dienas)** – gaida atbalstu *Plānošana*.
  - **Apstiprinātais pieprasījuma periods (dienas)** – gaida atbalstu *Pieprasījums*.
  - **Izpildīt minimumu** — Plānošanas optimizācija neatbalsta opcijas *Šodienas datums*, *Pirmā problēma* un *Vajadzības periods*. Tā vienmēr izmanto opciju *Šodienas datumu + sagādes laiku*.
  - **Minimālie periodi** – gaida atbalstu *Minimālo krājumu līmenis*.
  - **Plānošanas formula** - gaida atbalstu *Formulas versijas ar līdzproduktiem/līdzproduktiem*.
  - **Noklusējuma prioritāte** - gaida atbalstu *Formulas versijas ar līdzproduktiem/līdzproduktiem*.
  - **Pašreizējā prioritāte** - gaida atbalstu *Formulas versijas ar līdzproduktiem/līdzproduktiem*.
  - **Datums mainīts** - gaida atbalstu *Formulas versijas ar līdzproduktiem/līdzproduktiem*.
  - **Patērēt rīcībā esošos krājumus** - gaida atbalstu *Rīcībā esošo krājumu patēriņš*.

- Cilne **Izpildes laiks**:

  - **Pirkuma laiks** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.
  - **Ražošanas laiks** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.
  - **Pārsūtīšanas laiks** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.
  - **Darba dienas** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.

## <a name="master-plans-page"></a>Lapa Vispārējie plāni

Plānošanas optimizācijā netiek lietoti parametri vai opcijas lapā **Vispārējie plāni**:

- Kopsavilkuma cilne **Vispārīgi**.

  - **Iekļaut rīcībā esošos krājumus** - gaida atbalstu *Rīcībā esošo krājumu patēriņš*.
  - **Pārlabot rīcībā esošo** - gaida atbalstu *Rīcībā esošo krājumu patēriņš*.
  - **Patērēt rīcībā esošos krājumus** - gaida atbalstu *Rīcībā esošo krājumu patēriņš*.
  - **Iekļaut krājumu darījumus** - gaida atbalstu *Rīcībā esošo krājumu patēriņš*.
  - **Iekļaut pārdošanas piedāvājumus** – gaida atbalstu *Pārdošanas piedāvājumi*.
  - **Iekļaut piedāvājumu pieprasījumus** — gaida atbalstu *Piedāvājuma pieprasījumi*.
  - **Izmantot glabāšanas laika datumus** — gaida atbalstu *Glabāšanas laiks*.
  - **Iekļaut nepārtraukto plānu** — gaida atbalstu *Nepārtrauktā plānošana*.
  - **Metodes plānošana** – gaida atbalstu *Plānošana*.
  - **Ierobežoti rekvizīti** – gaida atbalstu *Plānošana*.
  - **Atpakaļplānošanas noslodzes periods** – gaida atbalstu *Plānošana*.
  - **Ierobežotā noslodze** – gaida atbalstu *Plānošana*.
  - **Ierobežotās noslodzes periods** – gaida atbalstu *Plānošana*.
  - **Ierobežota noslodze sastrēguma resursiem** – gaida atbalstu *Plānošana*.
  - **Noslodzes periods sastrēguma resursiem** – gaida atbalstu *Plānošana*.
  - **Plānotie pasūtījumi** – Plānošanas optimizācijā tiek lietotas fiksētas numuru sērijas.
  - **Sesija** – Plānošanas optimizācijā tiek lietotas fiksētas numuru sērijas.
  - **Nepārtrauktības plāns** – Plānošanas optimizācijā tiek lietotas fiksētas numuru sērijas.

- **Periods dienās** kopsavilkuma cine:

  - **Sasalšana** — Plānošanas optimizācijā nav plānots atbalsts *Sasalšanas periods*.
  - **Eksplozija** - gaida atbalstu *Plānošana*.
  - **Prognožu plāns** – gaida papildu atbalstu *Progoze*.
  - **Noslodze** – gaida atbalstu *Plānošana*.
  - **Nepārtrauktības plāns** — gaida atbalstu *Nepārtrauktā plānošana*.
  - **Darbības ziņojums** – gaida atbalstu *Darbības*.
  - **Aprēķinātie kavējumi** – gaida papildu atbalstu *Aprēķinātie kavējumi*.
  - **Secība** - gaida atbalstu *Ražošana*.

- **Aprēķinātās aizkaves** kopsavilkuma cilne:

  - **Nodrošiniet, lai plānotie pasūtījumi nebūtu izveidoti pirms vispārējā plānošanas izpildes datuma** – gaida atbalstu *Aprēķinātās aizkaves*.
  - **Pievienot aprēķināto aizkavi pieprasījuma datumam** (sadaļā **Plānotie pirkšanas pasūtījumi** ) – gaida atbalstu *Aprēķinātās aizkaves*.
  - **Pievienot aprēķināto aizkavi pieprasījuma datumam** (sadaļā **Plānotie ražošanas pasūtījumi** ) – gaida atbalstu *Aprēķinātās aizkaves*.
  - **Pievienot aprēķināto aizkavi pieprasījuma datumam** (sadaļā **Plānotā pārsūtīšana** ) – gaida atbalstu *Aprēķinātās aizkaves*.
  - **Pievienot aprēķināto aizkavi pieprasījuma datumam** (sadaļā **Plānotais Kanban** ) – gaida atbalstu *Aprēķinātās aizkaves*.

- **Secība** kopsavilkuma cilne:

  - **Plānoto pasūtījumu secība pēc vispārējās plānošanas** – gaida atbalstu *Secība*.
  - **Intervāla tips** – gaida atbalstu *Secība*.
  - **Perioda tips** – gaida atbalstu *Secība*.
  - **Intervālu skaits kampaņas ciklā** – gaida atbalstu *Secība*.

## <a name="released-product-details-page"></a>Izlaistās preces detalizētas informācijas lapa

Plānošanas optimizācijā netiek lietotas parametru opcijas lapā **Izlaistā produkta dati**:

- **Inženieris** kopsavilkuma cilne:

  - **Ražošanas veids** — Plānošanas optimizācija neatbalsta opciju *Plānošanas krājumi*, kas gaida abalstu *Plānošanas krājumi*.

## <a name="default-order-settings-page"></a>Lapa Pasūtījuma noklusējuma iestatījumi

Plānošanas optimizācijā netiek lietotas parametru opcijas lapā **Noklusējuma pasūtījuma iestatījumi**:

- Kopsavilkuma cilne **Pirkuma pasūtījums**:

  - **Pirkuma izpildes laiks** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.
  - **Darba dienas** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.

- **Krājumi** kopsavilkuma cilne:

  - **Piegādes datuma kontrole** — Plānošanas optimizācija neatbalsta *CTP* opciju, gaida atbalstu *CTP*.
  - **Krājuma izpildes laiks** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.
  - **Darba dienas** — Planning Optimization versijās, kuras ir vecākas par 2021. gada 6. augusta laidienu, Planning Optimization izmanto šo parametru, lai aprēķinātu pareizos pasūtījuma un piegādes datumus, taču tas nesaglabā aprēķināto izpildes laiku plānotajā pasūtījumā. Jaunākās versijās pakalpojums arī izmanto aprēķināto izpildes laiku, lai iestatītu lauku **Izpildes laiks** un **Darba dienas** atbilstoši plānotajam pasūtījumam.

## <a name="working-time-calendars-page"></a>Lapa Darba laika kalendāri

Plānošanas optimizācijā netiek lietots parametrs lapā **Darba laika kalendāri**:

- **Pamatkalendārs** – gaida atbalstu *Pamatkalendārs*.

## <a name="batch-disposition-master-page"></a>Lapa Partijas atgriešanas šablons

Plānošanas optimizācijā netiek lietots parametrs lapā **Partijas izvietojuma šablons**:

- **Iestatīšana** kopsavilkuma cilne:

  - **Atskaitāms** - gaida atbalstu *Partijas atgriešanas kodi*.
