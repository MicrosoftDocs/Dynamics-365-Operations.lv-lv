---
title: Commerce kanālu finanšu integrācijas iestatīšana
description: Šajā tēmā ir sniegti norādījumi par finanšu integrācijas funkcionalitātes iestatīšanu Commerce kanāliem.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b221bfede5d1db8d7970e1efede85e8dba7fe017
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413930"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce kanālu finanšu integrācijas iestatīšana

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Ievads

Šajā tēmā ir sniegti norādījumi par finanšu integrācijas funkcionalitātes iestatīšanu Commerce kanāliem. Plašāku informāciju par finanšu integrāciju skatiet tēmā [Apskats par Commerce kanālu finanšu integrāciju](fiscal-integration-for-retail-channel.md).

Finanšu integrācijas iestatīšanas procedūra ietver šādus uzdevumus:

1. Konfigurēt finanšu savienotājus, kas apzīmē finanšu ierīces vai pakalpojumus, kurus izmanto finanšu reģistrācijas nolūkiem, piemēram, fiskālos printerus.
2. Konfigurēt dokumentu nodrošinātājus, kas izveido finanšu dokumentus, kurus finanšu savienotāji reģistrēs finanšu ierīcēs vai pakalpojumos.
3. Konfigurēt finanšu reģistrācijas procesu, kas nosaka finanšu reģistrācijas darbību secību un finanšu savienotājus un finanšu dokumentu nodrošinātājus, ko izmanto katrai darbībai.
4. Piešķirt finanšu reģistrācijas procesus pārdošanas punkta (POS) funkcionalitātes profiliem.
5. Piešķirt savienotāja tehniskos profilus aparatūras profiliem.

## <a name="set-up-a-fiscal-registration-process"></a>Finanšu reģistrācijas procesa iestatīšana

Pirms sākat lietot finanšu integrācijas funkcionalitāti, būtu jākonfigurē tālāk norādītie iestatījumi.

1. Commerce parametru atjaunināšana.

    1. Lapas **Commerce koplietojamie parametri** cilnē **Vispārīgi** iestatiet opcijai **Iespējot finanšu integrāciju** vienumu **Jā**. Cilnē **Numuru sērijas** definējiet numuru sērijas šādām atsaucēm:

        - Finanšu tehniskā profila numurs
        - Finanšu savienotāja grupas numurs
        - Reģistrācijas procesa numurs

    2. Lapā **Commerce parametri** definējiet numuru sēriju finanšu funkcionālā profila numuram.

    > [!NOTE]
    > Numuru sērijas nav obligātas. Numurus visiem finanšu integrācijas elementiem var izveidot, izmantojot numuru sērijas vai manuāli.

