---
title: Tehniskie atribūti un tehnisko atribūtu meklēšana
description: Šajā tēmā izskaidrots, kā varat izmantot tehniskos atribūtus, lai norādītu visas nestandarta īpašības, lai nodrošinātu, ka visi preču šablona dati var tikt reģistrēti sistēmā. Tas arī izskaidro, kā varat izmantot tehnisko atribūtu meklēšanu, lai viegli atrastu produktus, pamatojoties uz šīm reģistrētajām iezīmēm.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f8803e46ce6f104a5afee64faaf393a2df47a61
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568115"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Tehniskie atribūti un tehnisko atribūtu meklēšana

[!include [banner](../includes/banner.md)]

Lai nodrošinātu, ka visus produkta pamatdatus var reģistrēt sistēmā, izmantojiet tehniskos atribūtus, lai norādītu visus nestandarta raksturlielumus. Pēc tam varat izmantot tehnisko atribūtu meklēšanu, lai viegli atrastu produktus, pamatojoties uz šīm reģistrētajām iezīmēm.

## <a name="create-engineering-attributes-and-attribute-types"></a>Izveidot tehniskos atribūtus un atribūtu veidus

Parasti tehniskiem produktiem ir daudz parametru un rekvizītu, kas ir jāaptver. Lai gan dažus rekvizītus varat reģistrēt, izmantojot standarta produktu laukus, pēc nepieciešamības varat izveidot arī jaunus tehniskos rekvizītus. Varat definēt savus *tehniskos atribūtus* un padarīt tos par daļu no produkta definīcijas.

Katram tehniskajam atribūtam ir jāpieder *atribūta veidam*. Šī prasība pastāv, jo katram tehniskajam atribūtam ir jābūt *datu veidam*, kas nosaka vērtību veidus, kurus tas var saturēt. Inženierijas atribūta veids var būt standarta veids (piemēram, brīvais teksts, vesels skaitlis vai decimāls) vai pielāgots veids (piemēram, teksts, kam ir noteikta vērtību kopa, no kuras atlasīt). Varat atkārtoti izmantot katru atribūta veidu ar jebkādu skaitu tehnisko atribūtu.

### <a name="set-up-engineering-attribute-types"></a>Iestatīt tehnisko atribūtu veidus

Lai skatītu, izveidotu vai rediģētu tehnisko atribūta veidu, rīkojieties šādi.

1. Dodieties uz **Tehniskā izmaiņu pārvaldība \> Iestatīšana \> Atribūti \> Atribūtu veidi**.
1. Atlasiet esošu atribūta veidu saraksta rūtī vai atlasiet **Jauns** darbības rūtī, lai izveidotu jaunu atribūta veidu.
1. Iestatiet tālāk minētos laukus:

    - **Atribūta veida nosaukums** - ievadiet atribūta veida nosaukumu.
    - **Veids** — Atlasiet standarta datu veidu (*Valūta*, *Datums un laiks*, *Decimāls*, *Vesels skaitlis*, *Teksts*, *Būla* vai *Atsauce*).
    - **Fiksēts saraksts** — Šī opcija ir pieejama tikai tad, ja lauks **Veids** ir iestatīts uz *Teksts*. Iestatiet to uz *Jā*, lai definētu konkrētas vērtības šī veida atribūtiem. Šādā gadījumā tiks izveidots nolaižamais saraksts. Izmantojiet kopsavilkuma cilni **Vērtība**, lai noteiktu vērtības, kas ir pieejamas šim atribūta veidam. Iestatiet šo opciju uz *Nē*, lai ļautu lietotājiem ievadīt jebkuru vērtību. Šādā gadījumā tiks izveidots ievades lauks.
    - **Vērtību diapazons** — Šī opcija ir pieejama tikai tad, ja lauks **Veids** ir iestatīts kā *Vesels skaitlis*, *Decimāls* vai *Valūta*. Iestatiet to uz *Jā*, lai noteiktu minimālās un maksimālās vērtības, kas tiks pieņemtas šī veida atribūtiem. Lietojiet kopsavilkuma cilni **Diapazons**, lai noteiktu minimālās un maksimālās vērtības un (valūtai) valūtu, kas tiek piemērota ievadītajiem ierobežojumiem. Iestatiet šo opciju uz *Nē*, lai akceptētu jebkuru vērtību. 
    - **Mērvienība** - Šis lauks ir pieejams tikai tad, ja lauks **Veids** ir iestatīts kā *Vesels skaitlis* vai *Decimāls*. Atlasiet mērvienību, kas attiecas uz šo atribūta veidu. Ja nav nepieciešama vienība, atstājiet šo lauku tukšu.

