---
title: EUR-00011 Ģenerēt ES pārdošanas saraksta atskaiti
description: Šajā procedūrā tiek izklāstīta ES pārdošanas saraksta pārskata izveide.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce3fa3eaae48499e58228d9d6dbf7ce7e97d2bd8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821835"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a>EUR-00011 Ģenerēt ES pārdošanas saraksta atskaiti

[!include [banner](../../includes/banner.md)]

Šajā procedūrā tiek izklāstīta ES pārdošanas saraksta pārskata izveide. Tā ietver EK iekšējo tirdzniecības transakciju pārsūtīšanu uz ES pārdošanas sarakstu un pārskata izveidi. Šī procedūra ietver arī kopienas iekšējo tirdzniecības transakciju izveidošanu demonstrācijas nolūkiem. Lai iegūtu plašāku informāciju par ES pārdošanas saraksta pārskatu, tai skaitā nepieciešamajiem priekšnoteikumiem, skatiet sadaļu Palīdzība.

Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem. Šī procedūra tika izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF un tādējādi Vācijā tiek izmantota kā iekšzemes valsts/reģiona piemērs. Šajā procedūrā kā ES valsts/reģiona piemērs tiek izmantota arī Portugāle. Lai varētu veikt šo procedūru, ir jākonfigurē ES pārdošanas saraksta pārskatu veidošana.

Šī procedūra ir paredzēta grāmatvežiem.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>EK iekšējās tirdzniecības transakcijas izveide demonstrācijas nolūkiem
1. Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ierakstiet "PRT-001".
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ierakstiet D0001.
6. Izvērsiet sadaļu Detalizēta informācija par rindu.
7. Noklikšķiniet uz cilnes Iestatījumi.
8. Laukā Krājumu PVN grupa ierakstiet vērtību "PILNS".
9. Noklikšķiniet uz Pievienot rindu.
10. Laukā Krājuma kods ierakstiet D0003.
11. Laukā Krājumu PVN grupa ierakstiet vērtību "SARKANS".
12. Noklikšķiniet uz Saglabāt.
13. Darbību rūtī noklikšķiniet uz Rēķins.
14. Noklikšķiniet uz Rēķins.
15. Izvērsiet sadaļu Parametri.
16. Laukā Daudzums atlasiet vērtību Visi.
17. Izvērsiet sadaļu Iestatīšana.
18. Laukā Rēķina datums iestatiet datumu “11.01.2016.”.
19. Noklikšķiniet uz OK.
20. Noklikšķiniet uz OK.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>EK iekšējo tirdzniecības transakciju pārsūtīšana uz ES pārdošanas sarakstu
1. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > ES pārdošanas saraksts.
2. Noklikšķiniet uz Pārvest.
3. Laukā Krājums atlasiet Jā, lai pārsūtītu krājuma darbības.
4. Laukā Pakalpojums atlasiet Jā, lai pārsūtītu pakalpojum darbības.
    * Varat arī norādīt papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāpārsūta.  
5. Noklikšķiniet uz Pārvest.
    * Apstipriniet, ka EK iekšējās tirdzniecības transakcijas ir veiksmīgi pārsūtītas uz ES pārdošanas sarakstu.  

## <a name="generate-the-eu-sales-list-report"></a>Ģenerēt ES pārdošanas sarakstu pārskatu
1. Noklikšķiniet uz Atskaišu veidošana.
2. Laukā Pārskata periods atlasiet vienumu Mēneša.
3. Laukā No datuma iestatiet datumu “01.01.2016.”.
4. Laukā Ģenerēt failu atlasiet Jā.
5. Laukā Ģenerēt pārskatu atlasiet Jā.
6. Laukā Faila nosaukums ierakstiet "EUSalesList".
7. Laukā Pārskata faila nosaukums ierakstiet "EUSalesList".
8. Laukā ES pārdošanas saraksta reģistrācijas ID ierakstiet "123".
    * Šis lauks ir pieejams tikai Vācijai.  
    * Varat arī norādīt pārsūtīšanai papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāiekļauj pārskatā.  
9. Noklikšķiniet uz OK.
    * Pārliecinieties, ka tiek parādīti uznirstošie logi, lai apstiprinātu, ka tiek lejupielādēts fails un kontroles pārskats.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>ES pārdošanas saraksta rindu atzīmēšana kā iekļautas pārskatā
1. Noklikšķiniet uz Atzīmēt.
2. Noklikšķiniet uz Iezīmēt pārskatam.
3. Sarakstā atlasiet rindu laukam Rēķina datums.
4. Laukā Kritēriji ierakstiet "01.01.2016.–31.01.2016.".
5. Sarakstā atlasiet rindu laukam Pārskata statuss.
6. Laukā Kritēriji atlasiet vienumu Iekļauts.
    * Varat arī norādīt papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāatzīmē kā iekļautas pārskatā.  
7. Noklikšķiniet uz OK.
8. Laukā Atlase izvēlieties vienumu Iekļauti pārskatā.

## <a name="mark-eu-sales-list-lines-as-closed"></a>ES pārdošanas saraksta rindu atzīmēšana kā slēgtas
1. Noklikšķiniet uz Atzīmēt.
2. Noklikšķiniet uz Iezīmēt kā aizvērtu.
3. Sarakstā atzīmējiet rindu laukam Rēķina datums.
4. Laukā Kritēriji ierakstiet "01.01.2016.–31.01.2016.".
5. Sarakstā atzīmējiet rindu laukam Pārskata statuss.
6. Laukā Kritēriji atlasiet vienumu ' Iekļauti pārskatā'.
    * Varat arī norādīt papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāatzīmē kā slēgtas.  
7. Noklikšķiniet uz OK.
8. Laukā Atlase izvēlieties vienumu Slēgts.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]