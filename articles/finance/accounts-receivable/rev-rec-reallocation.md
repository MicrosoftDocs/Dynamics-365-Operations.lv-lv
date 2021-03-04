---
title: Ieņēmumu atzīšanas atkārtota sadale
description: Šajā tēmā ir sniegta informācija par atkārtoto sadali, kas ļauj organizācijām pārrēķināt ieņēmumu cenas, ja ir mainīti pārdošanas līguma nosacījumi. Tā ietver saites uz citām tēmām, kas apraksta, kā atpazīt ieņēmumus vairākos scenārijos.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7c57ac5f3fc8d9a0e0b57ba5d7a3e2924bbd4c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995642"
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
- Procesu nevar palaist projekta pārdošanas pasūtījumos.
- Ja ir iesaistīti vairāki pārdošanas pasūtījumi, tiem jābūt vienā debitora kontā.
- Visiem atkārtoti sadalītajiem pārdošanas pasūtījumiem jābūt vienā un tajā pašā transakcijas valūtā.
- Procesu nevar atsaukt pēc tā palaišanas.

## <a name="set-up-reallocation"></a>Atkārtotās sadales iestatīšana

Viens parametrs ietekmē atkārtotās sadales procesu.

Tā kā atkārtoto sadali var veikt pārdošanas pasūtījumā, kas ir daļēji vai pilnībā iekļauts rēķinā, visi iepriekšējie rēķina uzskaites ieraksti jāizlabo, izmantojot jaunās atkārtoti sadalītās ieņēmumu cenas. Šis labojums tiek veikts, stornējot sākotnējā rēķina uzskaites ierakstu un grāmatojot jauno uzskaites ierakstu, kas ir balstīts uz atkārtoti sadalītajām ieņēmumu cenām.

