---
title: Noslodzes aprēķināšana plānotajiem darba pasūtījumiem
description: Šajā rakstā ir izskaidrots, kā aprēķināt noslodzes grafiku plānotajiem darba pasūtījumiem Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857958"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Noslodzes aprēķināšana plānotajiem darba pasūtījumiem

[!include [banner](../../includes/banner.md)]

 

Varat aprēķināt noslodzi plānotajiem darbu pasūtījumiem, lai iegūtu pārskatu par resursu darba noslodzi konkrētam periodam. Aprēķinus var veikt šādiem resursiem: uzturēšanas speciālisti, strādnieku grupas un līdzekļi.

1. Klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Pieprasījumi** > **Noslodze**.

2. Dialoglodziņā **Aprēķināt noslodzi** laukā > **Parādīt** atlasiet, kādu noslodzes veidu vēlaties aprēķināt: **Noslodze**, **Rezervēts** vai **Atlikums**.

3. Pārslēgšanas pogā **Izlaist nulli** atlasiet **Jā**, ja nevēlaties, lai rāda rezultātus, kas satur nulli.

4. Atlasiet resursa veidus, kam vēlaties aprēķināt noslodzi, atlasot **Jā** attiecīgajās pārslēgšanas pogās: **Darbinieks**, **Uzturēšanas darbinieku grupa**, **Rīks** un **Līdzeklis**.

5. Laukā **No datums** atlasiet aprēķina sākuma datumu.

6. Laukā **Intervāla veids** atlasiet aprēķina intervālu: **Diena**, **Nedēļa**, **Mēnesis** vai **Ceturksnis**.

7. Laukā **Perioda biežums** ievadiet intervālu skaitu, ko vēlaties aprēķināt. Piemēram, ja izvēlaties kā intervāla veidu **Diena** un laukā ievadāt skaitli "5", tiks veikts aprēķins par piecām dienām no sākuma datuma.

8. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

Šajā attēlā parādīts aprēķina rezultāts par trim nedēļām noslodzes veidam **Rezervēts**.

![1. attēls.](media/08-work-order-scheduling.png)

[!NOTE]
Ja savam aprēķinam izvēlaties noslodzes veidus **Noslodze** vai **Atlikums**, tiks parādīts tas pats rezultāts, ja atlasītajā periodā resursiem nav veiktas rezervācijas.

Informāciju par noslodzes aprēķināšanu uzturēšanas grafika rindām un neieplānotu darba pasūtījumiem skatiet sadaļā [Noslodzes aprēķināšana](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]