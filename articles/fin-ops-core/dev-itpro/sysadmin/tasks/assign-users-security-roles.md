---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Finance and Operations programmām, lietotājiem jābūt piešķirtai drošības lomai.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180971"
---
# <a name="assign-users-to-security-roles"></a>Drošības lomu piešķiršana lietotājiem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lai izmantotu citas iespējas, kas nav kopīgas iespējas, lietotājiem jābūt piešķirtiem drošības lomām. Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem. 

## <a name="automatically-assign-users-to-roles"></a>Automātiski piešķirt lietotājus lomām
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
2. Kokā atlasiet 'Uzskaites supervizors'. Atlasiet lomu, kurai vēlaties konfigurēt kārtulu. Šajā piemērā atlasiet Uzskaites supervizoru. 
3. Noklikšķiniet uz **Pievienot kārtulu**, lai atvērtu nolaižamo dialoglodziņu.
4. Sarakstā **Vaicājuma atlase** atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.  
5. Sarakstā **Dalības kārtulas nosaukums** noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Rediģēt vaicājumu**. Rediģējiet vaicājumu pēc nepieciešamības.  
7. Noklikšķiniet uz **Labi**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Izslēgt lietotājus no automātiskas lomu piešķiršanas
1. Aizvērt lapu.
2. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
3. Kokā atlasiet 'Uzskaites supervizors'. Atlasīt lomu. Šajā piemērā atlasiet Uzskaites supervizoru.  
4. Izvēlnē **Lomai piešķirtie lietotāji** atlasiet **Manuāli piešķirt/izslēgt lietotājus**.
5. Sarakstā **Piešķirt lomai vai izslēgt no lomas lietotājus** atzīmējiet atlasīto rindu. Atlasiet lietotāju.  
6. Sadaļā **Darbību rūts** atlasiet **Izslēgt no lomas**.
    
    Noklikšķiniet uz **Izslēgt no lomas**, lai izslēgtu atlasītos lietotājus no lomas. Lai atceltu izslēgšanu, atlasiet lietotājus, kuriem vēlaties atcelt izslēgšanu, un pēc tam noklikšķiniet uz **Atiestatīt statusu**. Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski. Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma. Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.  
