---
title: "Finanšu pārskati"
description: "Šajā tēmā ir aprakstīts, kur programmatūrā Microsoft Dynamics 365 for Finance and Operations, izdevumā Enterprise var piekļūt finanšu pārskatiem un kā lietot finanšu pārskatu iespējas. Tajā ir ietverts nodrošināto noklusējuma finanšu pārskatu apraksts."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fedde78a563939fd7080e748c412c89c71586823
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="financial-reporting"></a>Finanšu pārskati

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kur programmatūrā Microsoft Dynamics 365 for Finance and Operations, izdevumā Enterprise var piekļūt finanšu pārskatiem un kā lietot finanšu pārskatu iespējas. Tajā ir ietverts nodrošināto noklusējuma finanšu pārskatu apraksts.

<a name="accessing-financial-reporting"></a>Piekļuve finanšu atskaišu veidošanai
-----------------------------

Izvēlne **Finanšu pārskati** programmatūrā Finance and Operations ir pieejama tālāk norādītajās vietās.

-   **Virsgrāmata** &gt; **Pieprasījumi un pārskati**
-   **Budžeta veidošana** &gt; **Pieprasījumi un pārskati** &gt; **Pamata budžeta veidošana**
-   **Budžeta veidošana** &gt; **Pieprasījumi un pārskati** &gt; **Budžeta plānošana**
-   **Budžeta veidošana** &gt; **Pieprasījumi un pārskati** &gt; **Budžeta kontrole**
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
| Uzturēt finanšu pārskatus            | Uzturēt finanšu pārskatus            | Uzskaites vadītājs, Uzskaites supervizors, Finanšu kontrolieris, Budžeta pārvaldnieks |
| Ģenerēt finanšu pārskatus            | Ģenerēt finanšu pārskatus            | Direktors (CEO), Finanšu direktors (CFO), Grāmatvedis                                                            |
| Skatīt finanšu pārskatus                | Pārskatīt finanšu darbību          | Nav piešķirts                                                                   |

Kad lietotājs ir pievienots vai loma ir mainīta, lietotājam dažu minūšu laika ir jāspēj piekļūt finanšu atskaišu veidošanai. **Piezīme.** Visām finanšu pārskatu lomām tiek pievienota sistēmas administratora loma.

## <a name="default-reports"></a>Noklusējuma pārskati
Finanšu atskaišu veidošana nodrošina 22 noklusējuma finanšu atskaites. Viesiem pārskatiem programmatūrā Finance and Operations tiek izmantotas noklusējuma galvenā konta kategorijas. Šīs atskaites varat lietot tādas, kādas tās ir, vai kā sākuma punktu savām finanšu atskaišu veidošanas nepieciešamībām. Papildus tradicionālajiem finanšu pārskatiem, piemēram, peļņas vai zaudējumu aprēķinam un bilancei, šīs noklusējuma atskaites ietver atskaites, kurās ir redzami dažādie finanšu atskaišu veidi, ko varat izveidot. Visi tālāk esošajā tabulā norādītie pārskati ir saistīti ar Office Mix prezentāciju par attiecīgo pārskatu.

