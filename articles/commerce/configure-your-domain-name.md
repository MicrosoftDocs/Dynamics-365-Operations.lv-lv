---
title: Domēna nosaukuma konfigurēšana
description: Šajā rakstā ir izskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics 365 e-komercijas vietnei.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 00c75581ba08979dfbc784f949c30b9bf78d44c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892135"
---
# <a name="configure-your-domain-name"></a>Domēna nosaukuma konfigurēšana


[!include [banner](includes/banner.md)]

Šajā rakstā ir izskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics 365 e-komercijas vietnei. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domēnu pievienošana e-komercijas inicializēšanas laikā

Lai saistītu domēnus ar savu Dynamics 365 Commerce e-komercijas vidi, inicializējiet e-komerciju, kā aprakstīts tēmā [Jaunas e-komercijas nomnieka izvietošana](deploy-ecommerce-site.md). Inicializēšanas laikā jums tiek lūgts sniegt informāciju, kas tiks izmantota jūsu e-komercijas vides nodrošināšanai. Laukā **Atbalstītie resursdatora nosaukumi** pievienojiet visus domēnus, kurus plānojat izmantot šajā vidē. Vairāki domēni jāatdala ar semikolu. Šādā veidā domēni tiek konfigurēti visos nepieciešamajos komercijas komponentos, un tie ir gatavi izmantošanai, kad pārslēdzat datplūsmu no sava satura piegādes tīkla (CDN) vai tīmekļa servera un novirziet to uz e-komercijas priekšgalu.

## <a name="add-domains-after-e-commerce-initialization"></a>Domēnu pievienošana pēc e-komercijas inicializēšanas

Lai saistītu jaunus domēnus ar savu e-komercijas vidi pēc e-komercijas inicializēšanas, ir jāiesniedz pakalpojuma pieprasījums.

## <a name="additional-resources"></a>Papildu resursi

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]