---
title: Finanšu pārskata komponenti
description: Šajā rakstā ir izklāstīts, kā finanšu atskaišu veidošanā tiek izmantoti atskaišu definīciju komponenti jeb veidošanas bloki.
author: aprilolson
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: cb4c8f28848659557e3d60a130506ec3ae61b7f8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743430"
---
# <a name="financial-report-components"></a>Finanšu pārskata komponenti

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izklāstīts, kā finanšu atskaišu veidošanā tiek izmantoti atskaišu definīciju komponenti jeb veidošanas bloki. Šajos veidošanas blokos ir iekļautas rindas definīcijas, kolonnas definīcijas un atskaišu koka definīcijas. Šajā rakstā ir paskaidrots, kā sakārtot un bloķēt veidošanas blokus.

Finanšu atskaišu veidotāja dizains tika veidots ar mērķi sadalīt informāciju vismazākajos komponentos jeb veidošanas blokos, lai šos komponentus varētu pēc nepieciešamības jaukt un kombinēt. Tāpēc pārskatu formatējums ir nošķirts no finanšu datiem un varat mainīt pārskata noformējumu, neizmainot finanšu datus savā Microsoft Dynamics ERP sistēmā. Izmantojot šo veidošanas bloku pieeju, ir iespējams kombinēt tekstu, summas un aprēķinus, lai veidotu jums nepieciešamās atskaites. Turklāt šī elastība atbalsta radošu pieeju, atvieglojot darbību apskatīšanu dažādos veidos. Atsevišķie atskaites definīcijas veidošanas bloki ir līdzīgi trīsdimensiju izklājlapai, bet tie sniedz vairāk iespēju. Atskaites definīcija norāda rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, kas ir jāizmanto šai atskaitei. Tas iekļauj arī informāciju par to, kur glabāt ģenerēto atskaiti un kā to formatēt.

## <a name="building-blocks-of-a-report"></a>Pārskata veidošanas bloki

| Veidošanas bloks            | apraksts | Plašāka informācija |
|---------------------------|-------------|----------------------|
| Rindas definīcija            | Rindas definīcija atskaitē definē aprakstošās rindas (piemēram, algas vai pārdošana). Tajā ir uzskaitītas arī segmentu vērtības vai dimensijas, kas satur vērtības katram rindas vienumam un ietver rindu formātus un aprēķinus. | [Rindu definīcijas](row-definitions-financial-reporting.md) |
| Kolonnas definīcija         | Kolonnas definīcija nosaka periodu, kas jāizmanto, kad dati tiek izgūti no finanšu dimensijām. Tas ietver arī kolonnu formatējumu un aprēķinus. | [Kolonnu definīcijas](column-definitions-financial-reports.md) |
| Pārskatu koka definīcija | Pārskatu koka definīcija ir līdzīga uzņēmuma diagrammai. Tā satur atsevišķas pārskata vienības, kas pārstāv katru diagrammas lauku. Šīs vienības var būt konkrētas finanšu datu grupas vai augstāka līmeņa vienības, kurās ir apkopoti dati no citām pārskatu vienībām. | [Pārskata koku definīcijas](financial-reporting-tree-definitions.md) |
| Pārskata definīcija         | Pārskata definīcija izmanto rindu definīciju, kolonnu definīciju un papildu pārskata koka definīciju, lai izveidotu pārskatu. Tā arī sniedz papildu opcijas un iestatījumus, ko varat izmantot atskaites pielāgošanai. | [Pārskata definīcija](design-financial-report-definitions.md) |

Ja jums nav pieredzes atskaišu veidošanā, jums var noderēt atskaišu vednis, lai ātri izveidotu atskaites definīciju, kuru vēlāk varat pielāgot. Ja jums ir pieredze atskaišu veidošanā un vēlaties izmantot plašākas atskaišu noformēšanas iespējas, varat kombinēt jaunus vai jau eksistējošus veidošanas blokus, lai izveidotu jaunu atskaites definīciju. Lai izveidotu kvalitatīvas atskaites, jums nav pilnībā jāizprot visas pieejamās atskaites definīcijas opcijas. Iepazīstoties ar pārskatu izveides procesu, varat izvērst savas pārskatu definīcijas, lai izmantotu papildu funkcijas. Kad esat izveidojis vienkāršu atskaiti, varat pielāgot atskaites definīciju un jebkuru no atskaites definīcijas veidošanas blokiem.

