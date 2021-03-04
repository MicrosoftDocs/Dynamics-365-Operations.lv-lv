---
title: Prognozēšanas modeļa uzlabošana (priekšskatījums)
description: Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646083"
---
# <a name="improve-the-prediction-model-preview"></a>Prognozēšanas modeļa uzlabošana (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai. Jūs sākat uzlabot savu modeli **Klientu maksājumu prognožu** darbvietā programmā Microsoft Dynamics 365 Finance. Tad uzlabojumu darbības tiek pabeigtas AI Builder.

## <a name="select-historical-outcomes"></a>Vēsturisko iznākumu atlasīšana

Vispirms atlasiet vienu vai vairākus no trim iespējamiem iznākumiem rēķiniem: **Laicīgi**, **Novēloti** un **Ļoti novēloti**. Jāatlasa visi trīs rezultāti. Notīrot kāda rezultāta atlasi, rēķini tiks filtrēti no apmācības procesa, un prognozes precizitāte tiks samazināta.

[![Iznāķumu apstiprināšana](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Ja jūsu organizācijai nepieciešami tikai divi iznākumi, mainiet **Novēloti** un **Ļoti novēloti** slieksni uz 0 (nulle) dienām. Šādā veidā jūs efektīvi sakļaujat prognozes binārajā stāvoklī ar **Laicīgi** vai **Novēloti**.

## <a name="select-fields"></a>Atlasiet pārskata laukus

Kad atlasāt laukus iekļaušanai modelī, ņemiet vērā, ka sarakstā ir iekļauti visi pieejamie lauki elementā Common Data Service, kas ir kartēts Azure datu ezera datos. Dažus no šiem laukiem **nedrīkst** atlasīt. Lauki, kas nav jāatlasa, ietilpst vienā no trijām kategorijām:

- Šis lauks ir nepieciešams Common Data Service elementam, bet datu ezerā tam nav datu dublēšanas datu.
- Lauks ir ID un tādēļ nav jēgas izmantot algoritmiskās mācīšanās līdzekli.
- Lauks ataino informāciju, kas nebūs pieejama prognozēšanas laikā.

Šajās sadaļās ir redzami lauki, kas ir pieejami rēķina un klienta elementiem, un uzskaitīti lauki, kas **nav** jāatlasa apmācībai. Kategorija, kas norādīta katram no šiem laukiem, attiecas uz kategorijām iepriekšējā sarakstā.
 
### <a name="invoice-common-data-model-entity"></a>Rēķina Common Data Model elements

Nākamajā attēlā ir parādīti avoti, kas ir pieejami rēķina elementam.

[![Rēķina elementam pieejamie lauki](./media/available-fields.png)](./media/available-fields.png)

Apmācībām nav jāatlasa tālāk minētie lauki.

- **Rēķina konts** (2. kategorija)
- **Ir slēgts** (3. kategorija) — šis lauks tiek izmantots, lai filtrētu rēķinus apmācībām (slēgts) un prognozēšanai (nav slēgts).
- **Nosaukums** (1. kategorija)
- **Avota ID** (2. kategorija)
- **Avota ieraksts** (2. kategorija)
- **Avota tabula** (2. kategorija)

### <a name="customer-common-data-model-entity"></a>Debitora Common Data Model elements

Nākamajā attēlā ir parādīti avoti, kas ir pieejami debitora elementam.

[![Debitora elementam pieejamie lauki](./media/related-entities.png)](./media/related-entities.png)

Apmācībām nav jāatlasa tālāk minētais lauks.

- **Unikālā rindas atslēga** (2. kategorija)

## <a name="filters"></a>Filtri

Filtri pašlaik neatbalsta debitoru maksājumu prognozēšanas scenāriju. Tāpēc atlasiet **Izlaist šo darbību** un pārejiet uz kopsavilkuma lapu.

[![Fokusa režīms ar filtriem](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]