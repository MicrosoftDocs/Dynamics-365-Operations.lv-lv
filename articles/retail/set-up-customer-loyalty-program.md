---
title: Lojalitātes programmas pārskats
description: Šajā tēmā ir aprakstītas lojalitātes programmas iespējas programmā Microsoft Dynamics 365 for Retail un atbilstošās iestatīšanas darbības, kas palīdz mazumtirgotājam viegli sākt darbu ar savām lojalitātes programmām.
author: scott-tucker
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8c2a2347abddf03ed884dcfe68f645fde84c092a
ms.sourcegitcommit: 9b4c3fff2f30006b7bb491ef6ffe89d41bcbfa11
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2019
ms.locfileid: "1863776"
---
# <a name="loyalty-overview"></a>Lojalitātes programmas apskats

[!include [banner](includes/banner.md)]

Lojalitātes programmas var palīdzēt paaugstināt klientu lojalitāti, atlīdzinot klientiem par viņu veikto mijiedarbību ar mazumtirgotāja zīmolu. Programmā Microsoft Dynamics 365 for Retail varat iestatīt vienkāršas vai sarežģītas lojalitātes programmas, kas tiek lietotas jūsu juridiskajām personām jebkurā mazumtirdzniecības kanālā. Šajā tēmā ir aprakstītas lojalitātes programmas iespējas programmā Microsoft Dynamics 365 for Retail un atbilstošās iestatīšanas darbības, kas palīdz mazumtirgotājam viegli sākt darbu ar savām lojalitātes programmām.

Lojalitātes programmu var iestatīt tā, lai tajā būtu ietvertas tālāk aprakstītās opcijas.

- Iestatiet vairākus atlīdzības veidus, ko piedāvās jūsu lojalitātes programmas, un izsekojiet dalību lojalitātes programmās.
- Iestatiet lojalitātes programmas, kas atspoguļos dažādus jūsu piedāvāto atlīdzību atvieglojumus. Jūs varat iekļaut lojalitātes programmas pakāpes, lai piedāvātu lielākus atvieglojumus un atlīdzības klientiem, kuri iepērkas biežāk vai iztērē vairāk naudas jūsu veikalos.
- Definējiet pelnīšanas nosacījumus, lai identificētu darbības, kas klientam ir jāizpilda, lai iegūtu atlīdzību. Varat arī definēt atsaukšanas nosacījumus, lai identificētu, kad un kā klients var atcelt atlīdzības.
- Izsniedziet lojalitātes programmas kartes visos mazumtirdzniecības kanālos, kas piedalās jūsu lojalitātes programmā, un piesaistiet atlaižu kartes vienai vai vairākām lojalitātes programmām, kurās klients var piedalīties. Klienta ierakstu varat arī saistīt ar lojalitātes programmas karti, lai iespējotu lojalitātes programmas punktu apvienošanu no vairākām kartēm un to izpirkšanu.
- Manuāli pielāgojiet lojalitātes programmas kartes vai pārsūtiet lojalitātes programmas atlīdzību bilanci no vienas kartes uz citu, lai uzņemtu vai izsniegtu atlīdzību klientam.

## <a name="setting-up-loyalty-programs"></a>Lojalitātes programmas iestatīšana

Lai iespējotu lojalitātes programmas līdzekli programmā Dynamics 365 for Retail, ir jāiestata vairāki komponenti. Šajā diagrammā redzami lojalitātes programmas komponenti un tas, kā tie saistīti viens ar otru.

![Lojalitātes programmas iestatīšanas procesu plūsma](./media/loyaltyprocess.gif "Lojalitātes programmas komponenti un to savstarpējās saistības")

## <a name="loyalty-components"></a>Lojalitātes komponenti

Šī tabula apraksta katru komponentu un kur to izmanto lojalitātes programmas iestatījumos.

