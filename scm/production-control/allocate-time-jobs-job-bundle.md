---
title: "Piešķirt laiku darbu komplektā iekļautiem darbiem"
description: "Lapā Ražošanas izpilde var veikt darbu komplektēšanu. Pēc tam lapā Darbu saraksts var sākt vairākus darbus vienlaicīgi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a7d824048c37b69240385644eb15514918f17d9e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Piešķirt laiku darbu komplektā iekļautiem darbiem

[!include[banner](../includes/banner.md)]


Lapā Ražošanas izpilde var veikt darbu komplektēšanu. Pēc tam lapā Darbu saraksts var sākt vairākus darbus vienlaicīgi.

Kārtojot darbus komplektā, jānosaka, kā katram darbam iedalīt kopumā visiem darbiem reģistrēto laiku. Lai noteiktu sadalījumu, atlasiet vienu no tālāk norādītajām opcijām lapas **Sadalījuma atslēgas** laukā **Komplekta veids**.

-   **Aprēķins** — laiks tiek sadalīts starp darbiem atbilstoši darbiem aprēķinātajam laikam.
-   **Darbi** — laiks tiek sadalīts atbilstoši visiem komplektā iekļautajiem darbiem un kopumā visu darbu pabeigšanai patērētajam laikam.
-   **Neto laiks** — laiks ir sadalīts vienādi starp komplektā jebkurā laikā iekļautajiem darbiem.
-   **Reālais laiks** — tiek iedalīts faktiskais darba laiks. Izmaksas var aprēķināt saskaņā ar faktiskajām algu izmaksām. **Piezīme.** Sadalījuma atslēga **Reālais laiks** ir pieejama tikai tad, ja uzņēmums izmanto algu funkcionalitāti lapā Laiks un apmeklējums.

Nākamajos piemēros ir aprakstīti dažādu sadalījuma atslēgu izmantošanas rezultāti.

## <a name="example-scenario"></a>Piemēra situācija
Jāizpilda trīs darbu rindā iekļauti darbi. Jūs sākat pirmo darbu un pēc tam, nepabeidzot šo darbu, sākat otro un trešo darbu. Tādējādi veidojas trīs darbu komplekts. Nākamajā tabulā ir sniegts katra darba izpildes laika aprēķins.

| Darbs   | Ražošanas laiks |
|-------|-----------------|
| 1. darbs | 1 stunda          |
| 2. darbs | 3 stundas         |
| 3. darbs | 4 stundas         |
| KOPĀ | 8 stundas         |

Tabulā ir redzama informācija par katram darbam patērētajām darba stundām.

| Darbs    | Sākuma laiks | Beigu laiks | Saišķa laiks |
|--------|------------|----------|-------------|
| 1. darbs  | 9.00      | 11.00    | 2 stundas     |
| 2. darbs  | 10.00      | 13.00    | 3 stundas     |
| 3. darbs  | 10.00      | 15.00    | 5 stundas     |
| Komplekts | 9.00      | 15.00    | 6 stundas     |

Nākamajās sadaļās ir aprakstīti katrai sadalījuma atslēgai aprēķinātā laika rezultāti.

## <a name="estimation-allocation-key"></a>Novērtējuma sadalījuma atslēga
Nākamajā tabulā ir redzama iedalītā laika aprēķināšanas formula. Formula ir šāda: vienam darbam nepieciešamais laiks = kopējais komplekta laiks x (aprēķinātais darba laiks ÷ kopējais aprēķinātais laiks)

| Darbs   | Formula           | Piešķirtais laiks |
|-------|-------------------|----------------|
| 1. darbs | 6 × (1 ÷ 8) stundas | 0,75 stundas      |
| 2. darbs | 6 × (3 ÷ 8) stundas | 2,25 stundas     |
| 3. darbs | 6 × (4 ÷ 8) stundas | 3,00 stundas     |

## <a name="jobs-allocation-key"></a>Darbu sadalījuma atslēga
Nākamajā tabulā ir redzama iedalītā laika aprēķināšanas formula. Formula ir šāda: vienam darbam nepieciešamais laiks = kopējais komplekta laiks x darbu skaits

