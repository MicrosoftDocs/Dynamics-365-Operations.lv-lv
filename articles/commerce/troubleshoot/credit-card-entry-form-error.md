---
title: Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja maksājuma metodes sadaļa netiek ielādēta un rāda kļūdas ziņojumu.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018510"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu

[!include [banner](../../includes/banner.md)]

Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja **Maksājuma metodes** sadaļa netiek ielādēta un rāda kļūdas ziņojumu.

## <a name="description"></a>Apraksts

Atverot tiešsaistes veikala izrakstīšanās lapu, netiek ielādēta sadaļa **Maksājuma metode** un tiek rādīts kļūdas ziņojums: "Kaut kas neizdevās. Lūdzu, vēlāk mēģiniet vēlreiz.”

![Maksājumu moduļa kļūda](media/payment-module-error.jpg)

## <a name="resolution"></a>Novēršana

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Pagaidiet, kamēr beidzas Commerce Scale Unit kešdarbes termiņš

Maksājumu pakalpojumu iestatījumi tiešsaistes veikala izrakstīšanās lapā tiek glabāti Commerce Scale Unit un var paiet līdz 15 minūtēm, iekams tie parādās e-komercijas vietnē. Šie maksājumu pakalpojuma iestatījumi ietver izmaiņas pārdevēja konta ID, mākoņu API atslēgā un dažādos konfigurācijas iestatījumos, kas ir saistīti ar maksājuma metodi.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes kanāla iestatīšana](../channel-setup-online.md)
