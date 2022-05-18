---
title: Finance Insights iestatījumu problēmu novēršana
description: Šajā tēmā uzskaitītas problēmas, kas var rasties, kad izmantojat Finance Insights iespējas. Tajā arī skaidrots, kā atrisināt šos jautājumus.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 5669b414283013ae1de095de2201df066ab588dd
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725910"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insights iestatījumu problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā uzskaitītas problēmas, kas var rasties, kad izmantojat Finance Insights iespējas. Tajā arī skaidrots, kā atrisināt šos jautājumus.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Simptoms: Kādēļ nevar kartēt debitoru maksājumu ieskatu datu integrācijas veidnes mērķa kolonnu?

### <a name="resolution"></a>Novēršana

Iespējams, ka agrākai versijai izmantojat veidni. Pirms versijas 10.0.17 izlaišanas priekšskatiet debitorus, kuri konfigurēja **Debitora maksājuma ieskatu rezultātus (CDS uz Fin un Ops)** Datu integrācijas (DI) veidni, izmantojot **Maksājumu prognozēšanas rezultātu (priekšskatījuma)** elementu. Pēc jaunināšanas uz 10.0.17 vai jaunāku versiju, ir jāizmanto **Debitoru maksājumu ieskatu rezultāti (CDS uz Fin un Ops 10.0.17 vai jaunāka versija)** DI veidne, lai pabeigtu kartēšanu. Iespējams, ka nevarēsit kartēt DI veidnes mērķa kolonnu, kamēr datu pārvaldības elementu saraksts nav atsvaidzināts un tajā tiek parādīts **Maksājumu prognozēšanas rezultāta** elements. Lai atsvaidzinātu elementu sarakstu un rādītu maksājumu prognozēšanas rezultātu, Microsoft Dynamics izpildīsiet darbības gan finansēs 365 Dataverse, gan (iepriekš zināmas kā Common Data Service\[CDS\] administratora portāls).

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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Simptoms: Kad mēģinu atvērt AI Builder, izmantojot saites debitora maksājumu prognozēšanas iestatījumu lapā, kāpēc es saņemu šādu kļūdas ziņojumu: "Diemžēl ir bijis atvienošanās"?

### <a name="resolution"></a>Novēršana

Dynamics 365 finanšu lietotājiem jābūt Microsoft Power Apps vides lietotāja kontam un šim lietotāja kontam jābūt sistēmas pielāgotāja lomai. Sistēmas Microsoft Power Apps administrators var izveidot lietotāja kontu un piešķirt lomu. Pēc tam varat doties uz <https://make.preview.powerapps.com/>, pieteikties, izmantojot šo lietotāja kontu, un vēlreiz mēģināt saites.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Simptoms: kādēļ naudas plūsmas prognozes darbvietas cilne Naudas plūsmas prognoze nerāda nekādus datus?

### <a name="resolution"></a>Novēršana

Naudas plūsmas prognozēšanas funkcija naudas plūsmas un banku pārvaldībā un naudas plūsmas prognožu līdzekli Finance Insights ir jāiestata un jāiespējo, lai pareizi parādītu datus **Naudas plūsmas prognozes** darbvietā.

Vispirms iestatiet un aktivizējiet naudas plūsmas prognozes un likviditātes kontus. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../cash-bank-management/cash-flow-forecasting.md). Ja šis iestatījums ir pabeigts, bet nevarat redzēt sagaidāmos rezultātus, papildinformāciju skatiet sadaļā [Problēmu novēršanas naudas plūsmas prognozēšanas](../cash-bank-management/cash-flow-forecasting-tsg.md) iestatījumi.

Pēc tam apstipriniet, ka naudas plūsmas prognožu funkcija Finance Insights (**Naudas un bankas pārvaldība \> Iestatījumi \> Finance Insights \> Naudas plūsmas prognozes**) ir iespējota un ka AI modeļa apmācība ir pabeigta. Ja apmācība nav pabeigta, atlasiet **Prognoze tagad**, lai sāktu modeļu apmācību procesu.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Simptoms: kādēļ programmā Lifecycle Services nav Microsoft Dynamics redzama jauna pievienojumprogrammas poga?

### <a name="resolution"></a>Novēršana

Vispirms pārbaudiet, vai **vides** **·** **pārvaldnieka** vai projekta īpašnieka loma ir piešķirta lietotājam, Microsoft Dynamics kurš ir pierakstījies, laukā Projekta drošības loma pakalpojumā Lifecycle Services (LCS). Jaunu pievienojumprogrammu instalācijai ir nepieciešama viena no šīm projekta drošības lomām.

