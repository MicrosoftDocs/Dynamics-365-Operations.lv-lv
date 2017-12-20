--- 
title: "Patēriņa pieprasījuma izveide"
description: "Šajā procedūrā ir aprakstīts pieprasījuma izveides process."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7d8ca4e7eedea140f32e264c205b243027a06d03
ms.openlocfilehash: d1ea95d0bc283297fcedaee730e1829850f07998
ms.contentlocale: lv-lv
ms.lasthandoff: 11/20/2017

---
# <a name="create-a-requisition-for-consumption"></a>Patēriņa pieprasījuma izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts pieprasījuma izveides process. Tajā parādīti dažādi veidi, kā meklēt preces sagādes katalogā un kā pievienot preci, kas nav katalogā. Pirms sākt šo procedūru, jums ir jāiestata pirkšanas ierobežojumus uz Patēriņš kā pieprasījumu noklusējuma tipu. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Šo procedūru var veikt tikai no lietotāja profila, kas ir iestatīts kā darbinieks.  Šo uzdevumu parasti veic darbinieks. Darbinieka pieņemšanas darbā drošības loma ļaus veikt uzdevumus, vai, ja jūs izmantojat USMF, varat pieteikties kā Alicia.


## <a name="create-a-new-requisition"></a>Jauna pieprasījuma izveide
1. Pārejiet uz sadaļu Sagāde un avoti > Pirkuma pieprasījumi > Mani sagatavotie pirkšanas pieprasījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums dodiet pieprasījumam nosaukumu.
4. Laukā Pieprasītais datums ievadiet datumu.
    * Pēc noklusējuma, pieprasījuma datums un uzskaites datums tiek kopēti uz pirkšanas pieprasījuma rindām. Tos var mainīt rindas līmenī. Pieprasītais datums ir pieprasītais piegādes datums.  
5. Laukā Uzskaites datums ievadiet datumu.
    * Uzskaites datums tiek izmantots, lai grāmatotu uzskaites ierakstu virsgrāmatā un pārbaudītu pieejamos budžeta līdzekļus.  
6. Noklikšķiniet uz OK.
7. Laukā Pamatojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Darījuma pamatojuma iemesls, ko atlasījāt, pēc noklusējuma tiek parādīts pirkšanas pieprasījuma rindās, bet to var mainīt rindas līmenī.    
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Pamatojuma atlase
10. Detalizētas informācijas laukā ievadiet aprakstošu pieprasījuma pamatojumu

## <a name="add-a-line-to-the-requisition"></a>Rindas pievienošana pieprasījumam
1. Noklikšķiniet uz Pievienot rindu.
    * Ir divi veidi, kā pievienot rindas pirkšanas pieprasījumam. Ja jūs jau zināt preces numuru vai jau zināt, ka jūs pieprasāt preci, kas nav preču katalogā, tad varat pievienot rindu tieši ar "Pievienot rindu". Cits veids ir izmantot "Pievienot preces", kur varat izmantot meklēšanu un filtrēšanu, lai atrastu vienumus preču katalogā.    
2. Noklikšķiniet uz tikko izveidotās rindas.
    * Pieprasītājs ir darbinieks, kas ir pieprasījis šo pieprasījumu.   
    * Pēc noklusējuma persona, kas sagatavo pieprasījumu, ir darbinieks, kurš ir to pieprasījis. Jums ir jābūt atļaujai sagatavot pieprasījuma rindu cita darbinieka vārdā. Ja jums ir šādas atļaujas, tad šajā uzmeklēšanā parādīsies citi darbinieki.  
3. Laukā Krājuma kods ierakstiet kādu vērtību.
    * Krājumus, kas ir pieejami izvēlei, ierobežo kategorijas piekļuves ierobežojumi un pērkošas juridiskās personas sagādes katalogs.   
4. Laukā Daudzums ievadiet skaitli.

## <a name="add-more-products-to-the-requisition"></a>Vairāku preču pievienošana pieprasījumam
1. Noklikšķiniet uz Pievienot preces.
    * Tā ir opcija, kur var meklēt preces preču katalogā.    
2. Laukā Atrast sagādes kategorijas līmeni, ierakstiet meklējamo kategorijas nosaukuma pirmo daļu un pēc tam noklikšķiniet uz Enter.
    * Piemēram, ierakstiet comput.  
3. Izmantojiet saīsni InvokeDefaultButton.
4. Izmantojiet Filtru, lai filtrētu preču sarakstu atlasītajā kategorijā.
5. Atlasiet preces karti, ko vēlaties pievienot pieprasījumam.
6. Noklikšķiniet uz Pievienot rindām.
7. Laukā Daudzums ierakstiet kādu skaitli.
8. Laukā Atrast sagādes kategorijas līmeni, ierakstiet meklējamo kategorijas nosaukuma pirmo daļu un pēc tam noklikšķiniet uz Enter.
    * Piemēram, ierakstiet Augstas (marķieri).  
9. Izmantojiet saīsni InvokeDefaultButton.
10. Noklikšķiniet uz Pievienot rindām neuzskaitītas preces, lai pievienotu preci, kas nav norādīta sagādes katalogā.
11. Laukā Preces nosaukums ierakstiet kādu vērtību.
12. Laukā Mērvienība ierakstiet vērtību.
13. Noklikšķiniet uz Labi.
14. Laukā Krājuma apraksts pievienojiet preces aprakstu.
15. Laukā Daudzums ievadiet skaitli.
16. Laukā Vienības cena ievadiet kādu skaitli.
    * Ja jūs zināt cenu konkrētam kreditoram (kuru atlasījāt laukā Kreditora konts), tad šo cenu var ievadīt   
17. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Kreditori, kas ir pieejamai šajā laukā, ir atkarīgi no pirkšanas ierobežojumiem un statusa, kurš kreditoram ir pašreizējai kategorijai. Kā alternatīvu kreditora atlasei šeit, varat noklikšķināt uz pogas Ieteikt kreditoru.    
18. Sarakstā atlasiet kreditoru, kuru vēlaties izmantot.
19. Laukā Ārējais krājuma kods ierakstiet kādu vērtību.
    * Tas ir preces atsauces numurs, kas ir zināms kreditoram. Piemēram, tas varētu būt preces krājumu kods kreditora katalogā.  
20. Noklikšķiniet uz OK.

## <a name="distribute-amounts"></a>Sadaliet summas
1. Noklikšķiniet uz Finanšu dati.
2. Noklikšķiniet uz Sadalīt summas.
    * Šajā procesā ir parādīts, kā sadalīt pirmās rindas izmaksas starp 2 kontiem. To var izdarīt arī vēlāk, ja pieprasījums tiks pārskatīts.  
3. Noklikšķiniet uz Sadalīt, lai izveidotu sadales rindu.
4. Laukā Virsgrāmatas konts atlasiet pirmo izmaksu centru, kam jāuzņemas daļa no izmaksām.
5. Atlasiet citu sadales rindu.
6. Laukā Virsgrāmatas konts norādiet otro izmaksu centru.
7. Noklikšķiniet uz Sadalīt vienādi.
8. Aizvērt lapu.

## <a name="view-line-details"></a>Skatīt rindu detalizētu informāciju
1. Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.

## <a name="submit-the-requisition"></a>Pieprasījuma iesniegšana
1. Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.
2. Klikšķiniet Iesniegt.
3. Aizvērt lapu.
4. Laukā Komentārs ierakstiet piezīmi pieprasījuma apstiprinātājam.
5. Klikšķiniet Iesniegt.
6. Aizvērt lapu.
7. Atsvaidziniet lapu.


