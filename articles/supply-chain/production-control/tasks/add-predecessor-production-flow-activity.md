---
title: Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai
description: Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e64ad19c557c7b0fd8747bb9b748859e70eaa63a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149393"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai

[!include [banner](../../includes/banner.md)]

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

