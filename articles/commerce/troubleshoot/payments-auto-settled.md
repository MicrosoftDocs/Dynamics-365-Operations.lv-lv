---
title: Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad maksājums tiek apmaksāts Adyen portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018264"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad maksājums tiek apmaksāts Adyen portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.

## <a name="description"></a>Apraksts

Kad pasūtījums tiek veikts, maksājums tiek nekavējoties apmaksāts Adyen portālā pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.

## <a name="resolution"></a>Novēršana

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Manuālas e-komercijas maksājumu tveršanas konfigurēšana Adyen portālā

Lai konfigurētu manuālu e-komercijas maksājumu tveršanu Adyen portālā, izpildiet tālāk norādītās darbības.

1. Pierakstieties Adyen portālā.
1. Augšējā labajā stūrī atlasiet savu tirgotāja kontu e-komercijas kanālam.
1. Augšējā navigācijā atlasiet **Konts** un pēc tam atlasiet **Iestatījumi**.
1. Laukā **Tveršanas aizkave** atlasiet **manuāli**.

    ![Tveršanas aizkaves iestatīšana Adyen portālā](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Papildu resursi

[Adyen maksājumu tveršana](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../dev-itpro/adyen-connector.md)

[Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
