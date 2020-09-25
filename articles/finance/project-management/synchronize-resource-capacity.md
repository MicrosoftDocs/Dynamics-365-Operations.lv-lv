---
title: Sinhronizēt resursu noslodzi
description: Šī tēma sniedz informāciju par to, kā sinhronizēt resursa noslodzi kalendāros un projektos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760602"
---
# <a name="synchronize-resource-capacity"></a>Sinhronizēt resursu noslodzi

[!include [banner](../includes/banner.md)]

Resursu sinhronizēšanas process palīdz nodrošināt to, ka informācija kalendāram un pamatkalendāram nokļūst projekta resursu plānošanā. Ja kalendārs tiek mainīts, procesi veic nepieciešamos atjauninājumus projekta resursu plānošanai. Šie procesi arī palīdz uzlabot veiktspēju, jo kalendāra resursu informācija tiek sinhronizēta jau iepriekš. Tāpēc resursu plānošanas informācijas atjauninājumi notiek ātrāk. Procesu plānošanu ieteicams veikt kā pakešuzdevumu, nevis atsevišķi katram procesam. Pretējā gadījumā pastāv risks, ka kāds aizmirsīs ietvertos datumus, kad pēdējo reizi tika sinhronizēta informācija. Ja netiek izmantoti ietvertie datumi, datu sinhronizācijas laikā var rasties pārrāvumi.

![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizēt resursu noslodzes apkopojumus

Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursu kalendāra informāciju. Šajā informācijā ir ietverta pamatkalendāra informācija par visām izmaiņām projekta resursu kalendāra noslodzes tabulā. Ja projektā tiek pievienoti jauni resursi, sinhronizācija palīdz garantēt to, ka ir pieejama atjaunināta kalendāra informācija. Šo sinhronizāciju var veikt jebkurā laikā.

Ieteicams izmantot partijas. Opcijas ir pieejamas noslodzes rezervāciju sinhronizēšanas laikā.

1. Atlasiet **Projektu vadība un uzskaite** &gt; **Periodisks** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.
2. Iestatiet opcijas nākamajā tabulā.

    | Opcija      | Apraksts |
    |-------------|-------------|
    | Perioda kods | Ja vēlaties, atlasiet virsgrāmatas datumu intervāla kodu, lai resursu noslodzes apkopojumu sinhronizācijas procesam iestatītu sākuma un beigu datumus. |
    | Sākuma datums  | Ievadiet resursu noslodzes apkopojumu sinhronizācijas procesa sākuma datumu. |
    | Beigu datums    | Ievadiet resursu noslodzes apkopojumu sinhronizācijas procesa beigu datumu. |

[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
