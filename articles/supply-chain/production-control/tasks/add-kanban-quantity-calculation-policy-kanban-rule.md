---
title: Kanban daudzuma aprēķināšanas ierobežojuma pievienošana Kanban kārtulai
description: Šajā procedūrā parādīts, kā izveidot Kanban daudzuma aprēķināšanas politiku un pievienot Kanban nosacījumu, lai optimizētu Kanban lielumu un daudzumus.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a844d455b1e583f234ddc47280f5cac8ee0ab852
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579284"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]