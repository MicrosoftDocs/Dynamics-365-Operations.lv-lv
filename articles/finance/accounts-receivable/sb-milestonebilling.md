---
title: Atskaites punktu veidnes
description: Šajā tēmā skaidrots, kā iestatīt pagrieziena punkta rēķina izrakstīšanu abonementa norēķinos.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ecc4ddbb4d22eefac36f8cf8205d3b6084bd7d9d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686496"
---
# <a name="milestone-billing"></a>Apmaksa pēc atskaites punktiem

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā definēt veidnes atskaites punkta rēķina funkcionalitātei Abonementa norēķinos. Katrai rindai atskaites punkta veidnē varat noteikt sadalījuma procentus vai summu. Pēc tam varat piešķirt atskaites punkta veidni norēķinu grafika krājumiem, kas izmanto atskaites punkta norēķinu funkcionalitāti.

## <a name="add-a-template"></a>Pievienot veidni

Lai pievienotu atskaites punkta veidni, sekojiet šiem soļiem.

1. Pārejiet uz **sadaļu Abonementa \> norēķini Periodisko līgumu \> norēķinu iestatīšanas \> atskaites punkta veidnes**.
2. Atlasiet **Jauna**.
3. Lauka Atskaites **punkta veidne** ievadiet jaunās veidnes unikālo identifikatoru.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Laukā **Sadalījuma** metode atlasiet sadalījuma metodi.
6. Nav **obligāti**: laukā Kopējā summa norādiet veidnes kopējo summu.
7. Lai pievienotu rindu, atlasiet **Pievienot**. Pēc tam **laukā** Krājuma kods atlasiet krājuma kodu jaunajai rindai.
8. Veiciet vienu no šīm darbībām atkarībā no vērtības, kas atlasīta laukā **Sadalījuma** metode:

    - Ja kā sadalījuma **metodi** atlasījāt Procentus, **laukā Procenti** norādiet katrai rindai sadalījuma procentus. Norādot procentus, procentu summai, kas tiek rādīta laukā Kopā **procenti**, jābūt vienādai ar **100**.
    - Ja kā sadalījuma **metodi** atlasījāt Mainīgā summa, **laukā** Summa norādiet katras rindas summu.
    - Ja kā sadalījuma **metodi** atlasījāt Vienāda summa, summa nav jānorāda. Katra rinda tiks atjaunināta ar pareiziem procentiem un summu, pamatojoties uz krājumu skaitu, kas ir pievienoti veidnei.

9. Atlasiet **Saglabāt**.

## <a name="delete-a-template"></a>Veidnes dzēšana

Lai dzēstu atskaites punkta veidni, sekojiet šiem soļiem.

1. Atlasiet vienu vai vairākas rindas dzēšamajām rindām un pēc tam atlasiet **Dzēst**.
2. Kad tiek piedāvāts apstiprināt darbību, atlasiet **Jā**.

## <a name="milestone-template-fields"></a>Atskaites punkta veidnes lauki

Atskaites **punkta veidnes lapā** ir šādi lauki.

