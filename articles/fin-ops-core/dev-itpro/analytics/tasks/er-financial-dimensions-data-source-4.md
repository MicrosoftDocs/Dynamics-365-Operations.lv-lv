---
title: ER finanšu dimensijas, ko izmanto kā datu avotu (4. daļa. Pārskata palaišana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (4. daļa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f14be560ab014224e32169b4ac97682a669249b4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605309"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER finanšu dimensijas, ko izmanto kā datu avotu (4. daļa. Pārskata palaišana)

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem. Šīs darbības var veikt uzņēmumā DEMF.

Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (3. daļa: Pārskata izkārtošana). Jums nepieciešams konfigurēt arī noklusējuma dokumentu veidus Elektronisko pārskatu veidošanas parametru lapā. Noklusējuma dokumentu veidi tiek iestatīti arī lejupielādējot un importējot jebkādu ER konfigurāciju. 


## <a name="run-report"></a>Palaist pārskatu
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.
3. Kokā atlasiet 'Finanšu dimensiju parauga modelis\Virsgrāmatas žurnāla pārskats'.
4. Noklikšķiniet uz Palaist.
![ER konfigurāciju lapa.](../media/er-financial-dimensions-guides-run1.png)
5. Ievadiet vai atlasiet vērtību laukā Dimensijas nosaukums.
    * Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![Elektroniskā pārskata parametru slaids, nolaižamā saraksta dimensijas nosaukums.](../media/er-financial-dimensions-guides-run2.png)
6. Izvērsiet sadaļu Iekļaujamie ieraksti.
7. Noklikšķiniet uz Filtrēt.
8. Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.
9. Laukā Kritēriji ierakstiet '00057'.
10. Noklikšķiniet uz Labi.
11. Noklikšķiniet uz Labi.
![Elektroniskā pārskata parametru slaids, Pārskati, kas ietver sadaļu.](../media/er-financial-dimensions-guides-run3.png)
    * Pārskatiet ģenerēto izvadi. Katrai darbībai no izvēlētās partija, tiek piedāvātas finanšu dimensijas no atbilstošajām dimensijām. Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskatu nav atkarīgs no atlasīto dimensiju skaita, vai dimensiju skaita, kas ir konfigurētas šai instancei.  
![ER konfigurācijas ģenerētā izvade.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
