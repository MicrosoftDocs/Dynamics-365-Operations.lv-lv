---
title: Brīva teksta rēķina veidnes izveide
description: Šajā procedūrā ir paskaidrots, kā izveidot brīva teksta rēķina veidni.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abdcb307686800e0038212982c1eac6f1c14cf8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217486"
---
# <a name="create-a-free-text-invoice-template"></a>Brīva teksta rēķina veidnes izveide

[!include [banner](../includes/banner.md)]

Šajā apskatā izmantojiet demonstrācijas uzņēmuma “USMF” datus. Šī procedūra ir paredzēta lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.

## <a name="create-a-template"></a>Izveidot veidni

1. Pārejiet uz sadaļu Debitori > Rēķini > Periodiskie rēķini > Brīva teksta rēķina veidnes.
    * Lietojiet šo veidlapu, lai izveidotu brīva teksta rēķina veidnes, kuras var saturēt rēķina rindas, maksas, uzskaites sadales veidnes un Virsgrāmatas konta informāciju.  
2. Lai izveidotu jaunu brīva teksta rēķina veidni, noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Veidnes nosaukums.
    * Veidnes nosaukums unikāli identificē brīvā teksta rēķina veidni. Divām veidnēm nevar būt vienādi veidņu nosaukumi.  
4. Laukā Apraksts ievadiet veidnes aprakstu.
5. Izvērsiet cilni Rēķina rindas.
6. Laukā Apraksts ievadiet rēķina rindas aprakstu.
7. Laukā Galvenais konts atlasiet ieņēmumu kontu.
    * Debitoru grāmatošanas metožu lapā varat atlasīt debitora kredīta korespondējošo transakciju kontu kopējai rēķina summai.  
8. Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.  
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Laukā Krājuma nodokļu grupa atlasiet pašreizējās rēķina rindas krājuma PVN grupu.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
12. Laukā Vienības cena ievadiet vai apskatiet rēķina rindas vienas vienības cenu
    * Šī summa tiek reizināta ar vērtību laukā Daudzums, lai noteiktu rēķina rindas summu.  
13. Pievienojiet jaunu rindu brīva teksta rēķina veidnei.
14. Laukā Apraksts ievadiet rēķina rindas aprakstu.
15. Laukā Galvenais konts atlasiet ieņēmumu kontu.
    * Debitoru grāmatošanas metožu lapā varat atlasīt debitora kredīta korespondējošo transakciju kontu kopējai rēķina summai.  
16. Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.  
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Pašreizējā rēķina rindas krājuma PVN grupa.  
19. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
20. Ievadiet vai apskatiet vienību skaitu rēķina rindai.
    * Šis skaitlis tiek reizināts ar vērtību laukā Vienības cena, lai noteiktu rēķina rindas summu.  
21. Ievadiet vai apskatiet vienības cenu rēķina rindā. 
    * Šī summa tiek reizināta ar vērtību laukā Daudzums, lai noteiktu rēķina rindas summu.  
22. Apskatiet un modificējiet uzskaites sadales atsevišķai rindai un pastāvošām apakšrindām.
    * Uzskaites sadales definē, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīvā teksta rēķinā.  
23. Atjauniniet atlasītās rēķina rindas uzskaites sadales.
24. Noklikšķiniet uz Aizvērt.

## <a name="save-a-free-text-invoice-as-a-template"></a>Brīva teksta rēķina veidnes saglabāšana
Pašreizējo brīva teksta rēķinu varat saglabāt arī kā veidni. Cilnē Rēķins atlasot Saglabāt kā veidni, ievadiet veidnes nosaukumu un aprakstu. Ja veidne ar tādu nosaukumu jau pastāv, tiks parādīts paziņojums par to, ka veidne ar šādu nosaukumu jau pastāv. Jūs vienalga varat noklikšķināt uz Labi, lai to aizstātu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]