## <a name="organize-the-building-blocks"></a>Veidošanas bloku organizēšana
Izmantojiet mapes, lai organizētu savus veidošanas blokus pārskatu veidotājā. Visas mapes raksturo to ietverto veidošanas bloku tips. Piemēram, visas mapes, kas satur rindas definīcijas, atrodas atskaišu veidotāja rūtī **Rindas definīcijas**.

### <a name="create-a-folder"></a>Mapes izveide

1. Pārskatu veidotājā atlasiet veidošanas bloka tipu, lai sakārtotu navigācijas rūti. Piemēram, lai kārtotu rindu definīcijas, noklikšķiniet uz **Rindu definīcijas**.
2. Navigācijas rūtī atlasiet eksistējošu mapi, kurā izveidot jauno mapi, un pēc tam izpildiet vienu no šīm darbībām:

    - Ar peles labo pogu noklikšķiniet uz pamata mapes un pēc tam noklikšķiniet uz **Jauna mape**.
    - Atlasiet pamata mapi, noklikšķiniet uz **Fails** un pēc tam noklikšķiniet uz **Jauna mape**.

3. Kad tiek parādīta jaunā mape, ievadiet jaunās mapes nosaukumu un pēc tam nospiediet taustiņu Enter.

## <a name="lock-a-building-block"></a>Veidošanas bloka bloķēšana
Varat izveidot paroli, lai bloķētu vai palīdzētu aizsargātu kādu veidošanas bloku. Šādi varat paaugstināt atskaites komponenta drošības līmeni, bet nemainot visas sistēmas drošības iestatījumus. Parole var palīdzēt aizsargāt veidošanas bloka informāciju, kas ir svarīga jūsu mēneša beigu atskaišu veidošanas procesā. Jebkuras lomas lietotājs var bloķēt kādu veidošanas bloku. Taču citiem lietotājiem vienmēr ir tikai lasīšanas piekļuve attiecībā uz bloķētiem komponentiem. Lietotāji var atvērt, mainīt un saglabāt bloķēto komponentu ar jaunu nosaukumu. Lietotājs, kuram ir administratora loma, vienmēr var piekļūt bloķētam veidošanas blokam un mainīt to.

1. Atskaišu veidotājā atveriet bloķējamo atskaites komponentu, piemēram, rindas definīciju, kolonnas definīciju, atskaites definīciju vai atskaišu koka definīciju.
2. Izvēlnē **Rīki** noklikšķiniet uz **Aizsargāt/noņemt aizsardzību**. Varat arī rīkjoslā noklikšķināt uz **Aizsargāt/noņemt aizsardzību** (slēdzenes ikonas).
3. Dialoglodziņā **Aizsargāt** ievadiet un apstipriniet paroli un pēc tam noklikšķiniet uz **Labi**. Kad atvērts veidošanas bloks ir bloķēts, slēdzenes ikona rīkjoslā ir izcelta.

Lai atbloķētu kādu bloķētu veidošanas bloku, atveriet šo veidošanas bloku un pēc tam rīkjoslā noklikšķiniet uz ikonas **Aizsargāt/noņemt aizsardzību**. Varat arī izvēlnē **Rīki** noklikšķināt uz **Noņemt aizsardzību**.

## <a name="building-block-groups"></a>Veidošanas bloku grupas

Veidošanas bloki ir rindu definīcijas, kolonnu definīcijas, pārskata koku definīcijas un pārskatu definīcijas, kuras izveidojat pārskatam. Veidošanas bloku grupas ir definīciju un dimensiju kopu kolekcijas.

### <a name="view-a-building-block-group"></a>Veidošanas bloku grupas skatīšana

Varat skatīt visus veidošanas blokus, kas ir piešķirti veidošanas bloku grupai. Varat arī eksportēt vai importēt veidošanas bloku grupu.

1. Pārskatu veidotāja izvēlnē **Uzņēmums** noklikšķiniet uz vienuma **Veidošanas bloku grupas**.
2. Dialoglodziņā **Veidošanas bloku grupas** atlasiet apskatāmo veidošanas bloku.
3. Noklikšķiniet uz **Skatīt**, lai atvērtu dialoglodziņu **Skatīt veidošanas bloku grupu**, kurā varat skatīt veidošanas bloku grupas saturu.
4. Noklikšķiniet uz **Aizvērt**, lai aizvērtu dialoglodziņus.

### <a name="export-a-building-block-group"></a>Veidošanas bloku grupas eksportēšana

