---
title: Iespējojiet moderatora manuālo vērtējumu un atsauksmju publicēšanu
description: Šajā rakstā ir aprakstīts, kā ir iespējams manuāli publicēt novērtējumus un pārskatus, ko veic tajā regulētājs Microsoft Dynamics 365 Commerce, kā arī kā manuāli publicēt vērtējumus un pārskatus.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7d90cbbdc1ac0368c6ccfbeef7ff8db9b65679a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892627"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Iespējojiet moderatora manuālo vērtējumu un atsauksmju publicēšanu

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā ir iespējams manuāli publicēt novērtējumus un pārskatus, ko veic tajā regulētājs Microsoft Dynamics 365 Commerce, kā arī kā manuāli publicēt vērtējumus un pārskatus.

Dynamics 365 Commerce vērtējumu un atsauksmju risinājums izmanto Azure Cognitive Services, lai automātiski noņemtu vulgārus atsauksmju virsrakstus un saturus un publicētu vērtējumus un apskatus. Tāpēc nav vajadzīga manuāla iejaukšanās, lai pārskatītu un publicētu vērtējumus un atsauksmes jūsu e-komercijas vietnē.

Taču daži uzņēmumi varētu dot priekšroku moderatoriem, kuri manuāli pārskata un apstiprina atsauksmes pirms to publicēšanas. Lai iespējotu manuālu moderatora vērtējumu un atsauksmju publicēšanu, Commerce vietnes veidotājā ir jāiespējo līdzeklis **Vērtējumiem un atsauksmēm piešķirt moderatoru**.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Līdzekļa Vērtējumiem un atsauksmēm piešķirt moderatoru iespējošana Commerce vietnes veidotājā.

Lai Commerce vietnes veidotājā iespējotu līdzekli **Vērtējumiem un atsauksmēm piešķirt moderatoru**, izpildiet tālāk noradītās darbības.

1. Dodieties uz **Sākumlapa \> Atsauksmes \> Iestatījumi**.
1. Iestatiet opciju **Piešķirt vērtējumiem un atsauksmēm moderatoru** uz vērtību **Ieslēgta**.

> [!NOTE]
> Iespējojot līdzekli **Vērtējumiem un atsauksmēm piešķirt moderatoru**, tiek apturēta automātiska vērtējumu un atsauksmju publicēšana, tāpēc tagad ir vajadzīga manuāla publicēšana. Taču Azure Cognitive Services turpinās atsauksmju virsrakstos un saturā noņemt vulgāru valodu.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Vērtējumu un atsauksmju publicēšana

Iespējojot līdzekli **Vērtējumiem un atsauksmēm piešķirt moderatoru**, moderatoram ir manuāli jāpārskata un jāpublicē vērtējumi un atsauksmes, lai tās tiktu rādītas e-komercijas vietnē.

Lai pārskatītu un publicētu vērtējumus un atsauksmes Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Pārskati \> Moderācija**.
1. Režģī, ja rindas lauks **Statuss** ir iestatīts uz **Nepublicēta**, vērtējums un atsauksme Šajā laukā vēl nav publicēta. Lai skatītu tikai nepublicētus vērtējumus un atsauksmes, statusa filtrā virs režģa atlasiet **Statuss: Vajadzīgs pārskats**.
1. Atlasiet vienu vai vairākus vērtējumus ar statusu **Nepublicēts** un pēc tam komandjoslā atlasiet opciju **Publicēt**. Atlasītie vērtējumi un atsauksmes tiek pievienoti publicēšanas rindai un parādīsies e-komercijas vietnē pēc publicēšanas.

> [!NOTE]
> - Pēc tam, kad vērtējums un atsauksme ir publicēta, statusa vērtība tiek mainīta no **Nepublicēta** uz nulles vērtību (tukšs lauks).
> - Ja atlasāt vairākus vērtējumus un pārskatus ar jauktu statusu un pēc tam atlasāt **Publicēt**, vēl nepublicētie vērtējumi un atsauksmes tiks publicēti. Taču jau publicēti vērtējumi un atsauksmes netiks atkārtoti publicēti.

Šajā attēlā redzams piemērs, kurā trīs nepublicēti vērtējumi un atsauksmes tiek atlasīti Commerce vietnes veidotāja lapā **Moderācija**.

![Trīs nepublicēti vērtējumi un atsauksmes, kas atlasīti Commerce vietnes veidotāja lapā Moderācija.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija](sync-product-ratings.md)

[Novērtējumu un pārskatu importēšana un eksportēšana](import-export-reviews.md)

[Autentifikācijas starp pakalpojumiem konfigurēšana](service-to-service-auth.md)

[BUJ par vērtējumiem un atsauksmēm](ratings-reviews-faq.md)
