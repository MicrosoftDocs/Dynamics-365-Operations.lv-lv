---
title: BYOD plānoto pakešuzdevumu optimizēšana
description: Šajā tēmā ir izskaidrots, kā optimizēt veiktspēju, kad lietojat savu datu bāzes (BYOD) līdzekli, izmantojot Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: ed3ebbf09403090a1173c3cda1a4b11b74419b90
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052677"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>BYOD plānoto pakešuzdevumu optimizēšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā ir izskaidrots, kā optimizēt veiktspēju, kad lietojat savu datu bāzes (BYOD) līdzekli. Plašāku informāciju par BYOD skatiet [Lietot savu datu bāzi (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Veiktspējas apsvērumi datu eksportam

Kad entītijas ir publicētas mērķa datu bāzē, varat izmantot eksporta funkciju **Datu pārvaldības** darbvietā, lai pārvietotu datus. Eksporta funkcija ļauj definēt Datu kustības darbu, kas ietver vienu vai vairākas entītijas. Papildinformāciju par datu pārvaldību skatiet [Datu importēšanas un eksportēšanas darbu apskats](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Varat izmantot **Eksporta** lapu, lai eksportētu datus uz dažādiem mērķa datu formātiem, piemēram, komatatdalīto vērtību (CSV) failu. Šī lapa atbalsta arī SQL datu bāzes kā citu mērķi.

Varat izveidot datu projektu, kam ir vairāki elementi, un izmantot pakešuzdevumu, lai plānotu šī datu projekta palaišanu. Ja atlasāt opciju **Eksportēt pakešuzdevumā**, varat ieplānot periodisku datu eksporta darbu.

Lai palīdzētu saglabāt BYOD eksporta vispārējo uzticamību, jums ir jāuzmanās, kad eksporta projektam pievienojat vairākus elementus. Kad tiek noteikts entītiju skaits, kas jāpievieno vienam projektam, apsveriet šādus parametrus:

- Entītiju sarežģītība
- Paredzamais datu apjoms pa vienībām
- Kopējais laiks, kas būs nepieciešams, lai pabeigtu eksportēšanu darba līmenī

Lai panāktu vislabāko veiktspēju, centieties pievienot simtiem entītiju vienam projektam. Ieteicams izveidot vairākus darbus, no kuriem katrs ietver mazāk entītiju.

## <a name="scheduling-byod-batch-jobs"></a>BYOD pakešuzdevumu plānošana

Lai palīdzētu samazināt ietekmi uz Microsoft Dynamics 365 Human Resources lietotājiem, palaidiet BYOD pakešuzdevumus naktī vai pēc darba stundām. Noteikti pārbaudiet periodisko pakešuzdevumu laika joslu. Daži pakešuzdevumi izmanto Klusā okeāna standarta laiku (PST).

Lai palīdzētu izvairīties no veiktspējas problēmām, konfigurējot plānošanas biežumu BYOD pakešuzdevumiem, apsveriet šādus faktorus:

- Laiks, kas nepieciešams, lai pabeigtu katru pakešuzdevumu
- BYOD datiem nepieciešamais bizness

Iestatiet katra pakešuzdevuma biežumu uz vērtību, kas nodrošina, ka darbu var pabeigt krietni pirms nākamā plānotā izpildes laika. Izvairieties darbināt vairākus darbus paralēli, jo šī pieeja var negatīvi ietekmēt Human Resources veiktspēju.

Lai iegūtu vislabākos rezultātus, vienmēr izmantojiet opciju **Eksportēt pakešuzdevumā** lapā **Eksports**, lai ieplānotu BYOD pakešuzdevumus. Izvairieties plānot periodisku eksportu **Pārvaldīt \> Pārvaldīt periodisko datu darbus**.

## <a name="incremental-export"></a>Inkrementāla eksportēšana

Kad pievienojat entītiju datu eksportam, varat darīt vai nu pakāpenisku (eksports), vai pilnu virzību. Pilna virzība dzēš visus esošos ierakstus no elementa BYOD datu bāzē. Pēc tam tā ievieto pašreizējo ierakstu kopu no Human Resources elementa.

Lai veiktu pakāpenisko virzību, ir jāieslēdz izmaiņu izsekošana katram elementam **Elementu** lapā. Lai iegūtu papildu informāciju, skatiet [Iespējot izmaiņu izsekošanu entītijām](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Ja izvēlaties pakāpenisko virzību, pirmā virzība vienmēr ir pilnā virzība. SQL izseko izmaiņas no šīs pirmās pilnās virzības. Kad tiek ievietots jauns ieraksts vai ieraksts tiek atjaunināts vai dzēsts, izmaiņas tiek atspoguļotas mērķa entītijā.

## <a name="time-outs"></a>Pārtraukums

Šeit ir BYOD eksporta noklusējuma pārtraukumi:

- Desmit minūtes saīsināšanas operācijām
- Viena stunda lielapjoma ievietošanas operācijām

Kad apjomi ir augsti, šie pārtraukuma iestatījumi var nebūt pietiekami. Lai tos atjauninātu, dodieties uz **Datu pārvaldība \> Struktūras parametri \> Lietot savu datu bāzi**. Šie pārtraukumi ir specifiski uzņēmumam, un tie ir jāiestata atsevišķi katram uzņēmumam.

## <a name="known-limitations"></a>Zināmie ierobežojumi

BYOD līdzeklim ir šādi ierobežojumi:

- Sinhronizācijas laikā datu bāzē nedrīkst būt aktīvas slēdzenes. Aktīvās slēdzenes var izraisīt lēnu rakstīšanu vai pat nespēju eksportēt datus uz jūsu Azure SQL datu bāzi.
- Jūs nevarat eksportēt saliktos elementus savā datu bāzē. Pašlaik kompozītās entītijas netiek atbalstītas. Ir jāeksportē atsevišķas struktūras, kas veido kompozītu elementu. Tomēr varat eksportēt abus elementus vienā un tajā pašā datu projektā.
- Entītijas, kurām nav unikālu atslēgu, nevar eksportēt, izmantojot pakāpenisko virzību. Varat sastapties ar šo ierobežojumu, īpaši, ja mēģināt pakāpeniski eksportēt ierakstus no dažām gatavām entītijām. Tā kā šīs struktūras tika veidotas, lai iespējotu datu importu, tām nav unikāla atslēga.

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="incremental-push-doesnt-work-correctly"></a>Pakāpeniskā virzība nedarbojas pareizi

**Problēma:** kad elements ir pilnībā novirzīts, jūs redzat lielu ierakstu kopu BYOD, kad izmantojat **Atlasīt** izrakstu. Tomēr, kad veicat pakāpenisko virzību, ir redzami tikai daži ieraksti BYOD. Šķiet, it kā pakāpeniskā virzība dzēsa visus ierakstus un pievienoja tikai mainītos ierakstus BYOD.

**Risinājums:** SQL izmaiņu izsekošanas tabulas var nebūt paredzētajā stāvoklī. Šāda veida gadījumos iesakām izslēgt izmaiņu izsekošanu entītijai un pēc tam to atkal ieslēgt. Lai iegūtu papildu informāciju, skatiet [Iespējot izmaiņu izsekošanu entītijām](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Izstādīšanas tabulas netiek tīrītas

**Problēma:** izmantojot projekta izstādīšanu, izstādīšanas tabulas netiek pareizi notīrītas. Dati tabulās turpina pieaugt, radot veiktspējas problēmas.

**Risinājums:** izstādīšanas tabulās saglabājas septiņas vēstures dienas. Vēsturiskie dati, kas vecāki par septiņām dienām, tiek automātiski notīrīti no izstādīšanas tabulām, izmantojot pakešuzdevumu **Importēšanas eksporta izstādīšanas tīrīšana**. Ja šis darbs iestrēgs, tabulas netiks pareizi notīrītas. Šī pakešuzdevuma restartēšana turpinās procesu, lai automātiski notīrītu izstādīšanas tabulas.

## <a name="see-also"></a>Skatiet arī

[Datu pārvaldības pārskats](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Savas datu bāzes izmantošana (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Datu importēšanas un eksportēšanas darbu pārskats](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Izmaiņu izsekošanas iespējošana elementiem](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
