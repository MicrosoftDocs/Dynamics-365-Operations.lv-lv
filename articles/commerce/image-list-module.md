---
title: Attēlu saraksta modulis
description: Šajā tēmā tiek stāstīts par attēlu saraksta moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67da83410d819d01396d0b7d421076ee3b0f17ec
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780847"
---
# <a name="image-list-module"></a>Attēlu saraksta modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par attēlu saraksta moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

Attēlu saraksta moduli var izmantot, lai vietnes lapām viegli pievienotu attēlu kolekciju (masīvu). Katru attēlu masīvā var konfigurēt ar punktu tekstu un saistīt vietrāžus URL. Attēlu saraksta modulis ir piemērots zīmola logotipu vai saraksta, kas ietver logotipus, rādīšanai.

> [!IMPORTANT]
> - Attēlu saraksta modulis ir pieejams Commerce moduļu bibliotēkā Dynamics 365 Commerce versijas 10.0.20 izlaidē.
> - Attēla saraksta modulis tiek rādīts Adventure Works tēmā.

Šajā attēlā parādīts piemērs, kad attēlu saraksta modulī tiek parādīts saraksts ar tekstu, kas iekļauj logotipus Adventure Works uzņēmuma-patērētāja lapā (B2C).

![Attēlu saraksta moduļa piemērs, kurā parādīts saraksts ar tekstu, kas ietver logotipus](./media/Image_list.PNG)

Šajā attēlā parādīts piemērs, kad attēlu saraksta modulī tiek parādīts zīmola logotipus Adventure Works uzņēmuma-uzņēmuma lapā (B2B).

![Tā attēlu saraksta moduļa piemērs, kurā tiek rādīti zīmola logotipi](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Attēlu saraksta moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts       | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Attēlu saraksta moduļa teksta virsraksts. |
| Attēlu saraksts    | Attēli, teksts un vietrāži URL | Katrs masīva elements ir attēls, kas pievienots ar punktu tekstu un URL. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Pievienot attēlu saraksta moduli jaunai lapai

Lai pievienotu attēlu saraksta moduli jaunā lapā un iestatītu nepieciešamos rekvizītus Commerce vietņu veidotājā, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un atveriet mārketinga veidni jūsu vietnes mājas lapai (vai izveidojiet jaunu mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet attēlu saraksta **moduli** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atveriet vietnes sākumlapu (vai izveidojiet jaunu mājas lapu, izmantojot mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet sarakstu Attēls **un** pēc tam atlasiet **Labi**.
1. Attēlu saraksta moduļa rekvizītu rūtī pievienojiet virsrakstu (piemēram, **Mūsu zīmoli**).
1. Pievienojiet attēlu saraksta elementu un norādiet attēlu, daļu no punktu teksta un novirzīšanas URL.
1. Pievienojiet un konfigurējiet papildu attēlu sarakstu krājuma moduļus pēc nepieciešamības.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Adventure Works tēma](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
