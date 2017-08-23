--- 
title: "izveidot pārdošanas pasūtījumus;"
description: "Šajā procedūrā ir parādīts, kā izveidot pārdošanas pasūtījumu."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 62276765e1cc76b2328a7b5b57bd18593d93e4ab
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-orders"></a>izveidot pārdošanas pasūtījumus;

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pārdošanas pasūtījumu. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Pārdošanas pasūtījumus parasti izveido pārdošanas pasūtījumu apstrādātājs. 




## <a name="enter-sales-order-header-details"></a>Ievadiet pārdošanas pasūtījuma virsraksta informāciju
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet debitora ierakstu.
    * Šim piemēram atlasiet debitora numuru US-004.  
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz OK.

## <a name="enter-sales-order-line-details"></a>Ievadīt pārdošanas pasūtījuma rindas informāciju
    * Jūsu organizācijas pārdotās preces var tikt piedāvātas dažādos variantos, kas atšķiras pēc dimensijām, piemēram, konfigurācijas, krāsas, izmēra un stila. Tāpat preces var būt iestatītas noliktavas dimensiju lietošanai, piemēram, vietām, noliktavām un paletēm, kā arī plauktu dimensiju lietošanai, piemēram, partijām un sērijas numuriem. Kad tiek piešķirtas šīm dimensijas, jums pasūtījuma rindā ir jāatlasa vērtības šīm dimensijām. Lai uzlabotu pasūtījuma izveides efektivitāti, iespējams, attiecīgo dimensiju laukus vēlaties pievienot pasūtījuma režģim.  
1. Noklikšķiniet uz Pārdošanas pasūtījuma rinda.
2. Noklikšķiniet uz Dimensijas.
    * Šajā piemērā atlasiet dimensijas Krāsa, Vieta un Noliktava. Jūsu atlasītās dimensijas būs redzamas pārdošanas pasūtījuma režģī. Ja vēlaties, lai jūsu atlases saglabātos, opcijai Saglabāt iestatījumus norādiet vērtību Jā.   
3. Noklikšķiniet uz OK.
4. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Šim piemēram atlasiet krājuma kodu T0004.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Ja krājums ir daļa no pārdošanas kategorijas, šī krājuma nosaukums automātiski tiks parādīts laukā Pārdošanas kategorija.  
    * Ja preču dimensiju laukos jau ir kāda vērtība, tas ir tāpēc, ka šī vērtība tika kopēta no preces ieraksta, kur tā bija definēta kā noklusējuma preces dimensija. Noklusējuma vērtību varat mainīt jebkurā laikā.   
7. Laukā Krāsa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Laukā Daudzums ievadiet skaitli.
    * Ja krājums tiek pārdots citās vienībās, nevis tajās, kādās tas tika nopirkts, ražots un glabāts, un ja preces ierakstā ir iestatīta pārdošanas mērvienība, šī vērtība tiks rādīta laukā Vienība. Šo vērtību varat mainīt jebkurā laikā.   
    * Ja laukā Vieta jau ir kāda vērtība, šī vērtība tika kopēta no pasūtījuma virsraksta vai no pasūtījuma iestatījumiem, kas ir saistīti ar šo preci. Šo vērtību varat mainīt jebkurā laikā. Ja šis lauks ir tukšs, atlasiet kādu vērtību.   
    * Ja laukā Vienības cena jau ir kāda vērtība, šī vērtība tika kopēta no derīga tirdzniecības līguma vai no preces ieraksta. (Vienības cenas izcelsme var būt arī pārdošanas līgums, bet procedūra pārdošanas pasūtījumu izveidošanai no pārdošanas līgumiem atšķiras no šeit parādītās.) Ja šis lauks ir tukšs, ievadiet kādu vērtību.   
    * Laukā Atlaide ir norādīta atlaides summa uz vienu preces vienību. Lai aprēķinātu kopējo rindas atlaides summu, šī atlaides vērtība tiek reizināta ar rindas daudzumu.    Ja laukā Atlaide jau ir kāda vērtība, šī vērtība tika kopēta no derīga tirdzniecības līguma. Ja šis lauks ir tukšs, bet jūs vēlaties debitoram piešķirt rindas atlaidi, ievadiet kādu vērtību.  
    * Laukā Atlaide procentos ir procentuāla vērtība, par kādu jāsamazina rindas kopējā bruto summa.  Ja laukā Atlaide procentos jau ir kāda vērtība, tā tika kopēta no derīga tirdzniecības līguma. Ja šis lauks ir tukšs, bet jūs vēlaties debitoram piešķirt rindas atlaidi, ievadiet kādu vērtību.  
    * Laukā Neto summa ir vērtība, kas tiek aprēķināta, pamatojoties uz atlaižu koriģēto rindas daudzumu un vienības cenu.  Aprēķināto vērtību varat ignorēt un pārrakstīt uz citu.  

## <a name="review-the-order-totals"></a>Pārskatīt pasūtījuma kopsummas
1. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas pasūtījums.
2. Noklikšķiniet uz Kopsummas.
    * Lapā Kopsummas tiek rādīta detalizēta informācija par visu pasūtījumu. Šī informācija ietver apakšsummas apjomu, kas ir visu rindas neto summu kopsumma, koriģēta atbilstoši beigu rindas atlaidēm, kopējā rēķina summa, kas ir apakšsummas apjoms, koriģēts atbilstoši beigu pasūtījuma līmeņa atlaidei, papildmaksas un PVN, debitora kredīta limita situācija un citas summas.  Rēķina summa ir summa, kas tiks rādīta debitora rēķina dokumentā.  
3. Noklikšķiniet uz OK.


