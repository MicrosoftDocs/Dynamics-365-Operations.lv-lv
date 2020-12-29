---
title: Mazumtirdzniecības atlaižu pārvaldība
description: Šajā tēmā ir aprakstīta tirdzniecības atlaižu pārvaldība programmai Dynamics 365 Supply Chain Management.
author: t-benebo
manager: tfehr
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: MCRBrokerClaims, MCRBrokerWriteOffReasonPrompt, MCRRoyaltyVendTable, MCRRoyaltyVendTrans, PdsCustRebateGroup, PdsRebateAgreement, TAMCopyTradePromotions, TAMDeduction, TAMDeductionCreate, TAMDeductionDenyReason, TAMDeductionParmDeny, TAMDeductionParmMassUpdate, TAMDeductionParmMatch, TAMDeductionParmSplit, TAMDeductionParmWriteOff, TAMDeductionType, TAMDeductionWriteOffReason, TAMFundManagement, TAMFundUsage, TAMListPage, TAMMarketingObjective, TAMMerchEventType, TAMOneTimePromotion, TAMPromoCompareGraph, TAMPromoStatistic, TAMPromotionAnalysisSummary, TAMPromotionParameters, TAMPromotionPeriod, TAMTemplateListPage, TAMTradePromotionAnalysis, TAMTradePromotions, TAMWhatIfPromotionAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 13b665427a4caf206e0a3b3aca6b04c1529b9206
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432734"
---
# <a name="trade-allowance-management"></a>Mazumtirdzniecības atlaižu pārvaldība

[!include [banner](../includes/banner.md)]

Atlaižu pārvaldība palīdz uzņēmumiem pārvaldīt pārdošanas veicināšanas programmas, kurās tiek piedāvātas "samaksa par rezultātiem" naudas atlīdzība klientiem, kuri sasniedz apjoma un izturēšanās mērķus. Šī līdzekļa iespējas ir paredzētas uzņēmumiem, kas koncentrējas uz visaptverošiem veicināšanas procesiem peļņas gūšanas nolūkā, sākot ar reklāmas līdzekļu budžeta plānošanu un sadalījumu, līdz atlaižu līguma izveidei, pieprasījumu izveidei un apstrādei, maksājumu apstrādei un veicināšanas pasākumu efektivitātes analīzei.


Šis raksts sniedz plašu pārskatu par mazumtirdzniecības atlaižu pārvaldības funkciju un iepazīstinās ar pārdošanas veicināšanas programmas pārvaldības standarta uzdevumu kopu. Ir paredzams, ka šo funkcionalitāti izmantos vairāku veidu lietotāji ar darbības un lēmumu pieņemšanas atbildībām, savu attiecīgo mērķu sasniegšanai, kā norādīts tālāk.

- Diskrecionāro naudas līdzekļu piešķiršana atlasītiem kontiem un mazumtirdzniecības atlaižu līgumu izveide reklāmas nolūkā, pamatojoties uz atmaksas un vienreizējiem maksājumiem (par noteikto pakalpojumu)
- Noslēgto reklāmas līgumu salīdzināšana ar notiekošo pārdošanu un atmaksas pieprasījumu izveide
- Aprēķināšanas, apstiprināšanas, un ģenerēto summu pieprasījumu apstrādei un tos nodeva debitoru parādi (/ r) kā atvilkumi maksājumu nosegšanai
- Klienta daļējā maksājuma saskaņošana ar ieturējumu, kas ir jāmaksā
- Reklāmas līdzekļu izmantošanas izsekošana un programmas ienesīguma un efektivitātes izvērtēšana

## <a name="audience-and-purpose"></a>Mērķauditorija un nolūks

Informācija šajā dokumentā ir paredzēta uzņēmumu biznesa lēmumu pieņēmējiem, tādos amatos kā iepirkumu daļas vadītājs, finanšu direktors (chief financial officer — CFO) un galvenais grāmatvedis, kuriem ir tālāk norādītie pienākumi.

- Augsta līmeņa budžetu un līdzekļu sadalījums
- Pārdošanas veicināšanas plānošana un analīze
- Personāla, kas apstrādā atmaksu prasības, izpilda maksājumus, pamatojoties uz tirdzniecības pasākumiem, un sedz daļējus maksājumus un atvilkumus, pārvaldība

Cilvēki šajās lomās amatos meklē veidus, kā sasniegt tālāk norādītos mērķus.