### <a name="set-up-engineering-attributes"></a>Iestatīt tehniskos atribūtus

Lai skatītu, izveidotu vai rediģētu tehnisko atribūtu, rīkojieties šādi.

1. Dodieties uz **Tehniskā izmaiņu pārvaldība \> Iestatīšana \> Atribūti \> Tehniskie atribūti**.
1. Atlasiet esošu atribūtu saraksta rūtī vai atlasiet **Jauns** darbības rūtī, lai izveidotu jaunu atribūtu.
1. Iestatiet tālāk minētos laukus:

    - **Nosaukums** – ievadiet atribūta nosaukumu. Šis nosaukums tiek rādīts tikai lapā **Tehniskie atribūti**. Visur citur sistēmā lauka **Vārds un uzvārds** vērtība parasti tiek rādīta, lai identificētu atribūtu.
    - **Atribūta veids** — Atlasiet atribūta veidu, kas definēts iepriekšējā sadaļā.
    - **Vārds un uzvārds** — Ievadiet nosaukumu, kas identificēs atribūtu sistēmā (izņemot lapā **Tehniskie atribūti** ). 
    - **Apraksts** — ievadiet atribūta aprakstu.
    - **Palīdzības teksts** — Ievadiet palīdzības tekstu, kas citiem lietotājiem norāda, kam šis atribūts ir paredzēts.
    - **Noklusētā vērtība** — Ievadiet atribūtam noklusēto vērtību. Piedāvātās opcijas ir atkarīgas no atlasītā atribūta veida.
    - **Valūta** – Ja izvēlētais atribūta veids ir valūta, atlasiet valūtu, ko atribūts akceptēs, un parādiet vērtības elementā.

1. Ja izvēlētais atribūta veids ir vesels skaitlis vai decimāls, tiek rādīta kopsavilkuma cilne **Diapazons**. Šajā kopsavilkuma cilnē, pēc nepieciešamības iestatiet šādus laukus:

    - **Tolerances darbība** — Atlasiet, kā sistēmai jāreaģē, ja lietotājs ievada vērtību, kas atrodas ārpus norādītā diapazona. Ja atlasāt *Brīdinājums*, tiek parādīts brīdinājums, bet lietotājs var saglabāt vērtību. Ja atlasāt *Nav atļauts*, tiek parādīts brīdinājums, un vērtību nevar saglabāt, kamēr lietotājs to nelabo.
    - **Minimums** — Ievadiet minimālo ieteicamo vai akceptēto vērtību.
    - **Maksimums** — Ievadiet maksimālo ieteicamo vai akceptēto vērtību.

### <a name="engineering-attribute-inheritance"></a>Inženiertehniskā atribūta pārmantošana

Preču struktūrām, piemēram, pavadzīmēm (BOM) vai formulām, var nodot noteiktus atribūtus no pakārtotajiem elementiem uz vecākelementiem. Par šo procesu varat domāt kā par "apgriezto pārmantošanu".

#### <a name="turn-on-this-feature-for-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja jūsu sistēma jau neietver Šajā sadaļā aprakstītos līdzekļus, dodieties uz [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Uzlabota atribūta pārmantošana Engineering Change Management*.

#### <a name="attribute-inheritance-example"></a>Atribūta pārmantošanas piemērs

Pārtikas produktam, piemēram, burkānkūkai, sistēmai ir jāreģistrē katrs alergēns, kuru satur produkts. Burkānkūku sistēmā nevar modelēt kā inženiertehnisko produktu ar formulu. Šī formula satur burkānkūkas sastāvdaļas, piemēram, miltus, pienu, burkānus un riekstus. Šajā piemērā uzņēmums sniedz divus burkānkūkas modeļus: vienu ar laktozi un vienu bez laktozes.

