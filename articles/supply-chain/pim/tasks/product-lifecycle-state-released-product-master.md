---
title: Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam
description: Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62078025623a0cfc1ed6797c84907c7872dfaf38095855240b306e08f3decca7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716520"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem. Priekšnosacījums: pirms šī uzdevuma ceļveža atskaņošanas nepieciešams atskaņot uzdevumu ceļvedi “Jauna preces dzīves cikla stāvokļa izveidošana", lai pārliecinātos, ka ir izveidots vismaz viens preces dzīves cikla stāvoklis.


## <a name="find-a-released-product-master"></a>Izlaista preces šablona atrašana
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

> [!NOTE]
> Preces šablonam preces apakštips ir Preces šablons.  

## <a name="update-the-lifecycle-state"></a>Dzīves cikla stāvokļa atjaunināšana
1. Noklikšķiniet uz Rediģēt.
2. Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.
3. Noklikšķiniet uz Saglabāt.
4. Noklikšķiniet uz Jā.

> [!NOTE]
> Atlasot Jā, visi saistītie izlaistās preces varianti, kuriem ir tāds pats sākotnējais stāvoklis kā izlaistās preces šablonam, arī tiek atjaunināti uz jauno preces dzīves cikla stāvokli. Atlasot Nē, visiem variantiem tiek saglabāts pašreizējais stāvoklis. Varianti, kuriem ir atšķirīgs preces dzīves cikla stāvoklis no izlaistās preces šablona, netiek atjaunināti.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Variantu dzīves cikla stāvokļa pārbaude
1. Noklikšķiniet uz Izlaisto preču varianti.

> [!NOTE]
> Ņemiet vērā, ka visi varianti pārmanto atlasīto dzīves cikla stāvokli no izlaistās preces šablona.  

2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]