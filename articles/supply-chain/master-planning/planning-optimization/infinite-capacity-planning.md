---
title: Plānošana ar neierobežotu noslodzi
description: Šajā rakstā ir sniegta informācija par neierobežotas noslodzes plānošanu. Šeit aprakstīti arī pašreizējie funkcionalitātes ierobežojumi.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740010"
---
# <a name="scheduling-with-infinite-capacity"></a>Plānošana ar neierobežotu noslodzi

[!include [banner](../../includes/banner.md)]

Līdzeklis *Neierobežotās noslodzes Plānošana optimizācija* ievieš plānošanu, kuras pamatā ir maršruta informācija. Tas ļauj plānot darbus, balstoties uz plašu maršruta iestatījumu diapazonu. Plānošana aptver bieži izmantotos maršruta iestatījumus, tajā skaitā maršruta operāciju secību vai maršruta operāciju resursu prasības.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Neierobežotās noslodzes plānošanas līdzekli ieslēgt vai izslēgt

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot *neierobežotas noslodzes plānošanu optimizācijas līdzeklim* Līdzekļu [pārvaldības darbvietā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Papildinformāciju par šo līdzekli skatiet tēmā [Plānošana ar iespējā balstītu resursu atlasi](capability-based-scheduling.md).

## <a name="added-functionality"></a>Pievienota funkcionalitāte

Līdzeklis *Neierobežotās noslodzes Plānošana optimizācija* ļauj plānot darbu, kura pamatā ir maršruta informācija. Tāpēc ražošanas procesu plānošanai var izmantot maršruta iestatījumus. Lai gan šai funkcijai ir daži ierobežojumi, kas nav novecojusi vispārējās plānošanas programma, tas atbalsta visizplatītāko funkcionalitāti, kas ir nepieciešama ražošanas scenārijiem.

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

Kopsavilkumā plānošana atbalsta visbiežāk izmantotos scenārijus. Varat izveidot maršrutu, pievienot primārās un sekundārās operācijas, definēt nākamās operācijas, pievienot resursu prasības un pievienot uzstādīšanas laiku un izpildes laiku. Tad sistēma šo informāciju ņems vērā plānošanas laikā.

## <a name="limitations"></a>Ierobežojumi

Ir spēkā tālāk sniegtie ierobežojumi. Ja optimizācijas *līdzekļa plānošanai izmantojat neierobežotās noslodzes* plānošanu:

- Šis līdzeklis atbalsta tikai neierobežotu noslodzi.
- Šis līdzeklis neatbalsta resursu noslodzes funkcionalitāti.
- Šis līdzeklis neietver maršruta brāķi.
- Līdzeklis atbalsta *Ilgumu* tikai kā primāro resursu atlasi.
