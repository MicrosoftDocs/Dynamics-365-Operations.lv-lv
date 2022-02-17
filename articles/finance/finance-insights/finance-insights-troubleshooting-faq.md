---
title: Finance Insights iestatījumu problēmu novēršana
description: Šajā tēmā uzskaitītas problēmas, kas var rasties, kad izmantojat Finance Insights iespējas. Tajā arī skaidrots, kā atrisināt šos jautājumus.
author: panolte
ms.date: 01/29/2022
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
ms.openlocfilehash: f77cddfdab22bef8af7f62d49723e330c4f13261
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064870"
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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Simptoms: mēģinot atvērt AI Builder izmantojot saites Klientu maksājumu prognožu iestatīšanas lapā, kāpēc tiek parādīts šāds kļūdas ziņojums: "Atvainojiet, ir noticis atvienojums"?

### <a name="resolution"></a>Novēršana

Dynamics 365 Finance lietotājiem ir jābūt a Microsoft Power Apps lietotāja konts videi, un šim lietotāja kontam ir jābūt sistēmas pielāgotāja lomai. The Microsoft Power Apps sistēmas administrators var izveidot lietotāja kontu un piešķirt lomu. Pēc tam varat doties uz<https://make.preview.powerapps.com/>, piesakieties, izmantojot šo lietotāja kontu, un vēlreiz mēģiniet izveidot saites.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Simptoms: kādēļ naudas plūsmas prognozes darbvietas cilne Naudas plūsmas prognoze nerāda nekādus datus?

### <a name="resolution"></a>Novēršana

Naudas plūsmas prognozēšanas funkcija naudas plūsmas un banku pārvaldībā un naudas plūsmas prognožu līdzekli Finance Insights ir jāiestata un jāiespējo, lai pareizi parādītu datus **Naudas plūsmas prognozes** darbvietā.

Vispirms iestatiet un aktivizējiet naudas plūsmas prognozes un likviditātes kontus. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../cash-bank-management/cash-flow-forecasting.md). Ja šis iestatījums ir pabeigts, bet nevarat redzēt sagaidāmos rezultātus, papildinformāciju skatiet sadaļā [Problēmu novēršanas naudas plūsmas prognozēšanas](../cash-bank-management/cash-flow-forecasting-tsg.md) iestatījumi.

Pēc tam apstipriniet, ka naudas plūsmas prognožu funkcija Finance Insights (**Naudas un bankas pārvaldība \> Iestatījumi \> Finance Insights \> Naudas plūsmas prognozes**) ir iespējota un ka AI modeļa apmācība ir pabeigta. Ja apmācība nav pabeigta, atlasiet **Prognoze tagad**, lai sāktu modeļu apmācību procesu.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Simptoms: kāpēc nav redzama poga Instalēt jaunu pievienojumprogrammu Microsoft Dynamics Dzīves cikla pakalpojumi?

### <a name="resolution"></a>Novēršana

Vispirms pārbaudiet, vai **Vides vadītājs** vai **Projekta īpašnieks** loma ir piešķirta lietotājam, kas ir pierakstījies **Projekta drošības loma** lauks iekšā Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Jauno pievienojumprogrammu instalēšanai ir nepieciešama viena no šīm projekta drošības lomām.

Ja jums ir piešķirta pareizā projekta drošības loma, iespējams, būs jāatsvaidzina pārlūkprogrammas logs, lai redzētu **Instalējiet jaunu pievienojumprogrammu** pogu.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Simptoms: šķiet, ka finanšu ieskatu pievienojumprogramma netiek instalēta. Kāpēc ir tā, ka?

### <a name="resolution"></a>Novēršana

Tālāk norādītās darbības bija jāpabeidz.

- Pārbaudiet, vai jums ir **Sistēmas administrators** un **Sistēmas pielāgotājs** piekļūt Power Portal administrēšanas centrā.
- Pārbaudiet, vai a Dynamics 365 Finance vai līdzvērtīga licence tiek piemērota lietotājam, kurš instalē pievienojumprogrammu.
- Pārbaudiet, vai tālāk norādītais Azure AD lietotne ir reģistrēta Azure AD: 

  | Pieteikums                  | Programmas ID           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Simptoms: Kļūda: “Mēs neatradām nekādus datus atlasītajam filtra diapazonam. Lūdzu, atlasiet citu filtra diapazonu un mēģiniet vēlreiz. 

### <a name="resolution"></a>Novēršana

Pārbaudiet datu integratora iestatījumus, lai pārbaudītu, vai tas darbojas, kā paredzēts, un pārveido datus no AI Builder atpakaļ uz finansēm.  
Papildinformāciju skatiet [Izveidojiet datu integrācijas projektu](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Simptoms: klientu maksājumu prognozēšanas apmācība neizdevās, un AI Builder kļūdu stāvokļi: "Lai apmācītu modeli, prognozēšanai ir jābūt tikai 2 atšķirīgām iznākuma vērtībām. Kartējiet ar diviem rezultātiem un pārkvalificējiet", "Apmācības ziņojuma problēma: IsNotMinRequiredDistinctNonNullValues".

### <a name="resolution"></a>Novēršana

Šī kļūda norāda, ka pēdējā gadā nav pietiekami daudz vēsturisku darījumu, kas atbilst katrai kategorijā aprakstītajai kategorijai **Laikā**, **·**, un **Ļoti vēlu** kategorijām. Lai novērstu šo kļūdu, pielāgojiet **Ļoti vēlu** darījuma periods. Ja regulējat **Ļoti vēlu** darījuma periods neizlabo kļūdu, **Klientu maksājumu prognozes** nav labākais risinājums, jo tam ir nepieciešami dati katrā kategorijā apmācības nolūkos.

Lai iegūtu papildinformāciju par to, kā pielāgot **Laikā**, **·**, un **Ļoti vēlu** kategorijas, sk [Iespējot klientu maksājumu prognozes](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Simptoms: modeļa apmācība neizdevās

### <a name="resolution"></a>Novēršana

The **Naudas plūsmas prognoze** modeļu apmācībai ir nepieciešami dati, kas aptver vairāk nekā vienu gadu un satur vairāk nekā 100 darījumus. Šiem darījumiem ir jāietekmē likviditātes konti, kas ir iekļauti naudas plūsmas prognozes iestatījumos.

The **Klientu maksājumu prognozes** Lai izveidotu prognozes, pēdējo sešu līdz deviņu mēnešu laikā ir nepieciešami vismaz 100 klienta rēķini un maksājumu darījumi.  
