---
title: Konteineru iepakošana nosūtīšanai
description: Šajā rakstā ir aprakstīts iepakošanas process, kas ļauj validēt krājuma krājumus un iepakot tos konteineros.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708788"
---
# <a name="pack-containers-for-shipment"></a>Konteineru iepakošana nosūtīšanai

[!include [banner](../../includes/banner.md)]

Konteinera iepakošanas process ļauj validēt krājuma krājumus un iepakot tos konteineros. Šī procesa laikā noliktavas darbinieki parasti saņem krājumu vienības no lielapjoma glabāšanas zonām un pārvieto tos uz iepakošanas zonu. Pastāv vairāki noliktavas darbinieki, kas pārbauda krājumu daudzumus un tipus, un piešķiriet tos atbilstošajiem konteinera izmēriem. Kad konteiners ir pilnībā iepakots, tas tiek slēgts un pārvietots uz nosūtīšanas doka apgabalu, kur tas ir sagatavots nosūtīšanai.

Konteineri parāda fiziskas struktūras, kurās krājumi ir iepakoti, un sistēmā var izsekot konteinera informāciju. Šī informācija var būt noderīga transportēšanas plānošanas laikā, it īpaši, ja aprēķiniet nosūtīšanas maksas, pamatojoties uz konteineriem. Pirms nosūtīšanas varat skatīt kravā izmantoto konteineru skaitu, izmantoto konteineru tipus un katra konteinera fiziskās dimensijas (piemēram, kopējo tilpumu un svaru).

Ar konteineriem var izmantot vairākas saistītas izejošās noliktavas iespējas. Papildinformāciju skatiet tālāk minētajos rakstos.

