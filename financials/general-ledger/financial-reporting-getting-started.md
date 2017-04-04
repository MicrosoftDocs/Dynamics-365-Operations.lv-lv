---
title: "Finanšu pārskati"
description: "Šajā tēmā ir aprakstīts, kur piekļūt finanšu pārskatu Microsoft Dynamics 365 operācijām un kā izmantot finanšu atskaišu veidošanas iespējas. Tā ietver aprakstu par noklusējuma finanšu pārskatus, kas sniegti."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Finanšu pārskati

Šajā tēmā ir aprakstīts, kur piekļūt finanšu pārskatu Microsoft Dynamics 365 operācijām un kā izmantot finanšu atskaišu veidošanas iespējas. Tā ietver aprakstu par noklusējuma finanšu pārskatus, kas sniegti.

<a name="accessing-financial-reporting"></a>Piekļuve finanšu atskaišu veidošanai
-----------------------------

Jūs varat atrast **finanšu pārskatu** izvēlne tālāk ievieto Dynamics 365 operācijām:

-   **Virsgrāmatas**&gt;**uzziņās un pārskatos**
-   **Budžeta**&gt;**Inquires un atskaites**&gt;**pamata paredzēšana budžetā**
-   **Budžeta**&gt;**uzziņās un pārskatos**&gt;**budžeta plānošanu**
-   **Budžeta**&gt;**uzziņās un pārskatos**&gt;**budžeta kontroles**
-   Konsolidācija

Lai izveidotu un ģenerētu finanšu atskaites kādai juridiskajai personai, šai juridiskajai personai jums ir jāiestata šāda informācija:

-   Finanšu kalendārs
-   Virsgrāmata
-   Kontu diagramma
-   Valūta

Finanšu atskaišu veidošanas funkcijas ir pieejamas lietotājiem, kam ir piešķirtas atbilstošās privilēģijas un pienākumi, izmantojot viņu drošības lomas. Nākamajās sadaļās šīs privilēģijas un pienākumi ir uzskaitīti kopā ar saistītajām lomām.

### <a name="duties"></a>Pienākumi

| Pienākuma etiķete                            | Apraksts                                                             | AOT nosaukums                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Uzturēt finanšu pārskatu drošību | Uzturēt finanšu atskaišu drošību un veikt administratīvos uzdevumus. | FinancialReportsSecurityMaintain |
| Uzturēt finanšu pārskatus            | Projektēt un uzturēt finanšu atskaites.                                  | FinancialReportsMaintain         |
| Ģenerēt finanšu pārskatus            | Ģenerēt un atsvaidzināt finanšu atskaites.                                 | FinancialReportsGenerate         |
| Pārskatīt finanšu darbību          | Pārskatīt un analizēt finanšu veiktspēju.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Privilēģijas

| Privilēģijas etiķete                       | Apraksts                                                             | AOT nosaukums                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Uzturēt finanšu pārskatu drošību | Uzturēt finanšu atskaišu drošību un veikt administratīvos uzdevumus. | FinancialReportsSecurityMaintain |
| Uzturēt finanšu pārskatus            | Projektēt un uzturēt finanšu atskaites.                                  | FinancialReportsMaintainReports  |
| Ģenerēt finanšu pārskatus            | Ģenerēt un atsvaidzināt finanšu atskaites.                                 | FinancialReportsGenerateReports  |
| Skatīt finanšu pārskatus                | Skatīt finanšu atskaites.                                                 | FinancialReportsView             |

### <a name="roles"></a>Lomas

| Privilēģijas etiķete                       | Pienākums                                  | Lomas                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Uzturēt finanšu pārskatu drošību | Uzturēt finanšu pārskatu drošību | Drošības administrators                                                          |
| Uzturēt finanšu pārskatus            | Uzturēt finanšu pārskatus            | Grāmatvedības vadītājs, grāmatvedības vadītājs, finanšu kontrolieris, budžeta Manager |
| Ģenerēt finanšu pārskatus            | Ģenerēt finanšu pārskatus            | CEO, CFO, grāmatvede                                                            |
| Skatīt finanšu pārskatus                | Pārskatīt finanšu darbību          | Nav piešķirts                                                                   |

Kad lietotājs ir pievienots vai loma ir mainīta, lietotājam dažu minūšu laika ir jāspēj piekļūt finanšu atskaišu veidošanai. **Piezīme:** sistēmas administratora lomas dalībniekam tiek pievienots visiem posteņiem finanšu pārskatos.

## <a name="default-reports"></a>Noklusējuma pārskati
Finanšu atskaišu veidošana nodrošina 22 noklusējuma finanšu atskaites. Katra atskaite izmanto galveno kontu noklusējuma kategorijas Dynamics 365 operācijām. Šīs atskaites varat lietot tādas, kādas tās ir, vai kā sākuma punktu savām finanšu atskaišu veidošanas nepieciešamībām. Papildus tradicionālajiem finanšu pārskatiem, piemēram, peļņas vai zaudējumu aprēķinam un bilancei, šīs noklusējuma atskaites ietver atskaites, kurās ir redzami dažādie finanšu atskaišu veidi, ko varat izveidot. Katrā ziņojumā šādu tabulu saites uz Office Mix prezentāciju par pārskatu.

