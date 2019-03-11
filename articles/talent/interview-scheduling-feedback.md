---
title: Interviju plānošana un atsauksmes
description: Šajā tēmā ir sniegta informācija par interviju plānošanas un atsauksmju aktivitātēm programmā Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2019
ms.locfileid: "374940"
---
# <a name="interview-scheduling-and-feedback"></a>Interviju plānošana un atsauksmes

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Aktivitāte Plānotājs

Aktivitāte Plānotājs ir izvēles aktivitāte, kas sastāv no diviem komponentiem: Kandidāta pieejamības pieprasījums un Grafiks. Komponents Kandidāta pieejamība sniedz jums iespēju izmantot e-pastu, lai pieprasītu kandidāta pieejamību. Komponents Grafiks sniedz iespēju ieplānot intervijas, saskaņojot grafiku ar kandidātu un darbā pieņemšanas grupu.

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

    Ja ir atlasīts vienums **Ieteikumi**, tiek rādīti ieteikumi un interviju režģis tiek daļēji aizpildīts. Varat skatīt visu atlasīto intervētāju pašreizējo kalendārā reģistrēto pieejamību. Varat arī skatīt kandidāta kalendāru, ja tas ir iekšējs kandidāts.

3. Ja nav pieejams neviens ieteikums, kolonnā **Intervētāji** noklikšķiniet uz laika nišas, norādiet intervijas nosaukumu un detalizētu informāciju un aizpildiet detalizētu informāciju par vietu, ja tas ir nepieciešams. Varat izvēlēties intervijai pievienot **Skype darbam** saiti.

4. Lai iekļautu papildu intervētājus, noklikšķiniet uz režģa kolonnas **Pievienot interviju** un atlasiet vienu vai vairākus intervētājus. Varat izmantot daudzpunktes (...) opciju, lai noņemtu interviju no cikla.
    
5. Ja intervijas ir ieplānotas citā laika zonā, atlasiet nepieciešamo pilsētu/laika zonu augšējā labajā stūrī esošajā nolaižamajā sarakstā. Intervētāja pieejamības režģis tiek atjaunināts atbilstoši jaunajai laika joslai. Šī atlasītā laika josla tagad tiek rādīta arī skatā **Kopsavilkums par intervijām**, kas tiks kopīgots ar intervētājiem un kandidātu. 

6. Noklikšķiniet uz **Nosūtīt intervētājiem**, lai nosūtītu uzaicinājumu uz sapulci iesaistītajiem intervētājiem.

    Pēc intervijas pieprasījumu nosūtīšanas intervētājiem viņi var tiešā veidā atbildēt e-pasta uzaicinājumā, ko viņi ir saņēmuši.

    >[!NOTE]
    > Par katru 1:1 interviju intervētājiem ik pēc 24 stundām tiek nosūtīts atgādinājums, ja intervētājs nav atbildējis uz intervijas pieprasījumu (pieņēmis vai noraidījis).

    > Nevienai paneļintervijai netiek nodrošināti nekādi automatizēti atgādinājumi par intervijas pieprasījumu. Lai manuāli aktivizētu atgādinājumu, rediģējiet interviju un izmantojiet opciju **Atjaunināt un sūtīt**, un pieprasījums tiks vēlreiz nosūtīts intervētājiem.

    Intervētāja atbildes tiek reģistrētas un parādītas programmā Attract. Ja intervētājs noraida uzaicinājumu, jums par to tiek paziņots, lai jūs veiktu izmaiņas. Lai skatītu viņu atbildi programmas **Plānotājs** režģa skatā, noklikšķiniet uz burbuļa ikonas.

[![Attract personāla atlases speciālista skats intervētāja atbildes skatīšanai](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Kad interviju grafiks ir sagatavots kopīgošanai ar kandidātu, noklikšķiniet uz **Nosūtīt kandidātam**. Varat izvēlēties kandidātam rādīt vai nerādīt intervētāju vārdus un nišas.

8. Atlasiet e-pasta ziņojuma veidni un nosūtiet kandidātam kopsavilkumu par intervijām. Kandidāts šo informāciju var skatīt savā e-pasta klientā, kā arī kandidātu portālā.
    
>[!NOTE] 
> Kandidāta kalendārā reģistrētā pieejamība tiek parādīta tikai tad, ja tas ir iekšējs kandidāts. Līdzīgi, tikai iekšējiem kandidātiem var uzlabot interviju grafika ieteikumus. Pašlaik kandidāti (ārējie vai iekšējie) nesaņem e-pasta uzaicinājumu uz sapulci. Tā vietā kandidāts saņem tikai kopsavilkumu par intervijām.

## <a name="feedback-activity"></a>Aktivitāte Atsauksmes

Aktivitāte Atsauksmes ir darba veidnes izvēles aktivitāte. Šī aktivitāte sniedz intervijas dalībniekiem iespēju ievadīt kandidātam paredzētus ieteikumus vai komentārus ar atsauksmēm. Ja tiek atlasīts lauks **Pārmantot aktivitātes Atsauksmes dalībniekus no darbā pieņemšanas grupas**, personāla atlases speciālists, par pieņemšanu darbā atbildīgais vadītājs un intervētāji tiek automātiski pievienoti aktivitātei Atsauksmes. Organizācijas var atļaut intervētajiem skatīt citu personu atsauksmes pirms savu atsauksmju iesniegšanas. Organizācijas var atļaut intervētājiem arī rediģēt savas atsauksmes pēc to iesniegšanas. Intervētājiem tiek atgādināts iesniegt atsauksmes par nesen veiktajām intervijām, pamatojoties uz iepriekš iestatītu konfigurāciju darba veidnes ietvaros. Darbā pieņemšanas vadītājs vai darbam piesaistītais personāla atlases speciālists varat arī manuāli atgādināt intervētājam par atsauksmju iesniegšanu.

## <a name="interview-activity"></a>Aktivitāte Intervija

Aktivitāte Intervija ir izvēles aktivitāte, kas sastāv no trīs komponentiem: Kandidāta pieejamības pieprasījums, Grafiks un Atsauksmes. Izmantojiet aktivitāti Intervija darba veidnē, ja vēlaties komponentus Kandidāta pieejamības pieprasījums, Grafiks un Atsauksme iekļaut procesā, nevis tos izmantot atsevišķi darbā pieņemšanas procesa ietvaros.
