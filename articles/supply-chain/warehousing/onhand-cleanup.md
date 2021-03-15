---
title: Noliktavas pārvaldības rīcībā esošo ierakstu tīrīšanas darbs
description: Šajā tēmā ir aprakstīts rīcībā esošo ierakstu tīrīšanas darbs, kas palīdz uzlabot sistēmas veiktspēju, identificējot un dzēšot saistītus, bet nevajadzīgus ierakstus.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f045b9686bbdfcf3e82f5158f0fd28860354b7d7
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014487"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Noliktavas pārvaldības rīcībā esošo ierakstu tīrīšanas darbs

Vaicājumu, kas tiek izmantoti rīcībā esošo krājumu aprēķināšanai, veiktspēju ietekmē to ierakstu skaits, kas atrodas iesaistītajās tabulās. Viens no veiktspējas uzlabošanas veidiem ir samazināt to ierakstu skaitu, kuri datu bāzei ir jāņem vērā.

Šajā tēmā ir aprakstīts rīcībā esošo ierakstu tīrīšanas darbs, kas izdzēš nevajadzīgus ierakstus InventSum un WHSInventReserve tabulās. Šajās tabulas tiek glabāta rīcībā esošā informācija par krājumiem, kas ir iespējoti noliktavas pārvaldības apstrādei. (Šie krājumi tiek saukti par WHS krājumiem.) Šo ierakstu dzēšana var būtiski uzlabot rīcībā esošo aprēķinu veiktspēju.

## <a name="what-the-cleanup-job-does"></a>Kas ir tīrīšanas darbs

Rīcībā esošo ierakstu tīrīšanas darbs dzēš visus ierakstus WHSInventReserve un InventSum tabulās, ja visas lauka vērtības ir *0* (nulle). Šos ierakstus var dzēst, jo tie neveicina rīcībā esošo informāciju. Darbs dzēš tikai tos ierakstus, kas ir zem līmeņa **Novietojums**.

Ja ir atļauti negatīvi fiziskie krājumi, tīrīšanas darbs, iespējams, nevarēs izdzēst visus atbilstošos ierakstus. Šī ierobežojuma iemesls ir tas, ka darbam ir jānodrošina īpašs scenārijs, kurā unikālajai noliktavas vienībai ir vairāki sērijas numuri, un viens no šiem sērijas numuriem ir kļuvis negatīvs. Piemēram, sistēmai būs nulle rīcībā esošajā unikālās noliktavas vienības līmenī, ja unikālajai noliktavas vienībai ir 1. sērijas numurs + 1 gab. un 2. sērijas numurs – 1 gab. Šajā īpašajā scenārijā darbs veic plašuma dzēšanu, vispirms mēģinot izdzēst no zemākiem līmeņiem.

## <a name="schedule-and-configure-the-cleanup-job"></a>Tīrīšanas darba ieplānošana un konfigurēšana

Rīcībā esošo ierakstu tīrīšanas darbs ir pieejams **Krājumu vadība \> Periodiskie uzdevumi \> Tīrīt \> Noliktavas pārvaldības rīcībā esošo ierakstu tīrīšana**. Lietojiet standarta darba iestatījumus, lai kontrolētu darba izpildes jomu un grafiku. Turklāt tiek nodrošināti tālāk minētie iestatījumi.

- **Dzēst, ja nav atjaunināts ... dienas** — ievadiet minimālo dienu skaitu, cik ilgi darbam jāgaida, pirms tas dzēš rīcībā esošo ierakstu, kas ir samazinājies līdz nulles daudzumam. Izmantojiet šo iestatījumu, lai samazinātu to rīcībā esošo ierakstu dzēšanas risku, kas joprojām tiek lietoti. Ja vēlaties tīrīšanu veikt pēc iespējas drīzāk, ievadiet *0* (nulle) vai atstājiet lauku tukšu.
- **Maksimālais izpildes laiks (stundas)** — ievadiet tīrīšanas darba maksimālo izpildes laiku stundās. Ja darbs nav pabeigts pirms šī laika beigām, tas saglabās līdz šim paveikto darbu un pēc tam tiks aizvērts. Šī iespēja ir īpaši svarīga implementācijām, kurās ir augsta krājumu izmantošana. Šādos gadījumos darbs ir jāplāno, lai tas darbotos laikā, kad sistēmas noslodze ir iespējami mazāka. Ja vēlaties, lai pakešuzdevums turpinātu darboties, līdz tas ir pabeigts, ievadiet *0* (nulle) vai atstājiet lauku tukšu. Šis iestatījums ir pieejams tikai tad, ja saistītais līdzeklis [sistēmā ir ieslēgts](#max-execution-time).

Lai gan darbu varat palaist regulāro darba stundu laikā, iesakām to palaist ārpus darba laika. Tādējādi jūs palīdzat novērst konfliktus, kas var rasties, ja lietotājs strādā ar ierakstu, kas tiek arī tīrīts.

Ja darbs mēģina izdzēst ierakstu krājumam laikā, kad šo ierakstu izmanto cits lietotājs, tīrīšanas darbam vai lietotājam rodas bezizejas kļūda.

Kad darbs tiek palaists, tā izpildes lielums ir 100. Citiem vārdiem sakot, tas mēģinās izpildīt vienu reizi katrām 100 dzēšanām. Tomēr, tā kā dažas dzēšanas ir balstītas uz kopu, var būt scenāriji, kuros vienā darbībā var dzēst vairāk par 100 ierakstiem. Tāpēc dažreiz var rasties bloķēšanas eskalācijas.

## <a name="possible-user-impact"></a>Iespējamā lietotāja ietekme

Lietotāji var tikt ietekmēti, ja rīcībā esošo ierakstu tīrīšanas darbs dzēš visus ierakstus noteiktā līmenī (piemēram, unikālās noliktavas vienības līmenī). Šādā gadījumā funkcionalitāte, lai redzētu, ka krājumi iepriekš bijuši pieejami unikālajā noliktavas vienībā, iespējams, nedarbosies kā paredzēts, jo attiecīgie rīcībā esošie ieraksti vairs nav pieejami. Ar to var saskarties šādās situācijās:

- **Rīcībā esošo krājumu sarakstā**, kad lietotājs atceļ nosacījumu **Daudzums \<\> 0** atlasa nosacījumu **Slēgtas darbības** **Dimensiju rādīšanas** iestatījumos.
- **Fizisko krājumu pēc krājumu dimensijas** pārskatā par pagājušajiem periodiem, kad lietotājs iestata parametru **No datuma**.

Tomēr veiktspējas uzlabojums, ko nodrošina tīrīšanas darbs, vajadzētu kompensēt šos mazos funkcionalitātes zaudējumus.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Maksimālā izpildes laika iestatījuma iespējošana

Pēc noklusējuma iestatījums **Maksimālais izpildes laiks** nav pieejams. Ja vēlaties to lietot, ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu saistīto līdzekli jūsu sistēmā. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Maksimālais izpildes laiks noliktavas pārvaldības rīcībā esošo ierakstu tīrīšanas darbam*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]