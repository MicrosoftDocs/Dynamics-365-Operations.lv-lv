---
title: "Pasūtījumu solīšana"
description: "Šajā rakstā ir sniegta informācija par pasūtījuma solīšanu. Pasūtījuma solīšana jums palīdz saviem klientiem droši apsolīt piegādes datumus un nodrošina elastību, lai jūs spētu ievērot solītos datumus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8aa0a58b03ee18e42ca7770ea3e22311c1ddba67
ms.lasthandoff: 03/31/2017


---

# <a name="order-promising"></a>Pasūtījumu solīšana

Šajā rakstā ir sniegta informācija par pasūtījuma solīšanu. Pasūtījuma solīšana jums palīdz saviem klientiem droši apsolīt piegādes datumus un nodrošina elastību, lai jūs spētu ievērot solītos datumus.

Pasūtījumu solīšana aprēķina agrākos nosūtīšanas un saņemšanas datumus, un tā ir balstīta uz piegādes datuma kontroles metodi un transportēšanas dienām. Varat izvēlēties no četrām piegādes datuma kontroles metodēm:

-   **Pārdošanas izpildes laiks** -pārdošanas izpildes laiks ir laiks starp pārdošanas pasūtījuma izveidi un preču nosūtīšanas. Piegādes datumu aprēķina pamatā ir noklusējuma vairākas dienas un neuzskata par krājumu pieejamību, zināmu pieprasījuma vai plānoto piegādes.
-   **ATP (pieejams solīšanai)** -ATP ir daudzums krājumu, kas ir pieejama, un klients var solīja noteiktā datumā. ATP aprēķinā tiek iekļauti nesaistītie krājumi, izpildes laiki, plānotās ieejas plūsmas un izejas plūsmas.
-   **ATP + Izejas plūsmas rezerve **— nosūtīšanas datums ir vienāds ar ATP datumu, pieskaitot krājuma izejas plūsmas rezervi. Izejas plūsmas rezerve ir laiks, kas ir nepieciešams, lai krājumus sagatavotu sūtīšanai.
-   **CTP (pieejams solīšanai) **— pieejamība tiek aprēķināta, izmantojot izvēršanu.

## <a name="atp-calculations"></a>ATP aprēķini
ATP daudzums tiek aprēķināts, izmantojot metodi "kumulatīvo ATP ar skatienu uz priekšu". Galvenais šīs ATP aprēķinu metodes priekšrocība ir tā, ka tā var rīkoties gadījumos, kad problēmas starp ieņēmumu summa ir vairāk nekā jaunāko kvīti, kura apliecina (piemēram, ja no iepriekšējām ieejas plūsmas daudzums ir jāizmanto prasībai). "Skatīties uz priekšu ar kumulatīvo ATP" aprēķina metode ietver visus jautājumus, kas līdz kumulatīvā daudzuma saņemšanai pārsniedz kopējo daudzumu izsludināt. Tāpēc šī ATP aprēķina metode novērtē, vai kaut ko no agrāka perioda daudzuma var lietot vēlākā periodā.  

ATP daudzums ir nesaistītā krājumu bilance pirmajā periodā. Parasti tas tiek aprēķināts katram periodam, kurā ir plānota ieejas plūsma. Programma aprēķina ATP periodu dienās un aprēķina pašreizējo datumu kā pirmo datumu ATP daudzumam. Pirmajā periodā ATP ietver rīcībā esošos krājumus, atņemot debitoru pasūtījumus, kas ir jāizpilda vai ir nokavēti.  

ATP tiek aprēķināts, izmantojot šādu formulu:  

ATP = ATP iepriekšējā perioda + kvītis par pašreizējā periodā – jautājumi par pašreizējo periodu-neto izdošanas daudzums par katru turpmāko periodu līdz periodam, kad apliecinājumi visiem periodiem, līdz un ieskaitot nākamā perioda summa pārsniedz summu jautājumiem līdz un ieskaitot turpmāko periodu.  

Kad vairāk nav izdošanu un saņemšanu apsvēršanai, ATP daudzums sekojošajiem datumiem ir tāds pats, kā pēdējais aprēķinātais ATP daudzums.  

