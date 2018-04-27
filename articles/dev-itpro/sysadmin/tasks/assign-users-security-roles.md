--- 
title: "Piešķirt lietotājus drošības lomām"
description: "Lai piekļūtu programmai Microsoft Dynamics 365 for Finance and Operations, lietotājiem jābūt piešķirtai drošības lomai."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: da96ec8357ea209fd958e32ab438b13e668735df
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---
# <a name="assign-users-to-security-roles"></a>Drošības lomu piešķiršana lietotājiem

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Lai piekļūtu programmai Microsoft Dynamics 365 for Finance and Operations, lietotājiem jābūt piešķirtai drošības lomai. Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="automatically-assign-users-to-roles"></a>Automātiski piešķirt lietotājus lomām
1. Dodieties uz Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem.
2. Kokā atlasiet 'Uzskaites supervizors'.
    * Atlasiet lomu, kurai vēlaties konfigurēt kārtulu. Šajā piemērā atlasiet Uzskaites supervizoru.  
3. Noklikšķiniet uz Pievienot kārtulu, lai atvērtu nolaižamo dialoglodziņu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.  
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz Rediģēt vaicājumu.
    * Rediģējiet vaicājumu pēc nepieciešamības.  
7. Noklikšķiniet uz OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Izslēgt lietotājus no automātiskas lomu piešķiršanas
1. Aizvērt lapu.
2. Dodieties uz Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem.
3. Kokā atlasiet 'Uzskaites supervizors'.
    * Atlasīt lomu. Šajā piemērā atlasiet Uzskaites supervizoru.  
4. Noklikšķiniet Manuāli piešķirt/izslēgt lietotājus.
5. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet lietotāju.  
6. Noklikšķiniet Izslēgt no lomas.
    * Noklikšķiniet uz Izslēgt no lomas, lai izslēgtu atlasītos lietotājus no lomas. Lai noņemtu izslēgšanu, atlasiet lietotājus, kuriem vēlaties noņemt izslēgšanu, un pēc tam noklikšķiniet uz Atiestatīt statusu. Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski. Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma. Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.  


