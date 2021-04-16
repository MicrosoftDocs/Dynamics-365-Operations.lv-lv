---
title: Kvalitātes pārbaude
description: Šajā tēmā ir sniegta informācija par Kvalitātes pārbaudes līdzekli. Šis līdzeklis ļauj noliktavas darbiniekiem ātri veikt pārbaudes uz vietas, kamēr tie saņem krājumus saņemšanas doka zonā.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 60d566e3ef1fa4bc0cea960f7c75094f51823550
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838230"
---
# <a name="quality-check"></a>Kvalitātes pārbaude

[!include [banner](../includes/banner.md)]

*Kvalitātes pārbaudes* līdzeklis ļauj noliktavas darbiniekiem ātri veikt pārbaudes uz vietas, kamēr tie saņem krājumus saņemšanas doka zonā. Šīs vietas pārbaudes ir noderīgas, kad darbinieki pārbauda iepakojumu vai citas viegli atpazīstamas krājuma daļas. Šī funkcija palīdz darbiniekiem ātri apskatīt, vai kaut kas nav acīmredzami kļūdains vai sabojāts, pirms viņi krājumu novieto tā paredzētajā vietā.

Šis līdzeklis ir alternatīva standarta kvalitātes pārbaudes procesam. Tas piedāvā lielāku elastību un ātrāku apstrādi.

Izmantojot šo funkciju, saņemšanas un kvalitātes pārbaude notiek šādi:

1. Kad sūtījums pienāk, noliktavas darbinieks reģistrē saņemšanu. Darbinieks arī noskenē numura zīmi, lai reģistrētu atrašanās vietu.
1. Darbinieks veic ātro kvalitātes pārbaudi un ieraksta rezultātu (izdošana vai kļūme) šai numura zīmei.
1. Notiek viena no sekojošajām darbībām:

    - Ja kvalitātes pārbaude ir nokārtota, numura zīme tiek pieņemta un aizvadīta uz saņemšanas vietu kā parasti.
    - Ja kvalitātes pārbaude neizdodas, numura zīme tiek noraidīta, un esošais izvietošanas darbs tiek novirzīts uz alternatīvo atrašanās vietu turpmākai pārbaudei. Tiek izveidots jauns kvalitātes pasūtījums. Lai skatītu kvalitātes pasūtījumu, kas izveidots no neizdevušās kvalitātes pārbaudes, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pasūtījumi**.

Šo procesu var arī iestatīt tā, lai visas skenētās numura zīmes tiktu nekavējoties novirzītas uz kvalitātes pārbaudes atrašanās vietu.

## <a name="turn-on-the-quality-check-feature"></a>Ieslēgt kvalitātes pārbaudes līdzekli

Lai varētu izmantot *Kvalitātes pārbaudes* līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Kvalitātes pārbaude*

## <a name="set-up-the-feature-for-the-example-scenario"></a>Iestatīt līdzekli piemēra scenārijam

