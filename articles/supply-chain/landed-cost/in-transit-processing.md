---
title: Tranzīta preču apstrāde
description: Šajā tēmā ir aprakstīts, kā strādāt ar tranzīta preču pasūtījumiem. Kad pasūtījums vai reiss ir iestatīts izmantot tranzītā apstrādātās preces, par precēm var izrakstīt rēķinu, pirms tās ir saņemtas patēriņam noliktavā.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e85e3ba92b61e0208e1cf95d3f361d38772d83cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571045"
---
# <a name="goods-in-transit-processing"></a>Tranzīta preču apstrāde

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā strādāt ar tranzīta preču pasūtījumiem. Šis pasūtījuma veids tiek izmantots tikai **Kopīgo izmaksu** modulī. Kad pasūtījums vai reiss ir iestatīts izmantot tranzītā apstrādātās preces, par precēm var izrakstīt rēķinu, pirms tās ir saņemtas patēriņam noliktavā. Tā vietā preces tiek iekļautas rēķinā, kad tās atstāj kreditora noliktavu vai izcelsmes ostu, un finanšu izmaksas tiek atpazītas, kad sākas reiss. Šī funkcionalitāte ļauj jums pareizi īpašumtiesības nodot krājumiem, jo preces bieži kļūst par jūsu organizācijas rekvizītu, kad tās atstāj nosūtīšanas ostu.

Kad tiek izmantoti tranzītkravu pasūtījumi, finansiāli atjauninātie krājumi tiek saņemti pagaidu noliktavā, kas zināma kā tranzītkravu noliktava. Tad preces paliek šajā noliktavā, līdz tās var saņemt gala adresāta noliktavā (t.i., noliktavā, kas ir noteikta pirkšanas rindā). Tos nevar manuāli noņemt.

Kamēr krājumi ir tranzītā, tie nav pieejami krājumos un tos nevar izdot no noliktavas, lai varētu veikt piegādi. Tomēr jūs variet aplūkot tranzīta preču krājumus. Preces var izmantot arī vispārējai plānošanai. Šajā gadījumā izmantojiet apstiprināto piegādes datumu pirkšanas pasūtījuma rindā kā paredzēto datumu, kad krājumi būs pieejami patēriņam.

Šajās sadaļās aprakstīti iestatījumi, kas ir nepieciešami krājumu un reisu apstrādāšanai, izmantojot preču tranzīta koncepciju un funkcionalitāti.

## <a name="terms-of-delivery"></a>Piegādes nosacījumi

Aktivizējot moduli **Kopējās izmaksas**, tiek uzlaboti *Piegādes elementu standarta nosacījumi*, lai atbalstītu funkciju tranzīta līdzeklim.

Ja opcija **Tranzīta preču pārvaldība** ir iestatīta uz *Jā* piemērojamiem piegādes nosacījumiem, preces tiek novietotas tranzītkravu noliktavā. Šī darbība tiek izraisīta tikai tad, ja krājumu ieejas plūsma nav apstrādāta pirms rēķina apstrādes. Kad pasūtījuma piegādes nosacījumi ir iestatīti preču izmantošanai tranzītā, lietotāji vairs nevar grāmatot produktu ieejas plūsmu pirkšanas pasūtījumam. Ja mēģināts, rodas kļūda. Kļūdas ziņojums norāda, ka, lai turpinātu, tām ir jāizmanto tranzīkravu funkcionalitāte.

