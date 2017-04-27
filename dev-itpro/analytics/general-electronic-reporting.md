---
title: "Elektronisko atskaišu veidošanas pārskats"
description: "Šajā rakstā ir sniegts elektronisko atskaišu veidošanas (ER) rīka pārskats. Tajā ir ietverta informācija par galvenajiem jēdzieniem, ER atbalstītajiem scenārijiem, kā arī saraksts ar formātiem, kas ir izstrādāti un izlaisti kā daļa no šī risinājuma."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: b3e8174d07c9b9fd4210486c369c640fe07c49eb
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-overview"></a>Elektronisko atskaišu veidošanas pārskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts elektronisko atskaišu veidošanas (ER) rīka pārskats. Tajā ir ietverta informācija par galvenajiem jēdzieniem, ER atbalstītajiem scenārijiem, kā arī saraksts ar formātiem, kas ir izstrādāti un izlaisti kā daļa no šī risinājuma.

Elektronisko atskaišu veidošana (Electronic Reporting —ER) ir rīks, kuru varat izmantot, lai konfigurētu elektronisko dokumentu formātus saskaņā ar dažādu valstu/reģionu tiesiskajām prasībām. ER jums ļauj pārvaldīt šos formātus to lietošanas cikla laikā. Piemēram, varat pieņemt jaunas normatīvās prasības un varat ģenerēt biznesa dokumentus nepieciešamajā formātā, lai elektroniski apmainītos ar informāciju ar valsts institūcijām, bankām un citām pusēm. ER programma ir vērsta uz biznesa lietotājiem, nevis izstrādātājiem. Tā kā jūs konfigurējat formātus, nevis kodu, tad elektronisko dokumentu formātu izveidošanas un pielāgošanas process ir ātrāks un ērtāks. Pašlaik ER atbalsta darblapu formātus TEXT, XML un OPENXML. Taču paplašinājumu interfeiss sniedz atbalstu lielākam formātu skaitam.

## <a name="capabilities"></a>Spējas
ER programmai ir šādas iespējas:

-   Tā nodrošina vienu kopēju rīku elektronisko pārskatu izveidei dažādos domēnos un aizstāj vairāk nekā 20 dažādas programmas, kas nodrošina noteiktas veida elektronisko pārskatu izveides funkcijas programmatūrā Microsoft Dynamics 365 for Operations.
-   Tā nodrošina no pašreizējās Dynamics 365 for Operations implementācijas neatkarīgu pārskata formātu. (Tas nozīmē, ka formātu var lietot dažādās Dynamics 365 for Operations versijās.)
-   Tā atbalsta pielāgota formāta izveidošanu, balstoties uz sākotnējo formātu. Tā ietver iespējas automātiskai pielāgotā formāta jaunināšanai, ja notiek sākotnējā formāta izmaiņas, jo ir ieviestas kādas lokalizācijas/pielāgošanas prasības.
-   Tas kļūst par primāro standarta rīku lokalizācijas prasību atbalstam elektronisko atskaišu izveidē — gan korporācijai Microsoft, gan Microsoft partneriem.
-   Tā atbalsta iespēju sadalīt formātus partneriem un klientiem, izmantojot Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Koncepcijas
### <a name="components"></a>Komponenti

ER atbalsta divus komponentu tipus: **Datu modelis **un **Formāts**.

#### <a name="data-model-components"></a>Datu modeļa komponenti

Datu modeļa komponents ir abstrakts datu struktūras atspoguļojums, un tas tiek lietots, lai aprakstītu noteikta biznesa domēna apgabalu ar pietiekamu detalizāciju, lai apmierinātu atskaišu izveides prasības šajā domēnā. Datu modeļa komponents sastāv no šādām daļām:

-   Datu modelis kā domēnam raksturīgo biznesa elementu kopu, un hierarhiski strukturēta šo elementu attiecību definīcija
-   Modeļa kartēšana, kas nodrošina atlasīto Dynamics 365 for Operations datu avotu saistīšanu ar atsevišķiem datu modeļa elementiem, kuri izpildes laikā norāda datu plūsmu un kārtulas datu modeļa komponenta aizpildīšanai ar biznesa datiem.

