---
title: Norēķinu grafika pārskats
description: Šajā tēmā skaidrots, kā izveidot, dzēst un rediģēt norēķinu grafikus.
author: JodiChristiansen
ms.date: 02/09/2022
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
ms.openlocfilehash: e42be3f359e96f0861354ebc8e1e9c87478a5d89
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182716"
---
# <a name="billing-schedule-overview"></a>Norēķinu grafika pārskats

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

**Norēķinu grafika lapā** varat izveidot, dzēst vai rediģēt norēķinu grafikus. Varat arī pārskatīt norēķinu grafiku sarakstu. Veidojot norēķinu grafiku, tā noklusējuma vērtības nosaka norēķinu grupa, kas ar to ir saistīta. Papildinformācija ir iestatīta periodisko **līgumu norēķinu parametru** lapā.

## <a name="create-a-billing-schedule"></a>Izveidot norēķinu grafiku

Lai izveidotu rēķinu izrakstīšanas grafiku, veiciet šādas darbības.

1. **Norēķinu grafika lapā** atlasiet **Jauns**.
2. Rēķina grafika **izveides** dialoglodziņa laukā Norēķinu **grafika grupa** atlasiet norēķinu grafika grupu.
3. Laukā **Debitora** konts atlasiet debitora kontu.
4. Laukā **Sākuma** datums atlasiet sākuma datumu un pēc tam **laukā Periodu skaits** ievadiet periodu skaitu. Beigu **datuma lauks** tiek atjaunināts, pamatojoties uz ievadīto periodu skaitu. Ja atjaunināt lauku Norēķinu **beigu datums**, periodu skaits tiek **atjaunināts** uz **0** (nulle).
5. Atlasiet **Labi**.
6. Norēķinu grafika **lapas cilnes Vispārīgi** **laukā Apraksts** **ievadiet norēķinu grafika aprakstu.**
7. Laukā **Atskaites punkta veidne** izvēlieties atskaites punkta veidni atskaites punkta **norēķiniem**.

Lauki, piemēram **, rēķina konts** **un valūtas** kods, tiek atjaunināti ar informāciju no debitora.

Norēķinu **biežuma un** norēķinu **intervāla** lauki tiek iestatīti automātiski, pamatojoties uz atlasīto norēķinu grafika grupu.

8. Lai izveidotu atsevišķus rēķinus, iestatiet **opciju Rēķins** atsevišķi uz **Jā**.
9. Lai automātiski atjaunotu norēķinu grafiku pēc beigu norēķinu perioda, **·** **iestatiet** opciju Atjaunot automātiski uz Jā un pēc tam iestatiet rindas, **kas jāpievieno katrai atjaunošanai.**

Lauki **Parametri** tiek iestatīti automātiski, pamatojoties uz lapā Periodiskie **līguma rēķinu parametri iestatītajām** vērtībām.

10. Lai rēķina grafika summu izplānotu, iestatiet opciju Prorate **partial periodi** uz **Jā**.
11. Lai norēķinu grafika detaļu rindas līdzinātu ar mēneša beigām, iestatiet **opciju Līdzināt uz mēnesi** uz **Jā**.
12. Laukos **Līguma sākuma** datums **un Līguma beigu** datums ievadiet līguma sākuma un beigu datumus. Šie datumi ir tikai informācijai.

**Laukā** Maksājums ir norādīta debitora maksājuma informācija. Ja dokumenta rinda ir aizturēta vai pārtraukta, maksājuma informāciju nevar mainīt.

> [!NOTE]
> Kad jūs konsolidējiet rēķinus pēc krājuma, jāatbilst maksājuma **nosacījumu**, metodes **un** Norēķinu **grafika lauku** vērtībai. Pretējā gadījumā rēķinus nevar konsolidēt.

