---
title: Finanšu pārskatu veidošanas apskats
description: Šajā tēmā ir aprakstīts, kur var piekļūt finanšu pārskatiem programmā Microsoft Dynamics 365 Finance un kā lietot finanšu pārskatu izveides iespējas.
author: aprilolson
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43ab01d36f032e36a0daed6f94897bba42f8a189
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189001"
---
# <a name="get-started-with-financial-reporting"></a>Sākt darbu ar Financial reporting 

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kur var piekļūt finanšu pārskatiem un kā lietot finanšu pārskatu veidošanas iespējas. Tajā arī ir ietverts nodrošināto noklusējuma finanšu pārskatu apraksts.

## <a name="accessing-financial-reporting"></a>Piekļuve finanšu atskaišu veidošanai

Izvēlne **Finanšu pārskatu veidošana** atrodas tālāk norādītajās vietās:

-   **Virsgrāmata** &gt; **Pieprasījumi un pārskati**
-   **Budžeta veidošana** &gt; **Pieprasījumi un pārskati** &gt; **Pamata budžeta veidošana**
-   **Budžeta veidošana** &gt; **Pieprasījumi un pārskati** &gt; **Budžeta plānošana**
-   **Budžeta veidošana** &gt; **Pieprasījumi un pārskati** &gt; **Budžeta kontrole**
-   Konsolidācija

Lai izveidotu un ģenerētu finanšu atskaites kādai juridiskajai personai, šai juridiskajai personai jums ir jāiestata šāda informācija:

-   Finanšu kalendārs
-   Ledger
-   Kontu plāns
-   Valūta
-   Darbības grāmatošana vismaz vienā kontā
-   MainAccount ir norādīts kolonnā Atlasīts sadaļā **Virsgrāmata > Virsgrāmatas iestatīšana > Finanšu pārskatu iestatījumi**

## <a name="granting-security-access-to-financial-reporting"></a>Drošības piekļuves piešķiršana Financial Reporting
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

Kad lietotājs ir pievienots vai loma ir mainīta, lietotājam dažu minūšu laika ir jāspēj piekļūt finanšu atskaišu veidošanai. 

> [!NOTE]
> Visām finanšu pārskatu lomām tiek pievienota sistēmas administratora loma.

## <a name="report-deletions-and-expirations"></a>Ziņojumu dzēšana un derīguma beigas
Lietotāji, kas ģenerē pārskatu, var dzēst savus pārskatus. Lietotāji ar pienākumu **Uzturēt finanšu pārskata drošību** var dzēst citus pārskatus. 

Laidienā 10.0.8 tika ieviests beigu datumu jēdziens. Jaunais nepieciešamais līdzeklis ir iespējots lapā **Visi** līdzekļu pārvaldības darbvietā. **Finanšu pārskata saglabāšanas politikas** līdzeklī ir šādas izmaiņas:
* Jaunizveidotie pārskati tiks automātiski atzīmēti kā tādi, kuru beigu datums ir 90 dienas no to ģenerēšanas brīža.
* Visiem esošiem pārskatiem pirms līdzekļa instalēšanas tiks piešķirts 90 dienu derīguma termiņš. Datums uz īsu laiku var tikt parādīts kā tukšs, līdz tiek palaists finanšu atskaišu pakalpojums, tiek ģenerēts pārskats un pakalpojums veic atjaunināšanu esošajiem pārskatiem ar tukšu derīguma termiņu. 
* Lietotāji, kuriem ir **Finanšu pārskatu drošības uzturēšana**, var piekļūt šai funkcionalitātei. Jebkurš lietotājs pienākumā **Uzturēt finanšu pārskatu**, kuram ir piešķirta privilēģija **Uzturēt finanšu pārskata derīguma termiņu** būs arī iespēja labot derīguma termiņu. Pašlaik ir pieejamas divas saglabāšanas iespējas: 
  * Derīguma beigas pēc 90 dienām.
  * Iespēja iestatīt, ka pārskatam nekad nebeidzas termiņš.
  
Kad ir atlasīts termiņš, piemēram, 90 dienas, tas tiek lietots 90 dienas no šodienas. Šī ir atšķirīga uzvedība, nekā 90 dienas no sākotnējā izveides datuma iestatījuma, kas tika noteikts pārskata izveides laikā. 
  
