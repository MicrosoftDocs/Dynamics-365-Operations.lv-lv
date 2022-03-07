---
title: ER Izveidotā formāta komponentus kartēt uz datu modeļa elementiem (2016. novembris)
description: Šajā tēmā ir aprakstīts, kā kartēt datu modeļa elementus uz izveidotās elektronisko pārskatu (ER) konfigurācijas komponentiem.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e3d6bcf229f9020ff4dd0479e486f465ffd6383
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570844"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>ER Izveidotā formāta komponentus kartēt uz datu modeļa elementiem (2016. novembris)

[!include [banner](../../includes/banner.md)]

Nākamajā procedūrā ir parādīts, kā lietotājs ar lomu Sistēmas administrators vai lomu Elektroniskā pārskata izstrādātājs datu modeļa elementus var kartēt uz izveidotās elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas komponentiem, kas nosaka elektroniskā dokumenta formātu maksājumu biznesa jomai. Šis formāts vēlāk tiks lietots, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei. Šajā piemērā jūs izveidosiet formāta konfigurāciju parauga uzņēmumam 'Litware, Inc.'. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos. Lai izpildītu šīs darbības, vispirms ir jāizpilda uzdevuma ceļvedī "Izveidot formāta konfigurāciju" aprakstītās darbības.


## <a name="select-a-format-configuration"></a>Atlasīt formāta konfigurāciju
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.
4. Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.
5. Noklikšķiniet uz Veidotājs.

## <a name="map-format-components-to-data-model-elements"></a>Formātā komponentu kartēšana datu modeļa elementos
1. Noklikšķiniet uz Izvērst/sakļaut.
2. Noklikšķiniet uz cilnes Kartēšana.
3. Koka struktūrā izvērsiet elementu “modelis”.
4. Koka struktūrā atlasiet zaru “Xml\Ziņojums\ProcessingDate\DateTime”.
5. Koka struktūrā atlasiet zaru “modelis\ProcessingDateTime”.
6. Noklikšķiniet uz Saistīt.
7. Koka struktūrā atlasiet zaru “Xml\Ziņojums\MessageId\Virkne”.
8. Koka struktūrā atlasiet zaru “modelis\MessageIdentification”.
9. Noklikšķiniet uz Saistīt.
10. Kokā izvērsiet sadaļu “modelis\Maksājumi”.
11. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Summa\Virkne”.
12. Koka struktūrā atlasiet zaru “modelis\Maksājumi\InstructedAmount”.
13. Noklikšķiniet uz Saistīt.
14. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\TransDate\DateTime”.
15. Koka struktūrā atlasiet zaru “modelis\Maksājumi\TransactionDate”.
16. Noklikšķiniet uz Saistīt.
17. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Apraksts\Virkne”.
18. Kokā atlasiet “modelis\Maksājumi\Apraksts”.
19. Noklikšķiniet uz Saistīt.
20. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Valūta\Virkne”.
21. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.
22. Noklikšķiniet uz Saistīt.
23. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\ID”.
24. Koka struktūrā atlasiet zaru “modelis\Maksājumi\End2EndID”.
25. Noklikšķiniet uz Saistīt.
26. Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.
27. Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Konts“.
28. Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Aģents“.
29. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums\Virkne”.
30. Kokā atlasiet “modelis\Maksājumi\Kreditors\Nosaukums”.
31. Noklikšķiniet uz Saistīt.
32. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber\Virkne”.
33. Koka struktūrā atlasiet zaru “modelis\Maksājumi\Kreditors\Aģents\RoutingNumber”.
34. Noklikšķiniet uz Saistīt.
35. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber\Virkne”.
36. Kokā atlasiet “modelis\Maksājumi\Kreditors\Konts\Numurs”.
37. Noklikšķiniet uz Saistīt.
38. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums\Virkne”.
39. Kokā izvērsiet sadaļu “modelis\Maksājumi\Debitors”.
40. Kokā izvērsiet elementu “modelis\Maksājumi\Debitors\Konts“.
41. Kokā izvērsiet sadaļu “modelis\Maksājumi\Debitors\Aģents”.
42. Kokā atlasiet “modelis\Maksājumi\Debitors\Nosaukums”.
43. Noklikšķiniet uz Saistīt.
44. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber\Virkne”.
45. Koka struktūrā atlasiet zaru “modelis\Maksājumi\Debitors\Aģents\RoutingNumber”.
46. Noklikšķiniet uz Saistīt.
47. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber\Virkne”.
48. Kokā atlasiet “modelis\Maksājumi\Debitors\Konts\Numurs”.
49. Noklikšķiniet uz Saistīt.
50. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.
51. Kokā atlasiet “modelis\Maksājumi”.
52. Noklikšķiniet uz Saistīt.
53. Noklikšķiniet uz Saglabāt.

## <a name="validate-format-mapping"></a>Validēt formāta kartējumu
1. Noklikšķiniet uz Pārbaudīt.
    * Validējiet jauno kartēšanu, lai pārliecinātos, ka visi saistījumi ir pareizi.  
2. Aizvērt lapu.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Formāta konfigurācijas pašreizējās versijas statusa maiņa
Nākamajās darbībās jūs formāta konfigurācijas statusu no Melnraksts mainīsiet uz Pabeigts, lai to padarītu pieejamu maksājuma dokumentu ģenerēšanai.  
1. Noklikšķiniet uz Mainīt statusu.
2. Noklikšķiniet uz Pabeigt.
3. Apraksta laukā ierakstiet vērtību.
    * Piemēram, “1. versija”.  
4. Noklikšķiniet uz OK.
5. Atlasiet pašreizējās konfigurācijas pabeigto versiju.
    * Ņemiet vērā, ka konfigurācija tiek saglabāta kā pabeigta versija 1.1. Tā ir formāta versija 1, kas ir balstīta uz datu modeļa versiju 1.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Spēkā stāšanās datuma definēšana formāta pabeigtajai versijai
Katru formāta versiju var konfigurēt, kā pieejamu lietošanai, sākot ar noteiktu datumu. Ja noteiktā datumā ir aktīvas vairākas formāta versijas, tad lietošanai tiek atlasīts visjaunākais formāts (pamatojoties uz versijas numuru). Pareizās versijas atlasīšanai tiek lietota sesijas datuma vērtība.  

## <a name="restrict-access-to-created-format-from-companies"></a>Ierobežot piekļuvi izveidotajam formātam no uzņēmumiem
1. Izvērsiet sadaļu ISO valsts/reģiona kodi.
    * Piekļuvi katram formātam var ierobežot, identificējot konkrētas valstis/reģionus, kuros formāts tiek piemērots. Ja attiecīgā formāta valstu/reģionu saraksts ir tukšs, tad šo formātu var lietot jebkurā uzņēmumā. Ja valstu/reģionu sarakstā ir iekļauti kādi ISO valsts/reģiona kodi, tad šo formātu uzņēmumos var lietot tikai tad, ja uzņēmuma primārā adrese atrodas attiecīgajā valstī/reģionā.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]