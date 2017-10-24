--- 
title: "Pārskatīt konfigurācijas, lai veidotu pārskatus Microsoft Office formātos ar iegultiem attēliem elektronisko pārskatu veidošanai (ER)"
description: "Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī “ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (1. daļa: iestatīt parametrus)”."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dcc162a4c0ba81079eefb7564ab037c1287acd92
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a>Pārskatīt konfigurācijas, lai veidotu pārskatus Microsoft Office formātos ar iegultiem attēliem elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī “ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (1. daļa: iestatīt parametrus)”.

Šajā procedūrā parādīts, kā veidot elektronisko pārskatu (ER) konfigurācijas, lai programmā Microsoft Excel un Microsoft Word ģenerētu elektroniskos dokumentus, kas satur iegultos attēlus. Šajā piemērā jūs pārskatīsit parauga uzņēmuma “Litware, Inc.” ER konfigurācijas. 

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot USMF datu kopu.


## <a name="review-the-imported-data-model"></a>Pārskatīt importēto datu modeli
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Koka struktūrā atlasiet “Čeku modelis”.
3. Noklikšķiniet uz Veidotājs.
    * Šis modelis ir paredzēts, lai parādītu maksājumu čekus no biznesa viedokļa un šī modeļa kartējumu programmas datu avotiem. Pārskatiet šo modeli, izmantojot ER operāciju veidotāju. Ņemiet vērā, ka tiek rādīti šādi modeļa elementu atribūti: struktūra, nosaukums, apraksts, datu tips u.t.t.   
4. Kokā izvērsiet elementu “sakne”.
5. Kokā atlasiet 'root\cheques'.
6. Kokā izvērsiet 'root\cheques'.
7. Kokā izvērsiet 'root\cheques\attributes'.
8. Kokā izvērsiet 'root\payer'.
9. Kokā atlasiet 'root\istestrun'.
10. Kokā atlasiet 'root\layout'.
    * Šī modeļa izkārtojuma elements parāda detalizētu informāciju par čeku drukāšanas formas izkārtojumu atlasītajam bankas kontam. Tajā ir iekļauti arī divi mezgli ar datu tipu “Konteiners”, lai glabātu attēlus.   
11. Kokā izvērsiet 'root\layout'.
12. Kokā atlasiet 'root\layout\company logo'.
13. Kokā izvērsiet 'root\layout\company logo'.
14. Kokā atlasiet 'root\layout\company logo\image'.
15. Kokā atlasiet 'root\layout\company logo\isprinted'.
16. Kokā atlasiet 'root\layout\signature'.
17. Kokā izvērsiet 'root\layout\signature'.
18. Kokā atlasiet 'root\layout\signature\image'.
19. Kokā atlasiet 'root\layout\signature\isprinted'.
    * Ņemiet vērā, ka divi attēla datu modeļa elementi ir saistīti ar tabulu laukiem, kas satur uzņēmuma logotipa un pilnvarotas personas paraksta attēlus binārā formātā.  
20. Kokā izvērsiet 'root\layout\watermark'.
21. Noklikšķiniet uz Kartēšanas modelis datu avotam.
22. Noklikšķiniet uz Veidotājs.
23. Kokā izvērsiet “chequesselected”.
24. Kokā izvērsiet elementu “izkārtojums”.
25. Kokā izvērsiet 'layout\company logo'.
26. Kokā izvērsiet 'layout\signature'.
27. Kokā izvērsiet 'layout\watermark'.
28. Ieslēdziet opciju “Rādīt detalizēti”.
    * Ņemiet vērā, ka čeku datu modeļa elements ir saistīts ar tabulu TmpChequePrintout, kura izpildlaikā saturēs čeku ierakstus, kurus lietotājs ir atlasījis drukāšanai.   
29. Aizvērt lapu.
30. Aizvērt lapu.
31. Aizvērt lapu.

## <a name="review-the-imported-format"></a>Pārskatīt importēto formātu
1. Koka struktūrā izvērsiet “Čeku modelis”.
2. Kokā atlasiet 'Model for cheques\Cheques printing format'.
3. Noklikšķiniet uz Veidotājs.
4. Noklikšķiniet uz Pielikumi.
5. Noklikšķiniet uz Atvērt.
    * Atveriet pievienoto pārskata veidni programmā Excel.  
    * Pārskatiet pievienoto pārskata Excel veidni, kas tiks izmantota, lai drukātu čekus. Veidne satur divus čekus katrā lapā un ir paredzēta, lai izdrukātu čekus iepriekš izdrukātā veidlapā. Ņemiet vērā, ka ir iegulti divi tukši attēli. Šie tukšie attēli ir paredzēti uzņēmuma logotipam un tās personas parakstam, kas pilnvaro maksājumu. Pārbaudiet, vai attēlu nosaukumi programmā Excel ir attiecīgi CompLogo un SignatureImage.   
6. Aizvērt lapu.
7. Kokā izvērsiet “Pārskats”.
8. Kokā izversiet 'Report\ChequeLines'.
9. Kokā izvērsiet 'Report\ChequeLines\CompLogo'.
10. Ieslēdziet opciju “Rādīt detalizēti”.
    * Ņemiet vērā, ka “CompLogo” formāta šūnas elements ir Excel vienums, kas tiek izmantots, lai aizpildītu uzņēmuma logotipa attēlu pārskatā. Šis formāta elements ir saistīts ar attēlu datu modeļa elementu, kas izpildlaikā satur uzņēmuma logotipa attēlu binārā formātā.   
11. Noklikšķiniet uz cilnes Kartēšana.
12. Noklikšķiniet uz Rediģēšana iespējota.
    * Ņemiet vērā, ka varat pārveidot 'CompLogo' formāta šūnas elementu, lai tas vairs nebūtu aktivizēts. Tādā gadījumā saistītais Excel attēla elements paslēps uzņēmuma logotipu ģenerētajā pārskatā. Ja aktivizētā izteiksme atgriež vērtību TRUE un definētā saistība neparāda attēlu, saistītais Excel attēla elements rāda attēlu, kas ir saglabāts Excel veidnē.   
13. Aizvērt lapu.
14. Kokā izvērsiet “etiķetes: Konteiners”.
    * Dažas etiķetes, kas ir redzamas iepriekš izdrukātā čeka veidlapā, tiks iekļautas pārskatā, veidojot to testēšanas nolūkiem. Tomēr šīs etiķetes netiks drukātas īstās drukāšanas laikā, jo tās jau ir ietvertas iepriekš izdrukātajā veidlapā.  
15. Aizvērt lapu.


