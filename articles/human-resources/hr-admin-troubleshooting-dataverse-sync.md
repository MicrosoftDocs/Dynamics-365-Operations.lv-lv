---
title: Dataverse sinhronizācijas atiestatīšana
description: Šajā tēmā ir aprakstīts, kā novērst problēmu ierakstus, kas nesinhronizē pareizi starp Microsoft Dynamics 365 Human Resources un Cilvēkresursu kapitāla pārvaldības (HCM) kopējo Microsoft Dataverse risinājumu.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 8bfcd51b023c02590919155abbb836326408d298
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696240"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse sinhronizācijas atiestatīšana


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problēma

Ieraksti nav sinhronizēti starp korporācijas Microsoft Dynamics 365 Human Resources un Cilvēkkapitāla pārvaldības (HCM) kopējā risinājuma Microsoft Dataverse elementiem. Papildinformāciju par sinhronizāciju skatiet sadaļu [Dataverse integrācijas konfigurēšana](hr-admin-integration-common-data-service.md). Sinhronizēšanas kļūme var rasties, kad **Dataverse integrācijas atkārtotā mēģinājuma** vai **Dataverse integrācijas izlaistie pieprasījuma sinhronizācijas** pakešuzdevumi paliek stāvoklī **Notiek izpilde**.

## <a name="resolution"></a>Novēršana

Ja **Dataverse integrācijas atkārtotā mēģinājuma** vai **Dataverse integrācijas izlaistie pieprasījuma sinhronizācijas** pakešuzdevumi paliek stāvoklī **Notiek izpilde** vai **Tiek atcelts**, varat atiestatīt statusu. To var izdarīt, atceļot pakešuzdevumu, sekojot norādēm sadaļā [Palikušo pakešuzdevumu atiestatīšana](hr-admin-troubleshooting-batch-execution.md). Pēc pakešuzdevuma atcelšanas to var atiestatīt, iestatot statusu **Gaida**. Tad pakešuzdevums tiks palaists nākamā plānotā izpildes laika laikā.

1. Ja tas vēl nav izdarīts, iespējojiet līdzekli **Uzlabotais pakešu pārtraukšanas līdzeklis** **Līdzekļu pārvaldībā**.
   1. Atveriet **Līdzekļu pārvaldības** lapu (**Sistēmas administrēšana** > **Kopsavilkums** > **Līdzekļu pārvaldība**).
   2. Atlasiet cilni **Visi**.
   3. Atlasiet kolonnu **Līdzekļa nosaukums** un filtrējiet pēc **Uzlabotās partijas atsaukšana**.
   4. Atlasiet darbību **Iespējot**, ja tā jau nav aktivizēta.

2. Dataverse integrācijas atslēgšana.
   1. Dodieties uz **Microsoft Dataverse integrācijas** lapu (**Sistēmas administrēšana** ejiet uz **Saites** > **Integrācijas** > **Dataverse konfigurācija**).
   2. Iestatiet opciju **Iespējot Dataverse integrāciju** uz **Nē**.

3. Atceliet **Dataverse integrācijas atkārtotā mēģinājuma** pakešuzdevumu.
   1. Dodieties uz lapu **Pakešuzdevumi** sadaļā (**Sistēmas administrēšana** dodieties uz **Saites** > **Pakešuzdevumi** > **Pakešuzdevumi**).
   2. Filtrējiet kolonnu **Darba apraksts** pēc **Integrācijas**.
   3. Atlasiet **Dataverse integrācijas atkārtotā mēģinājuma** pakešuzdevumu.
   4. Darbības lentes sarakstā atlasiet **Pakešuzdevums**, **Piespiedu atcelšana** un pēc tam atlasiet **Jā**, lai apstiprinātu.

   > [!NOTE]
   > Atkarībā no tā, kad integrācija tika aktivizēta pirmo reizi, pakešdarbam var būt apraksts **Common Data Service integrācijas atkārtots mēģinājums**. Atlasiet šo pakešuzdevumu, ja tas tiek uzskaitīts, nevis **Dataverse integrācijas atkārtoto mēģinājumu** pakešuzdevumu.

4. Dzēst visus Dataverse integrācijas pakešuzdevumus.
   1. Lapā **Pakešuzdevumi** atlasiet **Dataverse integrāciju izlaisto pieprasījumu sinhronizāciju**, **Dataverse integrācijas atkārtoto mēģinājumu** un **Dataverse integrācijas sākotnējos sinhronizācijas** pakešuzdevumus.
   2. Darbības lentē atlasiet **Mainīt statusu**. 
   3. Atlasiet **Aizturēt** un pēc tam atlasiet **Labi**.
   4. Darbības lentē atlasiet darbību **Dzēst** un pēc tam atlasiet **Jā**, lai apstiprinātu darbību.

5. Ieslēgt Dataverse integrācijas pakešuzdevumus.
   1. Dodieties uz **Microsoft Dataverse integrācijas** lapu (**Sistēmas administrēšana** > **Saites** > **Integrācijas** > **Dataverse konfigurācija**).
   2. Iestatiet **Iespējot Dataverse integrāciju** uz **Jā**.

6. Dodieties uz lapu **Pakešuzdevumi** un apstipriniet, ka ir izveidoti **Dataverse integrācijas atkārtoti mēģinājumi** un **Dataverse integrācijas izlaisto pieprasījumu sinhronizācijas** pakešuzdevumi.

Kad pakešuzdevumi ir atkārtoti izveidoti, jūs tagad varat pārraudzīt **Dataverse integrācijas atkārtotu** pakešuzdevumu, lai redzētu, cik ilgs laiks nepieciešams darba izpildei. Pēc tam varat pārbaudīt, vai ieraksti tiek pareizi sinhronizēti ar HCM Common Solution Microsoft Dataverse sadaļā.

## <a name="see-also"></a>Skatiet arī

[Pakalpojuma Dataverse integrācijas konfigurēšana](hr-admin-integration-common-data-service.md)<br>
[Iestrēgušu pakešuzdevumu atiestatīšana](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
