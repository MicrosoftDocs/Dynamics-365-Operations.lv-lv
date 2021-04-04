---
title: Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585423"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.

## <a name="description"></a>Apraksts

Kad sinhronizējat tiešsaistes pasūtījumu, tiek saņemts šāds kļūdas ziņojums: "Lai apstrādātu kredītkartes darījumu, ir nepieciešams noklusējuma maksājumu pakalpojums."

![Neesoša noklusējuma maksājumu pakalpojuma kļūda](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Novēršana

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Noklusējuma maksājumu pakalpojuma apstiprināšana vai iestatīšana programmā Commerce Headquarters

Lai apstiprinātu vai iestatītu noklusējuma maksājumu pakalpojumu programmā Commerce Headquarters, izpildiet tālāk minētās darbības.

1. Pārejiet uz sadaļu **Debitoru parādi \> Maksājumu iestatīšana \> Maksājumu pakalpojumi**.
1. Pārliecinieties, ka opcija **Noklusējuma apstrādātājs jaunām kredītkartēm** ir iestatīts uz **Jā** vienam maksājumu pakalpojumam.

## <a name="additional-resources"></a>Papildu resursi

[Kredītkartes iestatīšana, autorizēšana un nolasīšana](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
