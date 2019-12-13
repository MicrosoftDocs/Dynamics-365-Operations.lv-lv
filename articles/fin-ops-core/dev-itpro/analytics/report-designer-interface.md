---
title: Pārskatu veidotāja saskarne
description: Šajā rakstā ir paskaidrots, kā pārvietoties atskaišu veidotājā un kā izmantot dažādās opcijas, lai izpildītu jūsu konkrētās prasības.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8c4118565ba65700e2073e2f981caf80fa738d94
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772515"
---
# <a name="report-designer-interface"></a>Pārskatu veidotāja saskarne

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā pārvietoties atskaišu veidotājā un kā izmantot dažādās opcijas, lai izpildītu jūsu konkrētās prasības.

## <a name="report-designer-menu-commands"></a>Pārskatu veidotāja izvēlnes komandas

Nākamajās tabulās ir aprakstītas izvēlnes komandas un opcijas, kuras varat izmantot, veidojot finanšu atskaites. Dažas izvēlnes komandas un opcijas ir pieejamas tikai īpašos apstākļos. Piemēram, pārskatu vienību paaugstināšanas un pazemināšanas komandas ir pieejamas tikai tad, kad tiek modificēta pārskatu koka definīcija.

### <a name="file-menu"></a>Izvēlne Fails

Izvēlne **Fails** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda                           | Apraksts |
|-----------------------------------|-------------|
| Jauna                               | Izveidot jaunu pārskata definīciju, rindas definīciju, kolonnas definīciju, pārskata koka definīciju, pārskata grupas definīciju vai mapi. Atkarībā no jūsu lietotāja lomas ir pieejamas papildu opcijas. |
| Atvērta                              | Atvērt eksistējošu rindas definīciju, kolonnas definīciju, pārskata koka definīciju vai pārskata definīciju. |
| Aizvērt                             | Tiek aizvērts pašreizējais veidošanas bloks. |
| Aizvērt visu                         | Tiek aizvērti visi veidošanas bloki. |
| Saglabāt                              | Tiek saglabāta pašreizējā rindas, kolonnas, pārskatu koka vai pārskata definīcija. |
| Saglabāšana kā                           | Tiek saglabāta pašreizējā rindas definīcija, kolonnas definīcija, pārskatu koka definīcija vai pārskata definīcija, piešķirot jaunu nosaukumu. |
| Rekvizīti                        | Atvērt dialoglodziņu **Rekvizīti**, kur varat mainīt pārskata nosaukumu un aprakstu. |
| Ģenerēt                          | Tiek ģenerēts pašreizējais pārskats. Šī komanda ir pieejama pārskata definīcijā. |
| Skatīt pārskatu                       | Atvērt ģenerētās atskaites jaunāko versiju. Šī komanda ir pieejama no pārskata definīcijas, ja esat ģenerējis vismaz vienu pārskatu. |
| Nesenās pārskatu definīcijas         | Tiek atvērts nesen izveidoto vai modificēto pārskatu saraksts. Pēc tam varat atlasīt sarakstā pārskatu. |
| Nesenās rindu definīcijas            | Tiek atvērts nesen izveidoto vai modificēto rindu definīciju saraksts. Pēc tam varat atlasīt sarakstā rindas definīciju. |
| Nesenās kolonnu definīcijas         | Tiek atvērts nesen izveidoto vai modificēto kolonnu definīciju saraksts. Pēc tam varat atlasīt sarakstā kolonnas definīciju. |
| Nesenās pārskatu koka definīcijas | Tiek atvērts nesen izveidoto vai modificēto pārskatu koka definīciju saraksts. Pēc tam varat atlasīt sarakstā pārskatu koka definīciju. |
| Iziet                              | Tiek aizvērts pārskatu veidotājs. |

### <a name="edit-menu"></a>Izvēlne Rediģēt

Izvēlne **Rediģēt** ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. Šajā izvēlnē ir tālāk aprakstītās komandas.