13. Cilnē Adrese **var** pārskatīt un atjaunināt laukus Piegādes **adrese un** Rēķina **adrese**.
14. Cilnē Kontaktinformācija **var** saistīt gala lietotāja kontu ar rēķinu izrakstīšanas grafiku.
15. Kontaktinformācijas **laukos** varat ievadīt kontaktu, e-pasta adresi un interneta adresi.
16. Lai izsekotu partnera komisijas informāciju, iestatiet partnera **konta un** partnera **komisijas likmes laukus**. Šie lauki ir tikai informācijai.
17. **Cilnē Kopsumma** var skatīt dažādas rēķinu grafikam aprēķinātās kopsummas.
18. Cilnē Aizturēt **var** skatīt audita informāciju par to, kad norēķinu grafiks tika aizturēts, kad aizturēšana tika noņemta.
19. Cilnē Darba **attiecību** pārtraukšana var skatīt to darba attiecību pārtraukšanas vēsturi, kas piemērota rēķinu grafikam vai noņemt no tā.
20. Atlasiet **Saglabāt**.
21. Kopsavilkuma cilnē **Norēķinu grafika** rindas atlasiet **Pievienot rindu**.
22. Laukā **Krājuma** kods atlasiet krājuma kodu. Ja pievienotais krājums ir ieņēmumu sadalāmais pamat krājums, rindas automātiski tiek atjauninātas ar pakārtotajām precēm. Ieņēmumu sadalīumā var labot tikai pamatvienumu. Pēc tam visi pakārtotie krājumi tiek attiecīgi atjaunināti.
23. Laukā **Krājuma** tips atlasiet krājuma tipu.
24. Atjauniniet sākuma un beigu datumus.
25. Pirms rēķinu izveides varat mainīt norēķinu biežumu, atjauninot lauku **Norēķinu** biežums. Kad norēķinu grafika pirmais rēķins ir izveidots, norēķinu biežumu nevar mainīt.
26. **Laukā** Vienība atlasiet krājuma mērvienību.
27. Laukā **Cenu noteikšanas** metode atlasiet krājuma cenu noteikšanas metodi.

Lauks **Vienības cena** tiek automātiski iestatīts no krājumiem. Tomēr, jūs variet atjaunināt to, ja jūs maināt cenu noteikšanas metodi uz **Flat**.

## <a name="remove-a-line-item"></a>Dokumenta rindas noņemšana

Lai noņemtu krājumu no norēķinu grafika, sekojiet šiem soļiem.

1. **Norēķinu grafika lapas** laukā Grafika **numurs** atlasiet rediģējamā norēķinu grafika numuru.
2. Kopsavilkuma cilnē **Norēķinu grafika rindas** atlasiet dzēšamo rindu un pēc tam atlasiet **Noņemt**.
3. Atlasiet **Saglabāt**.

Pārējā tēmā ir aprakstītas darbības un detalizēta informācija, kas ir pieejama kopsavilkuma **cilnes Norēķinu grafika rindas** rindās.

## <a name="billing-schedule-line-actions"></a>Norēķinu grafika rindas darbības

Pogas norēķinu grafika rindu **kopsavilkuma cilnē ļauj** jums piemērot darbības atsevišķām rindām.

