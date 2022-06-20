---
title: Prognozēšanas modeļa uzlabošana
description: Šajā rakstā ir aprakstītas funkcijas, kuras var izmantot, lai uzlabotu prognozēšanas modeļu veiktspēju.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: cb725f4e8f7b9dd81077f5c85059a024f3146092
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846891"
---
# <a name="improve-the-prediction-model"></a>Prognozēšanas modeļa uzlabošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas funkcijas, kuras var izmantot, lai uzlabotu prognozēšanas modeļu veiktspēju. Jūs sākat uzlabot savu modeli debitoru maksājumu **prognozēšanas darbvietā** Microsoft Dynamics 365 Finansēs. Pēc tam tiek pabeigti uzlabojuma soļi AI Builder.

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

Papildinformāciju par datu filtrēšanu skatiet sadaļā [Prognozēšanas modeļa izveide](/ai-builder/prediction-create-model#filter-your-data).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
