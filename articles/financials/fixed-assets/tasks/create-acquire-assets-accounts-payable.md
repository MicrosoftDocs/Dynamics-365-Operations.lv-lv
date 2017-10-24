--- 
title: "Līdzekļu izveide un iegūšana modulī Kreditori"
description: "Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9149378047fc22efbd401b7af86df07c1403e4f5
ms.openlocfilehash: cfe920b2ef493ab3ae36a9557001086ed99c3e4e
ms.contentlocale: lv-lv
ms.lasthandoff: 10/05/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Līdzekļu izveide un iegūšana modulī Kreditori

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu. Tas izmanto grāmatveža un kreditoriem maksājamo rēķinu darbinieka lomas, kā arī demonstrācijas uzņēmumu USMF.


## <a name="set-fixed-assets-parameters"></a>Pamatlīdzekļu parametru iestatīšana
1. Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.
2. Izvērsiet vai sakļaujiet sadaļu Pirkšanas pasūtījumi.
3. Atzīmējiet izvēles rūtiņu Atļaut līdzekļu iegādi no Pirkšanas.
4. Atzīmējiet izvēles rūtiņu Izveidot līdzekli produktu ieejas plūsmas vai rēķina grāmatošanas laikā.

## <a name="create-a-new-vendor-invoice"></a>Jauna kreditora rēķina izveide
1. Pārejiet uz sadaļu Kreditori > Darbvietas > Kreditora rēķina ieraksts.
2. Noklikšķiniet uz Jauns kreditora rēķins.
3. Laukā Rēķina konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Numurs ierakstiet kādu vērtību.
6. Ievadiet datumu laukā Grāmatošanas datums.
7. Noklikšķiniet uz Pievienot rindu.
8. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Pamatlīdzekļu iegādei var tikt izmantoti vai nu noliktavā neesoši krājumi vai sagādes kategorijas.  
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Laukā Daudzums ievadiet skaitli.
    * Viena rēķina rinda izveidos tikai vienu pamatlīdzekli neatkarīgi no daudzuma.  Rēķina daudzuma lauka vērtība tiks pārnesta uz pamatlīdzekļa daudzumu.  
11. Laukā Vienības cena ievadiet kādu skaitli.
12. Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.
13. Noklikšķiniet uz cilnes Pamatlīdzekļi.
14. Atzīmējiet izvēles rūtiņu Izveidot jaunu pamatlīdzekli..
15. Laukā Pamatlīdzekļa grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
16. Sarakstā atlasiet pamatlīdzekļu grupu, kura tiks izmantota jauna pamatlīdzekļa izveidei.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Noklikšķiniet uz Grāmatot.
    * Pamatlīdzeklis tiks izveidots un iegūts, iegrāmatojot rēķinu.  


