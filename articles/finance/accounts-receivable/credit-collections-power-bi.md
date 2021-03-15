---
title: Power BI satura pakotne Kredītu un iekasēšanas pārvaldība
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Kredītu un iekasēšanas pārvaldība. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: dc68926b8123c7e513f9df46e2b9f9b8ae1311e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979143"
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

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI satura skatīšanai nepieciešamie iestatījumi

Lai dati tiktu rādīti darbvietas **Debitoru kredīti un iekasēšana** Power BI vizuālajos līdzekļos, ir jāveic tālāk norādītā iestatīšana.

1. Dodieties uz **Sistēmas administrēšana > Iestatīšana > Sistēmas parametri** un iestatiet parametrus **Sistēmas valūta** un **Sistēmas maiņas kurss**.
2. Lai validētu finanšu kalendāra datumus, kas piešķirti aktīvajam laika periodam, dodieties uz **Virsgrāmata > Kalendāri > Finanšu kalendāri**.
3. Dodieties uz **Virsgrāmata > Iestatīšana > Virsgrāmata** un iestatiet vienumu **Uzskaites valūta** un **Maiņas kursa tips**.
4. Nosakiet maiņas kursu starp transakciju valūtām un uzskaites valūtu un starp uzskaites valūtu un sistēmas valūtu. Lai to izdarītu, dodieties uz **Virsgrāmata > Valūtas > Valūtas maiņas kursi**.
5. Dodieties uz **Sistēmas administrēšana > Iestatīšana > Elementu krātuve** un atsvaidziniet apkopošanas mērījumu **CustCollectionsBIMeasurementsV2**.

>[!NOTE] 
> Novecošanas perioda definīcijas jāiestata **Debitoru parametri > Kolekcijas > Kolekciju noklusējums**, lai iespējotu novecošanas datus Power BI saturā.

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

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Varat arī izmantot pamata datu eksportēšanas funkciju, lai eksportētu vizualizācijā apkopotos pamata datus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]