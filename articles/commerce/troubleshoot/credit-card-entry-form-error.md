---
title: Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad Nav ielādēta sadaļa Maksājumu metode un tiek rādīts kļūdas ziņojums.
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910447"
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