- Labāk izmantot tirdzniecības veicināšanas līdzekļus.
- Elastīgi ieviest dažādu veidu veicināšanas programmas un atlīdzības.
- Samazināt administratīvo slogu un kļūdas, kas ir saistītas ar veicināšanas veiktspējas pārraudzība un prasību apstrādāšanu.
- Uzlabot naudas plūsmas prognozes, uzkrājot turpmākām saistībām.
- Izmantot kvantitatīvu pamatu pašreizējām un turpmākām pārrunām ar debitoriem saistībā ar reklāmām.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Reklāmas pakalpojumu līdzekļu un mazumtirdzniecības atlaižu līgums

Tirdzniecības atlaižu līgums ir veicināšanas programma, kurā klientiem, kuri sasniedz konkrētus apjoma un/vai uzvedības mērķus, tiek piedāvātas naudas atlīdzības atbilstoši sasniegumiem. Veicināšanas līdzekļi ir budžeta izdevumi. Šādā veidā var ietvert reklāmas kampaņas.

### <a name="promotional-fund"></a>Veicināšanas fonds

Līdzekļi, kas tiek piešķirti tirdzniecības atlaižu līgumiem, tiek reģistrēti lapā **Fondi**. Lai atvērtu lapu **Fondi**, atlasiet **Pārdošana un mārketings** \> **Tirdzniecības atlaides** \> **Fondi** \> **Fondi**.

![Fondu lapa](./media/trade-allowance-management-funds-page.png "Fondu lapa")

Lapā **Fondi** varat skatīt informāciju par veicināšanas fondiem.

Kopsavilkuma cilne **Vispārīgi** parāda laiku periodu, kurā fonds ir derīgs, un tā budžeta summu. Lai fondu varētu piešķirt veicināšanas līgumam, lauka **Statuss** vērtībai ir jābūt **Apstiprināts**.

Kopsavilkuma cilnē **Debitori** tiek parādīta debitoru hierarhija. Lai atlasītu debitorus, kuri atbilst fonda mērķiem, velciet tos, lai tie atrastos sadaļā **Fonda debitori**. Šajā kopsavilkuma cilnē arī tiek parādīts, kā tiek sadalīta fonda kopējā summa.

Kopsavilkuma cilnē **Vienumi** tiek parādīti vienumi, kas ir iekļauti veicināšanas pasākumos.

### <a name="trade-allowance-agreement"></a>Mazumtirdzniecības atlaižu līgums

Kad ir izveidota fonda definīcija, nākamās darbības reklāmas pasākuma plānošanā ir reģistrēt reklāmas pakalpojumu līgumus (kuri tiek saukti par mazumtirdzniecības atlaižu līgumiem), piešķirt finansējumu un definēt izpildes mērķus katram tirdzniecības notikumam.

Mazumtirdzniecības atlaižu līgumus reģistrē lapā **Mazumtirdzniecības atlaižu līgumi**. Lai atvērtu lapu **Mazumtirdzniecības atlaižu līgumi**, atlasiet **Pārdošana un mārketings** \> **Mazumtirdzniecības atlaides** \> **Mazumtirdzniecības atlaižu līgumi**.

![Tirdzniecības atlaižu līgumu lapa](./media/trade-allowance-management-agreements-page.png "Tirdzniecības atlaižu līgumu lapa")

#### <a name="header"></a>Virsraksts

Atlasiet vienumu **Virsraksts**, lai pārslēgtos uz virsrakstu skatu.

Kopsavilkuma cilnē **Vispārīgi** lauki **Pasūtījums līdz** un **Pasūtījums no** nosaka periodu, kad līgums ir spēkā. Apstiprinājuma statuss **Iekšēji apstiprināts** līgumam norāda, ka līgums vēl nav derīgs, un to nevar izmantot pārdošanas pasūtījuma apstrādes laikā.

Sadaļa **Analīze** kopsavilkuma cilnē **Vispārīgi** ietver svarīgus laukus, kuri nosaka daudzumus un izmaksas, kas tiek izmantoti reklāmas pasākuma novērtēšanā.

- Lauks **Bāzes vienības** norāda preču daudzumu, kas ir jāpārdod ar atlasītajiem debitoriem, pirms tiek piemērots reklāmas pasākums.
- Vērtība **Aprēķinātais nosūtāmais daudzums** tiek aprēķināta, pamatojoties uz vērtību **Paaugstināšanas procenti**, kas ir šī reklāmas pasākuma plānotais mērķa palielinājums.
- Lauks **Mazumtirdzniecības atlaižu izmaksas** tiek aprēķināts, balstoties uz dažādu notikumu daudzumiem mazumtirdzniecības atlaižu līgumā.

