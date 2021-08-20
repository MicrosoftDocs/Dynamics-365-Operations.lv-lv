---
title: Lean manufacturing apakšuzņēmēja darba šūnas izveide
description: Lai modelētu lean manufacturing apakšlīguma darbu, jāizveido darba šūna, kas saistīta ar kreditoru, kurš nodrošina darbu.
author: cvocph
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acb0adf3e53830f951ae6d1faefd3f30aa3a445e28dc1a08b76a408bdf9af810
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744682"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Lean manufacturing apakšuzņēmēja darba šūnas izveide

[!include [banner](../../includes/banner.md)]

Lai modelētu lean manufacturing apakšlīguma darbu, jāizveido darba šūna, kas saistīta ar kreditoru, kurš nodrošina darbu. Apakšuzņēmēja darba šūna ir saistīta ar kreditoru, izmantojot kreditora veida resursa saistību. Atskaņojot šo ierakstu USMF demonstrācijas uzņēmumā, varat atlasīt kreditora konta ID 1002 un vietu 1.


## <a name="create-a-vendor-resource"></a>Kreditora resursa izveide
1. Dodieties uz Resursi.
2. Noklikšķiniet uz Jauns.
3. Laukā Resursi ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā veids atlasiet "Vendor".
6. Laukā Kreditors noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.

## <a name="create-the-resource-group"></a>Resursu grupas izveide
1. Dodieties uz Resursu grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Resursu grupa ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet vietu, kurai ir jāpiešķir darba šūna. Teorētiski vieta var apzīmēt atsevišķu vietu, ko vada kreditors. Tomēr vairumā gadījumu apakšuzņēmēja resursi ir tikai piešķirti vietai, kas pasūta apakšuzņēmēja darbu. Ņemiet vērā, ka apakšuzņēmēja darba šūnu ievades un izvades noliktavām jābūt tajā pašā vietā.  
6. Laukā Vieta ierakstiet kādu vērtību.
7. @SysTaskRecorder:_RequestClose
8. Atzīmējiet izvēles rūtiņu Darba šūna vai noņemiet tās atzīmi.
9. Laukā Ievades noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet noliktavu un vietu, kas tiek izmantota, lai novietotu materiālu kreditora pārvaldītai darba šūnai. Daudzos gadījumos noliktava un vieta tiek modelēta, izmantojot atsevišķu noliktavu katram kreditoram un vienu vietu darba šūnai.  
10. Laukā Ievades vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Laukā Izvades noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Definējiet noliktavu un vietu, kur tiek grāmatots materiāls, grāmatojot darba šūnas apakšuzņēmēju aktivitātes. Ja kreditora pārskati ir Kanban darbi, noliktava un vieta var būt kreditora vietnē. Vai arī noliktava un vieta var būt saņemšanas vieta, kas saistīta ar ražošanas plūsmas nākamo soli.  
12. Laukā Izvades vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
13. Izvērsiet vai sakļaujiet sadaļu Kalendāri.
14. Noklikšķiniet uz Pievienot.
15. Laukā Kalendārs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Saistiet darba šūnas darba laika kalendāru ar resursu grupu. Kritiskiem resursiem iesakām definēt noteiktus kalendārus, kas attēlo precīzus darba laikus un darba šūnas vai kreditora vietnes saistītās iespējas.  
16. Izvērsiet vai sakļaujiet sadaļu Resursi.
17. Noklikšķiniet uz Pievienot.
    * Apakšuzņēmēja resursu grupai ir nepieciešams kreditora veida saistītais resurss, kas saista resursu grupu ar kreditora kontu.  
18. Laukā Resursi noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet vai ievadiet kreditora resursu, ko izveidojāt iepriekšējā apakšuzdevumā.  
19. Izvērsiet vai sakļaujiet sadaļu Darba šūnas noslodze.
20. Noklikšķiniet uz Pievienot.
    * Darba šūnai ir jādefinē noslodze. Šajā piemērā izveidojām 100 vienību caurlaides noslodzi uz standarta darbdienu.  
21. Laukā Ražošanas plūsmas modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
22. Laukā Noslodzes periods atlasiet opciju.
23. Laukā Vidējais caurlaides daudzums ievadiet skaitli.
24. Laukā Vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
25. ResolveChanges vienumam Vienība.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]