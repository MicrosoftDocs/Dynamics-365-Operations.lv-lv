---
title: Izmaksu aprēķināšanas versiju ierobežojumi standarta izmaksām
description: Šajā rakstā ir aprakstīti ierobežojumi, kas standarta izmaksu grāmatošanas versijai ir spēkā.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867990"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Izmaksu aprēķināšanas versiju ierobežojumi standarta izmaksām

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti ierobežojumi, kas standarta izmaksu grāmatošanas versijai ir spēkā. 

Tālāk norādītie ierobežojumi palīdz nodrošināt atbilstību standarta izmaksu aprēķināšanas principiem.

-  Krājuma izmaksās jābūt iekļautām maksām. Ražoto krājumu maksas attēlo amortizētās konstantās izmaksas materiālu komplektā (MK) un maršruta informācijā. Tādēļ maksām ir jābūt iekļautām vienības izmaksās. Arī maksas par iegādātiem krājumiem ir jāiekļauj krājuma vienības izmaksās.

-  Standarta izmaksu aprēķina pamatā par ražotajiem krājumiem ir jābūt izmaksu ierakstiem standarta izmaksu aprēķināšanas versijā. Izmaksu datu alternatīvos avotus var izmantot tikai izmaksu aprēķināšanas versijai plānotajām izmaksām, piemēram, iegādāto krājumu pirkšanas cenas tirdzniecības līgumiem. Izmaksu datu alternatīvos avotus definē MK aprēķinu grupa.

-  MK aprēķinus ir jāveic viena līmeņa izvēršanas režīmā.

Standarta izmaksu krājumu izmaksu datus iespējams kopēt uz citu izmaksu versiju, kas ietver standarta vai plānotās izmaksas. Tomēr, krājumu izmaksu datus plānotajām izmaksām nevar kopēt uz izmaksu versiju, kas satur standarta izmaksas, jo agrāk uzskaitītie ierobežojumi šajā rakstā neattiecas uz plānotajām izmaksām.

## <a name="related-articles"></a>Saistītie raksti

[Izmaksu aprēķināšanas versiju pārskats](costing-versions.md)

[Atjaunināt standarta izmaksas neražošanas vidē](update-standard-costs-non-manufacturing-environment.md)

[Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]