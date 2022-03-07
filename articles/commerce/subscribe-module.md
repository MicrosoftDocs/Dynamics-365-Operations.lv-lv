---
title: Abonēšanas modulis
description: Šajā tēmā aplūkoti Abonēšanas moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 6440d761c07a33139babb9e07bdb251c6cb49676
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638806"
---
# <a name="subscribe-module"></a>Abonēšanas modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti Abonēšanas moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Abonēšanas moduļus var izmantot vietņu lapās, lai tvertu debitora informāciju biļeteniem vai veicināšanas pasākumiem.

Šajā ilustrācijā parādīts Adventure Works vietnes lapas kājenes abonēšanas moduļa piemērs.

![Adventure Works vietnes lapas kājenes abonēšanas moduļa piemērs](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Abonēšanas modulis ir pieejams Commerce moduļu bibliotēkā Dynamics 365 Commerce versijas 10.0.20 izlaidē.
> - Abonēšanas modulis tiek rādīts Adventure Works tēmā.
> - Abonēšanas modulim ir nepieciešams datu darbības paplašinājums, lai strādātu ar dažiem mārketinga e-pasta nodrošinātājiem, tādējādi biļetenu vai reklāmas e-pasta ziņojumus var nosūtīt pēc debitora informācijas tveršanas.

## <a name="subscribe-module-properties"></a>Abonēšanas moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts       | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Teksta virsraksts abonēšanas modulim, piemēram, **Abonēt biļetenu** vai **Pieteikties 10% atlaidei**. |
| Rindkopa     | Rindkopas teksts | Abonēšanas modulis atbalsta punktu tekstu bagātinātā teksta formātā, lai nodrošinātu papildu detaļas darbībai virsrakstā. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Abonēšanas moduļa pievienošana jaunā lapā

Lai pievienotu abonēšanas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus Commerce vietņu veidotājā, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un atveriet mārketinga veidni jūsu vietnes mājas lapai (vai izveidojiet jaunu mārketinga veidni).
1. Noklusējuma lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Abonēšana** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atveriet vietnes sākumlapu (vai izveidojiet jaunu mājas lapu, izmantojot mārketinga veidni).
1. Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Abonēšana** un pēc tam atlasiet **Labi**.
1. Abonēšanas moduļa rekvizītu rūtī pievienojiet virsrakstu, piemēram, **Abonēšana**.
1. Pievienojiet rindkopas tekstu, piemēram, **Jaunākās tendences, stili un veicināšanas pasākumi. Vai esat sarakstā? Abonējiet un saņemiet jaunākos karstos piedāvājumus!**
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Adventure Works tēma](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
