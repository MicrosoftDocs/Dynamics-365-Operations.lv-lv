---
title: "Labākās prakses dokumentus, izmantojot Virsgrāmatas žurnāla vienību ievešanai"
description: "Šajā tēmā ir sniegta padomus datu importēšanai v/g žurnālā, izmantojot vispārējo žurnāla vienību."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Labākās prakses dokumentus, izmantojot Virsgrāmatas žurnāla vienību ievešanai

Šajā tēmā ir sniegta padomus datu importēšanai v/g žurnālā, izmantojot vispārējo žurnāla vienību.  

Virsgrāmatas žurnāla vienība var izmantot, lai importētu dokumentus kontu vai ofseta konta tips ir **Virsgrāmatā, debitora, kreditora vai bankas**. Dokuments var ievadīta kā viena rinda, izmantojot gan **konta** laukā un **korespondējošais konts** laukā, vai arī kā vairāku rindiņu dokumenta, ja tikai **konta** lauks tiek izmantots (un **korespondējošais konts** katrā rindā tiek atstāts tukšs). Virsgrāmatas žurnāla vienību neatbalsta katru konta tipu. Tā vietā pastāv citi elementi tādiem scenārijiem, kur ir nepieciešamas citādas kontu tipu kombinācijas. Piemēram, lai importētu projekta darbības, izmantojiet projekta izdevumu žurnālā uzņēmums. Katrai entītijai ir paredzēta, lai atbalstītu specifiskiem scenārijiem, kas nozīmē papildu laukus var būt pieejami, subjekti, tiem scenārijiem, bet ne personas atšķirīgu scenāriju.

## <a name="setup"></a>Iestatīšana
Pirms importēšanas, izmantojot Virsgrāmatas žurnāla entītiju, apstiprināt šādu iestatījumu:

-   **Numuru sērijas iestatījumi žurnāla pakešuzdevuma numurs** - pēc noklusējuma, kad importējat, lietojot entītijas Virsgrāmatas žurnālā, žurnāla partijas numuru lieto numuru sēriju, kas ir definēts Virsgrāmatas parametri. Ja numuru sēriju žurnāla pakešuzdevuma numuram iestatāt uz **Manuāli**, noklusējuma numurs netiek lietots. Šis iestatījums netiek atbalstīts.
-   **Finanšu dimensijai konfigurācija** -katrai organizācijai jādefinē finanšu dimensijas pasūtījumu, kad vienības izmanto, lai importētu darījumiem. Pasūtījums ir definēts **Virsgrāmatas dimensiju integrāciju** formātā, pie **Virsgrāmatas**&gt;**kontu**&gt;**dimensijas**&gt;**finanšu dimensijai konfigurācija, kas domāta integrē lietojumprogrammas**&gt;**atlasiet datu subjekti**. Virsgrāmatas konta segmentiem, kas tiek importēti, ir nepieciešama vienāda secība. Pretējā gadījumā importēšanas laikā notiks kļūda.

## <a name="general-journal-entity-setup"></a>Virsgrāmatas žurnāla elementa iestatīšana
Datu pārvaldības divi iestatījumi ietekmē to, kā tiek lietots noklusētais žurnāla iedaļas numuru vai dokumenta numuru:

-   **Kopas, pamatojoties pārstrādes** (par datu subjekts)
-   **Automātiski ģenerētais** (uz lauka kartēšanu)

Nākamajās sadaļās ir aprakstīta šo iestatījumu ietekme, kā arī paskaidrots, kā tiek ģenerēti žurnālu pakešuzdevumu numuri un dokumentu numuri.

### <a name="journal-batch-number"></a>Žurnāla iedaļas numurs

-   Iestatījums **No kopas atkarīga apstrāde** elementā Virsgrāmatas žurnāls neietekmē veidu, kā tiek ģenerēti žurnālu pakešuzdevumu numuri.
-   Ja lauks **Žurnāla pakešuzdevuma numurs** ir iestatīts uz **Automātiski ģenerēts**, tad jauns žurnāla pakešuzdevuma numurs tiek veidots katrai rindai, kas tiek importēta. Šāda uzvedība nav ieteicama. Iestatījums **Automātiski ģenerēts** atrodas importēšanas projektā, sadaļā **Skatīt karti**, cilnē **Detalizēta informācija par kartēšanu**.
-   Ja lauks **Žurnāla pakešuzdevuma numurs** nav iestatīts uz **Automātiski ģenerēts**, tad žurnāla pakešuzdevuma numurs tiek veidots šādi:
    -   Ja žurnāla pakešuzdevuma numurs, kas definēts importētais fails atbilst esošiem, neiegrāmatotās ikdienas žurnālā Microsoft Dynamics 365 operācijām, visās rindās, kas ir atbilstošas žurnāla pakešuzdevuma numurs tiek importēts esošo žurnālu. Rindas nekad netiek importētas grāmatotā žurnāla pakešuzdevuma numurā. Tā vietā tiek izveidots jauns numurs.
    -   Ja žurnāla pakešuzdevuma numurs, kas definēts importētais fails neatbilst esošās, neiegrāmatotās ikdienas žurnālā Dynamics 365 operācijām, visās rindās, kas ir pašā žurnāla pakešuzdevuma numurs tiek sagrupēti zem jaunā žurnālā. Piemēram, visas rindas, kurās žurnāla pakešuzdevuma numurs ir 1, tiek importētas jaunā žurnālā, un visas rindas, kurās žurnāla pakešuzdevuma numurs ir 2, tiek importētas otrā jaunā žurnālā. Žurnāla pakešuzdevuma numurs tiek veidots, izmantojot numuru sēriju, kas ir definēta virsgrāmatas parametros.

