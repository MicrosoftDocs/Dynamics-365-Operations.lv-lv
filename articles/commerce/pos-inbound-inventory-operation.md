---
title: Ienākošo krājumu operācija punktā POS
description: Šajā tēmā ir aprakstītas pārdošanas punkta (POS) ienākošo krājumu operāciju iespējas.
author: hhaines
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: a14b98cab78896d3a6c2e567cadc1ff9a991a278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018958"
---
# <a name="inbound-inventory-operation-in-pos"></a>Ienākošo krājumu operācija punktā POS

[!include [banner](includes/banner.md)]

Programmas Microsoft Dynamics 365 Commerce versijā 10.0.10 un jaunākās versijā ienākošās un izejošās operācijas pārdošanas punktā (POS) aizvieto izdošanas un saņemšanas operāciju.

> [!NOTE]
> Commerce versijā 10.0.10 un jaunākās versijās visus jaunos līdzekļus POS lietojumprogrammā, kas ir saistīti ar veikala krājumu saņemšanu no pirkšanas pasūtījumiem un pārsūtīšanas pasūtījumiem, pievienos POS operācijai **Ienākošā operācija**. Ja jūs pašlaik izmantojat izdošanas un saņemšanas operāciju POS, mēs iesakām jums izstrādāt stratēģiju, lai pārietu no šīs operācijas uz jaunajām ienākošajām un izejošajām operācijām. Lai gan izdošanas un saņemšanas operācija netiks noņemta no preces, vairs netiks veiktas investīcijas no funkcionālās vai veiktspējas perspektīvas pēc versijas 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Priekšnosacījums: Konfigurējiet asinhrono dokumentu struktūru

Ienākošā operācija iekļauj veiktspējas uzlabojumus, lai nodrošinātu, ka lietotāji, kuriem ir augsts saņemšanas grāmatojumu apjoms daudzos veikalos vai uzņēmumos un kam ir daudz krājumu dokumentu, var apstrādāt šos dokumentus Commerce Headquarters, nepieredzot taimautus vai kļūmes. Šie uzlabojumi prasa asinhronas dokumentu struktūras izmantošanu.

Izmantojot asinhrono dokumenta struktūru, jūs varat veikt ienākošo dokumentu izmaiņas no POS uz Commerce Headquarters un pēc tam pāriet uz citiem uzdevumiem, kamēr notiek fonā notiek apstrāde uz Commerce Headquarters. Lai pārliecinātos, ka grāmatošana bijusi veiksmīga, varat pārbaudīt dokumenta statusu POS dokumentu saraksta lapā **Ienākošās operācijas**. POS programmā var arī izmantot ienākošo operāciju aktīvo dokumentu sarakstu, lai skatītu visus dokumentus, kurus nevarēja grāmatot Commerce Headquarters. Ja dokuments neizdodas, POS lietotāji var veikt labojumus un pēc tam vēlreiz mēģināt apstrādāt to programmā Commerce Headquarters.

> [!IMPORTANT]
> Pirms uzņēmums mēģina izmantot ienākošo operāciju POS, ir jābūt konfigurētai asinhronā dokumenta struktūrai.

Lai konfigurētu asinhronu dokumentu struktūru, veiciet šādas procedūras.

### <a name="create-and-configure-a-number-sequence"></a>Izveidojiet un konfigurējiet numuru sēriju

1. Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Numuru sērijas**.
2. Lapā **Numuru sērijas** izveidojiet numuru sēriju.
3. Laukā **Numuru sērijas kods** un **Nosaukums** ievadiet lietotāja definētās vērtības.
4. Kopsavilkuma cilnē **Atsauces** atlasiet **Pievienot**.
5. Laukā **Apgabals** atlasiet **Commerce parametri**.
4. Laukā **Atsauce** atlasiet **Retail dokumenta operācijas identifikators**.
5. Kopsavilkuma cilnē **Vispārīgi**, sadaļā **Iestatīšana** iestatiet opciju **Nepārtrauki** uz **Nē**, lai nodrošinātu, ka nav veiktspējas problēmu.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Izveidojiet un ieplānojiet divus pakešdarbus dokumentu apstrādes un pārraudzības uzdevumiem

> [!NOTE]
> Commerce versijā 10.0.13 un jaunākā šie pakešuzdevumi nav jākonfigurē, izmantojot pakešuzdevumu struktūru. Pakešu apstrādi var konfigurēt no izvēlnes **Retail and Commerce > Retail un Commerce IT**. Izmantojiet izvēlnes opcijas **Retail dokumentu operāciju pārraudzība** un **Retail dokumentu operāciju apstrāde** lai konfigurētu pakešuzdevumus.

