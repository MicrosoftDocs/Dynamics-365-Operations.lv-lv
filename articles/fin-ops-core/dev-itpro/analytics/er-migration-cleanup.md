---
title: ER migrācijas tīrīšana
description: Šajā rakstā skaidrots, kā var izmantot ER migrācijas tīrīšanas funkciju, lai atrisinātu problēmas ar ER veidnēm.
author: kfend
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
ms.openlocfilehash: bf32981ed5f43647038018bf2cd98e55ce233b3f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285097"
---
# <a name="er-migration-cleanup"></a>ER migrācijas tīrīšana 

[!include[banner](../includes/banner.md)]

Kad pārvaldāt Finance instances, varat izlemt migrēt jūsu pašreizējo instanci uz citu vietu. Piemēram, jūs varat migrēt savu ražošanas instanci uz jaunu smilškastes vidi. Ja konfigurējāt Elektronisko pārskatu (ER) struktūru, lai saglabātu veidnes Microsoft Azure BLOB krātuvē, **DocuValue** tabula jaunajā sandbox vidē attiecas uz BLOB uzglabāšanas instanci ražošanas vidē. Tomēr šai instancei nevar piekļūt no smilškastes vides, jo migrēšanas process neatbalsta artefaktu migrāciju BLOB krātuvē. Drīzāk tiek prognozēts, ka jaunajā smilškastes vidē jūs atsaucaties uz BLOB glabāšanas instanci smilškastes vidē, kas vēl neiegūst ER veidnes.

Ja mēģināt palaist ER formātu, kas izmanto veidni, lai ģenerētu biznesa dokumentus, tiek veikts izņēmums, un jūs tiekat informēts par trūkstošajām veidnēm. Varat arī izmantot ER migrācijas tīrīšanas rīka opciju, lai dzēstu un pēc tam atkārtoti importētu ER formāta konfigurāciju, kas satur veidni.

[![Palaist ER formātu.](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Jūs redzēsiet līdzīgu kļūdu, ja pārvietosieties uz **Konfigurācijas** lapu (**Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Konfigurācijas**) un konfigurāciju kokā, mēģināsiet dzēst ER formāta konfigurāciju, kas izmanto veidni.

[![ER formāta dzēšana.](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Veiciet tālāk norādītās darbības, lai atrisinātu problēmas ar ER veidnēm, kurām nevarat piekļūt.

1.  Dodieties uz **Organizācijas administrēšana** \> **Periodiskie** \> **Migrācijas tīrīšana** lapu.
2.  Atlasiet ER formāta konfigurāciju, ko nevar izpildīt vai dzēst.
3.  Atlasiet **Dzēst**.
4.  Apstipriniet atlasītās ER formāta konfigurācijas dzēšanu.
5.  [Importēt](download-electronic-reporting-configuration-lcs.md) dzēsto ER formāta konfigurāciju uz pašreizējo Finance instanci.

## <a name="applicability"></a>Piemērojamība

> [Svarīgi] **Migrācijas tīrīšanas** opcija ir paredzēta tikai ER formāta konfigurācijām, kas satur nepieejamas ER veidnes. Kad dzēšat ER formāta konfigurāciju, izmantojot **Migrācijas tīrīšanas** opciju, ER dzēš veidnes, kas saistītas ar konfigurācijas artefaktiem vienīgajā programmas datu bāzē. Atbilstošu fizisko failu esamība BLOB krātuvēs nav validēta. Tā vietā tiek pieņemts, ka tādu nav. Tāpēc neizmantojiet **Migrācijas tīrīšanas** opciju kā alternatīvu ER konfigurācijas dzēšanas opcijai **Konfigurācijas** lapā. Izmantojiet **Migrācijas tīrīšanas** opciju tikai, kad ER konfigurācijas dzēšanas opcija **Konfigurācijas** lapā nav izdevusies.
>
> Ja jūs izmantojat **Migrācijas tīrīšanas** opciju, lai dzēstu ER formāta konfigurāciju, kad saistītā veidne ir pieejama Blob glabātuvē, jūs izdzēšat tikai saistītos konfigurācijas artefaktus programmas datu bāzē. Veidnes fiziskais fails BLOB krātuvē saglabājas. Failu pārrakstīšana BLOB krātuvē vairs nav atļauta. Lai iegūtu papildinformāciju, skatiet [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Turklāt vairs nevarēsiet atkārtoti importēt konfigurācijas, kas dzēstas, izmantojot šajā vidē esošo Migrācijas tīrīšanu. Lai atrisinātu šo problēmu, ir nepieciešams atrast atbilstošo failu BLOB krātuvē un to manuāli dzēst.

[![ER formāta importēšana.](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Līdzīga problēma var rasties, ja migrējat jūsu programmas instanci uz citu atrašanās vietu, kas izmantota kā migrācijas mērķis vairāk nekā vienu reizi un kam BLOB krātuvē jau ir ER veidnes faili.

Tā kā jums varētu būt vairāki ER formāta konfigurācijas, šis process var būt laikietilpīgs. Tāpēc ieteicams izmantot [ER veidņu dublējumkopiju glabātuves](er-backup-storage-templates.md) iespēju, lai automātiski atkoptu veidnes ar sarautām atsaucēm.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
