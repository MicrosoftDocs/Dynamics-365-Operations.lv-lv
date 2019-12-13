---
title: Karuseļa modulis
description: Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785241"
---
# <a name="carousel-module"></a>Karuseļa modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Karuseļa modulis tiek izmantots, lai izvietotu vairākus reklāmas elementus karuselī, ko klienti var pārlūkot. Tas ir īpašs konteinera modulis, kas vieso citus moduļus. Piemēram, mazumtirgotājs var izmantot karuseļa moduli sākumlapā, lai parādītu vairākas jaunas preces vai veicināšanas pasākumus.

Karuseļa modulī varat pievienot centrālos un funkciju moduļus. Karuseļa moduļa rekvizīti nosaka, kā šie moduļi tiek atveidoti.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Karuseļa moduļu piemēri E-komercijā

- Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots sākumlapā.
- Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots preču informācijas lapā.
- Karuseli var izmantot jebkurā mārketinga lapā, lai reklamētu vairākus veicināšanas pasākumus vai preces.

## <a name="carousel-module-properties"></a>Karuseļa moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                                | Apraksts |
|---------------------------|--------------------------------------|-------------|
| Automātiskā atskaņošana                  | **Patiess** vai **Nepatiess**                | Ja vērtība ir iestatīta uz **Patiess**, pāreja starp elementiem karuselī tiek veikta automātiski. Ja vērtība ir iestatīta uz **Nepatiess**, pāreja netiek veikta, ja vien klients neizmanto tastatūru vai peli, lai pārvietotos no viena elementa uz nākamo. |
|  Slaidu pārejas intervāls | Vērtība sekundēs                   | Intervāls pārejām starp elementiem. |
| Pārejas animācija      | **Slīdināt** vai **Izbalēt**                | Pārejas efekts. |
| Platums                     | **Ietilpināt konteinerā** vai **Pilnekrāna režīms** | Ja vērtība ir iestatīta uz **Ietilpināt konteinerā**, tad elementi karuselī tiek ierobežoti ar karuseļa platumu. Ja vērtība ir iestatīta uz **Aizpildīt ekrānu**, elementi neaprobežojas ar karuseļa platumu, bet var pāriet pilnekrāna režīmā. Varat mainīt vērtību, lai sasniegtu vēlamo izkārtojumu. |

## <a name="add-a-carousel-module-to-a-page"></a>Karuseļa moduļa pievienošana lapā

Lai pievienotu karuseļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **karuseļa veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet karuseļa moduli.
1. Pievienojiet centrālo moduli karuseļa modulim.
1. Pievienojiet līdzekļa moduli karuseļa modulim.
1. Pārbaudiet veidni un publicējiet to. 
1. Izmantojiet jūsu tikko izveidoto karuseļa veidni lapas ar nosaukumu **karuseļa lapa** izveidei.
1. Jaunās lapas **Galvenajā** slotā pievienojiet karuseļa moduli.
1. Iestatiet karuseļa moduļa rekvizītu **Platums**, lai **Aizpildītu ekrānu**. 
1. Iestatiet rekvizītu **Pārejas animācija** uz **Slīdināt**.
1. Pievienojiet centrālo moduli karuseļa modulim.
1. Centrālajā modulī pievienojiet attēlu un virsrakstu un pēc tam atlasiet **Saglabāt**.
1. Pievienojiet līdzekļa moduli karuseļa modulim.
1. Līdzekļa modulī pievienojiet attēlu, virsrakstu un teksta rindkopu.
1. Saglabājiet un priekšskatiet lapu. Lapā ir jāparāda karuselis, kurā ir divi moduļi (centrālais modulis un līdzekļa modulis). Lai sasniegtu vēlamo efektu, varat mainīt papildus rekvizītus karuselim, centrālajam un līdzekļa modulim.
1. Pārbaudiet lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Brīdinājuma modulis](add-alert.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Līdzekļa modulis](add-feature-module.md)

[Centrālais modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)
