---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Finance and Operations programmām, lietotājiem jābūt piešķirtām drošības lomām.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
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
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143557"
---
# <a name="assign-users-to-security-roles"></a>Drošības lomu piešķiršana lietotājiem

[!include [banner](../../includes/banner.md)]

Lai izmantotu citas iespējas, kas nav kopīgas iespējas, lietotājiem jābūt piešķirtiem drošības lomām. Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem. 

## <a name="automatically-assign-users-to-roles"></a>Automātiski piešķirt lietotājus lomām
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
2. Kokā atlasiet 'Uzskaites supervizors'. Atlasiet lomu, kurai vēlaties konfigurēt kārtulu. Šajā piemērā atlasiet Uzskaites supervizoru. 
3. Noklikšķiniet uz **Pievienot kārtulu**, lai atvērtu nolaižamo dialoglodziņu.
4. Sarakstā **Vaicājuma atlase** atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.  
5. Sarakstā **Dalības kārtulas nosaukums** noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Rediģēt vaicājumu**. Rediģējiet vaicājumu pēc nepieciešamības.  
7. Noklikšķiniet uz **Labi**.
8. Noklikšķiniet uz **Palaist automātisko lomu piešķiri**.
9. Doties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana >Lietotāji > Lietotāji** (ideālā gadījumā atsevišķā pārlūka cilnē).
10. Pārskatiet dažādiem lietotājiem piešķirtās lomas, lai apstiprinātu, ka lomas piešķires vaicājums ir bijis pareizs. Pielāgojiet un vajadzības gadījumā palaidiet atkārtoti.

## <a name="exclude-users-from-automatic-role-assignment"></a>Izslēgt lietotājus no automātiskas lomu piešķiršanas
1. Aizvērt lapu.
2. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
3. Kokā atlasiet 'Uzskaites supervizors'. Atlasīt lomu. Šajā piemērā atlasiet Uzskaites supervizoru.  
4. Izvēlnē **Lomai piešķirtie lietotāji** atlasiet **Manuāli piešķirt/izslēgt lietotājus**.
5. Sarakstā **Piešķirt lomai vai izslēgt no lomas lietotājus** atzīmējiet atlasīto rindu. Atlasiet lietotāju.  
6. Sadaļā **Darbību rūts** atlasiet **Izslēgt no lomas**.
    
    Noklikšķiniet uz **Izslēgt no lomas**, lai izslēgtu atlasītos lietotājus no lomas. Lai atceltu izslēgšanu, atlasiet lietotājus, kuriem vēlaties atcelt izslēgšanu, un pēc tam noklikšķiniet uz **Atiestatīt statusu**. Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski. Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma. Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.  
