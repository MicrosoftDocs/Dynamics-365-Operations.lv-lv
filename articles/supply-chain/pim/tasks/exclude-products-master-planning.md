--- 
title: "Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas"
description: "Šajā procedūrā ir parādīts, kā izveidot jaunu preces dzīves cikla stāvokli, kas izslēdz preces no vispārējās plānošanas un MK līmeņa aprēķina."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 1685e8eb706e29ef5b195e9163bf19345fee78b6
ms.contentlocale: lv-lv
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot jaunu preces dzīves cikla stāvokli, kas izslēdz preces no vispārējās plānošanas un MK līmeņa aprēķina.


## <a name="create-an-obsolete-state"></a>Novecojuša stāvokļa izveide
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatīšana > Preces dzīves cikla stāvoklis.
2. Noklikšķiniet uz Jauns.
3. Laukā Stāvoklis ierakstiet vērtību.
4. Atlasiet Nē laukā Ir aktīvs plānošanai.
5. Apraksta laukā ierakstiet vērtību.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Novecojuša stāvokļa saistīšana ar izlaistu preci
1. Aizvērt lapu.
2. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
3. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Saīsināts nosaukums, izmantojot vērtību “M00”.
4. Noklikšķiniet uz Rediģēt.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.

