---
title: Slēgta piedāvājumu izteikšana PP
description: Šajā rakstā ir aprakstīts, kā iestatīt aizzīmogotu solījumu, lai glabātu kreditora piedāvājuma atbilžu noslēpumu, līdz pirkšanas personāls tās atzīst.
author: GalynaFedorova
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 40f1735d7efa5131b1462963758b6b48eec78fea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890891"
---
# <a name="sealed-bidding-for-rfqs"></a>Slēgta piedāvājumu izteikšana PP

[!include [banner](../includes/banner.md)]

Aizzīmogota izsole nodrošina, ka kreditora solītās atbildes ir slepenas, līdz pirkšanas personāls noņem aizzīmogotos piedāvājumus. Visiem piedāvājumiem, kas attiecas uz piedāvājuma pieprasījumu (PP), vispirms ir pieejami, kad tiem tiek noņemts zīmogs pēc piedāvājuma beigu datuma. Pirms tiek noņemti aizzīmogoti piedāvājumi, tam var piekļūt tikai lietotāji, kuriem ir atvēlētas lietotāju lomas un kuri pārstāv šo kreditoru.

> [!IMPORTANT]
> Veidlapu pārveidošana vai paplašināšana vai jaunu veidlapu vai biznesa loǵikas izveide var traucēt aizsardzībai, kuru Microsoft nodrošina zīmogotajiem piedāvājumiem. Jūs uzņematies atbildību par risku, kas izriet no jebkādu pārveidojumu, paplašinājumu, jaunu veidlapu vai biznesa loģikas izmantošanas, vai par nespēju lietot zīmogoto piedāvājumu līdzekli šādu pārveidojumu, paplašinājumu, jauno veidlapu vai biznesa loģikas dēļ.  Microsoft neuzņemas atbildību par jebkādiem bojājumiem, kas izriet no jebkādiem veidlapu pārveidojumiem vai paplašinājumiem, vai jebkurām veidlapām vai biznesa loģiku, kuru izveidojat, vai kuru trešā puse izveido jums. Microsoft nenodrošina tehnisku vai cita veida atbalstu gadījumā, ja tiek veiktas jebkādas veidlapu pārveides vai paplašinājumi vai ja tiek izveidotas jaunas veidlapas vai biznesa loģika, ko izveidojat jūs vai ko jūsu vārdā izveido trešā puse. Vienīgi jūs atbildat par to, ka tiek ievēroti visi spēkā esošie tiesību akti vai regulējumi, kuri attiecas uz zīmogotajiem piedāvājumiem.

## <a name="how-bids-are-kept-secure"></a>Kā piedāvājumi tiek saglabāti drošībā

Aizzīmogotā izsolē tiek izmantota asimetriska šifrēšana, lai šifrētu piedāvājuma šifrēšanas atslēgu (KEK) un simetriska šifrēšana, lai šifrētu faktisko piedāvājumu. Sistēma integrējas ar Microsoft Azure Key Vault, lai ģenerētu un pārvaldītu šifrēšanas atslēgas, ko izmanto, lai šifrētu aizzīmogotos piedāvājumus. Katram piedāvājumam ir sava šifrēšanas atslēga. Šī šifrēšana tiek droši glabāta Key Vault, kas pieder organizācijai, kas darbojas ar Dynamics 365 Supply Chain Management. Sistēma piekļūst atslēgai pēc pieprasījuma, kad nepieciešama šifrēšana un atšifrēšana.

## <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Šajā sadaļā ir aprakstīti priekšnosacījumi, kam jābūt vietā, lai varētu nosūtīt PP, kam nepieciešama aizzīmogota informācija.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>1. darbība: lietotāja piekļuves iestatīšana aizzīmogotai izsolei