### <a name="voucher-number"></a>Dokumenta numurs

-   Kad izmantojat iestatījumu **No kopas atkarīga apstrāde** elementā Virsgrāmatas žurnāls, dokumenta numuram ir jābūt norādītam importētajā failā. Katrai transakcijai virsgrāmatas žurnālā tiek piešķirts dokumenta numurs, kas ir norādīts importētajā failā, pat ja dokuments nav līdzsvarots. Ja vēlaties lietot kopas balstītu apstrādi, bet vēlaties izmantot dokumentu numuriem Dynamics 365 operācijas numuru sērijas, kas definēta, labojumfails ir sniedzis izlaišanai februārī 2016. Šī labojumfaila numurs ir 3170316, un tas ir pieejams lejupielādei no Lifecycle Services (LCS). Papildinformāciju skatiet rakstā [Lejupielādēt labojumfailus no Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Lai iespējotu šo funkcionalitāti, par žurnāla nosaukums, ko izmanto importa dinamika 365 operācijām, kas **numuru piešķiršana grāmatojot** uz **Jā**.
    -   Dokumenta numuram joprojām ir jābūt definētam importētajā failā. Tomēr šis skaitlis ir tikai pagaidu un tiek pārrakstīta ar Dynamics 365 darbības dokumenta numurs, grāmatojot žurnālu. Jums ir jānodrošina, ka žurnāla rindas tiek pareizi grupētas pēc pagaidu dokumenta numura. Piemēram, grāmatošanas laikā trīs rindās ir atrodami, kuriem ir pagaidu dokumenta numurs 1. Visas trīs rindas pagaidu dokumenta numurs tiek pārrakstīts ar nākamo numuru no numuru sērijas. Ja šīs trīs rindas nav līdzsvarots ieraksts, tad dokuments netiek grāmatots. Pēc tam, ja tiek konstatētas rindas, kuru pagaidu dokumenta numurs ir 2, šis numurs tiek pārrakstīts ar nākamo dokumenta numuru attiecīgajā numuru sērijā, un tā tālāk.

<!-- -->

-   Ja jūs neizmantojat **Set pamatojoties pārstrādes** iestatījumu, jums nav nepieciešams sniegt dokumenta numuram, kas iekļauts importētajā failā. Dokumentu numuri tiek veidoti importēšanas laikā, pamatojoties uz žurnāla nosaukuma iestatījumiem (**Tikai viens dokuments**, **Saistībā ar bilanci** un citiem). Piemēram, ja žurnāla nosaukums ir definēts kā **Saistībā ar bilanci**, tad pirmā rinda saņem jaunu noklusējuma dokumenta numuru. Pēc tam sistēma novērtē šo rindu, lai noteiktu, vai debeta summas ir vienādas ar kredīta summām. Ja rindā pastāv korespondējošais konts, tad nākamā importētā rinda saņem jaunu dokumenta numuru. Ja korespondējošā konta nav, tad sistēma novērtē, vai debeta summas ir vienādas ar kredīta summām, importējot katru jauno rindu.
-   Ja lauks **Dokumenta numurs** ir iestatīts uz **Automātiski ģenerēts**, tad importēšana neizdosies. Iestatījums **Automātiski ģenerēts** laukam **Dokumenta numurs** netiek atbalstīts.

Pēc noklusējuma elements Virsgrāmatas žurnāls izmanto no kopas atkarīgu apstrādi. Kad esat izvērtējis savas organizācijas biznesa prasības, iestatījumu **No kopas atkarīga apstrāde** varat mainīt, noklikšķinot uz **Datu elementi** darbvietā **Datu pārvaldība**. No kopas atkarīga apstrāde tiek izmantota, lai paātrinātu importēšanas procesu. Ja neizmantojat no kopas atkarīgu apstrādi, elementa Virsgrāmatas žurnāls importēšana notiks lēnāk.


