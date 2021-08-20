---
title: Ieturējumu pārvaldība, izmantojot ieturējumu rīku
description: Šajā tēmā aprakstīts, kā izmantot ieturējumu rīku, lai apstrādātu debitoru maksājumus, kuros ietverti ieturējumi.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 04d7c1de85978f7915246fd835a0866cefb6de310bba240ebcadc57089e10521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735115"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Ieturējumu pārvaldība, izmantojot ieturējumu rīku

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Šajā tēmā aprakstīts, kā izmantot ieturējumu rīku, lai apstrādātu debitoru maksājumus, kuros ietverti ieturējumi.

Debitors, kuram pienākas atlaide, var izlemt negaidīt atlaides izmaksu. Tā vietā klients var nosūtīt maksājumu, kas ietver ieturējumu par atlaides summu. Lai apstrādātu šādu transakcijas veidu, varat izmantot ieturējumu rīku, kurā saskaņojat ieturējumus, lai atvērtu kredīta transakciju, sadalītu ieturējumus, noraidītu ieturējumus un norakstītu ieturējumus.

> [!NOTE]
> Ieturējumu rīks ir bijis daļa no pārdošanas un mārketinga funkcionalitātes programmā Microsoft Dynamics 365 Supply Chain Management ilgu laiku. Tomēr tagad tas ir uzlabots, lai tas darbojas arī ar jaunāku moduli **Atlaižu pārvaldība**. Šajā tēmā ir aprakstīts, kā izmantot gan ieturējumu rīka vecākos līdzekļus, gan ieturējumu rīka atlaižu pārvaldības līdzekļus. Tomēr, ja neesat [ieslēdzis moduli **Atlaižu pārvaldība** jūsu sistēmai](rebate-management-enable.md), daļa no šeit aprakstītās funkcionalitātes nebūs jums pieejama.

## <a name="prerequisites"></a>Priekšnosacījumi

### <a name="set-up-the-old-deduction-management-system"></a>Iestatīt veco ieturējumu pārvaldības sistēmu

Varat izmantot ieturējumu rīku kopā ar veco Supply Chain Management ieturējumu pārvaldības iespējām, pat ja neizmantojat moduli **Atlaižu pārvaldība**. Tomēr vispirms ir jāsagatavo jūsu sistēma, kā aprakstīts šajā sadaļā.

