---
title: Transportēšanas pārvaldības programmas
description: Transportēšanas pārvaldības programmas definē loģiku, ko izmanto, lai izveidotu un apstrādātu transportēšanas likmes transportēšanas pārvaldības procesā.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aed20a4dc554db5d4c9bfe10992accc6ec719147
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233467"
---
# <a name="transportation-management-engines"></a>Transportēšanas pārvaldības programmas

[!include [banner](../includes/banner.md)]

Transportēšanas pārvaldības programmas definē loģiku, ko izmanto, lai izveidotu un apstrādātu transportēšanas likmes transportēšanas pārvaldības procesā. 

Transportēšanas pārvaldības programma aprēķina uzdevumus, piemēram, pārvadātāja transportēšanas likmi. Programmas sistēma ļauj mainīt aprēķina stratēģijas izpildlaikā, pamatojoties uz Supply Chain Management datiem. Transportēšanas pārvaldības programma līdzinās spraudnim, kas attiecas uz konkrēta pārvadātāja līgumu.

## <a name="what-engines-are-available"></a>Kādas programmas ir pieejamas?
Tālāk sniegtajā tabulā ir norādītas transportēšanas pārvaldības programmas, kas ir pieejamas.

| Transportēšanas pārvaldības programma | Apraksts                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Likmes noteikšanas programma**                  | Aprēķina likmes.                                                                                                                                                                                                                                                                                                           |
| **Vispārīgā programma**               | Vienkāršas papildu programmas, ko izmanto citas programmas, kam nav nepieciešami dati no Supply Chain Management, piemēram, norīkojumu programma. Norīkojumu programmas izmanto, lai samazinātu transportēšanas gala izmaksas noteiktiem pasūtījumiem un rindām, pamatojoties uz dimensijām, piemēram, apjomu un svaru. |
| **Attāluma noteikšanas programma**               | Aprēķina transportēšanas attālumu.                                                                                                                                                                                                                                                                                     |
| **Tranzīta laika noteikšanas programma**          | Aprēķina laiku, kas ir nepieciešams, lai transportētu no sākuma līdz beigu punktam.                                                                                                                                                                                                                                       |
| **Zonas noteikšanas programma**                  | Aprēķina zonu, pamatojoties uz pašreizējo adresi, un aprēķina zonu skaitu, kas jāšķērso, lai transportētu no adreses A uz adresi B.                                                                                                                                                                    |
| **Kravas pavadzīmes veids**            | Standartizē kravas rēķina un kravas pavadzīmes rindas. Izmantot automātiskai kravas pavadzīmes salīdzināšanai.                                                                                                                                                                                                                |


<a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Kuras programmas ir jākonfigurē, lai sūtījumam izveidotu likmes?
---------------------------------------------------

Lai izveidotu likmes sūtījumam, kam tiek izmantots noteikts pārvadātājs, ir jākonfigurē vairākas transportēšanas pārvaldības programmas. **Likmes noteikšanas programma** ir obligāti nepieciešama, taču, lai nodrošinātu **likmes noteikšanas programmas** atbalstu, var būt nepieciešamas citas transportēšanas pārvaldības programmas. Piemēram **likmes noteikšanas programmu** var izmantot, lai izgūtu datus no **attāluma noteikšanas programmas** un aprēķinātu likmi, pamatojoties uz attālumu starp avotu un mērķi.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Kas ir nepieciešams, lai inicializētu transportēšanas pārvaldības programmu?
Lai transportēšanas pārvaldības programma darbotos noteiktā veidā, tai ir jāiestata inicializēšanas dati. Ir jāiestata tālāk minētie, bet ne tikai, dati.
-   Atsauces uz citām transportēšanas pārvaldības programmām. Papildinformāciju skatiet šajā sadaļā sniegtajā konfigurācijas piemērā.
-   Atsauces uz .NET veidiem, ko lieto transportēšanas pārvaldības programma.
-   Vienkārši konfigurācijas dati.

Vairumā gadījumu, lai konfigurētu inicializēšanas datus, varat noklikšķināt uz transportēšanas pārvaldības programmas iestatīšanas veidlapā esošās pogas **Parametri**. **Tādas likmes noteikšanas programmas konfigurēšana, kurā ir atsauce uz attāluma noteikšanas programmu** Tālāk sniegtajā piemērā ir aprakstīta iestatīšana, kas ir nepieciešama likmes noteikšanas programmai, kuras pamatā ir .NET programmas tips Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine un kurā ir atsauce uz attāluma noteikšanas programmu.

