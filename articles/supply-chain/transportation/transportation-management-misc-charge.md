---
title: Transportēšanas pārvaldības papildmaksas
description: Šajā tēmā ir paskaidrots, kā transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 776c73b1a29666e393bed7c40059a578fe86cb0d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576188"
---
# <a name="transportation-management-miscellaneous-charges"></a>Transportēšanas pārvaldības papildmaksas

[!include [banner](../includes/banner.md)]

Kas attiecas uz visām papildizmaksām, transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu. Pretējā gadījumā tās netiks pievienotas pasūtījumam kā papildmaksa. **Izmaksu kods** nosaka, kā maksa tiek uzskaitīta saistībā ar pasūtījumu un pasūtījuma rindu, kur tā ir pievienota.

Dodieties uz **Transportēšanas pārvaldība > Iestatījumi > Novērtējums > Papildmaksas**, lai definētu kvalifikācijas kritērijus, kas nosaka, kad noteikts **Izmaksu kods** tiek piemērots maksai.

Katram attiecīgajam **Izmaksu moduļa** iestatījumam ir jābūt vismaz vienam iestatījumam (*Klients* un *Kreditors*), kur **Papildmaksu veids** ir iestatīts uz *Nav*. Ja tā nav, papildmaksa *netiks* pievienota pasūtījumam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]