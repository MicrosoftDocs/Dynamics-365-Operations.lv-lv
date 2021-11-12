---
title: Konfigurēt preci, kas jāiegādājas bez maksas
description: Šajā tēmā ir aprakstīts, kā konfigurēt preci, lai to var nopirkt bez maksas risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2ad96a3dde93a48694aee418ecfbbd33dc9830d6
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713889"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Konfigurēt preci, kas jāiegādājas bez maksas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt preci, lai to var nopirkt bez maksas risinājumā Microsoft Dynamics 365 Commerce.

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
