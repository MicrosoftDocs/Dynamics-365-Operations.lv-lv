---
title: Pasūtījumu aizturēšanas pārvaldība
description: Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad19ff166c15748b7bbb4b82ef71dbf3e1e8ebd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "323966"
---
# <a name="manage-order-holds"></a>Pasūtījumu aizturēšanas pārvaldība

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu. Pasūtījums var tikt aizturēts dažādu iemeslu dēļ. Piemēram, pasūtījumu var aizturēt līdz debitora adresi vai maksājuma metodi būs iespējams pārbaudīt vai līdz vadītājs varēs pārskatīt debitora kredīta limitu. Kamēr pasūtījums ir aizturēts, noliktava to nevar apstrādāt nosūtīšanai. 

Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-order-holds"></a>Iestatīt pasūtījumu aizturēšanas
1. Doties uz Pārdošana un mārketings > Iestatīšana > Pārdošanas pasūtījumi > Pasūtījumu aizturēšanas kodi.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet kādu vērtību laukā Aizturēšanas kods.
    * Piemēram, ierakstiet Atzvanīt.  
4. Apraksta laukā ierakstiet vērtību.
    * Piemēram, pasūtījums ir aizturēts, gaidot debitora atzvanīšanu.  
    * Ja vēlaties, atzīmējiet izvēles rūtiņu Noņemt rezervācijas, lai pasūtījumam noņemtu visas fiziskās rezervācijas, kad tiek pievienots šis aizturēšanas kods.  
5. Noklikšķiniet uz Saglabāt.

## <a name="place-order-on-hold"></a>Aizturēt pasūtījumu
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz Labi.
5. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
6. Laukā Daudzums ievadiet skaitli.
7. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas pasūtījums.
8. Noklikšķiniet uz Pasūtījumu aizturēšanas.
9. Noklikšķiniet uz Jauns.
10. Laukā Aizturēšanas kods atlasiet kodu, kuru izveidojāt iepriekšējā apakšuzdevumā.
11. Noklikšķiniet uz Saglabāt.
12. Aizvērt lapu.
13. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
14. Sarakstā atzīmējiet atlasīto rindu.
    * Pasūtījumiem, kas pašlaik ir aizturēti, ir atzīmēti lauki “Neapstrādāt” un “Aizturēts”.    
15. Darbību rūtī noklikšķiniet uz Izdot un iepakot.

## <a name="manage-order-holds"></a>Pasūtījumu aizturēšanas pārvaldība
1. Dodieties uz Pārdošana un mārketings > Pārdošanas pasūtījumi > Atvērtie pasūtījumi > Pasūtījumu aizturēšanas.
    * Pasūtījumu aizturēšanas lapa darbojas kā rīks, kurā varat gūt pārskatu par visām pašreizējām un apstrādātajām aizturēšanām, kā arī apstrādāt tās un saistītos pārdošanas pasūtījumus.      
2. Sarakstā atzīmējiet atlasīto rindu.
3. Darbību rūtī noklikšķiniet uz Aizturēt izsniegšanu.
4. Noklikšķiniet uz Izsniegt.
5. Sarakstā noņemiet atzīmi no atlasītās rindas.
    * Laukā Izsniegt lietotājam tagad ir redzams jūsu lietotāja ID.   
6. Noklikšķiniet uz Dzēst izsniegšanu.
7. Darbību rūtī noklikšķiniet uz Dzēst aizturēšanu.
    * Kad esat gatavs noņemt aizturēšanu un ļaut, lai pasūtījums pāriet uz nākamo izpildes darbību, aizturēšana ir jānotīra. Ja pasūtījumam nav jāveic nekādas izmaiņas, varat palaist darbību Notīrīt aizturēšanas. Taču varat arī izmantot darbību Dzēst un mainīt, ja aizturēšanas dzēšanas laikā pasūtījums ir jāatjaunina.      
    * Notīrīšanas un iesniegšanas darbība ir spēkā tikai tad, ja izmantojat zvanu centra funkcionalitāti.  
8. Noklikšķiniet uz Dzēst aizturēšanas.
    * Tagad aizturēšana ir dzēsta no pasūtījuma un noņemta no saraksta Aktīvās aizturēšanas. Lai skatītu visas aizturēšanas vai to apakškopu pēc noteikta statusa, mainiet vērtību laukā Rādīt.     

