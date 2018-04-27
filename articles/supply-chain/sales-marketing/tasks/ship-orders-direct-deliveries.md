--- 
title: "Pasūtījumu sūtīšana kā tiešās piegādes"
description: "Šajā procedūrā ir parādīts, kā pārdošanas pasūtījumam izveidot tiešu piegādi."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Pasūtījumu sūtīšana kā tiešās piegādes

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā pārdošanas pasūtījumam izveidot tiešu piegādi. Izmantojiet tiešo piegādi, ja vēlaties nosūtīt preces debitoram tieši no kreditora, nevis vispirms nosūtīt tās uz savu noliktavu. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Lai sekmīgi pabeigtu otro apakšuzdevumu "Tiešo piegāžu izveidošana, izmantojot rīku", pārliecinieties, ka krājumam, ko izvēlaties pārdošanas pasūtījumā, ir norādīts noklusējuma kreditors Izlaisto preču šablona kopsavilkuma cilnē Pirkšana.


## <a name="set-an-individual-order-for-direct-delivery"></a>Atsevišķa pasūtījuma iestatīšana tiešai piegādei
1. Dodieties uz Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, var atlasīt kontu US-001.  
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat atlasīt krājumu T0020.  
6. Noklikšķiniet uz Saglabāt.
7. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas pasūtījums.
8. Noklikšķiniet uz Tiešā piegāde.
    * Lapā Izveidot piegādi ir parādīts visu atvērto pārdošanas pasūtījumu rindu saraksts, kas kopētas no pārdošanas pasūtījuma. Jūs varat pārskatīt pasūtījuma informāciju, un, ja nepieciešams, pārveidot informāciju, piemēram, pirkšanas daudzumu un cenas noteikšanas nosacījumus, pirms tiešās piegādes izveidošanas.  
9. Laukā Iekļaut visus atlasiet Jā.
    * Ja vēlaties ģenerēt tiešu piegādi tikai pārdošanas pasūtījumu rindu apakškopai, atlasiet tās atsevišķi.  
    * Lauks Kreditora konts var būt vai var nebūt aizpildīts ar kreditora numuru. Ja precei ir iestatīts noklusējuma kreditors (saistītajās krājumu vajadzībās), šis kreditors tiks kopēts attiecīgajā rindā. Pretējā gadījumā kreditors ir jāievada manuāli. Šajā piemērā nākamajā solī tiks atlasīts jauns kreditors, pat ja lauks jau ir aizpildīts.   
10. Ievadiet vai atlasiet vērtību laukā kreditora konts.
    * Ja izmantojat USMF, varat atlasīt kontu 1001.  
11. Noklikšķiniet uz OK.
    * Ziņojums jūs informē, ka ir izveidots pirkšanas pasūtījums.   
12. Izvērsiet sadaļu Detalizēta informācija par rindu.
13. Noklikšķiniet uz cilnes Piegāde.
    * Laukā Tiešā piegāde tagad ir iestatīts vienums Jā.  
    * Tiešās piegādes statuss norāda izveidoto pirkšanas pasūtījumu.   
14. Darbību rūtī noklikšķiniet uz Vispārīgi.
15. Noklikšķiniet uz Saistītie pasūtījumi.
16. Noklikšķiniet, lai sekotu saitei laukā Pirkšanas pasūtījums.
17. Izvērsiet sadaļu Detalizēta informācija par rindu.
18. Noklikšķiniet uz cilnes Adrese.
    * Ņemiet vērā, ka šīs pirkšanas pasūtījuma rindas piegādes adrese ir debitora piegādes adrese, nevis jūsu uzņēmuma adrese.  
    * Mainot piegādes adresi pārdošanas pasūtījuma rindā vai sākotnējā pārdošanas pasūtījuma rindā, adrese attiecīgajā pasūtījuma rindā tiks automātiski atjaunināta.  
