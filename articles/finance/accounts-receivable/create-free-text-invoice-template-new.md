---
title: Brīva teksta rēķina veidnes izveide
description: Šajā procedūrā ir paskaidrots, kā izveidot brīva teksta rēķina veidni.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182533"
---
# <a name="create-a-free-text-invoice-template"></a>Brīva teksta rēķina veidnes izveide

[!include [banner](../includes/banner.md)]

Šajā apskatā izmantojiet demonstrācijas uzņēmuma “USMF” datus. Šī procedūra ir paredzēta lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.

## <a name="create-a-template"></a>Izveidot veidni

1. Dodieties **uz debitoru > rēķinu > periodisko rēķinu > brīva teksta rēķinu veidnēm**.
    * Izmantojiet šo lapu, lai izveidotu brīva teksta rēķina veidnes, kas var ietvert rēķina rindas, maksas, uzskaites sadales veidni un Virsgrāmatas konta informāciju.  
2. Noklikšķiniet **uz Jauns**, lai izveidotu jaunu brīva teksta rēķina veidni.
3. Laukā **Veidnes** nosaukums ievadiet vērtību.
    * Veidnes nosaukums unikāli identificē brīvā teksta rēķina veidni. Divām veidnēm nevar būt vienādi veidņu nosaukumi.  
4. **Laukā** Apraksts ievadiet veidnes aprakstu.
5. Izvērsiet cilni **Rēķina** rindas.
6. **Laukā** Apraksts ievadiet rēķina rindas aprakstu.
7. Laukā **Galvenais** konts atlasiet ieņēmumu kontu.
    * Debitora kredīta korespondējošo darbību var atlasīt kopējā rēķina summai debitoru grāmatošanas **metožu lapā**.  
8. Laukā **PVN grupa** noklikšķiniet uz nolaižamās pogas, lai atvērtu uzmeklēšanu.
    * PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.  
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. **Laukā Krājumu PVN** grupa atlasiet krājumu PVN grupu pašreizējai rēķina rindai.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
12. Laukā **Vienības** cena ievadiet vai skatiet rēķinā rindas vienības cenu
    * Šī summa tiek reizināta ar lauku **Daudzums**, lai noteiktu rēķina rindas summu.  
13. Pievienojiet jaunu rindu brīva teksta rēķina veidnei.
14. **Laukā** Apraksts ievadiet rēķina rindas aprakstu.
15. Laukā **Galvenais** konts atlasiet ieņēmumu kontu.
    * Debitora kredīta korespondējošo darbību var atlasīt kopējā rēķina summai debitoru grāmatošanas **metožu lapā**.  
16. Laukā **PVN grupa** noklikšķiniet uz nolaižamās pogas, lai atvērtu uzmeklēšanu.
    * PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.  
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā **Krājumu PVN grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Pašreizējā rēķina rindas krājuma PVN grupa.  
19. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
20. Ievadiet vai skatiet vienību skaitu rēķina rindai.
    * Šis skaitlis tiek reizināts ar vērtību laukā Vienības cena, lai noteiktu rēķina rindas summu.  
21. Ievadiet vai apskatiet vienības cenu rēķina rindā. 
    * Šī summa tiek reizināta ar vērtību laukā **Daudzums,** lai noteiktu rēķina rindas summu.  
22. Apskatiet un modificējiet uzskaites sadales atsevišķai rindai un pastāvošām apakšrindām.
    * Uzskaites sadales definē, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīvā teksta rēķinā.  
23. Atjauniniet atlasītās rēķina rindas uzskaites sadales.
24. Noklikšķiniet uz **Aizvērt**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Brīva teksta rēķina veidnes saglabāšana
Pašreizējo brīva teksta rēķinu varat saglabāt arī kā veidni. Kad atlasāt **Saglabāt** veidnē no **cilnes** Rēķins, norādiet veidnes nosaukumu un aprakstu. Ja veidne ar tādu nosaukumu jau pastāv, tiks parādīts paziņojums par to, ka veidne ar šādu nosaukumu jau pastāv. Joprojām varat noklikšķināt uz Labi **,** lai to aizstātu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