Jūsu izveidotie pakešuzdevumi tiks izmantoti, lai apstrādātu dokumentus, kuriem ir radusies kļūme vai taimauts. Tie tiks izmantoti arī tad, kad aktīvo krājumu dokumentu skaits, kas tiek apstrādāti no POS, pārsniedz sistēmas konfigurēto vērtību.

1. Dodieties uz **Sistēmas administrēšana \> Vaicājumi \> Pakešuzdevumi**.
2. Lapā **Pakešuzdevums** izveidojiet divus pakešuzdevumus:

    - Konfigurējiet vienu darbu, lai tas palaistu klasi **RetailDocumentOperationMonitorBatch**.
    - Konfigurējiet citu darbu, lai tas palaistu klasi **RetailDocumentOperationProcessingBatch**.

2. Ieplānojiet jauno pakešuzdevumu periodisku palaišanu. Piemēram, iestatiet grafiku tā, lai darbi tiktu izpildīti ik pēc piecām minūtēm.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Priekšnoteikums: Pievienojiet ienākošo operāciju POS ekrāna izkārtojumam

Lai jūsu organizācija varētu izmantot ienākošo operāciju funkcionalitāti, tai ir jākonfigurē POS operācija **Ienākošā operācija** vienā vai vairākos [POS ekrāna izkārtojumos](/dynamics365/unified-operations/retail/pos-screen-layouts). Pirms jaunās operācijas izvietošanas ražošanas vidē, pārliecinieties, vai ka to rūpīgi pārbaudāt un apmācāt savus lietotājus tās lietošanā.

## <a name="overview"></a>Pārskats

Izejošā operācija ļauj POS lietotājiem veikt šādus uzdevumus:

- Saņemiet krājumus veikala krājumos vai nu no apstiprinātajiem pirkšanas pasūtījuma dokumentiem vai nosūtītajiem pārsūtīšanas pasūtījumu dokumentiem.
- Skatiet informāciju par vēsturiskajām krājumu ieejas plūsmām septiņu dienu laikā pēc dokumenta pilnīgas saņemšanas.
- Izveidojiet jaunus ienākošo pārsūtīšanas pasūtījumu pieprasījumus.

Kad no POS programmas tiek palaista ienākošā operācija, parādās saraksta lapas skats. Šis skats parāda atvērtos pirkšanas pasūtījuma dokumentus un pārsūtīšanas pasūtījuma dokumentus, kuros ir krājumu rindas, kuras ir ieplānots saņemt pašreizējam veikalam. Lai atrastu un atlasītu konkrētu dokumentu, lietotāji var ritināt sarakstu vai izmantot meklēšanas līdzekli.

Ienākošo krājumu dokumentu sarakstam ir trīs cilnes:

- **Aktīvs** – šajā cilnē redzami dokumenti, kas ir pilnīgi vai daļēji atvērti, un kuros ir rindas vai daudzumi rindās, kas joprojām ir jāsaņem.
- **Melnraksts** – Šī cilne parāda jaunos ienākošo pārsūtīšanas pasūtījumu pieprasījumus, kurus izveidoja lietotāja veikals. Tomēr dokumenti tika saglabāti tikai lokāli. Tie vēl nav iesniegti Commerce Headquarters apstrādei.
- **Pabeigts** – Šī cilne parāda pirkšanas pasūtījuma vai pārsūtīšanas pasūtījuma dokumentu sarakstu, ko veikals ir pilnībā saņēmis pēdējo septiņu dienu laikā. Šī cilne ir paredzēta tikai informatīviem nolūkiem. Visa informācija par dokumentiem šim veikalam ir tikai lasāmi dati.

Skatot dokumentus jebkurā cilnē, lauks **Statuss** var palīdzēt izprast stadiju, kurā dokuments atrodas.

