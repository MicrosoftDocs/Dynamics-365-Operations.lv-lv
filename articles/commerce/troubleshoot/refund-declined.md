---
title: Atgriešanas pasūtījuma atmaksa ir noraidīta
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad atgriešanas pasūtījuma atmaksa ir noraidīta, jo rēķina izrakstīšanai izmantotā kredītkarte atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020760"
---
# <a name="refund-on-a-return-order-is-declined"></a>Atgriešanas pasūtījuma atmaksa ir noraidīta

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad atgriešanas pasūtījuma atmaksa ir noraidīta, jo rēķina izrakstīšanai izmantotā kredītkarte atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.

## <a name="description"></a>Apraksts

Atmaksa tiek noraidīta, ja kredītkarte, kas tiek izmantota atgriešanas pasūtījuma rēķinam, atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā. Tiek saņemts šāds kļūdas ziņojums: "Dažiem maksājumiem nav pareizais grāmatošanas statuss. Lūdzu, atkārtoti pārbaudiet visu maksājumu statusu pirms rēķina izrakstīšanas."

Maksājuma autorizācijas papildinformācijā tiks iekļauts šāds kļūdas ziņojums: "Adyen vārteja SendRequest() neizdevās ar statusu 'InternalServerError'.22144; Tukša atbilde atgriezta no Adyen.(22001);"

![Noraidītas atgriešanas pasūtījuma atmaksas kļūda](media/refund-order-decline.jpg)

## <a name="resolution"></a>Novēršana

### <a name="enable-blind-returns-in-adyen"></a>Diskrēti slēgto atgriešanu iespējošana Adyen

Lai iespējotu diskrēti slēgtās atgriešanas, izpildiet darbības [Dynamics 365 maksājumu savienotāja problēmu novēršana Adyen problēmām](adyen-support.md), lai sazinātos ar Adyen atbalsta komandu un pieprasītu, lai jūsu Adyen tirgotāja kontā tiktu iespējotas diskrēti slēgtās atgriešanas.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../dev-itpro/adyen-connector.md)

[Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
