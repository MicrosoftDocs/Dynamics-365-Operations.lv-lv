---
title: Pārdošanas atjauninājumu vēstures tīrīšanas darbs neizdodas vai tam ir veiktspējas problēmas
description: Pārdošanas vēstures tīrīšanas pakešuzdevums var neizdoties vai aizņemt ļoti ilgu laiku, ja ir liels pārdošanas atjauninājumu datu apjoms.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570345"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Pārdošanas atjauninājumu vēstures tīrīšanas darbs neizdodas vai tam ir veiktspējas problēmas

## <a name="symptoms"></a>Simptomi

**Pārdošanas atjauninājumu vēstures tīrīšanas** pakešuzdevums neizdodas vai tam ir veiktspējas problēmas.  

## <a name="cause"></a>Iemesls

Tas var notikt, kad sistēma ietver lielu skaitu pārdošanas atjauninājumu, kas var radīt lielu daudzumu pārdošanas atjauninājumu datu. Tīrīšanas darbs mēģina notīrīt visus šos datus ar vienu darbību. Tā rezultātā darbs var aizņemt ļoti ilgu laiku, lai to izpildītu, vai tas var neizdoties.

## <a name="resolution"></a>Novēršana

Jauna versija **Pārdošanas atjauninājumu vēstures tīrīšanas** pakešuzdevumam ir pieejama Supply Chain Management versijai 10.0.19 un jaunākām. Šis līdzeklis pēc noklusējuma nav ieslēgts. Detalizētu informāciju par to, kā tas darbojas un kā to iespējot līdzekļu pārvaldībā, skatiet rakstā [Pārdošanas vēstures datu tīrīšanas plānošana](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

