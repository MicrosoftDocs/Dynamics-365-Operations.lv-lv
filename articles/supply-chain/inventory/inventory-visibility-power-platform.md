---
title: Krājumu redzamības programma
description: Šajā rakstā ir aprakstīts, kā izmantot programmu Krājumu redzamība.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9886ddbf0b072283cffd73d4bfdc20835ccb3b7c
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762705"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility programmas lietošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izmantot programmu Krājumu redzamība.

Krājumu redzamība nodrošina modeļa vadītas programmas vizualizēšanu. Programmā ir trīs lapas: **Konfigurācija**, **Operāciju redzamība** un **Krājumu kopsavilkums**. Tam ir tālāk minētās vērtības:

- Tā nodrošina lietotāja interfeisu (UI) rīcībā esošo konfigurāciju un vieglās rezervēšanas konfigurāciju.
- Tas atbalsta reāllaika rīcībā esošo krājumu vaicājumus par dažādām dimensiju kombinācijām.
- Tas sniedz UI rezervāciju pieprasījumu grāmatošanai.
- Tas sniedz pārskatu par rīcībā esošajiem produktu krājumiem kopā ar visām dimensijām.
- Tas nodrošina rīcībā esošo preču krājumu saraksta skatu kopā ar iepriekš definētiem izmēriem. Rīcībā esošais saraksta skats var būt vai nu pilns kopsavilkums, vai iepriekš ielādēts rīcībā esoša vaicājuma rezultāts.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat darbu, uzinstalējiet un iestatiet Inventory Visibility pievienojumprogrammu, kā aprakstīts rakstā [Inventory Visibility instalēšana un iestatīšana](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a> Atveriet un autentificējiet programmu Krājumu redzamība

Lai atvērtu un autentificētu programmu Krājumu redzamība, veiciet tālāk norādītās darbības.

1. Piesakieties savā Power Apps vidē.
1. **Atveriet programmu Krājumu redzamība**.
1. **Atveriet lapu Darbības redzamība** no kreisās rūts.
1. **Atlasiet pogu Iestatījumi** (zobrata simbols) lapas augšdaļā.
1. Dialoglodziņā **Iestatījumi** ievadiet vērtības Klienta ID, nomnieka ID **un** Klienta noslēpums **,** **kuras atzīmējāt, instalējot** un [iestatot krājumu redzamību](inventory-visibility-setup.md).
1. **Atlasiet pogu Atsvaidzināt** blakus **laukam Bearer Token**. Sistēma ģenerē jaunu uzrādītāja marķieri, pamatojoties uz jūsu ievadīto informāciju.

    ![Rīcībā esošo vaicājumu iestatījumi.](media/inventory-visibility-query-settings.png "Rīcībā esošie vaicājumu iestatījumi")

1. Kad saņemat derīgu uzrādītāja marķieri, aizveriet dialoglodziņu. Uzrādītāja žetona derīguma termiņš beigsies pēc kāda laika. Tāpēc laiku pa laikam tas ir jāatsvaidzina, kad ir jāatjaunina konfigurācija, jāpublicē dati vai jāvaicā dati.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a> Konfigurējiet programmu Krājumu redzamība

Programmas **Krājumu redzamība lapa Konfigurācija** palīdz iestatīt vispārīgo datu pārvaldības konfigurāciju un līdzekļu konfigurāciju. Pēc lietojumprogrammas pievienošanas noklusējuma konfigurācija ietver Microsoft Dynamics 365 Supply Chain Management (`fno` datu avots) noklusējuma iestatījumu. Varat pārskatīt noklusēto iestatījumu. Pēc tam, pamatojoties uz jūsu uzņēmuma prasībām un ārējās sistēmas krājumu grāmatošanas prasībām, varat modificēt konfigurāciju, lai standartizētu veidu, kā krājumu izmaiņas var grāmatot, organizēt un vaicāt vairākās sistēmās.

Visu informāciju par to, kā konfigurēt risinājumu, skatiet sadaļā [Inventory Visibility konfigurēšana](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Darbības redzamība

Lapā **Darbības redzamība** tiek sniegti reāllaika rīcībā esoša krājumu vaicājuma, rezervācijas grāmatošanas un sadalījuma rezultāti, pamatojoties uz dažādām dimensiju kombinācijām. *Ja līdzeklis OnHandReservation* ir [ieslēgts](inventory-visibility-configuration.md), varat arī publicēt rezervācijas pieprasījumus **lapā Darbības redzamība**.

### <a name="on-hand-query"></a>Rīcībā esošie vaicājumi

Lapas **Darbības redzamība cilnē** Vaicājums **varat** vaicāt par rīcībā esošajiem krājumiem reāllaikā. Veiciet šīs darbības, lai iestatītu un palaistu vaicājumu.

1. **Atveriet programmu Krājumu redzamība**.
1. **Atveriet lapu Darbības redzamība** no kreisās rūts.
1. Cilnē **Rīcībā esošais vaicājums ievadiet** vaicājumu **Organization ID, Site ID un Location ID (** Atrašanās vietas ID).**·** **·**
1. **Laukā Produkta ID ievadiet vienu vai vairākus produktu ID**, lai iegūtu precīzu atbilstību savam vaicājumam. Ja lauku Produkta ID **atstāsit** tukšu, rezultātos tiks iekļauti visi produkti norādītajā vietā un vietā.
1. Lai iegūtu detalizētāku rezultātu (piemēram, skatu pēc dimensiju vērtībām, piemēram, krāsas un lieluma), laukā Grupēt rezultātu pēc **atlasiet Grupēt** pēc.
1. Lai atrastu vienumus, kuriem ir noteikta dimensijas vērtība (piemēram, krāsa = sarkana), laukā Filtrēt dimensijas atlasiet dimensiju **un pēc tam ievadiet dimensijas** vērtību.
1. Atlasiet **Vaicājums**. Jūs saņemsit sekmīgu (zaļu) ziņojumu, vai nesekmīgu (sarkanu) ziņojumu. Ja vaicājums neizdodas, pārbaudiet vaicājuma kritērijus un pārliecinieties, vai [uzrādītāja marķiera](#open-authenticate) derīguma termiņš nav beidzies.

Vēl viens veids, kā veikt rīcībā esošu vaicājumu, ir veikt tiešus API pieprasījumus. Jūs varat izmantot vienu vai `/api/environment/{environmentId}/onhand/indexquery`.`/api/environment/{environmentId}/onhand` Papildinformāciju skatiet sadaļā [Krājumu redzamības publiskās API.](inventory-visibility-api.md)

### <a name="reservation-posting"></a>Rezervāciju grāmatošana

**Izmantojiet lapas Darbības redzamība** cilni **Rezervācijas publicēšana**, lai publicētu rezervācijas pieprasījumu. Pirms rezervēšanas pieprasījuma grāmatošanas ir jāslēdz funkcija *OnHandReservation*. Papildinformāciju par šo līdzekli un to, kā to ieslēgt, skatiet sadaļā [Krājumu redzamības rezervācijas](inventory-visibility-reservations.md).

> [!NOTE]
> Iespēja veikt mīksto rezervāciju, izmantojot lietotāja interfeisu, ir paredzēta, lai ļautu jums pārbaudīt šo funkciju. Katram neobligātajam rezervācijas pieprasījumam jābūt saistītam ar transakciju pasūtījuma rindas maiņu (izveide, modificēšana, dzēšana utt.). Tāpēc mēs iesakām veikt tikai neobligātās rezervācijas, kas ir saistītas ar aizmugursistēmas pasūtījumu. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

Veiciet šīs darbības, lai publicētu neierobežotu rezervācijas pieprasījumu, izmantojot lietotāja interfeisu.

1. **Atveriet programmu Krājumu redzamība**.
1. **Atveriet lapu Darbības redzamība** no kreisās rūts.
1. Cilnes **Rezervācijas** grāmatošana **laukā Daudzums** norādiet daudzumu, kuru vēlaties veikt papildu rezervēšanai.
1. Notīriet izvēles rūtiņu **Iespējot negatīvos krājumus, lai atbalstītu oversell**, lai novērstu krājumu pārpārdošanu vai pārmērīgu rezervēšanu.
1. **Laukā Operators** atlasiet datu avotu un fizisko mēru, kas attiecas uz maznozīmīgo rezervēto daudzumu.
1. Ievadiet vaicājumu **vērtībām Organizācijas ID, Vietnes ID, Atrašanās vietas ID un** Preces **ID** **·** **·**.
1. Lai iegūtu detalizētāku rezultātu, atlasiet datu avotu, dimensijas un dimensiju vērtības.

Vēl viens veids, kā publicēt mīksto rezervāciju, ir veikt tiešus API pieprasījumus. Izmantojiet modeli, kas ir aprakstīts sadaļā [Izveidot vienu rezervācijas notikumu](inventory-visibility-api.md#create-one-reservation-event). Pēc tam atlasiet **Grāmatot**. Lai skatītu pieprasījuma atbildes informāciju, atlasiet **Rādīt informāciju**. Atbildes informācijā varat arī iegūt `reservationId` vērtību.

### <a name="allocation"></a>Sadalījums

Informāciju par to, kā pārvaldīt piešķīrumus no lietotāja interfeisa un API, skatiet sadaļā [Krājumu redzamības krājumu sadalījums](inventory-visibility-allocation.md).

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Krājumu kopsavilkums

Lapā **Krājumu kopsavilkums ir sniegts krājumu kopsavilkums** precēm kopā ar visām dimensijām. Tas ir pielāgots entītijas Inventory OnHand Sum *skats*. Krājumu kopsavilkuma dati tiek periodiski sinhronizēti no krājumu redzamības.

Lai iespējotu lapu Krājumu kopsavilkums **un iestatītu** sinhronizācijas biežumu, rīkojieties šādi:

1. Atveriet lapu **Konfigurācija**.
1. **Atveriet cilni Līdzekļu pārvaldība un iestatījumi**.
1. Iestatiet OnHandMostSpecificBackgroundService **līdzekļa pārslēgšanas** slēdzi uz *Jā*.
1. Kad līdzeklis ir iespējots, **kļūst pieejama sadaļa Pakalpojuma konfigurācija**, kurā ir iekļauta rinda līdzekļa OnHandMostSpecificBackgroundService **konfigurēšanai**. Šis iestatījums ļauj izvēlēties, cik bieži tiek sinhronizēti krājumu kopsavilkuma dati. **Izmantojiet kolonnas Vērtība pogas** Augšup **un** **lejup**, lai mainītu laiku starp sinhronizācijām (kas var būt pat 5 minūtes). Pēc tam atlasiet **Saglabāt**.

    ![OnHandMostSpecificBackgroundService iestatījums](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService iestatījums")

1. Atlasiet **Atjaunināt konfigurāciju**, lai saglabātu visas izmaiņas.

> [!NOTE]
> OnHandMostSpecificBackgroundService *līdzeklis* izseko tikai rīcībā esošās krājumu izmaiņas, kas radušās pēc līdzekļa ieslēgšanas. Dati par produktiem, kas nav mainīti kopš līdzekļa ieslēgšanas, netiks sinhronizēti no krājumu pakalpojuma kešatmiņas ar Dataverse vidi. **Ja lapā Krājumu kopsavilkums** netiek rādīta visa rīcībā esošā informācija, atveriet sadaļu Supply Chain Management, dodieties uz Inventory **Management > Periodic tasks > Inventory Visibility integrācija**, atspējojiet pakešuzdevumu un atkārtoti iespējojiet to. Tas veiks sākotnējo grūdienu, un nākamo 15 minūšu laikā visi dati tiks sinhronizēti ar *entītiju Inventory OnHand Sum.* Ja vēlaties izmantot *līdzekli OnHandMostSpecificBackgroundService*, ieteicams to ieslēgt, pirms veidojat pieejamās izmaiņas, un iespējot **krājumu redzamības integrācijas** pakešuzdevumu.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a> Racionalizēta rokas vaicājuma iepriekšēja ielāde

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management glabā daudz informācijas par jūsu rīcībā esošajiem krājumiem un padara to pieejamu dažādiem mērķiem. Tomēr daudzām ikdienas darbībām un trešo pušu integrācijām ir nepieciešama tikai neliela šo detaļu apakškopa, un, vaicājot sistēmai par visām tām, var rasties lielas datu kopas, kuru apkopošanai un pārsūtīšanai ir nepieciešams laiks. Tāpēc krājumu redzamības pakalpojums var periodiski ienest un glabāt racionalizētu rīcībā esošo krājumu datu kopu, lai šī optimizētā informācija būtu pastāvīgi pieejama. Rīcībā esošā krājumu informācija tiek filtrēta, pamatojoties uz konfigurējamiem biznesa kritērijiem, lai nodrošinātu, ka tiek iekļauta tikai visatbilstošākā informācija. Tā kā rīcībā esošie filtrētie krājumu saraksti tiek glabāti lokāli pakalpojumā Krājumu redzamība un tiek regulāri atjaunināti, tie atbalsta ātru piekļuvi, datu eksportēšanu pēc pieprasījuma un racionalizētu integrāciju ar ārējām sistēmām.

Lapas **Krājumu redzamības kopsavilkuma** iepriekšēja ielāde nodrošina entītijas Rīcībā esošs indeksa *vaicājuma iepriekšējas ielādes rezultātu* skats. Atšķirībā no *entītijas Krājumu kopsavilkums*, *entītija Rīcībā esošie indeksa vaicājuma iepriekšējas ielādes rezultāti* nodrošina rīcībā esošo krājumu sarakstu precēm kopā ar atlasītajām dimensijām. Krājumu redzamība sinhronizē iepriekš ielādētos kopsavilkuma datus ik pēc 15 minūtēm.

Lai skatītu **datus cilnē Krājumu redzamības kopsavilkuma** iepriekšēja ielāde, lapas Konfigurācija cilnē *Līdzekļu* pārvaldība **ir** jāieslēdz **līdzeklis OnHandIndexQueryPreloadBackgroundService** un pēc tam atlasiet **Atjaunināt konfigurāciju** (skatiet arī [Krājumu redzamības](inventory-visibility-configuration.md) konfigurēšana).

> [!NOTE]
> Tāpat kā *ar OnhandMostSpecificBackgroudService funkciju, līdzeklis OnHandIndexQueryPreloadBackgroundService* *izseko tikai rīcībā esošās krājumu izmaiņas,* kas radušās pēc līdzekļa ieslēgšanas. Dati par produktiem, kas nav mainīti kopš līdzekļa ieslēgšanas, netiks sinhronizēti no krājumu pakalpojuma kešatmiņas ar Dataverse vidi. **Ja lapā Krājumu kopsavilkums** netiek rādīta visa pieejamā informācija, dodieties uz Krājumu **pārvaldība > Periodiskie uzdevumi > krājumu redzamības integrācija**, atspējojiet pakešuzdevumu un atkārtoti iespējojiet to. Tas veiks sākotnējo grūdienu, un nākamo 15 minūšu laikā visi dati tiks sinhronizēti ar *rīcībā esošo indeksa vaicājuma iepriekšējas ielādes rezultātu* entītiju. Ja vēlaties izmantot šo līdzekli, ieteicams to ieslēgt, pirms veidojat pieejamās izmaiņas, un iespējot **krājumu redzamības integrācijas** pakešuzdevumu.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a> Krājumu kopsavilkumu filtrēšana un pārlūkošana

Lietojiet Dataverse sniegto **Detalizēto filtru**, varat izveidot personalizētu skatu, kurā rādītas jums svarīgākās rindas. Papildu filtra opcijas ļauj izveidot plašu skatījumu klāstu no vienkāršiem uz kompleksiem. Tie arī ļauj pievienot filtriem grupētus un ligzdotus nosacījumus. Papildinformāciju par to, kā izmantot papildu filtru, skatiet rakstā [Personisko skatu rediģēšana vai izveide, izmantojot režģa papildu filtrus](/powerapps/user/grid-filters-advanced).

Lapā **Krājumu kopsavilkums** ir trīs lauki virs režģa (**noklusējuma dimensija, pielāgotā dimensija** **un** mērs), kurus varat izmantot, lai kontrolētu, **kuras kolonnas** ir redzamas. Varat arī atlasīt jebkuru kolonnas galveni, lai filtrētu vai kārtotu pašreizējo rezultātu pēc šīs kolonnas. Tālāk redzamajā ekrānuzņēmumā ir izcelti lauki ar kategoriju, filtrēšanu, rezultātu skaitu un "ielādēt vairāk", kas pieejami **lapā Krājumu kopsavilkums**.

![Lapa Krājumu kopsavilkums.](media/inventory-visibility-onhand-list.png "Lapa Krājumu kopsavilkums")

Tā kā jums būs iepriekš definētas dimensijas, kas tiek izmantotas kopsavilkuma datu ielādei, **lapā Krājumu redzamības kopsavilkuma** iepriekšēja ielāde tiek rādītas ar dimensijām saistītas kolonnas. *Izmēri nav pielāgojami&mdash;, jo sistēma atbalsta tikai vietnes un atrašanās vietas dimensijas iepriekš ielādētiem rīcībā esošiem sarakstiem.* Lapas Krājumu **redzamības kopsavilkuma** iepriekšēja ielāde nodrošina filtrus, kas ir līdzīgi filtriem **lapā Krājumu kopsavilkums**, izņemot to, ka dimensijas jau ir atlasītas. Tālāk redzamajā ekrānuzņēmumā ir izcelti filtrēšanas lauki, kas **pieejami kopsavilkuma lapā Krājumu redzamības iepriekšēja** ielāde.

![Iepriekš ielādējiet kopsavilkuma lapu Krājumu redzamība.](media/inventory-visibility-preload-onhand-list.png "Krājumu redzamības kopsavilkuma lapas iepriekšēja ielāde")

Lapas Krājumu redzamības kopsavilkuma un **Krājumu kopsavilkuma** **iepriekšējas ielādes apakšdaļā** atradīsit informāciju, piemēram, "50 ieraksti (29 atlasīti)" vai "50 ieraksti". Šī informācija attiecas uz ierakstiem, kas pašlaik ielādēti no **Detalizētā filtra** rezultāta. Teksts "atlasīts 29" attiecas uz ierakstu skaitu, kas ir atlasīti, ielādētajiem ierakstiem izmantojot kolonnas virsraksta filtru. Ir arī **poga Ielādēt vairāk, ko varat izmantot, lai ielādētu vairāk** ierakstu no Dataverse. Noklusējuma ielādēto ierakstu skaits ir 50. Atlasot **Ielādēt vairāk**, skatā tiks ielādēti nākamie 1,000 pieejamie ieraksti. Skaits pogā **Ielādēt vēl** norāda pašlaik ielādētos ierakstus un kopējo ierakstu skaitu **Detalizētā filtra** rezultātā.
