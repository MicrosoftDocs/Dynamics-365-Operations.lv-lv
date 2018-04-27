--- 
title: "Tā formāta darbināšana, kurā ir izmantoti horizontāli paplašināmi diapazoni, lai Excel pārskatos dinamiski pievienotu kolonnas"
description: "Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2d705d0d2803b5254adc27e6715c1eac311898a7
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a>Tā formāta darbināšana, kurā ir izmantoti horizontāli paplašināmi diapazoni, lai Excel pārskatos dinamiski pievienotu kolonnas

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka tikko izveidotais Excel fails ietver finanšu dimensijām atlasīto kolonnu skaitu. Pārskata galvenē šajās kolonnās ir norādīti finanšu dimensiju nosaukumi. Transakcijas rindās šajās kolonnās ir norādītas finanšu dimensijas. Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskats nav atkarīgs no atlasīto dimensiju skaita vai no šai Dynamics 365 for Finance and Operations instancei konfigurēto dimensiju skaita.  


