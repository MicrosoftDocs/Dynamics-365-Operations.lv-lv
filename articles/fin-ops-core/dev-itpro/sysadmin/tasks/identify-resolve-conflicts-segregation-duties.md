---
title: Pienākumu sadales konfliktu identificēšana un atrisināšana
description: Šajā tēmā ir paskaidrots, kā identificēt un atrisināt pienākumu sadales konfliktus.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0638699c0e569bbe67024a87d6c55729642557cb085ee899aa98aa0022b12840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748316"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Pienākumu sadales konfliktu identificēšana un atrisināšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā identificēt un atrisināt pienākumu sadales konfliktus. Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem. Šī koncepcija ir nosaukta par pienākumu sadali. Ja drošības lomas definīcija vai lietotāju lomu piešķires pārkāpj noteikumus, tiek reģistrēts konflikts. Visi konflikti ir jāatrisina administratoram. Lai identificētu un atrisinātu konfliktus, veiciet sekojošo procedūru.

Pēc kārtulas pievienošanas pārbaudiet, vai visas esošās lomas ir saderīgas. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Pārbaudiet, vai esošās lomas atbilst jaunajiem nosacījumiem par pienākumu sadali
1. Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Pienākumu sadale** > **Pienākumu sadales nosacījumi**.
3. Atlasiet **Apstiprināt pienākumus un lomas**. Ja jebkuras esošās lomas pārkāpj kārtulas, tiek parādīts ziņojums, kas ietver kārtulas nosaukumu, lomu un konfliktējošo pienākumu nosaukumus. Konfliktējošās lomas ir jāpārkonfigurē, izmantojot **Drošības konfigurāciju**, un tās nevar ietvert konfliktējošos pienākumus. Ja neviena loma nepārkāpj atlasīto kārtulu, ziņojumā norādīts, ka visas lomas ir atbilstošas.   

> [!NOTE]
> Apstiprināšana tiek veikta tikai atlasītajai kārtulai. Ir svarīgi pārbaudīt katras kārtulas atbilstību.   

Kad tiek izveidota vai modificēta loma, automātiski tiek ieviestas pienākumu sadales kārtulas. Lomai nevar piešķirt konfliktējošos pienākumus.

Pēc tam pārbaudiet, vai visas esošās lomu piešķires ir saderīgas.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Pārbaude, vai lietotāju lomu piešķires atbilst jaunajām kārtulām par pienākumu sadali
1. Dodieties uz **Sistēmas administrēšana > Drošība > Pienākumu sadale > Pārbaudīt lietotāja lomu norīkojumu atbilstību**.
2. Atlasiet **Labi**. Paziņojumā tiek parādīti pārbaudes rezultāti. Konflikti tiek arī reģistrēti lapā **Pienākumu sadales konflikti**.   

Kad lietotājiem tiek piešķirtas lomas, automātiski tiek ieviestas pienākumu sadales kārtulas. Mēģinot piešķirt lietotāju lomām, kas ietver konfliktējošus pienākumus, saņemat kļūdas ziņojumu. Pēc tam jums ir jāatrisina konflikts, liedzot vai atļaujot papildu lomas piešķiri. Pēc piešķires piešķiršanas tiks piešķirta papildu loma. 

> [!NOTE]
> Konflikti pašlaik nav pārbaudīti lietotājiem, kuriem ir piešķirtas lomas, pamatojoties uz Active Directory Domain grupām.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Konfliktējošo lietotāju lomu piešķiru skatīšana un atrisināšana
1. Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Pienākumu sadale** > **Pienākumu sadales neatrisinātie konflikti**. 
2. Atlasiet konfliktu un pēc tam atlasiet vienu no šīm darbībām: 

  - **Noraidīt piešķiri**: noraidīt papildu drošības lomas piešķiri lietotājam. Liedzot automātisko lomu piešķiri, lietotājs tiek atzīmēts kā izslēgts no lomas. Izslēgtam lietotājam nav piešķirta piekļuve, kas ir saistīta ar lomu, un lietotāju nevar piešķirt lomai, kamēr administrators nenoņems izslēgšanu. 
-  **Atļaut piešķiri**: ignorēt konfliktu un atļaut piešķirt lietotāju abām drošības lomām. Ja ignorējat konfliktu, laukā **Ignorēšanas pamatojums** jāievada pamatojums. Visas ignorētās lomu piešķires var skatīt **Pienākumu sadales konfliktu** lapā.  

> [!NOTE]
> Ja vienam un tam pašam lietotājam ir norādīti vairāki konflikti, atlasiet lietotāja ierakstu un novērtējiet **Lietotāju** lapā piešķirtās lomas. Lai izvairītos no šī konflikta, apstipriniet katru kārtulu pēc tās pievienošanas vai modificēšanas.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]