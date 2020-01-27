---
title: Commerce priekšskatījuma vides konfigurēšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce priekšskatījuma vidi, kad tā ir nodrošināta.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906143"
---
# <a name="configure-a-commerce-preview-environment"></a>Commerce priekšskatījuma vides konfigurēšana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce priekšskatījuma vidi, kad tā ir nodrošināta.

## <a name="overview"></a>Pārskats

Šajā tēmā minētās procedūras veiciet tikai pēc tam, kad ir nodrošināta Commerce priekšskatījuma vide. Informāciju par to, kā nodrošināt Commerce priekšskatījuma vidi, skatiet [Commerce priekšskatījuma vides nodrošināšana](provisioning-guide.md).

Pēc tam, kad jūsu Commerce priekšskatījuma vide ir pilnībā nodrošināta, ir jāpabeidz papildu konfigurēšanas darbības pēc nodrošināšanas, pirms varat sākt novērtēt vidi. Lai veiktu šīs darbības, ir jāizmanto Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce un Dynamics 365 Retail

## <a name="before-you-start"></a>Pirms darba sākšanas

1. Pierakstieties [LCS portālā](https://lcs.dynamics.com).
1. Dodieties uz savu projektu.
1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijas labajā pusē atlasiet **Visa informācija**.
1. Lai atvērtu izvēlni, atlasiet **Pieteikties**, pēc tam atlasiet **Pieteikties vidē**.
1. Pārliecinieties, ka ir atlasīta **USRT** juridiskā persona (augšējā labajā stūrī).

## <a name="configure-the-point-of-sale-in-lcs"></a>Konfigurējiet pārdošanas punktu LCS

### <a name="associate-a-worker-with-your-identity"></a>Nodarbinātā saistīšana ar jūsu identitāti

Lai saistītu darbinieku ar jūsu identitāti LCS, rīkojieties šādi.

1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība \> Darbinieki \> Nodarbinātie**.
1. Sarakstā atrodiet un atlasiet šādu ierakstu **000713 – Endrjū Kollete**.
1. Darbību rūtī atlasiet **Mazumtirdzniecība**.
1. Atlasiet **Piesaistīt esošu identitāti**.
1. Laukā **E-pasts** (pa labi no **Meklēt, izmantojot e-pastu**) ievadiet savu e-pasta adresi.
1. Atlasiet **Meklēt**.
1. Atlasiet ierakstu ar savu vārdu.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt**.

### <a name="activate-cloud-pos"></a>mākoņa POS aktivizēšana;

Lai aktivizētu mākoņa POS LCS, rīkojieties šādi.

1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijas labajā pusē atlasiet **Visa informācija**.
1. Atlasiet **Pieteikšanās**, lai atvērtu izvēlni, un pēc tam atlasiet **Pieteikties mākoņa pārdošanas punktam**, lai atvērtu pārdošanas punktu (POS).
1. Atlasiet **Nākamais**.
1. Piesakieties, izmantojot savu Microsoft Azure Active Directory (Azure AD) kontu.
1. Sadaļā **Veikala nosaukums** atlasiet **Sanfrancisko**.
1. Atlasiet **Nākamais**.
1. Sadaļā **Reģistrs un ierīce** atlasiet **SANFRAN-1**.
1. Atlasiet **Aktivizēt**. Jūs esat izrakstījies un aizvirzīts uz POS pierakstīšanās lapu.
1. Tagad varat pieteikties mākoņa POS pieredzei, izmantojot operatora ID **000713** un paroli **123**.

## <a name="set-up-your-site-in-commerce"></a>Iestatiet savu vietni pakalpojumā Commerce.

Lai sāktu iestatīt priekšskatījuma vietni pakalpojumā Commerce, veiciet tālāk norādītās darbības.

1. Piesakieties vietnes pārvaldības rīkā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-Commerce (skatiet [e-Commerce inicializēšana](provisioning-guide.md#initialize-e-commerce)).
1. Atlasiet vietni **Fabrikam**, lai atvērtu vietnes iestatīšanas dialoglodziņu.
1. Atlasiet domēnu, kuru ievadījāt, kad inicializējat e-Commerce.
1. Kā noklusējuma kanālu atlasiet **Fabrikam paplašinātais tiešsaistes veikals**. (Pārliecinieties, ka atlasāt **paplašināto** tiešsaistes veikalu.)
1. Ka noklusējuma valodu atlasiet **en-us**.
1. Atstājiet lauka **Path** vērtību tādu, kāda tā ir.
1. Atlasiet **Labi**. Tiek parādīts vietnes lapu saraksts.

## <a name="enable-jobs-in-retail"></a>Iespējot darbvietas mazumtirdzniecībā

Lai iespējotu darbus mazumtirdzniecībā, izpildiet tālāk aprakstītās darbības.

1. Pierakstieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Mazumtirdzniecība \> Pieprasījumi un pārskati \> Pakešuzdevumi**.

    Šīs procedūras atlikušie soļi jāaizpilda katram no šiem darbiem:

    * Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojumu
    * Preču pieejamība
    * P-0001
    * Darbs Sinhronizēt pasūtījumus

1. Izmantojiet ātro filtru, lai meklētu darbu pēc nosaukuma.
1. Ja darba statuss ir **Aizturēts**, veiciet tālāk minētās darbības.

    1. Atlasiet ierakstu.
    1. Darbību rūtī noklikšķiniet uz cilnes **Pakešuzdevums**, pēc tam atlasiet **Mainīt statusu**.
    1. Atlasiet **Gaida** un pēc tam atlasiet **Labi**.

### <a name="run-full-data-synchronization-in-retail"></a>Veikt pilnu datu sinhronizāciju mazumtirdzniecībā

Lai mazumtirdzniecībā palaistu pilnu datu sinhronizāciju, veiciet tālāk norādītās darbības.

1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība \> Mazumtirdzniecības uzstādīšana \> Mazumtirdzniecības plānotājs \> Kanāla datubāze**.
1. Kanāls **Noklusējums** ir atlasīts no saraksta kreisajā pusē. Izvēlieties citu pieejamo kanālu. Šī kanāla nosaukums **scXXXXXXXXX**.
1. Darbību rūtī atlasiet **Pilnīga datu sinhronizācija**.
1. Ievadiet **9999** kā sadales grafiku.
1. Atlasiet **Labi**.
1. Atlasiet **Labi**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Kredītkartes informācijas pārbaude, lai veiktu pārbaudes pirkumus

Lai vietnē veiktu pārbaudes transakcijas, varat izmantot tālāk minēto pārbaudes kredītkartes informāciju.

- **Kartes numurs:** 4111-1111-1111-1111
- **Beigu datums:** 10/20
- **Kartes verificēšanas vērtības (CVV) kods:** 737

> [!IMPORTANT]
> Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju.

## <a name="next-steps"></a>Nākamās darbības

Kad nodrošināšanas un konfigurēšanas darbības ir pabeigtas, varat novērtēt priekšskatījuma vidi. Izmantojiet Commerce vietnes pārvaldības rīka URL, lai dotos uz autorēšanas pieredzi. Izmantojiet Commerce vietnes pārvaldības rīka URL, lai dotos uz mazumtirdzniecības klienta vietnes pieredzi.

Lai konfigurētu neobligātos līdzekļus savai Commerce priekšskatījuma videi, skatiet [Commerce priekšskatījuma vides neobligāto līdzekļu konfigurēšana](cpe-optional-features.md).

## <a name="additional-resources"></a>Papildu resursi

[Commerce priekšskatījuma vides pārskats](cpe-overview.md)

[Commerce priekšskatījuma vides nodrošināšana](provisioning-guide.md)

[Neobligāto līdzekļu konfigurēšana Commerce priekšskatījuma videi](cpe-optional-features.md)

[Commerce priekšskatījuma vides BUJ](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)

[Palīdzības resursi Dynamics 365 Retail](../retail/index.md)
