---
title: Izmaksu aprēķināšanas versiju ierobežojumi standarta izmaksām
description: Šajā tēmā aprakstīti ierobežojumi, kas tiek lietoti standarta izmaksu aprēķināšanas versijai.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2348d7721cd281bb2a1b5af007c98ce69377a412
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214439"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Izmaksu aprēķināšanas versiju ierobežojumi standarta izmaksām

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīti ierobežojumi, kas tiek lietoti standarta izmaksu aprēķināšanas versijai. 

Tālāk norādītie ierobežojumi palīdz nodrošināt atbilstību standarta izmaksu aprēķināšanas principiem.

-  Krājuma izmaksās jābūt iekļautām maksām. Ražoto krājumu maksas attēlo amortizētās konstantās izmaksas materiālu komplektā (MK) un maršruta informācijā. Tādēļ maksām ir jābūt iekļautām vienības izmaksās. Arī maksas par iegādātiem krājumiem ir jāiekļauj krājuma vienības izmaksās.

-  Standarta izmaksu aprēķina pamatā par ražotajiem krājumiem ir jābūt izmaksu ierakstiem standarta izmaksu aprēķināšanas versijā. Izmaksu datu alternatīvos avotus var izmantot tikai izmaksu aprēķināšanas versijai plānotajām izmaksām, piemēram, iegādāto krājumu pirkšanas cenas tirdzniecības līgumiem. Izmaksu datu alternatīvos avotus definē MK aprēķinu grupa.

-  MK aprēķinus ir jāveic viena līmeņa izvēršanas režīmā.

Standarta izmaksu krājumu izmaksu datus iespējams kopēt uz citu izmaksu versiju, kas ietver standarta vai plānotās izmaksas. Tomēr krājumu izmaksu datus plānotajām izmaksām nevar kopēt uz izmaksu versiju ar standarta izmaksām, jo iepriekš šajā tēmā uzskaitītie ierobežojumi neattiecas uz plānotajām izmaksām.

<a name="related-topics"></a>Saistītās tēmas
--------

[Izmaksu aprēķināšanas versiju pārskats](costing-versions.md)

[Atjaunināt standarta izmaksas neražošanas vidē](update-standard-costs-non-manufacturing-environment.md)

[Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas](update-standard-costs-manufacturing-environment.md)

