--- 
title: "Pārdošanas pasūtījumu apstiprināšana"
description: "Šajā procedūrā parādīts, kā apstiprināt pārdošanas pasūtījumus."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="confirm-sales-orders"></a>Pārdošanas pasūtījumu apstiprināšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā apstiprināt pārdošanas pasūtījumus. Tiek parādīts, kā apstiprināt vienu pasūtījumu un kā apstiprināt vairākus pasūtījumus uzreiz. Šos uzdevumus parasti veic pārdošanas pasūtījumu apstrādātājs. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākt, pārliecinieties, ka vienam debitoram ir vairāki atvērti pārdošanas pasūtījumi. Ja izmantojat USMF, varat izmantot debitoru US-027.


## <a name="confirm-a-single-sales-order"></a>Viena pārdošanas pasūtījuma apstiprināšana
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Sarakstā atrodiet un atlasiet pasūtījumu, kuru vēlaties apstiprināt.
3. Noklikšķiniet uz saites uz pārdošanas pasūtījuma numura, lai atvērtu atlasīto pasūtījumu.
4. Darbību rūtī noklikšķiniet uz Pārdot.
5. Noklikšķiniet uz Apstiprināt pārdošanas pasūtījumu.
6. Izvērsiet vai sakļaujiet sadaļu Parametri.
    * Pārliecinieties, ka lauks Grāmatošana Jā ir aktīvs.  
7. Opcijai Drukāt apstiprinājumu iestatiet Jā.
    * Lauks Kredīta limita pārbaude norāda metodi, ko izmanto, lai aprēķinātu debitora atlikušo kredītu. Pēc noklusējuma, tā tiek kopēta no lapas Debitoru moduļa parametri. Ja vēlaties izlaist kredīta limita pārbaudi, apstiprinot specifisku pārdošanas pasūtījumu, iestatiet Kredīta limita pārbaude uz Nav. Tomēr jums jāzina ka, pat ja šis lauks ir iestatīts uz Nav, kredīta limita pārbaude tiek joprojām veikta, ja debitoru pamatdatos ir atlasīta opcija Obligātais kredīta limits.  
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Jā.
10. Aizvērt lapu.
11. Darbību rūtī noklikšķiniet uz Opcijas.
12. Noklikšķiniet uz Mainīt skatījumu.
13. Noklikšķiniet uz Virsraksta skatījuma.
    * Kad pasūtījums ir apstiprināts, Dokumenta statuss tiek iestatīts uz Apstiprinājums.  
14. Darbību rūtī noklikšķiniet uz Pārdot.
15. Noklikšķiniet uz Pārdošanas pasūtījuma apstiprinājums.
16. Aizvērt lapu.

## <a name="confirm-multiple-sales-orders-at-once"></a>Vairāku pārdošanas pasūtījumu vienlaicīga apstiprināšana
1. Dodieties uz Pārdošana un mārketings > Pārdošanas pasūtījumi > Pasūtījuma apstiprināšana > Apstiprināt pārdošanas pasūtījumu.
2. Noklikšķiniet uz Atlasīt.
3. Sarakstā cilnē Diapazons atrodiet un atlasiet ierakstu ar atsauci uz lauku Debitora konts.
4. Laukā Kritēriji noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet debitora kontu, kam ir vairāki pasūtījumi, kurus vēlaties apstiprināt masveidā.
    * Ja izmantojat USMF, var atlasīt kontu US-027.  
6. Noklikšķiniet uz OK.
    * Cilnē Pārskats tiek parādīts pasūtījumu saraksts, kas atbilst vaicājuma kritērijiem. Tie tiks iekļauti apstiprinājumā.  
    * Laukā Kopgrāmatojums tiek norādīts parametrs, pēc kura vairāki pasūtījumi jāapkopo vienā apstiprinājuma dokumentā. Pēc noklusējuma opcija tiek kopēta no iestatījuma Noklusētās vērtības kopgrāmatojumam lapā Debitoru moduļa parametri.  
7. Laukā Kopgrāmatojums atlasiet vērtību “Pasūtījums”.
    * Minimālie parametri, lai izveidotu kopgrāmatojumus, ir Rēķina konts un Valūta. Tas nozīmē, ka kopgrāmatojumi, kuriem ir citi rēķina konti un citas valūtas, nav atļauti. Papildu parametrus var iestatīt lapā Kopgrāmatošanas parametri, kas ir pieejama no lapas Kreditoru parametri.  
8. Laukā Pārdošanas pasūtījums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atlasiet pasūtījuma numuru, kuru vēlaties padarīt par koppasūtījumu.
10. Noklikšķiniet uz Sakārtot.
11. Noklikšķiniet uz OK.
12. Noklikšķiniet uz OK.


