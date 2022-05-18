---
title: Krājumu darbību papildinformācija
description: Šajā tēmā sniegts pārskats par darbību informācijas lapu, kurā ir sniegta detalizēta informācija par atlasīto krājumu darbību.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735879"
---
# <a name="inventory-transaction-details"></a>Krājumu darbību papildinformācija

Izmantojiet lapu **Detalizēta informācija par** darbībām, lai skatītu jebkuras atlasītās krājumu darbības detaļas.

## <a name="open-the-transaction-details-page"></a>Atvērt lapu Detalizēta informācija par darījumu

Lai atvērtu lapu **Detalizēta informācija par** darbībām, sekojiet šiem soļiem.

1. Dodieties uz **vaicājumiem \> par krājumu vadību un pārskatiem \>**.
1. Atlasiet darbību, kuru vēlaties pārbaudīt.
1. Darbību rūtī atlasiet darbības **detaļas**.

## <a name="fasttabs-overview"></a>Kopsavilkuma cilni apskats

Lapa **Detalizēta informācija** par darbībām ir sadalīta vairākās FastTabs. Tabulā ir aprakstīts katras FastTab nolūks.

| Kopsavilkuma cilne | Apraksts |
|---|---|
| Vispārējā daļa | Šajā Kopsavilkuma cilnē ir parādīta pamatinformācija par atlasīto krājumu darbību. Papildus laukiem, kas parādās lapā Krājumu **darbības**, tajā iekļauti papildu lauki, kas ir aprakstīti tālāk šajā tēmā. |
| Grāmatojumi | Šajā kopsavilkuma cilnē ir parādīta informācija, kas saistīta ar atlasītās krājumu darbības fiziskajiem, finanšu un segšanas aspektiem. Atkarībā no pašreizējā darbības statusa daži lauki var būt tukši. Tomēr šie lauki tiks iestatīti automātiski, grāmatojot darbības. Papildus laukiem, kas parādās lapā **Krājumu** darbības, šajā FastTab ir iekļauti papildu lauki, kas ir aprakstīti tālāk šajā tēmā. |
| Virsgrāmatas grāmatošana | Šajā kopsavilkuma cilnē ir parādīts grāmatošanas tips un Virsgrāmatas konts, kas tiek izmantots fiziskai atjaunināšanai, finanšu atjaunināšanai, fiziskiem ieņēmumiem, fiziskajām papildmaksām, finanšu ieņēmumiem un finanšu izmaksām, kas saistītas ar atlasīto krājumu darbību. |
| Atsauces | Šajā Kopsavilkuma cilnē tiek parādīta papildu informācija par avota darbību, kas izveidoja atlasīto krājumu darbību. Piemēram, šī informācija var iekļaut detalizētu informāciju no pirkšanas pasūtījuma vai pārdošanas pasūtījuma. |
| Saistītā informācija | Šajā kopsavilkuma cilnē tiek parādīta papildinformācija par atlasīto krājumu darbību. Šie lauki, iespējams, netiks iestatīti, ja neizmantojat dažus līdzekļus, piemēram, sagādes kategorijas vai projektus. |
| Finanšu dimensijas — fiziskas | Šajā Kopsavilkuma cilnē tiek rādītas finanšu dimensijas vērtības, kas tika izmantotas, grāmatojot fizisko atjauninājumu. Ja fiziskais atjauninājums nav grāmatots, lauki būs tukši. |
| Finanšu dimensijas — finanšu | Šajā Kopsavilkuma cilnē tiek rādītas finanšu dimensijas vērtības, kas tika izmantotas, grāmatojot finanšu atjauninājumu. Ja finanšu atjaunināšana nav grāmatota, lauki ir tukši. |
| Krājumu dimensijas | Šajā kopsavilkuma cilnē tiek rādītas krājumu dimensijas vērtības, kas ir piešķirtas atlasītajai krājumu darbībai. Šīs vērtības ietver vietu, noliktavu, izmēru, krāsu, konfigurāciju, atrašanās vietu, partijas numuru, sērijas numuru, krājuma statusu, numura zīmi un īpašnieku. |

