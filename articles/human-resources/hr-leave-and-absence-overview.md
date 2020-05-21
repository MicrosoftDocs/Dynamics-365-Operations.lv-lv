---
title: Pārskats
description: Programmā Dynamics 365 Human Resources Atvaļinājumu un prombūtnes darbvieta nodrošina elastīgu struktūru jaunu atvaļinājumu plānu izveidei, darbplūsmas pieprasījumu pārvaldībai un intuitīvai darbinieku patstāvīgi izmantojamo pakalpojumu lapai, kurā var pieprasīt brīvo laiku.
author: andreabichsel
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bb123b808615ff7d770c7c6b83338a32d922be3
ms.sourcegitcommit: de217452a85429675994e9cc0e06eb4821cab3e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/30/2020
ms.locfileid: "3325769"
---
# <a name="overview"></a>Pārskats

Dynamics 365 Human Resources palīdz nodrošināt lieliskus atvaļinājuma atvieglojumus jūsu darbiniekiem. **Atvaļinājumu un prombūtnes** darbvieta nodrošina elastīgu struktūru jaunu atvaļinājumu plānu izveidei, darbplūsmas pieprasījumu pārvaldībai un intuitīvai darbinieku patstāvīgi izmantojamo pakalpojumu lapai, kurā var pieprasīt brīvo laiku. Analīze palīdz jūsu organizācijai izmērīt un pārraudzīt atvaļinājuma bilances un izmantošanu jūsu atvaļinājuma plānos.

## <a name="set-up-leave-and-absence"></a>Atvaļinājumu un prombūtnes iestatīšana

Pirms atvaļinājumu plānu izveidošanas saviem darbiniekiem, ir jāveic dažas iestatīšanas darbības:

- [Atvaļinājumu un prombūtnes parametru konfigurēšana](hr-leave-and-absence-parameters.md)
- [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md)
- [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Izveidojiet un pārvaldiet atvaļinājuma plānus

Pirms atvaļinājuma plānu izveides jūsu darbiniekiem ir jāizveido atvaļinājumu un prombūtnes tipi. Kad esat izveidojis atvaļinājumu plānu, piereģistrēt darbiniekus plānā. Varat arī palaist uzkrāšanas procesu, izveidot brīdinājumus un skatīt savu plānu analīzi.

- [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md)
- [Izveidot atvaļinājumu un prombūtnes plānu](hr-leave-and-absence-plans.md)
- [Piešķirt darbiniekus atvaļinājumu plānam](hr-leave-and-absence-enroll.md)
- [Atvaļinājumu un prombūtnes plānu uzkrāšana](hr-leave-and-absence-accrue.md)
- [Skatīt analīzi par atvaļinājumiem un prombūtni](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Pieprasīt brīvo laiku un pārvaldīt pieprasījumus

Jūsu darbinieki var iesniegt brīvā laika pieprasījumus, un tos var pārvaldīt **Darbinieku patstāvīgi izmantojamo pakalpojumu** darbvietā.

- [Pieprasīt brīvo laiku](hr-employee-self-service-request-time-off.md)
- [Atvaļinājumu un kavējumu pieprasījumu pārvaldība](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Atvaļinājumu un prombūtnes zināmās problēmas

### <a name="rounding-precision"></a>Noapaļošanas precizitāte

Jūs nevarat iestatīt **Noapaļošanas precizitāti**, iestatot **Noapaļošanas veidu**. Jūs varat iestatīt tikai **Noapaļošanas precizitāti**, izmantojot elementu **Atvaļinājuma un prombūtnes veids**. 

1. Sadaļā **Atvaļinājumu un prombūtnes veidi** atlasiet **Atvērt programmā Excel**, lai atvērtu elementu **Atvaļinājuma un prombūtnes veids**.

2. Kad fails tiek atvērts un ir iespējots, izvēlieties **Noformējums**.

3. Tabulā **Atvaļinājuma un prombūtnes veids** atlasiet zīmuļa opciju, lai rediģētu.

4. Atlasiet **RoundingPrecision** un **RoundingType** un pēc tam atlasiet **Pievienot**, lai pievienotu laukus sarakstam.

5. Atlasiet **Atjaunināt** un pēc tam atlasiet **Gatavs**.

6. Ievadiet vai atlasiet **Noapaļošanas veidu** katram atvaļinājuma veidam, ja tas jau nav iestatīts. 

7. Ievadiet **Noapaļošanas precizitāti** atbilstošajiem veidiem.

8. Atlasiet **Publicēt**, lai pārliktu izmaiņas uz Personāla vadību.

## <a name="leave-and-absence-preview-features"></a>Atvaļinājumu un prombūtnes priekšskatījuma līdzekļi

**Smilškastes** vidē varat izmēģināt jaunus atvaļinājumu un prombūtnes priekšskatījuma līdzekļus. Lai iegūtu informāciju par priekšskatījuma līdzekļu ieslēgšanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Priekšskatījuma līdzekļi ietver:

- **Atvaļinājuma atlikšana** — jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā. Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem. Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā tiek izveidots proporcionāls pārrēķins darbinieka atvaļinājuma bilancei. Jūs varat arī iekļaut pamatojuma kodus, apturot darbinieka atvaļinājumu. Lietotāja pieredze ir atjaunināta, lai norādītu atlikšanu. 

- **Pārnest nosacījumus** - varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. 

- **Iekļaut pamatojuma kodu un komentārus par korekcijām** – jūs varat iekļaut pamatojuma kodu un komentāru, veicot korekciju darbinieka atvaļinājuma bilancei. 

- **Pāreja uz atvaļinājumu un kavējumu parametriem** — tagad personāla vadības parametru izmantošanas vietā jūs varat izmantot tikai atvaļinājumu un prombūtnes parametrus. 
