---
title: Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad Nav ielādēta sadaļa Maksājumu metode un tiek rādīts kļūdas ziņojums.
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
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269760"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt **,** kad Nav ielādēta sadaļa Maksājumu metode un tiek rādīts kļūdas ziņojums.

## <a name="description"></a>Apraksts

Atverot tiešsaistes veikala izrakstīšanās lapu, netiek ielādēta sadaļa **Maksājuma metode** un tiek rādīts kļūdas ziņojums: "Kaut kas neizdevās. Lūdzu, vēlāk mēģiniet vēlreiz.”

![Maksājumu moduļa kļūda.](media/payment-module-error.jpg)

## <a name="resolution"></a>Novēršana

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Pagaidiet, kamēr beidzas Commerce Scale Unit kešdarbes termiņš

Maksājumu pakalpojumu iestatījumi tiešsaistes veikala izrakstīšanās lapā tiek glabāti Commerce Scale Unit un var paiet līdz 15 minūtēm, iekams tie parādās e-komercijas vietnē. Šie maksājumu pakalpojuma iestatījumi ietver izmaiņas pārdevēja konta ID, mākoņu API atslēgā un dažādos konfigurācijas iestatījumos, kas ir saistīti ar maksājuma metodi.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes kanāla iestatīšana](../channel-setup-online.md)