Papildu opcijas tiks apsvērtas turpmākajā funkcionalitātē. 90 dienu derīguma termiņš būs noklusējums, un lietotāji ar atbilstošajām atļaujām var ignorēt noklusējumu **Finanšu pārskatu** saraksta lapā.    

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
| [Detalizēta apgrozījuma bilance — noklusējums](trial-balance-financial-reports.md)| Skatiet informāciju par bilanci visiem kontiem, kuriem ir debeta un kredīta bilances, kā arī šo bilanču neto summu, kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.                                                                                                                                  |
| Izdevumu trīs gadu ceturkšņa tendence — noklusējuma             | Gūstiet ieskatu par izdevumiem pēdējos 12 ceturkšņos iepriekšējo trīs gadu laikā.                                                                                                                                                                                                                                   |
| Finanšu sadaļu JE un TB pārskats — noklusējums            | Skatiet apskatu par bilancēm un aktivitātēm attiecībā uz līdzekļa, saistību, īpašnieka kapitāla, ieņēmumu, izdevumu, peļņas vai zaudējumu finanšu sadaļām.                                                                                                                                                                           |
| [Peļņas vai zaudējumu aprēķins — noklusējuma pārskats](income-statement-financial-report.md)| Skatiet organizācijas ienesīgumu pašreizējam periodam un šim gadam.                                                                                                                                                                                                                                   |
| Virsgrāmatas transakciju saraksts — noklusējums                        | Skatiet detalizētu informāciju par bilanci visiem kontiem. Šajā atskaitē tiek rādītas debeta un kredīta bilances, kā arī papildu informācija par transakciju, piemēram, transakcijas datums, žurnāla numurs, dokuments, grāmatošanas tips un izsekošanas numurs.                                                                            |
| Koeficienti — noklusējums                                          | Skatiet maksātspēju, ienesīgumu un efektivitātes koeficientus organizācijai attiecībā uz gadu.                                                                                                                                                                                                                           |
| 12 mēnešu izdevumu atritināšana — noklusējums                       | Gūstiet ieskatu par izdevumiem katram no pēdējiem 12 mēnešiem. Šie 12 mēneši var attiekties uz periodu, kas ir ilgāks par vienu finanšu gadu.                                                                                                                                                                                                       |
| Ceturkšņa peļņas vai zaudējumu aprēķina atritināšana — noklusējums               | Skatiet organizācijas ienesīgumu pa ceturkšņiem pagājušajā gadā un no šī gada sākuma.                                                                                                                                                                                                                   |
| Bilances blakus — noklusējuma pārskats                      | Skatiet organizācijas finanšu pozīciju attiecībā uz gadu. Šajā atskaitē līdzās tiek rādīti aktīvi un saistības, kā arī akcionāru kapitāls.                                                                                                                                                                                |
| [Kopsavilkuma apgrozījuma bilance — noklusējums](trial-balance-financial-reports.md)| Skatiet bilances informāciju visiem kontiem, kam ir sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.                                                                                                                                                                  |
| [Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums](trial-balance-financial-reports.md)| Skatiet bilances informāciju par visiem kontiem, kam ir sākuma un beigu bilances un debeta un kredīta bilances, kopā ar šo to neto starpību pašreizējā un iepriekšējā gadā.                                                                                                                           |
| Iknedēļas pārdošanas un atlaides — noklusējums                     | Gūstiet ieskatu par pārdošanu un atlaidēm katrai mēneša nedēļai. Šajā atskaitē ir ietvertas četru nedēļu kopsummas.                                                                                                                                                                                                              |
| Pieejamie budžeta līdzekļi — noklusējuma pārskats                         | Skatiet pārskatītā budžeta, faktisko izdevumu, budžeta rezervāciju un pieejamo budžeta līdzekļu detalizētu salīdzinājumu par visiem kontiem.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finanšu atskaišu atvēršana
Kad atlasāt izvēlni **Finanšu pārskatu veidošana**, tiek parādīts saraksts ar uzņēmuma noklusējuma finanšu pārskatiem. Pēc tam varat atvērt vai modificēt kādu atskaiti. Lai atvērtu kādu no noklusējuma atskaitēm, atlasiet atskaites nosaukumu. Kad atskaiti atverat pirmo reizi, tā tiek automātiski tiek ģenerēta par iepriekšējo mēnesi. Piemēram, ja atskaiti pirmo reizi atverat 2019. gada augustā, šī atskaite tiek ģenerēta par 2019. gada 31. jūliju. Pēc atskaites atvēršanas varat sākt to pētīt, detalizējot konkrētus datus un mainot atskaites opcijas.

