---
title: Displeja iestatījumu pielietošana preču dimensijām
description: Šajā tēmā ir aplūkoti preču dimensiju displeja iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d6854c11822e07ff06426b7a35eac86cdc0e9b06
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356906"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Displeja iestatījumu pielietošana preču dimensijām

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aplūkoti preču dimensiju displeja iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce atbalsta izmēru, stilu un krāsu izmērus, lai atšķirtu preces variantus. Dimensijas parasti tiek rādītas kā teksta vērtības, piemēram, "Mazs", "Vidējs" un "Liels" izmēriem un "Melns" un "Brūns" krāsām. Tomēr, ja prece atbalsta daudzas variācijas, var būt grūti pārlūkot preces variantus, jo, lai skatītu attēlu katram variantam, ir nepieciešamas vairākas atlases. Lai atvieglotu preces variantu pārlūkošanu, Commerce versijas 10.0.20 laidienā var izmantot attēlus un heksadecimālos kodus, lai dimensijas parādītu kā paraugus.

Commerce vietnes veidotājā dimensiju iestatījumi tiek definēti **Vietas iestatījumi \> Paplašinājumi \> Dimensiju iestatījumi**. Nākamajā attēlā ir parādīts dimensiju iestatījumu piemērs vietņu veidotājā.

![Vietnes iestatījumu piemērs Commerce vietnes veidotājā.](./dev-itpro/media/swatch_site_settings.PNG)

Ir pieejami divi dimensiju iestatījumi:

- **Dimensijas, kas jārāda kā attēls** - norādiet, kurām dimensijām jāparādās e-komercijas vietņu lapās, piemēram, preču informācijas lapās (PDP) un meklēšanas rezultātu saraksta lapās. Jebkuru krāsu, izmēru un stila dimensiju kombināciju var parādīt kā paraugu. Ja dimensija ir atlasīta parādīšanai kā paraugs, Commerce moduļa renderēšana meklēs pieejamu heksadecimālo koda parauga konfigurāciju. Ja heksadecimālais kods nav konfigurēts, sistēmas loģika meklēs attēla URL parauga konfigurāciju. Ja nav konfigurēts ne heksadecimālais kods, ne attēla URL, tiks parādīts teksts.

    Nākamajā attēlā ir parādīts piemērs, kur e-komercijas vietnes PDP ietver krāsu un izmēru paraugus. Šajā piemērā krāsu dimensijai ir konfigurēts heksadecimālais kods. Tāpēc paraugi tiek parādīti kā krāsas. Tomēr izmēra dimensijai nav konfigurēts ne heksadecimālais kods, ne attēla URL. Tāpēc tiek parādīts teksts.

    ![Piemērs krāsu dimensijai, kas e-komercijas preču informācijas lapā tiek rādīti kā paraugi.](./dev-itpro/media/swatch_pdp.png)

- **Preču kartē rādāmās dimensijas** — norādiet, kurām dimensijām jāparādās produktu kartēs, kas tiek rādītas sarakstos un saraksta lapās. Lai dimensija varētu parādīties preču kartē, šai dimensijai ir jāiespējo šis iestatījums. Ir jāiespējo arī iestatījums **Dimensijas, lai parādītu kā attēlu**. Paraugu atlases darbība preču kartēs ir optimizēta krāsu dimensijai. Citām dimensijām var būt nepieciešams skata paplašinājums, lai pielāgotu parauga atlases darbību.

    Nākamajā attēlā ir parādīts piemērs, kur e-komercijas vietnes saraksta lapā ir preču kartes, kurās ir krāsu paraugi.

    ![Piemērs krāsu dimensijai, kas e-komercijas saraksta lapā tiek rādīti kā paraugi.](./dev-itpro/media/swatch_searchresults.PNG)

Informāciju par to, kā konfigurēt preču dimensijas tā, lai tās vietnes lapās tiktu rādītas kā paraugi, skatiet [Konfigurēt preču dimensiju vērtības, lai tās tiktu rādītas kā paraugi](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Meklēšanas rezultātu modulis](search-result-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Konfigurēt preču dimensiju vērtības, lai tās tiktu rādītas kā paraugi](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