Katrai organizācijai ir jāizlemj, vai labojumam jāatjaunina tikai virsgrāmata, vai arī debitoru parādi. Pieņemtais lēmums nosaka atbilstošo **virsgrāmatas parametru** lapas cilnes **Ieņēmumu atzīšana** opcijas **Grāmatot rēķinu labojumus debitoru parādos** iestatījumu (**Ieņēmumu atzīšana \> Iestatīšana \> Virsgrāmatas parametri**). Atbilstošais iestatījums ir atkarīgi no konkrētā scenārija. Lai iegūtu plašāku informāciju par iespējamiem scenārijiem, izmantojiet šīs tēmas sadaļā [Atkārtotās sadales scenāriji](#scenarios-for-reallocation) norādītās saites.

[![Ieņēmumu atzīšanas cilne virsgrāmatas parametru lapā](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

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

[![Atkārtoti sadalīt cenu ar jaunu pasūtījuma rindu lapu](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Lapas **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** augšējā režģa nosaukums ir **Pārdošana**. Tajā uzskaitīt debitora pārdošanas pasūtījumi. Atlasiet pārdošanas pasūtījumus, kas ir atkārtoti jāsadala Nevar atlasīt projekta pārdošanas pasūtījumus, jo projekta pārdošanas pasūtījumus nevar atkārtoti sadalīt. Nevar atlasīt arī tos pārdošanas pasūtījumus, kuriem jau ir atkārtotas sadales ID, jo ar projektu nesaistītos pārdošanas pasūtījumus var atkārtoti sadalīt tikai vienu reizi. Ja pārdošanas pasūtījumam ir atkārtotas sadales ID, cits lietotājs to jau ir atzīmējis atkārtotai sadalei.

Lapas apakšējā režģa nosaukums ir **Rindas**. Kad **pārdošanas** režģī ir atlasīts viens vai vairāki pārdošanas pasūtījumi, **rindu** režģis rāda pārdošanas pasūtījuma rindas. Atlasiet pārdošanas pasūtījuma rindas, kas ir atkārtoti jāsadala Ja atlasījāt tikai vienu pārdošanas pasūtījumu, tā paša pārdošanas pasūtījuma rindas ir atkārtoti jāsadala. Šāda situācija var rasties, ja kāda no pārdošanas pasūtījuma rindām tika iepriekš iekļauta rēķinā, un pēc tam tika pievienota jauna rinda vai arī esoša rinda tika noņemta vai atcelta. Ja rinda tika noņemta, tā netiks parādīta režģī. Tāpēc to nevar atlasīt. Tomēr tā joprojām tiks ņemta vērā, kad tiks izpildīts atkārtotās sadales process.

Kad esat beidzis atlasīt nepieciešamās pārdošanas pasūtījuma rindas, izmantojiet darbību rūts pogas, kā aprakstīts šeit:

- **Atjaunināt atkārtoto sadali** — aprēķināt jaunās ieņēmumu cenas summas atlasītajām pārdošanas pasūtījuma rindām. Ja rinda tika noņemta vai atcelta, atkārtotā sadale tiks veikta tikai esošajām atlasītajām rindām. Tālāk attēlā parādīts pārdošanas pasūtījuma rindu piemērs pirms atkārtotās sadales atjaunināšanas.

    [![Pārdošanas pasūtījuma rindas pirms atkārtotās sadales atjaunināšanas](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Jaunās ieņēmumu cenu summas tiek rādītas **rindu** režģa kolonnā **Atkārtoti sadalītā summa**. Šajā brīdī atkārtotā sadale ir apstrādāta, taču vēl nav aprēķināta. Tālāk attēlā parādīts pārdošanas pasūtījuma rindu piemērs pēc atkārtotās sadales atjaunināšanas.

    [![Pārdošanas pasūtījuma rindas pēc atkārtotās sadales atjaunināšanas](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Apstrādāt** — apstrādāt vai grāmatot atkārtoti sadalītās ieņēmumu cenas. Kad atlasīsit šo pogu, nevarēsit atsaukt atkārtoto sadali. Ja pirms pogas **Apstrādāt** atlases neatlasījāt opciju **Atjaunināt atkārtoto sadali**, tiek automātiski palaista atkārtotā sadale.

    - Ja neviena pārdošanas pasūtījuma rinda nav iekļauta rēķinā, ieņēmumu cenas summas tiek atjauninātas visiem pārdošanas pasūtījumiem, kas tika atlasīti atkārtotai sadalei.
    - Ja viena vai vairākas pārdošanas pasūtījuma rindas tiek iekļautas rēķinā, tiek grāmatoti labojumi uzskaites ierakstos un tiek labota detalizētā informācija par ieņēmumu grafiku, kas tika izveidota rēķinā iekļautajai pārdošanas pasūtījuma rindai.

- **Paredzētais dokuments** — parādīt to uzskaites ierakstu priekšskatījumu, kas izveidoti visām rēķinā iekļautajām pārdošanas pasūtījuma rindām. Ja rēķinā nav iekļauta neviena rinda, nekas netiek parādīts. Ja pirms pogas **Paredzētais dokuments** atlases neatlasījāt opciju **Atjaunināt atkārtoto sadali**, tiek automātiski palaista atkārtotā sadale.
- **Ieņēmumu atkārtota sadale** — atver lapu, kas rāda ieņēmumu cenas sadalījumu visām atlasītajām rindām. Lapā nav iespējams mainīt informāciju. Tā parāda rindu summas, kas tika izmantotas atkārtotajai sadalei.

    [![Rindu summas, kas tika izmantotas atkārtotai sadalei](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Atiestatīt atlasītā debitora datus** — ja atkārtotās sadales process tika sākts, bet netika pabeigts, notīriet atkārtotās sadales tabulas datus tikai atlasītajam debitoram. Piemēram, jūs atkārtotai sadalei atzīmējat vairākas pārdošanas pasūtījuma rindas, atstājat lapu atvērtu, neatlasot **Apstrādāt**, un pēc tam iestājas lapas noildze. Šajā gadījumā pārdošanas pasūtījuma rindas paliek atzīmētas un nebūs pieejamas citam lietotājam, lai pabeigtu atkārtotās sadales procesu. Atverot lapu, tā var būt arī tukša. Šādā gadījumā pogu **Atiestatīt atlasītā debitora datus** var izmantot, lai klīrētu neapstrādātos pārdošanas pasūtījumus, lai cits lietotājs varētu pabeigt atkārtotās sadales procesu.

## <a name="scenarios-for-reallocation"></a>Atkārtotas sadales scenāriji

Tālāk minētajās tēmās ir apskatīti dažādi ieņēmumu atzīšanas scenāriji:

- [Ieņēmumu atzīšanas atkārtotā sadale — 1. scenārijs](rev-rec-reallocation-scenario-1.md) — tiek ievadīti divi pārdošanas pasūtījumi, taču tie tiek tikai apstiprināti. Viens un tas pats scenārijs radīs līdzīgus rezultātus, ja vairāk nekā divu pārdošanas pasūtījumu statuss ir Apstiprināts.
- [Ieņēmumu atzīšanas atkārtotā sadale — 2. scenārijs](rev-rec-reallocation-scenario-2.md) — ievadīti divi pārdošanas pasūtījumi, un pēc tam debitors pievieno līgumam krājumu, kad pirmais pārdošanas pasūtījums ir iekļauts rēķinā.
- [Ieņēmumu atzīšanas atkārtotā sadale — 3. scenārijs](rev-rec-reallocation-scenario-3.md) — esošam, rēķinā iekļautam pārdošanas pasūtījumam tiek pievienota jauna rinda.
- [Ieņēmumu atzīšanas atkārtotā sadale — 4. scenārijs](rev-rec-reallocation-scenario-4.md) — esošam, daļēji rēķinā iekļautam pārdošanas pasūtījumam tiek noņemta rinda.
