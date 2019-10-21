---
title: Finanšu pārskatu veidošanas apskats
description: Šajā tēmā ir aprakstīts, kur var piekļūt finanšu pārskatiem programmā Microsoft Dynamics 365 Finance un kā lietot finanšu pārskatu izveides iespējas. Tajā ir ietverts nodrošināto noklusējuma finanšu pārskatu apraksts.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: caa449feba22c5804799b5317a8e29c139cc440e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178803"
---
# <a name="financial-reporting-overview"></a>Finanšu pārskatu veidošanas apskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kur var piekļūt finanšu pārskatiem un kā lietot finanšu pārskatu veidošanas iespējas. Tajā arī ir ietverts nodrošināto noklusējuma finanšu pārskatu apraksts.

<a name="accessing-financial-reporting"></a>Piekļuve finanšu atskaišu veidošanai
-----------------------------

Izvēlne **Finanšu atskaišu veidošana** atrodas šādas vietās:

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
| Uzturēt finanšu pārskatu drošību | Uzturēt finanšu atskaišu drošību un veikt administratīvos uzdevumus. | FinancialReportsSecuritySystemMaintain |
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
Finanšu atskaišu veidošana nodrošina 22 noklusējuma finanšu atskaites. Katrs pārskats izmanto noklusējuma galvenā konta kategorijas. Šīs atskaites varat lietot tādas, kādas tās ir, vai kā sākuma punktu savām finanšu atskaišu veidošanas nepieciešamībām. Papildus tradicionālajiem finanšu pārskatiem, piemēram, peļņas vai zaudējumu aprēķinam un bilancei, šīs noklusējuma atskaites ietver atskaites, kurās ir redzami dažādie finanšu atskaišu veidi, ko varat izveidot. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Noklusējuma atskaite                                                                                         | Apraksts                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 mēnešu atritināšanas vienas kolonnas peļņas vai zaudējumu aprēķins — noklusējums | Skatiet organizācijas ienesīgumu pēdējos 12 mēnešos vienā kolonnā.                                                                                                                                                                                                                                      |
| 12 mēnešu tendenču peļņas vai zaudējumu aprēķins — noklusējums                 | Skatiet organizācijas ienesīgumu katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                             |
| Faktiski pret budžetu — noklusējums                                | Skatiet detalizētu bilances informāciju par visiem kontiem sākotnējā budžetā un pārskatīto budžetu salīdziniet ar faktiskajām vērtībām, kam ir novirzes.                                                                                                                                                                          |
| Detalizēta informācija par auditu — noklusējums                                  | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances pārskata valūtā un vietējā valūtā, kā arī papildu informācija par transakcijām, piemēram, lietotāja ID, lietotājs, kurš pēdējais modificēja datus, pēdējās modifikācijas datums un žurnāla ID. |
| Bilanču saraksts — noklusējums                                   | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas sākuma un beigu bilances un debeta un kredīta bilances pašreizējam periodam un šim gadam, kā arī papildu informācija par transakcijām, piemēram, dokuments.                                                                    |
| Bilance — noklusējums                                   | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu.                                                                                                                                                                                                                                                             |
| Līdzās atvērta Bilance un Peļņas vai zaudējumu aprēķins — noklusējums | Skatiet organizācijas finansiālo pozīciju un ienesīguma attiecībā uz gadu vienu otram līdzās.                                                                                                                                                                                                                              |
| Naudas plūsma — noklusējums                                       | Gūstiet ieskatu par organizācijā ieplūstošo un no tas izplūstošo naudu.                                                                                                                                                                                                                                   |
| Detalizēts JE un TB pārskats — noklusējums                      | Skatiet sākuma bilanci un aktivitāšu informāciju visiem kontiem.                                                                                                                                                                                                                                                      |
| Detalizēta apgrozījuma bilance — noklusējums                         | Skatiet informāciju par bilanci visiem kontiem, kuriem ir debeta un kredīta bilances, kā arī šo bilanču neto summu, kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.                                                                                                                                  |
| Izdevumu trīs gadu ceturkšņa tendence — noklusējuma             | Gūstiet ieskatu par izdevumiem pēdējos 12 ceturkšņos iepriekšējo trīs gadu laikā.                                                                                                                                                                                                                                   |
| Finanšu sadaļu JE un TB pārskats — noklusējums            | Skatiet apskatu par bilancēm un aktivitātēm attiecībā uz līdzekļa, saistību, īpašnieka kapitāla, ieņēmumu, izdevumu, peļņas vai zaudējumu finanšu sadaļām.                                                                                                                                                                           |
| Peļņas vai zaudējumu aprēķins — noklusējuma pārskats                                | Skatiet organizācijas ienesīgumu pašreizējam periodam un šim gadam.                                                                                                                                                                                                                                   |
| Virsgrāmatas transakciju saraksts — noklusējums                        | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances, kā arī papildu informācija par transakciju, piemēram, transakcijas datums, žurnāla numurs, dokuments, grāmatošanas tips un izsekošanas numurs.                                                                            |
| Koeficienti — noklusējums                                          | Skatiet maksātspēju, ienesīgumu un efektivitātes koeficientus organizācijai attiecībā uz gadu.                                                                                                                                                                                                                           |
| 12 mēnešu izdevumu atritināšana — noklusējums                       | Gūstiet ieskatu par izdevumiem katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                                       |
| Ceturkšņa peļņas vai zaudējumu aprēķina atritināšana — noklusējums               | Skatiet organizācijas ienesīgumu pa ceturkšņiem pagājušajā gadā un no šī gada sākuma.                                                                                                                                                                                                                   |
| Bilances blakus — noklusējuma pārskats                      | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu. Šajā atskaitē līdzās tiek rādīti aktīvi un saistības, kā arī akcionāru kapitāls.                                                                                                                                                                                |
| Kopsavilkuma apgrozījuma bilance — noklusējums                          | Skatiet bilances informāciju visiem kontiem, kam ir sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.                                                                                                                                                                  |
| Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums           | Skatiet bilances informāciju par visiem kontiem, kam ir sākuma un beigu bilances un debeta un kredīta bilances, kopā ar šo to neto starpību pašreizējā un iepriekšējā gadā.                                                                                                                           |
| Iknedēļas pārdošanas un atlaides — noklusējums                     | Gūstiet ieskatu par pārdošanu un atlaidēm katrai mēneša nedēļai. Šajā atskaitē ir ietvertas četru nedēļu kopsummas.                                                                                                                                                                                                              |
| Pieejamie budžeta līdzekļi — noklusējuma pārskats                         | Skatiet pārskatītā budžeta, faktisko izdevumu, budžeta rezervāciju un pieejamo budžeta līdzekļu detalizētu salīdzinājumu par visiem kontiem.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finanšu atskaišu atvēršana
Kad noklikšķināt uz izvēlnes **Finanšu atskaišu veidošana**, tiek parādīts saraksts ar uzņēmuma noklusējuma finanšu atskaitēm. Pēc tam varat atvērt vai modificēt kādu atskaiti. Lai atvērtu kādu no noklusējuma atskaitēm, atlasiet atskaites nosaukumu. Kad atskaiti atverat pirmo reizi, tā tiek automātiski tiek ģenerēta par iepriekšējo mēnesi. Piemēram, ja atskaiti pirmo reizi atverat 2016. gada augustā, šī atskaite tiek ģenerēta par 2016. gada 31. jūliju. Pēc atskaites atvēršanas varat sākt to pētīt, detalizējot konkrētus datus un mainot atskaites opcijas.

