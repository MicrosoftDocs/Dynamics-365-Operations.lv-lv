---
title: Konfigurēt preci, kas jāiegādājas bez maksas
description: Šajā rakstā ir aprakstīts, kā konfigurēt preci, kurā to var nopirkt bez maksas Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bd7e4f7a7873e471f1aee94f15e7932e8d9eecd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890359"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Konfigurēt preci, kas jāiegādājas bez maksas

[!include [banner](includes/banner.md)]


Šajā rakstā ir aprakstīts, kā konfigurēt preci, kurā to var nopirkt bez maksas Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Konfigurēt preci

Lai preci pārdotu bez maksas risinājumā Dynamics 365 Commerce, tās cena ir jāiestata uz 0 (nulli). Turklāt ir jākonfigurē preces **Derīga nulles cena** iestatījums.

Lai konfigurētu **Derīga nulles cena** iestatījumu programmā Commerce Headquarters, sekojiet šiem soļiem.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Tirdzniebā laistās preces pēc kategorijas**.
1. Dodieties uz preci, kuru vēlaties pārdot par brīvu. 
1. Preces lapas **Commerce** sadaļā iestatiet opciju **Derīga nulles cena** uz **Jā**.

Šajā attēlā parādīts preces piemērs, kur opcija **Derīga nulles cena** iestatīta uz **Jā**.

![Piemērs precei, kuras opcija Derīga nulles cena, ir iestatīta uz Jā.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Tiešsaistes veikala funkcionalitātes profila konfigurēšana

Pirms brīvās darbības var apstrādāt, ir jākonfigurē **Atļaut norēķināties bez maksājumiem** funkcionalitātes profila iestatījumi jūsu tiešsaistes veikalā, lai transakcijas, kurām nav maksājumu, būtu atļautas. Papildinformāciju par to, kā izveidot funkcionalitātes profilus, skatiet sadaļā [Tiešsaistes funkcionalitātes profila izveide](online-functionality-profile.md).

Lai konfigurētu **Atļaut norēķināties bez maksājumiem** iestatījumu programmā Commerce Headquarters, veiciet šādas darbības.

1. Dodieties uz **Mazumtirdzniecība un Komercija \> Kanāla iestatījumi \> Tiešsaistes veikala iestatījumi**.
1. Veikala funkcionalitātes profila lapā zem **Norēķināties** iestatiet opciju **Atļaut norēķināties bez maksājumiem** uz **Jā**.

Šajā attēlā parādīts tiešsaistes veikala profila piemērs, kur opcija **Atļaut norēķināties bez maksājumiem** ir iestatīta uz **Jā**.

![Šajā attēlā parādīts tiešsaistes veikala profila piemērs, kur opcija Atļaut norēķināties bez maksājumiem ir iestatīta uz Jā.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Papildu resursi

[Mazumtirdzniecības pārdošanas cenu pārvaldība](price-management.md)

[Izveidot tiešsaistes funkcionalitātes profilu](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
