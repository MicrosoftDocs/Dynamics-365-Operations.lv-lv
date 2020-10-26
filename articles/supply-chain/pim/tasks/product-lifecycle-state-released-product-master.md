---
title: Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam
description: Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981138"
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

