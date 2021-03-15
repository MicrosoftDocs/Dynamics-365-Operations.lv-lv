---
title: Noklusējuma preces dzīves cikla stāvokļa izveidošana
description: Šajā procedūrā ir parādīts, kā izveidot noklusējuma preces dzīves cikla stāvokli un kā saistīt noklusējuma stāvokli ar izlaistajām precēm.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16f604d5e06859b15c6f610e7a5c822ef2089ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966909"
---
# <a name="create-a-default-product-lifecycle-state"></a>Noklusējuma preces dzīves cikla stāvokļa izveidošana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot noklusējuma preces dzīves cikla stāvokli un kā saistīt noklusējuma stāvokli ar izlaistajām precēm.


## <a name="create-a-default-lifecycle-state"></a>Noklusējuma dzīves cikla stāvokļa izveidošana
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatīšana > Preces dzīves cikla stāvoklis.
2. Noklikšķiniet uz Jauns.
3. Laukā Stāvoklis ierakstiet vērtību.
4. Atlasiet Jā laukā Noklusējums, kad izlaists juridiskajai personai.
5. Apraksta laukā ierakstiet vērtību.
6. Laukā Ir aktīvs plānošanai atlasiet Nē.

> [!NOTE]
> Ja jauna izlaistā prece nav jāiekļauj vispārējā plānošanā, atlasiet Nē. Ja tā ir jāiekļauj vispārējā plānošanā, atstājiet vadīklas noklusējuma vērtību Jā.  

## <a name="create-a-new-released-product"></a>Jaunas izlaistās preces izveide
1. Aizvērt lapu.
2. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
3. Noklikšķiniet uz Jauns.
4. Laukā Preces numurs ierakstiet vērtību.
5. Laukā Preces nosaukums ierakstiet kādu vērtību.
6. Laukā Meklēšanas nosaukums ierakstiet kādu vērtību.
7. Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.
8. Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.
9. Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.
10. Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.
11. Noklikšķiniet uz OK.

> [!NOTE]
> Noklusējuma preces dzīves cikla stāvoklis ir globāla definīcija.  

## <a name="change-the-product-to-an-active-state"></a>Maiņa uz aktīvu statusu precei
1. Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.

> [!NOTE]
> Pieņemot, ka esat iestatījis aktīvu stāvokli, tagad ir iespējams atlasīt aktīvo stāvokli, lai ļautu preci izmantot vispārējā plānošanā un MK līmeņa aprēķinā. Protams, tam ir nozīme tikai tad, ja ir norādīta visa produkta detalizētā informācija, kas nepieciešama konsekventai plānošanai.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]