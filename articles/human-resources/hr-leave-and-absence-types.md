---
title: Atvaļinājumu un prombūtnes veidu konfigurēšana
description: Iestatiet atvaļinājumu tipus, ko darbinieki var izņemt pakalpojumā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a23279678bab2564a4b7eef98f8a8a662ae0621
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693757"
---
# <a name="configure-leave-and-absence-types"></a>Atvaļinājumu un prombūtnes veidu konfigurēšana

> [!Important]
> Šajā tēmā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem savrupā programmā Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

2. Iestatiet atvaļinājuma veida **Brīvdienu labojumu** Atlasot šo opciju, tiks izmantots to brīvdienu skaits, kuras iekrīt darba dienā, lai noteiktu, kā uzkrāt brīvo laiku atvaļinājuma veidam. Piemēram, ja Ziemassvētki ir pirmdienā, Human Resources, apstrādājot uzkrājumus, atņem vienu dienu no atvaļinājuma veida.

   Brīvdienas varat iestatīt darba laika kalendārā. Papildinformāciju skatiet šeit šeit: [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md).
   
 3. Iestatiet atvaļinājuma veidam **Pārnesta atvaļinājuma veids**. Atlasot šo opciju, visas pārnešanas bilances tiks pārsūtītas uz norādīto atvaļinājumu veidu. Pārnestā atvaļinājuma veids ir jāiekļauj arī atvaļinājumu un prombūtnes plānā. 
 
4. Definējiet atvaļinājuma veidam **Beigu nosacījumu noteikumus**. Konfigurējot šo opciju, varat izvēlēties dienu vai mēnešu vienību un iestatīt beigu termiņu. Derīguma termiņa spēkā stāšanās datumu izmanto, lai noteiktu, kad sākt palaist pakešuzdevumu, kas apstrādā atvaļinājuma beigu datumu, vai datumu, kad noteikums stājas spēkā. Termiņa beigas vienmēr būs uzkrāšanas perioda sākuma datumā. Piemēram, ja uzkrāšanas perioda sākuma datums ir 2021. gada 3. augusts un termiņa beigu noteikums ir iestatīts uz 6 mēnešiem, noteikums tiks apstrādāts, pamatojoties uz termiņa beigu korespondējošo kontu no uzkrāšanas perioda sākuma datuma, tādējādi tas būtu izpildīts 2022. gada 3. februārī. Visas atvaļinājuma bilances, kas pastāv beigu laikā, tiks atskaitītas no atvaļinājuma veida, un tās tiks atspoguļotas atvaļinājumu bilancē.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Konfigurēt nepieciešamo pielikumu katram atvaļinājuma tipam

> [!NOTE]
> Lai izmantotu lauku **Nepieciešamais pielikums**, vispirms ieslēdziet līdzeklim **Konfigurēt nepieciešamo pielikumu atvaļinājumu pieprasījumiem** līdzekļu pārvaldībā. Lai iegūtu papildinformāciju par to, kā ieslēgt līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

1. Lapas **Atvaļinājums un prombūtne** cilnē **Saites** zem **Iestatījumi** atlasiet **Atvaļinājuma un prombūtnes tipi**.

2. Sarakstā atlasiet atvaļinājuma un prombūtnes tipu. Pēc tam sadaļā **Vispārīgi** izmantojiet lauku **Pielikums**, kas nepieciešams, lai norādītu, vai pielikums ir jāielādē, kad darbinieks iesniedz jaunu atvaļinājuma pieprasījumu atlasītajam atvaļinājuma tipam. 

Darbiniekiem būs jāielādē pielikums, kad tie iesniedz jaunu atvaļinājuma pieprasījumu ar atvaļinājuma tipu, kur ir iespējots lauks **Nepieciešams pielikums**. Lai skatītu pielikumu, kas tika augšupielādēts kā daļa no atvaļinājuma pieprasījuma, atvaļinājuma pieprasījuma apstiprinātāji var izmantot opciju **Pielikumi** darba vienumiem, kas tiem piešķirti. Ja atvaļinājuma pieprasījumam var piekļūt, izmantojot programmu Human Resources Microsoft Teams, atvaļinājuma pieprasījuma opciju **Skatīt detalizētu informāciju** var izmantot, lai skatītu detalizētu informāciju par to un visus pielikumus.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Konfigurēt atvaļinājuma vienības (stundas/dienas) pa atvaļinājuma daļām

> [!NOTE]
> Lai lietotu atvaļinājuma vienības atvaļinājuma tipa funkcionalitātē, vispirms ir jāslēdz līdzekli **Konfigurēt atvaļinājuma vienības pa atvaļinājuma veidiem** Līdzekļu pārvaldība. Lai iegūtu papildinformāciju par to, kā ieslēgt līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

> [!IMPORTANT]
> Pēc noklusējuma atvaļinājumu tipi juridiskajās personas izmanto atvaļinājuma vienības no atvaļinājumu parametru konfigurācijas juridiskas personas līmenī.
> 
> Atvaļinājuma vienību un prombūtnes tipu var modificēt tikai tad, ja šim atvaļinājuma tipam nav atvaļinājuma darbību.
> 
> Līdzekli nevar izslēgt pēc tā ieslēgšanas.

1. Lapas **Atvaļinājums un prombūtne** cilnē **Saites** zem **Iestatījumi** atlasiet **Atvaļinājuma un prombūtnes tipi**.

2. Sarakstā atlasiet atvaļinājuma un prombūtnes tipu. Pēc tam sadaļā **Vispārīgi** laukā **Vienība** atlasiet atvaļinājuma vienību. Var atlasīt **Stundas** vai **Dienas**.

3. Nav obligāti: ja laukā **Vienība** atlasījāt **Stundas**, varat izmantot lauku **Iespējot pusgada definīciju**, lai norādītu, vai darbinieki var atlasīt pirmo pusgadu vai otro brīvdienu, ja viņi pieprasa pusstundas atvaļinājumu.

Darbinieki, kas iesniedz jaunu atvaļinājuma pieprasījumu, var atlasīt dažādus atvaļinājumu tipus, lai veidotu sava atvaļinājuma pieprasījumu. Tomēr visiem atvaļinājumu tipiem, kas atlasīti kā daļa no viena atvaļinājuma pieprasījuma, jābūt vienai atvaļinājuma vienībai. Darbinieki var skatīt atvaļinājuma vienību katram atvaļinājuma veidam veidlapā **Pieprasīt brīvo laiku**.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
- [Izveidot atvaļinājumu un kavējuma plānu](hr-leave-and-absence-plans.md)
- [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md)
- [Pārtraukt atvaļinājumu](hr-leave-and-absence-suspend-leave.md)
- [Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
