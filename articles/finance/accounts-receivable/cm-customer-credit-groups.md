---
title: Debitoru kredītu grupas
description: Šajā rakstā ir sniegta informācija par debitoru kredīta grupām.
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 032e92431946f0a41bf2e52c155e422d4ea0b3b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886521"
---
# <a name="customer-credit-groups"></a>Debitoru kredītu grupas

[!include [banner](../includes/banner.md)]

Varat definēt debitoru grupas, kurām ir kopīgots kredīta limits. Tiek apsvērts arī individuālais kredīta limits, kas noteikts debitora rēķina kontā.

Debitoru kredīta grupas dalībniekus var atlasīt no dažādām juridiskajām personām. Kad jūs pievienojat debitoru debitoru kredīta grupas klientu sarakstam, katra debitora kredīta limita beigu datums tiek mainīts uz grupas piešķirto beigu datumu.

Varat izveidot debitoru kredīta grupas lapā **Debitoru kredīta grupas** (**Kredīta pārvaldība \> Iestatījumi> Debitoru kredīta grupas \> Debitoru kredīta grupas**).

1. Laukos **Grupas numurs** un **Apraksts** ievadiet grupas identifikatoru un aprakstu.
2. Laukos **Kredīta limits** un **Valūta** ievadiet kredīta limitu un valūtu, kas jālieto, kad sistēma pārbauda katra grupas locekļa kredīta limitu.
3. Laukā **Kredīta limita beigu datums** ievadiet datumu, kad kredīta limita termiņš beidzas. Debitora kredīta grupām ir jābūt beigu datumam.

Pēc debitora kredīta grupas iestatīšanas varat pievienot tai debitorus, norādot to juridisko personu un debitora konta ID. Kad pievienojat debitora kredīta grupai jaunu debitoru, sistēma meklē vienu un to pašu debitora kontu visās juridiskajās personās un piedāvā to pievienot debitora kredīta grupai.

Izmantojiet izvēlni **Vecuma bilances**, lai skatītu detalizētu vecumstruktūru bilanču informāciju par visiem debitoru kredītu grupas rēķinu debitoriem. Lapā **Vecumstruktūras bilance** tiek rādīts rēķina debitora kontu vecuma bilanču kopsavilkums.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