Pirms ieturējumu rīka lietošanas jāveic iestatījumi, kas aprakstīti sadaļā [Iestatīt ieturējumu pārvaldību](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Debitoram jābūt iestatītam arī kādam no atlaižu līgumiem: debitora atlaižu līgumam, kā aprakstīts sadaļā [Klientu atlaižu uzstādīšana un uzturēšana](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates), vai tirdzniecības atlaižu līgumam.

Ja jūs izmantojat ieturējumus debitora atlaidei, jums ir jāveic šie uzdevumi:

- [Iestatīt debitora atlaides](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Lai izmantotu ieturējuma rīku, atlaide ir jāapstiprina un jāapstrādā.

Ja jūs izmantojat ieturējumus tirdzniecības pabalsta atlaidei, jums ir jāveic šie uzdevumi:

- Atmaksas atlaižu iestatīšana.
- Atmaksas atlaižu piemērošana.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Konfigurējiet debitoru parādus un ieturējumus

Sistēma reģistrē visus ieturējumu notikumus prasību žurnālā. Tādēļ jūsu sistēmai ir jāietver žurnāls, ko var izmantot šim nolūkam. Ja jums vēl nav prasību žurnāla, iestatiet to tūlīt. Šis žurnāls ir nepieciešams, lai izveidotu ieturējumus tieši ieturējumu rīkā, klientu izlīgumā vai debitoru lapā.

Lai iestatītu jaunu ieturējumu pieprasījumu žurnālu, veiciet šīs darbības.

1. Dodieties uz **Virsgrāmata \> Žurnāla iestatīšana \> Žurnālu nosaukumi**.
1. Atlasiet **Jauns** un jaunajam žurnāla nosaukumam iestatiet šādus laukus:

    - **Nosaukums** - Ievadiet unikālu prasību žurnāla nosaukumu.
    - **Apraksts** — ievadiet jaunā žurnāla aprakstu.
    - **Žurnāla** - atlasiet *Ikdienas*.
    - **Dokumentu sērija** – piešķiriet esošu numuru sēriju. Vai arī izveidojiet jaunu numuru sēriju, kam ir uzņēmuma sfēra, un piešķiriet to jaunajam žurnāla nosaukumam.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
1. Cilnē **Ieturējumi** kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Prasību žurnāla nosaukums** uz tā žurnāla nosaukumu, kuru tikko izveidojāt.
1. Kopsavilkuma cilnē **Atgriešanas pasūtījums** iestatiet tālāk minētos laukus:

    - **Izveidot atgriešanas pasūtījumu** — iestatiet šo opciju, lai norādītu, ko sistēmai darīt, kad uz daudzumu balstīta prasība tiek apstiprināta:

        - *Jā* - izveidojiet atgriešanas pasūtījumu.
        - *Nē* – izveidojiet negatīvu pārdošanas pasūtījumu.

    - **Izveide bez pievienotā rēķina** - atlasiet vērtību, lai norādītu, kas sistēmai jādara, kad uz daudzumu pamatota prasība tiek apstiprināta, bet rēķins nav pievienots:

        - *Pieņiemt* - atgriešanas pasūtījuma izveide.
        - *Brīdinājums* – izveidot atgriešanas pasūtījumu, bet parādīt šādu brīdinājuma ziņojumu: "Prasība nav pievienota rēķinam."
        - *Kļūda* – neizveidot atgriešanas pasūtījumu un parādīt šādu kļūdas ziņojumu: "Prasība nav pievienota rēķinam. Labojumi ir atcelti."

    - **Izveidot atgriešanas pasūtījumu pirms ieturējumu apstiprināšanas** - iestatiet šo opciju uz *Jā*, ja atgriešanas pasūtījumus var izveidot pirms prasības apstiprināšanas. Šis iestatījums attiecas tikai uz prasībām, kas pamatotas uz daudzumu, kur opcija **Izveidot atgriešanas pasūtījumu** ir iestatīta uz *Jā*.

### <a name="configure-general-ledger-parameters"></a>Virsgrāmatas parametru konfigurēšana

Kad sistēma izveido prasību žurnālu jauniem ieturējumiem, tiek arī izveidoti divi jauni debitora darījumi: viens, lai nobīdītu prasības summu attiecībā pret oriģinālo rēķinu, un viens, lai reģistrētu debitora parādu prasības summai (jo prasība vēl nav apstiprināta). Tādēļ jāiestata sistēma tā, lai vienam dokumentam varētu būt vairākas debitora rindas.

Lai vienam dokumentam iespējotu vairākas debitora rindas, veiciet šīs darbības.

1. Dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmatas parametri**.
1. Cilnē **Virsgrāmata** kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Atļaut vairākas darbības vienā dokumentā** uz *Jā*.
1. Ja saņemat brīdinājuma ziņojumu, atlasiet **Aizvērt**, lai pieņemtu izmaiņas.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Izveidot ieturējuma iemeslus

Sistēmā ir nepieciešams, lai lietotāji norādītu iemeslu katram ieturējumam, ko tie ievada tieši ieturējumu līguma, debitora izlīgumā vai debitora lapā. Iemesls nosaka to, kā tiek apstrādāti ieturējumi, ja tie ir apstiprināti.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu iemesli**.
1. Vēlreiz atlasiet **Jauns**, lai režģim pievienotu rindu, un pēc tam iestatiet tai šādus laukus:

    - **Prasības iemesls** - Ievadiet unikālu iemesla nosaukumu.
    - **Apraksts** — ievadiet iemesla aprakstu, lai sniegtu papildinformāciju par tā lietošanu.
    - **Prasības pamats** – atlasiet prasības pamatu prasības iemeslam:

        - *Uz cenas balstīts* – apstiprināšanas laikā izveidojiet brīva teksta kredītu.
        - *Uz daudzumu balstīts* – izveidojiet negatīvu pārdošanas pasūtījumu vai atgriešanas pasūtījumu pēc apstiprināšanas.

    - **Atgriešanas iemesla kods** – izvēlieties atgriešanas iemesla kodu, lai piemērotu, kā vērtību **Atgriešanas iemesla kods** atgriešanas pasūtījumam.
    - **Veids** – Atlasiet ieturējuma veidu. Vērtība **Ieturējumu nobīde** atlasītajam veidam tiks izmantota, lai iestatītu lauku **Ieturējumu nobīde**, kad tiek izveidota ieturējums vai prasība. Ieturējumu tipi ir definēti lapā **Ieturējumu veidi** (**Pārdošana un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu veidi**).
    - **Prasības grāmatošanas konts** — šis lauks ir pieejams tikai tad, ja lauks **Prasības pamats** ir iestatīts *Uz cenu balstīts*. Kad ir apstiprināta prasība, kas pamatota uz cenu, sistēma piešķir virsgrāmatu kontu, kuru šeit atlasāt kā vērtību **Galvenais konts** brīvā teksta kredīta notai.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Iestatīt periodisko uzdevumu nokārtot apstiprinātos ieturējumus

Ieturējumiem, kas tiek izveidoti, izmantojot komandu **Jauns ieturējums** ieturējuma rīkā, debitora izlīgumā vai debitora lapā, varat iestatīt periodisko uzdevumu *Nokārtot apstiprinātos ieturējumus*, lai automātiski saskaņotu ieturējumus un kredītus, kuriem ir atbilstošas **Ieturējumu ID** vērtības un summas.

Lai ieplānotu šo uzdevumu, dodieties uz **Pārdošanas mārketings \> Periodiskie uzdevumi \> Nokārtot apstiprinātos ieturējumus** un iestatiet opcijas, filtrus un grafiku tāpat kā citiem periodisko uzdevumu tipiem.

> [!NOTE]
> Ja opcija **Automātiskais izlīgums** ir iestatīta uz *Jā* cilnē **Izlīgums** lapā **Debitoru parādu parametri** (**Debitoru parādi \> Iestatīšana \> Debitoru parametri**), periodiskais uzdevums *Nosegt apstiprinātos ieturējumus* neko nedarīs, jo kredīts tiks segts automātiski.

## <a name="create-a-deduction"></a>Ieturējuma izveide

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Izveidot ieturējumu žurnāla ierakstu, izmantojot debitoru maksājumu žurnālu

Lai izveidotu ieturējumu žurnāla ierakstu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Debitori \> Maksājumi \> Debitora maksājumu žurnāls**.
1. Atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunas rindas laukā **Nosaukums** atlasiet žurnāla nosaukumu.
1. Darbību rūtī atlasiet **Rindiņas**.
1. Ievadiet datumu, uzņēmuma kontu un debitora konta numuru.
1. Laukā **Rēķins** atlasiet rēķinu, ar kuru saistīts ieturējums.
1. Laukā **Kredīts** ievadiet debitora samaksāto summu.
1. Atlasiet **Labi**, lai apstiprinātu, ka summa ir mazāka par iezīmētās transakcijas kopsummu.
1. Atlasiet korespondējošā konta veidu un korespondējošo kontu.
1. Rīkjoslā virs režģa atlasiet **Ieturējumi**.
1. Lapā **Ieturējumi**, darbības rūtī atlasiet **Jauns**, lai režģim pievienotu rindu. Lauks **Ieturējumu ID** jaunajai rindai tiek iestatīts automātiski.
1. Laukā **Tips** atlasiet datu ieturējumu tipu.
1. Laukā **Summa** ievadiet summu, kas redzama laukā **Bilance** zem ieturējumu saraksta. Šī summa attiecas uz summu, ko debitors atskaitījis no maksājuma.
1. Aizveriet lapu **Ieturējums**. Jūs esat atgriezies lapā **Debitoru maksājumi**, kurā tagad ieturējumiem tiek parādīta jauna rinda.
1. Darbību rūtī atlasiet **Pārbaudīt \> Pārbaudīt**. Būtu jāsaņem šāds ziņojums: “Žurnāls ir kārtībā.”
1. Darbību rūtī atlasiet **Grāmatot**.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Ieturējumu izveide, izmantojot ieturējumu rīku

Lai ieturējumu rīkā izveidotu ieturējumu, veiciet tālāk norādītās darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Darbību rūtī atlasiet **Uzturēt \> Jauns ieturējums**.

    Dialoglodziņā **Jauns ieturējums** lauks **Ieturējuma ID** ir iestatīts, pamatojoties uz **Ieturējumu ID** numuru sēriju, kas ir definēta lapā **Tirdzniecības atlaižu pārvaldības parametri** (**Pārdošana un mārketings \> Iestatīšana \> Tirdzniecības atlaides \> Tirdzniecības atlaižu pārvaldības parametri**).

1. Iestatiet tālāk norādītos laukus.

    - **Debitora konts** - atlasiet debitora kontu, uz kuru attiecas ieturējums.
    - **Ārējās prasības numurs** – ievadiet debitora prasības atsauci.
    - **Prasības summa** – ievadiet nodokļu ietverošas prasības summu. Vērtībai jābūt pozitīvai.
    - **Valūta** - izvēlieties ieturējumu valūtu. Noklusētā vērtība ir valūta, kas iestatīta atlasītajam debitora kontam.
    - **Prasības pamats** – atlasiet prasības pamatu. Prasības pamats nosaka kredīta darījuma veidu, kas tiek izveidots pēc tam, kad ieturējums vai prasība ir apstiprināta.

        - *Uz cenu balstīts* – tiks izveidots melnraksta brīva teksta rēķins.
        - *Uz daudzumu balstīts* – tiks izveidots negatīvs pārdošanas pasūtījums vai atgriešanas pasūtījums.

    - **Prasības datums** – izvēlieties prasības datumu. Noklusējuma vērtība ir pašreizējais datums.
    - **Prasības iemesls** — atlasiet iemesla kodu, kas attiecas uz pašreizējiem ieturējumiem. Jūsu atlasītais prasības pamats ietekmē opcijas, kuras ir piemērojamas. Papildinformāciju par to, kā šeit izveidot un konfigurēt prasības iemeslus, kas ir pieejami atlasei, skatiet iepriekš šajā tēmā sadaļā [Izveidot ieturējumu iemeslus](#deduction-reasons).
    - **Piezīmes** – pievienojiet jebkādas piezīmes, kuras ir spēkā; Kad prasība ir apstiprināta, apstiprinātājs varēs rediģēt vai pievienot prasības piezīmes.
    - **Izveidot prasību žurnālu** — iestatiet šo opciju, lai norādītu, vai prasības žurnāls ir jāizveido, kad tiek izveidota prasība vai ieturējums:

        - *Jā* – Sistēma izveidos un publicēs vispārēju žurnālu, izmantojot prasību žurnālu, kas ir iestatīts lapā **Debitoru parādu parametri**. (Plašāku informāciju skatiet sadaļu [Konfigurēt debitoru parādus un ieturējumus](#accounts-receivable-deductions) iepriekš šajā tēmā.) Kad prasībai ir pievienots rēķins, prasību žurnāls tiek izmantots, lai samazinātu piemērojamā rēķina bilanci. Ja prasība vēlāk tiek noraidīta, prasību žurnāls un izlīgumi (ja pievienots rēķins) tiks anulēti.
        - *Nē* – pašlaik nav izveidots neviens prasību žurnāls. Tas tiks izveidots pēc prasības apstiprināšanas. Rēķinu joprojām var pievienot jaunajai prasībai, pat ja prasību žurnāls nav izveidots. Tomēr izlīgumu nevar veikt bez prasību žurnāla.

1. Atlasiet **Labi**.

    Izveidots jauns ieturējums. Ja jūs iestatāt opciju **Izveidot prasību žurnālu** uz *Jā*, tiek grāmatotas šādas darbības:

    - **Divas jaunas debitora darbības** – viena darbība korespondē prasības summu pret oriģinālo rēķinu. Ar citu darbību tiek reģistrēts debitora parāds prasības summai, jo prasība vēl nav apstiprināta. Oriģinālā rēķina darbība un korespondējošās prasības darbība tiks automātiski atzīmēta izlīgumam, ja pievienojat rēķinu, darbību rūtī atlasot **Uzturēt \> Pievienot rēķinu**.
    - **Divas korespondējošās darbības** – šīs darbības tiek grāmatotas **Ieturējumu korespondējošā** virsgrāmatas kontā.
    - **Prasību žurnāls** — lai skatītu prasību žurnālu katram ieturējumum, kas tiek rādīti ieturējumu rīkā, atlasiet cilni **Atsauces**. Prasību žurnāls ir parādīts laukā **Žurnāla partijas numurs**. Jūs varat arī skatīt prasību žurnālu cilnē **Ieturējumu notikumi**. Tur, tai būs **Atjaunināšanas tipa** vērtība *Saskaņot*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Ieturējumu izveide no debitora izlīguma

Ieturējumu izveides process no debitoru izlīguma ir līdzīgs ieturējumu izveides procesam, izmantojot ieturējumu risinājumu. Tomēr debitora un rēķina valūta tiek iestatīta automātiski, un rēķins ir pievienots. Darbības rūtī nav jāatlasa **Uzturēt \> Pievienot rēķinu**, ja veidojat prasību vai ieturējumus, izmantojot debitoru izlīguma lapu.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Atlasiet debitoru, kuram veidot ieturējumu.
1. Darbību rūtī, cilnē **Savākt**, grupā **Norēķināties** atlasiet **Norēķināties par darījumiem**.
1. Dialoglodziņā **Darbību iestatīšana** cilnē **Pārskats** atlasiet rēķinu, ar kuru izveidot ieturējumus.
1. Rīkjoslā atlasiet **Ieturējumus \> Jauns ieturējums**.

    Dialoglodziņā **Jauns ieturējums** lauks **Ieturējuma ID** ir iestatīts, pamatojoties uz **Ieturējumu ID** numuru sēriju, kas ir definēta lapā **Tirdzniecības atlaižu pārvaldības parametri** (**Pārdošana un mārketings \> Iestatīšana \> Tirdzniecības atlaides \> Tirdzniecības atlaižu pārvaldības parametri**). Lauks **Debitora konts** ir iestatīts uz debitora kontu, uz kuru attiecas ieturējums.

1. Iestatiet tālāk norādītos laukus.

    - **Ārējās prasības numurs** – ievadiet debitora prasības atsauci.
    - **Prasības summa** – ievadiet nodokļu ietverošas prasības summu. Vērtībai jābūt pozitīvai.
    - **Valūta** - izvēlieties ieturējumu valūtu. Noklusētā vērtība ir valūta, kas iestatīta atlasītajam debitora kontam.
    - **Prasības pamats** – atlasiet prasības pamatu. Prasības pamats nosaka kredīta darījuma veidu, kas tiek izveidots pēc tam, kad ieturējums vai prasība ir apstiprināta.

        - *Uz cenu balstīts* – tiks izveidots melnraksta brīva teksta rēķins.
        - *Uz daudzumu balstīts* – tiks izveidots negatīvs pārdošanas pasūtījums vai atgriešanas pasūtījums.

    - **Prasības datums** – izvēlieties prasības datumu. Noklusējuma vērtība ir pašreizējais datums.
    - **Prasības iemesls** — atlasiet iemesla kodu, kas attiecas uz pašreizējiem ieturējumiem. Jūsu atlasītais prasības pamats ietekmē opcijas, kuras ir piemērojamas. Papildinformāciju par to, kā šeit izveidot un konfigurēt prasības iemeslus, kas ir pieejami atlasei, skatiet iepriekš šajā tēmā sadaļā [Izveidot ieturējumu iemeslus](#deduction-reasons).
    - **Piezīmes** – pievienojiet jebkādas piezīmes, kuras ir spēkā; Kad prasība ir apstiprināta, apstiprinātājs varēs rediģēt vai pievienot prasības piezīmes.
    - **Izveidot prasību žurnālu** — iestatiet šo opciju, lai norādītu, vai prasības žurnāls ir jāizveido, kad tiek izveidota prasība vai ieturējums:

        - *Jā* – Sistēma izveidos un publicēs vispārēju žurnālu, izmantojot prasību žurnālu, kas ir iestatīts lapā **Debitoru parādu parametri**. (Plašāku informāciju skatiet sadaļu [Konfigurēt debitoru parādus un ieturējumus](#accounts-receivable-deductions) iepriekš šajā tēmā.) Kad prasībai ir pievienots rēķins, prasību žurnāls tiek izmantots, lai samazinātu piemērojamā rēķina bilanci. Ja prasība vēlāk tiek noraidīta, prasību žurnāls un izlīgumi (ja pievienots rēķins) tiks anulēti.
        - *Nē* – pašlaik nav izveidots neviens prasību žurnāls. Tas tiks izveidots pēc prasības apstiprināšanas. Rēķinu joprojām var pievienot jaunajai prasībai, pat ja prasību žurnāls nav izveidots. Tomēr izlīgumu nevar veikt bez prasību žurnāla.

1. Atlasiet **Labi**.

    Izveidots jauns ieturējums. Ja jūs iestatāt opciju **Izveidot prasību žurnālu** uz *Jā*, tiek grāmatotas šādas darbības:

    - **Divas jaunas debitora darbības** – viena darbība korespondē prasības summu pret oriģinālo rēķinu. Ar citu darbību tiek reģistrēts debitora parāds prasības summai, jo prasība vēl nav apstiprināta. Oriģinālā rēķina darbība un korespondējošās prasības darbība tiks automātiski atzīmēta izlīgumam, ja pievienojat rēķinu, darbību rūtī atlasot **Uzturēt \> Pievienot rēķinu**.
    - **Divas korespondējošās darbības** – šīs darbības tiek grāmatotas **Ieturējumu korespondējošā** virsgrāmatas kontā.
    - **Prasību žurnāls** — lai skatītu prasību žurnālu katram ieturējumum, kas tiek rādīti ieturējumu rīkā, atlasiet cilni **Atsauces**. Prasību žurnāls ir parādīts laukā **Žurnāla partijas numurs**. Jūs varat arī skatīt prasību žurnālu cilnē **Ieturējumu notikumi**. Tur, tai būs **Atjaunināšanas tipa** vērtība *Saskaņot*.

    Jūs esat atgriezies lapā **Norēķināties par darījumiem**, kurā atlasītais rēķins tagad ir parādīts kā iezīmēts. Poga **Grāmatot** ir pieejama tikai tad, ja opcija **Izveidot prasību žurnālu** ir iestatīta uz *Jā*. Ja pieejams, atlasiet **Grāmatot**, lai samazinātu rēķina bilanci par **Prasības summas** vērtību.

### <a name="create-a-deduction-from-a-customer-page"></a>Ieturējumu izveide no debitora lapas

Ieturējumu izveides process no debitoru lapas ir līdzīgs ieturējumu izveides procesam, izmantojot ieturējumu risinājumu. Tomēr debitors tiek iestatīts automātiski.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Atlasiet debitoru, kuram veidot ieturējumu.
1. Darbību rūts cilnes **Savākt** grupā **Ieturējumi** atlasiet **Izveidot ieturējumus**.

    Dialoglodziņā **Jauns ieturējums** lauks **Ieturējuma ID** ir iestatīts, pamatojoties uz **Ieturējumu ID** numuru sēriju, kas ir definēta lapā **Tirdzniecības atlaižu pārvaldības parametri** (**Pārdošana un mārketings \> Iestatīšana \> Tirdzniecības atlaides \> Tirdzniecības atlaižu pārvaldības parametri**). Lauks **Debitora konts** ir iestatīts uz debitora kontu, uz kuru attiecas ieturējums.

1. Iestatiet tālāk norādītos laukus.

    - **Ārējās prasības numurs** – ievadiet debitora prasības atsauci.
    - **Prasības summa** – ievadiet nodokļu ietverošas prasības summu. Vērtībai jābūt pozitīvai.
    - **Valūta** - izvēlieties ieturējumu valūtu. Noklusētā vērtība ir valūta, kas iestatīta atlasītajam debitora kontam.
    - **Prasības pamats** – atlasiet prasības pamatu. Prasības pamats nosaka kredīta darījuma veidu, kas tiek izveidots pēc tam, kad ieturējums vai prasība ir apstiprināta.

        - *Uz cenu balstīts* – tiks izveidots melnraksta brīva teksta rēķins.
        - *Uz daudzumu balstīts* – tiks izveidots negatīvs pārdošanas pasūtījums vai atgriešanas pasūtījums.

    - **Prasības datums** – izvēlieties prasības datumu. Noklusējuma vērtība ir pašreizējais datums.
    - **Prasības iemesls** — atlasiet iemesla kodu, kas attiecas uz pašreizējiem ieturējumiem. Jūsu atlasītais prasības pamats ietekmē opcijas, kuras ir piemērojamas. Papildinformāciju par to, kā šeit izveidot un konfigurēt prasības iemeslus, kas ir pieejami atlasei, skatiet iepriekš šajā tēmā sadaļā [Izveidot ieturējumu iemeslus](#deduction-reasons).
    - **Piezīmes** – pievienojiet jebkādas piezīmes, kuras ir spēkā; Kad prasība ir apstiprināta, apstiprinātājs varēs rediģēt vai pievienot prasības piezīmes.
    - **Izveidot prasību žurnālu** — iestatiet šo opciju, lai norādītu, vai prasības žurnāls ir jāizveido, kad tiek izveidota prasība vai ieturējums:

        - *Jā* – Sistēma izveidos un publicēs vispārēju žurnālu, izmantojot prasību žurnālu, kas ir iestatīts lapā **Debitoru parādu parametri**. (Plašāku informāciju skatiet sadaļu [Konfigurēt debitoru parādus un ieturējumus](#accounts-receivable-deductions) iepriekš šajā tēmā.) Kad prasībai ir pievienots rēķins, prasību žurnāls tiek izmantots, lai samazinātu piemērojamā rēķina bilanci. Ja prasība vēlāk tiek noraidīta, prasību žurnāls un izlīgumi (ja pievienots rēķins) tiks anulēti.
        - *Nē* – pašlaik nav izveidots neviens prasību žurnāls. Tas tiks izveidots pēc prasības apstiprināšanas. Rēķinu joprojām var pievienot jaunajai prasībai, pat ja prasību žurnāls nav izveidots. Tomēr izlīgumu nevar veikt bez prasību žurnāla.

1. Atlasiet **Labi**.

    Izveidots jauns ieturējums. Ja jūs iestatāt opciju **Izveidot prasību žurnālu** uz *Jā*, tiek grāmatotas šādas darbības:

    - **Divas jaunas debitora darbības** – viena darbība korespondē prasības summu pret oriģinālo rēķinu. Ar citu darbību tiek reģistrēts debitora parāds prasības summai, jo prasība vēl nav apstiprināta. Oriģinālā rēķina darbība un korespondējošās prasības darbība tiks automātiski atzīmēta izlīgumam, ja pievienojat rēķinu, darbību rūtī atlasot **Uzturēt \> Pievienot rēķinu**.
    - **Divas korespondējošās darbības** – šīs darbības tiek grāmatotas **Ieturējumu korespondējošā** virsgrāmatas kontā.
    - **Prasību žurnāls** — lai skatītu prasību žurnālu katram ieturējumum, kas tiek rādīti ieturējumu rīkā, atlasiet cilni **Atsauces**. Prasību žurnāls ir parādīts laukā **Žurnāla partijas numurs**. Jūs varat arī skatīt prasību žurnālu cilnē **Ieturējumu notikumi**. Tur, tai būs **Atjaunināšanas tipa** vērtība *Saskaņot*.

## <a name="create-a-credit-note-for-a-customer"></a>Kredīta notas izveidošana debitoram

Ja debitoram ir apstiprināta atlaide, ja vajadzīgs, var izveidot kredīta notu debitora kontā, tādējādi norādot atlaidi. Kredīts tiek parādīts ieturējumu rīkā, kur to var saskaņot ar ieturējumu.

Lai izveidotu kredīta notu, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Debitori \> Visi debitori**.
1. Atlasiet debitoru.
1. Darbību rūtī, cilnē **Savākt**, grupā **Norēķināties** atlasiet **Norēķināties par darījumiem**.
1. Dialoglodziņā **Norēķināties par darījumiem** atlasiet darījumu, kam atlaide tika piemērota.
1. Rīkjoslas izvēlnē **Funkcijas** atlasiet atlaižu programmas veidu, kas tiek lietots.
1. Lapas **Atlaide** cilnē **Pārskats** atlasiet izvēles rūtiņu **Atzīmēt** blakus atbilstošajiem atlaides ID.
1. Transakciju rūtī atlasiet **Funkcijas \> Izveidot kredīta notu**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Ieturējuma apstrāde ieturējumu rīkā

Ieturējumu rīkā varat saskaņot ieturējumus, lai atvērtu kredīta transakciju, sadalītu ieturējumus, noraidītu ieturējumus un norakstītu ieturējumus.

Atkarībā no tā, kā vēlaties apstrādāt ieturējumu, veiciet vienu vai vairākas no procedūrām turpmākajās apakšiedaļās. Ja nepieciešams, procedūras var apvienot. Piemēram, varat sadalīt ieturējumu divās daļās un pēc tam saskaņot vienu daļu ar kredītu, bet atlikušo daļu atstāt rīkā, lai to vēlāk saskaņotu ar citu kredītu. Varat arī saskaņot ieturējumu ar kredītu, kas ir mazāks par ieturējuma summu, un pēc tam noraidīt vai norakstīt atlikušo ieturējuma bilanci.

### <a name="match-a-deduction-to-a-credit"></a>Saskaņojiet ieturējumu ar kredītu, veiciet tālāk norādītās darbības

Lai saskaņotu ieturējumus ar kredītu, veiciet šīs darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Sadaļā **Atvērt darījumus** atlasiet izvēles rūtiņu **Atzīmēt** kredītam, lai tas atbilstu ieturējumiem. Ja ir uzskaitīti vairāki kredīti, varat atlasīt vairāk nekā vienu kredītu, kas jāsaskaņo ar ieturējumu. Ja vēlaties, lai sistēma automātiski izvēlētos kredītus, kas atbilst ieturējumu summai, rīkjoslā atlasiet atbilstošu opciju izvēlnē **Atlasīt ieturējumu summu**.
1. Darbību rūtī atlasiet vienumu **Uzturēt \> Saskaņot**. Sistēma saskaņo ieturējumu ar kredītu. Ja atlikusī bilance paliek ieturējumiem, tā tiek parādīta laukā **Atlikusī summa** cilnē **Ieturējumi**.

    > [!NOTE]
    > Ieturējumiem, kas tika izveidoti, izmantojot komandu **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā, komanda **Uzturēt \> Saskaņot** ir pieejama tikai tad, ja lauka **Prasības statuss** vērtība ir iestatīta uz *Pieņemts*. Šo komandu var izmantot, lai manuāli saskaņotu uz cenu balstītas vai uz daudzuma balstītas darbības saistītām kredītam sadaļā **Atvērtās darbības**. Šis kredīts tiek izveidots, kad ieturējums tiek apstiprināts (izmantojot komandu **Uzturēt \> Apstiprināt ieturējumu** ), vai arī, kad tas ir pievienots esošajam kredītam, kā aprakstīts tālāk šīs tēmas sadaļā [Kredīti, kas izveidoti ārpus apstiprinātā ieturējumu procesa](#credits-outside-approval). Periodisko uzdevumu *Nokārtot apstiprinātos ieturējumus* (**Pārdošanas mārketings \> Periodiskie uzdevumi \> Nokārtot apstiprinātos ieturējumus**) var arī izmantot, lai automātiski saskaņotu ieturējumus un kredītus, kam ir atbilstošas **Ieturējumu ID** vērtības un summas.

### <a name="split-a-deduction"></a>Sadalīt ieturējumus

Lai sadalītu ieturējumus, veiciet tālāk norādītās darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet vienumu **Uzturēt \> Sadalīt**.
1. Dialoglodziņa **Sadalīt**, laukā **Sadalīt summu** ievadiet summu, kas jāsadala no galvenajiem ieturējumiem. Pēc tam atlasiet **Labi**.
1. Cilnē **Ieturējumi** redzams jauns ieraksts sadalītajai summai. Sākotnējā ieturējumu ierakstā ietverts ieturējumu bilances atlikums. Tagad sākotnējās atlaides divas daļas var pārvaldīt atsevišķi.
1. Atlasiet sākotnējo ieturējumu ierakstu un pēc tam cilni **Atsauces**. Lauks **Sadalītā summa** parāda summu, kas tika sadalīta no sākotnējās summas.

### <a name="attach-an-invoice-to-a-deduction"></a>Rēķina pievienošana ieturējumiem

Varat pievienot rēķinu ieturējumiem, ja ieturējumi tika izveidoti, izmantojot komandu **Jaunie ieturējumi** ieturējumu rīkā, debitora izlīgumā vai debitora lapā un, ja tam pašlaik nav pievienots rēķins (t.i., kolonna **Rēķins** ir tukša).

Lai ieturējumam pievienotu rēķinu, veiciet šādas darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet **Uzturēt \> Pievienot rēķinu**.
1. Dialoglodziņā **Pievienot rēķinu** atlasiet rēķinu un pēc tam atlasiet **Labi**.
1. Dialoglodziņā **Norēķināties par darījumiem** izpildiet vienu no šīm darbībām atkarībā no tā, vai prasības žurnāls tika grāmatots, kad tika izveidoti ieturējumi:

    - Ja prasības žurnāls tika grāmatots, jūsu atlasītais rēķins un prasību žurnāla debitora kredīta transakcija kolonnā **Iezīmēt** parāda atzīmi. Atlasiet **Grāmatot**. Pievienotā rēķina atlikusī bilance tiek samazināta par prasības summu.
    - Ja prasības žurnāls netika grāmatots, kolonnā **Ietzīmet** nevienā darījumā nav atzīmēta atzīme. Tā kā jūs nevarat veikt ieturējumu nobīde pret prasību žurnālu, kamēr ieturējums nav apstiprināts, atlasiet **Atcelt**.

### <a name="detach-an-invoice-from-a-deduction"></a>Atvienojiet rēķinu no ieturējuma

Varat atvienot rēķinu no ieturējuma, ja ieturējums tika izveidots, izmantojot komandu **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā un, ja tam pašlaik nav pievienots rēķins (t.i., kolonna **Rēķins** parāda rēķina numuru) un, ja lauks **Prasības statuss** ir iestatīts uz *Atvērts*. Šo uzdevumu var pabeigt, jo ir pievienots nepareizs rēķins. Rēķins tiek noņemts no ieturējumiem, un tā atlikusī bilance tiek atjaunināta, ja tā tika samazināta, kad tika pievienots rēķins.

Lai noņemtu rēķinu, rīkojieties šādi.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet **Uzturēt \> Atvienot rēķinu**.

### <a name="approve-a-deduction"></a>Apstiprināt ieturējumus

Jūs varat apstiprināt ieturējumus, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā. Tomēr varat apstiprināt tikai ieturējumus, kur lauka **Prasības statuss** iestatījums ir *Atvērts*.

Lai apstiprinātu ieturējumus, veiciet tālāk norādītās darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet **Uzturēt \> Apstiprināt ieturējums**.
1. Dialoglodziņā **Apstiprināt ieturējumus** rediģējiet vai pievienojiet informāciju vērtībai **Piezīme** pēc vajadzības.
1. Ja ieturējumi ir balstīti uz cenu un tam nav pievienots rēķins, atlasiet krājumu PVN grupu. Parasti PVN grupa tiek iestatīta rēķinā. Tāpēc nodokļa krājuma kods ir jānorāda, kad tas nav pievienots rēķinam.
1. Atlasiet **Labi**.

    Šajā brīdī ieturējumiem nevar veikt turpmākas izmaiņas. Ja opcija **Izveidot prasības žurnālu** tika iestatīta uz *Nē*, kad tika izveidoti ieturējumi, prasību žurnāls tiek izveidots un grāmatots, kad ieturējums tiek apstiprināts. Pēc ieturējumu apstiprināšanas kredīts tiek izveidots un atvērts automātiski. Veids ir atkarīgs no ieturējumu **Prasības pamata** vērtības:

    - *Uz cenu balstīts* - ja ieturējums ir atkarīgs no cenas, debitora kontam tiek izveidots brīva teksta rēķins. Var pievienot aprakstu un grāmatot kredītu. Veidojot melnrakstu, šie lauki tiek aizpildīti ar ieturējumiem:

        - **Ieturējumu ID** — šis lauks ir pievienots virsrakstam, lai iespējotu izsekošanas atpakaļ ieturējumus.
        - **Galvenais konts** - vērtību nosaka vērtība **Prasības grāmatošanas konts**, kas ir iestatīta ieturējumu iemeslam, kas tiek piešķirts ieturējumiem.
        - **Krājumu PVN grupa** – vērtību nosaka piesaistītais rēķins vai vērtība, ko atlasījāt, apstiprinot ieturējumu.
        - **Vienības cena** – vērtība ir ieturējumu prasības summas kredīts.
        - **Rēķina teksts** - pēc noklusējuma šis lauks ir iestatīts uz ieturējumu **Piezīme** vērtību.

    - *Uz daudzumu balstīts* - ja ieturējums ir atkarīgs no daudzuma, tiek izveidots atvērts pārdošanas pasūtījums vai atgriešanas pasūtījums. Iestatījums **Izveidot atgriešanas pasūtījumu** lapa **[Debitoru parādu parametri](#accounts-receivable-deductions)** nosaka, vai pārdošanas pasūtījums vai atgriešanas pasūtījums tiek izveidots, kad tiek apstiprināts ieturējums. Tiek parādīta lapa **Kopēt pasūtījumus**, un tā tiek filtrēta, lai parādītu rindas, kur lauks **Rēķina konts** ir iestatīts ieturējumu debitora kontā. Rīkojieties šādi:

        1. Kopsavilkuma cilnē **Rēķini** sadaļa **Virsraksti** parāda pārdošanas rēķinus, kuru vērtība **Rēķina konts** atbilst ieturējumu debitora kontam. Izvēlieties piederīgs pārdošanas rēķins.
        1. Sadaļa **Rindas** rāda rindas no atlasītā pārdošanas rēķina. Atzīmējiet izvēles rūtiņu **Atlasīt** katrai rindai, kuru vēlaties kopēt. Vai sadaļā **Virsraksti** atzīmējiet izvēles rūtiņu **Atlasīt visas**, lai pārdošanas pasūtījums atlasītu visas rindas.
        1. Pēc vajadzības koriģējiet vērtību **Daudzums** vienai vai vairākām rindām.

            Visas atlasītās rindas līdz šim ir norādītas kopsavilkuma cilnē **Atlasītās rindas vai virsraksts, kas jākopē**.

        1. Pēc vajadzības atkārtojiet iepriekšējās divas darbības, līdz visas nepieciešamās rindas ir uzskaitītas kopsavilkuma cilnē **Atlasītās rindas vai virsraksts, kas jākopē**.
        1. Atlasiet **Labi**.

            Jaunais atgriešanas pasūtījums ir atvērts, un automātiski tiek iestatīti sekojošie lauki:

            - **Ieturējumu ID** — šis lauks ir pievienots virsrakstam, lai iespējotu izsekošanas atpakaļ ieturējumus.
            - **Atgriešanas iemesla kods** - Pēc noklusējuma šis lauks ir iestatīts uz vērtību **Atgriešanas iemesla kods**, kas ir iestatīta ieturējumu iemeslam, kas tiek piešķirts ieturējumiem.

Kad kredīts ir iekļauts rēķinā, tā tiek parādīta ieturējumu darba sadaļā **Atvērt transakcijas** attiecībā pret piemērojamo **Ieturējumu ID** vērtību, un tā lauka **Prasības veids** vērtība ir iestatīta uz *Citi kredīti*. Kredīts būs pieejams līdz tā nosegšanas ar ieturējumiem vienā no šiem veidiem:

- Nokārtojiet to manuāli, darbību rūtī atlasot **Uzturēt \> Saskaņot**.
- To automātiski nokārto periodiskais darbs *Nokārtot apstiprinātās prasības* (**Pārdošana un mārketings \> Periodiskie uzdevumi \> Nokārtot apstiprinātās prasības**).
- Tas tiek nokārtots automātiski, jo opcija **Automātiskais izlīgums** cilnē **Izlīgums** lapā **Debitoru parādu parametri** ir iestatīta uz *Jā*.

Lai skatītu kredītu, kas tiek izveidots pēc ieturējumu apstiprināšanas, varat izmantot arī pogu **Atvērt kredītu** ieturējumu resursa sadaļā **Atvērt transakcijas**.

### <a name="create-a-return-order"></a>Atgriešanas pasūtījuma izveidošana

Jūs varat izveidot ieturējumu atgriešanas pasūtījumu, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā. Tomēr jābūt šādiem nosacījumiem:

- Lauks **Prasības pamats** ir iestatīts uz *Uz daudzumu balstīts*.
- Lauks **Prasības statuss** ir iestatīts uz *Atvērts*.
- Opcija **Izveidot atgriešanas pasūtījumu** cilnē **Ieturējumi** lapā **[Debitoru parametri](#accounts-receivable-deductions)** ir iestatīta uz *Jā*.
- Opcija **Izveidot atgriešanas pasūtījumu pirms ieturējuma apstiprināšanas** cilnē **Ieturējumi** lapā **[Debitoru parametri](#accounts-receivable-deductions)** ir iestatīta uz *Jā*.

Lai izveidotu atgriešanas pasūtījumu, rīkojieties šādi.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet **Uzturēt \> Izveidot pārdošanas pasūtījumu**.
1. Dialoglodziņā **Apstiprināt ieturējumus** rediģējiet vai pievienojiet informāciju esošai vērtībai **Piezīme**, pēc vajadzības, un atlasiet **Labi**.
1. Dialoglodziņā **Kopēc pasūtījumus**, kopsavilkuma cilnē **Rēķini** sadaļa **Virsraksti** parāda pārdošanas rēķinus, kuru vērtība **Rēķina konts** atbilst ieturējumu debitora kontam. Izvēlieties piederīgs pārdošanas rēķins.
1. Sadaļa **Rindas** rāda rindas no atlasītā pārdošanas rēķina. Atzīmējiet izvēles rūtiņu **Atlasīt** katrai rindai, kuru vēlaties kopēt. Vai sadaļā **Virsraksti** atzīmējiet izvēles rūtiņu **Atlasīt visas**, lai pārdošanas pasūtījums atlasītu visas rindas.
1. Pēc vajadzības koriģējiet vērtību **Daudzums** vienai vai vairākām rindām.

    Visas atlasītās rindas līdz šim ir norādītas kopsavilkuma cilnē **Atlasītās rindas vai virsraksts, kas jākopē**.

1. Pēc vajadzības atkārtojiet iepriekšējās divas darbības, līdz visas nepieciešamās rindas ir uzskaitītas kopsavilkuma cilnē **Atlasītās rindas vai virsraksts, kas jākopē**.
1. Atlasiet **Labi**.

    Jaunais atgriešanas pasūtījums ir atvērts, un automātiski tiek iestatīti sekojošie lauki:

    - **Ieturējumu ID** — šis lauks ir pievienots virsrakstam, lai iespējotu izsekošanas atpakaļ ieturējumus.
    - **Atgriešanas iemesla kods** - Pēc noklusējuma šis lauks ir iestatīts uz vērtību **Atgriešanas iemesla kods**, kas ir iestatīta ieturējumu iemeslam, kas tiek piešķirts ieturējumiem.

### <a name="deny-a-deduction"></a>Liegt ieturējumus

Lai liegtu ieturējumus, veiciet tālāk norādītās darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet vienumu **Uzturēt \> Liegt**.
1. Dialoglodziņā **Liegt** atlasiet noraidītā iemesla kodu un pēc tam atlasiet **Labi**.
1. Laukā **Rādīt** zem Darbību rūts atlasiet *Slēgts*.

    Cilne **Ieturējumi** rada noraidīto ieturējumu un ieturējumam lauks **Atlikusī summa** tiek iestatīts uz *0,00*.

    Ieturējumiem, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā, notiek šādi notikumi:

    - Cilnē **Atsauces** tiek atjaunināti lauki sadaļā **Noliegums**.
    - Ja atlasījāt iespēju izveidot prasību žurnālu, kad tika izveidoti ieturējumi, un, ja rēķins ir pievienots ieturējumiem, kas samazina rēķina bilanci, rēķins tiek atvienots, un iepriekš pievienotā rēķina atlikusī bilance tiek palielināta par noraidītā prasības summu.
    - Ieturējumu lauks **Statuss** ir iestatīts uz *Slēgts*.
    - Ieturējumu lauks **Prasības tatuss** ir iestatīts uz *Noraidīts*.

Lai atceltu atteikumu, veiciet tālāk norādītās darbības.

1. Cilnē **Ieturējumi** atlasiet noraidītos ieturējumus.
1. Darbību rūtī atlasiet **Atcelt atteikumu**.

    Ieturējumiem, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā, notiek šādi notikumi:

    - Cilnē **Atsauces** tiek atjaunināti lauki sadaļā **Noliegums**.
    - Ieturējumu lauks **Statuss** ir iestatīts uz *Atvērts*.
    - Ieturējumu lauks **Prasības tatuss** ir iestatīts uz *Atvērts*.

### <a name="write-off-a-deduction"></a>Norakstīt ieturējumu

Lai norakstītu ieturējumus, veiciet tālāk norādītās darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet vienumu **Uzturēt \> Norakstīt**.
1. Dialoglodziņā **Norakstīt** atlasiet norakstītā iemesla kodu un pēc tam atlasiet **Labi**.
1. Laukā **Rādīt** atlasiet opciju *Slēgts*.

    Cilne **Ieturējumi** rada norakstīto ieturējumu un ieturējumam lauks **Atlikusī summa** tiek iestatīts uz *0,00*.

    Ieturējumiem, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā, notiek šādi notikumi:

    - Cilnē **Atsauces** tiek atjaunināti lauki sadaļā **Norakstīt**.
    - Ja prasības žurnālu izveidojāt ieturējumu izveides laikā, prasību žurnāls tiek grāmatots ieturējumu norakstīšanas iemesla kodā. Varat skatīt šo ierakstu cilnē **Ieturējumu notikumi**, kur tai ir **Atjaunināšanas tipa** vērtība *Norakstīšana*.
    - Ieturējumu lauks **Statuss** ir iestatīts uz *Slēgts*
    - Ieturējumu lauks **Prasības tatuss** ir iestatīts uz *Norakstīts*.

Lai atceltu norakstīšanu, veiciet tālāk norādītās darbības.

1. Cilnē **Ieturējumi** atlasiet noraidītos ieturējumus.
1. Darbību rūtī atlasiet vienumu **Atcelt norakstīšanu**.

    Ieturējumiem, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā, notiek šādi notikumi:

    - Cilnē **Atsauces** tiek atjaunināti lauki sadaļā **Norakstīt**.
    - Ja prasības žurnālu izveidojāt ieturējumu izveides laikā, prasību žurnāls tiek grāmatots ieturējumu norakstīšanas iemesla kodā. Varat skatīt šo ierakstu cilnē **Ieturējumu notikumi**, kur tai ir **Atjaunināšanas tipa** vērtība *Atcelt norakstīšanu*.
    - Ieturējumu lauks **Statuss** ir iestatīts uz *Atvērts*.
    - Ieturējumu lauks **Prasības tatuss** ir iestatīts uz *Atvērts*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kredīti, kas izveidoti ārpus apstiprinātāju ieturējumu procesa

Šī sadaļa attiecas tikai uz ieturējumiem, kas tika izveidoti, izmantojot **Jauns ieturējums** ieturējumu rīkā, debitora izlīgumā vai debitora lapā.

Iespējams, dažādi lietotāji jau ir izveidojuši brīva teksta rēķinu, atgriešanas pasūtījumu vai negatīvu pārdošanas pasūtījumu debitora prasībai ārpus procesa **Apstiprināt ieturējumu**. Kad ieturējumu ieturējums ir apstiprināts ieturējumu laukā, sistēma automātiski izveido citu brīvā teksta rēķinu, atgriešanas pasūtījumu vai negatīvu pārdošanas pasūtījumu. Šajā sadaļā ir aprakstīts, kā pievienot esošos kredītus ieturējumiem pirms ieturējumu apstiprināšanas, lai palīdzētu novērst kredītu dublikātus.

### <a name="attach-a-credit-to-deduction"></a>Pievienojiet ieturējumam kredītu

Šajā sadaļā ir aprakstīts, kā var pievienot kredītu kredīta ieturējumam.

Kad ieturējumam ir pievienots kredīts, varat to skatīt, izmantojot pogu rīkjosla **Atvērt kredītu** ieturējumu resursa sadaļā **Atvērt transakcijas**.

Kad kredīts ir iekļauts rēķinā, un ieturējums ir apstiprināts, kredīts tiek parādīts ieturējumu darba sadaļā **Atvērt transakcijas** attiecībā pret piemērojamo **Ieturējumu ID** vērtību, un tā lauka **Prasības veids** vērtība ir iestatīta uz *Citi kredīti*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Brīvā teksta pievienošana ieturējumiem

Lai ieturējumam pievienotu brīvo tekstu, veiciet šādas darbības.

1. Dodieties uz **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**.
1. Atlasiet atbilstošo rēķinu.
1. Darbību rūts cilnē **Rēķins** atlasiet **Pievienojiet kredītu ieturējumam**. Šī poga ir pieejama tikai tad, ja brīva teksta rēķina lauks **Ieturējuma ID** ir tukšs. Tukšs lauks norāda, ka brīvā teksta rēķins vēl nav pievienots ieturējumiem.
1. Lapā **Pievienot kredītu ieturējumam** var atlasīt *vienu* ieturējumu. Atlasei ir pieejami tikai atvērti *uz cenu balstīti* ieturējumi.
1. Atlasiet **Labi**. Lauks **Ieturējumu ID** ir iestatīts brīva teksta rēķina galvenē.

#### <a name="attach-a-return-order-to-a-deduction"></a>Atgriešanas pasūtījuma pievienošana ieturējumiem

Lai ieturējumam pievienotu atgriešanas pasūtījumu, veiciet šādas darbības.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi atgriešanas pasūtījumi**.
1. Atlasiet piemērojamo saņemtā vai atvērtā atgrieztā krājuma autorizācijas (AKA) kodu.
1. Darbību rūts cilnē **Atgriešanas pasūtījums** atlasiet **Pievienojiet kredītu ieturējumam**. Šī poga ir pieejama tikai tad, ja atgriešanas pasūtījuma lauks **Ieturējuma ID** ir tukšs. Tukšs lauks norāda, ka atgriešanas pasūtījums vēl nav pievienots ieturējumiem.
1. Lapā **Pievienot kredītu ieturējumam** var atlasīt *vienu* ieturējumu. Atlasei ir pieejami tikai atvērti *uz daudzumu balstīti* ieturējumi.
1. Atlasiet **Labi**. Lauks **Ieturējumu ID** ir iestatīts atgriešanas pasūtījuma galvenē.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Pārdošanas pasūtījuma pievienošana ieturējumiem

Lai ieturējumam pievienotu pārdošanas pasūtījumu, veiciet šādas darbības.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet piemērojamo atvērto, piegādāto vai rēķinā iekļauto pārdošanas pasūtījumu.
1. Darbību rūts cilnē **Rēķins** atlasiet **Pievienojiet kredītu ieturējumam**. Šī poga ir pieejama tikai tad, ja pārdošanas pasūtījuma lauks **Ieturējuma ID** ir tukšs. Tukšs lauks norāda, ka pārdošanas pasūtījums vēl nav pievienots ieturējumiem.
1. Lapā **Pievienot ieturējumu** var atlasīt *vienu* ieturējumu. Atlasei ir pieejami tikai atvērti *uz daudzumu balstīti* ieturējumi.
1. Atlasiet **Labi**. Lauks **Ieturējumu ID** ir iestatīts pārdošanas pasūtījuma galvenē.

#### <a name="detach-a-deduction-from-a-credit"></a>Atvienot ieturējumus no kredīta

Ja ir piesaistīti nepareizi ieturējumi, varat to atvienot no kredīta. Tomēr jābūt šādiem nosacījumiem:

- Kredīts ir piesaistīts ieturējumiem.
- Lauks **Prasības statuss** ir iestatīts uz *Atvērts*.

Lai atvienotu ieturējumus no kredīta, veiciet vienu no šīm darbībām atkarībā no kredīta tipa:

- **Brīva teksta rēķini**: lapā **Visi brīva teksta rēķini** atlasiet rēķinu. Tad, darbību rūts cilnē **Rēķins** atlasiet **Atvienojiet kredītu no ieturējumam**.
- **Atgriešanas pasūtījumi:** lapā **Visi atgriešanas pasūtījumi** izvēlieties pasūtījumu. Tad, darbību rūts cilnē **Atgriešanas pasūtījums** atlasiet **Atvienojiet kredītu no ieturējumam**.
- **Pārdošanas pasūtījumi:** lapā **Visi pārdošanas pasūtījumi** izvēlieties pasūtījumu. Tad, darbību rūts cilnē **Rēķins** atlasiet **Atvienojiet kredītu no ieturējumam**.

### <a name="attach-a-deduction-to-a-credit"></a>Pievienojiet ieturējumu kredītam, veiciet tālāk norādītās darbības

Šajā sadaļā ir aprakstīts, kā var pievienot ieturējumu kredītam no ieturējuma.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Ieturējumu pievienošana brīvam tekstam, atgriešanas pasūtījumam vai pārdošanas pasūtījuma kredītam

Lai pievienotu ieturējumu brīvam tekstam, atgriešanas pasūtījumam vai pārdošanas pasūtījuma kredītam, veiciet šīs darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasīt piemērojamos atvērtos ieturējumus.
1. Darbību rūtī atlasiet **Uzturēt \> Pievienot ieturējumu kredītam**. Šī poga ir pieejama tikai tad, ja lauka **Prasības statuss** vērtība ir iestatīta uz *Atvērts*.
1. Lapā **Pievienot kredītu** var atlasīt *vienu* kredītu. Norādīto kredītu veids ir atkarīgs no ieturējumu **Prasības pamata** vērtības:

    - *Uz cenas balstīts* - lapa parāda brīvā teksta rēķinus debitora kontam, kur lauks **Ieturējumu ID** ir tukšs. Tiek rādīti arī debitoru pieprasījumi, jo brīva teksta rēķins, iespējams, nav grāmatots. Tāpēc tam, iespējams, nav numura, uz kuru var atsaukties.
    - *Uz daudzumu balstīts* – rādīto kredītu tips ir atkarīgs no opcijas **Izveidot atgriešanas pasūtījumu** iestatījuma lapā **[Debitoru parādu parametri](#accounts-receivable-deductions)**:

        - *Jā* - lapa parāda atgriešanas pasūtījumus debitora kontam, kur lauks **Ieturējumu ID** ir tukšs.
        - *Nē* - lapa parāda pārdošanas pasūtījumus debitora kontam, kur lauks **Ieturējumu ID** ir tukšs.

1. Atlasiet **Labi**. Lauks **Ieturējumu ID** ir iestatīts kredīta galvenē.

Kad ieturējumam ir pievienots kredīts, varat to skatīt, izmantojot pogu rīkjosla **Atvērt kredītu** ieturējumu resursa sadaļā **Atvērt transakcijas**.

Kad kredīts ir iekļauts rēķinā, un ieturējums ir apstiprināts, kredīts tiek parādīts ieturējumu darba sadaļā **Atvērt transakcijas** attiecībā pret piemērojamo **Ieturējumu ID** vērtību, un tā lauka **Prasības veids** vērtība ir iestatīta uz *Citi kredīti*.

#### <a name="detach-a-credit-from-the-deduction"></a>Atvienot kredītu no ieturējuma

Ja ir piesaistīti nepareizi kredīti, varat to atvienot no ieturējuma. Darbību rūts grupā **Uzturēt** atlasiet **Atvienojiet ieturējumu no kredīta**. Vērtība **Ieturējumu ID** tiek noņemta no kredīta.

Poga **Atvienot ieturējumu no kredīta** ir pieejama tikai tad, ja ir ievēroti šādi nosacījumi:

- Kredīts ir piesaistīts ieturējumiem.
- Lauks **Prasības statuss** ir iestatīts uz *Atvērts*.

## <a name="create-a-one-time-promotion"></a>Izveidot vienreizēju veicināšanas pasākumu

Dažreiz jums, iespējams, nav apstiprinātas atlaides, ko var saskaņot ar ieturējumu. Šajā gadījumā varat izmantot līdzekli *vienreizēja paaugstināšana*, lai ieturējumu saskaņotu ar mazumtirdzniecības atlaidi, kas ir saistīta ar debitoru. Līdzeklis *vienreizēja paaugstināšana* izveido jaunu tirdzniecības atlaižu līgumu un vienreizējas izmaksas tirgū virzīšanas notikumu. Pēc tam tas vienreizējo izmaksu saskaņo ar ieturējumu un veic grāmatojumus, kas ir nepieciešami ieturējuma aizvēršanai.

Šis līdzeklis ir noderīgs, ja izmantojat mazumtirdzniecības atlaides. Papildinformāciju par mazumtirdzniecības atlaidēm skatiet [Mazumtirdzniecības atvieglojumu pārvaldība](../sales-marketing/trade-allowance.md).

Vispirms ir jāiestata veidne, ko var izmantot jauna tirdzniecības atlaižu līguma izveidei. Lai iestatītu veidni, veiciet tālāk aprakstītās darbības.

1. Pārejiet uz sadaļu **Pārdošana un mārketings \> Tirdzniecības atlaides \> Veidnes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukos ievadiet informāciju, kam jābūt norādītai līgumos, kas izveidoti no veidnes.
1. Kopsavilkuma cilnes **Debitori** laukā **Hierarhija** atlasiet hierarhijas līmeni.
1. Hierarhijas sarakstā atlasiet debitoru, kuram ir nesaskaņoti ieturējumi, un pēc tam atlasiet labo bultiņas pogu (**\>**). Debitors ir pievienots sarakstam **Mazumtirdzniecības atlaižu līguma debitori**.
1. Kad nepieciešams, iestatiet atlikušos laukus un pēc tam aizveriet lapu.
1. Dodieties uz **Pārdošana un mārketings \> Iestatīšana \> Tirdzniecības atlaide \> Tirdzniecības atļauju pārvaldības parametri**.
1. Cilnes **Pārskats** laukā **Vienreizējās veicināšanas pasākumu veidne** atlasiet tās veidnes nosaukumu, kuru izmantot, lai izveidotu vienreizējus veicināšanas pasākumus.

Pēc tam varat izveidot vienreizējo veicināšanas pasākumu ieturējumu rīkā. Lai izveidotu vienreizēju veicināšanu, rīkojieties šādi.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Atlasiet izvēles rūtiņu **Atzīmēt** blakus apstrādājamajam ieturējumam.
1. Darbību rūtī atlasiet **Uzturēt \> Norēķināties par ieturējumu kā vienreizēju veicināšanu**.
1. Dialoglodziņā **Vienreizējie veicināšanas pasākumi** veiciet tālāk norādītās darbības, lai saistītu ieturējumus ar vienu vai vairākiem līdzekļiem.

    1. Atlasiet **Jauns** un pēc tam laukā **Līdzekļu ID** atlasiet līdzekļu ID. Atkārtojiet šo darbību, lai pievienotu tik daudz līdzekļu, cik nepieciešams.
    1. Laukā **Procenti** blakus katram līdzekļu ID ievadiet ieturējuma procentuālo vērtību, kas jāpiešķir līdzekļiem. Summām, ko ievadāt laukos **Procenti**, kopā jāveido 100 procenti.

1. Atlasiet **Labi**. Sistēma izveido jaunu tirdzniecības atlaižu līgumu, kurā ir vienreizējas izmaksas tirgū virzīšanas notikums un kas saskaņo vienreizējo izmaksu ar ieturējumu.

## <a name="do-a-mass-update-of-deductions"></a>Ieturējumu atjaunināšana masveidā

Ja nepieciešams veikt vienādas izmaiņas vairākiem ieturējumiem, varat atlasīt šos ieturējumus un veikt to lauku atjaunināšanu masveidā.

Lai veiktu atjaunināšanu masveidā, veiciet tālāk norādītās darbības.

1. Doties uz **Tirdzniecība un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**.
1. Laukā **Rādīt** zem Darbību rūts atlasiet apskatāmo ieturējumu veidu.
1. Atzīmējiet izvēles rūtiņu blakus katram ieturējumam, kuru vēlāties jāatjaunināt. Tad darbību rūtī atlasiet **Uzturēt \> Masveida atjaunināšana**.
1. Dialoglodziņā **Masveida atjaunināšana** tiek parādīti atlasītie ieturējumi. Pēc izvēles atjauniniet laukus un pēc tam atlasiet **Labi**, lai pieņemtu izmaiņas.
