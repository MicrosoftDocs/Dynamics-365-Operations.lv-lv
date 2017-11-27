---
title: "Elektronisko pārskatu veidošanas apskats"
description: "Šajā tēmā ir sniegts elektronisko atskaišu veidošanas (ER) rīka apskats. Tajā ir ietverta informācija par galvenajiem jēdzieniem, ER atbalstītajiem scenārijiem, kā arī saraksts ar formātiem, kas ir izstrādāti un izlaisti kā daļa no šī risinājuma."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ea9550b7209064a2842d7e5efe55e9e51c23b9f8
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="electronic-reporting-overview"></a>Elektronisko pārskatu veidošanas apskats

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts elektronisko atskaišu veidošanas (ER) rīka apskats. Tajā ir ietverta informācija par galvenajiem jēdzieniem, ER atbalstītajiem scenārijiem, kā arī saraksts ar formātiem, kas ir izstrādāti un izlaisti kā daļa no šī risinājuma.

ER ir rīks, kuru varat izmantot, lai konfigurētu gan ienākošo, gan izejošo elektronisko dokumentu formātus saskaņā ar dažādu valstu/reģionu juridiskajām prasībām. ER jums ļauj pārvaldīt šos formātus to lietošanas cikla laikā. Varat, piemēram, pieņemt jaunas normatīvās prasības un varat ģenerēt biznesa dokumentus nepieciešamajā formātā, lai elektroniski apmainītos ar informāciju ar valsts institūcijām, bankām un citām pusēm.

ER programma ir vērsta uz biznesa lietotājiem, nevis izstrādātājiem. Tā kā jūs konfigurējat formātus, nevis kodu, tad elektronisko dokumentu formātu izveidošanas un pielāgošanas process ir ātrāks un ērtāks.

Pašlaik ER atbalsta darblapu formātus TEXT, XML, Microsoft Word dokuments un OPENXML. Taču paplašinājumu interfeiss sniedz atbalstu papildu formātiem.

## <a name="capabilities"></a>Spējas
ER programmai ir šādas iespējas:

- Tā nodrošina vienu kopīgu rīku elektronisko pārskatu izveidei dažādos domēnos un aizstāj vairāk nekā 20 dažādas programmas, kas nodrošina noteikta veida elektronisko pārskatu izveides funkcijas programmā Microsoft Dynamics 365 for Finance and Operations.
- Tā nodrošina no pašreizējās Finance and Operations ieviešanas neatkarīgu pārskata formātu. Tas nozīmē, ka formātu var lietot dažādās Finance and Operations versijās.
- Tā atbalsta pielāgota formāta izveidošanu, balstoties uz sākotnējo formātu. Turklāt tā ietver iespējas automātiskai pielāgotā formāta jaunināšanai, ja sākotnējais formāts tiek mainīts, jo ir ieviestas kādas lokalizācijas/pielāgošanas prasības.
- Tas kļūst par primāro standarta rīku lokalizācijas prasību atbalstam elektronisko atskaišu izveidē — gan korporācijai Microsoft, gan Microsoft partneriem.
- Tā atbalsta iespēju sadalīt formātus partneriem un klientiem, izmantojot Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Galvenie principi
### <a name="components"></a>Komponenti

ER atbalsta divus komponentu tipus: **Datu modelis** un **Formāts**.

#### <a name="data-model-components"></a>Datu modeļa komponenti

Datu modeļa komponents ir abstrakts datu struktūras atainojums. Tas tiek izmantots kāda specifiska biznesa domēna apgabala aprakstīšanai pietiekami detalizēti, lai nodrošinātu šī domēna pārskatu veidošanas prasības. Datu modeļa komponents sastāv no šādām daļām:

- Datu modelis kā domēnam raksturīgo biznesa elementu kopa, un hierarhiski strukturēta šo elementu attiecību definīcija.
- Modeļa kartēšana, kas nodrošina atlasīto Finance and Operations datu avotu saistīšanu ar atsevišķiem datu modeļa elementiem, kuri izpildes laikā norāda datu plūsmu un kārtulas datu modeļa komponenta aizpildīšanai ar biznesa datiem.

Datu modeļa biznesa elements tiek attēlots kā konteiners (ieraksts). Biznesa vienuma rekvizīti tiek attēloti kā datu elementi (lauki). Katram datu vienumam ir unikāls nosaukums, etiķete, apraksts un vērtība. Katra datu vienuma vērtība var būt izveidota tā, lai tā tiktu atpazīta kā virkne, vesels skaitlis, reāls skaitlis, datums, uzskaitījums, Būla vērtība un citi datu tipi. Turklāt tā var būt cits ieraksts kādā ierakstu sarakstā.

Viens datu modeļa komponents var ietvert vairākas domēnam specifisko uzņēmējdarbības elementu hierarhijas. Tāpat tas var ietvert modeļa kartējumus, kas izpildes laikā atbalsta no pārskata atkarīgu datu plūsmu. Hierarhijas tiek atšķirtas pēc viena ieraksta, kas tika atlasīts kā modeļa kartēšanas sakne. Piemēram, maksājumu domēna apgabala datu modelis varētu atbalstīt šādus kartējumus:

- Uzņēmums > Kreditors > AP domēna maksājumu transakcijas
- Debitors > Uzņēmums > AR domēna maksājumu transakcijas

Ņemiet vērā, ka biznesa elementi, piemēram, uzņēmums un maksājumu transakcijas, tiek izveidoti vienreiz. Pēc tam dažādi kartējumi tos lieto atkārtoti.

Modeļa kartējumam, kas atbalsta izejošos elektroniskos dokumentus, ir tālāk norādītās iespējas.

- Kā datu modeļa datu avotus var izmantot dažādus Finance and Operations datu tipus. Piemēram, tā var izmantot tabulas, datu elementus, metodes vai uzskaitījumus.
- Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.
- Tas atbalsta Finance and Operations datu pārveidošanu nepieciešamajās grupās. Tāpat tas ļauj filtrēt, kārtot un summēt datus, kā arī pievienot loģiski aprēķinātos laukus, kuri ir izveidoti, izmantojot formulas, kas atgādina Microsoft Excel formulas, kā parādīts nākamajā attēlā. Papildinformāciju skatiet tēmā [Formulas veidotājs elektronisko pārskatu veidošanā](general-electronic-reporting-formula-designer.md)).

[![Formulas veidotājs](./media/ER-overview-01.png)](./media/ER-overview-01.png) 

Modeļa kartējumam, kas atbalsta ienākošos elektroniskos dokumentus, ir tālāk norādītās iespējas.

- Tas var kā mērķus izmantot dažādus atjaunināmos datu elementus. Šo datu elementu klāstā ietilpst tabulas, datu elementi un skati. Datus var atjaunināt, izmantojot datus no ienākošiem elektroniskajiem dokumentiem. Vienā modeļa kartēšanā var izmantot vairākus mērķus.
- Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.

Datu modeļa komponents tiek izveidots katram biznesa domēnam, kurš ir jāizmanto kā vienots datu avots tādai pārskatu veidošanai, kas atdala pārskatus no datu avotu fiziskās ieviešanas. Tas pārstāv domēnam specifiskās biznesa koncepcijas un funkcionalitātes tādā formā, kas pārskata formāta sākotnējo noformējumu un turpmāko uzturēšanu padara efektīvāku.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Formāta komponenti izejošiem elektroniskajiem dokumentiem

Formāta komponents ir atskaišu veidošanas izvades shēma, kas tiks ģenerēta izpildes laikā. Shēma sastāv no šādiem elementiem:

- Formāts, kas nosaka izpildes laikā ģenerētā izejošā elektroniskā dokumenta struktūru un saturu.
- Datu avoti kā lietotāja ievades parametru kopa un domēnam specifisku datu modelis, kas izmanto atlasīto modeļa kartēšanu.
- Formāta kartēšana kā formāta datu avotu saistījumu kopa, kuriem ir atsevišķi formāta elementi, kas izpildes laikā norāda datu plūsmu un kārtulas formāta izvades ģenerēšanai.
- Formāta validēšana kā konfigurējamu kārtulu kopa, kas izpildes laikā regulē pārskata ģenerēšanu atkarībā no izpildes konteksta. Var būt, piemēram, kārtula, kas aptur kreditoru maksājumu izvades ģenerēšanu un parāda izņēmumu, ja trūkst atlasītā kreditora specifisku atribūtu, piemēram, bankas konta numura.

Formāta komponents atbalsta tālāk aprakstītās funkcijas.

- Pārskatu izvade kā atsevišķu failu izveidošana dažādos formātos: piemēram, teksts, XML, Microsoft Word dokuments vai darblapa.
- Vairāku failu izveidošana atsevišķi un šo failu iekapsulēšana .zip failos.

Formāta komponents jums ļauj pievienot noteiktus failus, kurus var izmantot pārskatu izvadē tālāk aprakstītajos veidos.

- Excel darbgrāmatas, kas ietver darblapu, kuru var izmantot kā veidni izvadei OPENXML darblapas formātā
- Word faili, kas ietver dokumentu, kuru var izmantot kā veidni izvadei Microsoft Word dokumenta formātā
- Citi faili, kurus var iekļaut formāta izvadē kā iepriekš definētus failus

Nākamajā attēlā ir parādīts, kā šiem formātiem notiek datu plūsmas.