| Lauks | Apraksts |
|-------|-------------| 
| Atskaites punkta veidne | Atskaites punkta veidnes unikālais identifikators. |
| Apraksts | Atskaites punkta veidnes apraksts. |
| Sadalījuma metode | <p>Atlasiet sadalījuma metodi:</p><ul><li>**Pabeigtības procenti** – kopējā pabeigtības vērtība tiek izmantota katrai rindai.</li><li>**Procenti** – sadalījumam var norādīt procentuālo summu. Visu procentu summai ir jābūt vienādai ar 100.</li><li>**Mainīga** summa – summu var norādīt sadalījumam. Sadalījuma summa tiek norādīta darbību līmenī.</li><li>**Vienāda summa** – sadalījuma procenti tiek automātiski aprēķināti un vienādi sadalīti starp krājumiem veidnē.</li></ul> |
| Kopsumma | Norādiet veidnes atskaites punkta summu. |
| **Līnijas** | |
| Krājuma numurs | Izvēlieties krājuma numuru atskaites punkta veidnei. |
| Preces nosaukums | Krājuma nosaukums. |
| Procentuālā vērtība | <p>Ievadiet rindas sadalījuma procentu likmi:</p><ul><li>Ja Sadalījuma **metodes lauks** ir iestatīts uz **Procenti**, norādiet rindas procentus.</li><li>Ja Sadalījuma **metodes lauks** ir iestatīts **uz** Vienāda summa, procenti tiek automātiski sadalīti vienādās daļās procentos, pamatojoties uz krājumu skaitu veidnē.</li></ul><p>Visu procentu summai ir jābūt vienādai ar 100.</p><p>Ja virsrakstā **ir** norādīta kopējā summa un rindas vērtība **procentos** tiek mainīta, Vērtība **Summa** tiek atjaunināta. Otrādi, ja maināt summas **vērtību**, procentu **vērtība** tiek atjaunināta.</p> |
| Summa | <p>Rindas sadalījuma summa:</p><ul><li>Ja Sadalījuma **metodes lauks** ir iestatīts **uz** Mainīgā summa, norādiet rindas summu.</li><li>Ja Sadalījuma **metodes lauks** **ir** iestatīts uz Vienāda summa, summa tiek automātiski sadalīta vienādās summās, pamatojoties uz krājumu skaitu veidnē un kopējo summas vērtību, **kas** norādīta galvenē.</li></ul><p>Visu summu summai jābūt vienādai ar **kopējo summas** vērtību, kas norādīta galvenē.</p><p>Ja virsrakstā **ir** norādīta kopējā summa un rindas vērtību **Summa** tiek mainīta, procentu **vērtība** tiek atjaunināta. Otrādi, ja maināt procentu **vērtību**, summa tiek **atjaunināta**.</p> |
| **Kopsummas** | |
| Kopējais procentuālais daudzums | Procentu summa. Visu procentu summai ir jābūt vienādai ar 100. |
| Kopsumma | Visu rindu **vērtību** Summa summa. Šai summai ir jābūt vienādai **ar** kopējo summas vērtību, kas norādīta galvenē. |
| Atlikusī summa | Atlikusī summa. Šī vērtība tiek aprēķināta, kā **kopējā** summas vērtība no virsraksta mīnus visu **rindu** Vērtību Summa summa.|

## <a name="milestone-allocation"></a>Atskaites punkta sadalījums

Pirms sākat lietot atskaites punkta funkcionalitāti, jāveic šie uzdevumi.

1. Pievienot vienu vai vairākas atskaites punkta veidnes.
2. Izveidojiet norēķinu grafika grupu. Norādiet **Atskaites punktu** kā krājuma tipu un atlasiet veidni.
3. Krājumu iestatīšanas **lapā** (Abonementa **norēķini \> Periodiskie līguma norēķinu \> iestatīšanas \>** krājumi) atlasiet krājumu saistību un vienības iestatījuma atskaites punkta veidni.

Pēc atskaites punkta veidņu, norēķinu grafika grupu un krājumu izveidošanas varat izveidot norēķinu grafiku, kas izmanto atskaites punkta funkcionalitāti.

Lai iestatītu norēķinu grafiku, kas izmanto atskaites punktus, sekojiet šiem soļiem.

1. **Norēķinu grafiku lapas visu/aktīvo** norēķinu **grafiku sarakstā** atlasiet **Jauns**.
2. **Lapā Visi norēķinu grafiki** izveidojiet jaunu norēķinu grafiku un norādiet debitora kontu un sākuma datumu.
3. Sadaļā Norēķinu **grafika rindas** atlasiet **Pievienot rindu**. Pēc tam pievienojiet krājuma numuru un iestatiet krājuma tipa **lauku** uz Atskaites **punktu**.

    Ja krājumam ir iestatīta noklusētā atskaites punkta veidne, atskaites punkta notikumi tiek automātiski pievienoti norēķinu grafika rindām. Atskaites punkta rindām beigu datumi ir tukši.

    Ja krājumam nav iestatīta atskaites punkta veidne, izvēlieties Atskaites **punkta sadalījumu**. Tad atskaites punkta iedalīšanas **lapā** izvēlieties atskaites punkta veidni un veiciet nepieciešamos atjauninājumus. Pēc tam **atlasiet Aizvērt**, lai atgrieztos norēķinu grafikā, un pabeidziet norēķinu grafika izveidi.

