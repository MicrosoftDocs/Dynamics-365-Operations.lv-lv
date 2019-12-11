---
title: Centrālais modulis
description: Šī tēma ietver centrālos moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785398"
---
# <a name="hero-module"></a>Centrālais modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šī tēma ietver centrālos moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Centrālais modulis tiek izmantots, lai reklamētu preces vai veicināšanas pasākumus, izmantojot attēlu un teksta kombināciju. Piemēram, mazumtirgotājs var pievienot centrālo moduli E-komercijas sākumlapai, lai reklamētu jaunu preci un piesaistītu klientu uzmanību.

Centrālo moduli vada dati no satura pārvaldība sistēmas (CMS). Tas ir savrups modulis, kas nav atkarīgs no citiem moduļiem lapā. Centrālo moduli var ievietot jebkurā vietnes lapā, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, pārdošanu vai līdzekļus).

## <a name="examples-of-hero-module-in-e-commerce"></a>Centrālo moduļu piemēri E-komercijā

- Centrālo moduli var izmantot E-komercijas vietnes sākumlapā, lai izceltu veicināšanas pasākumus un jaunās preces.
- Centrālais modulis var tikt izmantots preces informācijas lapā, lai parādītu informāciju par preci.
- Vairākus centrālos moduļus var ievietot karuseļa modulī, lai izceltu vairākas preces vai veicināšanas pasākumus.

## <a name="hero-module-properties"></a>Centrālā moduļa rekvizīti

| Rekvizīta nosaukums  | Vērtības | Apraksts |
|----------------|--------|-------------|
| Attēls          | Attēla fails | Attēlu var izmantot, lai rādītu preci vai veicināšanas pasākumu. Attēlu var augšupielādēt attēlu galerijā vai arī var izmantot esošu attēlu. |
| Virsraksts        | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Katram centrālajam modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa      | Rindkopas teksts | Centrālie moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt           | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** | Centrālie moduļi atbalsta vienu vai vairākas saites “aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |
| Teksta izvietojums | **Augšpusē pa kreisi**, **Augšpusē pa labi**, **Augšpusē centrā**, **Apakšpusē pa kreisi**, **Apakšpusē pa labi**, **Apakšpusē centrā**, **Centrā pa kreisi**, **Centrā pa labi** vai **Centrā** | Šis rekvizīts nosaka attēla novietojumu attiecībā pret tekstu. Piemēram, atlasot **Pa labi**, attēls tiek parādīts pa labi no teksta. |
| Teksta motīvs     | **Gaišs** vai **Tumšs** | Teksta krāsu shēmu var definēt, pamatojoties uz fona attēlu. Piemēram, ja attēlam ir tumšs fons, var lietot gaismas dizainu, lai tekstu padarītu redzamāku un panāktu atbilstību krāsu kontrasta koeficientu pieejamībai. |
| Gradients       | **Patiess** vai **Nepatiess** | Gradientu var lietot attēlam, lai nodrošinātu krāsu kontrasta attiecības pieejamības nolūkiem. |

## <a name="add-a-hero-module-to-a-new-page"></a>Centrālā moduļa pievienošana jaunā lapā

Lai pievienotu centrālo moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un izveidojiet lapas veidni ar nosaukumu **centrālā veidne**.
1. Noklusētās lapas **Galvenajā** slotā pievienojiet centrālo moduli.
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto centrālo veidni, lai izveidotu lapu ar nosaukumu **centrālā lapa**.
1. Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** zem **Atlasīt moduļus** izvēlieties centrālio moduli un pēc tam atlasiet **Labi**.
1. Strukturējuma kokā pa kreisi atlasiet centrālo moduli.
1. Rekvizītu rūts labajā pusē atlasiet **Pievienot attēlu**. Pēc tam vai nu atlasiet esošu attēlu, vai augšupielādējiet jaunu attēlu.
1. Atlasiet **Virsraksts**.
1. Dialoglodziņā **Virsraksts** pievienojiet virsraksta tekstu, atlasiet virsraksta līmeni un pēc tam atlasiet **Labi**.
1. Sadaļā **Bagātināts teksts** pievienojiet vēlamo tekstu.
1. Atlasiet **Pievienot darbības saiti**.
1. Dialoglodziņā **Darbības saite** pievienojiet saites tekstu, saites vietrādi URL un ARIA etiķeti saitei un pēc tam atlasiet **Labi**.
1. Lapas saglabāšana un savu izmaiņu priekšskatīšana
1. Pārbaudiet lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Brīdinājuma modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Līdzekļa modulis](add-feature-module.md)

[Video atskaņotāja modulis](add-video-player.md)
