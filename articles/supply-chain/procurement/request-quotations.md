---
title: Piedāvājuma pieprasījumu pārskats
description: Šajā tēmā ir sniegts apskats par piedāvājumu pieprasījumiem (request for quotation — RFQ). Organizācijas izsniedz piedāvājumu pieprasījumus, kad tām ir jāiegādājas preces vai pakalpojumi un tādēļ tās vēlas saņemt konkurētspējīgus piedāvājumus no vairākiem kreditoriem.
author: GalynaFedorova
ms.date: 10/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2154"
- intro-internal
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3de48c03ac73ee164dea0c329b2595db21c841cc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671959"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Piedāvājuma pieprasījumu pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts apskats par piedāvājumu pieprasījumiem (request for quotation — RFQ). Organizācijas izsniedz piedāvājumu pieprasījumus, kad tām ir jāiegādājas preces vai pakalpojumi un tādēļ tās vēlas saņemt konkurētspējīgus piedāvājumus no vairākiem kreditoriem. Piedāvājuma pieprasījumā kreditoriem tiek lūgts piedāvāt norādītā krājuma daudzuma cenas un piegādes laiku.
Kreditoriem var lūgt arī norādīt, vai pastāv jebkādas nejaušās izmaksas, piemēram, piegādes izmaksas, kā arī vai pastāv jebkādas atlaides lielu pasūtījumu vai savlaicīgas kreditora rēķina apmaksas gadījumā.

Piedāvājumu pieprasījumu procedūra sastāv no tālāk uzskaitītajiem uzdevumiem.

1. Izveidot piedāvājuma pieprasījumu un izsūtīt to vienam vai vairākiem kreditoriem.
1. Saņemt un reģistrēt piedāvājumus (piedāvājuma pieprasījuma atbildes).
1. Pārsūtīt jūsu pieņemtos piedāvājumus uz pirkšanas pasūtījumu, pirkšanas līgumu vai pirkšanas pieprasījumu.

Nākamajā attēlā ir parādīts apskats par piedāvājuma pieprasījuma procesu.

