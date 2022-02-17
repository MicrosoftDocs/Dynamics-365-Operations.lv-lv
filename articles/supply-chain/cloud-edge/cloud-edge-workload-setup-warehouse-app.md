---
title: Konfigurējiet mobilo lietotni Warehouse Management mākoņa un malu mēroga vienībām
description: Šajā tēmā ir paskaidrots, kā iestatīt noliktavas pārvaldības mobilās lietotnes noliktavām, kuras apkalpo mākoņa vai malas mēroga vienība.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071785"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurējiet mobilo lietotni Warehouse Management mākoņa un malu mēroga vienībām

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt noliktavas pārvaldības mobilās lietotnes, lai tās varētu izmantot noliktavās, kuras apkalpo mākoņa vai malas mēroga vienība.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat iestatīt mobilās ierīces, lai tās izveidotu savienojumu ar mākoņa vai malas mēroga vienību, pārbaudiet, vai tās var izveidot savienojumu ar uzņēmuma centru. Norādījumus sk [Instalējiet un pievienojiet mobilo lietotni Warehouse Management](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Papildu iestatīšana, palaižot mobilo lietotni Noliktavas pārvaldība pret mēroga vienību

Kā daļu no [izvietošanas process noliktavas mēroga vienību darba slodzēm](cloud-edge-landing-page.md#scale-unit-manager-portal), lielākā daļa datu, kas nepieciešami, lai savienotu jūsu noliktavas pārvaldības mobilās lietotnes ierīces, tiek automātiski sinhronizēti no uzņēmuma centrmezgla ar mēroga vienību. Tomēr jums ir jāievada dati uz **Azure Active Directory lietojumprogrammas** lappuse (**Sistēmas administrēšana \> Uzstādīt \>Azure Active Directory lietojumprogrammas**) par mēroga vienības izvietošanu. Turklāt, iespējams, būs jāatjaunina noklusējuma iestatījumi **Uzņēmums** vērtību lietotāja ID vai izveidot jaunu lietotāju. Lietotāji, kas ir saistīti ar uzņēmumu, kas neeksistē skalas vienības izvietošanā, nevarēs pieteikties, ja mobilā lietotne Noliktavas pārvaldība būs savienota ar šo mērogu vienību.

> [!NOTE]
> Tā kā dati par **Azure Active Directory lietojumprogrammas** lapa nav sinhronizēta, šie dati ir manuāli jāuztur, ja vēlaties pārvietot savas noliktavas darba slodzes uz citu mēroga vienību.

Atcerieties, ka katras noliktavas pārvaldības mobilās lietotnes savienojuma iestatīšanas ietvaros norādītais Azure Active Directory resursa vietrādim URL ir jāattiecas uz mēroga vienību, nevis uzņēmuma centru.
