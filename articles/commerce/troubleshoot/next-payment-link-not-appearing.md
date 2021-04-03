---
title: Netiek rādīta opcija Saglabāt manam nākamajam maksājumam
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem maksāšanas metodes netiek parādīta izvēles rūtiņa Saglabāt manam nākamajam maksājumam.
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585431"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Netiek rādīta opcija "Saglabāt manam nākamajam maksājumam"

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem **Maksāšanas metodes** netiek parādīta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.

## <a name="description"></a>Apraksts

E-komercijas vietnes norēķinu lapas sadaļā **Maksājuma metode** netiek parādīta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.

Attēlāzemāk parādīts norēķinu lapas piemērs, kurā ir iekļauta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.

![Izvēles rūtiņa Saglabāt manam nākamajam maksājumam Maksājumu modulī](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Novēršana

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Pārbaudīšana, vai programmā Commerce Headquarters ir pareizi konfigurēts Dynamics 365 Payment Connector for Adyen

Lai pārbaudītu, vai programmā Commerce Headquarters ir pareizi konfigurēts Dynamics 365 Payment Connector for Adyen, izpildiet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un tirdzniecība \> Kanāli \> Tiešsaistes veikali**.
1. Atlasiet tiešsaistes veikalu.
1. Kopsavilkuma cilnē **Maksājumu konti** pārliecinieties, vai lauka **Atļaut saglabāt maksājuma informāciju e-komercijā** vērtība ir iestatīta uz **Patiess**.

![Atļaut saglabāt maksājuma informāciju e-kommercijas laukā programmā Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Papildu resursi

[Maksājumu modulis](../payment-module.md)

[Tiešsaistes maksājumu instrumentu saglabāšana, izmantojot savienotāju Adyen](../dev-itpro/adyen-connector-listPI.md)