2. Augšupielādējiet finanšu savienotāju un finanšu dokumentu nodrošinātāju konfigurācijas.

    Finanšu dokumentu nodrošinātājs ir atbildīgs par finanšu dokumentu sagatavošanu, kuri norāda transakcijas un notikumus, kas reģistrēti POS, tādā formātā, kas tiek izmantots arī mijiedarbībai ar finanšu ierīci vai pakalpojumu. Piemēram, finanšu dokumentu nodrošinātājs var izveidot finanšu dokumenta attēlojumu XML formātā.

    Finanšu savienotājs ir atbildīgs par saziņu ar finanšu ierīci vai pakalpojumu. Piemēram, finanšu savienotājs var nosūtīt finanšu dokumentu, kuru izveidoja finanšu dokumentu nodrošinātājs XML formātā, uz fiskālo printeri. Plašāku informāciju par finanšu integrācijas komponentiem skatiet tēmā [Finanšu reģistrācijas process un finanšu integrācijas paraugi finanšu ierīcēm](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Lapā **Finanšu savienotāji** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu savienotāji**) augšupielādējiet XML konfigurāciju katrai ierīcei vai pakalpojumam, ko plānojat izmantot finanšu integrācijas nolūkos.

        > [!TIP]
        > Atlasot **Skatīt**, varat skatīt visus funkcionālos un tehniskos profilus, kas ir saistīti ar pašreizējo finanšu savienotāju.

    2. Lapā **Finanšu dokumentu nodrošinātāji** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu dokumentu nodrošinātāji**) augšupielādējiet XML konfigurāciju katrai ierīcei vai pakalpojumam, ko plānojat izmantot.

        > [!TIP]
        > Atlasot **Skatīt**, varat skatīt visus funkcionālos profilus, kas ir saistīti ar pašreizējo finanšu dokumentu nodrošinātāju.

    Finanšu savienotāju un finanšu dokumentu nodrošinātāju konfigurāciju piemērus skatiet tēmā [Finanšu integrācijas paraugi komplektā Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Datu kartēšana tiek uzskatīta par daļu no finanšu dokumentu nodrošinātāja. Lai iestatītu citus datu kartējumus tam pašam savienotājam (piemēram, ja pastāv valstij raksturīgi noteikumi), jums vajadzētu izveidot dažādus finanšu dokumentu nodrošinātājus.

3. Izveidojiet savienotāja funkcionālos profilus un savienotāja tehniskos profilus.

    1. Lapā **Savienotāja funkcionālie profili** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Savienotāja funkcionālie profili**) izveidojiet savienotāja funkcionālo profilu katrai finanšu savienotāja un ar šo finanšu savienotāju saistītā finanšu dokumentu nodrošinātāja kombinācijai.

        1. Atlasiet savienotāja nosaukumu.
        2. Atlasiet kādu dokumentu nodrošinātāju.

        Varat mainīt datu kartēšanas parametrus savienotāja funkcionālajā profilā. Lai atjaunotu noklusētos parametrus, kas definēti finanšu dokumentu nodrošinātāja konfigurācijā, atlasiet **Atjaunināt**.

        **Piemēri**

        |   | Formāts | Paraugs |
        |---|--------|---------|
        | **PVN likmju iestatījumi** | value : VATrate | 1 : 2000, 2 : 1800 |
        | **PVN kodu kartējums** | VATcode : value | vat20 : 1, vat18 : 2 |
        | **Norēķinu tipu kartējums** | TenderType : value | Cash : 1, Card : 2 |

        > [!NOTE]
        > Savienotāja funkcionālie profili attiecas tikai uz konkrētu uzņēmumu. Ja plānojat izmantot to pašu finanšu savienotāja un finanšu dokumentu nodrošinātāja kombināciju dažādos uzņēmumos, ir jāizveido savienotāja funkcionālais profils katram uzņēmumam.

    2. Lapā **Savienotāja tehniskie profili** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Savienotāja tehniskie profili**) izveidojiet savienotāja tehnisko profilu katram finanšu savienotājam.

        1. Atlasiet savienotāja nosaukumu.
        2. Atlasiet kādu savienotāja tipu. Ierīcēm, kas ir savienotas ar aparatūras staciju, atlasiet vienumu **Vietējais**.

            > [!NOTE]
            > Pašlaik tiek atbalstīti tikai vietējie savienotāji.

        Parametrus savienotāja tehniskā profila cilnēs **Ierīces** un **Iestatījumi** var mainīt. Lai atjaunotu noklusētos parametrus, kas definēti finanšu savienotāja konfigurācijā, atlasiet **Atjaunināt**. Ielādējot XML konfigurācijas jaunu versiju, tiek parādīts ziņojums, ka pašreizējais finanšu savienotājs vai finanšu dokumentu nodrošinātājs jau tiek izmantots. Šī procedūra nepārlabo manuālās izmaiņas, kas iepriekš veiktas savienotāja funkcionālajos profilos un savienotāja tehniskajos profilos. Lai lietotu noklusējuma parametru kopu no jaunas konfigurācijas, atlasiet vienumu **Atjaunināt** lapā **Savienotāja funkcionālie profili** vai lapā **Savienotāja tehniskie profili**.

4. Izveidojiet finanšu savienotāju grupas.

    Savienotāju grupā ir apvienoti tādu finanšu savienotāju funkcionālie profili, kuri veic identiskas funkcijas un finanšu reģistrācijas procesā tiek izmantoti tajā pašā darbībā. Piemēram, ja vairākus fiskālo printeru modeļus var izmantot veikalā, finanšu savienotājus šiem fiskālajiem printeriem var apvienot finanšu savienotāju grupā.

    1. Lapā **Finanšu savienotāju grupa** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu savienotāju grupas**) izveidojiet jaunu finanšu savienotāju grupu.
    2. Pievienojiet funkcionālos profilus savienotāju grupai. Cilnē **Funkcionālie profili** atlasiet vienumu **Pievienot** un atlasiet kādu profila numuru. Katram finanšu savienotājam noteiktā savienotāju grupā var būt tikai viens funkcionālais profils.
    3. Lai pārtrauktu attiecīgā funkcionālā profila izmantošanu, opcijai **Atspējot** iestatiet vienumu **Jā**. Šīs izmaiņas ietekmē tikai pašreizējo savienotāju grupu. Varat turpināt tā paša funkcionālā profila izmantošanu citās savienotāju grupās.

