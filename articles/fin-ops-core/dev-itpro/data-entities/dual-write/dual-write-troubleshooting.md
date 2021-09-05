---
title: Vispārējā problēmu novēršana
description: Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4adc2d83667a05d14a26ace23e5bd8026df4b5f
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380216"
---
# <a name="general-troubleshooting"></a>Vispārējā problēmu novēršana

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Spraudņa trasēšanas žurnāla iespējošana un skatīšana Dataverse, lai skatītu kļūdas informāciju

**Nepieciešamā loma, lai ieslēgtu trasēšanas žurnālu un skatītu kļūdas:** sistēmas administrators

Lai aktivizētu trasēšanas žurnālu, veiciet tālāk minētās darbības.

1. Piesakieties Customer Engagement programmā, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Sistēma** atlasiet **Administrēšana**.
2. Lapā **Administrēšana** atlasiet opciju **Sistēmas iestatījumi**.
3. Cilnes **Pielāgošana** laukā **Spraudņa un pielāgotās darbplūsmas aktivitātes izsekošana** atlasiet **Visi**, lai iespējotu spraudņa izsekošanas žurnālu. Ja vēlaties izsekot trasēšanas žurnāliem tikai tad, ja rodas izņēmumi, varat tā vietā izvēlēties opciju **Izņēmums**.


Lai skatītu trasēšanas žurnālu, veiciet tālāk minētās darbības.

1. Piesakieties Customer Engagement programmā, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Pielāgošana** atlasiet **Spraudņa trasēšanas žurnāls**.
2. Atrodiet trasēšanas žurnālus, kur lauks **Veida nosaukums** ir iestatīts uz **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Veiciet dubultklikšķi uz elementa, lai apskatītu pilno žurnālu, un pēc tam kopsavilkuma cilnē **Izpilde** pārskatiet **Ziņojuma bloka** tekstu.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Atkļūdošanas režīma iespējošana, lai novērstu tiešsaistes sinhronizācijas problēmas Finance and Operations programmās

**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators

Dataverse radušās duālā ieraksta kļūdas var parādīties Finance and Operations programmā. Lai iespējotu izvērsto kļūdu reģistrēšanu, izpildiet tālāk minētās darbības.

1. Visām projekta konfigurācijām programmā Finance and Operations ir karodziņš **IsDebugMode** tabulā **DualWriteProjectConfiguration**.
2. Atveriet elementu **DualWriteProjectConfiguration**, izmantojot Excel pievienojumprogrammu. Lai izmantotu pievienojumprogrammu, iespējojiet dizaina režīmu Finance and Operations Excel pievienojumprogrammā un pievienojiet lapai **DualWriteProjectConfiguration**. Papildinformāciju skatiet sadaļā [Elementa datu skatīšana un atjaunināšana programmā Excel](../../office-integration/use-excel-add-in.md).
3. Projektā iestatiet **IsDebugMode** uz **Jā**.
4. Palaidiet scenāriju, kas ģenerē kļūdas.
5. Izvērstie žurnāli ir pieejami tabulā **DualWriteErrorLog**.
6. Lai uzmeklēt tabulas pārlūka datus, izmantojiet šādu saiti: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, `999`aizvietošana.
7. Atjauniniet vēlreiz pēc [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), kas ir pieejams platformas atjauninājumiem 37 vai jaunākai versijai. Ja šis labojums ir instalēts, atkļūdošanas režīms tvers vairāk žurnālu.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Sinhronizācijas kļūdu pārbaude Finance and Operations programmas virtuālajā mašīnā

**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators

1. Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).
2. Atveriet LCS projektu, kuram izvēlējāties veikt duālā ieraksta pārbaudi.
3. Atlasiet elementu **Mākoņvides**.
4. Izmantojiet attālo darbvirsmu, lai pieteiktos Finance and Operations programmas virtuālajā mašīnā (VM). Izmantojiet lokālo kontu, kas tiek parādīts LCS.
5. Atveriet Notikumu skatītāju,
6. Atlasiet **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**.
7. Pārskatiet neseno kļūdu sarakstu.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Atsaistīt un saistīt citu Dataverse vidi no Finance and Operations programmas

**Nepieciešamā loma, lai atsaistītu vidi:** sistēmas administrators vai nu Finance and Operations programmai, vai Dataverse.

1. Piesakieties Finance and Operations programmā.
2. Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**.
3. Atlasiet visus darbojošos kartējumus, pēc tam atlasiet **Apturēt**.
4. Atlasiet **Atsaistīt vidi**.
5. Atlasiet **Jā**, lai apstiprinātu darbību.

Tagad varat saistīt jaunu vidi.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Nevar skatīt pārdošanas pasūtījuma rindas informācijas veidlapu 

Veidojot pārdošanas pasūtījumu Dynamics 365 Sales, noklikšķinot uz **+ pievienot preces**, varat tikt novirzīts uz Dynamics 365 Project Operations pasūtījuma rindas veidlapu. No šīs veidlapas nav iespējams skatīt pārdošanas pasūtījuma rindas **Informācijas** veidlapu. **Informācijas** opcija neparādās nolaižamajā sarakstā zem **Jaunas pasūtījuma rindas**. Tas notiek tāpēc, ka projekta operācijas ir uzstādītas jūsu vidē.

Lai atkārtoti iespējotu **Informācijas** veidlapas opciju, rīkojieties šādi:

1. Pārejiet uz **Pasūtījuma rindas** tabulu.
2. Atrodiet **Informācijas** veidlapu zem veidlapas zara.
3. Atlasiet **Informācijas** veidlapu un noklikšķiniet uz **Iespējot drošības lomas**.
4. Mainiet drošības iestatījumu uz **Parādīt visiem**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Kā iespējot un saglabāt tīkla izsekošanu, lai izsekošanu varētu pievienot atbalsta biļetēm

Iespējams, atbalsta komandai būs jāpārskata tīkla izsekošana, lai novērstu dažas problēmas. Lai izveidotu tīkla izskeošanu, rīkojieties šādi.

### <a name="chrome"></a>Chrome

1. Atvērtajā cilnē nospiediet **F12** vai izvēlieties **Izstrādātāja rīki**, lai atvērtu izstrādātāja rīkus.
2. Atveriet cilni **Tīkls** un filtra tekstlodziņā ierakstiet **integ**.
3. Palaidiet scenāriju un ievērojiet reģistrētos pieprasījumus.
4. Ar peles labo pogu noklikšķiniet uz ierakstiem un atlasiet **Saglabāt visu kā HAR ar saturu**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Atvērtajā cilnē nospiediet **F12** vai izvēlieties **Izstrādātāja rīki**, lai atvērtu izstrādātāja rīkus.
2. Atveriet cilni **Tīkls**.
3. Palaidiet scenāriju.
4. Atlasiet **Saglabāt**, lai eksportētu rezultātus kā HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
