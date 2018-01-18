---
title: "Piedāvājumu pieprasījumi (RFQ)"
description: "Šajā tēmā ir sniegts apskats par piedāvājumu pieprasījumiem (request for quotation — RFQ). Organizācijas izsniedz piedāvājumu pieprasījumus, kad tām ir jāiegādājas preces vai pakalpojumi un tādēļ tās vēlas saņemt konkurētspējīgus piedāvājumus no vairākiem kreditoriem."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 42ab7beb8a269cd37fd9100385bd302e4945c1e0
ms.contentlocale: lv-lv
ms.lasthandoff: 12/14/2017

---

# <a name="requests-for-quotation-rfqs"></a>Piedāvājumu pieprasījumi (RFQ)

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts apskats par piedāvājumu pieprasījumiem (request for quotation — RFQ). Organizācijas izsniedz piedāvājumu pieprasījumus, kad tām ir jāiegādājas preces vai pakalpojumi un tādēļ tās vēlas saņemt konkurētspējīgus piedāvājumus no vairākiem kreditoriem. Piedāvājuma pieprasījumā kreditoriem tiek lūgts piedāvāt norādītā krājuma daudzuma cenas un piegādes laiku. Kreditoriem var lūgt arī norādīt, vai pastāv jebkādas nejaušās izmaksas, piemēram, piegādes izmaksas, kā arī vai pastāv jebkādas atlaides lielu pasūtījumu vai savlaicīgas kreditora rēķina apmaksas gadījumā.

Piedāvājumu pieprasījumu procedūra sastāv no tālāk uzskaitītajiem uzdevumiem.

1. Izveidot piedāvājuma pieprasījumu un izsūtīt to vienam vai vairākiem kreditoriem.
2. Saņemt un reģistrēt piedāvājuma pieprasījuma atbildes (piedāvājumus).
3. Pārsūtīt jūsu pieņemtos piedāvājumus uz pirkšanas pasūtījumu, pirkšanas līgumu vai pirkšanas pieprasījumu.

Nākamajā attēlā ir parādīts apskats par piedāvājuma pieprasījuma procesu.

