---
title: Formātu modificēšana, lai ģenerētu dokumentus ar programmas datiem
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e820e909bcd80b4747c06ccaaeb05c03f52b6963
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129401"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Formātu modificēšana, lai ģenerētu dokumentus ar programmas datiem

[!include [banner](../../includes/banner.md)]

Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (3. daļa — modeļa un kartējuma modificēšana)".

Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus. Šajā procedūrā jūs modificēsit ER konfigurācijas, lai ne tikai sāktu tās lietot elektronisku dokumentu ģenerēšanai, bet arī pieteikumu datu atjaunināšanai. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot DEMF datu kopu.


## <a name="modify-format-to-collect-details-of-reporting"></a>Modificējiet formātu, lai apkopotu detalizētu informāciju par pārskatu veidošanu
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā izvērsiet "Intrastat (model)".
3. Kokā atlasiet "Intrastat (model)\Intrastat (format)".
4. Noklikšķiniet uz Veidotājs.
5. Kokā izvērsiet "File".
6. Kokā izvērsiet "File\Declaration".
7. Kokā atlasiet "File\Declaration\Data".
8. Laukā Daudzkārtīgums atlasiet "One many".
    * Konfigurējiet šo formāta elementu, lai arhivētu detalizētu informāciju par Intrastat pārskatu veidošanas procesu. Šis vienums attiecas uz arhīva galvenes ierakstu.  
9. Kokā izvērsiet "File\Declaration\Data".
10. Kokā atlasiet "File\Declaration\Data\Item".
11. Laukā Daudzkārtīgums atlasiet "Zero many".
    * Konfigurējiet šo formāta elementu, lai arhivētu detalizētu informāciju par Intrastat pārskatu veidošanas procesu. Šis vienums attēlos arhivēto rindu sarakstu.  
12. Kokā izvērsiet "File\Declaration\Data\Item".
13. Kokā atlasiet "File\Declaration\Data\Item\Dim1".
14. Laukā Nav iekļauts atlasiet Jā.
    * Šie dati netiks arhivēti, tāpēc varat izslēgt šo formāta elementu no Intrastat pārskatu veidošanas informācijas datu avota.  
15. Kokā izvērsiet "File\Declaration\Data\Item\Dim1".
16. Kokā atlasiet "File\Declaration\Data\Item\Dim1\property".
17. Laukā Nav iekļauts atlasiet Jā.
18. Kokā atlasiet "File\Declaration\Data\Item\Dim1\date".
19. Laukā Nav iekļauts atlasiet Jā.
20. Kokā atlasiet "File\Declaration\Data\Item\Dim2".
21. Laukā Nav iekļauts atlasiet Jā.
22. Kokā izvērsiet "File\Declaration\Data\Item\Dim2".
23. Kokā atlasiet "File\Declaration\Data\Item\Dim2\property".
24. Laukā Nav iekļauts atlasiet Jā.
25. Kokā atlasiet "File\Declaration\Data\Item\Dim2".
26. Laukā Nav iekļauts atlasiet Jā.
27. Kokā atlasiet "File\Declaration\Data\Item\Dim3".
    * Vairākiem formāta elementiem var būt vienāds nosaukums. Piemēram, Dim. Izmantojot šo formātu kā datu avotu Intrastat pārskata datu arhivēšanai, jūs nevarat tos skaidri atpazīt, tāpēc šiem formāta elementiem jums ir jādefinē alternatīvi nosaukumi.   
28. Laukā Nosaukums ierakstiet "Summa".
    * Summa  
29. Laukā Daudzkārtīgums atlasiet "Exactly one".
30. Kokā atlasiet "File\Declaration\Data\Item\Dim4".
31. Laukā Nosaukums ierakstiet "Krājums".
    * Objekts  
32. Laukā Daudzkārtīgums atlasiet "Exactly one".
    * Papildus noformējuma formāta elementiem ir jāarhivē šādi Intrastat pārskata dati: katra reģistrētā preces krājuma unikāls ieraksta identifikators un ģenerētā faila nosaukums. Tā kā šie dati netiks aizpildīti Intrastat pārskatā, ir jāpievieno formāts, kas ir saistīts ar šiem detalizētas informācijas elementiem kā datu avota vienumiem.  
33. Kokā atlasiet "File\Declaration\Data".
34. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
35. Kokā atlasiet "Data source\Item".
36. Laukā Nosaukums ierakstiet 'File name'.
    * Faila nosaukums  
37. Laukā Datu tips atlasiet "String".
38. Noklikšķiniet uz OK.
39. Kokā atlasiet "File\Declaration\Data\Item".
40. Noklikšķiniet uz Pievienot vienumu.
41. Laukā Nosaukums ierakstiet “Commodity rec ID”.
    * Commodity rec ID  
