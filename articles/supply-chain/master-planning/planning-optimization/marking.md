---
title: Krājumu marķēšana, izmantojot plānošanas optimizāciju
description: Šajā tēmā sniegta informācija par opcijām, kas pieejamas krājumu marķēšanai apstiprinātos pasūtījumos, kad izmantojat plānošanas optimizāciju.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263354"
---
# <a name="inventory-marking-with-planning-optimization"></a>Krājumu marķēšana, izmantojot plānošanas optimizāciju

[!include [banner](../../includes/banner.md)]

Šajā tēmā sniegta informācija par opcijām, kas pieejamas krājumu marķēšanai apstiprinātos pasūtījumos, kad izmantojat plānošanas optimizāciju.

*Marķēšana* tiek izmantota, lai saistītu piedāvājumu un pieprasījumu. Tas līdzinās *piesaistei*, kas norāda, kā vispārējā plānošana paredz segt pieprasījumu. No plānošanas viedokļa galvenā atšķirība ir tā, ka marķēšana ir daudz noturīgāka nekā piesaiste.

Marķēšana tika ieviesta, lai atbalstītu īpašos izmaksu novērtēšanas scenārijus pirmais iekšā, pirmais ārā (FIFO) un pēdējais iekšā, pirmais ārā (LIFO) principiem. Tomēr tagad tas tiek izmantots arī dažiem bezizmaksu scenārijiem. Marķēšana starp piedāvājumu un pieprasījumu nav obligāta un ir gandrīz pastāvīga. Marķēšanu var manuāli noņemt lietotājs, vai to var noņemt, palaižot pārdošanas pasūtījuma rindas izvēršanu, kad tiek izvēlēta opcija **Noņemt marķējumu**.

Piesaiste tiek kontrolēta, veicot vispārējo plānošanu nodrošinājuma periodā, lai saistītu pieprasījumu ar nepieciešamo piedāvājumu. Piesaisti var atjaunināt katrai plānošanas izpildei, lai optimizētu nepieciešamo piedāvājumu, lai apmierinātu pieprasījumu. Kad vispārējā plānošana atjaunina piesaistes informāciju, tā ievēro jebkuru esošo marķējumu.

Piesaiste sākas ar atbilstošu marķēšanu, rīcībā esošām rezervācijām un pasūtījuma rezervācijām šādā secībā:

1. Marķēšana starp pieprasījumu un piedāvājumu
1. Rīcībā esošas rezervācijas
1. Pasūtījuma rezervācijas

Apstiprinot plānoto pasūtījumu, **Apstiprināšanas** dialoglodziņš sniedz lauku **Atjaunot marķējumu**, ko lietojat, lai iestatītu marķēšanas opcijas pasūtījumiem, kas izveidoti apstiprināšanas laikā. Atlasiet vienu no šīm vērtībām:

- **Nē** – netiek lietota krājumu marķēšana.
- **Standarta** – krājumu marķēšana tiek atjaunināta atbilstoši piesaistei. Vajadzību pasūtījums (pieprasījums) ir marķēts pretēji izpildes pasūtījumam (piedāvājums). Ja izpildes pasūtījumā tiek saglabāts kāds daudzums, tas netiek marķēts, un atsauces informācija tiek atstāta tukša. Piemēram, ja pārdošanas pasūtījums par 100 ea ir piesaistīts pirkšanas pasūtījumam 150 ea, atsauces informācija tiks piešķirta tikai pārdošanas pasūtījumam.
- **Paplašināts** – gan vajadzību pasūtījums (pieprasījums), gan izpildes pasūtījums (piedāvājums) ir marķēts, neraugoties uz to, vai izpildes pasūtījumā paliek pāri kāds daudzums. Piemēram, ja pārdošanas pasūtījums par 100 ea ir piesaistīts pirkšanas pasūtījumam 150 ea, atsauces informācija tiks piešķirta tikai pārdošanas pasūtījumam.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]