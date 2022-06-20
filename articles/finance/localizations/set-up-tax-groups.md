---
title: Nodokļu grupu iestatīšana
description: Šajā rakstā ir izskaidrots, kā iestatīt nodokļu grupas nodokļu aprēķināšanas pakalpojumā.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862904"
---
# <a name="set-up-tax-groups"></a>Nodokļu grupu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt nodokļu grupas nodokļu aprēķināšanas pakalpojumā. Tajā ir arī izskaidrots, kā iestatīt nodokļu grupas piemērojamības noteikuma matricu un konfigurēt rindas matricā.

Nodokļu grupu koncepcija nodokļu aprēķināšanas Microsoft Dynamics pakalpojumā ir līdzīga 365 finanšu PVN grupu koncepcijai. Tās ir nodokļu kodu grupas. Nodokļu aprēķināšanas pakalpojums nodokļu kodu noteikšanai izmanto nodokļu grupas un krājumu nodokļu grupas iespēju.

Tomēr nodokļu aprēķina pakalpojumu nodokļu grupas atšķiras no Finanšu PVN grupām, jo tām nav papildu parametru, piemēram, **Izmantot** nodokli un **Neapliekamā nodokļa**. Tā vietā šie parametri ir pieejami nodokļu koda līmenī.

> [!IMPORTANT]
> Nodokļu grupu iestatījums nodokļu aprēķināšanas pakalpojumā ir juridiska persona – diagnostika. Šo iestatījumu varat pabeigt regulēšanas konfigurācijas pakalpojumā (RCS) tikai vienu reizi. Iespējojot nodokļu aprēķināšanas pakalpojumu finansēs, atlasītajai juridiskajai personai nodokļu grupas tiek automātiski sinhronizētas.

## <a name="set-up-a-tax-group"></a>Nodokļu grupas iestatīšana

Izpildiet šīs darbības, lai iestatītu nodokļu grupu.

1. Piesakieties regulēšanas [konfigurācijas pakalpojumā](https://marketing.configure.global.dynamics.com/).
2. Doties uz darbvietām **globalizācijas** \> **līdzekļu nodokļu** \> **aprēķins.**
3. Atlasiet līdzekli un versiju, kuru vēlaties iestatīt, un pēc tam atlasiet **Rediģēt**.
4. **Cilnē Vispārīgi** atlasiet Konfigurācijas **versija**.
5. **Cilnē Nodokļu grupa** atlasiet Pārvaldīt **kolonnu**. Ja nodokļu grupu iestatāt pirmo reizi, lauki kolonnā Pārvaldīt **tiek** iestatīti automātiski.
6. Sarakstā pa kreisi izvērsiet mezglu **Rindas** un atzīmējiet izvēles rūtiņu nodokļu **grupai**.

    ![Nodokļu grupa, kas atlasīta zem zara Rindas dialoglodziņā Pārvaldīt kolonnas.](media/select-tax-group.png)

7. Atlasiet labās bultiņas pogu, lai **labajā** pusē atlasītajam **kolonnu sarakstam** pievienotu nodokļu grupu.

    ![Nodokļu grupa pievienota atlasīto kolonnu sarakstam.](media/add-tax-group.png)

8. Atlasiet **Labi**.

## <a name="configure-a-tax-group"></a>Konfigurēt nodokļu grupu

Pēc nodokļu grupas iestatīšanas tiek izveidota nodokļu grupas piemērojamības noteikuma matrica. Varat pievienot rindas matricai, lai konfigurētu NODOKĻU grupu.

1. **Cilnē Nodokļu grupa** atlasiet **Pievienot**.
2. **Laukā Nodokļu** grupa ievadiet PVN grupas nosaukumu.

    > [!IMPORTANT]
    > Ieteicams nodokļu grupas nosaukumu ierobežot līdz 10 rakstzīmēm. Šis nosaukums tiek sinhronizēts ar Finansēm, kas PVN grupu nosaukumiem ierobežo 10 rakstzīmes.

3. Laukā **Nodokļu** kodi atzīmējiet izvēles rūtiņu katram nodokļa kodam, ko vēlaties iekļaut nodokļu grupā. Vienā nodokļu grupā var iekļaut vairākus nodokļu kodus.

    ![Vairāki nodokļu kodi, kas atlasīti nodokļu kodu laukā.](media/multiple-tax-codes-selection.png)

4. Atkārtojiet no 1. līdz 3. solim, lai pievienotu vairāk NODOKĻU grupu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
