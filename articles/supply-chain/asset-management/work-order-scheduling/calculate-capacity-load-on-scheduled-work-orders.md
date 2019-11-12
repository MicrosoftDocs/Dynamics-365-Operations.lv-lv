---
title: Noslodzes aprēķināšana plānotajiem darba pasūtījumiem
description: Šajā tēmā ir paskaidrots, kā aprēķināt noslodzi plānotajiem darba pasūtījumiem programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d7684d1a4f78c95ebc7fd0a88f1c7dc7fead0303
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652107"
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

![1. attēls](media/08-work-order-scheduling.png)

[!NOTE]
Ja savam aprēķinam izvēlaties noslodzes veidus **Noslodze** vai **Atlikums**, tiks parādīts tas pats rezultāts, ja atlasītajā periodā resursiem nav veiktas rezervācijas.

Informāciju par noslodzes aprēķināšanu uzturēšanas grafika rindām un neieplānotu darba pasūtījumiem skatiet sadaļā [Noslodzes aprēķināšana](../capacity-planning/calculate-capacity-load.md).