| Poga | Apraksts |
|--------|-------------|
| Pievienot rindu | Pievienot rindu norēķinu grafikam. |
| Pievienot no krājumu saraksta | Pievienot norēķinu grafikam vairākus krājumus, atlasot tos sarakstā. |
| Aizvākt | <p>Noņemiet atlasīto rindu no norēķinu grafika.</p><p>Krājumiem, kas ir daļa no ieņēmumu sadalīšanas, var noņemt tikai pamatobjektu. Pēc tam visi saistītie pakārtotie krājumi tiek noņemti automātiski.</p> |
| Skatīt norēķinu detalizēto informāciju | Skatiet norēķinu informāciju. |
| Pārtraukt darba attiecības | <p>Pārtraukt atlasītās rindas. Šī poga ir pieejama tikai tad, ja atlasītajām rindām ir statuss **Aktīvs**.</p><p>Krājumiem, kas ir daļa no ieņēmumu sadalīšanas, varat pārtraukt darba attiecības tikai pamatvienības.</p> |
| Noņemt izbeigšanu | <p>Noņemiet izbeigšanu no atlasītajām rindām. Šī poga ir pieejama tikai tad, ja atlasītajām rindām ir statuss **Izbeigts**.</p><p>Krājumiem, kas ir daļa no ieņēmumu sadalīšanas, darba attiecību pārtraukšanu var noņemt tikai no pamatvienības.</p> |
| Ievietot aizturēšanu | <p>Atlasiet detalizētu informāciju par atlasītās rindas aizturēšanu.</p><p>Krājumiem, kas ir daļa no ieņēmumu sadalīšanas, varat aizturēt tikai pamatobjektu.</p> |
| Noņemt aizturēšanu | <p>Aizvāciet aizturēšanu no atlasītās rindas.</p><p>Krājumiem, kas ir daļa no ieņēmumu sadalīšanas, varat noņemt aizturēšanu tikai no pamatvienības.</p> |
| Eskalācija un atlaide | Šī poga nav pieejama krājumiem, kas ir daļa no ieņēmumu sadalīšanas, izņemot pamatelementus, kuros ieņēmumu sadalīšanai tiek izmantota **nulles summas** sadalījuma metode. |
| Atlikšanas | <p>Ievadiet atlikto maksājumu opcijas atlasītajai rindai.</p><p>Šī poga nav pieejama pamatelementiem ieņēmumu saņēmumos.</p> |
| Atskaites punkta sadalījums | <p>Pārskatiet un atjauniniet atskaites punkta sadalījuma informāciju atlasītajai rindai.</p><p>Šī poga ir pieejama tikai tad, kad norēķinu grafika rindas vienība ir atskaites punkta krājums.</p> |
| Atbalsts un atjaunošana | <p>Pārskatiet un atjauniniet atlasītās rindas informāciju par atbalstu un atjaunošanu.</p><p>Šī poga ir pieejama tikai tad, ja norēķinu grafika rindas vienums ir atbalsts vai atjaunošanas krājums.</p> |
| Parādīt dimensijas | Rādīt vai slēpt dimensiju kolonnas, kas tiek parādītas norēķinu **grafika rindu** režģī. |
| Aprēķināt cenu par vienību | <p>Aprēķiniet krājuma vienības cenu, lai debitors varētu maksāt līguma summu par maksājumiem (piemēram, katru dienu, katru mēnesi, reizi ceturksnī, pusgadā vai reizi gadā). Varat atlasīt līguma cenu un cenu biežumu.</p><p>Var apskatīt izmaiņu audita pierakstu: vecā līguma cena un biežums, jaunā līguma cena un biežums, lietotājs, kurš veica izmaiņas, un izmaiņas datums un laiks.</p> |
| Saskaņošanas datums | <p>Norādiet atjaunošanas krājumu līdzināšanas datumu.</p><p>Ja laukā Krājumu grupa **atlasāt** krājumu grupu, visi krājumi norēķinu grafikā izmanto pirmās krājumu grupas krājuma līdzinājuma datumu. Ja lauks **Krājumu grupa** ir tukšs, var norādīt līdzinājuma datumu, ko izmantot visiem krājumiem.</p><p>Šī poga ir pieejama tikai tad, ja lauks **Norēķinu biežums** ir iestatīts kā **Ikgadēji**.</p> |
| Rēķinos neiekļautie ieņēmumi | <p>Iestatiet krājumu, lai izmantotu nenosācītu ieņēmumu līdzekli. Pēc tam var norādīt krājuma nenoslietos ieņēmumus un nenoārdāmās atlaides kontus.</p><p>Šī poga ir pieejama tikai krājumiem, kuru lauka Preces tips **iestatījums ir Standarta** **.** Tas nav pieejams esošiem norēķinu grafikiem vai norēķinu grafika rindām, kurās rēķins jau ir izveidots.</p> |
| Pievienot ieņēmumu sadales pakārtoto daļu | <p>Atlasiet pakārtoto krājumu, ko pievienot pārdošanas pasūtījumam.</p><p>Šī poga ir pieejama tikai pamatelementiem ieņēmumu saņēmumos.</p> |
| Potenciālo iepirkuma cenu kalkulācijas opcijas | Labot krājuma cenu noteikšanas opcijas. |

