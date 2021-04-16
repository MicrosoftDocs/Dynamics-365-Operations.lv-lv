---
title: Galvenā konta kategoriju iestatīšana
description: Šajā tēmā ir izskaidrots, kā iestatīt galvenā uzņēmuma kategorijas programmā Dynamics 365 Finance.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2dcaa27f20ca050d278aa378e90946b8cb40449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815120"
---
# <a name="set-up-main-account-categories"></a>Galvenā konta kategoriju iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā iestatīt galvenā uzņēmuma kategorijas. Galveno kontu kategorijas tiek izmantotas noklusējuma pārskatiem modulī Finanšu pārskatu izveidei un pakalpojumā Power BI. Galveno kontu kategorijas, kas tiek izveidotas pēc noklusējuma, var pārdēvēt, bet nevar dzēst. Papildu kontu kategorijas var izveidot un izmantot pārskata un analīzes nolūkiem. Šajā tēmā tiek izmantots USMF demonstrācijas uzņēmums.

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