---
title: Domēna nosaukuma konfigurēšana
description: Šajā tēmā paskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics365 e-komercijas vietnei.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770462"
---
# <a name="configure-your-domain-name"></a>Domēna nosaukuma konfigurēšana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā paskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics365 e-komercijas vietnei. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domēnu pievienošana E-komercijas inicializēšanas laikā

Lai saistītu domēnus ar savu e-komercijas vidi, inicializējiet E-komerciju, kā aprakstīts tēmā [Jaunas E-komercijas vietnes izvietošana](deploy-ecommerce-site.md). Inicializēšanas laikā jums tiek lūgts sniegt informāciju, kas tiks izmantota jūsu E-komercijas vides nodrošināšanai. Laukā **Atbalstītie resursdatora nosaukumi** pievienojiet visus domēnus, kurus plānojat izmantot šajā vidē. Vairāki domēni jāatdala ar semikolu. Šādā veidā domēni tiek konfigurēti visos nepieciešamajos E-komercijas komponentos, un tie ir gatavi izmantošanai, kad pārslēdzat datplūsmu no sava satura piegādes tīkla (CDN) vai tīmekļa servera un novirziet to uz E-komercijas priekšgalu.

## <a name="add-domains-after-e-commerce-initialization"></a>Domēnu pievienošana pēc E-komercijas inicializēšanas

Lai saistītu jaunus domēnus ar savu E-komercijas vidi pēc E-komercijas inicializēšanas, ir jāiesniedz pakalpojuma pieprasījums.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes veikala apskats](online-store-overview.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Jaunas e-komercijas vietnes izvietošana](deploy-ecommerce-site.md)

[Tiešsaistes vietnes saistīšana ar kanālu](associate-site-online-store.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)
