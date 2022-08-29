---
title: Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kas var rasties, sinhronizējot tiešsaistes pasūtījumu.
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
ms.openlocfilehash: aa57366fb8f351a8275c947220de78fe809b7b5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276694"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kas var rasties, sinhronizējot tiešsaistes pasūtījumu.

## <a name="description"></a>Apraksts

Kad sinhronizējat tiešsaistes pasūtījumu, tiek saņemts šāds kļūdas ziņojums: "Lai apstrādātu kredītkartes darījumu, ir nepieciešams noklusējuma maksājumu pakalpojums."

![Neesoša noklusējuma maksājumu pakalpojuma kļūda.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Novēršana

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Noklusējuma maksājumu pakalpojuma apstiprināšana vai iestatīšana programmā Commerce Headquarters

Lai apstiprinātu vai iestatītu noklusējuma maksājumu pakalpojumu programmā Commerce Headquarters, izpildiet tālāk minētās darbības.

1. Pārejiet uz sadaļu **Debitoru parādi \> Maksājumu iestatīšana \> Maksājumu pakalpojumi**.
1. Pārliecinieties, ka opcija **Noklusējuma apstrādātājs jaunām kredītkartēm** ir iestatīts uz **Jā** vienam maksājumu pakalpojumam.

## <a name="additional-resources"></a>Papildu resursi

[Kredītkartes iestatīšana, autorizēšana un nolasīšana](../../finance/accounts-receivable/credit-card-authorizations.md)
