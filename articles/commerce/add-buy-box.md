---
title: Iegādes lodziņa modulis
description: Šajā tēmā aplūkoti Buy box moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ac29180dbffac4d7db27856b801647aac878bc99
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638029"
---
# <a name="buy-box-module"></a>Pirkšanas lodziņa modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti Buy box moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Termins *iegādes lodziņš* tipiski tiek attiecināts uz preces informācijas lapas (product details page - PDP)apgabalu, kas ir “virs ieloces” un kurā ir ietverta visa svarīgākā informācija, kas nepieciešama preces pirkuma veikšanai. (Apgabals, kas ir “virs ieloces”, ir redzams, kad lapa tiek ielādēta pirmo reizi, lai lietotājiem skatīšanai nebūtu jāritina uz leju.)

Iegādes lodziņa modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas parādīti preces informācijas lapas iegādes lodziņā.

Preces informācijas lapas vietrādī URL ir ietverta preces ID. Visa informācija, kas nepieciešama iegādes lodziņa moduļa atveidošanai, tiek atvasināta no šīs preces ID. Ja preces ID nav norādīts, iegādes lodziņa modulis netiks pareizi atveidots lapā. Tāpēc iegādes loga moduli var izmantot tikai lapās, kurās ir preces konteksts. Lai to izmantotu lapā, kurā nav preces konteksta (piemēram, mājaslapa vai mārketinga lapa), jāveic papildu pielāgojumi.

Attēlā zemāk redzams iegādes lodziņa moduļa piemērs preces informācijas lapā.

![Iegādes lodziņa moduļa piemērs.](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Iegādes lodziņa moduļa rekvizīti un sloti 

Preces informācijas lapā iegādes lodziņš ir sadalīts divos reģionos: multivides reģions kreisajā pusē un satura reģions labajā pusē. Pēc noklusējuma multivides reģiona kolonnas platuma proporcija uz satura apgabala kolonnas platumu ir 2:1. Mobilajās ierīcēs abi reģioni ir grupēti. Tādējādi viens reģions tiek parādīts zem cita reģiona. Tēmas var izmantot, lai pielāgotu kolonnu platumus un salikšanas rangu.

Iegādes loga modulis atveido preces nosaukumu, aprakstu, cenu un vērtējumus. Tas arī ļauj klientiem izvēlēties preces variantus, kuriem ir dažādas preces īpašības, piemēram, lielums, stils un krāsa. Ja ir atlasīts preces variants, tad tiek atjaunināti citi rekvizīti iegādes lodziņā (piemēram, produkta apraksts un attēli), lai atspoguļotu informāciju par variantu. 

Tiek nodrošināts daudzuma atlasītājs, lai klienti varētu norādīt pērkamo vienumu daudzumu. Maksimālo daudzumu, ko var iegādāties, var definēt vietnes iestatījumos.

No iegādes loga klienti var veikt arī darbības, piemēram, pievienot preci grozam, pievienot produktu vēlmju sarakstam un izvēlēties saņemšanas vietu. Šīs darbības var veikt ar preci vai preces variantu. Lai preci pievienotu vēlmju sarakstam, klientam jābūt reģistrētam sistēmā.

Tēmas var izmantot, lai noņemtu vai mainītu iegādes loga produktu rekvizītu un darbības kontroļu kārtību. 

## <a name="module-properties"></a>Moduļa rekvizīti

- **Galvenes etiķete** — šis rekvizīts definē galvenes etiķeti preces nosaukumam. Ja iegādes logs atrodas lapas augšā, šis rekvizīts ir jāiestata uz **h1**, lai atbilstu pieejamības standartiem. 

- **Iespējot ieteikumus "pirkt līdzīgu preci"** - Šis rekvizīts ļauj pirkšanas lodziņā parādīt saites uz precēm, kas izskatās līdzīgi pašlaik skatītajam vienumam. Šis līdzeklis ir pieejams Komercijas izlaidumā 10.0.13 un jaunākās versijās.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduļi, ko var izmantot iegādes lodziņa modulī

- **Multivides galerija** — šis modulis tiek izmantots, lai parādītu preču attēlus preču informācijas lapā. Plašāku informāciju par šo moduli skatiet [Multivides galerijas modulis](media-gallery-module.md).
- **Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus. Plašāku informāciju par šo moduli skatiet [Veikalu atlasītāja modulis](store-selector.md).
- **Sociālā koplietošana** — Šo moduli var pievienot pirkšanas lodziņam, lai ļautu lietotājiem dalīties ar informāciju par produktu sociālajos medijos. Plašāku informāciju skatiet [Sociālās koplietošanas modulis](social-share-module.md).

## <a name="buy-box-module-settings"></a>Iegādes lodziņa moduļa iestatījumi

Iegādes lodziņa moduļa iestatījumus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.

- **Groza rindu daudzuma ierobežojums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).
- **Pievienot preci grozam** — informācija par to, kā pielietot iestatījumus **Pievienot preci grozam**, skatiet [Iestatījumi Pievienot preci grozam](add-cart-settings.md).

## <a name="buy-box-module-definition-extensions-in-the-adventure-works-theme"></a>Iegādes lodziņa moduļa definīcijas paplašinājumi Adventure Works tēmā

Iegādes lodziņa modulim, kuru sniedz Adventure Works tēma, ir moduļa definīcijas paplašinājums, kas atbalsta produkta specifikāciju moduļa ieviešanu pie PDP iegādes lodziņā. Lai parādītu preces specifikācijas īpašības PDP iegādes lodziņā, pievienojiet preces specifikācijas moduli iegādes lodziņa slotam.


> [!IMPORTANT]
> Adventure Works tēma ir pieejama Dynamics 365 Commerce versijas 10.0.20 laidienā.


## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Iegādes lodziņa modulis izgūst preču informāciju, izmantojot Commerce Scale Unit pieteikuma programmēšanas interfeisus (API). Preces ID no preces informācijas lapas tiek izmantots visas informācijas izgūšanai.

## <a name="add-a-buy-box-module-to-a-page"></a>Iegādes lodziņa moduļa pievienošana lapā

Lai pievienotu iegādes lodziņa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jauns fragments** atlasiet moduli **Iegādes lodziņš**.
1. Sadaļā **Fragmenta nosaukums** ievadiet nosaukumu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.
1. Iegādes lodziņa moduļa slotā **Mediju galerija** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Mediju galerija** un pēc tam atlasiet **Labi**.
1. Iegādes lodziņa moduļa slotā **Veikalu atlasītājs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **PDP veidne** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņā **Atlasīt fragmentu** atlasiet iepriekš izveidoto fragmentu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **PDP veidne**. Sadaļā **Lapas nosaukums** ievadiet **PDP lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas **Galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņā **Atlasīt fragmentu** atlasiet iepriekš izveidoto fragmentu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.
1. Saglabājiet un priekšskatiet lapu. Pievienojiet **?productid=&lt;product id&gt;** vaicājuma virknes parametru priekšskatījuma lapas vietrādim URL. Šādā veidā preces konteksts tiek izmantots priekšskatījuma lapas ielādei un atveidošanai.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to. Preču informācijas lapā ir jābūt redzamam iegādes lodziņam.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Veikalu atlasītāja modulis](store-selector.md)

[Multivides galerijas modulis](media-gallery-module.md)

[Konteinera modulis](add-container-module.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)

[Sociālo tīklu dalīšanās modulis](social-share-module.md)

[Iestātījumi Pievienot preci grozam](add-cart-settings.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)

[SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
