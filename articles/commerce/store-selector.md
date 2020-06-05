---
title: Veikala atlasītāja modulis
description: Šajā tēmā tiek stāstīts par veikala atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378212"
---
# <a name="store-selector-module"></a>Veikala atlasītāja modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par veikala atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Veikala atlasītāja modulis tiek izmantots klienta scenārijā "pērk tiešsaistē, saņem veikalā" (BOPIS). Tiek rādīts saraksts ar tiem veikaliem, kuros prece ir pieejama saņemšanai, kā arī veikala darba laiki un preču krājumi katram veikalam.

Veikala atlasītāja modulim ir nepieciešams preces konteksts un meklēšanas vieta veikalu atrašanai. Ja nav meklēšanas vietas, tā pēc noklusējuma ir klienta pārlūka vieta, ja klients tam ir devis piekrišanu. Modulī ir ievades lodziņš, kas ļauj klientam ievadīt vietu (pasta indeksu vai pilsētu un rajonu), lai atrastu tuvumā esošos veikalus.

Veikalu atlasīšanas modulis ir integrēts ar Bing karšu ģeokodēšanas lietojumprogrammas programmēšanas interfeisu (API), lai atrašanās vietu pārveidotu platumā un garumā. Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno lapā Commerce kopīgie parametri pakalpojumā Dynamics 365 Commerce.

Veikala atlasītāja moduli var pievienot pirkšanas kastes modulim preces informācijas lapā (PDP), lai parādītu veikalus, kuros prece ir pieejama saņemšanai. To var pievienot arī groza modulim. Veikala atlasītāja modulis pēc pievienošanas groza modulim rāda opcijas katras groza rindas elementam. Turklāt, izmantojot pielāgotu kodēšanu, šo moduli var pievienot citām lapām vai moduļiem, izmantojot paplašinājumus un pielāgojumus.

Lai BOPIS scenārijs darbotos, precēm jābūt konfigurētām ar piegādes režīmu "saņem debitors". Pretējā gadījumā modulis netiks uzrādīts attiecīgajās lapās. Plašāku informāciju par piegādes režīma konfigurēšanu skatiet rakstā [Piegādes veidu iestatīšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Šajā attēlā redzams veikala atlasītāja moduļa piemērs, kas izmantots PDP.

![Veikala atlasītāja moduļa piemērs](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Veikala atlasītāja moduļa izmantošana e-komercijā

- Veikala atlasītāja moduli var izmantot preces informācijas lapā (PDP), lai atrastu tuvumā esošus veikalus, kuros prece ir pieejama saņemšanai.
- Veikala atlasītāja moduli var izmantot groza lapā (PDP), lai atrastu tuvumā esošus veikalus, kuros grozs ir pieejama saņemšanai.

## <a name="store-selector-module-properties"></a>Veikala atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | apraksts |
|---------------------------|-----------------------|-------------|
| Meklēšanas rādiuss | Skaits | Nosaka veikalu meklēšanas rādiusu jūdzēs. Ja nav norādīta vērtība, tiek izmantots noklusētais meklēšanas rādiuss, kas ir 50 jūdzes.|
|Pakalpojuma noteikumi | Vietrādis URL    |  Bing karšu pakalpojumam nepieciešamā vietrāža URL pakalpojuma nosacījumi. |

## <a name="add-a-store-selector-module-to-a-page"></a>Veikala atlasītāja moduļa pievienošana lapai

Veikala atlasītāja modulim ir nepieciešams preces konteksts, tāpēc to var izmantot tikai pirkšanas kastes un groza moduļos. Veikala atlasītāja moduļi nedarbojas ārpus šiem moduļiem.

- Lai iegūtu informāciju par to, kā pievienot veikala atlasītāja moduli pirkšanas kastes modulim skatiet rakstu [Pirkšanas kastes modulis](add-buy-box.md). 
- Lai iegūtu informāciju par to, kā pievienot veikala atlasītāja moduli groza modulim skatiet rakstu [Groza modulis](add-cart-module.md)

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Īss PDP apskats](quick-tour-pdp.md)

[Īss groza un norēķināšanās apskats](quick-tour-cart-checkout.md)

[Iestatiet piegādes veidus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Bing karšu pārvaldība jūsu organizācijā](dev-itpro/manage-bing-maps.md)