| Komanda                                | Apraksts |
|----------------------------------------|-------------|
| Atsaukt                                   | Pēdējā darbība tiek atsaukta. |
| Atcelt atsaukšanu                                   | Pēdējā atsaukšanas darbība tiek atcelta. |
| Izgriezt                                    | Atlasītais teksts tiek dzēsts un kopēts starpliktuvē. |
| Kopēt                                   | Atlasītais teksts tiek kopēts starpliktuvē. |
| Ielīmēt                                  | No starpliktuves tiek ievietots pēdējais izgrieztais vai kopētais teksts. |
| Notīrīt                                  | Tiek dzēsts atlasītās veidošanas bloka šūnas saturs. |
| Atrast                                   | Atvērt dialoglodziņu **Meklēt un aizvietot**, kur varat meklēt tekstu skata rūtī. |
| Aizstāt                                | Atvērt dialoglodziņu **Meklēt un aizvietot**, kur varat meklēt un aizvietot tekstu skata rūtī. |
| Ievietot rindas no dimensijām            | Atvērt dialoglodziņu **Ievietot rindas no dimensijām**, kurā varat atlasīt dimensijas vērtības, kuras vēlaties iekļaut rindas definīcijā. Šī komanda ir pieejama rindas definīcijā. |
| Pārnumurēt rindas                          | Visi rindas kodi, kas satur ciparus, tiek pārnumurēti. Šī komanda ir pieejama rindas definīcijā. |
| Rindas saites                              | Atvērt dialoglodziņu **Rindu saites**, kur varat norādīt datu saišu avotus rindas definīcijām un pārskata koku definīcijām. Šī komanda ir pieejama rindas definīcijā. |
| Noapaļošanas korekcija                    | Atvērt dialoglodziņu **Noapaļošanas korekcijas**, kur varat norādīt noapaļošanas parametrus. Šī komanda ir pieejama rindas definīcijā. |
| Pārvaldīt dimensiju kopas                  | Atvērt dialoglodziņu **Dimensiju kopas**, kurā varat veidot un modificēt dimensiju kopas. Šī komanda ir pieejama rindas vai pārskatu koka definīcijā. |
| Ievietot rindu                             | Rindas definīcijā tiek ievietota tukša rinda vai kolonnas definīcijā — tukša galvenes rinda. Šī komanda ir pieejama rindas definīcijā vai kolonnas definīcijā. |
| Dzēst rindu                             | No rindas definīcijas tiek dzēsta atlasītā rinda vai no kolonnas definīcijas — atlasītā galvenes rinda. Šī komanda ir pieejama rindas definīcijā vai kolonnas definīcijā. |
| Ievietot kolonnu                          | Kolonnas definīcijā tiek ievietota tukša kolonna. Šī komanda ir pieejama kolonnas definīcijā. |
| Dzēst kolonnu                          | Atlasītā kolonna tiek dzēsta no kolonnas definīcijas. Šī komanda ir pieejama kolonnas definīcijā. |
| Ievietot pārskatu vienības no dimensijām | Atvērt dialoglodziņu **Ievietot pārskata vienības no dimensijām**, kurā varat atlasīt dimensijas vērtības, kuras vēlaties iekļaut pārskata koka definīcijā. Šī komanda ir pieejama pārskatu koka definīcijā. |
| Importēt dimensiju kopas hierarhiju         | Atvērt dialoglodziņu **Dimensijas kopas hierarhija**, kur varat importēt dimensiju kopas hierarhiju no finanšu datiem. Šī komanda ir pieejama pārskata koka definīcijā sistēmās, kuras ir ..\\financial-dimensions\\dimension-based. |
| Ievietot pārskatu vienību                  | Ievietot tukšu rindu pārskata koka definīcijā. Šī komanda ir pieejama pārskatu koka definīcijā. |
| Dzēst pārskatu vienību                  | Atlasītā pārskatu vienības rinda tiek dzēsta no pārskatu koka definīcijas. Šī komanda ir pieejama pārskatu koka definīcijā. |

### <a name="view-menu"></a>Izvēlne Skatīt

Izvēlne **Skatīt** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda         | Apraksts                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigācijas rūts | Tiek parādīta vai paslēpta navigācijas rūts.                                      |
| Rīkjoslas        | Atlasiet rīkjoslas, kas tiek parādītas.                                  |
| Statusa josla      | Rādīt vai paslēpt statusa informāciju logā **Pārskata veidotājs**. |
| Sveiciena lapa    | Tiek atvērta lapa **Laipni lūdzam!**.                                             |

### <a name="format-menu"></a>Izvēlne Formatēt

