---
title: Ieņēmumu atzīšanas atkārtota sadale
description: Šajā tēmā ir sniegta informācija par atkārtoto sadali, kas ļauj organizācijām pārrēķināt ieņēmumu cenas, ja ir mainīti pārdošanas līguma nosacījumi. Tā ietver saites uz citām tēmām, kas apraksta, kā atpazīt ieņēmumus vairākos scenārijos.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 53304842bdbe7dadb435ab3a0381f3835c2c443a
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487022"
---
# <a name="revenue-recognition-reallocation"></a>Ieņēmumu atzīšanas atkārtota sadale

[!include [banner](../includes/banner.md)]

Atkārtotā sadale ļauj organizācijām pārrēķināt ieņēmumu cenas, ja ir mainīti pārdošanas līguma nosacījumi. Ieņēmumu atzīšanas nolūkos pārdošanas pasūtījuma dokumenti tiek uzskatīti par līgumu.

Jūsu organizācijai pašai jānosaka, vai ir nepieciešama atkārtota sadale. Jaunas rindas pievienošana pārdošanas pasūtījumam vai jauna pārdošanas pasūtījuma pievienošana debitoram var neveidot līguma izmaiņas. Tālāk minētajiem scenārijiem var būt nepieciešama atkārtota sadale:

- Debitors pievienoja krājumus pārdošanas pasūtījumam vai noņēma krājumus no pārdošanas pasūtījuma pēc tam, kad pasūtījums tika pilnībā vai daļēji iekļauts rēķinā.
- Tam pašam līgumam tika ievadīti vairāki pārdošanas pasūtījumi apstiprinātā stāvoklī vai rēķinā iekļautajā stāvoklī.
- Debitors atgrieza vai saņēma krājuma kredītu pēc tam, kad sākotnējais pārdošanas pasūtījums tika pilnībā vai daļēji iekļauts rēķinā.

Pastāv daži svarīgi atkārtotās sadales procesa ierobežojumi:

- Procesu var palaist tikai vienu reizi. Tāpēc ir svarīgi to palaist tikai pēc visu izmaiņu veikšanas.

    - Šis ierobežojums ir noņemts versijā 10.0.17 un jaunākās versijās.

- Procesu nevar palaist projekta pārdošanas pasūtījumos.

    - Šis ierobežojums ir noņemts versijā 10.0.17 un jaunākās versijās.

- Ja ir iesaistīti vairāki pārdošanas pasūtījumi, tiem jābūt vienā debitora kontā.
- Visiem atkārtoti sadalītajiem pārdošanas pasūtījumiem jābūt vienā un tajā pašā transakcijas valūtā.
- Procesu nevar atsaukt pēc tā palaišanas.

    - Šis ierobežojums ir noņemts versijā 10.0.17 un jaunākās versijās.

- Atkārtotu sadali var veikt tikai pārdošanas pasūtījumiem vai projekta pārdošanas pasūtījumiem. To nevar veikt pārdošanas pasūtījumu un projekta pārdošanas pasūtījumu kombinācijai.

    - Šis ierobežojums ir noņemts versijā 10.0.17 un jaunākās versijās.

## <a name="set-up-reallocation"></a>Atkārtotās sadales iestatīšana

Viens parametrs ietekmē atkārtotās sadales procesu.

Tā kā atkārtoto sadali var veikt pārdošanas pasūtījumā, kas ir daļēji vai pilnībā iekļauts rēķinā, visi iepriekšējie rēķina uzskaites ieraksti jāizlabo, izmantojot jaunās atkārtoti sadalītās ieņēmumu cenas. Šis labojums tiek veikts, stornējot sākotnējā rēķina uzskaites ierakstu un grāmatojot jauno uzskaites ierakstu, kas ir balstīts uz atkārtoti sadalītajām ieņēmumu cenām.

