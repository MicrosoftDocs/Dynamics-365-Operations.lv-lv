---
title: Esošās vietnes lapas modificēšana
description: Šajā rakstā ir aprakstīts, kā modificēt esošu vietnes lapu Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/14/2020
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
ms.openlocfilehash: fb5348c2f29625647f06e48233f877a847677486
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286923"
---
# <a name="modify-an-existing-site-page"></a>Esošās vietnes lapas modificēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā modificēt esošu vietnes lapu Microsoft Dynamics 365 Commerce.

Kad ir jāmodificē lapa, pirmā darbība ir tās atvēršana lapas redaktorā. Dodieties uz vietni, kas satur jūsu lapu, un tad lapu sarakstā atrodiet lapu, ko vēlaties. Ja nevarat atrast lapu, varat izmantot autorēšanas rīka bagātīgās meklēšanas funkcionalitāti. Ierakstiet vai nu precīzu lapas nosaukumu, vai arī pirmos tā burtus un pēc tam zvaigznīti (\*). Tiek parādīts filtrēts lapu saraksts. Varat izmantot šo sarakstu, lai atrastu vēlamo lapu. Kad esat atradis pareizo lapu, atlasiet lapas nosaukumu, lai atvērtu lapu lapas redaktorā.

> [!TIP]
> Ja lapa ir redzama lapas inspektorā, varat atlasīt **Rediģēt** un pārbaudīt lapu, pirms atverat to lapas redaktorā. Šādā veidā varat izrakstīt vairākas lapas vienlaicīgi.

Kad lapa ir atvērta lapas redaktorā, pārliecinieties, ka tā ir izrakstīta jums. Autorēšanas rīka komandjosla ir dinamiska, kontekstjutīga un statusjutīga. Tāpēc tā rāda tikai darbības, ko pašlaik varat veikt lapā. Piemēram, ja lapa nav izrakstīta jums, pogas **Saglabāt** un **Pabeigt rediģēšanu** komandjoslā neparādās. Loga labajā pusē tiek parādīts arī lapas stāvoklis.

Ja lapa vēl nav izrakstīta jums, komandjoslā atlasiet **Rediģēt**. Komandjosla mainās, lai atspoguļotu lapas jauno stāvokli. Jūs saņemsiet arī paziņojumu par to, ka lapa tika izrakstīta jums.

Nākamā darbība ir veikt savas faktiskās izmaiņas. Bieži, lai atrastu un atlasītu moduli, ko vēlaties mainīt, izmantosiet lapas strukturējuma koku kreisajā pusē, un pēc tam veiksiet izmaiņas rekvizītu rūtī labajā pusē. 

Tomēr dažkārt izmaiņas var ietvert modeļu vai fragmentu pievienošanu vai noņemšanu. Lai pievienotu fragmentu vai moduli, izmantojiet lapas strukturējuma koku, lai atrastu slotu, kuram vēlaties pievienot moduli vai fragmentu, un pēc tam atlasiet daudzpunktes pogu (**...**) šim slotam. Tiek parādīta izvēlne, kurā ir iekļautas komandas moduļa vai fragmenta pievienošanai. Lai noņemtu moduli vai fragmentu, atrodiet un atlasiet to lapas strukturējuma kokā, atlasiet daudzpunktes pogu un pēc tam atlasiet komandu, lai dzēstu moduli vai fragmentu.

> [!TIP]
> Varat arī apskatīt un rediģēt rekvizītus jebkuram modulim, kas ir redzams vizuālā lapu veidotāja priekšskatījumā, atlasot to tieši.

Kad esat beidzis veikt izmaiņas un priekšskatījis to sekas, lapa ir jāreģistrē, komandjoslā atlasot **Pabeigt rediģēšanu**. 

Lai nekavējoties publicētu izmaiņas, komandjoslā atlasiet **Publicēt**. Jūsu modificētās lapas pēdējā reģistrētā versija ir publicēta un kļūst pieejama ārējiem lietotājiem, kuri skata jūsu vietni. 

## <a name="example-change-the-video-on-the-home-page"></a>Piemērs: video mainīšana sākumlapā

Tālāk minētajā piemērā ir parādīts, kā modificēt sākumlapu, mainot videoklipu, kas parādās video atskaņotāja modulī.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.
1. Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.
1. Komandjoslā atlasiet **Rediģēt**.
1. Lapas strukturējumā atlasiet slotu **Galvenais**.
1. Zem slota **Galvenais** izvērsiet visus mainīgos konteinera moduļus.
1. Atrodiet un atlasiet video atskaņotāja moduli.
1. Rekvizītu rūts labajā pusē atlasiet rekvizītu **Video**. Tiek parādīts līdzekļa atlasītājs.
1. Līdzekļu atlasītājā atlasiet pieejamo video līdzekli vai atlasiet **Augšupielādēt jaunu līdzekli**, lai augšupielādētu jaunu video līdzekli.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Laukā **Komentāri** ievadiet **Mainīts video** un pēc tam atlasiet **Labi**,
1. Atlasiet **Priekšskatījums**, lai priekšskatītu atjaunināto lapu. Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.
1. Atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)

[Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
