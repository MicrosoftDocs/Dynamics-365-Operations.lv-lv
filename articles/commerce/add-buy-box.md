---
title: Iegādes lodziņa modulis
description: Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686674"
---
# <a name="buy-box-module"></a>Iegādes lodziņa modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Termins *iegādes lodziņš* tipiski tiek attiecināts uz preces informācijas lapas apgabalu, kas ir “virs ieloces” un kurā ir ietverta visa svarīgākā informācija, kas nepieciešama preces pirkuma veikšanai. (Apgabals, kas ir “virs ieloces”, ir redzams, kad lapa tiek ielādēta pirmo reizi, lai lietotājiem skatīšanai nebūtu jāritina uz leju.)

Iegādes lodziņa modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas parādīti preces informācijas lapas iegādes lodziņā.

Preces informācijas lapas vietrādī URL ir ietverta preces ID. Visa informācija, kas nepieciešama iegādes lodziņa moduļa atveidošanai, tiek atvasināta no šīs preces ID. Ja preces ID nav norādīts, iegādes lodziņa modulis netiks pareizi atveidots lapā. Tāpēc iegādes loga moduli var izmantot tikai lapās, kurās ir preces konteksts. Lai to izmantotu lapā, kurā nav preces konteksta (piemēram, mājaslapa vai mārketinga lapa), jāveic papildu pielāgojumi.

Attēlā zemāk redzams iegādes lodziņa moduļa piemērs preces informācijas lapā.

![Iegādes lodziņa moduļa piemērs](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Iegādes lodziņa moduļa rekvizīti un sloti 

Preces informācijas lapā iegādes lodziņš ir sadalīts divos reģionos: multivides reģions kreisajā pusē un satura reģions labajā pusē. Pēc noklusējuma multivides reģiona kolonnas platuma proporcija uz satura apgabala kolonnas platumu ir 2:1. Mobilajās ierīcēs abi reģioni ir grupēti. Tādējādi viens reģions tiek parādīts zem cita reģiona. Tēmas var izmantot, lai pielāgotu kolonnu platumus un salikšanas rangu.

Iegādes loga modulis atveido preces nosaukumu, aprakstu, cenu un vērtējumus. Tas arī ļauj klientiem izvēlēties preces variantus, kuriem ir dažādas preces īpašības, piemēram, lielums, stils un krāsa. Ja ir atlasīts preces variants, tad tiek atjaunināti citi rekvizīti iegādes lodziņā (piemēram, produkta apraksts un attēli), lai atspoguļotu informāciju par variantu. 

Tiek nodrošināts daudzuma atlasītājs, lai klienti varētu norādīt pērkamo vienumu daudzumu. Maksimālo daudzumu, ko var iegādāties, var definēt vietnes iestatījumos.

No iegādes loga klienti var veikt arī darbības, piemēram, pievienot preci grozam, pievienot produktu vēlmju sarakstam un izvēlēties saņemšanas vietu. Šīs darbības var veikt ar preci vai preces variantu. Lai preci pievienotu vēlmju sarakstam, klientam jābūt reģistrētam sistēmā.

Tēmas var izmantot, lai noņemtu vai mainītu iegādes loga produktu rekvizītu un darbības kontroļu kārtību. 

## <a name="module-properties"></a>Moduļa rekvizīti

- **Galvenes etiķete** — šis rekvizīts definē galvenes etiķeti preces nosaukumam. Ja iegādes logs atrodas lapas augšā, šis rekvizīts ir jāiestata uz **h1**, lai atbilstu pieejamības standartiem. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduļi, ko var izmantot iegādes lodziņa modulī

- **Multivides galerija** — šis modulis tiek izmantots, lai parādītu preču attēlus preču informācijas lapā. Plašāku informāciju par šo moduli skatiet [Multivides galerijas modulis](media-gallery-module.md).
- **Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus. Plašāku informāciju par šo moduli skatiet [Veikalu atlasītāja modulis](store-selector.md).

## <a name="buy-box-module-settings"></a>Iegādes lodziņa moduļa iestatījumi

Iegādes lodziņa moduļa iestatījumus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.

- **Groza rindu daudzuma ierobežojums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).
- **Pievienot grozam** — šis rekvizīts tiek izmantots, lai noteiktu uzvedību pēc krājuma pievienošanas grozam. Iespējamās vērtības ir **Doties uz grozu**, **Nedoties uz grozu** un **Parādīt paziņojumus**. Kad vērtība ir iestatīta uz **Doties uz grozu**, lietotāji pēc krājuma pievienošanas tiek nosūtīti uz groza lapu. Kad vērtība ir iestatīta uz **Nedoties uz grozu**, lietotāji pēc krājuma pievienošanas netiek nosūtīti uz groza lapu. Kad vērtība ir iestatīta **Rādīt paziņojumus**, lietotājiem tiek parādīts apstiprinājuma paziņojums un viņi turpināt pārlūkot preces informācijas lapā. 

    Attēlā zemāk redzams "pievienots grozam" apstiprinājuma paziņojuma piemērs Fabrikam vietnē.

    ![Paziņojuma moduļa piemērs](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Iegādes lodziņa modulis izgūst preču informāciju, izmantojot Commerce Scale Unit pieteikuma programmēšanas interfeisus (API). Preces ID no preces informācijas lapas tiek izmantots visas informācijas izgūšanai.

## <a name="add-a-buy-box-module-to-a-page"></a>Iegādes lodziņa moduļa pievienošana lapā

Lai pievienotu iegādes lodziņa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Iegādes lodziņš**.
1. Sadaļā **Lapas fragmenta nosaukums** ievadiet nosaukumu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.
1. Iegādes lodziņa moduļa slotā **Mediju galerija** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Mediju galerija** un pēc tam atlasiet **Labi**.
1. Iegādes lodziņa moduļa slotā **Veikalu atlasītājs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **PDP veidne** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot lapas fragmentu**.
1. Dialoglodziņā **Atlasīt lapas fragmentu** atlasiet iepriekš izveidoto fragmentu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **PDP veidne**. Sadaļā **Lapas nosaukums** ievadiet **PDP lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas **Galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot lapas fragmentu**.
1. Dialoglodziņā **Atlasīt lapas fragmentu** atlasiet iepriekš izveidoto fragmentu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.
1. Saglabājiet un priekšskatiet lapu. Pievienojiet **?productid=&lt;product id&gt;** vaicājuma virknes parametru priekšskatījuma lapas vietrādim URL. Šādā veidā preces konteksts tiek izmantots priekšskatījuma lapas ielādei un atveidošanai.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to. Preču informācijas lapā ir jābūt redzamam iegādes lodziņam.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Veikalu atlasītāja modulis](store-selector.md)

[Multivides galerijas modulis](media-gallery-module.md)

[Konteinera modulis](add-container-module.md)

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)
