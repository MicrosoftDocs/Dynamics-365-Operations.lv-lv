---
title: Debitoru kredītu grupas
description: Šajā tēmā ir sniegta informācija par debitora kredītu grupu.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015311"
---
# <a name="customer-credit-groups"></a>Debitoru kredītu grupas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Varat definēt debitoru grupas, kurām ir vienāds kredīta limits. Tiek apsvērts arī individuālais kredīta limits, kas noteikts debitora rēķina kontā.

Debitoru kredīta grupas dalībniekus var atlasīt no dažādām juridiskajām personām. Kad jūs pievienojat debitoru debitoru kredīta grupas klientu sarakstam, katra debitora kredīta limita beigu datums tiek mainīts uz grupas piešķirto beigu datumu.

Varat izveidot debitoru kredīta grupas lapā **Debitoru kredīta grupas** (**Kredīta pārvaldība \> Iestatījumi> Debitoru kredīta grupas \> Debitoru kredīta grupas**).

1. Laukos **Grupas numurs** un **Apraksts** ievadiet grupas identifikatoru un aprakstu.
2. Laukos **Kredīta limits** un **Valūta** ievadiet kredīta limitu un valūtu, kas jālieto, kad sistēma pārbauda katra grupas locekļa kredīta limitu.
3. Laukā **Kredīta limita beigu datums** ievadiet datumu, kad kredīta limita termiņš beidzas. Debitora kredīta grupām ir jābūt beigu datumam.

Pēc debitora kredīta grupas iestatīšanas varat pievienot tai debitorus, norādot to juridisko personu un debitora konta ID. Kad pievienojat debitora kredīta grupai jaunu debitoru, sistēma meklē vienu un to pašu debitora kontu visās juridiskajās personās un piedāvā to pievienot debitora kredīta grupai.

Izmantojiet izvēlni **Vecuma bilances**, lai skatītu detalizētu vecumstruktūru bilanču informāciju par visiem debitoru kredītu grupas rēķinu debitoriem. Lapā **Vecumstruktūras bilance** tiek rādīts rēķina debitora kontu vecuma bilanču kopsavilkums.
