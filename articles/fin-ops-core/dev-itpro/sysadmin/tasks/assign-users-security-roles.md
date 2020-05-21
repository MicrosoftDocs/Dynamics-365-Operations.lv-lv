---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Finance and Operations programmām, lietotājiem jābūt piešķirtām drošības lomām.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
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
ms.openlocfilehash: f0421ad6c932f2c91de51169bda6c98f53d3bc65
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346449"
---
# <a name="assign-users-to-security-roles"></a>Drošības lomu piešķiršana lietotājiem

[!include [banner](../../includes/banner.md)]

Lai izmantotu citas iespējas, kas nav kopīgas iespējas Finance and Operations programmās, lietotājiem jābūt piešķirtām drošības lomām. Jūs varat piešķirt lietotājus lomām automātiski, pamatojoties uz kārtulām un biznesa datiem, izslēgt lietotājus no automātiskās lomas piešķires vai pievienot lietotājus lomām manuāli.

## <a name="automatically-assign-users-to-roles"></a>Automātiski piešķirt lietotājus lomām
Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem. 
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
2. Kokā atlasiet 'Uzskaites supervizors'. Atlasiet lomu, kurai vēlaties konfigurēt kārtulu. Šajā piemērā atlasiet Uzskaites supervizoru. 
3. Atlasiet **Pievienot kārtulu**, lai atvērtu dialoglodziņa izvēlni.
4. Sarakstā **Vaicājuma atlase** atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.  
5. Sarakstā **Dalības kārtulas nosaukums** noklikšķiniet uz saites atlasītajā rindā.
6. Atlasiet **Rediģēt vaicājumu**. Rediģējiet vaicājumu pēc nepieciešamības.  
7. Atlasiet **Labi**.
8. Atlasiet **Palaist automātisko lomu piešķiri**.
9. Doties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana >Lietotāji > Lietotāji** (ideālā gadījumā atsevišķā pārlūka cilnē).
10. Pārskatiet dažādiem lietotājiem piešķirtās lomas, lai apstiprinātu, ka lomas piešķires vaicājums ir bijis pareizs. Pielāgojiet un vajadzības gadījumā palaidiet atkārtoti.

## <a name="exclude-users-from-automatic-role-assignment"></a>Izslēgt lietotājus no automātiskas lomu piešķiršanas
1. Aizvērt lapu.
2. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
3. Kokā atlasiet 'Uzskaites supervizors'. Atlasīt lomu. Šajā piemērā atlasiet Uzskaites supervizoru.  
4. Izvēlnē **Lomai piešķirtie lietotāji** atlasiet **Manuāli piešķirt/izslēgt lietotājus**.
5. Sarakstā **Piešķirt lomai vai izslēgt no lomas lietotājus** atzīmējiet atlasīto rindu. Atlasiet lietotāju.  
6. Sadaļā **Darbību rūts** atlasiet **Izslēgt no lomas**.
7. Atlasiet **Izslēgt no lomas**, lai izslēgtu atlasītos lietotājus no lomas. Lai atceltu izslēgšanu, atlasiet lietotājus, kuriem vēlaties atcelt izslēgšanu, un pēc tam noklikšķiniet uz **Atiestatīt statusu**. Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma tiek piešķirta automātiski. Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma. Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.  

## <a name="manually-assign-users-to-roles"></a>Manuāla lomu piešķiršana lietotājiem
Lietotājiem, kas manuāli ir piesaistīti drošības lomām, administratoram arī jādzēš manuāli. Šie lietotāji netiek noņemti no lomām ar kārtulām automātiskai lomas piešķiršanai.

1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
2. Shēmā atlasiet lomu un izvēlnē **Lomai piešķirtie lietotāji** atlasiet **Manuāli piešķirt/izslēgt lietotājus**.
4. Sadaļā **Piešķirt lietotājus vai izslēgt lietotājus no lomas** lietotājiem, kuriem nav piešķirta loma, tiek uzskaitīti ar **Piešķires režīmu** iestatītu uz **Nav**. Atlasiet vienu vai vairākus lietotājus, kuriem jāpiešķir loma.
5. Sadaļā **Darbību rūts** atlasiet **Piešķirt lomu**. **Piešķires režīms** tiek atjaunināts uz **Manuāli**, un lietotājiem tagad ir piešķirta jauna loma.
