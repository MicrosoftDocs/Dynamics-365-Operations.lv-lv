---
title: Elektronisko pārskatu modeļa kartēšanas pārvaldība atsevišķās elektronisko pārskatu konfigurācijās
description: Šajā rakstā ir aprakstīts, kā pārvaldīt elektronisko pārskatu (ER) modeļa kartējumus atsevišķās ER konfigurācijās.
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23ac14ba06b6ab535545bacbafe90a4a3c946476
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290250"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>ER modeļa kartēšanas pārvaldība atsevišķās ER konfigurācijās

[!include [banner](../../includes/banner.md)]

Turpmāk uzskaitītajos posmos paskaidrots, kā lietotājs, kurš piešķirts sistēmas administratoram vai elektronisko ziņojumu izstrādātāja lomai, var pārvaldīt elektronisko ziņojumu (ER) modeļu veidošanu atsevišķās ER konfigurācijās. Šajā uzdevumu ceļvedis jūs izveidosiet nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. Lai izpildītu šīs uzskaitītajos posmos darbības, vispirms izpildiet uzskaitītajos posmos "ER: Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu". 

Jo ER konfigurācijas ir kopīgotas starp uzņēmumiem, var aizpildīt rokasgrāmatas uzdevumu, izmantojot uzņēmuma datu kopas pēc savas izvēles. Šī uzdevuma ceļveža funkcionalitāte ir pieejama tad, ja esat instalējis kādu no šiem labojumfailiem: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 versijai Dynamics AX 7.0 vai https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 versijai Dynamics 365 for Operations.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārbaudiet, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas uzdevuma ceļvedī “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.   

## <a name="add-a-new-er-model-configuration"></a>Pievienot jaunu ER modeļa konfigurāciju
1. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
    * Pievienojiet jaunu modeļa konfigurāciju. Nosaukumam jābūt unikālam konfigurāciju kokā.  
2. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Nosaukums ierakstiet “Parauga datu modelis”.
    * Parauga datu modelis  
4. Klikšķiniet Izveidot konfigurāciju.
5. Noklikšķiniet uz Veidotājs.
6. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
7. Laukā Nosaukums ierakstiet 'Sakne'.
    * Sakne  
8. Noklikšķiniet uz Pievienot.
9. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
10. Laukā Nosaukums ierakstiet "Uzņēmums".
    * Uzņēmums  
11. Noklikšķiniet uz Pievienot.
12. Ievadiet tekstu, juridiska persona vai uzņēmums, kurā lietotājs reģistrējies izpildes laikā aprakstu laukā Apraksts. 
    * Tās juridiskās persona vai uzņēmuma apraksts, kurā lietotājs ir pieteicies izpildlaikā.  
13. Noklikšķiniet uz Saknes atsauce.
14. Noklikšķiniet uz OK.
15. Noklikšķiniet uz Saglabāt.
16. Aizvērt lapu.
17. Noklikšķiniet uz Mainīt statusu.
18. Noklikšķiniet uz Pabeigt.
19. Noklikšķiniet uz Labi.

## <a name="add-a-new-er-model-mapping-configuration"></a>Pievienot jaunu ER datu modeļa kartējuma konfigurāciju
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns ievadiet "Model Mapping based on data model Sample data model".
3. Laukā Nosaukums ierakstiet "Sample mapping".
    * Kartējuma paraugs  
4. Klikšķiniet Izveidot konfigurāciju.
5. Izvērsiet priekšnoteikumu sadaļu.
    * Ir automātiski pievienota grupa “Ieviešanas priekšnoteikumi”. Grupa satur priekšnoteikumu komponentu, kas attiecas uz pamata datu modeļa konfigurāciju un ir atzīmēts kā Ieviešana. Tas nozīmē, ka šī parauga kartējuma modeļa kartēšanas konfigurācija tiek uzskatīta par datu modeļa Parauga datu modelis ieviešanu. Tāpēc šis komponents liks ER lejupielādēt modeļa kartējuma konfigurāciju Kartējuma paraugs no ER repozitorija, kad tiks lejupielādēta modeļa konfigurācija Parauga datu modelis.   
6. Noklikšķiniet uz Veidotājs.
    * Izveidotā modeļa kartējuma konfigurācija satur jaunu tukšu kartējumu ar tādu pašu nosaukumu kā izveidotajai konfigurācijai. Gadījumā, kad atlasītā pamata modeļa konfigurācija ietver modeļa kartējumus, tie tiks kopēti uz jaunu modeļa kartēšanas konfigurāciju.   
7. Noklikšķiniet uz Veidotājs.
8. Kokā atlasiet 'Dynamics 365 for Operations\Tabula'.
9. Noklikšķiniet uz Pievienot sakni.
10. Laukā Nosaukums ierakstiet "Uzņēmums".
    * Uzņēmums  
11. Laukā Tabula ierakstiet "CompanyInfo".
    * CompanyInfo  