Kad jūs izmantojat aizzīmogotu izsoli, tikai lietotāji, kas iestatīti kā kreditora kontaktpersonas, var skatīt, rediģēt un iesniegt piedāvājumus šim kreditoram līdz tiek beidzies izsoles periods. Šiem lietotājiem jābūt lomai **Kreditors (ārējs)**, un tiem jābūt iestatītiem kā kreditora konta kontaktpersonām. Kontaktpersonai arī jābūt atļaujai veikt kreditoru sadarbību, kā aprakstīts sadaļā [Iestatīt un uzturēt kreditoru sadarbību](set-up-maintain-vendor-collaboration.md).

Tā kā lietotāji, kuriem ir atbilstošas atļaujas un kuri ir iestatīti kā kreditora kontaktpersonas, var piekļūt aizzīmogotajiem kreditora piedāvājumiem, ir svarīgi izsekot, kas šie lietotāji ir. Sistēmas administrators, kas iestata lietotājus un drošības lomas, ir atbildīgs par aizzīmogotu piedāvājumu piekļuves ierobežošanu tiem lietotājiem, kuriem tiešām ir atļauts tos skatīt.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>2. darbība: iespējojiet aizzīmogotas izsoles līdzekli

Pirms sākat iestatīt vai izmantot šo līdzekli, ir jāpārliecinās, vai tas ir pieejams jūsu sistēmā. Administratori var izmantot darbvietu **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Sagāde un ieguve*
- **Līdzekļa nosaukums:** *Aizzīmogota izsole PP*

### <a name="step-3-set-up-azure-key-vault"></a>3. darbība: Azure Key Vault iestatīšana

Supply Chain Management izmanto šifrēšanas atslēgas, lai aizsargātu visus aizzīmogotos piedāvājumus un paturētu tos slepenos līdz atbilstošajam laikam. Tas izmanto Key Vault spēju priekšrocības, lai ģenerētu un pārvaldītu nepieciešamās atslēgas. Tādēļ, lai aktivizētu sistēmu, jums ir jāiestata savienojums no Supply Chain Management uz atslēgu.

> [!IMPORTANT]
> Atslēgai, kas tiek lietota aizzīmogotos piedāvājumos, jāatbilst šādiem nosacījumiem:
>
> - Ja testēšanai un izstrādei un testēšanai izmantojat kasti, tad vienai atvēlētai atslēgai, kas paredzēta glabātavai, un atsevišķai atslēgai ražošanai.
> - Key Vault ir jābūt veidotai Azure abonementā, kas pieder jūsu organizācijai (nevis abonementā, kurā jūs izmantojiet Supply Chain Management).
> - Katra atslēga ir jāizmanto tikai aizzīmogotiem piedāvājumiem. Jūs nedrīkstat izmantot aizzīmogotu cenu noteikšanas taustiņus citiem nolūkiem.

Katrs piedāvājums izgūst savu slepeno atslēgu. Šī atslēga tiek izmantota ikreiz, kad lietotājs skata, atjaunina vai noņem zīmogu no piedāvājuma.

Key Vault ģenerē atslēgu, kas tiek izmantota, lai izgūtu noslēpumu, kad kreditors kreditora sadarbības interfeisā atlasa **Piedāvājums**. Pēc tam atslēga beidzas pēc fiksēta laika, kad sagādes vadītājs iestata lapā **Piegādes un plānošanas parametri** risinājumā Supply Chain Management. Kad atslēga beidzas, neviena nevarēs skatīt, rediģēt vai noņemt aizzīmogotu piedāvājumu. Tāpēc ir svarīgi konfigurēt atslēgas beigu datumus, lai būtu pietiekami daudz laika, lai varētu pabeigt izsoles procesu.

Nākošās trīs darbībās jūs iestatīsiet savienojumu ar Key Vault. Vispirms jūs iestatīsit Key Vault, ko izmantot ar aizzīmogoto izsoli. Pēc tam konfigurēsiet Supply Chain Management, lai sazinātos ar Key Vault. Visbeidzot jūs iestatīsiet atslēgas beigu laiku.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>4. darbība: iestatīt Key Vault, ko izmantot ar aizzīmogoto izsoli

