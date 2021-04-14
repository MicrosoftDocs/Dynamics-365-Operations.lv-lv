---
title: Dokumentu importēšana, izmantojot Virsgrāmatas žurnāla entītiju
description: Šajā tēmā ir sniegti padomi par datu importēšanu virsgrāmatas žurnālā, izmantojot elementu Virsgrāmatas žurnāls.
author: rcarlson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a8046cf59f47799627dc09e2b788ab7bdd727e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749674"
---
# <a name="importing-vouchers-by-using-the-general-journal-entity"></a>Dokumentu importēšana, izmantojot Virsgrāmatas žurnāla entītiju

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegti padomi par datu importēšanu virsgrāmatas žurnālā, izmantojot elementu Virsgrāmatas žurnāls.

Elementu Virsgrāmatas žurnāls varat izmantot, lai importētu dokumentus, kuru konta vai korespondējošā konta tips ir **Virsgrāmata**, **Debitors**, **Kreditors** vai **Banka**. Dokumentu var ievadīt kā vienu rindu, izmantojot gan lauku **Konts**, gan lauku **Korespondējošais konts**, vai kā vairāku rindu dokumentu, kurā tiek izmantots tikai lauks **Konts** (un lauks **Korespondējošais konts** katrā rindā tiek atstāts tukšs). Elements Virsgrāmatas žurnāls neatbalsta visus kontu tipus. Tā vietā pastāv citi elementi tādiem scenārijiem, kur ir nepieciešamas citādas kontu tipu kombinācijas. Piemēram, lai importētu projekta darījumu izmantojiet elementu Projekta izdevumu žurnāls. Katrs elements ir paredzēts specifisku scenāriju atbalstam. Tas nozīmē, ka šajos scenārijos var būt pieejami papildu lauki. Tomēr papildu lauki elementos var nebūt pieejami dažādiem scenārijiem.

## <a name="setup"></a>Iestatīt
Pirms veicat importēšanu, izmantojot elementu Virsgrāmatas žurnāls, pārliecinieties par tālāk aprakstītajiem iestatījumiem.

- **Numuru sērijas iestatījumi žurnāla pakešuzdevuma numuram** —pēc noklusējuma, kad importējat, izmantojot entītiju Virsgrāmatas žurnāls, šis žurnāla pakešuzdevuma numurs izmanto virsgrāmatas parametriem definēto numuru sēriju. Ja numuru sēriju žurnāla pakešuzdevuma numuram iestatāt uz **Manuāli**, noklusējuma numurs netiek lietots. Šis iestatījums netiek atbalstīts.
- **Finanšu dimensijas konfigurācija** — katrai organizācijai ir jādefinē finanšu dimensiju secība, kad elementi tiek izmantoti, lai importētu transakcijas. Secība tiek definēta formātam **Virsgrāmatas dimensiju integrācija** sadaļā **Virsgrāmata** &gt; **Kontu plāns** &gt; **Dimensijas** &gt; **Finanšu dimensijas konfigurācija programmu integrēšanai** &gt; **Atlasīt datu elementus**. Virsgrāmatas konta segmentiem, kas tiek importēti, ir nepieciešama vienāda secība. Pretējā gadījumā importēšanas laikā notiks kļūda.

## <a name="general-journal-entity-setup"></a>Virsgrāmatas žurnāla elementa iestatīšana
Divi iestatījumi sadaļā Datu pārvaldība ietekmē, kā tiek lietots noklusējuma žurnāla pakešuzdevuma numurs vai dokumenta numurs.

- **No kopas atkarīga apstrāde** (datu elementā)
- **Automātiski ģenerēts** (lauka kartējumā)

Tālāk norādītajās sadaļās ir aprakstīta šo iestatījumu ietekme. Tie arī izskaidro, kā sistēma ģenerē partijas numurus žurnāliem un dokumentu numuriem.

### <a name="journal-batch-number"></a>Žurnāla iedaļas numurs