Kūkai ar laktozi sastāvdaļu līmenī ir šādi ingredienti:

- Sastāvdaļa "milti": atribūts "glutēns" = jā
- Sastāvdaļa "piens": atribūts "laktoze" = jā
- Sastāvdaļa "rieksti": atribūts "rieksti" = jā

Kūkā bez laktozes tiek izmantots bezlaktozes piens, un tai sastāvdaļu līmenī ir šādi atribūti:

- Sastāvdaļa "milti": atribūts "glutēns" = jā
- Sastāvdaļa "piens": atribūts "laktoze" = nē
- Sastāvdaļa "rieksti": atribūts "rieksti" = jā

Tā kā šie produkti pārsvarā ir līdzīgi, varētu būt parocīgi šos atribūtus padot no pakārtotā produkta (abas variācijas) uz vecākproduktu (pamata burkānkūka). Lai ieviestu šo "apgriezto pārmantošanu", varat lietot funkciju *Atribūta pārmantošana*. Šī funkcija tiek definēta katrai [inženiertehniskajai versijai](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Piesaistiet tehniskos atribūtus tehnisko produktu kategorijai

Daži tehniskie atribūti attiecas uz visiem produktiem, turpretī citi ir raksturīgi atsevišķiem produktiem vai produktu kategorijām. Piemēram, elektriskie atribūti nav nepieciešami mehāniskajiem produktiem. Tāpēc varat iestatīt *tehnisko produktu kategorijas*. Tehnisko produktu kategorija nosaka tehnisko atribūtu kolekciju, kam jābūt daļai no definīcijas produktiem, kas pieder šai kategorijai. Varat arī norādīt, kuri tehniskie atribūti ir obligāti un vai ir noklusētā vērtība.

Papildinformāciju par to, kā strādāt ar tehnisko produktu kategorijām, tostarp informāciju par to, kā pievienot atribūtus kategorijām, skatiet [Tehniskās versijas un tehnisko produktu kategorijas](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Atribūta vērtību iestatīšana inženiertehniskajiem atribūtiem

Tehniskie atribūti, kas ir pievienoti tehnisko produktu kategorijai, tiek parādīti, kad izveidojat jaunu tehnisko produktu, kas ir balstīts uz šo kategoriju. Tajā laikā varat iestatīt atribūtu vērtības. Vēlāk šīs vērtības var mainīt lapā **Tehniskās versijas** vai kā daļu no tehnisko izmaiņu pārvaldības tehnisko izmaiņu pasūtījumā. Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Izveidot tehnisko produktu

Lai izveidotu tehnisko produktu, atveriet lapu **Izlaistie produkti**. Pēc tam darbību rūts grupas **Jauns** cilnē **Produkts** atlasiet **Tehniskais produkts**.

Jānorāda tehniskā kategorija, kurai pieder šis produkts. Kategorija noteiks visas produkta noklusētās vērtības un īpašības. Tas arī iestatīs atribūtus, kas attiecas uz produktu. Pēc kategorijas atlasīšanas, vērtības tiks iestatītas atribūtiem. Pēc tam šīs vērtības var modificēt.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Meklēt produktus, izmantojot tehnisko atribūtu vērtības

Varat izmantot tehnisko atribūtu meklēšanu, lai atrastu produktus, meklējot to tehnisko atribūtu vērtības. Tādēļ viegli varat atrast tehniskos produktus, pamatojoties uz to īpašībām. Varat meklēt produktus, kas pieder tehnisko produktu kategorijai, vai arī varat meklēt visos tehniskos produktos.

Meklēšana ir pieejama preces šablona datu lapās un no transakciju krājumiem sistēmā, piemēram, pārdošanas pasūtījumos. Lai meklētu produktu, varat izmantot lapu **Tehnisko atribūtu meklēšana**. Pēc tam varat izmantot pogu **Pievienot kā jaunu rindu**, lai pievienotu produktu pārdošanas pasūtījuma rindām. Produktus meklēšanas rezultātos var arī pievienot tieši pasūtījumam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