Lai strādātu ar piegādes nosacījumu informāciju tranzītā citām precēm, dodieties uz **Sagāde un plānošana \> Iestatījumi \> Izplatīšana \> Piegādes nosacījumi**. Šajā tabulā ir aprakstīti lauki, kurus **Kopējo izmaksu** modulis pievieno **Piegādes nosacījumu** lapai, lai atbalstītu funkcionalitāti "Preces tranzītā". Abi lauki ir kopsavilkuma cilnē **Vispārīgi**. Plašāku informāciju par citiem šīs lapas laukiem skatiet [Piegādes nosacījumi (veidlapa)](/dynamicsax-2012//terms-of-delivery-form).

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas osta ir obligāta prasība | Iestatiet šo opciju kā *Jā*, ja piegādes osta ir obligāta, ja tiek piemēroti piegādes nosacījumi. |
| Tranzītpreču pārvaldīšana | Iestatiet šo opciju kā *Jā*, lai lietotu tranzītkravu pārvaldību, ja tiek piemēroti piegādes nosacījumi. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Noliktavas tranzītkravm un nepiegādātām precēm

Ja ir aktivizēts modulis **Kopējās izmaksas**, standarta entītija *Noliktavas* tiek uzlabota, lai iespējotu to, ka pirkuma pasūtījumi tiek izrakstīti rēķinos, kamēr preces ir tranzīta noliktavā.

Kopējās sūtījuma izmaksas pievieno divus jaunus noliktavu veidus: *tranzītkravas* un *preču nepiegādāšana*. Abu tipu noliktavas var izvēlēties kā noklusējuma noliktavas. Lai veiksmīgi apstrādātu tranzītkravu pasūtījumus, lapā **Noliktavas** jābūt konfigurētai gan noliktavai, kas atrodas tranzītā, gan nepiegādāto preču noliktavai. Pēc tam katrai noklusējuma noliktavai, kas tiks izmantota ar kopējām izmaksām un tranzīta precēm, katra tipa pieejamajām noliktavām ir jāatlasa preces, kas ir tranzīta noliktava un nepiegādāto preču noliktava.

*Tranzīta preču* noliktavas tips, tiks saistītas ar jūsu tranzītkrājumu noliktavu un šī noliktava tiks izmantota, lai apstrādātu preces tranzītpasūtījumus pirms to saņemšanas gala adresāta noliktavā. Parasti viena tranzītkrājumu noliktava ir pietiekoši katrai vietai, ja Vieta un Noliktava ir vienīgās krājumu dimensijas, kas tiek izmantotas krājumu pārvaldībai. Ja tiek izmantota arī Krājumu dimensija Vieta, katrai vietas un noliktavas kombinācijai ir jāiestata noliktava, kas atrodas tranzītā, lai varētu norādīt arī noklusējuma atrašanās vietu.

Lai strādātu ar noliktavām precēm tranzītā, pārejiet uz sadaļu **Krājumu pārvaldība \> Iestatījumi \> Krājumu sadale \> Noliktavas**. Šajā tabulā ir aprakstīti lauki, kurus **Kopējo izmaksu** modulis pievieno lapai **Noliktavas**, lai atbalstītu funkcionalitāti "Preces tranzītā". Abi lauki ir kopsavilkuma cilnē **Vispārīgi**. Papildinformāciju par citiem lapas laukiem skatiet [Noliktavas (veidlapa)](/dynamicsax-2012//warehouses-form).

| Lauks | Apraksts |
|---|---|
| Tranzītpreču noliktava | Identificējiet tranzītā saistītajām precēm noliktavu, kas saistīta ar galveno noliktavu. |
| Piegādes noliktava | Identificējiet nepiegādāto preču noliktavu, kas saistīta ar galveno noliktavu. |

## <a name="posting-rules-for-landed-cost"></a>Grāmatošanas noteikumi par kopējām izmaksām

Kopējās izmaksas pievieno divus jaunus grāmatošanas noteikumus, ko var konfigurēt. Šie grāmatošanas noteikumi tiek izmantoti, lai finansiāli iegrāmatotu tiešā pirkšanas pasūtījuma rēķina summas, lai identificētu īpašumtiesības precēm, kad tās atstāj izcelsmes punktu. Šis process aizstāj *saņemto preču, par kurām nav izrakstīts rēķins* konceptu, jo preces tiek iekļautas rēķinā pirms to saņemšanas. <!-- KFM: Add a link to the related scenario when available. -->

Lai strādātu ar grāmatošanas metodēm, pārejiet uz sadaļu **Krājumu pārvaldība \> Iestatījumi \> Grāmatošana \> Grāmatošana**. Cilnē **Pirkšanas pasūtījums** ir pieejami šādi jauni grāmatošanas noteikumi:

- **Kopējās izmaksas tranzīta precēm** – norādiet tranzīta preču pārvaldības grāmatošanas kārtulas.
- **Kopējās izmaksas, izmaksu izmaksu uzkrājums** – norādiet grāmatošanas noteikumus izmaksu konta uzkrājumam.

## <a name="goods-in-transit-orders"></a>Tranzītpreču pasūtījumi

Jūs varat pārskatīt un pārvaldīt tranzītpasūtījumus tieši **Kopējo izmaksu** modulī. Jūs varat apstrādāt tranzītpasūtījumus tieši no lapas **Tranzīta preču pasūtījumi**. Vai arī varat doties uz reisu, kas ir saistīts ar tranzītpasūtījumu, un apstrādāt visu reisu, nosūtīšanas konteineru vai folio. Kad jūs izrakstiet rēķinu par reisu un izveidojat tranzītkravu pasūtījumus, katrai krājumu un krājumu dimensiju kombinācijai, kas saistīta ar pirkšanas pasūtījuma rindu, tiek izveidots jauns tranzītkrājumos esošo preču pasūtījums.

Lai pārvaldītu tranzīta kravu, Kopējās izmaksas izmanto divu soļu procedūru:

1. Krājums tiek saņemts, kad tiek apstrādāts krājumu rēķins un tam ir piešķirts statuss *Tranzītā*.
1. Tranzīta preču pasūtījums tiek apstrādāts lapā **Tranzīta preču pasūtījumi** un pēc tam saņemts pirkšanas pasūtījumā norādītajā noliktavā. Šajā punktā statuss tiek mainīts uz *Saņemts*.

Lai strādātu ar tranzītpasūtījumu precēm, dodieties uz sadaļu **Kopējās izmaksas \> Periodiskie uzdevumi \> Tranzīta preču pasūtījumi**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Krājuma saņemšana no tranzīta preču noliktavām

Atkarībā no jūsu sistēmas iestatījumiem, ir iespējams saņemt preces no tranzīta preču pasūtījuma daudzos veidos.

### <a name="in-transit-receiving"></a>Tranzīta saņemšana

Var veikt tranzīta saņemšanu no jebkuras no šīm lapām:

- Lapā **Tranzīta precu pasūtījumi** atlasiet rindu un pēc tam darbību rūtī atlasiet **Saņemt**.
- Lapā **Visi reisi** atlasiet vai atveriet reisu. Pēc tam Darbību rūtī cilnē **Pārvaldīt**, **Tranzīta preču** grupā atlasiet **Saņemt preces tranzītā**.
- Lapā **Visi sūtījumu konteineri** atlasiet vai atveriet pārvadāšanas konteineru. Pēc tam Darbību rūtī cilnē **Pārvaldīt**, **Tranzīta preču** grupā atlasiet **Saņemt preces tranzītā**.
- Lapā **Visi folio** atlasiet vai atveriet folio. Pēc tam Darbību rūtī cilnē **Pārvaldīt**, **Tranzīta preču** grupā atlasiet **Saņemt preces tranzītā**.

> [!NOTE]
> Tranzīta saņemšana parasti tiek izmantota gadījumos, kad netiek izmantotas atrašanās vietas un partijas/sērijas izsekošana.

### <a name="arrival-journal"></a>Saņemšanas žurnāls

Preces var arī saņemt, izveidojot saņemšanas žurnālu. Saņemšanas žurnālu var izveidot tieši no reisu lapas. Jūsu organizācijas izveidotie noteikumi nosaka, vai preču saņemšanai saņemšanas žurnāls tiek izmantots.

1. Atvērt reisu, konteineru vai folio.
1. Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot saņemšanas žurnālu**.
1. Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:

    - **Inicializēt daudzumu** — iestatiet šo opciju kā *Jā*, lai iestatītu daudzumu no tranzīta daudzuma. Ja šī opcija ir iestatīta uz *Nē*, no tranzīta rindām uz precēm netiek iestatīts noklusējuma daudzums.
    - **Izveidot no tranzīt precēm** – iestatiet šo opciju kā *Jā*, lai no atlasītā reisa, konteinera vai folio atlasītās tranzīta rindas iegūtu daudzumus.
    - **Izveidot no pasūtījuma rindām** – iestatiet šo opciju kā *Jā*, lai iestatītu noklusējuma daudzumu saņemšanas žurnālā no pirkšanas pasūtījuma rindām. Noklusējuma daudzumu saņemšanas žurnālā var iestatīt šādā veidā, ja daudzums pirkšanas pasūtījuma rindā sakrīt ar daudzumu preču tranzīta pasūtījumā.

1. Apstrādājiet saņemšanas žurnālu, kā tas ir aprakstīts [Krājumu saņemšanas reģistrēšanai krājumu saņemšanas žurnālā](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal).

> [!NOTE]
> Saņemšanas žurnāls parasti tiek izmantots situācijās, kad tiek izmantotas atrašanās vietas un partijas/sērijas izsekošana, bet netiek izmantota noliktavas pārvaldība.
>
> Ja saņemšanas žurnālā ir norādīta izvietošanas vieta, pasūtījuma rindās nav jānorāda noklusējuma saņemšanas vietas.

## <a name="warehouse-management"></a>Noliktavas pārvaldība

Iespējojot moduli **Kopējās izmaksas**, tiek modificētas vairākas **Noliktavas pārvaldības** moduļa lapas, lai pasūtījuma apstrādi (it īpaši preču tranzītapstrāde) varētu veikt caur **Kopējo izmaksu** moduli. Šajā sadaļā ir ieskicē lauki un procesi, kas ir pievienoti **Noliktavas pārvaldības** modulim.

### <a name="mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumi

Preces var saņemt, izmantojot mobilo ierīci ar nosacījumu, ka mobilās ierīces izvēlne un **Noliktavas pārvaldības** modulis ir iestatīts preču saņemšanai saskaņā ar preču tranzīta pasūtījumu. Šajā sadaļā ir aprakstīts iestatījums, kas saistīts ar preču tranzīta saņemšanu.

Lai iestatītu mobilās ierīces tranzītā esošo preču apstrādei, pārejiet uz sadaļu **Noliktavas pārvaldība \> Iestatījumi \> Mobilās ierīces \> Mobilās ierīces izvēlnes vienumi**.

Kopējās izmaksas pievieno šādus darba izveides procesus mobilās ierīces izvēlnes vienumiem, lai atbalstītu tranzītā esošo preču apstrādi:

- Tranzītpreču krājuma saņemšana
- TRanzīta preču krājuma saņemšana un izvietošana

Šo procesu konfigurācijas iestatījumi ir līdzīgi [pirkšanas pasūtījuma saņemšanas un izvietošanas darba izveides procesu iestatījumiem](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work). Tomēr *Tranzīta preču krājuma saņemšanas un izvietošanas* procesā tiek pievienots arī šāds lauks.

- **Iespējojiet sūtīšanas konteinera pabeigtību** — ja šī opcija ir iestatīta uz *Jā*, kad izvietošanas darbs ir pabeigts, Warehouse Management mobile programma nodrošina papildu opciju ar nosaukumu **Sūtījumu konteiners ir pabeigts**. Kad šī opcija ir atlasīta, darbiniekam tiks lūgts apstiprināt konteinera pabeigšanas apstiprinājumu. Šajā brīdī visas īsās ieejas plūsmas tiks apstrādātas kā nepiegādāšanas darbības.

### <a name="location-directives"></a>Vietas direktīvas

Kopējās izmaksas pievieno jaunu darba pasūtījuma tipu, kura nosaukums ir *Preces tranzītā* **Novietojuma direktīvu** lapā. Šim darba pasūtījuma tipam jābūt konfigurētam tādā pašā veidā kā [pirkšanas pasūtījuma darba pasūtījuma tipiem](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Darbu veidnes

Šajā sadaļā ir aprakstīti līdzekļi, ko modulis **Izkraušanas izmaksas** pievieno darba veidnēm.

#### <a name="goods-in-transit-work-order-type"></a>Preces tranzīta darba pasūtījuma veids

Kopējās izmaksas pievieno jaunu darba pasūtījuma tipu, kura nosaukums ir *Preces tranzītā* **Darba veidņu** lapā. Šim darba pasūtījuma tipam jābūt konfigurētam tādā pašā veidā kā [pirkšanas pasūtījuma darba pasūtījuma tipiem](/dynamicsax-2012/appuser-itpro/create-a-work-template).

#### <a name="work-header-breaks"></a>Darba virsrakstu pārtraukumi

Darba veidnes, kuru darba pasūtījuma veids *Preces tranzītā* var konfigurēt, lai sadalītu darbu virsrakstus. Lapā **Darba veidnes** veiciet vienu no tālāk norādītajām darbībām:

- Veidnes cilnē **Vispārīgi** iestatiet darba virsraksta maksimumus. Šie maksimumi darbojas tādā pašā veidā, kā tie darbojas pirkšanas pasūtījuma darba veidnēs. (Papildinformāciju skatiet [pirkšanas pasūtījumu darbu veidnēs](/dynamicsax-2012/appuser-itpro/create-a-work-template).)
- Izmantojiet pogu **Darba virsraksta pārtraukumi**, lai definētu, kad sistēmai jāizveido jaunus darba virsrakstus, pamatojoties uz laukiem, kas tiek izmantoti kārtošanai. Piemēram, lai izveidotu darba virsrakstu katram konteinera ID, darbības rūtī atlasiet **Rediģēt vaicājumu** un pēc tam pievienojiet lauku **Konteinera ID** vaicājumu redaktora cilnei **Kārtošana**. Lauki, kas ir pievienoti cilnei **Kārtošana**, ir pieejami atlasei kā *grupēšanas lauki*. Lai iestatītu grupēšanas laukus, darbības rūtī atlasiet **Darba virsraksta pārtraukumi** un pēc tam katram laukam, kuru vēlaties izmantot kā grupēšanas lauku, atzīmējiet izvēles rūtiņu kolonnā **Grupēt pēc ša lauka**.

Izkraušanas izmaksas [izveido pārsniegtu darījumu](over-under-transactions.md), ja reģistrētais daudzums pārsniedz sākotnējā pasūtījuma daudzumu. Kad darba virsraksts ir pabeigts, sistēma atjaunina krājumu darbību statusu galvenā pasūtījuma daudzumam. Tomēr tā vispirms atjaunina daudzumu, kas ir saistīts ar pārsniegtu darbību pēc tam, kad galvenais ir pilnībā nopirkts.

Ja atceļat darba virsrakstu pārsniegtai darbībai, kas jau ir reģistrēta, pārsniegta darbība vispirms tiek samazināta ar atcelto daudzumu. Kad pārsniegta darbība tiek samazināta līdz daudzumam 0 (nulle), ieraksts tiek noņemts, un visi papildu daudzumi tiek noņemti attiecībā pret galveno pasūtījuma daudzumu.
