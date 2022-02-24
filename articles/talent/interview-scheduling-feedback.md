---
title: Plānot intervijas programmā Attract
description: Šajā tēmā ir sniegta informācija par interviju plānošanas un atsauksmju aktivitātēm programmā Attract.
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: shielas
ms.openlocfilehash: 33eba9796ca997fde4be9a46050207d313551bde
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461905"
---
# <a name="schedule-interviews-in-attract"></a>Plānot intervijas programmā Attract

[!include [banner](includes/banner.md)]

## <a name="scheduler-activity"></a>Plānotāja aktivitāte

Aktivitāte Plānotājs ir izvēles aktivitāte, kas sastāv no diviem komponentiem: Kandidāta pieejamības pieprasījums un Grafiks. Komponents Kandidāta pieejamība sniedz jums iespēju izmantot e-pastu, lai pieprasītu kandidāta pieejamību. Komponents Grafiks sniedz iespēju ieplānot intervijas, saskaņojot grafiku ar kandidātu un darbā pieņemšanas grupu.

Lai iestatītu plānotāja aktivitāti, kas ietver vai ierobežo kandidātus, kuru plānošana ir paredzēta, atlasiet vērtību laukā **Personas, kuras paredzēts plānot**. Pieejamās opcijas ir **Visi kandidāti**, **Ārējie kandidāti** un **Iekšējie kandidāti**. Piemēram, ja vēlaties izlaist iekšējos kandidātus pirmajā plānošanas kārtā, varat piešķirt plānotāja aktivitāti tikai ārējiem kandidātiem, iestatot vienumam **Personas, kuras paredzēts plānot** opciju **Ārējie kandidāti**.

### <a name="candidate-availability-request"></a>Kandidāta pieejamības pieprasījums

Lai sūtītu kandidātiem e-pasta ziņojumus ar viņu pieejamības pieprasījumiem, atlasiet lauku **Pieprasīt kandidāta pieejamību**. Ja šis lauks nav atlasīts, šī darbība netiek rādīta darba darbā pieņemšanas procesa ietvaros.

Lai nosūtītu pieejamības pieprasījumu, noklikšķiniet uz **Sūtīt pieprasījumu**, izvēlieties pieejamos datumus un e-pasta ziņojuma veidni un pēc tam nosūtiet e-pasta ziņojumu kandidātam.

