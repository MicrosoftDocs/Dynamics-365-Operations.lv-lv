---
title: Warehouse Management mobilās lietotnes konfigurēšana mākoņa un malas mēroga vienībām
description: Šajā rakstā ir izskaidrots, kā iestatīt noliktavas pārvaldības mobilās programmas noliktavām, kuras apkalpo mākoņa vai malas mēroga vienība.
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
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865243"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Warehouse Management mobilās lietotnes konfigurēšana mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt noliktavas pārvaldības mobilās programmas, lai tās varētu lietot noliktavās, kuras apkalpo mākoņa vai malas mēroga vienība.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat iestatīt mobilās ierīces savienojumam ar mākoņa vai malas skalas vienību, apstipriniet, ka tās var izveidot savienojumu ar uzņēmuma pārkraušanas vietu. Norādījumus skatiet šeit: [Noliktavas pārvaldības mobilās programmas instalēšana un savienošana](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Papildu iestatīšana, kad izmantojat mobilo programmu Noliktavas pārvaldība attiecībā pret mēroga vienību

Kā daļa no [noliktavas mēroga vienības darba noslodzes izvietošanas procesa, lielākā daļa datu, kas ir nepieciešami noliktavas pārvaldības mobilās](cloud-edge-landing-page.md#scale-unit-manager-portal) programmas ierīču savienošanai, tiek automātiski sinhronizēta no uzņēmuma pārkraušanas centra uz mēroga vienību. Tomēr, jums jāievada dati uz lietojumprogrammu **Azure Active Directory lapas** (Sistēmas **administrēšanas iestatīšanas \>\>Azure Active Directory programmas**), kas atrodas mēroga vienības izvietošanā. Turklāt, iespējams, jāatjaunina noklusētā **uzņēmuma** vērtība lietotāja ID vai jāizveido jauns lietotājs. Lietotāji, kas ir saistīti ar uzņēmumu, kurš nepastāv mēroga vienības izvietošanā, nevarēs pieteikties, ja noliktavas pārvaldības mobilā programma ir saistīta ar šo mēroga vienību.

> [!NOTE]
> Tā kā dati **Azure Active Directory programmu lapā** nav sinhronizēti, šie dati ir jāsaglabā manuāli, ja vēlaties pārvietot noliktavas darba slodzi uz citu mēroga vienību.

Atcerieties, ka kā daļa no katras noliktavas pārvaldības mobilās programmas savienojuma iestatījuma, Azure Active Directory uzņēmuma pārkraušanas centra vietā norādītajam resursa VIETRĀDIm URL ir jābūt mēroga vienībai.
