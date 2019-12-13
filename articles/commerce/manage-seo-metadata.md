---
title: SEO metadatu pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698353"
---
# <a name="manage-seo-metadata"></a>SEO metadatu pārvaldība

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

SEO metadatus vietnei var pārvaldīt, izmantojot vietnes kartes un lapas metadatus.
    
## <a name="site-maps"></a>Vietnes kartes

Vietnes karte ir jūsu tīmekļa vietnes lapu mašīnlasāms saraksts XML formātā. Tas paredzēts meklēšanas programmu lietošanai, lai tās varētu nodrošināt labākus meklēšanas rezultātus no jūsu vietnes. Meklētājprogrammas var manuāli uzņemt vietnes kartes vai tās var publicēt robots.txt failā.

Dynamics 365 Commerce atbalsta automātisku vietnes karšu ģenerēšanu. Kad lapas tiek vai netiek publicētas, vietas kartes tiek automātiski atjauninātas.

### <a name="turn-on-site-map-generation"></a>Vietnes kartes ģenerēšanas ieslēgšana

1. Pierakstieties autorēšanas rīkā.
1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas pārvaldība**.
1. Pārliecinieties, vai ir ieslēgta opcija **Vietnes lapas iespējotas**.

## <a name="page-metadata"></a>Lapas metadati

Dynamics 365 Commerce ļauj pārvaldīt SEO metadatus atsevišķām lapām. Varat apskatīt un modificēt šo informāciju lapas konteinera sadaļā **SEO rekvizīti**. Pašlaik tiek atbalstīti tālāk minētie SEO metadatu rekvizīti.

- Virsraksts
- Apraksts
- SEO atslēgvārdi
- Aria etiķetes
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Lapas metadatu modificēšana

Lai modificētu lapas metadatus, veiciet tālāk minētās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.
1. Atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.
1. Darbību rūtī atlasiet **Izrakstīt**.
1. Rekvizītu rūts labajā pusē izvērsiet **Noklusējuma metaetiķetes**.
1. Lai pievienotu jaunu metaetiķeti, atlasiet **Pievienot** un pēc tam laukā ievadiet etiķeti.

    Lai noņemtu esošu metaetiķeti, atlasiet miskastes simbolu pa labi no tās.

1. Atlasiet **Saglabāt** un pēc tam **Pārbaudīt**.
1. Laukā **Komentāri** ievadiet **Atjauninātas metaetiķetes** un pēc tam atlasiet **Labi**,
1. Atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.
1. Atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

