---
title: Pienākumu sadales konfliktu identificēšana un atrisināšana
description: Šajā tēmā ir paskaidrots, kā identificēt un atrisināt pienākumu sadales konfliktus.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69dabb44ef08bf798b86cd031536146880c8fd40
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982482"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Pienākumu sadales konfliktu identificēšana un atrisināšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā identificēt un atrisināt pienākumu sadales konfliktus. Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem. Šī koncepcija ir nosaukta par pienākumu sadali. Ja drošības lomas definīcija vai lietotāju lomu piešķires pārkāpj noteikumus, tiek reģistrēts konflikts. Visi konflikti ir jāatrisina administratoram. Lai identificētu un atrisinātu konfliktus, veiciet sekojošo procedūru. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Pārbaude, vai lietotāju lomu piešķires atbilst jaunajiem nosacījumiem par pienākumu sadali
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Pienākumu sadale > Pārbaudīt lietotāja lomu norīkojumu atbilstību**.
2. Atlasiet **Labi**. Paziņojumā tiek parādīti pārbaudes rezultāti. Ja pastāv konflikts, var atvērt lapu **Lietotāji** un mainīt lietotāja lomu piešķires. Konflikti tiek arī reģistrēti lapā **Pienākumu sadales konflikti**. Lai palaistu pārbaudes procesu kā pakešuzdevumu, atlasiet **Pakešapstrāde** un pēc tam iestatiet citus pakešuzdevumu parametrus. Kad pakešuzdevums tiks izpildīts, var pārskatīt konfliktus lapā **Pienākumu sadales konflikti**.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Konfliktējošo lietotāju lomu piešķiru skatīšana un atrisināšana
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales konflikti.** Atlasiet konfliktu un pēc tam atlasiet vienu no šīm pogām: **Noraidīt piešķiri — noraidīt lietotāja piešķiri papildu drošības lomai**. Liedzot automātisko lomu piešķiri, lietotājs tiek atzīmēts kā izslēgts no lomas. Izslēgtam lietotājam nav piešķirta piekļuve, kas ir saistīta ar lomu, un lietotāju nevar piešķirt lomai, kamēr administrators nenoņems izslēgšanu. Atļaut piešķiri — **Ignorēt** konfliktu un atļaut piešķirt lietotāju abām drošības lomām. Ja ignorējat konfliktu, laukā **Ignorēšanas pamatojums** jāievada pamatojums.  
2. Aizvērt lapu.
3. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales neatrisinātie konflikti.** Atlasiet konfliktu un pēc tam atlasiet vienu no šīm pogām: **Noraidīt piešķiri — noraidīt lietotāja piešķiri papildu drošības lomai**. Liedzot automātisko lomu piešķiri, lietotājs tiek atzīmēts kā izslēgts no lomas. Izslēgtam lietotājam nav piešķirta piekļuve, kas ir saistīta ar lomu, un lietotāju nevar piešķirt lomai, kamēr administrators nenoņems izslēgšanu. Atļaut piešķiri — **Ignorēt** konfliktu un atļaut piešķirt lietotāju abām drošības lomām. Ja ignorējat konfliktu, jāievada pamatojums laukā **Ignorēšanas pamatojums**.    
4. Aizvērt lapu.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Pārbaude, vai esošās lomas atbilst jaunajiem nosacījumiem par pienākumu sadali
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales nosacījumi**. Atlasiet nosacījumu.  
2. Atlasiet **Apstiprināt pienākumus un lomas**. Ja jebkuras esošās lomas pārkāpj atlasīto nosacījumu, tiek parādīts ziņojums, kas ietver lomas nosaukumu un konfliktējošo pienākumu nosaukumus. Administratoram vai nu jānorāda drošības riska mazinājums vai jāmodificē loma, lai tā nepārkāptu pienākumu sadales nosacījumus. Ja neviena loma nepārkāpj atlasīto nosacījumu, ziņojumā norādīts, ka visas lomas ir atbilstošas.  

