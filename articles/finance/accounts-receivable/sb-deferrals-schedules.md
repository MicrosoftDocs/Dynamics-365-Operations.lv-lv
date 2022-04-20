---
title: Atlikto maksājumu grafiki ieņēmumu un izdevumu atliktajiem izdevumiem
description: Šajā tēmā aprakstīti atlikto maksājumu grafiki ieņēmumu un izdevumu atlikto maksājumu sadaļā.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 953347500f83a4a16f43331b572d2029027a5f59
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557974"
---
# <a name="deferral-schedules"></a>Atlikšanas grafiki

Atlikto maksājumu grafiki tiek izveidoti pēc darbības iegrāmatošanas.

Var izmantot lapu Visi atlikto **maksājumu grafiki vai** Aktīvie **atlikto** maksājumu grafiki, lai pārskatītu informāciju par atlikto maksājumu grafiku. Parādītā informācija ir atkarīga no atlikto maksājumu grafika tipa (lineārā vai notikuma) un darbības tipa. Tas ietver atlikto maksājumu grafika rindas un atlikto maksājumu grafika kopsummas. Jūs variet izmantot lapu, lai modificētu atlikto maksājumu grafiku.

## <a name="recognize-revenue"></a>Ieņēmumu atzīšana

> [!NOTE]
> - Lai atpazītu ieņēmumus vienam atlikto maksājumu grafikam, sāciet ar 1. soli.
> - Lai atpazītu ieņēmumus vairākiem grafikiem, sāciet ar 2. soli.

1. Lapā Visi **atlikto maksājumu grafiki** režģī **Grafika** rindas atlasiet rindas, kuras vēlaties atpazīt, un pēc tam atlasiet **Atpazīt**.
2. Lapā Atpazīšanas **apstrāde** iestatiet atpazīšanas **darbības lauku**, lai izveidotu **atpazīšanas žurnālu**.
3. Laukā **Robeždats** atlasiet robeždatumu. Apstrādē tiks iekļautas tikai rindas, kuru beigu datums ir agrāks par atlasīto robeždatumu vai vienāds ar to.
4. Atlasiet **Filtru** un pievienojiet datu filtrus, lai sarakstā būtu tikai jums vēl derīgs ierakstu diapazons.
5. Atlasiet **Skatīt priekšskatījumu**, lai skatītu rindas.
6. Rindu sarakstā atlasiet visas rindas, kuras nevēlaties apstrādāt, un pēc tam atlasiet **Noņemt**.
7. Atlasiet, vai vēlaties apkopot atpazīšanas žurnāla ierakstu.
8. Lai apstrādātu **darbību**, sadaļā Darbības datums varat ignorēt darbības datumu ar noteiktu datumu. Darbības datumu var norādīt slēgtiem periodiem.
9. Lai apstrādātu kā paketes daļu, atlasiet **Pakete**. Dialoglodziņā Pakešapstrāde **iestatiet** paketes parametrus un pēc tam atlasiet Labi, **lai** atgrieztos lapā Atpazīšanas **apstrāde**. Ieņēmumu atzīšana tiks apstrādāta vēlāk, kad pakete tiks apstrādāta.
10. Atlasiet **Procesu**. Ja ne pievienot darbību paketei, visas rindas tiek nekavējoties apstrādātas. Pretējā gadījumā rindas tiks apstrādātas pēc paketes apstrādes.

## <a name="modify-a-schedule"></a>Grafika modificēšana

Lai modificētu atlikto maksājumu grafiku, sekojiet šiem soļiem.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku un pēc tam atlasiet Uzskaites **\> modificēšanas grafiks**.
2. **Lapā Modificēt grafiku** rediģējiet opcijas, ko vēlaties mainīt. Atkarībā no atlikto maksājumu grafika jūs nevarēsit rediģēt visas opcijas.
3. Atlasiet Priekšskatīt **,** lai pārskatītu atlikto maksājumu grafika izmaiņas.
4. Atlasiet **Labi**.

### <a name="straight-line-deferral-schedules"></a>Lineārā atlikto maksājumu grafiki

Ja atlikto maksājumu grafikam nav atpazītu vai ārēji grāmatotu rindu, var modificēt visu atlikto maksājumu grafiku, iekļaujot sākuma datumu.

Ja atlikto maksājumu grafikam ir kāda atpazīta vai ārēji grāmatota rinda un jūs modificējat atlikto maksājumu grafiku, atlikto maksājumu grafika iegūtā darbība ir atkarīga no atzīto rindu pārrēķināšanas datuma un atliktā maksājuma beigu datuma. Pēc noklusējuma pirmais neatpazītais periods nosaka atliktā maksājuma beigu datumu.

