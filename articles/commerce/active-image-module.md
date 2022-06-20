---
title: Aktīvā attēla modulis
description: Šajā rakstā ir ietverti aktīvie attēlu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3d532d21f847a80a16af814eeaf097a616605795
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853854"
---
# <a name="active-image-module"></a>Aktīvā attēla modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti aktīvie attēlu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Lai attēliem iegultu preču tagus, var izmantot aktīvā attēla moduli. E-komercijas vietnes lietotāji pēc tam var novietojiet kursoru virs tagiem, lai priekšskatītu preces, kas tiek parādītas attēlā. Priekšskatījumi tiek parādīti uznirstošos logus. Atlasot uznirstošo priekšskatījuma logu, lietotāji var doties tieši uz attiecīgās preces informācijas lapu (PDP).

Tagi tiek definēti, attēlam izmantojot X un Y koordinātas. Katrs atzīmētais punkts ir jākonfigurē ar preces ID, kas tiek rādīts attēlā.

Šajā attēlā parādīts priekšskatījuma uznirstošā loga piemērs Adventure Works mājas lapā.

![Priekšskatījuma uznirstošā loga piemērs aktīvā attēla modulī](./media/Active_image.PNG)

> [!IMPORTANT]
> - Aktīvā attēla modulis ir pieejams Dynamics 365 Commerce versijas 10.0.20 laidienā.
> - Aktīvā attēla modulis tiek rādīts Adventure Works tēmā.

## <a name="active-image-module-properties"></a>Aktīvā attēla moduļa rekvizīti

| Rekvizīta nosaukums      | Vērtības | Apraksts |
|--------------------|--------|-------------|
| Attēls              | Attēla fails | Attēlu var izmantot, lai rādītu vienu vai vairākas preces. Attēlu var augšupielādēt multivides bibliotēkā Commerce vietnes veidotājā vai izmantot esošu attēlu. |
| Platums              | Pikseļu skaits | Šis rekvizīts nosaka attēla platumu. Aktīvās koordinātas tiek aprēķinātas, pamatojoties uz attēla platumu.|
| Aktīvās koordinātas | X un Y koordinātas un preces ID numurs | Katrs aktīvā attēla masīvs sastāv no X un Y koordinātām un preces ID numura.|
| Virsraksts            | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pēc noklusējuma virsrakstam tiek izmantots virsraksta tags **H2**, bet tagu var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa          | Rindkopas teksts | Modulis atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, hipersaites, treknraksts, pasvītrots un slīpraksta teksts. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt               | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** atlasītājs | Modulis atbalsta vienu vai vairākas saites “aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |
| Apakštekts           | Virsraksts, teksts un saites | Var pievienot papildu kontekstu attēlam, piemēram, autora vai veidotāja vārdu, vai saites uz personīgajām papildmaksām.|
| Teksta motīvs         | **Gaišs** vai **Tumšs** | Pamatojoties uz fona attēlu, šis rekvizīts lietotājam ļauj iestatīt tekstu kā gaišu vai tumšu. Tas ir pieejams kā tēmas paplašinājums Adventure Works tēmā. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Pievienot aktīva attēla moduli jaunai lapai

Lai pievienotu aktīvā attēla moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un atveriet mārketinga veidni jūsu vietnes mājas lapai (vai izveidojiet jaunu mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet aktīvo attēlu **moduli** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atveriet vietnes sākumlapu (vai izveidojiet jaunu mājas lapu, izmantojot mārketinga veidni).
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet aktīvo attēlu **moduli** un pēc tam atlasiet **Labi**.
1. Aktīvā attēla moduļa rekvizītu rūtī pievienojiet attēlu un iestatiet attēla izmēram pārsvaidāmo platumu.
1. Iestatiet X un Y koordinātas un pievienojiet attiecīgo preces ID numuru.
1. Pievienojiet un konfigurējiet papildu aktīvā attēla moduļus pēc nepieciešamības.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Adventure Works tēma](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