| Komponents                                        | apraksts | Izmantošana |
|--------------------------------------------------|-------------|-----------------|
| Uzstādīt atlaižu (priekšnosacījumus)                  | Iestatīt atlaides, ko piedāvājat lojalitātes programmas klientiem. Varat, piemēram, piedāvāt 5 procentu atlaidi visam apģērbam. | Atlaides ir jāpievieno cenu grupām, pirms to iekļaušanas lojalitātes programmā. Cenu grupas tiek piešķirtas lojalitātes programmai un lojalitātes programmas līmeņiem. |
| Iestatiet cenu grupas (priekšnosacījumi)               | Cenu grupas tiek izmantotas, lai izveidotu un pārvaldītu cenas un atlaides mazumtirdzniecības produktiem. Iestatīt cenu grupas, kas ietver atlaides, kas attiecas uz jūsu lojalitātes programmu. | Cenu grupas tiek piešķirtas lojalitātes programmām un lojalitātes programmu līmeņiem. |
| Uzstādīt kanālus (priekšnosacījumi)                   | Mazumtirdzniecības kanāli ir tādi veikali kā tirdzniecības veikali, tiešsaistes veikali un zvanu centri, kas piedalās jūsu lojalitātes programmā. Jums ir jāiestata mazumtirdzniecības kanāli pirms to piešķiršanas lojalitātes programmai. | Varat piešķirt mazumtirdzniecības kanālus lojalitātes programmai, ja mazumtirdzniecības kanāls piedalās lojalitātes programmā. |
| Iestatiet lojalitātes programmas maksāšanas metodi (priekšnosacījums) | Maksāšanas metode ir jāiestata pirms lojalitātes programmas karti var izmantot pie kases un lojalitātes punktu uzskaitīšanai kā daļai no lojalitātes programmas. Lojalitātes programmas maksāšanas metode ir arī jāpievieno klientiem mazumtirdzniecības kanālā, pirms lojalitātes programmas punktus var izmantot norēķinos par precēm. | Iestatiet lojalitātes programmas maksājuma metodes veidu, un pēc tam piešķiriet lojalitātes programmas maksāšanas metodi mazumtirdzniecības kanāliem, kas piedalās lojalitātes programmā. |
| Iestatīt datumu intervālus                            | Datumu intervāli sniedz elastīgu veidu, kā iestatīt laika posmu, kas attiecas uz lojalitātes programmas līmeņiem. Izmantojiet datumu intervālus, lai norādītu, cik ilgi klients var palikt konkrētā līmenī, vai cik daudz laika klientam vajadzīgs, lai kvalificētos līmenim. | Datumu intervāli ir spēkā tikai tad, ja lojalitātes programmā izmantojat līmeņu sistēmu. Jāatlasa datumu intervāls, kas attiecas uz programmas līmeņiem, kā arī datumu intervālus, kas attiecas uz programmu līmeņu nosacījumiem. |
| Atlīdzības punktu iestatīšana                             | Atlīdzības punkti ir atlīdzības veids, kas tiek piedāvāts klientiem. Atlīdzības punkti var būt izpērkami vai neizpērkami. Izpērkamus atlīdzības punktus var apmainīt pret precēm. Neizpērkamus atlīdzības punktus var izmantot novērošanas nolūkā vai arī klienta paaugstināšanai uz nākamo atlīdzības programmas līmeni. | Atlīdzības punkti ir atrunāti līmeņu nosacījumos un tiek izmantoti, lai kvalificētu klientu noteiktam līmenim. Atlīdzības punkti ir arī atrunāti lojalitātes programmas shēmās pelnīšanas un izpirkšanas noteikumos. Pelnīšanas nosacījumos jūs norādāt atlīdzību, ko klients var nopelnīt par noteiktu darbību. Izpirkuma nosacījumos jūs norādāt atlīdzības, ko klients var apmainīt pret punktiem. |
| Lojalitātes programmu iestatīšana                          | Lojalitātes programma ir kodols jūsu piedāvātās lojalitātes programmas elementam. Katrai lojalitātes programmai var būt piešķirti arī lojalitātes programmas līmeņi. Atlaižu un cenu grupas tiek piešķirtas lojalitātes programmām jebkurā programmu līmenī vai pakāpes līmenī. | Jūs izveidojat lojalitātes programmas shēmas lojalitātes programmām. Jūs piešķirat lojalitātes programmas kartes jūsu lojalitātes programmā, un atlaižu kartes var tikt piešķirtas klientam. Mazumtirdzniecības kanāli piedalās lojalitātes programmās, kas ir piešķirtas lojalitātes programmu shēmām. Jebkurš klients ar lojalitātes programmas karti var piedalīties lojalitātes programmā, kas ir piesaistīta kartei. |
| Iestatīt lojalitātes programmas līmeņus un līmeņu nosacījumus              | Lojalitātes programmas līmeņi nav obligāti, taču tos varat noteikt lojalitātes programmās. Varat iestatīt bāzes atlaides un atlīdzības visiem klientiem, kuri piedalās lojalitātes programmā, un varat iestatīt papildu atlaides un atlīdzības klientiem, kuri sasniedz dažādus programmas līmeņus. Katram noteiktajam lojalitātes līmenim ir iespējams iestatīt kārtulas, kas kvalificē klientu šim līmenim. Varat arī noteikt, cik ilgi klienti var palikt noteiktā līmenī pēc tā sasniegšanas. | Lojalitātes programmas līmeņi un programmas līmeņu nosacījumi tiek atrunāti lojalitātes programmā. Ja nenosakāt nekādus lojalitātes programmas līmeņus, visi klienti, kuri piedalās lojalitātes programmā, pretendē uz atlaidēm, ko piešķirat lojalitātes programmas cenu grupā. Ja nosakāt lojalitātes programmas līmeņus, varat iestatīt pelnīšanas un izpirkšanas noteikumus programmas līmeņos lojalitātes programmas shēmā. |
| Lojalitātes programmas shēmu iestatīšana                           | Lojalitātes programmas shēmā norādiet pelnīšanas un izpirkšanas noteikumus, kas attiecas uz atlasīto lojalitātes programmu. Piešķiriet mazumtirdzniecības kanālus lojalitātes programmas shēmai, lai identificētu, kura lojalitātes programma, pelnīšanas un izpirkšanas noteikumi attiecas uz mazumtirdzniecības veikalu. | Lojalitātes programmas shēma tiek piešķirta lojalitātes programmai un mazumtirdzniecības kanāliem. Varat piešķirt vairākas lojalitātes programmas shēmas vienai un to pašai lojalitātes programmai, un vairākas lojalitātes programmas shēmas varat piešķirt vairākiem mazumtirdzniecības kanāliem. |
| Lojalitātes programmas karšu iestatīšana                             | Jebkurš klients ar lojalitātes programmas karti var piedalīties lojalitātes programmā, kas ir piesaistīta kartei. Lojalitātes programmas kartes var izsniegt anonīmi vai tās var piešķirt noteiktam klientam. Varat apskatīt lojalitātes programmas darījumus konkrētu kartei, un varat apskatīt kopsavilkumu lojalitātes programmas punktiem, kas ir uzkrāti kartē. Lojalitātes programmas kartes varat izsniegt no jebkura mazumtirdzniecības kanāla. Varat arī manuāli pielāgot lojalitātes programmas karti, lai paaugstinātu klientu uz citu līmeni, pievienotu lojalitātes programmas punktus vai pārsūtītu lojalitātes programmas punktu bilanci no vienas kartes uz citu. | Lojalitātes programmas varat piešķirt lojalitātes programmas kartei. |

