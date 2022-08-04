---
title: Sinhronizēt datumu un laiku importa darbiem
description: Lai izvairītos no problēmām ar laika joslu pārveidošanām, importa darbiem izmantojiet UTC laika zonas.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8faa7b73349c48d3a02b685546b47c4969c6027
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109438"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Sinhronizēt datumu un laiku importa darbiem

[!include [banner](../includes/banner.md)]

Ir svarīgi iestatīt jūsu importa darba laika joslu uz universālo koordinēto laiku (UTC). Jūs variet redzēt negaidītus datumus un laikus jūsu importētos datos, ja izmantojat citu iestatījumu. Bez pareizā iestatījuma importēšanas process pārveido UTC datumu vietējā formātā un tad sistēmas iestatījumi to pārveido vēlreiz.

Šī dubultā pārveidošana rada datumu maiņu starp programmām. Piemēram, dubultā pārveidošana var Dynamics 365 Human Resources radīt to, ka darbinieka sākuma datums no Dynamics 365 finanšu uz vēlāku datumu varētu atšķirties vietējo laika joslu atšķirību dēļ. Iestatot importa darbu UTC, šī problēma tiek atrisināta.

1. Programmā Dynamics 365 finanses un operācijas atlasiet **Datu pārvaldība**.

2. Atlasiet **Importēt projektus** un pēc tam atlasiet projektu.

3. Sadaļā **Avota datuma formāts** atlasiet **CSV-unikodu**.

   [![Mainīt avota datuma formātu uz UTC.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Mainiet **Laika joslu** uz **Universālo koordinēto laika joslu** un nomainiet **Valodu** uz **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