19. Noklikšķiniet uz cilnes Piegāde.
    * Tāpat kā pārdošanas pasūtījuma rindai arī saistītā pirkšanas pasūtījuma rindas tips ir iestatīts kā Tiešā piegāde.  
    * Pirkšanas pasūtījuma rindas vienumiem Piegādes datums un Apstiprinātais piegādes datums tiek attiecīgi iestatīti sākotnējā pārdošanas pasūtījuma rindas vienumu Pieprasītais saņemšanas datums un Apstiprinātais saņemšanas datums vērtības.   
    * Atjauninot jebkuru no šiem datumiem pirkšanas rindā vai pārdošanas rindā, datumi attiecīgajā pasūtījumā tiks automātiski atjaunināti.     
    * Pirkšanas pasūtījums, kas ir iestatīts preču piegādei tieši debitoram, ir saistīts ar sākotnējo pārdošanas pasūtījumu ar īpašas saistības starpniecību. Šī saistība paredz kārtulu, ka pavadzīmes atjaunināšanu pārdošanas pasūtījumam nevar veikt no pārdošanas pasūtījuma un tā jāveic, izmantojot pirkšanas pasūtījumu. Tomēr debitoru rēķinu izrakstīšana jāveic no pārdošanas pasūtījuma.  
20. Darbību rūtī noklikšķiniet uz Pirkt.
21. Noklikšķiniet uz Apstiprinājums.
22. Noklikšķiniet uz OK.
23. Darbību rūtī noklikšķiniet uz Saņemt.
24. Noklikšķiniet uz Produktu ieejas plūsma.
25. Laukā Produktu ieejas plūsma ierakstiet kādu vērtību.
26. Noklikšķiniet uz OK.
27. Darbību rūtī noklikšķiniet uz Vispārīgi.
28. Noklikšķiniet uz Saistītie pasūtījumi.
29. Sarakstā atzīmējiet atlasīto rindu.
    * Pēc tam, kad pirkšanas pasūtījums ir atjaunināts kā saņemts, vai, citiem vārdiem, pēc tam, kad kreditors ir nosūtījis preces uz jūsu klienta adresi, sākotnējā pārdošanas pasūtījuma statuss tiek automātiski atjaunināts uz Piegādāts.  
    * Tagad pārdošanas pasūtījumu var iekļaut rēķinā.    
30. Noklikšķiniet uz OK.
31. Aizvērt lapu.
32. Noklikšķiniet uz OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Tiešo piegāžu izveidošana, izmantojot rīku
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Dodieties uz Visi pārdošanas pasūtījumi.
4. Noklikšķiniet uz Jauns.
5. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Labi.
7. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
8. Izvērsiet sadaļu Detalizēta informācija par rindu.
9. Noklikšķiniet uz cilnes Piegāde.
    * Tā vietā, lai izveidotu tiešu piegādi pārdošanas pasūtījuma apstrādes ietvaros, kā norādīts iepriekšējā procedūrā, varat nodot šo uzdevumu iepirkumu speciālistam. Lai iekļautu pārdošanas pasūtījuma rindu tiešās piegādes apstrādes procesā, ir jāatzīmē rinda tiešajai piegādei.  
10. Laukā Tiešā piegāde atlasiet Jā.
    *   Ja krājums jau ir iestatīts tiešai piegādei pēc noklusējuma, laukā tiks automātiski iestatīta opcija Jā pasūtījuma rindu ievades laikā. Krājumu var iestatīt tiešai piegādei Izlaistās preces šablonā, iestatot opcijai Tiešā piegāde vienumu Jā un atlasot noklusējuma tiešās piegādes noliktavu.  
    * Tā kā pirkšanas pasūtījums vēl nav izveidots, tiešās piegādes statusam ir iestatīts Tiks veikta tiešā piegāde.   
11. Aizvērt lapu.
12. Aizvērt lapu.
13. Dodieties uz sadaļu Tiešā piegāde.
    * Tiešās piegādes lapa darboja kā rīks, kas nodrošina pirkšanas aģentam pārskatu par visām pārdošanas pasūtījuma rindām, kam tiks veikta tieša piegāde, un tas ļauj izveidot attiecīgos pirkšanas pasūtījumus. Turklāt tie var skatīt atvērtās tiešās piegādes pasūtījumus un apstiprinātos pasūtījumus cilnēs Apstiprinājums un Piegāde.   
14. Noklikšķiniet uz Izveidot tiešo piegādi.
15. Noklikšķiniet uz cilnes Apstiprinājums.
    * Kad esat izveidojis tiešās piegādes pasūtījumu, tas tiek automātiski pārvietots uz cilni Apstiprinājums. Varat izlemt pasūtījumu apstiprināt tieši no šīs lapas. Kad pirkums ir apstiprināts, tas tiek automātiski pārvietots uz cilni Piegāde, no kuras varat reģistrēt tā saņemšanu.  