5. Izveidojiet finanšu reģistrācijas procesu.

    Finanšu reģistrācijas procesu nosaka reģistrācijas darbību secība un katrā darbībā izmantotā savienotāju grupa.

    1. Lapā **Finanšu reģistrācijas process** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu reģistrācijas procesi**) izveidojiet jaunu ierakstu katram unikālajam finanšu reģistrācijas procesam.
    2. Pievienojiet procesam reģistrācijas darbības.

        1. Atlasiet **Pievienot**.
        2. Atlasiet finanšu savienotāja tipu.
        3. Laukā **Grupas numurs** atlasiet atbilstošo finanšu savienotāju grupu.

6. Piešķiriet finanšu reģistrācijas procesa elementus POS profiliem.

    1. Lapā **POS funkcionalitātes profili** (**Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**) piešķiriet finanšu reģistrācijas procesu POS funkcionalitātes profilam. Atlasiet **Rediģēt** un pēc tam cilnes **Finanšu reģistrācijas process** laukā **Procesa numurs** atlasiet procesu.
    2. Lapā **POS aparatūras profils** (**Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**) piešķiriet savienotāja tehnisko profilu aparatūras profilam. Atlasiet **Rediģēt**, pievienojiet rindu cilnē **Finanšu perifērijas ierīces** un pēc tam laukā **Profila numurs** atlasiet savienotāja tehnisko profilu.

    > [!NOTE]
    > Tam pašam aparatūras profilam varat pievienot vairākus tehniskos profilus. Tomēr aparatūras profilam vai POS funkcionalitātes profilam jābūt tikai vienam krustpunktam ar jebkuru finanšu savienotāju grupu.

    Finanšu reģistrācijas plūsmu nosaka finanšu reģistrācijas process, kā arī daži finanšu integrācijas komponentu parametri: paplašinājums Commerce Runtime finanšu dokumentu nodrošinātājam un paplašinājums Hardware Station finanšu savienotājam.

    - Abonēšana notikumiem un transakcijām finanšu reģistrācijā ir iepriekš definēta finanšu dokumentu nodrošinātājā.
    - Finanšu dokumentu nodrošinātājs ir atbildīgs arī par fiskālajai reģistrācijai izmantotā finanšu savienotāja identificēšanu. Tas atbilst savienotāja funkcionālajiem profiliem, kas ir iekļauti finanšu savienotāju grupā, kas ir norādīta finanšu reģistrācijas procesa pašreizējai darbībai ar savienotāja tehnisko profilu, kas ir piešķirts tādas aparatūras stacijas aparatūras profilam, ar kuru ir savienots pārī POS.
    - Finanšu dokumentu nodrošinātājs izmanto datu kartēšanas iestatījumus no finanšu dokumentu nodrošinātāja konfigurācijas, lai pārveidotu transakciju/notikumu datus, piemēram, nodokļus un maksājumus, kamēr tiek izveidots finanšu dokuments.
    - Ja finanšu dokumentu nodrošinātājs izveido finanšu dokumentu, finanšu savienotājs var to nosūtīt uz finanšu ierīci tādu, kāds tas ir, vai parsēt to un pārveidot par ierīces lietojumprogrammas interfeisa (API) komandu sēriju atkarībā no tā, kā tiek apstrādāti sakari.

7. Lapā **Finanšu reģistrācijas process** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu reģistrācijas procesi**) atlasiet vienumu **Validēt**, lai validētu finanšu reģistrācijas procesu.

    Ieteicams palaist šī tipa pārbaudes šādos gadījumos:

    - Pēc tam, kad ir pabeigti visi iestatījumi jaunam reģistrācijas procesam, tostarp piešķirot reģistrācijas procesus POS funkcionalitātes profiliem un aparatūras profiliem.
    - Pēc tam, kad veiktas esošā finanšu reģistrācijas procesa izmaiņas, un šīs izmaiņas var izraisīt cita finanšu savienotāja atlasi izpildes laikā (piemēram, mainot savienotāju grupu finanšu reģistrācijas procesa darbībai, iespējojot savienotāja funkcionālo profilu savienotāja grupā vai pievienojot jaunu savienotāja funkcionālo profilu savienotāja grupai).
    - Pēc izmaiņu veikšanas saistībā ar savienotāja tehnisko profilu piešķiri aparatūras profiliem.

8. Lapā **Sadales grafiks** palaidiet darbus **1070** un **1090**, lai pārsūtītu datus uz kanāla datu bāzi.

## <a name="set-up-fiscal-texts-for-discounts"></a>Atlaižu finanšu teksta iestatīšana