## <a name="fields-on-the-general-fasttab"></a>Lauki kopsavilkuma cilnē Vispārējā informācija

Šajā tabulā ir aprakstīti kopsavilkuma cilnes Vispārīgi **lauki**, kas nav arī redzami lapā **Krājumu** darbības.

| Lauks | Apraksts |
|---|---|
| Puse | Atlasītās krājumu darbības atbilstošās puses nosaukums. Piemēram, pirkšanas pasūtījuma darbība rāda kreditora nosaukumu pirkšanas pasūtījumā, un pārdošanas pasūtījuma darbība rāda debitora nosaukumu. Šis lauks nav pieejams visiem krājumu darbību tipiem. |
| Atsauce uz krājumiem | Ja ar atlasīto krājuma darbību ir saistīta cita krājumu darbība, šīs citas darbības tips. Piemēram, ja pirkšanas pasūtījums ir iezīmēts pret pārdošanas pasūtījumu, **pirkšanas** pasūtījuma darbības krājumu atsauces lauks tiks iestatīts uz *Pārdošanas pasūtījums*. Iezīmēšana automātiski parādās tiešās piegādes pasūtījumiem un starpuzņēmumu pasūtījumiem. Ja izmantojat atzīmēšanu ar izmaksu *aprēķināšanas* *metodēm, kas nav standarta izmaksas un pārvietojas vidējais*, sistēma izveidos nosegšanas un korekcijas precīzām atzīmētajām darbībām. Šādā veidā varat sasniegt "faktisko" izmaksu apmaksas, kas ignorē loģiku par pirmo reizi, pirmais ārā (FIFO); pēdējie ārā, pirmie ārā (LIFO); vai svērtais vidējais. |
| Noliktavas numurs | Specifiskā darbība, kas saistīta ar atlasīto krājumu darbību. Piemēram, ja pirkšanas pasūtījums ir iezīmēts pret pārdošanas pasūtījumu, **pirkšanas** pasūtījuma darbības krājuma numura lauks tiks iestatīts uz pārdošanas pasūtījuma numuru. |
| Projekta ID | Ja atlasītā krājumu darbība ir saistīta ar projektu, šis lauks ir iestatīts uz projekta numuru. |
| Laidiena ID | Unikālais laidiena ID, ko sistēma ir piešķīrusi atlasītajai krājumu darbībai. |
| Atsauce uz partiju | Ja cita krājumu darbība ir saistīta ar atlasīto krājumu darbību, šīs citas darbības partijas kods. Piemēram, ja pirkšanas pasūtījums ir iezīmēts pret pārdošanas pasūtījumu, **·** **pirkšanas pasūtījuma darbības atsauces partijas lauks būs pārdošanas pasūtījuma rindas krājumu darbības laidiena ID** vērtība. |
| Dimensijas numurs | Unikāls ID, kas parāda visu atlasītajai krājumu darbībai piešķirto krājumu dimensiju vērtību kombināciju. |
| Summa finansiāli atvērta | Vērtība, kas norāda, vai atlasītā krājuma darbība ir nosegta ar krājumu slēgšanas procesu. Ja šis lauks ir iestatīts *kā* Jā, darbība nav nosegta. |
| Prognozētais datums | Saņemšanas darbībām tas ir datums, kad paredzama krājumu ieejas plūsma. Piemēram, šajā laukā var rādīt paredzamo saņemšanas datumu krājuma bloķēšanas pasūtījumā vai piegādes datumu pirkšanas pasūtījuma rindā. |
| Krājumu datums | Šis lauks tiek iestatīts, kad reģistrācijas darbība veikta saņemšanas pasūtījumā pirms fiziskās ieejas plūsmas grāmatošanas. |
| Nefinanšu pārsūtīšana | Vērtība, kas norāda, vai atlasītā krājumu darbība ir nefinanšu pārsūtīšana. Nefinanšu pārsūtīšana notiek, kad krājumu dimensiju izmaiņas nav finansiāli izsekotas krājumu **modeļu grupas** lapā. |
| Pārsūtīšanas laidiena ID | Ja atlasītā krājumu darbība ir ar ko nesaistāma pārsūtīšana, **šis lauks ir iestatīts uz partijas ID** vērtību citai krājumu darbībai, ar kuru ir nosegta atlasītā darbība. |