Lai izmantotu atpazīšanas datumu, atlasiet vienu no šīm vērtībām **laukā Plānošanas** sākums: 
- **Pieļaujamais** daudzums — summa, kas tiek pārrēķināta pēc visu atpazīto rindu pārrēķina.
- **Atcelšana –** visas rindas pēc pārrēķina datuma tiek apgrieztas, izmantojot norādīto žurnāla nosaukumu un grāmatošanas datumu. Summa pēc pārrēķināšanas datuma tiek pārrēķināta.

Ja tiek izmantota veidne, izlaistie periodi tiek ignorēti, un veidne tiek izmantota tikai beigu datuma aprēķinam.

### <a name="event-based-deferral-schedules"></a>Uz notikumu pamatotie atlikto maksājumu grafiki

Uz notikumu balstītam atlikto maksājumu grafikam var modificēt visas neatpazītās rindas.

Ja atlikto maksājumu grafikam ir kāda atpazīta vai ārēji grāmatota rinda, nav iespējams modificēt veidni un atlikto maksājumu grafika sadalījuma tipu. Modificējot esošo atlikto maksājumu grafiku, lauka Izveidot atsevišķus notikumus **vienībai vērtību nevar** mainīt.

Ja rinda tiek atpazīta vai grāmatota ārēji, tiek atzīmēta **izvēles** rūtiņa Atpazīts.

## <a name="modify-a-deferral-or-recognition-account"></a>Modificēt atlikto maksājumu vai atzīšanas kontu

Lai modificētu atlikto maksājumu vai atzīšanas kontu atlikto maksājumu grafikam, sekojiet šiem soļiem.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku un pēc tam atlasiet kontu **Uzskaites \> modificēšana**.
2. Lapā Mainīt **kontu** atlasiet kontu, kuru vēlaties mainīt (atliktais, īstermiņa vai atpazīšanas).
3. Laukā **Jauns** konts atlasiet jaunu kontu.
4. Atlasiet, vai konta izmaiņas veido korekciju žurnāla ierakstus.
5. Ja iepriekšējā darbībā iestatāt **opciju** Jā, **atlasiet žurnāla nosaukumu laukā Žurnāla** **nosaukums un laukā Darbības datums norādiet darbības** datumu.
6. Atlasiet **Labi**.

## <a name="put-a-deferral-schedule-on-hold"></a>Aizturēt atlikto maksājumu grafiku

Lai atlikto maksājumu grafiku aizturētu, veiciet šos soļus.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku un pēc tam atlasiet Aizturēt **aizturēšanu \>**.
2. Lapā Aizturēta **vieta** atlasiet, vai vēlaties pārsūtīt bilanci no atliktā maksājuma konta vai aizturēšanas konta.
3. Ja izvēlējāties pārsūtīt bilanci, **atlasiet** žurnāla nosaukumu laukā Žurnāla nosaukums, **·** **laukā Aizturēts konts atlasiet aizturēto kontu un laukā Darbības datums norādiet darbības** datumu.
4. Atlasiet **Labi**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Noņemt atlikto maksājumu grafika aizturēšanu

Lai noņemtu atlikto maksājumu grafiku no aizturēšanas, sekojiet šiem soļiem.

1. Sarakstā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku un pēc tam atlasiet Aizturēt aizturēšanu **\>**
2. Laukā **Žurnāla** nosaukums atlasiet žurnāla nosaukumu.
3. Laukā **Darbības** datums norādiet darbības datumu.
4. Atlasiet **Labi**.

## <a name="cancel-unrecognized-amounts"></a>Atcelt neatzītās summas

> [!NOTE]
> Visas rindas, kas ir jau atpazītas vai grāmatotas ārēji, tiek izslēgtas no šī procesa.

Lai atlikto maksājumu grafikā atceltu neatpazītās summas, sekojiet šiem soļiem.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku un pēc tam atlasiet **Atcelt \> neatpazītās summas**.
2. Lapā Atcelt **neatpazīto summu** atlasiet, vai vēlaties izveidot atcelšanas ierakstus.
3. Ja izvēlējāties izveidot atcelšanas ierakstus, **atlasiet** žurnāla nosaukumu laukā Žurnāla nosaukums, **·** **laukā Atcelšanas konts atlasiet atcelšanas kontu un laukā Darbības datums norādiet darbības** datumu.
4. Atlasiet **Labi**.

## <a name="cancel-a-completed-schedule"></a>Pabeigta grafika atcelšana

Izmantojiet lapu Visi **atlikto maksājumu grafiki,** lai atsauktu visas atpazītās vai ārēji grāmatotās summas un atceltu atlikto maksājumu grafiku, lai novērstu tālāku atpazīšanu.

