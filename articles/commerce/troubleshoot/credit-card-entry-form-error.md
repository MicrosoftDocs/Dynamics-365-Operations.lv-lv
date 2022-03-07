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
ms.openlocfilehash: 613eb2af626ca315a8bacb89fb348a5b14bd17b1717a90c99bcede66baef9040
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752391"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu

[!include [banner](../../includes/banner.md)]

Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja **Maksājuma metodes** sadaļa netiek ielādēta un rāda kļūdas ziņojumu.

## <a name="description"></a>Apraksts

Atverot tiešsaistes veikala izrakstīšanās lapu, netiek ielādēta sadaļa **Maksājuma metode** un tiek rādīts kļūdas ziņojums: "Kaut kas neizdevās. Lūdzu, vēlāk mēģiniet vēlreiz.”

![Maksājumu moduļa kļūda.](media/payment-module-error.jpg)

## <a name="resolution"></a>Novēršana

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Pagaidiet, kamēr beidzas Commerce Scale Unit kešdarbes termiņš

Maksājumu pakalpojumu iestatījumi tiešsaistes veikala izrakstīšanās lapā tiek glabāti Commerce Scale Unit un var paiet līdz 15 minūtēm, iekams tie parādās e-komercijas vietnē. Šie maksājumu pakalpojuma iestatījumi ietver izmaiņas pārdevēja konta ID, mākoņu API atslēgā un dažādos konfigurācijas iestatījumos, kas ir saistīti ar maksājuma metodi.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes kanāla iestatīšana](../channel-setup-online.md)
