---
title: Interaktīvā līdzekļa modulis
description: Šajā rakstā ir ietverti interaktīvi līdzekļu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: deee7c35cfc4293480fda74665429121b71bbfab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898523"
---
# <a name="interactive-feature-module"></a>Interaktīvā līdzekļa modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti interaktīvi līdzekļu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Interaktīvie līdzekļu moduļi ir papildu moduļi, ko var izmantot vairāku preču kategoriju vai preču zīmolu tirgus, izmantojot attēlu un teksta kombināciju. Piemēram, mazumtirgotājs var pievienot interaktīvu funkcionalitātes moduli e-komercijas vietnes mājas lapai, lai veicinātu augšējo pārdošanas kategoriju iniciatīvas. Interaktīvās funkcionalitātes modulis ir līdzīgs elementa saraksta modulim, bet tam ir cits izkārtojums un atšķirīga mijiedarbības funkcionalitāte.

Katrs interaktīvās funkcionalitātes modulis ir interaktīvu krājumu moduļu kolekcija. Katra līdzekļa elementa moduli vada dati no satura pārvaldība sistēmas (CMS). Tas nav atkarīgs no citiem moduļiem vai datiem no programmas Commerce Headquarters. Interaktīvā līdzekļa moduli var pievienot jebkurai vietnes lapai, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, kategorijas vai zīmoli).

> [!IMPORTANT]
> - Interaktīvā līdzekļa modulis ir pieejams Dynamics 365 Commerce versijas 10.0.20 laidienā.
> - Interaktīvā līdzekļa modulis tiek rādīts Adventure Works tēmā.

Šajā ilustrācijā parādīts interaktīvā līdzekļa moduļa piemērs Adventure Works mājas lapā.

![Interaktīvā līdzekļa moduļa piemērs Adventure Works mājas lapā](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktīvā līdzekļa modulis un tēmas

Interaktīvā līdzekļa modulis var atbalstīt dažādus izkārtojumus un stilus, kas balstīti uz tēmu. Piemēram, Adventure Works tēmā interaktīvās funkcionalitātes modulim ir divu kolonnu izkārtojums, kas parāda krāsu efektus, kad vietas lietotājs novirzās pār katru krājumu. Interaktīvās funkcionalitātes modulis ir optimizēts pāra skaita attēliem, kas izkārtoti divu kolonnu izkārtojumā.

## <a name="interactive-feature-module-properties"></a>Interaktīvā līdzekļa modulis rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts       | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Interaktīvā līdzekļa moduļa teksta virsraksts. |

## <a name="interactive-feature-item-module-properties"></a>Interaktīvo līdzekļu krājuma modulis rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Attēls         | Attēla fails | Attēls, kurā ir prece vai kategorija. Attēlu var augšupielādēt multivides bibliotēkā Commerce vietnes veidotājā vai izmantot esošu attēlu. |
| Virsraksts       | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pēc noklusējuma virsrakstam tiek izmantots virsraksta tags **H2**, bet tagu var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa     | Rindkopas teksts | Modulis atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, hipersaites, treknraksts, pasvītrots un slīpraksta teksts. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt          | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** atlasītājs | Modulis atbalsta vienu vai vairākas saites “aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Interaktīvā līdzekļa moduļa pievienošana jaunā lapā

Lai pievienotu interaktīvā līdzekļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus Commerce vietņu veidotājā, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un atveriet mārketinga veidni jūsu vietnes mājas lapai (vai izveidojiet jaunu mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Interaktīvā **funkcija** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atveriet vietnes sākumlapu (vai izveidojiet jaunu mājas lapu, izmantojot mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņa Moduļu **atlase** sadaļā Atlasīt moduļus **atlasiet** moduli Interaktīvā **funkcija** un pēc tam atlasiet **Labi**.
1. Interaktīvā līdzekļa moduļa rekvizītu rūtī pievienojiet virsrakstu.
1. Interaktīvā **līdzekļa** slotā atlasiet elipses pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Interaktīvā **funkcionalitāte un** pēc tam atlasiet **Labi**.
1. Interaktīvā funkcionalitātes krājumu moduļa rekvizītu rūtī pievienojiet attēlu, virsraksta tekstu, punktu tekstu un URL.
1. Pievienojiet un konfigurējiet papildu interaktīvo līdzekļu krājuma moduļus pēc nepieciešamības.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Adventure Works tēma](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