Ja nav norādītas visas dimensijas, kas tiek izmantotas krājumam, kad tiek pabeigta ATP pārbaude, tās joprojām var norādīt izejas plūsmā un ieejas plūsmā. Šajā gadījumā ATP aprēķinā ieejas un izejas plūsmas ir jāapkopo esošajām dimensijām, lai samazinātu ieejas un izejas plūsmu rindu skaitu, kas izmantots ATP aprēķinā.  

ATP daudzums, kas tiek rādīts, vienmēr ir lielāks par vai vienāds ar 0 (nulle). Ja aprēķins atgriež negatīvu ATP daudzumu (piemēram, ja iepriekš apsolītais daudzums pārsniedz pieejamo daudzumu), programma daudzumu automātiski iestata uz **0**.

### <a name="example"></a>Piemērs

Lauks **ATP atpakaļejošā pieprasījuma laika periods** kontrolē, cik tālu iepriekš jāmeklē aizkavēti pieprasījuma pasūtījumi vai krājumu izejas plūsmas. Lauks **ATP atpakaļejošā piedāvājuma laika periods** kontrolē, cik tālu iepriekš jāmeklē aizkavēti piedāvājuma pasūtījumi vai krājumu ieejas plūsmas. Piemēram, ja pasūtījumi, kas aizkavējušies tikai par septiņām dienām, ir jāņem vērā ATP aprēķinā, tad abi lauki ir jāiestata uz **7**.  

Lauki **ATP atliktā pieprasījuma laika periods** un **ATP atliktā piedāvājuma laika periods** kontrolē, kad ATP aprēķinā tiek ņemti vēra atliktie pieprasījumi vai piedāvājumi. Piemēram, ja atliktais piedāvājums un pieprasījums ATP aprēķinā ir jāņem vērā parīt, abi lauki ir jāiestata uz **2**. Vērtība **2** nozīmē, ka krājumu daudzums aizkavētā pirkšanas pasūtījumā, kurš ir jāņem vērā ATP aprēķinā, tiks uzskatīts par pieejamu divas dienas pēc pašreizējā datuma.  

Nākamajam piemēram laukos **ATP atpakaļejošā pieprasījuma laika periods** un **ATP atpakaļejošā piedāvājuma laika periods** tiek ievadīta vērtība **7**, un laukos **ATP atliktā pieprasījuma laika periods** un **ATP atliktā piedāvājuma laika periods** tiek ievadīta vērtība **1**.  

Vēl nav saņemts pirkšanas pasūtījums par 200 gab. preces, kas bija jāsaņem pirms trim dienām. Tāpēc nav nosūtīta pārdošanas pasūtījuma rinda par 75 gab. tās pašas preces, kas bija jānosūta vakar.  

Klients zvana ar vēlas pasūtīt 150 gab. tās pašas preces. Kad pārbaudāt preces pieejamību, varat atrast, ka 10 dienas vēlāk tiks piegādāts cits pirkšanas pasūtījums par 100 gab. preces.  

Jūs izveidojat pārdošanas pasūtījuma rindu par preci un ievadāt **150** kā daudzumu.  

Tā kā piegādes datuma kontroles metode ir ATP, tiek aprēķināti ATP dati, lai atrastu agrāko iespējamo nosūtīšanas datumu. Pamatojoties uz iestatījumiem, kavējas iepirkuma pasūtījumu un pārdošanas pasūtījumu tiek uzskatīti par un pašreizējā datuma iegūtās ATP daudzums ir 0. Rīt, kad kavējas iepirkuma pasūtījumā ir paredzams saņemt, ATP daudzums tiek aprēķināts kā vairāk par 0 (šajā gadījumā tā tiek aprēķināta kā 125). Tomēr, 10 dienas no tagad, kad papildu pirkšanas pasūtījums par 100 gabali ir paredzams saņemt, ATP daudzums kļūst vairāk nekā 150.  

Tādēļ nosūtīšanas datums ir iestatīts uz 10 dienām no šī brīža, ATP aprēķinu pamatā. Tādējādi jūs klientu informējat, ka pieprasīto daudzumu var piegādāt 10 dienas no šī brīža.


