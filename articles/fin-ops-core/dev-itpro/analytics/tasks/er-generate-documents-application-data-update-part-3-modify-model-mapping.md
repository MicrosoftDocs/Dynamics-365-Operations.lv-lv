---
title: Modeļu un kartējumu modificēšana, lai ģenerētu dokumentus ar programmas datiem
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu. (2. daļa – dokumentu ģenerēšana).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751610"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Modeļu un kartējumu modificēšana, lai ģenerētu dokumentus ar programmas datiem

[!include [banner](../../includes/banner.md)]

Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (2. daļa: Ģenerēt dokumentus)". 

Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus. Šajā procedūrā jūs modificēsit ER konfigurācijas, lai sāktu tās lietot elektronisku dokumentu ģenerēšanai un pieteikumu datu atjaunināšanai. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot DEMF datu kopu.


## <a name="modify-data-model"></a>Datu modeļa modificēšana
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā atlasiet "Intrastat (model)".
    * Jums būs jāpaplašina, kā izmantosiet datu modeli. Papildus tā izmantošanai kā datu avotu, lai ģenerētu Intrastat pārskatu, datu modelis tiks izmantots, lai apkopotu informāciju par Intrastat pārskatu veidošanas procesu. Pēc tam detalizēta informācija tiks izmantota, lai atjauninātu pieteikumu datus.   
3. Noklikšķiniet uz Veidotājs.
4. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Jauns zars ievadiet “Modeļa sakne”.
6. Laukā Nosaukums ierakstiet "For application data update".
    * Pieteikumu datu atjaunināšanai  
7. Noklikšķiniet uz Pievienot.
8. Kokā atlasiet "For application data update".
    * Šis jaunais saknes vienums tika pievienots, lai norādītu datu plūsmu datu pārvietošanai no Intrastat pārskata (izmantots kā datu avots) uz pieteikuma tabulām (atjaunināšanas galamērķis). Ņemiet vērā, ka datu iegūšanai, kas grāmatoti izejošā dokumentā, un datu iegūšanai no dokumenta, kas tiek izmantots pieteikumu datu atjaunināšanai, ir jāizmanto dažādi saknes vienumi.   
9. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
10. Laukā Nosaukums ierakstiet "Archive header".
    * Arhīva galvene  
11. Laukā Vienuma tips atlasiet "Record list".
12. Noklikšķiniet uz Pievienot.
    * Tā kā izveidosit ierakstu katram ģenerētajam Intrastat pārskatam, jums tam ir jāizveido jauns vienums.  
13. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
14. Laukā Nosaukums ierakstiet 'File name'.
    * Faila nosaukums  
15. Laukā Vienuma tips atlasiet "String".
16. Noklikšķiniet uz Pievienot.
17. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
18. Laukā Nosaukums ierakstiet "Number of lines".
    * Rindu skaits  
19. Laukā Vienuma tips atlasiet "Integer".
20. Noklikšķiniet uz Pievienot.
    * Pievienojiet šo vienumu, lai norādītu Intrastat darbību skaitu, kas tiek reģistrētas pašreizējā pārskata veidošanas procesā.  
21. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
22. Laukā Nosaukums ierakstiet "Archive lines".
    * Arhīva rindas  
23. Laukā Vienuma tips atlasiet "Record list".
24. Noklikšķiniet uz Pievienot.
    * Pievienojiet šo vienumu, lai norādītu sarakstu ar Intrastat darbībām, kas tiek reģistrētas pašreizējā pārskata veidošanas procesā.  
25. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
26. Laukā Nosaukums ierakstiet "Summa".
    * Summa  
27. Laukā Vienuma tips atlasiet "Real".
28. Noklikšķiniet uz Pievienot.
29. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
30. Laukā Nosaukums ierakstiet "Commodity rec id".
    * Preces ieraksta ID  
31. Laukā Krājuma veids atlasiet "Int64".
32. Noklikšķiniet uz Pievienot.
33. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
34. Laukā Nosaukums ierakstiet "Item number".
    * Krājums  
35. Laukā Vienuma tips atlasiet "String".
36. Noklikšķiniet uz Pievienot.
37. Noklikšķiniet uz Saglabāt.
38. Aizvērt lapu.

## <a name="modify-model-mapping"></a>Modeļa kartējuma modificēšana
1. Kokā izvērsiet "Intrastat (model)".
2. Kokā atlasiet "Intrastat (model)\Intrastat (mapping)".
    * Modificējiet esošu modeļa kartējumu, lai sāktu to izmantot pieteikumu datu atjaunināšanai un arhivētu Intrastat pārskata datus.  
3. Noklikšķiniet uz Veidotājs.
4. Noklikšķiniet uz Jauns.
5. Laukā Nosaukums ierakstiet "Update archive".
    * Atjaunināt arhīvu  
6. Laukā Virziens atlasiet "To destination".
7. Noklikšķiniet uz Saglabāt.
    * Šis jaunais kartējums norāda datu plūsmu datu (Intrastat pārskata dati) pārvietošanai no datu modeļa uz pieteikuma tabulām (atjaunināšanas galamērķis). Ņemiet vērā, ka, lai iegūtu datus no pieteikuma pārskatu veidošanas procesam un pēc tam izmantotu datus no datu modeļa pieteikumu datu atjaunināšanai, ir jāizmanto dažādi modeļa saknes vienumi.   
