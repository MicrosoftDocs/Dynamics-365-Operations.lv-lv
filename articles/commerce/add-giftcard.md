---
title: Dāvanu kartes modulis
description: Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261579"
---
# <a name="gift-card-module"></a>Dāvanu kartes modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Dāvanu kartes ir parastā maksājuma forma, un dāvanu kartes modulis var tikt izmantots norēķinu modulī, lai pieņemtu dāvanu kartes. Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes. SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju.

Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md)

## <a name="module-properties"></a>Moduļa rekvizīti

- **Rādīt papildu laukus** - šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma. Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu. Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.

Atbalstītās vērtības:
-   PIN
-   Beigu datums
-   PIN un beigu datums 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Vietas iestatījumi dāvanu karšu moduļiem

Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \>Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**. Šis iestatījums atbalsta trīs vērtības:
- **Dynamics 365 dāvanu karte** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.
- **SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.
- **Dynamics 365, SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.

## <a name="add-a-gift-card-module-to-a-page"></a>Dāvanu kartes moduļa pievienošana lapā

Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md)
