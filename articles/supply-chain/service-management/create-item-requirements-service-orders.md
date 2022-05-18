---
title: Krājumu prasību izveide pakalpojumu pasūtījumiem
description: Šajā tēmā ir aprakstīts, kā izveidot krājumu prasības pakalpojumu pasūtījumiem.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a92843a82093826822ab9865e43fee07d65e94c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677819"
---
# <a name="create-item-requirements-for-service-orders"></a>Krājumu prasību izveide pakalpojumu pasūtījumiem

[!include [banner](../includes/banner.md)]

Varat izveidot pakalpojuma pasūtījumu, lai izsekotu un pārvaldītu saviem debitoriem sniegtos pakalpojumus. Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības prasības. Krājumu prasību var nekavējoties patērēt no krājumiem, vai tā var uzsākt attiecīgā krājuma ražošanas pasūtījumu.

Ja krājumu darījuma vietā izmantojat krājuma prasību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma prasību ražošanas plānošanā.

Krājumu prasības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu. Lai pakalpojumu pasūtījumā izveidotu krājumu vajadzību, šim pakalpojumu pasūtījumam ir jābūt piešķirtam projektam. Pēc tam, kad pakalpojuma pasūtījumam ir izveidota krājumu vajadzība, varat skatīt krājumu vajadzības atlasītā projekta veidlapā **Projekti**.

## <a name="create-an-item-requirement-for-a-service-order"></a>Krājumu vajadzības izveide pakalpojuma pasūtījumam

1. Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.
1. Atlasiet pakalpojuma pasūtījumu, kuram vēlaties izveidot krājumu vajadzību.
1. Sadaļas **Darbību rūts** cilnē **Nosūtīšana** noklikšķiniet uz **Krājumu prasība**.
1. Veidlapā **Krājumu vajadzības** ievadiet informāciju par nepieciešamo krājumu. Papildinformāciju par noteiktiem laukiem skatiet rakstā [Krājumu vajadzības (veidlapa)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Krājumu vajadzības izveide pakalpojuma līgumam

1. Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.
1. Atveriet pakalpojuma līgumu, kuram vēlaties izveidot krājumu vajadzību.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Pievienot**, lai izveidotu jaunu rindu.
1. Laukā **Transakcijas veids** atlasiet vienumu **Krājums**.
1. Laukā **Krājumu iestatījumi** atlasiet vienumu **Krājumu vajadzības**.
1. Laukā **Krājuma kods** atlasiet krājumu, kurš ir nepieciešams pakalpojuma līgumam.
1. Kopsavilkuma cilnē **Detalizēta informācija par rindu** cilnes **Preču dimensijas** laukā **Atrašanās vieta** atlasiet krājuma vienības atrašanās vietu.
1. Lai izveidotu pakalpojumu pasūtījumu no līguma rindas, kopsavilkuma cilnē **Rindas** noklikšķiniet uz **Pakalpojumu pasūtījumu izveide** un pēc tam ievadiet atbilstošo informāciju veidlapā **Pakalpojumu pasūtījumu izveide**.

## <a name="see-also"></a>Skatiet arī

[Automātiska pakalpojumu pasūtījumu izveide](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
