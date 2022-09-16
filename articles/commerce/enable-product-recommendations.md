---
title: Iespējot preču ieteikumus
description: Šajā rakstā skaidrots, kā veidot produktu ieteikumus, kas balstīti uz klienta inteliģences apmācību (AI-PARA) pieejamajiem Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
ms.date: 09/08/2022
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
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460026"
---
# <a name="enable-product-recommendations"></a>Iespējot preču ieteikumus

[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā veidot produktu ieteikumus, kas balstīti uz klienta inteliģences apmācību (AI-PARA) pieejamajiem Microsoft Dynamics 365 Commerce klientiem. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ieteikumu iepriekšpārbaude

1. Pārliecinieties, ka jums ir derīga Dynamics 365 Commerce ieteikumu licence.
1. Pārliecinieties, ka entitījas veikals ir pieslēgts klientam piederošajam Azure Data Lake Storage Gen2 kontam. Papildinformācijai skatiet [EPārliecinieties, ka Azure Data Lake Storage ir iegādāta un sekmīgi pārbaudīta vidē](enable-ADLS-environment.md).
1. Apstipriniet, ka Azure AD identitātes konfigurācija ietver ievadni ieteikumiem. Papildinformāciju par to, kā veikt šo darbību, skatīt zemāk.
1. Pārliecinieties, ka entitījas veikalam katru dienu ir ieplānota atsvaidzināšana uz Azure Data Lake Storage Gen2. Papildinformāciju skatiet [Pārliecinieties, ka elementa krātuves atsvaidzināšana ir automatizēta](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. RetailSale mērījumu iespējošana entitījas veikalam. Plašāku informāciju par šī procesa iestatīšanu skatiet sadaļā [Darbs ar mērījumiem](/dynamics365/ai/customer-insights/pm-measures).
1. Nodrošiniet, lai vide pašreiz atbalstītajos reģionos būtu konfigurējusi atbalstītos reģionus un tos, kā tas ir norādīts tālāk.

    - **Atbalstītie apgabali:** ES/ASV/CA/AU.
    - **Tiek atbalstīti reģioni:** US/CA/AU. Ja atbilstošais reģions neatbilst vienam no esošajiem atbalstītajiem reģioniem, rekomendāciju pakalpojums atlasīs vistuvākais atbalstīto pasniegšanas reģionu.

Pēc tam, kad ir veiktas iepriekš minētās darbības, būsit gatavi iespējot ieteikumus.

> [!NOTE]
> Ir zināms problēma, kur ieteikumi neparādās pēc tālāk norādīto darbību pabeigšanas. Šo problēmu rada datu plūsmas problēmas vidē. Ja jūsu vidē nav rekomendāciju rezultātu, [konfigurējiet alternatīvos datus rekomendāciju pakalpojumam, izpildot soļus sadaļā Iestatīt alternatīvu datu darbplūsmu rekomendācijām](set-up-alternate-data-flow.md). Lai veiktu šīs darbības, ir nepieciešamas Azure administratora atļaujas. Ja jums nepieciešama palīdzība, sazinieties ar FastTrack pārstāvi.

## <a name="azure-ad-identity-configuration"></a>Azure AD identitātes konfigurācija

Šis solis ir nepieciešams tikai klientiem, kuri darbojas kā pakalpojuma (IaaS) konfigurācija. Azure AD Identitātes konfigurācija ir automātiska debitoriem, kuri darbojas Azure Service Fabric, bet ieteicams pārbaudīt, vai šis iestatījums ir konfigurēts, kā paredzēts.

### <a name="setup"></a>Iestatīt

1. Commerce galvenajā pārvaldē meklējiet lapu **Azure Active Directory lietojumprogrammas**.
1. Pārbaudiet, vai ieraksts eksistē vienumam **RecommendationSystemApplication-1**. Ja ieraksta nav, izveidojiet ierakstu, izmantojot tālāk norādīto informāciju:

    - **Klienta Id**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Nosaukums**: RecommendationSystemApplication-1
    - **Lietotaja Id**: RetailServiceAccount

1. Saglabājiet un aizveriet lapu. 

## <a name="turn-on-recommendations"></a>Ieteikumu ieslēgšana

Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.

1. Programmā Commerce Headquarters meklējiet **Funkciju pārvaldība**.
1. Atlasiet **Visi**, lai skatītu pieejamo funkciju sarakstu. 
1. Meklēšanas lodziņā ievadiet **Ieteikumi**.
1. Atlasiet līdzekli **Preču ieteikumi**.
1. **Preču ieteikumi** rekvizītu rūtī atlasiet **Iespējot tagad**.

![Ieteikumu ieslēgšana.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Iepriekš minētā procedūra uzsāk preču ieteikumu sarakstu ģenerēšanu. Var paiet vairākas stundas pirms saraksts ir pieejams un var tikt redzams pārdošanas punktā (POS) vai Dynamics 365 Commerce.
> - Šī konfigurācija neiespējo visus ieteikumu līdzekļus. Papildu līdzekļi, piemēram, personalizēti ieteikumi, "pirkt ar līdzīgu izskatu" un "pirkt ar līdzīgu aprakstu", tiek kontrolēti ar īpašiem līdzekļu pārvaldības ierakstiem. Informāciju par to, kā iespējot šos līdzekļus Commerce galvenajā pārvaldībā, skatiet rakstā [Personalizēto ieteikumu iespējošana](personalized-recommendations.md), [Ieteikumu "pirkt ar līdzīgu izskatu" iespējošana](shop-similar-looks.md) un [Ieteikumu "pirkt ar līdzīgu aprakstu"](shop-similar-description.md) iespējošana.

## <a name="configure-recommendation-list-parameters"></a>Ieteikumu saraksta parametru konfigurēšana

Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības. Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai. Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Rekomendāciju iekļaušana e-komercijas iespējās

Pēc ieteikumu iespējošanas Commerce galvenajā pārvaldē Commerce moduļus, kuri izmantoti, lai rādītu e-komercijas iespēju ieteikumu rezultātus, var konfigurēt. Papildinformāciju skatiet sadaļā [Produktu kolekciju moduļi](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Parādīt ieteikumus POS ierīcēs

Pēc ieteikumu iespējošanas Commerce galvenajā pārvaldē, ieteikumu paneli ir jāpievieno vadības POS ekrānam, izmantojot izkārtojuma rīku. Lai uzzinātu vairāk par šo procesu, skatiet sadaļu [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalizētu ieteikumu iespējošana

Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus. Šādā veidā personalizētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS). Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.

Papildinformāciju par personalizēto ieteikumu saņemšanu skatiet [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iestatīt alternatīvu datu plūsmu rekomendācijām](set-up-alternate-data-flow.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Ieteikumu “pirkt līdzīgus modeļus” iespējošana](shop-similar-looks.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
