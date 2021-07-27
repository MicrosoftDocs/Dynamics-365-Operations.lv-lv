---
title: Container modulis
description: Šajā tēmā aplūkoti Container moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59887b058346d55341e68d553ec5dfbc6eb365d6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347570"
---
# <a name="container-module"></a>Konteinera modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti Container moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Konteinera modulis ir modulis, kas vieso citus moduļus. Konteinera moduļa galvenais nolūks ir definēt, izmantojot tam iestatītos rekvizītus, iekšā esošo moduļu izkārtojumu. Piemēram, šie moduļi var parādīties blakus divu kolonnu, trīs kolonnu, četru kolonnu vai sešu kolonnu izkārtojumā. Tie var būt ierobežoti ar konteinera platumu vai arī var aizpildīt ekrānu. Virsrakstu var pievienot arī katram konteinera modulim.

Tiek atbalstīti trīs standarta konteineru moduļu tipi: konteiners, konteiners ar 2 slotiem un konteiners ar 3 slotiem. Šajos konteineros var ievietot jebkura tipa moduļus. 

> [!NOTE] 
> Iesakām vienmēr ievietot moduļus konteinera modulī, lai tos varētu ierobežot ar konteinera platumu.

## <a name="examples-of-container-modules-in-e-commerce"></a>Konteinera moduļu piemēri E-komercijā

- Vietnes autors vēlas trīs kolonnu izkārtojumu, kurā līdzās ir redzami trīs moduļi. Tādēļ vietnes autors izmanto konteinera moduli — konteineru ar 3 slotu tipu.
- Vietnes autors vēlas sešu kolonnu izkārtojumu, kurā līdzās ir redzami seši moduļi. Tādēļ vietnes autors izmanto konteineru ar konteinera tipu, kurā ir sešas kolonnas.
- Vietnes autors vēlas ievietot moduli lapā, bet nevēlas, lai tas aizpildītu ekrānu. Tādēļ vietnes autors pievieno moduli konteinera modulim un iestata konteinera rekvizītu **Platums**, lai **Ietilpināt konteinerā**.

Sekojošajā attēlā ir parādīts konteinera moduļa piemērs, kurā atrodas karuseļa modulis Commerce vietņu veidotājā. Šajā piemērā konteinera moduļa rekvizīts **Platums** ir iestatīts uz **Aizpildīt ekrānu**.

![Konteinera moduļa piemērs.](./media/ecommerce-container.PNG)

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

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Konteinera veidne** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to. 
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet video atskaņotāja veidni, kuru izveidojāt. Sadaļā **Lapas nosaukums** ievadiet **Konteinera lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Kolonnu skaits** uz **1** un rekvizītu **Platums** uz **Ietilpināt konteinerā**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Satura bloks** un pēc tam atlasiet **Labi**.
1. Satura bloka moduļa rekvizītu rūtī konfigurējiet virsrakstu, attēlu un izkārtojumu.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Ir jābūt redzamam viena līdzekļa modulim, kas ietilpst konteinera moduļa platumā.
1. Konteinera moduļa rekvizītu rūtī nomainiet rekvizīta vērtību **Kolonnu skaits** uz **3**.
1. Pievienojiet konteineru modulim vēl divus satura bloka moduļus un konfigurējiet tos.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Tagad jābūt redzamiem trīs satura bloka moduļiem, kas parādās līdzās.
1. Kad esat sasnieguši vēlamo izkārtojumu, atlasiet **Pabeigt rediģēšanu**, lai pieteiktos lapā, un pēc tam atlasiet **Publicēt**, lai to publicētu.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Akordeona modulis](add-accordion.md)

[Cilnes modulis](add-tab.md)

[Karuseļa modulis](add-carousel.md)

[Teksta bloka modulis](add-content-rich-block.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]