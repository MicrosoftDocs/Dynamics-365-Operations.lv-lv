---
title: Dinamisku e-komercijas lapu izveide, pamatojoties uz URL parametriem
description: Šajā tēmā aprakstīts, kā iestatīts Microsoft Dynamics 365 Commerce e-komercijas lapu, kura var apkalpot dinamisku saturu, pamatojoties URL parametros.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795815"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Dinamisku e-komercijas lapu izveide, pamatojoties uz URL parametriem

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīts Microsoft Dynamics 365 Commerce e-komercijas lapu, kura var apkalpot dinamisku saturu, pamatojoties URL parametros.

E-komercijas lapu var konfigurēt, lai tā kalpotu dažādam saturam, pamatojoties uz segmentu vietrāža URL ceļā. Tāpēc šī lapa ir pazīstama kā dinamiskā lapa. Segments tiek izmantots kā parametrs lapas satura izgūšanai. Piemēram, lapa, kas ir nosaukta par **blog\_viewer**, tiek izveidota un saistīta ar URL `https://fabrikam.com/blog`. Pēc tam šo lapu var izmantot, lai parādītu dažādu saturu, balstoties uz pēdējo segmentu URL ceļā. Piemēram, pēdējais segments vietrādī URL `https://fabrikam.com/blog/article-1` ir **article-1**.

Atsevišķas pielāgotas lapas, kas ignorē dinamisko lapu, var tikt saistītas arī ar segmentiem vietrāža URL ceļā. Piemēram, lapa, kas ir nosaukta par **blog\_summary**, tiek izveidota un saistīta ar URL `https://fabrikam.com/blog/about-this-blog`. Kad tiek pieprasīts šis URL, tiek atgriezta **bloga\_kopsavilkuma** lapa, kas ir saistīta ar **/about-this-blog** parametru, nevis **blog\_viewer** lapa.

> [!NOTE]
> Dinamisko lapu satura viesošanas, izgūšanas un rādīšanas funkcionalitāte tiek īstenota, izmantojot pielāgotu moduli. Papildinformāciju skatiet šeit: [Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Dinamiskās e-komercijas lapas iestatīšana

Lai iestatītu dinamisku e-komercijas lapu, ir jāizveido dinamiskā lapa, jāizveido pamata vietrādis URL un jākonfigurē maršruts dinamiskajā lapā.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Izveidot lapu, kurā tiks rādīts dinamisks saturs

Lai izveidotu lapu, kurā tiks rādīts dinamisks saturs, izpildiet sekojošās darbības sadaļā [Pievienot jaunu vietnes lapu](add-new-page.md). Jūsu izveidotajai lapai būs nepieciešams ieviest moduli, kas izmanto pēdējo segmentu URL ceļā, lai izgūtu saturu no ārēja datu avota. Papildinformāciju par pielāgotu moduļa izstrādi skatiet sadaļā [Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Izveidot dinamiskās lapas pamata vietrādi URL

Lai izveidotu pamata URL dinamiskajai lapai Commerce vietnes veidotājā, sekojiet šiem soļiem.

1. Dodieties uz **Vietrāži URL** un atlasiet **Jauns \> Jauns URL**.
1. Dialoglodziņā **Izveidot jaunu URL** atlasiet **Iekšējo lapu**. Sadaļā **URL ceļš** ievadiet ceļu, kas kalpos kā dinamiskās lapas sakne (šajā piemērā **/blog**). Pēc tam atlasiet **Jauns**.
1. Dialoglodziņā **Atlasīt lapu** atlasiet izveidoto lapu, kura tiks rādīta kā dinamiskā lapa, un pēc tam atlasiet **Saglabāt**.
1. Atlasiet **Publicēt**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Konfigurēt maršrutu uz dinamisko lapu

Lai konfigurētu maršrutu uz dinamisko lapu Commerce vietnes veidotājā, sekojiet šiem soļiem.

1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. Sadaļā **Parametrizēti URL ceļi** atlasiet **Pievienot** un pēc tam ievadiet URL ceļu, ko ievadījāt, kad izveidojāt URL (šajā piemērā **/blog**).
1. Atlasiet **Saglabāt un publicēt**.

Kad maršruts ir konfigurēts, visi pieprasījumi uz parametrizētu URL ceļu atgriezīs lapu, kas ir saistīta ar šo URL. Ja jebkādi pieprasījumi ietver papildu segmentu, tiks atgriezta saistītā lapa, un lapas saturs tiks izgūts, kā parametru izmantojot segmentu. Piemēram, `https://fabrikam.com/blog/article-1` atgriezīs **blog\_summary** lapu, un lapas saturs tiks izgūts, izmantojot **/article-1** parametru.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Ignorēt parametrizētu URL ar pielāgotu lapu

Lai ignorētu parametrizētu URL ar pielāgotu lapu Commerce vietnes veidotājā, sekojiet šiem soļiem.

1. Dodieties uz **Vietrāži URL** un atlasiet **Jauns \> Jauns URL**.
1. Dialoglodziņā **Izveidot jaunu URL** atlasiet **Iekšējo lapu**. Sadaļā **URL ceļš** ievadiet ceļu, kas ietver ignorēšanas segmentu (šajā piemērā, **/blog/about-this-blog**). Pēc tam atlasiet **Jauns**.
1. Dialoglodziņā **Atlasīt lapu** atlasiet pielāgoto lapu un pēc tam atlasiet **Saglabāt**.
1. Atlasiet **Publicēt**.
1. Ja pielāgotā lapa vēl nav publicēta, atveriet lapas, dodieties uz **Lapas**, atlasiet pielāgoto lapu un tad atlasiet **Publicēt**.

Kad pielāgotā lapa ir publicēta, tā tiks apkalpota dinamiskās lapas, kam ir parametru saturs, vietā.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)

[Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
