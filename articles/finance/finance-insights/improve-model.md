---
title: Prognozēšanas modeļa uzlabošana (priekšskatījums)
description: Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 74005d17e2524b922b0fab1aab5350b85dfad771
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355680"
---
# <a name="improve-the-prediction-model-preview"></a>Prognozēšanas modeļa uzlabošana (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai. Jūs sākat uzlabot savu modeli **Klientu maksājumu prognožu** darbvietā programmā Microsoft Dynamics 365 Finance. Tad uzlabojumu darbības tiek pabeigtas AI Builder.

## <a name="select-historical-outcomes"></a>Vēsturisko iznākumu atlasīšana

Vispirms atlasiet vienu vai vairākus no trim iespējamiem iznākumiem rēķiniem: **Laicīgi**, **Novēloti** un **Ļoti novēloti**. Jāatlasa visi trīs rezultāti. Notīrot kāda rezultāta atlasi, rēķini tiks filtrēti no apmācības procesa, un prognozes precizitāte tiks samazināta.

[![Iznāķumu apstiprināšana.](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Ja jūsu organizācijai nepieciešami tikai divi iznākumi, mainiet **Novēloti** un **Ļoti novēloti** slieksni uz 0 (nulle) dienām. Šādā veidā jūs efektīvi sakļaujat prognozes binārajā stāvoklī ar **Laicīgi** vai **Novēloti**.

## <a name="select-fields"></a>Atlasiet pārskata laukus

Kad atlasāt laukus iekļaušanai modelī, ņemiet vērā, ka sarakstā ir iekļauti visi pieejamie lauki Microsoft Dataverse tabulā, kas ir kartēts Azure datu ezera datos. Dažus no šiem laukiem **nedrīkst** atlasīt. Lauki, kas nav jāatlasa, ietilpst vienā no trijām kategorijām:

- Šis lauks ir nepieciešams Dataverse tabulai, bet datu ezerā tam nav datu dublēšanas datu.
- Lauks ir ID un tādēļ nav jēgas izmantot algoritmiskās mācīšanās līdzekli.
- Lauks ataino informāciju, kas nebūs pieejama prognozēšanas laikā.

Šajās sadaļās ir redzami lauki, kas ir pieejami rēķina un klienta elementiem, un uzskaitīti lauki, kas **nav** jāatlasa apmācībai. Kategorija, kas norādīta katram no šiem laukiem, attiecas uz kategorijām iepriekšējā sarakstā.
 
### <a name="invoice-dataverse-table"></a>Rēķinu Dataverse tabula

Nākamajā attēlā ir parādīti avoti, kas ir pieejami rēķina tabulai.

[![Rēķina tabulai pieejamie lauki.](./media/available-fields.png)](./media/available-fields.png)

Apmācībām nav jāatlasa tālāk minētie lauki.

- **Rēķina konts** (2. kategorija)
- **Ir slēgts** (3. kategorija) — šis lauks tiek izmantots, lai filtrētu rēķinus apmācībām (slēgts) un prognozēšanai (nav slēgts).
- **Nosaukums** (1. kategorija)
- **Avota ID** (2. kategorija)
- **Avota ieraksts** (2. kategorija)
- **Avota tabula** (2. kategorija)

### <a name="customer-dataverse-table"></a>Debitoru Dataverse tabula

Nākamajā attēlā ir parādīti avoti, kas ir pieejami debitora tabulai.

[![Debitora tabulai pieejamie lauki.](./media/related-entities.png)](./media/related-entities.png)

Apmācībām nav jāatlasa tālāk minētais lauks.

- **Unikālā rindas atslēga** (2. kategorija)

## <a name="filters"></a>Filtri

Varat filtrēt rēķinus, kas tiek izmantoti apmācībai, iestatot filtra kritērijus laukiem rēķinā vai debitoru tabulās. Piemēram, varat iestatīt slieksni, lai iekļautu tikai tos rēķinus, kuru kopsumma ir vienāda ar noteikto summu vai pārsniedz to. Alternatīvi jūs varat izslēgt rēķinus, kas ir saistīti ar klientiem noteiktā debitoru grupā.

Papildinformāciju par datu filtrēšanu skatiet sadaļā [Prognozēšanas modeļa izveide](https://docs.microsoft.com/ai-builder/prediction-create-model#filter-your-data).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
