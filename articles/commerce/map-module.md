---
title: Kartes modulis
description: Šajā tēmā ir apskatīti kartes moduļi un aprakstīts, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 74991a2979540dab344f39976005250637fab29c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252586"
---
# <a name="map-module"></a>Kartes modulis

[!include [banner](includes/banner.md)]


Šajā tēmā ir apskatīti kartes moduļi un aprakstīts, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.

Kartes modulī tiek parādītas veikalu atrašanās vietas interaktīvajā kartē, kas tiek atveidota, izmantojot [Bing kartes V8 tīmekļa kontroli](https://docs.microsoft.com/bingmaps/v8-web-control/). Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno kopīgo parametru lapā pakalpojumā Commerce headquarters. Karšu moduļi sniedz dažādus skatus, piemēram, Ceļa, Gaisa un Ielas skatu, ko lietotāji var atlasīt, lai skatītu kartes atrašanās vietas. Tās pieļauj arī tādas mijiedarbības kā tālummaiņa un lietotāja atrašanās vietas izmantošana.

cKartes modulis darbojas savienojumā ar veikala atlasītāja moduli, lai noteiktu to veikalu ģeogrāfiskās atrašanās vietas, kas ir jāatveido kartē. Veikala atlasītājs un karšu moduļi mijiedarbojas kad lietotājs atlasa veikalu vienā no šiem moduļiem vietnes lapā. Karšu moduļus var pagarināt citiem scenārijiem, kas nav saistīti ar veikala atlasītāja moduļiem. Tomēr moduļa pielāgošana ir obligāta.

> [!NOTE]
> Kartes modulis ir pieejams Dynamics 365 Commerce 10.0.13 laidienā.

Attēlā zemāk redzams piemērs kartes modulim, kas tiek izmantots veikala atrašanās vietas lapā.

![Veikala atlasītāja moduļa piemērs](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | apraksts |
|---------------------------|-----------------------|-------------|
| Virsraksts | Teksts | Moduļa virsraksts. |
| Spraudītes opcijas: noklusējuma ikona | Attēls | Spraudītes simbola attēls, ko izmantot veikaliem, kas tiek parādīti kartē. |
| Spraudītes opcijas: aktīva ikona | Attēls | Spraudītes simbola attēls, ko izmantot veikalam, kas tiek atlasīts kartē. |
| Spraudītes opcijas: noklusējuma ikonas krāsa | Rakstzīmju virkne | Spraudītes simbolu krāsas teksts vai heksadecimālā vērtība kartē. |
| Spraudītes opcijas: aktīvās ikonas krāsa | Rakstzīmju virkne | Atlasītās spraudītes simbolu krāsas teksts vai heksadecimālā vērtība kartē. |
| Rādīt indeksu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, katrs spraudītes simbols, kas norāda veikalu, rādīs indeksu. Šis indekss atbildīs indeksam saraksta skatā, ko rāda veikala atlasītāja modulis. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Pievienot atļautos kartējuma vietrāžus URL uz vietnes satura drošības politikas direktīvām

Lai karšu modulis darbotos ar Bing kartēm, ir jānodrošina, ka ir atļauti šādi kartēšanas vietrāži URL jūsu vietnes satura drošības politikā (CSP). Šis iestatījums tiek veikts Commerce vietnes veidotājā, pievienojot atļautos vietrāžus URL dažādām vietnes CSP direktīvām (piemēram, **img-src**). Papildinformāciju skatiet [Satura drošības politika](manage-csp.md). 

- **connect-src** direktīvai pievienojiet **&#42;.bing.com**.
- **img-src** direktīvai pievienojiet **&#42;.virtualearth.net**.
- **script-src** direktīvai pievienojiet **&#42;.bing.com, &#42;.virtualearth.net**.
- **script style-src** direktīvai pievienojiet **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Mapes moduļa pievienošana lapā

Lai iegūtu detalizētu informāciju par to, kā konfigurēt kartes moduli lapā, skatiet [Veikala atlasītāja modulis](store-selector.md). 
 
## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Veikalu atlasītāja modulis](store-selector.md)

[Bing karšu pārvaldība organizācijā](./dev-itpro/manage-bing-maps.md)

[Bing karšu V8 tīmekļa kontrole](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]