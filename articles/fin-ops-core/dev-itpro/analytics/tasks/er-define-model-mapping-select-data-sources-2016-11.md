---
title: ER modeļu kartējumu definēšana un datu avotu atlasīšana tiem
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var atlasīt datu avotus datu modelim Elektroniskie pārskati.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b5f291372bc459bc1979dca4a95cfafb39e2ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567298"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>ER modeļu kartējumu definēšana un datu avotu atlasīšana tiem

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var atlasīt datu avotus datu modelim Elektroniskie pārskati (ER). Datu avoti tiks saistīti ar atlasītā datu modeļa atsevišķiem komponentiem noformēšanas laikā un aizpildīs biznesa datus šajā datu modelī izpildes laikā. Šajā piemērā jāatlasa parauga uzņēmumam Litware, Inc. izveidotie esošā datu modeļa datu avoti. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā "Jauna datu modeļa izveidošana” aprakstītās darbības.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Atvērt koka struktūru Elektronisko pārskatu veidošanas konfigurācijas
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.

## <a name="insert-a-new-model-mapping"></a>Jaunas modeļa kartēšanas iespraušana
1. Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.
2. Noklikšķiniet uz Veidotājs.
3. Noklikšķiniet uz Kartēšanas modelis datu avotam.
4. Noklikšķiniet uz Jauns.
    * Šādi tiks izveidots jauns ieraksts, kas kartēs datu modeli datu avotos. Šajā piemērā jūs kartēsiet datu modeli datu avotos vēlamajam maksājuma tipam: kredīta pārsūtīšana.     Ir iespējams izveidot vairāk nekā vienu kartēšanu konkrētam datu modelim. Piemēram, var izveidot kartēšanu dažāda veida maksājumiem, piemēram, tiešajam debetam vai kredīta pārsūtījumiem. Šajā piemērā jūs izveidosiet kartēšanu kredīta pārsūtījumiem.  
5. Laukā Nosaukums ierakstiet “CT kartēšana”.
    * CT kartēšana  
6. Laukā Apraksts ierakstiet "Maksājumu modeļa kartēšanas CT".
    * Maksājumu modeļa kartēšanas CT  
7. Laukā Definīcija ierakstiet “CustomerCreditTransferInitiation”.
    * CustomerCreditTransferInitiation  
8. ResolveChanges vienumam Definīcija.
9. Noklikšķiniet uz Saglabāt.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Pašreizējā modeļa kartēšanai nepieciešamo datu avotu definēšana
1. Noklikšķiniet uz Veidotājs.
2. Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.
3. Noklikšķiniet uz Pievienot sakni.
    * Ievadiet šo datu avotu, lai piekļūtu maksājumu transakcijām.  
4. Laukā Nosaukums ierakstiet “Transakcijas”.
    * Darbības  
5. Laukā Iezīme ievadiet “Transakcijas”.
    * Darbības  
6. Laukā Palīdzība ievadiet "Virsgrāmatas žurnāla rindas".
    * Virsgrāmatas žurnāla rindas  
7. Laukā Pieprasīt vaicājumu atlasiet Jā.
    * Atlasiet Jā.  
8. Laukā Tabula ierakstiet 'LedgerJournalTrans'.
    * LedgerJournalTrans  
9. Noklikšķiniet uz OK.
    * Atlasiet tabulu LedgerJournalTrans kā pašreizējā datu modeļa datu avotu.  
10. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
11. Noklikšķiniet uz Pievienot.
    * Noklikšķiniet uz Pievienot, lai pievienotu jaunu aprēķināto lauku.  
12. Laukā Nosaukums ierakstiet "$EndToEndID".
    * $EndToEndID  
13. Noklikšķiniet uz Rediģēt formulu.
14. Kokā atlasiet “Virkne\CONCATENATE”.
15. Noklikšķiniet uz Pievienot funkciju.
16. Kokā izvērsiet sadaļu "Transakcija".
17. Kokā atlasiet "Transakcijas\Dokuments".
18. Noklikšķiniet uz Pievienot datu avotu.
19. Laukā Formula ievadiet “CONCATENATE(Transactions.Voucher, "-", ”.
    * Ierakstiet [ , "-", ] formulas beigās.  
20. Kokā atlasiet "Virkne\TEXT".
21. Noklikšķiniet uz Pievienot funkciju.
22. Kokā atlasiet "Transakcijas\Ieraksta ID(RecId)".
23. Noklikšķiniet uz Pievienot datu avotu.
24. Laukā Formula ievadiet “CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))”.
    * Ierakstiet [))] formulas beigās.  