Lai atceltu visu atlikto maksājumu grafiku, veiciet šādus soļus.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku un pēc tam atlasiet Atcelt **\> pabeigto grafiku**.
2. Lapā Atcelt **pilnīgu grafiku** atlasiet, vai vēlaties izveidot atcelšanas ierakstus.
3. Ja izvēlējāties izveidot atcelšanas ierakstus, **atlasiet** žurnāla nosaukumu laukā Žurnāla nosaukums, **·** **atlasiet kontu laukā Atcelšanas konts un laukā Darbības datums norādiet darbības** datumu.
4. Atlasiet **Labi**.

## <a name="reverse-transactions"></a>Transakciju atsaukšana

> [!NOTE]
> - Lai atsauktu ieņēmumu atzīšanu vienam atlikto maksājumu grafikam, sāciet ar 1. soli.
> - Lai atgrieztu ieņēmumu atzīšanu vairākiem grafikiem, sāciet ar 2. soli.

1. **Lapā Visi atlikto maksājumu grafiki** režģī **Grafika** rindas atlasiet rindas, kuras vēlaties atcelt un pēc **tam atlasiet Atcelt**.
2. Lapā Atpazīšanas **apstrāde** iestatiet atpazīšanas **darbības lauku anulētās** **atpazīšanas žurnālu**.
3. Laukā **Robeždats** atlasiet robeždatumu. Apstrādē tiks iekļautas tikai rindas, kuru beigu datums ir agrāks par norādīto robeždatumu vai vienāds ar to.
4. Atlasiet **Filtru** un pievienojiet datu filtrus, lai sarakstā būtu tikai jums vēl derīgs ierakstu diapazons.
5. Atlasiet **Skatīt priekšskatījumu**, lai skatītu rindas.
6. Rindu sarakstā atlasiet visas rindas, kuras nevēlaties apstrādāt, un pēc tam atlasiet **Noņemt**.
7. Lauki **Nosaukums** un **Apraksts** tiek automātiski atjaunināti ar noklusējuma žurnāla nosaukumu un aprakstu. Vērtības var mainīt pēc jūsu pieprasītā. Varat arī atlasīt, vai vēlaties apkopot atpazīšanas žurnāla ierakstu.
8. Lai apstrādātu **darbību**, sadaļā Darbības datums varat ignorēt darbības datumu ar noteiktu datumu. Darbības datumu var norādīt slēgtiem periodiem.
9. Lai apstrādātu kā paketes daļu, atlasiet **Pakete**. Dialoglodziņā Pakešapstrāde **iestatiet** paketes parametrus un pēc tam atlasiet Labi, **lai** atgrieztos lapā Atpazīšanas **apstrāde**. Apgrieztā ieņēmumu atzīšana tiks apstrādāta vēlāk, pēc paketes apstrādes.
10. Atlasiet **Labi**. Ja ne pievienot darbību paketei, visas rindas tiek nekavējoties apstrādātas. Pretējā gadījumā rindas tiks apstrādātas pēc paketes apstrādes.

## <a name="apply-or-unapply-a-credit-note"></a>Lietot kredīta notu vai noņemt no tās

Lai pielietotu kredīta notu, sekojiet šiem soļiem.

> [!NOTE]
> Kad izveidojat **kredīta** **·** **notu** no pārdošanas pasūtījuma transakciju atlikto maksājumu lapas un iestatāt opciju Pielāgot esošo grafiku uz Jā, kredīta nota automātiski tiek piemērota grafikam, kad tiek grāmatota kredīta nota.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku.
2. **Kredīta korekciju** sarakstā atlasiet rindu un pēc tam atlasiet **Lietot**.
3. Lapā Lietot **kredīta notu (atliktos maksājumus)** **norādiet pārrēķināšanas datumu laukā Pārrēķina datums** **un beigu datumu laukā Beigu** datums.
4. Virsraksta sarakstā **atlasiet** pārdošanas pasūtījumu, kuram **ir** kredīta notas.
5. **Rindu sarakstā** izvēlieties rindu.
6. Atlasiet **Labi**.
7. Atlasiet **Jā**.

> [!NOTE]
> Lai lietotu kredīta notu vairākiem atsevišķiem krājumiem no dažādiem rēķiniem, šīs darbības ir jāatkārto.

Lai atceltu kredīta notu, izpildiet šīs darbības.

1. Lapā Visi **atlikto maksājumu grafiki** atlasiet atlikto maksājumu grafiku.
2. **Kredīta korekciju** sarakstā atlasiet rēķinu un pēc tam atlasiet **Noņemt piestrādi**.
3. Atlasiet **Jā**.

## <a name="fields"></a>Lauki

Lapā **Visi atlikto maksājumu grafiki** ir iekļauti tālāk iekļautie lauki.

