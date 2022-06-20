---
title: Elementu saraksta modulis
description: Šajā rakstā ir apskatīti elementa saraksta moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 44eb9b82ef9625734c7fe5ccba85207d9f210a00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905402"
---
# <a name="tile-list-module"></a>Elementu saraksta modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti elementa saraksta moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Elementu saraksta modulis ir karuseļveida elementu kolekcija. Tas tiek izmantots, lai tirgotu produktu kategorijas vai preču zīmolus, izmantojot attēlus un tekstu. Piemēram, mazumtirgotājs var pievienot elementu saraksta moduli e-komercijas vietnes mājas lapai, lai veicinātu visu augšējo pārdošanas kategoriju iniciatīvas.

Elementu saraksta moduli vada dati no satura pārvaldība sistēmas (CMS). Tas nav atkarīgs no citiem moduļiem vai datiem no programmas Commerce Headquarters. Elementu saraksta moduli var pievienot jebkurai vietnes lapai, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, kategorijas vai zīmoli).

Šajā ilustrācijā parādīts elementu saraksta moduļa un elementa moduļu piemērs Adventure Works mājas lapā.

![Elementu saraksta moduļa un elementa moduļu piemērs Adventure Works mājas lapā](./media/Tile_list.PNG)

> [!IMPORTANT]
> Elementu saraksta modulis ir pieejams Dynamics 365 Commerce versijas 10.0.20 laidienā.
> Elementu saraksta modulis tiek rādīts Adventure Works tēmā.

## <a name="tile-list-modules-and-themes"></a>Elementu saraksta moduļi un tēmas

Elementu saraksta modulis var atbalstīt dažādus izkārtojumus un stilus, kas balstīti uz tēmu. Piemēram, Adventure Works tēmā elementi parāda animācijas efektu, kad vietnes lietotāji norāda uz tiem. Katrā tēmā var būt papildu rekvizīti elementu sarakstam un elementu moduļiem. Tēmas izstrādātāji var arī izveidot papildu izkārtojumus elementu sarakstam un elementa moduļiem.

## <a name="tile-list-module-properties"></a>Elementu saraksta moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts       | Virsraksta teksts un virsraksta etiķete | Elementu saraksta moduļa teksta virsraksts. |

## <a name="tile-module-properties"></a>Elementa moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Attēls         | Attēla fails | Attēlu var izmantot, lai rādītu preci vai kategoriju. Attēlu var augšupielādēt multivides bibliotēkā Commerce vietnes veidotājā vai izmantot esošu attēlu. |
| Virsraksts       | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pēc noklusējuma virsrakstam tiek izmantots virsraksta tags **H2**, bet tagu var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa     | Rindkopas teksts | Modulis atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, hipersaites, treknraksts, pasvītrots un slīpraksta teksts. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt          | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** | Moduļi atbalsta vienu vai vairākas saites “aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |
| Elementa saite     | Saites teksts, saites vietrādis URL, ARIA etiķete un **Atvērt saiti jaunā cilnē** atlasītājs | Šis rekvizīts tiek izmantots, lai definētu saiti "izsaukt darbībai". Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē.|
| Icon          | Attēls | Papildus preces vai kategorijas attēlam var pievienot ikonas simbolu. Ikonas simbola attēls parādīsies virs preces vai kategorijas attēla. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Elementu saraksta moduļa pievienošana jaunā lapā

Lai pievienotu elementu saraksta moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un atveriet mārketinga veidni jūsu vietnes mājas lapai (vai izveidojiet jaunu mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet elementu saraksta **moduli** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atveriet vietnes sākumlapu (vai izveidojiet jaunu mājas lapu, izmantojot mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet elementu saraksta **moduli** un pēc tam atlasiet **Labi**.
1. Elerntu saraksta moduļa rekvizītu rūtī pievienojiet virsrakstu.
1. Elementa saraksta **slotā** atlasiet elipses pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Elements **un** pēc tam atlasiet **Labi**.
1. Elementa moduļa rekvizītu rūtī pievienojiet attēlu, virsrakstu un ikonas simbola attēlu.
1. Pievienojiet un konfigurējiet papildu elementa moduļus pēc nepieciešamības.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Adventure Works tēma](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