## <a name="loyalty-processes"></a>Lojalitātes programmas procesi

Šī tabula apraksta procesus, kas jāveic, lai sūtītu lojalitātes programmas konfigurācijas un datus jūsu veikaliem, kā arī, lai saņemtu no tiem lojalitātes programmas darbības.

| Procesa nosaukums                         | Apraksts | Lapas nosaukums |
|--------------------------------------|-------------|-----------|
| 1050 (Informācija par lojalitātes programmu)           | Izpildiet šo procesu, lai nosūtītu lojalitātes programmas datus no programmas Dynamics 365 for Retail uz mazumtirdzniecības veikaliem. Ir ieteicams šo procesu ieplānot un palaist to biežāk, tādējādi lojalitātes programmas dati tiks nosūtīti uz visiem veikaliem. | Sadales grafiks |
| Procesa lojalitātes programmas shēmas              | Palaidiet šo procesu, lai saistītu lojalitātes programmas shēmas ar mazumtirdzniecības kanāliem, kas tiek piešķirta lojalitātes programmas shēmai. Šo procesu var ieplānot tā, lai to varētu palaist kā pakešveida apstrādi. Šis process ir jāpalaiž, ja maināt lojalitātes programmas konfigurācijas datus, piemēram, lojalitātes programmas shēmas, lojalitātes programmas vai lojalitātes programmas atlīdzības punktus. | Procesa lojalitātes programmas shēmas |
| Apstrādāt bezsaistes lojalitātes programmu darījumus | Palaidiet šo procesu, lai atjauninātu lojalitātes programmas kartes tā, lai tiktu iekļauti bezsaistē apstrādāti darījumi. Šis process tiek lietots tikai tad, ja lapā **Retail koplietojamie parametri** ir atzīmēta izvēles rūtiņa **Iegūt bezsaistē**, lai atlīdzības varētu nopelnīt bezsaistē. | Apstrādāt bezsaistes lojalitātes programmu darījumus |
| Atjaunināt lojalitātes programmas kartes pakāpes            | Palaidiet šo procesu, lai izvērtētu klienta punktu nopelnīšanas darbības atbilstoši lojalitātes programmas pakāpju kārtulām un atjauninātu klienta pakāpes statusu. Šis process ir nepieciešams tikai tad, ja maināt līmeņu noteikumus lojalitātes programmā un vēlaties atjauninātos noteikumus piemērot jau izsniegtajām lojalitātes programmas kartēm. Šo procesu var palaist kā pakešveida apstrādi vai tikai konkrētām kartēm. | Atjaunināt lojalitātes programmas kartes pakāpes |

