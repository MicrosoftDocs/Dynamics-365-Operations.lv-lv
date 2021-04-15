---
title: Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.
author: Reza-Assadi
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801439"
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
