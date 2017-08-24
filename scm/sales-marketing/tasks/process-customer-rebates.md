--- 
title: "Debitora atlaižu ģenerēšana un apstrāde"
description: "Šajā procedūrā parādīts, kā apstrādāt debitora atlaides no prasību ģenerēšanas līdz brīdim, kad tās tiek nodotas kā uzkrājumi Debitoru parādos."
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
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
ms.openlocfilehash: fb5053ac5c5f9218b95d14baf4ea78f7a40479ff
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="generate-and-process-customer-rebates"></a>Debitora atlaižu ģenerēšana un apstrāde

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā apstrādāt debitora atlaides no prasību ģenerēšanas līdz brīdim, kad tās tiek nodotas kā uzkrājumi Debitoru parādos. Šeit ir izklāstīts konkrēts piemērs, kurā izskaidrots, kā dažādi nosacījumi atlaides rindās ietekmē gala summas, kas tiks kreditētas debitoram. Pirms iziet ceļvedi, jums jāizmanto USMF demonstrācijas datu uzņēmums un jāveic šādus uzdevumus. (1) Dodieties uz lapu Debitoru moduļa parametri un izvērst cilni Cenas un pēc tam cilni Detalizēta informācija par cenu un pārbaudiet, vai opcija Iespējot detalizētu informāciju par cenu ir iestatīta uz Jā. (2) Dodieties uz lapu Atlaižu līgumi un atlasiet debitora atlaides līgumu: USMF-000001. Ja lauks Darbplūsmas apstiprinājuma statuss nav iestatīts uz Apstiprināts, darbību rūtī jānoklikšķina uz Apstiprināšana, lai to apstiprinātu.


## <a name="review-a-customer-rebate-agreement"></a>Debitora atlaižu līguma pārskatīšana
1. Pārejiet uz sadaļu Pārdošana un mārketings > Debitora atlaides > Atlaižu līgumi.
    * Dažās nākamajās darbības apskatīti līguma USMF-000001 nosacījumi. Tas ļauj vieglāk saprast, kā debitora kredīta vērtības tiek aprēķinātas tālāk šajā procedūrā.  
    * Līgums paredzēts atsevišķam klientam — šajā piemērā debitoram US-009.  
    * Atlaides tiek dotas debitoram, ja tas iegādājas noteiktu preci. Šādā gadījumā preces krājuma kods ir T0020.   
    * Debitora pārdošanas apjoms, pret kuru tiek novērtētas atlaižu summas, ir jāuzkrāj katru nedēļu.  
    * Iestatījums "Cena ņemta no" ir Bruto, kas nozīmē, ka rindas atlaide nesamazina rindas pārdošanas summu, uz kuras pamata tiek novērtēta prasība.  
    * Laukā Atlaides rindas pārtraukuma tips parādīta atlaides aprēķināšanas metode. Šajā gadījumā pārdošanas mērķis, pret kuru jānovērtē atlaides, ir iestatīts uz Daudzums.   
    * Līguma rindās norādīts atlaides summas tips, faktiskā atlaides vērtība un sliekšņa vērtības. Šajā piemērā debitoram būs tiesības uz 20 USD atlaidi uz pārdoto vienību, ja tā iknedēļas preces pirkumi būs no 1 līdz 50 vienībām; un 40 USD atlaidi uz pārdoto vienību, ja iegādājas virs 50 vienībām.  
2. Aizvērt lapu.

## <a name="generate-rebate-claims"></a>Atlaižu prasību ģenerēšana
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
    * Lai imitētu atlaides prasību ģenerēšanas veidu, nākamais uzdevums ir izveidot pārdošanas pasūtījumu, kur prece un daudzums dos debitoram tiesības uz attiecīgo atlaidi.  
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
6. Daudzuma laukā iestatiet vērtību 40.
7. Noklikšķiniet uz Pārdošanas pasūtījuma rinda.
8. Noklikšķiniet uz Detalizēta informācija par cenu.
    * Ja šī opcija nav redzama, tas nozīmē, ka pirms ceļveža palaišanas opcija Iespējot detalizētu informāciju par cenu netika iestatīta uz Jā.  
