--- 
title: "Pienākumu sadales konfliktu identificēšana un atrisināšana"
description: "Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Pienākumu sadales konfliktu identificēšana un atrisināšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem. Šī koncepcija ir nosaukta par pienākumu sadali. Ja drošības lomas definīcija vai lietotāju lomu piešķires pārkāpj noteikumus, tiek reģistrēts konflikts. Visi konflikti ir jāatrisina administratoram. Lai identificētu un atrisinātu konfliktus, veiciet sekojošo procedūru. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Pārbaude, vai lietotāju lomu piešķires atbilst jaunajiem nosacījumiem par pienākumu sadali
1. Dodieties uz Sistēmas administrēšana > Drošība > Pienākumu sadale > Pārbaudīt lietotāja lomu norīkojumu atbilstību.
2. Noklikšķiniet uz OK.
    * Paziņojumā tiek parādīti pārbaudes rezultāti.     Ja pastāv konflikts, var atvērt lapu Lietotāji un mainīt lietotāja lomu piešķires. Konflikti tiek arī reģistrēti lapā Pienākumu sadales konflikti.     Lai palaistu pārbaudes procesu kā pakešuzdevumu, atlasiet Pakešapstrāde un pēc tam iestatiet pakešuzdevumu parametrus. Kad pakešuzdevums tiks izpildīts, var pārskatīt konfliktus lapā Pienākumu sadales konflikti.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Konfliktējošo lietotāju lomu piešķiru skatīšana un atrisināšana
1. Dodieties uz Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales konflikti.
    * Atlasiet konfliktu un pēc tam noklikšķiniet uz vienas no šīm pogām: Noraidīt piešķiri — noraidīt lietotāja piešķiri papildu drošības lomai. Liedzot automātisko lomu piešķiri, lietotājs tiek atzīmēts kā izslēgts no lomas. Izslēgtam lietotājam nav piešķirta piekļuve, kas ir saistīta ar lomu, un lietotāju nevar piešķirt lomai, kamēr administrators nenoņems izslēgšanu.     Atļaut piešķiri — ignorēt konfliktu un atļaut piešķirt lietotāju abām drošības lomām. Ja jūs ignorējat konfliktu, laukā Ignorēšanas pamatojums jāievada pamatojums.  
2. Aizvērt lapu.
3. Dodieties uz Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales neatrisinātie konflikti.
    * Atlasiet konfliktu un pēc tam noklikšķiniet uz vienas no šīm pogām: Noraidīt piešķiri — noraidīt lietotāja piešķiri papildu drošības lomai. Liedzot automātisko lomu piešķiri, lietotājs tiek atzīmēts kā izslēgts no lomas. Izslēgtam lietotājam nav piešķirta piekļuve, kas ir saistīta ar lomu, un lietotāju nevar piešķirt lomai, kamēr administrators nenoņems izslēgšanu.     Atļaut piešķiri — ignorēt konfliktu un atļaut piešķirt lietotāju abām drošības lomām. Ja jūs ignorējat konfliktu, laukā Ignorēšanas pamatojums jāievada pamatojums.    
4. Aizvērt lapu.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Pārbaude, vai esošās lomas atbilst jaunajiem nosacījumiem par pienākumu sadali
1. Dodieties uz Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales nosacījumi.
    * Atlasiet nosacījumu.  
2. Noklikšķiniet uz Apstiprināt pienākumus un lomas.
    * Ja jebkuras esošās lomas pārkāpj atlasīto nosacījumu, tiek parādīts ziņojums, kas ietver lomas nosaukumu un konfliktējošo pienākumu nosaukumus. Administratoram vai nu jānorāda drošības riska mazinājums vai jāmodificē loma, lai tā nepārkāptu pienākumu sadales nosacījumus.     Ja neviena loma nepārkāpj atlasīto nosacījumu, ziņojumā norādīts, ka visas lomas ir atbilstošas.  


