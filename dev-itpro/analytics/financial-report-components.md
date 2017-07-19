---
title: "Finanšu pārskata komponenti"
description: "Šajā rakstā ir izklāstīts, kā finanšu atskaišu veidošanā tiek izmantoti atskaišu definīciju komponenti jeb veidošanas bloki. Šajos veidošanas blokos ir iekļautas rindas definīcijas, kolonnas definīcijas un atskaišu koka definīcijas. Rakstā ir paskaidrots, kā organizēt un bloķēt veidošanas blokus un kā strādāt ar veidošanas bloku grupām."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5c09b1fc061f95cd78e9f18c2bdf846fdbfc7cf1
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="financial-report-components"></a>Finanšu pārskata komponenti

[!include[banner](../includes/banner.md)]


Šajā rakstā ir izklāstīts, kā finanšu atskaišu veidošanā tiek izmantoti atskaišu definīciju komponenti jeb veidošanas bloki. Šajos veidošanas blokos ir iekļautas rindas definīcijas, kolonnas definīcijas un atskaišu koka definīcijas. Rakstā ir paskaidrots, kā organizēt un bloķēt veidošanas blokus un kā strādāt ar veidošanas bloku grupām. 

Finanšu atskaišu veidotāja dizains tika veidots ar mērķi sadalīt informāciju vismazākajos komponentos jeb veidošanas blokos, lai šos komponentus varētu pēc nepieciešamības jaukt un kombinēt. Tādēļ jūsu atskaišu formatējums atrodas atsevišķi no jūsu finanšu datiem un atskaites noformējumu varat mainīt, nemainot finanšu datus savā Microsoft Dynamics ERP sistēmā. Izmantojot šo veidošanas bloku pieeju, ir iespējams kombinēt tekstu, summas un aprēķinus, lai veidotu jums nepieciešamās atskaites. Turklāt šī elastība atbalsta radošu pieeju, atvieglojot darbību apskatīšanu dažādos veidos. Atsevišķie atskaites definīcijas veidošanas bloki ir līdzīgi trīsdimensiju izklājlapai, bet tie sniedz vairāk iespēju. Atskaites definīcija norāda rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, kas ir jāizmanto šai atskaitei. Tas iekļauj arī informāciju par to, kur glabāt ģenerēto atskaiti un kā to formatēt. Labākos atkārtotas lietošanas un kopīgošanas nolūkos varat izveidot veidošanas bloku grupu, kas ir pastāvošo atskaites definīciju, rindas definīciju, kolonnas definīciju, atskaišu koka definīciju un dimensiju kopu kolekcija, kura ir saistīta ar uzņēmumu.

## <a name="building-blocks-of-a-report"></a>Pārskatu veidošanas bloki
| Veidošanas bloks            | Apraksts                                                                                                                                                                                                                                                                              | Plašāka informācija                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Rindas definīcija            | Rindas definīcija atskaitē definē aprakstošās rindas (piemēram, algas vai pārdošana). Tajā ir uzskaitītas arī segmentu vērtības vai dimensijas, kas satur vērtības katram rindas vienumam un ietver rindu formātus un aprēķinus.                                                    | [Rindu definīcijas](row-definitions-financial-reporting.md)                       |
| Kolonnas definīcija         | Kolonnas definīcija nosaka periodu, kas jāizmanto, kad dati tiek izgūti no finanšu dimensijām. Tas ietver arī kolonnu formatējumu un aprēķinus.                                                                                                                                 | [Kolonnu definīcijas](column-definitions-financial-reports.md)         |
| Pārskata koka definīcija | Pārskata koka definīcija līdzinās organizācijas diagrammai. Tā satur atsevišķas pārskata vienības, kas pārstāv katru diagrammas lauku. Vienības var būt vai nu atsevišķas nodaļas no finanšu datiem vai augstāka līmeņa vienības, kas apkopo datus no citām pārskata vienībām. | [Pārskata koku definīcijas](financial-reporting-tree-definitions.md) |
| Pārskata definīcija         | Pārskata definīcija izmanto rindu definīciju, kolonnu definīciju un papildu pārskata koka definīciju, lai izveidotu pārskatu. Tā arī sniedz papildu opcijas un iestatījumus, ko varat izmantot atskaites pielāgošanai.                                                                    | [Pārskata definīcija](design-financial-report-definitions.md)                  |