Izvēlne **Formāts** ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. Šajā izvēlnē ir tālāk aprakstītās komandas.

| Komanda               | Apraksts |
|-----------------------|-------------|
| Stili un formatējums | Atvērt dialoglodziņu **Stili un formatējums**, kur varat izveidot un modificēt teksta stilu rindu definīcijās un kolonnu definīcijās. Šī komanda ir pieejama rindas definīcijā vai kolonnas definīcijā. |
| Kolonnas platums          | Atvērt dialoglodziņu **Kolonnas platums**, kur varat iestatīt atlasītās kolonnas platumu. Šī komanda ir pieejama rindas definīcijā, kolonnas definīcijā vai pārskatu koka definīcijā. |
| Paslēpt                  | Tiek paslēpta atlasītā kolonna. Šī komanda ir pieejama rindas definīcijā, kolonnas definīcijā vai pārskatu koka definīcijā. |
| Parādīt slēpto                | Tiek parādītas tās kolonnas, kuras ir paslēptas starp atlasītajām kolonnām. Šī komanda ir pieejama rindas definīcijā, kolonnas definīcijā vai pārskatu koka definīcijā. |

### <a name="company-menu"></a>Izvēlne Uzņēmums

Izvēlne **Uzņēmums** ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. Šajā izvēlnē ir tālāk aprakstītās komandas.

| Komanda               | Apraksts                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Uzņēmumi             | Atvērt dialoglodziņu **Uzņēmumi**, kurā varat veidot un modificēt uzņēmumus.                                          |
| Veidošanas bloku grupas | Atvērt dialoglodziņu **Veidošanas bloku grupas**, kur varat veidot, modificēt, importēt un eksportēt veidošanas bloku grupas. |

### <a name="go-menu"></a>Izvēlne Doties uz:

Izvēlne **Doties uz:** ir pieejama visiem lietotājiem, un tajā ir ietvertas tālāk aprakstītās komandas.

> [!NOTE]
> Ja navigācijas rūts nav redzama, šīs komandas nerada redzamu efektu.

| Komandas                   | Apraksts                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Pārskatu definīcijas         | Navigācijas rūtī tiek parādītas pārskata definīcijas.                                    |
| Rindu definīcijas            | Navigācijas rūtī tiek parādītas rindas definīcijas.                                       |
| Kolonnu definīcijas         | Navigācijas rūtī tiek parādītas kolonnas definīcijas.                                    |
| Pārskatu koku definīcijas | Navigācijas rūtī tiek parādītas pārskatu koka definīcijas.                            |
| Drošība                   | Navigācijas rūtī tiek parādīta lietotāju, grupu un uzņēmumu drošības informācija. |

### <a name="tools-menu"></a>Izvēlne Rīki

Izvēlne **Rīki** ir pieejama visiem lietotājiem, bet dažām komandām ir ierobežota pieejamība. Šajā izvēlnē ir tālāk aprakstītās komandas.

| Komanda                       | Apraksts |
|-------------------------------|-------------|
| Aizsargāt                       | Pašreizējam veidošanas blokam tiek lietota parole. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Pārskatu rindas statuss           | Atvērt dialoglodziņu **Pārskata rindas statuss**, kur varat redzēt visus nesen ģenerētos pārskatus un detalizētu informāciju par katru pārskatu. |
| Avota sistēmas informācija     | Tiek parādīti jūsu Microsoft Dynamics ERP sistēmas iestatījumi. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Paņemtie krājumi             | Tiek parādītas pašreiz atvērtās rindu, kolonnu, pārskatu koka un pārskatu definīcijas. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Atsvaidzināt kešotos finanšu datus | Tiek atjaunināti finanšu dimensiju kolonnās ietvertie dati. |
| Opcijas                       | Atvērt dialoglodziņu **Opcijas**, kurā varat mainīt lietotāja preferences pārskata veidotāja videi. |

### <a name="window-menu"></a>Izvēlne Windows