## <a name="loyalty-enhancements"></a>Lojalitātes programmas uzlabojumi

Kā daļu no 2018. gada oktobra laidiena programma Retail ir ieguvusi jaunu lojalitātes programmas funkcionalitāti. Tālāk ir aprakstīts katrs no jaunajiem uzlabojumiem.

- Kā daļu no lojalitātes programmas shēmas iepriekšējos laidienos mazumtirgotāji varēja izveidot dažādas nopelnīšanas un izpirkšanas kārtulas atkarībā no pakāpēm, lai nošķirtu atlīdzības klientiem dažādās pakāpēs. Tagad kā daļu no nopelnīšanas un izpirkšanas kārtulām mazumtirgotāji var ietvert arī “piederības”, lai noteikta klientu grupa varētu veidot daļu no pastāvošajām pakāpēm, bet šiem klientiem tik un tā tiktu atlīdzināts atšķirīgi. Šādi tiek novērta nepieciešamība veidot papildu pakāpes.
    
    > [!NOTE]
    > Lojalitātes shēmā ietvertās nopelnīšanas kārtulas ir papildinošas. Piemēram, ja ir izveidota kārtula zelta pakāpes dalībniekam kā atlīdzību piešķirt 10 punktus par katru ASV dolāru, un ja ir izveidota arī kārtula klientam ar piederību “veterāns” kā atlīdzību piešķirt 5 punktus par katru ASV dolāru, tad veterāns, kurš ir arī dalībnieks ar zelta pakāpi, nopelnītu 15 punktus par 1 ASV dolāru, jo šis klients ir kvalificēts abām rindām. Taču, ja klients–veterāns nebūtu zelta pakāpes dalībnieks, šis klients nopelnītu 5 punktus par katru dolāru. Lai atspoguļotu izmaiņas kanālos, palaidiet darbu **Apstrādāt lojalitātes shēmas** un **1050** (informācija par lojalitātes programmu).
    
    ![Uz piederību balstīta pelnīšana](./media/Affiliation-based-earning.png "Uz piederību balstīta pelnīšana")

- Mazumtirgotājiem bieži vien ir īpašas cenas noteiktai klientu grupai, kuriem mazumtirgotāji nevēlas piemērot lojalitātes programmas. Šāda grupa varētu būt, piemēram, vairumtirgotāji vai darbinieki, kas saņem īpašu izcenojumu un lojalitātes programmas punktus. Parasti “piederības” tiek izmantotas, lai šādām klientu grupām nodrošinātu īpašu izcenojumu. Lai noteiktām klientu grupām liegtu iespēju pelnīt lojalitātes programmas punktus, mazumtirgotājs var norādīt vienu vai vairākas piederības savas lojalitātes programmas shēmas sadaļā **Izslēgtās piederības**. Tādējādi, ja klienti, kas ir ietverti kādā izslēgtā piederībā, ir pastāvošas lojalitātes programmas dalībnieki, viņi nevarēs nopelnīt lojalitātes programmas punktus par saviem pirkumiem. Lai atspoguļotu izmaiņas kanālos, palaidiet darbu **Apstrādāt lojalitātes shēmas** un **1050** (informācija par lojalitātes programmu).

    ![Izslēgtās piederības](./media/Excluded-affiliations.png "Piederību izslēgšana no lojalitātes programmas punktu pelnīšanas")
    
