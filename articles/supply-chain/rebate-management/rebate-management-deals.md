---
title: Atlaižu pārvaldības darījumi
description: Šajā tēmā aprakstīts, kā izveidot Atlaižu pārvaldības darījumus. Darījumi tiek izmantoti, lai kontrolētu dažādas metodes un bāzes atlaižu un patentmaksu aprēķināšanai. Tās iekļauj iekļaušanas un izslēgšanas kārtulas.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5b8a1beae80ad63f26cd1b532d1d6026a5b38a8701c9c1d0aadfee5da8965477
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716496"
---
# <a name="rebate-management-deals"></a>Atlaižu pārvaldības darījumi

[!include [banner](../includes/banner.md)]

Atlaižu pārvaldības darījumi tiek izmantoti, lai kontrolētu dažādas metodes un bāzes atlaižu un patentmaksu aprēķināšanai. Tās iekļauj iekļaušanas un izslēgšanas kārtulas. Ir trīs atlaižu pārvaldības darījumu veidi: debitoru atlaides, debitoru patentmaksas un kreditora atlaides. Visiem trim veidiem tiek lietoti līdzīgi iestatījumi. Šī tēma norāda uz atšķirībām to atrašanās vietās.

## <a name="create-a-deal"></a>Darījuma izveide

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Visi atlaižu pārvaldības darījumi**. Lapā **Visi atlaižu pārvaldības darījumi** varat izveidot un strādāt ar visu trīs veidu darījumiem.

    Alternatīvi cilnē sekojiet kādai no norādītajām darbībām: Katrā gadījumā saraksta lapa, kas tiek parādīta, nodrošina visus tos pašus iestatījumus kā **Visu atlaižu pārvaldības darījumu** saraksta lapai, bet tā ir filtrēta, lai rādītu tikai viena veida darījumus.

    - Lai izveidotu tikai debitora atlaides darījumus, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Debitoru atlaižu darījumi**.
    - Lai izveidotu tikai debitora honorāru darījumus, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Debitoru patentmaksas darījumi**.
    - Lai izveidotu tikai kreditora atlaides darījumus, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Debitoru atlaižu darījumi**.

1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot jaunu darījumu** iestatiet šādus laukus:

    - **Atlaižu pārvaldības darījums** - Ja atlaides darījumiem [esat iestatījis numuru sēriju](rebate-management-parameters.md), šis lauks automātiski tiek iestatīts uz unikālu, sistēmas ģenerētu ID. Citādi ir jāievada unikāls ID.
    - **Apraksts** — ievadiet darījuma aprakstu.
    - **Modulis** – izvēlieties partnera tipu, uz ko attiecas darījums (*Debitors* vai *Kreditors*). Atkarībā no jūsu uzsāktās lapas, šis lauks var būt iestatīts automātiski, pamatojoties uz atlasīto darījuma veidu. Šajā gadījumā lauks ir tikai lasāms.
    - **Veids** – atlasiet darījuma veidu (*Atlaide* vai *Patentmaksa*). Atkarībā no jūsu uzsāktās lapas, šis lauks var būt iestatīts automātiski, pamatojoties uz atlasīto darījuma veidu. Šajā gadījumā lauks ir tikai lasāms.
    - **Saskaņot pēc** - atlasiet, kā darījums jāaprēķina un jāsaskaņo:

        - *Darījums* - atsevišķa atlaide ir jāapstrādā visām darījuma atlaidēm un ieturējumiem.
        - *Rinda* – atlaides jāapstrādā katrai darījuma rindai.

    - **Grāmatošanas profils** – izvēlieties [grāmatošanas profilu](rebate-management-posting.md), kuru izmantot darījumiem, uz ko attiecas piedāvājums. Šis lauks ir pieejams tikai tad, ja lauks **Saskaņot pēc** ir iestatīts uz *Darījums*. Ja iestatījums ir *Rinda*, profils tiks piešķirts vēlāk katrai darījumam pievienotajai rindai.
    - **Grāmatošanas profils garantijai** – izvēlieties [grāmatošanas profilu](rebate-management-posting.md), kuru izmantot garantijas darījumiem. Grāmatošanas profili ir nepieciešami garantijas darījumiem tikai tad, ja garantija attiecas uz patentmaksu. Pretējā gadījumā, lai gan grāmatošanas metode nav obligāta, ja grāmatošanas metode nav norādīta, grāmatojot vērtību, tiks parādīta kļūda. Šis lauks ir pieejams tikai tad, ja lauks **Saskaņot pēc** ir iestatīts uz *Patentmaksa*. 
    - **Atlaides izvade** — atlasiet, kā jāsamaksā atlaide vai patentmaksa:

        - *Finanšu* – izveidojiet brīvā teksta kredīta notu vai kreditoru debeta notu, lai rēķinus varētu maksāt vai saņemt vēlāk. Ņemiet vērā, ka nosacījumus **var** izmantot ar atlaidēm, ja ir atlasīta šī opcija. Šī ir vienīgā pieejamā opcija, ja lauks **Saskaņot pēc** ir iestatīts uz *Patentmaksa*.
        - *Krājums* - izveidojiet pārdošanas pasūtījumu vienībām saskaņā ar darījuma iestatījumu. Šajā pārdošanas pasūtījumā katram krājumam tiek piešķirta cena 0 (nulle). Ņemiet vērā, ka nosacījumus **nevar** izmantot ar atlaidēm, ja ir atlasīta šī opcija.

    - **Atlaides valūta** — atlasiet valūtu, kas jāizmanto, maksājot atlaidi, ieturējumus vai autoritāti.
    - **Dokumentu piezīmes** - ievadiet piezīmes par darījumu, kā pieprasīts.
    - **Kumulatīvā garantija** – šo opciju varat iestatīt uz *Jā* tikai tad, ja lauka **Veids** iestatījums ir *Royalty*. Šī opcija ietekmē garantijas ieturējumu maksājumu aprēķinu. Lūk, piemērs:

        - Darījuma garantija ir pārdot vērtību, kas izdos maksājumu par $10000 ceturksnī.
        - Organizācija, kas pārdod preces, pārdod vērtību, kas izraisa ieturējumu maksājumu par $12000 1. ceturksnī. Rezultāts ir patentmaksa $12000, kas tiek maksāta, atņemot $10000 garantiju.
        - Ja opcija **Kumulatīvā garantija** ir iestatīta uz *Jā*, papildu $2000 summa, kas tika maksāta 1. ceturksnī, attiecas uz 2. ceturksni. Tāpēc debitoram tiek garantēts $8000 (debitora $10000 mīnus $2000 papildmaksājums).
        - 2. ceturksnī tiek reģistrēts pārdošanas apjoms, kas izraisa $5000 patentmaksu.
        - Sistēma identificē maksājumu $3000 (maksājumu $8000 mīnus $5000 maksātā patentmaksa).
        - Ja opcija **Kumulatīvās garantija** ir iestatīta uz *Nē*, visi $10000 tiek garantēti katru ceturksni. Šī garantija atbilst ieteiktajai maksājuma summai $5000 2. ceturksnī (garantētie $10000 mīnus $5000 samaksātās patentmaksas).

