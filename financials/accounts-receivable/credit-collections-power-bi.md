---
title: "Power BI satura pakotne Kredītu un iekasēšanas pārvaldība"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Kredītu un iekasēšanas pārvaldība. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c066e1a190a5536ad67368b4e059ab6bc66718e6
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Power BI satura pakotne Kredītu un iekasēšanas pārvaldība

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Kredītu un iekasēšanas pārvaldība**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Kredītu un iekasēšanas pārvaldība** ir izveidota kredītu un iekasēšanas vadītāju un iekasēšanas dienesta darbinieku vajadzībām. Tā nodrošina informāciju par galvenajiem kredītu un iekasēšanas rādītājiem, piemēram, vidējo maksājuma saņemšanas laiku, nokavēto bilanci, kredītrisku un debitoriem, kuri ir pārsnieguši kredīta limitu. Tajā tiek izmantoti transakciju dati, un tā nodrošina visu uzņēmumu kredīta un iekasēšanas transakciju apkopotus skatus. Tā nodrošina arī sadalījumu pēc uzņēmuma, debitoru grupas un debitora.

Šajā Power Bi satura pakotnē ir ietvertas 10 pārskatu lapas, kas ir norādītas tālāk.

- Divi apskata lapas (viena kredītu pārskata lapa un viena iekasēšanas pārskata lapa)
- Astoņas detalizētas informācijas lapas, kas sniedz detalizētu informāciju par kredītu un iekasēšanas rādītājiem, kuri ir norādīti atbilstoši dažādām dimensijām

Visas summas ir norādītas sistēmas valūtā. Sistēmas valūtu varat iestatīt lapā **Sistēmas parametri**.

Pēc noklusējuma tiek rādīti pašreizējā uzņēmuma kredītu un iekasēšanas dati. Lai skatītu visu uzņēmumu datus, piešķiriet lomai pienākumu **CustCollectionsBICrossCompany**.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Ja lietojat programmatūras Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise 2017. gada jūlija atjauninājumu, Power BI satura pakotne **Kredītu un iekasēšanas pārvaldība** tiek rādīts darbvietā **Debitoru kredīti un iekasēšana**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Satura pakotnē **CustCollectionsBICrossCompany** ir ietverts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts pārskats par Power BI satura pakotnē **CustCollectionsBICrossCompany** ietvertajām vizualizācijām.

