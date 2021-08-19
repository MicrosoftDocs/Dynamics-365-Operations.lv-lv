---
title: Preču vērtējumu sinhronizācija pakalpojumā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīts, kā sinhronizēt preču vērtējumus risinājumā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f2112c87912a1d130017c5804c4193b62c1e5a476be79bfd485640ec98b42f77
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730903"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Preču vērtējumu sinhronizācija pakalpojumā Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā sinhronizēt preču vērtējumus risinājumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Lai izmantotu preču vērtējumus vairākos kanālos, piemēram, pārdošanas punktā (POS) un zvanu centros, preču novērtējumi no vērtējumu un pārskatu pakalpojuma ir jāimportē Commerce kanāla datu bāzē. Kad preču vērtējumi ir pieejami vairākos kanālos, tie var netieši palīdzēt klientiem to mijiedarbības laikā ar pārdošanas partneriem.

Šajā tēmā ir aprakstīti tālāk norādītie uzdevumi.

1. Konfigurējiet **Preču vērtēšanas sinhronizācijas darbu** kā pakešuzdevumu, lai sinhronizētu preču novērtējumus no **Vērtējumu un apskatu pakalpojuma**.
1. Pārbaudīt, vai pakešuzdevumu preču vērtējuma sinhronizēšana bija veiksmīga.
1. Padarīt preces vērtējumus pieejamus POS.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Konfigurēt mazumtirdzniecības pakešuzdevumu, lai sinhronizētu preču vērtējumus.

> [!IMPORTANT]
> Pirms sākat, pārliecinieties, ka ir instalēta Dynamics 365 Commerce versija 10.0.6 vai jaunāka.

### <a name="initialize-the-commerce-scheduler"></a>Komercijas plānotāja inicializēšana

Lai inicializētu komercijas plānotāju, rīkojieties šādi.

1. Dodieties uz **Retail un Commerce \> Headquarters uzstādīšanas programmas \> Commerce plānotājs \> Inicializēt komercijas plānotāju**. Varat arī meklēt “inicializēt komercijas plānotāju”.
1. Dialoglodziņā **Inicializēt komercijas plānotāju** pārliecinieties, vai opcija **Dzēst esošo konfigurāciju** ir iestatīta uz **Nē** un pēc tam atlasiet **Labi**.

### <a name="verify-the-retailproductrating-subjob"></a>Pārbaudīt RetailProductRating apakšdarbu

Lai pārbaudītu, vai **RetailProductRating** apakšdarbs pastāv, rīkojieties, kā norādīts tālāk.

1. Dodieties uz **Retail un Commerce \> Headquarters uzstādīšanas programmas \> Commerce plānotājs \> Plānotāja apakšdarbi**. Vai arī meklējiet “plānotāja apakšdarbi”.
1. Apakšdarbu sarakstā atrodiet vai meklējiet **RetailProductRating** apakšdarbu.

Tālāk redzamajā attēlā ir parādīts Commerce apakšdarba detalizētas informācijas piemērs.