Ja jums ir piešķirta pareizā projekta drošības loma, iespējams, būs jāatsvaidzina pārlūka logs, lai skatītu **pogu Instalēt jaunu pievienojumprogrammu**.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Simptoms: Nešķist instalēt finanšu ieskatu pievienojumprogrammu. Kādēļ tas ir?

### <a name="resolution"></a>Novēršana

Šādiem soļiem jābūt pabeigtiem.

- Pārbaudiet, vai jums ir **sistēmas administratora** un **sistēmas pielāgotāja** piekļuve Power Portal administratora centrā.
- Pārbaudiet, vai Dynamics 365 finanšu vai ekvivalenta licence ir lietota lietotājam, kurš instalē šo pievienojumprogrammu.
- Pārbaudiet, vai šī Azure AD programma ir reģistrēta Azure AD: 

  | Pieteikums                  | Programmas ID           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Simptoms: kļūda: "Mēs neatradām datus atlasītajam filtra diapazonam. Lūdzu, atlasiet citu filtru diapazonu un mēģiniet vēlreiz." 

### <a name="resolution"></a>Novēršana

Pārbaudiet datu integrētāja iestatījumus, lai apstiprinātu, ka tā darbojas, kā paredzēts, un apstiprinātu datus no atpakaļ AI Builder uz Finansēm.  
Papildinformāciju skatiet sadaļā [Datu integrācijas projekta izveide](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Simptoms: neizdevās debitora maksājuma prognozēšanas AI Builder apmācība, un kļūdas gadījumi: "Prognozēšana drīkst būt tikai 2 atšķirīgas rezultātu vērtības, lai varētu veikt modeļa apmācību. Kartēt uz diviem rezultātiem un pārdalīt", "Apmācību pārskata problēma: IsNotMinRequiredDistinctNonNullValues".

### <a name="resolution"></a>Novēršana

Šī kļūda norāda, ka pēdējā **gadā** nav pietiekami daudz vēsturisko darbību, kas norāda katru kategoriju, kas aprakstīta kategorijās Pēc laika, **Vēls** un **Ļoti vēlu**. Lai atrisinātu šo kļūdu, koriģējiet ļoti **vēlu** darbības periodu. Ja koriģējot ļoti **vēlu** darbības periodu, kļūdu nelabo, **debitora** maksājumu prognozes nav labākais risinājums, ko izmantot, jo apmācību nolūkiem tajā ir nepieciešami dati katrā kategorijā.

Papildinformāciju par to, kā pielāgot laika **,** **nokavētas** un ļoti vēlu **kategorijas**, skatiet sadaļā Iespējot debitora [maksājumu prognozes](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Simptoms: Modeļu apmācība neizdevās

### <a name="resolution"></a>Novēršana

Naudas **plūsmas prognozes modeļa** apmācībai nepieciešami dati, kas satur 100 vai vairāk darbības, kas aptver vairāk par gadu. Ieteicams, lai jums būtu vismaz divi gadi datu ar vairāk nekā 1000 darbībām.

Debitora **maksājuma prognozēšanas līdzeklim ir nepieciešamas vairāk nekā 100 darbības iepriekšējos** sešos līdz deviņiem mēnešiem. Darbībās var būt iekļauti brīvā teksta rēķini, pārdošanas pasūtījumi un debitoru maksājumi. Šie dati ir izplatīti pa konfigurācijas **lapā noteiktām** laic pieejamiem, **nokavētiem** **un** ļoti vēliem **iestatījumiem**.    

Budžeta **priekšlikuma funkcijai** nepieciešami vismaz trīs budžeta gadi vai faktiskie dati. Šis risinājums izmanto trīs līdz desmit projekciju datu gadiem. Vairāk nekā trīs gadi dos labākus rezultātus. Pats dati darbojas vislabāk, ja vērtības ir variācijas. Ja datos ir visi nemainīgie dati, piemēram, nomas izdevumi, apmācība var neizdoties, jo, nepastāvot variācijām, AI nav jāprojektē summas.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Simptoms: kļūdas ziņojums norāda, ka "Tabula ar nosaukumu" "msdyn_paypredpredictionresultentities" nepastāv. Attālais serveris atgrieza kļūdu: (404) Nav atrasts..."

### <a name="resolution"></a>Novēršana

Vide ir sasniegusi datu pārsūtīšanas pakalpojumu maksimālo tabulas ierobežojumu. Papildinformāciju par limitu skatiet **tēmas** sadaļā Iespējot reāllaika datu izmaiņu tuvu atrašanās vietu, pārskatu [Eksportēt uz Azure data Atkat.](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md)
