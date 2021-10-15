---
title: Finance Insights iestatījumu problēmu novēršana
description: Šajā tēmā uzskaitītas problēmas, kas var rasties, kad izmantojat Finance Insights iespējas. Tajā arī skaidrots, kā atrisināt šos jautājumus.
author: panolte
ms.date: 08/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512894"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insights iestatījumu problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā uzskaitītas problēmas, kas var rasties, kad izmantojat Finance Insights iespējas. Tajā arī skaidrots, kā atrisināt šos jautājumus.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Simptoms: Kādēļ nevar kartēt debitoru maksājumu ieskatu datu integrācijas veidnes mērķa kolonnu?

### <a name="resolution"></a>Novēršana

Iespējams, ka agrākai versijai izmantojat veidni. Pirms versijas 10.0.17 izlaišanas priekšskatiet debitorus, kuri konfigurēja **Debitora maksājuma ieskatu rezultātus (CDS uz Fin un Ops)** Datu integrācijas (DI) veidni, izmantojot **Maksājumu prognozēšanas rezultātu (priekšskatījuma)** elementu. Pēc jaunināšanas uz 10.0.17 vai jaunāku versiju, ir jāizmanto **Debitoru maksājumu ieskatu rezultāti (CDS uz Fin un Ops 10.0.17 vai jaunāka versija)** DI veidne, lai pabeigtu kartēšanu. Iespējams, ka nevarēsit kartēt DI veidnes mērķa kolonnu, kamēr datu pārvaldības elementu saraksts nav atsvaidzināts un tajā tiek parādīts **Maksājumu prognozēšanas rezultāta** elements. Lai atsvaidzinātu elementu sarakstu un rādītu maksājumu prognozēšanas rezultātu, izpildīsiet gan Microsoft Dynamics 365 Finance, gan Dataverse (iepriekš zināmas kā Common Data Service \[CDS\] administratora portāls).

### <a name="in-finance"></a>Finance

Pēc jaunināšanas izpildiet šīs darbības sadaļā Finance.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Datu pārvaldība**.
2. Darbvietā **Datu pārvaldība** atlasiet elementu **Struktūras parametri**.
3. Lapā **Datu importēšanas/eksportēšanas struktūras parametri** atlasiet **Elementa iestatījumi** un pēc tam atlasiet **Atsvaidzināt elementu sarakstu**.
4. Aizveriet lapu **Datu importēšanas/eksportēšanas struktūras parametri**.
5. Darbvietā **Datu pārvaldība** atlasiet elementu **Datu elementi**.
6. Meklējiet "Maksājumu prognozēšanas rezultāts." Pārbaudiet, vai **Maksājuma prognozēšanas rezultāta** elements nav priekšskatījuma versija. Priekšskatījuma versijas nosaukums beidzas sadaļā "(priekšskatījums)." Ja ir redzama tikai entītijas priekšskatījuma versija, sazinieties ar Microsoft atbalsta dienestu.

### <a name="in-dataverse"></a>Programmā Dataverse

Izpildiet šīs darbības [Power Platform administrēšanas centrā](https://admin.powerplatform.microsoft.com/environments), lai atjauninātu savu datu integrācijas projektus.

1. Ja izmantojat Finance Insights versiju, noņemiet DI projektu, kas ir saistīts ar **Debitoru maksājumu ieskatu rezultātiem (CDS uz Fin un Ops)** veidni.
2. Izpildiet darbības sadaļā [Izveidot datu integrētātāja projektu](create-data-integrate-project.md). Izmantojiet **Debitora maksājuma ieskatu rezultātu (CDS uz Fin un Ops 10.0.17 vai jaunāku)** veidni.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Simptoms: kādēļ naudas plūsmas prognozes darbvietas cilne Naudas plūsmas prognoze nerāda nekādus datus?

### <a name="resolution"></a>Novēršana

Naudas plūsmas prognozēšanas funkcija naudas plūsmas un banku pārvaldībā un naudas plūsmas prognožu līdzekli Finance Insights ir jāiestata un jāiespējo, lai pareizi parādītu datus **Naudas plūsmas prognozes** darbvietā.

Vispirms iestatiet un aktivizējiet naudas plūsmas prognozes un likviditātes kontus. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../cash-bank-management/cash-flow-forecasting.md). Ja šis iestatījums ir pabeigts, bet nevarat redzēt sagaidāmos rezultātus, papildinformāciju skatiet sadaļā [Problēmu novēršanas naudas plūsmas prognozēšanas](../cash-bank-management/cash-flow-forecasting-tsg.md) iestatījumi.

Pēc tam apstipriniet, ka naudas plūsmas prognožu funkcija Finance Insights (**Naudas un bankas pārvaldība \> Iestatījumi \> Finance Insights \> Naudas plūsmas prognozes**) ir iespējota un ka AI modeļa apmācība ir pabeigta. Ja apmācība nav pabeigta, atlasiet **Prognoze tagad**, lai sāktu modeļu apmācību procesu.
