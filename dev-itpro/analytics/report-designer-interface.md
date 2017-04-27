---
title: "Pārskatu veidotāja saskarne"
description: "Šajā rakstā ir paskaidrots, kā pārvietoties atskaišu veidotājā un kā izmantot dažādās opcijas, lai izpildītu jūsu konkrētās prasības."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 50 - 10
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 58c56aca6f339a5ec13703605334dd45b208ab2c
ms.lasthandoff: 03/29/2017


---

# <a name="report-designer-interface"></a>Pārskatu veidotāja saskarne

Šajā rakstā ir paskaidrots, kā pārvietoties atskaišu veidotājā un kā izmantot dažādās opcijas, lai izpildītu jūsu konkrētās prasības. 

<a name="report-designer-menu-commands"></a>Pārskatu veidotāja izvēlnes komandas
-----------------------------

Nākamajās tabulās ir aprakstītas izvēlnes komandas un opcijas, kuras varat izmantot, veidojot finanšu atskaites. Dažas izvēlnes komandas un opcijas ir pieejamas tikai īpašos apstākļos. Piemēram, komandas, kas paredzētas pārskata vienības paaugstināšanai vai pazemināšanai, ir pieejamas tikai tad, kad modificējat pārskata koka definīciju.

### <a name="file-menu"></a>Izvēlne Fails

Izvēlne **Fails** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda                           | Apraksts                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jauns                               | Izveidot jaunu pārskata definīciju, rindas definīciju, kolonnas definīciju, pārskata koka definīciju, pārskata grupas definīciju vai mapi. Atkarībā no jūsu lietotāja lomas ir pieejamas papildu opcijas. |
| Atvērta                              | Atvērt eksistējošu rindas definīciju, kolonnas definīciju, pārskata koka definīciju vai pārskata definīciju.                                                                                             |
| Aizvērt                             | Aizvērt pašreizējo veidošanas bloku.                                                                                                                                                                |
| Aizvērt visu                         | Aizvērt visus veidošanas blokus.                                                                                                                                                                       |
| Saglabāt                              | Saglabāt pašreizējo rindas definīciju, kolonnas definīciju, pārskata koka definīciju vai pārskata definīciju.                                                                                             |
| Saglabāt Kā                           | Saglabāt pašreizējo rindas definīciju, kolonnas definīciju, pārskata koka definīciju vai pārskata definīciju, norādot jaunu nosaukumu.                                                                            |
| Rekvizīti                        | Atvērt dialoglodziņu **Rekvizīti**, kur varat mainīt pārskata nosaukumu un aprakstu.                                                                                                   |
| Ģenerēt                          | Ģenerēt pašreizējo pārskatu. Šī komanda ir pieejama no pārskata definīcijas.                                                                                                                 |
| Apskatīt pārskatu                       | Atvērt programmatūrā Dynamics 365 for Operations ģenerētā pārskata jaunāko versiju. Šī komanda ir pieejama no pārskata definīcijas, ja esat ģenerējis vismaz vienu pārskatu.                                 |
| Nesen izmantotās pārskatu definīcijas         | Rādīt sarakstu ar pārskatiem, kas nesen izveidoti vai modificēti. Tad varat atlasīt pārskatu no saraksta.                                                                                    |
| Nesen izmantotās rindu definīcijas            | Rādīt sarakstu ar rindu definīcijām, kas nesen izveidotas vai modificētas. Tad varat atlasīt rindas definīciju no saraksta.                                                                    |
| Nesen izmantotās kolonnu definīcijas         | Rādīt sarakstu ar kolonnu definīcijām, kas nesen izveidotas vai modificētas. Tad varat atlasīt kolonnas definīciju no saraksta.                                                              |
| Nesen izmantotās pārskatu koku definīcijas | Rādīt sarakstu ar pārskatu koku definīcijām, kas nesen izveidotas vai modificētas. Tad varat atlasīt pārskata koka definīciju no saraksta.                                              |
| Iziet                              | Iziet no pārskatu veidotāja.                                                                                                                                                                            |

### <a name="edit-menu"></a>Rediģēšanas izvēlne

Izvēlne **Rediģēt** ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. Šajā izvēlnē iekļautas tālāk minētās komandas.

