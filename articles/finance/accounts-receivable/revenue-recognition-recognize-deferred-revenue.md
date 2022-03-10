---
title: Atlikto ieņēmumu atzīšana
description: Šajā tēmā ir sniegta informācija par to, kā atzīt ieņēmumus, izmantojot ieņēmumu atzīšanas līdzekli.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f6b221104d7012d82a0021b6d8f9cc10fe44cb7b8f3473ab8e7ae7a89be0a5e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726114"
---
# <a name="recognize-deferred-revenue"></a>Atlikto ieņēmumu atzīšana

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Ieņēmumu atzīšanas līdzekli nav iespējams ieslēgt, izmantojot līdzekļu pārvaldību. Pašlaik jāizmanto konfigurācijas atslēgas, lai to ieslēgtu.

Šajā tēmā ir aprakstīts ieņēmumu atzīšanas process ieņēmumu atzīšanas grafikā. Pēc tam, kad pārdošanas pasūtījumam ir iegrāmatots rēķins, katrai pārdošanas pasūtījuma rindai, kurai ir ieņēmumu grafiks, tiek izveidots ieņēmumu atzīšanas grafiks. Ieņēmumu grafiks rindā tiek izmantots, lai noteiktu, vai rindas ieņēmumi ir jāatliek.

## <a name="view-revenue-recognition-schedule-details"></a>Detalizētas informācijas par ieņēmumu atzīšanas grafiku skatīšana

Pastāv divi veidi, kā piekļūt detalizētai informācijai par ieņēmumu atzīšanas grafiku.

- Varat atvērt ieņēmumu atzīšanas grafiku tieši no rēķinā norādītā pārdošanas pasūtījuma. Šādā gadījumā informācija ieņēmumu grafikā tiek filtrēta, lai rādītu detalizētu informāciju tikai atlasītajam pārdošanas pasūtījumam. Šī pieeja ir noderīga, ja validējat pārdošanas pasūtījuma grafika detalizēto informāciju.
- Varat atvērt ieņēmumu atzīšanas grafiku no lapas **Ieņēmumu atzīšana \> Periodiskie uzdevumi**. Šo pieeju bieži izmanto, kad ieņēmumi tiek atzīti perioda beigās. Kad lapa tiek atvērta pirmo reizi, netiek rādīta nekāda informācija. Izmantojiet filtrus virs režģa, lai definētu kritērijus grafika detalizētajai informācijai, kas jāparāda. Varat filtrēt pēc rēķina datumiem, ievadot datumu diapazonu, pārdošanas pasūtījumu, debitoru, projekta ID vai stāvokli.

