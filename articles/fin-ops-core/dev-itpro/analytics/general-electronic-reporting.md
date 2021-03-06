---
title: Elektroniskie pārskati (ER)
description: Šajā tēmā ir sniegts elektronisko atskaišu veidošanas (ER) rīka pārskats. Tajā ir aprakstītas galvenās koncepcijas, atbalstītie scenāriji un formāti, kas ir daļa no risinājuma.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26088a01b0e849a5df559631591ec65d7885452b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944369"
---
# <a name="electronic-reporting-er-overview"></a>Elektronisko pārskatu veidošanas (ER) apskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts elektronisko atskaišu veidošanas (ER) rīka apskats. Tajā ir ietverta informācija par galvenajiem jēdzieniem, ER atbalstītajiem scenārijiem, kā arī saraksts ar formātiem, kas ir izstrādāti un izlaisti kā daļa no šī risinājuma.

ER ir rīks, kuru varat izmantot, lai konfigurētu gan ienākošo, gan izejošo elektronisko dokumentu formātus saskaņā ar dažādu valstu/reģionu juridiskajām prasībām. ER jums ļauj pārvaldīt šos formātus to lietošanas cikla laikā. Varat, piemēram, pieņemt jaunas normatīvās prasības un varat ģenerēt biznesa dokumentus nepieciešamajā formātā, lai elektroniski apmainītos ar informāciju ar valsts institūcijām, bankām un citām pusēm.

ER programma ir vērsta uz biznesa lietotājiem, nevis izstrādātājiem. Tā kā jūs konfigurējat formātus, nevis kodu, tad elektronisko dokumentu formātu izveidošanas un pielāgošanas process ir ātrāks un ērtāks.

Pašlaik modulis ER atbalsta šādus darblapu formātus: TEXT, XML, Microsoft Word dokuments, un OPENXML Taču paplašinājumu interfeiss sniedz atbalstu papildu formātiem.

## <a name="capabilities"></a>Spējas

ER programmai ir šādas iespējas:

- Tā nodrošina vienu kopēju rīku elektronisko pārskatu izveidei dažādos domēnos un aizstāj vairāk nekā 20 dažādas programmas, kas izpilda kāda veida elektronisko pārskatu izveides darbības programmā Finance and Operations.
- Tā atskaišu formātu izolē no pašreizējās implementācijas. Citiem vārdiem, formāts ir piemērojamas dažādām versijām.
- Tā atbalsta pielāgota formāta izveidošanu, balstoties uz sākotnējo formātu. Turklāt tā ietver iespējas automātiskai pielāgotā formāta jaunināšanai, ja sākotnējais formāts tiek mainīts, jo ir ieviestas kādas lokalizācijas/pielāgošanas prasības.
- Tas kļūst par primāro standarta rīku lokalizācijas prasību atbalstam elektronisko atskaišu izveidē — gan korporācijai Microsoft, gan Microsoft partneriem.
- Tā atbalsta iespēju izplatīt formātus partneriem un debitoriem, izmantojot portālu Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Galvenie principi

### <a name="components"></a>Komponenti

ER atbalsta divus komponentu tipus: **Datu modelis** un **Formāts**.

#### <a name="data-model-and-model-mapping-components"></a>Datu modeļa un modeļa kartēšanas komponenti

Datu modeļa komponents ir abstrakts datu struktūras atainojums. Tas tiek izmantots kāda specifiska biznesa domēna apgabala aprakstīšanai pietiekami detalizēti, lai nodrošinātu šī domēna pārskatu veidošanas prasības. Datu modeļa komponents sastāv no šādām daļām:

- <a name="DataModelComponent"></a>Datu modelis kā domēnam raksturīgo biznesa elementu kopa, un hierarhiski strukturēta šo elementu attiecību definīcija.
- <a name="ModelMappingComponent"></a>Modeļa kartēšana, kas atlasīto programmas datu avotu saista ar atsevišķiem datu modeļa elementiem, kuri izpildes laikā norāda datu plūsmu un kārtulas biznesa datu aizpildīšanai datu modeļa komponentā.

