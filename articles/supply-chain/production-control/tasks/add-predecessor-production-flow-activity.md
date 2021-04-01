---
title: Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai
description: Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d76ec6ac928228011f42355bebd553576bcfd275
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255449"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]