## <a name="fields-on-the-updates-fasttab"></a>Lauki kopsavilkuma cilnē Atjauninājumi

Šajā tabulā ir aprakstīti kopsavilkuma cilnes Atjauninājumi **lauki**, kas nav arī redzami lapā **Krājumu** darbības.

| Lauks | Apraksts |
|---|---|
| Reāls dokuments | Dokumenta numurs virsgrāmatā, kur tika ģenerēta atlasītās krājumu darbības fiziskā grāmatošana. |
| Maršruts | Maršruts, kas saistīts ar atlasīto krājumu darbību. Šis lauks tiek iestatīts tikai ražošanas izdošanas saraksta darbībām, kur materiālu komplekts (MK) vai formulas rinda attiecas uz noteiktu krājumu. |
| Pavadzīme | Pavadzīmes numurs, kas tika ievadīts pirkšanas pasūtījuma produktu ieejas plūsmas darbībai. |
| Fiziskā izmaksu summa | Summa, kas fiziski grāmatota Virsgrāmatā. Standarta izmaksu precei šī summa parāda standarta izmaksas. Citām izmaksu aprēķināšanas metodēm tas parāda novērtēto vidējo vērtību precei grāmatošanas laikā. |
| Fiziskie ieņēmumi | Atlikto ieņēmumu summa, kas grāmatota virsgrāmatā fiziskā atjauninājumam. |
| Kravas ID | Ja pašreizējā darbība ir saistīta ar noslodzi transportēšanas pārvaldībā, šis lauks rāda unikālo kravas numuru, kas ietver krājumu. |
| Fiziski grāmatots | Vērtība, kas norāda, vai atlasītā krājuma darbība ir fiziski grāmatota. Ja pašreizējā darbība tiek grāmatota Virsgrāmatā, būs arī fizisks dokuments. |
| Finansiāli grāmatots | Vērtība, kas norāda, vai atlasītā krājuma darbība ir finansiāli grāmatota. Ja pašreizējā darbība tiek grāmatota Virsgrāmatā, būs arī finanšu dokuments. |
| Iegrāmatotais fiziskais maksājums | Vērtība, kas norāda, vai ir iegrāmatotas ar atlasīto krājumu darbību saistītās fiziskās izmaksas. |
| Iegrāmatotais finanšu maksājums | Vērtība, kas norāda, vai ir iegrāmatotas finanšu izmaksas, kas saistītas ar atlasīto krājumu darbību. |
| Finanšu dokuments | Dokumenta numurs Virsgrāmatā, kur tika ģenerēta finansiālā grāmatošana. |
| Rēķins | Rēķina numurs, kas ģenerēts, piemēram, pirkšanas pasūtījumam vai pārdošanas pasūtījumam. |
| Pielāgojums | Summa, kas atlasītajai krājumu darbībai tika koriģēta no krājumu slēgšanas un pielāgošanas procesa. |
| Peļņa un zaudējumi, grāmatotā summa | Atlasītās krājumu darbības summa, kas grāmatota peļņas un zaudējumu aprēķinā. |
| Negrāmatots rēķins | Saistītā pirkšanas pasūtījuma rēķina numurs, kas ir redzams lapā Neizlemts **kreditora rēķins**. |
| Finansiāla slēgšana | Datums, kad darbība tika segta pilnībā. |
| Atbilstoši pieļaujamā svara daudzumam | Nosegjamais pieļaujamā svara daudzums. |
| Nosegtais daudzums | Daudzums, kas ir nosegts atlasītajai krājumu darbībai. |
| Nosegtā summa | Vērtība, kas nosegta atlasītajai krājumu darbībai. |