## <a name="billing-schedule-line-details"></a>Norēķinu grafika rindas detalizēta informācija

Kad jūs izvēlieties rindu Norēķinu grafika **rindu kopsavilkuma** cilnē, jūs variet skatīt detalizētu informāciju par šo rindu. Šīs detaļas tiek sadalītas dažādās cilnēs.

### <a name="general-tab"></a>Cilne Vispārīgi

Tālākā informācija ir pieejama cilnē **Vispārīgi**.

| Lauks vai sadaļa | Apraksts |
|------------------|-------------|
| Lietojums | <p>Šajā sadaļā sniegta informācija par lietošanas krājumiem. Tajā ir šādi lauki:</p><ul><li>**Lietojuma** identifikators – mērītāja vai lietošanas krājuma identifikators.</li><li>**Lasīšanas opcija** – lietojuma lasījuma opcija: lasīšana **vai** **patēriņš**.</li><li>**Aprēķinātais** patēriņš – norāda lietošanas krājuma novērtēto patēriņu, kam ir periodi, kuros rēķins nav izveidots. Lapā Norēķinu **detalizēta informācija** varat pārskatīt norēķinu informācijas rindas aprēķinātā patēriņam.</li></ul> |
| Ārējās atsauces\* | Šajā sadaļā ir iekļauti **ārējo** un **rindu numuru** lauki, kur var norādīt ārējo atsauču informāciju. |
| Atskaites punkts | <p>Šī sadaļa sniedz informāciju par atskaites punkta krājumiem. Tas satur lauku **Plānotais pabeigšanas** datums, kas rāda krājuma pabeigšanas datumu.</li></ul> |
| Teksts | Rindas komentārs. Teksts ir tulkots debitora vai juridiskas personas noklusējuma valodā. |
| Krājumu grupa | Rindas krājuma grupa. |
| Saskaņošanas datums | Norēķinu grafika līdzinājuma datums. |

\* Konsolidējot rēķinus pēc krājuma lapā Izveidot **rēķinu, ārējās** atsauces laukiem **jāsakrīt**. Ja viena rakstzīme atšķiras, krājumi rēķinā netiks konsolidēti. Ārējās atsauces sadaļā nav veiktas pārbaudes **nevienam** laukam, **un** vērtībai rindas numura laukā jābūt pozitīvam veselam skaitlim.

### <a name="address-tab"></a>Cilne Adreses

Cilnē Adrese ir pieejama šāda **informācija**.

| Lauks | Apraksts |
|-------|-------------|
| Piegādes adrese | <p>Izvēlieties rindas krājuma piegādes adresi. Noklusējuma piegādes adrese ir primārā piegādes adrese no kopsavilkuma **cilnes** Adrese.</p><p>Mainot adresi, varat atlasīt šādas adreses opcijas:</p><ul><li>**Adreses** – atlasiet pašreizējā debitora adresi.</li><li>**Tiek lietota** – atlasiet adresi, kas pašreiz tiek izmantota pašreizējam debitoram.</li><li>**Cita adrese** – atlasiet adresi jebkuram debitora ierakstam.</li></ul><p>Krājumiem, kas izmanto ieņēmumu sadali, var rediģēt tikai pamatelementa adresi. Pakārtoto krājumu adrese sakrīt ar vecākelementa adresi un to nevar rediģēt atsevišķi.</p> |
| Vekseļa adrese | <p>Izvēlieties vekseļa adresi šim rindas krājumam. Noklusējuma piegādes adrese ir primārā piegādes adrese no kopsavilkuma **cilnes** Adrese. Ja nepieciešams, adresi var mainīt, pamatojoties uz pieejamo adrešu nolūku:</p><ul><li>Ja nevienai no adresēm nav **rēķina** nolūka, noklusējuma rēķina adrese ir primārā debitora adrese neatkarīgi no nolūka.</li><li>Ja vienai vai vairākām adresēm ir **rēķina** nolūks, noklusējuma rēķina adrese ir pēdējā ievadītā adrese.</li><li>**Ja** vienai vai vairākām adresēm ir rēķina mērķis un viena no rēķina adresēm ir iestatīta kā primārā adrese, noklusējuma rēķina adrese ir adrese, **kam** ir rēķina mērķis un kura ir iestatīta kā primārā adrese.</li><li>Krājumiem, kas izmanto ieņēmumu sadali, var rediģēt tikai pamatelementa adresi. Pakārtoto krājumu adrese sakrīt ar vecākelementa adresi un to nevar rediģēt atsevišķi.</li></ul> |

