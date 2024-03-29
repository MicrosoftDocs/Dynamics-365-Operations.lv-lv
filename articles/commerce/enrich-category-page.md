---
title: Kategorijas ielādes lapas papildināšana
description: Šajā rakstā ir apskatīta kategoriju lapu bagātināšana Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e3397ffee9b32f3d3efedea38255f88daee5233c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282166"
---
# <a name="enrich-a-category-landing-page"></a>Kategorijas ielādes lapas papildināšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīta kategoriju lapu bagātināšana Dynamics 365 Commerce.

Commerce nodrošina noklusējuma kategorijas mērķlapu, kas tiek izmantota, kad tiek parādīti kategorijas dati. Noklusējuma kategorijas lapa satur obligātos elementus, piemēram, uzlabotājus, kategorizētas preces izvietošanu, šķirošanas iespējas, izvēles kopsavilkumu un lappušu numerācijas vadīklas. 

Tomēr, tā vietā, lai izmantotu noklusējuma kategorijas lapu, iespējams, vēlēsieties izmantot "papildinātu" kategorijas mērķlapu, kam ir vairāk satura un specifiskāki elementi. Parasta papildināšana var ietvert kategorijai specifiska mārketinga satura pievienošanu kategorijas lapai. Šis saturs var ietvert vairāku preces izvietošanu dažādās kategorijās papildu pārdošanas nolūkam, redakcijas sarakstus, attēlus, video un citu tekstu. Varat vai nu modificēt noklusējuma kategorijas lapu, vai definēt citu kategorijas lapu noteiktai kategorijai.

![Bagātināta kategorijas ielādes lapa.](./media/CategoryLandingPages.png)

Commerce vietnes veidotājā lapa **Prece** ietver kategoriju sarakstu no kanāla, kas piešķirts vietnei. Ja kategorijas lapai atlasīts statuss **Papildināts**, šī kategorijas lapa ir tikusi papildināta. Pretējā gadījumā kategorijai tiek izmantota noklusējuma kategorijas lapa un saturs. Varat priekšskatīt gan papildinātas, gan nepapildinātas kategorijas lapas, atlasot kategorijas nosaukumu.

Lai papildinātu kategorijas lapu, veiciet tālāk minētās darbības.

1. Lapā **Preces** atlasiet tās kategorijas nosaukumu, kurai vēlaties papildināt kategorijas lapu. Lapas redaktorā tiek atvērta atlasītās kategorijas noklusējuma kategorijas lapa.
2. Atlasiet **Papildināt kategorijas lapu**.
3. Atlasiet papildinātās kategorijas lapas veidni. Ja izdarāt tikai nelielas izmaiņas, varat atlasīt noklusējuma kategorijas lapu. Vai arī varat atlasīt noteiktas kategorijas lapas veidni. Kad atlasāt veidni, tiek atvērts lapas redaktors, un atlasītā veidne tiek izmantota, lai izveidotu jaunu kategorijas lapu atlasītajai kategorijai. Lapa tiek izrakstīta jums, un tagad varat veikt savas izmaiņas.

> [!NOTE]
> Moduļi, kas izmanto kategorijas specifikācijas datus, izmanto datus no atlasītās kategorijas. Jūsu atlasītā veidnes iestatījumi nosaka izmaiņas, ko varat veikt.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)

[Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
