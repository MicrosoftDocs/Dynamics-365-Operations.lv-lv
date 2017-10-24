--- 
title: "Finanšu dimensiju definēšana"
description: "Šajā uzdevumu ceļvedī parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b72acf763f0f6dbc64c3e00986bc9eb0e366bb5
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="define-financial-dimensions"></a>Finanšu dimensiju definēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumu ceļvedī parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju.  Ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Uz elementu balstītas finanšu dimensijas izveide
1. Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas.
2. Noklikšķiniet uz Jauns.
3. Laukā Lietotāja vērtības no atlasiet sistēmas definētu elementu, uz kuru balstīt finanšu dimensiju. 
4. Laukā Dimensijas nosaukums ievadiet vērtību, lai aprakstītu finanšu dimensiju.
    * Nosaukums var atšķirties no sistēmas definētā elementa nosaukuma, bet nedrīkst saturēt atstarpes vai īpašas rakstzīmes.  
5. Noklikšķiniet uz Aktivizēt.
    * Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas. Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.  
6. Aktivizācijas paziņojumā noklikšķiniet uz Aizvērt.
7. Noklikšķiniet uz Aktivizēt.
    * Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.  
8. Noklikšķiniet uz Dimensiju vērtības.
    * Dažas dimensijas vērtības attiecas tikai uz konkrētu uzņēmumu. Jūs varat pārliecināties, vai tās attiecas tikai uz konkrētu uzņēmumu, pārbaudot, vai uzņēmuma nosaukums parādās dimensiju vērtību sarakstā.  

## <a name="create-a-custom-financial-dimension"></a>Pielāgotās finanšu dimensijas izveide
1. Aizvērt lapu.
2. Noklikšķiniet uz Jauns.
3. Laukā "Izmantot vērtības no" atlasiet <Custom dimension>.
4. Laukā Dimensijas nosaukums ievadiet vērtību, lai aprakstītu finanšu dimensiju.
    * Nosaukumā nedrīkst būt atstarpes vai īpašas rakstzīmes.  
    * Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku.   
    * Jūs varat ievadīt rakstzīmes, kas paliek vienādas katrai dimensijas vērtībai, piemēram, burtus vai pārnesumzīmi. Varat arī ievadīt numura zīmes (#) un zīmes & kā vietturi burtiem un cipariem, kas mainīsies ikreiz, kad tiks izveidota dimensijas vērtība. Izmantojiet numura zīmi (#) kā vietturi cipariem un zīmi & kā vietturi burtiem.  Piemērs: lai dimensijas vērtību noteiktu kā burtus CC un trīs ciparus, kā formāta maska ir jāieraksta CC-###.  
5. Noklikšķiniet uz Aktivizēt.
    * Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas. Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.  
6. Noklikšķiniet uz Aktivizēt.
    * Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.  
7. Noklikšķiniet uz Dimensiju vērtības.
8. Noklikšķiniet uz Jauns.
9. Laukā Dimensijas vērtība ievadiet nosaukumu, lai aprakstītu savu finanšu dimensijas vērtību.
10. Laukā Apraksts ierakstiet aprakstu, kas apraksta jūsu finanšu dimensijas vērtību.