Dažos gadījumos uz finanšu dokumenta jādrukā īpašs teksts, ja tiek piemērota atlaide. Atlaižu finanšu tekstu var iestatīt lapā **Finanšu savienotāju grupa** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu savienotāju grupas**).

- Manuālām atlaidēm, kuras tiek piemērotas POS, jāiestata finanšu teksts informācijas kodam vai informācijas kodu grupai, kas POS funkcionalitātes profilā ir norādīti kā informācijas kods **Preces atlaide**.

    1. Lapā **Finanšu savienotāju grupa** atlasiet **Finanšu dokumenta teksts**.
    2. Cilnē **Informācijas kodi** atlasiet **Pievienot** un atlasiet informācijas kodu vai informācijas kodu grupu.
    3. Vienumam **Informācijas koda numurs** atlasiet vērtību.
    4. Laukā **Apakškoda numurs** atlasiet vērtību, ja apakškods ir nepieciešams atlasītajam informācijas kodam.
    5. Laukā **Finanšu dokumenta teksts** norādiet finanšu tekstu, kas jādrukā uz finanšu dokumenta.
    6. Iestatiet opcijai **Izdrukāt lietotāja ievadi finanšu dokumentā** vienumu **Jā**, lai pārlabotu tekstu uz finanšu dokumenta ar informāciju, ko lietotājs manuāli ievada POS. Šī opcija attiecas tikai uz informācijas kodiem, kuriem ir ievades veids **Teksts**.

    > [!NOTE]
    > Var norādīt finanšu tekstu vairākiem informācijas kodiem, lai nodrošinātu atbalstu scenārijiem, kuru ietvaros tiek izmantotas informācijas kodu grupas, saistīti informācijas kodi un aktivizēti informācijas kodi. Šajos scenārijos finanšu dokumentā būs ietverti finanšu teksti no visiem informācijas kodiem, kas ir saistīti ar transakcijas rindu, kurai tika piemērota atlaide.

- Kanālam raksturīgu atlaižu gadījumā ir jādefinē finanšu teksts atlaides ID.

    1. Lapā **Finanšu savienotāju grupa** atlasiet **Finanšu dokumenta teksts**.
    2. Cilnē **Atlaides** atlasiet **Pievienot** un atlasiet atlaides ID.
    3. Laukā **Finanšu dokumenta teksts** norādiet finanšu tekstu, kas jādrukā uz finanšu dokumenta.

    > [!NOTE]
    > Ja tai pašai transakcijas rindai tiek piemērotas vairākas atlaides, finanšu dokumentā būs ietverti finanšu teksti no visām atlaidēm, kuras ir saistītas ar attiecīgo transakcijas rindu.

## <a name="set-error-handling-settings"></a>Kļūdu apstrādes iestatījumu veikšana