| Lauki | Apraksts |
|--------|-------------|
| **Galvene** | |
| **Ieplānot** | |
| Sadalījuma tips | Uz notikumiem balstītu atlikto maksājumu sadalījuma tips: procenti **vai** **summa**. |
| Pārklasificēšanas datums | <p>Jaunākais datums, kad tika apstrādāta atlikto maksājumu grafika īstermiņa pārklasificēšana. Šis datums tiek atjaunināts katru reizi **, kad atlikto maksājumu grafikam** tiek izmantota notikuma īstermiņa pārklasificēšana.</p>Šis lauks ir pieejams tikai tad, ja tiek lietoti atrites periodi vai fiksētā gada īstermiņa atliktā maksājuma metode. |
| **Konts** | |
| Atlikto maksājumu konts | Konts, kas tiek izmantots atlikto maksājumu summai. |
| Atzīšanas konts | Konts, kas tiek lietots atpazīšanas summai. |
| Atzīšanas veids | Atpazīšanas tips. |
| Sadales veids | Sadales veids. |
| **Darījums** | |
| Izveides avots | Avots, no kura tika izveidota darbība. |
| Darījuma veids | Darbības tips. |
| Pārdošanas pasūtījums | Pārdošanas pasūtījuma numurs. |
| Rēķins | Rēķina numurs. |
| Krājums | Krājuma numurs. |
| **Norēķinu grafiks** | |
| Norēķinu grafika numurs | Atbilstošā norēķinu grafika numurs. |
| Norēķinu rindas statuss | Atbilstošās norēķinu grafika rindas krājuma statuss. |
| Ārējās atsauces | Informācija par ārējām atsaucēm no norēķinu grafika: **ārējais** un **rindas numurs**. |
| Kopsummas | <p>Atlikto maksājumu grafika kopsummas:</p><ul><li>**Ilgtermiņa** – ilgtermiņa atlikto maksājumu summu summa. Šī vērtība ir **pieejama** **·** **tikai tad, ja īstermiņa atlikto maksājumu metodes lauks ieņēmumu un izdevumu atlikto maksājumu parametru lapā ir iestatīts** uz Nav vai īstermiņa summa ir lielāka par 0 (nulli).</li><li>**Īstermiņa** – īstermiņa atlikto maksājumu summu summa. Šī vērtība ir **pieejama** **·** **tikai tad, ja īstermiņa atlikto maksājumu metodes lauks ieņēmumu un izdevumu atlikto maksājumu parametru lapā ir iestatīts** uz Nav vai īstermiņa summa ir lielāka par 0 (nulli).</li><li>**Neatpazīta** – neatpazīto summu visām rindām.</li><li>**Pasaka** – ārēji grāmatoto summu summa visām rindām.</li><li>**Atpazīta** – visu rindu atzīto summu summa.</li><li>**Ārēji iegrāmatots un atpazīts** – ārēji grāmatoto un atpazīto apjomu summa visām rindām.</li><li>**Kopējā summa** – visu rindu kopsumma.</li></ul> |
| **Grafika rindas** | |
| Rinda | Rindas kārtas numurs. |
| Atlikšanas sākuma datums | Atliktā maksājuma grafika sākuma datums |
| Atlikšanas beigu datums | Atliktā maksājuma grafika beigu datums. |
| Summa | Atliktā maksājuma summa |
| Ārēji grāmatots | Vērtība, kas norāda, vai rinda ir grāmatota ārēji. |
| Atzīts | Vērtība, kas norāda, vai rinda ir atpazīta. |
| Žurnāla iedaļas numurs | Partijas numurs, ar kuru summa tika atpazīta. |
| Notikuma apraksts | Notikuma apraksts. Šis lauks ir pieejams tikai atlikto maksājumu grafikiem, kas pamatoti uz notikumiem. |
| **Kredīta korekcijas** | |
| Rēķins | <p>Rēķina numurs.</p><p>Šī vērtība norāda rēķinu kredīta notas korekcijai, kas jau ir piemērota atlikto maksājumu grafikam.</p> |
| Piemērotā summa | Kredīta korekcijas summa, kas jau piemērota atlikto maksājumu grafikam. |
| Lietošanas datums | Datums, kad tika lietota kredīta korekcija. |
| **Pielāgojums** | Korekcijas vērtības tiek parādītas tikai tad, ja atlikto maksājumu grafikam apstrādāts kredītrēķins. Ja kredīta nota nav apstrādāta, šīs vērtības tiek slēptas. |
| Korekcijas summa | Kopējā korekcijas summa, kas aprēķināta, kā *oriģinālā summa* – *grafika summa*. |
| Sākotnējais beigu datums | Atlikto maksājumu grafika sākotnējais beigu datums |
| Sākotnējā grafika summa | Sākotnējā atlikto maksājumu grafika kopsumma. |
