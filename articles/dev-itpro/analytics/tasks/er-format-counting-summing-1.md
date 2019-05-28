---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (1. daļa. Formāta izveide)
description: Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f925ef8d772189a505f2793de1176756866bf4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544637"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1-create-format"></a>ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (1. daļa: Formāta izveide)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus. Šīs darbības var veikt jebkurā uzņēmumā.

Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai "Litware, Inc." ir pieejams un atzīmēts kā aktīvs.  
2. Atlasiet Litware, Inc. nodrošinātāju.
3. Noklikšķiniet uz Repozitoriji.
    * Ja tipa “Operācijas resursi” repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.  
4. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.
6. Noklikšķiniet uz Izveidot repozitoriju.
7. Noklikšķiniet uz OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Iegūt piekļuvi korporācijas Microsoft nodrošinātajām Intrastat konfigurācijām
1. Noklikšķiniet uz Atvērt.
2. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.
3. Noklikšķiniet uz Importēt.
    * Noklikšķiniet uz Atlasītās konfigurācijas versijas 1.1 importēšana.  
4. Noklikšķiniet uz Jā.
5. Aizvērt lapu.
6. Aizvērt lapu.
7. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
8. Kokā struktūrā izvērsiet 'Intrastat model'.
9. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.

