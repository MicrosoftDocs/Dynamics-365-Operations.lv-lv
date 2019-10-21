---
title: ER datu modeļa kartēšana ar izvēlētajiem datu avotiem
description: Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko pārskatu izstrādātājs datu modeli Elektronisko pārskatu veidošana (Electronic reporting — ER) var kartēt uz izvēlētajiem Microsoft Dynamics 365 Finance datu avotiem.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44f6ac3263f115e76d054e68c99d58dc11e6f1a0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182236"
---
# <a name="er-map-data-model-to-selected-data-sources"></a>ER datu modeļa kartēšana ar izvēlētajiem datu avotiem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko pārskatu izstrādātājs datu modeli Elektronisko pārskatu veidošana (Electronic reporting — ER) var kartēt uz izvēlētajiem datu avotiem. Šis modeļa kartējums vēlāk tiks izmantots kā datu avots formāta konfigurācijā, kas tiks izmantota, lai pārvaldītu elektroniskos maksājuma dokumentus. Šajā piemērā parauga uzņēmuma Litware, Inc. datu modelis tiek kartēts par datu avotiem. Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras "Datu avotu atlasīšana modeļa kartēšanai" darbības.


## <a name="open-er-configurations-tree"></a>ER konfigurācijas koka atvēršana
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Konfigurācijas.

## <a name="select-created-model-mapping"></a>Izveidotās modeļa kartēšanas atlasīšana
1. Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.
    * Pārliecinieties, ka modeļa konfigurācija "Maksājumi (vienkāršotas modelis)" tika izveidota iepriekš. Pretējā gadījumā beidziet šeit sniegto norādījumu izpildi un atgriezties pēc tam, kad ir izpildīts uzdevuma ceļvedis “Izveidot jaunu konfigurāciju ar izvēlēta domēna datu modeli”.  
2. Noklikšķiniet uz Modeļa veidotājs.
3. Noklikšķiniet uz Kartēšanas modelis datu avotam.
4. Atlasiet ierakstu "CT kartēšana".
    * CT kartēšana  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Izveidoto datu avotu saistīšana ar datu modeļa elementiem