Kļūdu apstrādes opcijas, kas pieejamas finanšu integrācijā, tiek iestatītas finanšu reģistrācijas procesā. Plašāku informāciju par kļūdu apstrādi finanšu integrācijā skatiet tēmā [Kļūdu apstrāde](fiscal-integration-for-retail-channel.md#error-handling).

1. Lapā **Finanšu reģistrācijas process** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu reģistrācijas procesi**) varat iestatīt šādus parametrus katrai finanšu reģistrācijas procesa darbībai:

    - **Atļaut izlaist** — šis parametrs iespējo opciju **Izlaist** kļūdu apstrādes dialoglodziņā.
    - **Atļaut atzīmēt kā reģistrētu** — šis parametrs iespējo opciju **Atzīmēt kā reģistrētu** kļūdu apstrādes dialoglodziņā.
    - **Kļūdas gadījumā turpināt** — ja šis parametrs ir iespējots, finanšu reģistrācijas process POS reģistrā var turpināties arī tad, ja transakcijas vai notikuma finanšu reģistrācija ir nesekmīga. Pretējā gadījumā, lai palaistu nākamās transakcijas vai notikuma finanšu reģistrāciju, operatoram ir atkārtot jāmēģina izpildīt nesekmīgo finanšu reģistrāciju, jāizlaiž šī reģistrācija vai attiecīgā transakcija vai notikums ir jāatzīmē kā reģistrēts. Plašāku informāciju skatiet rakstā [Neobligātā finanšu reģistrācija](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Ja ir iespējots parametrs **Kļūdas gadījumā turpināt**, parametrs **Atļaut izlaist** un parametrs **Atļaut atzīmēt kā reģistrētu** automātiski tiek atspējots.

2. Opcijām **Izlaist** un **Atzīmēt kā reģistrētu** kļūdu apstrādes dialoglodziņā ir nepieciešama atļauja **Atļaut izlaist reģistrāciju vai atzīmēt kā reģistrētu**. Tādēļ lapā **Atļauju grupas** (**Retail un Commerce \> Darbinieki \> Atļauju grupas**) ir jāiespējo atļauja **Atļaut izlaist reģistrāciju vai atzīmēt kā reģistrētu**.
3. Opcijas **Izlaist** un **Atzīmēt kā reģistrētu** ļauj operatoriem ievadīt papildu informāciju, kad finanšu reģistrācija neizdodas. Lai šī funkcionalitāte būtu pieejama, ir jānorāda informācijas kodi **Izlaist** un **Atzīmēt kā reģistrētu** finanšu savienotāju grupā. Pēc tam operatoru ievadītā informācija tiek saglabāta kā informācijas koda transakcija, kas saistīta ar finanšu transakciju. Plašāku informāciju par informācijas kodiem skatiet tēmā [Informācijas kodi un informācijas kodu grupas](../info-codes-retail.md).

    > [!NOTE]
    > Trigera funkcija **Prece** netiek atbalstīta informācijas kodiem, kas tiek izmantoti opcijām **Izlaist** un **Atzīmēt kā reģistrētu** finanšu savienotāju grupās.

    - Lapas **Finanšu savienotāju grupa** cilnē **Informācijas kodi** atlasiet informācijas kodus vai informācijas kodu grupas laukos **Izlaist** un **Atzīmēt kā reģistrētu**.

    > [!NOTE]
    > Jebkurā finanšu reģistrācijas procesa darbībā var izveidot vienu finanšu dokumentu un vienu ar finansēm nesaistītu dokumentu. Finanšu dokumentu nodrošinātāja paplašinājums norāda visus transakciju vai notikumu veidus saistībā ar finanšu dokumentiem vai arī ar finansēm nesaistītiem dokumentiem. Kļūdu apstrādes līdzeklis attiecas tikai uz finanšu dokumentiem.
    >
    > - **Finanšu dokuments** — obligāts dokuments, kas ir veiksmīgi jāreģistrē (piemēram, finanšu dokuments).
    > - **Ar finansēm nesaistīts dokuments** — transakcijas vai notikuma papildu dokuments (piemēram, dāvanu karte).

4. Ja operatoram ir jāspēj turpināt pašreizējās operācijas apstrādāšanu (piemēram, transakcijas izveidošanu vai pabeigšanu) arī pēc darbspējas pārbaudes kļūda rašanās, iespējojiet atļauju **Atļaut izlaist darbspējas pārbaudes kļūdu** lapā **Atļauju grupas** (**Retail un Commerce \> Darbinieki \> Atļauju grupas**). Plašāku informāciju par darbspējas pārbaudes procedūru skatiet rakstā [Finanšu reģistrācijas darbspējas pārbaude](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>POS finanšu X/Z pārskatu iestatīšana

Lai iespējotu finanšu X/Z pārskatu izpildi no POS, ir jāpievieno jaunas pogas POS izkārtojumam.

- Lapā **Pogu rindas** sekojiet instrukcijām sadaļā [POS operāciju pievienošana POS izkārtojumam, izmantojot Pogu rindas veidotāju](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), lai instalētu veidotāju un atjauninātu POS izkārtojumu.

    1. Atlasiet atjaunināmo izkārtojumu. 
    2. Pievienojiet jaunu pogu un iestatiet **Drukāt finanšu X** pogas rekvizītu.
    3. Pievienojiet jaunu pogu un iestatiet **Drukāt finanšu Z** pogas rekvizītu.
    4. Lapā **Sadales grafiks** palaidiet darbu **1090**, lai pārsūtītu izmaiņas uz kanāla datu bāzi.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Atliktas finanšu reģistrācijas manuālas izpildes iespējošana

Lai iespējotu atliktas finanšu reģistrācijas manuālu izpildīšanu, POS izkārtojumam jums ir jāpievieno jauna poga.

- Lapā **Pogu rindas** sekojiet instrukcijām sadaļā [POS operāciju pievienošana POS izkārtojumam, izmantojot Pogu rindas veidotāju](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), lai instalētu veidotāju un atjauninātu POS izkārtojumu.

    1. Atlasiet atjaunināmo izkārtojumu.
    2. Pievienojiet jaunu pogu un iestatiet pogas rekvizītu **Pabeigt finanšu reģistrācijas procesu**.
    3. Lapā **Sadales grafiks** palaidiet darbu **1090**, lai jūsu veiktās izmaiņas pārsūtītu uz kanāla datu bāzi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]