---
title: "Izveidot krājumu prasības pakalpojumu pasūtījumiem"
description: "Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e76b0c636470a89ba2091363efe2f34eb3d58f88
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="create-item-requirements-for-service-orders"></a>Izveidot krājumu prasības pakalpojumu pasūtījumiem 

[!include [banner](../includes/banner.md)]


Varat izveidot pakalpojuma pasūtījumu, lai izsekotu un pārvaldītu saviem debitoriem sniegtos pakalpojumus. Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības. Krājumu vajadzību var nekavējoties patērēt no krājumiem, vai tā var uzsākt attiecīgā krājuma ražošanas pasūtījumu.

Ja krājumu darījuma vietā izmantojat krājuma vajadzību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma vajadzību ražošanas plānošanā.

Krājumu vajadzības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu. Lai pakalpojumu pasūtījumā izveidotu krājumu vajadzību, šim pakalpojumu pasūtījumam ir jābūt piešķirtam projektam. Pēc tam, kad pakalpojuma pasūtījumam ir izveidota krājumu vajadzība, varat skatīt krājumu vajadzības atlasītā projekta veidlapā **Projekti**.

## <a name="create-an-item-requirement-for-a-service-order"></a>Krājumu vajadzības izveide pakalpojuma pasūtījumam

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.

2.  Atlasiet pakalpojuma pasūtījumu, kuram vēlaties izveidot krājumu vajadzību.

3.  Sadaļas **Darbību rūts** cilnē **Nosūtīšana** noklikšķiniet uz **Krājumu vajadzības**.

4.  Veidlapā **Krājumu vajadzības** ievadiet informāciju par nepieciešamo krājumu. Papildinformāciju par noteiktiem laukiem skatiet rakstā [Krājumu vajadzības (veidlapa)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Krājumu vajadzības izveide pakalpojuma līgumam

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.

2.  Atveriet pakalpojuma līgumu, kuram vēlaties izveidot krājumu vajadzību.

3.  Kopsavilkuma cilnē **Rindas** noklikšķiniet uz **Pievienot**, lai izveidotu jaunu rindu.

4.  Laukā **Transakcijas veids** atlasiet vienumu **Krājums**.

5.  Laukā **Krājumu iestatījumi** atlasiet vienumu **Krājumu vajadzības**.

6.  Laukā **Krājuma kods** atlasiet krājumu, kurš ir nepieciešams pakalpojuma līgumam.

7.  Kopsavilkuma cilnē **Detalizēta informācija par rindu** cilnes **Preču dimensijas** laukā **Atrašanās vieta** atlasiet krājuma vienības atrašanās vietu.

8.  Lai izveidotu pakalpojumu pasūtījumu no līguma rindas, kopsavilkuma cilnē **Rindas** noklikšķiniet uz **Pakalpojumu pasūtījumu izveide** un pēc tam ievadiet atbilstošo informāciju veidlapā **Pakalpojumu pasūtījumu izveide**. 


## <a name="see-also"></a>Skatiet arī

[Automātiska pakalpojumu pasūtījumu izveide](create-service-orders-automatically.md).

  