- [Kopuma konteinerinēšana](wave-containerization.md)
- [Izejošā kārtošana](outbound-sorting.md)
- [Mazu paku nosūtīšana](small-parcel-shipping.md)
- [Apstiprināt un pārsūtīt](confirm-and-transfer.md)
- [Iestatīt dažādas iepakošanas un glabāšanas dimensijas](packing-vs-storage-dimensions.md)
- [Iepakošanas darbs izejošo konteineru iepakošanai un sūtījumu apstrādei](packing-work.md)
- [Iepakošanas konteineri no noliktavas pārvaldības mobilās programmas](warehouse-app-packing-containers.md)
- [Piemēra scenārijs — iepakot konteinerus ar noliktavas pārvaldības mobilo programmu](warehouse-app-pack-containers-scenario.md)
- [Drukāt konteinera etiķetes](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Iestatīt noliktavu manuālas iepakošanas darbību lietošanai

Ir divi galvenie nosūtīšanas operāciju organizēšanas veidi:

- **Kopuma izveide un apstrāde** – darbinieki izņem krājumus, pamatojoties uz nosūtīšanas noliktavas darbu. Tad tās novietojiet krājumus tieši nosūtīšanas vietā, kur tie ir gatavi tūlītējai kravai. Papildinformāciju par to, kā iestatīt un izmantot šo procesu, skatiet sadaļā [Kopuma izveide un apstrāde](wave-processing.md).
- **Manuāla iepakošana iepakošanas stacijās – šim procesam ir papildu operācija starp izdošanas un nosūtīšanas** operācijām. Tā vietā, lai krājumus ievietotu *durvju durvju nosūtīšanas vietā*, darbinieki to ievieto iepakošanas *vietā*. Pēc tam viņi pārvalda iepakošanas procesu iepakošanas stacijā, izmantojot **Web** klientā lapu Paka. Lai iespējotu šo procesu, sistēmai jākonfigurē tā, kā aprakstīts šajā sadaļā.

### <a name="set-up-warehouse-locations-for-packing"></a>Iestatīt iepakošanas noliktavu vietas

Jums ir jābūt vismaz vienai iepakojuma vietai, kur darbinieki ievietos krājuma vienības tā, lai tos varētu iepakot konteineros. Papildinformāciju par to, kā izveidot noliktavas atrašanās [vietas, skatiet sadaļā Vietu konfigurēšana WMS iespējotā noliktavā](tasks\configure-locations-wms-enabled-warehouse.md). Tālāk minētās apakšsadaļas apraksta, kā izveidot un iestatīt iepakošanas vietas.

#### <a name="set-up-location-types-for-packing"></a>Iestatīt iepakošanas novietojuma veidus

Jums jādefinē iepakojuma *vietu* atrašanās vietas veids. Novietojuma tipus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus. Katra atrašanās vietas tipa nosaukums parasti apraksta kaut ko par to, kā šis vietas veids jāizmanto. Šeit iestatītais novietojuma tips ir jāsaista ar katru atrašanās vietu, kas tiek izmantota iepakošanas operācijām.

Izpildiet šīs darbības, lai iestatītu atrašanās vietas tipu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma veidi**.
1. Darbību rūtī atlasiet Jauns, lai **režģim** pievienotu atrašanās vietas veidu.
1. Iestatiet sekojošos laukus jaunajam atrašanās vietas tipam:

    - **Atrašanās** vietas tips - ievadiet atrašanās vietas tipa nosaukumu. Katram nosaukumam ir jābūt unikālam, un tam ir jāapraksta informācija par to, kā vietas veids ir paredzēts izmantošanai.
    - **Apraksts** – ievadiet īsu atrašanās vietas tipa aprakstu.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Informēt sistēmu par iepakojuma novietojuma veidu

Pēc atrašanās vietas tipa izveides, jāiestata sistēma, lai to atpazītu kā vietas veidu, ko izmantot iepakošanas operācijām.

Izpildiet šīs darbības, lai iestatītu atrašanās vietas tipu, kas tiek izmantots iepakošanas operācijām.

1. Pāriet uz noliktavas **pārvaldības iestatīšanas \> noliktavas \> pārvaldības parametriem**
2. Cilnes Vispārīgi **kopsavilkuma** cilnē **Atrašanās** vietas veidi iestatiet lauku Iepakojuma novietojuma veids uz atrašanās vietas veidu, **ko** izmantosit iepakošanas staciju identificēšanai.

> [!NOTE]
> Ja jaunināt Microsoft Dynamics AX no versijas, *statuss* Iepakojuma statuss ir noņemts no kravām un kravām, jo tas nedarbojas pastāvīgi un izraisīja liekus datus. Tādēļ ir **novecojušas lapas** **Kravās** un Kravās iepakošanas sarakstā. Konteineri, kas ir jāiepako, tiek izsekoti novietojuma līmenī.
>
> Iepriekšējās versijās jūs definējat **iepakošanas vietu, izmantojot iepakošanas novietojuma lauka profila ID** **·** **lapas** Noliktavas pārvaldības parametri cilnē Iepakojums, lai norādītu novietojuma *profilu.* Lai norādītu atrašanās vietas veidu, kā aprakstīts šajā rakstā, **·** **·** **·** *pašreizējā* versijā izmantojiet lauku Iepakojuma novietojuma veids lapas Noliktavas pārvaldības parametri cilnē Vispārīgi. Jaunais lauks ir labāk saskaņots ar procesu sagatavošanas vietu un galīgās nosūtīšanas vietu identificēšanai.
>
> Lai gan varat **turpināt izmantot veco profila ID** iepakošanas novietojuma laukam, **ieteicams** sākt lietot jauno iepakojuma novietojuma tipa lauku, jo vecais lauks tiks novecojis.
>
> Ja notīrāt vecā profila **ID iestatījumu iepakošanas novietojuma** laukam un pēc tam saglabājat lapu, lauks tiks neatgriezeniski atspējots. Instalācijām **, kur iepakošanas novietojuma** lauka profila ID nekad nav izmantots, tā vienmēr tiek deaktivizēta. Pēc iepakošanas vietas lauka **Profila ID** iestatīšanas izmantojiet šajā rakstā aprakstītos iestatījumus, lai iestatītu un identificētu iepakojuma vietu.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Iestatīt iepakošanas vietu novietojuma profilus

Katrs *atrašanās* vietas profils izveido informāciju un noteikumus, kas attiecas uz saistītajām vietām. Tā kā jums ir nepieciešams, lai iepakošanas darbības izmantotu vismaz vienā vietā, papildus atrašanās vietas tipam tam ir jāizveido atrašanās vietas profils. Katru profilu var izmantot jebkurš atrašanās vietu skaits. Lai izsekotu numura zīmes, ir jāiestata iepakošanai izmantotās vietas.

Izpildiet šīs darbības, lai iestatītu iepakošanas vietas novietojuma profilu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Atlasiet esošu profilu saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. Jaunā vai atlasītā profila virsrakstā iestatiet šādus laukus:

    - **Atrašanās vietas profila ID** - ievadiet unikālu profila ID.
    - **Nosaukums** – ievadiet profilam aprakstošu nosaukumu.

1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Atrašanās** vietas formāts – izvēlieties atrašanās vietas formātu, ko izmantot pašreizējai atrašanās vietai. Vietu formāti ir nosaukumdošanas sistēma, ko izmanto, lai izveidotu unikālus un saskanīgus nosaukumus dažādām noliktavā izmantotajām novietojuma nodalījuma pozīcijām. Ja jums vēl nav nepieciešamais formāts, varat to izveidot, **dodoties uz Noliktavas vadības iestatīšanas noliktavas \>\>\> novietojuma formātiem.** Lai iegūtu papildu informāciju, skatiet [Konfigurēt novietojumus WMS iespējotā noliktavā](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Novietojuma veids** – atlasiet atrašanās vietas veidu **, kas ir iestatīts kā iepakošanas vietas veids noliktavas pārvaldības parametru** lapā, kā aprakstīts iepriekš šajā rakstā.
    - **Izmantojiet numura zīmes izsekošanu** - iepakošanas vietām iestatiet šo opciju kā *Jā*. Sistēmai jābūt iespējai izsekot numura zīmi iepakošanas vietās, lai tā varētu kontrolēt iepakošanas procesu.
    - **Atļaut negatīvu krājumu** daudzumu - iepakojuma novietojumiem iestatiet šo opciju kā *Nē*.
    - **Atļaut jauktus** krājumus — iepakojuma novietojumiem iestatiet šo opciju kā *Jā*. Šis iestatījums ir nepieciešams, jo daudzi dažādi krājumu numuri parasti vienlaicīgi tiek piegādāti uz iepakojuma vietām.
    - **Atļaut jauktus krājumu statusus** — iepakojumu novietojumiem iestatiet šo opciju kā *Jā*. Šis iestatījums ir nepieciešams, jo krājumi ar atšķirīgiem krājumu statusiem parasti tiek vienlaicīgi piegādāti uz iepakojuma vietām.
    - **Atļaut jauktas krājumu partijas** — iepakojumu novietojumiem iestatiet šo opciju kā *Jā*. Šī opcija automātiski tiek iestatīta uz Jā, *kad* opcija **Atļaut jauktus** krājumus ir iestatīta uz *Jā*.

#### <a name="set-up-packing-locations"></a>Iestatīt iepakošanas vietas

Ir jābūt vismaz vienai vietai, kur *darbinieki* ievietos krājumu vienības, kas jāiepako konteineros.

Izpildiet šīs darbības, lai pievienotu iepakošanas vietu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** vietu.
1. Iestatiet sekojošos laukus jaunajai atrašanās vietai:

    - **Noliktava** – norādiet noliktavu, kurā jāpastāv iepakojuma vietai.
    - **Vieta** – ievadiet jaunās atrašanās vietas nosaukumu.
    - **Atrašanās vietas profila ID** - noteikti norādiet iepriekšējā sadaļā izveidoto ID.

## <a name="set-up-the-packing-process"></a>Iestatīt iepakošanas procesu

Šajā sadaļā ir aprakstīts, kā konfigurēt iestatījumus, kas iespējo iepakošanas procesu, un ļaut darbiniekiem iepako krājumus konteineros.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Konteineru iepakošanas politiku iestatīšana

Katra *konteinera iepakošanas* politika nosaka, kā jāapstrādā konteiners. Katru reizi, kad izveidojat jaunu konteineru, jūs atlasīsiet arī konteinera iepakojuma politiku, ko tam piemērot.

Lai iestatītu konteinera iepakošanas politiku, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru iepakošanas politikas**.
1. Atlasiet esošu politiku saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. Jaunās vai atlasītās politikas galvenē iestatiet tālāk norādītos laukus.

    - **Konteinera iepakošanas** politika - ievadiet unikālu politikas nosaukumu.
    - **Apraksts** – ievadiet politikas aprakstošo nosaukumu.

1. Cilnē Pārskats **iestatiet** šādus laukus. Šie lauki ļauj norādīt, kādas darbības jāveic, kad konteiners ir aizvērts, vai darboties ar vai bez darba izveides un kad konteiners jāatlaiž no iepakošanas stacijas.

    - **Noliktava** – atlasiet noliktavu, uz ko attiecas iepakojuma politika.
    - **Noklusējuma galīgā sūtījuma novietojums** — norādiet konteineram vēlamo atrašanās vietu pēc tā slēgšanas. Šis lauks ir pieejams tikai tad, ja konteinera **izlaišanas ierobežojuma** lauks ir iestatīts uz *Padarīt pieejamu beigu nosūtīšanas vietā*.
    - **Noklusējuma vieta kārtošanai —** šis lauks tiek izmantots ar [izejošās kārtošanas](outbound-sorting.md) iespēju.
    - **Svara vienība** — atlasiet noklusējuma mērvienību, ko izmantot, kad konteiners tiek aizvērts un manifestēts. Parasti šī mērvienība būs mērvienība, ko izmanto iepakošanas stacijas svari. Šis lauks attiecas uz politikām ar vai bez darba izveides.
    - **Konteinera slēgšanas politika** — atlasiet vienu no šīm opcijām, lai definētu, kas jānotiek, kad konteiners tiek slēgts:

        - *Automātiskā izlaide* – konteiners tiks uzskatīts par izlaistu no iepakošanas stacijas, **un tiks izraisīta darbība, kas norādīta konteinera** izlaišanas ierobežojuma laukā.
        - *Aizkavēta* izlaišana — konteiners netiks nekavējoties izlaists no iepakošanas stacijas. Noliktavas darbiniekam tā vēlāk ir manuāli jāizlaiž.
        - *Nav* obligāti – kamēr darbinieks slēdz konteineru, viņi var izvēlēties, vai konteiners ir jāatlaiž.

        Ja iepakošanas stacija apstrādā galvenokārt atsevišķus konteinerus, kas tiek nosūtīti tieši debitoriem, visizplatītākā pieeja ir nekavējoties izlaist konteinerus. Ja iepakošanas stacija apstrādā sūtījumus, kas sastāv no vairākiem konteineriem vai pat paletēm, ieteicams atlikt izlaišanu, līdz viss sūtījums vai palete ir iepakota un gatava savākšanai.

    - **Konteinera atbrīvošanas politika** — atlasiet vienu no šīm opcijām, lai definētu, kas jānotiek, kad konteiners tiek izlaists no iepakošanas vietas:

        - *Padarīt pieejamu beigu nosūtīšanas vietā* - atjauniniet konteineru līdz galīgās nosūtīšanas vietai. Ja atlasāt šo opciju, izmantojiet **noklusējuma** galīgā sūtījuma lauka novietojumu, lai norādītu vēlamo konteinera atrašanās vietu pēc tā slēgšanas.
        - *Izveidot darbu konteinera pārvietošanai* no iepakošanas stacijas — izveidojiet darbu konteinera pārvietošanai no iepakošanas stacijas uz sagatavošanas zonu vai tieši uz iepakošanas stacijām. Izmantojiet lauku **Darba veidne**, lai norādītu darba veidni, kas ir jāizmanto, veidojot darbu konteineram.
        - *Piešķirt konteineru izejošai kārtošanas pozīcijai* – šī opcija tiek izmantota ar [nosūtīšanas kārtošanas](outbound-sorting.md) iespēju.

        Vairumā gadījumu ieteicams izveidot darbu konteineru pārvietošanai, jo šī pieeja labāk parāda faktiskos manuālos procesus noliktavā. Tomēr vienkāršiem scenārijiem vai situācijām, kad iepakošanas stacija atrodas tieši durvju zonā, varētu būt ieteicams, lai konteiners būtu nekavējoties pieejams galīgā nosūtīšanas vietā.

    - **Darba veidne** — atlasiet darba veidni, kas jālieto, konteineram veidojot darbu. Šis lauks ir **pieejams** *tikai* tad, kad konteinera izlaišanas ierobežojuma lauks ir iestatīts uz Izveidot darbu konteinera pārvietošanai no iepakošanas stacijas un saistībā ar darba pasūtījuma *veidu ar nosaukumu Iepakotā konteinera izdošana.* Papildinformāciju skatiet darba veidnēs [un novietojuma direktīvās](control-warehouse-location-directives.md).

    Atlikušajos soļos jūs konfigurēsiet iestatījumus, kas ir saistīti ar *manifestēšanu*. Manifests ir konteinera, konteineru grupas vai sūtījuma svara norādīšanas process kopā ar izsekošanas ID, kas ir saņemts no transportēšanas nodrošinātāja. Dynamics 365 Supply Chain Management nav integrēts ar ārējā transportēšanas nodrošinātāju sistēmām. Tā vietā noliktavas darbiniekiem ir jādrukā etiķetes, kas ir saņemtas no transportēšanas nodrošinātāja, un pēc tam skenējiet izsekošanas numuru, kad tie pabeidz manifesta procedūru.

    Tā kā manifesta prasības atšķiras no debitora uz debitoru un pat no nosūtīšanas uz nosūtīšanu, iepakošanas politika darbplūsmā ļauj būtiski elastīgi. Varat iestatīt konteineru, konteineru grupu un sūtījumu manifestus jebkurā kombinācijā.

    Ja izmantojat vairāku līmeņu manifesta procedūru, darbiniekiem ir jā manifestā visi konteineri, pirms tie manifestā ir saistīta konteineru grupa, un viņiem ir jā manifestā visas konteineru grupas, pirms tie manifestē saistīto sūtījumu.

1. Kopsavilkuma cilnē **Konteinera manifests** iestatiet šādus laukus:

    - **Automātisks manifests konteinera** slēgšanas laikā – iestatiet šo opciju *uz Jā*, lai lietotu manifesta informāciju kā daļu no konteinera slēgšanas procesa. Ja neizmantojat transportēšanas integrāciju, informācija ir jāieraksta manuāli.
    - **Konteinera manifesta prasības** — atlasiet vienu no šīm opcijām:

        - *Neviens* – netiks izmantots manifestēšanas process.
        - *Manuāla* – manifestēšana tiks pieprasīta, izmantojot iepakošanas darbplūsmu. Sistēma neļaus slēgt vai izlaist konteineru, kamēr manifestēšana nav pabeigta.
        - *Transportēšanas* pārvaldība — manifestēšana tiks veikta, izmantojot transportēšanas pārvaldības (TMS) likmes programmas. Tā kā šai opcijai ir nepieciešama pielāgotā izstrāde, lai ieviestu konkrētu programmu transportēšanas nodrošinātājam, tā nestrādās ārpus pašreizējās versijas rūtiņas.

    - **Drukāt konteinera saturu** – iestatiet šo opciju kā Jā *,* lai automātiski drukātu konteinera satura pārskatu, kad konteiners ir reģistrēts kā slēgts. Pārskatu var drukāt arī pēc pieprasījuma.

1. Kopsavilkuma cilnes **Konteineru grupa manifesta** laukā **Konteineru grupas manifesta** prasības atlasiet vienu no šīm opcijām:

    - *Neviens* — konteineru grupas manifests netiks ietverts kā prasība iepakošanas darbplūsmā.
    - *Manuāli* – konteineru grupas manifests tiks ietverts kā prasība iepakošanas darbplūsmā. Lai grupu varētu ietvert manifestā, ir jāaizver visi grupā ietvertie konteineri. Atlasiet šo opciju, ja jums ir jāaizpilda manifests katrai konteineru grupai, kas ir iepakota iepakošanas stacijā. Parasti šī opcija tiek atlasīta, ja konteineri ir iepakoti uz paletes un visa palete tiek manifestā.

    > [!NOTE]
    > Pašreizējā versija neatbalsta konteineru grupu manifesta pārskatus, un konteineru grupām nav TMS programmas atbalsta.

1. Kopsavilkuma cilnē **Kravas manifests** iestatiet šādus laukus:

    - **Sūtījuma manifesta prasības** – atlasiet vienu no šīm opcijām:

        - *Neviens* - sūtījuma manifests netiks ietverts kā prasība iepakošanas darbplūsmā.
        - *Manuāli* – sūtījuma manifests tiks iekļauts kā prasība iepakošanas darbplūsmā. Kamēr manifests nav pabeigts, nevar izlaist nekādus sūtījuma konteinerus.
        - *Transportēšanas* pārvaldība — manifestēšana tiks veikta, izmantojot TMS likmju programmas. Tā kā šai opcijai ir nepieciešama pielāgotā izstrāde, lai ieviestu konkrētu programmu transportēšanas nodrošinātājam, tā nestrādās ārpus pašreizējās versijas rūtiņas.

        Ja ir jāaizpilda visa sūtījuma manifests, kas iepakots iepakošanas stacijā, ir jāiespējo sūtījuma manifests. Parasti to izmanto, kad ir nepieciešams viens konsolidēts manifests, pat ja sūtījums sastāv no vairākiem konteineriem vai konteineru grupām.

    - **Drukāt pavadzīmi** – iestatiet šo opciju kā *Jā*, lai automātiski drukātu pavadzīmi kā daļu no sūtījuma manifesta. Pavadzīmi var drukāt arī pēc pieprasījuma.

### <a name="set-up-container-types"></a>Konteinera veidu iestatīšana

Manuāla iepakošanas procesa laikā konteineri jāizveido pirms krājumus var iepakot tajā. Katram konteineram ir jābūt balstītam uz *konteinera* veidu, kas nosaka konteinera maksimālo fizisko tilpumu un svara noslodzi.

Izpildiet šīs darbības, lai izveidotu konteinera veidu.

1. Pārejiet uz **noliktavas pārvaldības \> iestatīšanas \> konteineru \> konteinera tipiem**.
1. Lai pievienotu konteinera veidu, darbību **rūtī** atlasiet Jauns.
1. Iestatiet tālāk norādītos laukus jaunajam konteinera veidam:

    - **Konteinera veida kods** - ievadiet unikālu konteinera veida ID.
    - **Apraksts** — ievadiet jaunā konteinera veida aprakstu.
    - **Taras svars** – ievadiet konteinera faktisko vai novērtēto svaru.
    - **Maksimālais neto svars** – ievadiet maksimālo svaru, ko konteinerā var uzglabāt.

1. Sadaļas **Konteinera dimensijas** laukos **Garums**, **Platums**,**·** **Augstums** un Tilpums ievadiet pašam konteinera fiziskās dimensijas.
1. Sadaļā Maksimums **laukos Garums,** Platums **,** **·** **Augstums** **un Tilpums ievadiet maksimālās fiziskās dimensijas**, kuras konteiners var apstrādāt.
1. Varat definēt papildu atribūtus konteineru tipiem, kas ir saistīti ar citām operācijām, kas izmanto konteinerus. Papildinformāciju skatiet sadaļā [Konteinerizēšana](wave-containerization.md).

> [!NOTE]
> Manuāla iepakošanas procesa ietvaros **sistēma** **izmanto** tikai lauka Maksimālais neto svars vērtību un lauka Tilpums **vērtību sadaļā** Maksimums.

### <a name="set-up-packing-profiles"></a>Iepakošanas profilu iestatīšana

*Iepakošanas* procesam ir nepieciešami iepakošanas profili. Tos var atlasīt vai iestatīt pēc noklusējuma, kad lapā Pakotne sākat iepakošanas **darbību**.

Lai iestatītu iepakošanas profilu, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Iepakošanas profili**.
1. Atlasiet esošu profilu saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. Jaunā vai atlasītā profila virsrakstā iestatiet šādus laukus:

    - **Iepakošanas profila ID** - ievadiet īsu profila ID.
    - **Apraksts** – ievadiet iepakošanas profila aprakstu.
    - **Konteinera iepakošanas** politika — atlasiet iepakojuma ierobežojumu, kas attiecas uz profilu. Papildinformāciju skatiet šī [raksta sadaļā Iestatīt konteinera](#packing-policy) iepakošanas politikas.
    - **Konteinera ID režīms** — atlasiet, vai konteinera ID jāizveido automātiski, veidojot konteineru, vai tas ir jāizveido manuāli.
    - **Konteinera veids** — atlasiet konteinera veidu, kas tiek izmantots pēc noklusējuma, izveidojot jaunu konteineru.
    - **Slēdzot konteineru**, automātiski izveidot konteineru — atzīmējiet šo izvēles rūtiņu, lai automātiski izveidotu jaunu konteineru, ja iepriekšējais konteiners ir slēgts, un pašreizējā sūtījumā joprojām ir viena vai vairākas rindas.

### <a name="set-up-warehouse-workers"></a>Iestatīt noliktavas darbiniekus

Katram lietotājam vai darbiniekam, kas iepako **konteinerus** *·*, izmantojot tīmekļa klienta lapu Pakot, vai iepakošanas darbības kodam mobilajā programmā Noliktavas *pārvaldība ir nepieciešams lietotāja konts, kas ir saistīts ar darbinieka/* personas ierakstu, kuram ir piešķirtas nepieciešamās drošības piekļuves tiesības. (Papildinformāciju par to, kā iestatīt lietotājus, skatiet [Izveidot jaunus lietotājus](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Ievērojiet šos soļus, lai *iepakošanas procesam* iestatītu darbinieka/personas ierakstu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** darba lietotāju.
1. Iestatiet darbinieka **lauku** esošajam darbinieka ierakstam, kas ir definēts **personāla** vadības modulī lietotājam, kurš pabeigs iepakošanas procesu.
1. Kopsavilkuma cilnē **Profils** iestatiet tālāk minētos laukus:

    - **Konteinera iepakošanas politika** - atlasiet konteinera iepakojuma politiku, kas nosaka, kā jāapstrādā konteineri iepakošanas stacijā. Atlasītā konteinera iepakošanas politika tiks iepriekš atlasīta darbiniekam, kad tas atvērs iepakošanas staciju. Papildinformāciju skatiet šādā grāmatošanas sadaļā: Uzlabota [iepakošanas funkcionalitāte](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Iepakošanas profila ID** — atlasiet iepakošanas profila ID, kas nosaka iepakošanas ierobežojumu un iestatījumus, kuri ir jāizmanto. Ja atlasītais iepakošanas profila ID ir saistīts ar konteinera iepakošanas politiku, **nevarēsit mainīt konteinera iepakojuma politikas** lauka iestatījumu šajā lapā.

1. Kopsavilkuma cilnē **Noklusējuma iepakošanas** stacija atlasiet noklusējuma vietu, noliktavu un atrašanās vietu, kas attiecas uz darbinieku.
1. Ja darbinieks izmantos mobilo programmu Noliktavas pārvaldība, lai pārvaldītu un reģistrētu savu konteinera iepakošanas darbu, **kopsavilkuma** cilnē Lietotāji iestatiet vienu vai vairākus kontus, kurus darbinieks var izmantot, lai pieteiktos programmā. Papildinformāciju skatiet mobilās [ierīces lietotāju kontos](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Piemēra situācija

Šajā sadaļā sniegts piemēra scenārijs, kurā parādīts, kā izveidot pasūtījumu un iepakot krājumus.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/fin-ops/get-started/demo-data.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Šo scenāriju var izmantot arī kā ieteikumus par iespējas izmantošanu ražošanas sistēmā. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības katram iestatījumam, kas šeit aprakstīts.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Pieteikties kā lietotājs, kas var veikt iepakošanas darbu

Piesakieties Piegādes ķēžu pārvaldībā, izmantojot lietotāja kontu, kam ir atļauja iepakot konteinerus. *Lietotājs Sia Funderburk* ir iekļauts kā daļa no demonstrācijas datiem un tam ir nepieciešamās atļaujas. Šim lietotājam ir lietotāja ID *administrators*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Izveidot pārdošanas pasūtījumu un pabeigt darbu

Sekojiet šiem soļiem, lai izveidotu pārdošanas pasūtījumu un pabeigtu darbu pasūtīto krājumu pārvietošanai uz iepakošanas staciju.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet *US-005*.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts un ietver vienu, tukšu rindu kopsavilkuma **cilnē Pārdošanas pasūtījuma** rindas. Iestatiet šādas vērtības jaunajai pasūtījuma rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *2*
    - **Vieta:** *6*
    - **Noliktava:** *62*

1. Kamēr joprojām ir atlasīta pasūtījuma rinda, kopsavilkuma **\> cilnes** Pārdošanas pasūtījuma rindas rīkjoslā **atlasiet Krājumu** rezervēšana.
1. Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Ziņojumā ir norādīts pasūtījuma nosūtīšanas un kopuma KODS.

1. Kamēr joprojām ir atlasīta pasūtījuma rinda, kopsavilkuma **cilnes** \> **·** **Pārdošanas pasūtījuma rindas rīkjoslā atlasiet Detalizēta informācija par noliktavas** darbu. Ja kopumu palaišanai izmantojat pakešveida apstrādi, iespējams, darbs būs jāizveido īsu laiku.
1. **Darba lapas** Darbību rūts cilnē Darbs **atlasiet** Pabeigts **darbs**.
1. Darba pabeigšanas **lapā** iestatiet lietotāja ID **lauku** uz *62*.
1. Darbību rūtī atlasiet Apstiprināt **darbu**.
1. Kad saņemat ziņojumu, kas norāda, ka jūsu darbs ir derīgs, atlasiet Pabeigt darbu, **lai** pabeigtu noliktavas krājumu izdošanas procesu un ievietotu tos *Pakotnes* novietojumā.
1. Atzīmējiet kravas **ID** vērtību, kas rādīts darbam augšējā režģī.

### <a name="pack-the-ordered-items-into-a-container"></a>Iepakot pasūtītos krājumus konteinerā

Noliktavas krājumi tagad ir nonākuši iepakojuma zonā un ir gatavi iepakošanai konteineros. Veiciet šīs darbības, lai sistēmā izveidotu jaunu konteineru un to iepakotu.

1. Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Iepakot**.
1. Dialoglodziņā **Atlasīt iepakošanas vietu** iestatiet sekojošas vērtības:

    - **Vieta:** *6*
    - **Noliktava:** *62*
    - **Atrašanās vieta:** *Pakotne*
    - **Iepakošanas profila ID:** *WH62*

1. Atlasiet **Labi**.
1. Pakotnes lapā **,** laukā Numura **zīme vai krava** ievadiet sūtījuma ID, ko iepriekš atzīmējāt. Tagad kopsavilkuma cilnē Atvērtās rindas jums ir jāseko atlikušajām **neatpakotajām** precēm.
1. Darbību rūtī atlasiet Jauns **konteiners**, lai sistēmā izveidotu konteineru.
1. **Jaunā konteinera dialoglodziņa ID laukam** Konteinera veids **iestatiet** *vērtību SmallBox.*
1. Atlasiet **Labi,** lai izveidotu konteineru.
1. Atlasiet **Labi,** lai atgrieztos uz **pakotnes** lapu. Pašlaik **atvērtajā** konteineru kopsavilkuma cilnē tiek **rādīta izveidotā konteinera ID** vērtība.
1. Šajā scenārijā jūs iepakosiet tikai vienu no pasūtītajām vienībām tūlīt. Tādēļ kopsavilkuma cilnē **Krājuma iepakojums** iestatiet šādas vērtības:

    - **Daudzums:** *1.00*
    - **Identifikators:** *A0001*

    Uzreiz pēc Identifikatora **vērtības** atlases lapa atjaunina kopsavilkuma cilnes Atvērt rindas un Visas rindas, **·** **lai** norādītu, ka viena prece ir iepakota. Tagad vajadzētu būt iepakotam vienam no diviem krājuma *A0001 gabaliem*.

1. Darbību rūtī atlasiet **Slēgt konteineru**.
1. Dialoglodziņā Slēgt **konteineru** atlasiet Iegūt sistēmas svaru **, lai** aizpildītu noklusēto **bruto svara** vērtību.
1. Atlasiet **Labi,** lai slēgtu konteineru.

> [!TIP]
> Ir dažādi veidi, kā skatīt konteinerus atbilstoši kontekstam. Piemēram, iepakojot sūtījumu, bieži ir noderīgi skatīt konteinerus, kas ir daļa no kravas, vai visus konteinerus, kas fiziski atrodas iepakošanas stacijā. Lapā **Iepakošanas** stacija ir pogas, ko varat izmantot, lai skatītu visus iepakošanas stacijā atvērtos un slēgtos konteinerus. Šie skati nav ierobežoti noteiktai kravai. Tie var būt ļoti noderīgi gadījumos, kad viens darbinieks iepako konteineru un cits darbinieks manifestē un izlaiž konteineru.
>
> Ir pieejams arī visu konteineru konsolidēts skats. Šis skats noder lielākā daļa lietotāju, kas strādā ārpus vienas iepakošanas stacijas konteksta. Lai to skatītu, dodieties uz sadaļu **Noliktavas pārvaldības \> iepakošanas un konteinerizēšanas konteineri \>**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
