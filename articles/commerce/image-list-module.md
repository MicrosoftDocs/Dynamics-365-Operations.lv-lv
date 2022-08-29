---
title: Attēlu saraksta modulis
description: Šajā rakstā ir apskatīti attēlu saraksta moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: e89624a98d3cbdd861391e994386ae57d2c38aa0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269840"
---
# <a name="image-list-module"></a>Attēlu saraksta modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti attēlu saraksta moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

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
