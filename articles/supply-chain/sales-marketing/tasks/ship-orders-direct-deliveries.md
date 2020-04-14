---
title: Pasūtījumu sūtīšana kā tiešās piegādes
description: Šajā tēmā ir parādīts, kā pārdošanas pasūtījumam izveidot tiešu piegādi.
author: omulvad
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchEditLines, PurchTableReferences, MCRDropShipWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81ebd845d9900d891b17618b3719d45060a1968f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148428"
---
# <a name="ship-orders-as-direct-deliveries"></a>Pasūtījumu sūtīšana kā tiešās piegādes

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir parādīts, kā pārdošanas pasūtījumam izveidot tiešu piegādi. Izmantojiet tiešo piegādi, ja vēlaties nosūtīt preces debitoram tieši no kreditora, nevis vispirms nosūtīt tās uz savu noliktavu. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Lai sekmīgi pabeigtu otro apakšuzdevumu "Tiešo piegāžu izveidošana, izmantojot rīku", pārliecinieties, ka krājumam, ko izvēlaties pārdošanas pasūtījumā, ir norādīts noklusējuma kreditors Izlaisto preču šablona kopsavilkuma cilnē Pirkšana.

## <a name="set-an-individual-order-for-direct-delivery"></a>Atsevišķa pasūtījuma iestatīšana tiešai piegādei
1. Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Debitora konts** un pēc tam atlasiet **Labi**
4. Ievadiet vai atlasiet vērtības laukā **Krājuma numurs** un **Vieta**, pēc tam atlasiet **Saglabāt**.
5. Darbību rūtī atlasiet **Pārdošanas pasūtījums** un pēc tam atlasiet **Tiešā piegāde**. Lapā Izveidot piegādi ir parādīts visu atvērto pārdošanas pasūtījumu rindu saraksts, kas kopētas no pārdošanas pasūtījuma. Jūs varat pārskatīt pasūtījuma informāciju, un, ja nepieciešams, pārveidot informāciju, piemēram, pirkšanas daudzumu un cenas noteikšanas nosacījumus, pirms tiešās piegādes izveidošanas.  
6. Atlasiet **Jā** laukā **Iekļaut visus**.
    - Ja vēlaties ģenerēt tiešu piegādi tikai pārdošanas pasūtījumu rindu apakškopai, atlasiet tās atsevišķi.  
    - Lauks **Kreditora konts** var būt vai var nebūt aizpildīts ar kreditora numuru. Ja precei ir iestatīts noklusējuma kreditors (saistītajās krājumu vajadzībās), šis kreditors tiks kopēts attiecīgajā rindā. Pretējā gadījumā kreditors ir jāievada manuāli. Šajā piemērā nākamajā solī tiks atlasīts jauns kreditors, pat ja lauks jau ir aizpildīts.   
7. Ievadiet vai atlasiet vērtību laukā **Kreditora konts** un pēc tam atlasiet **Labi**, Ziņojums jūs informē, ka ir izveidots pirkšanas pasūtījums.   
8. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
9. Atlasiet cilni **Piegāde** un pārbaudiet, vai lauks **Tiešā piegāde** ir iestatīts uz **Jā**.
10. Darbību rūtī atlasiet **Vispārīgi**.
11. Atlasiet **Saistītie pasūtījumi**.
12. Atlasiet saiti laukā **Pirkšanas pasūtījums**.
13. Izvērsiet sadaļu **Detalizēta informācija par rindām** atlasiet cilni **Adrese**.
    - Šīs pirkšanas pasūtījuma rindas piegādes adrese ir debitora piegādes adrese, nevis jūsu uzņēmuma adrese.  
    - Mainot piegādes adresi pārdošanas pasūtījuma rindā vai sākotnējā pārdošanas pasūtījuma rindā, adrese attiecīgajā pasūtījuma rindā tiks automātiski atjaunināta.  
