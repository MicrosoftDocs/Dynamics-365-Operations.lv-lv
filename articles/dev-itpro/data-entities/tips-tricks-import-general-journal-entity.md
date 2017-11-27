---
title: "Labākās prakses dokumentu importēšanai, izmantojot elementu Virsgrāmatas žurnāls"
description: "Šajā tēmā ir sniegti padomi par datu importēšanu virsgrāmatas žurnālā, izmantojot elementu Virsgrāmatas žurnāls."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 688fa17072cb340d6d02be31528339fb98601825
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Labākās prakses dokumentu importēšanai, izmantojot elementu Virsgrāmatas žurnāls

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegti padomi par datu importēšanu virsgrāmatas žurnālā, izmantojot elementu Virsgrāmatas žurnāls.  

Elementu Virsgrāmatas žurnāls varat izmantot, lai importētu dokumentus, kuru konta vai korespondējošā konta tips ir **Virsgrāmata, Debitors, Kreditors vai Banka**. Dokumentu var ievadīt kā vienu rindu, izmantojot gan lauku **Konts**, gan lauku **Korespondējošais konts**, vai kā vairāku rindu dokumentu, kurā tiek izmantots tikai lauks **Konts** (un lauks **Korespondējošais konts** katrā rindā tiek atstāts tukšs). Elements Virsgrāmatas žurnāls neatbalsta visus kontu tipus. Tā vietā pastāv citi elementi tādiem scenārijiem, kur ir nepieciešamas citādas kontu tipu kombinācijas. Piemēram, lai importētu projekta darījumu izmantojiet elementu Projekta izdevumu žurnāls. Katrs elements ir izstrādāts, lai atbalstītu noteiktus scenārijus, tādējādi attiecīgajiem scenārijiem paredzētos elementos var būt pieejami tādi papildu lauki, kas nav pieejami citiem scenārijiem paredzētos elementos.

## <a name="setup"></a>Iestatīšana
Pirms veicat importēšanu, izmantojot elementu Virsgrāmatas žurnāls, pārliecinieties par tālāk aprakstītajiem iestatījumiem.

-   **Numuru sērijas iestatījumi žurnāla pakešuzdevuma numuram** — pēc noklusējuma, kad importējat, izmantojot entītiju Virsgrāmatas žurnāls, šis žurnāla pakešuzdevuma numurs izmanto virsgrāmatas parametriem definēto numuru sēriju. Ja numuru sēriju žurnāla pakešuzdevuma numuram iestatāt uz **Manuāli**, noklusējuma numurs netiek lietots. Šis iestatījums netiek atbalstīts.
-   **Finanšu dimensijas konfigurācija** — katrai organizācijai ir jādefinē finanšu dimensiju secība, kad elementi tiek izmantoti, lai importētu transakcijas. Secība tiek definēta formātam **Virsgrāmatas dimensiju integrācija** sadaļā **Virsgrāmata** &gt; **Kontu plāns** &gt; **Dimensijas** &gt; **Finanšu dimensijas konfigurācija programmu integrēšanai** &gt; **Atlasīt datu elementus**. Virsgrāmatas konta segmentiem, kas tiek importēti, ir nepieciešama vienāda secība. Pretējā gadījumā importēšanas laikā notiks kļūda.

## <a name="general-journal-entity-setup"></a>Virsgrāmatas žurnāla elementa iestatīšana
Divi iestatījumi sadaļā Datu pārvaldība ietekmē, kā tiek lietots noklusējuma žurnāla pakešuzdevuma numurs vai dokumenta numurs.

-   **No kopas atkarīga apstrāde** (datu elementā)
-   **Automātiski ģenerēts** (lauka kartējumā)

Nākamajās sadaļās ir aprakstīta šo iestatījumu ietekme, kā arī paskaidrots, kā tiek ģenerēti žurnālu pakešuzdevumu numuri un dokumentu numuri.

### <a name="journal-batch-number"></a>Žurnāla iedaļas numurs

