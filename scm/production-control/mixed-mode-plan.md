---
title: "Jaukts režīms plānošana - apvienot diskrētiem, procesu un liesās plānošanas"
description: "Šajā rakstā ir sniegta informācija par jaukta režīma plānošanu. Jaukta režīma plānošanā savu piegādes ķēdi varat modelēt, pamatojoties uz materiālu plūsmu. Microsoft Dynamics 365 operācijām nodrošina audumam slīdēt seko jūsu modeļiem, neatkarīgi no piegādes politiku, kas ir atlasīts (kanbans, ražošanas pasūtījumus, pirkšanas pasūtījumus, partijas rīkojumus vai pārvietošanas pasūtījumiem)."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Jaukts režīms plānošana - apvienot diskrētiem, procesu un liesās plānošanas

Šajā rakstā ir sniegta informācija par jaukta režīma plānošanu. Jaukta režīma plānošanā savu piegādes ķēdi varat modelēt, pamatojoties uz materiālu plūsmu. Microsoft Dynamics 365 operācijām nodrošina audumam slīdēt seko jūsu modeļiem, neatkarīgi no piegādes politiku, kas ir atlasīts (kanbans, ražošanas pasūtījumus, pirkšanas pasūtījumus, partijas rīkojumus vai pārvietošanas pasūtījumiem). 

Varat atlasīt vispārējo stratēģiju preces piegādei, neatkarīgi no preces struktūras.  

Piemēram, var būt Kanban kontrole komplektācijā, kur materiāli ir ņemti komplektēšanas zonai atbilstoši ražošanas pasūtījumiem, Kanban, pārsūtīšanām, partijas pasūtījumiem, vai jebkurai kombinācijai, kas ir lietderīga piegādes ķēdes raksturlielumiem, bet jums joprojām var būt visu piegāžu pilna redzamība. Šī iespēja noved pie optimizētiem piegādes ķēdes procesiem un uzlabotas redzamības piegādes ķēdē.  

Vispārējā plānošanā izmantojamo piegādes politiku granularitāte ir atkarīga no noliktavas dimensijām, kas ir iespējotas kā vajadzības dimensijas. Lai iespējotu vispārējo plānošanu, lai kontrolētu papildināšanu un piegādes dažādu tipu novietojumos (piemēram, atdalot dažādu ražošanas vienību ražošanas stāvus vai atdalot dažādu tipu materiālu un pabeigto preču noliktavas), ieteicams iespējot vietu un noliktavu kā vajadzības dimensijas. Alternatīvi, noliktavu kā nodrošinājuma dimensiju var izlaist. Šajā gadījumā, kad izmantojat papildu noliktavas vadību, visas kustības noliktavā tiek kontrolētas ar noliktavas darbu, bet visas kustības starp noliktavām var kontrolēt ar atvilkumu Kanban.

## <a name="supply-policies"></a>Piedāvājuma politikas
Operāciju plānošanas jauktā režīmā 365 dinamika kontrolē, kā produkts ir piegādātas un, pamatojoties uz piegādes, kā atvasinātie pieprasījumi (patēriņa preces no likumprojektu materiālu \[MK\]) tiek izsniegtas. Pamatojoties uz pasūtījuma tipu, sistēma automātiski izvēlas materiālus, kas atbilst prasībām.  

Piedāvājuma politikas var noteikt preču līmenī vai jebkurā granularitātē, kas atbalsta jūsu prasības. Piedāvājuma politiku granularitāte tiek definēta lapā **Pasūtījuma noklusējuma iestatījumi**.  

Piedāvājuma politikas var kontrolēt ar preču, krājumu dimensijām (konfigurāciju, krāsu un lielumu), vietu un noliktavu. Šis iestatījums tiek veikts lapā **Krājumu vajadzība**.  

Noklusējuma pasūtījuma tips kontrolē, kādu pasūtījumu ģenerē vispārējā plānošana.  

Neatkarīgi no tā, cik piegādes ķēdē ir modelēta, Dynamics 365 operāciju atbalsta jūsu piegādes politiku sajaukums. Jums var būt ražošanas pasūtījumi, kas tiek iegūti no Kanban. Alternatīvi, jums var būt partijas pasūtījums, kam nepieciešama prece, ko piedāvā ar pārsūtīšanām vai Kanban.  

Dinamika 365 operācijām pārliecinās, vai audumam slīdēt seko modelim.  

Noliktava materiālu izdošanai tiek piešķirta dinamiski izpildes laikā, pēc piegādes politiku definēšanas.  

Parasti Kanban netiek izveidoti nākotnes datumiem, jo Kanban ir īss dzīves cikls. Lai saglabātu pilnu redzamību piegādes ķēdē, esam ieviesuši jaunu plānošanas jēdzienu "plānotais Kanban", kas tiek izmantots, lai aprēķinātu atvasinātās vajadzības, un palīdz garantēt, ka vajadzības tiek nodrošinātas, pamatojoties uz to pašu loģiku, kas tiek izmantota, veidojot faktisko Kanban.  

Tāda pati loģika pastāv visiem citiem piedāvājuma politiku tipiem. Tāpēc ilgtermiņa materiālu plānošanas pamatā ir tāda pati loģika, kura gaidāma faktisko pasūtījumu gadījumā, pēc tam, kad ražošana un piegāde ir apstiprināta.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Materiālu sadalījumu crosssupply politika – resursu patēriņu MK
Resursu patēriņš ir svarīgi funkcionalitāti. Resursu patēriņš ļauj materiālu izdošanas noliktavai būt atlasītai dinamiski, pamatojoties uz piedāvājumu politiku (pasūtījuma tipu), un arī atvieglo pamatdatu uzturēšanu.  

Resursu patēriņš pieprasa, lai noliktava, no kuras tiek izdoti materiāli, tiktu piešķirta, pamatojoties uz to, kādā veidā prece tiek piedāvāta. Citiem vārdiem sakot, izpildes laikā sistēma atrod resursus, kas ir jāizmanto ražošanā. Pamatojoties uz šiem resursiem, sistēma atrod izdošanas noliktavu.  

Darbam, kas nav atkarīgs no piedāvājuma politikas, nav jāmaina informācija par MK, ja piedāvājums mainās. Ad hoc izmaiņu dinamiku 365 operācijām pārliecinās, ka materiāli ir ņemti no labi noliktavas.

## <a name="process-manufacturing--the-production-type"></a>Ražošanas process — ražošanas veids
Pilnīgu elastību jauktā režīmā, mēs iesakām izmantot ražošanas IMS tips visiem produktiem. Pēc tam varat izmantot ražošanas pasūtījumus, kanbans, pārsūtīšanas pasūtījumi vai pirkšanas pasūtījumi jāpiegādā preces. Ražošanas procesam ir jāizmanto ražošanas veids **Formula**, **Līdzprodukts**, **Blakusprodukts** vai **Plānošanas krājums**. Šiem ražošanas veidiem nevar izmantot Kanban un ražošanas pasūtījumus.


