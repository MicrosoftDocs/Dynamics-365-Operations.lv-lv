--- 
title: "Kartēt modeļus finanšu dimensiju kā datu avota lietošanai elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.openlocfilehash: a3eafa7b66dcc0c2481d7eeaf98bed7f58e4be33
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Kartēt modeļus finanšu dimensiju kā datu avota lietošanai elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem. Šīs darbības var veikt jebkurā uzņēmumā.

Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (1. daļa: datu modeļa izveide).


## <a name="add-required-data-sources-to-model-mapping"></a>Pievienot nepieciešamos datu avotus modeļa kartēšanai
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.
3. Noklikšķiniet uz Veidotājs.
4. Noklikšķiniet uz Kartēšanas modelis datu avotam.
5. Noklikšķiniet uz Jauns.
6. Laukā Definīcija, atlasiet Ieraksts.
7. Laukā Nosaukums ierakstiet 'Dimensiju datu kartēšana'.
8. Laukā Apraksts ierakstiet 'Dimensiju datu kartēšana'.
9. Noklikšķiniet uz Saglabāt.
10. Noklikšķiniet uz Veidotājs.
11. Kokā atlasiet "Dynamics 365 for Operations\Table".
12. Noklikšķiniet uz Pievienot sakni.
13. Laukā Nosaukums ierakstiet "Uzņēmums".
14. Laukā Tabula ierakstiet "CompanyInfo".
15. Noklikšķiniet uz Labi.
16. Koka struktūrā atlasiet 'Funkcijas\Detalizēta informācija par finanšu dimensijām'.
17. Noklikšķiniet uz Pievienot sakni.
    * Šis datu avots norāda finanšu dimensiju sfēru, kas tiks definēta jebkuram pārskatam, kas tiks izmantots šajā modelī kā datu avots.  
18. Laukā Nosaukums ierakstiet kādu vērtību.
19. Atlasiet Jā laukā Jautāt dimensijas.
    * Atlasiet Jā, lai lietotājs varētu atlasīt dimensijas Lietotāja dialoglodziņā izpildes laikā. Ja iestatīts uz Nē, visas pašreizējās instances finanšu dimensijas tiks izmantotas pēc noklusējuma.  
20. Finanšu dimensiju atlases laukā atlasiet 'Juridiska persona'.
    * Atlasiet Visu, lai lietotājs varētu atlasīt vēlamo dimensiju pašreizējai instancei laukā Uzmeklēšana.  Atlasiet juridisko personu, lai lietotājs varētu atlasīt dimensijas uzņēmumam laukā Uzmeklēšana.  Atlasīt Dimensiju, lai lietotājs varētu atlasīt dimensijas, izmantojot vienu dimensiju kopu.  
21. Atlasiet Jā laukā Jautāt galveno kontu.
    * Iestatiet “Jautāt galveno kontu” uz Jā, lai atļautu lietotājiem atlasīt galveno kontu kā daļu no dimensiju saraksta.   Ja ir iestatīts uz Nē, galvenais konts netiks iekļauts dimensiju sarakstā, un opcija “Vai galvenais konts ir obligāts” ir iespējota. Ja opcija “Vai galvenais konts ir obligāts” ir iestatīta uz Jā, iekļaujiet galveno kontu dimensiju sarakstā, neatkarīgi no lietotāja veiktās atlases.  
22. Noklikšķiniet uz OK.
23. Kokā atlasiet "Dynamics 365 for Operations\Table records".
24. Noklikšķiniet uz Pievienot sakni.
25. Laukā Nosaukums ierakstiet 'LedgerJournal'.
26. Laukā Pieprasīt vaicājumu atlasiet Jā.
27. Laukā Tabula ievadiet 'LedgerJournalTable'.
28. Noklikšķiniet uz OK.