- **Melnraksts** — Pārsūtīšanas pasūtījuma dokuments ir saglabāts tikai veikala kanāla datu bāzē. Informācija par pārsūtīšanas pasūtījuma pieprasījumu vēl nav iesniegta Commerce Headquarters.
- **Pieprasīts** – Pirkšanas pasūtījums vai pārsūtīšanas pasūtījums ir izveidots Commerce Headquarters un ir pilnībā atvērts. Šim dokumentam vēl nav apstrādātas kvītis. Pirkšanas pasūtījuma dokumenta tipa dokumentiem saņemšana var sākties jebkurā laikā, kamēr statuss ir **Pieprasīts**.
- **Daļēji nosūtīts** – Pārsūtīšanas pasūtījuma dokumentam ir viena vai vairākas rindas vai daļēji rindu daudzumi, kas iegrāmatoti kā nosūtīti no izejošās noliktavas. Šīs nosūtītās rindas ir pieejamas saņemšanai, izmantojot ienākošo operāciju.
- **Pilnībā nosūtīts** — Pārsūtīšanas pasūtījumam ir bijušas visas tās rindas un pilnie rindas daudzumi, kurus izejošā noliktava grāmatojusi kā nosūtītus. Viss dokuments ir pieejams saņemšanai, izmantojot ienākošo operāciju.
- **Daļēji saņemts** — veikalā tiek saņemtas dažas rindas vai rindu daudzumi pirkšanas pasūtījuma vai pārsūtīšanas pasūtījuma dokumentā, bet dažas rindas paliek atvērtas.
- **Pilnībā saņemts** – visas rindas un daudzumi pirkšanas pasūtījuma vai pārsūtīšanas pasūtījuma dokumentā ir pilnībā saņemtas. Dokumenti ir pieejami tikai cilnē **Pabeigt** un ir lasāmi tikai veikala lietotājiem.
- **Notiek** – Šis statuss tiek izmantots, lai informētu ierīces lietotājus, ka dokumentu aktīvi apstrādā cits lietotājs.
- **Apturēts** — Šis statuss tiek parādīts pēc tam, kad tiek atlasīts **Apturēt saņemšanu**, lai īslaicīgi apturētu saņemšanas procesu.
- **Apstrāde HQ** — Dokuments tika iesniegts Commerce Headquarters no POS programmas, taču tas vēl nav veiksmīgi iegrāmatots programmā Commerce Headquarters. Dokumentam tiek veikta asinhronās dokumenta grāmatošana. Pēc tam, kad dokuments ir sekmīgi iegrāmatots Commerce Headquarters, tā statuss ir jāatjaunina, lai tas būtu **Pilnībā saņemts** vai **Daļēji saņemts**.
- **Apstrāde neizdevās** – Dokuments tika iegrāmatots Commerce Headquarters un noraidīts. Rūts **Detalizēta informācija** rāda grāmatošanas kļūmes iemeslu. Dokuments ir jārediģē, lai izlabotu datu problēmas, un pēc tam tas atkārtoti jāiesniedz Commerce Headquarters apstrādei.

Kad sarakstā atlasāt dokumenta rindu, parādās rūts **Detalizēta informācija**. Šajā rūtī tiek rādīta papildu informācija par dokumentu, piemēram, informācija par nosūtīšanu un datumu. Progresa josla rāda, cik daudz vienumu vēl ir jāapstrādā. Ja dokuments nav veiksmīgi apstrādāts programmā Commerce Headquarters, rūts **Detalizēta informācija** rāda kļūmes ziņojumus, kas ir saistīti ar kļūmi.

Dokumentu saraksta lapas skatā varat izvēlēties **Pasūtījuma informāciju** programmas joslā, lai skatītu detalizētu informāciju par dokumentu. Varat arī aktivizēt saņemšanas apstrādi atbilstošajās dokumenta rindās.

Dokumentu saraksta lapas skatā varat izveidot arī jaunu izejošā pārsūtīšanas pasūtījuma pieprasījumu veikalam. Dokumenti saglabā statusu **Melnraksts**, un tos var mainīt vai dzēst, līdz tie tiek iesniegti Commerce Headquarters apstrādei. Pēc tam, kad tie ir iesniegti Commerce Headquarters, pārsūtīšanas pasūtījuma rindas vairs nevar mainīt no POS programmas.

## <a name="receiving-process"></a>Saņemšanas process

Pēc pārsūtīšanas pirkšanas pasūtījuma vai pasūtījuma dokumenta atlases cilnē **Aktīvs** varat atlasīt **Pasūtījuma informācija**, lai sāktu saņemšanas procesu.

Pēc noklusējuma tiek parādīts skats **Saņem tagad**. Šis skats ir optimizēts svītru koda skenēšanai. To var izmantot, lai izveidotu skenēto krājumu sarakstu, lai varētu saņemt šos krājumus. Lai sāktu saņemšanas procesu, varat sākt skenēt preču svītrkodus.