[![Ieņēmumu grafiku lapas ilustrācija.](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

Kopsavilkuma cilne **Finanšu dimensija** zem režģa parāda pārdošanas pasūtījuma rindas finanšu dimensijas. Šīs dimensijas tika ņemtas vērā, veicot grāmatošanu atliktajos ieņēmumos. Tās tiek ņemtas vērā arī tad, kad ieņēmumi tiek atzīti. Izmantotās dimensiju vērtības ir atkarīgas no konta struktūras, kas ir piešķirta ieņēmumu un atlikto ieņēmumu galvenajiem kontiem.

## <a name="recognize-revenue"></a>Ieņēmumu atzīšana

Atzīstiet ieņēmumus, palaižot procesu **Izveidot žurnālu** lapā **Ieņēmumu atzīšana**. Šo lapu varat atvērt no pārdošanas pasūtījuma vai arī sadaļā **Periodiskie uzdevumi**. Ja process tiek palaists no pārdošanas pasūtījuma, tas atzīst ieņēmumus tikai atlasītajam pārdošanas pasūtījumam. Parasti tā vietā process tiek palaists no sadaļas **Periodiskie uzdevumi** tā, lai tas atzītu ieņēmumus visiem iegrāmatotajiem pārdošanas pasūtījumu rēķiniem.

Lai definētu ieņēmumu atlases un grāmatošanas kritērijus, atlasiet **Izveidot žurnālu**, lai atvērtu dialoglodziņu **Izveidot žurnālu**.

[![Žurnāla parametru opciju izveide.](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Lai noteiktu grāmatošanas datumu, kas tiek izmantots ieņēmumu atzīšanas laikā, dialoglodziņā lietojiet lauku grupas **Apstrādes datums** opcijas. Atlasot **Atlasītais datums**, varat ievadīt grāmatošanas datumu laukā **Darījuma datums**. Atlasot **Ieņēmumu grafika datums**, transakcijas datums netiek izmantots. Tā vietā katras grafika rindas lauka **Atzīšanas datums** vērtība tiek izmantota kā grāmatošanas datums.

Pēc tam laukā **Sākuma datums** ievadiet ieņēmumu atzīšanas sākuma datumu. Visas grafika rindas, kurās atzīšanas datums ir vienāds ar sākuma datumu vai pirms tā, tiks atzītas, ja vien tās nav aizturētas.

Pēc tam, kad esat beidzis definēt datumus, dialoglodziņā atlasiet **Labi**, lai izveidotu žurnālu. Jūs saņemsit informatīvu ziņojumu, kurā parādīts izveidoto transakciju skaits un žurnāls, kurā tās izveidotas. Žurnāls netiek grāmatots automātiski. Tādēļ ieņēmumu atzīšanas vadītājam ir laiks pārbaudīt, kuras grafika rindas tiek atzītas.

Pēc procesa izpildes grafika rindām, kas tika pārsūtītas uz žurnālu, tiek piešķirts statuss **Apstrādāts**. Karodziņš **Apstrādāts** norāda, ka rindas ir pārsūtītas uz žurnālu, bet tās var grāmatot vai negrāmatot. Kad ieņēmumu atzīšanas žurnāls ir iegrāmatots, karodziņš **Apstrādāts** saglabājas. Ja ieņēmumu atzīšanas žurnāls tiek izdzēsts vai arī ja rinda tiek izdzēsta, karodziņš **Apstrādāts** tiek noņemts. Šādā veidā rindu var atzīt, kad process **Izveidot žurnālu** tiek palaists vēlreiz.

[![Lapa Ieņēmumu atzīšanas grafiki.](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Lapā **Ieņēmumu atzīšanas žurnāls** (**Ieņēmumu atzīšana \> Žurnāla ieraksti \> Ieņēmumu atzīšanas žurnāls**) atveriet **Rindas**, lai skatītu detalizētu informāciju par to, kas tiek atzīts. Katrai grafika rindai, kas tiek atzīta, vienmēr tiek izveidota atsevišķa transakcija pat tad, ja visas rindas ir iegrāmatotas tajā pašā datumā, izmantojot vienādus virsgrāmatas kontus.

[![Lapa Žurnāla dokuments.](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Kolonnā **konts** ir parādīts atlikto ieņēmumu virsgrāmatas konts. Šo virsgrāmatas kontu nevar rediģēt. Šis ierobežojums palīdz garantēt, ka tiek atbrīvots pareizs atlikto ieņēmumu virsgrāmatas konts. Šis virsgrāmatas konts nav pārbaudīts attiecībā pret konta struktūru, jo tas, iespējams, ir mainīts kopš pēdējo reizi tika veikta grāmatošana uz atlikto ieņēmumu virsgrāmatas kontu.

Kolonnā **Korespondējošais konts** ir parādīts ieņēmumu virsgrāmatas konts. Pēc noklusējuma ieņēmumu virsgrāmatas konts tiek iegūts no krājumu grāmatošanas metodēm un finanšu dimensijas tiek iegūtas no pārdošanas pasūtījuma rindas. Šis virsgrāmatas konts tiek validēts attiecībā pret pašreizējo konta struktūru. Tomēr to var rediģēt, ja konta struktūra ir mainījusies un ir nepieciešamas papildu finanšu dimensijas.

Noklusējuma summa tiek iegūta no atbilstošās grafika rindas, un to nevar mainīt.

Pēc noklusējuma, ja pārdošanas pasūtījums ir daudzvalūtu pārdošanas pasūtījums, maiņas kurss tiek iestatīts uz maiņas kursu no rēķina. Tas palīdz nodrošināt, ka uzskaites valūtas un pārskata valūtas summas tiek pilnībā atbrīvotas. Noapaļošanas dēļ grafika pēdējās rindas maiņas kurss var nedaudz atšķirties no rēķina likmes.

Pēc tam, kad ieņēmumu atzīšanas žurnāls ir iegrāmatots, dokuments tiek ievadīts grafikā. Ja vienai grafika rindai ir vairāk nekā viens dokuments, rindā tiek parādīta zvaigznīte (\*). Lai skatītu dokumentus, kas iegrāmatoti šai rindai, atlasiet **Dokumentu transakcijas**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Detalizētas informācijas par ieņēmumu atzīšanas grafiku modificēšana

Vairumu datu detalizētajā informācijā par ieņēmumu grafiku nevar rediģēt. Grafikam nevar pievienot jaunas rindas, un esošās rindas nevar dzēst. Detalizētā informācija par ieņēmumu grafiku jāuztur katrai pārdošanas pasūtījuma rindai, lai palīdzētu nodrošināt, ka laika gaitā organizācija atzīst tādu pašu summu, kas tika atlikta.

### <a name="edit-schedule-lines"></a>Grafika rindu rediģēšana

Grafika rindās ir atļauts veikt dažus rediģējumus. Rindās var mainīt tālāk norādītos laukus.

- **Aizturēts** — šo karodziņu var iestatīt vai notīrīt pirms rindas apstrādes. Lai notīrītu karodziņu, atlasiet rindu un pēc tam atlasiet **Noņemt aizturēšanu**. Ieņēmumus nevar atzīt rindās, kas ir aizturētas. Rindas var aizturēt automātiski, ja ieņēmumu grafiks ir iestatīts automātiskai aizturēšanai.

    [![Ieņēmumu grafiki — grafika rindu rediģēšana.](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Atzīšanas datums** — atzīšanas datumu var mainīt pirms rindas apstrādes. Izpildot procesu, kas izveido žurnālu ieņēmumu atzīšanai, laukā **Ieņēmumu atzīšana sākuma datumā** tiek ievadīts datums. Šis datums tiek salīdzināts ar datumu laukā **Atzīšanas datums**, lai noteiktu, kuras rindas jāatzīst.
- **Izlaižamā summa** — summu, kas tiks izlaista, var mainīt pirms rindas apstrādes. Varat samazināt atzīstamo ieņēmumu summu, bet to nevar palielināt. Šis lauks ļauj organizācijai atzīt daļu no ieņēmumiem atzīšanas datumā. Ja summa tiek mainīta, summa laukā **Atlikusī summa** rāda, cik daudz ieņēmumu vēl joprojām ir jāatzīst.
- **Izlaižamais daudzums** — ja ieņēmumu grafiks ir iestatīts vienam gadījumam vai vienam mēnesim, lauks **Izlaižamais daudzums** rāda pārdošanas pasūtījuma rindas daudzumu. Šo lauku var arī rediģēt, un tas nodrošina citu veidu, kā atzīt daļu no ieņēmumiem. Piemēram, ja daudzums rindā ir 5, varat ignorēt daudzumu, lai tas būtu mazāks par 5. Summa laukā **Izlaižamā summa** tiek atjaunināta proporcionāli.

### <a name="update-contract-terms"></a>Līguma nosacījumu atjaunināšana

Detalizēta informācija par ieņēmumu grafiku tiek veidota, pamatojoties uz ieņēmumu grafiku, kas tiek piešķirts pārdošanas pasūtījuma rindai, grāmatojot rēķinu. Ja pārdošanas pasūtījuma rindas ieņēmumu grafiks nav pareizs, pārdošanas pasūtījumā to nevar mainīt pēc tam, kad pārdošanas pasūtījumam ir izrakstīts rēķins. Tā vietā ir jāizmanto poga **Atjaunināt līguma nosacījumus**, lai mainītu ieņēmumu grafiku. Ieņēmumu grafiku var mainīt pirms vai pēc ieņēmumu atzīšanas.

Lai mainītu grafiku, atlasiet jebkuru grafika rindu krājumam, ko maināt. Tālāk esošajā ilustrācijā ir atlasīta rinda krājumam S0008, kas tika grāmatots, izmantojot 12 mēnešu ieņēmumu grafiku. Atlasot pogu **Atjaunināt līguma nosacījumus**, dialoglodziņā tiek parādīti līguma sākuma un beigu datumi un ieņēmumu grafiks.

[![Līguma sākuma un beigu datumi.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Mainiet līguma sākuma un beigu datumus, lai tie atspoguļotu pareizo datumu diapazonu. Kad maināt datumu diapazonu, vērtībai laukā **Gadījumu skaits** jāatbilst sistēmā definētajam ieņēmumu grafikam. Šajā piemērā ir jāiestata 24 mēnešu ieņēmumu grafiks, jo līgums tika mainīts uz 24 mēnešu līgumu. Tā kā pastāv 24 mēnešu ieņēmumu grafiks, tas tiek ievadīts pēc noklusējuma, un līgumu var mainīt. Ja nepastāv ieņēmumu grafiks, kam ir atbilstošs gadījumu skaits, līgumu nevar mainīt. Kad esat pabeidzis līguma noteikumu un ieņēmumu grafika atjaunināšanu atbilstoši savām vajadzībām, dialoglodziņā atlasiet **Labi**, lai saglabātu veiktās izmaiņas.

[![Atjaunināta līguma datumu diapazons.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Līguma izmaiņām ir tālāk izklāstītā ietekme uz detalizēto informāciju par ieņēmumu grafiku.

- Ja precei nav atrasti nekādi ieņēmumi, visa iepriekšējā detalizētā informācija par grafiku tiek noņemta un aizstāta ar jauno detalizēto informāciju par ieņēmumu grafiku. Piemēram, krājumam S0008 sākotnēji bija 12 rindas detalizētajā informācijā par grafiku. Šīs 12 rindas tiek noņemtas un aizstātas ar 24 rindām, pamatojoties uz jauno ieņēmumu grafiku.
- Ja ieņēmumi ir atzīti precei, daļa ieņēmumu tika atzīta nepareizi, jo atzīšana tika balstīta uz nepareizu ieņēmumu grafiku. Šīs rindas ir jāatsauc un jāatzīst vēlreiz, pamatojoties uz jauno grafiku. Šādā gadījumā tiek izveidotas jaunas ieņēmumu grafika rindas, kurām ir negatīvas summas sākotnējā atzīšanas datumā. Pēc tam tiek izveidotas jaunas rindas, lai atzītu summas, pamatojoties uz jauno ieņēmumu grafiku. Piemēram, 2019. gada 8. augustā jūs atzināt ieņēmumus 10,53 ASV dolāru apmērā. 2019. gada 8. septembrī jūs atzināt ieņēmumus 13,16 ASV dolāru apmērā. Tādēļ tajā pašā datumā tiek izveidotas divas jaunas rindas. Viena rinda ir paredzēta 10,53 ASV dolāriem un otra rinda — 13,16 ASV dolāriem. Pēc tam tiek izveidotas divdesmit četras jaunas rindas un kopējie atliktie ieņēmumi 160,61 ASV dolāru apmērā tiek tajās sadalīti. Varat grāmatot storno rindas, palaižot procesu **Izveidot žurnālu**.

[![Ieņēmumu atzīšanas grafiks.](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]