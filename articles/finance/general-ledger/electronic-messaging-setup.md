---
title: Elektronisko ziņojumu iestatīšana
description: Šajā rakstā ir sniegta informācija, kā iestatīt elektronisko ziņojumu (EM) funkcionalitāti.
author: AdamTrukawka
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 12beb1adbfa4e2f235c8a7c69e786d342c4a4f68
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279308"
---
# <a name="set-up-electronic-messages"></a>Elektronisko ziņojumu iestatīšana

[!include [banner](../includes/banner.md)]

Funkcionalitāte **Elektroniskie ziņojumi** (EM) palīdz uzturēt dažādus elektronisko pārskatu veidošanas procesus dažādiem dokumentu tipiem. Dažos sarežģītos scenārijos, kas atbalsta [valstij raksturīgus pārskatu līdzekļus](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality) EM funkcionalitāte ir iestatīta daudzu ziņojumu statusu, ziņojumu vienumu statusu, darbību, papildu lauku un izpildāmo klašu kombinācija. Šādu scenāriju gadījumā datu elementu pakotnes ir pieejamas importam. Ja izmantojat šīs datu elementu pakotnes, importējiet tās juridiskajā personā, izmantojot rīku Datu pārvaldība. Plašāku inf. par to, kā izmantot rīku Datu pārvaldība, sk. sadaļā [Datu pārvaldība](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Ja neimportējat datu elementu pakotni, varat manuāli iestatīt EM funkcionalitāti. Šajā gadījumā ir jāiestata šādi elementi:

- [Numuru sērijas](#sequences)
- [Ziņojuma krājuma veidi](#types)
- [Ziņojuma krājuma statusi](#item)
- [Ziņojuma statusi](#statuses)
- [Papildlauki](#additional)
- [Izpildāmās klases darbības](#executable)
- [Ierakstu aizpildīšanas darbības](#populate)
- [Aizpildīt ierakstus no vairākiem uzņēmumiem](#multiple-companies-populate)
- [Tīmekļa lietojumprogrammas](#applications)
- [Tīmekļa pakalpojuma iestatījumi](#settings)
- [Ziņojuma apstrādes darbības](#actions)
- [Elektroniska ziņojuma apstrāde](#processing)

Nākamajās sadaļās ir sniegta plašāka inform. par katru no šiem elementiem.

## <a name="number-sequences"></a><a id="sequences"></a>Numuru sērijas

Iestatiet numuru sērijas gan ziņojumiem, gan ziņ. vienumiem. Numuru sērijas tiek izmantotas, lai automātiski numurētu ziņojumus un ziņojumu vienumus. Piešķirtie numuri tiek izmantoti kā ziņojumu un ziņojumu vienumu unikāli identifikatori sistēmā. Numuru sērijas elektroniskajai ziņojumapmaiņai var iestatīt, dodoties uz **Virsgrāmata** \> **Virsgrāmatas iestatīšana** \> **Virsgrāmatas parametri**.

## <a name="message-item-types"></a><a id="types"></a>Ziņojuma krājuma veidi

Ziņojumu vienumu veidi norāda ierakstu veidus, kas tiek izmantoti elektron. ziņojumos. Ziņ. vien. veidus var iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu vienumu veidi**.

## <a name="message-item-statuses"></a><a id="item"></a>Ziņojuma krājuma statusi

Ziņojumu krājumu statusi norāda statusus, kas attiecas uz ziņojumu vienumiem apstrādē, kuru iestatāt. Ziņ. vien. statusus var iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu vienumu statusi**.

Ziņojuma vienuma statusa parametrs **Atļaut dzēšanu** nosaka, vai var dzēst ziņojuma vienumus ar šo statusu, izmantojot lapu **Elektroniskie ziņojumi** vai lapu **Elektronisko ziņojumu vienumi**.

## <a name="message-statuses"></a><a id="statuses"></a>Ziņojuma statusi

Iestatiet ziņojumu statusus, kam jābūt pieejamiem ziņojumu apstrādē. Ziņ. statusus var iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu statusi**.

Nākamajā tabulā ir aprakstīti lauki lapā **Ziņojuma statusi**.

| Lauka nosaukums          | Apraksts |
|---------------------|-------------|
| Ziņojuma statuss      | Ievadiet unikālu ziņojuma statusa nosaukumu. Ziņojumu statusi tiek izmantoti, lai raksturotu elektroniskā ziņojuma stāvokli katrā noteiktā brīdī. Jūsu ievadītais nosaukums tiek rādīts lapā **Elektroniskie ziņojumi** un žurnālā, kas saistīts ar elektroniskajiem ziņojumiem. |
| Apraksts         | Ievadiet ziņojuma statusa aprakstu. |
| Atbildes tips       | Atlasiet ziņojuma statusa atbildes tipu. Dažu darbību apstrāde var radīt vairāk nekā vienu atbildes tipu. Piemēram, tipa **Tīmekļa pakalpojums** darbības var izraisīt vai nu atbildes tipu **Izpildīts veiksmīgi**, vai **Tehniska kļūda** atkarībā no darbības izpildes rezultāta. Šajā gadījumā definējet ziņojuma statusus abiem atbilžu tipiem. Papildinformāciju par darbību tipiem un atbilžu tipiem, kas tiem ir saistītas, [skatiet](#action-types) tālāk šī raksta sadaļā Ziņojumu apstrādes darbību veidi. |
| Ziņojuma krājuma statuss | Dažreiz elektroniskā ziņojuma statuss attiecīgi ietekmē saistīto ziņojumu vienumu statusu. Atlasiet ziņojuma vienuma statusu šajā laukā, lai saistītu to ar ziņojuma statusu. |
| Atļaut dzēšanu        | Atzīmējiet šo izvēles rūtiņu, ja lietotāji var dzēst elektroniskos ziņojumus, kuriem ir šis statuss, lapā **Elektroniskie ziņojumi**. |

## <a name="additional-fields"></a><a id="additional"></a>Papildlauki

EM funkcionalitāte ļauj jums apkopot ierakstus no darbību tabulām Microsoft Dynamics 365 Finanses kā ziņojumu krājumus. Šādā veidā var sagatavot ierakstus pārskatiem un pēc tam ziņot par tiem. Tomēr transakciju tabulās dažreiz nav pietiekami daudz informācijas, lai aizpildītu ierakstus tādā veidā, kas atbilst pārskatu izveides prasībām. Lai aizpildītu visu informāciju, kas ir jāziņo par ierakstu, varat izveidot papildu laukus. Papildu laukus var saistīt gan ar ziņojumiem, gan ziņojumu vienumiem. Papildu laukus var iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Papildu lauki**.

Nākamajā tabulā ir aprakstīti galvenie lauki lapā **Papildu lauki**.

| Lauks       | Apraksts |
|-------------|-------------|
| Lauka nosaukums  | Ievadiet ar lauku saistīto elektronisko ziņojumu vai ziņojumu vienumu papildu lauka nosaukumu. Šis nosaukums tiek parādīts lietotāja interfeisā, strādājot ar procesu. Nosaukumu var izmantot arī elektronisko pārskatu ER konfigurācijās, kas ir saistītas ar procesu. |
| Apraksts | Ievadiet papildu lauka aprakstu. |
| Lietotāja labojumi   | Atlasiet šai opcijai iestatījumu **Jā**, ja lietotāji var mainīt papildu lauka vērtību lietotāja interfeisā. |
| Skaitītājs     | Atlasiet šai opcijai iestatījumu **Jā**, ja papildu laukā jābūt numuru sērijai elektroniskajā ziņojumā. Papildu lauka vērtība tiek aizpildīta automātiski darbības ar tipu **Elektroniskā pārskata veidošanas eksports** palaišanas laikā. |
| Paslēpts      | Iestatiet šo opciju kā **Jā**, ja papildu lauks ir jāpaslēp UI lapā **Elektroniskie ziņojumi** vai lapā **Elektroniskā ziņojuma vienumi**. |

Kopsavilkuma cilnē **Vērtības** var iepriekš definēt vērtības, kas var būt papildu laukam. Šīs vērtības pēc tam ir pieejamas lietotājiem, lai tos atlasītu. Tādēļ apstrādes laikā tos nav manuāli jāaizpilda. Tabulā ir sniegts lauku apraksts.

| Lauks                | Apraksts |
|----------------------|-------------|
| Lauka vērtība          | Ievadiet lauka vērtību, ko izmantot ziņojumam vai ziņojuma vienumam pārskata veidošanas laikā. |
| Apraksts          | Ievadiet lauka vērtības aprakstu. |
| Konta veids         | Dažas lauku vērtības var lietot tikai ar noteiktiem konta tipiem. Atlasiet vienu no šīm vērtībām: **Visi**, **Debitors** vai **Kreditors**. |
| Konta kods         | Ja atlasījāt **Debitors** vai **Kreditors** laukā **Konta tips**, varat vēl vairāk ierobežot lauka vērtības izmantošanu ar noteiktu grupu vai tabulu. |
| Konta/grupas numurs | Ja atlasījāt **Debitors** vai **Kreditors** laukā **Konta tips** un ja ievadījāt grupu vai tabulu laukā **Konta kods**, šajā laukā var ievadīt noteiktu grupu vai kontrahentu. |
| Ir spēkā            | Norādiet datumu, kad vērtība ir jāsāk ņemt vērā. |
| Termiņa beigas           | Norādiet datumu, kad vērtība ir jābeidz ņemt vērā. |

Pēc noklusējuma tādu kritēriju kombinācijas, kas definēti laukos **Konta/grupas numurs**, **Konta kods**, **Ir spēkā** un **Termiņa beigas**, neietekmē vērtību atlasi papildu laukiem. Tomēr šīs kombinācijas var tikt izmantotas izpildāmā klasē, lai īstenotu noteiktu loģiku, kas aprēķina papildu lauku vērtības.

## <a name="executable-class-settings"></a><a id="executable"></a>Izpildāmās klases darbības

Izpildāmā klase ir X++ metode vai klase, ko elektroniskā ziņojumu apstrāde var izsaukt saistībā ar darbību, ja procesam ir vajadzīga novērtēšana.

Apstrādes laikā varat manuāli iestatīt izpildāmo klasi, kas ir jāizsauc, dodoties uz **Nodoklis** \> **Iestatījums** \> **Elektroniskie ziņojumi** \> **Izpildāmās klases iestatījumi**. Lapā **Izpildāmās klases iestatījumi** izveidojiet rindu un iestatiet šādus laukus.

| Lauks                 | Apraksts |
|-----------------------|-------------|
| Izpildāmā klase      | Ievadiet nosaukumu, kas tiks izmantots, iestatot ziņojumu apstrādes darbību, saistībā ar kuru tiek izsaukta šī klase. |
| apraksts           | Ievadiet izpildāmās klases aprakstu. |
| Izpildāmās klases nosaukums | Atlasiet X++ izpildāmo klasi. |
| Izpildes līmenis       | Šis lauks tiek iestatīts autom., jo vērtība ir iepriekš definēta atlasītajai izpildāmajai klasei. Šis lauks ierobežo saistītās vērtēšanas palaišanas līmeni. |
| Klases apraksts     | Šis lauks tiek iestatīts autom., jo vērtība ir iepriekš definēta atlasītajai izpildāmajai klasei. |
| Darbības tips           | Šis lauks ir pieejams, kad līdzeklis **\[EM\] Izpildāmas klases darbības tips** ir ieslēgts darbvietā **Līdzekļu pārvaldība**. Lietojiet šo lauku, lai norādītu izpildāmās klases darbības tipu. Šis lauks sniedz precīzāku kontroli pār nākamajām darbībām, kas pieejamas elektroniskajam ziņojumam lapā **Elektroniskie ziņojumi**. |

Dažām izpildāmām klasēm var būt obligātie parametri, kas jānosaka pirms izpildāmā klase tiek palaista pirmo reizi. Lai definētu šos parametrus, Darbību rūtī atlasiet **Parametri**. Parādītajā dialoglodziņā iestatiet aukus un pēc tam atlasiet **Labi**. Ir svarīgi atlasīt vienumu **Labi**. Citādi parametri netiks saglabāti datu bāzē, un izpildāmā klase netiks pareizi izsaukta.

## <a name="populate-records-actions"></a><a id="populate"></a>Ierakstu aizpildīšanas darbības

Ierakstu aizpild. darbības izmanto, lai iestatītu darb., kas pievieno ierakstus ziņoj. vienumu tabulā, lai tos varētu pievienot elektr. ziņojumam. Piemēram, ja elektroniskajam ziņojumam ir jāziņo par debitora rēķiniem, ir jāiestata ierakstu aizpildīšanas darbība, kas ir saistīta ar lauku **Datu avots** tabulā Debitoru rēķinu žurnāls.

Ierakstu aizpild. darbības var iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ier. aizpild. darb**. Izveidojiet jaunu ierakstu katrai darbībai, kas pievieno ierakstus tabulā, un iestatiet šādus laukus.

| Lauks       | Apraksts |
|-------------|-------------|
| Vārds        | Ievadiet nosaukumu darbībai, kas aizpilda ierakstus jūsu procesā. |
| Apraksts | Ievadiet ierakstu aizpildīšanas darbības aprakstu. |

Cilnē **Datu avotu iestatīšana** pievienojiet rindu katram datu avotam, kas tiek izmantots procesā, un iestatiet šādus laukus.

| Lauks                  | apraksts |
|------------------------|-------------|
| Vārds/nosaukums                   | Ievadiet datu avota nosaukumu. |
| Ziņojuma krājuma veids      | Atlasiet ziņojumu vienuma tipu, lai izmantotu, kad tiek izveidoti ieraksti datu avotam. |
| Konta veids           | Atlasiet konta tipu, lai jāsaistītu ar ierakstiem no datu avotu. |
| Galvenās tabulas nosaukums      | Atlasiet tabulu, kura būs datu avotam. |
| Dokumenta numura lauks  | Atlasiet lauku, no kura ņems dokumenta numuru atlasītajā galvenajā tabulā. Šī lauka vērtība tiek izmantota kā ziņojuma krājuma lauka **Dokumenta numurs** vērtība. |
| Dokumenta datuma lauks    | Atlasiet lauku, no kura ņems dokumenta datumu atlasītajā galvenajā tabulā. Šī lauka vērtība tiek izmantota kā ziņojuma krājuma lauka **Ziņojuma krājuma datums** vērtība. |
| Dokumenta konta lauks | Atlasiet lauku, no kura ņems dokumenta kontu atlasītajā galvenajā tabulā. Šī lauka vērtība tiek izmantota kā ziņojuma krājuma lauka **Konta numurs** vērtība. |
| Uzņēmums                | Šis lauks ir pieejams, ja darbvietā **Līdzekļa pārvaldība** ir ieslēgti līdzeklim **Starpuzņēmumu vaicājumi aizpildīto ierakstu darbībām**. Izmantojiet šo funkciju, lai iestatītu starpuzņēmumu datu avotus aizpildīto ierakstu darbībām. Datus var ienest no vairākiem uzņēmumiem. |
| Lietotāja vaicājums             | <p>Ja iestatāt vaicājumu, virs režģa atlasot darbvietā **Labot vaicājumu** un norādot kritērijus, kas jāpiemēro atlasītajai vispārējai tabulai, kurā tiek ievadīti dati, šī izvēles rūtiņa tiek atzīmēta automātiski. Pretējā gadījumā visi ieraksti tiek aizpildīti no atlasītā galvēnās tabulas avota.</p><p>Ja līdzeklis **Starpuzņēmumu vaicājumi par aizpildīto ierakstu darbībām** ir ieslēgts darbvietā **Līdzekļu pārvaldība**, un ieraksti ir jāievāc no vairākiem uzņēmumiem, pievienojiet rindu katrai papildu juridiskajai personai, kas jāiekļauj pārskatos. Katrai jaunai rindai atlasiet **Labot vaicājumu** un norādiet saistīto kritēriju, kas ir specifisks juridiskajai personai, kas ir norādīta rindas laukā **Uzņēmums**. Kad režģis **Datu avota iestatījums** būs pabeigts, tas saturēs rindas visām juridiskajām personām, kas jāiekļauj pārskatā.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a> Aizpildīt ierakstus no vairākiem uzņēmumiem

Ja jūsu uzņēmumam ir jāsniedz pārskats no vairākām juridiskajām personām vienā finanšu datu bāzē, [iestatiet](#populate) aizpildīto ierakstu darbības visām juridiskajām personām, no kurām dati jāiekļauj pārskatā.

Lai iespējotu šo spēju finanšu vidē, sekojiet šiem soļiem. 

1. Pārejiet uz **sadaļu Darbalauku** \> **līdzekļu pārvaldība.**
2. Atrodiet un atlasiet **starpuzņēmumu vaicājumus aizpildīto ierakstu darbību līdzeklim** sarakstā.
3. Atlasiet **Iespējot tagad**. 

Lai iestatītu aizpildīto [ierakstu darbības vairākiem](#populate) uzņēmumiem, no kuriem dati jāiekļauj pārskatā, sekojiet šiem soļiem.

1. Doties uz nodokļu **iestatīšanas** \> **·** \> **elektroniskajiem ziņojumiem** \> **Aizpildīt ierakstu darbības.**

    Ja starpuzņēmumu **vaicājumi** aizpildīto ierakstu darbību funkcijai ir iespējoti, **datu avotu iestatīšanas** **režģis** darbību lapā Aizpildītie ieraksti ietver **lauku** Uzņēmums. Esošiem ierakstiem, kas tika izveidoti [aizpildīto ierakstu darbību vispārīgās iestatīšanas laikā](#populate), šis lauks rāda pašreizējās juridiskās personas identifikatoru.

2. Datu avotu **iestatījumu** režģī pievienojiet rindu katrai juridiskajai personai, kas jāiekļauj pārskatā, un iestatiet šādus laukus.

    | Lauka nosaukums             | Vērtība |
    |------------------------|-------|
    | Vārds/nosaukums                   | Ievadiet teksta vērtību, kas palīdzēs saprast, no kurienes ir šis ieraksts. Piemēram, ievadiet **Datu avota nosaukumu - 1. filiāle**. |
    | Ziņojuma krājuma veids      | Atlasiet ziņojuma krājuma tipu, kas nepieciešams jūsu EM apstrādei. |
    | Konta veids           | Norādiet konta tipu, kas nepieciešams jūsu EM apstrādei. Ja EM apstrādei nav specifisku kontu tipu, atlasiet **Visi**. |
    | Galvenās tabulas nosaukums      | Norādiet galvenās tabulas nosaukumu, kas nepieciešams jūsu EM apstrādei. |
    | Dokumenta numura lauks  | Norādiet lauku, kas satur dokumenta numuru jūsu EM apstrādes ierakstos. |
    | Dokumenta datuma lauks    | Norādiet lauku, kas satur dokumenta datumu jūsu EM apstrādes ierakstos. |
    | Dokumenta konta lauks | Norādiet lauku, kas satur dokumenta kontu jūsu EM apstrādes ierakstos. |
    | Uzņēmums                | Atlasiet filiāles juridiskās personas ID. |
    | Lietotāja vaicājums             | Šī izvēles rūtiņa tiek automātiski atzīmēta, kad definējat kritērijus, atlasot **Vaicājumu Labot**. |

3. Katrai jaunai rindai atlasiet **Vaicājumu** Rediģēt un norādiet **juridiskās personas saistītos kritērijus, kas ir norādīti** rindas laukā Uzņēmums.

## <a name="web-applications"></a><a id="applications"></a>Tīmekļa lietojumprogrammas

Tīmekļa programmas iestatījumus izmanto, lai iestatītu tīmekļa programmu, lai tā atbalstītu Open Authorization (OAuth) 2.0. OAuth ir atvērts standarts, kas ļauj lietotājam piešķirt “drošu deleģēto piekļuvi” programmai lietotāju vārdā, nenorādot lietotāju piekļuves akreditācijas datus. Varat arī izpildīt autorizēšanas procesu, iegūstot autorizācijas kodu un piekļuves marķieri. Tīmekļa programmas iestatījumus varat iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektroniskie ziņojumi** \> **Tīmekļa programmas**.

Nākamajā tabulā ir aprakstīti lauki lapā **Tīmekļa programmas**.

| Lauks                        | Apraksts |
|------------------------------|-------------|
| Lietojumprogrammas nosaukums             | Ievadiet tīmekļa programmas nosaukumu. |
| Apraksts                  | Ievadiet tīmekļa programmas aprakstu. |
| Pamata vietrādis URL                     | Ievadiet tīmekļa programmas interneta pamatadresi. |
| Autorizācijas URL ceļš       | Norādiet ceļu, kas tiek izmantots, lai izveidotu URL autorizēšanai. |
| Marķiera URL ceļš               | Norādiet ceļu, kas tiek izmantots, lai izveidotu URL marķierim. |
| Novirzīšanas vietrādis URL                 | Ievadiet novirzīšanas URL. |
| Klienta ID                    | Ievadiet tīmekļa programmas klienta ID. |
| Klienta noslēpums                | Ievadiet tīmekļa programmas klienta noslēpumu. |
| Servera marķieris                 | Ievadiet tīmekļa programmas servera marķieri. |
| Autorizācijas formāta kartēšana | Atlasiet ER formātu, kas tiek izmantots, lai ģenerētu autorizācijas pieprasījumu. |
| Importēt marķieru modeļa kartēšanu   | Atlasiet ER importēšanas modeļa kartēšanu, ko izmanto, lai saglabātu piekļuves marķieri. |
| Piešķirtais tvērums                | Tvērums, kas piešķirts pieprasījumiem programmai. Šis lauks tiek automātiski atjaunināts. |
| Piekļuves marķiera termiņš beigsies pēc  | Atlikušais laiks pirms piekļuves marķiera termiņa beigām. Šis lauks tiek automātiski atjaunināts. | 
| Pieņemt                       | Norādiet tīmekļa pieprasījuma rekvizītu **Pieņemt**. Piemēram, ievadiet **application/vnd.hmrc.1.0+json**. |
| Satura veids                 | Norādiet satura tipu. Piemēram, ievadiet **application/json**. |

Turklāt lapas **Tīmekļa programmas** darbību rūtī ir pieejamas šādas pogas autorizācijas procesa atbalstam:

- **Iegūt autorizācijas kodu** — inicializē tīmekļa programmas autorizāciju. Šī funkcija izmanto ER formātu, kas ir norādīts laukā **Autorizācijas formāta kartēšana**, lai ģenerētu autorizācijas pieprasījumu.
- **Iegūt piekļuves marķieri** — inicializē piekļuves marķiera ieguves procesu.
- **Atsvaidzināt piekļuves marķieri** — atsvaidzina piekļuves marķieri. Šī funkcija izmanto ER formātu, kas ir norādīts laukā **Importēt marķiera modeļa kartēšanu**, lai importētu informāciju par saņemto piekļuves marķieri.

Kad tīmekļa programmas piekļuves marķieris ir saglabāts sistēmas datubāzē šifrētā formātā, to var izmantot tīmekļa pakalpojumu pieprasījumiem. Drošības nolūkos pieeja marķierim ir jāierobežo tikai drošības lomām, kurām ir atļauts risināt šos pieprasījumus. Ja kāds ārpus drošības grupas mēģina risināt pieprasījumu, tiek parādīts kļūdas paziņojums, ka viņiem nav atļauts sadarboties, izmantojot atlasīto tīmekļa programmu. Lai iestatītu drošības lomas, kurām ir pieeja piekļuves marķierim, izmantojiet kopsavilkuma cilni **Drošības lomas** lapā **Tīmekļa programmas**. Ja drošības lomas tīmekļa programmai nav definētas, tikai sistēmas administrators var sadarboties, izmantojot šo tīmekļa programmu.

Katrai darbībai ar izvēlēto tīmekļa programmu kopsavilkuma cilne **Darbību žurnāls** saglabā informāciju par lietotāju un datumu un laiku.

Dažiem tīmekļa pakalpojumiem var būt nepieciešams, lai pieprasījumos tiktu iekļauti dažādi virsraksti. Sistēmas administrators var iestatīt papildu virsrakstus un to vērtības kopsavilkuma cilnē **Papildu virsraksti** un pēc tam tos izmantot pieprasījuma ģenerēšanas laikā.

## <a name="web-service-settings"></a><a id="settings"></a>Tīmekļa pakalpojuma iestatījumi

Tīm. pakalp. iestatījumus izmanto, lai iestatītu tiešo datu pārs. uz tīm. pakalp. Tīmekļa pakalpojuma iestatījumus varat iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektroniskie ziņojumi** \> **Tīmekļa pakalpojuma iestatījumi**.

Nākamajā tabulā ir aprakstīti lauki lapā **Tīmekļa pakalpojumu iestatījumi**.

| Lauks                          | apraksts |
|--------------------------------|-------------|
| Tīmekļa pakalpojums                    | Ievadiet tīmekļa pak. nosaukumu. |
| apraksts                    | Ievadiet tīmekļa pakalpojuma aprakstu. |
| Interneta adrese               | <p>Ievadiet tīm. pakalpojuma interneta adresi. Ja tīmekļa programma tīmekļa pakalpojumam ir norādīta un ja tīmekļa pakalpojuma interneta adresei jābūt tādai pašai, kāda ir definēta attiecīgajai tīmekļa programmai, atlasiet vienumu **Kopēt pamata URL**. Tīmekļa lietojumprogrammas pamata URL pēc tam tiek kopēts šajā laukā.</p><p>**Brīdinājums:** Trešās puses pakalpojumiem vai citiem pakalpojumiem, ko šeit konfigurējat, nav nepieciešama sertifikācija, un tie var neatbilst Microsoft konfidencialitātes standartiem. Lai iegūtu plašāku informāciju par šī pakalpojuma nodrošināto saskaņotības līmeni, jums jāpārskata katra pakalpojuma konfidencialitātes dokumentācija un jādarbojas kopā ar katru pakalpojumu sniedzēju. Esat atbildīgs par to, lai šie pakalpojumi atbilstu jūsu drošības, konfidencialitātes un juridiskajiem standartiem. Jūs uzņematies pakalpojumu izmantošanas risku. Korporācija Microsoft nesniedz tiešas garantijas, garantijas vai nosacījumus. Stingri ieteicams izmantot tikai pakalpojumus, kas nodrošina drošus un autorizētus savienojumus, piemēram, HTTPS.</p> |
| Sertifikāts                    | Atlasiet Azure Key Vault sertifikātu, kas iestatīts iepriekš. |
| Tīmekļa programma                | Atlasiet tīmekļa programmu, kas iestatīta iepriekš. |
| Atbildes veids — XML        | Iestatiet šai opcijai **Jā**, ja atbildes tips ir XML. |
| Pieprasīšanas metode                 | Norādiet pieprasījuma metodi. HTTP definē pieprasījuma metožu kopu, kas norāda darbību, kura jāveic attiecīgajam resursam. Pieprasīšanas metode var būt **GET**, **POST** vai cita HTTP metode. |
| Pieprasījuma galvenes                | Norādiet piepras. galv. Pieprasījuma galvene ir HTTP galvene, ko var izmantot HTTP pieprasījumā. Tas nav saistīts ar ziņojuma saturu. |
| Pieņemt                         | Norādiet tīmekļa pieprasījuma rekvizītu Pieņemt. |
| Akceptēt kodēšanu                | Norādiet vienuma akceptēt kodēšanu vērtību. Kodēšanas akceptēšanas pieprasījuma HTTP galvene izziņo klientam saprotamu satura kodēšanu. Šī satura kodēšana parasti ir saspiešanas algoritms. |
| Satura veids                   | Norādiet satura tipu. Satura tipa elementa HTTP galvene norāda resursa plašsaziņas līdzekļu tipu. |
| Sekmīgas atbildes kods       | Norādiet HTTP statusa kodu, kas norāda, ka pieprasījums bija veiksmīgs. |
| Pieprasījuma galveņu formāta kartēšana | Atlasiet ER formātu, kas tiek izmantots, lai ģenerētu tīmekļa pieprasījuma galvenes. |

## <a name="message-processing-actions"></a><a id="actions"></a>Ziņojuma apstrādes darbības

Ziņojumu apstr. darbības izmanto, lai izveidotu darbības jūsu procesiem un iestatītu to parametrus. Ziņojumu apstrādes darbības var iestatīt, dodoties uz **Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu apstrādes darb**.

Tabulā ir aprakstīti lapā **Ziņojumu apstrādes darbības** esošie lauki.

### <a name="general-fasttab"></a>Cilne Vispārīgi

| Lauks                                     | apraksts |
|-------------------------------------------|-------------|
| Darbības veids                               | Atlasiet darbības tipu. Papildinformāciju par pieejamajām opcijām skatiet [tālāk šī raksta sadaļā](#action-types) Ziņojumu apstrādes darbību veidi. |
| Formāta kartēšana                            | Atlasiet ER formātu, kas jāizsauc attiecīgajai darbībai. Šis lauks ir pieejams tikai darbību tipiem **Elektr. pārsk. veidoš. eksports**, **Elektr. pārsk. veidoš. imports** un **Elektr. pārsk. veidoš. eksporta ziņojums**. |
| Formāta kartējums URL ceļam               | Atlasiet ER formātu, kas jāizsauc attiecīgajai darbībai. Šis formāts tiek izmantots, lai veidotu ceļu URL adresei, kas tiks pievienota interneta pamatadresei, kas norādīta atlasītajam tīmekļa serverim. Šis lauks ir pieejams tikai darbību tipam **Tīmekļa pakalpojums**. |
| Ziņojuma krājuma veids                         | Atlasiet ierakstu tipu, kuram ir jāizvērtē attiecīgā darbība. Šis lauks ir pieejams darbību tipiem **Ziņojuma vienuma izpildes līmenis**, **Elektroniskā pārskata veidošanas eksports**, **Elektroniskā pārskata veidošanas imports** un **Tīmekļa pakalpojumi**, un citiem tipiem. Ja šis lauks ir atstāts tukšs, tiek novērtēti visi ziņojumu vienumu tipi, kas definēti ziņojumu apstrādei. |
| Izpildāmā klase                          | Atlasiet esošu izpildāmās klases iestatījumu. Šis lauks ir pieejams tikai darbību tipiem **Ziņojuma vienuma izpildes līmenis** un **Ziņojuma vienuma izpildes līmenis**. |
| Ierakstu aizpildīšanas darbība                   | Atlasiet esošu aizpildītu ierakstu darbību. Šis lauks ir pieejams tikai darbību tipam **Aizpildīt ierakstus**. |
| Tīmekļa pakalpojums                               | Atlasiet esošu tīmekļa pakalpojumu. Šis lauks ir pieejams tikai darbību tipam **Tīmekļa pakalpojums**. |
| Sūtāmā faila nosaukums                         | Ievadiet nosaukumu pielikumam elektroniskajam ziņojumam, kas jānosūta šai darbībai. Ja vairākiem pielikumiem ir vienāds oriģinālais faila nosaukums, tiks nosūtīts jaunākais. Ja netiek atrasts neviens pielikums ar norādīto sākotnējā faila nosaukumu, pieprasījums tiks nosūtīts bez satura. Šis lauks ir pieejams tikai darbību tipam **Tīmekļa pakalpojums**. |
| Faila nosaukums                                 | Norādiet faila nosaukumu, kurš būs darbības rezultāts. Šis fails var būt atbilde no tīmekļa servera vai ģenerētais pārskats. Šis lauks ir pieejams tikai darbību tipiem **Tīmekļa pakalpojums** un **Elektroniskā pārskata veidošanas eksporta ziņojums**. |
| Pievienot failus avota dokumentiem          | Atzīmējiet šo izvēles rūtiņu, lai pievienotu ģenerētos failus ierakstiem EM krājumu atsauces galvenajā tabulā. Šis lauks ir pieejams tikai darbību tipiem **Elektronisko ziņojumu eksportēšana** un **Tīmekļa pakalpojums**. |
| Pievienot vienumiem failus no izvades arhīva | Atzīmējiet šo izvēles rūtiņu, lai izvilktu atsevišķus XML failus no izvades arhīva faila un pievienotu tos atbilstošajiem elektroniskā ziņojuma vienumiem. Šis lauks ir pieejams tikai darbību tipam **Elektroniskā pārskata veidošanas eksports**. |
| Ziņojuma krājumu skaits vienā eksportēšanas reizē        | Norādiet ierobežojumu ziņojuma elementu skaitam, kas jāietver vienā failā (ziņojums). Šis lauks ir pieejams tikai darbību tipam **Elektroniskā pārskata veidošanas eksports**. |
| Izmantot ER avotu                             | Atzīmējiet šo izvēles rūtiņu, lai ER avota parametrus izmantotu importam. Pretējā gadījumā tiek izmantots pielikums no elektroniskā ziņojuma. Šis lauks ir pieejams tikai darbību tipam **Elektroniskā pārskata veidošanas imports**. |
| Rādīt dialoglodziņu                               | Iestatiet šai opcijai vienumu **Jā**, ja dialoglodziņš ir jāparāda lietotājiem pirms pārskata izveidošanas. Šis lauks ir pieejams tikai darbību tipam **Elektroniskā pārskata veidošanas eksporta ziņojums**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Ziņojumu apstrādes darbību tipi

Laukā **Darbības tips** ir pieejamas tālāk norādītās opcijas.

- **Izveidot ziņojumu** — lietojiet šo darbības tipu, lai lietotāji manuāli izveidotu ziņojumus lapā **Elektroniskais ziņojums**. Šim darbības tipam nevar iestatīt sākotnējo statusu.
- **Aizpildīt ierakstus** — šis darbības tips jau ir jāiestata. Saistiet to ar ierakstu aizpildīšanas darbību, lai darbību varētu iekļaut apstrādē. Tiek pieņemts, ka šo darbības tipu lieto pirmajai darbībai ziņojumu apstrādē (ja iepriekš netika izveidots elektroniskais ziņojums), vai darbībai, kas pievieno ziņojumu vienumus ziņojumam, kas iepriekš izveidots ar darbības tipu **Izveidot ziņojumu**. Tādēļ šāda tipa darbībām var iestatīt tikai ziņojumu vienumu beigu statusu. Sākotnējo statusu var iestatīt tikai ziņojumiem.
- **Ziņojuma izpildes līmenis** — lietojiet šo darbības tipu, lai iestatītu izpildāmo klasi, kas jānovērtē ziņojuma līmenī.
- **Ziņojuma vienuma izpildes līmenis** — lietojiet šo darbības tipu, lai iestatītu izpildāmo klasi, kas jānovērtē ziņojuma vienuma līmenī.
- **Elektr. pārskata veidošanas eksports** — lietojiet šo darbības tipu darbībām, kuras ģenerē pārskatu, kas balstās uz eksportēšanas ER konfigurāciju ziņoj. vienuma līmenī.
- **Elektronisko pārskatu veidošanas eksporta ziņojums** — lietojiet šo darbības tipu darbībām, kuras ģenerē pārskatu, kas balstās uz eksportēšanas ER konfigurāciju ziņojuma līmenī (piemēram, ja ziņojumam nav neviena ziņojuma vienuma).
- **Elektroniskā pārskata veidošanas imports** — lietojiet šo darbības tipu darbībām, kuras ģenerē pārskatu, kas balstās uz importēšanas ER konfigurāciju.
- **Ziņojuma līmeņa lietotāja apstrāde** — lietojiet šo darbības tipu darbībām, kas paredz manuālas lietotāju darbības ziņojumu līmenī. Piemēram, lietotājs var atjaunināt ziņojumu statusu.
- **Lietotāja apstrāde** — lietojiet šo darbības tipu darbībām, kas paredz manuālas lietotāju darbības ziņojumu vienumu līmenī. Piemēram, lietotājs var atjaunināt ziņojumu vienumu statusu.
- **Tīmekļa pakalpojums** — lietojiet šo darbības tipu darbībām, kas ģenerēto pārskatu nosūta uz tīmekļa pakalpojumu. Šo darbības tipu neizmanto Itālijas pirkšanas un pārdošanas rēķinu paziņojumu pārskatiem. Šim darbību tipam lapā **Ziņojumu apstrādes darbības** ietilpst kopsavilkuma cilne **Detalizēta papildinformācija**, kurā varat norādīt apstiprinājuma tekstu. Šis apstiprinājuma teksts tiek parādīts lietotājiem pirms pieprasījumi tiek adresēti izvēlētajam tīmekļa pakalpojumam.
- **Pieprasīt verifikāciju** — lietojiet šo darbības tipu, lai pieprasītu verifikāciju no servera.

### <a name="initial-statuses-fasttab"></a>Cilne Sākotnējie statusi

> [!NOTE]
> Kopsavilkuma cilne **Sākotnējie statusi** nav pieejama darbībām, kuru sākotnējais darbības tips ir **Izveidot ziņojumu**.

| Lauks               | Apraksts |
|---------------------|-------------|
| Ziņojuma krājuma statuss | Atlasiet ziņojuma vienuma statusu, kuram ir jānovērtē atlasītā ziņojumu apstrādes darbība. |
| apraksts         | Atlasītā ziņojuma vienuma statusa apraksts. |

### <a name="result-statuses-fasttab"></a>Cilne Beigu statusi

| Lauks               | apraksts |
|---------------------|-------------|
| Ziņojuma statuss      | Atlasiet ziņojuma statusu, kuram ir jānovērtē atlasītā ziņojumu apstrādes darbība. Šis lauks ir pieejams tikai ziņojumu apstrādes darbībām, kas tiek novērtētas ziņojuma līmenī. Piemēram, tas ir pieejams darbībām, kuru tips ir **Elektroniskā pārskata veidošanas eksports** un **Elektroniskā pārskata veidošanas imports**, bet tas nav pieejams darbībām, kuru tips ir **Lietotāja apstrāde** un **Ziņojuma vienuma izpildes līmenis**. |
| apraksts         | Atlasītā ziņojuma statusa apraksts. |
| Atbildes veids       | Atlasītā ziņojuma statusa atbildes tips. |
| Ziņojuma krājuma statuss | Atlasiet beigu statusus, kuriem jābūt pieejamiem pēc atlasītās ziņojumu apstrādes darbības novērtēšanas. Šis lauks ir pieejams tikai ziņojumu apstrādes darbībām, kas tiek novērtētas ziņojuma vienuma līmenī. Piemēram, tas ir pieejams darbību tipiem **Lietotāja apstrāde** un **Ziņojuma krājuma izpildes līmenis**. Ziņojumu apstrādes darbībām, kuras tiek novērtētas ziņojuma līmenī, šis lauks rāda ziņojuma vienuma statusu, kas tika iestatīts atlasītajam ziņojuma statusam. |

Tabulā ir parādīti beigu statusi, kas ir jāiestata dažādiem darbību tipiem un atbilžu tipiem.

| Elektroniskā ziņojuma darbības tips/atbildes tips | Izpildīts veiksmīgi | Biznesa kļūda | Tehniska kļūda | Lietotāja definēts | Atcelt |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Izveidot ziņojumu                               | X                     |                |                 |              |        |
| Elektroniskā pārskata veidošanas eksports                  | X                     |                |                 |              |        |
| Elektroniskā pārskata veidošanas imports                  |                       |                |                 |              |        |
| Tīmekļa pakalpojums                                  | X                     |                | X               |              |        |
| Lietotāja apstrāde                              |                       |                |                 |              |        |
| Ziņojuma izpildes līmenis                      |                       |                |                 |              |        |
| Aizpildīt ierakstus                             |                       |                |                 |              |        |
| Ziņojuma krājuma izpildes līmenis                 |                       |                |                 |              |        |
| Pieprasīt verifikāciju                         | X                     | X              | X               |              |        |
| Elektronisko pārskatu veidošanas eksporta ziņojums          | X                     |                |                 |              |        |
| Ziņojuma līmeņa lietotāja apstrāde                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Elektroniska ziņojuma apstrāde

Elektroniska ziņojuma apstrāde ir EM funkcionalitātes pamatkoncepts. Tā apkopo darbības, kuras jānovērtē elektroniskajam ziņojumam. Darbības var saistīt, izmantojot sākotnējo statusu un beigu statusu. Vai arī darbības, kuru tips ir **Lietotāja apstrāde**, var sākt neatkarīgi. Lai iestatītu elektronisko ziņojumu apstrādi, dodieties uz **Nodokļi** \> **Iestatījums** \> **Elektroniskie ziņojumi** \> **Elektronisko ziņojumu apstrāde**.

Kopsav. cilne **Darbība** ļauj pievienot iepr. definētas darb. apstrādei. Var norādīt, vai darbība ir jāpalaiž atsevišķi vai arī to var sākt apstrāde. Lai norādītu, ka darbību apstrādē var inicializēt tikai lietotājs, iestatiet attiecīgajai darbībai laukā **Izpildīt atsevišķi** vienumu **Jā**. Ja darbības ir jāizpilda apstrādē ziņojumiem vai ziņojumu vienumiem, kuru statuss ir definēts kā sākotnējais statuss šai darbībai, iestatiet laukā **Izpildīt atsevišķi** vienumu **Nē**. Darbības, kuru tips ir **Lietotāja darbība**, vienmēr ir jāpalaiž atsevišķi.

Dažreiz ir nepieciešams apkopot virknē vairākas darbības, pat ja pirmajai darbībai ir iestatīta atsevišķa palaišana. Piemēram, lietotājam inicializējiet pārskata ģenerēšanu. Tomēr uzreiz pēc pārskata ģenerēšanas tas jānosūta uz tīmekļa pakalpojumu, un atbildes no tīmekļa pakalpojuma ir jāatspoguļo sistēmā. Šādā gadījumā varat izveidot nedalāmu virkni darbībām, kuras vienmēr jāpalaiž kopā. Kopsavilkuma cilnē **Darbība** virs režģa atlasiet **Nedalāmas virknes** un izveidojiet virkni. Pēc tam visām darbībām, kas jāizpilda kopā vienā secībā, atlasiet virkni laukā **Nedalāma virkne**. Šim piemēram laukā **Izpildīt atsevišķi** var iestatīt vienumu **Jā** pirmajai darbībai virknē, un vienumu **Nē** pārējām darbībām.

Darbību veidi **Elektronisko pārskatu eksports** un **Elektronisko pārskatu eksporta ziņojums** darbojas ER formātā, kam ir ievades parametri. Ja elektroniskā ziņojumu apstrādē ir ietvertas kāda no šo tipu darbībām, pirms pārskata izveides jānorāda ievades parametru vērtības. Šādā veidā sistēma var izmantot partiju tam, lai izveidotu pārskatu. Var atlasīt **Parametri** virs režģa, lai iestatītu parametrus atlasītajam darbības tipam (**Elektronisko pārskatu eksports** vai **Elektronisko pārskatu eksporta ziņojums**). Atzīmējiet izvēles rūtiņu **Izmantot parametrus** darbībai, kas ir jāpalaiž ar norādītajiem parametriem partijā.

Izmantojiet kopsav. cilni **Ziņ. vienuma papildu lauki**, lai pievienotu iepriekš defin. papildu laukus, kas saistīti ar ziņ. vienumiem. Ir jāpievieno papildu lauki katram ziņojuma vienuma tipam, ar kuru lauki ir saistīti. Varat norādīt noklusējuma vērtību, kas apstrādes laikā tiks piešķirta papildu laukam.

Izmantojiet kopsav. cilni **Ziņoj. papildu lauki**, lai pievienotu iepriekš defin. papildu laukus, kas saistīti ar ziņojumiem. Varat norādīt noklusējuma vērtību, kas apstrādes laikā tiks piešķirta papildu laukam.

Izmantojiet kopsav. cilni **Drošības lomas**, lai iestatītu drošības lomas, kas ir iepriekš definētas sistēmā noteiktai apstrādei. Lietot., kam ir noteikta loma, redz tikai apstrādi, kas definēta attiecīgajai lomai.

Izmantojiet kopsav. cilni **Pakete**, lai iestatītu apstrādi darbam pakešveida režīmā. Ieteicams iestatīt pakešveida apstrādi tieši lapā **Elektroniskie ziņojumi** vai **Elektronisko ziņojumu krājumi**, kad atlasāt **Palaist apstrādi** darbību rūtī, lai sāktu apstrādi.
