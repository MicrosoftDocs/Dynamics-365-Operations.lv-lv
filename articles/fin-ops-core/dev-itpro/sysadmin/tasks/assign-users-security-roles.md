---
title: Piešķirt lietotājus drošības lomām
description: Lai piekļūtu finanšu un operāciju programmām, lietotājiem jābūt piešķirtiem drošības lomām.
author: Peakerbl
ms.date: 02/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5e69a79f123daff3f85d0100647615ad818288e
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103874"
---
# <a name="manage-users-and-security-roles"></a>Lietotāju un drošības lomu pārvaldība

[!include [banner](../../includes/banner.md)]

Lai izmantotu jebko citu, nevis parastās iespējas finanšu un operāciju programmās, lietotājiem ir jāpiešķir drošības lomas. Jūs varat piešķirt lietotājus lomām automātiski, pamatojoties uz kārtulām un biznesa datiem, izslēgt lietotājus no automātiskās lomas piešķires vai pievienot lietotājus lomām manuāli.

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
Šajā procedūrā skaidrots, kā izslēgt lietotājus no automātiskas lomu piešķiršanas.

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

## <a name="manually-remove-users-from-roles"></a>Manuāli noņemt lietotājus no lomām
Lietotājiem, kas manuāli ir piesaistīti drošības lomām, administratoram arī jādzēš manuāli. Šie lietotāji netiek noņemti no lomām ar kārtulām automātiskai lomas piešķiršanai.

1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.
2. Lai noņemtu vienu lietotāju, rīkojieties šādi:
   1. Koka struktūrā atlasiet lomu. 
   2. Lomas **apgabalā Lietotāji,** kas piešķirti, atlasiet lietotāju, kas ir jānoņem.
   3. Atlasiet **Noņemt** un lietotājs ir noņemts no lomas.
3. Lai noņemtu vairākus lietotājus, rīkojieties šādi:
   1. Koka struktūrā atlasiet lomu. 
   2. Lomai **piešķirtajiem lietotājiem** atlasiet Manuāli **piešķirt/izslēgt lietotājus**.
   3. Lapā Piešķirt **lietotājus lomai vai izslēgt no** lomas lapas lietotājiem, kuriem nav piešķirta loma, **·** **kolonnā Piešķires režīms ir Nav.** Atlasiet lietotājus, kas ir jāizslēdz no lomas.
   4. Sadaļā **Darbību rūts** atlasiet **Izslēgt no lomas**. Tagad **piešķires režīma** kolonna ir atjaunināta uz **Manuāli,** un lietotāji tagad ir izslēgti no lomas.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

