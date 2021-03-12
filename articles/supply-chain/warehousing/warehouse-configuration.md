---
title: Noliktavas konfigurācijas pārskats
description: Šajā rakstā ir paskaidrots, kā konfigurēt noliktavu. Tajā ir ietverta informācija par to, kā iespējot noliktavas izkārtojumu un noliktavas procesus.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b0ebb5d7f77e2104d0280bcee7c018d9cf97bd5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970160"
---
# <a name="warehouse-configuration-overview"></a>Noliktavas konfigurācijas pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā konfigurēt noliktavu. Tajā ir ietverta informācija par to, kā iespējot noliktavas izkārtojumu un noliktavas procesus.

> [!NOTE]
> Šis raksts attiecas uz moduļa **Noliktavas pārvaldība** (uzlabotās noliktavas) līdzekļiem. Tas neattiecas uz noliktavas līdzekļiem modulī **Krājumu vadība**.

## <a name="warehouse-layout"></a>Noliktavas izkārtojums
Noliktavu vadības sistēma programmatūrā Supply Chain Management sniedz jums elastīgus veidus, kā definēt savas noliktavas izkārtojumu, lai tas atbilstu mainīgajām vajadzībām, tāpēc varat sasniegt optimālu noliktavas efektivitāti.

-   Optimālai preču izvietošanai varat izveidot augstas prioritātes un zemas prioritātes glabāšanas zonas.
-   Noliktavas varat sadalīt zonās, lai pielāgotos dažādām glabāšanas vajadzībām, piemēram, temperatūras prasībām vai dažādiem krājumu apgrozījuma ātrumiem.
-   Noliktavu novietojumus varat norādīt jebkurā līmenī (piemēram, vieta, noliktava, aile, statīvs, plaukts un nodalījuma pozīcija).
-   Novietojumus varat grupēt, izmantojot fiziskās ietilpības ierobežojumu iestatījumus.
-   Varat kontrolēt veidu, kā krājumi tiek glabāti un izdoti, pamatojoties uz vaicājuma definētām kārtulām.

Lai programmatūrā Supply Chain Management izmantotu noliktavas pārvaldību, jums ir jāizveido noliktava, un tā jāiespējo papildu vai specializētākām noliktavas pārvaldības darbībām. Lapā **Noliktavas** atzīmējiet opciju **Izmantot noliktavas pārvaldības procesus**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonu grupas, zonas, novietojumu tipi un novietojumi

Kā daļa no noliktavas izkārtojuma iespējošanas procesa jums ir jādefinē noliktavas zonu grupas, kā arī zonas, novietojumu profili, novietojumu tipi un novietojumi.

-   **Zonu grupas** — loģiska vai fiziska zonu grupēšana noliktavas ietvaros.
-   **Zonas** — loģiska vai fiziska novietojumu grupēšana noliktavas ietvaros.
-   **Novietojumu profili** — loģiska vai fiziska novietojumu grupēšana tādiem novietojumiem, kam ir vienādas noliktavas novietojumu apstrādes politikas (piemēram, šeit var glabāt dažādu krājumu numuru sajaukumu, un ir spēkā tie paši fiziskās ietilpības ierobežojumi).
-   **Novietojumu tipi** — loģiska vai fiziska noliktavas novietojumu grupēšana. Piemēram, varat izveidot atrašanās vietas veidu visiem novietojuma veidiem. Obligātie iestatījumi lapā **Noliktavas pārvaldības parametri** vada sagatavošanas posmu novietojuma tipu un galīgās nosūtīšanas novietojuma tipu definēšanas procesu.
-   **Novietojumi** — novietojuma informācijas zemākais līmenis. Novietojumi tiek izmantoti, lai izsekotu, kur rīcībā esošie krājumi tiek glabāti un izdoti noliktavā.