![Detalizēta informācija par RetailProductRating apakšdarbu.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Ja neatrodat **RetailProductRating** apakšdarbu, iespējams, jau esat palaidis darbu **Sinhronizēt preču vērtējumus** darbu un darbu **1040 CDX** pirms Commerce plānotāja inicializēšanas. Šādā gadījumā veiciet šīs darbības, lai palaistu darbu **Pilnīga datu sinhronizācija**.

> 1. Dodieties uz **Retail un Commerce \> Headquarters uzstādīšanas programmas \> Commerce plānotājs \> Kanāla datubāze**. Vai arī meklējiet “kanāla datubāze”.
> 1. Atlasiet sinhronizējamo kanāla datubāzi.
> 1. Darbību rūtī atlasiet **Pilnīga datu sinhronizācija**.
> 1. Dialoglodziņa nolaižamajā sarakstā **Atlasīt sadales grafiki** atlasiet **1040 — preces** un pēc tam atlasiet **Labi**.
> 1. Atkārtojiet iepriekšējās procedūras darbības, lai pārbaudītu, vai **RetailProductRating** apakšdarbs ir izveidots.

### <a name="import-product-ratings"></a>Preču vērtējumu importēšana

Lai importētu preču vērtējumus Commerce no vērtējumu un pārskatu pakalpojuma, rīkojieties, kā aprakstīts tālāk.

1. Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Commerce plānotājs \> Sinhronizēt preces vērtējuma darbu**. Varat arī meklēt “Sinhronizēt preces vērtējuma darbu”.
1. Dialoglodziņā **Izvilkt preces vērtējumus**, kas atrodas kopsavilkuma cilnē **Palaist fonā**, atlasiet **Periodiskums**.
1. Dialoglodziņā **Definēt periodiskumu** iestatiet periodiskuma modeli. (Ieteicamā vērtība ir divas stundas.) Neplānojiet periodiskumu, kas ir mazāks par vienu stundu.
1. Atlasiet **Labi**.
1. Iestatiet opciju **Pakešveida apstrāde** uz **Jā**. Šis iestatījums palīdz garantēt, ka jūs varēsiet pārbaudīt žurnālus un pārbaudīt pakešuzdevuma statusu.
1. Atlasiet **Labi**, lai ieplānotu pakešuzdevumu.

Tālāk redzamajā attēlā ir parādīta pakešuzdevuma konfigurācija programmā Commerce.

![Pakešuzdevumu preču vērtējuma sinhronizēšanas konfigurācija.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Pārbaudīt, vai pakešuzdevumu preču vērtējuma sinhronizēšana bija veiksmīga

Lai pārbaudītu, vai pakešuzdevums **Sinhronizēt preces vērtējumu** bija veiksmīgs, veiciet šādas darbības.

1. Dodieties uz **Retail un commerce \> Sistēmas administrators \> Uzziņas \> Pakešuzdevumi** vai, ja izmantojat tikai Commerce noliktavas vienību (SKU), **Retail un Commerce \> Uzziņas un pārskati \> Pakešuzdevumi**. Vai arī meklējiet “Pakešuzdevumi”.
1. Lai skatītu detalizētu informāciju par pakešuzdevumu, pakešuzdevumu sarakstā, kolonnā **Darba apraksts** meklējiet aprakstu, kas satur “Izvilkt preces vērtējumus”.
1. Atlasiet darba ID, lai skatītu detalizētu informāciju par pakešuzdevumu, piemēram, plānoto sākuma datumu/laiku un periodiskuma tekstu.

Tālāk esošajā attēlā parādīts piemērs ar pakešuzdevuma detalizētu informāciju programmā Commerce, kad pakešuzdevums tiek plānots izpildei divu stundu intervālos.

![.Pakešuzdevumu preču vērtējuma sinhronizēšanas detalizēta informācija.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Padarīt preces vērtējumus pieejamus POS

Vērtējumu un pārskatu risinājums Dynamics 365 Commerce ir vairāku kanālu risinājums. Tomēr preču vērtējumi pēc noklusējuma netiek parādīti POS. Lai palīdzētu klientiem veikalos skatīt vērtējumus un pārskatus, kad viņiem palīdz pārdošanas partneri, jums ir jāieslēdz preču vērtējumi POS.

Lai ieslēgtu preču vērtējumus POS, veiciet tālāk minētās darbības.

1. Pārejiet uz sadaļu **Retail un Commerce \> Commerce iestatīšana \> Parametri \> Komercijas parametri**. Varat arī meklēt “Commerce parametri”.
1. Cilnē **Konfigurācijas parametri** atlasiet **Jauns**.
1. Ievadiet nosaukumu, piemēram, **RatingsAndReviews.EnableProductRatingsForRetailStores**, un iestatiet vērtību uz **Patiess**.
1. Atlasiet **Saglabāt**.
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**. Vai arī meklējiet “Sadales grafiks”.
1. Darbu sarakstā atlasiet **1110** (**Globālā konfigurācija**) un pēc tam atlasiet **Palaist tūlīt**.
1. Pēc tam, kad darbs ir veiksmīgi palaists, pārbaudiet, vai preču vērtējumi tagad ir redzami POS.

Tālāk esošajā attēlā parādīts piemērs par Commerce parametru konfigurāciju, lai POS sistēmā ieslēgtu preces vērtējumus.

![Commerce parametru konfigurācija preču vērtējumiem POS sistēmā.](media/rnr-hq-enable-ratings-in-pos.png)

Nākamajā attēlā ir parādīts piemērs ar preces vērtējumiem POS sistēmā.

![Preču vērtējumi POS sistēmā.](media/rnr-pos-catalog-ratings.png)

Nākamajā attēlā ir parādīts piemērs ar preces vērtējumiem zvanu centra kanālos.

![Preču vērtējumi zvanu centra kanālā.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]