[![RFQ procesi](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Piedāvājuma pieprasījumu varat izveidot no plānotiem pasūtījumiem, pirkšanas pieprasījuma vai manuāli ievadītiem datiem. Jūsu izveidotais piedāvājuma pieprasījums tiek saukts par piedāvājuma pieprasījuma gadījumu. Piedāvājuma pieprasījuma gadījums ir pamatdokuments, ko jūs izmantojat, lai izsniegtu piedāvājuma pieprasījumu katram kreditoram.

Pēc piedāvājuma pieprasījuma gadījuma sagatavošanas un kreditoru pievienošanas šim piedāvājuma pieprasījuma gadījumam atlasiet **Sūtīt**. Tiek ģenerēts piedāvājuma pieprasījuma žurnāls katram kreditoram, kuram nosūtījāt šo piedāvājuma pieprasījumu. Varat konfigurēt sūtīšanas darbības drukas pārvaldības iestatījumus tā, lai drukātu katra kreditora pārskatu arhivēšanas nolūkos vai sūtītu pārskatu uz katra kreditora e-pasta adresi. Turklāt katra kreditora piedāvājuma pieprasījuma žurnālu varat izmantot, lai ģenerētu pārskatu, ko vēlāk varat nosūtīt vai atkārtoti nosūtīt šim kreditoram. Var arī konfigurēt sūtīšanas darbību tā, lai tā ģenerētu atbildes lapu, ko kreditors var aizpildīt.

Šajā tēmā ir apskatīta procedūra piedāvājumu pieprasījumu apstrādāšanai, kad netiek izmantota kreditora sadarbība. Ja jūsu sistēma ir iestatīta kreditoru sadarbībai, kreditori var ievadīt piedāvājumus tieši programmā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Papildinformāciju skatiet šeit: [Kreditoru sadarbība ar debitoriem](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Ja pēc piedāvājuma pieprasījuma nosūtīšanas ir nepieciešams veikt tā grozījumus, pēc grozījumu pabeigšanas šo piedāvājuma pieprasījumu varat nosūtīt kreditoriem vēlreiz, izmantojot abas grozījumu darbības: Izveidot un Finalizēt.

Kad piedāvājumus saņemat pa e-pastu, jums tie ir jāievada lapā **Atbildes uz piedāvājumu pieprasījumiem**. Ja atlasāt opciju **Kopēt datus uz atbildēm**, atbildē tiek kopēti dati no PP gadījuma, piemēram, daudzums un datumi. Varat mainīt šos datus atbilstoši kreditora piedāvājumam.

Ja kādam kreditoram ir nepieciešama vēl viena iterācija, atlasiet **Atgriezt** lapā **Atbilde uz piedāvājuma pieprasījumu**. Izpildot atgriešanas darbību, tiek ģenerēts jauns žurnāls un pārskats, kas tiks drukāts, arhivēts un nosūtīts atbilstoši drukas pārvaldības iestatījumiem.

Ja PP gadījumam pievienojāt punktu skaitīšanas kritēriju, PP atbildē tiek ietverts punktu skaitīšanas panelis, kur varat ievadīt punktu skaitu. Kopējie rādītāji ir redzami, kad atbildes salīdzināt lapā **Salīdzināt atbildes**. Šajā lapā varat salīdzināt arī citus atbilžu datus, piemēram, rindas cenu, piegādes datumu un kopējo cenu.

Kad esat izvēlējies kādu piedāvājumu vai daļējus piedāvājumus, varat tos pieņemt un pārējos — noraidīt. Tiek ģenerēti pieņemšanas žurnāli un noraidīšanas žurnāli, kā arī atbilstošie pārskati, un tie tiks drukāti, arhivēti un nosūtīti atbilstoši drukas pārvaldības iestatījumiem. Kad pieņemat kādu piedāvājumu vai noteiktas piedāvājuma rindas, tiek ģenerēts pirkšanas līgums vai pirkšanas pasūtījums vai tiek atjaunināts pirkšanas pieprasījums atkarībā no piedāvājuma pieprasījums pirkšanas veida. Varat izveidot tirdzniecības līgumu turpmākai izmantošanai jebkurai atbildei neatkarīgi no tā, vai esat to pieņēmis vai noraidījis.

Piedāvājuma pieprasījuma statuss ir redzams piedāvājuma pieprasījuma virsrakstā, un tas ir atkarīgs no piedāvājuma pieprasījuma rindu statusa. Statuss norāda, cik lielā mērā šo piedāvājuma pieprasījumu esat apstrādājis. Katram piedāvājuma pieprasījumam ir divas statusu vērtības: zemākais statuss un augstākais statuss. Zemākais statuss ir jebkuras rindas PP vismazāk advancētais stāvoklis, un augstākais statuss ir jebkuras rindas PP visvairāk advancētais stāvoklis. Piemēram, ja PP ietvaros vismazāk apstrādātais stāvoklis ir izveidotai rindai, PP zemākais statuss ir **Izveidots**. Ja PP ietvaros visvairāk apstrādātais stāvoklis ir rindai, kas ir nosūtīta kreditoriem, PP augstākais statuss ir **Nosūtīts**. Statusi tiek automātiski atjaunināti līdzko jūs apstrādājat PP.

PP virsraksta zemāko un augstāko statusu varat skatīt lapā **Visi piedāvājuma pieprasījumi**. PP rindas zemāko un augstāko statusu varat skatīt lapas **Piedāvājumu pieprasījumi** cilnē **Rindas**.

Tālāk ir secīgi norādīti piedāvājuma pieprasījuma apstrādes statusi.

1. **Izveidots**
2. **Nosūtīts**
3. **Saņemts**
4. **Pieņemts**, **Atcelts** vai **Noraidīts**

Šie statusi ir detalizētāk aprakstīti tālāk šajā tēmā.

## <a name="setting-up-rfq-functionality"></a>PP funkcionalitātes iestatīšana

Lai varētu izveidot PP gadījumu, vispirms ir jāiestata PP informācija lapā **Sagādes un avotu parametri**. Izveidojot PP gadījumu, varat norādīt noklusējuma vērtības, kas tiek kopētas uz PP. Varat norādīt tālāk uzskaitītās vērtības.

- Jaunu PP pirkšanas tips: **Pirkšanas pasūtījums** vai **Pirkšanas līgums**
- Beigu datums un laiks
- Piegādes informācija un maksājumu nosacījumi
- Lauki, kas ir jāiekļauj PP atbildē

Varat mainīt šīs vērtības noteiktam PP gadījumam.

Ir jākonfigurē arī grozījumu process. Šīs konfigurēšanas ietvaros varat ieslēgt lauku bloķēšanu. Ja ir ieslēgta lauku bloķēšana, tad sagādes speciālistam, kas vēlas veikt piedāvājuma pieprasījuma grozījumus, vispirms cilnes **Piedāvājums** sadaļā **Grozījums** ir jāatlasa **Izveidot**. Kad piedāvājuma pieprasījums ir atjaunināts ar grozījumu, sagādes speciālistam ir jāpabeidz šis process, atlasot **Finalizēt**. Darbība Finalizēt ģenerē e-pasta ziņojumu, kas kreditorus informē par grozīto piedāvājuma pieprasījumu.

Lapā **Sagādes un avotu parametri** varat atlasīt veidni, ko izmantot kreditoriem sūtītajos e-pasta paziņojumos. Kad tiek izveidota veidne, tā var saturēt tālāk norādītos aizstāšanas marķierus.

- %Piedāvājuma pieprasījuma gadījums%
- %Piedāvājuma atgriešanas iemesls%
- %Grozījuma iemesls%
- %Grozījumu sagatavoja%
- %Uzņēmums%
- %Piedāvājuma pieprasījuma gadījuma nosaukums%
- %ExpiryDateTime%
- %Datums%

Marķieri %Piedāvājuma atgriešanas iemesls% un %Grozījuma iemesls%i tiek aizstāti ar tekstu, ko sagādes speciālists var ievadīt, pabeidzot grozījumu vednī **Grozījums**. Marķieru %Grozījumu sagatavoja% un %Uzņēmums% vērtības tiek automātiski iegūtas no PP. Marķieris %Datums% tiek aizstāts ar pašreizējo datumu.

E-pasta veidne ir nepieciešama arī tad, ja piedāvājuma pieprasījumu atceļat pēc tam, kad tas ir nosūtīts. Šī e-pasta veidne tiek izmantota, lai kreditoru kontaktpersonām sūtītu paziņojumu par atcelšanu. Veidnei ir jābūt atlasītai lapā **Sagādes un avotu parametri**. Kad tiek izveidota veidne, tajā var būt tālāk norādītie aizstāšanas marķieri.

- %Atcelšanas iemesls%
- %Piedāvājuma pieprasījuma gadījums% 
- %Piedāvājuma pieprasījumu atcēla%
- %Uzņēmums%
- %Piedāvājuma pieprasījuma gadījuma nosaukums%
- %Datums%

Marķieris %Atcelšanas iemesls% tiek aizstāts ar tekstu, ko sagādes speciālists var ievadīt vednī **Atcelšana**. Marķieris %Datums% tiek aizstāts ar pašreizējo datumu.

Ja vēlaties PP atbildē izmantot iemeslu kodus, lai norādītu, kāpēc piedāvājums tika noraidīts vai pieņemts, jums ir jāuzstāda iemeslu kodu lapā **Kreditoru iemesli**.

Sagādes un avotu lapā **Formas iestatīšana** varat konfigurēt savu drukāto vai saglabāto piedāvājumu pieprasījumu dokumentu izskatu.

> [!NOTE]
> Publiskā sektora konfigurācijai jau nosūtīta piedāvājuma pieprasījuma mainīšanai ir jāizmanto grozījumu process. Kad piedāvājuma pieprasījums ir nosūtīts, lauki tiek bloķēti. Tādēļ, lai veiktu piedāvājuma pieprasījuma izmaiņas, ir jāatlasa **Izveidot**, uzsākot grozījumu procesu, kā aprakstīts iepriekš. Bloķēšanas uzvedību kontrolē lapas **Sagādes un avotu parametri** opcija **Bloķēt piedāvājuma pieprasījumu pēc tā nosūtīšanas**. Pēc noklusējuma šis parametrs ir iestatīts uz **Jā**, un publiskā sektora konfigurācijai šo noklusējuma iestatījumu nevar mainīt. Tādēļ, lai gan konfigurācijā, kas nav publiskā sektora konfigurācija, grozījumu procesu var apstrādāt manuāli, publiskā sektora konfigurācijā tas ir jāizmanto obligāti.

Kad izveidojat pirkšanas pasūtījuma PP un pievienojat šim PP krājumu vienību, tiek ģenerēta krājumu transakcija, kuras ieejas plūsmas statuss ir **Piedāvājuma saņemšana**. Kad izmantojat vispārējo plānu piegāžu aprēķināšanai, tiek ņemtas vērā tikai PP rindas ar šo statusu. Ja vēlaties, lai PP rindas tiktu iekļautas vispārējā plānā kā paredzētās ieejas plūsmas, šī darbība ir jākonfigurē vispārējās plānošanas iestatījumos.

Pirkšanas pārvaldnieks vai aģents var izveidot un uzturēt lūgumu veidus, kas atbilst organizācijas sagādes prasībām. Katru lūguma veidu var saistīt ar kādu punktu skaitīšanas metodi. Punktu skaitīšanas metodes satur kritērijus, ko var izmantot cenu piedāvājumu novērtēšanai. Lūgumu veidi, punktu skaitīšanas metodes un punktu skaitīšanas kritēriji ir jāiestata lapās **Lūguma veids** un **Punktu skaitīšanas metode**.

## <a name="creating-and-sending-an-rfq"></a>PP izveidošana un nosūtīšana

Jūs izveidojat PP, atlasāt kreditorus, kuru piedāvājumus vēlaties saņemt, un pēc tam nosūtāt PP kreditoriem. Varat izmantot drukas pārvaldību, lai piedāvājuma pieprasījuma pārskatu un atbildes lapas pārskatus maršrutētu uz vēlamo galamērķi.

Varat izveidot piedāvājuma pieprasījumu ar pirkšanas veidu **Pirkšanas pasūtījums** vai pirkšanas veidu **Pirkšanas līgums**.

Ja piedāvājuma pieprasījuma veids ir **Pirkšanas pasūtījums**, notiek tālāk aprakstītās darbības.

- Izveidojot PP rindas, tiek ģenerētas krājumu transakcijas, kuru ieejas plūsmas statuss ir **Piedāvājuma saņemšana**.
- Pieņemot piedāvājumu, tiek ģenerēts pirkšanas pasūtījums.

Ja piedāvājuma pieprasījuma veids ir **Pirkšanas līgums**, notiek tālāk aprakstītās darbības.

- PP tiek izmantots līgumam par noteikta preces daudzuma vai vērtības iegādi laika gaitā. Jums ir jāatlasa datumu diapazons, kas attiecas uz pirkšanas līgumu, un tās personas vārdu, kura pārvalda pirkšanas līgumu.
- Pieņemot piedāvājumu, tiek ģenerēts pirkšanas līgums.

Ja PP tiek ģenerēts no pirkšanas pieprasījuma, tiek automātiski piešķirts tips **Pirkšanas pieprasījums**. Jūs nevarat manuāli izveidot tipa **Pirkšanas pieprasījums** PP.

Piedāvājuma pieprasījumu no pirkšanas pieprasījuma varat izveidot tikai tad, ja pirkšanas pieprasījuma statuss ir **Tiek pārskatīts** un jūs esat norīkots nākamā darbplūsmas uzdevuma veikšanai. Pirkšanas pieprasījuma rindas tiek automātiski atjauninātas, kad pieņemat no kreditoriem saņemto piedāvājumu pieprasījumu atbilžu (piedāvājumu) rindas. Kamēr notiek PP apstrāde, nevarat pabeigt, noraidīt vai apstiprināt pirkšanas pieprasījumu vai veikt jebkādu citu darbību ar to.

Kad izveidojat piedāvājuma pieprasījumu, varat atlasīt lūguma veidu. Lūguma veids nosaka punktu skaitīšanas kritēriju kopu, kas tiek izmantota PP atbilžu novērtēšanai.

Varat pievienot anketu PP gadījumam. Pēc tam šī anketa ir redzama visās atbildēs pēc tam, kad esat nosūtījis PP.

PP gadījumam pievienojamos kreditorus var atlasīt trīs veidos.

- Pievienojiet kreditorus pa vienam.
- Meklējiet visus kreditorus, kas atbilst noteiktiem kritērijiem.
- Automātiski pievienojiet visus kreditorus, kas ir apstiprināti PP rindās izmantotajām sagādes kategorijām.

Kad piedāvājuma pieprasījuma gadījums ir gatavs, atlasiet **Sūtīt**. Izpildot sūtīšanas darbību, tiek ģenerēti žurnāli un pārskati, kas tiks drukāti, arhivēti un nosūtīti atbilstoši drukas pārvaldības iestatījumiem.

Ja, sūtot piedāvājuma pieprasījumu kreditoriem, lapā **Piedāvājuma pieprasījuma sūtīšana** opcijas **Cenu pārrēķinā izmantot kreditoru datus** un **Izmantot informāciju par krājumiem pēc kreditora** iestatāt uz **Jā**, tiek automātiski ievadīta noteikta informācija par kreditoru. Varat mainīt šo informāciju lapā **Piedāvājuma pieprasījuma atbilde**.

Tālāk esošajā tabulā ir parādīts, kā mainās PP statuss, kad izveidojat PP un nosūtāt to kreditoriem.

| Darbība                             | Zemākais PP galvenes statuss | Augstākais PP galvenes statuss                        | Zemākais PP rindas statuss | Augstākais PP rindas statuss |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Izveidojiet PP galveni un rindu.    | Izveidota                  | Izveidota                                          | Izveidota                | Izveidota |
| Nosūtiet PP noteiktam kreditoram. | Nosūtīts                     | Nosūtīts                                             | Nosūtīts                   | Nosūtīts |
| Pievienojiet citu kreditoru.                | Izveidota                  | Nosūtīts (PP ir nosūtīts tikai vienam kreditoram.) | Izveidota                | Nosūtīts |
| Nosūtiet PP otram kreditoram. | Nosūtīts                     | Nosūtīts                                             | Nosūtīts                   | Nosūtīts |

> [!NOTE]
> Piedāvājuma pieprasījumam jebkurā brīdī varat pievienot citus kreditorus, un zemākie un augstākie statusi tiek atjaunināti atbilstoši jaunajiem kreditoriem. Piemēram, ja esat saņēmis piedāvājumus no visiem kreditoriem un esat pieņēmis vismaz vienu piedāvājuma rindu, PP virsraksta zemākais statuss ir **Noraidīts**, bet augstākais statuss ir **Pieņemts**. Ja pievienojat jaunu kreditoru, visu rindu zemākais statuss tiek mainīts uz **Izveidots**. Tāpēc piedāvājuma pieprasījuma virsrakstā zemākais statuss tiek atjaunināts uz **Izveidots**, bet augstākais statuss joprojām paliek **Pieņemts**.

## <a name="amending-an-rfq"></a>PP grozījumu veikšana

Dažreiz pēc PP nosūtīšanas ir nepieciešams to mainīt. Piedāvājuma pieprasījums ir jāmaina, piemēram, ja ir mainīti piegādes datumi vai ja vēlaties saņemt papildu preces vai citu preču daudzumu. Varat konfigurēt grozījumu procesu, uzstādot stingrākus vai mazāk stingrus ierobežojumus.

Ja grozījuma procesu konfigurējat, uzstādot stingrākus ierobežojumus, lai modificētu laukus jau nosūtītā piedāvājuma pieprasījuma gadījumā, šajā piedāvājuma pieprasījuma gadījumā ir jāatlasa **Izveidot**, uzsākot grozījumus. Kad izmaiņu veikšana ir pabeigta, jums ir jāatlasa **Finalizēt**. Pēc tam jūs saņemat norādījumus par informācijas pievienošanu e-pasta ziņojumam, kas tiek nosūtīts, lai informētu kreditorus par grozījumiem. Atjauninātais piedāvājuma pieprasījuma pārskats, kurā ir piezīme par grozījumiem, tiek automātiski pievienots e-pasta ziņojumam.

Ja grozījuma procesu konfigurējat, uzstādot mazāk stingrus ierobežojumus, nav nepieciešamības atlasīt **Izveidot**, lai varētu mainīt laukus jau nosūtītā piedāvājuma pieprasījuma gadījumā. Taču piedāvājuma pieprasījumam ir manuāli jāpievieno piezīme par grozījumu, un šis gadījums ir jānosūta vēlreiz. Ņemiet vērā, ka šo pieeju var lietot tikai tad, ja neviena no atbildēm (piedāvājumiem) nav rediģēta. Ja esat ievadījis kādu atbildi un tās statuss ir **Saņemts**, poga **Sūtīt** nav pieejama. Tādā gadījumā jums ir jāatlasa **Izveidot** un pēc tam — **Finalizēt**, tāpat kā procesos ar stingrākiem ierobežojumiem. Pēc tam atbilde tiek atiestatīta, lai atspoguļotu piedāvājuma pieprasījumā veiktās izmaiņas. 

Ja piedāvājumu ievadīšanai kreditori izmanto kreditoru sadarbības interfeisu, jums vienmēr ir jāizmanto grozījumu process, lai informētu kreditorus par piedāvājuma pieprasījuma gadījuma veiktajām izmaiņām. Šī prasība palīdz novērst situācijas, kad kreditori izsaka piedāvājumu par novecojušu piedāvājuma pieprasījuma gadījumu, kamēr tiek veikts viņu piedāvājums. Papildinformāciju par kreditoru sadarbību skatiet šeit: [Kreditoru sadarbība ar ārējiem kreditoriem](vendor-collaboration-work-external-vendors.md). 

Ja saistībā ar piedāvājuma izteikšanu vēlaties uzaicināt papildu kreditorus un ja piedāvājuma pieprasījuma gadījumam nav veiktas nekādas izmaiņas, varat izmantot pogu **Sūtīt**. Jūsu pievienotie kreditori būs redzami lapā **Sūtīt** un saņems e-pasta uzaicinājumu.

## <a name="receiving-and-registering-rfq-replies"></a>PP atbilžu saņemšana un reģistrēšana

Nosūtot PP, tiek automātiski ģenerēta atbildes lapa. Saņemot atbildes (cenu piedāvājumus) uz PP, jums ir jāievada informācija par katru kreditoru konkrētam kreditoram paredzētā PP atbildes lapā. Ja esat pievienojis punktu skaitīšanas kritērijus, varat skaitīt atbilžu iegūtos punktus. Pēc tam jūs salīdzināt kreditoru piedāvājumus un sakārtojat tos atbilstoši saviem punktu skaitīšanas kritērijiem, piemēram, pēc izdevīgākās kopējās cenas vai izdevīgākā kopējā piegādes laika.

Ja piedāvājuma pieprasījuma gadījumam ir pievienota anketa, jums ir manuāli jāievada atbildes uz jautājumiem atbildes lapā.

Varat arī ievadīt alternatīvas rindas, ja attiecīgais piedāvājuma pieprasījuma gadījums ļauj izmantot alternatīvas rindas. Kopsavilkuma cilnē **Pirkšanas piedāvājuma rindas** atlasiet **Pievienot rindu**. Pēc tam ievadiet preces informāciju, piemēram, krājuma kodu vai sagādes kategoriju, daudzumu, cenu un atlaidi.

Ja esat ievadījis atbildi, taču vēlaties saņemt no kreditora jaunu piedāvājumu, varat vēlreiz nosūtīt PP. Tiek ģenerēts jauns žurnāls un pārskats, un varat tos izmantot, lai kreditoram pieprasītu izmaiņas.

Varat skatīt pārskatu par visiem IP un to atbilžu statusiem lapā **Piedāvājuma pieprasījuma sekojums**.

Nākamajā tabulā ir redzams, kā tiek mainīts piedāvājuma pieprasījuma statuss, kad saņemat piedāvājumus un reģistrējat informāciju piedāvājuma pieprasījuma atbildes lapā.

| Darbība                                         | Zemākais piedāvājuma statuss | Augstākais piedāvājuma statuss | Zemākais PP galvenes statuss | Augstākais PP galvenes statuss | Zemākais PP rindas statuss | Augstākais PP rindas statuss |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Reģistrējiet viena kreditora piedāvājumu un saglabājiet to.        | Nosūtīts              | Saņemts           | Nosūtīts                     | Saņemts                  | Nosūtīts                   | Saņemts |
| Reģistrējiet otrā kreditora piedāvājumu un saglabājiet to. | Saņemts          | Saņemts           | Saņemts                 | Saņemts                  | Saņemts               | Saņemts |

> [!NOTE]
> Ja atgriežat piedāvājumu kādam kreditoram papildu pārrunu nolūkos, gan zemākais, gan augstākais statuss joprojām paliek **Saņemts**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Piedāvājumu pieņemšana un noraidīšana un pieņemto piedāvājumu pārsūtīšana uz lejupstraumes dokumentiem

Kad esat noteicis labāko piedāvājumu, piemēram, piedāvājumu ar izdevīgāko kopējo cenu, jūs pieņemat šo piedāvājumu. Varat pieņemt dažas piedāvājuma rindas un noraidīt citas. Varat arī pieņemt dažādu kreditoru piedāvājumu rindas. Ņemiet vērā, ka, pieņemot dažas rindas, tiek piedāvāts noraidīt visas pārējās rindas. Tādēļ, ja vēlaties pieņemt citas rindas, uzvednē ir jāatlasa **Atcelt**. Piedāvājuma pieprasījuma atbildes statuss katram kreditoram, no kura jūs pieņemat piedāvājumus vai to rindas, tiek atjaunināts uz **Pieņemts**. 

Kad pieņemat piedāvājumu vai noteiktas piedāvājuma rindas, tiek automātiski ģenerēts pirkšanas pasūtījums vai pirkšanas līgums. Pēc tam varat noraidīt piedāvājumus no visiem pārējiem kreditoriem.

Atbildē varat pievienot iemesla kodu, lai paskaidrotu, kāpēc pieņēmāt vai noraidījāt piedāvājumu.

Kad pieņemat PP atbildi, kuras tips ir **Pirkšanas pieprasījums**, PP atbildes rindas atjaunina pirkšanas pieprasījuma rindas ar tālāk norādīto informāciju.

- Vienības cena
- Atlaide procentos
- Atlaižu summa
- Pirkšanas izmaksas
- Rindu maksas
- Kreditors
- Ārējais numurs
- Ārējais nosaukums

Tālāk esošajā tabulā ir parādīts, kā tiek mainīts PP statuss, kad pieņemat vai noraidāt kreditoru piedāvājumus.

| Darbība                      | Zemākais piedāvājuma statuss | Augstākais piedāvājuma statuss | Zemākais PP virsraksta statuss | Augstākais PP galvenes statuss | Zemākais PP rindas statuss | Augstākais PP rindas statuss |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Pieņemiet vienu piedāvājumu.     | Saņemts          | Pieņemts           | Saņemts                 | Pieņemts                  | Saņemts               | Pieņemts |
| Noraidīt visus pārējos piedāvājumus.  | Noraidīts          | Pieņemts           | Noraidīts                 | Pieņemts                  | Noraidīts               | Pieņemts |

