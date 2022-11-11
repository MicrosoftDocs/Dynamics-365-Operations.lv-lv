---
title: Krājumu iezīmēšana
description: Šis raksts sniedz informāciju par opcijām, kas ir pieejamas krājumu iezīmēšanai apstiprinātos pasūtījumos.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740608"
---
# <a name="inventory-marking"></a>Krājumu iezīmēšana

[!include [banner](../../includes/banner.md)]

Šis raksts sniedz informāciju par opcijām, kas ir pieejamas krājumu iezīmēšanai apstiprinātos pasūtījumos.

*Marķēšana* tiek izmantota, lai saistītu piedāvājumu un pieprasījumu. Tas līdzinās *piesaistei*, kas norāda, kā vispārējā plānošana paredz segt pieprasījumu. No plānošanas viedokļa galvenā atšķirība ir tā, ka marķēšana ir daudz noturīgāka nekā piesaiste.

Marķēšana tika ieviesta, lai atbalstītu īpašos izmaksu novērtēšanas scenārijus pirmais iekšā, pirmais ārā (FIFO) un pēdējais iekšā, pirmais ārā (LIFO) principiem. Tomēr tagad tas tiek izmantots arī dažiem bezizmaksu scenārijiem. Marķēšana starp piedāvājumu un pieprasījumu nav obligāta un ir gandrīz pastāvīga. Marķēšanu var manuāli noņemt lietotājs, vai to var noņemt, palaižot pārdošanas pasūtījuma rindas izvēršanu, kad tiek izvēlēta opcija **Noņemt marķējumu**.

Piesaiste tiek kontrolēta, veicot vispārējo plānošanu nodrošinājuma periodā, lai saistītu pieprasījumu ar nepieciešamo piedāvājumu. Piesaisti var atjaunināt katrai plānošanas izpildei, lai optimizētu nepieciešamo piedāvājumu, lai apmierinātu pieprasījumu. Kad vispārējā plānošana atjaunina piesaistes informāciju, tā ievēro jebkuru esošo marķējumu.

Piesaiste sākas ar atbilstošu marķēšanu, rīcībā esošām rezervācijām un pasūtījuma rezervācijām šādā secībā:

1. Marķēšana starp pieprasījumu un piedāvājumu
1. Rīcībā esošas rezervācijas
1. Pasūtījuma rezervācijas

Apstiprinot plānoto pasūtījumu, **Apstiprināšanas** dialoglodziņš sniedz lauku **Atjaunot marķējumu**, ko lietojat, lai iestatītu marķēšanas opcijas pasūtījumiem, kas izveidoti apstiprināšanas laikā. Atlasiet vienu no šīm vērtībām:

- *Nē* – netiek lietota krājumu marķēšana.
- *Standarta* – krājumu marķēšana tiek atjaunināta atbilstoši piesaistei. Vajadzību pasūtījums (pieprasījums) ir marķēts pretēji izpildes pasūtījumam (piedāvājums). Ja izpildes pasūtījumā tiek saglabāts kāds daudzums, tas netiek marķēts, un atsauces informācija tiek atstāta tukša. Piemēram, ja pārdošanas pasūtījums par 100 ea ir piesaistīts pirkšanas pasūtījumam 150 ea, atsauces informācija tiks piešķirta tikai pārdošanas pasūtījumam.
- *Paplašināts* – gan vajadzību pasūtījums (pieprasījums), gan izpildes pasūtījums (piedāvājums) ir marķēts, neraugoties uz to, vai izpildes pasūtījumā paliek pāri kāds daudzums. Piemēram, ja pārdošanas pasūtījums par 100 ea ir piesaistīts pirkšanas pasūtījumam 150 ea, atsauces informācija tiks piešķirta tikai pārdošanas pasūtījumam.
- *Viena līmeņa standarts* – tiek izmantots viena līmeņa apzīmējums. Viena līmeņa iezīmēšana atzīmē tikai galveno krājumu, nevis tā materiālu komplekta (MK) komponentus. Tāpēc komponentu piešķiršanu ražošanas pasūtījumiem var uzturēt elastīgu pēc apstiprināšanas. Viena līmeņa atzīmēšana ļauj sistēmai optimizēt pēdējās minūtes pieprasījuma izmaiņas. Standarta *viena* līmeņa iezīmēšanas prasību pasūtījumi tiek iezīmēti pret to izpildes pasūtījumiem, bet izpildes pasūtījumi netiek atzīmēti, ja tiem ir atlikušais daudzums.
- *Viena līmeņa paplašināts* – tiek izmantota viena līmeņa iezīmēšana. Paplašinātā *viena* līmeņa iezīmēšanas prasību pasūtījumi tiek iezīmēti pret to izpildes pasūtījumiem, un izpildes pasūtījumi vienmēr tiek iezīmēti neatkarīgi no tā, vai saglabājas kāds daudzums.

Lai iestatītu sistēmai noklusējuma atzīmēšanas opciju, dodieties uz sadaļu Vispārējās **plānošanas iestatījuma \> vispārējās \> plānošanas parametri**. Pēc tam cilnē **Standarta atjaunināšana** iestatiet lauku Atjaunināt iezīmēšanu **uz** vēlamo opciju.

> [!NOTE]
> Viena *līmeņa standarta un* Viena *līmeņa paplašinātās* opcijas ir pieejamas tikai tad *, ja jūsu* sistēmā ir aktivizēta pasūtījuma pasūtījuma automatizācijas funkcija. Papildinformāciju par šo funkciju un to, kā to iespējot, skatiet [sadaļā "Pasūtīt preču piegādes automatizāciju"](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
