---
title: "Piedāvājuma pieprasījumi (PP)"
description: "Šajā rakstā ir sniegts pārskats par piedāvājuma pieprasījumiem (PP), kuras organizācijas izsniedz, kad tām jāiegādājas preces vai pakalpojumus, un tādēļ vēlas saņemt vairāku kreditoru konkurētspējīgus piedāvājumus. Piedāvājuma pieprasījumā kreditoriem tiek lūgts piedāvāt norādītā krājuma daudzuma cenas un piegādes laiku. Kreditoriem var lūgt arī norādīt, vai pastāv jebkādas nejaušās izmaksas, piemēram, piegādes izmaksas, kā arī vai pastāv jebkādas atlaides lielu pasūtījumu vai savlaicīgas kreditora rēķina apmaksas gadījumā."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d681f4c107a9dbc1ea8c5e1de38b2d45cf19bcfa
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="request-for-quotations-rfqs"></a>Piedāvājuma pieprasījumi (PP)

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par piedāvājuma pieprasījumiem (PP), kuras organizācijas izsniedz, kad tām jāiegādājas preces vai pakalpojumus, un tādēļ vēlas saņemt vairāku kreditoru konkurētspējīgus piedāvājumus. Piedāvājuma pieprasījumā kreditoriem tiek lūgts piedāvāt norādītā krājuma daudzuma cenas un piegādes laiku. Kreditoriem var lūgt arī norādīt, vai pastāv jebkādas nejaušās izmaksas, piemēram, piegādes izmaksas, kā arī vai pastāv jebkādas atlaides lielu pasūtījumu vai savlaicīgas kreditora rēķina apmaksas gadījumā.

Piedāvājuma pieprasījuma (PP) process ietver tālāk norādītos uzdevumus.

-   PP izveidošana un sūtīšana vienam vai vairākiem kreditoriem
-   PP atbilžu (piedāvājumu) saņemšana un reģistrēšana
-   Pieņemto piedāvājumu pārsūtīšana uz pirkšanas pasūtījumu, pirkšanas līgumu vai pirkšanas pieprasījumu

Šajā ilustrācijā parādīts pārskats par PP procesu.  

