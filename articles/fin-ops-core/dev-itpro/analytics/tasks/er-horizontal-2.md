---
title: ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (2. daļa. Formāta palaišana)
description: Šajā rakstā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus kā OPENXML darblapas (Excel) failus. (2. daļa)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, SysQueryForm
ms.openlocfilehash: 08755eafa2a18993ba669f0deccd75477bfae410
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290400"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (2. daļa. Formāta palaišana)

[!include [banner](../../includes/banner.md)]

Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes. Šīs darbības var veikt uzņēmumā DEMF.

Lai izpildītu šos soļus, vispirms ir jāpabeidz procedūras "ER Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos (1. daļa: Izstrādāt formātu)" darbības.

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
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka tikko izveidotais Excel fails ietver finanšu dimensijām atlasīto kolonnu skaitu. Pārskata galvenē šajās kolonnās ir norādīti finanšu dimensiju nosaukumi. Transakcijas rindās šajās kolonnās ir norādītas finanšu dimensijas. Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskatu nav atkarīgs no atlasīto dimensiju skaita, vai dimensiju skaita, kas ir konfigurētas šai instancei.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