Kas krājumu svītrkodi tiek skenēti skatā **Saņem tagad**, programma validē krājumus atlasītajam pirkšanas vai pārsūtīšanas pasūtījuma dokumentam, lai nodrošinātu, ka katrs skenētais vienums atbilst derīgam krājumam dokumentā. Skatā **Saņem tagad**, tiek pieņemts, ka katrs svītrkoda skenējums tiek pieņemts attēlo vienas vienības daudzuma kvīti, ja vien šis daudzums nav iegults svītrkodā. Šajā skatā var atkārtoti skenēt svītrkodus, lai izveidotu sarakstu ar visiem kvīts krājumiem un daudzumiem.

### <a name="example-scenario"></a>Piemēra situācija

Lietotājs saņem pirkšanas pasūtījumu, kas satur 10 svītrkoda 5657900266 vienības. Lietotājs var skenēt šo svītrkodu 10 reizes, lai atjauninātu lauku **Saņem tagad** par vienu vienumu katrā skenēšanā. Kad lietotājs pabeidz skenējumus, krājuma rindas lauka **Saņem tagad** radīs, ka ir saņemts daudzums 10.

Vai arī scenārijā, kurā krājumu daudzums ir liels, lietotājs var izvēlēties manuāli ievadīt daudzumu, nevis skenēt svītrkodu katram saņemtajam krājumam. Šādā gadījumā lietotājs var skenēt svītrkodu vienu reizi, lai pievienotu krājumu sarakstam **Saņem tagad**. Lietotājs pēc tam var atlasīt saistīto rindu skatā **Saņem tagad** un pēc tam rūtī **Detalizēta informācija**, kas parādās lapas labajā pusē, atjaunināt krājuma lauku **Saņemšanas daudzums**.

Kaut arī skats **Saņem tagad** ir optimizēts svītrkodu skenēšanai, lietotāji var arī atlasīt **Saņemt preci** programmas joslā un pēc tam ievadīt krājuma ID vai svītrkoda datus, izmantojot dialoglodziņu. Kad ievadītais krājums ir pārbaudīts, lietotājam tiek piedāvāts ievadīt saņemšanas daudzumu.

Skats **Saņemt tagad** sniedz fokusētu veidu, kādā lietotāji var redzēt, kurus produktus viņi saņem. Var izmantot arī skatu **Pilns pasūtījumu saraksts**. Šis skats parāda visu dokumenta rindu sarakstu atlasītajam pirkšanas vai pārsūtīšanas pasūtījuma dokumentam. Lietotāji var manuāli atlasīt rindas sarakstā un pēc tam rūtī **Detalizēta informācija** atjaunināt atlasītās rindas lauku **Saņemšanas daudzums**. Skatā **Pilns pasūtījumu saraksts** lietotāji var skenēt svītrkodus, vai arī izmantot funkciju **Saņemt preci**, lai ievadītu krājuma ID vai svītrkodu, un datus par saņemto daudzumu, bez nepieciešamības vispirms sarakstā atlasīt atbilstīgo krājuma rindu.

### <a name="over-receiving-validations"></a>Validāciju pārlieka saņemšana

Validācijas notiek dokumenta rindu saņemšanas procesā. Tās ietver validācijas pasūtījuma apjoma pārsniegšanai. Ja lietotājs mēģina saņemt vairāk krājumu, nekā bija pasūtīts uz pirkšanas pasūtījumu, bet vai nu nav konfigurēta pasūtījuma apjoma pārsniegšana, vai saņemtais daudzums pārsniedz pirkšanas pasūtījuma rindai konfigurēto pasūtījuma apjoma pārsniegšanas toleranci, lietotājs saņem kļūdu, un lietotājam nav atļauts saņemt pārsniegto daudzumu.

Pārsūtīšanas pasūtījuma dokumentiem nav atļauta pārlieka saņemšana. Lietotāji vienmēr saņems kļūdas, ja mēģinās saņemt vairāk nekā tika nosūtīts pārsūtīšanas pasūtījuma rindai.

### <a name="close-purchase-order-lines"></a>Slēgt pirkšanas pasūtījuma rindas

Varat saņemšanas procesa laikā slēgt atlikušo daudzumu ienākošā pirkšanas pasūtījumā, ja kravas nosūtītājs ir apstiprinājis, ka nevar nosūtīt visu pieprasīto daudzumu. Lai izmantotu šo iespēju, uzņēmumam jābūt konfigurētam atļaut nepilnu pirkšanas pasūtījumu piegādi. Turklāt nepilnas piegādes tolerances procentiem jābūt definētiem pirkšanas pasūtījuma rindai.

