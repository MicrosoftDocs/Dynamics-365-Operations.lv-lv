---
title: Preces lapas papildināšana
description: Šajā rakstā ir aprakstīts, kā bagātināt preču lapu Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ad58f0324c91c7488e5eb823fa3d0e1758ec63fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847630"
---
# <a name="enrich-a-product-page"></a>Preces lapas papildināšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā bagātināt preču lapu Microsoft Dynamics 365 Commerce.

Pēc noklusējuma jūsu vietne izmanto vispārējo lapu, lai parādītu preces datus. Šajā lapā ir ietverta pamatinformācija par preci un vadīklas, kas nepieciešamas tās pārdošanai. Tomēr varat papildināt no Tirdzniecības mēroga vienības servera nākošo informāciju ar papildu attēliem vai tekstu par konkrēto preci. Šis process ir pazīstams kā preces lapas papildināšana.

Daudzos gadījumos jums vajadzēs savām precēm izmantot specifisku papildu saturu. Kad autorēšanas rīkā dosieties uz **Mazumtirdzniecība un komercija**, redzēsiet preču sarakstu no kanāla, kas ir piešķirts vietnei. Šajā sarakstā kolonna **Papildināts** norāda, vai preces lapa par preci ir papildināta. Ja kolonnā izdarīta atzīme, šai precei ir papildināta preces lapa. Ja atzīme nav izdarīta, precei tiek izmantota noklusējuma preces lapa un saturs. Varat priekšskatīt gan papildinātas, gan nepapildinātas preces lapas, sarakstā atlasot preces nosaukumu.

## <a name="enrich-a-product-page"></a>Preces lapas papildināšana

Lai papildinātu preces lapu, veiciet tālāk minētās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Preces**.
1. Atlasiet jebkuru preci, kurai nav papildinātas preces lapas.
1. Darbību rūtī atlasiet **Papildināt preces lapu**.
1. Atlasiet **PDP veidne** un pēc tam atlasiet **Labi**.
1. Lapas strukturējuma kokā kreisajā izvērsiet slotu **Galvenais**.
1. Atlasiet daudzpunktes pogu (**...**) slotam **Galvenais** un pēc tam atlasiet **Pievienot moduli**.
1. Atlasiet **2. konteiners** un pēc tam atlasiet **Labi**.
1. Atlasiet daudzpunktes pogu **2. konteiners** un pēc tam atlasiet **Pievienot moduli**.
1. Atlasiet **Līdzeklis** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī labajā pusē laukā **Bagātināts teksts** ievadiet atjaunināto preces aprakstu.
1. Laukā **Virsraksts** ievadiet virsraksta tekstu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Laukā **Komentāri** ievadiet **Papildināta prece** un pēc tam atlasiet **Labi**,
1. Atlasiet **Priekšskatījums**, lai priekšskatītu papildinātās preces lapu. Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.
1. Atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)

[Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