12. Noklikšķiniet uz OK.
13. Kokā izvērsiet elementu “Uzņēmums”.
14. Kokā izvērsiet 'Company\find()'.
15. Kokā atlasiet 'Company\find()\Name'.
16. Noklikšķiniet uz Saistīt.
17. Noklikšķiniet uz Saglabāt.
18. Aizvērt lapu.
19. Aizvērt lapu.
20. Darbību rūtī noklikšķiniet uz Konfigurācijas.
21. Noklikšķiniet uz Lietotāja parametri.
22. Laukā Palaist iestatījumus atlasiet Jā.
23. Noklikšķiniet uz OK.
24. Noklikšķiniet uz Rediģēt.
25. Laukā Palaist melnrakstu atlasiet Jā.

## <a name="add-a-new-er-format-configuration"></a>Jaunas ER formāta konfigurācijas pievienošana
1. Kokā atlasiet "Sample data model".
2. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Jauns ievadiet "Format based on data model Sample data model".
4. Laukā Nosaukums ierakstiet "Sample format".
    * Parauga formāts  
5. Klikšķiniet Izveidot konfigurāciju.
6. Noklikšķiniet uz Veidotājs.
7. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
8. Kokā atlasiet elementu “Teksts\Virkne”.
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz cilnes Kartēšana.
11. Koka struktūrā izvērsiet elementu “modelis”.
12. Kokā atlasiet 'model\Company'.
13. Noklikšķiniet uz Saistīt.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.
    * Palaist melnraksta versiju izveides formāts testēšanas nolūkos.  
16. Noklikšķiniet uz Palaist.
    * Kopsavilkuma cilnē Versijas noklikšķiniet uz Palaist.  
17. Noklikšķiniet uz OK.
    * Pārskatiet izvadi, kas norādīts, kurā nav pieteicies lietotājs, kurš darbojas šī formāta konfigurāciju uzņēmuma nosaukums. Izveidotā modeļa kartēšanas konfigurācijā tiek izmantota šī formāta konfigurācija, jo ir pieejama tikai vienu konfigurācija, kas satur nepieciešamā modeļa kartējumus.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Alternatīvas ER modeļa kartējuma konfigurācijas pievienošana
1. Kokā atlasiet "Sample data model".
2. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Jauns ievadiet "Model Mapping based on data model Sample data model".
4. Laukā Nosaukums ierakstiet "Sample mapping (alternative)".
    * Kartējuma paraugs (alternatīva)  
5. Klikšķiniet Izveidot konfigurāciju.
6. Noklikšķiniet uz Veidotājs.
7. Noklikšķiniet uz Veidotājs.
8. Kokā atlasiet 'Dynamics 365 for Operations\Tabula'.
9. Noklikšķiniet uz Pievienot sakni.
10. Laukā Nosaukums ierakstiet "Uzņēmums".
    * Uzņēmums  
11. Laukā Tabula ierakstiet "CompanyInfo".
    * CompanyInfo  
12. Noklikšķiniet uz OK.
13. Noklikšķiniet uz Rediģēt.
14. Kokā atlasiet “Virkne\CONCATENATE”.
15. Noklikšķiniet uz Pievienot funkciju.
16. Kokā izvērsiet elementu “Uzņēmums”.
17. Kokā izvērsiet 'Company\find()'.
18. Kokā atlasiet 'Company\find()\Name'.
19. Noklikšķiniet uz Pievienot datu avotu.
20. Laukā Formula ierakstiet vērtību.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Kokā atlasiet 'Company\find()\Company(DataArea)'.
22. Noklikšķiniet uz Pievienot datu avotu.
23. Laukā Formula ierakstiet vērtību.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Noklikšķiniet uz Saglabāt.
25. Aizvērt lapu.
26. Noklikšķiniet uz Saglabāt.
27. Aizvērt lapu.
28. Aizvērt lapu.
29. Laukā Palaist melnrakstu atlasiet Jā.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Esošas ER modeļa kartēšanas konfigurācijas izmantošana
1. Kokā atlasiet "Sample data model\Sample format".
2. Noklikšķiniet uz Palaist.
    * Atlasīto ER formāta konfigurācijas melnraksta versiju nevar izpildīt, jo ir vairāk nekā viena modeļu kartēšanas konfigurācija, kas pieejama nedefinētam datu modelim, kurš ir izvēlēts kā aktīva ER formāta datu avots.   
    * Pēc tam jūs definēsiet alternatīvu modeļu kartēšanas konfigurāciju kā vienu no tiem modeļu kartējumiem, kas tiks izmantoti kā datu avoti ER formāta izpildei.   
3. Kokā atlasiet "Sample data model\Sample mapping (alternative)".
4. Modeļu kartējuma laukā Noklusējums atlasiet vērtību Jā.
5. Kokā atlasiet "Sample data model\Sample format".
6. Noklikšķiniet uz Palaist.
7. Noklikšķiniet uz Labi.
    * Noklusējuma modeļu kartēšanas konfigurācija tiek izmantota šai formāta konfigurācijai, lai ģenerētu elektronisko dokumentu (izveidotā izvade ietver uzņēmuma kodu).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