[![Datu plūsma izejošo formātu komponentiem](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Lai palaistu atsevišķi ER formāta konfigurāciju un ģenerētu izejošu elektronisko dokumentu, ir nepieciešams identificēt formāta konfigurācijas kartējumu.

#### <a name="format-components-for-incoming-electronic-documents"></a>Formāta komponenti ienākošiem elektroniskajiem dokumentiem
Formāta komponents ir ienākošā dokumenta shēma, kas tiek importēta izpildes laikā. Shēma sastāv no šādiem elementiem:

- Formāts, kas definē izpildes laikā importētā ienākošā un datus ietverošā elektroniskā dokumenta struktūru un saturu. Formāta komponents tiek izmantots, lai ienākošu dokumentu parsētu dažādos formātos, piemēram, kā tekstu un XML.
- Formāta kartēšanu, kas atsevišķus formāta elementus saista ar domēnam specifiskiem datu modeļa elementiem. Izpildlaikā elementi datu modelī norāda datu plūsmu un kārtulas, kas jāizmanto datu importēšanai no ienākoša dokumenta, un pēc tam šos datus saglabā datu modelī.
- Formāta validēšana kā konfigurējamu kārtulu kopa, kas izpildes laikā regulē datu importēšanu atkarībā no izpildes konteksta. Var būt, piemēram, kārtula, kas aptur kreditoru datu importēšanu tādam bankas izrakstam, kurā ir kreditora maksājumi, un parāda izņēmumu, ja trūkst kādu specifisku kreditora atribūtu, piemēram, kreditora identifikācijas koda.

Nākamajā attēlā ir parādīts, kā šiem formātiem notiek datu plūsmas.

[![Datu plūsma ienākošo formātu komponentiem](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Lai palaistu atsevišķu ER formāta konfigurāciju un importētu datus no ienākoša elektroniskā dokumenta, ir nepieciešams identificēt formāta konfigurācijas vēlamo kartējumu, kā arī modeļa kartējuma integrācijas punktu. Vienu un to pašu modeļa kartējumu un mērķus varat izmantot kopā ar dažādiem formātiem, kas paredzēti dažāda tipa ienākošajiem dokumentiem.

#### <a name="component-versioning"></a>Komponenta versiju izveide

ER komponentiem tiek atbalstīta versiju izveide. ER komponentu izmaiņu pārvaldīšanai tiek sniegta tālāk aprakstītā darbplūsma.

1. Sākotnēji izveidotā versija tiek atzīmēta kā versija **Melnraksts**. Šo versiju var rediģēt, un tā ir pieejama testu izpildīšanai.
2. Versiju **Melnraksts** var pārveidot par versiju **Pabeigts**. Šo versiju var izmantot vietējos atskaišu procesos.
3. Versiju **Pabeigts** var pārveidot par versiju **Koplietots**. Šī versija tiek publicēta LCS, un to var izmantot globālos pārskatu izveides procesos.
4. Versiju **Koplietots** var pārveidot par versiju **Pārtraukts**. Pēc tam šo versiju var dzēst.

Versijas, kuru statuss ir **Pabeigts** vai **Koplietots**, ir pieejamas citai datu apmaiņai. Komponentam, kam ir šie statusi, var izpildīt tālāk norādītās darbības.

- Komponentu var serializēt XML formātā un eksportēt kā XML formāta failu.
- Komponentu var atkārtoti serializēt no XML faila un importēt programmā Finance and Operations kā jaunu ER komponenta versiju.

#### <a name="component-date-effectivity"></a>Komponenta spēkā stāšanās datums

ER komponentu versijas ir ar spēkā stāšanās datumu. ER komponentam varat iestatīt datumu **Spēkā no**, lai norādītu datumu, kad šis komponents stājas spēkā pārskatu veidošanas procesiem. Finance and Operations sesijas datums tiek izmantots, lai noteiktu, vai komponents ir derīgs izpildei. Ja noteiktam datumam ir derīgas vairākas versijas, tad atskaišu veidošanas procesiem tiek izmantota jaunākā versija.

#### <a name="component-access"></a>Komponenta piekļuve

Piekļuve ER formāta komponentiem ir atkarīga no iestatījuma ISO valsts/reģiona kodam. Ja šis iestatījums atlasītajai formāta konfigurācijas versijai ir atstāts tukšs, formāta komponentam izpildes laikā var piekļūt no jebkura uzņēmuma. Ja šis iestatījums satur ISO valsts/reģiona kodus, formāta komponents ir pieejams tikai no uzņēmumiem, kuru primārā adrese ir definēta vienam no formāta komponenta ISO valsts/reģiona kodiem.

Datu formāta komponenta dažādām versijām var būt dažādi iestatījumi ISO valsts/reģiona kodiem.

#### <a name="configuration"></a>Konfigurācija

ER konfigurācija ir konkrēta ER komponenta aplika. Šis komponents var būt datu modeļa komponents vai formāta komponents. Konfigurācija var ietvert kāda ER komponenta dažādās versijas. Katra konfigurācija tiek atzīmēta kā piederoša konkrētam konfigurācijas nodrošinātājam. Konfigurācijas komponenta versiju **Melnraksts** var rediģēt, ja šīs konfigurācijas īpašnieks Finance and Operations ER iestatījumos ir atlasīts kā aktīvs nodrošinātājs.

Katra modeļa konfigurācija ietver datu modeļa komponentu. No konkrētas datu modeļa konfigurācijas var atvasināt jaunu formāta konfigurāciju. Konfigurāciju kokā šī izveidotā formāta konfigurācija tiek rādīta kā sākotnējā datu modeļa konfigurācijas pakārtotais elements.

Izveidotā formāta konfigurācija ietver formāta komponentu. Sākotnējā modeļa konfigurācijas datu modeļa komponents automātiski tiek ievietots pakārtotā formāta konfigurācijas formāta komponentā kā noklusējuma datu avots.

ER konfigurācija tiek koplietota Finance and Operations uzņēmumiem.

#### <a name="provider"></a>Piegādātājs

ER nodrošinātājs ir puses identifikators, kas tiek izmantots, lai norādītu katras ER konfigurācijas autoru (īpašnieku). ER jums ļauj pārvaldīt konfigurāciju nodrošinātāju sarakstu. Formāta konfigurācijas, kas ir izlaistas elektroniskajiem dokumentiem Finance and Operations risinājuma ietvaros, ir atzīmētas kā piederošas **Microsoft** konfigurācijas nodrošinātājam.

Lai uzzinātu, kā reģistrēt jaunu ER nodrošinātāju, noskatieties uzdevuma ceļvedi **ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu** (daļa no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**).

#### <a name="repository"></a>Repozitorijs

ER repozitorijā glabājas ER konfigurācijas. Pašlaik tiek atbalstīti divi ER repozitoriju tipi: **Operāciju resursi** un **LCS projekts**.

Repozitorijs **Operācijas resursi** nodrošina piekļuvi to konfigurāciju sarakstam, ko korporācija Microsoft kā ER konfigurāciju nodrošinātājs ir izlaidusi Finance and Operations risinājuma ietvaros. Šīs konfigurācijas var importēt pašreizējā Finance and Operations instancē un izmantot elektronisko pārskatu veidošanai. Tās var izmantot arī papildu lokalizācijām un pielāgojumiem.

Repozitorijs **LCS projekts** nodrošina piekļuvi noteikta LCS projekta (LCS projekta līdzekļu bibliotēkas) konfigurāciju sarakstam, kurš tika atlasīts repozitorija reģistrācijas posmā. ER sniedz iespēju koplietotās konfigurācijas no pašreizējās Finance and Operations instances augšupielādēt konkrētā repozitorijā **LCS projekts**. Konfigurācijas varat arī importēt no repozitorija **LCS projekts** pašreizējā Finance and Operations instancē.

Nepieciešamos veida **LCS projekts** repozitorijus var atsevišķi reģistrēt katram pašreizējās Finance and Operations instances konfigurāciju nodrošinātājam. Katru repozitoriju var piešķirt noteiktam konfigurācijas nodrošinātājam.

## <a name="supported-scenarios"></a>Atbalstītie scenāriji
### <a name="building-a-data-model"></a>Datu modeļa veidošana

ER nodrošina modeļa veidotāju, kuru varat izmantot, lai izveidotu datu modeli noteiktam biznesa domēnam. Visus domēnam raksturīgos biznesa elementus un attiecības starp tiem varat norādīt datu modelī kā hierarhisku struktūru. Nākamajā attēlā ir parādīts šāda tipa datu modeļa piemērs (maksājumu domēna datu modelis). 

[![Maksājuma domēna datu modelis](./media/ER-overview-04.png)](./media/ER-overview-04.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku datu modeli** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="translating-data-model-content"></a>Datu modeļa satura tulkošana

Datu modeļa saturu (etiķetes un aprakstus) var tulkot citās programmatūrā Finance and Operations atbalstītajās valodās. Iespējams, datu modeļa saturu vēlaties tulkot tālāk uzskaitīto iemeslu dēļ.

-   Izstrādes laikā, lai saturu padarītu saprotamāku formāta veidotājiem, kuri runā citās valodās un kuri datu modeli izmantos formāta komponentu datu kartēšanai.
-   Izpildes laikā, lai saturu padarītu lietotājiem draudzīgāku, uzvednes un palīdzību izpildes laika parametriem, kā arī konfigurētus validēšanas ziņojumus (kļūdām un brīdinājumiem) rādot tādā valodā, kādai dod priekšroku programmatūrā lietotājs, kurš ir pieteicies pašlaik.

Nākamajā attēlā ir parādīts piemērs tam, kā datu modeļa saturs no angļu valodas tiek tulkots japāņu valodā. 

[![Datu modeļa saturs angļu valodā](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Datu modeļa saturs, kas pārtulkots japāņu valodā](./media/ER-overview-06.png)](./media/ER-overview-06.png)


### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Datu modeļa kartējumu konfigurēšana izejošajiem dokumentiem

ER nodrošina modeļa kartēšanas veidotāju, kas lietotājiem sniedz iespēju savus izstrādātos datu modeļus kartēt uz noteiktiem Finance and Operations datu avotiem. Pamatojoties uz kartējumu, izpildes laikā dati no atlasītajiem datu avotiem tiek importēti datu modelī. Pēc tam datu modelis tiek izmantots kā abstrakts datu avots ER formātiem, kas ģenerē izejošus elektroniskos dokumentus. Nākamajā attēlā ir parādīts šī tipa datu modeļa kartējuma piemērs (maksājumu domēna datu modeļa kartējums **SEPA kredīta pārskaitījums**). 

[![Datu modeļa kartējuma piemērs](./media/ER-overview-07.png)](./media/ER-overview-07.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevumu ceļvežus **ER Definēt modeļa kartēšanu un atlasīt datu avotus** un **ER Kartēt datu modeli uz atlasītajiem datu avotiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Datu modeļa kartējumu konfigurēšana ienākošiem dokumentiem
ER nodrošina modeļu kartēšanas veidotāju, kas lietotājiem savus izveidotos datu modeļus ļauj kartēt uz noteiktiem galamērķiem. Datu modeļus var kartēt, piemēram, uz Finance and Operations atjaunināmiem datu komponentiem (tabulām, datu elementiem un skatiem). Pamatojoties uz kartējumu, Finance and Operations dati izpildes laikā tiek atjaunināti, izmantojot datus no datu modeļa. Kā abstrakta ER formāta krātuve šis datu modelis tiek aizpildīts ar datiem, kas tiek importēti no ienākoša elektroniskā dokumenta. Nākamajā attēlā ir parādīts šāda tipa datu modeļa kartējuma piemērs. Šajā piemērā maksājumu domēna datu modeļa kartējums **NETS importa kartējums** tiek izmantots, lai atbalstītu bankas izrakstu importēšanu Norvēģijas bankas formātā NETS.

[![NETS datu modeļa importa kartējuma piemērs](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Izveidotā modeļa komponenta kā modeļa konfigurācijas saglabāšana

Modulī ER izstrādātu datu modeli var glabāt kopā ar saistītajiem datu kartējumiem kā pašreizējās Finance and Operations instances modeļa konfigurāciju. Nākamajā attēlā ir parādīts šāda tipa datu modeļa konfigurācijas piemērs (maksājumu modeļa konfigurācija). 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Kartēt datu modeli uz atlasītajiem datu avotiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Tāda formāta veidošana, kas kā pamatu izmanto datu modeli

ER atbalsta formāta veidotāju, ko varat izmantot, lai veidotu elektroniskā dokumenta formātu kādam atlasītajam biznesa domēnam, kā pamatu atlasot modeļa komponentu. Tas pats ER formāta veidotājs jums ļauj izveidoto formātu kartēt uz atlasīto domēna datu modeļa kartēšanu kā datu avotu. Nākamajā attēlā ir parādīts šāda tipa formāta piemērs (formāta konfigurācija, kas nodrošina **BACS** maksājuma formātu Apvienotajai Karalistei). 

[![Piemērs formātam, kuram kā pamats ir datu modelis](./media/ER-overview-09.png)](./media/ER-overview-09.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku formātu** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigurācijas veidošana, lai ģenerētu elektroniskos dokumentus OPENXML darblapas formātā

ER formāta veidotāju var izmantot, lai veidotu elektronisko dokumentu OPENXML darblapas formātā. Nākamajā attēlā ir parādīts šāda tipa formāta piemērs (formāta konfigurācija, lai ģenerētu OPENXML darblapu ar informāciju par atlasītu maksājumu žurnālu).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot konfigurāciju atskaitēm OPENXML formātā** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**). Kā daļu no veidnes importēšanas uzdevuma ceļveža kā veidni izmantojiet Excel failu [Maksājumu pārskata veidne (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Konfigurācijas veidošana, lai ģenerētu elektroniskos dokumentus Word dokumenta formātā
ER formāta veidotāju var izmantot, lai veidotu elektronisko dokumentu Word dokumenta formātā. Nākamajā attēlā ir parādīts šāda tipa formāta piemērs. Ņemiet vērā, ka šis formāts atkārtoti izmanto esošo ER konfigurāciju, kas sākotnēji bija veidota tā, lai pārskata izvadi ģenerētu OPENXML formātā.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, noskatieties uzdevuma ceļvedi ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā Microsoft WORD (daļa no biznesa procesa 7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)). Kā daļu no šī uzdevumu ceļveža darbības veidnes importēšanai kā veidnes ER formātam izmantojiet tālāk norādītos Word failus.

- [Maksājumu pārskata veidne (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Maksājumu pārskata saistītā veidne (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Konfigurācijas veidošana datu importēšanai no ienākošiem elektroniskajiem dokumentiem  
ER formāta veidotāju var izmantot, lai aprakstītu elektronisku dokumentu, kurš tiek plānots datu importēšanai XML vai teksta formātā. Izveidotais formāts tiek lietots, lai parsētu ienākošu dokumentu. ER formāta kartējuma veidotāju var izmantot, lai definētu izveidotā formāta elementu saistīšanu ar datu modeli. Nākamajos attēlos ir redzams šāda tipa formāta un formātu kartējuma piemērs. Šajā piemērā tiek importēti NETS bankas izraksti, kas ietver informāciju par kreditoru maksājumiem teksta formātā.

[![ER-format-designer](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER-model-mapping-designer](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, noskatieties uzdevuma ceļvedi Izveidot nepieciešamās ER konfigurācijas, lai importētu datus no ārēja faila (daļa no biznesa procesa 7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)). Lai izpildītu šo ceļvedi, izmantot tālāk norādītos failus.

- [ER datu modeļa konfigurācija (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER formāta konfigurācija (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [XML formātā ienākoša dokumenta piemērs (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Darbgrāmatas piemērs ienākoša dokumenta datu pārvaldīšanai (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Izveidotā formāta komponenta glabāšana formāta konfigurācijā

Modulī ER izstrādātu formātu var glabāt kopā ar konfigurētajiem datu kartējumiem kā pašreizējās Finance and Operations instances formāta konfigurāciju. Iepriekšējā attēlā ir parādīts šāda tipa formāta konfigurācijas piemērs (**BACS (UK)**, kas ir konfigurācijas **Maksājumu modelis** pakārtotais elements). Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku formātu** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>Finance and Operations konfigurēšana izveidota formāta iekšējai lietošanai

Programmatūru Finance and Operations var konfigurēt tā, lai elektronisko pārskatu ģenerēšanai sāktu izmantot izveidotu formātu. Atsauce uz izveidoto formāta konfigurāciju ir jādefinē noteikta domēna iestatījumos. Piemēram, lai elektroniskiem kreditoru maksājumiem BACS formātā sāktu izmantot ER formāta konfigurāciju, noteiktās maksāšanas metodēs ir jāietver atsauce uz šo formāta konfigurāciju, kā tas ir redzams tālāk esošajos attēlos. 

[![Formāta BACS (UK) konfigurācija](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Atsauces uz formātu BACS (UK) ietveršana maksāšanas metodē](./media/ER-overview-15.png)](./media/ER-overview-15.png)

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Lietot formātu, lai ģenerētu elektroniskus dokumentus maksājumiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

## <a name="handling-er-components"></a>Darbs ar ER komponentiem
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponenta publicēšana pakalpojumos LCS, lai to piedāvātu ārēji (lokalizācija)

Izveidota komponenta (modeļa vai formāta) īpašnieks var izmantot ER, lai komponenta pabeigto versiju publicētu pakalpojumos LCS. Pašreizējās ER konfigurācijas nodrošinātājam ir nepieciešams repozitorijs ar tipu **LCS projekts**. Kad komponenta pabeigtas versijas statuss no **PABEIGTS** tiek mainīts uz **KOPLIETOTS**, šī versija tiek publicēta pakalpojumos LCS. Kad komponents ir publicēts pakalpojumos LCS, šī komponenta īpašnieks kļūst par pakalpojuma nodrošinātāju, lai atbalstītu šo komponentu. Piemēram, ja formāta komponents ir paredzēts, lai ģenerētu elektronisku dokumentu, kurš ir juridiski nepieciešams (piemēram, saskaņā ar kādu lokalizācijas scenāriju), tad tiek pieņemts, ka šis formāts saglabāsies atbilstošs likumdošanas izmaiņām un ka tā nodrošinātājs izdos šī komponenta jaunās versijas katru reizi, kad radīsies jaunas likumdošanas prasības. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services**(daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponenta importēšana no LCS iekšējai izmantošanai

ER jums sniedz iespēju ER komponentus no LCS importēt pašreizējā Finance and Operations instancē. Ir nepieciešams repozitorijs ar tipu **LCS projekts**. Kad ER komponents no LCS ir importēts pašreizējā Finance and Operations instancē, šīs instances īpašnieks kļūst par importētā komponenta īpašnieka (autora) nodrošinātā pakalpojuma patērētāju. Ja ir izstrādāts, piemēram, formāta komponents noteikta elektroniskā dokumenta ģenerēšanai no Finance and Operations valstij/reģionam raksturīgā formātā (lokalizācijas scenārijs), tad tiek pieņemts, ka pakalpojuma patērētājs varēs iegūt visus šim formātam veiktos atjauninājumus, lai nodrošinātu tā atbilstību likumdošanas prasībām. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Importēt konfigurāciju no Lifecycle Services** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formāta veidošana, atlasot citu formātu kā pamatu (pielāgošana)

ER jums ļauj izveidot (atvasināt) jaunu komponentu no komponenta pašreizējās versijas (bāzes), kas tika importēta no LCS. Piemēram, lietotājs vēlas atvasināt jaunu formātu, lai ieviestu kaut kādas īpašas elektroniskā dokumenta prasības (piemēram, papildu lauku vai izsmeļošu aprakstu) un atbalstītu pielāgošanas scenāriju. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Jaunināt formātu, pieņemot tam jaunu pamata versiju** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formāta atjaunināšana, atlasot jaunu pamata formāta versiju (pārskatīt)

ER jums ļauj atvasinātā komponenta pašreizējā melnraksta versijā automātiski pieņemt pamata komponenta jaunākajā versijā veiktās izmaiņas. Šis process tiek saukts par *pārbāzēšanu*. Piemēram, no LCS importētā formāta jaunākajā versijā ieviestās jaunās normatīvās izmaiņas var automātiski sapludināt elektroniskā dokumenta šī formāta pielāgotajā versijā. Visas izmaiņas, kuras nevar sapludināt automātiski, tiek uzskatītas par konfliktiem. Šie konflikti tiek parādīti manuālai atrisināšanai atbilstošā komponenta veidotāja rīkā. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER formāta jaunināšana, ieviešot šī formāta jauno bāzes versiju** (daļa no biznesa procesa **7.5.5.3. Izmainīta IT pakalpojumu/risinājumu komponenta iegāde/izstrāde (10683)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>Finance and Operations risinājumā ietverto ER konfigurāciju saraksts
| Domēnam specifiskās datu modeļu konfigurācijas: virsraksts | Domēns                | No datu modeļa atkarīgās formāta konfigurācijas: virsraksts | Apraksts                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Audita faila modelis                                 | Finanšu audits       |                                                   |                                                                    |
|                                                  |                       | Audita fails (NL)                                   | Audita faila formāts Nīderlandei                                  |
| BAS modelis                                        | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | BAS formāts Austrālijai                                           |
| Būvniecības nozares shēmas modelis               | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | CIS ikmēneša atgriešana (UK)                           | CIS ikmēneša atgriešanas formāts Apvienotajai Karalistei                   |
| Atgādinājuma vēstules modelis                          | Elektroniskie rēķini  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Atgādinājuma vēstule (DK)                     | OIOUBL atgādinājuma vēstules formāts Dānijai                        |
| Elektroniskais virsgrāmatas uzskaites modelis (MX)          | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | Papildu virsgrāmatas XML (MX)                         | Papildu virsgrāmatas transakcijas uz kontu, atskaites formāts Meksikai |
|                                                  |                       | Kontu plāna XML (MX)                         | Kontu plāna atskaites formāts Meksikai                          |
|                                                  |                       | Žurnālu XML (MX)                                 | Žurnālu transakciju atskaites formāts Meksikai                      |
|                                                  |                       | Apgrozījuma bilances XML (MX)                            | Apgrozījuma bilances atskaites formāts Meksikai                             |
| Elster modelis                                     | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster formāts Vācijai                                          |
| ES pārdošanas saraksta modelis                              | Tirdzniecības atskaites       |                                                   |                                                                    |
|                                                  |                       | ES pārdošanas saraksts (DE)                                | ES pārdošanas saraksta TXT formāts Vācijai                               |
|                                                  |                       | ES pārdošanas saraksts (DK)                                | ES pārdošanas saraksta TXT formāts Dānijai                               |
|                                                  |                       | ES pārdošanas saraksts (FR)                                | ES pārdošanas saraksta XML formāts Francijai                                |
|                                                  |                       | ES pārdošanas saraksts (NL)                                | ES pārdošanas saraksta XML formāts Nīderlandei                           |
|                                                  |                       | ES pārdošanas saraksta TXT (UK)                            | ES pārdošanas saraksta TXT formāts Apvienotajai Karalistei                    |
|                                                  |                       | ES pārdošanas saraksta XML (UK)                            | ES pārdošanas saraksta XML formāts Apvienotajai Karalistei                    |
|                                                  |                       | ES pārdošanas saraksta atskaite pēc kolonnām                   | ES pārdošanas saraksta atskaite pēc kolonnām                                    |
|                                                  |                       | ES pārdošanas saraksta atskaite pēc rindām                      | ES pārdošanas saraksta atskaite pēc rindām                                       |
| FEC uzskaites modelis (FR)                        | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | FEC uzskaites datu XML (FR)                      | FEC uzskaites datu eksporta XML formāts Francijai                   |
| Vācijas audita fails                                | Finanšu audits       |                                                   |                                                                    |
|                                                  |                       | Vācijas audita faila izvade                          | Audita faila izvade Vācijai un Austrijai                          |
| Intrastat modelis                                  | Tirdzniecības atskaites       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat formāts Vācijai                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat formāts Dānijai                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastat INTRACOM formāts Francijai                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastat SAISUNIC formāts Francijai                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat formāts Nīderlandei                               |
|                                                  |                       | Intrastat (UK)                                    | Intrastat formāts Apvienotajai Karalistei                            |
|                                                  |                       | Intrastat pārskats                                  | Intrastat Excel kontroles atskaite                                     |
| Debitora rēķina modelis                           | Elektroniskie rēķini  |                                                   |                                                                    |
|                                                  |                       | OIOUBL projekta kredīta nota (DK)                   | OIOUBL projekta kredīta notas formāts Dānijai                      |
|                                                  |                       | OIOUBL projekta rēķins (DK)                       | OIOUBL projekta rēķina formāts Dānijai                          |
|                                                  |                       | OIOUBL pārdošanas kredīta nota (DK)                     | OIOUBL pārdošanas kredīta notas formāts Dānijai                        |
|                                                  |                       | OIOUBL pārdošanas rēķins (DK)                         | OIOUBL pārdošanas rēķina formāts Dānijai                            |
| OB deklarācijas modelis                             | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | OB deklarācija (NL)                               | OB deklarācijas formāts Nīderlandei                          |
| Maksājuma modelis                                    | Maksājumi              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice maksājuma formāts Dānijai                        |
|                                                  |                       | Vekseļa pārskaitījums (FR)                  | Vekseļa pārskaitījuma formāts Francijai                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91 kreditora maksājuma formāts Nīderlandei                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB tiešā debeta maksājuma formāts Francijai                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB iekšzemes kreditora maksājuma formāts Francijai                    |
|                                                  |                       | Nordea kreditors (DK)                                | Nordea Corporate Netbank kreditora maksājuma formāts Dānijai         |
|                                                  |                       | ANZ tiešā kredīta pakalpojums (AU)                    | Formāts ANZ tiešā kredīta pakalpojumam Austrālijai                 |
|                                                  |                       | CBA tiešā kredīta pakalpojums (AU)                    | Formāts CBA tiešā kredīta pakalpojumam Austrālijai                 |
|                                                  |                       | NAB tiešā kredīta pakalpojums (AU)                    | Formāts NAB tiešā kredīta pakalpojumam Austrālijai                 |
|                                                  |                       | STG tiešā kredīta pakalpojums (AU)                    | Formāts STG tiešā kredīta pakalpojumam Austrālijai                 |
|                                                  |                       | WBC tiešās ievades sistēma (AU)                      | Formāts WBC tiešās ievades sistēmai Austrālijai                   |
|                                                  |                       | DirectLink (NZ)                                   | Formāts DirectLink Jaunzēlandei                              |
|                                                  |                       | JBA maksājuma fails (JP)                             | JBA maksājuma formāts Japānai                                       |
|                                                  |                       | ISO20022 kredīta pārskaitījums                          | SEPA kredīta pārskaitījuma formāts Eiropai                             |
|                                                  |                       | ISO20022 kredīta pārskaitījums (FR)                     | SEPA kredīta pārskaitījuma formāts Francijai                             |
|                                                  |                       | ISO20022 kredīta pārskaitījums (DE)                     | SEPA kredīta pārskaitījuma formāts Vācijai                            |
|                                                  |                       | ISO20022 kredīta pārskaitījums (NL)                     | SEPA kredīta pārskaitījuma formāts Nīderlandei                    |
|                                                  |                       | ISO20022 tiešais debets                             | SEPA tiešā debeta formāts Eiropai                                |
|                                                  |                       | ISO20022 tiešais debets (FR)                        | SEPA tiešā debeta formāts Francijai                                |
|                                                  |                       | ISO20022 tiešais debets (DE)                        | SEPA tiešā debeta formāts Vācijai                               |
|                                                  |                       | ISO20022 tiešais debets (NL)                        | SEPA tiešā debeta formāts Nīderlandei                       |
|                                                  |                       | BACS (UK)                                         | BACS kreditora maksājuma formāts Apvienotajai Karalistei                  |
| Atgriezes maksa                                   | Nodokļu atskaites         |                                                   |                                                                    |
|                                                  |                       | Atgrieztās papildmaksas pārdošanas saraksts                         | Atgrieztās maksas pārdošanas saraksta formāts                                   |
| Holandiešu XBRL integrācijas modelis                     | XBRL pārskati        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL eksporta formāts Nīderlandei                    |
| GAF modelis (MY)                                   | Finanšu audits       |                                                   |                                                                    |
|                                                  |                       | GAF fails (MY)                                     | GAF formāts Malaizijai                                         |
| Kreditoru vecumstruktūras atskaite (CN)                         | Kreditoru datu analīze |                                                   |                                                                    |
|                                                  |                       | Kreditoru vecumstruktūras atskaites formāts (CN)                   | Kreditoru vecumstruktūras atskaites formāts Ķīnai                               |
| Kreditora rēķina deklarācijas modelis                 | Kreditoru datu analīze |                                                   |                                                                    |
|                                                  |                       | Kreditora rēķina deklarācija (IS)                   | Kreditora rēķina deklarācijas formāts Islandei                      |
|                                                  |                       | Kreditora rēķina deklarācijas atskaite (IS)            | Kreditora rēķina deklarācijas atskaite Islandei                      |



<a name="see-also"></a>Skatiet arī
--------

[Lokalizācijas prasības — izveidot elektronisko atskaišu konfigurāciju](electronic-reporting-configuration.md)

[Elektronisko atskaišu veidošanas konfigurācijas dzīves cikla pārvaldīšana](general-electronic-reporting-manage-configuration-lifecycle.md)