4. Lai izveidotu rēķinus norēķinu grafikam, jāatjaunina beigu datums katram atskaites punkta notikumam. Atsevišķam norēķinu grafikam varat atjaunināt atskaites punkta notikuma beigu datumu norēķinu grafika rindās. Lai atjauninātu vairākus norēķinu grafikus, atlasiet atjaunināt **pabeigšanas datuma procesu**.
5. Pēc beigu datuma atjaunināšanas varat izveidot rēķinu. Atsevišķam norēķinu grafikam atlasiet **Ģenerēt rēķinu** lapā **Visi norēķinu** grafiki. Lai izveidotu rēķinus vairākiem norēķinu grafikiem, atlasiet Ģenerēt rēķinu **vai Ģenerēt rēķinu** pakešveida **apstrādi zem Periodiskie** **uzdevumi**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Rediģēt atskaites punkta sadalījumu norēķinu grafika rindā

Lai rediģētu atskaites punkta sadalījumu norēķinu grafika rindā, sekojiet šiem soļiem.

1. Norēķinu grafika **lapas lapā** > **visi vai** **aktīvie norēķinu grafiki laukā Grafika** numurs atlasiet norēķinu grafika numuru.
2. Sadaļā Norēķinu **grafika rindas** ievadiet krājumu, kā vienību **norādiet atskaites** punktu un izvēlieties Atskaites **punkta sadalījumu**.
3. Laukā **Atskaites punkta** veidne izvēlieties atskaites punkta veidni.
4. Atlasiet **Procesu**. Atskaites punkta veidnes rindas tiek automātiski pievienotas norēķinu grafika rindām.

## <a name="milestone-allocation-fields"></a>Atskaites punkta sadalījuma lauki

Atskaites **punkta iedalīšanas** lapā ir šādi lauki.

| Lauks | Apraksts |
|-------|-------------|
| Pamatkrājums | Pamatelementa krājuma kods. |
| Pilna cena | <p>Krājuma paplašinātā cena Vērtība atbilst norēķinu **grafika rindas** neto summas vērtībai.</p></p>Atskaites punkta pamatelementam noklusējuma vērtība ir atskaites **punkta** veidnei noteiktā kopējās summas vērtība. Ja kopsumma ir 0 (nulle), noklusējuma vērtība ir norēķinu **grafika** rindas neto summas vērtība.</p> |
| Atskaites punkta veidne | Rindas krājuma atskaites punkta veidnes ID. |
| Veidnes apraksts | Atskaites punkta veidnes apraksts. |
| Sadalījuma metode | Sadalījuma metode, kas tiek izmantota atskaites punkta veidnei. |
| **Līnijas** | Noklusētās vērtības visām rindām ir balstītas uz izvēlēto atskaites punkta veidni. Ja nepieciešams, tos var mainīt. |
| Krājuma numurs | Krājuma numurs atskaites punkta sadalījuma veidnei. |
| Preces nosaukums | Preces nosaukums. |
| Procentuālā vērtība | <p>Rindas sadalījuma procenti. Visu procentu summai ir jābūt vienādai ar 100.</p><p>Mainot rindas **procentuālo vērtību**, tiek atjaunināta **neto** summas vērtība. Otrādi, ja tiek mainīta neto **summas vērtība**, procentu **vērtība tiek** atjaunināta.</p> |
| Neto summa | <p>Rindas sadalījuma summa. Visu rindu neto summu summai jābūt vienādai ar galvenē **norādīto** paplašinātās cenas vērtību.</p><p>Mainot rindas neto **summas vērtību**, tiek atjaunināta **procentu** vērtība. Otrādi, ja maināt procentu **vērtību, neto** summas vērtība tiek **atjaunināta**.</p> |
| **Kopsummas** | |
| Procenti kopā | Visu rindu **vērtību** Procentos summa. Šai summai ir jābūt vienādai ar 100. |
| Kopsumma | Neto summas **vērtību summa** visām rindām. Šai summai jābūt vienādai **ar paplašinātās** cenas vērtību, kas norādīta galvenē. |
| Atlikusī summa | Atlikusī summa. Šī vērtība tiek aprēķināta, no **virsraksta atņemot** kopējo neto summas vērtību **no virsraksta paplašinātās** cenas vērtību visās rindās. Beigu summai ir jābūt 0 (nulle). |