Lai konfigurētu uzņēmumu atļaut nepilnu pirkšanas pasūtījumu piegādi, programmā Commerce headquarters dodieties uz **Sagāde un avoti** > **Iestatījumi** > **Sagādes un avotu parametri**. Cilnē **Piegāde** ieslēdziet parametru **Pieņemt nepilnu piegādi**. Tad palaidiet **1070** (**Kanāla konfigurācija**) sadales grafika darbu, lai sinhronizētu iestatījumu izmaiņas kanālos.

Nepilnas piegādes tolerances procentus pirkšanas pasūtījuma rindā precēm var definēt iepriekš, kā daļu no preces konfigurācijām Commerce headquarters. Vai arī tos var iestatīt vai pārrakstīt noteiktā pirkšanas pasūtījumā Commerce Headquarters.

Kad organizācija ir pabeigusi pirkšanas pasūtījumu nepilnas piegādes konfigurācijas, POS lietotāji redzēs jaunu opciju **Slēgt atlikušo daudzumu** rūtī **Informācija**, kad tiks atlasīta ienākoša pirkšanas pasūtījuma rinda operācijā **Ienākošie krājumi**. Ja lietotājs slēdz atlikušo daudzumu, POS veic validāciju, lai pārbaudītu, vai daudzums, kas tiek slēgts, atrodas pirkšanas pasūtījuma rindā definēto nepilnas piegādes tolerances procentu ietvaros. Ja nepilnās piegādes tolerance ir pārsniegta, tiek parādīts kļūdas ziņojums, un lietotājs nevarēs slēgt atlikušo daudzumu, līdz iepriekš saņemtais daudzums un **Saņemt tagad** daudzums atbilst vai pārsniedz minimālo daudzumu, kas jāsaņem, pamatojoties uz nepilnas piegādes tolerances procentiem. 

Ja pirkšanas pasūtījuma rindai ieslēgta opcija **Slēgt atlikušo daudzumu**, kad lietotājs pabeidz saņemšanu, izmantojot darbību **Beigt saņemšanu**, uz Commerce headquarters tiek nosūtīts slēgšanas pieprasījums un jebkurš nesaņemts daudzums no šī pasūtījuma rindas tiks atcelts. Šajā brīdī rinda tiek uzskatīta par pilnībā saņemtu. 

### <a name="receiving-location-controlled-items"></a>Atrašanās vietas kontrolētu krājumu saņemšana

Ja saņemtie krājumi tiek kontrolēti ar atrašanās vietu, lietotāji var atlasīt vietu, no kuras tie vēlas saņemt krājumus saņemšanas procesa laikā. Ieteicams konfigurēt noklusēto saņemšanas atrašanās vietu veikala noliktavai, lai padarītu šo procesu efektīvāku. Pat ja noklusējuma atrašanās vieta ir konfigurēta, lietotāji var pēc vajadzības ignorēt saņemšanas vietu atlasītās rindās.

Operācija ievēro konfigurāciju **Tukšā kvīts atļauta** noliktavas dimensijā **Atrašanās vieta** un neprasa ievadīt atrašanās vietas dimensiju, ja ir konfigurēta tukša saņemšanas vieta. Ja krājumam nav atļautas tukšas saņemšanas vietas, POS programmā tiek rādīta kļūda, un ir jāieraksta vieta, pirms saņemšanu var grāmatot.

### <a name="receive-all"></a>Saņemt visu

Pēc nepieciešamības varat atlasīt **Saņemt visu** programmas joslā, lai ātri atjauninātu daudzumu **Saņem tagad** visām dokumenta rindām uz maksimālo vērtību, kas ir pieejama saņemšanai šīm rindām.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Neplānotu krājumu saņemšana pirkšanas pasūtījumos

Commerce versijā 10.0.14 un jaunākās lietotāji var saņemt preci, kas sākotnēji nebija iekļauta pirkšanas pasūtījumā. Lai iespējotu šo funkcionalitāti, ieslēdziet **Pirkšanas pasūtījuma rindu pievienošana pārdošanas punkta saņemšanas laikā**.  

Šis līdzeklis darbojas tikai pirkšanas pasūtījuma saņemšanai. Nav iespējams saņemt krājumus pret pārsūtīšanas pasūtījumiem, ja krājumi iepriekš netika pasūtīti un nosūtīti no nosūtīšanas noliktavas.

