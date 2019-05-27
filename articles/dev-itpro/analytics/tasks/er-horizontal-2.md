---
title: ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (2. daļa. Formāta palaišana)
description: Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33c1a3134659bb66a67166fec3d7f53af0aa4c6c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544430"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2-run-format"></a>ER izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas programmas Excel pārskatos (2. daļa: Palaist formātu)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes. Šīs darbības var veikt uzņēmumā DEMF.

Lai izpildītu šos soļus, vispirms ir jāpabeidz procedūras “ER Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos (1. daļa: Izstrādāt formātu)“ darbības.

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="find-created-format"></a>Atrast izveidoto formātu
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.
3. Koka struktūrā atlasiet 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.

## <a name="execute-format-to-create-excel-output"></a>Izpildīt formātu, lai izveidotu Excel izvadi
1. Noklikšķiniet uz Palaist.
2. Laukā Dimensijas ierakstiet 'BusinessUnit;CostCenter;Department'.
    * Ievadiet vai atlasiet vērtību laukā Dimensijas nosaukums.  Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Izvērsiet sadaļu Iekļaujamie ieraksti.
4. Noklikšķiniet uz Filtrēt.
5. Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.
6. Laukā Kritēriji ierakstiet '00057..00058'.
    * 00057..00058  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka tikko izveidotais Excel fails ietver finanšu dimensijām atlasīto kolonnu skaitu. Pārskata galvenē šajās kolonnās ir norādīti finanšu dimensiju nosaukumi. Transakcijas rindās šajās kolonnās ir norādītas finanšu dimensijas. Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskats nav atkarīgs no atlasīto dimensiju skaita vai dimensiju skaita, kas ir konfigurētas šai Dynamics 365 for Finance and Operations Enterprise edition instancei.  

