---
title: Preces lapas papildināšana
description: Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097342"
---
# <a name="enrich-a-product-page"></a>Preces lapas papildināšana


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

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
