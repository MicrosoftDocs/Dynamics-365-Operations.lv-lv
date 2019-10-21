---
title: Elektronisko pārskatu veidošanas (ER) modeļu kartēšanas konfigurāciju izveide
description: Izmantojiet šo procedūru, lai izveidotu jaunu elektronisko pārskatu veidošanas (ER) modeļa kartējuma konfigurāciju un izmantotu iebūvētās ER funkcijas, lai nodrošinātu apkopoto aprēķinu efektivitāti.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcfc258e7fe364779fd77cc79413e8d5e871e214
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182696"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Elektronisko pārskatu veidošanas (ER) modeļu kartēšanas konfigurāciju izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai izveidotu jaunu elektronisko pārskatu veidošanas (ER) modeļa kartējuma konfigurāciju un izmantotu iebūvētās ER funkcijas, lai nodrošinātu apkopoto aprēķinu efektivitāti. Šajā procedūrā izveidosit konfigurāciju parauga uzņēmumam Litware, Inc. 

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.

Šīs darbības var veikt, izmantojot jebkuru datu kopu. Lai izpildītu tālāk norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu”.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Noklikšķiniet uz Rādīt filtrus.
4. Laukā “Nosaukums” ievadiet filtra vērtību “Intrastat” un izmantojiet filtra operatoru “sākas ar”.
    * Lietojiet šo filtru, lai atrastu “Intrastat” datu modeļa konfigurāciju. Šis modelis jau var būt konfigurāciju kokā. Šādā gadījumā, izlaidiet nākamo apakšuzdevumu.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Iegūt piekļuvi korporācijas Microsoft nodrošinātajai Intrastat modeļa konfigurācijai
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet elementu Microsoft nodrošinātājs.  
5. Noklikšķiniet uz Repozitoriji.
    * Noklikšķiniet uz Repozitoriji elementā Microsoft nodrošinātājs.  
6. Noklikšķiniet uz Rādīt filtrus.
7. Laukā “Tipa nosaukums” ievadiet filtra vērtību “resursi” un izmantojiet filtra operatoru “satur”. 
8. Noklikšķiniet uz Atvērt.
9. Kokā atlasiet “Intrastat modelis”.
10. Noklikšķiniet uz Importēt.
11. Noklikšķiniet uz Jā.
    * Jūs importējāt ER modeļa konfigurāciju, kas satur datu modeli, kuru izmantosit, lai izpētītu, kā var izmantot jauno ER funkcionalitāti.  
12. Aizvērt lapu.
13. Aizvērt lapu.
14. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.

## <a name="add-a-new-model-mapping-configuration"></a>Pievienot jaunu modeļa kartējuma konfigurāciju
1. Kokā atlasiet “Intrastat modelis”.
2. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Jauns ievadiet “Uz datu modeli Intrastat balstīts modeļa kartējums”.
4. Laukā Nosaukums ierakstiet “Intrastat parauga kartēšana”.
    * Intrastat parauga kartēšana  
5. Klikšķiniet Izveidot konfigurāciju.