Elementi, ko izveidojat, lai definētu savas noliktavas izkārtojumu, tiek izmantoti vaicājumos, kurus iestatāt darbu veidnēs, lai noliktavā vadītu darba pasūtījumus. Tādēļ, kad definējat zonas, novietojumu tipus un citus elementus, ņemiet vērā veidu, kā dažādi apgabali noliktavā tiek izmantoti dažādiem procesiem. Turklāt ņemiet vērā arī tādus faktorus kā konkrēta apgabala fiziskie raksturlielumi. Piemēram, var būt apgabali, kur varat izmantot tikai noteikta veida autoiekrāvēju. Vai arī, ja jūsu uzņēmumam vienās telpās ir gan ražošanas, gan pabeigtās preces, iespējams, programmatūrā Supply Chain Management vēlaties izveidot vienu noliktavu, bet pēc tam abas operācijas sadalīt, izveidojot divas zonu grupas. Piešķiriet saviem elementiem aprakstošus nosaukumus, lai tos būtu vienkārši identificēt, kad tos izmantojat veidņu vaicājumos.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Novietojumu dimensiju ierobežojumi, novietojumu profili un fiksēti izdošanas novietojumi

Jums ir jāņem vērā noliktavas fiziskais izkārtojums — gan lai noteiktu glabāšanas ietilpību (novietojuma dimensiju ierobežojumi un novietojuma profili), gan kā daļu no jūsu centieniem optimāli veikt noliktavas procesus. 

Novietojumu dimensiju ierobežojumi palīdz nodrošināt, ka netiek izveidots darbs, lai pieprasītu krājumus izvietot tādā novietojumā, kur šādu krājumu izvietošanai nav fiziskās ietilpības. Piemēram, ja dažos novietojumos noliktavā katrā novietojumā var ievietot tikai vienu paleti, tad var iespējot novietojuma dimensijas ierobežojumus. Vērtību **Daudzums** var iestatīt uz **1**, un vērtību **Vienība** var iestatīt uz **PL** kādā noteiktā novietojumu profilu grupējumā. 

Ja ir nepieciešami papildu aprēķini, lai kontrolētu novietojuma ietilpības ierobežojumus, var izmantot novietojuma profila iestatījumus. Tādā gadījumā ietilpības aprēķināšanas laikā tiek ņemts vērā svars un tilpums. 

Lai sasniegtu optimālus izejošos procesus, jums ir jāizvērtē, vai izmantot fiksētos izdošanas novietojumus un/vai iepakošanas novietojumus. Bieži minimālā/maksimālā papildināšana tiek izmantota papildināšanas procesiem no lielapjoma apgabala uz fiksētiem izdošanas novietojumiem, un tajā pašā noliktavā un preces variantiem var iespējot vairākus fiksētos izdošanas novietojumus. Apsveriet elastību, kādu varat sasniegt, iespējojot atvēlētus pieprasījuma papildināšanas pārpildes novietojumus, kas tiek izmantoti tikai kopuma/noslodzes papildināšanas apstrādei.

### <a name="location-setup-wizard"></a>Novietojuma iestatīšanas vednis

Lai noliktavā ātri izveidotu novietojumus, varat izmantot vedni **Novietojuma iestatīšana**. Kā daļu no šī procesa varat ērti uzturēt novietojumu nosaukumu formātu.

## <a name="warehouse-processes"></a>Noliktavas procesi
Kā daļa no noliktavas konfigurēšanas ir svarīgi noliktavas procesus iespējot atbilstoši biznesa vajadzībām. Vissvarīgākie komponenti, kas jums ir jākonfigurē, ir kopumu veidnes, darbu veidnes, darbu pūli un novietojumu direktīvas.

### <a name="wave-templates"></a>Kopumu veidnes

Kopumu veidnes jums palīdz iespējot izejošo procesu “Pārvietot uz noliktavu”. Tiklīdz pasūtījuma rindas tiek izlaistas (vai nu tieši no pirmdokumentiem, izmantojot pakešuzdevumu procesus vai noslodzes, kas jau ir izveidotas), tiek izmantota kopumu veidnes funkcionalitāte. 

Varat izveidot trīs tālāk norādīto tipu kopuma veidnes. 
-   **Nosūtīšana**
-   **Ražošanas pasūtījums**
-   **Kanban** 