Ja jums nav pieredzes atskaišu veidošanā, jums var noderēt atskaišu vednis, lai ātri izveidotu atskaites definīciju, kuru vēlāk varat pielāgot. Ja jums ir pieredze atskaišu veidošanā un vēlaties izmantot plašākas atskaišu noformēšanas iespējas, varat kombinēt jaunus vai jau eksistējošus veidošanas blokus, lai izveidotu jaunu atskaites definīciju. Lai izveidotu kvalitatīvas atskaites, jums nav pilnībā jāizprot visas pieejamās atskaites definīcijas opcijas. Iepazīstoties ar pārskatu izveides procesu, varat izvērst savas pārskatu definīcijas, lai izmantotu papildu funkcijas. Kad esat izveidojis vienkāršu atskaiti, varat pielāgot atskaites definīciju un jebkuru no atskaites definīcijas veidošanas blokiem.

## <a name="organize-the-building-blocks"></a>Veidošanas bloku organizēšana
Izmantojiet mapes, lai organizētu savus veidošanas blokus pārskatu veidotājā. Visas mapes raksturo to ietverto veidošanas bloku tips. Piemēram, visas mapes, kas satur rindas definīcijas, atrodas atskaišu veidotāja rūtī **Rindas definīcijas**.

### <a name="create-a-folder"></a>Mapes izveide

1.  Pārskatu veidotājā atlasiet veidošanas bloka tipu, lai sakārtotu navigācijas rūti. Piemēram, lai kārtotu rindu definīcijas, noklikšķiniet uz **Rindu definīcijas**.
2.  Navigācijas rūtī atlasiet eksistējošu mapi, kurā izveidot jauno mapi, un pēc tam izpildiet vienu no šīm darbībām:
    -   Ar peles labo pogu noklikšķiniet uz pamata mapes un pēc tam noklikšķiniet uz **Jauna mape**.
    -   Atlasiet pamata mapi, noklikšķiniet uz **Fails** un pēc tam noklikšķiniet uz **Jauna mape**.

3.  Kad tiek parādīta jaunā mape, ievadiet jaunās mapes nosaukumu un pēc tam nospiediet taustiņu Enter.

## <a name="lock-a-building-block"></a>Veidošanas bloka bloķēšana
Varat izveidot paroli, lai bloķētu vai palīdzētu aizsargātu kādu veidošanas bloku. Šādi varat paaugstināt atskaites komponenta drošības līmeni, bet nemainot visas sistēmas drošības iestatījumus. Parole var palīdzēt aizsargāt veidošanas bloka informāciju, kas ir svarīga jūsu mēneša beigu atskaišu veidošanas procesā. Jebkuras lomas lietotājs var bloķēt kādu veidošanas bloku. Taču citiem lietotājiem vienmēr ir tikai lasīšanas piekļuve attiecībā uz bloķētiem komponentiem. Lietotāji var atvērt, mainīt un saglabāt bloķēto komponentu ar jaunu nosaukumu. Lietotājs, kuram ir administratora loma, vienmēr var piekļūt bloķētam veidošanas blokam un mainīt to.
1.  Atskaišu veidotājā atveriet bloķējamo atskaites komponentu, piemēram, rindas definīciju, kolonnas definīciju, atskaites definīciju vai atskaišu koka definīciju.
2.  Izvēlnē **Rīki** noklikšķiniet uz **Aizsargāt/noņemt aizsardzību**. Varat arī rīkjoslā noklikšķināt uz **Aizsargāt/noņemt aizsardzību** (slēdzenes ikonas).
3.  Dialoglodziņā **Aizsargāt** ievadiet un apstipriniet paroli un pēc tam noklikšķiniet uz **Labi**. Kad atvērts veidošanas bloks ir bloķēts, slēdzenes ikona rīkjoslā ir izcelta.

Lai atbloķētu kādu bloķētu veidošanas bloku, atveriet šo veidošanas bloku un pēc tam rīkjoslā noklikšķiniet uz ikonas **Aizsargāt/noņemt aizsardzību**. Varat arī izvēlnē **Rīki** noklikšķināt uz **Noņemt aizsardzību**.

## <a name="building-block-groups"></a>Veidošanas bloku grupas

Veidošanas bloki ir rindu definīcijas, kolonnu definīcijas, pārskata koku definīcijas un pārskatu definīcijas, kuras izveidojat pārskatam. Veidošanas bloku grupas ir definīciju un dimensiju kopu kolekcijas, kas ir saistītas ar uzņēmumu. Veidošanas bloku grupas var atbilst noteiktam uzņēmumam, vai vairāki uzņēmumi var koplietot vienu un to pašu veidošanas bloku kopu. Ja kādiem no jūsu uzņēmumiem ir citi kontu plāni, katram uzņēmumam varat izvēlēties izmantot atšķirīgu veidošanas bloku grupu. Varat arī nosaukt visus atsevišķos veidošanas blokus tā, lai to nosaukumi atspoguļotu, kuram uzņēmumam tie atbilst.
### <a name="create-a-building-block-group"></a>Veidošanas bloku grupas izveide