-   Iestatījums **No kopas atkarīga apstrāde** elementā Virsgrāmatas žurnāls neietekmē veidu, kā tiek ģenerēti žurnālu pakešuzdevumu numuri.
-   Ja lauks **Žurnāla pakešuzdevuma numurs** ir iestatīts uz **Automātiski ģenerēts**, tad jauns žurnāla pakešuzdevuma numurs tiek veidots katrai rindai, kas tiek importēta. Šāda uzvedība nav ieteicama. Iestatījums **Automātiski ģenerēts** atrodas importēšanas projektā, sadaļā **Skatīt karti**, cilnē **Detalizēta informācija par kartēšanu**.
-   Ja lauks **Žurnāla pakešuzdevuma numurs** nav iestatīts uz **Automātiski ģenerēts**, tad žurnāla pakešuzdevuma numurs tiek veidots šādi:
    -   Ja importētajā failā definētais žurnāla pakešuzdevuma numurs atbilst esošajam, negrāmatotajam ikdienas žurnālam, tad visas rindas, kam ir atbilstošs žurnāla pakešuzdevuma numurs, tiek importētas esošajā žurnālā. Rindas nekad netiek importētas grāmatotā žurnāla pakešuzdevuma numurā. Tā vietā tiek izveidots jauns numurs.
    -   Ja importētajā failā definētais žurnāla pakešuzdevuma numurs neatbilst esošajam, negrāmatotajam ikdienas žurnālam, tad visas rindas, kam ir tāds pats žurnāla pakešuzdevuma numurs, tiek grupētas jaunā žurnālā. Piemēram, visas rindas, kurās žurnāla pakešuzdevuma numurs ir 1, tiek importētas jaunā žurnālā, un visas rindas, kurās žurnāla pakešuzdevuma numurs ir 2, tiek importētas otrā jaunā žurnālā. Žurnāla pakešuzdevuma numurs tiek veidots, izmantojot numuru sēriju, kas ir definēta virsgrāmatas parametros.

### <a name="voucher-number"></a>Dokumenta numurs

-   Kad izmantojat iestatījumu **No kopas atkarīga apstrāde** elementā Virsgrāmatas žurnāls, dokumenta numuram ir jābūt norādītam importētajā failā. Katrai transakcijai virsgrāmatas žurnālā tiek piešķirts dokumenta numurs, kas ir norādīts importētajā failā, pat ja dokuments nav līdzsvarots. Ja vēlaties lietot no kopas atkarīgu apstrādi, bet vēlaties arī lietot numuru sēriju, kas ir definēta dokumentu numuriem, ir nodrošināts labojumfails versijas 2016. gada februāra laidienam. Šī labojumfaila numurs ir 3170316, un tas ir pieejams lejupielādei no Lifecycle Services (LCS). Papildinformāciju skatiet rakstā [Lejupielādēt labojumfailus no Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Lai iespējotu šo funkcionalitāti, žurnāla nosaukumam, kas tiek izmantots importēšanai, vienumu **Numuru piešķiršana grāmatojot** iestatiet uz **Jā**.
    -   Dokumenta numuram joprojām ir jābūt definētam importētajā failā. Taču šis numurs ir tikai pagaidu, un žurnāla grāmatošanas laikā tas tiek pārrakstīts ar dokumenta numuru. Jums ir jānodrošina, ka žurnāla rindas tiek pareizi grupētas pēc pagaidu dokumenta numura. Piemēram, grāmatošanas laikā tiek konstatētas trīs rindas, kurās pagaidu dokumenta numurs ir 1. Visu trīs rindu pagaidu dokumenta numurs tiek pārrakstīts ar nākamo numuru attiecīgajā numuru sērijā. Ja šīs trīs rindas nav līdzsvarots ieraksts, tad dokuments netiek grāmatots. Pēc tam, ja tiek konstatētas rindas, kuru pagaidu dokumenta numurs ir 2, šis numurs tiek pārrakstīts ar nākamo dokumenta numuru attiecīgajā numuru sērijā, un tā tālāk.

<!-- -->

-   Kad neizmantojat iestatījumu **No kopas atkarīga apstrāde**, importētajā failā nav jānorāda dokumenta numurs. Dokumentu numuri tiek veidoti importēšanas laikā, pamatojoties uz žurnāla nosaukuma iestatījumiem (**Tikai viens dokuments**, **Saistībā ar bilanci** un citiem). Piemēram, ja žurnāla nosaukums ir definēts kā **Saistībā ar bilanci**, tad pirmā rinda saņem jaunu noklusējuma dokumenta numuru. Pēc tam sistēma novērtē šo rindu, lai noteiktu, vai debeta summas ir vienādas ar kredīta summām. Ja rindā pastāv korespondējošais konts, tad nākamā importētā rinda saņem jaunu dokumenta numuru. Ja korespondējošā konta nav, tad sistēma novērtē, vai debeta summas ir vienādas ar kredīta summām, importējot katru jauno rindu.
-   Ja lauks **Dokumenta numurs** ir iestatīts uz **Automātiski ģenerēts**, tad importēšana neizdosies. Iestatījums **Automātiski ģenerēts** laukam **Dokumenta numurs** netiek atbalstīts.

Pēc noklusējuma elements Virsgrāmatas žurnāls izmanto no kopas atkarīgu apstrādi. Kad esat izvērtējis savas organizācijas biznesa prasības, iestatījumu **No kopas atkarīga apstrāde** varat mainīt, noklikšķinot uz **Datu elementi** darbvietā **Datu pārvaldība**. No kopas atkarīga apstrāde tiek izmantota, lai paātrinātu importēšanas procesu. Ja neizmantojat no kopas atkarīgu apstrādi, elementa Virsgrāmatas žurnāls importēšana notiks lēnāk.




