---
title: Vērtējumu un atsauksmju konfigurēšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fcdf571378c25d71b3ef4f3baad062a25390417
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993554"
---
# <a name="configure-ratings-and-reviews"></a>Vērtējumu un atsauksmju konfigurēšana

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, parādot ko citi klienti domā par šīm precēm. E-komercijas tīmekļa vietnēm vērtējumi un atsauksmes ir arī mehānisms klientu atsauksmju apkopošanai par precēm. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai

Konfigurācijas vērtības vērtējumiem un atsauksmēm, piemēram, īrnieka ID, atsauksmes teksta garums un atsauksmes nosaukuma garums tiek konfigurēti vietnes līmenī. 

Lai konfigurētu vietni vērtējumu un atsauksmju rādīšanai, veiciet šīs darbības. 

1. Dodieties uz **Sākums \> Vietnes**.
1. Atlasiet vietnes nosaukumu 
1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**. 
1. Laukā **Rediģēt teksta maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes tekstam (piemēram, **1000**). 
1. Laukā **Rediģēt nosaukuma maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes nosaukumam (piemēram, **55**). 
1. Atlasiet **Saglabāt un publicēt**. 

Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.

![Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Preču vērtējuma saistīšana ar PDP sadaļu Atsauksmes

Preces vērtējums tiek parādīts zem produkta nosaukuma preču papildinformācijas lapas (PDP) augšdaļā. Preces vērtējumu var konfigurēt tā, lai tas būtu saistīts ar tās pašas PDP sadaļu **Atsauksmes**. 

Lai saistītu preces vērtējumu ar PDP sadaļu **Atsauksmes**, veiciet tālāk norādītās darbības.

1. Atveriet PDP veidni. 
1. Dodieties uz **Iegādes lodziņa konteinera moduļa iestatījumi**.
1. Sadaļā **Iegādes lodziņš** atlasiet **Preču vērtējumi** un pēc tam atzīmējiet izvēles rūtiņu **Saistīt klikšķi ar pilnu atsauksmju moduli**.

Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.

![Preces vērtējuma saistīšana ar PDP sadaļu Atsauksmes](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Saites konfigurēšana konfidencialitātes un politikas lapai

Lai konfigurētu saiti konfidencialitātes un politikas lapai, veiciet šādas darbības.

1. Dodieties uz **Sākums \> Vietnes**.
1. Atlasiet vietnes nosaukumu 
1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. Cilnē **Maršruti** zem **RNR konfidencialitāte un politika** atlasiet **Pievienot saiti**. Ja saite jau ir ievadīta un jūs vēlaties to aizstāt, atlasiet saiti. 
1. Dialoglodziņā **Pievienot saiti** atlasiet saiti konfidencialitātes un politikas lapai un pēc tam atlasiet **Labi**. 
1. Atlasiet **Saglabāt un publicēt**. 

Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.

![Saites konfigurēšana konfidencialitātes un politikas lapai](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Konfigurējiet vērtējumu un pārskata moduļus preces detalizētas informācijas lapās

Informāciju par vērtējumu un apskatu konfigurēšanu preču detalizētas informācijas lapā skatiet sadaļā [Vērtējumu un apskatu moduļi](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Konfigurējiet vērtējumu un pārskata moduļus preces detalizētas informācijas lapās](ratings-reviews-modules.md)

[Preču vērtējumu sinhronizācija Dynamics 365 Retail](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]