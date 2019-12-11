---
title: Preču ieteikumu iespējošana
description: Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770143"
---
# <a name="enable-product-recommendations"></a>Preču ieteikumu iespējošana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ieteikumu iepriekšpārbaude
Pirms iespējošanas, lūdzu, ievērojiet, ka preces ieteikumi tiek atbalstīti tikai nākotnes līgumu un iespēju līgumu klientiem, kas atbalsta veidojumu 10.0.6 un ir migrējuši savu krātuvi, lai izmantotu BDL. 

Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi. Lai uzzinātu vairāk par šo iestatīšanas procesu, dodieties [šeit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Ieteikumu ieslēgšana

Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.

1. Dodieties uz **Mazumtirdzniecība** &gt; **Preču ieteikumi** &gt; **Ieteikuma parametri**.
1. Mazumtirdzniecības koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.
1. Iestatiet opciju **Iespējot ieteikumus** uz **Jā**.

![Preču ieteikumu iespējošana](./media/enableproductrecommendations.png)

> [!NOTE]
> Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu. Var paiet vairākas stundas pirms saraksts ir pieejams un redzams pārdošanas punktā (POS) vai Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>Ieteikumu saraksta parametru konfigurēšana
Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības. Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai. Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Parādīt ieteikumus POS ierīcēs
Pēc ieteikumu iespējošanas birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku. Lai uzzinātu vairāk par šo procesu, dodieties [šeit.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Preču ieteikumu sarakstu pievienošana lapām](add-reco-list-to-page.md)

[Ieteikumu paneļa pievienošana POS ierīcēm](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


