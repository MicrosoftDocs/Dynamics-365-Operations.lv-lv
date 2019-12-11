---
title: Container modulis
description: Šajā tēmā tiek stāstīts par konteinera moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697064"
---
# <a name="container-module"></a>Container modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par konteinera moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Konteinera modulis ir modulis, kas vieso citus moduļus. Tas ir vispārīgākais konteiners, kas tiek izmantots programmā Dynamics 365 Commerce. Konteinera moduļa galvenais nolūks ir definēt, izmantojot tam iestatītos rekvizītus, iekšā esošo moduļu izkārtojumu. Piemēram, šie moduļi var parādīties blakus divu kolonnu, trīs kolonnu, četru kolonnu vai sešu kolonnu izkārtojumā. Tie var būt ierobežoti ar konteinera platumu vai arī var aizpildīt ekrānu. Virsrakstu var pievienot arī katram konteinera modulim.

Ir trīs standarta konteineru moduļu tipi: konteiners, konteiners ar 2 slotiem un konteiners ar 3 slotiem. Šajos konteineros var ievietot jebkura tipa moduļus. Ir arī īpaši konteineru moduļu tipi, piemēram, karuselis, satura bagātinātais bloks, satura izvietošana, grozs, norēķināšanās, iegādes lodziņš, galvene un kājene. Šiem konteineriem ir īpaši mērķi, un tajos var ievietot tikai specifiskus atbalstītus moduļu tipus.

Iesakām ievietot moduļus konteinerā, lai tos varētu ierobežot ar konteinera platumu.

## <a name="examples-of-container-modules-in-e-commerce"></a>Konteinera moduļu piemēri E-komercijā

- Vietnes autors vēlas trīs kolonnu izkārtojumu, kurā līdzās ir redzami trīs moduļi. Tādēļ vietnes autors izmanto konteinera moduli — konteineru ar 3 slotu tipu.
- Vietnes autors vēlas sešu kolonnu izkārtojumu, kurā līdzās ir redzami seši moduļi. Tādēļ vietnes autors izmanto konteineru ar konteinera tipu, kurā ir sešas kolonnas.
- Vietnes autors vēlas ievietot moduli lapā, bet nevēlas, lai tas aizpildītu ekrānu. Tādēļ vietnes autors pievieno moduli konteinera modulim un iestata konteinera rekvizītu **Platums**, lai **Ietilpināt konteinerā**.

## <a name="container-module-properties"></a>Konteinera moduļa pievienošana

| Rekvizīta nosaukums     | Vērtības | Apraksts |
|-------------------|--------|-------------|
| Virsraksts           | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pēc izvēles konteineram var nodrošināt virsrakstu. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Platums             | **Ietilpināt konteinerā** vai **Pilnekrāna režīms** | Ja vērtība ir iestatīta uz **Ietilpināt konteinerā** (noklusējuma vērtība), elementi konteinerā ir ierobežoti ar konteinera platumu. Ja vērtība ir iestatīta uz **Aizpildīt ekrānu**, moduļi neaprobežojas ar konteinera platumu, bet var pāriet pilnekrāna režīmā. |
| Kolonnu skaits | **1**, **2**, **3**, **4**, **6** vai **12** | Šis rekvizīts nosaka kolonnu skaitu konteinerā. Konteinerā var būt līdz 12 kolonnām. |

## <a name="container-with-2-slots"></a>Konteiners ar 2 slotiem

Konteiners ar 2 slotu tipu ir optimizēts divu kolonnu izkārtojumam. Šim konteinera tipam ir divi sloti, lai varētu skatīt blakus izvietotos iekšā esošos moduļus.

Papildu rekvizītus var izmantot, lai optimizētu izkārtojumu dažādiem skatu portiem (mobilajām ierīcēm, planšetdatoriem, datoriem utt.). Katram skatījuma portam var definēt katras kolonnas platumu. Pieejami tālāk norādītie kolonnas platuma iestatījumi.

- **75%/25%** — pirmā moduļa platums ir 75 procenti, un otrā moduļa kolonnas platums ir 25 procenti. Ir pieejama arī opcija **25%/75%**.
- **50%/50%** — abiem moduļiem ir vienāds kolonnu platums.
- **67%/33%** — pirmā moduļa platums ir 67 procenti, un otrā moduļa kolonnas platums ir 33 procenti. Ir pieejama arī opcija **33%/67%**.
- **100%** — abiem moduļiem ir pilnu kolonnu platums. Tāpēc moduļi tiek grupēti vertikāli vienā kolonnā. Lai gan šis vienas kolonnas izkārtojums ir vērsts pret konteinera nolūku ar 2 slotu tipu, tas var būt vēlams dažiem skatījuma portiem (piemēram, īpaši maza izmēra skata portiem, piemēram, mobilajām ierīcēm).

