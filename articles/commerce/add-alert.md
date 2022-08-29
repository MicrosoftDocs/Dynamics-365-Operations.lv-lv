---
title: Akcijas reklāmkaroga modulis
description: Šajā rakstā ir apskatīti moduļu to moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fbde146923d1448e382cbf2458880f7e300f605c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279740"
---
# <a name="promo-banner-module"></a>Akcijas reklāmkaroga modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti moduļu to moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Veicināšanas reklāmlogu moduļi tiek izmantoti, lai lapā rādītu iekļautos informatīvos ziņojumus. Tos var izmantot, lai visā vietnē rādītu veicināšanas pasākumus, kas tiek rādīti visās e-komercijas vietnes lapās. 

Veicināšanas reklāmlogu moduļi atbalsta teksta ziņojumu un saiti. Ja vairāki ziņojumi ir pievienoti veicināšanas reklāmlogu modulim, tas kļūst par rotējošu karuseļa reklāmkarogu, kas ļaus klientiem pārlūkot visus ziņojumus. 

Veicināšanas reklāmlogu moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Lietojuma piemēri veicināšanas reklāmlogiem e-Commerce sistēmā

Veicināšanas reklāmlogus var izmantot vietnes galvenē, lai parādītu veicināšanas pasākumus vai ziņojumus visā vietnē, kā tas ir tālāk esošajos piemēros.

“Ikgadējā pārdošana beidzas pēc 10 dienām”

“Labi ietaupiet ar skolas sākuma izpārdošanu. Iepērcieties tūlīt.”

"Veikals Pateicības dienas IZPĀRDOŠANAi!" 

Attēlā zemāk ir parādīts veicināšanas reklāmkaroga piemērs.

![Veicināšanas reklāmkaroga moduļa piemērs.](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Veicināšanas reklāmkarogu moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                              | Apraksts |
|---------------------------|------------------------------------|-------------|
| Reklāmkaroga ziņojumi           | Teksts un saites                     | Teksta un saišu masīvs. |
| Automātiskā atskaņošana                  | **Patiess** vai **Nepatiess**              | Vērtība, kas norāda, vai ziņojumi tiek automātiski iestatīti, ja ir konfigurēti vairāki ziņojumi. |
| Slaidu pārejas intervāls | Milisekunžu skaits (ms)      | Intervāls, ko izmanto, lai pārlūkotu ziņojumus. |
| Atļaut noraidīšanu             | **Patiess** vai **Nepatiess**              | Ja vērtība ir iestatīta uz **Patiess**, debitori var noraidīt brīdinājumu. |
| Rādīt karuseļveida ziņojumu     | **Patiess** vai **Nepatiess**              | Vērtība, kas norāda, vai karuseļa paziņojumi ir jārāda, lai klienti varētu manuāli pārvietoties pa vairākiem reklāmkaroga vienumiem. |
| Teksta līdzinājums            | **Pa labi**, **Pa kreisi** vai **Centrā** | Teksta līdzinājums veicināšanas reklāmkaroga modulī. |
| Saistīt                      | URL                              | Vietrādis URL neobligātai vietnei. |
|Teksta līdzinājums             | **Pa labi**, **Pa kreisi** vai **Centrā** | Šis rekvizīts ir pieejams kā tēmas paplašinājums Adventure Works tēmā. Tas ļauj lietotājam iestatīt teksta līdzinājumu veicināšanas reklāmlogos. |

> [!IMPORTANT]
> Adventure Works tēma ir pieejama Dynamics 365 Commerce versijas 10.0.20 laidienā.

## <a name="add-a-promo-banner-module-to-a-page"></a>Veicināšanas reklāmloga moduļa pievienošana jaunā lapā 

Lai pievienotu veicināšanas reklāmloga moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņa Jauna **veidne sadaļā** Veidnes nosaukums **ievadiet** **Att. att. atl**. un tad atlasiet **Labi**.
1. Sadaļā **Lapas struktūra** pievienojiet moduli **Noklusējuma lapa** slotam **Pamatteksts**. 
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to. 
1. Izmantojiet jūsu tikko izveidoto brīdinājuma veidni, lai izveidotu lapu ar nosaukumu **Veicināšanas reklāmloga lapa**. 
1. Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli. 
1. Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt konteineru**.
1. Sadaļā **Lapas struktūra** pievienojiet veicināšanas reklāmkaroga moduli konteinera modulim.
1. Reklāmkaroga moduļa iestatījumos pievienojiet vienu vai vairākus reklāmkarogu ziņojumus. Katrai ziņai var būt teksts kopā ar saiti. Varat rediģēt pārējos rekvizītus, lai tālāk pielāgotu moduli.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapas augšdaļā ieraudzīsiet brīdinājumu ar jūsu pievienoto tekstu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

> [!NOTE]
> Veicināšanas reklāmlogs parasti tiek izmantots lapas galvenes slotā vai apakšvadītāja slotā.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Karuseļa modulis](add-carousel.md)

[Teksta bloka modulis](add-content-rich-block.md)

[Satura bloka modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
