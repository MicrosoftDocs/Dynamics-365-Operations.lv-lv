--- 
title: "Konfigurāciju importēšana dokumentu ģenerēšanai, izmantojot lietojumprogrammas datu atjauninājumu elektronisko pārskatu veidošanai (ER)"
description: "Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7085e92b85a5003334c19598de632fcaf08da49e
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="import-configurations-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Konfigurāciju importēšana dokumentu ģenerēšanai, izmantojot lietojumprogrammas datu atjauninājumu elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.

daļa: konfigurāciju importēšana)". Šajā procedūrā importēsiet nepieciešamo Excel veidni ER formāta konfigurācijās, kuras ir izveidotas parauga uzņēmumam “Litware, Inc.”, un pēc tam, izmantojot tās, ģenerēsit elektroniskos dokumentus. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot DEMF datu kopu. Pirms sākat, lejupielādējiet un saglabājiet failus, kas norādīti palīdzības tēmā "Elektronisko dokumentu ģenerēšana un pieteikumu datu atjaunināšana, izmantojot ER rīku" (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/generate-electronic-documents-update-application-data/). Faili ir Intrastat (model).xml, Intrastat (mapping).xml un Intrastat (format).xml.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  
    * Šīs procedūras darbības norāda, kā izmantot ER iespējas, lai pabeigtu pieteikumu datu atjaunināšanu, un kā ģenerēt Intrastat pārskatu. Detalizēta informācija par pārskatu veidošanas procesu tiek arhivēta pieteikuma tabulās. Pašlaik, kad Intrastat pārskatu veidošanas process tiek aktivizēts no Intrastat formas, arhivēšana tiek veikta, pamatojoties uz esošā pirmkodā programmētu loģiku. Šajā procedūrā jums jākonfigurē līdzīga vienkāršota pieteikumu datu loģika, izmantojot tikai ER struktūru. Pirmkodā izmaiņas netiks veiktas.   

## <a name="import-er-configurations"></a>ER konfigurāciju importēšana
1. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
2. Noklikšķiniet uz Mainīt.
3. Noklikšķiniet uz Ielādēt no XML faila.
    * Importējiet ER modeļa konfigurāciju, kas satur datu modeli, kurš paredzēts lietošanai kā datu avots Intrastat pārskatu ģenerēšanai. Vēlāk jums būs jāpaplašina šī datu modeļa definīcija, lai izmantotu to pieteikumu datu atjaunināšanai, lai arhivētu detalizētu informāciju par Intrastat pārskatu veidošanas procesu.   
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Intrastat (model).xml.  
4. Noklikšķiniet uz OK.
5. Kokā atlasiet "Intrastat (model)".
6. Noklikšķiniet uz Veidotājs.
7. Kokā izvērsiet "For outgoing document".
8. Kokā izvērsiet "For outgoing document\Transactions".
    * Pārskatiet importētā datu modeļa struktūru. Ievērojiet, ka saknes vienums "For outgoing document" ir definēts datu plūsmas norādīšanai, lai iegūtu datus no pieteikuma un izmantotu to kā datu avotu Intrastat pārskata ģenerēšanai. Vienums "Transactions (Record list)" tiek izmantots, lai attēlotu sarakstu ar Intrastat darbībām, par kurām jāatskaitās. Arhivējot pārskatos iekļauto preču kodus, šajā datu plūsmā ir nepieciešams atsevišķa preču koda "Commodity rec id (Int64)" unikālais identifikators.   
9. Aizvērt lapu.
10. Noklikšķiniet uz Mainīt.
11. Noklikšķiniet uz Ielādēt no XML faila.
    * Importējiet ER kartēšanas konfigurāciju, kas norāda datu plūsmu datu iegūšanai no pieteikuma un vēlākai to izmantošanai, lai ģenerētu Intrastat pārskatu. Vēlāk jums būs jāpaplašina šī modeļa kartēšanas definīcija, lai iegūtu datus no Intrastat pārskata un izmantotu tos pieteikumu datu atjaunināšanai, lai arhivētu detalizētu informāciju par Intrastat pārskatu veidošanas procesu.   
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Intrastat (mapping).xml.  
12. Noklikšķiniet uz OK.
13. Kokā izvērsiet "Intrastat (model)".
14. Kokā atlasiet "Intrastat (model)\Intrastat (mapping)".
15. Noklikšķiniet uz Veidotājs.
    * Ievērojiet, ka pašreizējais modeļa kartējums laukā Virziens satur vērtību "To model". Tas nozīmē, ka šī modeļa kartējums ir izstrādāts, lai iegūtu datus no programmas un glabātu tos datu modelī.  
16. Noklikšķiniet uz Veidotājs.
17. Kokā izvērsiet "List".
18. Kokā izvērsiet "Transactions= List".
    * Pārskatiet modeļa kartējuma struktūru, kas izmanto datu modeli, kurš ir filtrēts, pamatojoties uz saknes vienumu "For outgoing document". Ņemiet vērā, ka pievienotais datu avots "List" nodrošina piekļuvi nepieciešamajiem pieteikumu datiem, kurus veido Intrastat tabulas ierakstu saraksts.  
19. Aizvērt lapu.
20. Aizvērt lapu.
21. Noklikšķiniet uz Mainīt.
22. Noklikšķiniet uz Ielādēt no XML faila.
    * Importējiet ER formāta konfigurāciju, kas norāda Intrastat pārskata izkārtojumu un datu aizpildīšanas procesu pārskatā. Vēlāk jums būs jāpaplašina šī formāta definīcija, lai datus no Intrastat pārskata ievietotu datu modelī un pēc tam izmantotu tos pieteikumu datu atjaunināšanai, lai arhivētu detalizētu informāciju par Intrastat pārskatu veidošanas procesu.   
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Intrastat (format).xml.  
23. Noklikšķiniet uz OK.
24. Kokā atlasiet "Intrastat (model)\Intrastat (format)".
25. Noklikšķiniet uz Veidotājs.
26. Noklikšķiniet uz Izvērst/sakļaut.
27. Kokā atlasiet "File\Declaration".
28. Noklikšķiniet uz cilnes Kartēšana.
29. Kokā atlasiet "File".
    * Pārskatiet formāta struktūru, kas tiek izmantota, lai ģenerētu Intrastat pārskatu. Ņemiet vērā, ka tā ir paredzēta, lai ģenerētu XML failu, aizpildot datus no datu modeļa, kas balstīts uz saknes vienumu "For outgoing document". Pārbaudiet, vai lietotāja dialoglodziņa veidlapā ir definēts ģenerētā faila nosaukums (šim mērķim tiek izmantots 'fn' datu avots).   
30. Aizvērt lapu.


