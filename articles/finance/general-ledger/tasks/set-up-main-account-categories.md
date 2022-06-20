---
title: Galvenā konta kategoriju iestatīšana
description: Šajā rakstā skaidrots, kā iestatīt galvenās konta kategorijas Dynamics 365 finansēs.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c48011c9988bdca694851476540db574efef7909
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879568"
---
# <a name="set-up-main-account-categories"></a>Galvenā konta kategoriju iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt galvenā konta kategorijas. Galveno kontu kategorijas tiek izmantotas noklusējuma pārskatiem modulī Finanšu pārskatu izveidei un pakalpojumā Power BI. Galveno kontu kategorijas, kas tiek izveidotas pēc noklusējuma, var pārdēvēt, bet nevar dzēst. Papildu kontu kategorijas var izveidot un izmantot pārskata un analīzes nolūkiem. Šajā rakstā tiek lietots USMF demonstrācijas uzņēmums.

## <a name="create-a-main-account-category"></a>Galvenā konta kategorijas izveide
1. Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Uzņēmumu diagramma > Uzņēmumi >Galvenā uzņēmuma kategorijas**.
2. Atlasiet **Jauns**.
3. Lodziņā **Galvenā uzņēmuma kategorijas** ievadiet unikālu lauka nosaukumu.
4. Laukā **Apraksta lauks** ievadiet galvenā uzņēmuma kategorijas aprakstu.
5. Laukā **Galvenā uzņēmuma veids** atlasiet galvenā uzņēmuma veidu, kas tiks sasaistīts ar kategoriju.

## <a name="link-main-accounts-to-account-category"></a>Galveno kontu saistīšana ar kontu kategoriju
1. Noklikšķiniet uz **Sasaistīt galvenos kontus**.
2. Sarakstā atlasiet galvenos uzņēmumus, lai piešķirtu galvenā uzņēmuma kategoriju, atzīmējot rūtiņas kolonnā **Saistīts**. Ja galvenos kontus piešķirt galveno kontu kategorijai, kontu bilances tiks apkopotas, kad šī kategorija tiks izmantota finanšu pārskatiem un analīzei.  
3. Atlasiet vai notīriet opciju **Saistīts**, lai izvēlētos galvenos kontus.
4. Atlasiet **Labi**.
5. Atlasiet **Jā**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
