---
title: Pārdošanas pasūtījuma lapā maksājuma veidam jābūt kredītkartes kļūdai
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad pēc pasūtījuma sinhronizācijas pārdošanas pasūtījuma lapā tiek parādīts kļūdas paziņojums.
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
ms.openlocfilehash: 1d6813a642aefa59e20a7c77ddcf53ce7d3625eb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347348"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Pārdošanas pasūtījuma lapā "maksājuma veidam jābūt kredītkartes kļūdai"

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad pēc pasūtījuma sinhronizācijas pārdošanas pasūtījuma lapā tiek parādīts kļūdas paziņojums.

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
