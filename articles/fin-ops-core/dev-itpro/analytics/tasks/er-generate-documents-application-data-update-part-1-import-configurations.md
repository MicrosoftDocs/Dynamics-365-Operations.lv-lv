---
title: Konfigurāciju importēšana, lai ģenerētu dokumentus ar programmas datiem
description: Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru "ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".
author: NickSelin
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96f636b19f9babc9a7893c12233d67fb2f044638
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751110"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Konfigurāciju importēšana, lai ģenerētu dokumentus ar programmas datiem

[!include [banner](../../includes/banner.md)]

Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru "ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".

daļa: konfigurāciju importēšana". Šajā procedūrā importēsiet nepieciešamo Excel veidni ER formāta konfigurācijās, kuras ir izveidotas parauga uzņēmumam “Litware, Inc.”, un pēc tam, izmantojot tās, ģenerēsit elektroniskos dokumentus. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot DEMF datu kopu. Pirms sākat, lejupielādējiet un saglabājiet failus, kas norādīti palīdzības tēmā “Elektronisko dokumentu ģenerēšana un pieteikumu datu atjaunināšana, izmantojot ER rīku" (generate-electronic-documents-update-application-data/). Faili ir Intrastat (model).xml, Intrastat (mapping).xml un Intrastat (format).xml.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  
    * Šīs procedūras darbību aprakstā ir paskaidrots, kā izmantot ER iespējas, lai pabeigtu izmaiņu saglabāšanu programmas datos, un kā ģenerēt Intrastat pārskatu. Detalizēta informācija par pārskatu veidošanas procesu tiek arhivēta pieteikuma tabulās. Pašlaik, kad Intrastat pārskatu veidošanas process tiek aktivizēts no Intrastat formas, arhivēšana tiek veikta, pamatojoties uz esošā pirmkodā programmētu loģiku. Šajā procedūrā jums jākonfigurē līdzīga vienkāršota pieteikumu datu loģika, izmantojot tikai ER struktūru. Pirmkodā izmaiņas netiks veiktas.   

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
    * Pārskatiet importētā datu modeļa struktūru. Ievērojiet, ka saknes vienums 'Izejošajam dokumentam' ir definēts datu plūsmas norādīšanai, lai iegūtu datus no pieteikuma un izmantotu to kā datu avotu Intrastat pārskata ģenerēšanai. Vienums 'Transakcijas (ierakstu saraksts)' tiek izmantots, lai attēlotu sarakstu ar Intrastat darbībām, par kurām jāatskaitās. Arhivējot pārskatos iekļauto preču kodus, šajā datu plūsmā ir nepieciešams atsevišķa preču koda 'Commodity rec id (Int64)' unikālais identifikators.   
9. Aizvērt lapu.
10. Noklikšķiniet uz Mainīt.
11. Noklikšķiniet uz Ielādēt no XML faila.
    * Importējiet ER kartēšanas konfigurāciju, kas norāda datu plūsmu datu iegūšanai no pieteikuma un vēlākai to izmantošanai, lai ģenerētu Intrastat pārskatu. Vēlāk jums būs jāpaplašina šī modeļa kartēšanas definīcija, lai iegūtu datus no Intrastat pārskata un izmantotu tos pieteikumu datu atjaunināšanai, lai arhivētu detalizētu informāciju par Intrastat pārskatu veidošanas procesu.   
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Intrastat (mapping).xml.  
12. Noklikšķiniet uz OK.
13. Kokā izvērsiet "Intrastat (model)".
14. Kokā atlasiet "Intrastat (model)\Intrastat (mapping)".
15. Noklikšķiniet uz Veidotājs.
    * Ievērojiet, ka pašreizējais modeļa kartējums laukā Virziens satur vērtību 'Uz modeli'. Tas nozīmē, ka šī modeļa kartējums ir izstrādāts, lai iegūtu datus no programmas un glabātu tos datu modelī.  
16. Noklikšķiniet uz Veidotājs.
17. Kokā izvērsiet "List".
18. Kokā izvērsiet "Transactions= List".
    * Pārskatiet modeļa kartējuma struktūru, kas izmanto datu modeli, kurš ir filtrēts, pamatojoties uz saknes vienumu 'Izejošajam dokumentam.' Ņemiet vērā, ka pievienotais datu avots 'List' nodrošina piekļuvi nepieciešamajiem pieteikumu datiem, kurus veido Intrastat tabulas ierakstu saraksts.  
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
    * Pārskatiet formāta struktūru, kas tiek izmantota, lai ģenerētu Intrastat pārskatu. Ņemiet vērā, ka tā ir paredzēta, lai ģenerētu XML failu, aizpildot datus no datu modeļa, kas balstīts uz saknes vienumu 'Izejošajam dokumentam'. Pārbaudiet, vai lietotāja dialoglodziņa veidlapā ir definēts ģenerētā faila nosaukums (šim mērķim tiek izmantots 'fn' datu avots).   
30. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]