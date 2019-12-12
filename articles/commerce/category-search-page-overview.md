---
title: Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats
description: Šajā tēmā ir sniegts pārskats par noklusējuma kategorijas ielādes lapu un meklēšanas rezultātu lapu programmā Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/31/2019
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3835502c33fbc63f68f2d6350d805badb3891568
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697294"
---
# <a name="overview-of-default-category-landing-page-and-search-results-page"></a>Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegts pārskats par noklusējuma kategorijas ielādes lapu un meklēšanas rezultātu lapu programmā Microsoft Dynamics 365 Commerce E-komercija.

## <a name="default-category-landing-page"></a>Noklusējuma kategorijas ielādes lapa

Noklusējuma kategorijas ielādes lapa ir lapa, uz kuru parasti tiek novirzīti vietnes lietotāji, kad viņi atlasa kategoriju navigācijas hierarhijā. Kategorijas lapa ļauj jums pārlūkot, un jūs varat arī kārtot un attīrīt kategorizētās preces.

![Noklusējuma kategorijas ielādes lapa](./media/SimpleCategoryLandingDressCategory.png)

Lapas augšdaļā ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kurām ir kategorizēts tirdzniecības vadītājs. Konfigurācija tiek veikta kā kanāla navigācijas hierarhijas konfigurācijas sastāvdaļa. Lapas apakšdaļā ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircēju.

Kategorijai ir svarīgi šādi komponenti.

- **Preču izvietošanas elementi** parāda preces, ko tirdzniecības vadītājs ir definējis kategorijā kā navigācijas hierarhijas konfigurācijas sastāvdaļu.
- **Rafinētāji un izvēles kopsavilkums** ir filtri, kas sniedz uzskaitījumu un ko var izmantot krājumu precizēšanai. Tirdzniecības vadītājs tos konfigurē kā daļu no metadatu konfigurācijas, kas ir saistīti ar kanāla kategorijām un preču atribūtiem.
- **Kārtošanas opcijas** izmanto vietņu apmeklētāji, lai šķirotu preces. Pēc noklusējuma ir pieejamas šādas kārtošanas opcijas.

    - Cena – no zemas līdz augstai
    - Cena – no zemas līdz augstai
    - Preces nosaukums – \[A-Z\]
    - Preces nosaukums – \[A-Z\]
    - Vērtējumi – no zema līdz augstam
    - Vērtējumi – no zema līdz augstam

- **Lappušu numerācija** ļauj vietnes apmeklētājiem pāriet no vienas lapas ar kategorizētā produkta rezultātiem uz citu lapu.
- **Kopējais skaits** nodrošina kopējo preču skaitu, kas definēts kategorijā.

## <a name="enrich-a-category-landing-page"></a>Kategorijas ielādes lapas papildināšana

Ja vēlaties, lai kategorijas ielādes lapai būtu vairāk pielāgota pieredze noteiktai kategorijai, varat “bagātināt” kategorijas ielādes lapu šai kategorijai. Piemēram, varat pievienot mārketinga video un dažas kategorijas stāstījumus, lai piesaistītu pircēju uzmanību. Plašāku informāciju skatiet tēmā [Kategorijas ielādes lapas bagātināšana](enrich-category-page.md).

![Bagātināta kategorijas ielādes lapa](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automātiskās piedāvāšanas un meklēšanas rezultātu lapas

Vietnes lietotāji var apskatīt vietni, atverot kategoriju no navigācijas hierarhijas vai meklēšanas laukā ievadot meklējamo terminu.

Tiklīdz lietotāji sāk ievadīt vārdus meklēšanas laukā, viņiem tiek sniegta visaptveroša automātiskās piedāvāšanas funkcionalitāte, kas piedāvā meklēšanas terminus.

Piedāvājam dažus piedāvājumu tipus, kas var tikt rādīti.

- **Atslēgvārdi** tiek izmantoti, lai atrastu elementus visās precēs, kas ir pievienotas kanālam.
- **Preces** sniedz tiešas saites uz preču informācijas lapu.
- **Atlasītie kategorijas meklēšanas ieteikumi** uzskaita dažādas kategorijas un ļauj lietotājiem meklēt atslēgvārdu noteiktā kategorijā.

![Visaptveroša automātiskā piedāvāšana](./media/ImmersiveAutoSuggestUX.png)

Kad lietotāji atlasa vienu no atslēgvārdiem vai atlasītajiem kategoriju meklēšanas ieteikumiem, vai ja nav ieteikumu meklētajam terminam, kas tiek ievadīts, viņi tiek novirzīti uz meklēšanas rezultātu lapu. Pēc tam lietotāji var pārlūkot, kārtot un precizēt meklēšanas rezultātu sarakstu, lai atrastu vēlamo elementu.

![Meklēšanas ielāde](./media/SearchLanding.png)

Meklēšanas rezultātu lapai ir svarīgi šādi komponenti.

- **Preču izvietošanas elementi** parāda preces lietotāja meklēšanai. Pēc noklusējuma šie elementi tiek kārtoti pēc mākoņa darbinātā meklēšanas atbilstības rādītāja lietotāja meklēšanai.
- **Rafinētāji un izvēles kopsavilkums** ir filtri, kas sniedz uzskaitījumu un ko var izmantot krājumu precizēšanai. Tirdzniecības vadītājs tos konfigurē kā metadatu “kanāla kategorijas un preču atribūti” konfigurācijas daļu.
- **Kārtošanas opcijas** izmanto vietņu apmeklētāji, lai šķirotu preces. Pēc noklusējuma ir pieejamas šādas kārtošanas opcijas.

    - Cena – no zemas līdz augstai
    - Cena – no zemas līdz augstai
    - Preces nosaukums – \[A-Z\]
    - Preces nosaukums – \[A-Z\]
    - Vērtējumi – no zema līdz augstam
    - Vērtējumi – no zema līdz augstam
    - Noklusējuma vērtība

- **Lappušu numerācija** ļauj vietnes apmeklētājiem pāriet no vienas lapas ar kategorizētā produkta rezultātiem uz citu lapu.
- **Kopējais skaits** nodrošina kopējo preču skaitu, kas definēts kategorijā un kas atbilst meklēšanas kritērijiem.

## <a name="additional-resources"></a>Papildu resursi

[Sākumlapas pārskats](quick-tour-home-page.md)

[Preču papildinformācijas lapu apskats](quick-tour-pdp.md)

[Pārskats par grozu un norēķināšanās lapām](quick-tour-cart-checkout.md)

[Pārskats par konta pārvaldības lapām](quick-tour-account-management.md)
