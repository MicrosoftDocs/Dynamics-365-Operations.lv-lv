---
title: Iegādes lodziņa modulis
description: Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 35b7027e0f0b680dd82ebfcea754fef1617c0163
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261402"
---
# <a name="buy-box-module"></a>Iegādes lodziņa modulis


[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Termins *iegādes lodziņš* tipiski tiek attiecināts uz preces informācijas lapas apgabalu, kas ir “virs ieloces” un kurā ir ietverta visa svarīgākā informācija, kas nepieciešama preces pirkuma veikšanai. (Apgabals, kas ir “virs ieloces”, ir redzams, kad lapa tiek ielādēta pirmo reizi, lai lietotājiem skatīšanai nebūtu jāritina uz leju.)

Iegādes lodziņa modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas parādīti preces informācijas lapas iegādes lodziņā.

Preces informācijas lapas vietrādī URL ir ietverta preces ID. Visa informācija, kas nepieciešama iegādes lodziņa moduļa atveidošanai, tiek atvasināta no šīs preces ID. Ja preces ID nav norādīts, iegādes lodziņa modulis netiks pareizi atveidots lapā. Tāpēc iegādes loga moduli var izmantot tikai lapās, kurās ir preces konteksts. Lai to izmantotu lapā, kurā nav preces konteksta (piemēram, mājaslapa vai mārketinga lapa), jāveic papildu pielāgojumi.

## <a name="buy-box-module-properties-and-slots"></a>Iegādes lodziņa moduļa rekvizīti un sloti 

Preces informācijas lapā iegādes lodziņš ir sadalīts divos reģionos: multivides reģions kreisajā pusē un satura reģions labajā pusē. Pēc noklusējuma multivides reģiona kolonnas platuma proporcija uz satura apgabala kolonnas platumu ir 2:1. Mobilajās ierīcēs abi reģioni ir grupēti. Tādējādi viens reģions tiek parādīts zem cita reģiona. Tēmas var izmantot, lai pielāgotu kolonnu platumus un salikšanas rangu.

Iegādes loga modulis atveido preces nosaukumu, aprakstu, cenu un vērtējumus. Tas arī ļauj klientiem izvēlēties preces variantus, kuriem ir dažādas preces īpašības, piemēram, lielums, stils un krāsa. Ja ir atlasīts preces variants, tad tiek atjaunināti citi rekvizīti iegādes lodziņā (piemēram, produkta apraksts un attēli), lai atspoguļotu informāciju par variantu. 

Tiek nodrošināts daudzuma atlasītājs, lai klienti varētu norādīt pērkamo vienumu daudzumu. Maksimālo daudzumu, ko var iegādāties, var definēt vietnes iestatījumos.

No iegādes loga klienti var veikt arī darbības, piemēram, pievienot preci grozam, pievienot produktu vēlmju sarakstam un izvēlēties saņemšanas vietu. Šīs darbības var veikt ar preci vai preces variantu. Lai preci pievienotu vēlmju sarakstam, klientam jābūt reģistrētam sistēmā.

Tēmas var izmantot, lai noņemtu vai mainītu iegādes loga produktu rekvizītu un darbības kontroļu kārtību. 

## <a name="module-properties"></a>Moduļa rekvizīti

- **Galvenes etiķete** — šis rekvizīts definē galvenes etiķeti preces nosaukumam. Ja iegādes logs atrodas lapas augšā, šis rekvizīts ir jāiestata uz **h1**, lai atbilstu pieejamības standartiem. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduļi, ko var izmantot iegādes lodziņa modulī

- **Multivides galerija** — šis modulis tiek izmantots, lai parādītu preču attēlus preču informācijas lapā. Tas var atbalstīt no viena līdz vairākiem attēliem. Tā atbalsta arī sīktēlu attēlus. Sīktēlu attēlus var sakārtot vai nu horizontāli (kā rindu zem attēla), vai vertikāli (kā kolonnu blakus attēlam). Multivides galerijas modulis var tikt pievienots **Multivides** slotam iegādes lodziņa modulī. Tas pašlaik atbalsta tikai attēlus. 
- **Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus. Plašāku informāciju par šo moduli skatiet [Veikala atlasītāja modulis](store-selector.md).

## <a name="buy-box-module-settings"></a>Iegādes lodziņa moduļa iestatījumi

Iegādes loga moduļiem ir trīs iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.

- **Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumu pārbaude** — ja vērtība ir iestatīta uz **Patiess**, prece tiek pievienota grozam tikai pēc tam, kad iegādes lodziņa modulis apstiprina, ka šī prece ir krājumos. Šī krājuma pārbaude tiek veikta gadījumā, kad prece tiks nosūtīta, gan gadījumā, kad prece tiks saņemta veikalā. Ja vērtība ir iestatīta uz **Nepatiess**, krājumu pārbaude netiek veikta pirms preces pievienošanas grozam un pasūtījuma veikšanas. Lai iegūtu informāciju par to, kā konfigurēt krājumu iestatījumus aizmugurē, skatiet [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).

- **Krājumu buferis** — šis rekvizīts tiek izmantots, lai norādītu krājuma bufera numuru. Krājumi tiek uzturēti reālajā laikā, un situācijā, kad daudzi klienti veic pasūtījumus, var būt sarežģīti uzturēt precīzu krājumu uzskaiti. Kad ir veikta krājuma pārbaude, ja krājumi ir mazāki par buferā esošo daudzumu, tiek uzskatīts, ka prece vairs nav pieejama. Tāpēc, kad pārdošana notiek ātri, izmantojot vairākus kanālus, un krājumu uzskaite nav pilnībā sinhronizēta, pastāv mazāks risks, ka tiks pārdota prece, kas vairs nav pieejama.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Iegādes loga modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API. Preces ID no preces informācijas lapas tiek izmantots visas informācijas izgūšanai.

## <a name="add-a-buy-box-module-to-a-page"></a>Iegādes lodziņa moduļa pievienošana lapā

Lai pievienotu iegādes lodziņa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet fragmentu ar nosaukumu **iegādes lodziņa fragments** un pievienojiet tam iegādes lodziņa moduli.
1. Iegādes lodziņā moduļa **Multivides** slotā pievienojiet multivides galerijas moduli.
1. Iegādes loga slotā **Veikala atlasītājs** pievienojiet veikala atlasītāja moduli.
1. Pārbaudiet lapu un publicējiet to.
1. Izveidojiet veidni preces informācijas lapai un nosauciet to par **PDP veidni**.
1. Noklusējuma lapas pievienošana
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet iegādes lodziņa fragmentu.
1. Saglabājiet veidni, pabeidziet to rediģēt un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto veidni lapas ar nosaukumu **PDP lapa** izveidei.
1. Jaunās lapas **Galvenajā** slotā pievienojiet iegādes lodziņa fragmentu.
1. Saglabājiet un priekšskatiet lapu. Pievienojiet **?productid=&lt;product id&gt;** vaicājuma virknes parametru priekšskatījuma lapas vietrādim URL. Šādā veidā preces konteksts tiek izmantots priekšskatījuma lapas ielādei un rādīšanai.
1. Saglabājiet lapu, pabeidziet to rediģēt un publicējiet to. Preču informācijas lapā ir jābūt redzamam iegādes lodziņam.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Veikalu atlasītāja modulis](store-selector.md)

[Konteinera modulis](add-container-module.md)

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)
