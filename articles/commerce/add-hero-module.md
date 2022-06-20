---
title: Satura bloka modulis
description: Šis raksts aptver satura bloka moduļus un apraksta, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 253600e48bab2ecfb1e744e15d2fe36fa1ec6765
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870614"
---
# <a name="content-block-module"></a>Satura bloka modulis

[!include [banner](includes/banner.md)]

Šis raksts aptver satura bloka moduļus un apraksta, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.

Satura bloka modulis tiek izmantots, lai reklamētu preces vai veicināšanas pasākumus, izmantojot attēlu un teksta kombināciju. Piemēram, mazumtirgotājs var pievienot satura bloka moduli e-Commerce sākumlapai, lai reklamētu jaunu preci un piesaistītu klientu uzmanību.

Satura bloka moduli vada dati no satura pārvaldība sistēmas (CMS). Tas ir savrups modulis, kas nav atkarīgs no citiem moduļiem lapā. Satura bloka moduli var ievietot jebkurā vietnes lapā, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, pārdošanu vai līdzekļus).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Satura bloka moduļa piemēri e-Commerce

- Satura bloka moduli var izmantot e-Commerce vietnes sākumlapā, lai izceltu veicināšanas pasākumus un jaunās preces.
- Satura bloka modulis var tikt izmantots preces informācijas lapā, lai parādītu informāciju par preci.
- Vairākus satura bloka moduļus var ievietot karuseļa modulī, lai izceltu vairākas preces vai veicināšanas pasākumus.

## <a name="content-block-modules-and-themes"></a>Satura bloku moduļi un tēmas

Satura bloku moduļi var atbalstīt dažādus izkārtojumus un stilus, kas balstīti uz tēmu. Piemēram, Fabrikam tēma atbalsta trīs izkārtojuma variācijas satura bloka modulī: varonis, funkcija un mozaīka. Varoņa izkārtojumā tiek rādīts fonā esošs attēls ar teksta pārklājumu. Funkciju izkārtojumā attēls un teksts ir redzams līdzās. Mozaīkas izkārtojums atļauj vairākus satura blokus mozaīkas formātā.

Turklāt dizainā var būt dažādi rekvizīti katram izkārtojumam. Dizaina izstrādātājs var veidot vairāk izkārtojumu ar vairāk stiliem, izmantojot satura bloka moduli.

Tālāk esošajā attēlā redzams satura bloka moduļa piemērs ar varonis izkārtojumu.

![Hero moduļa piemērs.](./media/Hero.PNG)

Tālāk esošajā attēlā redzams satura bloka moduļa piemērs ar funkcijas izkārtojumu.

![Līdzekļu moduļu piemēri.](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Satura bloka moduļa rekvizīti

| Rekvizīta nosaukums  | Vērtības | Apraksts |
|----------------|--------|-------------|
| Attēls          | Attēla fails | Attēlu var izmantot, lai rādītu preci vai veicināšanas pasākumu. Attēlu var augšupielādēt attēlu galerijā vai arī var izmantot esošu attēlu. |
| Virsraksts        | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Katram centrālajam modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa      | Rindkopas teksts | Centrālie moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt           | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** | Centrālie moduļi atbalsta vienu vai vairākas saites “aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Satura bloka moduļa rekvizīti, kas pakļauti Fabrikam motīvam 

| Rekvizīta nosaukums  | Vērtības | Apraksts |
|----------------|--------|-------------|
| Teksta izvietojums | **Pa kreisi**, **Pa labi**, **Pa vidu** | Šis rekvizīts nosaka teksta novietojumu attiecībā pret attēlu. Tas attiecas tikai uz varoņa izkārtojumu. |
| Teksta motīvs     | **Gaišs** vai **Tumšs** | Teksta krāsu shēmu var definēt, pamatojoties uz fona attēlu. Piemēram, ja attēlam ir tumšs fons, var lietot gaismas dizainu, lai tekstu padarītu redzamāku un panāktu atbilstību krāsu kontrasta koeficientu pieejamībai. Tas attiecas tikai uz varoņa izkārtojumu.|
| Attēla izvietojums       | **Pa kreisi**,  **Pa labi** | Šis rekvizīts norāda, vai attēlam jāatrodas pa kreisi vai pa labi no teksta. Tas attiecas tikai uz funkciju izkārtojumu.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Satura bloka moduļa pievienošana jaunā lapā

Lai pievienotu centrālo moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un izveidojiet lapas veidni ar nosaukumu **Satura bloka veidne**.
1. Noklusētās lapas **Galvenajā** slotā pievienojiet centrālo moduli.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Izmantojiet jūsu tikko izveidoto konteinera varoņa veidni, lai izveidotu lapu ar nosaukumu **Satura bloka lapa**.
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduļa to moduli un pēc tam atlasiet **Labi**.
1. Strukturējuma kokā pa kreisi atlasiet satura bloka moduli.
1. Rekvizītu rūts labajā pusē atlasiet **Pievienot attēlu**. Pēc tam vai nu atlasiet esošu attēlu, vai augšupielādējiet jaunu attēlu.
1. Atlasiet **Virsraksts**.
1. Dialoglodziņā **Virsraksts** pievienojiet virsraksta tekstu, atlasiet virsraksta līmeni un pēc tam atlasiet **Labi**.
1. Sadaļā **Bagātināts teksts** pievienojiet vēlamo tekstu.
1. Atlasiet **Pievienot saiti**.
1. Dialoglodziņā **Saite** pievienojiet saites tekstu, saites vietrādi URL un ARIA etiķeti saitei un pēc tam atlasiet **Labi**.
1. Atlasiet **Varonis** izkārtojumu.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to. 

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Akcijas reklāmkaroga modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Teksta bloka modulis](add-content-rich-block.md)

[Video atskaņotāja modulis](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
