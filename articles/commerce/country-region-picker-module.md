---
title: Valsts / reģiona atlasītāja modulis
description: Šajā tēmā aprakstīts valsts/reģiona atlasītāja modelis un tā konfigurēšana Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
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
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 3134e10c096525ec2d82365a25eff16a3c5d5e11
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472645"
---
# <a name="countryregion-picker-module"></a>Valsts / reģiona atlasītāja modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā aprakstīts valsts/reģiona atlasītāja modelis un tā konfigurēšana Microsoft Dynamics 365 Commerce.

Valsts / reģiona atlasītāja modulis izmanto Dynamics 365 Commerce līdzekli [ģeolokācijas noteikšana un pārvirzīšana](geo-detection-redirection.md), lai rādītu ieteicamos URL tiem klientiem, kuri pieprasa e-komercijas vietnes URL, kas nav saistīta ar viņu valsti vai reģionu.

Piemēram, klients Kanādā pieprasa vietnes URL, kas nav saistīts ar Kanādu. Šādā gadījumā valsts / reģiona atlasītāja modulis rāda dialoglodziņu, kas iesaka vietnes URL vietrāžus, kuri ir saistīti ar Kanādu. Šajā attēlā parādīts valsts / reģiona atlasītāja dialoglodziņa piemērs.

![Valsts / reģiona atlasītāja dialoglodziņa piemērs sākumlapā.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties&quot;></a>Valsts / reģiona atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums              | Vērtība       | Apraksts |
| -------------------------- | ----------- | ----------- |
| Virsraksts                    | Teksts        | Galvene, kas tiek rādīta virs dialoglodziņa. |
| Apakšvirsraksts                 | Teksts        | Apakšvirsraksts, kas tiek rādīts zem galvenes. |
| Valsts: Displeja virkne    | Teksts        | URL opcijas parādāmais nosaukums (piemēram, &quot;Kanāda"). |
| Valsts: Displeja apakšvirkne | Teksts        | Neobligāta URL opcijas parādīšanas apakšvirne (piemēram, "Angļu" vai "Franču"). |
| Valsts: Valsts attēls     | Mediju līdzeklis | Neobligāts attēls, kas tiek saistīts ar URL opciju (piemēram, Kanādas karoga attēls). |
| Valsts: Valsts URL       | Teksts        | URL, kas atbilst kanālam un lokalizācijai, kas ir konfigurētas valstij vai reģionālā Commerce vietnes veidotāja lapā **Kanāli** (**Vietnes iestatījumi\>Kanāli**). Šim URL ir precīzi jāatbilst tam, kas konfigurēts lapā **Kanāli**. |
| Darbības saite                | Darbības saite | Neobligāta saite, kas parādās dialoglodziņa apakšdaļā. Piemēram, šī saite var norādīt uz iekšēju lapu, kurā sniegts visu vietnes atbalstīto valstu un reģionu saraksts. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Valsts / reģiona atlasītāja moduļa pievienošana lapai

Valsts / reģiona atlasītāja moduli var pievienot galvenes modulim vai nu tieši, vai ar kopīgotu fragmentu. Papildinformāciju par galvenes moduļiem skatiet sadaļā [Galvenes modulis](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Valsts / reģiona atlasītāja moduļa konfigurēšana Commerce vietnes veidotājā

> [!NOTE]
> URL, kurus iesakāt saviem klientiem, ir jākonfigurē kā valstu objektus valsts / reģiona atlasītāja modulī.

Katram URL, kuru vēlaties rādīt un ieteikt klientiem, veiciet šīs darbības Commerce vietnes veidotājā.

1. Atlasiet valsts / reģiona atlasītāja moduļa spraugu.
1. Rekvizītu rūtī zem **Valstu saraksts** atlasiet **Pievienot valsti**.
1. Atlasiet jaunās **Valsts** lodziņu.
1. Laukā **Parādāmā virkne** ievadiet parādāmo nosaukumu (piemēram, **Kanāda**).
1. Neobligāti: Laukā **Parādāmā apakšvirkne** ievadiet parādāmo apakšvirkni (piemēram, **Franču** vai **fr-ca**).
1. Neobligāti: Mediju krātuvē atlasiet attēlu.
1. Laukā **Valsts URL** ievadiet URL vietrādi. Šim URL ir precīzi jāatbilst tam, kas tiek rādīts lapā **Kanāli** un kas tiek kartēts kanālā, tostarp lokalizācijai, kas tiek saistīta ar valsti vai reģionu.
1. Atlasiet **Labi**.
1. Atkārtojiet šīs darbības citu valstu URL vietrāžiem, kurus vēlaties rādīt valsts / reģiona atlasītāja modulī.

## <a name="additional-resources"></a>Papildu resursi

[Ģeolokācijas noteikšanas un pārvirzīšanas iestatīšana](geo-detection-redirection.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Galvenes modulis](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
