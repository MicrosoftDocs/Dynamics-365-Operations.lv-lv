---
title: Pasūtījumu aizturēšanas pārvaldība
description: Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0a6acbc55a69f854463e72391fb0fff4dfb459c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817729"
---
# <a name="manage-order-holds"></a>Pasūtījumu aizturēšanas pārvaldība

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu. Pasūtījums var tikt aizturēts dažādu iemeslu dēļ. Piemēram, pasūtījumu var aizturēt līdz debitora adresi vai maksājuma metodi būs iespējams pārbaudīt vai līdz vadītājs varēs pārskatīt debitora kredīta limitu. Kamēr pasūtījums ir aizturēts, noliktava to nevar apstrādāt nosūtīšanai. 

Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-order-holds"></a>Iestatīt pasūtījumu aizturēšanas
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Iestatīšana > Pārdošanas pasūtījumi > Pasūtījumu aizturēšanas kodi**.
2. Klikšķiniet **Jauns**.
3. Ierakstiet kādu vērtību laukā **Aizturēšanas kods**. Piemēram, ierakstiet 'Atzvanīt'.  
4. Laukā **Apraksts** ierakstiet kādu vērtību.
    - Piemēram, pasūtījums ir aizturēts, gaidot debitora atzvanīšanu.  
    - Ja vēlaties, atzīmējiet izvēles rūtiņu **Noņemt rezervācijas**, lai pasūtījumam noņemtu visas fiziskās rezervācijas, kad tiek pievienots šis aizturēšanas kods.  
5. Noklikšķiniet uz **Saglabāt**.

## <a name="place-order-on-hold"></a>Aizturēt pasūtījumu
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Klienta konts**.
4. Noklikšķiniet uz **Labi**.
5. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
6. Laukā **Daudzums** ierakstiet kādu skaitli.
7. **Darbību rūtī** noklikšķiniet uz **Pārdošanas pasūtījums**.
8. Noklikšķiniet uz **Pasūtījumu aizturēšanas**.
9. Klikšķiniet **Jauns**.
10. Laukā **Aizturēšanas kods** atlasiet kodu, kuru izveidojāt iepriekšējā apakšuzdevumā.
11. Noklikšķiniet uz **Saglabāt**.
12. Aizvērt lapu.
13. Pārejiet uz sadaļu **Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
14. Sarakstā atzīmējiet atlasīto rindu. Pasūtījumiem, kas pašlaik ir aizturēti, ir atzīmēti lauki “Neapstrādāt” un “Aizturēts”.
15. Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.

## <a name="manage-order-holds"></a>Pasūtījumu aizturēšanas pārvaldība
1. Dodieties uz **Pārdošana un mārketings > Pārdošanas pasūtījumi > Atvērtie pasūtījumi > Pasūtījumu aizturēšanas**. Lapa **Pasūtījumu aizturēšanas** darbojas kā rīks, kurā varat gūt pārskatu par visām pašreizējām un apstrādātajām aizturēšanām, kā arī apstrādāt tās un saistītos pārdošanas pasūtījumus.     
2. Sarakstā atzīmējiet atlasīto rindu.
3. **Darbību rūtī** noklikšķiniet uz **Aizturēt izsniegšanu**.
4. Noklikšķiniet uz **Izsniegt**.
5. Sarakstā noņemiet atzīmi no atlasītās rindas. Laukā **Izsniegt lietotājam** tagad ir redzams jūsu lietotāja ID.   
6. Noklikšķiniet uz **Dzēst izsniegšanu**.
7. **Darbību rūtī** noklikšķiniet uz **Dzēst aizturēšanu**.
    - Kad esat gatavs noņemt aizturēšanu un ļaut, lai pasūtījums pāriet uz nākamo izpildes darbību, aizturēšana ir jānotīra. Ja pasūtījumam nav jāveic nekādas izmaiņas, varat palaist darbību Notīrīt aizturēšanas. Taču varat arī izmantot darbību Dzēst un mainīt, ja aizturēšanas dzēšanas laikā pasūtījums ir jāatjaunina.      
    - Darbība **Notīrīt un iesniegt** ir spēkā tikai tad, ja izmantojat zvanu centra funkcionalitāti.  
8. Noklikšķiniet uz **Dzēst aizturēšanas**. Tagad aizturēšana ir dzēsta no pasūtījuma un noņemta no saraksta Aktīvās aizturēšanas. Lai skatītu visas aizturēšanas vai to apakškopu pēc noteikta statusa, mainiet vērtību laukā Rādīt.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]