---
title: Debitoru kredītu grupas
description: Šajā tēmā ir sniegta informācija par debitora kredītu grupu.
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835320"
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