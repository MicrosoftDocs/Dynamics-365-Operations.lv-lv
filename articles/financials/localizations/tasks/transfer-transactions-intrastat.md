--- 
title: "Transakciju pārsūtīšana uz Intrastat"
description: "Šajā procedūrā ir izklāstīta Intrastat parametru iestatīšana un transakciju pārsūtīšana uz Intrastat."
author: Anasyash
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cc21497a6905cdb57bd687b7bff0d9dc810ba9eb
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-transactions-to-the-intrastat"></a>Transakciju pārsūtīšana uz Intrastat

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir izklāstīta Intrastat parametru iestatīšana un transakciju pārsūtīšana uz Intrastat. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.


## <a name="create-new-and-update-existing-commodity-code"></a>Izveidojiet jaunu un atjauniniet esošu preces kodu
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatījumi > Kategorijas un atribūti > Kategoriju hierarhijas.
2. Sarakstā atrodiet vai atlasiet ierakstu Intrastat preču kodi.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Koka struktūrā atlasiet “ieraksts”.
    * Piemēram, atlasiet 'Intrastat\Skaļrunis'.  
5. Noklikšķiniet uz Rediģēt.
6. Izvērsiet sadaļu Ārējā tirdzniecība.
7. Laukā Papildu vienības ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet 'gab.'.  
8. Atlasiet Jā laukā Svars netiek lietots.
9. Koka struktūrā atlasiet “Intrastat”.
10. Noklikšķiniet uz Jauns kategorijas zars.
11. Laukā Nosaukums ievadiet preces nosaukumu.
    * Piemēram, ierakstiet "Citas preces".  
12. Laukā Kods ievadiet preces kodu.
    * Piemēram, ierakstiet '995 00 00'.  
13. Laukā Draudzīgais nosaukums ierakstiet vērtību.
    * Piemēram, ierakstiet 'Cits'.  
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Piešķiriet preces kodu preces hierarhijai un izlaistai precei
1. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību “pārdošana”.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Koka struktūrā izvērsiet elementu “kategorijas līmenis”.
    * Piemēram, izvērsiet 'Pārdošanas hierarhija\Sadzīves audiosistēma'.  
4. Koka struktūrā atlasiet “kategorija, kas tiks piešķirta preces kodam”.
    * Piemēram, atlasiet 'Pārdošanas hierarhija\Sadzīves audiosistēma/Skaļruņi'.  
5. Izvērsiet sadaļu Preču kodi.
6. Noklikšķiniet uz Pievienot.
7. Laukā Atlasīt hierarhiju atlasiet “Instrastat”.
8. Sarakstā atrodiet un atlasiet preces kodu
    * Piemēram, atlasiet '920 20 34 Skaļrunis'.  
9. Noklikšķiniet uz SelectCodes.
10. Noklikšķiniet uz OK.
11. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
12. Sarakstā izvēlieties izlaisto preci, kas tiks piešķirta preces kodam.
    * Piemēram, atlasiet 'D0001'.  
13. Noklikšķiniet uz Rediģēt.
14. Izvērsiet sadaļu Ārējā tirdzniecība.
15. Laukā Prece ievadiet preces kodu
    * Piemēram, atlasiet vērtību '920 20 34 Skaļrunis'.    
16. Laukā Papildmaksas procentos ievadiet skaitli.
    * Piemēram, ievadiet '3'.  
17. Laukā Valsts/reģions ievadiet vai atlasiet izcelsmes valsti vai reģionu
    * Piemēram, atlasiet 'AUT'.  
18. Izvērsiet sadaļu Pārvaldīt krājumus.
19. Laukā Neto svars ievadiet svaru kilogramos.
    * Piemēram, ievadiet '2.5'.  
20. Noklikšķiniet uz Saglabāt.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Iestatiet Intrastat transakciju kodus un ārējās tirdzniecības parametrus
1. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Transakciju kodi
2. Noklikšķiniet uz Jauns.
3. Laukā Transakcijas kods ierakstiet vērtību.
    * Piemēram, ievadiet '21' transakcijas kodam, kas tiek izmantots kā atgriešana.  
4. Laukā Nosaukums ierakstiet transakcijas koda nosaukumu.
    * Piemēram, ievadiet 'Atgriešana'.  
5. Laukā Statistiskā summa atlasiet opciju.
    * Piemēram, atlasiet "Tukšs', kas norāda Statistisko vērtību, kas jāpārskata transakcijām ar Transakcijas kodu "21", vienmēr ir nulle.  
6. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri
7. Laukā Transakcijas kods ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet '11'.  
8. Laukā Kredīta nota ievadiet vai atlasiet kādu vērtību.
    * Šī vērtība norāda fizisko atgriešanu. Kredīta piezīmes fiziskajai atgriešanai tiks pārsūtītas Intrastat žurnālā ar pretēju virzienu. Piemēram, saņemšanas atgriešana tiek pārsūtīta kā nosūtīšana.   Pretējā gadījumā kredīta piezīme tiek uzskatīta par labojumu, un tiek pārsūtīta ar tādu pašu virzienu un pretēju zīmi. Piemēram, saņemšanas labošana tiek pārsūtīta kā saņemšana ar negatīvu summu, un aktīvais karodziņš tiek iestatīts uz "Labojums".  
9. Izvērsiet sadaļu Pārsūtīšana.
10. Atlasiet Jā laukā Krājumi ar preču kodu.
    * Atlasiet šo opciju, lai pārsūtītu tikai transakcijas ar piešķirtu preces kodu. Transakcijas bez preces koda netiks pārsūtītas uz Intrastat.  
