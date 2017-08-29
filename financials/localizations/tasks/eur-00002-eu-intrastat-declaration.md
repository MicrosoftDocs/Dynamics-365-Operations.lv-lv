--- 
title: "ES Intrastat deklarācijas ģenerēšana"
description: "Šajā procedūrā ir aprakstīti soļi, kas nepieciešami, lai eksportētu Intrastat deklarāciju elektroniskā faila formātā un priekšskatītu deklarācijas datus Excel formātā."
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bf6f564ab19347f29476f02e51a690b1a27ba454
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="generate-an-eu-intrastat-declaration"></a>ES Intrastat deklarācijas ģenerēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīti soļi, kas nepieciešami, lai eksportētu Intrastat deklarāciju elektroniskā faila formātā un priekšskatītu deklarācijas datus Excel formātā. 

Lai varētu veikt šo procedūru, ir jāveic transakciju pārsūtīšana uz Intrastat. 

Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.


## <a name="import-configurations-with-settings"></a>Importēt konfigurācijas ar iestatījumiem
1. Dodieties uz Darbvietas > Elektronisko atskaišu veidošana
2. Noklikšķiniet uz Iestatīt aktīvu.
3. Noklikšķiniet uz Repozitoriji.
4. Noklikšķiniet uz Atvērt.
5. Atveriet kolonnas Konfigurācijas nosaukums filtru.
6. Lietojiet filtru laukam “Konfigurācijas nosaukums” ar vērtību “Intrastat (DE)”, izmantojot filtra operatoru “sākas ar”.
    * Atlasiet konfigurācijas nosaukumu, kas attiecas uz jūsu juridiskās personas valsti. Šai procedūrai kā piemērs tiek izmantota Vācijas juridiskā persona (DEMF), līdz ar to ir jāizvēlas “Intrastat (DE)”.  
    * Noklikšķiniet uz Importēt un pēc tam uz Jā.  
7. Atveriet kolonnas Konfigurācijas nosaukums filtru.
8. Lietojiet filtru laukam “Konfigurācijas nosaukums” ar vērtību “Intrastat pārskats”, izmantojot filtra operatoru “sākas ar”.
    * Noklikšķiniet uz Importēt un pēc tam uz Jā.  

## <a name="set-up-foreign-trade-parameters"></a>Iestatīt ārējās tirdzniecības parametrus
1. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri
2. Izvērsiet sadaļu Elektroniskie pārskati.
3. Laukā Faila formāta kartēšana ievadiet vai atlasiet vērtību Intrastat (DE)
4. Laukā Pārskata formāta kartēšana ievadiet vai atlasiet vērtību Intrastat pārskats
5. Izvērsiet sadaļu Noapaļošanas nosacījumi.
    * Jums ir jāiestata noapaļošanas nosacījumi, kas ir spēkā jūsu valstī/reģionā Intrastat pārskatiem.  
6. Ievadiet skaitli laukā Noapaļošanas nosacījums.
    * Ievadiet noapaļošanas precizitāti, piemēram, ievadiet “0,01”.  
7. Ievadiet skaitli laukā Aiz komata esošo ciparu skaits summai.
    * Piemēram, ievadiet “2”.  
8. Atlasiet opciju laukā Noapaļošana zem 1 kg.
    * Piemēram, atlasiet “Noapaļošana uz augšu līdz 1 kg”.  
9. Ievadiet skaitli laukā Noapaļošanas nosacījums.
    * Piemēram, ievadiet “1”, lai noapaļotu svaru līdz veselam skaitlim.  
10. Izvērsiet sadaļu Minimālā robeža.
11. Laukā Svars ievadiet skaitli.
    * Piemēram, ievadiet “10” kā minimālo svaru.  
12. Laukā Summa ievadiet skaitli.
    * Piemēram, ievadiet “200” kā minimālo daudzumu.  
13. Laukā Prece ievadiet vai atlasiet kādu vērtību.

## <a name="set-up-compression-of-intrastat"></a>Iestatīt Intrastat arhivēšanu
1. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Intrastat arhivēšana.
2. Noklikšķiniet uz Noņemt.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Piemēram, sadaļā Pieejams atlasiet vienumu Prece.  
4. Noklikšķiniet uz Pievienot.

## <a name="generate-intrastat-declaration"></a>Ģenerēt Intrastat deklarāciju
1. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat
2. Noklikšķiniet uz Pārbaudīt.
    * Pārbaude tiek veikta saskaņā ar lauku Iestatījumu pārbaude lapā Ārējās tirdzniecības parametri.  
3. Noklikšķiniet uz OK.
4. Noklikšķiniet uz Atjaunināt.
5. Noklikšķiniet uz Minimālā robeža.
6. Laukā Sākuma datums ievadiet kādu datumu.
    * Piemēram, ievadiet 2015. gada 1. janvāris.  
7. Laukā Arhivēt atlasiet Jā.
8. Laukā Beigu datums ievadiet kādu datumu.
    * Piemēram, ievadiet 2015. gada 31. janvāris.  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz Atjaunināt.
11. Noklikšķiniet uz Arhivēt.
    * Šī arhivēšana tiek veikta atbilstoši tam, kā ir iestatīti Instrastat arhivēšanas iestatījumi.  
12. Laukā Sākuma datums ievadiet kādu datumu.
    * Piemēram, ievadiet 2015. gada 1. janvāris.  
13. Laukā Beigu datums ievadiet kādu datumu.
    * Piemēram, ievadiet 2015. gada 31. janvāris.  
14. Noklikšķiniet uz OK.
15. Noklikšķiniet uz Atjaunināt.
16. Noklikšķiniet uz Atjaunot sērijas numurus.
17. Noklikšķiniet uz OK.
18. Noklikšķiniet uz Izvade.
19. Noklikšķiniet uz Atskaite.
20. Laukā No datuma ievadiet pārskata perioda pirmo datumu.
    * Piemēram, iestatiet datumu “2015. gada 1. janvāris”.  
21. Laukā Līdz datumam ievadiet datumu.
    * Piemēram, ievadiet 2015. gada 31. janvāris.  
22. Laukā Ģenerēt failu atlasiet Jā.
23. Ierakstiet vērtību laukā Faila nosaukums.
24. Laukā Ģenerēt pārskatu atlasiet Jā.
25. Ierakstiet vērtību laukā Pārskata faila nosaukums.
26. Laukā Virziens atlasiet opciju.
    * Piemēram atlasiet “Izejošie krājumi”.  
27. Noklikšķiniet uz OK.