1. Atlasiet **Labi**, lai izveidotu darījumu un aizvērtu dialoglodziņu.

Šī procedūra izveido jaunā darījuma galvenes līmeni. Pēc tam darījumam tiks pievienotas rindas.

## <a name="add-lines-to-a-deal"></a>Pievienot darījumam rindas

Pēc tam, kad esat izveidojis darījumu, kā aprakstīts iepriekšējā sadaļā, varat to atvērt no saraksta lapas. Pēc tam varat pievienot rindas, lai identificētu debitorus vai kreditorus, krājumus, laika periodus, bāzi un darījuma aprēķina metodes. Darījumam var būt viena vai vairākas rindas. Ja darījumam ir vairākas rindas, parasti tās ir viena tipa vai ar tām ir saistīti vienādi parametri. Kamēr nav pievienotas rindas darījumam, darījums faktiski netiks darīts.

1. Atveriet attiecīgo atlaižu darījumu saraksta lapu, kā aprakstīts iepriekšējā sadaļā.
1. Atrodiet un atveriet darījumu, ar kuru vēlaties strādāt.
1. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet vienu no šīm pogām, lai režģim pievienotu darījuma rindu:

    - **Pievienot rindu** - pievienot jaunu, tukšu darījuma rindu.
    - **Kopēt rindu** - Ja esoša darījuma rinda ir līdzīga darījuma rindai, ko vēlaties pievienot, varat izvēlēties šo pogu, lai nokopētu tās kopiju. Jaunā darījuma rinda ietvers visus iestatījumus no saistīto Atlaižu pārvaldības informācijas. Pēc tam varat rediģēt iestatījumus. Piemēram, parasti atjaunināsiet krājumu saistību un atlaides procentus.

1. Jaunajā pasūtījuma rindā iestatiet šādus laukus:

    - **Atlaižu pārvaldības numurs** - Ja atlaides darījumiem [esat iestatījis numuru sēriju](rebate-management-parameters.md), šis lauks automātiski tiek iestatīts uz unikālu, sistēmas ģenerētu ID. Citādi ir jāievada unikāls ID.
    - **Veids** – darījuma veids, uz kuru attiecas rinda (*Atlaide* vai *Patentmaksa*). Vērtība tiek kopēta no galvenes, un to nevar mainīt.
    - **Apraksts** — ievadiet darījuma rindas aprakstu.
    - **Uzņēmums** – atlasiet uzņēmumu (juridisku personu), uz kuru attiecas darījuma rinda. Apstrādes laikā lietotāji var apstrādāt tikai tās darījuma rindas, kas ir piešķirtas uzņēmumam, kuru tie pašreiz izmanto. **Debitora atlaižu darījumu** saraksta lapa sniedz vairāku uzņēmumu skatu, balstoties uz lietotāja drošības piekļuvi. Tomēr atlaides varat rediģēt un apstrādāt tikai tam uzņēmumam, kuru pašlaik izmantojat.
    - **Konta kods** – izvēlieties debitoru vai kreditoru darbības jomu, uz kuru attiecas darījuma rinda:

        - *Tabula* – darījuma rinda attiecas uz konkrētu debitoru vai kreditoru.
        - *Grupa* – darījuma rinda attiecas uz debitoru vai kreditoru grupu. Lai iegūtu papildu informāciju par to, kā iestatīt grupas, skatiet [Atlaižu pārvaldības grupas](rebate-management-groups.md).
        - *Visi* – darījuma rinda attiecas uz visiem debitoriem vai kreditoriem.

    - **Konta saistība** - Ja laukā **Konta kods** atlasījāt *Tabula*, atlasiet attiecīgo debitoru vai kreditoru, uz kuru attiecas darījums. Ja atlasījāt *Grupa*, atlasiet debitoru vai kreditoru grupu. Ja atlasījāt vērtību *Visi*, šis lauks nav pieejams.
    - **Krājuma kods** – izvēlieties darbības jomu, uz kuru attiecas darījuma rinda:

        - *Tabula* – darījuma rinda attiecas uz konkrētu krājumu.
        - *Grupa* – darījuma rinda attiecas uz krājumu grupu. Lai iegūtu papildu informāciju par to, kā iestatīt grupas, skatiet [Atlaižu pārvaldības grupas](rebate-management-groups.md).
        - *Visi* – darījuma rinda attiecas uz visiem krājumiem.

    - **Krājuma saistība** - Ja laukā **Krājuma kods** atlasījāt *Tabula*, atlasiet attiecīgo krājumu, uz kuru attiecas darījums. Ja atlasījāt *Grupa*, atlasiet krājumu grupu. Ja atlasījāt vērtību *Visi*, šis lauks nav pieejams.
    - **Vienības veids** — atlasiet vienības veidu, kas attiecas uz darījuma rindu (*Krājumu vienība* vai *Pieļaujamā svara vienība*). Ievērojiet, ka šis lauks vecākiem ierakstiem var būt tukšs. Šajā gadījumā tiek pieņemts, ka vērtība *Krājuma vienība* ir norādīta.
    - **(Krājumu vadības parametri)** – atlikušajos darījuma rindas laukos norādiet krājumu vadības parametru vērtības, kas tiks izmantotas, lai definētu krājumus, kas ir iekļauti darījumā (piemēram, krājuma izmērs, krāsa, stils, vieta un noliktava). Lai pievienotu vai noņemtu dimensijas, darbību rūtī atlasiet **Rādīt dimensijas**.