42. Laukā Datu tips atlasiet "Int64".
43. Noklikšķiniet uz Labi.
44. Noklikšķiniet uz cilnes Kartēšana.
45. Kokā atlasiet "File\Declaration\Data\File name".
46. Noklikšķiniet uz Saistīt.
47. Koka struktūrā izvērsiet elementu “modelis”.
48. Kokā izvērsiet "model\Transactions".
49. Kokā atlasiet “File\Declaration\Data\Item = model.Transactions\Commodity rec ID”.
50. Kokā atlasiet “model\Transactions\Commodity rec ID”.
51. Noklikšķiniet uz Saistīt.
52. Klikšķiniet Saglabāt.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Modificējiet formātu, lai saglabātu atmiņā detalizētu informāciju par pārskatu veidošanu

1. Noklikšķiniet uz Kartēt formātu uz modeli.
2. Klikšķiniet Jauns.
3. Laukā Definīcija ievadiet vai atlasiet saknes vienumu 'Programmas datu atjauninājumam'.
    * Pieteikumu datu atjaunināšanai.
4. Laukā Nosaukums ierakstiet "Mapping to update data".
    * Kartēšana datu atjaunināšanai  
5. Noklikšķiniet uz Saglabāt.
    * Šis kartējums definē to, kā detalizēta informācija par Intrastat pārskatu tiek apkopota datu modelī, kura struktūru nosaka atlasītais saknes vienums 'Programmas datu atjauninājumam'. Šī detalizētā informācija, modeļa kartējums ar to pašu saknes vienumu 'Programmas datu atjauninājumam' un virziens 'Uz galamērķi' tiks izmantots pieteikumu datu atjaunināšanai. Pieteikumu datu atjaunināšana sākas tūlīt pēc tam, kad tiek ģenerēts izejošais Intrastat pārskats. Izpildes laikā pieteikumu datu atjaunināšanu var izlaist, bet datu modelim ir jābūt tukšam (ar tukšu ierakstu sarakstu).
6. Noklikšķiniet uz Veidotājs.
    * Pēc noklusējuma izejošais Intrastat pārskata formāts tiek pievienots kā datu avots šī modeļa kartēšanai.  
    * Saistiet noformētā pārskata elementus (izmantoti kā datu avots) ar datu modeļa elementiem, kas ir filtrēts, pamatojoties uz atlasīto modeļa saknes vienumu.  
7. Kokā izvērsiet "Archive header".
8. Kokā izvērsiet "Archive header\Archive lines".
9. Kokā izvērsiet "format".
10. Kokā izvērsiet "format\Declaration: XML Element(Declaration)".
11. Kokā izvērsiet "format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)".
12. Kokā izvērsiet "format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)".
13. Kokā izvērsiet "format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)".
14. Kokā izvērsiet "format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)".
15. Kokā atlasiet "Archive header\Number of lines".
16. Noklikšķiniet uz Rediģēt.
17. Kokā atlasiet “List\COUNT”.
18. Noklikšķiniet uz Pievienot funkciju.
19. Kokā izvērsiet "format".
20. Kokā izvērsiet "format\Declaration: XML Element(Declaration)".
21. Kokā izvērsiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
22. Kokā atlasiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
23. Noklikšķiniet uz Pievienot datu avotu.
24. Laukā Formula ievadiet "COUNT(format.Declaration.Data.Item)".
    * COUNT(format.Declaration.Data.Item)  
25. Noklikšķiniet uz Saglabāt.
26. Aizvērt lapu.
27. Kokā atlasiet "Archive header\File name".
28. Kokā atlasiet "format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name)".
29. Noklikšķiniet uz Saistīt.
30. Kokā atlasiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)`.
31. Kokā atlasiet "Archive header\Archive lines\Item number".
32. Noklikšķiniet uz Saistīt.
33. Kokā atlasiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)`.
34. Kokā atlasiet "Archive header\Archive lines\Amount".
35. Noklikšķiniet uz Saistīt.
36. Kokā atlasiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)`.
37. Kokā atlasiet “Archive header\Archive lines\Commodity rec ID”.
38. Noklikšķiniet uz Saistīt.
39. Kokā atlasiet "Archive header\Archive lines".
40. Kokā atlasiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
41. Noklikšķiniet uz Saistīt.
42. Kokā atlasiet "Archive header".
43. Kokā atlasiet `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
44. Noklikšķiniet uz Saistīt.
45. Klikšķiniet Saglabāt.
46. Aizvērt lapu.
47. Aizvērt lapu.
48. Aizvērt lapu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]