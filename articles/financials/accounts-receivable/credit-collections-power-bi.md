---
title: Power BI satura pakotne Kredītu un iekasēšanas pārvaldība
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Kredītu un iekasēšanas pārvaldība. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a80a180623d1cca77c633f12bcd92a088e089ee5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "325185"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Power BI satura pakotne Kredītu un iekasēšanas pārvaldība

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Kredītu un iekasēšanas pārvaldība**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Kredītu un iekasēšanas pārvaldība** ir izveidota kredītu un iekasēšanas vadītāju un iekasēšanas dienesta darbinieku vajadzībām. Tā nodrošina informāciju par galvenajiem kredītu un iekasēšanas rādītājiem, piemēram, vidējo maksājuma saņemšanas laiku, nokavēto bilanci, kredītrisku un debitoriem, kuri ir pārsnieguši kredīta limitu. Tajā tiek izmantoti transakciju dati, un tā nodrošina visu uzņēmumu kredīta un iekasēšanas transakciju apkopotus skatus. Tā nodrošina arī sadalījumu pēc uzņēmuma, debitoru grupas un debitora.

Šajā Power BIi satura pakotnē ir ietvertas 10 pārskatu lapas, kas ir norādītas tālāk.

- Divi apskata lapas (viena kredītu pārskata lapa un viena iekasēšanas pārskata lapa)
- Astoņas detalizētas informācijas lapas, kas sniedz detalizētu informāciju par kredītu un iekasēšanas rādītājiem, kuri ir norādīti atbilstoši dažādām dimensijām

Visas summas ir norādītas sistēmas valūtā. Sistēmas valūtu varat iestatīt lapā **Sistēmas parametri**.

Pēc noklusējuma tiek rādīti pašreizējā uzņēmuma kredītu un iekasēšanas dati. Lai skatītu visu uzņēmumu datus, piešķiriet lomai pienākumu **CustCollectionsBICrossCompany**.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Kredītu un iekasēšanas pārvaldība** tiek rādīta darbvietā **Debitoru kredīti un iekasēšana**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Power BI satura pakotnē **CustCollectionsBICrossCompany** ir ietverts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts apskats par vizualizācijām Power BI satura pakotnē **CustCollectionsBICrossCompany**.

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

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Varat arī izmantot pamata datu eksportēšanas funkciju, lai eksportētu vizualizācijā apkopotos pamata datus.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Power BI satura pakotnes **Kredītu un iekasēšanas pārvaldība** pārskata aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet rakstā [Apskats par Power BI integrāciju elementu krātuvē](../../dev-itpro/analytics/power-bi-integration-entity-store.md).


|                   Elements                    |      Galvenie apkopošanas mērījumi      |             Datu avots              |                           Lauks                            |                                    Apraksts                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  |            smmActivities             | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) |     Slēgto aktivitāšu skaits un vidējais šo aktivitāšu slēgšanas laiks.     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           Atvērto aktivitāšu skaits.                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             Veco bilanču summa.                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           Summas, kuru apmaksa ir nokavēta.                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases, CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        Slēgto pieteikumu skaits un vidējais šo pieteikumu slēgšanas laiks.        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              Atvērto pieteikumu skaits.                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       Atvērto atgādinājuma vēstuļu skaits.                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     Grāmatoto atgādinājuma vēstuļu bilance.                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                Transakciju ar iekasēšanas statusu bilance.                 |
|           CustCollectionsBICredit           | CreditExposed, AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed), Sum(AmountOverCreditLimit)       | Kredītriska summa un debitoru kredīta limita pārsniegšanas summas |
|         CustCollectionsBICustOnHold         |               Bloķēta                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     Aizturēto debitoru skaits.                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        Vidējais maksājuma saņemšanas laiks 30 dienās.                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 Nākamā gada laikā paredzēto maksājumu summa.                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                Izveidoto procentu paziņojumu skaits.                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 Visu aizturēto pārdošanas pasūtījumu skaits.                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                Norakstīto transakciju summa.                 |

