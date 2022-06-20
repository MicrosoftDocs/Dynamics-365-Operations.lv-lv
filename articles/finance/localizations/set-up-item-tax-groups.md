---
title: Krājumu nodokļu grupu iestatīšana
description: Šajā rakstā skaidrots, kā iestatīt krājumu nodokļu grupas nodokļu aprēķināšanas pakalpojumā.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3bc705bc8173ad2bc8ef883e6dc80b0a187314ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846468"
---
# <a name="set-up-item-tax-groups"></a>Krājumu nodokļu grupu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt krājumu nodokļu grupas nodokļu aprēķināšanas pakalpojumā. Šeit skaidrots arī, kā iestatīt krājuma nodokļu grupas piemērojamības noteikuma matricu un konfigurēt rindas matricā.

Krājumu nodokļu grupu koncepcija nodokļu aprēķināšanas pakalpojumā ir līdzīga krājumu PVN grupu koncepcijai Microsoft Dynamics 365 Finansēs. Tās ir nodokļu kodu grupas. Nodokļu aprēķināšanas pakalpojums nodokļu kodu noteikšanai izmanto nodokļu grupas un krājumu nodokļu grupas iespēju.

> [!IMPORTANT]
> Krājumu nodokļu grupu iestatījumi nodokļu aprēķināšanas pakalpojumā ir juridiska persona – diagnostika. Šo iestatījumu varat pabeigt regulēšanas konfigurācijas pakalpojumā (RCS) tikai vienu reizi. Iespējojot nodokļu aprēķināšanas pakalpojumu finansēs, atlasītajai juridiskajai personai krājumu nodokļu grupas tiek automātiski sinhronizētas.

## <a name="set-up-an-item-tax-group"></a>Krājumu PVN grupas iestatīšana 

Sekojiet šiem soļiem, lai iestatītu vienību PVN grupu.

1. Piesakieties regulēšanas [konfigurācijas pakalpojumā](https://marketing.configure.global.dynamics.com/).
2. Doties uz darbvietām **globalizācijas** \> **līdzekļu nodokļu** \> **aprēķins.**
3. Atlasiet līdzekli un versiju, kuru vēlaties iestatīt, un pēc tam atlasiet **Rediģēt**.
4. **Cilnē Vispārīgi** atlasiet Konfigurācijas **versija**.
5. **Cilnē Krājumu NODOKĻU grupa** atlasiet kolonnu **Pārvaldīt**. Ja krājumu nodokļu grupu iestatāt pirmo reizi, lauki kolonnā Pārvaldīt **tiek** iestatīti automātiski.
6. Sarakstā pa kreisi izvērsiet mezglu **Rindas** un atzīmējiet izvēles rūtiņu krājuma **PVN grupai**.

    ![Krājumu NODOKĻU grupa, kas atlasīta zem zara Rindas dialoglodziņā Pārvaldīt kolonnas.](media/select-item-tax-group.png)

7. Atlasiet labās bultiņas pogu, lai **labajā pusē** atlasītajam kolonnu **sarakstam** pievienotu krājumu nodokļu grupu.

    ![Krājumu nodokļu grupa pievienota atlasīto kolonnu sarakstam.](media/add-item-tax-group.png)

8. Atlasiet **Labi**.

## <a name="configure-an-item-tax-group"></a>Konfigurēt krājuma nodokļu grupu

Pēc krājumu nodokļu grupas iestatīšanas tiek izveidota piemērojamības noteikuma matrica. Varat pievienot rindas matricai, lai konfigurētu krājumu nodokļu grupu.

1. **Cilnē Krājumu nodokļu grupa** atlasiet **Pievienot**.
2. **Laukā Krājumu PVN** grupa ievadiet krājumu PVN grupas nosaukumu.

    > [!IMPORTANT]
    > Ieteicams krājuma nodokļu grupas nosaukumu ierobežot līdz 10 rakstzīmēm. Šis nosaukums tiek sinhronizēts ar Finansēm, kas krājumu PVN grupu nosaukumiem ierobežo 10 rakstzīmes.

3. Laukā **Nodokļu** kodi atzīmējiet izvēles rūtiņu katram nodokļa kodam, ko vēlaties iekļaut krājumu nodokļu grupā. Vienā krājumu NODOKĻU grupā var iekļaut vairākus nodokļu kodus.

    ![Vairāki nodokļu kodi, kas atlasīti nodokļu kodu laukā.](media/multiple-tax-codes-selection.png)

4. Atkārtojiet no 1. līdz 3. solim, lai pievienotu vairāk krājumu NODOKĻU grupu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