- Mazumtirgotāji var ģenerēt lojalitātes programmas karšu numurus kanālos. Pirms 2018. gada oktobra atjauninājuma mazumtirgotāji varēja izmantot fiziskas lojalitātes kartes vai ģenerēt lojalitātes karti, izmantojot unikālu informāciju par klientu, piemēram, tālruņa numuru. Lai iespējotu lojalitātes programmas karšu automātisko ģenerēšanu mazumtirdzniecības veikalos, ar veikalu saistītajā funkcionalitātes profilā ieslēdziet opciju **Ģenerēt lojalitātes programmas kartes numuru**. Lai izsniegtu lojalitātes programmas kartes klientiem tiešsaistes kanālos, mazumtirgotāji var izmantot IssueLoyaltyCard API. Mazumtirgotāji var nodrošināt šim API lojalitātes programmas kartes numuru, kas tiks izmantots lojalitātes programmas kartes ģenerēšanai, vai arī sistēma izmanto programmā Dynamics 365 for Retail iestatīto lojalitātes programmas karšu numuru sēriju. Taču, ja API izsaukšanas laikā nav nevienas numuru sērijas un mazumtirgotājs nenorāda lojalitātes programmas kartes numuru, tiek parādīta kļūda.

    ![Lojalitātes programmas kartes ģenerēšana](./media/Generate-loyalty-card.png "Lojalitātes programmas kartes numura automātiska ģenerēšana")

- Nopelnītie un izpirktie lojalitātes programmas punkti tagad tiek saglabāti par katru transakciju un pārdošanas pasūtījumu attiecībā pret pārdošanas rindu, tādēļ pilnīgas vai daļējas preču atgriešanas gadījumā var atlīdzināt vai atņemt to pašu summu. Turklāt šī punktu redzamība pārdošanas rindas līmenī sniedz iespēju zvanu centra lietotājiem atbildēt uz klientu jautājumiem par to, cik punktu katrai rindai tika nopelnīti vai izpirkti. Pirms šo izmaiņu ieviešanas atlīdzības punkti vienmēr tika pārrēķināti preču atgriešanas laikā, tādēļ tika iegūta no sākotnējās atšķirīga summa, ja nopelnīšanas vai izpirkšanas kārtulas bija mainītas, un zvanu centra lietotājiem nebija redzams punktu sadalījums. Punktus katrai lojalitātes programmas kartei var apskatīt formā **Karšu transakcijas**. Lai iespējotu šo līdzekli, ieslēdziet konfigurācijas opciju **Grāmatot lojalitātes punktus par katru pārdošanas rindu** cilnē **Mazumtirdzniecības koplietojamie parametri** \> **Vispārīgi**.

    > [!NOTE]
    > Ir ļoti ieteicams ieslēgt šo līdzekli, lai nodrošinātu pareizā punktu skaita atmaksu debitoram vai iekasēšanu no debitora atgriešanas gadījumā.

- Tagad mazumtirgotāji var definēt piešķiršanas periodu katram atlīdzības punktam. Piešķiršanas perioda konfigurācijas definē laiku, cik ilgi pēc nopelnīšanas datuma atlīdzības punkti kļūst pieejami klientiem. Nepiešķirtos punktus var skatīt lapas **Lojalitātes programmas kartes** kolonnā **Nepiešķirtie punkti**. Turklāt mazumtirgotāji var definēt maksimālo lojalitātes programmas atlīdzības punktu ierobežojumu vienai lojalitātes programmas kartei. Šo lauku var izmantot, lai samazinātu lojalitātes programmas krāpšanas ietekmi. Kad ir sasniegts maksimālais piešķiramo punktu skaits, lietotājs nevar nopelnīt vairāk punktu. Mazumtirgotājs var izlemt bloķēt šādas kartes, līdz ir veikta izmeklēšana par potenciālu krāpšanu. Ja mazumtirgotājs konstatē krāpšanu, mazumtirgotājs var ne tikai bloķēt šī klienta lojalitātes programmas karti, bet var arī atzīmēt kā bloķētu pašu klientu. Lai to izdarītu, kopsavilkuma cilnes **Mazumtirdzniecība** sadaļā **Visi debitori** rekvizītu **Bloķēt klientam reģistrēšanos lojalitātes programmā** iestatiet uz **Jā**. Bloķētajiem klientiem nevarēs izsniegt lojalitātes programmas karti nevienā no kanāliem.

    ![Atlīdzības punktu piešķiršana un maksimālais skaits](./media/Vesting-and-maximum-reward-points.png "Atlīdzības punktu piešķiršanas un maksimālā skaita definēšana")

