---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Microsoft Dynamics 365 for Finance and Operations Enterprise edition, lietotājiem jābūt piešķirtām drošības lomām.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556713"
---
# <a name="assign-users-to-security-roles"></a>Drošības lomu piešķiršana lietotājiem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lai piekļūtu Microsoft Dynamics 365 for Finance and Operations Enterprise edition, lietotājiem jābūt piešķirtām drošības lomām. Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


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

