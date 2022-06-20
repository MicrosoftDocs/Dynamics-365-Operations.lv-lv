---
title: Netiek rādīta opcija Saglabāt manam nākamajam maksājumam
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem maksāšanas metodes nav redzama izvēles rūtiņa Saglabāt nākamajam maksājumam.
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
ms.openlocfilehash: efa04c87f78c376fd00da1b26aedb9e8b428dfa5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871559"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Netiek rādīta opcija "Saglabāt manam nākamajam maksājumam"

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir **sniegti** **problēmu** novēršanas norādījumi, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem maksāšanas metodes nav redzama izvēles rūtiņa Saglabāt nākamajam maksājumam.

## <a name="description"></a>Apraksts

E-komercijas vietnes norēķinu lapas sadaļā **Maksājuma metode** netiek parādīta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.

Attēlāzemāk parādīts norēķinu lapas piemērs, kurā ir iekļauta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.

![Izvēles rūtiņa Saglabāt manam nākamajam maksājumam Maksājumu modulī.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Novēršana

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Pārbaudīšana, vai programmā Commerce Headquarters ir pareizi konfigurēts Dynamics 365 Payment Connector for Adyen

Lai pārbaudītu, vai programmā Commerce Headquarters ir pareizi konfigurēts Dynamics 365 Payment Connector for Adyen, izpildiet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un tirdzniecība \> Kanāli \> Tiešsaistes veikali**.
1. Atlasiet tiešsaistes veikalu.
1. Kopsavilkuma cilnē **Maksājumu konti** pārliecinieties, vai lauka **Atļaut saglabāt maksājuma informāciju e-komercijā** vērtība ir iestatīta uz **Patiess**.

![Atļaut saglabāt maksājuma informāciju e-kommercijas laukā programmā Commerce Headquarters.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Papildu resursi

[Maksājumu modulis](../payment-module.md)

[Tiešsaistes maksājumu instrumentu saglabāšana, izmantojot savienotāju Adyen](../dev-itpro/adyen-connector-listPI.md)