Kopsavilkuma cilnē **Debitori**, sarakstā pa kreisi var atlasīt un skatīt debitoru grupas, kuras ir iestatītas kā iepriekš definētas hierarhijas. Pēc tam varat atlasīt visu hierarhiju vai noteiktus kontus kā mērķus atlaižu līgumam.

Kopsavilkuma cilnē **Vienumi**, tāpat kā kopsavilkuma cilnē **Vienumi** lapā **Fondi**, preces tiek pievienotas līgumam, lai to pārdošanu saistītu ar atlaidi, par ko tika panākta vienošanās.

Kopsavilkuma cilnē **Fondi** varat skatīt reklāmas pasākumu fondus, kas ir saistīti ar šo līgumu. Varat skatīt arī šī līguma notikumu izmaksu sadalījumu. 100 procentu notikumu izmaksu sadalījums nozīmē, ka šis reklāmas pasākums tiks finansēts tikai no viena fonda. Reklāmas pasākumu līgumā var arī izmantot vairāku fondu līdzekļus un izmantot vienādu vai diferencētu procentuālo sadalījumu.

#### <a name="lines"></a>Līnijas

Pēc tam atlasiet **Rindas**, lai pārslēgtos uz rindu skatu.

Cilnē **Tirdzniecības notikumi** tiek parādīti līguma segto notikumu veidi. Ir trīs veidu notikumi: atmaksa, vienreizējs maksājums un pie rēķina.

Atlasot tirdzniecības notikumu un pēc tam atlasot cilni **Summas**, tiek atrasta detalizētu informāciju par notikumu.

![Tirdzniecības atlaižu līguma rindas](./media/trade-allowance-management-agreements-lines.png "Tirdzniecības atlaižu līguma rindas")

Sadaļā **Mazumtirdzniecības atlaižu rindas** norādiet daudzumu vai summu diapazonus, kas debitoram ir jāsasniedz definīcijām, lai iegūtu atlīdzības.

**Atmaksas** veida tirdzniecības notikuma gadījumā augšējās sadaļas cilne **Summas** nosaka noteikumus, saskaņā ar kuriem atmaksa tiks piemērota, izveidota un apmaksāta. Piemēram, kārtulas var noteikt tālāk aprakstītos nosacījumus atmaksas prasībai.

- Tas ir balstīts uz pārdošanas pasūtījuma izveides datumu (vērtība **Aprēķina datuma veids** ir **Izveidots**).
- Tas tiek aprēķināts, pamatojoties uz pārdošanas pasūtījuma rindas summu pirms atlaidēm, nevis uz neto summu, kas ietver atlaides (vērtība **Ņemts no** ir **Bruto**).
- Tas ir balstīts uz pārdoto preču apjomu, nevis uz summu (vērtība **Atlaides rindas pārtraukuma veids** ir **Daudzums**).
- Tas tiek aprēķināts par mēneša periodu (vērtība **Uzkrātā pārdošana pēc** ir **Mēnesis**). 
- Tas ir noteikts kā ieturējums, nevis izmantojot A/P (vērtība **Maksājuma veids** ir **Debitoru ieturējumus**).

**Vienreizējā maksājuma** veida tirdzniecības notikuma gadījumā cilnē **Summas** tiek parādīts daudzumu, kas jāmaksā debitoram ieturējuma formā, ja debitors sasniedz noteiktus izpildes rādītājus. Apstiprinājuma statusu kā **Atvērts** norāda, ka vienreizējais maksājums vēl nav veikts.

Lai līgumu piemērotu pārdošanas pasūtījumiem, kas atbilst līguma nosacījumiem, līguma statusam ir jābūt **Apstiprināts**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Pārdošanas veikšana saskaņā ar plānoto tirdzniecības notikumu un atmaksas prasību izveide

Izveidojot pārdošanas pasūtījumu, kurā ir rindas, kas izpilda līguma prasības, varat skatīt saistīto informāciju lapā **Pārdošanas pasūtījums**, atlasot **Pārdošanas pasūtījuma rinda** \> **Skatīt** \> **Cenu detaļas**.

Lapā **Cenu informācija** kopsavilkuma cilnē **Atlaides** pārdošanas darbinieks var redzēt atmaksu no derīga tirdzniecības atlaižu līguma (tiek rādīts atlaižu programmas ID) un kopējo summu, kas tiek piemērota šai rindai. Šī summa tiek rādīta arī laukā **Atlaižu summa** sadaļā **Plānotais uzcenojums** lapā **Cenu informācija**.

