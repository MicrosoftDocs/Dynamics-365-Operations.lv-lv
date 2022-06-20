---
title: Pārdošanas pasūtījuma lapā maksājuma veidam jābūt kredītkartes kļūdai
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad pārdošanas pasūtījuma lapā pēc pasūtījuma sinhronizēšanas tiek rādīts kļūdas ziņojums.
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
ms.openlocfilehash: 794317a84a8a0ff205ac1b6a5caa6ef1cf098ea3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905347"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Pārdošanas pasūtījuma lapā "maksājuma veidam jābūt kredītkartes kļūdai"

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad pārdošanas pasūtījuma lapā pēc pasūtījuma sinhronizēšanas tiek rādīts kļūdas ziņojums.

## <a name="description"></a>Apraksts

Kad pēc pasūtījuma sinhronizēšanas atverat pārdošanas pasūtījuma lapu, tiek saņemts šāds kļūdas ziņojums: "Maksājuma veidam jābūt kredītkartei, jo ir norādīts kredītkartes numurs."

![Maksājuma veidam jābūt kredītkartes kļūdai.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Novēršana

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Iestatīt maksājuma veidu programmā Commerce Headquarters

1. Pārejiet uz sadaļu **Debitori \> Maksājumu iestatījumi \> Apmaksas nosacījumi**.
1. Navigācijas kreisajā pusē atlasiet apmaksas nosacījumus.
1. Laukā **Maksājuma veids** pārliecinieties, ka ir atlasīta **Kredītkarte**.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes pārdošanas un maksājumu grāmatošana](../tasks/posting-online-sales-payments.md)
