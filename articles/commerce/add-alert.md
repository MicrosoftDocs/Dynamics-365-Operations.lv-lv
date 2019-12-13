---
title: Brīdinājuma modulis
description: Šajā tēmā ir ietverti brīdinājumu moduļi un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785356"
---
# <a name="alert-module"></a>Brīdinājuma modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir ietverti brīdinājumu moduļi un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Brīdinājuma modulis tiek izmantots, lai lapā rādītu iekļautos informatīvos ziņojumus. Brīdinājumu moduļi atbalsta teksta ziņojumu un saiti. Tos var izmantot, lai visā vietnē rādītu veicināšanas pasākumus, kas tiek rādīti visās e-komercijas vietnes lapās. 

Brīdinājumu moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Brīdinājumu moduļu piemēri E-komercijā

Brīdinājumu moduļus var izmantot vietnes galvenē, lai norādītu vietnes veicināšanas pasākumus un ziņojumus. Daži piemēri:

“Ikgadējā pārdošana beidzas pēc 10 dienām”

“Labi ietaupiet ar skolas sākuma izpārdošanu. Iepērcieties tūlīt.”

## <a name="alert-module-properties"></a>Brīdinājuma moduļa rekvizīti

| Rekvizīta nosaukums  | Vērtība                              | Apraksts |
|----------------|------------------------------------|-------------|
| Teksts           | Teksts                               | Brīdinājuma modulī redzamais teksta ziņojums. |
| Teksta līdzinājums | **Pa labi**, **Pa kreisi** vai **Centrā** | Vērtība, kas nosaka, kā brīdinājuma modulī tiek līdzināts teksts. |
| Noraidīt brīdinājumu  | **Patiess** vai **Nepatiess**              | Ja vērtība ir iestatīta uz **Patiess**, klients var noraidīt brīdinājumu. |
| Saistīt           | URL                                | Vietrādis URL neobligātai vietnei. |

## <a name="add-an-alert-module-to-a-page"></a>Brīdinājuma moduļa pievienošana lapā 

Lai pievienotu brīdinājuma moduli lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **brīdinājuma veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet brīdinājuma moduli.
1. Pārbaudiet veidni un publicējiet to. 
1. Izmantojiet jūsu tikko izveidoto brīdinājuma veidni, lai izveidotu lapu ar nosaukumu **brīdinājuma lapa**. 
1. Jaunās lapas **Galvenajā** slotā pievienojiet brīdinājuma moduli.
1. Brīdinājuma moduļa iestatījumos ievadiet brīdinājuma tekstu. Var rediģēt pārējos rekvizītus, ja vēlaties tālāk pielāgot brīdinājuma moduli.
1. Saglabājiet un priekšskatiet lapu. Lapas augšdaļā ieraudzīsiet brīdinājumu ar jūsu pievienoto tekstu.
1. Pārbaudiet lapu un publicējiet to. 

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Karuseļa modulis](add-carousel.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Līdzekļa modulis](add-feature-module.md)

[Centrālais modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)
