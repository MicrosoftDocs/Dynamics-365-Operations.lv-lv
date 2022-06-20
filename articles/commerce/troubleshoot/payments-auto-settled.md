---
title: Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad maksājums tiek apmaksāts A saņemšanas portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.
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
ms.openlocfilehash: c01a2fda54e198a43fa84ae83686fc1701958b6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890273"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad maksājums tiek apmaksāts A saņemšanas portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.

## <a name="description"></a>Apraksts

Kad pasūtījums tiek veikts, maksājums tiek nekavējoties apmaksāts Adyen portālā pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.

## <a name="resolution"></a>Novēršana

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Manuālas e-komercijas maksājumu tveršanas konfigurēšana Adyen portālā

Lai konfigurētu manuālu e-komercijas maksājumu tveršanu Adyen portālā, izpildiet tālāk norādītās darbības.

1. Pierakstieties Adyen portālā.
1. Augšējā labajā stūrī atlasiet savu tirgotāja kontu e-komercijas kanālam.
1. Augšējā navigācijā atlasiet **Konts** un pēc tam atlasiet **Iestatījumi**.
1. Laukā **Tveršanas aizkave** atlasiet **manuāli**.

    ![Tveršanas aizkaves iestatīšana Adyen portālā.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Papildu resursi

[Adyen maksājumu tveršana](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector pakalpojumam Adyen](../dev-itpro/adyen-connector.md)

[Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