## <a name="creating-and-modifying-financial-reports"></a>Finanšu atskaišu veidošana un modificēšana
No finanšu atskaišu saraksta varat izveidot jaunu atskaiti vai modificēt jau esošu atskaiti. Ja jums ir atbilstošās atļaujas, varat izveidot jaunu finanšu pārskatu, darbību rūtī atlasot **Jauns**. Ierīcē tiek lejupielādēta pārskatu veidošanas programma. Kad ir palaista pārskatu veidošanas programma, varat izveidot jaunu pārskatu. Kad esat saglabājis jauno atskaiti, tā kļūst redzama finanšu atskaišu sarakstā. Sarakstā tiek rādīti pārskati, kas tika izveidoti uzņēmumam, kuru lietojat programmā Dynamics 365 Finance. 

## <a name="reporting-tree-definitions"></a>Pārskata koku definīcijas 
Viens no komponentiem, kas tiek izmantots finanšu pārskatu izveidei, ir pārskatu koka definīcija. Atskaišu koka definīcija palīdz definēt jūsu organizācijas struktūru un hierarhiju. Tā ir starpdimensiju hierarhiska struktūra, kas ir balstīta uz dimensiju attiecībām jūsu finanšu datos. Tā sniedz informāciju atskaites vienības līmenī un kopsavilkuma līmenī visām kokā esošajām vienībām.

Var izveidot neierobežotu pārskata koku skaitu, lai skatītu jūsu uzņēmuma datus dažādos veidos. Katrs pārskata koks var saturēt jebkuru nodaļu un kopsavilkuma vienību kombināciju, bet pārskata definīcija var saistīt tikai vienu pārskata koku vienlaicīgi. 


## <a name="troubleshooting-issues-opening-report-designer"></a>Problēmu novēršana, atverot pārskatu noformētāju
Pastāv dažas tipiskas problēmas, kas var radīt traucējumus, atverot pārskatu noformētāju. Problēmas un to risināšanas darbības ir šādas.

1. problēma: pārskatu noformētājs netiek sākts, atlasot **Jauns** vai **Rediģēt**.

