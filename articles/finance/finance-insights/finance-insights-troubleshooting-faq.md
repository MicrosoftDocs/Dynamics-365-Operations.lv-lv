---
title: Finance Insights iestatījumu problēmu novēršana
description: Šajā tēmā uzskaitītas problēmas, kas var rasties, kad izmantojat Finance Insights iespējas. Tajā arī skaidrots, kā atrisināt šos jautājumus.
author: panolte
ms.date: 11/03/2021
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
ms.openlocfilehash: c1bbdbec2bc0273a73ffc13a4cce024543af5a13
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968840"
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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Simptoms: Kad mēģinu atvērt, izmantojot saites debitora maksājumu prognozēšanas iestatījumu lapā, kāpēc es saņemu šādu kļūdas ziņojumu: "Diemžēl ir bijis AI Builder atvienošanās"?

### <a name="resolution"></a>Novēršana

Dynamics 365 Finance Lietotāja kontam jābūt vides lietotāja kontam un šim lietotāja Microsoft Power Apps kontam jābūt sistēmas pielāgotāja lomai. Sistēmas Microsoft Power Apps administrators var izveidot lietotāja kontu un piešķirt lomu. Pēc tam varat doties <https://make.preview.powerapps.com/> uz, pieteikties, izmantojot šo lietotāja kontu, un vēlreiz mēģināt saites.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Simptoms: kādēļ naudas plūsmas prognozes darbvietas cilne Naudas plūsmas prognoze nerāda nekādus datus?

### <a name="resolution"></a>Novēršana

Naudas plūsmas prognozēšanas funkcija naudas plūsmas un banku pārvaldībā un naudas plūsmas prognožu līdzekli Finance Insights ir jāiestata un jāiespējo, lai pareizi parādītu datus **Naudas plūsmas prognozes** darbvietā.

Vispirms iestatiet un aktivizējiet naudas plūsmas prognozes un likviditātes kontus. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../cash-bank-management/cash-flow-forecasting.md). Ja šis iestatījums ir pabeigts, bet nevarat redzēt sagaidāmos rezultātus, papildinformāciju skatiet sadaļā [Problēmu novēršanas naudas plūsmas prognozēšanas](../cash-bank-management/cash-flow-forecasting-tsg.md) iestatījumi.

Pēc tam apstipriniet, ka naudas plūsmas prognožu funkcija Finance Insights (**Naudas un bankas pārvaldība \> Iestatījumi \> Finance Insights \> Naudas plūsmas prognozes**) ir iespējota un ka AI modeļa apmācība ir pabeigta. Ja apmācība nav pabeigta, atlasiet **Prognoze tagad**, lai sāktu modeļu apmācību procesu.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Simptoms: kādēļ programmā Lifecycle Services nav redzama jauna Microsoft Dynamics pievienojumprogrammas poga?

### <a name="resolution"></a>Novēršana

Vispirms pārbaudiet, vai vides pārvaldnieka vai projekta īpašnieka loma ir piešķirta lietotājam, kurš ir pierakstījies, laukā Projekta drošības loma **pakalpojumā** **·** **·** Microsoft Dynamics Lifecycle Services (LCS). Jaunu pievienojumprogrammu instalācijai ir nepieciešama viena no šīm projekta drošības lomām.

Ja jums ir piešķirta pareizā projekta drošības loma, iespējams, būs jāatsvaidzina pārlūka logs, lai skatītu pogu Instalēt **jaunu** pievienojumprogrammu.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Simptoms: Nešķist instalēt finanšu ieskatu pievienojumprogrammu. Kādēļ tas ir?

### <a name="resolution"></a>Novēršana

Šādiem soļiem jābūt pabeigtiem.

- Pārbaudiet, vai jums **ir sistēmas administratora un sistēmas** **pielāgotāja** piekļuve Power Portal administratora centrā.
- Pārbaudiet, vai Dynamics 365 Finance vai vai vai licences numurs attiecas uz lietotāju, kurš instalē pievienojumprogrammu.
- Pārbaudiet, vai Azure AD šī programma ir Azure AD reģistrēta: 

  | Pieteikums                  | Programmas ID           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