- Iestatījums **No kopas atkarīga apstrāde** elementā Virsgrāmatas žurnāls neietekmē veidu, kā tiek ģenerēti žurnālu pakešuzdevumu numuri.
- Ja lauks **Žurnāla pakešuzdevuma numurs** ir iestatīts uz **Automātiski ģenerēts**, tad jauns žurnāla pakešuzdevuma numurs tiek veidots katrai rindai, kas tiek importēta. Šāda uzvedība nav ieteicama. Iestatījums **Automātiski ģenerēts** atrodas importēšanas projektā, sadaļā **Skatīt karti**, cilnē **Detalizēta informācija par kartēšanu**.
- Ja lauks **Žurnāla pakešuzdevuma numurs** nav iestatīts uz **Automātiski ģenerēts**, tad žurnāla pakešuzdevuma numurs tiek veidots šādi:

    - Ja importētajā failā definētais žurnāla pakešuzdevuma numurs atbilst esošajam, negrāmatotajam ikdienas žurnālam, tad visas rindas, kam ir atbilstošs žurnāla pakešuzdevuma numurs, tiek importētas esošajā žurnālā. Rindas nekad netiek importētas grāmatotā žurnāla pakešuzdevuma numurā. Tā vietā tiek izveidots jauns numurs.
    - Ja importētajā failā definētais žurnāla pakešuzdevuma numurs neatbilst esošajam, negrāmatotajam ikdienas žurnālam, tad visas rindas, kam ir tāds pats žurnāla pakešuzdevuma numurs, tiek grupētas jaunā žurnālā. Piemēram, visas rindas, kurās žurnāla pakešuzdevuma numurs ir 1, tiek importētas jaunā žurnālā, un visas rindas, kurās žurnāla pakešuzdevuma numurs ir 2, tiek importētas otrā jaunā žurnālā. Žurnāla pakešuzdevuma numurs tiek veidots, izmantojot numuru sēriju, kas ir definēta virsgrāmatas parametros.

### <a name="voucher-number"></a>Dokumenta numurs

- Kad izmantojat iestatījumu **No kopas atkarīga apstrāde** elementā Virsgrāmatas žurnāls, dokumenta numuram ir jābūt norādītam importētajā failā. Katrai transakcijai virsgrāmatas žurnālā tiek piešķirts dokumenta numurs, kas ir norādīts importētajā failā, pat ja dokuments nav līdzsvarots. Ievērojiet nākamos punktus, ja vēlaties lietot no kopas atkarīgu apstrādi, bet vēlaties arī lietot numuru sēriju, kas ir definēta dokumentu numuriem.

    - Lai iespējotu šo funkcionalitāti, žurnāla nosaukumam, kas tiek izmantots importēšanai, vienumu **Numuru piešķiršana grāmatojot** iestatiet uz **Jā**.
    - Dokumenta numuram joprojām ir jābūt definētam importētajā failā. Taču šis numurs ir tikai pagaidu, un žurnāla grāmatošanas laikā tas tiks pārrakstīts ar dokumenta numuru. Pārliecinieties, ka žurnāla rindas tiek pareizi grupētas pēc pagaidu dokumenta numura. Piemēram, grāmatošanas laikā tiek konstatētas trīs rindas, kurās pagaidu dokumenta numurs ir 1. Visu trīs rindu pagaidu dokumenta numurs tiek pārrakstīts ar nākamo numuru attiecīgajā numuru sērijā. Ja šīs trīs rindas nav līdzsvarots ieraksts, tad dokuments netiks grāmatots. Pēc tam, ja tiek konstatētas rindas, kuru pagaidu dokumenta numurs ir 2, šis numurs tiek pārrakstīts ar nākamo dokumenta numuru attiecīgajā sērijā, un tā tālāk.

- Kad neizmantojat iestatījumu **No kopas atkarīga apstrāde**, importētajā failā nav jānorāda dokumenta numurs. Dokumentu numuri tiek veidoti importēšanas laikā, pamatojoties uz žurnāla nosaukuma iestatījumiem (**Tikai viens dokuments**, **Saistībā ar bilanci** un citiem). Piemēram, ja žurnāla nosaukums ir definēts kā **Saistībā ar bilanci**, tad pirmā rinda saņem jaunu noklusējuma dokumenta numuru. Pēc tam sistēma novērtē šo rindu, lai noteiktu, vai debeta summas ir vienādas ar kredīta summām. Ja rindā pastāv korespondējošais konts, tad nākamā importētā rinda saņem jaunu dokumenta numuru. Ja korespondējošā konta nav, tad sistēma novērtē, vai debeta summas ir vienādas ar kredīta summām, importējot katru jauno rindu.
- Ja lauks **Dokumenta numurs** ir iestatīts uz **Automātiski ģenerēts**, tad importēšana neizdosies. Iestatījums **Automātiski ģenerēts** laukam **Dokumenta numurs** netiek atbalstīts.

Pēc noklusējuma elements Virsgrāmatas žurnāls izmanto no kopas atkarīgu apstrādi. Kad esat izvērtējis savas organizācijas biznesa prasības, iestatījumu **No kopas atkarīga apstrāde** varat mainīt, noklikšķinot uz **Datu elementi** darbvietā **Datu pārvaldība**. No kopas atkarīga apstrāde tiek izmantota, lai paātrinātu importēšanas procesu. Ja neizmantojat no kopas atkarīgu apstrādi, elementa Virsgrāmatas žurnāls importēšana notiks lēnāk.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]