## <a name="creating-and-modifying-financial-reports"></a>Finanšu atskaišu veidošana un modificēšana
No finanšu atskaišu saraksta varat izveidot jaunu atskaiti vai modificēt jau esošu atskaiti. Ja jums ir atbilstošās atļaujas, varat izveidot jaunu finanšu pārskatu, darbību rūtī noklikšķinot uz **Jauns**. Ierīcē tiek lejupielādēta pārskatu veidošanas programma. Kad ir palaista pārskatu veidošanas programma, varat izveidot jaunu pārskatu. Kad esat saglabājis jauno atskaiti, tā kļūst redzama finanšu atskaišu sarakstā. Sarakstā tiek rādīti tikai pārskati, kas tika izveidoti tam uzņēmumam, kuru lietojat programmā Finance. 

> [!NOTE] 
> Datorā, kurā tiek lejupielādēts pārskatu izveides klients, ir jābūt instalētai Microsoft .NET Framework versijai 4.6.2. Šo Microsoft .NET Framework versiju var lejupielādēt un instalēt no [Microsoft lejupielādes centra](https://www.microsoft.com/download/details.aspx?id=53345). Ja lietojat pārlūkprogrammu Chrome, lai varētu lejupielādēt pārskatu veidošanas klientu, ir jāinstalē paplašinājums ClickOnce. Ja lietojat inkognito režīmu, pārliecinieties, ka paplašinājums ClickOnce ir iespējots inkognito režīmā. Varat arī modificēt atskaiti, kas ir redzama finanšu atskaišu sarakstā. Kad ir atlasīts apgabals ap atskaites nosaukumu, darbību rūtī noklikšķiniet uz **Rediģēt**. Tiek palaista atskaišu veidotāja programma.

## <a name="additional-resources"></a>Papildu resursi
- [Skatīt finanšu pārskatus](view-financial-reports.md)