- Piederības tiek izmantotas, lai nodrošinātu īpašu izcenojumu un atlaides, bet pastāv dažas piederības, kuras mazumtirgotāji nevēlaties rādīt saviem klientiem. Piemēram, dažiem klientiem varētu nepatikt piederība ar nosaukumu “Daudz tērējošs klients”. Turklāt pastāv dažas piederības, ko nevajadzētu pārvaldīt veikalā, piemēram, piederību “darbinieki”, jo jūs nevēlaties, lai kasieri varētu izlemt, kurš ir darbinieks, līdz ar to piešķirot uz darbinieka statusu balstītas atlaides. Tagad mazumtirgotāji var atlasīt piederības, kuras mazumtirdzniecības kanālos būtu jāslēpj. Piederības, kas ir atzīmētas kā **Slēpt kanālos**, nevar skatīt, pievienot vai noņemt pārdošanas punktos (POS). Taču precēm tik un tā tiek izmantoti ar piederību saistītie izcenojumi un atlaides.

    ![Piederību slēpšana](./media/Hide-affiliations.png "Piederību slēpšana kanālos")
    
- Zvanu centra lietotāji tagad var vienkāršāk meklēt klientu, izmantojot informāciju par klienta lojalitātes programmas karti, un pāriet uz klienta lojalitātes programmas kartes un lojalitātes programmas transakciju lapām no lapas **Klientu apkalpošana**.

    ![Klientu apkalpošana](./media/Customer-service.png "Klienta lojalitātes programmas informācijas atrašana")
    
- Ja lojalitātes programmas karte ir bojāta, ir nepieciešams ģenerēt aizstāšanas karti un esošos punktus pārsūtīt uz jauno karti. Šajā laidienā aizstāšanas kartes plūsma ir vienkāršota. Turklāt klienti dažus vai visus savus lojalitātes programmas punktus var dāvināt draugiem un ģimenes locekļiem. Kad punkti tiek pārsūtīti, katrai lojalitātes programmas kartei tiek izveidoti punktu korekcijas ieraksti. Aizstāšanas kartes un pārsūtīšanas bilances funkcionalitātei var piekļūt no lapas **Lojalitātes programmas kartes**.

    ![Aizstāšana un punktu pārsūtīšana](./media/Replace-and-transfer-points.png "Lojalitātes programmas kartes aizstāšana vai bilances pārsūtīšana")
    
- Mazumtirgotājiem var būt nepieciešamība tvert informāciju par konkrēta kanāla efektivitāti attiecībā uz klientu reģistrēšanu lojalitātes programmā. Tagad tiek saglabāts lojalitātes programmu karšu reģistrācijas avots, tādēļ mazumtirgotāji var izmantot šos datus pārskatiem. Reģistrācijas avots tiek automātiski tverts visām izsniegtajām lojalitātes programmas kartēm no MPOS/CPOS vai e-komercijas kanāliem. Lojalitātes programmas kartēm, kas tiek izsniegtas no dokumentu apstrādes biroja programmas, zvanu centra lietotājs var atlasīt atbilstošu kanālu.
- Iepriekšējos laidienos mazumtirgotāji varēja izmantot MPOS/CPOS, lai izpirktu lojalitātes programmas punktus klientiem veikalā. Taču, tā kā lojalitātes programmas bilance tiek rādīta kā lojalitātes punktu skaits, šajos laidienos kasieris nevarēja redzēt valūtas vērtību tai summai, ko varētu lietot attiecībā uz pašreizējo transakciju. Pirms lojalitātes programmas punktu izmaksāšanas kasierim šie punkti bija jākonvertē valūtā. Pašreizējā laidienā, kad rindas ir pieskaitītas transakcijai, kasieris var redzēt, kādu lojalitātes programmas punktu summu var izmantot pašreizējās transakcijas segšanai, tādēļ transakcijai var ērti lietot dažus vai visus lojalitātes programmas punktus. Turklāt kasieris var redzēt punktus, kuru derīgums beigsies nākamo 30 dienu laikā, tādēļ kasieris var veikt papildu pārdošanu un šķērspārdošanu, lai motivētu klientu transakcijā iztērēt punktus, kam beidzas derīguma termiņš.

    ![Ar lojalitātes programmas punktiem segtā bilance](./media/Points-covered-by-loyalty-balance.png "Ar lojalitātes programmas punktiem segtās bilances rādīšana")

    ![Punkti, kam beidzas derīguma termiņš](./media/Expiring-points.png "Derīguma termiņam tuvojošos punktu skatīšana")

