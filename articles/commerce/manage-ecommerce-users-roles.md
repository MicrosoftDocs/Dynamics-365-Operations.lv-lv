---
title: Lietotāju un lomu pārvaldība e-tirdzniecībā
description: Šajā tēmā izskaidrots, kā piešķirt lietotājiem piekļuvi Microsoft Dynamics 365 Commerce vietnes autorēšanas videi.
author: bicyclingfool
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
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003537"
---
# <a name="manage-e-commerce-users-and-roles"></a>Lietotāju un lomu pārvaldība e-tirdzniecībā


[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā piešķirt lietotājiem piekļuvi Microsoft Dynamics 365 Commerce vietnes autorēšanas videi.

Lai palīdzētu kontrolēt lietotāju piekļuvi un piešķirtu lietotājiem atļaujas veikt noteiktus uzdevumus, vietnes autorēšanas vide izmanto drošības grupas, ko izveidojat Microsoft Azure Active Directory (Azure AD). Vispirms no Azure AD piešķiriet jaunu vai esošu drošības grupu katrai lomai autorēšanas vidē. Pēc tam piešķiriet vai atsauciet atļaujas atsevišķiem lietotājiem, vai nu pievienojot šos lietotājus atbilstošai drošības grupai, vai noņemot tos no drošības grupas.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Lomu pārskats autorēšanas vidē

Dynamics 365 for Commerce autorēšanas vide atbalsta tālāk minētās lomas.

| Loma                 | Apraksts |
|----------------------|-------------|
| Sistēmas administrators | Lietotājiem, kuriem ir šī loma, ir visas privilēģijas visiem rīkiem, vērtējumiem un apskatiem. Viņi var arī izveidot vietnes. |
| Administrators   | Lietotājiem, kuriem ir šī loma, ir visas privilēģijas visiem rīkiem un RnR noteiktā vietnes struktūrā. |
| Tīmekļa producents         | Lietotāji, kuriem ir šī loma, var izveidot lapas, fragmentus un veidnes, augšupielādēt un pārvaldīt līdzekļus un papildināt preces un kategorijas. |
| Lasītājs               | Lietotāji, kuriem ir šī loma, var skatīt lapas, veidnes, līdzekļus, fragmentus, izkārtojumus un iestatījumus, bet nevar veikt izmaiņas. |
| RnR moderators        | Lietotāji, kuriem ir šī loma, var moderēt preču apskatus. |

## <a name="system-administrator-role"></a>Sistēmas administratora loma

Kad jūs nodrošināt Dynamics 365 Commerce Microsoft Dynamics Lifecycle Services (LCS) vidē, jums tiek lūgts norādīt drošības grupu lomai **Sistēmas administrators**. Šī loma tiek automātiski piemērota visām vietnēm, ko izveidojat jūsu konfigurētajā vidē. Šīs lomas drošības grupu var atjaunināt tikai LCS. Visu vietņu lapā **Vietnes administrēšana** tas parādās kā tikai lasāms un paredzēts tikai informatīviem nolūkiem.

## <a name="administrator-role"></a>Administratora loma

Kad jūs Commerce izveidojat jaunu vietni, jums tiek lūgts nodrošināt drošības grupu lomai **Administrators**. Skatīt šajā tēmā iepriekš minēto tabulu, lai apskatītu šai lomai piešķirtās atļaujas.

## <a name="add-or-update-security-groups"></a>Drošības grupu pievienošana vai atjaunināšana

Pēc vietnes izveides tikai tie lietotāji, kuri ir drošības grupās, kas saistītas ar lomām **Sistēmas administrators** un **Administrators**, var piekļūt šīs vietnes autorēšanas videi. Lai piešķirtu lietotājiem lomas **Tīmekļa producents**, **RnR moderators** un **Lasītājs**, šīm lomām ir jāpiešķir drošības grupas. Lai lomai pievienotu drošības grupu vai atjauninātu drošības grupu, kas pašlaik ir piešķirta lomai, veiciet tālāk minētās darbības.

1. Dodieties uz vietni, ko vēlaties atjaunināt.
1. **Vietnes vadība** atveriet lapu **Drošība**.
1. Atlasiet lomu, ko paredzēts modificēt.
1. Pievienojiet vai noņemiet lomām drošības grupas.

## <a name="additional-resources"></a>Papildu resursi

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

[Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei](search-engine-optimization-considerations.md)

[Satura drošības politikas (CSP) pārvaldība](manage-csp.md)