1. Darbību rūtī atlasiet **Saglabāt**.
1. Ja vēlaties vēl vairāk ierobežot krājumu kopu, uz kuru attiecas darījuma rinda, atlasiet rindu un pēc tam kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet **Filtrs**, lai atvērtu standarta **Pieprasījuma** dialoglodziņu.
1. Katrai pievienotajā darījuma rindai iestatiet aprēķina informāciju un citas detaļas kopsavilkuma cilnē **Atlaižu pārvaldība**, kā aprakstīts nākamajā sadaļā.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Pievienot Atlaižu pārvaldības informāciju darījuma rindai

Katrai darījuma rindai ir jāiestata detalizēta informācija par **Atlaižu pārvaldības informāciju** kopsavilkuma cilnē. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet darījuma rindu. Pēc tam iestatiet šīs darījuma rindas vērtības, izmantojot dažādas cilnes kopsavilkuma cilnē **Atlaižu pārvaldības informācija**. Tālāk sniegtās apakšsadaļas apraksta, kā izmantot katru cilni.

### <a name="settings-on-the-general-tab"></a>Kopsavilkuma cilnes Vispārīgi iestatījumi

Kopsavilkuma cilnes **Atlaižu pārvaldības informācija** cilnē **Vispārīgi** varat iestatīt aprēķina metodi un pamatu atlasītajai darījuma rindai. Šis iestatījums kontrolē, vai ir nepieciešams minimālais pirkums, grāmatošanas metodes, kas saistītas ar darījuma rindu, un aprēķina detaļas. Nākamajā tabulā ir aprakstīti pieejamie lauki.

