---
title: Netiek rādīta opcija Saglabāt manam nākamajam maksājumam
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem maksāšanas metodes nav redzama izvēles rūtiņa Saglabāt nākamajam maksājumam.
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
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287489"
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