Izvēlne **Logs** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda              | Apraksts |
|----------------------|-------------|
| Kārtot elementus horizontāli    | Visi atvērtie logi tiek parādīti viens aiz otra. |
| Kārtot elementus vertikāli      | Visi atvērtie logi tiek parādīti viens virs otra. |
| Kaskāde              | Visi atvērtie logi tiek parādīti līmeņos, lai būtu redzama visu logu virsrakstjosla. |
| Sasaldēt horizontāli    | Atlasītā rinda tiek sasaldēta. Tādējādi, veicot ritināšanas darbību, šī rinda joprojām ir redzama logā. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Sasaldēt vertikāli      | Atlasītā kolonna tiek sasaldēta. Tādējādi, veicot ritināšanas darbību, šī kolonna joprojām ir redzama logā. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Atvērto logu saraksts | Tiek parādīts atvērto logu saraksts. Atlasiet logu, lai to pārvietotu priekšpusē. |

### <a name="help-menu"></a>Palīdzības izvēlne

Izvēlne **Palīdzība** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Command | Apraksts                                                              |
|---------|--------------------------------------------------------------------------|
| Palīdzība    | Atveriet palīdzības tēmas lapu par finanšu pārskatiem. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Pārskatu veidotāja rīkjoslas pogas
Tabulās ir aprakstītas rīkjoslas pogas, kuras varat izmantot, veidojot pārskatus. Daļa rīkjoslas pogu ir pieejamas tikai noteiktos apstākļos. Piemēram, pārskatu vienību paaugstināšanas un pazemināšanas pogas ir pieejamas tikai tad, kad tiek modificēta pārskatu koka definīcija.

### <a name="standard-toolbar"></a>Standarta rīkjosla

Izmantojot standarta rīkjoslu, varat ātri piekļūt failam un rediģēt komandas. Šajā rīkjoslā ir ietvertas tālāk aprakstītās pogas.

