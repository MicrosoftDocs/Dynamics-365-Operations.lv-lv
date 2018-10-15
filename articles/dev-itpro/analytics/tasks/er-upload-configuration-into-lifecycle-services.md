--- 
title: "ER Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju un to augšupielādēt pakalpojumos Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a>ER Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju un to augšupielādēt pakalpojumos Microsoft Lifecycle Services (LCS).

Šajā piemērā jūs izveidosiet konfigurācijas un augšupielādēsiet to pakalpojumos LCS parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem. Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības. Lai izpildītu šīs darbības, ir nepieciešama arī piekļuve pakalpojumiem LCS.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Atlasiet Litware, Inc. un iestatiet to kā aktīvu.
3. Noklikšķiniet uz Konfigurācijas.

## <a name="create-a-new-data-model-configuration"></a>Jaunas datu modeļa konfigurācijas izveide
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
    * Jūs izveidosiet konfigurāciju, kas satur parauga datu modeli elektroniskajiem dokumentiem. Šī datu modeļa konfigurācija vēlāk tiks augšupielādēta pakalpojumos LCS.  
2. Laukā Nosaukums ierakstiet “Parauga modeļa konfigurācija”.
    * Parauga modeļa konfigurācija  
3. Laukā Apraksts ierakstiet “Parauga modeļa konfigurācija”.
    * Parauga modeļa konfigurācija  
4. Klikšķiniet Izveidot konfigurāciju.
5. Noklikšķiniet uz Modeļa veidotājs.
6. Noklikšķiniet uz Jauns.
7. Laukā Nosaukums ierakstiet “Ieejas punkts”.
    * Ieejas punkts  
8. Noklikšķiniet uz Pievienot.
9. Noklikšķiniet uz Saglabāt.
10. Aizvērt lapu.
11. Noklikšķiniet uz Mainīt statusu.
12. Noklikšķiniet uz Pabeigt.
13. Noklikšķiniet uz OK.

## <a name="register-a-new--repository"></a>Reģistrēt jaunu repozitoriju
1. Aizvērt lapu.
2. Noklikšķiniet uz Repozitoriji.
    * Šādi jums tiek ļauts atvērt sarakstu ar repozitorijiem, kas paredzēti konfigurācijas nodrošinātājam Litware, Inc.  
3. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
    * Tas jums ļauj pievienot jaunu repozitoriju.  
4. Laukā Konfigurācijas repozitorija tips atlasiet LCS.
5. Noklikšķiniet uz Izveidot repozitoriju.
6. Laukā Projekts ievadiet vai atlasiet kādu vērtību.
    * Atlasiet vēlamo LCS projektu. Jums ir nepieciešama piekļuve šim projektam.  
7. Noklikšķiniet uz OK.
    * Pabeidziet jauna repozitorija ierakstu.  
8. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet LCS repozitorija ierakstu.  
    * Ņemiet vērā, ka reģistrētais repozitorijs ir atzīmēts ar pašreizējo nodrošinātāju — tas nozīmē, ka šajā repozitorijā var novietot — un līdz ar to atlasītajā LCS projektā var augšupielādēt — tikai konfigurācijas, kas pieder šim nodrošinātājam.  
9. Noklikšķiniet uz Atvērt.
    * Atveriet repozitoriju, lai skatītu sarakstu ar ER konfigurācijām. Tas būs tukšs, ja šis projekts vēl nav lietots ER konfigurāciju koplietošanai.  
10. Aizvērt lapu.
11. Aizvērt lapu.

## <a name="upload-configuration-into-lcs"></a>Augšupielādēt konfigurāciju pakalpojumos LCS
1. Noklikšķiniet uz Konfigurācijas.
2. Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.
    * Atlasiet izveidotu konfigurāciju, kas jau pabeigta.  
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet atlasītās konfigurācijas versiju, kuras statuss ir “Pabeigts”.  
4. Noklikšķiniet uz Mainīt statusu.
5. Noklikšķiniet uz Koplietot.
    * Kad konfigurācija ir publicēta pakalpojumos LCS, tās statuss no “Pabeigts” mainās uz “Koplietots”.  
6. Noklikšķiniet uz OK.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet konfigurācijas versiju, kuras statuss ir “Koplietots”.  
    * Ņemiet vērā, ka atlasītās versijas statuss no “Pabeigts” ir mainīts uz “Koplietots”.  
8. Aizvērt lapu.
9. Noklikšķiniet uz Repozitoriji.
    * Šādi jums tiek ļauts atvērt sarakstu ar repozitorijiem, kas paredzēti konfigurācijas nodrošinātājam Litware, Inc.  
10. Noklikšķiniet uz Atvērt.
    * Atlasiet LCS repozitoriju un atveriet to.  
    * Ņemiet vērā, ka atlasītā konfigurācija tiek rādīta kā atlasītā LCS projekta līdzeklis.  
    * Atveriet LCS, izmantojot https://lcs.dynamics.com. Atveriet projektu, kas iepriekš tika izmantots repozitorija reģistrēšanai, atveriet šī projekta sadaļu “Līdzekļu bibliotēka” un izvērst līdzekļa tipa “GER konfigurācija” saturu —būs pieejama augšupielādētā ER konfigurācija. Ņemiet vērā, ka augšupielādēto LCS konfigurāciju var importēt citā Microsoft Dynamics 365 for Finance and Operations Enterprise edition instancē, ja nodrošinātājiem ir piekļuve šim LCS projektam.  