1.  Atskaišu veidotāja izvēlnē **Uzņēmums** noklikšķiniet uz **Veidošanas bloku grupas**.
2.  Dialoglodziņā **Veidošanas bloku grupas** noklikšķiniet uz **Jauns**.
3.  Ievadiet unikālu veidošanas bloku grupas nosaukumu un aprakstu. Katrā laukā var būt ne vairāk par 256 rakstzīmēm. (Ieskaitot atstarpes.)
4.  Noklikšķiniet uz **Labi**, lai izveidotu jauno veidošanas bloku grupu.

### <a name="assign-a-building-block-group"></a>Veidošanas bloku grupas piesaiste

Kad esat izveidojis bloku grupu, tā ir jāpiešķir vismaz vienam uzņēmumam. Pēc tam varat izveidot atskaites, rindas, kolonnas un atskaišu koka definīcijas un saglabāt tās šajā veidošanas bloku grupā. Pirms sākat tālāk aprakstīto procedūru, ir jāaizver visi veidošanas bloki.
1.  Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Uzņēmumi**.
2.  Dialoglodziņā **Uzņēmumi** atlasiet uzņēmumu, kuram piešķirt veidošanas bloku grupu.
3.  Noklikšķiniet uz **Modificēt**.
4.  Dialoglodziņa **Modificēt uzņēmumu** laukā **Veidošanas bloku grupa** atlasiet veidošanas bloku grupu, kuru vēlaties piešķirt uzņēmumam, vai noklikšķiniet uz vienuma **Jauns**, lai izveidotu jaunu veidošanas bloku grupu.
5.  Noklikšķiniet uz **Labi**, lai piešķirtu veidošanas bloku grupu.
6.  Noklikšķiniet uz **Aizvērt**, lai aizvērtu dialoglodziņu **Uzņēmumi**. Atlasītā veidošanas bloku grupa tagad ir piešķirta uzņēmumam. Tagad visas jaunās rindas definīcijas, kolonnas un citas definīcijas, kas tika izveidotas, būs daļa no veidošanas bloku grupas, kura ir piešķirta šim uzņēmumam. Varat arī importēt .tdbx failu vai pārskatu no citas sistēmas.

### <a name="view-a-building-block-group"></a>Veidošanas bloku grupas apskatīšana

Kad veidošanas bloku grupa ir izveidota un tiek izmantota, varat skatīt visus tai piešķirtos veidošanas blokus. Veidošanas bloku grupu varat arī eksportēt vai importēt, kā arī veidošanas bloku grupām varat veikt papildu uzturēšanu.
1.  Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Veidošanas bloku grupas**.
2.  Dialoglodziņā **Veidošanas bloku grupas** atlasiet apskatāmo veidošanas bloku.
3.  Noklikšķiniet uz **Skatīt**, lai atvērtu dialoglodziņu **Skatīt veidošanas bloku grupu**, kurā varat skatīt veidošanas bloku grupas saturu.
4.  Noklikšķiniet uz **Aizvērt**, lai aizvērtu dialoglodziņus.

### <a name="save-a-building-block-group-under-a-new-name"></a>Saglabāt veidošanas bloku grupu ar jaunu nosaukumu

Jau esošu veidošanas bloku grupu varat saglabāt ar jaunu nosaukumu. Pēc tam jauno veidošanas bloku grupu varat modificēt, nemainot sākotnējo veidošanas bloku grupu.
1.  Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Veidošanas bloku grupas**.
2.  Dialoglodziņā **Veidošanas bloku grupas** atlasiet veidošanas bloku grupu, kuru saglabāt ar jaunu nosaukumu.
3.  Noklikšķiniet uz **Saglabāt kā**.
4.  Ievadiet jaunu veidošanas bloku grupas nosaukumu un aprakstu.
5.  Noklikšķiniet uz **OK**. Jaunā veidošanas bloku grupa tiek attēlota dialoglodziņā **Veidošanas bloku grupas**.

### <a name="export-a-building-block-group"></a>Veidošanas bloku grupas eksportēšana

