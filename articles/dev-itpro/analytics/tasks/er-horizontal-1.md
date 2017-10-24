--- 
title: "Izveidot formātu horizontāli paplašināmu diapazonu izmantošanai, lai dinamiski pievienotu kolonnas programmas Excel pārskatos elektronisko pārskatu veidošanai (ER)"
description: "Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Izveidot formātu horizontāli paplašināmu diapazonu izmantošanai, lai dinamiski pievienotu kolonnas programmas Excel pārskatos elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes. Šīs darbības var veikt jebkurā uzņēmumā.

Lai veiktu šīs darbības, vispirms veiciet tālāk aprakstītās trīs norādes par uzdevumu: 

"ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu"

"ER Lietot finanšu dimensijas kā datu avotu (1. daļa. Noformēt datu modeli)"

"ER Lietot finanšu dimensijas kā datu avotu (2. daļa. Modeļa kartēšana)"

Nepieciešams arī lejupielādēt un saglabāt veidnes lokālo kopiju kopā ar parauga pārskatu, kas pieejams šeit: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="create-a-new-report-configuration"></a>Izveidot jaunu pārskata konfigurāciju
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.
3. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
4. Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli 'Finanšu dimensiju parauga modelis'.
    * Izmantojiet iepriekš izveidoto modeli kā jaunā pārskata datu avotu.  
5. Laukā Nosaukums ierakstiet 'Sample report with horizontally expandable ranges'.
    * Izveidot pārskata paraugu ar horizontāli paplašināmiem diapazoniem  
6. Laukā Nosaukums ierakstiet 'To make Excel output with dynamically adding columns'.
    * Lai sagatavotu Excel izvadi ar dinamisku kolonnu pievienošanu  
7. Laukā Datu modeļa definīcija atlasiet Ieraksts.
8. Klikšķiniet Izveidot konfigurāciju.

## <a name="design-the-report-format"></a>Izstrādāt pārskata formātu
1. Noklikšķiniet uz Veidotājs.
2. Ieslēdziet pārslēgšanas pogu ‘Show details’.
3. Darbību rūtī noklikšķiniet uz Importēt.
4. Noklikšķiniet uz Importēt no Excel.
5. Noklikšķiniet uz Pielikumi.
    * Importējiet pārskata veidni. Šajā nolūka izmantojiet lejupielādēto Excel failu.  
6. Noklikšķiniet uz Jauns.
7. Noklikšķiniet uz Fails.
8. Aizvērt lapu.
9. Ievadiet vai atlasiet kādu vērtību laukā Veidne.
    * Atlasiet lejupielādējamo veidni.  
10. Noklikšķiniet uz OK.
    * Pievienot jaunu diapazonu, lai dinamiski izveidotu finanšu dimensiju Excel izvadi ar visu atlasīto kolonnu skaitu (lietotāja dialoglodziņa veidlapā). Visu kolonnu visās šūnās ir norādīts atsevišķs finanšu dimensijas nosaukums.  
11. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
12. Koka struktūrā atlasiet 'Excel\Range'.
13. Laukā Excel diapazons ierakstiet 'DimNames'.
    * DimNames  
14. Laukā Replicēšanas virziens atlasiet 'Horizontal'.
15. Noklikšķiniet uz Labi.
16. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
17. Noklikšķiniet uz Pārvietot uz augšu.
18. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.
19. Noklikšķiniet uz Izgriezt.
20. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
21. Noklikšķiniet uz Ielīmēt.
22. Koka struktūrā izvērsiet 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
23. Koka struktūrā izvērsiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.
24. Koka struktūrā izvērsiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.
25. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.
    * Pievienot jaunu diapazonu, lai dinamiski izveidotu finanšu dimensiju Excel izvadi ar visu atlasīto kolonnu skaitu (lietotāja dialoglodziņa veidlapā). Visu kolonnu visās šūnās ir norādīta atsevišķa finanšu dimensijas vērtība visām pārskata transakcijām.  
26. Noklikšķiniet uz Pievienot diapazonu.
27. Laukā Excel diapazons ierakstiet 'DimValues'.
    * DimValues  
28. Laukā Replicēšanas virziens atlasiet 'Horizontal'.
29. Noklikšķiniet uz Labi.
30. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.
31. Noklikšķiniet uz Izgriezt.
32. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.
33. Noklikšķiniet uz Ielīmēt.
34. Koka struktūrā izvērsiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.

## <a name="map-format-elements-to-data-sources"></a>Saistīt formātā elementus ar datu avotiem
1. Noklikšķiniet uz cilnes Kartēšana.
2. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis'.
3. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts'.
4. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.
5. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.
6. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.
7. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Kods: Virkne'.
8. Noklikšķiniet uz Saistīt.
9. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.
10. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.
11. Noklikšķiniet uz Saistīt.
12. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.
13. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Kredīts: Reāls'.
14. Noklikšķiniet uz Saistīt.
15. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.
16. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Debets: Reāls'.
17. Noklikšķiniet uz Saistīt.
18. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.
19. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Valūta: Virkne'.
20. Noklikšķiniet uz Saistīt.
21. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.
22. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Datums: Datums'.
23. Noklikšķiniet uz Saistīt.
24. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.
25. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Dokuments: Virkne'.
26. Noklikšķiniet uz Saistīt.
27. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.
28. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Partija: Virkne'.
29. Noklikšķiniet uz Saistīt.
30. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.
31. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.
32. Noklikšķiniet uz Saistīt.
33. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.
34. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Partija: Virkne'.
35. Noklikšķiniet uz Saistīt.
36. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.
37. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts'.
38. Noklikšķiniet uz Saistīt.
39. Koka struktūrā izvērsiet 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.
40. Koka struktūrā atlasiet 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.
41. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.
42. Noklikšķiniet uz Saistīt.
43. Koka struktūrā atlasiet 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.
44. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
45. Noklikšķiniet uz Saistīt.
46. Koka struktūrā atlasiet 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.
47. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Uzņēmums: Virkne'.
48. Noklikšķiniet uz Saistīt.
49. Noklikšķiniet uz Saglabāt.
50. Aizvērt lapu.


