---
title: Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021131"
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

[Kredītkartes iestatīšana, autorizēšana un nolasīšana](../../finance/accounts-receivable/credit-card-authorizations.md)