Datu modeļa biznesa elements tiek attēlots kā konteiners (ieraksts). Biznesa vienuma rekvizīti tiek attēloti kā datu elementi (lauki). Katram datu vienumam ir unikāls nosaukums, etiķete, apraksts un vērtība. Katra datu vienuma vērtība var būt izveidota tā, lai tā tiktu atpazīta kā virkne, vesels skaitlis, reāls skaitlis, datums, uzskaitījums, Būla vērtība un citi datu tipi. Turklāt tā var būt cits ieraksts kādā ierakstu sarakstā.

Viens datu modeļa komponents var ietvert vairākas domēnam specifisko uzņēmējdarbības elementu hierarhijas. Tāpat tas var ietvert modeļa kartējumus, kas izpildes laikā atbalsta no pārskata atkarīgu datu plūsmu. Hierarhijas tiek atšķirtas pēc viena ieraksta, kas tika atlasīts kā modeļa kartēšanas sakne. Piemēram, maksājumu domēna apgabala datu modelis varētu atbalstīt šādus kartējumus:

- Uzņēmums \> kreditors \> parādu kreditoriem domēna maksājumu transakcijas
- Debitors \> uzņēmums \> debitoru parādu domēna maksājumu transakcijas

Ņemiet vērā, ka biznesa elementi, piemēram, uzņēmums un maksājumu transakcijas, tiek izveidoti vienreiz. Pēc tam dažādi kartējumi tos lieto atkārtoti.

Modeļa kartējumam, kas atbalsta izejošos elektroniskos dokumentus, ir tālāk norādītās iespējas.

- Kā datu avotus kādam datu modelim tā var izmantot dažādus datu tipus. Piemēram, tā var izmantot tabulas, datu elementus, metodes vai uzskaitījumus.
- Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.
- Tas atbalsta datu pārveidošanu nepieciešamajās grupās. Turklāt tas sniedz iespēju filtrēt, kārtot un summēt datus, kā arī pievienot loģiski aprēķinātos laukus, kuri ir izveidoti, izmantojot formulas, kas līdzinās Microsoft Excel formulām. Papildinformāciju skatiet tēmā [Formulas veidotājs elektronisko pārskatu (EP) veidošanā](general-electronic-reporting-formula-designer.md)).

Modeļa kartējumam, kas atbalsta ienākošos elektroniskos dokumentus, ir tālāk norādītās iespējas.

- Tas var kā mērķus izmantot dažādus atjaunināmos datu elementus. Šo datu elementu klāstā ietilpst tabulas, datu elementi un skati. Datus var atjaunināt, izmantojot datus no ienākošiem elektroniskajiem dokumentiem. Vienā modeļa kartēšanā var izmantot vairākus mērķus.
- Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.

Datu modeļa komponents tiek izveidots katram biznesa domēnam, kurš ir jāizmanto kā vienots datu avots tādai pārskatu veidošanai, kas atdala pārskatus no datu avotu fiziskās ieviešanas. Tas pārstāv domēnam specifiskās biznesa koncepcijas un funkcionalitātes tādā formā, kas pārskata formāta sākotnējo noformējumu un turpmāko uzturēšanu padara efektīvāku.

#### <a name="format-components-for-outgoing-electronic-documents"></a><a name="FormatComponentOutbound"></a>Formāta komponenti izejošiem elektroniskajiem dokumentiem

Formāta komponents ir atskaišu veidošanas izvades shēma, kas tiks ģenerēta izpildes laikā. Shēma sastāv no šādiem elementiem:

- Formāts, kas nosaka izpildes laikā ģenerētā izejošā elektroniskā dokumenta struktūru un saturu.
- Datu avoti kā lietotāja ievades parametru kopa un domēnam specifisku datu modelis, kas izmanto atlasīto modeļa kartēšanu.
- Formāta kartēšana kā formāta datu avotu saistījumu kopa, kuriem ir atsevišķi formāta elementi, kas izpildes laikā norāda datu plūsmu un kārtulas formāta izvades ģenerēšanai.
- Formāta validēšana kā konfigurējamu kārtulu kopa, kas izpildes laikā regulē pārskata ģenerēšanu atkarībā no izpildes konteksta. Var būt, piemēram, kārtula, kas aptur kreditoru maksājumu izvades ģenerēšanu un parāda izņēmumu, ja trūkst atlasītā kreditora specifisku atribūtu, piemēram, bankas konta numura.