### <a name="product-tab"></a>Cilne Prece

Tālākā informācija ir pieejama cilnē **Prece**.

| Lauks vai sadaļa | Apraksts |
|------------------|-------------|
| Noliktavas dimensijas | <p>Šajā sadaļā ir norādīta krājuma glabāšanas informācija. Tas satur sērijas **numura** lauku, kas rāda krājuma sērijas numuru.</p><p>Šis sērijas numurs tiek kopēts no sākotnējā pārdošanas pasūtījuma atbalsta un atjaunošanas procesa laikā. Krājumiem, kas izmanto ieņēmumu sadali, pamatelementa sērijas numurs tiek kopēts uz visiem pakārtotajiem krājumiem. Sērijas numurs tiek kopēts, kad periodiskā **līguma** norēķinu **parametru** **lapā sērijas numura kopēšanas opcija ir iestatīta uz** Jā.</li></ul> |
| Preces dimensijas | Preces detalizēta informācija par krājumu un vērtības tiek automātiski atjauninātas, pamatojoties **uz norēķinu** grafika rindā atlasīto Varianta numura vērtību. |

### <a name="account-tab"></a>Cilne Konts

Cilnē Konts ir pieejama šāda **informācija**.

| Lauks | Apraksts |
|-------|-------------|
| Galvenais konts | Galvenais konts, kas izveidots pārdošanas rindā. Noklusētā vērtība ir no pārdošanas pasūtījuma. Šis lauks var būt tukšs. |
| Krājumu finanšu dimensijas | <p>Noklusētās finanšu dimensijas vērtības, pamatojoties uz debitora un krājuma ierakstu.</p><p>Krājumiem, kas izmanto ieņēmumu sadali, pakārtotie krājumi izmanto debitora finanšu dimensijas vērtības un krājumu ierakstus, kā aprakstīts iepriekš. Ja atjaunināsiet atvasināto krājumu finanšu dimensiju vērtības, varat importēt datu elementu.</p> |

### <a name="renewals-tab"></a>Cilne Atjaunošana

Tālākā informācija ir pieejama cilnē **Atjaunošana**.

| Lauks | Apraksts |
|-------|-------------|
| Atjaunot automātiski | <p>Vērtība, kas norāda, vai norēķinu grafika rinda tiek automātiski atjaunota nākamajam norēķinu periodam:</p><ul><li>**Jā** – veidojot rēķinu, norēķinu grafika rinda tiek automātiski atjaunota nākamajam norēķinu periodam.</li><li>**Nē** – norēķinu grafika rinda netiek automātiski atjaunota. Norēķinu grafiks jāatjauno manuāli.</li></ul> |
| Rindas, kas jāpievieno atjaunošanai | Rindu skaits, kas jāpievieno norēķinu grafika atjaunošanai. |

Turklāt cilnē Atjaunošana ir pieejamas tālāk norādītās **pogas**.