14. Atlasiet cilni **Piegāde**.
    - Tāpat kā pārdošanas pasūtījuma rindai arī saistītā pirkšanas pasūtījuma rindas tips ir iestatīts kā Tiešā piegāde.  
    - Pirkšanas pasūtījuma rindas Piegādes datums un Apstiprinātais piegādes datums tiek attiecīgi iestatītas ar sākotnējā pārdošanas pasūtījuma rindu Pieprasītais saņemšanas datums un Apstiprinātais saņemšanas datums vērtības.   
    - Atjauninot jebkuru no šiem datumiem pirkšanas rindā vai pārdošanas rindā, datumi attiecīgajā pasūtījumā tiks automātiski atjaunināti.     
    - Pirkšanas pasūtījums, kas ir iestatīts preču piegādei tieši debitoram, ir saistīts ar sākotnējo pārdošanas pasūtījumu ar īpašas saistības starpniecību. Šī saistība paredz kārtulu, ka pavadzīmes atjaunināšanu pārdošanas pasūtījumam nevar veikt no pārdošanas pasūtījuma un tā jāveic, izmantojot pirkšanas pasūtījumu. Tomēr debitoru rēķinu izrakstīšana jāveic no pārdošanas pasūtījuma.  
15. Darbību rūtī atlasiet **Pirkšana**.
16. Atlasiet **Apstiprināšana**.
17. Atlasiet **Labi**.
18. Darbību rūtī atlasiet **Saņemt**.
19. Atlasiet **Preču ieejas plūsma**.
20. Laukā **Prod. ieejas pl.** ierakstiet vērtību.
21. Atlasiet **Labi**.
22. Darbību rūtī atlasiet **Vispārīgi**.
23. Atlasiet **Saistītie pasūtījumi** un iezīmējiet vēlamo ierakstu.
    - Pēc tam, kad pirkšanas pasūtījums ir atjaunināts kā saņemts, vai, citiem vārdiem, pēc tam, kad kreditors ir nosūtījis preces uz jūsu klienta adresi, sākotnējā pārdošanas pasūtījuma statuss tiek automātiski atjaunināts uz Piegādāts.  
    - Tagad pārdošanas pasūtījumu var iekļaut rēķinā.    
24. Atlasiet **Labi**.
25. Aizvērt lapu.
26. Atlasiet **Labi**. Aizveriet lapas un atgriezieties lapā sākuma lapā.

## <a name="create-direct-deliveries-from-the-workbench"></a>Tiešo piegāžu izveidošana, izmantojot rīku
1. Dodieties uz **Navigācija > Moduļi > Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Debitora konts** un pēc tam atlasiet **Labi**.
4. Laukā **Krājuma kods** un **vieta** ievadiet vai atlasiet kādu vērtību.
5. Izvērsiet sadaļu **Detalizēta informācija par rindu**, pēc tam atlasiet cilni **Piegāde**. Tā vietā, lai izveidotu tiešu piegādi pārdošanas pasūtījuma apstrādes ietvaros, kā norādīts iepriekšējā procedūrā, varat nodot šo uzdevumu iepirkumu speciālistam. Lai iekļautu pārdošanas pasūtījuma rindu tiešās piegādes apstrādes procesā, ir jāatzīmē rinda tiešajai piegādei.  
6. Atlasiet **Jā** laukā **Tiešā piegāde**.
    - Ja krājums jau ir iestatīts tiešai piegādei pēc noklusējuma, laukā tiks automātiski iestatīta opcija Jā pasūtījuma rindu ievades laikā. Krājumu var iestatīt tiešai piegādei Izlaistās preces šablonā, iestatot opcijai Tiešā piegāde vienumu Jā un atlasot noklusējuma tiešās piegādes noliktavu.  
    - Tā kā pirkšanas pasūtījums vēl nav izveidots, tiešās piegādes statuss ir iestatīts uz "Tiks veikta tiešā piegāde".   
7. Atlasiet **Saglabāt**.
8. Aizveriet lapas, kamēr atgriežaties sākuma lapā.
9. Meklēšanas joslā ievadiet `Direct delivery`.
    - Tiešās piegādes lapa darboja kā rīks, kas nodrošina pirkšanas aģentam pārskatu par visām pārdošanas pasūtījuma rindām, kam tiks veikta tieša piegāde, un tas ļauj izveidot attiecīgos pirkšanas pasūtījumus. Turklāt tie var skatīt atvērtās tiešās piegādes pasūtījumus un apstiprinātos pasūtījumus cilnēs Apstiprinājums un Piegāde.  
    - Kad esat izveidojis tiešās piegādes pasūtījumu, tas tiek automātiski pārvietots uz cilni Apstiprinājums. Varat izlemt pasūtījumu apstiprināt tieši no šīs lapas. Kad pirkums ir apstiprināts, tas tiek automātiski pārvietots uz cilni Piegāde, no kuras varat reģistrēt tā saņemšanu.  