Formāta komponents atbalsta tālāk aprakstītās funkcijas.

- Pārskatu izveides izvade, izveidojot atsevišķus dažādu formātu, piemēram, teksta, XML, Microsoft Word dokumenta vai darblapas, failus.
- Vairāku failu izveidošana atsevišķi un šo failu iekapsulēšana .zip failos.

Formāta komponents jums ļauj pievienot noteiktus failus, kurus var izmantot pārskatu izvadē tālāk aprakstītajos veidos.

- Excel darbgrāmatas, kas ietver darblapu, kuru var izmantot kā veidni izvadei OPENXML darblapas formātā
- Word faili, kuros ir ietverts dokumentu, kuru var izmantot kā veidni izvadei Microsoft Word dokumenta formātā
- Citi faili, kurus var iekļaut formāta izvadē kā iepriekš definētus failus

Nākamajā attēlā ir parādīts, kā šiem formātiem notiek datu plūsmas.

[![Datu plūsma izejošo formātu komponentiem](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Lai palaistu atsevišķi ER formāta konfigurāciju un ģenerētu izejošu elektronisko dokumentu, ir nepieciešams identificēt formāta konfigurācijas kartējumu.

#### <a name="format-components-for-incoming-electronic-documents"></a><a name="FormatComponentInbound"></a>Formāta komponenti ienākošiem elektroniskajiem dokumentiem

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
- Komponentu var atkārtoti serializēt no XML faila un importēt programmā kā jaunu ER komponenta versiju.

#### <a name="component-date-effectivity"></a>Komponenta spēkā stāšanās datums

ER komponentu versijas ir ar spēkā stāšanās datumu. ER komponentam varat iestatīt datumu **Spēkā no**, lai norādītu datumu, kad šis komponents stājas spēkā pārskatu veidošanas procesiem. Lai definētu, vai komponents ir derīgs izpildei, tiek izmantots programmas sesijas datums. Ja noteiktam datumam ir derīgas vairākas versijas, tad atskaišu veidošanas procesiem tiek izmantota jaunākā versija.

#### <a name="component-access"></a>Komponenta piekļuve

Piekļuve ER formāta komponentiem ir atkarīga no iestatījuma ISO valsts/reģiona kodam. Ja šis iestatījums atlasītajai formāta konfigurācijas versijai ir atstāts tukšs, formāta komponentam izpildes laikā var piekļūt no jebkura uzņēmuma. Ja šis iestatījums satur ISO valsts/reģiona kodus, formāta komponents ir pieejams tikai no uzņēmumiem, kuru primārā adrese ir definēta vienam no formāta komponenta ISO valsts/reģiona kodiem.

Datu formāta komponenta dažādām versijām var būt dažādi iestatījumi ISO valsts/reģiona kodiem.

#### <a name="configuration"></a><a name="Configuration"></a>Konfigurācija

ER konfigurācija ir konkrēta ER komponenta aplika. Šis komponents var būt datu modeļa komponents vai formāta komponents. Konfigurācija var ietvert kāda ER komponenta dažādās versijas. Katra konfigurācija tiek atzīmēta kā piederoša konkrētam konfigurācijas nodrošinātājam. Konfigurācijas komponenta versiju **Melnraksts** var rediģēt, ja šīs konfigurācijas īpašnieks programmas ER iestatījumos ir atlasīts kā aktīvs nodrošinātājs.

Katra modeļa konfigurācija ietver datu modeļa komponentu. No konkrētas datu modeļa konfigurācijas var atvasināt jaunu formāta konfigurāciju. Konfigurāciju kokā šī izveidotā formāta konfigurācija tiek rādīta kā sākotnējā datu modeļa konfigurācijas pakārtotais elements.

Izveidotā formāta konfigurācija ietver formāta komponentu. Sākotnējā modeļa konfigurācijas datu modeļa komponents automātiski tiek ievietots pakārtotā formāta konfigurācijas formāta komponentā kā noklusējuma datu avots.

ER konfigurācija tiek koplietota programmas uzņēmumiem.

#### <a name="provider"></a><a name="Provider"></a>Nodrošinātājs

ER nodrošinātājs ir puses identifikators, kas tiek izmantots, lai norādītu katras ER konfigurācijas autoru (īpašnieku). ER jums ļauj pārvaldīt konfigurāciju nodrošinātāju sarakstu. Formāta konfigurācijas, kas elektroniskajiem dokumentiem tiek izlaistas kā daļa no Finance and Operations risinājuma, ir atzīmētas kā **Microsoft** konfigurācijas nodrošinātājam piederošas.

Lai uzzinātu, kā reģistrēt jaunu ER nodrošinātāju, noskatieties uzdevuma ceļvedi **ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu** (daļa no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)** ).

#### <a name="repository"></a><a name="Repository"></a>Repozitorijs

ER repozitorijā glabājas ER konfigurācijas. Pašlaik tiek atbalstīti šādi ER repozitoriju tipi: 

- LCS koplietojamā bibliotēka
- LCS projekts
- Failu sistēma
- RCS
- Operations resursi
- Globālais repozitorijs

Repozitorijs **LCS koplietotā bibliotēka** nodrošina piekļuvi konfigurāciju sarakstam koplietojamo līdzekļu bibliotēkā pakalpojumā Lifecycle Services (LCS). Šāda veida ER repozitoriju var reģistrēt tikai Microsoft nodrošinātājam. No LCS koplietojamo līdzekļu bibliotēkas jaunākās ER konfigurāciju versijas var importēt pašreizējā instancē.

Repozitorijs **LCS projekts** nodrošina piekļuvi noteikta LCS projekta (LCS projekta līdzekļu bibliotēkas) konfigurāciju sarakstam, kurš tika atlasīts, kad repozitorijs tika reģistrēts. ER sniedz iespēju koplietotās konfigurācijas no pašreizējās instances augšupielādēt konkrētā repozitorijā **LCS projekts**. Konfigurācijas varat arī importēt no repozitorija **LCS projekts** pašreizējā jūsu Finance and Operations programmu instancē.

Repozitorijs **Failu sistēma** nodrošina piekļuvi konfigurāciju sarakstam, kuras atrodas kā xml faili noteiktā mapē tāda datora vietējā failu sistēmā, kurā tiek viesots AOS pakalpojums. Repozitorija reģistrācijas posmā ir atlasīta nepieciešamā mape. Konfigurācijas var arī importēt no repozitorija **Failu sistēma** pašreizējā instancē. 

Ņemiet vērā, ka šī veida repozitorijam var piekļūt tālāk norādītajās vidēs:

- Mākoņvides, kas izvietotas izstrādes nolūkos (satur pievienoto komplektu pārbaudes modeļus)
- Lokāli izvietotas vides

Papildinformāciju skatiet tēmā [Elektronisko pārskatu veidošanas (ER) konfigurāciju importēšana](./electronic-reporting-import-ger-configurations.md).

Repozitorijs **RCS** nodrošina piekļuvi noteiktas [Konfigurācijas pakalpojums (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) instances konfigurāciju sarakstam, kura tika atlasīta repozitorija reģistrācijas posmā. ER ļauj importēt pabeigtas vai koplietojamas konfigurācijas no atlasītās RCS instances pašreizējā instancē, lai tās varētu izmantot elektronisko pārskatu veidošanai.

Papildinformāciju skatiet tēmā [Elektronisko pārskatu veidošanas (ER) konfigurāciju no RCS importēšana](./rcs-download-configurations.md).

Repozitorijs **Globālais repozitorijs** nodrošina piekļuvi konfigurāciju sarakstam globālajā repozitorijā [Konfigurācijas pakalpojums](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Šāda veida ER repozitoriju var reģistrēt tikai Microsoft nodrošinātājam. No LCS globālā repozitorija jaunākās ER konfigurāciju versijas var importēt pašreizējā instancē.

Papildinformāciju skatiet tēmā [Importēt elektronisko pārskatu (ER) konfigurācijas no konfigurācijas pakalpojuma globālā repozitorija](./er-download-configurations-global-repo.md).

Repozitorijs **Operācijas resursi** nodrošina piekļuvi to konfigurāciju sarakstam, ko korporācija Microsoft kā ER konfigurāciju nodrošinātājs ir sākotnēji izlaidusi programmas risinājuma ietvaros. Šīs konfigurācijas var importēt pašreizējā instancē un izmantot elektronisko pārskatu veidošanai vai paraugu uzdevumu ceļvežu atskaņošanai. Tās var izmantot arī papildu lokalizācijām un pielāgojumiem. Ņemiet vērā, ka jaunākās versijas, ko nodrošina Microsoft ER konfigurācijas, ir jāimportē no LCS koplietojamo līdzekļu bibliotēkas, izmantojot attiecīgo ER repozitoriju.

Nepiec. repozitorijus **LCS projekts**, **Failu sistēma** un **Regulējošās konfigurācijas pakalpojumi (RCS)** var atsevišķi reģ. katram pašreizējās instances konfigurāciju nodrošinātājam. Katru repozitoriju var piešķirt noteiktam konfigurācijas nodrošinātājam.

## <a name="supported-scenarios"></a>Atbalstītie scenāriji

### <a name="building-a-data-model"></a>Datu modeļa veidošana

ER nodrošina modeļa veidotāju, kuru varat izmantot, lai izveidotu datu modeli noteiktam biznesa domēnam. Visus domēnam raksturīgos biznesa elementus un attiecības starp tiem varat norādīt datu modelī kā hierarhisku struktūru. 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku datu modeli** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="translating-data-model-content"></a>Datu modeļa satura tulkošana

Datu modeļa saturu (etiķetes un aprakstus) var tulkot citās programmas atbalstītajās valodās. Iespējams, datu modeļa saturu vēlaties tulkot tālāk uzskaitīto iemeslu dēļ.

- Izstrādes laikā, lai saturu padarītu saprotamāku formāta veidotājiem, kuri runā citās valodās un kuri datu modeli izmantos formāta komponentu datu kartēšanai.
- Izpildes laikā, lai saturu padarītu lietotājiem draudzīgāku, uzvednes un palīdzību izpildes laika parametriem, kā arī konfigurētus validēšanas ziņojumus (kļūdām un brīdinājumiem) rādot tādā valodā, kādai dod priekšroku programmatūrā lietotājs, kurš ir pieteicies pašlaik.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Datu modeļa kartējumu konfigurēšana izejošajiem dokumentiem

ER nodrošina modeļu kartēšanas veidotāju, kas lietotājiem savus izveidotos datu modeļus ļauj kartēt uz noteiktiem programmas datu avotiem. Pamatojoties uz kartējumu, izpildes laikā dati no atlasītajiem datu avotiem tiek importēti datu modelī. Pēc tam datu modelis tiek izmantots kā abstrakts datu avots ER formātiem, kas ģenerē izejošus elektroniskos dokumentus. 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevumu ceļvežus **ER Definēt modeļa kartēšanu un atlasīt datu avotus** un **ER Kartēt datu modeli uz atlasītajiem datu avotiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Datu modeļa kartējumu konfigurēšana ienākošiem dokumentiem

ER nodrošina modeļu kartēšanas veidotāju, kas lietotājiem savus izveidotos datu modeļus ļauj kartēt uz noteiktiem galamērķiem. Datu modeļus var kartēt, piemēram, uz atjaunināmiem datu komponentiem (tabulām, datu elementiem un skatiem). Pamatojoties uz kartējumu, dati izpildes laikā tiek atjaunināti, izmantojot datus no datu modeļa. Kā abstrakta ER formāta krātuve šis datu modelis tiek aizpildīts ar datiem, kas tiek importēti no ienākoša elektroniskā dokumenta. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Izveidotā modeļa komponenta kā modeļa konfigurācijas saglabāšana

ER var glabāt izstrādātu datu modeli, kopā ar saistītiem datu kartējumiem, kā pašreizējās instances modeļa konfigurāciju. Nākamajā attēlā ir parādīts šāda tipa datu modeļa konfigurācijas piemērs (maksājumu modeļa konfigurācija).

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Kartēt datu modeli uz atlasītajiem datu avotiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Tāda formāta veidošana, kas kā pamatu izmanto datu modeli

ER atbalsta formāta veidotāju, ko varat izmantot, lai veidotu elektroniskā dokumenta formātu kādam atlasītajam biznesa domēnam, kā pamatu atlasot modeļa komponentu. Tas pats ER formāta veidotājs jums ļauj izveidoto formātu kartēt uz atlasīto domēna datu modeļa kartēšanu kā datu avotu. 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku formātu** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigurācijas veidošana, lai ģenerētu elektroniskos dokumentus OPENXML darblapas formātā

ER formāta veidotāju var izmantot, lai veidotu elektronisko dokumentu OPENXML darblapas formātā. 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot konfigurāciju atskaitēm OPENXML formātā** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ). Kā daļu no veidnes importēšanas uzdevuma ceļveža kā veidni izmantojiet Excel failu [Maksājumu pārskata veidne (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Konfigurācijas veidošana, lai ģenerētu elektroniskos dokumentus Word dokumenta formātā

ER formāta veidotāju var izmantot, lai veidotu elektronisko dokumentu Word dokumenta formātā. Nākamajā attēlā ir parādīts šāda tipa formāta piemērs. Ņemiet vērā, ka šis formāts atkārtoti izmanto esošo ER konfigurāciju, kas sākotnēji bija veidota tā, lai pārskata izvadi ģenerētu OPENXML formātā.

Lai iepazītos ar detalizētu informāciju par šo scenāriju, noskatieties uzdevuma ceļvedi ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā Microsoft WORD (daļa no biznesa procesa 7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)). Kā daļu no šī uzdevumu ceļveža darbības veidnes importēšanai kā veidnes ER formātam izmantojiet tālāk norādītos Word failus.

- [Maksājumu pārskata veidne (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Maksājumu pārskata saistītā veidne (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Konfigurācijas veidošana datu importēšanai no ienākošiem elektroniskajiem dokumentiem

ER formāta veidotāju var izmantot, lai aprakstītu elektronisku dokumentu, kurš tiek plānots datu importēšanai XML vai teksta formātā. Izveidotais formāts tiek lietots, lai parsētu ienākošu dokumentu. ER formāta kartējuma veidotāju var izmantot, lai definētu izveidotā formāta elementu saistīšanu ar datu modeli. 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, noskatieties uzdevuma ceļvedi Izveidot nepieciešamās ER konfigurācijas, lai importētu datus no ārēja faila (daļa no biznesa procesa 7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)). Lai izpildītu šo ceļvedi, izmantot tālāk norādītos failus.

- [ER datu modeļa konfigurācija (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER formāta konfigurācija (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [XML formātā ienākoša dokumenta piemērs (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Darbgrāmatas piemērs ienākoša dokumenta datu pārvaldīšanai (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Izveidotā formāta komponenta glabāšana formāta konfigurācijā

ER var glabāt izstrādātu formātu kopā ar konfigurētajiem datu kartējumiem kā pašreizējās instances formāta konfigurāciju. Iepriekšējā attēlā ir parādīts šāda tipa formāta konfigurācijas piemērs (**BACS (UK)**, kas ir konfigurācijas **Maksājumu modelis** pakārtotais elements). Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku formātu** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Finance konfigurēšana izveidota formāta iekšējai lietošanai

Programma var konfigurēt, lai izveidotu formātu sāktu lietot elektronisko atskaišu ģenerēšanai. Atsauce uz izveidoto formāta konfigurāciju ir jādefinē noteikta domēna iestatījumos. Piemēram, lai elektroniskiem kreditoru maksājumiem BACS formātā sāktu izmantot ER formāta konfigurāciju, noteiktās maksāšanas metodēs ir jāietver atsauce uz šo formāta konfigurāciju.

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Lietot formātu, lai ģenerētu elektroniskus dokumentus maksājumiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

## <a name="handling-er-components"></a>Darbs ar ER komponentiem

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponenta publicēšana pakalpojumos LCS, lai to piedāvātu ārēji (lokalizācija)

Izveidota komponenta (modeļa vai formāta) īpašnieks var izmantot ER, lai komponenta pabeigto versiju publicētu pakalpojumos LCS. Pašreizējās ER konfigurācijas nodrošinātājam ir nepieciešams repozitorijs ar tipu **LCS projekts**. Kad komponenta pabeigtas versijas statuss no **PABEIGTS** tiek mainīts uz **KOPLIETOTS**, šī versija tiek publicēta pakalpojumos LCS. Kad komponents ir publicēts pakalpojumos LCS, šī komponenta īpašnieks kļūst par pakalpojuma nodrošinātāju, lai atbalstītu šo komponentu. Piemēram, ja formāta komponents ir paredzēts, lai ģenerētu elektronisku dokumentu, kurš ir juridiski nepieciešams (piemēram, saskaņā ar kādu lokalizācijas scenāriju), tad tiek pieņemts, ka šis formāts saglabāsies atbilstošs likumdošanas izmaiņām un ka tā nodrošinātājs izdos šī komponenta jaunās versijas katru reizi, kad radīsies jaunas likumdošanas prasības. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponenta importēšana no LCS iekšējai izmantošanai

ER jums ļauj importēt ER komponentus no LCS uz pašreizējo instanci. Ir nepieciešams repozitorijs ar tipu **LCS projekts**. Kad ER komponents no LCS ir importēts pašreizējā instancē, šīs instances īpašnieks kļūst par importētā komponenta īpašnieka (autora) nodrošinātā pakalpojuma patērētāju. Piemēram, ja kāds formāta komponents ir izstrādāts, lai ģenerētu noteiktu elektronisko dokumentu no programmas kādas valsts/reģiona specifiskā formātā (lokalizācijas scenārijs), tiek pieņemts, ka šī pakalpojuma patērētājs varēs iegūt visus šim formātam veiktos atjauninājumus, lai saglabātu atbilstību likumdošanas prasībām. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Importēt konfigurāciju no Lifecycle Services** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formāta veidošana, atlasot citu formātu kā pamatu (pielāgošana)

ER jums ļauj izveidot (atvasināt) jaunu komponentu no komponenta pašreizējās versijas (bāzes), kas tika importēta no LCS. Piemēram, lietotājs vēlas atvasināt jaunu formātu, lai ieviestu kaut kādas īpašas elektroniskā dokumenta prasības (piemēram, papildu lauku vai izsmeļošu aprakstu) un atbalstītu pielāgošanas scenāriju. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Jaunināt formātu, pieņemot tam jaunu pamata versiju** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)** ).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formāta atjaunināšana, atlasot jaunu pamata formāta versiju (pārskatīt)

ER jums ļauj atvasinātā komponenta pašreizējā melnraksta versijā automātiski pieņemt pamata komponenta jaunākajā versijā veiktās izmaiņas. Šis process tiek saukts par *pārbāzēšanu*. Piemēram, no LCS importētā formāta jaunākajā versijā ieviestās jaunās normatīvās izmaiņas var automātiski sapludināt elektroniskā dokumenta šī formāta pielāgotajā versijā. Visas izmaiņas, kuras nevar sapludināt automātiski, tiek uzskatītas par konfliktiem. Šie konflikti tiek parādīti manuālai atrisināšanai atbilstošā komponenta veidotāja rīkā. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER formāta jaunināšana, ieviešot šī formāta jauno bāzes versiju** (daļa no biznesa procesa **7.5.5.3. Izmainīta IT pakalpojumu/risinājumu komponenta iegāde/izstrāde (10683)** ).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Finance izlaisto ER konfigurāciju saraksts

ER konfigurāciju saraksts programmai Finance tiek pastāvīgi atjaunināts. Atveriet [Globālo repozitoriju](er-download-configurations-global-repo.md), lai pārskatītu pašreiz atbalstīto ER konfigurāciju sarakstu. Kopsavilkuma cilnē **Detalizēta informācija par pārtraukšanu** varat pārskatīt informāciju par konfigurācijām, kuras ir pārtrauktas vai kuras vairs netiek uzturētas. 

![Globālā repozitorija satura filtrēšana Konfigurācijas repozitorija lapā](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) konfigurāciju izveide](electronic-reporting-configuration.md)
- [Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
