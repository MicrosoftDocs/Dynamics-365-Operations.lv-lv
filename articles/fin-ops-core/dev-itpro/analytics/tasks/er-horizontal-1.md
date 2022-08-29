---
title: ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (1. daļa. Formāta noformēšana)
description: Šajā rakstā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus kā OPENXML darblapas (Excel) failus. (1. daļa)
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: 3fa8dcac309220d05225e87fd29ef6b741bfcc54
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290430"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (1. daļa. Formāta noformēšana)

[!include [banner](../../includes/banner.md)]

Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes. Šīs darbības var veikt jebkurā uzņēmumā.

Lai veiktu šīs darbības, vispirms veiciet tālāk aprakstītās trīs norādes par uzdevumu:

"ER: Konfigurācijas nodrošinātāja izveide un atzīmēšana kā aktīvu"

"ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa: Datu modeļa noformēšana)"

"ER finanšu dimensijas, kuras izmanto kā datu avotu (2. daļa: Modeļa kartēšana)"

Ir nepieciešams arī lejupielādēt un saglabāt veidnes ar pārskata paraugu lokālu kopiju, kas pieejama šeit: [Finanšu dimensijas parauga tīmekļa pakalpojuma pārskats](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

## <a name="create-a-new-report-configuration"></a>Izveidot jaunu pārskata konfigurāciju

1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā atlasiet `Financial dimensions sample model`.
3. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
4. Laukā Jauns ievadiet `Format based on data model Financial dimensions sample model`.
    * Izmantojiet iepriekš izveidoto modeli kā jaunā pārskata datu avotu.  
5. Laukā Nosaukums ierakstiet `Sample report with horizontally expandable ranges`.
    * Izveidot pārskata paraugu ar horizontāli paplašināmiem diapazoniem  
6. Laukā Apraksts ievadiet `To make Excel output with dynamically adding columns`.
    * Lai sagatavotu Excel izvadi ar dinamisku kolonnu pievienošanu  
7. Laukā Datu modeļa definīcija atlasiet Ieraksts.
8. Klikšķiniet Izveidot konfigurāciju.

## <a name="design-the-report-format"></a>Izstrādāt pārskata formātu

1. Noklikšķiniet uz Veidotājs.
2. Ieslēdziet pārslēgšanas pogu `Show details`.
3. Darbību rūtī noklikšķiniet uz Importēt.
4. Noklikšķiniet uz Importēt no Excel.
5. Noklikšķiniet uz Pielikumi.
    * Importējiet pārskata veidni. Šajā nolūka izmantojiet lejupielādēto Excel failu.  
6. Klikšķiniet Jauns.
7. Noklikšķiniet uz Fails.
8. Aizvērt lapu.
9. Ievadiet vai atlasiet kādu vērtību laukā Veidne.
    * Atlasiet lejupielādējamo veidni.  
10. Noklikšķiniet uz OK.
    * Pievienot jaunu diapazonu, lai dinamiski izveidotu finanšu dimensiju Excel izvadi ar visu atlasīto kolonnu skaitu (lietotāja dialoglodziņa veidlapā). Visu kolonnu visās šūnās ir norādīts atsevišķs finanšu dimensijas nosaukums.  
11. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
12. Kokā atlasiet `Excel\Range`.
13. Laukā Excel diapazons ierakstiet `DimNames`.
    * DimNames  
14. Laukā Replicēšanas virziens atlasiet `Horizontal`.
15. Noklikšķiniet uz Labi.
16. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. Noklikšķiniet uz Pārvietot uz augšu.
18. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. Noklikšķiniet uz Izgriezt.
20. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. Noklikšķiniet uz Ielīmēt.
22. Kokā izvērsiet `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. Kokā izvērsiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. Kokā izvērsiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * Pievienot jaunu diapazonu, lai dinamiski izveidotu finanšu dimensiju Excel izvadi ar visu atlasīto kolonnu skaitu (lietotāja dialoglodziņa veidlapā). Visu kolonnu visās šūnās ir norādīta atsevišķa finanšu dimensijas vērtība visām pārskata transakcijām.  
26. Noklikšķiniet uz Pievienot diapazonu.
27. Laukā Excel diapazons ierakstiet `DimValues`.
    * DimValues  
28. Laukā Replicēšanas virziens atlasiet `Horizontal`.
29. Noklikšķiniet uz Labi.
30. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. Noklikšķiniet uz Izgriezt.
32. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. Noklikšķiniet uz Ielīmēt.
34. Kokā izvērsiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>Saistīt formātā elementus ar datu avotiem

1. Noklikšķiniet uz cilnes Kartēšana.
2. Kokā izvērsiet `model: Data model Financial dimensions sample model`.
3. Kokā izvērsiet `model: Data model Financial dimensions sample model\Journal: Record list`.
4. Kokā izvērsiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. Kokā izvērsiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. Noklikšķiniet uz Saistīt.
9. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. Noklikšķiniet uz Saistīt.
12. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. Noklikšķiniet uz Saistīt.
15. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. Noklikšķiniet uz Saistīt.
18. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. Noklikšķiniet uz Saistīt.
21. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. Noklikšķiniet uz Saistīt.
24. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. Noklikšķiniet uz Saistīt.
27. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. Noklikšķiniet uz Saistīt.
30. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. Noklikšķiniet uz Saistīt.
33. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. Noklikšķiniet uz Saistīt.
36. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. Kokā atlasiet `model: Data model Financial dimensions sample model\Journal: Record list`.
38. Noklikšķiniet uz Saistīt.
39. Kokā izvērsiet `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. Kokā atlasiet `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. Noklikšķiniet uz Saistīt.
43. Kokā atlasiet `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. Noklikšķiniet uz Saistīt.
46. Kokā atlasiet `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. Kokā atlasiet `model: Data model Financial dimensions sample model\Company: String`.
48. Noklikšķiniet uz Saistīt.
49. Noklikšķiniet uz Saglabāt.
50. Aizvērt lapu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
