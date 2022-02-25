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
ms.openlocfilehash: 371a8c7178cd7c5091d6dd9a91d0ee03b943a269
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103192"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Pārdošanas atjauninājumu vēstures tīrīšanas darbs neizdodas vai tam ir veiktspējas problēmas

## <a name="symptoms"></a>Simptomi

**Pārdošanas atjauninājumu vēstures tīrīšanas** pakešuzdevums neizdodas vai tam ir veiktspējas problēmas.  

## <a name="cause"></a>Iemesls

Tas var notikt, kad sistēma ietver lielu skaitu pārdošanas atjauninājumu, kas var radīt lielu daudzumu pārdošanas atjauninājumu datu. Tīrīšanas darbs mēģina notīrīt visus šos datus ar vienu darbību. Tā rezultātā darbs var aizņemt ļoti ilgu laiku, lai to izpildītu, vai tas var neizdoties.

## <a name="resolution"></a>Novēršana

Jauna versija **Pārdošanas atjauninājumu vēstures tīrīšanas** pakešuzdevumam ir pieejama Supply Chain Management versijai 10.0.19 un jaunākām. Šis līdzeklis nav ieslēgts pēc noklusējuma. Detalizētu informāciju par to, kā tā darbojas un kā to iespējot līdzekļu pārvaldībā, skatiet pārdošanas [vēstures tīrīšanas veiktspējas uzlabojumi](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