Kad pārdošanas rēķins ir iegrāmatots, attiecīgā atmaksas prasība tiek izveidota katrai rēķina rindai.

> [!NOTE]
> Lai skatītu lapu **Cenu informācija**, lapā **Debitoru parametri**, cilnē **Cenas** atlasiet izvēles rūtiņu **Iespējot cenu informāciju**. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Pieprasījumu apstrāde un nodošana kā atvilkumi debitoriem

Nākamās darbības atmaksu apstrādes procesā ir pieprasījumu pārskatīšana, aprēķināšana un apstiprināšana, un pēc tam to konvertēšana ieturējumos.

Atmaksas rīkā reklāmas pasākuma līguma īpašnieks regulāri pārskata un apstrādā izveidotos pieprasījumus. Šajā rīkā arī debitoru administrators pārveido apstiprinātos pieprasījumus ieturējumos vai regulāros maksājumos atkarībā no pieprasījuma maksājuma metodes.

Lapā **Atmaksas rīks** lapu, varat pārskatīt pieprasījumu rindas. Ja pieprasījumu statuss ir **Jāpārrēķina**, tie ir jāpārrēķina iespējamas kumulācijas dēļ.

### <a name="recalculate-claims"></a>Pieprasījumu pārrēķināšana

Lai pārrēķinātu pieprasījumus, darbību rūtī atlasiet **Uzkrāt**. Pēc tam dialoglodziņā **Uzkrātās atlaides** atlasiet debitoru.

Pārrēķināšanas rezultātā programma izveido jaunus pieprasījumus summām, lai pielāgotu sākotnējos pieprasījumus kvalifikācijas summai uz vienu vienību. Viens korekcijas pieprasījums tiek ģenerēts katrai unikālai debitora, vienības, valūtas, mērvienības, krājumu dimensijas, finanšu dimensijas un PVN grupas kombinācijai. Šiem korekciju pieprasījumiem ir tāda pati atsauce uz pārdošanas pasūtījumu un rēķina numuru kā pieprasījumiem, kuri tiek koriģēti (t.i., pieprasījumi, kas sākotnēji tika izveidoti no pārdošanas dokumenta). Atšķirībā no sākotnēja pieprasījuma korekcijas pieprasījumam nav vērtību laukos, kas apraksta sākotnējās pārdošanas pasūtījuma rindas summas un daudzumu.

Pēc tam, kad pārrēķināšana ir pabeigta, pieprasījumu statuss tiek mainīts uz **Aprēķināts**. Lai apstiprinātu pieprasījumus, darbību rūtī atlasiet **Apstiprināt**.

### <a name="process-claims-and-pass-them-to-ar"></a>Pieprasījumu apstrāde un nodošana debitoriem

Pieprasījumi tagad ir gatavi debitoru apstrādei. Lai tos apstrādātu, darbību rūtī atlasiet **Apstrādāt**. 

Apstrādājot pieprasījumus, to statuss ir nomainīts uz **Atzīmēt** un norāda, ka žurnāla grāmatošana (grāmatotais žurnāls ir atlaižu uzkrājuma žurnāls, kā norādīts debitoru parametros) ir izraisījusi tālāk aprakstītos notikumus. 

- Pieprasījumi ir pārsūtīti uz pagaidu debitora bilanci kā ieturējumi.
- Atlaižu uzkrājumu konts ir kreditēts pārstāvēt nākotnes saistības debitoram.
- Atlaižu izdevumu konts ir debetēts, lai atpazītu izmaksas, kas radušās saistībā ar pārdošanu.

Lai pabeigtu procesu, debitora darbiniekam tagad ir jāapstrādā uzkrājuma ieturējumi, pārsūtot tos uz debitoru bilanci kā kredīta nota (saistības). 

Lai sāktu uzdevumu, lapas **Debitors** darbību rūtī atlasiet **Apkopot** \> **Transakciju segšana**. Pēc tam lapā **Transakciju segšana** atlasiet **Funkcijas** \> **Atmaksas programma**. Šī atlaižu lapa parāda visus iepriekš apstrādātos atmaksas pieprasījumus.

Ja vēlaties izveidot kredīta notu, atzīmējiet izvēles rūtiņu **Atzīmēt** visām rindām un pēc tam atlasiet **Funkcijas** \> **Izveidot kredīta notu**.

