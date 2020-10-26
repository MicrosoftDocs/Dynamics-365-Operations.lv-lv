---
title: Pienākumu sadales iestatīšana
description: Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982410"
---
# <a name="set-up-segregation-of-duties"></a>Pienākumu sadales iestatīšana

[!include [banner](../../includes/banner.md)]

Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem. Šī koncepcija ir nosaukta par pienākumu sadali. Piemēram, iespējams, nevēlēsieties, lai viena un tā pati persona apstiprina preču saņemšanu un apstrādātu maksājumus kreditoram. Pienākumu sadale palīdz samazināt pārkāpumu risku un palīdz arī noteikt kļūdas vai neatbilstības. Pienākumu sadali var izmantot arī, lai lietotu iekšējās kontroles politikas. Lai izveidotu nosacījumus, veiciet tālākminēto procedūru. Lai izpildītu šo procedūru, jums ir jābūt sistēmas administratoram. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DAT. 

1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales nosacījumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kārtulas vērtību.
4. Laukā **Pirmais pienākums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet pirmo pienākumu, ko kontrolē nosacījumi.
6. Laukā **Otrais pienākums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu. 
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet otro pienākumu, ko kontrolē nosacījumi.
10. Laukā **Stingrība** atlasiet opciju. Atlasiet riska smagumu, kas rodas, ja viens un tas pats lietotājs vai loma pilda abus pienākumus.  
11. Laukā **Drošības risks** ierakstiet vērtību. Ievadiet drošības riska aprakstu.  
12. Laukā **Drošības mazinājums** ierakstiet vērtību. Ievadiet darbību parakstu, kas jāveic, lai mazinātu drošības risku. Piemēram, var mazināt risku, veicot detalizētāku procesa pārskatīšanu, veicot ikmēneša vadības pārskatīšanu vai koplietojot resursus ar citām nodaļām.     
13. Noklikšķiniet uz **Saglabāt**.

