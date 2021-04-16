---
title: Commerce galvenajā pārvaldē netiek rādīti klientu ieraksti
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja klientu ieraksti nekavējoties netiek rādīti Commerce galvenajā pārvaldē.
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801799"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Commerce galvenajā pārvaldē netiek rādīti klientu ieraksti

[!include [banner](../../includes/banner.md)]

Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja klientu ieraksti nekavējoties netiek rādīti Commerce galvenajā pārvaldē.

## <a name="description"></a>Apraksts

Izveidojot jaunu klienta ierakstu, izmantojot e-komercijas tīmekļa vitrīnu, atbilstošais klienta ieraksts nekavējoties neparādās Commerce galvenajā pārvaldē.

## <a name="resolution"></a>Novēršana

### <a name="disable-customer-creation-in-async-mode"></a>Klienta izveides atspējošana asinhronajā režīmā

> [!IMPORTANT]
> Ja atspējot asinhrona klienta izveidi, sistēmas sniegumam vajadzētu tikt ietekmētam, jo katra ieraksta izveidē radīsies reāllaika pieprasījums Commerce galvenajai pārvaldei. Turklāt, ja Commerce galvenā pārvalde nedarbojas (piemēram, apkalpošanas plūsmu laikā), jaunu klientu izveides plūsmas radīs kļūdas.

Lai atspējotu klientu izveidi asinhronajā režīmā Commerce galvenajā pārvaldē, izpildiet šādas darbības:

1. Dodieties uz **Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitāšu profili**.
1. Ja jau neizmantojat sava tiešsaistes kanāla funkcionalitātes profilu, izveidojiet to.
1. Pārliecinieties, ka opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Nē**.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāli \> Tiešsaistes veikali**.
1. Atlasiet tiešsaistes veikalu, kuram atspējot asinhrono klientu izveidi.
1. Cilnē **Vispārīgi** pārliecinieties, ka lauks **Funkcionalitātes profils** ir iestatīts uz to funkcionalitātes profilu, kuru izmantojat savam tiešsaistes kanālam.

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana risinājumā Commerce](../set-up-b2c-tenant.md)