Pēc kredīta notas izveidošanas tiek grāmatots žurnāls. (Grāmatotais žurnāls ir Kreditora patēriņa žurnāls, kā norādīts parametros / r). Tā rezultātā reālu atbildību (kredīts) summa ir pārcelts uz debitora bilanci. Finansiāli šī situācija nozīmē, ka ir notikuši tālāk aprakstītie notikumi.

- Debitora parādu konts ir kreditēts.
- Atlaižu uzkrājuma konts ir debetēts.

Lai apstiprinātu **Vienreizējā maksājuma** veida tirdzniecības notikumu, atlasiet notikumu lapā **Mazumtirdzniecības atlaižu līgumi** un pēc tam cilnē **Summa** atlasiet **Apstiprināt**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Ieturējumu, kas ir jāmaksā, un debitora daļējo maksājumu segšana, izmantojot ieturējumu rīku

Bieži vien, sagaidot atmaksu, debitori izvēlas dažiem rēķiniem piemērot daļējo samaksu. Lai novērstu maksājumu saskaņošanas problēmas nākotnē, debitoru lietvedis reģistrē daļējās samaksas kā ieturējumus, reģistrējot faktiskos klientu maksājumus. Pēc tam ieturējumu rīkā šos debitoru ieturējumus var viegli segt attiecībā pret pieprasījumu summām, kuras jāmaksā uzņēmumam.

Lai reģistrētu klienta daļējo samaksu maksājumu žurnālā, atlasiet **Debitori** \> **Maksājumi** \> **Maksājumu žurnāls** un izveidojiet jaunu maksājumu žurnālu. Pēc tam darbību rūtī atlasiet **Ieturējumi**. Lapā **Ieturējumi** varat izveidot un izsekot summu, kas noteikta kā daļēja samaksa.

Iekasēšanas menedžeris tagad ir atbildīgs par atvērtā kredīta notas transakcijas un daļējās samaksas transakcijas savstarpēju segšanu ieturējumu rīkā.

Lai pārvaldītu ieturējumus, atlasiet **Pārdošana un mārketings** \> **Mazumtirdzniecības atlaides** \> **Ieturējumi** \> **Ieturējumu rīks**. Lapas augšējā sadaļā ir rindas, kas apzīmē daļējās samaksas no debitora. Lapas apakšējā sadaļā norādītas klientu atvērtās kredīta transakcijas. 

Lai segtu ieturējumu attiecībā pret atvērto transakciju, atzīmējiet ieturējumu rindu un pēc tam atvērto transakciju cilnē atzīmējiet rindu. Darbību rūtī noklikšķiniet uz vienuma Uzskaite > Saskaņošana

Sākotnējā pieprasījuma statuss tagad ir iestatīts uz **Pabeigts**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Reklāmas pasākuma un līdzekļu patēriņa efektivitātes analīze

Lai iegūtu pārskatu par programmas svarīgāko statistiku un līdzekļu lietojumu, varat izmantot vairākus pārskatus un analītiskus skatus, kas ir pieejami sadaļā Mazumtirdzniecības atlaižu pārvaldība.

Lapā **Mazumtirdzniecības atlaižu aktivitāte** cilnē **Pārskats** redzama galvenā informācija par mazumtirdzniecības atlaižu līgumu. Citās cilnēs redzama konkrētāka informācija par saistītajiem dokumentiem, maksājumiem un citiem ar šo programmu saistītiem notikumiem.

Cilnē **Kopsavilkums** redzams reklāmas kampaņā pārdoto produktu kopējais daudzums, rēķinā iekļautā pārdošanas summa, kā arī samaksātās atmaksas un vienreizējie maksājumi.

Cilnē **Atmaksu kredīti** ir ietverta detalizēta informācija par atsevišķām atmaksām, kas ir kreditētas klientam.

Lai iegūtu analītiskāku pārskatu par dažādiem reklāmas kampaņas izpildes kritērijiem, var izmantot analīzes skatījumu. Lai atvērtu analīzes skatījumu, noklikšķiniet uz **Pārdošana un mārketings** \> **Mazumtirdzniecības atlaides** \> **Mazumtirdzniecības atlaižu līgumi**. Darbību rūtī noklikšķiniet uz **Analīze**.  

Lai iegūtu analītiskāku pārskatu par dažādiem reklāmas kampaņas izpildes kritērijiem, var izmantot analīzes skatījumu. Lai atvērtu analīzes skatījumu, noklikšķiniet uz **Pārdošana un mārketings** \> **Mazumtirdzniecības atlaides** \> **Mazumtirdzniecības atlaižu līgumi**. Darbību rūtī noklikšķiniet uz **Analīze**. 

