---
title: Nederīga numura zīme vai atrašanās vietas kļūda mobilajā programmā
description: Skenējot numura zīmes ID vai atrašanās vietu, iespējams, saņemsit kļūdu, ka tā nav derīga. Pārliecinieties, ka numura zīmes ID nav rezervējis kas cits.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f9f10dbade0d13b8fc4b0fc92981d84e6e28e83e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477035"
---
# <a name="invalid-license-plate-or-location-error-when-scanning-in-the-mobile-app"></a>Nederīga numura zīme vai atrašanās vietas kļūda, veicot skenēšanu mobilajā programmā

## <a name="symptoms"></a>Simptomi

Skenējot numura zīmes ID vai atrašanās vietu, iespējams, saņemsit šādu kļūdas ziņojumu:

> Noliktavas vienība vai novietojums nav derīgs.

## <a name="resolution"></a>Novēršana

Pārliecinieties, ka numura zīmes ID nav rezervējis kas cits. Šī problēma parasti radās, kad vērtība, ko lietotājs skenēja Warehouse Management mobile lietotnē, bija gan derīga atrašanās vieta, gan derīgs numura zīmes ID. Tomēr šī problēma tika atrisināta versijā 10.0.11.