- Versijas 8.1.3 laidienā zvanu centra kanālā ir iespējota opcija Maksāt ar lojalitātes programmas punktiem. Lai iespējotu šo opciju, izveidot lojalitātes programmas norēķinu veidu un saistiet to ar zvanu centru. 

    > [!NOTE]
    > Tā kā lojalitātes programmas maksājumi ir iestatīti kā maksājumu ar karti, lapā **Kartes iestatīšana** ir jāatlasa kāda karte. 

    ![Lojalitātes programmas kartes iestatīšana](./media/LoyaltyCardSetup.png "Lojalitātes programmas kartes iestatīšana")

    Pēc šo iestatījumu veikšanas debitori var izpirkt savus lojalitātes programmas punktus zvanu centrā. Turklāt esam vēl vairāk uzlabojuši lietotāju pieredzi, nodrošinot parametra Summa, ko var apmaksāt ar lojalitātes punktiem, lai zvanu centra lietotāji varētu skatīt lojalitātes programmas bilanci, nepārejot uz citu ekrānu.

- Daudzi mazumtirgotāji piešķir lojalitātes programmas punktus, pamatojoties tikai uz pārdošanas transakcijām, taču mazumtirgotāji, kas vairāk orientējas uz debitoriem, vēlas atlīdzināt debitoriem par jebkuru mijiedarbību ar attiecīgo zīmolu. Piemēram, šie mazumtirgotāji vēlas sniegt atlīdzības par tiešsaistes aptaujas aizpildīšanu, veikala apmeklēšanu, mazumtirgotāja profila atzīmēšanu ar Patīk pakalpojumā Facebook vai Twitter sīkziņu publicēšanu par šo mazumtirgotāju. Lai to izdarītu, mazumtirgotājs var definēt neierobežotu skaitu cita aktivitātes veida aktivitāšu un definēt tām attiecīgās pelnīšanas kārtulas. Ir pieejams arī pakļauts Retail Server API PostNonTransactionalActivityLoyaltyPoints, ko var izsaukt, kad tiek noteikta aktivitāte, par kuru debitoram ir jāpiešķir lojalitātes programmas punkti. Šim API ir nepieciešami parametri Lojalitātes kartes ID, Kanāla ID un Cita aktivitātes veida ID, lai varētu atrast debitoru, kuram ir jānodrošina atlīdzība, un noteikt šis aktivitātes pelnīšanas kārtulu. 

    Punktu piešķiršana par aktivitātēm, kas nav saistītas ar transakcijām, parasti sastāv no divām galvenajām darbībām, kas ir norādītas tālāk.

    - Noteikšana, ka ir notikusi aktivitāte, par kuru ir jānodrošina atlīdzība.
    - Atbilstošā punktu skaita piešķiršana.

    Pirmā ir ārpus programmas Microsoft Dynamics 365 for Retail veikta darbība, piemēram, Twitter sīkziņas publicēšana par zīmolu vai zīmola profila atzīmēšana ar Patīk pakalpojumā Facebook. Kad ir atpazīta šī aktivitāte, mazumtirgotāji var izsaukt iepriekš minēto Retail Server API un reāllaikā piešķirt lojalitātes programmas punktus. Šādos gadījumos nav nepieciešama pārskatīšanas darbība, jo ir notikusi aktivitāte un ir jāpiešķir atbilstošais punktu skaits. Taču noteiktos gadījumos mazumtirgotājs var vēlēties pārskatīt ierakstus pirms punktu piešķiršanas. Piemēram, mazumtirgotājs veikalā rīko semināru, kuram debitori var reģistrēties e-komercijas tīmekļa vietnē vai jebkurā citā notikumu reģistrācijas lietojumprogrammā. Taču lojalitātes programmas punkti ir jāpiešķir tikai tiem debitoriem, kuri ir ieradušies. Šādiem gadījumiem versijas 10.0 laidienā ir ietverts datu elements ar nosaukumu **Mazumtirdzniecības lojalitātes programmas citas aktivitātes veida rindas**. Šis datu elements sniedz mazumtirgotājiem iespēju izmantot datu importēšanas/eksportēšanas struktūru (Data Import/Export Framework — DIXF) vai OData API, lai reģistrētu aktivitātes, par kurām debitoriem ir jāpiešķir lojalitātes programmas punkti. Datu elements nodrošina aktivitāšu glabāšanu žurnālā ar nosaukumu **Citu aktivitāšu lojalitātes programmas rindas**, ko var izmantot pārskatīšanas un izmainīšanas nolūkiem. Pēc datu pārskatīšanas IT lietotājs var manuāli grāmatot aktivitāšu rindas vai izpildīt darbu ar nosaukumu **Apstrādāt cita aktivitātes veida lojalitātes programmas rindas**, kas nodrošina visu negrāmatoto aktivitāšu rindu grāmatošanu un punktu piešķiršanu debitoriem, pamatojoties uz pelnīšanas kārtulām. Iepriekš aprakstītajā gadījumā notikumu reģistrācijas lietojumprogramma izsauc OData API, lai nosūtītu debitora informāciju uz programmu Dynamics 365 for Retail. Taču IT lietotājs var grāmatot tikai to debitoru aktivitāšu rindas, kuri apmeklēja semināru, un dzēst citu debitoru aktivitāšu rindas. 

    > [!NOTE]
    > Pašlaik sistēma prasa lietotājiem piespiedu kārtā iestatīt numuru sēriju citiem aktivitātes veidiem, taču turpmākajos laidienos tā nebūs obligāta darbība. Lai iestatītu numuru sēriju, pārejiet uz sadaļu **Mazumtirdzniecības koplietojamie parametri** \> **Numuru sērijas** un atlasiet numuru sēriju vienumam **Lojalitātes programmas cita aktivitātes veida ID**.