| Noklusējuma pārskats                                                                                         | Apraksts                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 mēnešu atritināšanas vienas kolonnas peļņas vai zaudējumu aprēķins — noklusējuma pārskats](https://mix.office.com/watch/76kc7bm3wnt1) | Skatiet organizācijas ienesīgumu pēdējos 12 mēnešos vienā kolonnā.                                                                                                                                                                                                                                      |
| [12 mēnešu tendenču peļņas vai zaudējumu aprēķins — noklusējuma pārskats](https://mix.office.com/watch/12brmfge5p8r)                 | Skatiet organizācijas ienesīgumu katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                             |
| [Faktiski pret budžetu — noklusējuma pārskats](https://mix.office.com/watch/fi439lkwr0no)                                | Skatiet detalizētu bilances informāciju par visiem kontiem sākotnējā budžetā un pārskatīto budžetu salīdziniet ar faktiskajām vērtībām, kam ir novirzes.                                                                                                                                                                          |
| [Detalizēta informācija par auditu — noklusējuma pārskats](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances pārskata valūtā un vietējā valūtā, kā arī papildu informācija par transakcijām, piemēram, lietotāja ID, lietotājs, kurš pēdējais modificēja datus, pēdējās modifikācijas datums un žurnāla ID. |
| [Bilanču saraksts — noklusējuma pārskats](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas sākuma un beigu bilances un debeta un kredīta bilances pašreizējam periodam un šim gadam, kā arī papildu informācija par transakcijām, piemēram, dokuments.                                                                    |
| [Bilance — noklusējuma pārskats](https://mix.office.com/watch/zkgq0u7visw9)                                   | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu.                                                                                                                                                                                                                                                             |
| [Bilance un peļņas vai zaudējumu aprēķins blakus — noklusējuma pārskats](https://mix.office.com/watch/zkgq0u7visw9) | Skatiet organizācijas finansiālo pozīciju un ienesīguma attiecībā uz gadu vienu otram līdzās.                                                                                                                                                                                                                              |
| [Naudas plūsma — noklusējuma pārskats](https://mix.office.com/watch/jd3go9pz6390)                                       | Gūstiet ieskatu par organizācijā ieplūstošo un no tas izplūstošo naudu.                                                                                                                                                                                                                                   |
| [Detalizēts JE un TB pārskats — noklusējuma pārskats](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Skatiet sākuma bilanci un aktivitāšu informāciju visiem kontiem.                                                                                                                                                                                                                                                      |
| [Detalizēta apgrozījuma bilance — noklusējuma pārskats](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Skatiet informāciju par bilanci visiem kontiem, kuriem ir debeta un kredīta bilances, kā arī šo bilanču neto summu, kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.                                                                                                                                  |
| [Izdevumu trīs gadu ceturkšņa tendence — noklusējuma pārskats](https://mix.office.com/watch/gwm4zu7tmtj8)             | Gūstiet ieskatu par izdevumiem pēdējos 12 ceturkšņos iepriekšējo trīs gadu laikā.                                                                                                                                                                                                                                   |
| [Finanšu sadaļu JE un TB pārskats — noklusējuma pārskats](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Skatiet apskatu par bilancēm un aktivitātēm attiecībā uz līdzekļa, saistību, īpašnieka kapitāla, ieņēmumu, izdevumu, peļņas vai zaudējumu finanšu sadaļām.                                                                                                                                                                           |
| [Peļņas vai zaudējumu aprēķins — noklusējuma pārskats](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Skatiet organizācijas ienesīgumu pašreizējam periodam un šim gadam.                                                                                                                                                                                                                                   |
| [Virsgrāmatas transakciju saraksts — noklusējuma pārskats](https://mix.office.com/watch/19h9v2rmh48vy)                        | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances, kā arī papildu informācija par transakciju, piemēram, transakcijas datums, žurnāla numurs, dokuments, grāmatošanas tips un izsekošanas numurs.                                                                            |
| [Koeficienti — noklusējuma pārskats](https://mix.office.com/watch/b08hfc5h92me)                                          | Skatiet maksātspēju, ienesīgumu un efektivitātes koeficientus organizācijai attiecībā uz gadu.                                                                                                                                                                                                                           |
| [Atritināšanas 12 mēnešu izdevumu pārskats — noklusējuma pārskats](https://mix.office.com/watch/iywod5qmqhz7)                       | Gūstiet ieskatu par izdevumiem katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                                       |
| [Atritināšanas ceturkšņa peļņas vai zaudējumu aprēķins — noklusējuma pārskats](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Skatiet organizācijas ienesīgumu pa ceturkšņiem pagājušajā gadā un no šī gada sākuma.                                                                                                                                                                                                                   |
| [Bilances blakus — noklusējuma pārskats](https://mix.office.com/watch/zkgq0u7visw9)                      | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu. Šajā atskaitē līdzās tiek rādīti aktīvi un saistības, kā arī akcionāru kapitāls.                                                                                                                                                                                |
| [Kopsavilkuma apgrozījuma bilance — noklusējuma pārskats](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Skatiet bilances informāciju visiem kontiem, kam ir sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.                                                                                                                                                                  |
| [Kopsavilkuma apgrozījuma bilance pa gadiem — noklusējuma pārskats](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Skatiet bilances informāciju par visiem kontiem, kam ir sākuma un beigu bilances un debeta un kredīta bilances, kopā ar šo to neto starpību pašreizējā un iepriekšējā gadā.                                                                                                                           |
| [Iknedēļas pārdošanas un atlaides — noklusējuma pārskats](https://mix.office.com/watch/112ng0hy5de0j)                     | Gūstiet ieskatu par pārdošanu un atlaidēm katrai mēneša nedēļai. Šajā atskaitē ir ietvertas četru nedēļu kopsummas.                                                                                                                                                                                                              |
| [Pieejamie budžeta līdzekļi — noklusējuma pārskats](https://mix.office.com/watch/15hcpezcbx7tv)                         | Skatiet pārskatītā budžeta, faktisko izdevumu, budžeta rezervāciju un pieejamo budžeta līdzekļu detalizētu salīdzinājumu par visiem kontiem.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finanšu atskaišu atvēršana
Kad noklikšķināt uz izvēlnes **Finanšu atskaišu veidošana**, tiek parādīts saraksts ar uzņēmuma noklusējuma finanšu atskaitēm. Pēc tam varat atvērt vai modificēt kādu atskaiti. Lai atvērtu kādu no noklusējuma atskaitēm, atlasiet atskaites nosaukumu. Kad atskaiti atverat pirmo reizi, tā tiek automātiski tiek ģenerēta par iepriekšējo mēnesi. Piemēram, ja atskaiti pirmo reizi atverat 2016. gada augustā, šī atskaite tiek ģenerēta par 2016. gada 31. jūliju. Pēc atskaites atvēršanas varat sākt to pētīt, detalizējot konkrētus datus un mainot atskaites opcijas.

## <a name="creating-and-modifying-financial-reports"></a>Finanšu atskaišu veidošana un modificēšana
No finanšu atskaišu saraksta varat izveidot jaunu atskaiti vai modificēt jau esošu atskaiti. Ja jums ir atbilstošās atļaujas, varat izveidot jaunu finanšu pārskatu, darbību rūtī noklikšķinot uz **Jauns**. Ierīcē tiek lejupielādēta pārskatu veidošanas programma. Kad ir palaista pārskatu veidošanas programma, varat izveidot jaunu pārskatu. Kad esat saglabājis jauno atskaiti, tā kļūst redzama finanšu atskaišu sarakstā. Sarakstā tiek rādīti tikai pārskati, kas tika izveidoti tam uzņēmumam, kuru lietojat programmatūrā Finance and Operations. Papildinformāciju par finanšu pārskatu izveides un modificēšanas procesu programmatūrā Finance and Operations skatiet šajos Dynamics finanšu pārskatu [emuāra ierakstos](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/). **Piezīme.** Datorā, kurā lejupielādējat pārskatu veidošanas klientu, ir jābūt instalētai Microsoft .NET Framework versijai 4.6.2. Šo Microsoft .NET Framework versiju var lejupielādēt un instalēt [šeit](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Ja lietojat pārlūkprogrammu Chrome, lai varētu lejupielādēt pārskatu veidošanas klientu, ir jāinstalē paplašinājums ClickOnce. Ja lietojat inkognito režīmu, pārliecinieties, ka paplašinājums ClickOnce ir iespējots inkognito režīmā. Varat arī modificēt atskaiti, kas ir redzama finanšu atskaišu sarakstā. Kad ir atlasīts apgabals ap atskaites nosaukumu, darbību rūtī noklikšķiniet uz **Rediģēt**. Tiek palaista atskaišu veidotāja programma.

<a name="see-also"></a>Skatiet arī
--------

[Finanšu pārskatu skatīšana](view-financial-reports.md)

[Dynamics finanšu pārskatu veidošanas emuārs](http://blogs.msdn.com/b/dynamics_financial_reporting/)