9. Izvērsiet sadaļu Atlaides.
    * Cilnē Atlaides uzskaitīti atlaižu līgumi, kas attiecas uz pašreizējo pasūtījuma rindu un tiek parādīta novērtētā atlaides summa. Ņemiet vērā, ka parādītās summas ir tikai norādes par to, kādas var būt nākotnes atlaides prasības. Faktiskās atlaides summas var atšķirties atkarībā no: kopējā pārdošanas apjoma, ko debitors sasniedza saskaņā ar periodisko atlaides līgumu; vai debitors ir atgriezis visu vai daļēju daudzumu; un vai piemērojamajam pārdošanas pasūtījumam tika izrakstīts rēķins.  
10. Aizvērt lapu.
11. Noklikšķiniet uz Pievienot rindu.
12. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
13. Daudzuma laukā iestatiet vērtību 60.
14. Noklikšķiniet uz Saglabāt.
15. Darbību rūtī noklikšķiniet uz Rēķins.
16. Noklikšķiniet uz Rēķins.
17. Izvērsiet sadaļu Parametri.
18. Laukā Daudzums atlasiet vērtību Visi.
19. Noklikšķiniet uz OK.
20. Noklikšķiniet uz OK.

## <a name="process-rebate-claims"></a>Atlaižu prasību apstrāde
1. Pārejiet uz sadaļu Pārdošana un mārketings > Debitora atlaides > Atlaides.
    * Lapa Atlaides darbojas rīks, kurā var pārskatīt, apstiprināt un apstrādāt atlaides prasības. Tagad apstrādājiet prasības, kas tika izveidotas, izrakstot rēķinu pārdošanas pasūtījumam debitoram US-009, uz kuru attiecas atlaides līgums USMF-000001.   
    * Pirmā rinda attiecas uz 800 USD atlaides prasību, kas balstās uz produkta T0020 40 vienību pārdošanu un aprēķināti kā 20 USD uz vienību. Tas atbilst pirmā daudzuma pārtraukuma nosacījumiem atlaides līgumā.  
    * Otrā ir 2400 USD prasība, kas balstās produkta T0020 60 vienību pārdošanu un aprēķināta kā 40 USD uz vienību atbilstoši otrajam daudzuma pārtraukumam līgumā.  
    * Abas prasības ir stāvoklī "Jāaprēķina". Tas nozīmē, ka tās ir saistītas ar līgumu, kas periodiski izseko debitora pārdošanas apjomu un tās ir atkārtoti jāaprēķina, lai ņemtu vērā kopējo pārdošanas apjomu attiecīgajā periodā.   
2. Noklikšķiniet uz Uzkrāt.
3. Laukā Debitors ievadiet vai atlasiet kādu vērtību.
4. Laukā Sākuma datums atlasiet šodienas datumu.
5. Noklikšķiniet uz OK.
    * Funkcijas Uzkrāt lietošanas rezultātā novērtētā prasību summa tikusi koriģēta, lai ņemtu vērā faktu, ka debitora kopējais pārdošanas apjoms attiecīgajā periodā ir augstāks nekā pirmās atlaides ģenerēšanas brīdī. Precīzāk sakot, tā kā kopējais nopirktais daudzums ir sasniedzis 100 vienības, debitoram tagad ir tiesības uz 40 USD uz vienību (atbilstoši līguma otrajam daudzuma pārtraukumam) vai kopējo atlaides summu 400 USD apmērā. Starpība ir ierakstīta kā jauna prasības "korekcija" papildu 800 USD. Atlaides prasību, kas tika iekļautas funkcijā Uzkrāt atjauninājumu, statuss tagad ir iestatīts uz Aprēķināts.   
6. Sarakstā atzīmējiet visas rindas.
7. Noklikšķiniet uz Apstiprināt.
8. Noklikšķiniet uz Apstrādāt.
9. Laukā Debitors ievadiet vai atlasiet kādu vērtību.
10. Noklikšķiniet uz OK.
    * Ziņojums parāda, ka atlaide tika sekmīgi apstrādāta, un prasību statuss ir mainīts uz Atzīmēt. Tas nozīmē, ka Atlaižu uzkrājuma žurnāla grāmatošanas rezultātā: a) prasības tagad ir nodotas uz pagaidu debitora bilanci kā atskaitījumi; b) Atlaižu uzkrājuma konts tika kreditēts, kas ir nākotnes saistības pret debitoru; un c) Atlaižu izdevumu konts tika debetēts, lai atzītu izmaksas, kas radušās saistībā ar pārdošanu.   


