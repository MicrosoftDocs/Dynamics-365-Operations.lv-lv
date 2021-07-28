---
title: Preču ieteikumu iespējošana
description: Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a94a74f4eb00c24142f0390bcf352db0594ca0b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349476"
---
# <a name="enable-product-recommendations"></a>Iespējot preču ieteikumus

[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ieteikumu iepriekšpārbaude

Pirms iespējošanas ievērojiet, ka preces ieteikumi tiek atbalstīti tikai tiem Commerce klientiem, kuri ir migrējuši savu krātuvi, lai izmantotu Azure Data Lake Storage. 

Pirms ieteikumu iespējošanas birojā ir jābūt iespējotām šādām konfigurācijām:

1. Pārliecinieties, ka Azure Data Lake Storage ir iegādāta un sekmīgi pārbaudīta vidē. Papildinformācijai skatiet [EPārliecinieties, ka Azure Data Lake Storage ir iegādāta un sekmīgi pārbaudīta vidē](enable-ADLS-environment.md).
2. Pārliecinieties, ka elementa krātuves atsvaidzināšana ir automatizēta. Papildinformāciju skatiet [Pārliecinieties, ka elementa krātuves atsvaidzināšana ir automatizēta](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Apstipriniet, ka Azure AD identitātes konfigurācija ietver ievadni ieteikumiem. Papildinformāciju par to, kā veikt šo darbību, skatīt zemāk.

Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi. Lai uzzinātu vairāk par šo iestatīšanas procesu, skatiet [Darbs ar mērvienībām](/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD identitātes konfigurācija

Šis solis ir nepieciešams visiem klientiem, kas izmanto infra-structure kā pakalpojuma (IaaS) konfigurāciju. Klientiem, kas darbojas Service Fabric (SF), šim solim ir jābūt automātiskam, un ieteicams pārbaudīt, vai iestatījums ir konfigurēts, kā paredzēts.

### <a name="setup"></a>Iestatīt

1. Birojā meklējiet **Azure Active Directory pieteikumu** lapu.
2. Pārbaudiet, vai pastāv ieraksts "RecommendationSystemApplication-1".

Ja ieraksts nepastāv, pievienojiet jaunu ierakstu ar šādu informāciju:

- **Klienta ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Nosaukums** -RecommendationSystemApplication-1
- **Lietotāja ID** - RetailServiceAccount

Saglabājiet un aizveriet lapu. 

## <a name="turn-on-recommendations"></a>Ieteikumu ieslēgšana

Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.

1. Programmā Commerce Headquarters meklējiet **Funkciju pārvaldība**.
1. Atlasiet **Visi**, lai skatītu pieejamo funkciju sarakstu. 
1. Meklēšanas lodziņā ievadiet **Ieteikumi**.
1. Atlasiet līdzekli **Preču ieteikumi**.
1. **Preču ieteikumi** rekvizītu rūtī atlasiet **Iespējot tagad**.

![Ieteikumu ieslēgšana.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu. Var paiet vairākas stundas pirms saraksts ir pieejams un var tikt redzams pārdošanas punktā (POS) vai Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Ieteikumu saraksta parametru konfigurēšana

Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības. Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai. Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Parādīt ieteikumus POS ierīcēs

Pēc ieteikumu iespējošanas Commerce dokumentu apstrādes birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku. Lai uzzinātu vairāk par šo procesu, skatiet sadaļu [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalizētu ieteikumu iespējošana

Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus. Šādā veidā personalizētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS). Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.

Papildinformāciju par personalizēto ieteikumu saņemšanu skatiet [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce .](enable-adls-environment.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]