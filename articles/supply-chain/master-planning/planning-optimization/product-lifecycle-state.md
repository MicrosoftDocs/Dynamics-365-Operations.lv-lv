---
title: Neiekļaut preces, kurām ir noteikti preces dzīves cikla stāvokļi
description: Šajā rakstā ir izskaidrots, kā izslēgt preces, balstoties uz to dzīves cikla stāvokli, kad tiek izmantota plānošanas optimizācijas funkcionalitāte.
author: t-benebo
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6bf6f1d9a82200240f55c387396d9d70dfa6dfc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873845"
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