| Komanda                                | Apraksts                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Atsaukt                                   | Atsaukt pēdējo darbību.                                                                                                                                                                                              |
| Atcelt atsaukšanu                                   | Atgriezt pēdējo atsaukto darbību.                                                                                                                                                                                      |
| Izgriezt                                    | Dzēst atlasīto tekstu un kopēt to uz starpliktuvi.                                                                                                                                                            |
| Kopija                                   | Kopēt atlasīto tekstu uz starpliktuvi.                                                                                                                                                                           |
| Ielīmēt                                  | Ievietot pēdējo izgriezto vai kopēto tekstu no starpliktuves.                                                                                                                                                    |
| Notīrīt                                  | Dzēst atlasītās veidošanas bloka šūnas saturu.                                                                                                                                                           |
| Meklēt                                   | Atvērt dialoglodziņu **Meklēt un aizvietot**, kur varat meklēt tekstu skata rūtī.                                                                                                                              |
| Aizstāt                                | Atvērt dialoglodziņu **Meklēt un aizvietot**, kur varat meklēt un aizvietot tekstu skata rūtī.                                                                                                                  |
| Ievietot rindas no dimensijām            | Atvērt dialoglodziņu **Ievietot rindas no dimensijām**, kurā varat atlasīt dimensijas vērtības, kuras vēlaties iekļaut rindas definīcijā. Šī komanda ir pieejama no rindas definīcijas.                                  |
| Pārnumurēt rindas                          | Pārnumurēt visus rindu skaitliskos kodus. Šī komanda ir pieejama no rindas definīcijas.                                                                                                                                   |
| Rindu saites                              | Atvērt dialoglodziņu **Rindu saites**, kur varat norādīt datu saišu avotus rindas definīcijām un pārskata koku definīcijām. Šī komanda ir pieejama no rindas definīcijas.                            |
| Noapaļošanas korekcija                    | Atvērt dialoglodziņu **Noapaļošanas korekcijas**, kur varat norādīt noapaļošanas parametrus. Šī komanda ir pieejama no rindas definīcijas.                                                                  |
| Pārvaldīt dimensiju kopas                  | Atvērt dialoglodziņu **Dimensiju kopas**, kurā varat veidot un modificēt dimensiju kopas. Šī komanda ir pieejama no rindas definīcijas vai pārskata koka definīcijas.                                              |
| Ievietot rindu                              | Ievietot tukšu rindu rindas definīcijā vai tukšu virsraksta rindu kolonnas definīcijā. Šī komanda ir pieejama no rindas definīcijas vai kolonnas definīcijas.                                               |
| Dzēst rindu                             | Dzēst atlasīto rindu no rindas definīcijas vai atlasīto virsraksta rindu no kolonnas definīcijas. Šī komanda ir pieejama no rindas definīcijas vai kolonnas definīcijas.                                       |
| Ievietot kolonnu                          | Ievietot tukšu kolonnu kolonnas definīcijā. Šī komanda ir pieejama no kolonnas definīcijas.                                                                                                             |
| Dzēst kolonnu                          | Dzēst atlasīto kolonnu no kolonnas definīcijas. Šī komanda ir pieejama no kolonnas definīcijas.                                                                                                         |
| Ievietot pārskata vienības no dimensijām | Atvērt dialoglodziņu **Ievietot pārskata vienības no dimensijām**, kurā varat atlasīt dimensijas vērtības, kuras vēlaties iekļaut pārskata koka definīcijā. Šī komanda ir pieejama no pārskata koka definīcijas. |
| Importēt dimensiju kopas hierarhiju         | Atvērt dialoglodziņu **Dimensijas kopas hierarhija**, kur varat importēt dimensiju kopas hierarhiju no finanšu datiem. Šī komanda ir pieejama pārskata koka definīcijā sistēmās, kuras ir balstītas uz dimensijām.  |
| Ievietot pārskata vienību                  | Ievietot tukšu rindu pārskata koka definīcijā. Šī komanda ir pieejama no pārskata koka definīcijas.                                                                                                |
| Dzēst pārskata vienību                  | Dzēst atlasīto pārskata vienības rindu no pārskata koka definīcijas. Šī komanda ir pieejama no pārskata koka definīcijas.                                                                             |

### <a name="view-menu"></a>Skata izvēlne

Izvēlne **Skatīt** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda         | Apraksts                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigācijas rūts | Rādīt vai paslēpt navigācijas rūti.                                      |
| Rīkjoslas        | Atlasīt rīkjoslas, kas ir redzamas.                                  |
| Statusa josla      | Rādīt vai paslēpt statusa informāciju logā **Pārskata veidotājs**. |
| Iepazīšanās lapa    | Atvērt lapu **Laipni lūdzam!**                                             |