| Pārskata lapa                 | Vizualizēšana |
|-----------------------------|---------------|
| Pārskats par iekasēšanu        | <ul><li>Debitori ar nokavētu termiņu</li><li>Debitori, kam pārsniegts kredīta limits</li><li>DSO 30 dienās</li><li>Atvērtie pieteikumi</li><li>Vidējais dienu skaits līdz pieteikuma slēgšanai</li><li>Atvērtās aktivitātes</li><li>Vidējais dienu skaits līdz aktivitāšu slēgšanai</li><li>Atvērtie procentu paziņojumi</li><li>Atvērtās atgādinājuma vēstules</li><li>Debitora aizturēšana</li><li>Pārdošanas aizturēšana</li><li>Vecas bilances</li><li>Iekasēšanas statusa summas</li><li>Iekasēšanas koda summas</li><li>Norakstīšana pēc iemesla</li><li>Bilances apmaksai pēc reģiona</li><li>Paredzētie maksājumi</li></ul> |
| Pārskats par kredītu             | <ul><li>Debitori ar nokavētu termiņu</li><li>Kredīta limita un apmaksājamās bilances salīdzinājums</li><li>Debitori, kuri ir pārsnieguši kredīta limitu (režģis)</li><li>Debitori, kam pārsniegts kredīta limits, pēc uzņēmuma</li><li>Izmantotā kredīta un kopējā kredīta limita salīdzinājums</li><li>Kredīta limits salīdzinājumā ar izmantoto kredītu pēc reģiona</li><li>Debitori pēc kredītreitinga</li></ul> |
| Kredīta limits                | <ul><li>Kredīta limits</li><li>Detalizēta informācija par kredīta limitu</li><li>Kredīta limits pēc debitora</li><li>Kredīta limits pēc debitoru grupas</li><li>Kredīta limits pēc kredītreitinga katram uzņēmumam</li><li>Kredīta limits salīdzinājumā ar izmantoto kredītu pēc reģiona</li></ul> |
| Debitori, kam pārsniegts kredīta limits | <ul><li>Debitori, kam pārsniegts kredīta limits</li><li>Detalizēta informācija par debitoriem, kuri ir pārsnieguši kredīta limitu</li><li>Debitori, kam pārsniegts kredīta limits, pēc uzņēmuma</li><li>Debitori, kas ir pārsnieguši kredīta limitu, pēc debitoru grupas</li><li>Debitori, kam pārsniegts kredīta limits, pēc reģiona</li></ul> |
| Debitori ar nokavētu termiņu          | <ul><li>Debitori ar nokavētu termiņu</li><li>Detalizēta informācija par debitoriem ar nokavētu termiņu</li><li>Debitori ar nokavētu termiņu pēc uzņēmuma</li><li>Debitori ar nokavētu termiņu pēc debitoru grupas</li><li>Debitori ar nokavētu termiņu pēc reģiona</li></ul> |
| Vecas bilances               | <ul><li>Vecas bilances</li><li>Detalizēta informācija par vecajām bilancēm</li><li>Vecās bilances pēc uzņēmuma</li><li>Vecās bilances pēc debitoru grupas</li></ul> |
| Paredzētie maksājumi           | <ul><li>Paredzētie maksājumi</li><li>Detalizēta informācija par paredzētajiem maksājumiem</li><li>Paredzētie maksājumi pēc uzņēmuma</li><li>Paredzētie maksājumi pēc debitoru grupas</li><li>Paredzētie maksājumi pēc reģiona</li></ul> |
| Norakstīšana                  | <ul><li>Norakstīšana pēc reģiona</li><li>Detalizēta informācija par norakstīšanu</li><li>Norakstīšana pēc galvenā konta</li><li>Norakstīšana pēc uzņēmuma</li><li>Norakstīšana pēc debitoru grupas</li><li>Norakstīšana pēc reģiona</li></ul> |
| Iekasēšanas gadījumu statuss          | <ul><li>Apstrīdēts</li><li>Neizpildītais apmaksas solījums</li><li>Apsolīta samaksa</li><li>Detalizēta informācija par iekasēšanas statusu</li><li>Iekasēšanas statusa summas</li><li>Atvērtie pieteikumi</li><li>Atvērtās aktivitātes</li></ul> |
| Atgādinājuma vēstules         | <ul><li>Atgādinājuma koda summas</li><li>Detalizēta informācija iekasēšanas koda summu</li><li>Atgādinājuma vēstules summa pēc uzņēmuma</li><li>Atgādinājuma vēstules summa pēc debitoru grupas</li><li>Atgādinājuma vēstules summa pēc reģiona</li></ul> |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet sadaļā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Varat arī izmantot pamata datu eksportēšanas funkciju, lai eksportētu vizualizācijā apkopotos pamata datus.

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Dynamics 365 for Finance and Operations. Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai.

Power BI satura pakotne **Kredītu un iekasēšanas pārvaldība** ir pieejama LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Noteikti lejupielādējiet Power BI satura pakotni **Kredītu un iekasēšanas pārvaldība**, kas ir paredzēta jūsu Dynamics 365 for Finance and Operations versijai.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Power BI satura pakotnes **Kredītu un iekasēšanas pārvaldība** pārskata aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-integration-entity-store).

| Elements                                      | Galvenie apkopošanas mērījumi           | Datu avots                                 | Lauks                                                      | apraksts |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Slēgto aktivitāšu skaits un vidējais šo aktivitāšu slēgšanas laiks. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Atvērto aktivitāšu skaits. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Veco bilanču summa. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Summas, kuru apmaksa ir nokavēta. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Slēgto pieteikumu skaits un vidējais šo pieteikumu slēgšanas laiks. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Atvērto pieteikumu skaits. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Atvērto atgādinājuma vēstuļu skaits. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Grāmatoto atgādinājuma vēstuļu bilance. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Transakciju ar iekasēšanas statusu bilance. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Kredītriska summa un debitoru kredīta limita pārsniegšanas summas |
| CustCollectionsBICustOnHold                 | Bloķēta                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Aizturēto debitoru skaits. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Vidējais maksājuma saņemšanas laiks 30 dienās. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Nākamā gada laikā paredzēto maksājumu summa. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Izveidoto procentu paziņojumu skaits. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Visu aizturēto pārdošanas pasūtījumu skaits. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Norakstīto transakciju summa. |