Šajā sadaļā ir sniegti norādījumi un piemērs, kas parāda, kā iestatīt *Kvalitātes pārbaudes* funkciju un sagatavot parauga datus piemēru scenārijam, kas sniegts tālāk šajā tēmā.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo [scenārija piemēru](#example-scenario), strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

### <a name="quality-check-template"></a><a name="quality-template"></a>Kvalitātes pārbaudes veidne

Kvalitātes pārbaudes veidne definē noteikumus, lai veiktu ātro pārbaudi uz vietas kvalitātes saņemšanas laikā.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Kvalitātes pārbaudes veidne**.
1. Atlasiet **Jauns**, lai režģim pievienotu veidni.
1. Definējot jauno veidni, iestatiet šādas vērtības:

    - **Kvalitātes pārbaudes veidnes nosaukums:** *Doka pārbaude*

        Ievadiet nosaukumu, kas identificē šai veidnei piemērotās politikas.

    - **Pieņemšanas politika:** *Uzvedne lietotājam*

        Norādiet, vai lietotājiem ir jāsaņem uzvedne, lai pieņemtu vai noraidītu krājumu kvalitāti, kamēr tie apstrādā darbu, vai arī kvalitāte automātiski tiks noraidīta. Pieejamās opcijas ir *Automātiska noraidīšana* un *Uzvedne lietotājam*.

    - **Kvalitātes apstrādes politika:** *Izveidot kvalitātes pasūtījumu*

        Atlasiet politiku, kas jāizmanto, kad krājumu kvalitāte tiek noraidīta. Pieejamas šādas opcijas

        - *Izveidot tikai darbu* - vienkārši izveidojiet darbu, lai atvieglotu krājumu kustību.
        - *Izveidot kvalitātes pasūtījumu* - izveidojiet kvalitātes pasūtījumu, lai atvieglotu kvalitātes testus.

    - **Testa grupa:** *Norobežojums*

        Norādiet testu grupu, kas jāizmanto izveidotajā kvalitātes pasūtījumā. Testu grupas ir iestatītas **Krājumu pārvaldības** modulī.

        Atstājiet opciju **Destruktīvais teksts** testa grupai izslēgtu. Šī opcija definē, vai paraugs tiks iznīcināts kā daļa no testiem testu grupas ietvaros. Ja tiek izmantots desktruktīvais tests, sistēma veido krājumu darbību, kad krājumam tiek izveidots kvalitātes pasūtījums. Jaunā krājumu darbība prognozē testa daudzuma krājumu samazināšanos. Krājumu samazināšana notiek, kad kvalitātes pasūtījums tiek pabeigts, izmantojot validācijas soli. Krājumu darbība tiek identificēta kā kvalitātes pasūtījums.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Darba klase - Kvalitātes pārbaude

Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu tipu, ko noliktavas darbinieki var apstrādāt mobilajā ierīcē.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.
1. Atlasiet **Jauns**, lai izveidotu darba klasi.
1. Galvenē iestatiet šādas vērtības:

    - **Darba klases ID:** *QC pārbaude*

        Ievadiet nosaukumu, kas identificē darba klasi.

    - **Apraksts:** *QC pārbaude*

        Ievadiet īsu aprakstu, kas norāda, kam tiek lietota darba klase.

    - **Darba pasūtījuma tips:** *Kvalitātes pārbaudes kvalitāte*

        Atlasiet darba klases izveidoto darba pasūtījumu tipu. Iestatot kvalitātes kontroles darbu, vienmēr atlasiet *Kvalitātes pārbaudes kvalitāti*.

1. Kopsavilkuma cilnē **Derīgs novietojuma tips** atstājiet **Atrašanās vietas veida** lauku tukšu.

    Ja atlasāt atrašanās vietas tipu, tiek ierobežotas vietas, kur krājumus var ievietot pēc to izdošanas. Šis lauks tiek izmantots, kad novietojuma direktīva mēģina atrisināt novietojumu vai kad noliktavas darbinieks manuāli precizē mobilās ierīces izvēlnes elementa novietojumu.

Lai iegūtu vairāk informācijas par darba klasēm un to izveidi, skatiet sadaļu [Izveidot darba klasi](tasks/create-work-class.md).

### <a name="work-template"></a>Darba veidne

Darbu veidnes ļauj jums definēt darba operācijas, kas jāveic noliktavā. Parasti, noliktavas darba operācijas sastāv no darbību pāra: noliktavas darbinieks paņem rīcībā esošos krājumus vienā novietojumā un pēc tam liek paņemtos krājumus citā novietojumā. Kvalitātes kontroles darba veidne nosaka darba operācijas kvalitātes pārbaužu veikšanai.

#### <a name="purchase-orders"></a>Pirkšanas pasūtījumi

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Galvenē iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumi*.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Atlasiet darba veidni, kurai jāietver kvalitātes pārbaudes darbība. Sadaļā **Pārskats**, kas atrodas laukā **Darba veidnes**, atlasiet *51 PO kvīti*.
1. Sadaļā **Darba veidnes detaļas** ievērojiet, ka režģim ir divas esošas rindas: viena *Saņemšanai* un viena *Izvietošanai*.
1. Sadaļā **Darba veidnes detaļas** atlasiet **Jauns**, lai režģim pievienotu kvalitātes kontroles rindu. Ievērojiet, ka **Rindas numura** lauks jaunajai rindai ir iestatīts uz *3*.
1. Jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.

    - **Darba tips:** *Kvalitātes pārbaude*
    - **Darba klases ID:** *Pirkums*
    - **Kvalitātes pārbaudes veidnes nosaukums:** *Doka pārbaude*

        Atlasiet darba klases unikālo ID. Šo vērtību izmantojat, lai konfigurētu izvēlnes elementus mobilajā ierīcē un darba veidus, kuru var apstrādāt šīs izvēlnes elementi.

1. Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jūsu darbu līdz šim.

    Jūs saņemat informatīvu ziņojumu, kurā teikts: "Nederīgs - Kvalitātes pārbaudei ir jābūt tieši pēc saņemšanas." Tāpēc **Rindas numura** vērtība ir jāmaina tikko pievienotajai rindai.

1. Lai mainītu **Rindas numura** vērtību jaunajai rindai, rīkojieties šādi:

    1. Sadaļā **Darba veidnes detaļas** atlasiet rindu, kur **Darba tipa** lauks ir iestatīts uz *Kvalitātes pārbaude*.
    2. Atlasiet pogu **Pārvietot uz augšu** vai uz **Pārvietot uz leju**, lai pārvietotu *Kvalitātes pārbaudes* rindu tā, lai tā būtu pēc *Saņemšanas* rindas.

1. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="quality-in-quality-check"></a>Kvalitāte kvalitātes pārbaudē

Pēc tam izveidojiet darba veidni kvalitātes pārbaudei.

1. Lapas **Darba veidnes** virsrakstā mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kvalitāte kvalitātes pārbaudē*.
1. Lai režģim sadaļā **Pārskats** pievienotu rindu, darbības rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba veidne:** *51 kvalitātes pārbaude*

        Ievadiet veidnes nosaukumu.

    - **Darba veidnes apraksts:** *51 kvalitātes pārbaude*

1. Darbības rūtī atlasiet **Saglabāt**, lai padarītu pieejamu sadaļu **Darba veidnes informācija**.
1. Kamēr jaunā veidne joprojām ir atlasīta sadaļā **Pārskats**, atlasiet **Jauns** sadaļā **Darba veidnes informācija**, lai režģī pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba veids:** *Izdošana*
    - **Darba klases ID:** *QC pārbaude*

        Atlasiet [Darba klases](#work-class) nosaukumu, ko izveidojāt iepriekš kvalitātes kontroles darbam.

1. Sadaļā **Darba veidnes informācija** atlasiet **Jauns**, lai pievienotu citu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba veids:** *Izvietošana*
    - **Darba klases ID:** *QC pārbaude*

        Atlasiet [Darba klases](#work-class) nosaukumu, ko izveidojāt iepriekš kvalitātes kontroles darbam.

1. Darbību rūtī atlasiet **Saglabāt**.

Plašāku informāciju par darbu veidnēm skatiet sadaļā [Noliktavas darbu kontrolēšana, izmantojot darba veidnes un novietojuma direktīvas](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Novietojuma direktīva — kvalitātes kļūmes

Novietojuma direktīvas ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Piemēram, pārdošanas pasūtījuma transakcijā novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti. Jums ir jākonfigurē novietojuma direktīvas kārtula, lai noteiktu, kā tiek apstrādātas neveiksmīgas kvalitātes pārbaudes.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisās puses rūtī iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumiem*, lai strādātu ar šāda veida atrašanās vietas direktīvām.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma direktīvu kvalitātes pārbaudēm.
1. Galvenē iestatiet šādas vērtības:

    - **Kārtas numurs:** akceptējiet noklusējuma vērtību.
    - **Nosaukums:** *51 uz kvalitāti*

1. Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.

    - **Darba veids:** *Izvietošana*
    - **Vieta:** *5*
    - **Noliktava:** *51*

1. Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jūsu direktīvu un padarītu kopsavilkuma cilni **Rindas** pieejamu.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.

    - **No daudzuma:** *1*
    - **Līdz daudzumam:** *1 000 000*

1. Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jauno rindu un padarītu kopsavilkuma cilni **Novietojuma direktīvas darbības** pieejamu.
1. Kamēr jaunā rinda joprojām ir atlasīta kopsavilkuma cilnē **Rindas** atlasiet **Jauns** kopsavilkuma cilnē **Novietojuma direktīvas darbības**, lai režģī pievienotu rindu, tādējādi rindai var iestatīt darbību.
1. Jaunā rindā iestatiet **Nosaukums** lauku uz *Kvalitāte*. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.
1. Darbības rūtī atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** pieejamu **Novietojuma direktīvu darbības** kopsavilkuma cilnē.
1. Kamēr tikko pievienotā rinda joprojām ir atlasīta kopsavilkuma cilnē **Novietojuma direktīvas darbības**, atlasiet **Rediģēt vaicājumu**, lai atvērtu dialoglodziņu, kur varat rediģēt vaicājumu darbībai.
1. Cilnē **Diapazons** atlasiet **Pievienot**, lai vaicājumam pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Atvasinātā tabula:** *Vietas*
    - **Lauks:** *Novietojums*
    - **Kritēriji:** *KPS*

    *QMS* atrašanās vieta ir noliktavas atrašanās vieta kvalitātei.

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Jums tūlīt ir jānomaina pirkšanas pasūtījuma novietojuma direktīvu secība noliktavai *51*. Saglabājiet jauno *51 uz kvalitāti* novietojuma direktīvu, atsvaidziniet lapu un sarakstā atlasiet atrašanās vietas direktīvu. Pēc tam darbības rūtī izmantojiet pogas **Pārvietot uz augšu** un uz **Pārvietot uz leju**, lai novietojuma direktīvu ievietotu noliktavai *51* šādā secībā. (Pirms atlasāt **Pārvietot uz augšu** vai uz **Pārvietot uz leju**, sarakstā atlasiet atrašanās vietas direktīvu.)

    1. 51 uz kvalitāti
    2. 51 PO tiešais
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumi

Konfigurējiet izvēlnes elementu, lai mobilās ierīces varētu veikt **Kvalitātes pārbaudes** funkciju.

#### <a name="purchase-putaway"></a>Pirkuma izvietošana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Sarakstā atlasiet **Pirkšanas izvietošana** izvēlnes krājumu.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Sadaļā **Darba klases** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba klases ID:** *QC pārbaude*

        Ievadiet [Darba klases](#work-class) nosaukumu, ko izveidojāt iepriekš kvalitātes kontroles darbam.

    - **Darba pasūtījuma tips:** *Kvalitātes pārbaudes kvalitāte*

1. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="purchase-order-line-receiving"></a>Pirkšanas pasūtījuma rindas saņemšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Izvēlnes elementa nosaukums:** *PO rindas saņemšana*
    - **Nosaukums:** *PO rindas saņemšana*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Nē*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.

    - **Darba izveides process:** *Pirkšanas pasūtījuma rindas saņemšana un nosūtīšana*
    - **Ģenerēt numura zīmi:** *Jā*
    - **Darba veidne:** *51 PP kvīts*

1. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Izvēlnes elementa pievienošana mobilās ierīces izvēlnei

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Kreisajā rūtī atlasiet izvēlni **Ienākošie**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kolonnā **Pieejamās izvēlnes un izvēlņu elementi** atrodiet jaunu **PP rindas saņemšanas** izvēlnes elementu.
1. Atlasiet bultiņas pa labi pogu, lai pārvietotu **PP rindas saņemšana** uz kolonnu **Izvēlnes struktūra**.
1. Kolonnā **Izvēlnes struktūra** atlasiet **PP rindas saņemšanu** un atlasiet augšupvērsto un lejupvērsto bultiņu, lai pārvietot izvēlnes elementu uz vēlamo pozīciju mobilās lietotnes izvēlnē.
1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Piemēra situācija

Pēc tam, kad esat veicis visus iepriekš aprakstītos, pieejamos parauga datus un to iestatījis, varat strādāt ar šo scenāriju, lai izmēģinātu *Kvalitātes pārbaudes* funkciju. Šajā scenārijā parādītās vērtības pieņem, ka strādājat ar standarta demonstrācijas datiem, ar kuriem atlasījāt **USMF** juridisko personu un ka sagatavojāt parauga ierakstus, kas ir aprakstīti iepriekš šajā tēmā. Šis scenārijs kalpo arī kā piemērs, kas parāda, kā līdzekli var izmantot ražošanas iestatījumā.

### <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

1. Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:

    - **Tirgotāja konts:** *104*
    - **Noliktava:** *51*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu un atvērtu jaunu pirkšanas pasūtījumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** režģim tiek pievienota jauna, tukša rinda. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *M9203*
    - **Daudzums:** *3*
    - **Vienība:** *PL*

1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="process-quality-check-receiving"></a>Apstrādāt kvalitātes pārbaudes saņemšanu

Pēc tam, kad pirkšanas pasūtījums ir izveidots, to var saņemt, izmantojot **PP rindas saņemšanas** izvēlnes elementu un *Kvalitātes pārbaudes* funkciju.

#### <a name="receive-pallet-1"></a>Saņemt paletes 1

1. Pierakstieties Warehouse Management mobile programmā kā lietotājs noliktavā *51*. (Ievadiet *51* kā lietotāja ID un *1* kā paroli.)
1. Dodieties uz **Ienākošie \> PP rindas saņemšana**.
1. Laukā **PONUM** ievadiet savu pirkuma pasūtījuma numuru.
1. Apstipriniet pirkšanas pasūtījumu numuru.
1. Laukā **LINENUM** ievadiet pirkšanas pasūtījuma rindas numuru, kas tiek saņemts. Tā kā pasūtījumam šajā scenārijā ir tikai viena rinda, jums jāievada *1* laukā **LINENUM** katram saņemšanas solim.
1. Apstipriniet rindas numuru.
1. Ievadiet saņemto daudzumu laukā **DAUDZ.**. Tā kā pirkšanas pasūtījums ir paredzēts trīs paletēm (*PL*) šajā scenārijā, un ir trīs saņemšanas soļi, jūs ievadīsiet *1* laukā **DAUDZ.** katrai saņemšanas darbībai.
1. Apstipriniet daudzumu.

    Lapā **Kvalitātes pārbaude**, kas parādās, nav ierakstu lauku. Tam ir tikai apstiprinājuma (atzīme) poga apakšā un izvēlnes poga (**≡**) augšā. (Izvēlnes poga dažreiz tiek saukta par hamburgeru vai hamburgeru pogu.) Lai paātrinātu kvalitātes pārbaudes procesu, kad palete iztur kvalitātes pārbaudi, lietotājs vienkārši apstiprina **Kvalitātes pārbaudes** lapu.

    ![Kvalitātes pārbaudes lapa](media/quality-check.png "Kvalitātes pārbaudes lapa")

1. Izvēlieties apstiprināšanas pogu, lai nokārtotu kvalitātes pārbaudi paletei 1 no 1. rindas.

    **Pirkšanas pasūtījumi: Izvietot** lapa parāda detalizētu informāciju par izvietošanas darbu:

    - **LOC:** sistēmas noteiktā atrašanās vieta

        Šī atrašanās vieta ir norādītā izvietošanas vieta pirkšanas pasūtījuma saņemšanai.

    - **LP:** sistēmas ģenerētais numura zīmes ID
    - **Krājums:** *M9203*
    - **Daudzums:** *1 PL: 100 ea*

    Tiek norādīts arī krājuma apraksts.

1. Apstipriniet izvietošanas darbu.

    Lapā **Uzdevums** pirkšanas pasūtījuma rindas saņemšanai jūs saņemsiet ziņojumu "Darbs pabeigts". Lauks **LINENUM** ir pieejams, lai varētu sākt saņemt nākamo paleti.

#### <a name="receive-pallet-2"></a>Saņemt paletes 2

Šim scenārijam palete 2 tiks noraidīta.

1. Laukā **LINENUM** ievadiet *1* un apstipriniet rindas numuru.
1. Lauks **DAUDZ.** tagad ir pieejams. Ievadiet *1* un apstipriniet daudzumu.

    Tiek parādīta lapa **Kvalitātes pārbaude**. Šai kvīts paletei kvalitāte tiks noraidīta, un tā tiks ievietota *QMS* kvalitātes novietojumā.

1. Lapas augšā atlasiet izvēlnes pogu (**≡**), un pēc tam izvēlnē atlasiet **Noraidīt**.
1. Parādītajā lapā **Uzdevums** ievadiet **QMS** kā *Izvietot* novietojumu, lai nosūtītu paletes tālākai pārbaudei.

    **Kvalitāte kvalitātes pārbaudē: Izvietot** lapa parāda detalizētu informāciju par izvietošanas darbu:

    - **LOC:** *QMS*

        Šī atrašanās vieta ir norādītā izvietošanas vieta noraidītai kvalitātes saņemšanai.

    - **LP:** sistēmas ģenerētais numura zīmes ID
    - **Krājums:** *M9203*
    - **Daudzums:** *1 PL: 100 ea*

    Tiek norādīts arī krājuma apraksts.

1. Apstipriniet izvietošanas darbu.

    Lapā **Uzdevums** pirkšanas pasūtījuma rindas saņemšanai jūs saņemsiet ziņojumu "Darbs pabeigts". Lauks **LINENUM** ir pieejams, lai varētu sākt saņemt nākamo paleti.

Tagad jūs esat pabeiguši kvalitātes pārbaudi un izveidojis kvalitātes pasūtījumu noraidītajai paletei. Lai skatītu izveidoto kvalitātes pasūtījumu, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pasūtījumi**.

Kvalitātes pasūtījumu pārbaudes tagad var apstrādāt. Šajā tēmā nav iekļauta kvalitātes testēšana.

Papildinformāciju par kvalitātes pārvaldību skatiet [Pārskats par kvalitātes pārvaldību](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Saņemt paletes 3

Šim scenārijam palete 3 tiks pieņemta.

1. Laukā **LINENUM** ievadiet *1* un apstipriniet rindas numuru.
1. Lauks **DAUDZ.** tagad ir pieejams. Ievadiet *1* un apstipriniet daudzumu.

    Tiek parādīta lapa **Kvalitātes pārbaude**. Šai kvīts paletei kvalitāte tiks pieņemta, un tā tiks ievietota vairuma izvietošanas novietojumā.

1. Izvēlieties apstiprināšanas pogu, lai nokārtotu kvalitātes pārbaudi.

    **Pirkšanas pasūtījumi: Izvietot** lapa parāda detalizētu informāciju par izvietošanas darbu:

    - **LOC:** sistēmas noteiktā atrašanās vieta

        Šī atrašanās vieta ir norādītā izvietošanas vieta pirkšanas pasūtījuma saņemšanai.

    - **LP:** sistēmas ģenerētais numura zīmes ID
    - **Krājums:** *M9203*
    - **Daudzums:** *1 PL: 100 ea*

    Tiek norādīts arī krājuma apraksts.

1. Apstipriniet izvietošanas darbu.

    Lapā **Uzdevums** pirkšanas pasūtījuma rindas saņemšanai jūs saņemsiet ziņojumu "Darbs pabeigts". Lauks **LINENUM** ir pieejams, lai varētu sākt saņemt nākamo paleti.

1. Lapas augšā atlasiet izvēlnes pogu (**≡**), un pēc tam izvēlnē atlasiet **Atcelt**, lai atgrieztos izvēlnē.

Tagad varat aizvērt mobilo programmu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]