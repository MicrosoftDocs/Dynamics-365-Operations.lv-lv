---
title: Pārdošanas pasūtījumu apstiprināšana
description: Šajā procedūrā parādīts, kā apstiprināt pārdošanas pasūtījumus.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6476271689feaaa00e44f98f17ac34976c46644
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432586"
---
# <a name="confirm-sales-orders"></a>Pārdošanas pasūtījumu apstiprināšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā apstiprināt pārdošanas pasūtījumus. Tiek parādīts, kā apstiprināt vienu pasūtījumu un kā apstiprināt vairākus pasūtījumus uzreiz. Šos uzdevumus parasti veic pārdošanas pasūtījumu apstrādātājs. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākt, pārliecinieties, ka vienam debitoram ir vairāki atvērti pārdošanas pasūtījumi. Ja izmantojat USMF, varat izmantot debitoru US-027.


## <a name="confirm-a-single-sales-order"></a>Viena pārdošanas pasūtījuma apstiprināšana
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Sarakstā atrodiet un atlasiet pasūtījumu, kuru vēlaties apstiprināt.
3. Noklikšķiniet uz saites uz pārdošanas pasūtījuma numura, lai atvērtu atlasīto pasūtījumu.
4. **Darbību rūtī** noklikšķiniet uz **Pārdot**.
5. Noklikšķiniet uz **Apstiprināt pārdošanas pasūtījumu**.
6. Izvērsiet sadaļu **Parametri**. Pārliecinieties, vai opcija **Grāmatošana** ir iestatīta uz 'Jā'.  
7. Opcijai **Drukāt apstiprinājumu** uz 'Jā'. Lauks **Kredīta limita pārbaude** norāda metodi, ko izmanto, lai aprēķinātu debitora atlikušo kredītu. Pēc noklusējuma, tā tiek kopēta no lapas Debitoru moduļa parametri. Ja vēlaties izlaist kredīta limita pārbaudi, apstiprinot specifisku pārdošanas pasūtījumu, iestatiet **Kredīta limita pārbaude** uz 'Nav'. Tomēr jums jāzina ka, pat ja šis lauks ir iestatīts uz 'Nav', kredīta limita pārbaude tiek joprojām veikta, ja debitoru pamatdatos ir atlasīta opcija **Obligātais kredīta limits**. 
8. Noklikšķiniet uz **Labi**.
9. Noklikšķiniet uz pogas **Jā**.
10. Aizvērt lapu.
11. **Darbību rūtī** noklikšķiniet uz **Opcijas**.
12. Noklikšķiniet uz **Mainīt skatu**.
13. Noklikšķiniet uz **Virsraksta skats**. Kad pasūtījums ir apstiprināts, **Dokumenta statuss** tiek iestatīts uz 'Apstiprinājums'. 
14. **Darbību rūtī** noklikšķiniet uz **Pārdot**.
15. Noklikšķiniet uz **Pārdošanas pasūtījuma apstiprinājums**.
16. Aizvērt lapu.

## <a name="confirm-multiple-sales-orders-at-once"></a>Vairāku pārdošanas pasūtījumu vienlaicīga apstiprināšana
1. Dodieties uz **Pārdošana un mārketings > Pārdošanas pasūtījumi > Pasūtījuma apstiprināšana > Apstiprināt pārdošanas pasūtījumu**.
2. Noklikšķiniet uz **Atlasīt**.
3. Sarakstā cilnē **Diapazons** atrodiet un atlasiet ierakstu ar atsauci uz lauku **Debitora konts**.
4. Laukā **Kritēriji** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet debitora kontu, kam ir vairāki pasūtījumi, kurus vēlaties apstiprināt masveidā. Ja izmantojat USMF, var atlasīt kontu US-027.  
6. Noklikšķiniet uz **Labi**.
    - Cilnē **Pārskats** tiek parādīts pasūtījumu saraksts, kas atbilst vaicājuma kritērijiem. Tie tiks iekļauti apstiprinājumā.  
    - Laukā **Kopgrāmatojums** sadaļā **Parametri** tiek norādīts parametrs, pēc kura vairāki pasūtījumi jāapkopo vienā apstiprinājuma dokumentā. Pēc noklusējuma opcija tiek kopēta no iestatījuma N **oklusētās vērtības kopgrāmatojumam** lapā **Debitoru moduļa parametri**.  
7. Laukā **Kopgrāmatojums** atlasiet vērtību “Pasūtījums”. Minimālie parametri, lai izveidotu kopgrāmatojumus, ir **Rēķina konts** un **Valūta**. Tas nozīmē, ka kopgrāmatojumi, kuriem ir citi rēķina konti un citas valūtas, nav atļauti. Papildu parametrus var iestatīt lapā **Kopgrāmatošanas parametri**, kas ir pieejama no lapas **Debitoru moduļa parametri**. 
8. Laukā **Pārdošanas pasūtījums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atlasiet pasūtījuma numuru, kuru vēlaties padarīt par koppasūtījumu.
10. Noklikšķiniet uz **Sakārtot**.
11. Noklikšķiniet uz **Labi**.
12. Noklikšķiniet uz **Labi**.

