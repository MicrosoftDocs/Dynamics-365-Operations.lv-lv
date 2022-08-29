---
title: Jaunas vietnes lapas pievienošana
description: Šajā rakstā ir aprakstīts, kā pievienot jaunu vietnes lapu Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f6714463c9d5dc844b03f78f0f6ff60c5f270da3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270323"
---
# <a name="add-a-new-site-page"></a>Jaunas vietnes lapas pievienošana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pievienot jaunu vietnes lapu Microsoft Dynamics 365 Commerce.

Pēc tam, kad esat izveidojis veidnes un fragmentus jūsu vietnei, nākamais solis ir izveidot lapas, kas tās izmanto. Lai sāktu darbu, jāatlasa veidne vai izkārtojums, lapas nosaukums un lapas vietrādis URL.

## <a name="template-or-layout"></a>Veidne vai izkārtojums

Jaunajai lapai varat izmantot veidni vai izkārtojumu. Papildinformāciju skatiet tēmā [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>Norādiet lapas nosaukumu

Lapas nosaukumam jābūt unikālam jūsu vietnē, un tam jābūt aprakstošam, lai varētu to viegli atrast, un citiem cilvēkiem ir jāzina, kam paredzēta lapa. Varat pārdēvēt lapu vēlāk, to labojot, pēc tam rekvizītu rūtī atlasot pildspalvas simbolu blakus lapas nosaukumam.

## <a name="specify-the-page-url"></a>Norādiet lapas URL

Jums var būt opcija ievadīt vietrādi URL savai jaunai lapai. Veidojot lapu, varat ievadīt virkni, kas tiks izmantota pilnīga vietrāža URL izveidei. Šī virkne ir zināma kā relatīvais vietrādis URL vai URL rinda. Tiek ģenerēts pilnīgs vietrādis URL, pamatojoties uz URL rindu, un tam ir piešķirta jaunā lapa. Varat vēlāk mainīt URL rindu pirms lapas publicēšanas. Papildinformāciju skatiet tēmā [Lapas vietrāža URL izveide](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce atdala vietrāžus URL un saturu. Citiem vārdiem, var izveidot lapu, kas nav saistīta ar vietrādi URL, un var izveidot vietrādi URL, kas nav saistīts ar lapu. Tāpēc satura pārnešanu var veikt vietrādim URL, tam nav nepieciešama dīkstāve un ir vieglāk pārvaldīt pārvirzīšanu.

## <a name="add-a-new-page"></a>Jaunas lapas pievienošana

Lai vietnei pievienotu jaunu vietnes lapu, veiciet tālāk norādītās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Atlasiet **Jauna lapa**.
1. Dialoglodziņā **Jauna lapa** atlasiet veidni un pēc tam atlasiet **Labi**.
1. Laukā **Lapas nosaukums** ievadiet lapas nosaukumu (piemēram, **Mana jauna lapa**).
1. Laukā **URL** ievadiet virkni (URL rinda), lai pabeigtu vietrādi URL (piemēram, **mynewpage**).
1. Atlasiet **Labi**. Tiek atvērts lapas redaktors. Ievērojiet, ka galvene un kājene tiek automātiski pievienoti lapai, pamatojoties uz jūsu atlasīto veidni.
1. Lapas strukturējumā atlasiet slotu **Galvenais**, atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Atlasiet **Konteiners** un pēc tam atlasiet **Labi**.
1. Atlasiet daudzpunktes pogu **Mainīgs konteiners** un pēc tam atlasiet **Pievienot moduli**.
1. Atlasiet **Bagātināta satura bloks** un pēc tam atlasiet **Labi**.
1. Atlasiet **Bagātinātā satura bloks**, atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli**.
1. Atlasiet **Bagātinātā satura bloka elements** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī pa labi atlasiet **Rindkopa** un pēc tam laukā ievadiet **Mans testa teksts**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Laukā **Komentāri** ievadiet **Pievienota jauna lapa** un pēc tam atlasiet **Labi**.
1. Atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.
1. Atlasiet **Publicēt**.
1. Navigācijas ceļā (atpakaļceļš) atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Vietrāži URL**.
1. Sarakstā atrodiet un atlasiet savu vietrādi URL (**mynewpage**).
1. Atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)

[Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
