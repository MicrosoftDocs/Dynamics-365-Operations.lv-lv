---
title: Neiekļaut preces, kurām ir noteikti preces dzīves cikla stāvokļi
description: Šajā tēmā skaidrots, kā izslēgt preces, pamatojoties uz to dzīves cikla stāvokli, kad tiek izmantota plānošanas optimizācijas funkcionalitāte.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 371d98eefa482fc3e430f2f0977ddffb9dd0d30e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645096"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Neiekļaut preces, kurām ir noteikti preces dzīves cikla stāvokļi

[!include [banner](../../includes/banner.md)]

Izlaistās preces un izlaistās preces versijas iekļauj lauku **Preces dzīves cikla stāvoklis**. Šis lauks ļauj jums cita starpā kontrolēt, kuras preces ir iekļautas vispārējā plānošanā. Varat pievienot, noņemt un rediģēt dzīves cikla stāvokļus, kā nepieciešams, ejot uz **Preces informācijas pārvaldība \> Iestatīšana \> Preces dzīves cikla stāvoklis**. Katram preču dzīves cikla stāvoklim iestatiet opciju **Ir aktīvs plānošanai** uz *Jā*, ja preces, kurām ir šis stāvoklis, ir jāiekļauj vispārējās plānošanas laikā. Kad opcija ir iestatīta uz *Nē*, saistītās preces un varianti tiks izslēgti no visas vispārējās plānošanas un visiem aprēķiniem materiālu komplekta (MK) līmenī.

Izlaistās preces un varianti, kuros **Preču dzīves cikla stāvokļa** lauks ir atstāts tukšs, tiek apstrādāti tā, it kā tiem būtu preces dzīves cikla stāvoklis, kurā opcija **Ir aktīvs plānošanai** ir iestatīta uz *Jā*. Citiem vārdiem sakot, tās tiks iekļautas vispārējās plānošanas laikā.

> [!NOTE]
> Lai izvairītos no nevajadzīgiem piedāvājuma ieteikumiem, mēs iesakām jums saistīt visas novecojušās izlaistās preces un variantus ar prešu dzīves cikla stāvokli, kur opcija **Ir aktīvs plānošanai** ir iestatīta uz *Nē*. Šī pieeja ir īpaši svarīga, kad strādājat ar preču konfigurācijas variantiem, kas nav atkārtoti izmantojami, jo tas palīdzēs novērst zaudējumu rašanos.

## <a name="related-resources"></a>Saistītie resursi

Lai iegūtu vairāk informācijas par preču dzīves cikliem, skatiet [Preču dzīves cikla pārskats](../../pim/product-lifecycle.md).

Lai iegūtu detalizētu informāciju, kas iekļauj darbības preču dzīves ciklu izmantošanai, lai izslēgtu preces no vispārējās plānošanas un MK līmeņa aprēķiniem, skatiet [Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]