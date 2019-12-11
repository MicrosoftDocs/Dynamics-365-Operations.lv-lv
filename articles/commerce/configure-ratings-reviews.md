---
title: Vērtējumu un atsauksmju konfigurēšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770485"
---
# <a name="configure-ratings-and-reviews"></a>Vērtējumu un atsauksmju konfigurēšana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Vērtējumi un atsauksmes par E-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, parādot ko citi klienti domā par šīm precēm. E-komercijas tīmekļa vietnēm vērtējumi un atsauksmes ir arī mehānisms klientu atsauksmju apkopošanai par precēm. 

Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās. Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās (PDP). Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP) 

Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).

- Atsauksmes moduļa rakstīšana
- Preču atsauksmju saraksta modulis
- Vērtējumu histogrammas modulis
 
Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP)](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).

Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.

![Dialoglodziņš Moduļa pievienošana](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Atsauksmes rakstīšanas modulis

Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci. Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi. Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).

Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**. Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.

![Dialoglodziņš Rakstīt atsauksmi](media/rnr-eCommerce-write-review-module.png)

Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.

| Rekvizīta nosaukums | Vērtība        | Rekvizīta apraksts                 |
|---------------|--------------|--------------------------------------|
| Vārds/nosaukums          | Atsauksmes rakstīšana | Atsauksmes rakstīšanas moduļa nosaukums. |

### <a name="ratings-histogram-module"></a>Vērtējumu histogrammas modulis

Vērtējumu histogrammas modulis parāda vērtējumu histogrammu. Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).

Vērtējumu histogrammas modulim nav nepieciešama konfigurācija. Jums tikai jāpievieno modulis PDP veidnē. 

Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).

![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Preču atsauksmju saraksta modulis

Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām. Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).

Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.

| Rekvizīta nosaukums              | Vērtība | Rekvizīta apraksts |
|----------------------------|-------| ---------------------|
| Katrā lapā parādītās atsauksmes | 10.    | Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP). Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**. |

#### <a name="ratings-histogram--summary-view"></a>Vērtējumu histogramma — kopsavilkuma skats

Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli. Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai

Konfigurācijas vērtības vērtējumiem un atsauksmēm, piemēram, īrnieka ID, atsauksmes teksta garums un atsauksmes nosaukuma garums tiek konfigurēti vietnes līmenī. 

Lai konfigurētu vietni vērtējumu un atsauksmju rādīšanai, veiciet šīs darbības. 

1. Dodieties uz **Sākums \> Vietnes**.
1. Atlasiet vietnes nosaukumu 
1. Dodieties uz **Vietnes pārvaldība \>Paplašināmība**. 
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
1. Sadaļā **Iegādes lodziņš**atlasiet **Preču vērtējumi** un pēc tam atzīmējiet izvēles rūtiņu **Saistīt klikšķi ar pilnu atsauksmju moduli**.

Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.

![Preces vērtējuma saistīšana ar PDP sadaļu Atsauksmes](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Saites konfigurēšana konfidencialitātes un politikas lapai

Lai konfigurētu saiti konfidencialitātes un politikas lapai, veiciet šādas darbības.

1. Dodieties uz **Sākums \> Vietnes**.
1. Atlasiet vietnes nosaukumu 
1. Dodieties uz **Vietnes pārvaldība \>Paplašināmība**.
1. Cilnē **Maršruti** zem **RNR konfidencialitāte un politika** atlasiet **Pievienot saiti**. Ja saite jau ir ievadīta un jūs vēlaties to aizstāt, atlasiet saiti. 
1. Dialoglodziņā **Pievienot saiti** atlasiet saiti konfidencialitātes un politikas lapai un pēc tam atlasiet **Labi**. 
1. Atlasiet **Saglabāt un publicēt**. 

Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.

![Saites konfigurēšana konfidencialitātes un politikas lapai](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Preču vērtējumu sinhronizācija Dynamics 365 Retail](sync-product-ratings.md)
