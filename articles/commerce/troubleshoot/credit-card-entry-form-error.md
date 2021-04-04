---
title: Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja maksājuma metodes sadaļa netiek ielādēta un rāda kļūdas ziņojumu.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585424"
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
