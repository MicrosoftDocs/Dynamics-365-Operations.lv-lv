---
title: Atvaļinājumu un prombūtnes parametru konfigurēšana
description: Definējiet cilvēkresursu parametrus atvaļinājumam un prombūtnei pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712380"
---
# <a name="configure-leave-and-absence-parameters"></a>Atvaļinājumu un prombūtnes parametru konfigurēšana

Pirms atvaļinājumu un prombūtnes plānu iestatīšanas pakalpojumā Dynamics 365 Human Resources, ir ieteicams pārbaudīt visu saistīto personāla vadības parametru iestatījumus, tostarp:

- Atvaļinājumu pieprasījumu numuru sēriju
- Likuma par ģimenes un medicīniskajiem atvaļinājumiem (FMLA) iestatījumus
- Darbinieku patstāvīgi izmantojamo pakalpojumu iestatījumus atvaļinājumu un prombūtnes pieprasījumiem
- Atvaļinājumu un prombūtnes parametri

## <a name="view-and-change-human-resources-parameters"></a>Skatīt un mainīt personāla vadības parametrus

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.

3. Cilnē **Numuru sērijas** pārbaudiet **Numuru secības kodu** **Atvaļinājuma pieprasījuma ID** un pēc nepieciešamības veiciet izmaiņas. Šis iestatījums nosaka secību, kas tiek izmantota, lai automātiski piešķirtu ID atvaļinājumu pieprasījumiem.

4. Cilnē **FMLA** pārbaudiet FMLA iestatījumus un pēc nepieciešamības mainiet.

5. Cilnē **Darbinieku patstāvīgi izmantojamie pakalpojumi** norādiet, vai vadītāji var ievadīt atvaļinājumu un kavējumu pieprasījumus savu darbinieku vārdā.

7. Atlasiet **Saglabāt**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Skatīt un mainīt atvaļinājumu un prombūtnes parametrus

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatīšana**atlasiet **Atvaļinājumu un prombūtnes parametri**.

3. Cilnē **Vispārīgi** iestatiet šādus parametrus:
 
    - Iestatiet **Vienību atvaļinājumam un prombūtni** vai nu stundām, vai dienām. Ja dienas, jūs varat atlasīt **Iespējot pusi dienas definīciju**, lai ļautu darbiniekiem izvēlēties vai nu pirmo, vai otro pusi no dienas , kad tiek veikti prombūtnes pieprasījumi. 

    - Atlasiet **Darba mēnešu spēkā stāšanās datums**, lai iestatītu, kad uzkrāšanas likmes stājas spēkā atvaļinājumu plāniem, izmantojot darba mēnešus.

    - Atlasiet **Bilances aprēķinu**, lai parādītu bilances, kas tiek rādītas no šodienas vai no uzkrāšanas perioda. Ja atlasāt **Bilanci no šodienas**, bilance parāda visu uzkrājumu, korekciju un pieprasījumu kopsummu no šodienas. Ja atlasāt **Bilance no uzkrāšanas perioda**, bilance rāda visu uzkrājumu, korekciju un pieprasījumu kopsummu no uzkrājumu perioda, kas definēts, izmantojot atvaļinājumu plāna biežumu. 

    - Iestatiet sākuma laiku pārnestā termiņa beigu pakešuzdevumam.  
    
    - Atlasiet **Jā** opcijām **Atļaut darbiniekiem pirkt atvaļinājumu** un **Atļaut darbiniekiem pārdot atvaļinājumu**. Ja šīm opcijām atlasāt **Jā**, varat izveidot pirkšanas un pārdošanas atvaļinājuma politikas un dot iespēju darbiniekiem iesniegt pirkšanas un pārdošanas atvaļinājumu pieprasījumus.

## <a name="configure-calendar-parameters"></a>Konfigurējiet kalendāra parametrus

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatīšana**atlasiet **Atvaļinājumu un prombūtnes parametri**.

3. Cilnē **Kalendārs** pēc nepieciešamības mainiet kalendāra iestatījumus.

4. Atlasiet **Saglabāt**.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