25. Noklikšķiniet uz Saglabāt.
    * Pārliecinieties, ka izveidotajā formulā nav kļūdu. Skatiet cilni KĻŪDAS zem formulas redaktora vadīklas.  
26. Aizvērt lapu.
27. Noklikšķiniet uz OK.
    * Pievienojiet aprēķināto lauku šim datu avotam.  
28. Noklikšķiniet uz Pievienot.
    * Noklikšķiniet uz Pievienot, lai pievienotu jaunu aprēķināto lauku.  
29. Laukā Nosaukums ierakstiet "$Amount".
    * $Amount  
30. Noklikšķiniet uz Rediģēt formulu.
31. Kokā izvērsiet sadaļu "Transakcija".
32. Kokā atlasiet "Transakcijas\Debets(AmountCurDebit)".
33. Noklikšķiniet uz Pievienot datu avotu.
34. Laukā Formula ievadiet “Transactions.AmountCurDebit - ”.
    * Ierakstiet [ - ] formulas beigās.  
35. Kokā atlasiet "Transakcijas\Kredīts(AmountCurCredit)".
36. Noklikšķiniet uz Pievienot datu avotu.
37. Noklikšķiniet uz Saglabāt.
38. Aizvērt lapu.
39. Noklikšķiniet uz OK.
    * Šādi pašreizējam datu modelim atlasītajam datu avotam tiks pievienots aprēķinātais lauks $Amount.  
40. Kokā atlasiet "Transactions\$Amount".
41. Kokā izvērsiet sadaļu "Transakcija".
42. Koka struktūrā izvērsiet vai sakļaujiet zaru “Transactions\$Amount".
43. Koka struktūrā izvērsiet vai sakļaujiet zaru “Transakcijas”.
44. Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.
45. Noklikšķiniet uz Pievienot sakni.
    * Ievadiet šo datu avotu, lai piekļūtu uzņēmuma bankas konta detaļām.  
46. Laukā Nosaukums ierakstiet "BankAccount".
    * BankAccount  
47. Laukā Iezīme ievadiet “Bankas konts”.
    * Bankas konts  
48. Laukā Palīdzība ievadiet “Bankas konts”.
    * Bankas konts  
49. Laukā Pieprasīt vaicājumu atlasiet Jā.
    * Atlasiet Jā.  
50. Laukā Tabula ierakstiet "BankAccountTable".
    * BankAccountTable  
51. Noklikšķiniet uz OK.
    * Atlasiet tabulu BankAccountTable kā pašreizējā datu modeļa datu avotu.  
52. Noklikšķiniet uz Pievienot sakni.
    * Ievadiet šo datu avotu, lai piekļūtu uzņēmuma bankas konta rekvizītiem.  
53. Laukā Nosaukums ierakstiet "Uzņēmums".
    * Uzņēmums  
54. Laukā Iezīme ierakstiet vērtību.
    * Uzņēmuma informācija  
55. Laukā Palīdzība ievadiet "Uzņēmuma informācija".
    * Uzņēmuma informācija  
56. Laukā Pieprasīt vaicājumu atlasiet Jā.
    * Atlasiet Jā.  
57. Laukā Tabula ierakstiet "CompanyInfo".
    * CompanyInfo  
58. Noklikšķiniet uz OK.
    * Atlasiet tabulu CompanyInfo kā pašreizējā datu modeļa datu avotu.  
59. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
60. Noklikšķiniet uz Pievienot sakni.
    * Iespraudiet aprēķināto lauku kā jaunu datu avotu.  
61. Laukā Nosaukums ievadiet "ProcessingDateTime".
    * ProcessingDateTime  
62. Laukā Atzīme ievadiet tekstu Apstrādes datums un laiks.
    * Apstrādes datums un laiks  
63. Noklikšķiniet uz Rediģēt formulu.
64. Koka struktūrā atlasiet zaru “Datums/laiks\SESSIONNOW”.
65. Noklikšķiniet uz Pievienot funkciju.
66. Noklikšķiniet uz Saglabāt.
67. Aizvērt lapu.
68. Noklikšķiniet uz OK.
    * Pievienojiet aprēķināto lauku ProcessingDateTime kā pašreizējā datu modeļa datu avotu.  
69. Noklikšķiniet uz Saglabāt.
70. Aizvērt lapu.
71. Aizvērt lapu.
72. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]