---
title: Jūs saņemsiet uzaicinājumu saglabāt krājumu vajadzības iestatījumus, pat ja izmaiņas nav veiktas
description: Jūs saņemsiet uzaicinājumu saglabāt krājumu vajadzības iestatījumus, pat ja izmaiņas nav veiktas.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 29ee23164430f219ff3d0c94216a8be43f480ce309f6cdac3dac6ed5b6d030af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730086"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Jūs saņemsiet uzaicinājumu saglabāt krājumu vajadzības iestatījumus, pat ja izmaiņas nav veiktas

KB numurs: 4615588

## <a name="symptoms"></a>Simptomi

Dažos scenārijos, varat saņemt šādu ziņojumu, atverot **krājumu vajadzības** lapu pēc tam, kad importējat krājumus, izmantojot *Krājumu vajadzības V2* elementu:

> Vai pirms aizvēršanas vēlaties saglabāt savas veiktās izmaiņas?

Jūs saņemat šo ziņojumu, kaut arī neesat veicis nekādas izmaiņas.

## <a name="resolution"></a>Novēršana

**Krājumu vajadzības** lapa ietver kompleksu noklusējumu loģiku, kas var izraisīt ziņojuma rādīšanu pēc tiešu izmaiņu veikšanas datubāzē, piemēram, izmantojot elementa importu. Piemēram, `AREGENERALSETTINGSOVERRIDDEN` elementa lauks ir iestatīts uz *Nē*, bet jūs importējiet failu, kas nodrošina jaunas vai modificētas vērtības tādiem laukiem kā `PRODUCTCOVERAGEGROUPID` un/vai `VENDORACCOUNTNUMBER`. Šajā gadījumā, tā kā lauks `AREGENERALSETTINGSOVERRIDDEN` ir iestatīts uz *Nē*, vērtības automātiski tiek notīrītas no laukiem, atverot **Krājumu vajadzības** lapu pirmo reiz pēc importēšanas. Ja izmaiņas saglabājat kā uzvednes ziņojumu, tās tiek saglabātas datu bāzē. Pretējā gadījumā nākamajā lapas atvēršanas reizē saņemsit to pašu ziņojumu.

Lai novērstu šo darbību, bet ietvertu arī vērtības tādiem laukiem kā `PRODUCTCOVERAGEGROUPID`, izmantojot elementa importēšanu, iestatiet `AREGENERALSETTINGSOVERRIDDEN` uz *Jā*, kad veicat importēšanu.
