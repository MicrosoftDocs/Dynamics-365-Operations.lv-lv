---
title: Sinhronizēt datumu un laiku importa darbiem
description: Lai izvairītos no problēmām ar laika joslu pārveidošanām, importa darbiem izmantojiet UTC laika zonas.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570485"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Sinhronizēt datumu un laiku importa darbiem

[!include [banner](../includes/banner.md)]

Ir svarīgi iestatīt jūsu importa darba laika joslu uz universālo koordinēto laiku (UTC). Jūs variet redzēt negaidītus datumus un laikus jūsu importētos datos, ja izmantojat citu iestatījumu. Bez pareizā iestatījuma importēšanas process pārveido UTC datumu vietējā formātā un tad sistēmas iestatījumi to pārveido vēlreiz.

Šī dubultā pārveidošana rada datumu maiņu starp programmām. Piemēram, dubultā pārveidošana var radīt darbinieka sākuma datumu, kas var atšķirties no vietējo laika joslu atšķirībām Dynamics 365 Human Resources un Dynamics 365 Finance to dēļ. Iestatot importa darbu UTC, šī problēma tiek atrisināta.

1. Pakalpojumā Dynamics 365 Finance and Operations atlasiet **Datu pārvaldība**.

2. Atlasiet **Importēt projektus** un pēc tam atlasiet projektu.

3. Sadaļā **Avota datuma formāts** atlasiet **CSV-unikodu**.

   [![Mainīt avota datuma formātu uz UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Mainiet **Laika joslu** uz **Universālo koordinēto laika joslu** un nomainiet **Valodu** uz **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]