| Darbs   | Formula | Piešķirtais laiks |
|-------|---------|----------------|
| 1. darbs | 6 ÷ 3   | 2 stundas        |
| 2. darbs | 6 ÷ 3   | 2 stundas        |
| 3. darbs | 6 ÷ 3   | 2 stundas        |

## <a name="net-time-allocation-key"></a>Neto laika sadalījuma atslēga
Nākamajā tabulā ir redzama iedalītā laika aprēķināšanas formula. Formula ir šāda: vienā pārskatā aprēķinātais laiks = komplekta laiks ÷ darbu skaits

|                              | 09:00–10:00 (1 stunda) | 10:00–11:00 (1 stunda) | 11:00–13:00 (2 stundas) | 13:00–15:00 (2 stundas) | Piešķirtais laiks |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Darbu skaits komplektā | 1                    | 3                    | 2                     | 1                     | Nav attiecināms |
| 1. darbs                        | 1 ÷ 1 = 1 stunda       | 1 ÷ 3 = 0,33 stundas    | Nav attiecināms        | Nav attiecināms        | 1,33 stundas     |
| 2. darbs                        | Nav attiecināms       | 1 ÷ 3 = 0,33 stundas    | 2 ÷ 2 = 1 stunda        | Nav attiecināms        | 1,33 stundas     |
| 3. darbs                        | Nav attiecināms       | 1 ÷ 3 = 0,33 stundas    | 2 ÷ 2 = 1 stunda        | 2 ÷ 1 = 2 stundas       | 3,33 stundas     |

## <a name="real-time-allocation-key"></a>Reāllaika sadalījuma atslēga
Ja vēlaties ražošanas izmaksas aprēķināt atbilstoši reālajām izmaksām, jānoņem opcijas **Izmaksu kategorija** atlase lapā **Ražošanas pasūtījumu noklusējuma iestatījumi**. Nākamajā tabulā ir redzama iedalītā laika aprēķināšanas formula. Formula ir šāda: vienam darbam faktiski patērētais laiks = komplekta darbiem faktiski patērētais laiks

| Darbs   | Faktiskais laiks |
|-------|-------------|
| 1. darbs | 2 stundas     |
| 2. darbs | 3 stundas     |
| 3. darbs | 5 stundas     |

Ņemiet vērā strādnieka, kam stundas likme ir 12,00 USD, veiktos trīs darbus. Šo darbu izpildei patērētajā laikā netika nopelnīta virsstundu apmaksa vai prēmija. Darbinieks šo trīs komplekta darbu izpildei kopumā patērēja sešas stundas. Tātad algas izmaksas ir šādas: 6 x 12,00 USD = 72,00 USD. Izmantojot reālā laika sadalījumu, vienas stundas izmaksas tiek pārrēķinātas, izmantojot neto laika formulas koeficientu. Katram darbam patērētais faktiskais laiks pēc tam tiek pārnests kopā ar pareizo izmaksu cenu stundā. Piemēram, darbam ir patērētas sešas stundas, kaut iedalītas tika 10 stundas. Nākamajā tabulā ir redzama izmaksu aprēķināšanas formula. Formula ir šāda: vienas stundas izmaksas = (kopējais komplekta laiks uz vienu darbu (neto laiks) ÷ vienam darbam faktiski patērētais laiks) x vienas stundas standarta izmaksu cena

| Darbs   | Koriģēto izmaksu aprēķins stundā | Koriģētās izmaksas stundā | Piešķirtais laiks | Kopējās darba izmaksas |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| 1. darbs | (1,33 ÷ 2) × 12,00 USD                 | USD 8,00                | 2 stundas        | USD 16,00         |
| 2. darbs | (1,33 ÷ 3) × 12,00 USD                 | USD 5,33                | 3 stundas        | USD 16,00         |
| 3. darbs | (3,33 ÷ 5) × 12,00 USD                 | USD 8,00                | 5 stundas        | USD 40,00         |

Koriģētās vienas stundas izmaksas un darba laiks tiek iegrāmatots ražošanas žurnālā. **Piezīme.** Ja lapā **Ražošanas pasūtījumu noklusējuma iestatījumi** ir atzīmēta cilnes **Vispārīgi** opcija **Izmaksu kategorija**, katram darbam faktiski patērētais laiks tiek pārnests ražošanas žurnālā, kur izmaksas tiek attiecinātas uz konkrēta darba izmaksu kategoriju.




