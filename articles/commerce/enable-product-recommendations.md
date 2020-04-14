---
title: Preču ieteikumu iespējošana
description: Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154417"
---
# <a name="enable-product-recommendations"></a>Preču ieteikumu iespējošana

[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ieteikumu iepriekšpārbaude

Pirms iespējošanas, lūdzu, ievērojiet, ka preces ieteikumi tiek atbalstīti tikai tiem Commerce klientiem, kuri ir migrējuši savu krātuvi, lai izmantotu Azure Data Lake Storage (ADLS). 

Veicamās darbības ADLS iespējošanai skatiet [Kā iespējot ADLS programmas Dynamics 365 vidē.](enable-ADLS-environment.md)

Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi. Lai uzzinātu vairāk par šo iestatīšanas procesu, dodieties [šeit.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Ieteikumu ieslēgšana

Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.

1. Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu parametri**.
1. Koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.
1. Iestatiet opciju **Iespējot ieteikumus** uz **Jā**.

![Preču ieteikumu iespējošana](./media/enableproductrecommendations.png)

> [!NOTE]
> Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu. Var paiet vairākas stundas pirms saraksts ir pieejams un redzams pārdošanas punktā (POS) vai Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Ieteikumu saraksta parametru konfigurēšana

Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības. Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai. Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Parādīt ieteikumus POS ierīcēs

Pēc ieteikumu iespējošanas Commerce dokumentu apstrādes birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku. Lai uzzinātu vairāk par šo procesu, skatiet sadaļu [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalizētu ieteikumu iespējošana

Papildinformāciju par personalizēto ieteikumu saņemšanu skatiet sadaļā [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[ADLS iespējošana Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)