11. Laukā Pārsūtīt, ja atbilst kritērijam atlasiet opciju.
    * Piemēram, atlasiet vienumu “Viens no atlasītajiem”.  
12. Izvērsiet sadaļu Preču kodu hierarhija.
13. Noklikšķiniet uz cilnes Valsts/reģiona rekvizīti.
14. Noklikšķiniet uz Jauns.
15. Laukā Valsts/reģions ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet vērtību “FRA”.  
16. Laukā Intrastat kods ievadiet valsts ISO kodu.
    * Piemēram, ierakstiet “FR”.  
17. Laukā Valsts/reģiona tips atlasiet "ES".
18. Noklikšķiniet uz cilnes Numuru sērijas.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Iestatiet piegādes veidus un nosacījumus izmaksu iekļaušanai Intrastat
1. Dodieties uz Pārdošana un mārketings > Iestatīšana > Sadale > Piegādes veidi
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Piemēram, atlasiet “20 Air”.  
3. Izvērsiet sadaļu Ārējā tirdzniecība.
4. Noklikšķiniet uz Rediģēt.
5. Laukā Transportēšana ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet “02”.  
6. Dodieties uz Debitoru parādi > Maksu iestatīšana > Maksas kods.
7. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Maksas kods, izmantojot vērtību "kravu pārvadāšana".
8. Izvērsiet sadaļu Ārējā tirdzniecība.
9. Noklikšķiniet uz Rediģēt.
10. Atlasiet Jā laukā Intrastat rēķina vērtība.
    * Summa tiks pārsūtīta uz lauku Rēķina izmaksas un tiks saskaitīta ar pārsūtīto summu laukā Rēķina summa.    Atlasiet Jā laukā Intrastat statistiskā vērtība, ja izmaiņu summa ir jāpārsūta uz lauku Statistiskās izmaksas un jāsaskaita ar vērtību Statistiskā summa.  

## <a name="sell-products-for-eu-customers"></a>Preču pārdošana ES debitoriem
1. Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts atlasiet ES debitoru
    * Piemēram, atlasiet “DE-012 Litware Retail”.  
4. Izvērsiet sadaļu Piegāde.
5. Laukā Piegādes veids ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet “20 Air”.  
6. Noklikšķiniet uz OK.
7. Novietojiet kursoru uz pirmās pārdošanas pasūtījuma rindas.
8. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet “D001”.  
9. Izvērsiet sadaļu Detalizēta informācija par rindu.
10. Noklikšķiniet uz cilnes Ārējā tirdzniecība.
    * Transportēšana tiek aizpildīta automātiski no izvēlētā piegādes veida.  
11. Laukā Osta ievadiet vai atlasiet kādu vērtību.
12. Noklikšķiniet uz Finanšu dati.
    * Atbilstoši iestatījumiem šī summa tiks iekļauta Intrastat rēķina vērtībā.  
13. Noklikšķiniet uz Uzturēt maksas.
14. Laukā Maksas kods ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet “KRAVAS PĀRVADĀŠANA”.  
15. Atzīmējiet izvēles rūtiņu Saglabāt.
16. Laukā Maksu vērtība ievadiet kādu skaitli.
    * Piemēram, ievadiet “10”.  
17. Noklikšķiniet uz Saglabāt.
18. Aizvērt lapu.
19. Darbību rūtī noklikšķiniet uz Rēķins.
20. Noklikšķiniet uz Rēķins.
21. Izvērsiet sadaļu Parametri.
22. Laukā Daudzums atlasiet vērtību Visi.
23. Izvērsiet sadaļu Iestatīšana.
24. Laukā Rēķina datums ievadiet datumu.
    * Piemēram, ievadiet “31.01.2015.”  
25. Noklikšķiniet uz OK.
26. Noklikšķiniet uz OK.
27. Aizvērt lapu.
28. Noklikšķiniet uz Jauns.
29. Laukā Debitora konts atlasiet ES debitoru.
    * Piemēram, atlasiet “DE-013 Trey Wholesales”  
30. Noklikšķiniet uz OK.
31. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet “D0001”.  
32. Noklikšķiniet uz Saglabāt.
33. Noklikšķiniet uz Rēķins.
34. Laukā Rēķina datums ievadiet datumu.
    * Piemēram, ievadiet datumu “31.01.2015.”  
35. Noklikšķiniet uz OK.
36. Noklikšķiniet uz OK.

## <a name="transfer-transactions-to-the-intrastat"></a>Transakciju pārsūtīšana uz Intrastat
1. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.
2. Noklikšķiniet uz Pārvest.
3. Atlasiet Jā laukā Debitora rēķins.
4. Noklikšķiniet uz Filtrēt.
5. Sarakstā atzīmējiet rindu ar datumu
6. Laukā Kritēriji ierakstiet kādu vērtību.
    * Piemēram, ievadiet perioda filtru 2015. gada janvārim (precīza vērtība ir atkarīga no datuma formāta): 1.1.2015.–31.1.2015.  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz OK.
9. Sarakstā atrodiet un atlasiet pārsūtīto ierakstu.
10. Noklikšķiniet uz cilnes Vispārīgi.
    * Pārskatiet pārsūtītos datus, tostarp saņēmēja/nosūtītāja valsti\reģionu, izcelsmes valsti, svaru, daudzumu, daudzumu papildmērvienībās, preci, transakcijas kodu, rēķinu summas un statistiskās summas.   Ja nepieciešams, datus var modificēt.  


