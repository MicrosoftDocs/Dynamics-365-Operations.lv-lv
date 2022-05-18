---
title: Finanšu dimensiju definēšana
description: Šajā procedūrā parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10a991938f68c0ade19999e48a02f032c92a6779
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716948"
---
# <a name="define-financial-dimensions"></a>Finanšu dimensiju definēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju. Ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.

## <a name="create-an-entity-backed-financial-dimension"></a>Uz elementu balstītas finanšu dimensijas izveide
1. Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Lietotāja vērtību veidlapa** atlasiet sistēmas definētu elementu, uz kuru balstīt finanšu dimensiju. 
4. Laukā **Dimensijas nosaukums** ievadiet vērtību, lai aprakstītu finanšu dimensiju. Nosaukums var atšķirties no sistēmas definētā elementa nosaukuma, bet nedrīkst saturēt atstarpes vai īpašas rakstzīmes.
5. Noklikšķiniet uz **Aktivizēt**. Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas. Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.  
6. Aktivizēšanas ziņojumā noklikšķiniet uz **Aizvērt**.
7. Noklikšķiniet uz **Aktivizēt**. Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.  
8. **Darbību rūtī** noklikšķiniet uz **Dimensiju vērtības**. Dažas dimensijas vērtības attiecas tikai uz konkrētu uzņēmumu. Jūs varat pārliecināties, vai tās attiecas tikai uz konkrētu uzņēmumu, pārbaudot, vai uzņēmuma nosaukums parādās dimensiju vērtību sarakstā.  

## <a name="create-a-custom-financial-dimension"></a>Pielāgotās finanšu dimensijas izveide
1. Klikšķiniet **Jauns**.
2. Laukā **Izmantot vērtības no** atlasiet **Pielāgota dimensija**.
3. Laukā **Dimensijas nosaukums** ievadiet vērtību, lai aprakstītu finanšu dimensiju.
    - Nosaukumā nedrīkst būt atstarpes vai īpašas rakstzīmes.  
    - Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku.   
    - Jūs varat ievadīt rakstzīmes, kas paliek vienādas katrai dimensijas vērtībai, piemēram, burtus vai pārnesumzīmi. Varat arī ievadīt numura zīmes (#) un zīmes & kā vietturi burtiem un cipariem, kas mainīsies ikreiz, kad tiks izveidota dimensijas vērtība. Izmantojiet numura zīmi (#) kā vietturi cipariem un zīmi & kā vietturi burtiem.  Piemērs: lai dimensijas vērtību noteiktu kā burtus CC un trīs ciparus, kā formāta maska ir jāieraksta CC-###.  
4. Noklikšķiniet uz **Aktivizēt**. Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas. Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.     
5. Noklikšķiniet uz **Aktivizēt**. Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.      
6. **Darbību rūtī** noklikšķiniet uz **Dimensiju vērtības**.
7. Klikšķiniet **Jauns**.
8. Laukā **Dimensijas vērtība** ievadiet nosaukumu, lai aprakstītu savu finanšu dimensijas vērtību.
9. Laukā **Apraksts** ierakstiet aprakstu, kas apraksta jūsu finanšu dimensijas vērtību.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
