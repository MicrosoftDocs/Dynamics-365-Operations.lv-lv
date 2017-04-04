---
title: "Iekļaut fizisko vērtību"
description: "Lapas Krājumu modeļu grupas kopsavilkuma cilnes Krājumu modelis izvēles rūtiņu Iekļaut fizisko vērtību izmanto, lai norādītu, vai fiziski atjauninātas transakcijas tiek ņemtas vērā, aprēķinot krājuma faktisko vidējo izmaksu cenu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 961f768ac4b0044e138aeaec41c7f915b92c33df
ms.lasthandoff: 03/31/2017


---

# <a name="include-physical-value"></a>Iekļaut fizisko vērtību

Lapas Krājumu modeļu grupas kopsavilkuma cilnes Krājumu modelis izvēles rūtiņu Iekļaut fizisko vērtību izmanto, lai norādītu, vai fiziski atjauninātas transakcijas tiek ņemtas vērā, aprēķinot krājuma faktisko vidējo izmaksu cenu.

Izvēles rūtiņā **Iekļaut fizisko vērtību** ir pieejamas tālāk norādītās vērtības.

| Vērtība    | Rezultāts                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Atlasīts | Gan fiziski, gan finansiāli atjauninātās transakcijas izmanto faktisko vidējo izmaksu cenas aprēķināšanai. |
| Notīrīts  | Lai aprēķinātu faktisko vidējo izmaksu cenu, izmanto tikai finansiāli atjauninātās transakcijas.                                     |

Izvēles rūtiņai atkarībā no izmantotā krājumu modeļa ir nedaudz atšķirīga funkcija.

-   Ja, izmantojot FIFO (pirmais iekšā, pirmais ārā) LIFO (pēdējais iekšā, pirmais ārā) vai LIFO datuma krājumu modeli, ir atlasīta izvēles rūtiņa **Iekļaut fizisko vērtību**, krājumu slēgšana gadījumā tiek veiktas fiziski atjaunināto transakciju korekcijas.
-   Ja, izmantojot šos krājumu modeļus, izvēles rūtiņa **Iekļaut fizisko vērtību** netiek atlasīta, krājumu slēgšanas gadījumā tiek nosegtas tikai finansiāli atjauninātās transakcijas.
-   Ja tiek izmantots svērtā vidējā vai svērtā vidējā datuma krājuma modelis, krājumu slēgšana sedz tikai finansiāli atjauninātās transakcijas neatkarīgi no tā, vai izvēles rūtiņa **Iekļaut fizisko vērtību** ir atlasīta vai nē.

**1. piemērs.** Izvēles rūtiņa** Iekļaut fizisko vērtību** ir atlasīta, un ir saņemti tālāk norādītie pirkšanas pasūtījumi.

-   Pirkšanas pasūtījums par 2 vienību daudzumu un izmaksu cenu USD 10,00, kura pavadzīme ir atjaunināta.
-   Pirkšanas pasūtījums par 3 vienību daudzumu un izmaksu cenu USD 12,00, kura rēķins ir atjaunināts.

Šajā gadījumā faktiskā vidējā izmaksu cena ir USD 11,20, jo gan fiziski, gan finansiāli atjauninātās transakcijas ir izmantotas izmaksu cenas aprēķināšanai. **2. piemērs.** Izvēles rūtiņa **Iekļaut fizisko vērtību** nav atlasīta, un izmaksu cena krājumu iestatījumā ir USD 10,00. Tiek saņemts pirkšanas pasūtījums par 20 vienību daudzumu un izmaksu cenu USD 12,00, kura pavadzīme ir atjaunināta. Kad pārdošanas pasūtījums ir iegrāmatots, iegrāmatotā izmaksu summa ir USD 10,00, jo faktiskā vidējā izmaksu cena neiekļauj fiziski iegrāmatotās transakcijas. **Piezīme.** Salīdzinājumam — ja, iegrāmatojot pārdošanas pasūtījumu, izvēles rūtiņa **Iekļaut fizisko vērtību** šim krājumam ir atlasīta, iegrāmatoto izmaksu summa ir USD 12,00.


