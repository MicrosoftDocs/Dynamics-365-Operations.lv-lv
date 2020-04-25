---
title: Kanban daudzuma aprēķināšanas ierobežojuma pievienošana Kanban kārtulai
description: Šajā procedūrā parādīts, kā izveidot Kanban daudzuma aprēķināšanas politiku un pievienot Kanban nosacījumu, lai optimizētu Kanban lielumu un daudzumus.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19f563379a10bbe42681a5f61779fb9e72d1f60c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211012"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban daudzuma aprēķināšanas ierobežojuma pievienošana Kanban kārtulai

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot Kanban daudzuma aprēķināšanas politiku un pievienot Kanban nosacījumu, lai optimizētu Kanban lielumu un daudzumus. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta vērtību plūsmas pārvaldniekam. Šī procedūra ir nepieciešama, lai izveidotu procedūru Aprēķināt Kanban daudzuma ieteikumus. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Kanban daudzuma aprēķina politikas izveide
1. Pārejiet uz sadaļu Ražošanas kontrole > Periodiskie uzdevumi > Kanban daudzuma aprēķins > Kanban daudzuma aprēķinu politikas.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
    * Piemēram, ierakstiet Speaker2016.  
4. Laukā Vispārējais plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet StaticPlan, lai aprēķinātu pieprasījumu.  
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz Saglabāt.
8. Laukā Minimālais Kanban daudzums ievadiet "1".
    * Šis ir Kanban papildu skaits, ko lieto Kanban daudzuma aprēķināšanai.  
9. Iestatiet vērtību "1" laukā Drošības koeficients.
    * Šis ir faktors, kas tiek izmantots, lai aprēķinātu papildu drošības krājumu daudzumu.  
10. Laukā Dienas uz priekšu ievadiet “30”.
    * Šis ir dienu skaits pirms Kanban daudzuma aprēķināšanas datuma, kas iekļauts pieprasījuma aprēķināšanā.  
11. Laukā Dienas aiz muguras ievadiet “30”.
    * Šis ir dienu skaits uz priekšu, skaitot no Kanban daudzuma aprēķināšanas datuma, kas iekļauts pieprasījuma aprēķināšanā.  Aprēķināšanai izmantotā formula ir redzama ar faktiskajām vērtībām. Piemēram, Kanban daudzums = ((vidējais dienas pieprasījums x izpildes laiks x 2) / preču daudzums uz materiālu apstrādes vienību) + 1  
12. Aizvērt lapu.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban daudzuma aprēķināšanas politikas pievienošana Kanban nosacījumam
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Šai procedūrai atlasiet Kanban nosacījumu 000020.  
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Pārslēdziet sadaļas Kanban daudzuma aprēķinu politikas paplašinājumu.
5. Noklikšķiniet uz Pievienot.
    * Pievienojiet Kanban daudzuma aprēķināšanas politiku, kuru izveidojāt iepriekšējā apakšuzdevumā.  
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet politiku Speaker2016, kuru izveidojāt iepriekšējā apakšuzdevumā.  

