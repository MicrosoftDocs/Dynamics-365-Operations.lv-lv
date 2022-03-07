---
title: Atgriezeniskās izmaksu aprēķināšanas kļūda krājuma slēgšanas laikā
description: Agrākajos laidienos, iespējams, krājuma slēgšanas laikā saņēmāt atgriezeniskās izmaksu aprēķināšanas kļūdu. Šī problēma ir atrisināta.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476969"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Atgriezeniskās izmaksu aprēķināšanas kļūda krājuma slēgšanas laikā

## <a name="symptoms"></a>Simptomi

Laidienos pirms 10.0.13 izlaiduma, ja neizmantojat taupīgo ražošanas izmaksu plūsmu, krājuma slēgšanas laikā saņemat šādu kļūdainu brīdinājuma ziņojumu:

> Jūs gatavojaties izpildīt Krājumu slēgšanu ar datumu %1. Nav reģistrēta neviena Atgriezeniska izmaksu aprēķināšana ar datumu %1 salīdzināšanas perioda beigas. Lūdzu atceraties veikt Atgriezenisko izmaksu aprēķināšanu ar datumu %1 salīdzināšanas perioda beigas. Krājumu vērtība, pārdoto preču cena un novirzes varētu nebūt pareizas apakšgrāmatā vai virsgrāmatā, līdz tas tiek izpildīts.

## <a name="resolution"></a>Novēršana

Šī problēma ir novērsta, 10.0.13 laidienā un jaunākos. Papildinformāciju skatiet [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