| Poga | Apraksts |
|--------|-------------|
| Nenodzēsto ieņēmumu žurnāla ieraksta audits | Skatiet visas izmaiņas krājumiem, kas izmanto nenosācāmo ieņēmumu līdzekli. |
| Pievienot atjaunošanas termiņu | Pievienojiet krājumam atjaunošanas terminu. Jaunā atjaunošanas termiņa sākuma datums ir nākamais datums pēc iepriekšējā termiņa beigu datuma. Atjaunošanas **beigu datumu**, atlikto **maksājumu sākuma datumu**, **atlikto maksājumu beigu datumu**, krājumu **daudzumu** un **vienības** cenu laukus var atjaunināt. |
| Modificēt atjaunošanas termiņu | <p>Modificējiet atjaunošanas terminu. Sākotnējam terminam pirms sākotnējā žurnāla ieraksta izveides var mainīt atliktā maksājuma sākuma un beigu datumu. Turpmākiem nosacījumiem sākuma datumu nevar mainīt. Tas vienmēr ir nākamais datums pēc iepriekšējā perioda beigām.</p><p>Ja atjaunošanas termins pastāv pēc modificējamā termina, termina datumus nevar mainīt. Šajā gadījumā atjaunošanas krājumam **var** atjaunināt **tikai laukus** Daudzums un Vienības cena.</p><p>Piemēram, pastāv trīs termini. <ul><li>Pirmo terminu nevar mainīt, jo tas jau ir sākts.</li><li>Otrajam termins var mainīt tikai daudzumu un vienības cenu.</li><li>Trešajam termins var mainīt visas vērtības, izņemot sākuma datumu. Turklāt opcija Plānot **no veidnes ļauj** izveidot atlikto maksājumu grafiku, kas ir balstīts uz nenosācītā ieņēmumu krājuma veidni. Kad opcija ir iestatīta uz **Jā**, **veidnes** laukā Atlasiet atlikto maksājumu veidni un pēc savas izvēles mainiet atliktā maksājuma sākuma un beigu datumu. Turpmākiem atjaunošanas nosacījumiem tiek izmantota tā pati atlikto maksājumu veidne. Tomēr atliktā maksājuma veidni var mainīt.</p></li></ul> |

### <a name="termination-tab"></a>Cilne Darba attiecību pārtraukšana

Atbrīvošanas cilnē ir pieejama šāda **informācija**.

| Lauks | Apraksts |
|-------|-------------|
| Atbrīvošanas datums | Datums, kad norēķinu grafika rinda tiek izbeigta. Noklusētā vērtība ir no lauka **Atbrīvošanas** datums galvenē. Vērtību var mainīt pēc jūsu pieprasītā. |
| Izbeigšanas veids | Darba attiecību pārtraukšanas tips. Noklusētā vērtība ir no lauka **Atbrīvošanas** tips galvenē. |

### <a name="hold-tab"></a>Cilne Aizturēšana

Ja tiek izmantoti ieņēmumu un izdevumu atliktie norēķini, cilnē **Aizturēts** tiek rādīts atliktā maksājuma datums.

### <a name="escalation-and-discount-tab"></a>Eskalācijas un atlaides cilne

Šī informācija ir pieejama cilnē Eskalācija **un** atlaide.

| Lauks | Apraksts |
|-------|-------------|
| Eskalācija | <p>Atlasiet, vai rēķina grafika rindai ir atļautas eskalācijas. Veidojot rēķinu grafika rindu, tiek lietota jebkura eskalācijas rinda no virsraksta.</p><ul><li>**Jā** – eskalācijas var lietot rindai. Ja ir atlasīta šī opcija, varat iestatīt rēķinu grafika rindu eskalācijas lapā Eskalācija **un** atlaide.</li><li>**Nē** – eskalācijas nevar lietot rindai.</li></ul><p>Noklusējuma iestatījums ir balstīts uz atlasīto **norēķinu grafika** grupu.</p> |

### <a name="price-changes-tab"></a>Cilne Cenas izmaiņas

Rindās, kas tiek mainītas **no** standarta **cenas uz** vienotā cenu, cilnes **Cenu izmaiņas** režģī ir ietvertas šādas kolonnas:

- Mainīt datumu
- Izmaiņas veic lietotājs
- Standarta cena
- Vienotā cena
- Cenas pielāgošana