| Lauks | Apraksts |
|---|---|
| Aprēķina metode | Atlasiet metodi, kuru izmantot, kad atlasītā darījuma rinda ir kombinēta ar citām darījuma rindām (*Pakāpenisks*, *Kumulatīvs*, *Secīgs* vai *Kopējs*). Šī lauka vērtība var ievērojami ietekmēt atlaižu aprēķinu rezultātu. Lai iegūtu pilnu aprakstu par katru metodi un piemērus, kas parāda, kā tā ietekmē atlaides aprēķinu, skatiet tālāk šīs tēmas sadaļā [Darījuma rindu aprēķināšanas metodes](#calc-methods). |
| Pamats | Atlasiet, vai atlaide tiek piemērota, pamatojoties uz daudzumu (t.i., uz kopējo nopirkto vai pārdoto preču skaitu) vai uz vērtību (t.i., uz kopējo iegādāto vai pārdoto preču cenu). |
| Darījuma veids | <p>Atlasiet procesa punktu, kad jāveic aprēķins:</p><ul><li>*Pasūtījums* – izmantot pasūtīto daudzumu vai vērtību kā pamatu aprēķinam.</li><li>*Piegādāts* – izmantot pasūtīto daudzumu vai vērtību kā pamatu aprēķinam.</li><li>*Rēķins* – izmantot aprēķināto daudzumu vai vērtību kā pamatu aprēķinam.</li></ul> |
| Vienība | Ja atlasījāt *Daudzumu* laukā **Pamata**, atlasiet vienību, kurā ir jānorāda šis daudzums. |
| Minimālā summa | Ievadiet minimālo summu, kas jāsamaksā par periodu. Jūs varat ievadīt negatīvu vērtību, lai ļautu negatīvas atlaides summas, ja kredīta notas pārsniedz pārdošanas apjomu par periodu. |
| Atlaižu samazināšanas princips | Atlasiet [atlaižu samazināšanas principu](rebate-reduction-principle.md), uz kuru attiecas darījuma rinda. |
| Varianta numurs | Ja darījuma rinda attiecas uz krājumu ar variantiem, atlasiet variantu, uz kuru attiecas darījuma rinda. |
| Kreditora atlaižu pamats | <p>Šis lauks tiek rādīts tikai kreditora atlaidēm (t.i., darījumiem, kuru **Moduļa** lauks ir iestatīts kā *Kreditors*). Atlasiet kreditora atlaižu pamatu:</p><ul><li>*Pirkšanas pasūtījums* - atlaide, ko kreditors saņem, ir balstīta uz pirkšanas pasūtījuma daudzumu vai vērtību.</li><li>*Pārdošanas pasūtījums* – kreditors saņem atlaidi tikai pēc preču pārdošanas. Atlaide tiek pamatota uz pārdošanas pasūtījuma daudzumu vai vērtību.</li></ul> |
| Cenas bāze | <p>Šis lauks tiek rādīts tikai kreditora atlaidēm (t.i., darījumiem, kuru **Moduļa** lauks ir iestatīts kā *Kreditors*). Ja laukā *Kreditora atlaides bāze* atlasījāt **Pārdošanas pasūtījumu**, atlasiet piemērojamo cenas bāzi:</p><ul><li><p>*FIFO* – Lai aprēķinātu atlaidi, jāpalaiž periodiskais uzdevums **Aprēķināt FIFO pirkšanas cenu**. (Lai palaistu uzdevumu, dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Aprēķināt FIFO pirkšanas cenu**.) Lai aprēķinātu pārdoto krājumu vērtību, tiks izmantots noteikums "pirmais iekšā, pirmais ārā" (First in, first out – FIFO). Pēc tam šī vērtība tiks izmantota, lai aprēķinātu kreditoru atlaides. Lūk, piemērs:</p><ul><li>**Pārdotie krājumi:** 1000 vienības $3,00 = $3000</li><li>**Pašreizējā pirkšanas cena, pamatojoties uz FIFO:** $2,00</li><li>**Darba aprēķins:** *Pārdotās vienības* × *Pašreizējā pirkšanas cena* = 1000 × $2,00 = $2000</li></ul></li><li><p>*Pēdējā pirkšanas cena* – vērtība no pēdējās pirkšanas darbības tiks izmantota kreditora atlaižu apmaksasm. Lūk, piemērs:</p><ul><li>**Pārdotie krājumi:** 1000 vienības $3,00 = $3000</li><li>**Pēdējā pirkšanas cena:** $2,00</li><li>**Darba aprēķins:** *Pārdotās vienības* × *Pēdējā pirkšanas cena* = 1000 × $2,00 = $2000</li></ul></li><li><p>*Vidējā pirkšanas cena* - pēdējo *X* mēnešu svērtā vidējā vērtība tiks izmantota, lai aprēķinātu kreditora atlaides. Ja izvēlaties šo opciju, mēnešu skaits ir jāievada laukā **Mēnešu skaits** (kas pieejams tikai tad, ja lauks **Cenas bāze** ir iestatīts uz *Vidējo pirkšanas cenu*). Lūk, piemērs:</p><ul><li>**Pārdotie krājumi:** 1000 vienības $3,00 = $3000</li><li>**Vidējā pirkšanas cena:** $2,00</li><li>**Darba aprēķins:** *Pārdotās vienības* × *Vidējā pirkšanas cena* = 1000 × $2,00 = $2000</li></ul></li><li><p>*Pārdošanas cena* – pārdošanas cena tiks izmantota kreditora atlaižu jāaprēķina. Lūk, piemērs:</p><ul><li>**Pārdotie krājumi:** 1000 vienības $3,00 = $3000</li><li>**Vidējā pirkšanas cena:** $2,00</li><li>**Darba aprēķins:** *Pārdotās vienības* × *Pēdējā pirkšanas cena* = 1000 × $3,00 = $3000</li></ul></li></ul> |
| Mēnešu skaits | Šis lauks tiek rādīts tikai kreditora atlaidēm (t.i., darījumiem, kuru **Moduļa** lauks ir iestatīts kā *Kreditors*). Ja atlasījāt *Vidējo pirkšanas cenu* laukā **Cenas bāze**, ievadiet mēnešu skaitu, kas jālieto. |
| Grāmatošanas metode | Atlasiet [grāmatošanas profilu](rebate-management-posting.md), uz kuru attiecas darījuma rinda. Šo profilu izmanto tikai tad, ja lauks **Saskaņot pēc** darījuma galvenē ir iestatīts uz *Rinda*. Ja lauks **Saskaņot pēc** ir iestatīts uz *Darījums*, vienmēr tiek izmantots darījuma galvenē iestatītais grāmatošanas profils. Ja darījuma rindā nav iestatīts grāmatošanas profils, tiks izmantots darījuma galvneē iestatītais grāmatošanas profils. |
| Garantijas grāmatošanas profils | Šis lauks darbojas tāpat kā lauks **Grāmatošanas profils**, taču tas attiecas tikai uz honorāriem. |
| Maksājuma veids | Maksājuma tips grāmatošanas metodei, kas atlasīta darījumam. |
| Iekļauts tirdzniecības nodoklis | Atlasiet, vai darbība ir nodokļus ietveroša. Nodokļu ietveršana ir būtiska tikai tad, ja lauks **Pamata** ir iestatīts uz *Vērtība*. Rēķina summa tiks izmantota kā nodokļu iekļaujošā summa. Ja atlaides aprēķina pamatā ir procenti, sistēma reizinās atlaides procentus ar nodokļiem ietverošo summu. Ņemiet vērā, ka aprēķinos tiek izmantota tirdzniecības nodokļa vērtība no darījuma rindas. |
| Iekļaut kredīta notas | <p>Iestatiet šo opciju kā *Jā*, lai iekļautu kredīta notas atlaides aprēķinā.</p><p>Iestatot šo opciju kā *Jā*, ietekme mainās atkarībā no lauka **Darījuma veids** vērtības:</p><ul><li>Ja lauks **Darījuma veids** ir iestatīts uz *Rēķins*, aprēķins būs faktors kredīta notās. Šī konfigurācija ir parastā konfigurācija.</li><li>Ja lauks **Darījuma veids** ir iestatīts uz *Pasūtījums*, aprēķins būs faktors abos pārdošanas pasūtījumos, kuriem ir negatīvas vērtības un atvērti atgrieztie pasūtījumi.</li></ul> |
| Summa ar atlaidi | Iestatiet šo opciju kā *Jā*, lai aprēķinu balstītu uz krājuma vai krājumu atlaides summu gadījumos, kad tiek sniegtas darījuma rindas atlaides. |
| Tikai apmaksātie rēķini | Iestatiet šo opciju kā *Jā*, ja aprēķinā jāņem vērā tikai pilnībā apmaksāti rēķini. (Citiem vārdiem sakot, atlaides netiks aprēķinātas daļēji apmaksātiem rēķiniem.) Šī opcija ir pieejama tikai tad, ja lauka **Darījuma veids** ir iestatīts uz *Rēķins*. |
| Ietvert brīvo tekstu | Iestatiet šo opciju kā *Jā*, lai iekļautu brīvā teksta rēķinus aprēķinā. Brīvā teksta rēķinus var ietvert tikai darījuma rindām, kurās lauks **Krājuma kods** ir iestatīts uz *Visi*. |
| Iekļaut nosegšanas atlaidi | Iestatiet šo opciju kā *Jā*, lai samazinātu atlaidi par pirmo nosegšanas atlaidi. Ir pieņemts, ka organizācija izmantos pirmo nosegšanas atlaidi. Iestatiet šo opciju uz *Nē*, lai aktivizētu nosegšanas atlaides vēlāku izmantošanai. |
| Dokumentu piezīmes | Ievadiet piezīmes, kas atlaižu darbību žurnāla rindās jāizmanto kā darbības teksts. |

### <a name="settings-on-the-dates-tab"></a>Iestatījumi cilnē Datumi

Cilnes **Datumi** kopsavilkuma cilnē **Atlaižu pārvaldības informācija** iestatījumi nosaka cilnē **Vispārīgi** norādīto aprēķinu biežumu un laiku. Tie nosaka, kā aprēķini tiek aprēķināti apstrādes laikā.

Šajā cilnē varat norādīt datumu diapazonu, kam atlasītā darījuma rinda ir derīga, un aprēķināšanas biežumu. Varat arī norādīt, vai un kad jāgrāmato garantijas.

Rīkjoslas pogas var izmantot, lai pievienotu režģim datumu rindas vai noņemtu tās. Ja eksistē vairākas datumu rindas, derīgie datumu diapazoni nedrīkst pārklāties. Pretējā gadījumā, mēģinot saglabāt darījumu, saņemsit kļūdas ziņojumu.

Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai rindai.

| Lauks | Apraksts |
|---|---|
| No datuma | Ievadiet pirmo datumu, uz kuru attiecas datuma rinda. Ja darījuma virsrakstā ir norādīti datumi "no" un "līdz", tie tiek izmantoti kā noklusējuma vērtības katrai jaunai datuma rindai. |
| Līdz datumam | Ievadiet pēdējo datumu, uz kuru attiecas datuma rinda. Ja darījuma virsrakstā ir norādīti datumi "no" un "līdz", tie tiek izmantoti kā noklusējuma vērtības katrai jaunai datuma rindai. |
| Kam | Norādiet, cik bieži jāaprēķina darījuma rinda. Šeit ievadiet veselu skaitli un pēc tam vienību laukā **Uzkrāt pēc**. Piemēram, lai aprēķinātu katru otro nedēļu, iestatiet lauku **Uz** uz *2* un lauku **Uzkrāt pēc** uz *Nedēļām*. |
| Uzkrāt pēc | Atlasiet vienību, kas attiecas uz iestatījumu **Uz**. Atlasīt *Darbmūžu*, lai aprēķinātu visu darījuma rindas darbmūžu. Atlasiet *Pielāgotu periodu*, lai atlasītu Virsgrāmatā definēto periodu. Šajā gadījumā jāiestata arī lauks **Perioda tips**. |
| Perioda tips | Šis lauks ir pieejams tikai tad, ja lauks **Uzkrāt pēc** ir iestatīts uz *Pielāgots periods*. Atlasei pieejamās vērtības ir no Virsgrāmatā noteiktām periodu tipiem. |
| Nedēļas pirmā diena | Norādiet, kā periodam tiek identificētas nedēļas. Šis lauks ir pieejams tikai tad, ja lauks **Uzkrāt pēc** ir iestatīts uz *Nedēļas*. |
| Prasība pēc | Norādiet, cik bieži uz darījuma rindu var pieprasīt atlaidi. Šeit ievadiet veselu skaitli un pēc tam vienību laukā **Pieprasīt pēc**. |
| Pieprasīt pēc | Atlasiet vienību, kas attiecas uz iestatījumu **Pieprasīt pēc**. Atlasīt *Mūžs*, lai atļautu prasības tikai vienu reizi visa darījuma rindas darbmūžs. Atlasiet *Pielāgotu periodu*, lai atlasītu Virsgrāmatā definēto periodu. Šajā gadījumā jāiestata arī lauks **Prasības perioda tips**. |
| Prasības perioda veids | Šis lauks ir pieejams tikai tad, ja lauks **Pieprasīt pēc** ir iestatīts uz *Pielāgots periods*. Atlasei pieejamās vērtības ir no Virsgrāmatā noteiktām periodu tipiem. |
| Grāmatošanas process | Atzīmējiet šo izvēles rūtiņu, ja prasības rinda ir jāapstrādā grāmatošanas laikā. Šī opcija ir pieejama tikai darījuma rindām, kur lauks **Darījuma veids** cilnē **Vispārīgi** ir iestatīts uz *Piegādāts* vai *Rēķins*. Uzkrājumiem uzkrājumi tiks grāmatoti, kad tiks ģenerēta piegādes pavadzīme vai rēķins. |
| Garantija pēc | Šis lauks attiecas tikai uz honorāru darījumiem. Norādiet, cik bieži autoritātes garantijas jāaprēķina periodā, ko nosaka **Uzkrāt pēc** iestatījums. Šeit ievadiet veselu skaitli un pēc tam laukā **Garantija apmaksāta** atlasiet apmaksas laiku. |
| Garantija apmaksāta | <p>Šis lauks attiecas tikai uz honorāru darījumiem. Lai noteiktu garantijas aprēķina biežumu, tas darbojas kopā ar lauku **Garantija par**. Atlasiet vienu no šīm vērtībām:</p><ul><li><p>*Perioda sākums* – garantija tiek maksāta datuma rindai definētā līguma perioda sākumā. Pilnā garantija tiek apstrādāta vispirms. Tikai to honorāru vērtība, kas pārsniedz garantijas summu, tiek grāmatota kā honorārs. Lūk, piemērs:</p><ul><li>**Garantijas minimums:** $10000 par diviem mēnešiem.</li><li>**1. mēnesis:** $10000 tika grāmatoti kā garantija, un $0 tika grāmatoti kā honorāri.</li><li>**2. mēnesis:** $2000 tika grāmatoti kā honorāri, un $0 tika grāmatoti kā garantijas.</li><li>**Darba aprēķins:** *Atlikušās garantijas* – *Grāmatotie honorāri* $0 = $0 – $2,000 = -$2000.</li></ul><p>Tā kā ir nepieciešams $2000 apmaksas maksājums, tiek izveidots žurnāls $2000.</p><p>**Piezīme:** Garantija ir jāaprēķina un jāgrāmato kopā ar ieturējumu uzkrājumiem pirmajam periodam.</p></li><li><p>*Perioda beigas* – garantija netiek maksāta līdz ieturējumu līguma beigām, kā norādīts datuma rindā. Lūk, piemērs:</p><ul><li>**Garantijas minimums:** $10000 par diviem mēnešiem.</li><li>**1. mēnesis:** $5000 tika grāmatoti kā honorāri, un tika izveidots žurnāls.</li><li>**2. mēnesis:** $7000 tika grāmatoti kā honorāri, un tika izveidots žurnāls.</li><li>**Darba aprēķins:** Tā kā honorāru summa pārsniedz garantijas summu, $0 tiek grāmatoti garantiju kontā.</li></ul><p>**Piezīme:** Garantija ir jāaprēķina un jāgrāmato tikai kopā ar ieturējumu uzkrājumiem un atlaižu darījumiem pēdējam periodam.</p></li></ul> |
| Garantijas minimums | Šis lauks attiecas tikai uz honorāru darījumiem. Ievadiet minimālo garantijas summu par honorāru darījuma virsrakstā definētajā valūtā. |

### <a name="settings-on-the-lines-tab"></a>Iestatījumi cilnē Rindas

Kopsavilkuma cilnes **Atlaižu pārvaldības informācija** cilnē **Rindas** varat iestatīt aprēķina metodi un pamatu atlasītajai darījuma rindai. Katra aprēķina rinda izveido daudzumu vai vērtības slieksni un saistīto atlīdzības summu vai krājumus. Lauks **Pamata** cilnē **Vispārīgi** norāda, vai katra aprēķina rinda tiek balstīta uz daudzumu vai vērtību.

Rīkjoslas pogas var izmantot, lai pievienotu režģim aprēķinu rindas vai noņemtu tās. Var būt jebkāds aprēķinu rindu skaits. Tomēr, ja eksistē vairākas aprēķina rindas, daudzums "līdz" un "no" vai vērtību diapazoni nedrīkst pārklāties.

Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai aprēķina rindai.

| Lauks | Apraksts |
|---|---|
| No daudz./vērtības | Ievadiet minimālo daudzumu vai vērtību, uz kuru attiecas aprēķina rinda. |
| Līdz daudz/vērtībai | Ievadiet maksimālo daudzumu vai vērtību, uz kuru attiecas aprēķina rinda. |
| Atlaižu pārvaldības metode | <p>Šis lauks ir pieejams tikai darījumiem, kuru **Atlaides izvades** lauks virsrakstā ir iestatīts uz *Finanšu*. Atlasiet metodi, ko izmantot atlaides aprēķināšanai:</p><ul><li>*Fiksēts* – rindai tiek izmantota fiksētas cenas summa.</li><li>*Procenti* — tiek izmantoti pārdošanas summas procenti.</li><li>*Likme* – tiek izmantota fiksēta cenas summa katram pasūtījumam.</li></ul><p>**Svarīgi:** ir ieteicams izmantot to pašu metodi katrai aprēķina rindai cilnē **Rindas**. Ja nepieciešama jauna metode, izveidojiet jaunu darījuma rindu. Atcerieties, ka varat izmantot pogu **Kopēt rindu** kopsavilkuma cilnē **Atlaižu pārvaldība**, lai no esošas darījuma rindas izveidotu jaunu darījuma rindu.</p><p>**Piezīme:** Ja lauks **Atlaides izvade** ir iestatīts uz *Krājums*, šis lauks vienmēr tiek iestatīts uz *Fiksēts*. Plašāku informāciju par to, kā norādīt krājumus, skatiet tekstu, kas seko šai tabulai. |
| Atlaižu pārvaldības summa | Šis lauks ir pieejams tikai darījumiem, kuru **Atlaides izvades** lauks virsrakstā ir iestatīts uz *Finanšu*. Ievadiet summu, kas jāizmanto atlaides aprēķinam, pamatojoties uz metodi, ko izvēlējāties laukā **Atlaižu pārvaldības metode**. |

Kā tika norādīts iepriekšējā tabulā, darījumiem, kur **Atlaides izvades** lauks galvenē ir iestatīts uz *Krājums*, jums ir jānorāda krājumi, kas tiks nodrošināti katrai aprēķina rindai cilnē **Rindas**. Lai norādītu krājumus, rīkojieties šādi.

1. Cilnē **Rindas** izveidojiet nepieciešamo aprēķina rindu, ja tās nav, un atlasiet to.
1. Ja darījums nav saglabāts kopš aprēķina rindas izveides, darbību rūtī atlasiet **Saglabāt**.
1. Cilnē **Rindas** atlasiet **Krājumi**.
1. Lai režģim pievienotu krājumus, izmantojiet pogas darbību rūtī, vai noņemiet krājumus pēc vajadzības lapā **Krājumi**. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Krājuma kods** – atlasiet krājumu, kas tiks norādīts.
    - **(Citas dimensijas)** – ja nepieciešams izmantot vairākas dimensijas, lai definētu krājumu (piemēram, krājumu konfigurāciju, izmēru, krāsu, stilu, vietu vai noliktavu), norādiet tās. Lai pievienotu vai noņemtu pieejamās dimensijas, darbību rūtī atlasiet **Rādīt dimensijas**.
    - **Daudzums** – ievadiet daudzumu, kas tiks nodrošināts pēc atlasītās aprēķina rindas sliekšņa beigām.
    - **Vienība** – atlasiet vienību, kurā ir norādīta **Daudzuma** vērtība.
    - **Vairāki** – šis lauks darbojas kopā ar lauku **Daudzums**. Piemēram, krājumu rindā lauku **Daudzums** iestatiet uz *2* un lauku **Vairāki** *100*. Ja pēc tam kopējais pārdošanas pasūtījuma daudzums ir 150, divi krājumi būs brīvi (divi uz 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Cilnes Krājumu dimensijas iestatījumi

Kopsavilkuma cilnes **Krājumu dimensijas** kopsavilkuma cilnē **Atlaižu pārvaldības informācija** ir redzamas visas atlasītajai darījuma rindai norādītās preces pieejamās dimensiju vērtības. Tajā ir ietvertas dimensijas, kas nav parādītas kopsavilkuma cilnē **Atlaižu pārvaldība**. Vērtības varat rediģēt tikai tām dimensijām, kas attiecas uz atlasīto preci.

Jūs varat pievienot papildu dimensijas režģim kopsavilkuma cilnē **Atlaižu pārvaldība**, darbību rūtī atlasot **Rādīt dimensijas**.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Darījuma rindu aprēķina metodes

Katru reizi iestatot informāciju vienai no darījuma rindām, kā aprakstīts iepriekšējā sadaļā, jums ir jāizvēlas aprēķina metode tai rindai. Šajā sadaļā skaidroti katra aprēķina metode un sniegti piemēri, kas parāda, kā katra metode aprēķina kopējo atlaidi pasūtījumiem un darījuma rindām. Šajos piemēros pasūtījumi un darījuma rindas ir identiskas. Atšķiras tikai aprēķina metodes.

### <a name="stepped-calculation-method"></a>Pakāpeniskā aprēķināšanas metode

Kompromisa aprēķināšanas metode tiek aprēķināta, balstoties uz soli pa solim, kur katra darījuma rinda inkrementāli sniedz ieguldījumu atlaides virzienā, līdz tiek sasniegts pārdošanas daudzums vai vērtība. Soļi var tikt balstīti vai nu uz pārdoto preču daudzumu, vai arī uz pārdoto preču vērtību, atkarībā no lauka **Pamata** iestatījuma cilnes **Vispārīgi** kopsavilkuma cilnē **Atlaižu pārvaldības informācija**.

Piemēram, darījuma rinda ir iestatīta tā, lai **Aprēķina metodes** lauks tiktu iestatīts uz *Pakāpenisks* un **Pamata** lauks būtu iestatīts uz *Vērtība*. Tā ietver aprēķina rindas, kurās ir sniegtas šādas atlaides:

- **A rinda:** 10 procenti līdz $1000
- **B rinda:** 25 procenti līdz $2500

Ja iegādāto vai pārdoto preču vērtība ir $2000 pārdoto preču $350 tiek aprēķināta šādi:

- **Atlaide (A):** *Slieksnis (A)* × *Procenti (A)* = $1000 × 10 procenti = $100
- **Atlaide (B):** (*Pārdotā vērtība* – *Slieksnis (A)*) × *Procenti (B)* = ($2000 - $1000) × 25 procenti = $250
- **Kopējā atlaide:** *Atlaide (A)* + *Atlaide (B)* = $100 + $250 = $350

Ja lauks **Pamata** ir iestatīts uz *Daudzums* *Vērtības* vietā, pakāpeniskā aprēķina metode darbojas līdzīgi. Pirmais solis tiek izmantots identificētais daudzums, līdz tiek sasniegts otrais solis. Otrais solis tiek izmantots identificētais daudzums, līdz tiek sasniegts trešais solis. Šis process tad turpinās caur visiem turpmākajiem soļiem.

### <a name="cumulative-calculation-method"></a>Kumulatīvā aprēķina metode

Kumulatīvā aprēķina metode izmanto tikai vienu aprēķina rindu, lai aprēķinātu atlaidi. Ja darījuma rindai ir pieejamas vairākas aprēķina rindas, sasniegtā augstākā vērtība vai augstākā daudzuma aprēķina rinda tiek izmantota visam daudzumam vai vērtībai. Līdzīgi citām aprēķina metodēm kopējā metode izmanto lauka **Pamata** iestatījums cilnes **Vispārīgi** kopsavilkuma cilnē **Atlaižu pārvaldības informācija**, lai noteiktu, vai atlaides aprēķināšanai tiek izmantots pārdošanas daudzums vai pārdošanas vērtība.

Piemēram, darījuma rinda ir iestatīta tā, lai **Aprēķina metodes** lauks tiktu iestatīts uz *Kumulatīvs* un **Pamata** lauks būtu iestatīts uz *Vērtība*. Tā ietver aprēķina rindas, kurās ir sniegtas šādas atlaides:

- **A rinda:** 10 procenti līdz $1000
- **B rinda:** 25 procenti līdz $2500

Ja iegādāto vai pārdoto preču vērtība ir $2000, aprēķinā tiek izmantota tikai B rinda. Galīgā atlaide par $500 tiek aprēķināta šādi:

- **Kopējā atlaide:** *Pārdotā vērtība* × *Atlaide (B)* = $2000 × 25 procenti = $500

### <a name="rolling-calculation-method"></a>Secīgā aprēķināšanas metode

Secīģā aprēķināšanas metode aprēķina visas iespējamās aprēķina rindas darījumam. Ja ir vairākas aprēķina rindas un tiek sasniegta vairāk nekā viena no tām, tiks izmantotas visas sasniegtās aprēķina rindas, bet augstākas sliekšņi attiecas uz katru procentuālo daļu. Līdzīgi citām aprēķina metodēm kopējā metode izmanto lauka **Pamata** iestatījums cilnes **Vispārīgi** kopsavilkuma cilnē **Atlaižu pārvaldības informācija**, lai noteiktu, vai atlaides aprēķināšanai tiek izmantots pārdošanas daudzums vai pārdošanas vērtība.

Piemēram, darījuma rinda ir iestatīta tā, lai **Aprēķina metodes** lauks tiktu iestatīts uz *Secīgs* un **Pamata** lauks būtu iestatīts uz *Vērtība*. Tā ietver aprēķina rindas, kurās ir sniegtas šādas atlaides:

- **A rinda:** 10 procenti līdz $1000
- **B rinda:** 25 procenti līdz $2500

Ja iegādāto vai pārdoto preču vērtība ir $2000, galīgā atlaide par $600 tiek aprēķināta šādi:

- **Atlaide (A):** *Slieksnis (A)* × *Procenti (A)* = $1000 × 10 procenti = $100
- **Atlaide (B):** *Pārdotā vērtība* × *Procenti (B)* = $2000 × 25 procenti = $500
- **Kopējā atlaide:** *Atlaide (A)* + *Atlaide (B)* = $100 + $500 = $600

### <a name="total-calculation-method"></a>Galīgā aprēķina metode

Galīgā aprēķina metode izmanto visas aprēķina rindas atlaides aprēķināšanai. Tā piemēro kopējo daudzumu, lai aprēķinātu atlaidi katrai sasniegtajai aprēķina rindai, un katra aprēķina rinda piemēro tās procentuālo vērtību pilnai summai. Līdzīgi citām aprēķina metodēm kopējā metode izmanto lauka **Pamata** iestatījums cilnes **Vispārīgi** kopsavilkuma cilnē **Atlaižu pārvaldības informācija**, lai noteiktu, vai atlaides aprēķināšanai tiek izmantots pārdošanas daudzums vai pārdošanas vērtība.

Piemēram, darījuma rinda ir iestatīta tā, lai **Aprēķina metodes** lauks tiktu iestatīts uz *Kopējs* un **Pamata** lauks būtu iestatīts uz *Vērtība*. Tā ietver aprēķina rindas, kurās ir sniegtas šādas atlaides:

- **A rinda:** 10 procenti līdz $1000
- **B rinda:** 25 procenti līdz $2500

Ja iegādāto vai pārdoto preču vērtība ir $2000, galīgā atlaide par $700 tiek aprēķināta šādi:

- **Atlaide (A):** *Pārdotā vērtība* × *Procenti (A)* = $2000 × 10 procenti = $200
- **Atlaide (B):** *Pārdotā vērtība* × *Procenti (B)* = $2000 × 25 procenti = $500
- **Kopējā atlaide:** *Atlaide (A)* + *Atlaide (B)* = $200 + $500 = $700