[![RFQ procesi.](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Piedāvājuma pieprasījumu gadījumu varat izveidot no plānotiem pasūtījumiem, no pirkšanas pieprasījuma vai ar manuālu ievadīšanu. PP gadījums ir pamatdokuments, ko jūs izmantojat, lai izsniegtu PP katram kreditoram.

Pēc piedāvājuma pieprasījuma sagatavošanas un kreditoru pievienošanas atlasiet **Sūtīt** (publiskajā sektorā tas ir **Sūtīt un publicēt** ) šim piedāvājuma pieprasījuma gadījumam. Tiek ģenerēts piedāvājuma pieprasījuma žurnāls katram kreditoram, kuram nosūtījāt šo piedāvājuma pieprasījumu. Sūtīšanas darbības drukāšanas opcijas varat konfigurēt tā, lai katra kreditora pārskats tiktu drukāts uz arhīvu vai lai pārskats tiktu sūtīts uz katra kreditora e-pasta adresi. Turklāt katra kreditora piedāvājuma pieprasījuma žurnālu varat izmantot, lai ģenerētu pārskatu, ko vēlāk varat nosūtīt vai atkārtoti nosūtīt šim kreditoram. Var arī konfigurēt sūtīšanas darbību tā, lai tā ģenerētu atbildes lapu, ko kreditors var aizpildīt.

Šajā tēmā ir apskatīta procedūra piedāvājumu pieprasījumu apstrādāšanai, kad netiek izmantota kreditora sadarbība. Ja sistēma ir iestatīta kreditoru sadarbībai, kreditori var tieša veidā ievadīt piedāvājumus programmatūrā Supply Chain Management. Papildinformāciju skatiet rakstā [Kreditoru sadarbība ar debitoriem](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) un [Kreditoru sadarbība ar ārējiem kreditoriem](vendor-collaboration-work-external-vendors.md).

Ja jums jāveic PP grozījumus pēc nosūtīšanas, ir iespējams PP atkārtoti nosūtīt kreditoriem, kad pabeigsiet, izmantojot divas grozījuma darbības: izveidot un finalizēt.

Kad piedāvājumus saņemat pa e-pastu, šos piedāvājumus varat apstrādāt no lapas **Piedāvājumu pieprasījumi**.

Ja no kāda kreditora ir nepieciešama vēl viena iterācija, atlasiet **Atgriezt** lapā **Piedāvājuma pieprasījums**. Izpildot atgriešanas darbību, tiek ģenerēts jauns žurnāls un pārskats, kas tiks drukāts, arhivēts un nosūtīts atbilstoši drukāšanas iestatījumiem.

Ja savam piedāvājuma pieprasījuma gadījumam pievienojāt punktu skaitīšanas kritērijus, piedāvājuma pieprasījumā ir punktu skaitīšanas panelis, kur varat ievadīt punktu skaitu. Kopējie rādītāji ir redzami piedāvājuma pieprasījumā un laikā, kad salīdzināt atbildes lapā **Salīdzināt atbildes**. Lapā **Salīdzināt atbildes** varat salīdzināt arī citus atbilžu datus, piemēram, rindas cenu, piegādes datumu un kopējo cenu.

Kad esat izvēlējies kādu piedāvājumu vai noteiktu skaitu rindu kādā piedāvājumā, varat pieņemt visas vai dažas rindas un atteikt pārējās. Tiek ģenerēti pieņemšanas žurnāli un atteikšanas žurnāli, kā arī atbilstošie pārskati, un tie tiks drukāti, arhivēti un nosūtīti atbilstoši drukāšanas iestatījumiem. Kad pieņemat kādu piedāvājumu vai noteiktas piedāvājuma rindas, tiek ģenerēts pirkšanas līgums vai pirkšanas pasūtījums vai tiek atjaunināts pirkšanas pieprasījums atkarībā no piedāvājuma pieprasījums pirkšanas veida. Varat izveidot tirdzniecības līgumu turpmākai izmantošanai jebkurai atbildei neatkarīgi no tā, vai esat to pieņēmis vai atteicis.

Piedāvājuma pieprasījuma gadījumam ir divi statusi: zemākais un augstākais, un šo statusu varat apskatīt saraksta lapā vienumam **Visi piedāvājumu pieprasījumi**. Zemākais statuss ir jebkuras piedāvājumu pieprasījuma gadījuma rindas vismazāk advancētais stāvoklis, un augstākais statuss ir jebkuras piedāvājumu pieprasījuma gadījuma rindas advancētais stāvoklis. Piemēram, pieņemsim, ka piedāvājuma pieprasījuma gadījums ar trīs rindām tiek nosūtīts diviem kreditoriem, tātad pastāv divi piedāvājumu pieprasījumi un katrā ir trīs rindas. Visas rindas ir **Nosūtīts**. Tagad piedāvājums tiek ievadīts no viena kreditora, un piedāvājuma pieprasījuma rindas iegūst statusu **Saņemts**. Tas nozīmē, ka no piedāvājuma pieprasījuma gadījuma trīs rindām visām šīm rindām ir statuss **Nosūtīts** attiecībā uz vienu piedāvājuma pieprasījumu un ir statuss **Saņemts** attiecībā uz otru piedāvājuma pieprasījumu. Viszemākais statuss tādā situācijā ir **Nosūtīts**, un visaugstākais statuss ir **Saņemts**.

Šie statusi ir detalizētāk aprakstīti tālāk šajā tēmā.

## <a name="setting-up-rfq-functionality"></a>PP funkcionalitātes iestatīšana

Lai varētu izveidot PP gadījumu, vispirms ir jāiestata PP informācija lapā **Sagādes un avotu parametri**. Izveidojot PP gadījumu, varat norādīt noklusējuma vērtības, kas tiek kopētas uz PP. Varat norādīt tālāk uzskaitītās vērtības.

- Jaunu PP pirkšanas tips: **Pirkšanas pasūtījums** vai **Pirkšanas līgums**
- Beigu datuma un laika nobīde no PP gadījuma izveidošanas dienas.
- Lūguma veids, kas PP gadījumam var norādīt noklusējuma vērtības specifiskai punktu skaitīšanas metodei.
- Piegādes informācija un maksājumu nosacījumi.

Varat mainīt šīs vērtības noteiktam PP gadījumam.

Ir jākonfigurē arī grozījumu process. Šīs konfigurēšanas ietvaros varat ieslēgt lauku bloķēšanu. Ja ir ieslēgta lauku bloķēšana, sagādes speciālistam, kas vēlas veikt piedāvājuma pieprasījuma grozījumus, šim piedāvājuma pieprasījuma gadījumam vispirms ir jāatlasa **Izveidot** cilnes **Piedāvājums** sadaļā **Grozījums**. Kad piedāvājuma pieprasījuma gadījums ir atjaunināts ar grozījumu, sagādes speciālistam ir jāpabeidz šis process, atlasot **Finalizēt**. Darbība Finalizēt ģenerē e-pasta ziņojumu, kas kreditorus informē par grozīto piedāvājuma pieprasījumu.

Lapā **Sagādes un avotu parametri** varat atlasīt veidni, ko izmantot kreditoriem sūtītajos e-pasta paziņojumos. Kad ir izveidota veidne sadaļā **E-pasta veidnes**, tajā var būt tālāk norādītie aizstāšanas marķieri.

- %Piedāvājuma pieprasījuma gadījums%
- %Piedāvājuma atgriešanas iemesls%
- %Grozījuma iemesls%
- %Grozījumu sagatavoja%
- %Company%
- %Piedāvājuma pieprasījuma gadījuma nosaukums%
- %Derīguma datums un laiks%
- %Date%

Marķieri %Piedāvājuma atgriešanas iemesls% un %Grozījuma iemesls% tiek aizstāti ar tekstu, ko sagādes speciālists var ievadīt, pabeidzot grozījumu vednī **Grozījums**. Marķieru %Grozījumu sagatavoja% un %Company% vērtības tiek automātiski iegūtas no RFQ. Marķieris %Date% tiek aizstāts ar pašreizējo datumu.

Ja kādu piedāvājuma pieprasījumu vēlaties atcelt pēc tam, kad tas ir nosūtīts, to var izdarīt no piedāvājuma pieprasījuma gadījuma. Lai atceltu, ir nepieciešama e-pasta veidne, lai nosūtītu kreditoru kontaktpersonām paziņojumu par atcelšanu. Veidnei ir jābūt atlasītai lapā **Sagādes un avotu parametri**. Kad tiek izveidota veidne, tajā var būt tālāk norādītie aizstāšanas marķieri.

- %Atcelšanas iemesls%
- %Piedāvājuma pieprasījuma gadījums%
- %Piedāvājuma pieprasījumu atcēla%
- %Company%
- %Piedāvājuma pieprasījuma gadījuma nosaukums%
- %Date%

Marķieris %Atcelšanas iemesls% tiek aizstāts ar tekstu, ko sagādes speciālists var ievadīt vednī **Atcelšana**. Marķieris %Date% tiek aizstāts ar pašreizējo datumu.

Ja piedāvājumā vēlaties izmantot iemeslu kodus, lai norādītu, kāpēc tas tika atteikts vai pieņemts, jums ir jāiestata iemeslu kodi lapā **Kreditoru iemesli**.

Sagādes un avotu lapā **Formas iestatīšana** varat konfigurēt savu drukāto vai saglabāto piedāvājumu pieprasījumu dokumentu izskatu.

> [!NOTE]
> Publiskā sektora konfigurācijai jau nosūtīta piedāvājuma pieprasījuma mainīšanai ir jāizmanto grozījumu process. Kad piedāvājuma pieprasījums ir nosūtīts, lauki tiek bloķēti.
Tādēļ, lai veiktu piedāvājuma pieprasījuma izmaiņas, ir jāatlasa **Izveidot**, uzsākot grozījumu procesu, kā aprakstīts iepriekš. Bloķēšanas uzvedību kontrolē lapas **Sagādes un avotu parametri** opcija **Bloķēt piedāvājuma pieprasījumu pēc tā nosūtīšanas**. Pēc noklusējuma šis parametrs ir iestatīts uz **Jā**, un publiskā sektora konfigurācijai šo noklusējuma iestatījumu nevar mainīt. Tādēļ, lai gan konfigurācijā, kas nav publiskā sektora konfigurācija, grozījumu procesu var apstrādāt manuāli, publiskā sektora konfigurācijā tas ir jāizmanto obligāti.

Kad izveidojat piedāvājuma pieprasījuma gadījumu ar tipu “Pirkšanas pasūtījums” un šim piedāvājuma pieprasījumam pievienojat kādu krājumu vienību, tiek ģenerēta krājumu transakcija, kuras ieejas plūsmas statuss ir **Piedāvājuma saņemšana**. Kad izmantojat vispārējo plānu piegāžu aprēķināšanai, tiek ņemtas vērā tikai piedāvājuma pieprasījuma rindas ar šo statusu. Ja vēlaties, lai piedāvājuma pieprasījuma gadījuma rindas tiktu ietvertas vispārējā plānā kā paredzētās ieejas plūsmas, šī uzvedība ir jākonfigurē vispārējās plānošanas iestatījumos.

Pirkšanas pārvaldnieks vai aģents var izveidot un uzturēt lūgumu veidus, kas atbilst organizācijas sagādes prasībām. Katru lūguma veidu var saistīt ar kādu punktu skaitīšanas metodi. Punktu skaitīšanas metodes satur kritērijus, ko var izmantot cenu piedāvājumu novērtēšanai. Lūgumu veidi, punktu skaitīšanas metodes un punktu skaitīšanas kritēriji ir jāiestata lapās **Lūguma veids** un **Punktu skaitīšanas metode**.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Izvēlēties noklusējuma laukus, ko iekļaut kreditoru PP atbildes formās

Varat norādīt specifiskus informācijas tipus, ko vēlaties saņemt no kreditoriem, kad tie atbild uz piedāvājuma pieprasījumu (PP). Lauki, ko atzīmējat kā noklusējuma, tiek ietverti tiešsaistes veidlapā, kas paredzēta kreditoru sadarbībai. Lai veiktu šīs izmaiņas iestatījumos:

1. Ja vēl neesat to izdarījis, izmantojiet [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu , lai iespējotu līdzekli *Atlasiet kreditoru PP atbildes formās iekļaujamos PP laukus*.
1. Dodieties uz **Sagāde un avoti > Iestatījumi > Sagādes un avotu parametri**.
1. Atvērt cilni **Piedāvājuma pieprasījums**.
1. Atlasiet atbildes lauku saiti **Noklusējuma piedāvājuma pieprasījumi** zem virsraksta **Iestatiet noklusējuma vērtības piedāvājuma pieprasījumiem**.
1. Atveras dialoglodziņš **Noklusējuma piedāvājuma pieprasījumu atbildes lauki**.
1. Sadaļa **Kreditoru PP atbildes formās ietvertie PP lauki** ietver slīdni katram laukam, kas pieejams izmantošanai PP atbildes formās. Lauki, kas šajā sadaļā iestatīti uz *Jā* tiks iekļauti (kopā ar to vērtībām) PP atbildes formās. Iestatiet slīdni uz *Nē* katram laukam, kurā vēlaties neļaut kreditoriem apskatīt datus, pārbaudot piedāvājumus. Tas ļauj ievadīt prognozētās vai paredzētās vērtības PP ievades laikā iekšējiem nolūkiem, kreditoriem neredzot ievadīto informāciju.

Šos iestatījumus pēc nepieciešamības var pārlabot atsevišķiem PP gadījumiem.

## <a name="creating-and-sending-an-rfq"></a>PP izveidošana un nosūtīšana

Jūs izveidojat piedāvājuma pieprasījuma gadījumu, atlasāt kreditorus, no kuriem vēlaties saņemt piedāvājumus par šo piedāvājuma pieprasījuma gadījumu, un pēc tam nosūtāt piedāvājuma pieprasījumus šiem kreditoriem. Varat izmantot drukāšanas iestatījumus, lai piedāvājuma pieprasījuma pārskatu un atbildes lapas pārskatus maršrutētu uz vēlamo galamērķi.

Varat manuāli izveidot piedāvājuma pieprasījuma gadījumu ar pirkšanas tipu **Pirkšanas pasūtījums** vai pirkšanas tipu **Pirkšanas līgums**.

Ja piedāvājuma pieprasījuma gadījuma tips ir **Pirkšanas pasūtījums**, tam ir tālāk norādītā uzvedība, kas atšķiras no citiem piedāvājuma pieprasījuma gadījumu tipiem.

- Kad tiek izveidotas piedāvājuma pieprasījuma gadījuma rindas, tiek ģenerētas krājumu transakcijas, kuru ieejas plūsmas statuss ir **Piedāvājuma saņemšana**.
- Pieņemot piedāvājumu, tiek ģenerēts pirkšanas pasūtījums.

Ja piedāvājuma pieprasījuma gadījuma tips ir **Pirkšanas līgums**, tam ir tālāk norādītā uzvedība, kas atšķiras no citiem piedāvājuma pieprasījuma gadījumiem.

- Piedāvājuma pieprasījuma gadījums tiek izmantots līgumam par noteikta preces daudzuma vai vērtības iegādi laika gaitā. Jums ir jāatlasa datumu diapazons, kas attiecas uz pirkšanas līgumu, un tās personas vārdu, kura pārvalda pirkšanas līgumu.
- Pieņemot piedāvājumu, tiek ģenerēts pirkšanas līgums.

Ja piedāvājuma pieprasījuma gadījums tiek ģenerēts no pirkšanas pieprasījuma, tiek automātiski piešķirts tips **Pirkšanas pieprasījums**. Jūs nevarat manuāli izveidot piedāvājuma pieprasījuma gadījumu ar tipu **Pirkšanas pieprasījums**.

Piedāvājuma pieprasījuma gadījumu no pirkšanas pieprasījuma varat izveidot tikai tad, ja pirkšanas pieprasījuma statuss ir **Tiek pārskatīts** un jūs esat norīkots nākamā darbplūsmas uzdevuma veikšanai. Pirkšanas pieprasījuma rindas tiek automātiski atjauninātas, kad pieņemat no kreditoriem saņemto piedāvājumu (piedāvājumu pieprasījumu atbilžu) rindas. Pirkšanas pieprasījumus varat pabeigt, atteikt, apstiprināt, kā arī citas darbības ar pirkšanas pieprasījumiem varat veikt tikai pēc tam, kad pieprasījuma rinda ir atjaunināta ar pieņemto piedāvājuma pieprasījuma rindu vai kad piedāvājuma pieprasījuma gadījums ir atcelts.

Kad izveidojat piedāvājuma pieprasījuma gadījumu, varat atlasīt lūguma tipu. Lūguma tips nosaka punktu skaitīšanas kritēriju kopu, kas piedāvājuma pieprasījuma gadījumam tiek izmantota piedāvājuma pieprasījuma atbilžu novērtēšanai.

Varat pievienot anketu PP gadījumam. Pēc tam šī anketa ir redzama visās piedāvājuma pieprasījuma atbildēs, kad esat nosūtījis piedāvājuma pieprasījumu. Anketas aizpildīšana ir obligāts uzdevums, un piedāvājumu var iesniegt tikai pēc tam.

Lai gan tiek nodrošināti noklusējumi, jūs varat pēc nepieciešamības mainīt sadaļas **Kreditoru PP atbildes formās ietvertie PP lauki** iestatījumus katram atsevišķam PP gadījumam. Lai to izdarītu, izveidojiet vai atveriet PP gadījumu. Pēc tam darbības rūtī atveriet cilni **Piedāvājums** un tad sadaļā **Atbildes** atlasiet **Iestatīt PP atbildes noklusējumus**. Tiek atvērts dialoglodziņš **Noklusējuma piedāvājuma pieprasījumu atbildes lauki**, kas darbojas tāpat, kā iestatot kreditoru PP atbildes formas, vienīgi jūsu šeit veiktās izmaiņas ietekmēs tikai pašreizējo PP gadījumu. Lai iegūtu sīkāku informāciju par to, kā iespējot šo funkcionalitāti un kā tā darbojas, skatiet [Izvēlēties noklusējuma laukus, ko iekļaut kreditoru PP atbildes formās](#default-reply-fields).

PP gadījumam pievienojamos kreditorus var atlasīt trīs veidos.

- Pievienojiet kreditorus pa vienam.
- Meklējiet visus kreditorus, kas atbilst noteiktiem kritērijiem.
- Automātiski pievienojiet visus kreditorus, kas ir apstiprināti piedāvājuma pieprasījuma gadījuma rindās izmantotajām sagādes kategorijām.

Kad piedāvājuma pieprasījuma gadījums ir gatavs, atlasiet **Sūtīt**. Ar sūtīšanas darbību tiek ģenerēti žurnāli un pārskati, kas tiks drukāti, arhivēti un nosūtīti atbilstoši drukāšanas iestatījumiem.

Ja lapā **Piedāvājuma pieprasījuma sūtīšana** opcijas **Cenu pārrēķinā izmantot kreditoru datus** un **Izmantot informāciju par krājumiem pēc kreditora** iestatāt uz **Jā**, kad piedāvājuma pieprasījumu sūtāt kādam kreditoram, attiecīgajam kreditoram paredzētajā piedāvājumā tiek automātiski ievadīta noteikta informācija par kreditoru.

## <a name="amending-an-rfq-case"></a>Piedāvājuma pieprasījuma gadījuma grozījumu veikšana

Reizēm pēc piedāvājuma pieprasījuma gadījuma nosūtīšanas ir nepieciešams to mainīt. Piedāvājuma pieprasījums gadījums varētu būt jāmaina, piemēram, ja ir mainīti piegādes datumi vai ja vēlaties saņemt papildu preces vai citu preču daudzumu. Varat konfigurēt grozījumu procesu, uzstādot stingrākus vai mazāk stingrus ierobežojumus.

Ja grozījuma procesu konfigurējat, uzstādot stingrākus ierobežojumus, lai modificētu laukus jau nosūtītā piedāvājuma pieprasījuma gadījumā, šajā piedāvājuma pieprasījuma gadījumā ir jāatlasa **Izveidot**, uzsākot grozījumus. Kad izmaiņu veikšana ir pabeigta, jums ir jāatlasa **Finalizēt**. Pēc tam jūs saņemat norādījumus par informācijas pievienošanu e-pasta ziņojumam, kas tiek nosūtīts, lai informētu kreditorus par grozījumiem. Atjauninātais piedāvājuma pieprasījuma pārskats, kurā ir piezīme par grozījumiem, tiek automātiski pievienots e-pasta ziņojumam.

Ja grozījuma procesu konfigurējat, uzstādot mazāk stingrus ierobežojumus, nav nepieciešamības atlasīt **Izveidot**, lai varētu mainīt laukus jau nosūtītā piedāvājuma pieprasījuma gadījumā. Taču piedāvājuma pieprasījumam ir manuāli jāpievieno piezīme par grozījumu, un šis gadījums ir jānosūta vēlreiz. Ņemiet vērā, ka šo pieeju var lietot tikai tad, ja neviena no atbildēm (piedāvājumiem) nav rediģēta. Ja esat ievadījis kādu atbildi un tās statuss ir **Saņemts**, poga **Sūtīt** nav pieejama. Tādā gadījumā jums ir jāatlasa **Izveidot** un pēc tam — **Finalizēt**, tāpat kā procesos ar stingrākiem ierobežojumiem. Pēc tam atbilde tiek atiestatīta, lai atspoguļotu piedāvājuma pieprasījumā veiktās izmaiņas.

Ja piedāvājumu ievadīšanai kreditori izmanto kreditoru sadarbības interfeisu, jums vienmēr ir jāizmanto grozījumu process, lai informētu kreditorus par piedāvājuma pieprasījuma gadījuma veiktajām izmaiņām. Šī procedūra palīdz novērst situācijas, kad kreditori izsaka piedāvājumu par novecojušu piedāvājuma pieprasījuma gadījumu, kamēr viņu piedāvājums tiek apstrādāts. Papildinformāciju par kreditoru sadarbību skatiet šeit: [Kreditoru sadarbība ar ārējiem kreditoriem](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Ja saistībā ar piedāvājuma izteikšanu vēlaties uzaicināt papildu kreditorus un ja piedāvājuma pieprasījuma gadījumam nav veiktas nekādas izmaiņas, varat izmantot pogu **Sūtīt**. Jūsu pievienotie kreditori būs redzami lapā **Sūtīt** un saņems e-pasta uzaicinājumu.

## <a name="receiving-and-registering-rfq-replies"></a>PP atbilžu saņemšana un reģistrēšana

Nosūtot PP, tiek automātiski ģenerēta atbildes lapa. Kad saņemat piedāvājumus PP, jums tos jāievada caur lapu **Piedāvājuma pieprasījums**, noklikšķinot uz darbības **Rediģēt PP atbildi.** Tas jums ļaus piedāvājuma informāciju ievadīt atvēlētā piedāvājuma formā. Sākotnēji vienuma **Atbildes norise** vērtība ir **Nav sākts**. Kad noklikšķināt uz **Rediģēt piedāvājuma pieprasījuma atbildi**, norises statuss ir **Pircējs atjaunina**, līdz piedāvājums tiek iesniegts. Kad esat ievadījis piedāvājuma informāciju, noklikšķiniet uz **Iesniegt**. Atbildes norises statuss tiek mainīts uz **Iesniedza pircējs**. Līdzīgi, kad ir iespējota kreditoru sadarbība, vienums **Atbildes norise** tiek atjauninātas, kreditoram mijiedarbojoties ar šo piedāvājumu. Pēc tam statuss no **Kreditors atjaunina** mainās uz **Iesniedza kreditors**. Kad piedāvājums ir iesniegts, žurnāls tiek izveidots kā **Saņemts**. Atbilde (piedāvājums) ir jāiesniedz, lai to varētu reģistrēt kā saņemtu, un tikai pēc tam to var tālāk apstrādāt kā pieņemtu vai atteiktu.

Ja ir nepieciešams piedāvājumu atjaunināt, jums ir jāizpilda šī pati iepriekš aprakstītā procedūra un jāiesniedz vēlreiz.

Ņemiet vērā, ka formas **Piedāvājuma pieprasījums** rediģēšana ir atļauta tikai attiecībā uz informāciju, kas ir saistīta ar piedāvājuma apstrādāšanu, nevis piedāvājuma ievadīšanu. Lai piedāvājumu ievadītu vai modificētu, noklikšķiniet uz **Rediģēt piedāvājuma pieprasījuma atbildi**.

Kad ievadāt piedāvājuma informāciju un gadījumā, ja piedāvājuma pieprasījuma gadījums ļauj izmantot alternatīvas rindas, varat pievienot alternatīvas rindas tādām rindām, kam ir tikai sagādes kategorija, bet nav norādīts kataloga krājums. Noklikšķiniet uz **Pievienot alternatīvu**, lai pievienotu alternatīvas rindas.

Ja esat ievadījis atbildi, bet ir nepieciešams jauns piedāvājums no kreditora, piedāvājuma pieprasījumu varat atgriezt. Tiek ģenerēts jauns žurnāls un pārskats, ko varat nosūtīt kreditoram.

Lapā **Piedāvājuma pieprasījuma sekojums** varat skatīt apskatu par visiem piedāvājuma pieprasījumiem un to statusiem: **Nosūtīts, Saņemts, Pieņemts, Atteikts, Atcelts, Noraidīts**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Piedāvājumu pieņemšana un noraidīšana un pieņemto piedāvājumu pārsūtīšana uz lejupstraumes dokumentiem

Kad esat noteicis labāko piedāvājumu, piemēram, piedāvājumu ar izdevīgāko kopējo cenu, jūs pieņemat šo piedāvājumu. Varat pieņemt dažas piedāvājuma rindas un noraidīt citas.
Varat arī pieņemt dažādu kreditoru piedāvājumu rindas. Ņemiet vērā, ka, pieņemot dažas rindas, tiek piedāvāts noraidīt visas pārējās rindas. Tādēļ, ja vēlaties pieņemt citas rindas, uzvednē ir jāatlasa **Atcelt**. Piedāvājuma pieprasījuma atbildes statuss katram kreditoram, no kura jūs pieņemat piedāvājumus vai to rindas, tiek atjaunināts uz **Pieņemts**.

Ja pirkšanas pasūtījuma vai pirkšanas līguma sagatavošanas laikā jums ir nepieciešams piedāvājuma pieprasījumam pievienot kādu papildu rindu, to var izdarīt, noklikšķinot uz **Pievienot rindu** lapas **Piedāvājuma pieprasījums** rindu režģī. Šo rindu varat skatīt un rediģēt tikai lapā **Piedāvājuma pieprasījums**. Pēc pieņemšanas tā ir redzama piedāvājuma lapā.

Kad pieņemat kādu piedāvājumu vai vienu vai vairākas piedāvājuma rindas, automātiski tiek ģenerēts pirkšanas pasūtījums vai pirkšanas līgums. Pēc tam varat noraidīt piedāvājumus no visiem pārējiem kreditoriem.

Atbildē varat pievienot iemesla kodu, lai paskaidrotu, kāpēc pieņēmāt vai noraidījāt piedāvājumu.

Kad pieņemat piedāvājumu ar tipu **Pirkšanas pieprasījums**, pirkšanas pieprasījuma rindas tiek atjauninātas ar tālāk norādīto informāciju, kas atspoguļo pieņemtā piedāvājuma informāciju.

- Vienības cena
- Atlaides procenti
- Atlaides summa
- Pirkšanas izmaksas
- Rindu maksas
- Kreditors
- Ārējais numurs
- Ārējais apraksts

Tālāk esošajā tabulā ir parādīts, kā tiek mainīts PP statuss, kad pieņemat vai noraidāt kreditoru piedāvājumus.

## <a name="statuses--highest-and-lowest"></a>Statusi — augstākais un zemākais

Piedāvājuma pieprasījuma gadījuma cilnē Kreditors varat redzēt rindas ar visaugstāko un viszemāko statusu attiecībā uz konkrētu kreditoru. Kad kreditors ir pievienots un neviena rinda vēl nav nosūtīta, gan viszemākais, gan visaugstākais statuss tiek <strong>Izveidots.</strong> Kad PP tiek nosūtīts kreditoram ar visām rindām, abu rindu statuss tiks <strong>Nosūtīts</strong>. Ja dažas rindas piedāvājumā no kreditora tiek pieņemtas, bet citas tiek atteiktas, atteiktās rindas saņem viszemāko statusu, kas ir <strong>Atteikts</strong>, un pieņemtās rindas saņem visaugstāko statusu, kas ir <strong>Pieņemts</strong>.

Piedāvājuma pieprasījuma gadījuma rindās varat redzēt visaugstāko un viszemāko statusu katrai rindai visos kreditoros. Ja kādu rindu esat nosūtījis visiem kreditoriem attiecīgajā piedāvājuma pieprasījuma gadījumā, bet neviens vēl nav atbildējis, tad viszemākais un visaugstākais statuss ir **Nosūtīts**. Kad ir atbildējis vismaz viens kreditors, visaugstākais statuss mainās uz **Saņemts**. Ja gadījumam pievienojat jaunu kreditoru, viszemākais statuss mainās uz **Izveidots**

Visaugstākais un viszemākais statuss piedāvājuma pieprasījuma gadījumā ir apkopojums no statusa \<cilnē Kreditors un cilnē Rindas.

Šie statusi tiek vērtēti šādā secībā no viszemākā uz visaugstāko: Izveidots, Nosūtīts, Saņemts, Atteikts, Pieņemts, Noraidīts, Atcelts.

Nākamajā tabulā ir parādīts, kā mainās piedāvājuma pieprasījuma gadījuma statuss, kad izveidojat piedāvājuma pieprasījuma gadījumu ar rindām un pēc tam to nosūtāt kreditoriem.

| **Darbība**                                | **Zemākais piedāvājuma pieprasījuma gadījuma statuss** | **Augstākais piedāvājuma pieprasījuma gadījuma statuss** | **Zemākais piedāvājuma pieprasījuma gadījuma rindas statuss** | **Augstākais piedāvājuma pieprasījuma gadījuma rindas statuss** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Izveidojiet piedāvājuma pieprasījuma gadījuma virsrakstu un rindu.      | Izveidots                    | Izveidots                     | Izveidots                         | Izveidots                          |
| Nosūtiet piedāvājuma pieprasījumus visiem kreditoriem attiecīgajā piedāvājuma pieprasījuma gadījumā. | Nosūtīts                       | Nosūtīts                        | Nosūtīts                            | Nosūtīts                             |
| Pievienojiet citu kreditoru.                       | Izveidots                    | Nosūtīts                        | Izveidots                         | Nosūtīts                             |
| Nosūtiet piedāvājuma pieprasījumu otram kreditoram.        | Nosūtīts                       | Nosūtīts                        | Nosūtīts                            | Nosūtīts                             |

Visām rindām piedāvājuma pieprasījumos, kas ir saistīti ar šo piedāvājuma pieprasījuma gadījumu, ir statuss **Nosūtīts**.

Nākamajā tabulā ir redzams, kā tiek mainīts piedāvājuma pieprasījuma statuss, kad saņemat piedāvājumus un reģistrējat informāciju piedāvājuma pieprasījuma atbildes lapā.

| **Darbība**                                               | **Zemākais statuss visu piedāvājuma pieprasījumu visās rindās** | **Augstākais statuss visu piedāvājuma pieprasījumu visās rindās** | **Zemākais piedāvājuma pieprasījuma gadījuma virsraksta statuss** | **Augstākais piedāvājuma pieprasījuma gadījuma virsraksta statuss** | **Zemākais piedāvājuma pieprasījuma gadījuma rindas statuss** | **Augstākais piedāvājuma pieprasījuma gadījuma rindas statuss** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Reģistrējiet viena kreditora piedāvājumu kādam piedāvājuma pieprasījumam un saglabājiet to.        | Nosūtīts                                           | Saņemts                                        | Nosūtīts                              | Saņemts                           | Nosūtīts                            | Saņemts                         |
| Reģistrējiet otrā kreditora piedāvājumu kādam piedāvājuma pieprasījumam un saglabājiet to. | Saņemts                                       | Saņemts                                        | Saņemts                          | Saņemts                           | Saņemts                        | Saņemts                         |


Nākamajā piemērā varat redzēt visaugstāko un viszemāko statusu piedāvājuma pieprasījuma gadījumam, kur viens piedāvājums ir saņemts un otrs piedāvājums ir pieņemts. Kad kāds saņemts piedāvājums tiek atteikts, piedāvājuma pieprasījuma gadījuma virsrakstā un rindā viszemākais statuss no Saņemts mainās uz Atteikts.


|            <strong>Darbība</strong>             | <strong>Zemākais statuss visu piedāvājuma pieprasījumu visās rindās</strong> | <strong>Augstākais statuss visu piedāvājuma pieprasījumu visās rindās</strong> | <strong>Zemākais piedāvājuma pieprasījuma gadījuma virsraksta statuss</strong> | <strong>Augstākais piedāvājuma pieprasījuma gadījuma virsraksta statuss</strong> | <strong>Zemākais piedāvājuma pieprasījuma gadījuma rindas statuss</strong> | <strong>Augstākais piedāvājuma pieprasījuma gadījuma rindas statuss</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Pieņemiet vienu piedāvājumu. (vai vismaz vienu rindu) |                          Saņemts                           |                           Pieņemts                           |                    Saņemts                    |                    Pieņemts                     |                   Saņemts                   |                   Pieņemts                    |
|           Atsakiet visus pārējos piedāvājumus.           |                          Atteikts                           |                           Pieņemts                           |                    Atteikts                    |                    Pieņemts                     |                   Atteikts                   |                   Pieņemts                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]