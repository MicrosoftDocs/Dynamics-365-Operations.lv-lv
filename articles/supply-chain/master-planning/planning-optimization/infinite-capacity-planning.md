---
title: Plānošana ar neierobežotu noslodzi
description: Šajā tēmā ir sniegta informācija par neierobežotas noslodzes plānošanu Plānošanas optimizēšanai. Šeit aprakstīti arī pašreizējie funkcionalitātes ierobežojumi.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b8f08af3b58e5c0f8480ae540478d60bb8d36193
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469930"
---
# <a name="scheduling-with-infinite-capacity"></a>Plānošana ar neierobežotu noslodzi

[!include [banner](../../includes/banner.md)]

Līdzeklis *Neierobežotās noslodzes Plānošana optimizācija* ievieš plānošanu, kuras pamatā ir maršruta informācija. Tas ļauj plānot darbus, balstoties uz plašu maršruta iestatījumu diapazonu. Plānošana Plānošanas optimizācijai aptver bieži izmantotos maršruta iestatījumus, tostarp maršruta operāciju secību vai maršruta operāciju resursu prasības.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Ieslēgt neierobežotās noslodzes plānošanas līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Vispārējā plānošana*
- **Līdzekļa nosaukums**: *Bezgalīga noslodzes plānošana plānošanas optimizācijai*

Papildinformāciju par šo līdzekli skatiet tēmā [Plānošana ar iespējā balstītu resursu atlasi](capability-based-scheduling.md).

## <a name="added-functionality"></a>Pievienota funkcionalitāte

Līdzeklis *Neierobežotās noslodzes Plānošana optimizācija* ļauj plānot darbu, kura pamatā ir maršruta informācija. Tāpēc ražošanas procesu plānošanai var izmantot maršruta iestatījumus. Lai gan šim līdzeklim ir daži ierobežojumi, kuru iebūvētajam pamatplānojumam nav, tas atbalsta visbiežāk sastopamās funkcionalitātes, kas nepieciešamas ražošanas scenārijiem.

Šis līdzeklis apsver gan *vienkāršus maršrutus*, gan *maršruta tīklus*. Izmantojot lauku **Nākošais** maršruta operācijā, varat iestatīt kompleksus maršrutus, kuriem ir vairāki sākuma punkti un vairākas darbības, kas darbojas paralēli. Plānošanas laikā sistēma apsvērs šāda veida sarežģītas maršruta struktūras.

Turklāt līdzeklis atbalsta *paralēlās operācijas* maršrutos. Izmantojot opcijas *Primārais* un *Sekundārais* maršruta operāciju laukā **Prioritāte**, varat definēt maršruta struktūru, kur viena maršruta operācija ir primārā operācija un cita operācija ir sekundāra. Šajā gadījumā plānošanas laikā sistēma ņems vērā maršruta struktūru.

Plānošanas procesa laikā sistēma ņem vērā arī *resursu prasības*, kas noteiktas operācijai. Sistēma izmanto resursu prasības, lai noteiktu, kuri resursi ir nepieciešami darbības veikšanai. Pašlaik līdzeklis *Neierobežotās noslodzes Plānošanas optimizācija* atbalsta šādus resursu pieprasījumu tipus:

- Resursa tips
- Resurss
- Resursa grupa
- Iespēja (Papildinformāciju par šo līdzekli skatiet tēmā [Plānošana ar iespējā balstītu resursu atlasi](capability-based-scheduling.md).)

> [!NOTE]
>
> - Ja resurss un/vai resursu grupa ir iestatīta uz neierobežotu noslodzi, vispārējā plānošana tos aplūkos kā neierobežotu noslodzi.
> - Prasības, kas saistītas ar personāla resursiem, piemēram, prasmju vai sertifikātu prasības, vēl nav atbalstītas.

Līdzeklis atbalsta arī operāciju rekvizītus **Iestatīšanas laiks** un **Izpildes laiks**. Iestatot šos rekvizītus maršruta operācijā, plānošanas process izveidos atbilstošus iestatījumus un apstrādās darbus.

Kopumā Plānošanas optimizācijas plānošana atbalsta visbiežāk izmantotos scenārijus. Varat izveidot maršrutu, pievienot primārās un sekundārās operācijas, definēt nākamās operācijas, pievienot resursu prasības un pievienot uzstādīšanas laiku un izpildes laiku. Tad sistēma šo informāciju ņems vērā plānošanas laikā.

## <a name="limitations"></a>Ierobežojumi

Uz Plānošanas optimizāciju attiecas šādi ierobežojumi:

- Šis līdzeklis atbalsta tikai neierobežotu noslodzi.
- Šis līdzeklis neatbalsta resursu noslodzes funkcionalitāti.
- Šis līdzeklis neietver maršruta brāķi.
- Līdzeklis atbalsta *Ilgumu* tikai kā primāro resursu atlasi.

Ņemiet vērā, ka līdzeklis *Neierobežotās noslodzes Plānošanas optimizācija* ir uzlabots. Microsoft plāno ieviest atbalstu papildu plānošanas iestatījumiem turpmākajos laidienos.
