--- 
title: " Lojalitātes programmas shēmu definēšana"
description: "Šajā procedūrā ir aprakstīts, kā definēt lojalitātes programmas shēmu."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 1fc193e113961705f18488a4341652b3576fb275
ms.contentlocale: lv-lv
ms.lasthandoff: 11/14/2017

---

# <a name="define-loyalty-schemes"></a> Lojalitātes programmas shēmu definēšana

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā definēt lojalitātes programmas shēmu. Lojalitātes programmas shēmas ir atlīdzības peļņas un izpirkšanas kārtulas lojalitātes programmai. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Debitori > Lojalitātes programma > Lojalitātes programmas shēmas.
2. Noklikšķiniet uz Jauns.
3. Laukā Shēmas ID ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Lojalitātes programmai var būt vairākas lojalitātes programmas shēmas. Lojalitātes programmas shēmas var būt visiem kanāliem vai tikai kanālu apakšgrupai.  
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Klikšķiniet Saglabāt.
9. Noklikšķiniet uz Pievienot rindu.
10. Laukā Aktivitātes veids atlasiet opciju.
    * Atlasiet Pirkt preces pēc summas, lai debitori atlīdzības punktus saņemtu, ņemot vērā to, kādas summas viņi iztērē. Atlasiet Pirkt preces pēc daudzuma, lai debitori atlīdzības punktus saņemtu, ņemot vērā to, cik preces viņi iegādājas.  Atlasiet Pārdošanas transakciju skaits, lai debitori atlīdzības punktus saņemtu par katru pārdošanas transakciju neatkarīgi no tā, kāda prece vai tās daudzums tiek iegādāts.  
    * Atlasiet kategoriju. Kategorija ierobežos to, kurām precēm šī pelnīšanas kārtula tiek lietota.  
    * Lai pelnīšanas kārtula tiktu lietota visām precēm, atstājiet šo lauku tukšu.  
11. Laukā Aktivitātes summa/daudzums ievadiet skaitli.
    *  Darbības veidam Pārdošanas transakciju skaits vienmēr lietojiet vērtību 1.0. Darbības veidam Pirkt preces pēc summas vai Pirkt preces pēc daudzuma jebkurai transakcija, kuras summa ir mazāka par ievadīto vērtību nav, neaktivizēs atlīdzības punktu iegūšanas kārtulu. Piemēram, ja darbības veids ir Pirkt preces pēc summas un tika ievadīta vērtība 10.00, saskaņā ar atlīdzības punktu saņemšanas kārtulu pārdošanas transakcijai ar summu 9.00 netiks piešķirti atlīdzības punkti.  
12. Laukā Aktivitātes valūta ierakstiet vērtību.
13. Laukā Atlīdzības punktu ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
14. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
15. Laukā Atlīdzības punkti ievadiet skaitli.
    * Summas veida atlīdzības punktu gadījumā nopelnītās summas tiks reģistrētas kā decimāldaļas. Piemēram, ja saskaņā ar atlīdzības punktu saņemšanas kārtulu par katru 1 iztērēto Kanādas dolāru tiek iegūts 1 atlīdzības punkts un debitors iztērē 1,25 Kanādas dolārus, tad debitors nopelna 1,25 atlīdzības punktus. Daudzuma veida atlīdzības punktu gadījumā nopelnītās summas tiks reģistrētas kā vesels skaitlis. Piemēram, ja saskaņā ar atlīdzības punktu saņemšanas kārtulu par katru 1 iztērēto Kanādas dolāru tiek iegūts 1 atlīdzības punkts un debitors iztērē 1,25 Kanādas dolārus, tad debitors nopelna 1,0 atlīdzības punktus.  
16. Noklikšķiniet uz Saglabāt.
17. Noklikšķiniet uz Pievienot rindu.
    * Izpirkšanas kārtulas tiek izmantotas, ja tiek lietota lojalitātes programmas maksāšanas metode.  
18. Laukā Atlīdzības punktu ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Tiek rādīti tikai izpērkamie atlīdzības programmas punkti.  
19. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
20. Laukā Atlīdzības punkti ievadiet skaitli.
21. Laukā Izpirkšanas tips atlasiet opciju.
    * Atlasot Maksājums pēc summas, lauks Summa vai daudzums tiek apstrādāts kā valūtas vērtība. Šajā gadījumā atlīdzības programmas punktu skaits, kas tiek izmantots atkarībā no maksājuma valūtas vienības, ir fiksēts koeficients. Atlasot Maksājums pēc daudzuma, lauks Summa vai daudzums tiek apstrādāts kā daudzuma vērtība. Šajā gadījumā atlīdzības programmas punktu skaits, kas tiek izmantots atkarībā no vienības daudzuma, ir fiksēts koeficients, tomēr summa valūtā var mainīties, ja preču cena, kas samaksāta, izmantojot lojalitātes programmas atlīdzības punktus, mainās, ņemot vērā daudzumu. Lojalitātes programmas punktu atlaides izpirkšanas veids ir derīgs tad, ja konfigurācijas atslēgas opcijai Valsts/reģiona specifika ir aktivizēts Krievija, un POS funkcionalitātes profila ISO kods ir iestatīts RU.  
    * Atlasiet kategoriju. Kategorija ierobežos to, kurām precēm šī izpirkšanas kārtula tiek lietota.  
    * Lai izpirkšanas kārtula tiktu lietota visām precēm, atstājiet šo lauku tukšu.  
22. Laukā Summa vai daudzums ievadiet skaitli.
23. Laukā Valūta ierakstiet kādu vērtību.
24. Noklikšķiniet uz Saglabāt.
25. Noklikšķiniet uz Pievienot rindu.
    * Sarakstā Pieejamie organizāciju mezgli atlasiet vismaz vienu zaru un pārvietojiet to uz atlasīto organizācijas zaru sarakstu, noklikšķinot uz starp diviem sarakstiem redzamās bultiņas.  
26. Noklikšķiniet uz OK.
27. Noklikšķiniet uz Saglabāt.
    * Ikreizi, kad tiek mainīti lojalitātes programmas shēmas kanāli, ir jāizpilda darbība Procesa lojalitātes programmas shēmas. Tādā veidā kanāli saņems atjauninātas lojalitātes programmas shēmas.  


