---
title: Transportēšanas pārvaldības papildmaksas
description: Šajā tēmā ir paskaidrots, kā transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433248"
---
# <a name="transportation-management-miscellaneous-charges"></a>Transportēšanas pārvaldības papildmaksas

[!include [banner](../includes/banner.md)]

Kas attiecas uz visām papildizmaksām, transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu. Pretējā gadījumā tās netiks pievienotas pasūtījumam kā papildmaksa. **Izmaksu kods** nosaka, kā maksa tiek uzskaitīta saistībā ar pasūtījumu un pasūtījuma rindu, kur tā ir pievienota.

Dodieties uz **Transportēšanas pārvaldība > Iestatījumi > Novērtējums > Papildmaksas**, lai definētu kvalifikācijas kritērijus, kas nosaka, kad noteikts **Izmaksu kods** tiek piemērots maksai.

Katram attiecīgajam **Izmaksu moduļa** iestatījumam ir jābūt vismaz vienam iestatījumam (*Klients* un *Kreditors*), kur **Papildmaksu veids** ir iestatīts uz *Nav*. Ja tā nav, papildmaksa *netiks* pievienota pasūtījumam.