Lietotāji nevar pievienot jaunas preces pirkšanas pasūtījumam POS saņemšanas laikā, ja tiek iespējota pirkšanas pasūtījuma [izmaiņu pārvaldības darbplūsma](../supply-chain/procurement/purchase-order-approval-confirmation.md) Commerce Headquarters (HQ). Lai iespējotu izmaiņu pārvaldību, visas izmaiņas pirkšanas pasūtījumā vispirms ir jāapstiprina, pirms saņemšana ir atļauta. Tā kā šis process ļauj uztvērējam pievienot jaunas rindas pirkšanas pasūtījumam, saņemšana neizdosies, ja ir iespējota izmaiņu pārvaldības darbplūsma. Ja izmaiņu pārvaldība ir iespējota visiem pirkšanas pasūtījumiem vai kreditoram, kas ir saistīts ar pirkšanas pasūtījumu, kas tiek aktīvi saņemts POS, lietotājs nevar pievienot jaunas preces pirkšanas pasūtījumam POS saņemšanas laikā.

Funkcionalitāte, kas iespējo pievienot rindas, nevar tikt izmantota kā risinājums, lai saņemtu papildu preču daudzumus, kas jau ir pirkšanas pasūtījumā. Pārsniegšana tiek pārvaldīta, izmantojot standarta [pārsniegšanas](#over-receiving-validations) iestatījumus preču rindai pirkšanas pasūtījumā.

Ja opcija **Pievienot rindas pārdošanas pasūtījumam saņemšanas punkta laikā** ir iespējota, un lietotājs saņem ar **Ienākošo operāciju** POS, ja lietotājs skenē vai pievieno produkta svītrkodu vai produkta numuru, kas pašreizējā pirkšanas pasūtījumā nav atpazīts kā prece, bet tiek atpazīts kā derīgs vienums, lietotājs saņem ziņojumu par preces pievienošanu pirkšanas pasūtījumam. Ja lietotājs pievieno krājumu pirkšanas pasūtījumam, ievadītais daudzums sadaļā **Saņem tagad** tiek uzskatīts par pirkšanas pasūtījuma rindas pasūtīto daudzumu.

Kad pirkšanas pasūtījuma saņemšana ir pabeigta un iesniegta HQ apstrādei, pievienotās rindas tiek veidotas pirkšanas pasūtījuma pamatdokumentā. Pirkšanas pasūtījuma rindā, kas atrodas HQ, redzēsiet **POS pievienots** karogu Pirkšanas pasūtījuma rindas cilnē **Vispārīgi**. **POS pievienots** karogs norāda, ka POS saņemšanas process pievienoja pirkšanas pasūtījuma rindu, un tā nebija rinda, kas bija pirkšanas pasūtījumā pirms saņemšanas.

### <a name="cancel-receiving"></a>Atcelt saņemšanu

Jums vajadzētu izmantot funkciju **Atcelt saņemšanu** programmas joslā vienīgi tad, ja vēlaties iziet no dokumenta un nevēlaties saglabāt izmaiņas. Piemēram, jūs sākotnēji atlasījāt nepareizu dokumentu un nevēlaties saglabāt nevienu no iepriekšējiem saņemšanas datiem.

### <a name="pause-receiving"></a>Pauzēt saņemšanu

Ja saņemat krājumu, varat izmantot funkciju **Apturēt saņemšanu**, ja vēlaties saņemšanas procesa pārtraukumu. Piemēram, jūs varētu vēlēties veikt citu operāciju no POS, piemēram, zvanīt klientu pārdošanas daļai vai aizkavēt saņemšanas grāmatošanu.

Kad atlasāt **Apturēt saņemšanu**, dokumenta statuss tiek mainīts uz **Apturēts**. Tāpēc lietotāji zinās, ka dokumentam ir ievadīti dati, bet dokuments vēl nav iesniegts. Kad esat gatavs atsākt saņemšanas procesu, atlasiet apturēto dokumentu un pēc tam atlasiet **Pasūtījuma informācija**. Jebkādi **Saņem tagad** daudzumi, kurus iepriekš saglabāja, tiek aizturēti un ir skatāmi skatā **Pilns pasūtījumu saraksts**.

### <a name="review"></a>Pārskats

Pirms kvīts galīgās saistīšanu uz Commerce Headquarters (HQ), varat izmantot pārskata funkcionalitāti, lai validētu ienākošo dokumentu. Pārskats brīdinās par jebkādiem trūkstošiem vai neprecīziem datiem, kas var izraisīt apstrādes kļūmi, un sniegs iespēju labot problēmas pirms kvīts pieprasījuma iesniegšanas. Lai iespējotu **Pārskata** funkciju programmu joslā, iespējojiet **Iespējot apstiprināšanu POS ienākošo un izejošo krājumu operāciju** funkciju, izmantojot **Funkciju pārvaldības** darbvietu programmā Commerce Headquarters (HQ).

**Pārskata** funkcija ienākošajā dokumentā validē šādas izejas plūsmas:

- **Pārsniegtie daudzumi** – saņemšanas daudzums ir lielāks par pasūtīto daudzumu. Šīs problēmas nopietnību nosaka pārsniegšanas konfigurācija Commerce Headquarters (HQ).
- **Nepietiekami daudzumi** – saņemšanas daudzums ir mazāks par pasūtīto daudzumu. Šīs problēmas nopietnību nosaka nepietiekamības konfigurācija Commerce Headquarters (HQ).
- **Sērijas numurs** — sērijas numurs netiek nodrošināts vai validēts serializētam krājumam, kam nepieciešams sērijas numurs, lai reģistrētos krājumos.
- **Novietojums nav iestatīts** — atrašanās vieta nav norādīta vienumam, ko kontrolē ar atrašanās vietu, ja tukša atrašanās vieta nav atļauta.
- **Dzēstās rindas** – pasūtījumam ir dzēstas rindas, ko izdzēš aa Commerce Headquarters (HQ) lietotājs, kas nav zināms POS lietojumprogrammā.

Iestatiet opciju **Iespējot automātisku pārbaudes** parametru uz **Jā** **Commerce parametri** > **Krājumi** > **Veikala krājumi**, lai validācija tiktu veikta automātiski, kad ir atlasīta opcija **Pabeigt saņemšanu**.

### <a name="finish-receiving"></a>Pabeigt saņemšanu

Pēc tam, kad esat pabeidzis ievadīt visus **Saņem tagad** daudzumus produktiem, ir programmas joslā jāatlasa **Pabeigt saņemšanu** programmas joslā, lai apstrādātu saņemšanu.

Kad lietotāji pabeidz pirkšanas pasūtījuma saņemšanu, tiek piedāvāts ievadīt vērtību laukā **Kvīts numurs**, ja šī funkcionalitāte ir konfigurēta. Parasti šī vērtība ir ekvivalenta kreditora pavadzīmes identifikatoram. **Kvīts numura** dati tiks glabāti produktu ieejas plūsmas žurnālā programmā Commerce Headquarters. Kvīšu numuri netiek tverti pārsūtīšanas pasūtījumu kvītīm.

Kad tiek izmantota asinhronā dokumenta apstrāde, kvīts tiek iesniegta, izmantojot asinhronu dokumenta struktūru. Laiks, kas nepieciešams, lai dokuments tiktu grāmatots, ir atkarīgs no dokumenta izmēra (rindu skaita) un vispārējās apstrādes satiksmes, kas notiek serverī. Parasti šis process notiek dažu sekunžu laikā. Ja dokumenta grāmatošana neizdodas, lietotājam tiek paziņots, izmantojot dokumentu sarakstu **Ienākošā operācija**, kur dokumenta statuss tiks atjaunināts uz **Apstrādes kļūme**. Lietotājs var atlasīt neizdevušos dokumentu POS, lai skatītu kļūdu ziņojumus un kļūmes iemeslu rūtī **Detalizēta informācija**. Neizdevies dokuments paliek negrāmatots, un ir nepieciešams, ka lietotājs atgriežas pie dokumenta rindām, POS atlasot **Pasūtījuma informācija**. Pēc tam lietotājam ir jāatjaunina dokuments ar labojumiem, pamatojoties uz kļūdām. Pēc dokumenta izlabošanas lietotājs var vēlreiz mēģināt apstrādāt to, atlasot **Pabeigt izpildi** programmu joslā.

## <a name="create-an-inbound-transfer-order"></a>Izveidojiet ienākošās pārsūtīšanas pasūtījumu

No POS lietotāji var izveidot jaunus pārsūtīšanas pasūtījumu dokumentus. Lai sāktu procesu, programmas joslā atlasiet **Jauns**, kad atrodaties galvenajā dokumentu sarakstā **Ienākošā operācija**. Pēc tam tiek parādīta uzvedne, lai atlasītu noliktavu vai veikalu **Pārsūtīt no**, kas nodrošinās krājumus jūsu veikala atrašanās vietā. Vērtības tiek ierobežotas līdz atlasei, kas definēta veikala izpildes grupas konfigurācijā. Ienākošās pārsūtīšanas pieprasījumā jūsu pašreizējais veikals vienmēr būs noliktava **Pārsūtīšana uz** pārsūtīšanas pasūtījumam. Šo vērtību nevar mainīt.

Pēc vajadzības varat ievadīt vērtības laukos **Nosūtīšanas datums**, **Saņemšanas datums** un **Piegādes veids**. Varat arī pievienot piezīmi, kas tiks uzglabāta kopā ar pārsūtīšanas pasūtījuma galveni, kā pielikumu dokumentam Commerce Headquarters.

Pēc kājenes informācijas izveides varat pievienot preces pārsūtīšanas pasūtījumam. Lai sāktu vienumu un pieprasīto daudzumu pievienošanu, atlasiet **Pievienot preci**. Rūtī **Detalizēta informācija** žurnāla rindām varat arī pievienot rindai specifisku piezīmi. Šīs piezīmes tiks uzglabātas kā rindas pielikums.

Kad ienākošā pārsūtījuma pasūtījumā ir ievadītas rindas, jāatlasa **Saglabāt**, lai saglabātu dokumenta izmaiņas lokāli, vai **Iesniegt pieprasījumu**, lai iesniegtu pasūtījuma informāciju Commerce Headquarters turpmākai apstrādei. Ja atlasāt **Saglabāt**, melnraksta dokuments tiek saglabāts kanāla datu bāzē, un izejošā noliktava nevar palaist dokumentu, kamēr tas nav veiksmīgi apstrādāts, izmantojot **Iesniegt pieprasījumu**. Izvēlieties **Saglabāt** tikai tad, ja neesat gatavs iesniegt pieprasījumu Commerce Headquarters apstrādei.

Ja dokuments ir saglabāts lokāli, to var atrast cilnē **Melnraksti** dokumentu sarakstā **Ienākošā operācija**. Kamēr dokumenta statuss ir **Melnraksts**, jūs varat to rediģēt, atlasot **Rediģēt**. Jūs variet atjaunināt, pievienot vai dzēst rindas pēc nepieciešamības. Varat arī dzēst visu dokumentu, kamēr tā statuss ir **Melnraksts**, atlasot **Dzēst** cilnē **Melnraksti**.

Pēc tam, kad melnraksta dokuments ir sekmīgi iesniegts Commerce Headquarters, tas cilnē **Aktīvs**, un tam ir statuss **Pieprasīts**. Šajā brīdī lietotāji saņemšanas veikalā vai noliktavā vairs nevar rediģēt pieprasīto ienākošā pārsūtīšanas pasūtījuma dokumentu. Tikai lietotāji, kas atrodas izejošajā noliktavā, var rediģēt dokumentu, POS programmā atlasot **Izejošā operācija**. Rediģēšanas bloķēšana nodrošina, ka nav konfliktu, jo ienākošais pieprasītājs maina pārsūtīšanas pasūtījumu tajā pašā laikā, kad izejošais nosūtītājs aktīvi veic pasūtījumu izdošanu un nosūtīšanu. Ja pēc pārsūtīšanas pasūtījuma iesniegšanas ir pieprasītas izmaiņas no ienākošā veikala vai noliktavas, ir jākontaktējas ar nosūtītāju un jāievada izmaiņas.

Kad dokumenta statuss ir **Pieprasīts**, tas ir redzams cilnē **Aktīvs**. Tomēr to nevar saņemt ienākošajā veikalā vai noliktavā. Pēc tam, kad nosūtīšanas noliktava ir nosūtījusi dažus vai visus pārsūtīšanas pasūtījumus, ienākošais veikals vai noliktava var grāmatot kvītis punktā POS. Kad izejošā puse apstrādā pārsūtīšanas pasūtīšanas dokumentus, viņu statuss tiek atjaunināts no **Pieprasīts** uz **Nosūtīts** vai **Daļēji nosūtīts**. Pēc tam, kad dokumentiem ir statuss **Nosūtīts** vai **Daļēji nosūtīts**, ienākošais veikals vai noliktava var grāmatot to kvītis, izmantojot ienākošās operācijas saņemšanas procesu.

## <a name="related-topics"></a>Saistītās tēmas

[Izejošo krājumu operācija punktā POS](pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]