## <a name="map-data-model-elements-to-added-data-sources"></a>Kartēt datu modeļa elementus pievienotajiem datu avotiem
1. Kokā izvērsiet 'Žurnāls'.
2. Kokā izvērsiet 'Žurnāls\Darbība'.
3. Kokā izvērsiet 'Žurnāls\Darbība\Dimensiju dati'.
4. Kokā izvērsiet 'Dimensiju iestatījums'.
5. Kokā izvērsiet 'LedgerJournal'.
6. Kokā izvērsiet "LedgerJournal\<Relations".
7. Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans".
8. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Voucher".
9. Kokā atlasiet 'Žurnāls\Darbība\Dokuments'.
10. Noklikšķiniet uz Saistīt.
11. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".
    * Ņemiet vērā, ka visām iestatītajām atsaucēm uz finanšu dimensijām, piemēram, LedgerDimension, ir pieejams attiecīgais datu avota vienums (LedgerDimension.Dimension). Šī datu avota vienums nodrošina finanšu dimensijas no dimensiju kopas kā ierakstu sarakstu.  
12. Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".
13. Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".
14. Kokā izvērsiet "LedgerJournal\\<Relācijas\LedgerJournalTrans\Konts.Dimensija(LedgerDimension.Dimension)\Galvenais konts un dimensijas\Vērtība".
15. Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition".
16. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name".
17. Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Nosaukums'.
18. Noklikšķiniet uz Saistīt.
19. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description".
20. Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Apraksts'.
21. Noklikšķiniet uz Saistīt.
22. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code".
23. Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Kods'.
24. Noklikšķiniet uz Saistīt.
25. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".
26. Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati'.
27. Noklikšķiniet uz Saistīt.
28. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)".
29. Kokā atlasiet 'Žurnāls\Darbība\Debets'.
30. Noklikšķiniet uz Saistīt.
31. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)".
32. Kokā atlasiet 'Žurnāls\Darbība\Datums'.
33. Noklikšķiniet uz Saistīt.
34. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)".
35. Kokā atlasiet 'Žurnāls\Darbība\Valūta'.
36. Noklikšķiniet uz Saistīt.
37. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)".
38. Kokā atlasiet 'Žurnāls\Darbība\Kredīts'.
39. Noklikšķiniet uz Saistīt.
40. Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans".
41. Kokā atlasiet 'Žurnāls\Darbība'.
42. Noklikšķiniet uz Saistīt.
43. Kokā atlasiet 'LedgerJournal\Žurnāla iedaļas numurs(JournalNum)'.
44. Kokā atlasiet 'Žurnāls\Iedaļa'.
45. Noklikšķiniet uz Saistīt.
46. Kokā atlasiet 'LedgerJournal'.
47. Kokā atlasiet 'Žurnāls'.
48. Noklikšķiniet uz Saistīt.
49. Kokā izvērsiet 'Dimensijas'.
50. Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas'.
51. Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija'.
52. Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Nosaukums'.
53. Kokā izvērsiet 'Dimensiju iestatīšana\Kods'.
54. Noklikšķiniet uz Saistīt.
55. Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Pārskata kolonnas nosaukums'.
56. Kokā atlasiet 'Dimensiju iestatīšana\Nosaukums'.
57. Noklikšķiniet uz Saistīt.
58. Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas'.
59. Kokā atlasiet 'Dimensiju iestatīšana'.
60. Noklikšķiniet uz Saistīt.
61. Kokā atlasiet 'Uzņēmums'.
62. Noklikšķiniet uz Rediģēt.
63. Laukā expressionAsStringText field ievadiet 'Uzņēmums.'atrast()'.'nosaukums()''.
    * Uzņēmums.'atrast()'.'nosaukums()'  
64. Noklikšķiniet uz Saglabāt.
65. Aizvērt lapu.
66. Noklikšķiniet uz Saglabāt.
67. Aizvērt lapu.

## <a name="complete-this-draft-models-version"></a>Pabeigt šo modeļa melnraksta versiju
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Noklikšķiniet uz Mainīt statusu.
4. Noklikšķiniet uz Pabeigt.
5. Noklikšķiniet uz OK.

