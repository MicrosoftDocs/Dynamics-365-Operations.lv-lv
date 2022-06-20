---
title: Transportēšanas pārvaldības papildmaksas
description: Šajā rakstā ir izskaidrots, kā transportēšanas ģenerētās maksas ir jāsaista ar maksas kodu.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cc4c595d8b61cb9b6c81af4bf7f03faa1a12960
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849218"
---
# <a name="transportation-management-miscellaneous-charges"></a>Transportēšanas pārvaldības papildmaksas

[!include [banner](../includes/banner.md)]

Kas attiecas uz visām papildizmaksām, transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu. Pretējā gadījumā tās netiks pievienotas pasūtījumam kā papildmaksa. **Izmaksu kods** nosaka, kā maksa tiek uzskaitīta saistībā ar pasūtījumu un pasūtījuma rindu, kur tā ir pievienota.

Dodieties uz **Transportēšanas pārvaldība > Iestatījumi > Novērtējums > Papildmaksas**, lai definētu kvalifikācijas kritērijus, kas nosaka, kad noteikts **Izmaksu kods** tiek piemērots maksai.

Katram attiecīgajam **Izmaksu moduļa** iestatījumam ir jābūt vismaz vienam iestatījumam (*Klients* un *Kreditors*), kur **Papildmaksu veids** ir iestatīts uz *Nav*. Ja tā nav, papildmaksa *netiks* pievienota pasūtījumam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]