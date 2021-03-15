---
title: Pienākumu sadales iestatīšana
description: Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcbd32131f9980a4f55e91b9d7ad48171069f72e
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826398"
---
# <a name="set-up-segregation-of-duties"></a>Pienākumu sadales iestatīšana

[!include [banner](../../includes/banner.md)]

Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem. Šī koncepcija ir nosaukta par pienākumu sadali. Piemēram, iespējams, nevēlēsieties, lai viena un tā pati persona apstiprina preču saņemšanu un apstrādātu maksājumus kreditoram. Pienākumu sadale palīdz samazināt pārkāpumu risku un palīdz arī noteikt kļūdas vai neatbilstības. Pienākumu sadali var izmantot arī, lai lietotu iekšējās kontroles politikas. Lai izveidotu nosacījumus, veiciet tālākminēto procedūru. Lai izpildītu šo procedūru, jums ir jābūt sistēmas administratoram.

1. Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Pienākumu sadale** > **Pienākumu sadales nosacījumi**.
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

> [!IMPORTANT] 
> Veidojot kārtulu, pienākumu sadales kārtulas netiek pārbaudītas. Varat izveidot kārtulu, kas izveido konfliktu esošajām lomām. Esošās lietotāja lomu piešķires var arī būt pretrunā ar jauno kārtulu. Pēc kārtulas izveidošanas vai modificēšanas ir jāpārbauda atbilstība. Papildinformāciju skatiet sadaļā [Pienākumu sadales konfliktu identificēšana un atrisināšana](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]