8. Noklikšķiniet uz Veidotājs.
9. Kokā atlasiet "Data model\Data model".
    * Pievienojiet nepieciešamo datu avotu. Šis ir datu modelis, kas ietver detalizētu informāciju par pārskatā iekļautajām Intrastat darbībām, kuras nepieciešams arhivēt.  
10. Noklikšķiniet uz Pievienot sakni.
11. Laukā Nosaukums ierakstiet "model".
    * modelis  
12. Laukā Definīcija ievadiet vai atlasiet vērtību 'Programmas datu atjauninājumam'.
    * Pieteikumu datu atjaunināšanai  
13. Noklikšķiniet uz Labi.
14. Koka struktūrā izvērsiet elementu “modelis”.
15. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
16. Kokā atlasiet "model\Archive header".
17. Noklikšķiniet uz Pievienot.
    * Tā kā vēlaties arhivēšanas nolūkā uzskaitīt pārskatā iekļautās Intrastat darbības, jāpievieno atbilstošs datu avots.  
18. Laukā Nosaukums ierakstiet "Enumerated lines".
    * Uzskaitījuma rindas  
19. Noklikšķiniet uz Rediģēt formulu.
20. Kokā atlasiet "List\ENUMERATE".
21. Noklikšķiniet uz Pievienot funkciju.
22. Koka struktūrā izvērsiet elementu “modelis”.
23. Kokā izvērsiet "model\Archive header".
24. Kokā atlasiet "model\Archive header\Archive lines".
25. Noklikšķiniet uz Pievienot datu avotu.
26. Laukā Formula ievadiet "ENUMERATE(model.'Archive header'.'Archive lines')".
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. Noklikšķiniet uz Saglabāt.
28. Aizvērt lapu.
29. Noklikšķiniet uz OK.
30. Noklikšķiniet uz Pievienot mērķi.
    * Pievienojiet pieteikuma tabulas kā nepieciešamos mērķus, kuriem vajadzīga atjaunināšana, lai arhivētu detalizētu informāciju par pārskatā iekļautajām Intrastat darbībām.  
31. Laukā Nosaukums ierakstiet "Archive".
    * Arhivēt  
32. Laukā Tabulas nosaukums ierakstiet "IntrastatArchiveGeneral".
    * IntrastatArchiveGeneral  
    * Saglabājiet ieraksta darbību 'Ievietot', lai varētu pievienot ierakstus katra Intrastat pārskatu veidošanas procesa detalizētas informācijas arhivēšanas laikā.  
33. Laukā Reģistrēt informācijas žurnālu atlasiet Jā.
    * Atlasiet Jā, lai iegūtu informāciju par problēmām, kas saistītas ar pieteikumu datu atjaunināšanu.  
34. Laukā Izlaist ieraksta darbības validēšanu atlasiet Jā.
    * Atlasiet Jā, lai likvidētu pārbaudes kļūdas par tukšu lauku 'Intrastat arhīva ID'. Tas tiks veikts pēc ierakstu pievienošanas, pamatojoties uz sērijas numuru iestatījumiem, kas konfigurēti šai tabulai formā Ārējās tirdzniecības parametri.  
35. Noklikšķiniet uz OK.
    * Saistiet pievienoto datu avotu (filtrētais modelis, pamatojoties uz atlasīto saknes vienumu) elementus ar elementiem no pievienotā galamērķa.  
36. Kokā izvērsiet "Archive".
37. Kokā izvērsiet "Archive\<Relations".
38. Kokā izvērsiet "Archive\<Relations\IntrastatArchiveDetail".
39. Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)".
40. Kokā izvērsiet "model\Archive header\Enumerated lines".
41. Kokā izvērsiet "model\Archive header\Enumerated lines\Value".
42. Kokā atlasiet "model\Archive header\Enumerated lines\Value\Amount".
43. Noklikšķiniet uz Saistīt.
44. Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)".
45. Kokā atlasiet "model\Archive header\Enumerated lines\Value\Commodity rec id".
46. Noklikšķiniet uz Saistīt.
47. Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)".
48. Kokā atlasiet "model\Archive header\Enumerated lines\Value\Item number".
49. Noklikšķiniet uz Saistīt.
50. Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)".
51. Kokā atlasiet "model\Archive header\Enumerated lines\Number".
52. Noklikšķiniet uz Saistīt.
53. Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail".
54. Kokā atlasiet "model\Archive header\Enumerated lines".
55. Noklikšķiniet uz Saistīt.
56. Kokā atlasiet "Archive\File name(FileName)".
57. Kokā atlasiet "model\Archive header\File name".
58. Noklikšķiniet uz Saistīt.
59. Kokā atlasiet "Archive\Number of lines(NumberOfLines)".
60. Kokā atlasiet "model\Archive header\Number of lines".
61. Noklikšķiniet uz Saistīt.
62. Kokā atlasiet "Archive".
63. Kokā atlasiet "model\Archive header".
64. Noklikšķiniet uz Saistīt.
65. Noklikšķiniet uz Saglabāt.
66. Aizvērt lapu.
67. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]