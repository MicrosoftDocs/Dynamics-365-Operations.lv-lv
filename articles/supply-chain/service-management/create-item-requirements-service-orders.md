---
title: Krājumu prasību izveide pakalpojumu pasūtījumiem
description: Šajā tēmā ir aprakstīts, kā izveidot krājumu prasības pakalpojumu pasūtījumiem.
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75a05147883f1592b3a09e02e238661f6c20cf27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575295"
---
# <a name="create-item-requirements-for-service-orders"></a>Krājumu prasību izveide pakalpojumu pasūtījumiem

[!include [banner](../includes/banner.md)]

Varat izveidot pakalpojuma pasūtījumu, lai izsekotu un pārvaldītu saviem debitoriem sniegtos pakalpojumus. Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības. Krājumu vajadzību var nekavējoties patērēt no krājumiem, vai tā var uzsākt attiecīgā krājuma ražošanas pasūtījumu.

Ja krājumu darījuma vietā izmantojat krājuma vajadzību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma vajadzību ražošanas plānošanā.

Krājumu vajadzības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu. Lai pakalpojumu pasūtījumā izveidotu krājumu vajadzību, šim pakalpojumu pasūtījumam ir jābūt piešķirtam projektam. Pēc tam, kad pakalpojuma pasūtījumam ir izveidota krājumu vajadzība, varat skatīt krājumu vajadzības atlasītā projekta veidlapā **Projekti**.

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
