---
title: Atgriešanas pasūtījuma atmaksa ir noraidīta
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad atgriešanas pasūtījuma atmaksa ir noraidīta, jo rēķinos izmantotā kredītkarte atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268237"
---
# <a name="refund-on-a-return-order-is-declined"></a>Atgriešanas pasūtījuma atmaksa ir noraidīta

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad atgriešanas pasūtījuma atmaksa ir noraidīta, jo rēķinos izmantotā kredītkarte atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.

## <a name="description"></a>Apraksts

Atmaksa tiek noraidīta, ja kredītkarte, kas tiek izmantota atgriešanas pasūtījuma rēķinam, atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā. Tiek saņemts šāds kļūdas ziņojums: "Dažiem maksājumiem nav pareizais grāmatošanas statuss. Lūdzu, atkārtoti pārbaudiet visu maksājumu statusu pirms rēķina izrakstīšanas."

Maksājuma autorizācijas papildinformācijā tiks iekļauts šāds kļūdas ziņojums: "Adyen vārteja SendRequest() neizdevās ar statusu 'InternalServerError'.22144; Tukša atbilde atgriezta no Adyen.(22001);"

![Noraidītas atgriešanas pasūtījuma atmaksas kļūda.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Novēršana

### <a name="enable-blind-returns-in-adyen"></a>Diskrēti slēgto atgriešanu iespējošana Adyen

Lai iespējotu diskrēti slēgtās atgriešanas, izpildiet darbības [Dynamics 365 maksājumu savienotāja problēmu novēršana Adyen problēmām](adyen-support.md), lai sazinātos ar Adyen atbalsta komandu un pieprasītu, lai jūsu Adyen tirgotāja kontā tiktu iespējotas diskrēti slēgtās atgriešanas.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../dev-itpro/adyen-connector.md)

[Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