Parametri tiek izmantoti, lai noteiktu, cik tālu sistēmai ir automātiski jāiet, apstrādājot izejošo darbu. Kopuma veidne tiek atlasīta, balstoties uz kopuma veidnes secību un kritērijiem, kas ir noteikti šajā veidnē. Ja veidne ir uzskaitīta secības augšpusē, kritēriji šajā veidnē tiek pārbaudīti vispirms. Ja kritēriji ir izpildīti, šī kopuma veidne tiek apstrādāta. Pretējā gadījumā tiek pārbaudīti kritēriji nākamajā veidnē, un tā tālāk. Tādēļ veidni, kurā ir visspecifiskākie kritēriji, ieteicams novietot kopumu veidņu secības saraksta augšpusē, lai tā tiktu apstrādāta vispirms. Piemēram, jūs šodien vēlaties apstrādāt visu darbu attiecībā uz kādu noteiktu pārvadātāju un īslaicīgi aizkavēt darba apstrādi citiem pārvadātājiem. Tādā gadījumā kopumu veidnei, kas atlasa darbu šim pārvadātājam, secībā ir jāatrodas augstāk par citām veidnēm. Pretējā gadījumā var tikt apstrādāts darbs citiem pārvadātājiem, pirms ir pabeigts darbs šim pārvadātājam. 

Katrā kopumu veidnē jums ir jānorāda kopumu apstrādes metodes. Pieejamās metodes ir atkarīgas no kopumu veidnes tipa.

### <a name="work-templates"></a>Darbu veidnes

Darbu veidņu definīcijām ir svarīga loma noliktavas pārvaldības darbu procesu definēšanā. Tās nosaka, kāds darbs tiek veikts un kā šis darbs tiek izpildīts. Veidnes var arī ietvert direktīvu kodu, kas saista ar novietojuma direktīvu, lai noteiktu, kur darbs tiek veikts. Darbu veidnes ietver vaicājumu, kas norāda darbu kritērijus. Katrā veidnē ir jāiekļauj vismaz viena izdošanas operācija un viena izvietošanas operācija, lai vadītu pamata darba operāciju rīcībā esošo krājumu nodošanai no viena novietojuma uz citu. 

Ja vairākiem darbiniekiem ir jāspēj apstrādāt darbu kādām no jūsu noliktavas operācijām, tad krājumiem var noderēt jēdziena *sagatavošanas posmi* izmantošana un atsevišķa darbu izpildes dažādās darba klasēs.

### <a name="work-pools"></a>Darbu pūli

Darbu pūli tiek izmantoti, lai organizētu darba grupās. Piemēram, varat izveidot darbu kopu, lai klasificētu konkrētas noliktavas atrašanās vietā notiekošos darbus. Visu darbu veidu, izņemot inventarizācijas, gadījumā darbu kopu var piešķirt darbu veidnei. Cikla inventarizācijas gadījumā darbu pūlu varat piešķirt tālāk norādītajām lapām.

-   Cikla inventarizācijas plāni
-   Cikla inventarizācijas robežvērtības
-   Cikla inventarizācijas darbs pēc novietojuma
-   Cikla inventarizācijas darbs pēc krājuma

Kad darba izveidei izmantojat darba veidnes, darbam automātiski tiek piešķirta darbu kopa. 

Darbu pūla ID var izmantot arī, lai ierobežotu darbu tipu, kāds ir vērsts uz noteiktu noliktavas darbinieku, ja vien šī funkcionalitāte ir konfigurēta attiecīgajā mobilās ierīces izvēlnes vienumā.

### <a name="location-directives"></a>Novietojuma direktīvas

Kā liecina nosaukums, novietojuma direktīvas tiek izmantotas, lai darbu transakcijas noliktavā virzītu uz atbilstošajiem novietojumiem. Citiem vārdiem sakot, tās nosaka, kur izdot un izvietot. 

Lai varētu vieglāk un ātrāk definēt darbības, kas ir saistītas ar katru novietojuma direktīvas rindu, izmantojiet kādu no iepriekš definētajām stratēģijām. Piemēram, varat izmantot stratēģiju **Tukšs novietojums bez ienākoša darba**, lai noliktavā meklētu brīvus novietojumus, vai izmantot stratēģiju **FEFO partijas rezervēšana** izejošajai pārdošanas izdošanai.

<a name="additional-resources"></a>Papildu resursi
--------

[Vietu konfigurēšana noliktavā ar iespējotu WMS](tasks/configure-locations-wms-enabled-warehouse.md)



