---
title: Numuru sēriju pārskats
description: Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori.
author: MargoC
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4de5cc79b5c1e38e10bb6a382b279459a64a03c7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559388"
---
# <a name="number-sequences-overview"></a>Numuru sēriju pārskats

[!include [banner](../includes/banner.md)]

Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori. Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par *atsauci*.

Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci. Numuru sēriju iestatīšanai ieteicams izmantot lapas sadaļā **Organizācijas administrēšana**. Ja ir nepieciešami modelim raksturīgi iestatījumi, varat kādā modulī izmantot parametru lapu, lai šajā modulī esošajām atsaucēm norādītu numuru sērijas. Piemēram, sadaļā **Debitori** un **Debitori** varat iestatīt numuru sēriju grupas, lai konkrētas numuru sērijas piešķirtu konkrētiem debitoriem vai kreditoriem.

Iestatot numuru sēriju, ir jānorāda tvērums, kas nosaka, kura organizācija šo numuru sēriju izmanto. Tvērums var būt **Koplietots**, **Uzņēmums**, **Juridiska persona** vai **Pārvaldības struktūrvienība**. Tvērumus **Juridiskā persona** un **Uzņēmums** var kombinēt ar iestatījumu **Finanšu kalendāra periods**, lai izveidotu vēl specifiskākas numuru sērijas.

Numuru sēriju formāti sastāv no segmentiem. Numuru sērijas, kuru tvērums nav **Koplietots**, var ietvert tvērumam atbilstošus segmentus. Piemēram, numuru sērija ar tvērumu **Juridiska persona** var ietvert juridiskas personas segmentu. Ja numuru sērijas formātā ietilpst tvēruma segments, konkrēta ieraksta tvērumu varat identificēt, skatoties uz tā numuru.

