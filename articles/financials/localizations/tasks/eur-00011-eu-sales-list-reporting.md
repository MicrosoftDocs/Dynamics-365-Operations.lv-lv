---
title: EUR-00011 Iestatīt ES pārdošanas saraksta atskaišu veidošanu
description: Šajā uzdevumā tiek sniegts pārskats par priekšnosacījumiem, kas nepieciešami ES pārdošanas saraksta pārskatam.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aef1d19aabb7937fcd961a9657b8ca65c064b0b1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "371264"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a>EUR-00011 Iestatīt ES pārdošanas saraksta atskaišu veidošanu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumā tiek sniegts pārskats par priekšnosacījumiem, kas nepieciešami ES pārdošanas saraksta pārskatam. Lai iegūtu plašāku informāciju par ES pārdošanas saraksta pārskatu, tai skaitā nepieciešamajiem priekšnoteikumiem, skatiet Dynamics 365 for Finance and Operations palīdzību.

Šis uzdevums attiecas uz visām Eiropas valstīm/reģioniem. Šis ceļvedis tika izveidots, izmantojot demonstrācijas datu uzņēmumu DEMF un tādējādi Vācijā tiek izmantota kā iekšzemes valsts/reģiona piemērs. Šajā ceļvedī kā iekšzemes valsts/reģiona piemērs tiek izmantota arī Portugāle.

Šie uzdevumi ir paredzēti sistēmas administratoriem.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Elektroniskā pārskata konfigurāciju importēšana ES pārdošanas saraksta pārskatos
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Iestatīt aktīvu.
3. Noklikšķiniet uz Repozitoriji.
4. Noklikšķiniet uz Atvērt.
5. Darbību rūtī noklikšķiniet uz Opcijas.
6. Noklikšķiniet uz Detalizēts filtrs/kārtošana.
7. Noklikšķiniet uz Pievienot.
8. Laukā Lauks atlasiet "Konfigurācijas nosaukums".
9. Laukā Kritēriji ierakstiet "ES pārdošanas saraksts (DE)".
10. Noklikšķiniet uz OK.
11. Noklikšķiniet uz Importēt.
12. Noklikšķiniet uz Jā.
13. Darbību rūtī noklikšķiniet uz Opcijas.
14. Noklikšķiniet uz Detalizēts filtrs/kārtošana.
15. Noklikšķiniet uz Atiestatīt.
16. Noklikšķiniet uz Pievienot.
17. Laukā Lauks atlasiet "Konfigurācijas nosaukums".
18. Laukā Kritēriji ierakstiet "Pārskats par ES pārdošanas sarakstu pa rindām".
19. Noklikšķiniet uz OK.
20. Noklikšķiniet uz Importēt.
21. Noklikšķiniet uz Jā.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>PVN kodu iestatīšana ES pārdošanas saraksta pārskatiem
1. Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN kodi.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka PVN kods, izmantojot vērtību “VAT19”.
3. Izvērsiet sadaļu Pārskata iestatījumi.
    * Pārbaudiet, vai opcija Nav iekļauts ir iestatīta uz Nē.  
    * Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu šo iestatījumu.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>PVN grupu iestatīšana ES pārdošanas saraksta pārskatiem
1. Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Pārdošanas nodokļa grupas.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka PVN grupa, izmantojot vērtību “AR-DOM”.
3. Noklikšķiniet uz Rediģēt.
4. Izvērsiet sadaļu Iestatīšana.
5. Sarakstā atlasiet pirmo rindu.
6. Atzīmējiet izvēles rūtiņu Neapliekams.
7. Sarakstā atlasiet otro rindu.
8. Atzīmējiet izvēles rūtiņu Neapliekams.
9. Sarakstā atlasiet trešo rindu.
10. Atzīmējiet izvēles rūtiņu Neapliekams.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Krājumu PVN grupu iestatīšana ES pārdošanas saraksta pārskatiem
1. Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Krājumu pārdošanas nodokļa grupas.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka Krājuma PVN grupa, izmantojot vērtību “PILNS”.
    * Pārbaudiet, vai opcija Pārskata veids ir iestatīta uz "Krājums".  
    * Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu vērtību šajā laukā.  
3. Izmantojiet ātro filtru, lai filtrētu pēc lauka Krājuma PVN grupa, izmantojot vērtību “SARKANS”.
    * Pārbaudiet, vai opcija Pārskata veids ir iestatīta uz "Pakalpojums".  
    * Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu vērtību šajā laukā.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Valsts/reģiona parametru iestatīšana ES pārdošanas saraksta pārskatiem
1. Dodieties uz Nodokļi > Iestatīšana > Pārdošanas nodoklis > Valsts/reģiona parametri.
2. Noklikšķiniet uz Jauns.
3. Laukā Valsts/reģions ierakstiet "PRT".
4. Laukā PVN ierakstiet "PT".

## <a name="create-tax-exempt-numbers"></a>PVN reģistrācijas numuru izveide
1. Dodieties uz Nodokļi > Iestatīšana > Pārdošanas nodoklis > PVN reģ. numuri.
2. Noklikšķiniet uz Jauns.
3. Laukā Valsts/reģions ierakstiet "PRT".
4. Laukā PVN reģ. numurs ierakstiet “PT12345”.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>ES pārdošanas saraksta pārskatu parametru iestatīšana
1. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.
2. Noklikšķiniet uz cilnes ES pārdošanas saraksts.
3. Atlasiet Jā laukā Pārsūtīšanas pirkumi.
4. Izvērsiet sadaļu Noapaļošanas nosacījumi.
5. Iestatiet Noapaļošanas nosacījumu uz "0,1".
6. Laukā Lietot minimālo vērtību atlasiet Jā.
7. Laukā Decimālciparu skaits ievadiet "2".
8. Izvērsiet sadaļu Elektroniskie pārskati.
9. Laukā Faila formāta kartēšana atlasiet "ES pārdošanas saraksts (DE)".
10. Laukā Pārskata formāta kartēšana atlasiet "Pārskats par ES pārdošanas sarakstu pa rindām".
11. Noklikšķiniet uz cilnes Valsts/reģiona rekvizīti.
    * Pārbaudiet, vai lauks Valsts/reģiona tips valstij/reģionam DEU ir iestatīts uz "Iekšzemes".  
    * Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu vērtību šajā laukā.  
12. Noklikšķiniet uz Jauns.
13. Laukā Valsts/reģions ierakstiet "PRT".
14. Laukā Intrastat kods ierakstiet "PT".
15. Laukā Valsts/reģiona tips atlasiet "ES".
16. Noklikšķiniet uz cilnes Numuru sērijas.
    * Pārbaudiet, vai Atsaucei "ES pārdošanas saraksts" ir norādīts Numuru sērijas kods.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Debitora izveide ES pārdošanas saraksta pārskatu demonstrācijas nolūkiem
1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ierakstiet "PRT-001".
4. Laukā Nosaukums ierakstiet "Debitors no Portugāles".
5. Laukā Debitoru grupa atlasiet "10".
6. Laukā PVN grupa atlasiet "AR-DOM".
7. Laukā PVN reģ. numurs atlasiet “PT12345”.
8. Laukā Valsts/reģions ierakstiet "PRT".
9. Noklikšķiniet uz Saglabāt.