[![Attract personāla atlases speciālista skats kandidāta pieejamības pieprasījuma sūtīšanai](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Kad kandidāts saņem e-pasta ziņojumu, lai atbildētu uz pieprasījumu, viņš var pierakstīties kandidātu portālā, izvēlēties datumus, kas atbilst viņa pieejamībai, un noklikšķināt uz **Iesniegt**.

### <a name="schedule"></a>Ieplānošana
Ir pieejamas vairākas konfigurācijas, ko var izmantot interviju plānotājs, lai ātri izveidotu interviju ciklu un nosūtītu to intervētājiem un kandidātiem.

1. Noklikšķiniet uz **Izveidot grafiku** un lodziņā **Pievienot intervētājus** norādiet visus intervētājus, kas piedalīsies interviju ciklā.
[![Attract personāla atlases speciālista skats interviju cikla plānošanas sākšanai](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Ja kandidāts ir atbildējis uz intervijas pieprasījuma pieejamības pieprasījumu, lauks **Intervijas datums** tiek automātiski aizpildīts, izmantojot kandidāta atlasīto datumu. Ja tas ir vajadzīgs, varat atlasīt citu datumu.
    
    Ja atlasāt lauku **Norādīt šo kā paneļinterviju**, kreisajā pusē esošā intervētāju grupa tiek pārvietota uz vienu paneļinterviju ciklu, lai izveidotu interviju. Pēc tam ir jānorāda konkrēta interviju secība.
    
    Interviju grafiks ir jāveido tā, lai tas vislabāk atbilstu dalībnieku pieejamībai. Ja tiek intervēts iekšējs kandidāts, varat ietvert viņa pieejamību grafika ieteikumos.
    
    Lai rīkotu tiešsaistes sapulci, atlasiet lauku **Pievienot Skype sapulces** — pēc tam katram intervijas notikumam ir pieejama **Skype darbam** saite.

2. Atlasiet katram intervijas notikuma intervijas ilgumu un pēc tam noklikšķiniet uz **Labi**, lai sāktu grafika izveidi.

    Ja ir atlasīts vienums **Ieteikumi**, tiek rādīti ieteikumi un interviju režģis tiek daļēji aizpildīts. Varat skatīt visu atlasīto intervētāju pašreizējo kalendārā reģistrēto pieejamību. Varat arī skatīt kandidāta kalendāru, ja tas ir iekšējs kandidāts. Intervētājiem un iekšējiem kandidātiem var skatīt aizņemtos laika posmus, darba laiku, laiku ārpus biroja un arī noteikt, vai tie ir atzīmējuši savā kalendārā darbu citur noteiktos laika posmos. 

3. Ja nav pieejams neviens ieteikums, kolonnā **Intervētāji** noklikšķiniet uz laika nišas, norādiet intervijas nosaukumu un detalizētu informāciju un aizpildiet detalizētu informāciju par vietu, ja tas ir nepieciešams. Varat izvēlēties intervijai pievienot **Skype darbam** saiti.

4. Lai iekļautu papildu intervētājus, noklikšķiniet uz režģa kolonnas **Pievienot interviju** un atlasiet vienu vai vairākus intervētājus. Varat izmantot daudzpunktes (...) opciju, lai noņemtu interviju no cikla.
    
5. Ja intervijas ir ieplānotas citā laika zonā, atlasiet nepieciešamo pilsētu/laika zonu augšējā labajā stūrī esošajā nolaižamajā sarakstā. Intervētāja pieejamības režģis tiek atjaunināts atbilstoši jaunajai laika joslai. Šī atlasītā laika josla tagad tiek rādīta arī skatā **Kopsavilkums par intervijām**, kas tiks kopīgots ar intervētājiem un kandidātu. 

6. Noklikšķiniet uz **Nosūtīt intervētājiem**, lai nosūtītu uzaicinājumu uz sapulci iesaistītajiem intervētājiem.

    Pēc intervijas pieprasījumu nosūtīšanas intervētājiem viņi var tiešā veidā atbildēt e-pasta uzaicinājumā, ko viņi ir saņēmuši.

    >[!NOTE]
    > Par katru 1:1 interviju intervētājiem ik pēc 24 stundām tiek nosūtīts atgādinājums, ja intervētājs nav atbildējis uz intervijas pieprasījumu (pieņēmis vai noraidījis).

    > Nevienai paneļintervijai netiek nodrošināti nekādi automatizēti atgādinājumi par intervijas pieprasījumu. Lai manuāli aktivizētu atgādinājumu, rediģējiet interviju un izmantojiet opciju **Atjaunināt un sūtīt**, un pieprasījums tiks vēlreiz nosūtīts intervētājiem.

    Intervētāja atbildes tiek reģistrētas un parādītas programmā Attract. Ja intervētājs noraida uzaicinājumu, jums par to tiek paziņots, lai jūs veiktu izmaiņas. Lai skatītu viņu atbildi programmas **Plānotājs** režģa skatā, noklikšķiniet uz burbuļa ikonas.

[![Attract personāla atlases speciālista skats intervētāja atbildes skatīšanai](./media/schedule-interviewer-response2.png)](./media/schedule-interviewer-response2.png)

7. Kad interviju grafiks ir sagatavots kopīgošanai ar kandidātu, noklikšķiniet uz **Nosūtīt kandidātam**. Varat izvēlēties kandidātam rādīt vai nerādīt intervētāju vārdus un nišas.

8. Atlasiet e-pasta ziņojuma veidni un nosūtiet kandidātam kopsavilkumu par intervijām. Kandidāts šo informāciju var skatīt savā e-pasta klientā, kā arī kandidātu portālā.
    
>[!NOTE] 
> Kandidāta kalendārā reģistrētā pieejamība tiek parādīta tikai tad, ja tas ir iekšējs kandidāts. Līdzīgi, tikai iekšējiem kandidātiem var uzlabot interviju grafika ieteikumus. Pašlaik kandidāti (ārējie vai iekšējie) nesaņem e-pasta uzaicinājumu uz sapulci. Tā vietā kandidāts saņem tikai kopsavilkumu par intervijām.

Kandidāti saņems e-pastu, kurā ir apkopots viņu interviju cikls. E-pasts satur .ics failu, ko var saglabāt viņu personiskajā kalendārā, lai nodrošinātu ērtāku piekļuvi un paziņojumu par interviju.

>[!TIP] 
> Ja atkārtoti nosūtāt kandidātiem intervijas grafiku, viņi saņems pielikumā vēl vienu .ics failu. Ir ieteicams atjaunināt kandidāta intervijas kopsavilkuma e-pasta veidnes, lai nodrošinātu, ka kandidāti dzēš iepriekš pievienotos interviju notikumus un neredz savā kalendārā dublikātus. 

## <a name="feedback-activity"></a>Atsauksmju sniegšanas aktivitāte

Aktivitāte Atsauksmes ir darba veidnes izvēles aktivitāte. Šī aktivitāte sniedz intervijas dalībniekiem iespēju ievadīt kandidātam paredzētus ieteikumus vai komentārus ar atsauksmēm. 

Lai iekļautu vai ierobežotu kandidātus, par kuriem tiek sniegtas atsauksmes, atlasiet vērtību laukā **Personas, par kurām intervētājiem jāsniedz atsauksmes**.  Pieejamās opcijas ir **Visi kandidāti**, **Ārējie kandidāti** un **Iekšējie kandidāti**. Piemēram, ja vēlaties izlaist iekšējos kandidātus pirmajā plānošanas kārtā, iestatiet vienumam **Personas, par kurām intervētājiem jāsniedz atsauksmes** opciju **Ārējie kandidāti**.

Ja atlasāt lauku **Pārmantot aktivitātes Atsauksmes dalībniekus no darbā pieņemšanas grupas**, personāla atlases speciālists, par pieņemšanu darbā atbildīgais vadītājs un intervētāji tiek automātiski pievienoti aktivitātei Atsauksmes. Organizācijas var atļaut intervētajiem skatīt citu personu atsauksmes pirms savu atsauksmju iesniegšanas. Organizācijas var atļaut intervētājiem arī rediģēt savas atsauksmes pēc to iesniegšanas. Intervētājiem tiek atgādināts iesniegt atsauksmes par nesen veiktajām intervijām, pamatojoties uz iepriekš iestatītu konfigurāciju darba veidnes ietvaros. Darbā pieņemšanas vadītājs vai darbam piesaistītais personāla atlases speciālists varat arī manuāli atgādināt intervētājam par atsauksmju iesniegšanu.

## <a name="interview-activity"></a>Aktivitāte Intervija

Aktivitāte Intervija ir izvēles aktivitāte, kas sastāv no trīs komponentiem: **Kandidāta pieejamības pieprasījums**, **Grafiks** un **Atsauksmes**. Izmantojiet intervijas aktivitāti darba veidnē, ja vēlaties visus komponentus Kandidāta pieejamības pieprasījums, Grafiks un Atsauksmes iekļaut procesā, nevis tos izmantot atsevišķi.

Lai iekļautu vai ierobežotu kandidātus, kurus paredzēts intervēt, atlasiet vērtību laukā **Personas, kuras paredzēts intervēt**. Pieejamās opcijas ir **Visi kandidāti**, **Ārējie kandidāti** un **Iekšējie kandidāti**. Piemēram, ja vēlaties izlaist iekšējos kandidātus pirmajā intervēšanas kārtā, iestatiet vienumam **Personas, kuras paredzēts intervēt** opciju **Ārējie kandidāti**.
