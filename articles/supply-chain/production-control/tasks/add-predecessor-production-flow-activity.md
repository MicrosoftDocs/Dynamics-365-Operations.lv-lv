--- 
title: "Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai"
description: "Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā. Aktivitāte var ietvert vienu vai vairākas pirmstecīgas vai pēctecīgas aktivitātes. 

Šajā procedūrā ir aprakstīts, kā saistīt pirmstecīgu aktivitāti ar aktivitāti. 

Lai veiktu šo uzdevumu jums ir nepieciešama ražošanas plūsma, kurai ir pieejama melnraksta versija ar vismaz divām aktivitātēm, kuras var pievienot. 

Lai uzzinātu vairāk, izlasiet rakstu krājumu “Lean manufacturing ražošanas plūsmas un aktivitātes”.


## <a name="find-the-production-flow-and-version"></a>Meklēt ražošanas plūsmu un versiju
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Noklikšķiniet uz Aktivitātes.

## <a name="select-an-activity-and-add-a-predecessor"></a>Atlasīt aktivitāti un pievienot pirmstecīgu aktivitāti
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
2. Noklikšķiniet uz Pievienot pirmstecīgu aktivitāti.
3. Ievadiet vai atlasiet vērtību laukā Aktivitāte.
4. Laukā Cikla laika koeficients ievadiet skaitli.
    * Aktivitāšu relācijas noklusējuma cikla laika koeficients ir 1. Tiek pieņemts, ka abas aktivitātes tiek sāktas ar vienādu tempu vai izgatavošanas laiku. Ja pirmstecīgā aktivitāte tiek izpildīta ātrāk (īsāks izgatavošanas laiks), koeficientam ir jābūt zemākam par 1; ja pirmstecīgā aktivitāte tiek izpildīta ar lēnāk (lielāks izgatavošanas laiks) cikla laika koeficients ir lielāks par 1.  
5. Noklikšķiniet uz OK.


