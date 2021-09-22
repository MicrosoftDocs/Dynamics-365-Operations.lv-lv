---
title: Nevar atkārtoti izlaist daļēji nosūtītu kravu uz noliktavu
description: Agrākās versijās nevar atkārtoti izlaist daļēji nosūtītas kravas, ja izmantojat noteiktas funkcionalitātes ar nepilnīgām rezervācijām. Tas ir fiksēts.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477001"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Nevar atkārtoti izlaist daļēji nosūtītu kravu uz noliktavu

## <a name="symptoms"></a>Simptomi

Nevar izlaist daļēji nosūtītu kravu uz noliktavu. Kad veicat izlaišanu uz noliktavu, parādās ziņojums "Operācija pabeigta", bet nekas nenotiek, un atlikušajam daudzumam netiek izveidots neviens darbs. Šī problēma rodas, kad izmantojat transportēšanas noslodzes funkcionalitāti un ir nepilnīga rezervācija.

## <a name="resolution"></a>Novēršana

[KB problēma 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Daļēji nosūtītas kravas var atkārtoti ielikt kopumā un atkārtoti apstrādāt") ir fiksēta [laidienā 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