Varat eksportēt veidošanas bloku grupu vai konkrētus pārskatu veidošanas blokus no veidošanas bloku grupas. Varat izmantot eksportēto veidošanas bloku grupu kā rezerves veidošanas bloku grupu. Varat arī kopēt eksportētos datus no vienas veidošanas bloku grupas citā vai no vienas Finance and Operations instalācijas citā. Pārskatu veidotājā kopā ar veidošanas bloku grupu tiek ietverti arī ar atsauci izmantotie fontu stili un dimensiju kopas.
1.  Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Veidošanas bloku grupas**.
2.  Dialoglodziņā **Veidošanas bloku grupas** atlasiet eksportējamo veidošanas bloku grupu un tad noklikšķiniet uz vienuma **Eksportēt**.
3.  Dialoglodziņā **Eksportēt** atlasiet eksportējamās pārskatu definīcijas.
    -   Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    -   Lai eksportētu noteiktas atskaites, rindas, kolonnas, koku struktūras vai dimensiju kopas, noklikšķiniet uz atbilstošās cilnes un pēc tam atlasiet eksportējamos vienumus. Lai atlasītu vairākus cilnes vienumus, nospiediet un turiet taustiņu Ctrl. **Piezīme.** Kad atlasāt eksportējamās atskaites, tiek atlasītas arī saistītās rindas, kolonnas, koku struktūras un dimensiju kopas.

4.  Kad esat beidzis eksportējamo vienumu atlasīšanu, noklikšķiniet uz **Eksportēt**.
5.  Dialoglodziņā **Saglabāt kā** atlasiet atrašanās vietu, uz kuru eksportēt veidošanas bloku grupu.
6.  Laukā **Faila nosaukums** ievadiet faila nosaukumu. Atskaišu veidotājs automātiski pievieno faila nosaukuma paplašinājumu .tdbx.
7.  Noklikšķiniet uz **Saglabāt**. Veidošanas bloku grupa ir saglabāta jūsu norādītajā atrašanās vietā.

### <a name="import-a-building-block-group"></a>Veidošanas bloku grupas importēšana

Veidošanas bloku grupu varat importēt esošā veidošanas bloku grupā vai varat izveidot jaunu veidošanas bloku grupu šiem datiem. Visas importētās veidošanas bloku grupas saglabā savus oriģinālos fontu stilus un uzņēmuma atsauces, un iekļauj attiecīgās dimensiju kopas.
1.  Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Veidošanas bloku grupas**.
2.  Dialoglodziņā **Veidošanas bloku grupas** atlasiet veidošanas bloku grupu, uz kuru importēt veidošanas bloku grupu, un tad noklikšķiniet uz vienuma **Importēt**.
3.  Dialoglodziņā **Atvērt** atlasiet importējamo veidošanas bloku grupu un tad noklikšķiniet uz vienuma **Atvērt**.
4.  Dialoglodziņā **Importēt** atlasiet importējamās pārskatu definīcijas.
    -   Lai importētu visas atskaites definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    -   Lai importētu atsevišķus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet importējamos pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas.

5.  Kad esat beidzis importējamo vienumu atlasīšanu, noklikšķiniet uz **Importēt**.

### <a name="undo-a-checkout-of-a-building-block"></a>Veidošanas bloka izrakstīšanas atsaukšana

Kad atverat kādu veidošanas bloku, citiem lietotājiem ir tikai lasīšanas piekļuve attiecībā uz šo veidošanas bloku. Reizēm lietotāji aizmirst aizvērt kādu veidošanas bloku vai izslēdz savu sistēmu, neaizverot šo veidošanas bloku. Tāpēc šis veidošanas bloks paliek izrakstīts, un citi lietotāji to nevar atvērt. Šajās situācijās finanšu atskaišu veidošanas administrators var izmantot dialoglodziņu **Izrakstītie vienumi**, lai atgrieztu veidošanas blokus, kurus lietotāji ir atstājuši izrakstītā statusā. **Piezīme.** Lai atgrieztu veidošanas blokus, izmantojot dialoglodziņu **Izrakstītie vienumi**, jums ir nepieciešama administratora loma.
1.  Pārskatu veidotāja izvēlnē **Rīki** noklikšķiniet uz vienuma **Izrakstītie vienumi**.
2.  Dialoglodziņā **Izrakstītie vienumi** atlasiet **Rādīt vienumus no visiem lietotājiem**. Saraksts tiek atjaunināts, lai parādītu visus veidošanas blokus, kas ir izrakstīti, un lietotājus, kuri ir tos izrakstījuši.
3.  Atlasiet veidošanas bloku un tad noklikšķiniet uz **Atsaukt izrakstīšanu**.
4.  Noklikšķiniet uz **Jā**, lai atgrieztu veidošanas bloku.

# <a name="see-also"></a>Skatiet arī

[Finanšu pārskati](financial-reporting-intro.md)