### <a name="format-menu"></a>Formatēšanas izvēlne

Izvēlne **Formāts** ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. Šajā izvēlnē iekļautas tālāk minētās komandas.

| Komanda               | Apraksts                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stili un formatējums | Atvērt dialoglodziņu **Stili un formatējums**, kur varat izveidot un modificēt teksta stilu rindu definīcijās un kolonnu definīcijās. Šī komanda ir pieejama no rindas definīcijas vai kolonnas definīcijas. |
| Kolonnas platums          | Atvērt dialoglodziņu **Kolonnas platums**, kur varat iestatīt atlasītās kolonnas platumu. Šī komanda ir pieejama no rindas definīcijas, kolonnas definīcijas vai pārskata koka definīcijas.                      |
| Paslēpt                  | Paslēpt atlasīto kolonnu. Šī komanda ir pieejama no rindas definīcijas, kolonnas definīcijas vai pārskata koka definīcijas.                                                                                        |
| Parādīt                | Padarīt redzamas paslēptās kolonnas, kas atrodas starp atlasītajām kolonnām. Šī komanda ir pieejama no rindas definīcijas, kolonnas definīcijas vai pārskata koka definīcijas.                                                      |

### <a name="company-menu"></a>Uzņēmuma izvēlne

Izvēlne **Uzņēmums** ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. Šajā izvēlnē iekļautas tālāk minētās komandas.

| Komanda               | Apraksts                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Uzņēmumi             | Atvērt dialoglodziņu **Uzņēmumi**, kurā varat veidot un modificēt uzņēmumus.                                          |
| Veidošanas bloku grupas | Atvērt dialoglodziņu **Veidošanas bloku grupas**, kur varat veidot, modificēt, importēt un eksportēt veidošanas bloku grupas. |

### <a name="go-menu"></a>Izvēlne Doties

Izvēlne **Doties** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas. **Piezīme:** šīm komandām nav acīmredzama efekta, ja nav redzama navigācijas rūts.

| Komandas                   | Apraksts                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Pārskatu definīcijas         | Attēlot pārskatu definīcijas navigācijas rūtī.                                    |
| Rindu definīcijas            | Attēlot rindu definīcijas navigācijas rūtī.                                       |
| Kolonnu definīcijas         | Attēlot kolonnu definīcijas navigācijas rūtī.                                    |
| Pārskata koku definīcijas | Attēlot pārskatu koku definīcijas navigācijas rūtī.                            |
| Drošība                   | Navigācijas rūtī parādīt drošības informāciju lietotājiem, grupām un uzņēmumiem. |

### <a name="tools-menu"></a>Izvēlne Rīki

Izvēlne **Rīki** ir pieejama visiem lietotājiem, bet dažām komandām ir ierobežota pieejamība. Šajā izvēlnē iekļautas tālāk minētās komandas.

| Komanda                       | Apraksts                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aizsargāt                       | Lietot paroli pašreizējam veidošanas blokam. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma.                                                                           |
| Pārskata rindas statuss           | Atvērt dialoglodziņu **Pārskata rindas statuss**, kur varat redzēt visus nesen ģenerētos pārskatus un detalizētu informāciju par katru pārskatu.                                                                                    |
| Avota sistēmas informācija     | Parādīt Microsoft Dynamics ERP sistēmas iestatījumus. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma.                                                                 |
| Izrakstītie vienumi             | Parādīt rindu definīcijas, kolonnu definīcijas, pārskata koku definīcijas un pārskatu definīcijas, kuras šobrīd ir atvērtas. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Atsvaidzināt kešatmiņas finanšu datus | Atjaunināt datus finanšu dimensiju kolonnā.                                                                                                                                                               |
| Opcijas                       | Atvērt dialoglodziņu **Opcijas**, kurā varat mainīt lietotāja preferences pārskata veidotāja videi.                                                                                                                       |

### <a name="window-menu"></a>Izvēlne Logs

Izvēlne **Logs** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda              | Apraksts                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mozaīkot horizontāli    | Rādīt visus atvērtos logus citu citam blakus.                                                                                                                                                     |
| Mozaīkot vertikāli      | Rādīt visus atvērtos logus citu virs cita.                                                                                                                                               |
| Kaskadēt              | Pārklāt visus atvērtos logus tā, lai paliek redzama tikai katra loga virsraksta josla.                                                                                                                      |
| Sasaldēt horizontāli    | Sasaldēt atlasīto rindu tā, lai ritinot šī rinda logā paliek redzama. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma.       |
| Sasaldēt vertikāli      | Sasaldēt atlasīto kolonnu tā, lai ritinot šī kolonna logā paliek redzama. Komanda ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma. |
| Atvērto logu saraksts | Rādīt sarakstu ar atvērtajiem logiem. Atlasiet logu, lai to pārvietotu uz priekšpusi.                                                                                                               |