| Poga                                                                                       | Apraksts |
|----------------------------------------------------------------------------------------------|-------------|
| [![Poga Jauns](./media/rowc130389.png)](./media/rowc130389.png)                              | Izveidojiet jaunu (tukšu) pārskata, rindas, kolonnas vai pārskatu koka definīciju. |
| [![Poga Atvērt](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Tiek atvērta esošā rindas, kolonnas, pārskatu koka vai pārskata definīcija. |
| [![Poga Saglabāt](./media/savec130389.png)](./media/savec130389.png)                           | Tiek saglabāta pašreizējā rindas, kolonnas, pārskatu koka vai pārskata definīcija. |
| [![Poga Kopēt](./media/copyc130389.png)](./media/copyc130389.png)                           | Atlasītais teksts tiek kopēts starpliktuvē. |
| [![Poga Izgriezt](./media/cutc130389.png)](./media/cutc130389.png)                              | Atlasītais teksts tiek dzēsts un kopēts starpliktuvē. |
| [![Poga Ielīmēt](./media/pastec130389.png)](./media/pastec130389.png)                        | Starpliktuvē saglabātais teksts tiek ievietots norādītajā vietā. |
| [![Poga Atsaukt](./media/undoc130389.png)](./media/undoc130389.png)                           | Pēdējā darbība tiek atsaukta. |
| [![Poga Atcelt atsaukšanu](./media/redoc130389.png)](./media/redoc130389.png)                           | Pēdējā atsaukšanas darbība tiek atcelta. |
| [![Poga Atrast](./media/findc130389.png)](./media/findc130389.png)                           | Atvērt dialoglodziņu **Meklēt un aizvietot**, kur varat meklēt un aizvietot tekstu aktīvajā logā. |
| [![Poga Ievietot rindu](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Rindas definīcijā tiek ievietota tukša rinda vai kolonnas definīcijā — tukša galvenes rinda. Šī poga ir pieejama rindas definīcijā vai kolonnas definīcijā. |
| [![Poga Ievietot kolonnu](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Kolonnas definīcijā tiek ievietota tukša kolonna. Šī poga ir pieejama kolonnas definīcijā. |
| [![Poga Bloķēt](./media/lockc130389.png)](./media/lockc130389.png)                           | Pašreizējam veidošanas blokam tiek lietota parole. Šī poga ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| [![Poga Rindas saite](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Atvērt dialoglodziņu **Rindu saites**, kur varat norādīt datu saišu avotus rindas definīcijām un pārskata koku definīcijām. Šī poga ir pieejama rindas definīcijā. |
| [![Poga Paaugstināt](./media/promotec130389.png)](./media/promotec130389.png)                  | Pārskatu koka definīcijas vienība tiek paaugstināta. Kad atlasāt pakārtoto vienību un tad noklikšķināt uz **Paaugstināt**, pakārtotā vienība tiek pārvietots uz to pašu līmeni kā tās pamata vienība. |
| [![Poga Pazemināt](./media/demotec130389.png)](./media/demotec130389.png)                     | Pārskatu koka definīcijas vienība tiek pazemināta. Kad atlasāt vienību un tad noklikšķināt uz **Pazemināt**, vienība kļūst par apakšelementu vienībai, kas ir pirms tā. |
| [![Poga Izvērst](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Visas pārskatu koka definīcijas vienības tiek izvērstas atlasītās vienības līmenī. |
| [![Poga Sakļaut](./media/collapsec130389.png)](./media/collapsec130389.png)               | Sakļaut pārskata koku. |
| [![Poga Palīdzība](./media/helpc130389.png)](./media/helpc130389.png)                           | Atvērt palīdzību. |

### <a name="formatting-toolbar"></a>Formatēšanas rīkjosla

Formatēšanas rīkjosla sniedz ērtu piekļuvi stila komandām. Šajā rīkjoslā ir ietvertas tālāk aprakstītās pogas.

| Poga                                                                                                       | Apraksts                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Poga Fonta stils](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Pašreizējam tekstam tiek iestatīts atlasītais fonta stils.      |
| [![Poga Fonts](./media/fonttype.png)](./media/fonttype.png)                                                 | Pašreizējam tekstam tiek iestatīts atlasītais fonts.              |
| [![Poga Fonta lielums](./media/fontsize.png)](./media/fontsize.png)                                            | Pašreizējam tekstam tiek iestatīts atlasītais fonta lielums (punktos). |
| [![Poga Treknraksts](./media/boldc130389.png)](./media/boldc130389.png)                                           | Pašreizējam tekstam tiek iestatīts treknraksts.                             |
| [![Poga Slīpraksts](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Pašreizējam tekstam tiek iestatīts slīpraksts.                           |
| [![Poga Pasvītrot](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Pašreizējam tekstam tiek iestatīts pasvītrojums.                             |
| [![Poga Samazināt atkāpi](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Tiek samazināta pašreizējā teksta atkāpe.                |
| [![Poga Palielināt atkāpi](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Tiek palielināta pašreizējā teksta atkāpe.                |
| [![Poga Fona krāsa](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Mainīt pašreizējās šūnas fona krāsu.        |
| [![Poga Fonta krāsa](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Mainīt pašreizējā teksta krāsu.                   |

### <a name="report-designer-toolbar"></a>Atskaišu veidotāja rīkjosla

Atskaišu veidotāja rīkjosla sniedz ātru piekļuvi komandām, kas paredzētas, lai pārvietotos atskaišu veidotājā. Šajā rīkjoslā atrodas tālāk aprakstītās pogas.

| Poga                                                                                              | Apraksts |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![Poga Pārskata definīcija](./media/reportc130389.png)](./media/reportc130389.png)                 | Rādīt pārskata definīciju, kas ir uzskaitīta izvēlnē **Logs**. |
| [![Poga Rindas definīcija](./media/rowc130389.png)](./media/rowc130389.png)                          | Tiek parādīta aktīvajai pārskata definīcijai piešķirtā rindas definīcija. |
| [![Poga Kolonnas definīcija](./media/columnc130389.png)](./media/columnc130389.png)                 | Tiek parādīta aktīvajai pārskata definīcijai piešķirtā kolonnas definīcija. |
| [![Poga Pārskata koka definīcija](./media/treec130389.png)](./media/treec130389.png)             | Tiek parādīta aktīvajai pārskata definīcijai piešķirtā pārskatu koka definīcija. |
| [![Poga Pārskatu skatītājs](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Tiek palaists pārskatu skatītājs un parādīta ģenerētā pārskata jaunākā versija. Ja ģenerējāt vismaz vienu pārskatu, šī poga ir pieejama pārskata definīcijā. |
| [![Poga Ģenerēt pārskatu](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Tiek ģenerēts pārskats, izmantojot aktīvo pārskata definīciju. Šī poga ir pieejama pārskata definīcijā. |

## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošana](financial-reporting-intro.md)

[Ģenerēt finanšu pārskatus](generate-financial-report.md)