* Pārlūkprogrammā Internet Explorer atlasiet **Iestatījumi**, pēc tam atlasiet **Interneta opcijas**. Atlasiet cilni **Drošība**. Atlasiet Uzticamās vietnes un pēc tam atlasiet **Vietnes**. Sadaļā **Vietnes pievienošana zonai** ievadiet “\*\.dynamics.com” (bez pēdiņām) un pēc tam atlasiet **Pievienot**. 
* Pārlūkprogrammā Internet Explorer atlasiet **Iestatījumi**, pēc tam atlasiet **Interneta opcijas**. Atlasiet cilni **Drošība**. Atlasiet Uzticamās vietnes. Apgabalā ar nosaukumu Šīs zonas drošības līmenis, mainiet opciju uz **Vidēji zems**.
* Atspējojiet uznirstošo elementu bloķētāju savā pārlūkprogrammā.
* Darbstacijām ir nepieciešams instalēt Microsoft .NET Framework 4.6.2 vai jaunāku versiju. Šo Microsoft .NET Framework versiju var lejupielādēt un instalēt no [Microsoft lejupielādes centra](https://www.microsoft.com/download/details.aspx?id=53345).
* Lietojot pārlūkprogrammu Chrome, ir jāinstalē paplašinājums ClickOnce, lai varētu lejupielādēt Pārskatu noformētāja klientu. Ja lietojat Chrome inkognito režīmu, pārliecinieties, ka paplašinājums ClickOnce ir iespējots inkognito režīmā. Papildinformāciju par Chrome ClickOnce paplašinājumu skatiet šeit: [Sistēmas prasības mākoņa izvietojumiem](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Ja izmantojat pārlūkprogrammu Microsoft Edge ar pārlūku Chrome, jums nav jāinstalē Edge Chromium paplašinājums ClickOnce. Tomēr, lai lejupielādētu pārskatu veidotāja klientu, ir jāiespējo ClickOnce opcija. Ja lietojat inkognito režīmu, pārliecinieties, ka paplašinājums ClickOnce ir iespējots inkognito režīmam.
     1. Atveriet jaunu pārlūkprogrammu Microsoft Edge.
     2. Ievadiet **edge://flags** un atlasiet **Enter**.
     3. Meklējiet **ClickOnce atbalsta** opciju vai izmantojiet šo tiešo saiti: **edge://flags/#edge-click-once**.
     4. Iestatiet nolaižamās izvēlnes opciju kā **iespējotu**.
     5. Atlasiet **Restartēt pārlūku**.

2. problēma: lietotājam nav piešķirtas nepieciešamās atļaujas Financial Reporting izmantošanai. 

* Lai pārbaudītu, vai lietotājam nav atļauju, atlasiet **Jā** kļūdai “Nevar izveidot savienojumu ar Financial Reporting serveri. Atlasiet Jā, ja vēlaties turpināt un norādīt citu servera adresi.” Pēc tam atlasiet **Savienojuma pārbaude**. Ja jums nav atļaujas, tiks parādīts ziņojums, ka “Neizdevās izveidot savienojumu. Lietotājam nav atbilstošu atļauju, lai izveidotu savienojumu ar serveri. Sazinieties ar sistēmas administratoru.”
* Nepieciešamās atļaujas ir minētas iepriekš sadaļā [Drošības piekļuves piešķiršana Financial Reporting](#granting-security-access-to-financial-reporting). Financial Reporting drošība ir balstīta uz šīm privilēģijām. Ja jums netiks piešķirtas šīs privilēģijas, (vai cita drošības loma, kas ietver šīs privilēģijas) jums nebūs piekļuves. 
* Integrācijas uzdevums **Uzņēmuma lietotāju nodrošinājums uzņēmumam** (kas ir arī atbildīgs par un pazīstams kā lietotāja integrācija) darbojas ar 5 minūšu intervālu. Var paiet līdz 10 minūtēm, līdz jebkuras atļaujas izmaiņas stājas spēkā Financial Reporting. 
  Ja cits lietotājs var atvērt Pārskatu noformētāju, atlasiet **Rīki** un pēc tam atlasiet **Integrācijas statuss**. Pārbaudiet, vai integrācijas karte, “Uzņēmuma lietotāju nodrošinājums uzņēmumam” ir veiksmīgi izpildīta, jo tika piešķirta atļauja izmantot Financial Reporting. 
* Iespējams, ka cita kļūda ir liegusi pabeigt **Dynamics lietotāja integrācija Financial Reporting lietotājā**. Iespējams, ka ir iniciēta un vēl nav pabeigta datamart atiestatīšana, vai arī ir radusies cita sistēmas kļūda. Vēlāk mēģiniet palaist procesu vēlreiz. Ja problēma joprojām pastāv, sazinieties ar sistēmas administratoru.

3. problēma: ir iespējams pieteikties Pārskatu noformētājā paplašinājumā ClickOnce, bet nav iespējams pabeigt pieteikšanos Pārskatu noformētājā. 

* Ievadot pieteikšanās akreditācijas datus, starpība, starp jūsu lokālajā datora iestatīto laiku un Financial Reporting servera laiku, nedrīkst pārsniegt piecas minūtes. Ja atšķirība ir lielāka par piecām minūtēm, sistēma pieteikties neļaus. 
* Šādā gadījumā, ieteicams iespējot Windows opciju, automātiski iestatīt datora laiku. 

## <a name="additional-resources"></a>Papildu resursi
- [Skatīt finanšu pārskatus](view-financial-reports.md)
- [Pārskatu koka definīcijas finanšu pārskatos](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]