### <a name="help-menu"></a>Palīdzības izvēlne

Izvēlne **Palīdzība** ir pieejama visiem lietotājiem un ietver tālāk minētās komandas.

| Komanda | apraksts                                                  |
|---------|--------------------------------------------------------------|
| Palīdzība    | Atvērt Dynamics 365 for Operations palīdzības vikilapu par finanšu pārskatiem. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Pārskatu veidotāja rīkjoslas pogas
Tabulās ir aprakstītas rīkjoslas pogas, kuras varat izmantot, veidojot pārskatus. Dažas rīkjoslas pogas ir pieejamas tikai īpašos apstākļos. Piemēram, pogas, kas paredzētas pārskata vienības paaugstināšanai vai pazemināšanai, ir pieejamas tikai tad, kad modificējat pārskata koka definīciju.

### <a name="standard-toolbar"></a>Standarta rīkjosla

Standarta rīkjosla nodrošina ātru piekļuvi failu un rediģēšanas komandām. Šajā rīkjoslā atrodas tālāk aprakstītās pogas.

| Poga                                                                                                                                                                                   | Apraksts                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Poga Jauns](./media/rowc130389.png)](./media/rowc130389.png)                              | Izveidot jaunu (tukšu) pārskata definīciju, rindas definīciju, kolonnas definīciju vai pārskata koka definīciju.                                                                               |
| [![Poga Atvērt](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Atvērt eksistējošu rindas definīciju, kolonnas definīciju, pārskata koka definīciju vai pārskata definīciju.                                                                                   |
| [![Poga Saglabāt](./media/savec130389.png)](./media/savec130389.png)                           | Saglabāt pašreizējo rindas definīciju, kolonnas definīciju, pārskata koka definīciju vai pārskata definīciju.                                                                                   |
| [![Poga Kopēt](./media/copyc130389.png)](./media/copyc130389.png)                           | Kopēt atlasīto tekstu uz starpliktuvi.                                                                                                                                               |
| [![Poga Izgriezt](./media/cutc130389.png)](./media/cutc130389.png)                              | Dzēst atlasīto tekstu un kopēt to uz starpliktuvi.                                                                                                                                |
| [![Poga Ielīmēt](./media/pastec130389.png)](./media/pastec130389.png)                        | Ievietot tekstu no starpliktuves.                                                                                                                                                    |
| [![Poga Atsaukt](./media/undoc130389.png)](./media/undoc130389.png)                           | Atsaukt pēdējo darbību.                                                                                                                                                                  |
| [![Poga Atcelt atsaukšanu](./media/redoc130389.png)](./media/redoc130389.png)                           | Atgriezt pēdējo atsaukto darbību.                                                                                                                                                          |
| [![Poga Atrast](./media/findc130389.png)](./media/findc130389.png)                           | Atvērt dialoglodziņu **Meklēt un aizvietot**, kur varat meklēt un aizvietot tekstu aktīvajā logā.                                                                                  |
| [![Poga Ievietot rindu](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Ievietot tukšu rindu rindas definīcijā vai tukšu virsraksta rindu kolonnas definīcijā. Šī poga ir pieejama no rindas definīcijas vai kolonnas definīcijas.                    |
| [![Poga Ievietot kolonnu](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Ievietot tukšu kolonnu kolonnas definīcijā. Šī poga ir pieejama no kolonnas definīcijas.                                                                                  |
| [![Poga Bloķēt](./media/lockc130389.png)](./media/lockc130389.png)                           | Lietot paroli pašreizējam veidošanas blokam. Šī poga ir pieejama lietotājiem, kuriem ir **veidotāja** vai **administratora** loma.                                                 |
| [![Poga Rindas saite](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Atvērt dialoglodziņu **Rindu saites**, kur varat norādīt datu saišu avotus rindas definīcijām un pārskata koku definīcijām. Šī poga ir pieejama no rindas definīcijas. |
| [![Poga Paaugstināt](./media/promotec130389.png)](./media/promotec130389.png)                  | Paaugstināt pārskata koka definīcijas vienību. Kad atlasāt pakārtoto vienību un tad noklikšķināt uz **Paaugstināt**, pakārtotā vienība tiek pārvietots uz to pašu līmeni kā tās pamata vienība.                |
| [![Poga Pazemināt](./media/demotec130389.png)](./media/demotec130389.png)                     | Pazemināt pārskata koka definīcijas vienību. Kad atlasāt vienību un tad noklikšķināt uz **Pazemināt**, vienība kļūst par apakšelementu vienībai, kas ir pirms tā.                               |
| [![Poga Izvērst](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Izvērst visas pārskata koka definīcijas vienības atlasītās vienības līmenī.                                                                                                   |
| [![Poga Sakļaut](./media/collapsec130389.png)](./media/collapsec130389.png)               | Sakļaut pārskata koku.                                                                                                                                                           |
| [![Poga Palīdzība](./media/helpc130389.png)](./media/helpc130389.png)                           | Atvērt palīdzību.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Formatēšanas rīkjosla

Formatēšanas rīkjosla sniedz ērtu piekļuvi stila komandām. Šajā rīkjoslā atrodas tālāk aprakstītās pogas.

| Poga                                                                                                                                                                                                   | Apraksts                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Poga Fonta stils](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Lietot atlasīto fonta stilu pašreizējam tekstam.      |
| [![Poga Fonts](./media/fonttype.png)](./media/fonttype.png)                                                 | Iestatīt atlasīto fontu pašreizējam tekstam.              |
| [![Poga Fonta lielums](./media/fontsize.png)](./media/fontsize.png)                                            | Iestatīt atlasīto fonta lielumu (punktos) pašreizējam tekstam. |
| [![Poga Treknraksts](./media/boldc130389.png)](./media/boldc130389.png)                                           | Pārveidot pašreizējo tekstu treknrakstā.                             |
| [![Poga Slīpraksts](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Pārveidot pašreizējo tekstu slīprakstā.                           |
| [![Poga Pasvītrot](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Pasvītrot pašreizējo tekstu.                             |
| [![Poga Samazināt atkāpi](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Samazināt pašreizējā teksta atkāpi.                |
| [![Poga Palielināt atkāpi](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Palielināt pašreizējā teksta atkāpi.                |
| [![Poga Fona krāsa](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Mainīt pašreizējās šūnas fona krāsu.        |
| [![Poga Fonta krāsa](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Mainīt pašreizējā teksta krāsu.                   |

### <a name="report-designer-toolbar"></a>Atskaišu veidotāja rīkjosla

Atskaišu veidotāja rīkjosla sniedz ātru piekļuvi komandām, kas paredzētas, lai pārvietotos atskaišu veidotājā. Šajā rīkjoslā atrodas tālāk aprakstītās pogas.

| Poga                                                                                                                                                                                          | Apraksts                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Poga Pārskata definīcija](./media/reportc130389.png)](./media/reportc130389.png)                 | Rādīt pārskata definīciju, kas ir uzskaitīta izvēlnē **Logs**.                                                                                                            |
| [![Poga Rindas definīcija](./media/rowc130389.png)](./media/rowc130389.png)                          | Rādīt rindas definīciju, kas ir piešķirta aktīvajai pārskata definīcijai.                                                                                                    |
| [![Poga Kolonnas definīcija](./media/columnc130389.png)](./media/columnc130389.png)                 | Rādīt kolonnas definīciju, kas ir piešķirta aktīvajai pārskata definīcijai.                                                                                                 |
| [![Poga Pārskata koka definīcija](./media/treec130389.png)](./media/treec130389.png)             | Rādīt pārskata koka definīciju, kas ir piešķirta aktīvajai pārskata definīcijai.                                                                                         |
| [![Poga Pārskatu skatītājs](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Palaist pārskatu skatītāju un parādīt ģenerētā pārskata jaunāko versiju. Šī poga ir pieejama no pārskata definīcijas, ja esat ģenerējis vismaz vienu pārskatu. |
| [![Poga Ģenerēt pārskatu](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Ģenerēt pārskatu no aktīvās pārskata definīcijas. Šī poga ir pieejama no pārskata definīcijas.                                                                      |



<a name="see-also"></a>Skatiet arī
--------

[Finanšu atskaišu veidošana programmatūrai Microsoft Dynamics ERP](financial-reporting-intro.md)

[Finanšu pārskata ģenerēšana](\financials\general-ledger\generate-financial-report.md)


