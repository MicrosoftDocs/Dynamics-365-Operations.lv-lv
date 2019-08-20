---
title: Datu integrācijas problēmu novēršanas rokasgrāmata
description: Šajā tēmā ir sniegta problēmu novēršanas informācija par datu integrāciju starp programmām Microsoft Dynamics 365 for Finance and Operations un Common Data Service.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797279"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Datu integrācijas problēmu novēršanas rokasgrāmata

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Iespējojiet spraudņa izsekošanu Common Data Service un pārbaudiet duālā ieraksta spraudņa kļūdas detaļas

Ja radusies problēma vai kļūda ar duālā ieraksta sinhronizāciju, varat pārbaudīt kļūdas trasēšanas žurnālā:

1. Pirms varat pārbaudīt kļūdas, ir jāiespējo spraudņa izsekošana, izmantojot norādījumus rakstā [Reģistrēt spraudni](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs), lai iespējotu spraudņa izsekošanu. Tagad varat pārbaudīt kļūdas.
2. Piesakieties pakalpojumā Dynamics 365 for Sales.
3. Noklikšķiniet uz ikonas Iestatījumi (zobrats) un atlasiet **Papildu iestatījumi**.
4. Izvēlnē **Iestatījumi** izvēlieties **Pielāgošana > Spraudņa izsekošanas žurnāls**.
5. Lai parādītu detalizētu kļūdas informāciju, noklikšķiniet uz tipa nosaukuma **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Duālā ieraksta sinhronizācijas kļūdu pārbaude programmā Finance and Operations

Varat pārbaudīt kļūdas testēšanas laikā, veicot tālāk norādītās darbības.

+ Piesakieties Lifecycle Services (LCS).
+ Atveriet LCS projektu, kuru izvēlējāties, lai veiktu duālā ieraksta testēšanu.
+ Pārejiet uz Cloud Hosted Environments.
+ Attālā darbvirsma uz Finance and Operations virtuālās mašīnas, izmantojot lokālo kontu, kas tiek parādīts LCS.
+ Atvērt notikumu skatītāju. 
+ Dodieties uz **Programmas un Pakalpojumu žurnāli > Microsoft > Dynamics > AX-DualWriteSync > Darbības**. Tiek parādītas kļūdas un detaļlizēta informācija.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Kā noņemt saiti un saistīt citu Common Data Service vidi no programmas Finance and Operations

Varat atjaunināt saites, veicot tālāk norādītās darbības.

+ Dodieties uz Finance and Operations vidi.
+ Atveriet Datu pārvaldība.
+ Noklikšķiniet uz **Saite uz CDS programmām**.
+ Atlasiet visus darbojošos kartējumus un noklikšķiniet uz **Apturēt**. 
+ Atlasiet visus kartējumus un noklikšķiniet uz **Dzēst**.

    > [!NOTE]
    > Opcija **Dzēst** netiks parādīta, ja ir atlasīta veidne**CustomerV3-Account**. Ja nepieciešams, atceliet tās atlasi. **CustomerV3-Account** ir vecāka nodrošināta veidne un darbojas ar risinājumu No potenciālā klienta līdz skaidrai naudai. Tā kā tā ir izlaista globāli, tā tiek parādīta zem visām veidnēm.

+ Noklikšķiniet uz **Atsaistīt vidi**.
+ Noklikšķiniet uz **Jā**, lai apstiprinātu.
+ Lai piesaistītu jauno vidi, izpildiet [instalēšanas rokasgrāmatā](https://aka.ms/dualwrite-docs) aprakstītās darbības.