Katrai organizācijai ir jāizlemj, vai labojumam jāatjaunina tikai virsgrāmata, vai arī debitoru parādi. Pieņemtais lēmums nosaka atbilstošo **virsgrāmatas parametru** lapas cilnes **Ieņēmumu atzīšana** opcijas **Grāmatot rēķinu labojumus debitoru parādos** iestatījumu (**Ieņēmumu atzīšana \> Iestatīšana \> Virsgrāmatas parametri**). Atbilstošais iestatījums ir atkarīgi no konkrētā scenārija. Lai iegūtu plašāku informāciju par iespējamiem scenārijiem, izmantojiet šīs tēmas sadaļā [Atkārtotās sadales scenāriji](#scenarios-for-reallocation) norādītās saites.

[![Ieņēmumu atzīšanas cilne virsgrāmatas parametru lapā.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Ja opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Jā**, atkārtotas sadales process rada šādu rezultātu:

- Debitoru parādos ir izveidots kredīta dokuments, lai stornētu rēķinu, kam nepieciešama korekcija.

    - Kredīta dokuments atkārtoti izmanto sākotnējā rēķina numuru, bet tam tiek pievienots “-1”.
    - Kredīta dokuments tiek automātiski segts pret sākotnējo rēķinu. Ja sākotnējais rēķins jau ir segts ar citu kredīta dokumentu vai maksājumu, šis segums tiek automātiski stornēts.
    - Kredīta dokuments tiek grāmatots virsgrāmatā, lai stornētu uzskaites ierakstu, kas tika iegrāmatots sākotnējā rēķinā. Tomēr krājumu un pārdoto preču pašizmaksas (PPPI) transakciju ieraksti nav stornēti.

- Jaunais rēķins, kas ir balstīts uz jaunajām atkārtoti sadalītās cenas summām, tiek izveidots debitoru parādos.

    - Jaunais rēķins atkārtoti izmanto sākotnējā rēķina numuru, bet tam tiek pievienots “-2”.
    - Jaunais rēķins tiek automātiski nosegts pret jebkuru kredīta dokumentu vai maksājumiem, kas iepriekš tika segti ar sākotnējo rēķinu.
    - Jaunais rēķins tiek grāmatots virsgrāmatā, izmantojot jaunās, atkārtoti sadalītās ieņēmumu cenas summas. Tas netiek vēlreiz grāmatots krājuma un PPPI kontos, jo šie ieraksti tiek uzturēti sākotnējā rēķina uzskaites ierakstā.

Ja opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Nē**, atkārtotas sadales process rada šādu rezultātu:

- Storno uzskaites ieraksts tiek grāmatots tikai virsgrāmatā. Tiek atsaukta visa uzskaite no sākotnējā rēķina, izņemot krājumu un PPPI konta ierakstus.
- Jauns uzskaites ieraksts tiek grāmatots tikai virsgrāmatā, pamatojoties uz jaunajām atkārtoti sadalītajām ieņēmumu cenām. Tas netiek vēlreiz grāmatots krājuma un PPPI kontos, jo šie ieraksti tiek uzturēti sākotnējā rēķina uzskaites ierakstā.
- Rēķins **debitora transakciju** lapā netiek ietekmēts vai mainīts, taču joprojām rāda sākotnējo uzskaites ierakstu. Nav atsauces uz storno vai jaunajiem uzskaites ierakstiem.

Kā jau ir norādīts, varat atjaunināt tikai virsgrāmatu vai virsgrāmatu un debitoru parādus. Abām pieejām ir priekšrocības un trūkumi. Ieteicams novērtēt organizācijas prasības, lai noteiktu, kuru opciju izmantot. Ja atjaunināt gan virsgrāmatu, gan debitoru parādus, jaunajā rēķinā tiks parādīti pareizie uzskaites ieraksti, un tos var skatīt **debitora transakciju** lapas dokumentā. Turklāt segšanas process izmantos atjauninātos uzskaites ierakstus, lai grāmatotu visas termiņatlaides un peļņu vai zaudējumus. No otras puses, kredīta dokuments un jaunais rēķins tiks parādīts kontu pārskatos un vecumstruktūras pārskatos tāpat kā citi kredīta dokumenti un debitoru rēķini. Šo dokumentu apraksts norāda, vai tie ir izveidoti ar uzskaites korekcijas palīdzību.

## <a name="run-the-reallocation-process"></a>Atkārtotās sadales procesa palaišana

Lai sāktu atkārtotās sadales procesu, jebkurā pārdošanas pasūtījumā, kas atkārtoti jāsadala, atlasiet opciju **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Vai arī atveriet **Ieņēmumu atzīšana \> Periodiskie uzdevumi \> Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, un pēc tam ievadiet atbilstošus filtrus, piemēram, debitora kontu.

[![Atkārtoti sadalīt cenu ar jaunu pasūtījuma rindu lapu.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Lapas **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** augšējā režģa nosaukums ir **Pārdošana**. Tajā uzskaitīt debitora pārdošanas pasūtījumi. Atlasiet pārdošanas pasūtījumus, kas ir atkārtoti jāsadala. Ja pārdošanas pasūtījumam ir atkārtotas sadales ID, cits lietotājs to jau ir atzīmējis atkārtotai sadalei. Ja viens vai vairāki pārdošanas pasūtījumi iepriekš tika atkārtoti sadalīti un tie ir jāiekļauj citā atkārtotā sadalē, vispirms ir jāatceļ šo pārdošanas pasūtījumu atkārtota sadale. Pēc tam to(s) var iekļaut jaunā atkārtotā sadalē. Papildinformāciju skatiet tālāk šīs tēmas sadaļās [Atkārtotas sadales atsaukšana](#undo-a-reallocation) un [Vairākkārtēja atkārtota sadale](#reallocate-multiple-times).

Lapas apakšējā režģa nosaukums ir **Rindas**. Kad **pārdošanas** režģī ir atlasīts viens vai vairāki pārdošanas pasūtījumi, **rindu** režģis rāda pārdošanas pasūtījuma rindas. Atlasiet pārdošanas pasūtījuma rindas, kas ir atkārtoti jāsadala Ja atlasījāt tikai vienu pārdošanas pasūtījumu, tā paša pārdošanas pasūtījuma rindas ir atkārtoti jāsadala. Šāda situācija var rasties, ja kāda no pārdošanas pasūtījuma rindām tika iepriekš iekļauta rēķinā, un pēc tam tika pievienota jauna rinda vai arī esoša rinda tika noņemta vai atcelta. Ja rinda tika noņemta, tā netiks parādīta režģī. Tāpēc to nevar atlasīt. Tomēr tā joprojām tiks ņemta vērā, kad tiks izpildīts atkārtotās sadales process.

Kad esat beidzis atlasīt nepieciešamās pārdošanas pasūtījuma rindas, izmantojiet darbību rūts pogas, kā aprakstīts šeit:

- **Atjaunināt atkārtoto sadali** — aprēķināt jaunās ieņēmumu cenas summas atlasītajām pārdošanas pasūtījuma rindām. Ja rinda tika noņemta vai atcelta, atkārtotā sadale tiks veikta tikai esošajām atlasītajām rindām. Tālāk attēlā parādīts pārdošanas pasūtījuma rindu piemērs pirms atkārtotās sadales atjaunināšanas.

    [![Pārdošanas pasūtījuma rindas pirms atkārtotās sadales atjaunināšanas.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Jaunās ieņēmumu cenu summas tiek rādītas **rindu** režģa kolonnā **Atkārtoti sadalītā summa**. Šajā brīdī atkārtotā sadale ir apstrādāta, taču vēl nav aprēķināta. Tālāk attēlā parādīts pārdošanas pasūtījuma rindu piemērs pēc atkārtotās sadales atjaunināšanas.

    [![Pārdošanas pasūtījuma rindas pēc atkārtotās sadales atjaunināšanas.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Apstrādāt** — apstrādāt vai grāmatot atkārtoti sadalītās ieņēmumu cenas. Kad atlasīsit šo pogu, nevarēsit atsaukt atkārtoto sadali. Ja pirms pogas **Apstrādāt** atlases neatlasījāt opciju **Atjaunināt atkārtoto sadali**, tiek automātiski palaista atkārtotā sadale.

    - Ja neviena pārdošanas pasūtījuma rinda nav iekļauta rēķinā, ieņēmumu cenas summas tiek atjauninātas visiem pārdošanas pasūtījumiem, kas tika atlasīti atkārtotai sadalei.
    - Ja viena vai vairākas pārdošanas pasūtījuma rindas tiek iekļautas rēķinā, tiek grāmatoti labojumi uzskaites ierakstos un tiek labota detalizētā informācija par ieņēmumu grafiku, kas tika izveidota rēķinā iekļautajai pārdošanas pasūtījuma rindai.

- **Paredzētais dokuments** — parādīt to uzskaites ierakstu priekšskatījumu, kas izveidoti visām rēķinā iekļautajām pārdošanas pasūtījuma rindām. Ja rēķinā nav iekļauta neviena rinda, nekas netiek parādīts. Ja pirms pogas **Paredzētais dokuments** atlases neatlasījāt opciju **Atjaunināt atkārtoto sadali**, tiek automātiski palaista atkārtotā sadale.
- **Ieņēmumu atkārtota sadale** — atver lapu, kas rāda ieņēmumu cenas sadalījumu visām atlasītajām rindām. Lapā nav iespējams mainīt informāciju. Tā parāda rindu summas, kas tika izmantotas atkārtotajai sadalei.

    [![Rindu summas, kas tika izmantotas atkārtotai sadalei.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Atiestatīt atlasītā debitora datus** — ja atkārtotās sadales process tika sākts, bet netika pabeigts, notīriet atkārtotās sadales tabulas datus tikai atlasītajam debitoram. Piemēram, jūs atkārtotai sadalei atzīmējat vairākas pārdošanas pasūtījuma rindas, atstājat lapu atvērtu, neatlasot **Apstrādāt**, un pēc tam iestājas lapas noildze. Šajā gadījumā pārdošanas pasūtījuma rindas paliek atzīmētas un nebūs pieejamas citam lietotājam, lai pabeigtu atkārtotās sadales procesu. Atverot lapu, tā var būt arī tukša. Šādā gadījumā pogu **Atiestatīt atlasītā debitora datus** var izmantot, lai klīrētu neapstrādātos pārdošanas pasūtījumus, lai cits lietotājs varētu pabeigt atkārtotās sadales procesu.

## <a name="undo-a-reallocation"></a>Atkārtotas sadales atsaukšana

Atkārtotu sadali var atsaukt, palaižot citu atkārtotu sadali. Atkārtotu sadali veic vēlreiz, un lietotājs atlasa dažādas pārdošanas pasūtījuma rindas, ko iekļaut otrajā atkārtotas sadales procesā.

Ja atkārtota sadale ir veikta divos vai vairākos atsevišķos pārdošanas pasūtījumos, to var atsaukt, atlasot **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** no jebkura pārdošanas pasūtījuma, kas ir iekļauts atkārtotajā sadalē. Jūs nevarat doties uz **Ieņēmumu atzīšana \> Periodiskie uzdevumi \> Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, lai atsauktu atkārtotu sadali, jo lapa, kas tiek atvērta šādā veidā, parāda tikai tos pārdošanas pasūtījumus, kuriem nav atkārtotas sadales ID. Atkārtotas sadales ID tiek piešķirts pēc tam, kad dokuments ir atkārtoti sadalīts.

Lapā **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** noņemiet atzīmi visiem pārdošanas pasūtījumiem, kas ir jāizslēdz no līgumiskās vienošanās. Lai apstrādātu atkārtotu sadali, darbību rūtī izmantojiet atbilstošās pogas, piemēram, **Atjaunināt atkārtoto sadali** un **Apstrādāt**. Ja visiem pārdošanas pasūtījumiem, izņemot aktīvo pārdošanas pasūtījumu, ir noņemta atzīme, tad, apstrādājot izmaiņas, atkārtotas sadales ID tiks noņemts.

Ja atkārtota sadale ir veikta, pievienojot jaunu rindu pilnībā vai daļēji rēķinā iekļautam pārdošanas pasūtījumam, atkārtotu sadali var atsaukt, tikai noņemot šo rindu no pārdošanas pasūtījuma un pēc tam vēlreiz palaižot atkārtotas sadales darbību. Pārdošanas pasūtījuma rinda ir jānoņem, jo tiek pieņemts, ka visas pārdošanas pasūtījuma rindas ir daļa no tā paša līguma. Ja atrodaties lapā **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, pārdošanas pasūtījuma rindai atzīmi nevar noņemt.

## <a name="reallocate-multiple-times"></a>Vairākkārtēja atkārtota sadale

Ja līgumā ir veiktas vairākas izmaiņas, attiecībā uz vienu un to pašu pārdošanas pasūtījumu var veikt vairākas atkārtotas sadales. Katra atkārtota sadale izraisa atkārtotas sadales ID piešķiršanu pārdošanas pasūtījumam vai pārdošanas pasūtījumu grupai, lai sagrupētu izmaiņas. Ja tiek veiktas vairākas atkārtotas sadales, katrā papildu atkārtotā sadalē tiek izmantots tas pats atkārtotas sadales ID, kā pirmajā atkārtotā sadalē.

Piemēram, tiek ievadīts pārdošanas pasūtījums 00045, un tam ir vairākas rindas. Kad pārdošanas pasūtījums ir pilnībā iekļauts rēķinā, tam tiek pievienota jauna pārdošanas pasūtījuma rinda. Pēc tam tiek palaista atkārtota sadale, atverot lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** vai nu no pārdošanas pasūtījuma 00045 vai dodoties uz **Ieņēmumu atzīšana \> Periodiskie uzdevumi \> Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Atkārtotas sadales ID **Reall000001** ir piešķirts pārdošanas pasūtījumam.

Tam pašam līgumam tiek izveidots otrs pārdošanas pasūtījums — 00052. Atkārtotu sadali var palaist vēlreiz no pārdošanas pasūtījuma 00045, bet nevis no pārdošanas pasūtījuma 00052, atverot lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Ja no pārdošanas pasūtījuma 00052 atvērsit lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, pārdošanas pasūtījums 00045 netiks rādīts, jo tam ir piešķirts atkārtotas sadales ID. Šajā lapā tiek rādīti tikai tie pārdošanas pasūtījumi, kuriem nav atkārtotas sadales ID.

Pastāv divi veidi, kā veikt otro atkārtoto sadali. Pārdošanas pasūtījuma 00045 atkārtotu sadali var atsaukt. Šajā gadījumā atkārtotas sadales ID tiek noņemts, un pēc tam varat veikt atkārtotu sadali vai nu no pārdošanas pasūtījuma 00045 vai pārdošanas pasūtījuma 00052. Varat arī atvērt lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** no pārdošanas pasūtījuma 00045 un pievienot otru pārdošanas pasūtījumu. Kad atkārtota sadale ir apstrādāta, atkārtotas sadales ID **Reall000001** tiks piešķirts gan pārdošanas pasūtījumam 00045, gan pārdošanas pasūtījumam 00052.

## <a name="scenarios-for-reallocation"></a>Atkārtotas sadales scenāriji

Tālāk minētajās tēmās ir apskatīti dažādi ieņēmumu atzīšanas scenāriji.

- [Ieņēmumu atzīšanas atkārtotā sadale — 1. scenārijs](rev-rec-reallocation-scenario-1.md) — tiek ievadīti divi pārdošanas pasūtījumi, taču tie tiek tikai apstiprināti. Viens un tas pats scenārijs radīs līdzīgus rezultātus, ja vairāk nekā divu pārdošanas pasūtījumu statuss ir Apstiprināts.
- [Ieņēmumu atzīšanas atkārtotā sadale — 2. scenārijs](rev-rec-reallocation-scenario-2.md) — ievadīti divi pārdošanas pasūtījumi, un pēc tam debitors pievieno līgumam krājumu, kad pirmais pārdošanas pasūtījums ir iekļauts rēķinā.
- [Ieņēmumu atzīšanas atkārtotā sadale — 3. scenārijs](rev-rec-reallocation-scenario-3.md) — esošam, rēķinā iekļautam pārdošanas pasūtījumam tiek pievienota jauna rinda.
- [Ieņēmumu atzīšanas atkārtotā sadale — 4. scenārijs](rev-rec-reallocation-scenario-4.md) — esošam, daļēji rēķinā iekļautam pārdošanas pasūtījumam tiek noņemta rinda.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
