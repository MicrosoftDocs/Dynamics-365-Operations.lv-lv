---
title: Reisa statusa iestatījumi
description: Šajā tēmā ir aprakstīts, kā izveidot statusa vērtības, ko lietotāji var piešķirt reisiem.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 80433c17ed9d790d88b20ecc253c8e4459ffea10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829792"
---
# <a name="voyage-status-setup"></a>Reisa statusa iestatījumi

[!include [banner](../../includes/banner.md)]

Lapā **Reisu statusi** izveidojiet statusa vērtību kopu, ko lietotāji var piešķirt reisiem. Lietotāji var piešķirt reisa statusa vērtības visiem reisa līmeņiem: reisa, nosūtīšanas konteinera, folio, pirkšanas pasūtījuma un krājuma (pirkšanas rindas un pārsūtīšanas pasūtījuma rindas). Tos lieto diviem nolūkiem:

- Informēt lietotāju par reisa, pārvadāšanas konteinera, folio, pirkšanas pasūtījuma vai krājuma statusu (pirkšanas rindas un pārsūtīšanas pasūtījuma rindas).
- Ierobežojiet izmaksu zonas izmantošanu, novēršot modificēšanu vai dzēšanu.

Lai iestatītu reisa statusus, dodieties uz **Kopējās izmaksas \> Iestatījumi \> Reisa statusi**. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu statusus.

Katrai izmaksu zonai ir sava reisa statusu kopa un hierarhija. Tādēļ **Reisa statusu** lapas **Izmaksu apgabala** laukā vispirms ir jāatlasa izmaksu zona, kurai vēlaties skatīt vai izveidot reisu statusus. Pēc tam katram reisa statusam iestatiet tālāk sniegtajā tabulā aprakstītos laukus, kā nepieciešams. Ņemiet vērā, ka reisa statusu var automātiski mainīt arī sistēmas notikumi, piemēram, noteikumi, kas izveidoti, izmantojot izsekošanas kontroles centru.

| Lauks | Apraksts |
|---|---|
| Reisa statuss | Ievadiet reisa statusa nosaukumu. |
| Apraksts | Ievadiet reisa statusa aprakstu. |
| Modificē | Atzīmējiet šo izvēles rūtiņu, ja lietotājiem ir atļauts modificēt reisus ar šo statusu. |
| Delete | Atzīmējiet šo izvēles rūtiņu, ja lietotājiem ir atļauts dzēst reisus ar šo statusu. |
| Obligāts | Atzīmējiet šo izvēles rūtiņu, lai padarītu reisa statusu par obligātu, lai to nevar izlaist. |
| Pamatelements | Lietojiet šo lauku, lai izveidotu hierarhiju starp statusa vērtībām. Reisu statusus (manuāli vai automātiski) hierarhijā var mainīt tikai uz leju no pamatobjekta statusa uz vienu no tā bērnu statusiem.

> [!NOTE]
> Jāiestata tikai konkrēti reisa statusi, ko izmanto jūsu organizācija. Tipiski reisu statusi ietver *Apstiprināts*, *Tranzīta preces*, *Saņemts*, *Gatavs izmaksu skaitīšanai* un *Izmaksas*. Tomēr, iespējams, ir citi statusi.
