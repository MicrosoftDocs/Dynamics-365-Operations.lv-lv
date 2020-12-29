---
title: Atvaļinājumu un prombūtnes veidu konfigurēšana
description: Iestatiet atvaļinājumu tipus, ko darbinieki var izņemt pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419519"
---
# <a name="configure-leave-and-absence-types"></a>Atvaļinājumu un prombūtnes veidu konfigurēšana

Atvaļinājumu veidi pakalpojumā Dynamics 365 Human Resources definē, kādu veidu prombūtnes laiku darbinieki var pieprasīt. Varat pielāgot atvaļinājumu veidus atbilstoši organizācijas vajadzībām. Atvaļinājumu veidu piemēri ietver:

- Apmaksāts brīvais laiks (PTO)
- Neapmaksāts atvaļinājums
- Apmaksāts atvaļinājums
- Slimības atvaļinājums
- Medicīnisks atvaļinājums
- Ģimenes atvaļinājums
- Īslaicīga invaliditāte
- Apbedīšanas atvaļinājums

## <a name="add-a-leave-type"></a>Pievienot atvaļinājuma tipu

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatīšana** atlasiet **Atvaļinājumu un kavējumu veidi**.

3. Atlasiet **Jauns**.

4. Ievadiet atvaļinājuma veida nosaukumu laukā **Veids**, atlasiet darbplūsmu no **Darbplūsmas ID** un ievadiet aprakstu laukā **Apraksts**.

5. Laukā **Vispārīgi** atlasiet **Neviens**, **Plānots** vai **Neplānots** nolaižamajā sarakstā **Kategorija**.

6. Atlasiet pelnīšanas kodu no nolaižamā saraksta **Ienākumu veida kods**.

7. Laukā **Nepieciešams pamatojuma kods** izvēlieties, vai vēlaties pieprasīt pamatojuma kodu. Ja vēlaties pieprasīt pamatojuma kodus, iespējams, tie ir jāpievieno. Sadaļā **Pamatojumu kodi** atlasiet **Pievienot**, atlasiet pamatojuma kodu un pēc tam blakus atzīmējiet izvēles rūtiņu **Iespējoti**.

8. Sadaļā **Ierobežot piekļuvi atlasītajām lomām** izvēlieties, vai vēlaties ierobežot piekļuvi. Pēc tam atlasiet drošības lomas sadaļā **Drošības lomas šim atvaļinājuma veidam**. Drošības lomas ir definētas darbplūsmā, ko atlasījāt laukā **Darbplūsmas ID** iepriekš šajā procedūrā.

9. Sadaļā **Kalendāra krāsa** izvēlieties krāsu, ko parādīt atvaļinājuma un kavējumu kalendāros šim atvaļinājuma tipam. 

10. Sadaļā **Atlikšanas attiecības** izvēlieties, vai vēlaties, lai šo atvaļinājuma veidu aiztur cits cits atvaļinājuma veids vai arī to aptur cits atvaļinājuma veids. Ja prombūtnes atvaļinājuma pieprasījums ir iesniegts atliktam atvaļinājuma veidam, tad aizturētā atvaļinājuma veidam automātiski tiks izveidota atvaļinājuma atlikšana. 

10. Atlasiet **Saglabāt**.

## <a name="configure-leave-type-rules"></a>Konfigurēt atvaļinājumu veidu kārtulas

1. Iestatiet noapaļošanas opcijas atvaļinājuma veidam. Opcijas ietver **Neviens**, **Uz augšu**, **Uz leju** un **Tuvākais**. Atvaļinājuma veidam var arī iestatīt noapaļošanas precizitāti.

2. Iestatiet atvaļinājuma veida **Brīvdienu labojumu** Atlasot šo opciju, Human Resources izmanto to brīvdienu skaitu, kuras iekrīt darba dienā, lai noteiktu, kā uzkrāt brīvo laiku atvaļinājuma veidam. Piemēram, ja Ziemassvētki ir pirmdienā, Human Resources, apstrādājot uzkrājumus, atņem vienu dienu no atvaļinājuma veida.

   Brīvdienas varat iestatīt darba laika kalendārā. Papildinformāciju skatiet šeit šeit: [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md)
   
 3. Iestatiet atvaļinājuma veidam **Pārnesta atvaļinājuma veids**. Atlasot šo opciju, visas pārnešanas bilances tiks pārsūtītas uz norādīto atvaļinājumu veidu. Pārnestā atvaļinājuma veids ir jāiekļauj arī atvaļinājumu un prombūtnes plānā. 
 
 4. Definējiet atvaļinājuma veidam **Beigu nosacījumu noteikumus**. Konfigurējot šo opciju, varat izvēlēties dienu vai mēnešu vienību un iestatīt beigu termiņu. Varat arī iestatīt termiņa beigu nosacījuma spēkā stāšanās datumu. Visas atvaļinājuma bilances, kas pastāv beigu laikā, tiks atskaitītas no atvaļinājuma veida, un tās tiks atspoguļotas atvaļinājumu bilancē. 
 
 
## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
- [Izveidot atvaļinājumu un kavējuma plānu](hr-leave-and-absence-plans.md)
- [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md)
- [Pārtraukt atvaļinājumu](hr-leave-and-absence-suspend-leave.md)