- Lai debitoriem nodrošinātu labu apkalpošanu un ātri izpildītu debitoru pieprasījumus, ir svarīgi kasierim nodrošināt piekļuvi visam debitora profilam. Versijas 10.0 laidienā kasieris varēs POS sistēmā skatīt lojalitātes programmas vēstures informāciju, kā arī informāciju par saistīto lojalitātes programmu un pakāpi.
- Bezmaksas nosūtīšana vai nosūtīšana ar atlaidi ir viens no īpaši motivējošajiem faktoriem, lai klienti iepirktos tiešsaistē. Lai mazumtirgotāji varētu iestatīt piegādes akcijas, versijas 10.0 laidienā ir ieviests jauns akcijas veids ar nosaukumu “Piegādes sliekšņa atlaide”, kurā mazumtirgotājs var definēt sliekšņus, pēc kuru sasniegšanas debitori var saņemt piegādes atlaidi vai bezmaksas piegādi. Piemēram, bezmaksas piegāde divu dienu laikā pasūtījumiem virs 35 USD vai bezmaksas piegāde divu dienu laikā visiem lojalitātes programmas debitoriem. Šis līdzeklis izmanto jauno papildu automātisko maksu iespēju. Skatiet [dokumentāciju par papildu automātiskajām maksām](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges). Šīs papildu automātiskās maksas ir jāiespējo, lai darbotos piegādes akcija. Tās var iespējot, ieslēdzot konfigurācijas opciju Izmantot papildu automātiskās maksa lapas **Mazumtirdzniecības rekvizīti** cilnē**Debitoru pasūtījumi**. Turklāt, tā kā mazumtirgotājs var iestatīt vairākus maksu veidus, piemēram, apstrādes un uzstādīšanas maksas, mazumtirgotājam ir jānorāda, kura maksa tiek uzskatīta par piegādes maksu. Piegādes atlaides attiecas tikai uz piegādes maksām. Lai norādītu, ka maksas ir piegādes maksas, pārejiet uz formu **Maksas kodi**, kas ir pieejama sadaļā **Mazumtirdzniecība** \> **Mazumtirdzniecības IT** \> **Kanāla iestatīšana** \> **Maksas**, un atzīmējiet attiecīgās maksas izvēles rūtiņu Piegādes maksa. Tagad varat pāriet uz formu **Mazumtirdzniecības piegādes sliekšņa atlaide** un iestatīt atlaidi.

    Līdzīgi kā preču atlaidēm, arī šai atlaidei ir pieejamas visas esošās standarta atlaides iespējas, piemēram, iespēja mazumtirgotājam ierobežot šīs atlaides, izmantojot kuponus, lai šīs atlaides varētu saņemt tikai tie debitori, kuriem ir kuponi. Turklāt šīm atlaidēm tiek izmantota cenu grupu iespēja, lai noteiktu piemērotību šo atlaižu saņemšanai. Piemēram, mazumtirgotājs var izvēlēties izpildīt šīs akcijas tikai tiešsaistes kanālos un/vai visos kanālos noteiktām debitoru grupām, piemēram, lojalitātes programmas debitoriem. Ja pasūtījuma rindas ar norādīto piegādes režīmu atbilst definētajam slieksnim, tiek lietota piegādes atlaide un piegādes maksas tiek samazinātas, pamatojoties uz iestatīto atlaidi. 

    > [!NOTE]
    > Atšķirībā no citām periodiskajām atlaidēm, piemēram, daudzuma, vienkāršajām, komplekta un sliekšņa atlaidēm, piegādes atlaides lietošanas gadījumā netiek pievienota atlaides rinda, bet gan tiek tiešā veidā rediģēta piegādes maksa un maksas aprakstam pievienots atlaides nosaukums.
