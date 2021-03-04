---
title: Dynamics 365 Commerce novērtējuma vides konfigurācija
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce novērtējuma vidi, pēc tās nodrošināšanas.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413943"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce novērtējuma vides konfigurācija

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce novērtējuma vidi, pēc tās nodrošināšanas.

## <a name="overview"></a>Pārskats

Šajā tēmā minētās procedūras veiciet tikai pēc tam, kad ir nodrošināta Commerce novērtējuma vide. Informāciju par to, kā nodrošināt Commerce novērtējuma vidi, skatiet [Commerce novērtējuma vides nodrošināšana](provisioning-guide.md).

Kad jūsu Commerce novērtējuma vide ir pilnībā nodrošināta, ir jāpabeidz papildu pēc nodrošināšanas konfigurācijas darbības, pirms var sākt novērtēt vidi. Lai veiktu šīs darbības, ir jāizmanto Microsoft Dynamics Lifecycle Services (LCS) un Dynamics 365 Commerce.

## <a name="before-you-start"></a>Pirms darba sākšanas

1. Pierakstieties [LCS portālā](https://lcs.dynamics.com).
1. Dodieties uz savu projektu.
1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijas labajā pusē atlasiet **Pieteikties vidē**. Jūs tiksiet nosūtīts uz Commerce galveno biroju.
1. Pārliecinieties, ka ir atlasīta **USRT** juridiskā persona (augšējā labajā stūrī).

Pēc nodrošināšanas darbību laikā Commerce Headquarters, pārliecinieties, ka **USRT** juridiskā persona vienmēr ir atlasīta.

## <a name="configure-the-point-of-sale"></a>Pārdošanas punkta konfigurācija

### <a name="associate-a-worker-with-your-identity"></a>Nodarbinātā saistīšana ar jūsu identitāti

Lai saistītu darbinieku ar jūsu identitāti, veiciet Commerce Headquarters norādītās darbības.

1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Darbinieki \> Nodarbinātie**.
1. Sarakstā atrodiet un atlasiet šādu ierakstu **000713 – Endrjū Kollete**.
1. Darbību rūtī atlasiet **Commerce**.
1. Atlasiet **Piesaistīt esošu identitāti**.
1. Laukā **E-pasts** (pa labi no **Meklēt, izmantojot e-pastu**) ievadiet savu e-pasta adresi.
1. Atlasiet **Meklēt**.
1. Atlasiet ierakstu ar savu vārdu.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt**.

### <a name="activate-cloud-pos"></a>mākoņa POS aktivizēšana;

Lai aktivizētu mākoņa POS, veiciet LCS norādītās darbības.

1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijas labajā pusē atlasiet **Pieteikties mākoņa pārdošanas punktā**.
1. Atlasiet **Tālāk**, lai atvērtu dialoglodziņu **Pirms darba sākšanas**.
1. Atstājiet lauku **Servera URL**, kā tas ir. Atlasiet **Nākamais**.
1. Piesakieties, izmantojot savu Microsoft Azure Active Directory (Azure AD) kontu.
1. Sadaļā **Veikala nosaukums** atlasiet **Sanfrancisko** un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Reģistrs un ierīce** atlasiet **SANFRAN-1**.
1. Atlasiet **Aktivizēt**. Jūs esat izrakstījies un aizvirzīts uz POS pierakstīšanās lapu.
1. Tagad varat pieteikties mākoņa POS pieredzei, izmantojot operatora ID **000713** un paroli **123**.

## <a name="set-up-your-site-in-commerce"></a>Iestatiet savu vietni pakalpojumā Commerce.

Lai sāktu iestatīt novērtējuma vietni pakalpojumā Commerce, veiciet tālāk norādītās darbības.

1. Piesakieties vietņu veidotājā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-komerciju (skatiet [e-komercijas inicializēšana](provisioning-guide.md#initialize-e-commerce)).
1. Atlasiet vietni **Fabrikam**, lai atvērtu vietnes iestatīšanas dialoglodziņu.
1. Atlasiet domēnu, kuru ievadījāt, kad inicializējat e-Commerce.
1. Kā noklusējuma kanālu atlasiet **Fabrikam paplašinātais tiešsaistes veikals**. (Pārliecinieties, ka atlasāt **paplašināto** tiešsaistes veikalu.)
1. Ka noklusējuma valodu atlasiet **en-us**.
1. Atstājiet lauka **Path** vērtību tādu, kāda tā ir.
1. Atlasiet **Labi**. Tiek parādīts vietnes lapu saraksts.

## <a name="enable-jobs"></a>Darbu iespējošana

Lai iespējotu darbus pakalpojumā Commerce, izpildiet tālāk aprakstītās darbības.

1. Pierakstieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Mazumtirdzniecība un komercija \> Pieprasījumi un pārskati \> Pakešuzdevumi**.

    Šīs procedūras atlikušie soļi jāaizpilda katram no šiem darbiem:

    * Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojumu
    * Preču pieejamība
    * P-0001
    * Darbs Sinhronizēt pasūtījumus

1. Izmantojiet ātro filtru, lai meklētu darbu pēc nosaukuma.
1. Ja darba statuss ir **Izpilda**, veiciet tālāk norādītās darbības:

    1. Atlasiet ierakstu.
    1. Darbību rūtī noklikšķiniet uz cilnes **Pakešuzdevums**, pēc tam atlasiet **Mainīt statusu**.
    1. Atlasiet **Atcelt** un pēc tam atlasiet **Labi**.

Pēc izvēles var arī iestatīt atkārtošanās intervālu uz vienu (1) minūti šādiem darbiem:

* Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojuma darbu
* P-0001 darbs
* Darbs Sinhronizēt pasūtījumus

### <a name="run-full-data-synchronization"></a>Izpildīt pilnīgu datu sinhronizāciju

Lai pakalpojumā Commerce palaistu pilnu datu sinhronizāciju, veiciet Commerce Headquarters norādītās darbības.

1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Mazumtirdzniecības uzstādīšana \> Komercijas plānotājs \> Kanāla datubāze**.
1. Atlasiet kanālu ar nosaukumu **scXXXXXXXXX**.
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

Kad nodrošināšanas un konfigurēšanas darbības ir pabeigtas, varat sākt izmantot novērtējuma vidi. Izmantojiet Commerce vietnes veidotāja URL, lai dotos uz autorēšanas pieredzi. Izmantojiet Commerce vietnes URL, lai dotos uz mazumtirdzniecības klienta vietnes pieredzi.

Lai konfigurētu neobligātos līdzekļus savai Commerce novērtējuma videi, skatiet [Commerce novērtējuma vides neobligāto līdzekļu konfigurācija](cpe-optional-features.md).

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce novērtējuma vides pārskats](cpe-overview.md)

[Nodrošināt Dynamics 365 Commerce novērtējuma vidi](provisioning-guide.md)

[Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-optional-features.md)

[BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-bopis.md)

[Dynamics 365 Commerce novērtējuma vide - bieži uzdotie jautājumi](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]