Varat eksportēt veidošanas bloku grupu vai konkrētus pārskata veidošanas bloku grupā ietvertos veidošanas blokus. Eksportēto veidošanas bloku grupu var izmantot kā dublējumkopiju. Varat arī kopēt eksportētos datus no vienas instalācijas uz citu. Pārskatu veidotājā kopā ar veidošanas bloku grupu ir ietverti arī ar atsauci norādītie fontu stili un dimensiju kopas.

1. Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Veidošanas bloku grupas**.
2. Dialoglodziņā **Veidošanas bloku grupas** atlasiet eksportējamo veidošanas bloku grupu un pēc tam noklikšķiniet uz **Eksportēt**.
3. Dialoglodziņā **Eksportēt** atlasiet eksportējamās pārskatu definīcijas.

    - Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    - Lai eksportētu noteiktas atskaites, rindas, kolonnas, koku struktūras vai dimensiju kopas, noklikšķiniet uz atbilstošās cilnes un pēc tam atlasiet eksportējamos vienumus. Lai atlasītu vairākus cilnes vienumus, nospiediet un turiet taustiņu Ctrl.

    > [!NOTE]
    > Ja eksportēšanai tiek atlasīti pārskati, tiek atlasītas arī saistītās rindas, kolonnas, koki un dimensiju kopas.

4. Kad esat beidzis eksportējamo vienumu atlasīšanu, noklikšķiniet uz **Eksportēt**.
5. Dialoglodziņā **Saglabāt kā** atlasiet atrašanās vietu, uz kuru eksportēt veidošanas bloku grupu.
6. Laukā **Faila nosaukums** ievadiet faila nosaukumu. Atskaišu veidotājs automātiski pievieno faila nosaukuma paplašinājumu .tdbx.
7. Noklikšķiniet uz **Saglabāt**. Veidošanas bloku grupa ir saglabāta jūsu norādītajā atrašanās vietā.

### <a name="import-a-building-block-group"></a>Veidošanas bloku grupas importēšana

Varat importēt veidošanas bloku grupu esošā veidošanas bloku grupā. Visas importētās veidošanas bloku grupas saglabā savus oriģinālos fontu stilus un uzņēmuma atsauces, un iekļauj attiecīgās dimensiju kopas.

1. Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Veidošanas bloku grupas**.
2. Dialoglodziņā **Veidošanas bloku grupas** atlasiet veidošanas bloku, kurā importēt veidošanas bloku grupu, un pēc tam noklikšķiniet uz **Importēt**.
3. Dialoglodziņā **Atvērt** atlasiet importējamo veidošanas bloku grupu un pēc tam noklikšķiniet uz **Atvērt**.
4. Dialoglodziņā **Importēt** atlasiet importējamās pārskatu definīcijas.

    - Lai importētu visas atskaites definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    - Lai importētu atsevišķus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet importējamos pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas.

5. Kad esat beidzis importējamo vienumu atlasīšanu, noklikšķiniet uz **Importēt**.

### <a name="undo-a-checkout-of-a-building-block"></a>Veidošanas bloka izrakstīšanas atsaukšana

Kad atverat kādu veidošanas bloku, citiem lietotājiem ir tikai lasīšanas piekļuve attiecībā uz šo veidošanas bloku. Reizēm lietotāji aizmirst aizvērt kādu veidošanas bloku vai izslēdz savu sistēmu, neaizverot šo veidošanas bloku. Tāpēc šis veidošanas bloks paliek izrakstīts, un citi lietotāji to nevar atvērt. Šajās situācijās finanšu atskaišu veidošanas administrators var izmantot dialoglodziņu **Izrakstītie vienumi**, lai atgrieztu veidošanas blokus, kurus lietotāji ir atstājuši izrakstītā statusā.

> [!NOTE]
> Lai atzīmētu veidošanas blokus, izmantojot dialoglodziņu **Paņemtie krājumi**, ir jābūt piešķirtai administratora lomai.

1. Pārskatu veidotāja izvēlnē **Rīki** noklikšķiniet uz vienuma **Izrakstītie vienumi**.
2. Dialoglodziņā **Paņemtie krājumi** atlasiet **Rādīt krājumus no visiem lietotājiem**. Saraksts tiek atjaunināts un tiek parādīti visi paņemtie veidošanas bloki un to lietotāji.
3. Atlasiet veidošanas bloku un pēc tam noklikšķiniet uz **Atsaukt paņemšanu**.
4. Noklikšķiniet uz **Jā**, lai piešķirtu veidošanas bloku.

## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskati](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]