---
title: Pārdošanas pasūtījuma lapā maksājuma veidam jābūt kredītkartes kļūdai
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad pārdošanas pasūtījuma lapā pēc pasūtījuma sinhronizēšanas tiek rādīts kļūdas ziņojums.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285637"
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
