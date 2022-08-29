---
title: Karuseļa modulis
description: Šis raksts aptver carousel moduļus un apraksta, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 8bf9f7294dfbb4e16814dbdfb27bf646fcb5f4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275832"
---
# <a name="carousel-module"></a>Karuseļa modulis

[!include [banner](includes/banner.md)]

Šis raksts aptver carousel moduļus un apraksta, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.

Karuseļa modulis tiek izmantots, lai izvietotu vairākus veicināšanas elementus (ieskaitot bagātinātus attēlus) rotējošā karuseļa reklāmlogā, ko klienti var pārlūkot. Piemēram, mazumtirgotājs var izmantot karuseļa moduli sākumlapā, lai parādītu vairākas jaunas preces vai veicināšanas pasākumus.

Karuseļa modulī varat pievienot satura bloka moduļus. Karuseļa moduļa rekvizīti nosaka, kā šie moduļi tiek atveidoti.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Karuseļa moduļu piemēri E-komercijā

- Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots sākumlapā.
- Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots preču informācijas lapā.
- Karuseli var izmantot jebkurā mārketinga lapā, lai reklamētu vairākus veicināšanas pasākumus vai preces.

Attēlā zemāk redzams piemērs karuseļa modulim, kas tiek izmantots sākumlapā. Šajā karuseļa modulī ir vairāki satura bloka elementi.

![Karuseļa moduļa piemērs.](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Karuseļa moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | Apraksts |
|---------------------------|-----------------------|-------------|
| Automātiskā atskaņošana                  | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, pāreja starp elementiem karuselī tiek veikta automātiski. Ja vērtība ir iestatīta uz **Nepatiess**, pāreja netiek veikta, ja vien klients neizmanto tastatūru vai peli, lai pārvietotos no viena elementa uz nākamo. |
| Slaidu pārejas intervāls | Vērtība sekundēs    | Intervāls pārejām starp elementiem. |
| Pārejas veids           | **Slīdināt** vai **Izbalēt** | Pārejas efekts starp vienumiem. |
| Paslēpt karuseļa apvēršanas indikatoru     | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, karuseļa ziņojums un secības indikators ir slēpts. |
| Atļaut karuseļa noraidīšanu    | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, lietotāji var noraidīt karuseli. |

## <a name="add-a-carousel-module-to-a-page"></a>Karuseļa moduļa pievienošana lapā

Lai pievienotu karuseļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Karuseļa veidni** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.  
1. Izmantojiet jūsu tikko izveidoto karuseļa veidni lapas ar nosaukumu **Karuseļa lapa** izveidei.
1. Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli. 
1. Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt ekrānu**.
1. Sadaļā **Lapas struktūra** pievienojiet karuseļa moduli konteinera modulim.
1. Pievienojiet satura bloka moduli karuseļa modulim. Iestatiet satura bloka moduļa rekvizītus, sniedzot **Virsraksts**, **Saite**, **Izkārtojums** un citus rekvizītus.
1. Pievienojiet un konfigurējiet citu satura bloka moduli.
1. Iestatiet papildu rekvizītus karuseļa modulim, ja nepieciešams.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapā ir jāparāda karuselis, kurā ir divi moduļi (centrālais modulis un līdzekļa modulis). Lai sasniegtu vēlamo efektu, varat mainīt papildus rekvizītus karuselim, centrālajam un līdzekļa modulim.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Akcijas reklāmkaroga modulis](add-alert.md)

[Teksta bloka modulis](add-content-rich-block.md)

[Satura bloka modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