Datu modeļa biznesa elements tiek attēlots kā konteiners (ieraksts). Biznesa vienuma rekvizīti tiek attēloti kā datu elementi (lauki). Katram datu vienumam ir unikāls nosaukums, etiķete, apraksts un vērtība. Katra datu vienuma vērtība var būt izveidota tā, lai tā tiktu atpazīta kā virkne, vesels skaitlis, reāls, datums, uzskaitījuma tips, Būla vērtība un citi datu veidi. Turklāt tā var būt cits ieraksts kādā ierakstu sarakstā. Viens datu modeļa komponents var saturēt vairākas domēnam raksturīgo biznesa elementu hierarhijas, kā arī modeļa kartējumus, kas izpildes laikā atbalsta konkrētu atskaitei raksturīgu datu plūsmu. Hierarhijas tiek atšķirtas pēc viena ieraksta, kas tika atlasīts kā modeļa kartēšanas sakne. Piemēram, maksājumu domēna apgabala datu modelis varētu atbalstīt šādus kartējumus:

-   Uzņēmums -&gt; kreditors -&gt; parādu kreditoriem domēna maksājumu transakcijas
-   Debitors -&gt; uzņēmums -&gt; debitoru parādu domēna maksājumu transakcijas

Ņemiet vērā, ka biznesa elementi (piemēram, uzņēmums un maksājumu transakcijas) tiek izveidoti vienreiz. Pēc tam dažādi kartējumi tos lieto atkārtoti. Modeļa kartēšanai ir šādas iespējas:

-   Kā datu modeļa datu avotus var izmantot dažādus Dynamics 365 for Operations datu tipus. Piemēram, tā var izmantot tabulas, datu elementus, metodes vai uzskaitījumus.
-   Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.
-   Tā atbalsta Dynamics 365 for Operations datu pārveidošanu par nepieciešamajām grupām, datu filtrēšanu, kārtošanu un summēšanu, kā arī papildināšanu ar loģiski aprēķinātajiem laukiem, kas ir izveidoti, izmantojot Microsoft Excel tipa formulas (papildinformāciju skatiet tēmā [Formulas veidotājs modulī Elektroniskie pārskati](general-electronic-reporting-formula-designer.md)).

