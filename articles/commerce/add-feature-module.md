---
title: Līdzekļa modulis
description: Šajā tēmā tiek stāstīts par līdzekļu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785289"
---
# <a name="feature-module"></a>Līdzekļa modulis 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par līdzekļu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Līdzekļa modulis tiek izmantots, lai reklamētu preces vai veicināšanas pasākumus, izmantojot attēlu un teksta kombināciju. Piemēram, mazumtirgotājs var pievienot līdzekļa moduli preces informācijas lapai, lai izceltu preces līdzekļus.

Līdzekļa moduli vada dati no satura pārvaldība sistēmas (CMS). Tas ir savrups modulis, kas nav atkarīgs no citiem moduļiem lapā. Līdzekļa moduli var ievietot jebkurā vietnes lapā, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, pārdošanu vai līdzekļus).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Līdzekļu moduļu piemēri E-komercijā

Līdzekļa moduli var izmantot šādās lapās.

- Preces informācijas lapa preces līdzekļu rādīšanai
- Sākumlapa preču reklamēšanai
- Kategorijas lapa preču kategorijas izcelšanai

## <a name="feature-module-properties"></a>Līdzekļa moduļa rekvizīti

| Rekvizīta nosaukums     | Vērtības | Apraksts |
|-------------------|--------|-------------|
| Attēls             | Attēla fails | Attēlu var izmantot, lai reklamētu preci vai veicināšanas pasākumu. Attēlu var augšupielādēt attēlu galerijā vai arī var izmantot esošu attēlu. |
| Virsraksts           | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Katram līdzekļu modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa         | Rindkopas teksts | Līdzekļu moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt              | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** | Līdzekļu moduļi atbalsta vienu vai vairākas saites “Aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |
| Attēla izvietojums   | **Pa labai**, **Pa kreisi**, **Augšā** vai **Apakšā** | Šis rekvizīts nosaka attēla novietojumu attiecībā pret tekstu. Piemēram, atlasot **Pa labi**, attēls tiek parādīts pa labi no teksta. |
| Attēlu kolonnas lielums | Skaitlis no **1** līdz **12** | Šis rekvizīts nosaka attēla izmēru attiecībā pret tekstu. Izmērs ir izteikts kā kolonnu skaits lapā. Lapā ir 12 kolonnas. Pēc noklusējuma attēlam un tekstam ir vienāds izmērs (sešas kolonnas katrai). Tomēr izmērus var pielāgot pēc nepieciešamības. |

## <a name="add-a-feature-module-to-a-new-page"></a>Līdzekļa moduļa pievienošana jaunā lapā 

Lai pievienotu līdzekļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes**un izveidojiet lapas veidni ar nosaukumu **līdzekļa veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet līdzekļa moduli.
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto līdzekļa veidni, lai izveidotu lapu ar nosaukumu **līdzekļa lapa**.
1. Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** zem **Atlasīt moduļus** atlasiet līdzekļa moduli un pēc tam atlasiet **Labi**.
1. Strukturējuma kokā pa kreisi atlasiet līdzekļa moduli.
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

[Centrālais modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)