| Noklusējuma pārskats                                                                                         | apraksts                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | Skatiet organizācijas ienesīgumu pēdējos 12 mēnešos vienā kolonnā.                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | Skatiet organizācijas ienesīgumu katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | Skatiet detalizētu bilances informāciju par visiem kontiem sākotnējā budžetā un pārskatīto budžetu salīdziniet ar faktiskajām vērtībām, kam ir novirzes.                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances pārskata valūtā un vietējā valūtā, kā arī papildu informācija par transakcijām, piemēram, lietotāja ID, lietotājs, kurš pēdējais modificēja datus, pēdējās modifikācijas datums un žurnāla ID. |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas sākuma un beigu bilances un debeta un kredīta bilances pašreizējam periodam un šim gadam, kā arī papildu informācija par transakcijām, piemēram, dokuments.                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu.                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | Skatiet organizācijas finansiālo pozīciju un ienesīguma attiecībā uz gadu vienu otram līdzās.                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | Gūstiet ieskatu par organizācijā ieplūstošo un no tas izplūstošo naudu.                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Skatiet sākuma bilanci un aktivitāšu informāciju visiem kontiem.                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Skatiet informāciju par bilanci visiem kontiem, kuriem ir debeta un kredīta bilances, kā arī šo bilanču neto summu, kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | Gūstiet ieskatu par izdevumiem pēdējos 12 ceturkšņos iepriekšējo trīs gadu laikā.                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Skatiet apskatu par bilancēm un aktivitātēm attiecībā uz līdzekļa, saistību, īpašnieka kapitāla, ieņēmumu, izdevumu, peļņas vai zaudējumu finanšu sadaļām.                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Skatiet organizācijas ienesīgumu pašreizējam periodam un šim gadam.                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances, kā arī papildu informācija par transakciju, piemēram, transakcijas datums, žurnāla numurs, dokuments, grāmatošanas tips un izsekošanas numurs.                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | Skatiet maksātspēju, ienesīgumu un efektivitātes koeficientus organizācijai attiecībā uz gadu.                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | Gūstiet ieskatu par izdevumiem katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Skatīt uzņēmuma rentabilitātes katru ceturksni pagājušajā gadā un līdz šim gadam.                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu. Šajā atskaitē līdzās tiek rādīti aktīvi un saistības, kā arī akcionāru kapitāls.                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Skatiet bilances informāciju visiem kontiem, kam ir sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Skatīt visus kontus, kuriem ir sākuma un beigu bilances un debeta un kredīta atlikumus, kopā ar to neto starpība kārtējam gadam un pagājušajā gadā bilances informāciju.                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | Gūstiet ieskatu par pārdošanu un atlaidēm katrai mēneša nedēļai. Šajā atskaitē ir ietvertas četru nedēļu kopsummas.                                                                                                                                                                                                              |
| [Budžeta līdzekļus - noklusējuma](https://mix.office.com/watch/15hcpezcbx7tv)                         | Skatīt detalizētu salīdzinājumu pārskatītais budžets, faktiskie izdevumi budžeta atrunas, un budžeta līdzekļus, kas ir pieejami visiem kontiem                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finanšu atskaišu atvēršana
Kad noklikšķināt uz izvēlnes **Finanšu atskaišu veidošana**, tiek parādīts saraksts ar uzņēmuma noklusējuma finanšu atskaitēm. Pēc tam varat atvērt vai modificēt kādu atskaiti. Lai atvērtu kādu no noklusējuma atskaitēm, atlasiet atskaites nosaukumu. Kad atskaiti atverat pirmo reizi, tā tiek automātiski tiek ģenerēta par iepriekšējo mēnesi. Piemēram, ja atverat ziņojumu pirmo reizi augusta 2016, ziņojumā tiek ģenerēts 2016. gada 31 jūlijs. Pēc atskaites atvēršanas varat sākt to pētīt, detalizējot konkrētus datus un mainot atskaites opcijas.

## <a name="creating-and-modifying-financial-reports"></a>Finanšu atskaišu veidošana un modificēšana
No finanšu atskaišu saraksta varat izveidot jaunu atskaiti vai modificēt jau esošu atskaiti. Ja jums ir atbilstošas atļaujas, var izveidot jaunu finanšu atskaiti, noklikšķinot uz **New** darbību rūtī. Ziņojums dizaineru programma ir jāielādē ierīcē. Pēc atskaišu izstrādes rīks startē pēc tam var izveidot jaunu atskaiti. Kad esat saglabājis jauno atskaiti, tā kļūst redzama finanšu atskaišu sarakstā. Saraksts rāda tikai pārskatus, kas tika izveidota sabiedrība, kuru lietojat programmā Dynamics 365 operācijām. Plašāku informāciju par procesu, veidojot un modificējot finanšu atskaitēm programmā Dynamics 365 operācijām uz tiem atsaucamies [emuāra ziņas](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) no finanšu dinamiku pārskata blog. **Piezīme:** lejupielādējamo ziņojumu designer klienta, jābūt instalētai versijai 4.6.2 Microsoft .NET Framework instalēta tā datoru. Šo Microsoft .NET Framework versiju var lejupielādēt un instalēt no [te](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Ja izmantojat Chrome, lai lejupielādētu ziņojumu designer klienta jāinstalē ClickOnce paplašinājums. Ja izmantojat inkognito režīmu, pārliecinieties, vai ir iespējota ClickOnce paplašinājumu inkognito režīmā. Varat arī modificēt atskaiti, kas ir redzama finanšu atskaišu sarakstā. Kad ir atlasīts apgabals ap atskaites nosaukumu, darbību rūtī noklikšķiniet uz **Rediģēt**. Tiek palaista atskaišu veidotāja programma.

<a name="see-also"></a>Skatiet arī
--------

[View financial reports](view-financial-reports.md)

[Dynamics finanšu pārskatu veidošanas emuārs](http://blogs.msdn.com/b/dynamics_financial_reporting/)