Lai iestatītu Key Vault, rīkojieties šādi. Darbību secība ir svarīga.

1. Ja vēl neesat iestatījis Azure abonementu, kas ir atsevišķi no abonementa, kurā darbināt Supply Chain Management, iestatiet to.
1. Iestatiet Key Vault savā atsevišķā Azure krātuvē. Papildinformāciju skatiet šeit: [Azure Key Vault krātuves uzturēšana](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Iestatiet programmu Supply Chain Management, lai tā darbotos kā Key Vault klients. Papildinformāciju skatiet šeit: [Azure Key Vault klienta iestatīšana](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>5. darbība: Key Vault parametru konfigurēšana Supply Chain Management

Lai konfigurētu Supply Chain Management tā, lai tas komunicētu ar Key Vault aizzīmogotās izsoles laikā, veiciet šīs darbības.

1. Piesakieties Supply Chain Management un dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Key Vault parametri**.
1. Atlasiet **Jauns**, lai izveidotu ierakstu, un iestatiet tam šādus laukus:

    - **Nosaukums** – ievadiet nosaukumu.
    - **Apraksts** – ievadiet aprakstu.
    - **Key Vault URL** — ievadiet noklusējuma Key Vault URL.
    - **Key Vault klients** - ievadiet interaktīvā klienta ID programmā Active Directory, kas ir saistīta ar Key Vault autentifikācijai.
    - **Key Vault slepenā atslēga** – ievadiet sertifikāta slepeno atsauci.
    - **Iespējots aizzīmogotai izsolei** — iestatiet šo opciju kā *Jā*.

![Key Vault parametru lapa](media/sealed-bidding-key-vault-param.png "Key Vault parametru lapa")

> [!NOTE]
> Ir iespējams vienlaicīgi iespējot tikai vienu Key Vault konfigurāciju aizzīmogotai izsolei. Pirms atspējot esošu Key Vault konfigurāciju, pārliecinieties, ka visiem aizzīmogotajiem piedāvājumiem, kas to izmanto, ir noņemti. Pārbaudiet katru *Aizzīmogotā* tipa PP gadījumu un pārliecinieties, vai visas tā aizzīmogotās atbildes ir noņemtas.

### <a name="step-6-set-the-key-expiration-time"></a>6. darbība: atslēgas beigu laika iestatīšana

Lai iestatītu beigu laiku, kas tiek piemērots atslēgai, kas tiek ģenerēta katram jaunam piedāvājumam, veiciet šīs darbības.

1. Dodieties uz **Sagādes un avotu parametri \> Iestatīšana \> Sagādes un avotu parametri**.
1. Cilnes **Piedāvājuma pieprasījums** laukā **Dienas nobīde** ievadiet PP perioda pēdējo dienu skaitu. Kad PP ir izveidots, šeit ievadītais dienu skaits tiek pievienots sistēmas datumam, lai definētu noklusējuma PP beigu datumu.
1. Laukā **Šifrēšanas atslēgas beigu dienas nobīde** ievadiet dienu skaitu, pēc kura katrai šifrēšanas atslēgai ir jābūt derīgai. Kad šifrēšanas atslēga beidzas, neviena nevarēs skatīt, rediģēt vai noņemt aizzīmogotu piedāvājumu, kas to izmanto.

> [!TIP]
> Lauka **Šifrēšanas atslēgas beigu dienas nobīde** vērtība nedrīkst būt mazāka par lauka **Dienas nobīde** vērtību.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>7. darbība: noklusējuma piedāvājuma veida iestatīšana

Katram PP gadījumam ir piedāvājuma veids. Piedāvājuma veids nosaka, vai PP gadījums sniedz atvērtu vai aizzīmogotu izsoli.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>PP gadījumi, kam nav lūguma veida

Lai iestatītu noklusējuma piedāvājuma veidu, kas tiek piešķirts jauniem PP gadījumiem, kuriem nav piešķirts lūguma veids to izveides laikā, veiciet šīs darbības.

1. Dodieties uz **Sagādes un avotu parametri \> Iestatīšana \> Sagādes un avotu parametri**.
1. Cilnē **Piedāvājuma pieprasījums** iestatiet lauku **Piedāvājuma veids** uz *Aizzīmogots*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>PP gadījumi, kam ir lūguma veids

Lai iestatītu noklusējuma piedāvājuma veidu, kas tiek piešķirts jauniem PP gadījumiem, kuriem ir piešķirts lūguma veids to izveides laikā, veiciet šīs darbības.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Iestatīšana \> Piedāvājuma pieprasījums \> Lūguma tips**.
1. Izveidojiet jaunu lūguma veidu vai atlasiet esošu lūguma veidu, kurā vēlaties izmantot aizzīmogotu piedāvājuma veidu *Aizzīmogots*.
1. Laukam **Piedāvājuma tips** iestatiet vērtību *Aizzīmogots*.
1. Atkārtojiet šīs darbības katram papildu lūguma veidam, kur vēlaties ieviest aizzīmogotu izsoli.

> [!TIP]
> Lūguma veids nav jāpiešķir, veidojot jaunu PP. Ja tiek piešķirts lūguma veids, PP noklusējuma piedāvājuma veids var to izgūt. Pretējā gadījumā var izmantot sagādes un plānošanas parametros definēto noklusējuma lūguma veidu.

## <a name="the-sealed-bidding-process"></a>Zīmogotais izsoles process

Aizzīmogotas izsoles process ir gandrīz tāds pats, kā aprakstīts sadaļā [Piedāvājuma pieprasījuma (PP) pārskats](request-quotations.md). Galvenā atšķirība ir tā, ka piedāvājuma dati un to pielikumi tiek šifrēti, līdz aizzīmogoti piedāvājumi tiek noņemti.

> [!IMPORTANT]
> [Aptaujas](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) netiek šifrētas, un tās nevajadzētu izmanto sensitīvas informācijas iegūšanai.

Tālāk ir sniegts šā procesa izklāsts:

1. Izveidojiet piedāvājuma pieprasījumu un izsūtiet to vienam vai vairākiem kreditoriem.
1. Kreditori atbild, iesniedzot aizzīmogotu piedāvājumu.
1. Jūs noņemsiet aizzīmogotus piedāvājumus pēc piedāvājuma ieraksta beigu laika.
1. Piedāvājumi kļūst redzami, un tos var novērtēt un salīdzināt.
1. Kad piedāvājums ir pieņemts, jūs ģenerējat pirkšanas pasūtījumu, veidojat pirkšanas līgumu vai atjauniniet pirkšanas pieprasījumu.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Izveidot PP gadījumu, kam tiek izmantots aizzīmogots piedāvājums

Aizzīmogotās izsoles PP gadījuma izveides process ir gandrīz tāds pats kā nezīmogotas izsoles process. Informāciju par to, kā izveidot abus PP gadījumus, skatiet sadaļā [Piedāvājuma pieprasījuma izveide](tasks/create-request-quotation.md). Šajā sadaļā ir iezīmēti daži svarīgi apsvērumi, izveidojot PP aizzīmogotai izsolei.

Aizzīmogotas izsoles PP gadījumu vērtībai **Piedāvājuma veids** jābūt *Aizzīmogotai*. Pastāv trīs veidi, kā piešķirt šo vērtību PP gadījumam:

- Pēc vērtības izveides iestatiet vērtību tieši PP gadījumā.
- Definējiet aizzīmogoto izsoli kā noklusējuma piedāvājuma tipu visiem PP gadījumiem Sagādes un avotu parametros. (Skatiet [Iestatiet noklusējuma piedāvājuma tipa sadaļu](#set-default-bid-type) iepriekš šajā rakstā.)
- Veidojot jaunu PP gadījumu, atlasiet lūguma veidu, kas ir iestatīts aizzīmogotai izsolei. (Skatiet sadaļu [Iestatīt noklusējuma piedāvājuma veidu](#set-default-bid-type).)

Aizzīmogotās izsoles PP gadījuma vērtība **Beigu datums un laiks** nosaka, kad iesniegtos aizzīmogotos piedāvājumus var noņemt. Vērtība **Beigu datums un laiks** katrā rindā atbildīs virsraksta vērtībai.

Jūs nevarat mainīt piedāvājuma veidu pēc PP gadījuma nosūtīšanas.

### <a name="vendors-respond-to-an-rfq"></a>Kreditori atbild uz PP

Kreditori, kas atbild uz aizzīmogotu piedāvājumu, izmanto to pašu procedūru, ko izmanto, lai atbildētu uz atvērtiem piedāvājumiem, kā norādīts [Darbs ar PP Kreditoru izsoles darbvietā](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Detalizētus norādījumus par to, kā strādāt gan ar atvērtiem piedāvājumiem, gan ar aizzīmogotiem piedāvājumiem, skatiet šeit: [Ievadīt un salīdzināt PP piedāvājumus un piemaksas līgumus](tasks/enter-compare-rfq-bids-award-contracts.md). Vienīgā atšķirība starp aizzīmogotiem piedāvājumiem un atvērto piedāvājumu apstrādi ir tāda, ka līdz izsoles perioda beigām sagādes profesionāli nevar atvērt kreditora aizzīmogotu piedāvājumu. Tikai kreditora kontaktpersona var atvērt šī kreditora aizzīmogoto piedāvājumu.

> [!IMPORTANT]
> Aizzīmogotai izsolei kreditori var augšupielādēt pielikumus tikai PDF formātā. Citi formāti netiks pieņemti.

Kad reģistrēts piegādātāja lietotājs atlasa **Piedāvājumu** aizzīmogotā piedāvājuma PP, viņi var ievadīt savus piedāvājuma datus un šie dati tiks aizsargāti. Kreditori var saglabāt darbu, gatavojot piedāvājumu, atgriezties pie tā tik bieži, cik nepieciešams, un pēc tam iesniegt to tad, kad tas ir gatavs. Kreditori var skatīt savu piedāvājumu arī pēc tā iesniegšanas. Ja kreditoriem pēc tā iesniegšanas ir jāmaina piedāvājums, viņi var to atsaukt, atjaunināt un atkārtoti iesniegt jebkurā laikā, līdz beidzas izsoles periods.

Aizzīmogotas izsoles laikā ir spēkā šādi nosacījumi:

- Aizzīmogotās izsoles laikā sistēma izveido žurnālu *Piedāvājuma pieprasījums*.
- Kad kreditors iesniedz piedāvājumu, PP žurnāli bez rindām tiek izveidoti ar aizzīmogotu cenu.
- Kad aizzīmogoti pieteikumi ir noņemti, tiek izveidoti PP žurnāli, kuriem ir cena un summa. Šim žurnālam var piekļūt, atlasot **Piedāvājumu pieprasījuma žurnāli** lapā **Visi piedāvājumu pieprasījumi**.
- Sistēma glabā žurnālu katrai darbībai, ko lietotāji veic ar aizzīmogotu piedāvājumu. Šīs darbības ietver piedāvājuma skatīšanu, rediģēšanu un saglabāšanu. Šis žurnāls ir redzams gan kreditoram, gan sagādes profesionāļiem, kuriem ir pieeja piedāvājumam.
- Piedāvājuma norises gaitā sagādes profesionāļiem var skatīt tās statusu. Pēc tam statuss būs vai nu *Kreditors atjaunina* vai *Iesniedza kreditors*.
- Aizzīmogotā piedāvājumā ievietoto rindu statuss paliek *Nosūtīts*, līdz aizzīmogoti piedāvājumi tiek noņemti.
- Ja kreditors izvēlas noraidīt piedāvājumu, piedāvājumam būs statuss **Atbildes progress**, kuru *Kreditors ir noraidjis*. Šis statuss būs redzams sagādes personālam.
- Atbildes anketās **netiek** glabātas šifrētā datu bāzes formā. Tāpēc tie nav aizzīmogoti. Tomēr PP lietotāja interfeisā tās nebūs redzamas, līdz aizzīmogoti gadījumi tiek noņemti.

### <a name="all-sealed-bid-activities-are-logged"></a>Tiek reģistrētas visas aizzīmogotās piedāvājumu aktivitātes

Detalizēts žurnāls reģistrē visas lietotāja aktivitātes un darbības piedāvājumam. Darbību žurnāls iespējo organizācijas, lai noteiktu, kas atjaunināja piedāvājumu tā darbmūža laikā un kādi bija atjauninājumi. Tas arī ļauj organizācijām apstiprināt, ka tikai autorizēti cilvēki piekļūst aizzīmogotam piedāvājumam. Darbību žurnāls ir pieejams katra piedāvājuma lapā **Aktivitāte**.

### <a name="review-rfq-activity"></a>Pārskatīt PP aktivitāti

Tiek reģistrēta katra mijiedarbība ar piedāvājumu, un to var skatīt lapā **Aktivitāte**. Tālāk redzamajā attēlā parādīts piemērs.

![Lapas Aktivitātes piemērs](media/sealed-bidding-rfq-activity.png "Lapas Aktivitātes piemērs")

Kreditori var piekļūt lapai **Aktivitāte**, atlasot **Aktivitāte** lapā **Piedāvājuma pieprasījums aizzīmogotiem piedāvājumiem**. Sagādes personāls var tai piekļūt, atlasot **Aktivitāte** lapā **Piedāvājuma pieprasījums**. Darbību žurnāls nodrošina pilnu redzamību kreditoriem un sagādes personālam, kam ir piekļuve piedāvājumam. Tāpēc tas var atklāt jebkādu nesankcionētu piekļuvi.

### <a name="unseal-sealed-bids"></a>Noņemt aizzīmogotos piedāvājumus

Kad ir pagājusi aizzīmogotā piedāvājuma PP gadījumam konfigurētā vērtība **Beigu datums un laiks**, vairs nav pieejama poga **Atcelt aizzīmogošanu**. Atlasiet **Atcelt aizzīmogošanu**, lai atceltu visus aizzīmogotos piedāvājumus atlasītajam PP gadījumam. Visi piedāvājuma dati un pielikumi tad kļūst redzami, lai varētu pārvaldīt atbildes uz gadījumu. Turklāt tiek izveidoti žurnāli, kuros ir iesniegtie piedāvājuma dati.

Tiek reģistrēts katrs aizzīmogošanas noņemšanas notikums, un to var skatīt lapā **Aktivitāte**.

### <a name="process-accepted-bids"></a>Apstrādāt pieņemtos piedāvājumus

Iepriekš aizzīmogoto piedāvājumu salīdzināšanas un apstiprināšanas process ir tāds pats kā atvērto piedāvājumu process. Informāciju par to, kā atzīmēt, salīdzināt, noraidīt un pieņemt noņemtos aizzīmogotus piedāvājumus, skatiet šeit: [Ievadīt un salīdzināt PP piedāvājumus un piemaksas līgumus](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>PP darbību žurnālu nekad nevar dzēst

Neviens, pat ne administratori un Microsoft atbalsts, nevar rediģēt vai dzēst PP darbību žurnālu. Šis ierobežojums palīdz nodrošināt aizzīmogoto piedāvājumu procesu atbilstību. Tas arī palīdz nodrošināt precīzas revīzijas liecības uzturēšanu.
