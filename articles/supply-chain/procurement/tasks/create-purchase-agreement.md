--- 
title: "Pirkšanas līguma izveide"
description: "Šī procedūra palīdz izveidot pirkšanas līgumu."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 22a252d98da5415f50a1d6ffb28f57aae19b5d14
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-agreement"></a>Pirkšanas līguma izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra palīdz izveidot pirkšanas līgumu. Parasti to veic pirkšanas pārvaldnieks. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākt, jāiestata pirkšanas līgumu klasifikācijas. Kad esat izveidojis vienošanos, to var izmantot, veidojot PP, un šādi pirkšanas līguma nosacījumi tiks kopēti virsrakstā un jebkurās pasūtījuma rindās, kuras līgums ietekmē.


## <a name="create-a-new-purchase-agreement"></a>Jauna pirkšanas līguma izveide
1. Pārejiet uz sadaļu Sagāde un avoti > Pirkšanas līgumi > Pirkšanas līgumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Pirkšanas līgumu klasifikācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Izvērsiet sadaļu Vispārīgi.
10. Laukā Beigu datums ievadiet kādu datumu.
    * Beigu datums būs noklusējuma datums visām saistību rindām un noteiks, cik ilgi katra saistība ir spēkā.  
11. Laukā Dokumenta nosaukums ievadiet pirkuma līguma nosaukumu.
    * Atstājiet lauku Noklusējuma saistības iestatītu Uz preču daudzumu attiecināmas saistības (vai mainiet, ja tā nav šādi iestatīta).  
    * Noklusējuma saistību vērtība nosaka jūsu opcijas līguma rindās. Ja jums ir nepieciešams jauns saistību tips, veidojot līguma rindas, ir jāmaina noklusējuma saistības virsrakstā.  Pastāv 4 saistību tipi: Uz preču daudzumu attiecināmas saistības — attiecībā uz noteiktu preču daudzumu; Uz preču vērtību attiecināmas saistības — attiecībā uz konkrētu preces valūtas summu; Uz preces kategorijas vērtību attiecināmās saistības — attiecībā uz konkrētu valūtas summu sagādes kategorijā, kur summa var būt attiecināma uz kataloga krājumu vai krājumu, kas nav katalogā; Uz vērtību attiecināmās saistības — attiecībā uz konkrētu valūtas summu, kuru var izpildīt ar jebkuru preci vai jebkuru sagādes kategoriju.  
12. Noklikšķiniet uz OK.

## <a name="add-a-commitment"></a>Saistību pievienošana
1. Noklikšķiniet uz Pievienot rindu.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Atlasiet preci, kurai vēlaties pievienot saistības.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Daudzums ievadiet skaitli.
    * Tas ir kopējais daudzums, kuru vienojāties iegādāties no kreditora.  
7. Laukā Vienības cena ievadiet kādu skaitli.
8. Izvērsiet sadaļu Detalizēta informācija par rindu.
9. Iestatiet opciju Sasniegts maksimums uz Jā.
    * Opcija Sasniegts maksimums ierobežo saistību izmantošanu. Jūs varat iegādāties tikai līdz daudzumam, kas norādīts rindas laukā Daudzums.  
10. Sakļaujiet sadaļu Detalizēta rindas informācija.

## <a name="add-header-conditions"></a>Virsraksta nosacījumu pievienošana
1. Darbību rūtī noklikšķiniet uz Opcijas.
2. Noklikšķiniet uz Mainīt skatījumu.
3. Noklikšķiniet uz Virsraksta skatījuma.
4. Izvērsiet noteikumu sadaļu.
5. Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Maksājuma nosacījumi no kreditora konta tiek šeit rādīti pēc noklusējuma.       
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Piegādes veids noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Laukā Piegādes nosacījumi noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="confirm-and-activate-the-agreement"></a>Līguma apstiprināšana un aktivizēšana
1. Darbību rūtī noklikšķiniet uz Pirkšanas līgums.
2. Noklikšķiniet uz Apstiprinājums.
    * Iestatiet opciju Atzīmēt līgumu kā efektīvu uz Jā.  
3. Noklikšķiniet uz Labi.
4. Darbību rūtī noklikšķiniet uz Pirkšanas līgums.
5. Noklikšķiniet uz Pirkšanas līguma apstiprinājumi.
    * Opcija Priekšskatījums/Drukāt ļauj ģenerēt dokumentu pirkšanas līgumam, ko pēc tam var izdrukāt vai nosūtīt kreditoram. Ja atjaunināt līgumu vēlāk un atkārtoti to apstiprināt, abas versijas tiks parādītas šeit.  
6. Aizvērt lapu.