[![Piedāvājuma pieprasījuma process](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Varat izveidot PP no plānotiem pasūtījumiem, pirkšanas pieprasījuma vai manuāli ievadītiem datiem. Izveidotais PP tiek saukts par PP gadījumu, un tas ir galvenais dokuments, ko izmantojat, lai izsniegtu PP katram kreditoram. Pēc PP gadījuma sagatavošanas un kreditoru pievienošanas noklikšķiniet uz **Nosūtīt** PP gadījuma sadaļā — katram kreditoram, kuram nosūtāt PP, tiek ģenerēts PP žurnāls. Varat konfigurēt sūtīšanas darbības drukas pārvaldības iestatījumus tā, lai drukātu katra kreditora pārskatu arhivēšanas nolūkos vai sūtītu pārskatu uz katra kreditora e-pasta adresi. Turklāt katra kreditora PP žurnālu var izmantot, lai ģenerētu pārskatu, ko vēlāk varat nosūtīt vai atkārtoti nosūtīt kreditoram. Var arī konfigurēt sūtīšanas darbību tā, lai tiktu ģenerēta atbildes lapa, ko kreditors var aizpildīt.  

Ja pēc PP nosūtīšanas ir nepieciešams veikt grozījumus, pēc grozījumu pabeigšanas varat atkārtoti nosūtīt PP kreditoriem.  

Saņemot piedāvājumus, tie ir jāievada lapa **Atbildes uz piedāvājuma pieprasījumiem**. Ja atlasāt opciju **Kopēt datus uz atbildēm**, atbildē tiek kopēti dati no PP gadījuma, piemēram, daudzums un datumi. Varat mainīt šos datus atbilstoši kreditora piedāvājumam.  

Ja konkrētam kreditoram ir nepieciešama vēl viena atbilde, noklikšķiniet uz **Atgriezt**lapā **Piedāvājuma pieprasījuma atbilde**. Izpildot atgriešanas darbību, tiek ģenerēts jauns žurnāls un pārskats, kas tiks drukāts, arhivēts un nosūtīts atbilstoši drukas pārvaldības iestatījumiem.  

Ja PP gadījumam pievienojāt punktu skaitīšanas kritēriju, PP atbildē tiek ietverts punktu skaitīšanas panelis, kur varat ievadīt punktu skaitu. Kopējais punktu skaits tiek rādīts, kad salīdzināt atbildes lapā **Salīdzināt atbildes**, kur varat salīdzināt arī citus atbilžu datus, piemēram, rindas cenu, piegādes datumu un kopējo cenu.  

Kad esat izvēlējies piedāvājumu vai daļēju piedāvājumu, varat to pieņemt un noraidīt pārējos. Tiek ģenerēti pieņemšanas žurnāli, noraidīšanas žurnāli un atbilstošie pārskati. Tie tiks drukāti, arhivēti un nosūtīti saskaņā ar drukas pārvaldības iestatījumiem. Kad pieņemat piedāvājumu vai noteiktas piedāvājuma rindas, tiek ģenerēts pirkšanas līgumu vai pirkšanas pasūtījums vai tiek atjaunināts pirkšanas pieprasījums atkarībā no PP pirkšanas veida. Varat izveidot tirdzniecības līgumu turpmākai izmantošanai jebkurai atbildei neatkarīgi no tā, vai esat to pieņēmis vai noraidījis.  

PP statuss ir redzams PP virsrakstā un ir atkarīgs no PP rindu statusa. Statuss norāda, cik lielā mērā esat apstrādājis PP. Katram PP ir divas statusu vērtības: mazākais un lielākais. Zemākais statuss ir jebkuras rindas PP vismazāk advancētais stāvoklis, un augstākais statuss ir jebkuras rindas PP visvairāk advancētais stāvoklis. Piemēram, ja PP ietvaros vismazāk apstrādātais stāvoklis ir izveidotai rindai, PP zemākais statuss ir **Izveidots**. Ja PP ietvaros visvairāk apstrādātais stāvoklis ir rindai, kas ir nosūtīta kreditoriem, PP augstākais statuss ir **Nosūtīts**. Statusi tiek automātiski atjaunināti līdzko jūs apstrādājat PP.  

PP virsraksta zemāko un augstāko statusu varat skatīt lapā **Visi piedāvājuma pieprasījumi**. PP rindas zemāko un augstāko statusu varat skatīt lapas **Piedāvājumu pieprasījumi** cilnē **Rindas**.  

Tālāk ir secīgi norādīti PP apstrādes statusi.

1.  **Izveidots**
2.  **Nosūtīts**
3.  **Saņemts**
4.  **Pieņemts**/**Atcelts**/**Noraidīts**

Statusi ir detalizētāk aprakstīti sadaļās šī raksta turpinājumā.

## <a name="setting-up-rfq-functionality"></a>PP funkcionalitātes iestatīšana
Lai varētu izveidot PP gadījumu, vispirms ir jāiestata PP informācija lapā **Sagādes un avotu parametri**. Izveidojot PP gadījumu, varat norādīt noklusējuma vērtības, kas tiek kopētas uz PP. Varat norādīt tālāk uzskaitītās vērtības.

-   Jaunu PP pirkšanas tips: **Pirkšanas pasūtījums** vai **Pirkšanas līgums**
-   Beigu datuma un laika iestatījumi
-   Piegādes informācija un maksājumu nosacījumi.
-   Lauki, kas ir jāiekļauj PP atbildē

Varat mainīt šīs vērtības noteiktam PP gadījumam. Ir jākonfigurē arī grozījumu process. Šīs konfigurēšanas ietvaros varat ieslēgt lauku bloķēšanu. Ja ir ieslēgta lauku bloķēšana, sagādes speciālistam, kas vēlas veikt PP grozījumus, vispirms ir jānoklikšķina uz **Izveidot** cilnes **Piedāvājums** sadaļā **Grozījums**. Kad PP ir atjaunināts, veicot grozījumu, sagādes speciālistam ir jāpabeidz process, noklikšķinot uz **Pabeigt**.** **Veicot pabeigšanas darbību, tiek ģenerēts e-pasta ziņojums, lai paziņotu kreditoriem par grozīto PP. Kreditoriem sūtītā e-pasta paziņojuma veidni varat atlasīt lapā **Sagādes un avotu parametri**. Kad tiek izveidota veidne, tā var saturēt tālāk norādītos aizstāšanas marķierus.

-   %Piedāvājuma atgriešanas iemesls%
-   %Grozījuma iemesls%
-   %Grozījumu sagatavoja%
-   %Uzņēmums%

Marķieri %Piedāvājuma atgriešanas iemesls% un %Grozījuma iemesls%i tiek aizstāti ar tekstu, ko sagādes speciālists var ievadīt, pabeidzot grozījumu vednī **Grozījums**. Marķieru %Grozījumu sagatavoja% un %Uzņēmums% vērtības tiek automātiski iegūtas no PP.  

Ja vēlaties PP atbildē izmantot iemeslu kodus, lai norādītu, kāpēc piedāvājums tika noraidīts vai pieņemts, jums ir jāuzstāda iemeslu kodu lapā **Kreditoru iemesli**.  

Varat konfigurēt drukātā vai saglabātā PP dokumenta izskatu moduļa Sagāde un avoti lapā **Formas iestatījumi**.  

Kad izveidojat pirkšanas pasūtījuma PP un pievienojat šim PP krājumu vienību, tiek ģenerēta krājumu transakcija, kuras ieejas plūsmas statuss ir **Piedāvājuma saņemšana**. Kad izmantojat vispārējo plānu piegāžu aprēķināšanai, tiek ņemtas vērā tikai PP rindas ar šo statusu. Ja vēlaties, lai PP rindas tiktu iekļautas vispārējā plānā kā paredzētās ieejas plūsmas, šī darbība ir jākonfigurē vispārējās plānošanas iestatījumos.  

Kā iepirkumu nodaļas vadītājs vai aģents varat izveidot un uzturēt lūgumu veidus, kas atbilst jūsu organizācijas sagādes prasībām. Katrs lūguma veids var būt saistīts ar punktu skaitīšanas metodēm. Punktu skaitīšanas metodes satur kritērijus, ko var izmantot cenu piedāvājumu novērtēšanai. Lūgumu veidi, punktu skaitīšanas metodes un punktu skaitīšanas kritēriji ir jāiestata lapās **Lūguma veids** un **Punktu skaitīšanas metode**.

## <a name="creating-and-sending-an-rfq"></a>PP izveidošana un nosūtīšana
Jūs izveidojat PP, atlasāt kreditorus, kuru piedāvājumus vēlaties saņemt, un pēc tam nosūtāt PP kreditoriem. Varat izmantot drukas pārvaldību, lai maršrutētu PP pārskatu un atbildes lapas pārskatus uz vēlamo galamērķi.  

Varat izveidot PP ar pirkšanas tipu **Pirkšanas pasūtījums** vai **Pirkšanas līgums**  

Ja PP tiek ģenerēts no pirkšanas pieprasījuma, tiek automātiski piešķirts tips **Pirkšanas pieprasījums**. Jūs nevarat manuāli izveidot tipa **Pirkšanas pieprasījums** PP. Ja PP tips ir **Pirkšanas pasūtījums**

-   Izveidojot PP rindas, tiek ģenerētas krājumu transakcijas, kuru ieejas plūsmas statuss ir **Piedāvājuma saņemšana**.
-   Pieņemot piedāvājumu, tiek ģenerēts pirkšanas pasūtījums.

Ja PP tips ir **Pirkšanas līgums**

-   PP tiek izmantots līgumam par noteikta preces daudzuma vai vērtības iegādi laika gaitā. Jums ir jāatlasa datumu diapazons, kas attiecas uz pirkšanas līgumu, un tās personas vārdu, kura pārvalda pirkšanas līgumu.
-   Pieņemot piedāvājumu, tiek ģenerēts pirkšanas līgums.

Varat izveidot PP no pirkšanas pieprasījuma tikai tad, ja pirkšanas pieprasījuma statuss ir **Tiek pārskatīts** un jūs esat norīkots nākamā darbplūsmas uzdevuma veikšanai. Pirkšanas pieprasījuma rindas tiek automātiski atjauninātas, kad pieņemat no kreditoriem saņemto PP atbilžu (piedāvājumu) rindas. Kamēr notiek PP apstrāde, nevarat pabeigt, noraidīt vai apstiprināt pirkšanas pieprasījumu vai veikt jebkādu citu darbību ar to.  

Izveidojot PP, varat atlasīt noteiktu lūguma veidu. Lūguma veids nosaka punktu skaitīšanas kritēriju kopu, kas tiek izmantota PP atbilžu novērtēšanai.  

Varat pievienot anketu PP gadījumam. Pēc tam šī anketa ir redzama visās atbildēs pēc tam, kad esat nosūtījis PP.  

PP gadījumam pievienojamos kreditorus var atlasīt trīs veidos.

-   Pievienojiet kreditorus pa vienam.
-   Meklējiet visus kreditorus, kas atbilst noteiktiem kritērijiem.
-   Automātiski pievienojiet visus kreditorus, kas ir apstiprināti PP rindās izmantotajām sagādes kategorijām.

Kad PP gadījumu ir pabeigts, noklikšķiniet uz **Sūtīt**. Izpildot sūtīšanas darbību, tiek ģenerēti žurnāli un pārskati, kas tiks drukāti, arhivēti un nosūtīti atbilstoši drukas pārvaldības iestatījumiem.  

Ja, sūtot pieprasījumu kreditoriem, lapā **Piedāvājuma pieprasījuma sūtīšana** atzīmējāt izvēles rūtiņas **Cenu pārrēķinā izmantot kreditoru datus** un **Izmantot informāciju par krājumiem pēc kreditora**, tiek automātiski ievadīta noteikta informācija par kreditoru. Varat mainīt šo informāciju lapā **Piedāvājuma pieprasījuma atbilde**.  

Tālāk esošajā tabulā ir parādīts, kā mainās PP statuss, kad izveidojat PP un nosūtāt to kreditoriem.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Darbība**                         | **Zemākais PP virsraksta statuss** | **Augstākais PP virsraksta statuss**                   | **Zemākais PP rindas statuss** | **Augstākais PP rindas statuss** |
| Izveidojiet PP galveni un rindu.    | Izveidota                      | Izveidota                                         | Izveidota                    | Izveidota                     |
| Nosūtiet PP noteiktam kreditoram. | Nosūtīts                         | Nosūtīts                                            | Nosūtīts                       | Nosūtīts                        |
| Pievienojiet citu kreditoru.                | Izveidota                      | Nosūtīts (PP ir nosūtīts tikai vienam kreditoram.) | Izveidota                    | Nosūtīts                        |
| Nosūtiet PP otram kreditoram. | Nosūtīts                         | Nosūtīts                                            | Nosūtīts                       | Nosūtīts                        |

**Piezīme.** Jebkurā brīdī varat pievienot citus kreditorus PP, un zemākie un augstākie statusi tiek mainīti atbilstoši jaunajiem kreditoriem. Piemēram, ja esat saņēmis piedāvājumus no visiem kreditoriem un esat pieņēmis vismaz vienu piedāvājuma rindu, PP virsraksta zemākais statuss ir **Noraidīts**, bet augstākais statuss ir **Pieņemts**. Ja pievienojat jaunu kreditoru, visu rindu zemākais statuss tiek mainīts uz **Izveidots**. Tāpēc PP virsraksta zemākais statuss tiek mainīts uz **Izveidots** un augstākais statuss joprojām paliek **Pieņemts**.

## <a name="amending-an-rfq"></a>PP grozījumu veikšana
Dažreiz pēc PP nosūtīšanas ir nepieciešams to mainīt. Tā var notikt, jo, piemēram, ir mainīts piegādes datums vai vēlaties saņemt papildu preces vai citu preču daudzumu. Varat konfigurēt grozījumu procesu, uzstādot stingrākus vai mazāk stingrus ierobežojumus.  

Ja izmantojat grozījumu procesu ar stingrākiem ierobežojumiem, lai varētu mainīt PP gadījuma laukus, vispirms PP gadījumā ir jānoklikšķina uz **Izveidot**, lai sāktu grozījuma procesu. Kad esat veicis visas izmaiņas, ir jānoklikšķina uz **Pabeigt**. Pēc tam saņemat norādījumus par informācijas pievienošanu e-pasta ziņojumam, kas tiek nosūtīts, lai informētu kreditorus par grozījumiem. Ziņojumam tiek automātiski pievienots atjauninātais PP pārskats, kas satur piezīmi par grozījumiem.  

Ja izmantojat grozījumu procesu ar mazāk stingriem ierobežojumiem, pirms jau nosūtīta PP gadījuma lauku mainīšanas nav nepieciešams izveidot grozījumu. Taču PP ir manuāli jāpievieno piezīme par grozījumu.

## <a name="receiving-and-registering-rfq-replies"></a>PP atbilžu saņemšana un reģistrēšana
Nosūtot PP, tiek automātiski ģenerēta atbildes lapa. Saņemot atbildes (cenu piedāvājumus) uz PP, jums ir jāievada informācija par katru kreditoru konkrētam kreditoram paredzētā PP atbildes lapā. Ja esat pievienojis punktu skaitīšanas kritēriju, varat novērtēt atbildes. Pēc tam jūs salīdzināt kreditoru piedāvājumus un sakārtojat tos atbilstoši saviem punktu skaitīšanas kritērijiem, piemēram, pēc izdevīgākās kopējās cenas vai izdevīgākā kopējā piegādes laika.  

Ja PP gadījumam ir pievienota anketa, jums ir manuāli jāievada atbildes uz jautājumiem atbildes lapā.  

Ja ir jāievada citas rindas un PP gadījumā tas ir atļauts, kopsavilkuma cilnē **Pirkšanas piedāvājuma rindas** noklikšķiniet uz **Pievienot rindu**. Pēc tam ievadiet preces informāciju, piemēram, krājuma kodu vai sagādes kategoriju, daudzumu, cenu un atlaidi.  

Ja esat ievadījis atbildi, taču vēlaties saņemt no kreditora jaunu piedāvājumu, varat vēlreiz nosūtīt PP. Tādējādi tiek ģenerēts jauns žurnāls un pārskats, ko varat izmantot, lai kreditoram pieprasītu izmaiņas.  

Varat skatīt pārskatu par visiem IP un to atbilžu statusiem lapā **Piedāvājuma pieprasījuma sekojums**.  

Tālāk esošajā tabulā ir redzams, kā tiek mainīts PP statuss, kad saņemat piedāvājumus un reģistrējat informāciju PP atbildes lapā.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Darbība**                                     | **Zemākais piedāvājuma statuss** | **Augstākais piedāvājuma statuss** | **Zemākais PP virsraksta statuss** | **Augstākais PP virsraksta statuss** | **Zemākais PP rindas statuss** | **Augstākais PP rindas statuss** |
| Reģistrējiet viena kreditora piedāvājumu un saglabājiet to.        | Nosūtīts                  | Saņemts               | Nosūtīts                         | Saņemts                      | Nosūtīts                       | Saņemts                    |
| Reģistrējiet otra kreditora piedāvājumu un saglabājiet to. | Saņemts              | Saņemts               | Saņemts                     | Saņemts                      | Saņemts                   | Saņemts                    |

**Piezīme.** Ja atgriežat piedāvājumu kreditoram papildu pārrunām, gan zemākais, gan augstākais statuss joprojām paliek **Saņemts**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Piedāvājumu pieņemšana un noraidīšana un pieņemto piedāvājumu pārsūtīšana uz lejupstraumes dokumentiem

Kad esat noteicis labāko piedāvājumu, piemēram, piedāvājumu ar izdevīgāko kopējo cenu, jūs pieņemat šo piedāvājumu. Attiecīgā kreditora PP atbildes statuss tiek atjaunināts uz **Pieņemts**. Kad pieņemt piedāvājumu vai noteiktu piedāvājuma rindu, tiek automātiski ģenerēts pirkšanas pasūtījums vai pirkšanas līgums un varat noraidīt citu kreditoru piedāvājumus.  

Kad pieņemat PP atbildi, kuras tips ir **Pirkšanas pieprasījums**, PP atbildes rindas atjaunina pirkšanas pieprasījuma rindas ar tālāk norādīto informāciju.

-   Vienības cena
-   Atlaide procentos
-   Atlaižu summa
-   Pirkšanas izmaksas
-   Rindu maksas
-   Piegādātājs
-   Ārējais numurs
-   Ārējais nosaukums

Atbildē varat pievienot iemesla kodu, lai paskaidrotu, kāpēc pieņēmāt vai noraidījāt piedāvājumu.  

Varat pieņemt dažas piedāvājuma rindas un noraidīt citas. Varat arī pieņemt dažādu kreditoru piedāvājumu rindas. Taču ņemiet vērā, ka, pieņemot dažas rindas, tiek piedāvāts noraidīt visas citas rindas. Tāpēc, ja vēlaties pieņemt citas rindas, uzvednē ir jānoklikšķina uz **Atcelt**.  

Tālāk esošajā tabulā ir parādīts, kā tiek mainīts PP statuss, kad pieņemat vai noraidāt kreditoru piedāvājumus.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Darbība**              | **Zemākais piedāvājuma statuss** | **Augstākais piedāvājuma statuss** | **Zemākais PP virsraksta statuss** | **Augstākais PP virsraksta statuss** | **Zemākais PP rindas statuss** | **Augstākais PP rindas statuss** |
| Pieņemiet vienu piedāvājumu. | Saņemts              | Pieņemts               | Saņemts                     | Pieņemts                      | Saņemts                   | Pieņemts                    |
| Noraidīt citus piedāvājumus.  | Atteikts              | Pieņemts               | Atteikts                     | Pieņemts                      | Atteikts                   | Pieņemts                    |






