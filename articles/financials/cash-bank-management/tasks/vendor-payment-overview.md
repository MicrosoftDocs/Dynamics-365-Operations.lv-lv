--- 
title: "Kreditoru maksājumu pārskats"
description: "Šis uzdevumu ceļvedis palīdzēs izprast dažādas metodes, ko izmanto, lai izveidotu kreditoru maksājumus, ieskaitot to, kā izmantot maksājuma priekšlikumu vai manuāli ievadīt vienreizēju maksājumu."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 020d147744df24b2065e66e5fc68ed5d5479127b
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="vendor-payment-overview"></a>Kreditoru maksājumu pārskats

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevumu ceļvedis palīdzēs izprast dažādas metodes, ko izmanto, lai izveidotu kreditoru maksājumus, ieskaitot to, kā izmantot maksājuma priekšlikumu vai manuāli ievadīt vienreizēju maksājumu. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.

1. Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Atlasiet maksājumu žurnālu, kurā jāsaglabā kreditoru maksājumi. 
4. Atlasiet žurnālu vai ievadiet to manuāli.
5. Noklikšķiniet uz Rindas.
6. Noklikšķiniet uz Maksājuma priekšlikums.
7. Noklikšķiniet uz Izveidot maksājuma priekšlikumu.
    * Maksājuma priekšlikums ir vaicājums, ko izmanto, lai atlasītu rēķinus apmaksai. Maksājamo rēķinu sarakstu var rediģēt pirms kreditoru maksājumu izveides vai ģenerēšanas.  
8. Atlasiet rēķinus apmaksai pēc izpildes datuma, termiņatlaides vai abus tipus. 
9. Ievadiet datumu salīdzināšanai ar izpildes datumu vai termiņatlaidi. 
10. Nav obligāti: ievadiet visiem maksājumiem izmantojamo maksājuma datumu.
    * Šeit ievadītais datums tiks uzskatīts par maksājuma datumu visiem izveidotajiem maksājumiem neatkarīgi no apmaksas datuma vai termiņatlaides datuma.  
11. Nav obligāti: ievadiet minimālo maksājuma datumu, ko var izmantot kā maksājuma datumu.
    * Agrākais maksājuma datums būs agrākais datums, ko izmanto, veidojot maksājumus. Piemēram, ja rēķina apmaksas datums ir agrākais maksājuma datums, par maksājuma datumu kļūs apmaksas datums nevis agrākais maksājuma datums, lai apmaksātu rēķinu pēdējā iespējamā datumā.  
12. Ievadiet vaicājuma papildu ierobežojumus sadaļā Iekļaujamie ieraksti.
    * Filtru bieži lieto, lai ierobežotu apmaksai atlasītos rēķinus pēc kreditoru grupas vai maksāšanas metodes. Piemēram, var pievienot filtru, lai šajā maksājumu izpildē apmaksātu rēķinus tikai ar čeku.  
13. Ievadiet vaicājuma papildu ierobežojumu vai maksājuma noklusējuma iestatījumus. 
    * Papildu parametrus var izmantot, lai definētu maksājuma valūtu vai iespējotu šai maksājumu izpildei centralizētos maksājumus.  
14. Noklikšķiniet uz OK.
    * Noklikšķinot uz Labi, parādīsies vaicājuma rezultāti. Ja nevēlaties priekšskatīt apmaksai atlasīto rēķinu sarakstu, var atgriezties uz kopsavilkuma cilni Parametri un mainīt iestatījumu Izveidot maksājumus bez rēķina priekšskatīšanas = Jā.  
15. Izvēlēties pogu Rādīt maksājuma pārskatu, lai apskatītu maksājumus, kas tiks izveidoti kreditoram saistībā ar atlasīto rēķinu.
16. Izvēlēties pogu Paslēpt maksājuma pārskatu, lai paslēptu maksājumus. 
17. Noklikšķiniet uz Izveidot maksājumus.
    * Pirms izvēlaties Izveidot maksājumus, ar peles labo pogu var noklikšķināt uz režģa un eksportēt rēķinu sarakstu uz Excel. Poga Izveidot maksājumu izveidos kreditoru maksājumus maksājumu žurnālā.  
18. Ieskenējiet savus maksājumus un pārliecinieties, vai maksāšanas metode ir norādīta visiem maksājumiem. 
    * Ja ģenerējat tādus maksājumus, kā čeka drukāšana vai elektroniskā maksājuma izveide, jānosaka maksāšanas metode. Maksāšanas tips arī noteiks noklusējuma bankas kontu, no kura tiks veikts maksājums.  
19. Noklikšķiniet uz Jauns, lai izveidotu vienreizēju maksājumu.
    * Vienreizējs maksājums var tikt pievienots maksājumu žurnālam jebkurā laikā pirms grāmatošanas. To var izdarīt, noklikšķinot uz pogas Jauns un pievienojot maksājuma informāciju manuāli, nevis pēc tam, izmantojot maksājuma priekšlikumu.  
20. Atlasiet kreditoru, kuram tiks veikts maksājums.
21. Ja pastāv rēķins apmaksai, atlasiet Transakciju nosegšana, lai atlasītu apmaksājamo rēķinu.
    * Ja tā ir priekšapmaksa, šī darbība nav obligāta. Maksājumu var izveidot, neatlasot rēķinu.  
22. Atzīmējiet visus rēķinus, kas tiks apmaksāti.
    * Ja apmaksājamo rēķinu atlasīšanai izmantojat funkciju Transakciju nosegšana, maksājuma summa tiks automātiski aprēķināta, pamatojoties uz rēķiniem, kurus atzīmējāt apmaksai, un summu, kuru ievadījāt laukā Nosedzamā summa.  
23. Noklikšķiniet uz OK.
24. Ja vēlaties dzēst maksājumu, atzīmējiet rindu.
25. Noklikšķiniet uz Dzēst.
    * Dzēšot maksājumu, tiks izdzēsts tikai konkrētais maksājums. Visi apmaksai atzīmētie rēķini joprojām būs pieejami apmaksai ar citu maksājumu.  
26. Noklikšķiniet uz Jā.
27. Izvēlieties Ģenerēt maksājumu, lai drukātu čekus vai izveidotu elektroniskā maksājuma failu.
28. Atlasiet maksājuma metodi, kuru vēlaties izveidot.
    * Maksājumu žurnāls var saturēt gan čekus, gan elektroniskos maksājumus, bet vienlaikus var izveidot tikai vienu maksājuma veidu.  
29. Atlasiet bankas kontu, no kura ģenerēt maksājumus.
30. Noklikšķiniet uz OK.
    * Maksājumi tiks izveidoti tikai maksājumiem, kas atbilst atlasītajai Maksājuma metodei un Bankas kontam.  
31. Ja ģenerējat čekus, izvēlieties Dokuments, lai nodrošinātu pareizu drukas adresātu čekiem.
32. Noklikšķiniet uz OK.
33. Noklikšķiniet uz Labi, lai izveidotu maksājumus.
34. Noklikšķiniet uz Grāmatot, ja visi maksājumi ir apstiprināti un ģenerēti. 


