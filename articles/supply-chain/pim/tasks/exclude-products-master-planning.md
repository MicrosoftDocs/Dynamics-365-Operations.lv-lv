---
title: Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas
description: Šajā procedūrā ir parādīts, kā izveidot jaunu preces dzīves cikla stāvokli, kas izslēdz preces no vispārējās plānošanas un MK līmeņa aprēķina.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f72be341b81515b7c5540d66f61647df93af41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567035"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]