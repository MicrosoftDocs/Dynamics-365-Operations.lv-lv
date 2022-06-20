---
title: Lietotāju un lomu pārvaldība e-tirdzniecībā
description: Šajā rakstā skaidrots, kā piešķirt lietotājiem piekļuvi jūsu vietnes autorizēšanas videi Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ac4342e4439db229997d9d4a0ad32f3664a795b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868965"
---
# <a name="manage-e-commerce-users-and-roles"></a>Lietotāju un lomu pārvaldība e-tirdzniecībā


[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā piešķirt lietotājiem piekļuvi jūsu vietnes autorizēšanas videi Microsoft Dynamics 365 Commerce.

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

Kad jūs Commerce izveidojat jaunu vietni, jums tiek lūgts nodrošināt drošības grupu lomai **Administrators**. Skatiet iepriekš šajā rakstā tabulu, lai iegūtu pārskatu par šīs lomas dotajām atļaujām.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]