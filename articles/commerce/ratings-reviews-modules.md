---
title: Vērtējumu un apskatu moduļi
description: Šajā rakstā ir ietverti vērtējumi un pārskatīšanas moduļi, kas tiek izmantoti preces informācijas lapās Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ede42caac78dc48fa6315a2d3c22f1e0f12f0810
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283592"
---
# <a name="ratings-and-reviews-modules"></a>Vērtējumu un apskatu moduļi

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti vērtējumi un pārskatīšanas moduļi, kas tiek izmantoti preces informācijas lapās (PPS)Microsoft Dynamics 365 Commerce.

Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, kā arī tas ir mehānisms, ka iegūt klientu atsauksmes par precēm. 

Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās. 

Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās. Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci. Šos PDP līdzekļus kontrolē vērtējumu un apskatu moduļi.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP) 

Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).
- Atsauksmes moduļa rakstīšana
- Preču atsauksmju saraksta modulis
- Vērtējumu histogrammas modulis
 
Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP).](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).

Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.
![Dialoglodziņš Moduļa pievienošana.](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Atsauksmes moduļa rakstīšana

Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci. Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi. Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).
Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**. Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.

![Dialoglodziņš Rakstīt atsauksmi.](media/rnr-eCommerce-write-review-module.png)

Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.

| Rekvizīta nosaukums | Vērtība        | Rekvizīta apraksts                 |
|---------------|--------------|--------------------------------------|
| Vārds/nosaukums          | Atsauksmes rakstīšana | Atsauksmes rakstīšanas moduļa nosaukums. |

### <a name="ratings-histogram-module"></a>Vērtējumu histogrammas modulis

Vērtējumu histogrammas modulis parāda vērtējumu histogrammu. Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).
Vērtējumu histogrammas modulim nav nepieciešama konfigurācija. Jums tikai jāpievieno modulis PDP veidnē. Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).
![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Preču atsauksmju saraksta modulis

Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām. Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).
Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.

| Rekvizīta nosaukums              | Vērtība | Rekvizīta apraksts |
|----------------------------|-------| ---------------------|
| Katrā lapā parādītās atsauksmes | 10.    | Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP). Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**. |

#### <a name="ratings-histogram--summary-view"></a>Vērtējumu histogramma — kopsavilkuma skats

Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli. Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī.](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
