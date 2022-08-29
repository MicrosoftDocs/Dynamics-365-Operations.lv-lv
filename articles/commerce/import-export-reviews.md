---
title: Novērtējumu un pārskatu importēšana un eksportēšana
description: Šajā rakstā ir aprakstīts, kā importēt un eksportēt preču novērtējumus un pārskatus Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271940"
---
# <a name="import-and-export-ratings-and-reviews"></a>Novērtējumu un pārskatu importēšana un eksportēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā importēt un eksportēt preču novērtējumus un pārskatus Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce piedāvā [vērtējumus un pārskatus](ratings-reviews-overview.md) kā par channel risinājumu. Kad pārslēdzaties Dynamics 365 Commerce uz "novērtējumu un pārskatīšanas risinājumu", iespējams, vēlēsieties pārvietot esošos vērtējumus un pārskata datus uz Commerce platformu. Jūs, iespējams, vēlēsieties arī eksportēt novērtējumus un pārskata datus no Commerce, balstoties uz jūsu uzņēmējdarbības prasībām. Savienotājs Power Automate ļauj jums importēt vērtējumus un pārskatus par Commerce un eksportēt tos no Commerce.

> [!NOTE]
> Papildinformāciju par to, kā sākt darbu ar loģikas plūsmām Power Automate, skatiet sadaļā [Mākoņa plūsmas izveide Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms jūs varat importēt un eksportēt novērtējumus un pārskatus, jums ir jāizpilda šādi priekšnosacījumi:

- Vērtējumus un pārskatīšanas risinājumam jābūt iespējotam jūsu e-komercijas vietnei Commerce platformā. Papildinformāciju skatiet sadaļā [Pieteikšanās vērtējumu un pārskatīšanas lietošanai](opt-in-ratings-reviews.md).
- Dynamics 365 novērtējumi un pārskati Power App Connector ir jākonfigurē, lai iespējotu darbības "iesniegt pārskatus" vai "eksporta pārskati"Power Automate. Papildinformāciju skatiet – [Dynamics 365 Commerce vērtējumi un pārskati (priekšskatījums](/connectors/dynamics365ratingsre/)).
- Pakalpojuma -pakalpojuma (S2S) autentifikācija ir jākonfigurē, lai droši izsauktu novērtējumus un pārskata programmas programmēšanas interfeisu (API) no ārpus Commerce. Papildinformāciju skatiet sadaļā [Pakalpojuma-pakalpojuma autentifikācijas konfigurēšana](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Importēt vērtējumus un pārskatus

Lai importētu novērtējumus un pārskatītu datus no esošās sistēmas sistēmā Commerce, jums ir jāpievieno Dynamics 365 novērtējumi un pārskatīšanas savienotājs Power Automate Power Automate esošajai plūsmai vai jaunai. Papildinformāciju skatiet – [Dynamics 365 Commerce vērtējumi un pārskati (priekšskatījums](/connectors/dynamics365ratingsre/)).

> [!IMPORTANT]
> Pirms šīs procedūras pabeigšanas jākonfigurē [S2S autentifikācija](service-to-service-auth.md).

Lai importētu vērtējumus un pārskatus Commerce, izmantojot Dynamics 365 vērtējumus un pārskata savienotāju Power Automate, rīkojieties šādi.

1. Atlasiet darbību **Iesniegt lietotāja** pārskatu.
1. Izveidojiet savienojumu, izmantojot Azure Active Directory (Azure AD) programmas informāciju, kas tika izveidota, konfigurējot S2S autentifikāciju. Papildinformāciju skatiet sadaļā [Pakalpojuma-pakalpojuma autentifikācijas konfigurēšana](service-to-service-auth.md).
1. Darbība **Iesniegt lietotāja pārskatu** pa vienam pārskatam. Tādēļ atkārtojiet šo darbību. Izmantojiet avota pārskatus kā sarakstu, lai iesniegtu lielapjoma pārskatus.
    
## <a name="export-ratings-and-reviews"></a>Eksportēt novērtējumus un pārskatus

Lai eksportētu vērtējumus un pārskatītu datus no Commerce, jums ir jāpievieno Dynamics 365 vērtējumi un pārskatīšanas savienotājs Power Automate Power Automate esošai plūsmai vai jaunai. Papildinformāciju skatiet – [Dynamics 365 Commerce vērtējumi un pārskati (priekšskatījums](/connectors/dynamics365ratingsre/)).

Lai eksportētu vērtējumus un pārskatus no Commerce, izmantojot Dynamics 365 novērtējumu un pārskata savienotāju Power Automate, rīkojieties šādi.

1. Izvēlieties Eksporta **visu pārskata** darbību.
1. Pabeidziet darbību. 

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija](sync-product-ratings.md)

[Iespējojiet moderatora manuālo vērtējumu un atsauksmju publicēšanu](manual-publish-rating-reviews.md)

[Autentifikācijas starp pakalpojumiem konfigurēšana](service-to-service-auth.md)

[BUJ par vērtējumiem un atsauksmēm](ratings-reviews-faq.md)
