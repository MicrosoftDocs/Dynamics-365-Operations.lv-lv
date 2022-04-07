---
title: Atvaļinājumu un kavējumu parametru konfigurēšana
description: Šajā tēmā aprakstīts, kā definēt personāla vadības parametrus atvaļinājumam un kavējumiem Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e2bc672fd352fea088db356a6fc2b8eedebe5920
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509197"
---
# <a name="configure-leave-and-absence-parameters"></a>Atvaļinājumu un kavējumu parametru konfigurēšana

>[!Important]
>Šajā tēmā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem savrupā programmā Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pirms atvaļinājumu un kavējumu plānu iestatīšanas Dynamics 365 Human Resources ieteicams pārbaudīt iestatījumus visiem saistītajiem personāla **vadības parametriem**, tai skaitā:

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

>[!IMPORTANT]
>Pašlaik priekšskatījumā tiek apskatīts atvaļinājums un prombūtne uzņēmumos. Jums vajadzēs iespējot to savā **Smilškastes** vidē, lai parādītu atvaļinājumu un prombūtnes opciju. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Skatīt un mainīt Personāla vadības kopīgotos parametrus

1. Lapā **Personāla vadība** atlasiet cilni **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgotie parametri**.

3. Cilnē **Iepriekšēja piekļuve** atlasiet **Jā** opcijai **Iespējot starpuzņēmuma atvaļinājumu skatu**, lai ļautu atvaļinājumu apskatīt visā uzņēmumā.

4. Atlasiet **Saglabāt**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Skatīt un mainīt atvaļinājumu un prombūtnes parametrus

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatīšana** atlasiet **Atvaļinājumu un prombūtnes parametri**.

3. Cilnē **Vispārīgi** iestatiet šādus parametrus:
 
    - Iestatiet **Vienību atvaļinājumam un prombūtni** vai nu stundām, vai dienām. Ja dienas, jūs varat atlasīt **Iespējot pusi dienas definīciju**, lai ļautu darbiniekiem izvēlēties vai nu pirmo, vai otro pusi no dienas , kad tiek veikti prombūtnes pieprasījumi. 

    - Atlasiet **Darba mēnešu spēkā stāšanās datums**, lai iestatītu, kad uzkrāšanas likmes stājas spēkā atvaļinājumu plāniem, izmantojot darba mēnešus.

    - Atlasiet **Bilances aprēķinu**, lai parādītu bilances, kas tiek rādītas no šodienas vai no uzkrāšanas perioda. Ja atlasāt **Bilanci no šodienas**, bilance parāda visu uzkrājumu, korekciju un pieprasījumu kopsummu no šodienas. Ja atlasāt **Bilance no uzkrāšanas perioda**, bilance rāda visu uzkrājumu, korekciju un pieprasījumu kopsummu no uzkrājumu perioda, kas definēts, izmantojot atvaļinājumu plāna biežumu. 

    - Iestatiet sākuma **laiku pakešuzdevumam** Pārnest **beigu** datumu.  
    
    - Atlasiet **Jā** opcijām **Atļaut darbiniekiem pirkt atvaļinājumu** un **Atļaut darbiniekiem pārdot atvaļinājumu**. Ja šīm opcijām atlasāt **Jā**, varat izveidot pirkšanas un pārdošanas atvaļinājuma politikas un dot iespēju darbiniekiem iesniegt pirkšanas un pārdošanas atvaļinājumu pieprasījumus.

## <a name="configure-calendar-parameters"></a>Konfigurējiet kalendāra parametrus

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatīšana** atlasiet **Atvaļinājumu un prombūtnes parametri**.

3. Cilnē **Kalendārs** pēc nepieciešamības mainiet kalendāra iestatījumus.

4. Atlasiet **Saglabāt**.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