[![Excel tipa formulu redaktors](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Katram biznesa domēnam tiek izstrādāts datu modeļa komponents, kas ir jāizmanto kā vienots pārskatu izveides datu avots, tādējādi nošķirot pārskatu izveidi no Dynamics 365 for Operations datu avotu fiziskās implementācijas un atveidojot domēnam raksturīgās biznesa koncepcijas un funkcijas tādā veidā, kas padara pārskata formāta sākotnējo noformēšanu un turpmāko uzturēšanu efektīvāku.

#### <a name="format-components"></a>Formāta komponenti

Formāta komponents ir atskaišu veidošanas izvades shēma, kas tiks ģenerēta izpildes laikā. Shēma sastāv no šādiem elementiem:

-   Formāts, kas nosaka izpildes laikā ģenerētā elektronisko atskaišu dokumenta struktūru un saturu
-   Datu avoti kā lietotāja ievades parametru kopa un domēnam specifisku datu modelis, kas izmanto atlasīto modeļa kartēšanu
-   Formāta kartēšana kā formāta datu avotu saistījumu kopa, kuriem ir atsevišķi formāta elementi, kas izpildes laikā norāda datu plūsmu un kārtulas formāta izvades ģenerēšanai
-   Formāta validācija kā konfigurējamu kārtulu kopa, kas kontrolē atskaites ģenerēšanu izpildes laikā atkarībā no izpildes konteksta (piemēram, kārtula, kas aptur kreditoru maksājumu izvades ģenerēšanu un parāda izņēmumu, ja atlasītajam kreditoram trūkst noteiktu atribūtu, piemēram, bankas konta numura).

Formāta komponents atbalsta tālāk aprakstītās funkcijas.

-   Atskaišu izvades kā atsevišķu failu izveidošanu dažādos formātos: kā tekstu, XML vai darblapu
-   Vairākus failu izveidošanu atsevišķi, kā arī šo failu iekapsulēšanu zip failos

Formāta komponents nodrošina iespēju pievienot noteiktus failus, kurus var izmantot atskaišu izvadē tālāk aprakstītajos veidos.

-   Excel darbgrāmatas, kas ietver darblapu, kuru var izmantot kā veidni izvadei OPENXML darblapas formātā
-   Citi faili, kurus var iekļaut formāta izvadē kā iepriekš definētus failus

#### <a name="component-versioning"></a>Komponenta versiju izveide

ER komponentiem tiek atbalstīta versiju izveide. ER komponentu izmaiņu pārvaldīšanai tiek sniegtas tālāk aprakstītā darbplūsma.

-   Sākotnēji izveidotā versija tiek atzīmēta kā versija **MELNRAKSTS**. Šo versiju var rediģēt, un tā ir pieejama testu izpildīšanai.
-   Versiju** MELNRAKSTS** var pārveidot par versiju **PABEIGTS**. Šo versiju var izmantot vietējos atskaišu procesos.
-   Versiju **PABEIGTS** var pārveidot par versiju **KOPLIETOTS**. Šī versija tiek publicēta LCS, un to var izmantot globālos pārskatu izveides procesos.
-   Versiju **KOPLIETOTS **var pārveidot par versiju **PĀRTRAUKTS**. Pēc tam šo versiju var dzēst.

Versijas, kuru statuss ir ** PABEIGTS** vai **KOPLIETOTS**, var izmantot citu datu apmaiņai. Komponentam, kam ir šie statusi, var izpildīt tālāk uzskaitītās darbības.

-   Tos var serializēt XML formātā un eksportēt no programmatūras Dynamics 365 for Operations kā XML formāta failu.
-   Tos var atkārtoti serializēt no XML faila un importēt programmatūrā Dynamics 365 for Operations kā jaunu ER komponenta versiju.

#### <a name="component-date-effectivity"></a>Komponenta spēkā stāšanās datums

ER komponentu versijas ir ar spēkā stāšanās datumu. ER komponentam var definēt datumu** Spēkā no**, lai norādītu datumu, kad šis komponents stājas spēkā atskaišu veidošanas procesiem. Dynamics 365 for Operations sesijas datums tiek izmantots, lai noteiktu, vai komponents ir derīgs izpildei. Ja noteiktam datumam ir derīgas vairākas versijas, tad atskaišu veidošanas procesiem tiek izmantota jaunākā versija.

#### <a name="component-access"></a>Komponenta piekļuve

Piekļuve ER formāta komponentiem ir atkarīga no iestatījuma ISO valsts/reģiona kodam. Ja šis iestatījums atlasītajai formāta konfigurācijas versijai ir atstāts tukšs, šim formāta komponentam izpildes laikā var piekļūt no jebkura Dynamics 365 for Operations uzņēmuma. Ja šajā iestatījumā ir norādīti ISO valsts/reģiona kodi, formāta komponentam var piekļūt tikai no Dynamics 365 for Operations uzņēmumiem, kuru primārā adrese ir norādīta vienam no formāta komponenta ISO valsts/reģiona kodiem. Datu formāta komponenta dažādām versijām var būt dažādi iestatījumi ISO valsts/reģiona kodiem.

#### <a name="configuration"></a>Konfigurācija

ER konfigurācija ir aplika noteiktam ER komponentam — **Datu modelis **vai **Formāts**. Konfigurācija var ietvert noteikta ER komponenta dažādās versijas. Katra konfigurācija tiek atzīmēta kā piederoša noteiktam konfigurācijas nodrošinātājam. Konfigurācijas komponenta versiju **MELNRAKSTS** var rediģēt, ja šīs konfigurācijas īpašnieks Dynamics 365 for Operations ER iestatījumos ir atlasīts kā aktīvs nodrošinātājs. Katra modeļa konfigurācija satur komponentu **Datu modelis**. Jaunu formāta konfigurāciju var izveidot (atvasināt) no konkrētas datu modeļa konfigurācijas. Izveidotā formāta konfigurācija konfigurāciju kokā tiek rādīta kā sākotnējā datu modeļa konfigurācijas pakārtotais elements. Izveidotā formāta konfigurācija ietver komponentu **Formāts**. Sākotnējā modeļa konfigurācijas komponents **Datu modelis** automātiski tiek ievietots pakārtotā formāta konfigurācijas komponentā **Formāts** kā noklusējuma datu avots. ER konfigurācija tiek koplietota Dynamics 365 for Operations uzņēmumiem.

#### <a name="provider"></a>Piegādātājs

ER nodrošinātājs ir puses identifikators, kas tiek izmantots, lai norādītu katras ER konfigurācijas autoru (īpašnieku). ER jums ļauj pārvaldīt konfigurāciju nodrošinātāju sarakstu. Formāta konfigurācijas, kas ir izlaistas elektroniskajiem dokumentiem Dynamics 365 for Operations risinājuma ietvaros, ir atzīmētas kā piederošas **Microsoft** konfigurācijas nodrošinātājam.

#### <a name="repository"></a>Repozitorijs

ER repozitorijā glabājas ER konfigurācijas. Pašlaik tiek atbalstīti šādi ER repozitoriju veidi: **Operāciju resursi** un **LCS projekts**. Veida **Operāciju resursi** repozitorijs nodrošina piekļuvi to konfigurāciju sarakstam, ko korporācija Microsoft kā ER konfigurāciju nodrošinātājs ir izlaidusi Dynamics 365 for Operations risinājuma ietvaros. Šīs konfigurācijas var importēt pašreizējā Dynamics 365 for Operations instancē un izmantot elektronisko pārskatu veidošanai. Tās var izmantot arī papildu lokalizācijām/pielāgojumiem. Repozitorijs **LCS projekts **nodrošina piekļuvi noteikta LCS projekta (LCS projekta līdzekļu bibliotēkas) konfigurāciju sarakstam, kurš tika atlasīts repozitorija reģistrācijas posmā. Modulis ER sniedz iespēju augšupielādēt koplietotās konfigurācijas no pašreizējās Dynamics 365 for Operations instances konkrētā veida **LCS projekts** repozitorijā. Varat arī importēt konfigurācijas no konkrēta veida **LCS projekts** repozitorija pašreizējā Dynamics 365 for Operations instancē. Nepieciešamos veida **LCS projekts** repozitorijus var atsevišķi reģistrēt katram pašreizējās Dynamics 365 for Operations instances konfigurāciju nodrošinātājam. Katru repozitoriju var piešķirt noteiktam konfigurācijas nodrošinātājam.

## <a name="supported-scenarios"></a>Atbalstītie scenāriji
### <a name="building-a-data-model"></a>Datu modeļa veidošana

ER nodrošina modeļa veidotāju, kuru varat izmantot, lai izveidotu datu modeli noteiktam biznesa domēnam. Visus domēnam raksturīgos biznesa elementus un attiecības starp tiem varat norādīt datu modelī kā hierarhisku struktūru. Nākamajā attēlā ir parādīts šāda tipa datu modeļa piemērs (maksājumu domēna datu modelis). [![Datu modeļa piemērs](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Lai iepazītu šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER domēnam specifiska datu modeļa izveide** (daļa no biznesa procesa **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**).

### <a name="translating-data-model-content"></a>Datu modeļa satura tulkošana

Datu modeļa saturu (etiķetes un aprakstus) var tulkot citās programmatūrā Dynamics s 365 for Operations atbalstītajās valodās. Iespējams, datu modeļa saturu vēlaties tulkot tālāk uzskaitīto iemeslu dēļ.

-   Izstrādes laikā, lai saturu padarītu saprotamāku formāta veidotājiem, kuri runā citā valodā un kuri datu modeli izmantos formāta komponentu datu kartēšanai
-   Izpildes laikā — lai padarītu saturu vieglāk lietojamu, nodrošinot izpildes laikā lietoto parametru palīdzības materiālus un uzvednes, kā arī konfigurētos validācijas ziņojumus (kļūdu un brīdinājuma ziņojumus) rādīšanu valodā, ko ir izvēlējies lietotājs, kurš pašlaik ir pieteicies programmatūrā Dynamics 365 for Operations.

Nākamajā attēlā ir parādīts piemērs tam, kā datu modeļa saturu no angļu valodas var tulkot japāņu valodā. [![Datu modeļa saturs angļu valodā](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Japāņu valodā tulkots datu modeļa saturs](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Datu modeļa kartējumu konfigurēšana

Modulis ER nodrošina modeļa kartēšanas veidotāju, kas sniedz lietotājiem iespēju kartēt savus izstrādātos datu modeļus ar noteiktiem Dynamics 365 for Operations datu avotiem. Nākamajā attēlā ir parādīts šī tipa datu modeļa kartējuma piemērs (maksājumu domēna datu modeļa kartējums **SEPA kredīta pārskaitījums**). [![Datu modeļa kartēšanas piemērs ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Lai iepazītu šo scenāriju, atskaņojiet uzdevumu ceļvežus **ER modeļa kartēšanas definēšana un datu avotu atlasīšana** un **ER datu modeļa kartēšana ar atlasītajiem datu avotiem** (daļa no biznesa procesa **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Izveidotā modeļa komponenta kā modeļa konfigurācijas saglabāšana

Modulī ER izstrādātu datu modeli var saglabāt kopā ar saistītajiem datu kartējumiem kā pašreizējās Dynamics 365 for Operations instances modeļa konfigurāciju. Nākamajā attēlā ir parādīts šāda tipa datu modeļa konfigurācijas piemērs (maksājumu modeļa konfigurācija). [![Datu modeļa konfigurācijas piemērs ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Lai iepazītu šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER datu modeļa kartēšana ar izvēlētajiem datu avotiem** (daļa no biznesa procesa **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Tāda formāta veidošana, kas kā pamatu izmanto datu modeli

ER atbalsta formāta veidotāju, ko varat izmantot, lai izveidotu konkrēta elektroniskā dokumenta formātu atlasītajam biznesa domēnam, kā pamatu atlasot modeļa komponentu. Tas pats ER formāta veidotājs jums ļauj izveidoto formātu kartēt uz atlasīto domēna datu modeļa kartēšanu kā datu avotu. Nākamajā attēlā ir parādīts šāda tipa formāta piemērs (formāta konfigurācija, kas nodrošina **BACS** maksājuma formātu Apvienotajai Karalistei). [![Tāda formāta piemērs, kas ir izveidots, pamatojoties uz datu modeli](./media/pic-format-1024x690.png)](./media/pic-format.png) Lai iepazītu šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER domēnam specifiska formāta izveide** (daļa no biznesa procesa **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigurācijas veidošana, lai ģenerētu elektroniskos dokumentus OPENXML darblapas formātā

ER formāta veidotāju var izmantot, lai veidotu īpašu elektronisko dokumentu OPENXML darblapas formātā. Tālāk esošajā attēlā ir redzams šī formāta veida piemērs (formāta konfigurācija, lai ģenerētu OPENXML darblapu ar informāciju par atlasītu maksājumu žurnāla):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Lai iepazītu šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER konfigurācijas izveide pārskatiem OPENXML formātā** (daļa no biznesa procesa **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**). Izmantojiet tālāk norādīto Excel failu kā veidni ER formāta izstrādei, lai izpildītu šī uzdevuma ceļveža formāta veidnes importēšanas darbību: [Maksājumu pārskata veidne (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Izveidotā formāta komponenta glabāšana formāta konfigurācijā

Modulī ER izstrādātu formātu var saglabāt kopā ar konfigurētajiem datu kartējumiem kā pašreizējās Dynamics 365 for Operations instances formāta konfigurāciju. Iepriekšējā attēlā ir parādīts šāda tipa formāta konfigurācijas piemērs (**BACS (UK)**, kas ir konfigurācijas **Maksājumu modelis **pakārtotais elements). Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Izveidot domēnam specifisku formātu** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Dynamics 365 for Operations konfigurēšana izveidota formāta iekšējai lietošanai

Programmatūru Dynamics 365 for Operations var konfigurēt tā, lai elektronisko pārskatu ģenerēšanai sāktu izmantot izveidotu formātu. Atsauce uz izveidoto formāta konfigurāciju ir jādefinē noteikta domēna iestatījumos. Piemēram, lai elektroniskiem kreditoru maksājumiem BACS formātā sāktu izmantot ER formāta konfigurāciju, noteiktās maksāšanas metodēs ir jāietver atsauce uz šo formāta konfigurāciju, kā tas ir redzams tālāk esošajos attēlos. 

[![Formāta BACS (UK) konfigurācija](media/ger-bacs-uk-format-configuration.png) 

[![Atsauces uz formātu BACS (UK) ietveršana maksāšanas metodē](media/ger-bacs-uk-format-method.png) 

Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Lietot formātu, lai ģenerētu elektroniskus dokumentus maksājumiem** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

## <a name="handling-er-components"></a>Darbs ar ER komponentiem
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponenta publicēšana pakalpojumos LCS, lai to piedāvātu ārēji (lokalizācija)

Izveidota komponenta (modeļa vai formāta) īpašnieks var izmantot ER, lai komponenta pabeigto versiju publicētu pakalpojumos LCS. Pašreizējās ER konfigurācijas nodrošinātājam ir nepieciešams repozitorijs ar tipu **LCS projekts**. Kad komponenta pabeigtas versijas statuss no **PABEIGTS** tiek mainīts uz **KOPLIETOTS**, šī versija tiek publicēta pakalpojumos LCS. Kad komponents ir publicēts pakalpojumos LCS, šī komponenta īpašnieks kļūst par pakalpojuma nodrošinātāju, lai atbalstītu šo komponentu. Piemēram, ja formāta komponents ir paredzēts, lai ģenerētu elektronisku dokumentu, kurš ir juridiski nepieciešams (piemēram, saskaņā ar kādu lokalizācijas scenāriju), tad tiek pieņemts, ka šis formāts saglabāsies atbilstošs likumdošanas izmaiņām un ka tā nodrošinātājs izdos šī komponenta jaunās versijas katru reizi, kad radīsies jaunas likumdošanas prasības. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services **(daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponenta importēšana no LCS iekšējai izmantošanai

Modulis ER sniedz iespēju importēt ER komponentus no LCS pašreizējā Dynamics 365 for Operations instancē. Ir nepieciešams repozitorijs ar tipu **LCS projekts**. Kad ER komponents ir importēts no LCS pašreizējā Dynamics 365 for Operations instancē, šīs instances īpašnieks kļūst par importētā komponenta īpašnieka (autora) nodrošinātā pakalpojuma patērētāju. Piemēram, ja ir izstrādāts formāta komponents noteikta elektroniskā dokumenta ģenerēšanai no programmatūras Dynamics 365 for Operations valstij/reģionam raksturīgā formātā (lokalizācijas scenārijs), tiek pieņemts, ka pakalpojuma patērētājs varēs iegūt visus šim formātam veiktos atjauninājumus, lai nodrošinātu tā atbilstību likumdošanas prasībām. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Importēt konfigurāciju no Lifecycle Services** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formāta veidošana, atlasot citu formātu kā pamatu (pielāgošana)

ER jums ļauj izveidot (atvasināt) jaunu komponentu no komponenta pašreizējās versijas (bāzes), kas tika importēta no LCS. Piemēram, lietotājs vēlas atvasināt jaunu formātu, lai ieviestu kaut kādas īpašas elektroniskā dokumenta prasības (piemēram, papildu lauku vai izsmeļošu aprakstu) un atbalstītu pielāgošanas scenāriju. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Jaunināt formātu, pieņemot tam jaunu pamata versiju** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formāta atjaunināšana, atlasot jaunu pamata formāta versiju (pārskatīt)

ER jums ļauj atvasinātā komponenta pašreizējā melnraksta versijā automātiski pieņemt pamata komponenta jaunākajā versijā veiktās izmaiņas. Šis process tiek saukts par *pārbāzēšanu*. Piemēram, no LCS importētā formāta jaunākajā versijā ieviestās jaunās normatīvās izmaiņas var automātiski sapludināt elektroniskā dokumenta šī formāta pielāgotajā versijā. Visas izmaiņas, kuras nevar sapludināt automātiski, tiek uzskatītas par konfliktiem. Šie konflikti tiek parādīti manuālai atrisināšanai atbilstošā komponenta veidotāja rīkā. Lai iepazītos ar detalizētu informāciju par šo scenāriju, atskaņojiet uzdevuma ceļvedi **ER Jaunināt formātu, pieņemot tam jaunu pamata versiju** (daļa no biznesa procesa **7.5.4.3. Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus (10677)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Dynamics 365 for Operations risinājumā ietverto ER konfigurāciju saraksts
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




