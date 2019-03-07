---
title: Ziņošana par MK pabeigšanu
description: Šajā rakstā ir sniegta informācija par ziņošanu par MK pabeigšanu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80bda7dd469bc5c07ba0160e5e8c349ed2137fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "340986"
---
# <a name="report-boms-as-finished"></a>Ziņošana par MK pabeigšanu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par ziņošanu par MK pabeigšanu.

Lapa **Ziņot kā pabeigtu** un **Maksimālais pabeigto krājumu daudzums** tiek lietotas, lai paziņot par materiālu komplektu (MK) pabeigšanu. Konceptuāli ziņošana par MK pabeigšanu ir tāds pats process kā ziņošana par ražošanas pasūtījuma pabeigšanu. Šo procesu var izmantot, piemēram, vienkāršos montāžas un komplektēšanas procesos, kur ražošanas pasūtījumiem nav nepieciešamas papildu iespējas. Lapa **Ziņot kā pabeigtu** jums ļauj ziņot par vairāku MK pabeigšanu vienā partijā. Lapā **Maksimālais pabeigto krājumu daudzums** vienlaikus varat ziņot tikai par viena MK pabeigšanu. Lapai **Ziņot kā pabeigtu** var piekļūt, izmantojot izvēlnes elementu modulī Krājumu vadība, un abām lapām var piekļūt, izmantojot izvēlnes elementus lapā **Izlaistās preces**.

## <a name="report-as-finished-page"></a>Lapa Ziņot kā pabeigtu
Ja lapu **Ziņot kā pabeigtu**atverat no kādas izlaistas preces, tad šī lapa jums piedāvā ziņot par standarta noklusējuma daudzuma pabeigšanu. Pēc noklusējuma tiek parādīta aktīvā MK versija, bet šo MK versiju varat mainīt, ja pastāv citas apstiprinātās versijas. Šī lapa jums ļauj arī dzēst ierakstus un izveidot jaunus ierakstus izlaistajām precēm, par kurām ir jāziņo kā par pabeigtām. Lai izmantotu vaicājumu preču atlasīšanai, noklikšķiniet uz izvēlnes vienuma **Atlasīt**. Atlasītajām precēm varat manuāli apstiprināt ziņošanu par pabeigšanu, noklikšķinot uz **Labi**. Alternatīvi varat iestatīt, lai šis process tiek izpildīts partijā. Kad ir apstiprināta ziņošana par pabeigšanu, sistēma ģenerē MK žurnālu, kur tiek apstrādāta grāmatošana krājumos. Šis žurnāls sastāv no viena rindas krājuma pabeigtajai precei un viena rindas krājuma katrai MK rindai. Varat kontrolēt, vai šis žurnāls tiek grāmatots automātiski vai paliek atvērts papildu korekcijām.

## <a name="max-report-as-finished-page"></a>Maks. pabeigto krājumu daudzums (lapa)
Lapā **Maksimālais pabeigto krājumu daudzums** katra MK rinda norāda preces gabalu skaitu, ko var ziņot kā pabeigtu. Šis aprēķins ir balstīts uz katras materiālu rindas fiziski pieejamajiem rīcībā esošajiem krājumiem. Nākamajā piemērā viens gabals krājuma koda FG patērē divus gabalus izejmateriāla RM10 un vienu gabalu izejmateriāla RM20. Tā kā rīcībā ir tikai 10 gabali RM10, tad maksimālais daudzums FG, par ko var ziņot kā pabeigtu, ir pieci gabali. Šī vērtība tiek rādīta laukā **Maksimālais pabeigto krājumu daudzums**.

| Līmenis | Krājuma kods | Daudzums | Rīcībā esošs | Maks. Ziņot kā pabeigtu |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>MK, kuriem ir vairāki līmeņi
Ja MK ir vairāki līmeņi, tad varat kontrolēt, kā materiāli tiek uzskaitīti visos līmeņos, izmantojot lauku **Izvēršana**. Šis lauks ir pieejams gan lapā **Ziņot kā pabeigtu**, gan lapā **Maksimālais pabeigto krājumu daudzums**. Pieejamas šādas opcijas

-   **Nekad** — ja pastāv materiālu iztrūkums, pamata MK netiek izvērsti.
-   **Vienmēr** — visi pamata MK tiek pilnīgi izvērsti. Tāpēc netiek izmantoti nekādi brīvie rīcībā esošie krājumi daļēji pabeigtiem komponentu krājumiem.
-   **Iztrūkums** — pamata MK tiek izvērsti tikai tad, ja nav pieejams viss nepieciešamā materiāla daudzums.

### <a name="example"></a>Piemērs

Šajā piemērā trīs gabali pabeigtās preces (krājuma kods FG) ir gatavas ziņošanai par pabeigšanu. Pastāv divu līmeņu MK, kā šeit parādīts.

| Līmenis | Krājuma kods | MK rindas daudzums | Rīcībā esošs |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Nākamajās tabulās ir parādīts, kā lauka **Izvēršana** iestatījums ietekmē veidu, kā tiek ģenerētas MK žurnāla rindas. **Izvēršana: Nekad**

| Līmenis | Krājuma kods | Daudzums |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Kā tas ir redzams iepriekš esošajā tabulā, žurnālā par atskaitītu tiek uzskatīts tikai krājums ar kodu COMP. Krājums ar kodu RM, kas ir daļa no krājuma ar kodu COMP, netiek izvērsts žurnāla rindā, un divas rīcībā esošās krājuma COMP vienības netiek ņemtas vērā. **Izvēršana: Vienmēr**

| Līmenis | Krājuma kods | Daudzums |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

Šajā gadījumā krājums ar kodu COMP ir izvērsts tā izejmateriālā, krājumā ar kodu RM. Abi rīcībā esošie COMP gabali patērējamajā RM daudzumā netiek ņemti vērā. **Izvēršana: Iztrūkums**

| Līmenis | Krājuma kods | Daudzums |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

Šajā gadījumā abi krājumam koda COMP rīcībā esošie gabali tiek ņemti vērā. Taču, tā kā ir nepieciešami trīs gabali krājuma ar kodu FG, tad ir nepieciešams arī viens gabals krājuma ar kodu RM, lai saražotu vienu papildu gabalu ar kodu COMP.



