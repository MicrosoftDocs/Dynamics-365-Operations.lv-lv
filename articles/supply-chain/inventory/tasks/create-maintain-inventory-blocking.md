---
title: Krājuma bloķēšanas izveide un uzturēšana
description: Šajā tēmā aprakstīts, kā izmantot krājumu aizturēšanu, lai novērstu fiziski rīcībā esošo krājumu rezervēšanu citos izejošajos pirmdokumentos.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d602abe4491f6cbbd0fce25a566acf97a25f3bf1e6214e95c80fda2638d14dde
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773279"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Krājuma bloķēšanas izveide un uzturēšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts, kā izmantot krājumu aizturēšanu, lai novērstu fiziski rīcībā esošo krājumu rezervēšanu citos izejošajos pirmdokumentos. Pirms sākat procedūras šajā tēmā, jābūt krājumam, kuram ir pieejami fiziski rīcībā esošie krājumi.

## <a name="block-inventory"></a>Bloķēt krājumus

Lai izveidotu krājuma aizturēšanas ierakstu tā, ka krājumi tiek bloķēti, rīkojieties šādi.

1. Dodieties uz **Krājumu vadība \> Periodiskie uzdevumi \> Krājumu aizturēšana**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunā aizturēšanas ieraksta virsrakstā iestatiet lauku **Krājuma numurs** precei, kuru vēlaties bloķēt, un ievadiet aprakstu.
1. Kopsavilkuma cilnē **Vispārīgi** laukā **Daudzums** ievadiet bloķējamo vienumu skaitu.
1. Kopsavilkuma cilnē **Krājumu dimensijas** norādiet vietu un noliktavu, kur krājumi, ko vēlaties bloķēt, pašlaik atrodas.
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Krājumu bloķēšanas nosacījumu atjaunināšana

Lai atjauninātu krājuma aizturēšanas ierakstu, rīkojieties šādi.

1. Dodieties uz **Krājumu vadība \> Periodiskie uzdevumi \> Krājumu aizturēšana**.
1. Saraksta rūtī atlasiet atbilstošo aizturēšanas ierakstu.
1. Pēc nepieciešamības rediģējiet ierakstu. Piemēram, var mainīt lauka **Paredzamais datums** vērtību, lai norādītu, kad bloķētajiem krājumiem ir jābūt pieejamiem rezervācijai. Ja ir atlasīta opcija **Plānotie ieņēmumi**, plānotajai transakcijai parādīsies datums. (Opcija **Paredzamā saņemšana** tiek atlasīta pēc noklusējuma, manuāli veidojot aizturēšanas ierakstu.)
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="unblock-inventory"></a>Krājumu atbloķēšana

Lai noņemtu krājuma aizturēšanas ierakstu tā, ka krājumi tiek atbloķēti, rīkojieties šādi.

1. Dodieties uz **Krājumu vadība \> Periodiskie uzdevumi \> Krājumu aizturēšana**.
1. Saraksta rūtī atlasiet atbilstošo aizturēšanas ierakstu.
1. Darbību rūtī atlasiet **Dzēst**.
1. Tiek piedāvāts apstiprināt operāciju. Lai turpinātu, atlasiet **Jā**.
1. Aizvērt lapu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
