---
title: "Pārskats par numuru sērijām"
description: "Numuru sērijas Microsoft Dynamics 365 operācijām, izmanto, lai ģenerētu lasāms, unikālu identifikatoru pamatdatu ierakstus un darījumu uzskaiti, kas nepieciešama identifikatorus. Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par <em>atsauci</em>."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a812c93a13fd36f44e659c9976099af62793098f
ms.lasthandoff: 03/31/2017


---

# <a name="number-sequence-overview"></a>Pārskats par numuru sērijām

Numuru sērijas Microsoft Dynamics 365 operācijām, izmanto, lai ģenerētu lasāms, unikālu identifikatoru pamatdatu ierakstus un darījumu uzskaiti, kas nepieciešama identifikatorus. Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par <em>atsauci</em>.

Pirms jūs varat izveidot jaunus ierakstus atsauce Microsoft Dynamics 365 operācijām, numuru sērija jāiestata un saistītu ar atsauci. Numuru sēriju iestatīšanai ieteicams izmantot lapas sadaļā **Organizācijas administrēšana**. Ja ir nepieciešami modelim raksturīgi iestatījumi, varat kādā modulī izmantot parametru lapu, lai šajā modulī esošajām atsaucēm norādītu numuru sērijas. Piemēram, sadaļā **Debitori** un **Debitori** varat iestatīt numuru sēriju grupas, lai konkrētas numuru sērijas piešķirtu konkrētiem debitoriem vai kreditoriem. Iestatot numuru sēriju, ir jānorāda tvērums, kas nosaka, kura organizācija šo numuru sēriju izmanto. Tvērums var būt **Koplietots**, **Uzņēmums**, **Juridiska persona** vai **Pārvaldības struktūrvienība**. Tvērumus **Juridiskā persona** un **Uzņēmums** var kombinēt ar iestatījumu **Finanšu kalendāra periods**, lai izveidotu vēl specifiskākas numuru sērijas. Numuru sēriju formāti sastāv no segmentiem. Numuru sērijas, kuru tvērums nav **Koplietots**, var ietvert tvērumam atbilstošus segmentus. Piemēram, numuru sērija ar tvērumu **Juridiska persona** var ietvert juridiskas personas segmentu. Ja numuru sērijas formātā ietilpst tvēruma segments, konkrēta ieraksta tvērumu varat identificēt, skatoties uz tā numuru. Turklāt segmentiem, kas atbilst tvērumiem, numuru sērijas formāti var ietvert segmentus **Konstante** un **Burti un cipari**. Segments **Konstante** ietver nemainīgu burtu, skaitļu vai simbolu kopu. Segments **Burti un cipari** ietver burtu vai ciparu kopu, kas tiek palielināta katru reizi, kad tiek izmantots numurs. Izmantot numura zīme (\#) pārstāvēt skaitļu palielināšanai un zīmi (&), lai pārstāvētu burtus palielināšanai. Piemēram, šis formāts \#\#\#\#\#\_2017 izveido secības 00001\_2017, 00002\_2017, un tā tālāk.
Numuru sēriju piemēri
------------------------

Tālāk sniegtajos piemēros ir parādīts, kā izmantot segmentus, lai izveidotu numuru sēriju formātus. Šajos piemēros ir īpaši parādītas tvēruma segmentu izmantošanas ietekmes.
### <a name="expense-report-numbers"></a>Izdevumu pārskatu numuri

Nākamajā piemērā izdevumu pārskatu numuri tiek iestatīti juridiskajai personai ar nosaukumu **CS**. **Apgabals: **Ceļošana un izdevumi **Atsauce: **Izdevumu atskaites numurs **Tvērums: **Juridiska persona **Juridiska persona: **CS
| Segmenti  | Segmenta tips | Vērtība     |
|-----------|--------------|-----------|
| 1. segments | Juridiska persona | CS        |
| 2. segments | Konstants     | -EXPENSE- |
| 3. segments | Burtciparu | \#\#\#\#  |

**Formatēta numura piemērs**: CS-EXPENSE-0039 Varat iestatīt līdzīgu numuru sērijas formātu arī citām juridiskajām personām. Juridiskajai personai ar nosaukumu, piemēram, **RW**, ja maināt tikai juridiskās personas segmenta vērtību, formatētais numurs ir RW-EXPENSE-0039. Citām juridiskajām personām varat mainīt arī visu numuru sērijas formātu. Varat, piemēram, izlaist juridiskās personas tvēruma segmentu, lai izveidotu formatētu numuru, piemēram, Exp-0001.

### <a name="sales-order-numbers"></a>Pārdošanas pasūtījumu numuri

Nākamajā piemērā pārdošanas pasūtījumu numuri ir iestatīti uzņēmumam, kura ID ir **CEU**. **Apgabals: **Pārdošana **Atsauce: **Pārdošanas pasūtījums **Tvērums: **Uzņēmums **Uzņēmums: **CEU
| Segmenti  | Segmenta veids | Vērtība    |
|-----------|--------------|----------|
| 1. segments | Konstants     | SO-      |
| 2. segments | Burtciparu | \#\#\#\# |

**Formatēta numura piemērs**: SO-0029 Kaut arī tvēruma segments nav iekļauts šajā formātā, numerācija tiek restartēta katram uzņēmuma ID. Ja izmantojat vienu formātu visiem uzņēmumu ID, tie paši numuri tiek izmantoti katrā uzņēmumā. Piemēram, pārdošanas pasūtījuma numurs SO-0029 tiek izmantots katrā uzņēmumā. Citu uzņēmumu ID varat mainīt arī visu numuru sērijas formātu.

### <a name="purchase-requisition-numbers"></a>Pirkšanas pieprasījumu numuri

Nākamajā piemērā pirkšanas pieprasījumu numuri tiek izmantoti visas organizācijas līmenī. **Apgabals: **Pirkšana **Atsauce: **Pirkšanas pieprasījums **Tvērums: **Koplietots
| Segmenti  | Segmenta veids | Vērtība    |
|-----------|--------------|----------|
| 1. segments | Konstants     | Req      |
| 2. segments | Burtciparu | \#\#\#\# |

**Formatēta numura piemērs**: Req0052 Tā kā tvērums ir **Koplietots**, šis numuru sērijas formāts tiek lietots visā organizācijā. Dažādām organizācijas daļām nevarat iestatīt atšķirīgus numuru sēriju formātus. Ar numuru sēriju veiktspēju saistītie apsvērumi
-----------------------------------------------

Pirms iestatāt numuru sērijas, ņemiet vērā tālāk sniegto informāciju par to, kā numuru sēriju konfigurācija var ietekmēt sistēmas veiktspēju.
### <a name="continuous-and-non-continuous-number-sequences"></a>Nepārtrauktas numuru sērijas un numuru sērijas ar pārtraukumiem

Numuru sērijas var būt nepārtrauktas vai ar pārtraukumiem. Nepārtrauktā numuru sērijā netiek izlaists neviens numurs, bet numurus nedrīkst izmantot secīgi. Numuru sērijās ar pārtraukumiem numuri tiek izmantoti secīgi, bet numuru sērija numurus var izlaist. Piemēram, ja lietotājs atceļ darījumu, numurs tiek izveidots, bet netiek lietots. Nepārtrauktā numuru sērijā šis numurs vēlāk tiek izmantots atkal. Numuru sērijā ar pārtraukumiem šis numurs vairs netiek izmantots. Nepārtrauktas numuru sērijas parasti ir nepieciešamas ārējiem dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem un rēķiniem. Tomēr nepārtrauktas numuru sērijas var negatīvi ietekmēt sistēmas atbildes laikus, jo sistēmai numurs no datu bāzes ir jāpieprasa katru reizi, kad tiek izveidots jauns dokuments vai ieraksts. Ja izmantojat numuru sēriju ar pārtraukumiem, varat iespējot vienumu **Numuru rezervēšana** kopsavilkuma cilnē **Veiktspēja**, kas atrodas lapā **Numuru sērijas**. Ja norādāt rezervēto numuru daudzumu, sistēma atlasa šos numurus un saglabā tos atmiņā. Jauni numuri no datu bāzes tiek pieprasīti tikai pēc tam, kad ir izmantots šis rezervētais daudzums. Ja vien nav ar likumu noteiktas prasības izmantot nepārtrauktas numuru sērijas, labākas veiktspējas nolūkos ieteicams izmantot numuru sērijas ar pārtraukumiem.

### <a name="automatic-cleanup-of-number-sequences"></a>Automātiskā numuru sēriju tīrīšana

Ja rodas elektropadeves traucējumi, programmas kļūda vai citas neparedzētas kļūmes, sistēma nevar automātiski pārstrādāt nepārtraukto numuru secību numurus. Lai atgūtu zaudētos numurus, manuāli vai automātiski varat palaist tīrīšanas procesu. Kad plānojat tīrīšanas procesu, rūpīgi apsveriet servera lietojumu. Mēs iesakām veikt tīrīšanu kā pakešuzdevumu ārpus sastrēgumstundām.




