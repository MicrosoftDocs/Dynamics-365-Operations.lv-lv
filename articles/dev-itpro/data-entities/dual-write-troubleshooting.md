---
title: Datu integrācijas problēmu novēršanas rokasgrāmata
description: Šajā rakstā ir sniegta informācija par problēmu novēršanu datu integrācijai starp programmām Microsoft Dynamics 365 for Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873109"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Datu integrācijas problēmu novēršanas rokasgrāmata

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Iespējojiet spraudņu izsekošanas žurnālus programmā Common Data Service un pārbaudiet informāciju par duālās rakstīšanas spraudņu kļūdām.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Ja duālās rakstīšanas sinhronizācijas laikā radīsies problēma vai kļūda, veiciet šīs darbības kļūdu pārbaudei izsekošanas žurnālā.

1. Lai varētu pārbaudīt kļūdas, vispirms ir jāiespējo spraudņu izsekošanas žurnāli. Lai iegūtu norādījumus, atveriet “Skatīt izsekošanas žurnālus” [Pamācība: uzrakstiet un reģistrējiet spraudni](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Tagad varat pārbaudīt kļūdas.

2. Pierakstieties programmā Microsoft Dynamics 365 for Sales.
3. Atlasiet pogu **Iestatījumi** (zobrata simbols), pēc tam atlasiet **Papildu iestatījumi**.
4. Izvēlnē **Iestatījumi** atlasiet **Pielāgošana \> Spraudņu izsekošanas žurnāls**.
5. Atlasiet tipa nosaukumu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, lai parādītu informāciju par kļūdu.

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a>Pārbaudiet duālās rakstīšanas sinhronizācijas kļūdas programmā Finance and Operations

Veiciet šīs darbības, lai pārbaudītu kļūdas testēšanas laikā.

1. Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).
2. Atveriet LCS projektu, kuram ir jāveic testēšana.
3. Atlasiet **Mākoņvides**.
4. Izveidojiet Attālās darbvirsmas savienojumu ar Dynamics 365 for Finance and Operations virtuālo mašīnu (VM), izmantojot vietējo kontu, kas parādīts portālā LCS.
5. Atveriet komponentu Notikumu skatītājs. 
6. Pārejiet uz sadaļu **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**. Tiek parādītas kļūdas un detalizēta informācija.

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a>Atsaistiet vienu Common Data Service vidi no programmas Finance and Operations un saistiet ar citu vidi

Veiciet šīs darbības, lai atjauninātu saites.

1. Pārejiet uz programmas Finance and Operations vidi.
2. Atveriet Datu pārvaldība.
3. Atlasiet **Saistiet ar CDS lietojumprogrammām**.
4. Atlasiet visus darbojošos kartējumus un pēc tam atlasiet **Apturēt**.
5. Atlasiet visus kartējumus un pēc tam atlasiet **Dzēst**.

    > [!NOTE]
    > Opcija **Dzēst** nav pieejama, ja ir atlasīta veidne **CustomerV3-Account**. Notīriet šīs veidnes atlasi, ja nepieciešams. **CustomerV3-Account** ir vecāka nodrošināta veidne un darbojas ar risinājumu No potenciālā klienta līdz skaidrai naudai. Tā parādās zem visām veidnēm, jo ir izlaista visā pasaulē.

6. Atlasiet **Atsaistīt vidi**.
7. Atlasiet **Jā**, lai apstiprinātu darbību.
8. Lai piesaistītu jauno vidi, izpildiet [instalēšanas rokasgrāmatā](https://aka.ms/dualwrite-docs) aprakstītās darbības.