1. Noklikšķiniet uz Veidotājs.
2. Koka skatā atlasiet Apstrādes datums un laiks(ProcessingDateTime).
3. Kokā atlasiet "Apstrādes datums(ProcessingDateTime)".
4. Noklikšķiniet uz Saistīt.
5. Kokā atlasiet "Maksājuma ziņojuma identifikācija(MessageIdentification)".
6. Kokā izvērsiet sadaļu "Transakcija".
7. Kokā atlasiet "Transakcijas\Žurnāla partijas numurs(JournalNum)".
8. Noklikšķiniet uz Saistīt.
9. Kokā struktūrā atlasiet "Maksājumi".
10. Kokā atlasiet "Transakcijas".
11. Noklikšķiniet uz Saistīt.
12. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas”.
13. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Kreditors”.
14. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Kreditors\Konts”.
15. Kokā atlasiet "Maksājumi= Transakcijas\Kreditors\Konts\Valūtas kods(Currency)'.
16. Kokā izvērsiet "Transakcijas\vendBankAccountInTransactionCompany()".
17. Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Valūta(CurrencyCode)".
18. Noklikšķiniet uz Saistīt.
19. Kokā atlasiet "Maksājumi= Transakcijas\Kreditors\Konts\IBAN kods(IBAN).
20. Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)".
21. Noklikšķiniet uz Saistīt.
22. Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Konts\Numurs”.
23. Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Bankas konta numurs(AccountNum)".
24. Noklikšķiniet uz Saistīt.
25. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Kreditors\Aģents”.
26. Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Aģents\Nosaukums”.
27. Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Nosaukums".
28. Noklikšķiniet uz Saistīt.
29. Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Aģents\Maršrutēšanas numurs(RoutingNumber)”.
30. Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Maršrutēšanas numurs(RegistrationNum)".
31. Noklikšķiniet uz Saistīt.
32. Kokā atlasiet "Maksājumi= Transakcijas\Kreditors\Aģents\SWIFT kods(SWIFT)".
33. Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\SWIFT kods(SWIFTNo)".
34. Noklikšķiniet uz Saistīt.
35. Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Nosaukums”.
36. Kokā izvērsiet sadaļu “Transakcijas\findVendTable()”.
37. Koka skatā atlasiet Transakcijas\findVendTable()\name().
38. Noklikšķiniet uz Saistīt.
39. Kokā atlasiet "Maksājumi= Transakcijas\Valūtas kods(Currency)".
40. Kokā izvērsiet 'Transactions\>Relations'.
41. Kokā izvērsiet 'Transactions\>Relations\Currency table(Currency)'.
42. Kokā atlasiet 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.
43. Noklikšķiniet uz Saistīt.
44. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Debitors”.
45. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Debitors\Konts”.
46. Kokā atlasiet "Maksājumi= Transakcijas\Debitors\Konts\Valūtas kods(Currency)'.
47. Kokā atlasiet "Bankas konts(BankAccount)".
48. Kokā izvērsiet sadaļu "Bankas konts(BankAccount)".
49. Kokā atlasiet "Bankas konts(BankAccount)\Valūta(CurrencyCode)".
50. Noklikšķiniet uz Saistīt.
51. Kokā atlasiet "Bankas konts(BankAccount)\IBAN".
52. Kokā atlasiet "Maksājumi= Transakcijas\Debitors\Konts\IBAN kods(IBAN).
53. Noklikšķiniet uz Saistīt.
54. Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Konts\Numurs”.
55. Kokā atlasiet "Bankas konts(BankAccount)\Bankas konta numurs(AccountNum)".
56. Noklikšķiniet uz Saistīt.
57. Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Debitors\Aģents”.
58. Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Aģents\Nosaukums”.
59. Kokā atlasiet "Bankas konts(BankAccount)\Nosaukums".
60. Noklikšķiniet uz Saistīt.
61. Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Aģents\Maršrutēšanas numurs(RoutingNumber)”.
62. Kokā atlasiet "Bankas konts(BankAccount)\Maršrutēšanas numurs(RegistrationNum)".
63. Noklikšķiniet uz Saistīt.
64. Kokā atlasiet "Maksājumi= Transakcijas\Debitors\Aģents\SWIFT kods(SWIFT)".
65. Kokā atlasiet "Bankas konts(BankAccount)\SWIFT kods(SWIFTNo)".
66. Noklikšķiniet uz Saistīt.
67. Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Nosaukums”.
68. Kokā atlasiet "Informācija par uzņēmumu(Company)".
69. Kokā izvērsiet sadaļu "Informācija par uzņēmumu(Company)".
70. Kokā atlasiet "Informācija par uzņēmumu(Company)\Nosaukums".
71. Noklikšķiniet uz Saistīt.
72. Kokā atlasiet “Maksājumi= Transakcijas\Apraksts”.
73. Kokā atlasiet “Transakcijas\Apraksts(Txt)”.
74. Noklikšķiniet uz Saistīt.
75. Kokā atlasiet "Maksājumi= Transakcijas\Pilns identifikācijas kods(End2EndID)".
76. Kokā atlasiet 'Transactions\$EndToEndID'.
77. Noklikšķiniet uz Saistīt.
78. Kokā atlasiet "Maksājumi= Transakcijas\Instruētā summa(InstructedAmount)".
79. Kokā atlasiet "Transactions\$Amount".
80. Noklikšķiniet uz Saistīt.
81. Kokā atlasiet "Maksājumi= Transakcijas\Transakcijas datums(TransactionDate)".
82. Kokā atlasiet “Transakcijas\Datums(TransDate)”.
83. Noklikšķiniet uz Saistīt.

## <a name="validate-created-mapping"></a>Izveidotās kartēšanas apstiprināšana
1. Noklikšķiniet uz Pārbaudīt.
    * Validējiet jauno kartēšanu, lai pārliecinātos, ka visi saistījumi ir pareizi.  
2. Noklikšķiniet uz bultiņas, lai izvērstu vai sakļautu sadaļu Kļūdu saraksts.
3. Noklikšķiniet uz Saglabāt.
4. Aizvērt lapu.
5. Aizvērt lapu.
6. Aizvērt lapu.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Mainiet modeļa konfigurācijas pašreizējās versijas statusu.
1. Noklikšķiniet uz Mainīt statusu.
    * Mainiet izstrādātās modeļa konfigurācijas statusu — no Melnraksts uz Pabeigts, lai tā kļūtu pieejama maksājumu formāta noformējumam.  
2. Noklikšķiniet uz Pabeigt.
    * Atlasiet Pabeigt.  
3. Apraksta laukā ierakstiet vērtību.
    * Piemēram, “1. versija”.  
4. Noklikšķiniet uz OK.
5. Atlasiet pašreizējās konfigurācijas pabeigto versiju.
    * Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.  