Turklāt segmentiem, kas atbilst tvērumiem, numuru sērijas formāti var ietvert segmentus **Konstante** un **Burti un cipari**. Segments **Konstante** ietver nemainīgu burtu, skaitļu vai simbolu kopu. Segments **Burti un cipari** ietver burtu vai ciparu kopu, kas tiek palielināta katru reizi, kad tiek izmantots numurs. Izmantojiet restītes simbolu (\#), lai apzīmētu pieaugošus numurus, un simbolu &, lai apzīmētu pieaugošus burtus. Piemēram, izmantojot formātu \#\#\#\#\#\_2017, tiek izveidota sērija 00001\_2017, 00002\_2017 utt.

## <a name="number-sequence-examples"></a>Numuru sēriju piemēri

Tālāk sniegtajos piemēros ir parādīts, kā izmantot segmentus, lai izveidotu numuru sēriju formātus. Šajos piemēros ir īpaši parādītas tvēruma segmentu izmantošanas ietekmes.

### <a name="expense-report-numbers"></a>Izdevumu pārskatu numuri

Nākamajā piemērā izdevumu pārskatu numuri tiek iestatīti juridiskajai personai ar nosaukumu **CS**.

- **Joma:** Ceļošana un izdevumi
- **Atsauce:** Izdevumu pārskata numurs
- **Tvērums:** Juridiskā persona
- **Juridiskā persona:** CS

| Segmenti  | Segmenta tips | Vērtība     |
|-----------|--------------|-----------|
| 1. segments | Juridiska persona | CS        |
| 2. segments | Konstants     | -EXPENSE- |
| 3. segments | Burtciparu | \#\#\#\#  |

**Formatēta numura piemērs**: CS-EXPENSE-0039

Līdzīgu numuru sērijas formātu varat iestatīt citām juridiskajām personām. Juridiskajai personai ar nosaukumu, piemēram, **RW**, ja maināt tikai juridiskās personas segmenta vērtību, formatētais numurs ir RW-EXPENSE-0039. Citām juridiskajām personām varat mainīt arī visu numuru sērijas formātu. Varat, piemēram, izlaist juridiskās personas tvēruma segmentu, lai izveidotu formatētu numuru, piemēram, Exp-0001.

### <a name="sales-order-numbers"></a>Pārdošanas pasūtījumu numuri

Nākamajā piemērā pārdošanas pasūtījumu numuri ir iestatīti uzņēmumam, kura ID ir **CEU**.

- **Joma:** Pārdošana
- **Atsauce:** Pārdošanas pasūtījums
- **Tvērums:** Uzņēmums
- **Uzņēmums:** CEU

| Segmenti  | Segmenta veids | Vērtība    |
|-----------|--------------|----------|
| 1. segments | Konstants     | SO-      |
| 2. segments | Burtciparu | \#\#\#\# |

**Formatēta numura piemērs**: SO-0029

Kaut arī tvēruma segments nav iekļauts šajā formāts, numerācija tiek restartēta katram uzņēmuma ID. Ja izmantojat vienu formātu visiem uzņēmumu ID, tie paši numuri tiek izmantoti katrā uzņēmumā. Piemēram, pārdošanas pasūtījuma numurs SO-0029 tiek izmantots katrā uzņēmumā. Citu uzņēmumu ID varat mainīt arī visu numuru sērijas formātu.

### <a name="purchase-requisition-numbers"></a>Pirkšanas pieprasījumu numuri

Nākamajā piemērā pirkšanas pieprasījumu numuri tiek izmantoti visas organizācijas līmenī.

- **Joma:** Pirkšana
- **Atsauce:** Pirkšanas pieprasījums
- **Tvērums:** Koplietots

| Segmenti  | Segmenta veids | Vērtība    |
|-----------|--------------|----------|
| 1. segments | Konstants     | Req      |
| 2. segments | Burtciparu | \#\#\#\# |

**Formatēta numura piemērs**: Req0052

Tā kā tvērums ir **Koplietots**, šis numuru sērijas formāts tiek izmantots visā organizācijā. Dažādām organizācijas daļām nevarat iestatīt atšķirīgus numuru sēriju formātus.

## <a name="performance-considerations-for-number-sequences"></a>Ar numuru sēriju veiktspēju saistītie apsvērumi

Pirms iestatāt numuru sērijas, ņemiet vērā tālāk sniegto informāciju par to, kā numuru sēriju konfigurācija var ietekmēt sistēmas veiktspēju.

### <a name="continuous-and-non-continuous-number-sequences"></a>Nepārtrauktas numuru sērijas un numuru sērijas ar pārtraukumiem

Numuru sērijas var būt nepārtrauktas vai ar pārtraukumiem. Nepārtrauktā numuru sērijā netiek izlaists neviens numurs, bet numurus nedrīkst izmantot secīgi. Numuru sērijās ar pārtraukumiem numuri tiek izmantoti secīgi, bet numuru sērija numurus var izlaist. Piemēram, ja lietotājs atceļ darījumu, numurs tiek izveidots, bet netiek lietots. Nepārtrauktā numuru sērijā šis numurs vēlāk tiek izmantots atkal. Numuru sērijā ar pārtraukumiem šis numurs vairs netiek izmantots.

Nepārtrauktas numuru sērijas parasti ir nepieciešamas ārējiem dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem un rēķiniem. Tomēr nepārtrauktas numuru sērijas var negatīvi ietekmēt sistēmas atbildes laikus, jo sistēmai numurs no datu bāzes ir jāpieprasa katru reizi, kad tiek izveidots jauns dokuments vai ieraksts.

Ja izmantojat numuru sēriju ar pārtraukumiem, varat iespējot vienumu **Numuru rezervēšana** kopsavilkuma cilnē **Veiktspēja**, kas atrodas lapā **Numuru sērijas**. Ja norādāt rezervēto numuru daudzumu, sistēma atlasa šos numurus un saglabā tos atmiņā. Jauni numuri no datu bāzes tiek pieprasīti tikai pēc tam, kad ir izmantots šis rezervētais daudzums.

Ja vien nav ar likumu noteiktas prasības izmantot nepārtrauktas numuru sērijas, labākas veiktspējas nolūkos ieteicams izmantot numuru sērijas ar pārtraukumiem.

### <a name="automatic-cleanup-of-number-sequences"></a>Automātiskā numuru sēriju tīrīšana

Ja rodas elektropadeves traucējumi, programmas kļūda vai citas neparedzētas kļūmes, sistēma nevar automātiski pārstrādāt nepārtraukto numuru secību numurus. Lai atgūtu zaudētos numurus, manuāli vai automātiski varat palaist tīrīšanas procesu.

Kad plānojat tīrīšanas procesu, rūpīgi apsveriet servera lietojumu. Mēs iesakām veikt tīrīšanu kā pakešuzdevumu ārpus sastrēgumstundām.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]