### <a name="container-with-2-slots-properties"></a>Konteiners ar 2 slotu rekvizītiem

| Rekvizīta nosaukums                   | Vērtības | Apraksts |
|---------------------------------|--------|-------------|
| Virsraksts                         | Virsraksta teksts un virsraksta etiķete | Pēc izvēles konteineram var nodrošināt. |
| X-maza skata porta konfigurācija | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** vai **100%** | Šis rekvizīts nosaka izkārtojumu īpaši maza izmēra skata portiem. |
| Maza izmēra skata porta konfigurācija   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** vai **100%** | Šis rekvizīts nosaka izkārtojumu maza izmēra skata portiem, piemēram, mobilajām ierīcēm. |
| Vidēja izmēra skata porta konfigurācija  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** vai **100%** | Šis rekvizīts nosaka izkārtojumu vidēja izmēra skata portiem, piemēram, planšetdatoriem. |
| Liela izmēra skata porta konfigurācija   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** vai **100%** | Šis rekvizīts nosaka izkārtojumu liela skata portiem, piemēram, datoriem. |

## <a name="container-with-3-slots"></a>Konteiners ar 3 slotiem

Konteiners ar 3 slotu moduļa tipu ir optimizēts trīs kolonnu izkārtojumam.

Papildu rekvizītus var izmantot, lai optimizētu izkārtojumu dažādiem skatu portiem. Katram skatījuma portam var definēt katras kolonnas platumu. Pieejami tālāk norādītie kolonnas platuma iestatījumi.

- **33%/33%/33%** – visiem trim moduļiem ir vienāds kolonnu platums.
- **50%/25%/25%** — pirmā moduļa platums ir 50 procenti, un katram no atlikušajiem diviem moduļiem kolonnas platums ir 25 procenti. Opcijas **25%/50%/25%** un **25%/25%/50%** arī ir pieejamas.
- **16%/16%/67%** — katram no pirmajiem diviem moduļiem kolonnu platums ir 16 procenti, un trešā moduļa kolonnas platums ir 67 procenti. Opcijas **16%/67%/16%** un **67%/16%/16%** arī ir pieejamas.

### <a name="container-with-3-slots-properties"></a>Konteiners ar 3 slotu rekvizītiem

| Rekvizīta nosaukums                   | Vērtības | Apraksts |
|---------------------------------|--------|-------------|
| Virsraksts                         | Virsraksta teksts un virsraksta etiķete | Pēc izvēles konteineram var pievienot virsrakstu. |
| X-maza skata porta konfigurācija | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** vai **67%/16%/16%** | Šis rekvizīts nosaka izkārtojumu īpaši maza izmēra skata portiem. |
| Maza izmēra skata porta konfigurācija   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** vai **67%/16%/16%** | Šis rekvizīts nosaka izkārtojumu maza izmēra skata portiem, piemēram, mobilajām ierīcēm. |
| Vidēja izmēra skata porta konfigurācija  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** vai **67%/16%/16%** | Šis rekvizīts nosaka izkārtojumu vidēja izmēra skata portiem, piemēram, planšetdatoriem. |
| Liela izmēra skata porta konfigurācija   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** vai **67%/16%/16%** | Šis rekvizīts nosaka izkārtojumu liela skata portiem, piemēram, datoriem. |

## <a name="add-a-container-module-to-a-page"></a>Konteinera moduļa pievienošana lapā

Lai pievienotu konteinera atskaņotāja moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **konteinera veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet konteinera moduli.
1. Pievienojiet līdzekļa moduli konteinera modulim.
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto konteinera veidni, lai izveidotu lapu ar nosaukumu **konteinera lapa**.
1. Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.
1. Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Kolonnu skaits** uz **1** un rekvizītu **Platums** uz **Ietilpināt konteinerā**.
1. Pievienojiet līdzekļa moduli konteinera modulim.
1. Līdzekļa moduļa rekvizītu rūtī konfigurējiet virsrakstu.
1. Saglabājiet un priekšskatiet lapu. Ir jābūt redzamam viena līdzekļa modulim, kas ietilpst konteinera moduļa platumā.
1. Konteinera moduļa rekvizītu rūtī mainiet rekvizīta **Kolonnu skaits** vērtību uz **3**.
1. Pievienojiet vēl divus līdzekļa moduļus konteinera modulim.
1. Saglabājiet un priekšskatiet lapu. Tagad jābūt redzamiem trīs funkciju moduļiem, kas parādās līdzās.
1. Pēc tam, kad esat sasnieguši vēlamo izkārtojumu, pārbaudiet lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Karuseļa modulis](add-carousel.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