|          Parametrs           |                                                                                  Apraksts                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET veids, kas izskaidro likmes bāzes piešķires datus konkrētai shēmai. Parametra vērtības sintakse sastāv no diviem segmentiem, kas ir atdalīti ar vertikālo joslu ( |
|  <em>MileageEngineCode</em>  |                       Attāluma noteikšanas programmas kods, kas identificē attāluma noteikšanas programmas ierakstu datu bāzē.                        |
| <em>ApportionmentEngine</em> |                        Vispārīgās programmas kods, kas identificē norīkojumu programmu datu bāzē.                        |

<a name="how-is-metadata-used-in-transportation-management-engines"></a>Kā transportēšanas pārvaldības programmas izmanto metadatus?
----------------------------------------------------------

Transportēšanas pārvaldības programmas, kas izmanto programmatūrā Supply Chain Management definētos datus, var izmantot dažādas datu shēmas. Transportēšanas pārvaldības sistēma ļauj dažādām transportēšanas pārvaldības programmām izmantot vienas un tās pašas vispārējo fizisko datu bāžu tabulas. Lai nodrošinātu, ka programmas datu izpildes laika interpretācija ir pareiza, varat definēt metadatus datu bāzes tabulām. Tas samazina jaunu transportēšanas pārvaldības programmu izstrādes izmaksas, jo sistēmā Operations nav nepieciešamas papildu tabulu un veidlapu struktūras.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Ko var izmantot likmes aprēķinos kā meklēšanas datus?
Datus, kas tiek izmantoti, aprēķinot likmes, kontrolē metadatu konfigurācija. Piemēram, ja likmes vēlaties meklēt, pamatojoties uz pasta indeksiem, metadati jāiestata, pamatojoties uz pasta indeksa uzmeklēšanas veidu.

## <a name="do-all-engine-configurations-require-metadata"></a>Vai visām programmas konfigurācijām ir nepieciešami metadati?
Nē, transportēšanas pārvaldības programmām, kas tiek izmantotas likmju aprēķiniem nepieciešamo datu izgūšanai no ārējām sistēmām, metadati nav nepieciešami. Likmju datus šīm programmām var izgūt no ārējām transportēšanas pārvadātāju sistēmām, parasti izmantojot tīmekļa pakalpojumu. Piemēram, varat izmantot attāluma noteikšanas programmu, kas tieši izgūst datus no pakalpojuma Bing kartes, tādēļ metadati šai programmai nav nepieciešami.

| **Piezīme.**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transportēšanas pārvaldības programmas, kas tiek nodrošinātas kopā ar Supply Chain Management, izmanto datus, kas tiek izgūti no programmas. Programmas, kas veido savienojumu ar ārējām sistēmām, nav ietvertas sistēmas Operations komplektācijā. Taču, lietojot programmu paplašināšanas modeli, paplašinājumus var izveidot, izmantojot programmatūru Visual Studio Tools. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Kā konfigurēt metadatus transportēšanas pārvaldības programmai?
Dažādām transportēšanas pārvaldības programmām metadatus konfigurē atšķirīgi.

| Transportēšanas pārvaldības programma               | Metadatu konfigurēšana                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Likmes noteikšanas programma**                                | Ir nepieciešams **likmes bāzes veids**. Likmes bāzes veids satur likmes pamatdatu metadatus un likmes bāzes piešķires datus. Likmes bāzes metadatu struktūru nosaka likmes noteikšanas programmas veids. Likmes bāzes piešķires metadatu struktūru nosaka likmes bāzes piešķīrēja veids, kas ir saistīts ar šo likmes noteikšanas programmu. Likmes noteikšanas programmas likmes bāzes veidu var iestatīt lapās **Likmes noteikšanas programma** un **Likmes šablons**. |
| **Zonas noteikšanas programma**                                | Metadati jāiestata tieši zonas šablonā.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Pārvadājumu ilguma noteikšanas programma** un **attāluma noteikšanas programma** | Izgūst metadatus tieši no attāluma noteikšanas programmas konfigurācijas iestatījumu formas.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Likmes noteikšanas programmas metadatu piemērs** Transportēšanas pārvaldības programmā ir jānorāda sūtījuma izcelsmes adrese, galamērķa administratīvais apgabals un valsts/reģions un sākuma un beigu punkts. Izmantojot šīs prasības, metadati izskatīsies kā tālāk sniegtajā tabulā norādītie dati. Tabulā ir sniegta arī informācija par nepieciešamo datu veidu.
-   Definējiet šo informāciju sadaļā **Transportēšanas pārvaldība** &gt; **Iestatīšana** lapā **Likmes bāzes veids**.

| Sērija | Nosaukums                          | Lauka tips | Datu tips | Uzmeklēšanas tips    | Obligāts |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Izcelsmes pasta indekss            | Piešķire | Virkne    | Pasta indekss    | Atlasīts  |
| 2        | Galamērķa administratīvais apgabals             | Piešķire | Virkne    | Valsts          |           |
| 3        | Galamērķa sākuma pasta indekss | Piešķire | Virkne    | Pasta indekss    | Atlasīts  |
| 4.        | Galamērķa beigu pasta indekss   | Piešķire | Virkne    | Pasta indekss    | Atlasīts  |
| 5.        | Galamērķa valsts           | Piešķire | Virkne    | Valsts/reģions |           |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]