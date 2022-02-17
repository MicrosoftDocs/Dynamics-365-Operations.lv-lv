---
title: Commerce kanālu finanšu integrācijas iestatīšana
description: Šajā tēmā ir sniegti norādījumi par finanšu integrācijas funkcionalitātes iestatīšanu Commerce kanāliem.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fd37934e1ebd103d66c5181e0bfb75047f4cb6a3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076967"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce kanālu finanšu integrācijas iestatīšana

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegti norādījumi par finanšu integrācijas funkcionalitātes iestatīšanu Commerce kanāliem. Plašāku informāciju par finanšu integrāciju skatiet tēmā [Apskats par Commerce kanālu finanšu integrāciju](fiscal-integration-for-retail-channel.md).

## <a name="set-up-commerce-parameters"></a>Iestatiet tirdzniecības parametrus

1. Lapas **Commerce koplietojamie parametri** cilnē **Vispārīgi** iestatiet opcijai **Iespējot finanšu integrāciju** vienumu **Jā**.
1. Cilnē **Numuru sērijas** definējiet numuru sērijas šādām atsaucēm:

    - Finanšu tehniskā profila numurs
    - Finanšu savienotāja grupas numurs
    - Reģistrācijas procesa numurs

1. Lapā **Commerce parametri** definējiet numuru sēriju finanšu funkcionālā profila numuram.

    > [!NOTE]
    > Numuru sērijas nav obligātas. Numurus visiem finanšu integrācijas elementiem var izveidot, izmantojot numuru sērijas vai manuāli.

## <a name="set-up-a-fiscal-registration-process"></a>Finanšu reģistrācijas procesa iestatīšana

Finanšu integrācijas iestatīšanas procedūra ietver šādus uzdevumus:

- Konfigurēt finanšu savienotājus, kas apzīmē finanšu ierīces vai pakalpojumus, kurus izmanto finanšu reģistrācijas nolūkiem, piemēram, fiskālos printerus.
- Konfigurēt dokumentu nodrošinātājus, kas izveido finanšu dokumentus, kurus finanšu savienotāji reģistrēs finanšu ierīcēs vai pakalpojumos.
- Konfigurēt finanšu reģistrācijas procesu, kas nosaka finanšu reģistrācijas darbību secību un finanšu savienotājus un finanšu dokumentu nodrošinātājus, ko izmanto katrai darbībai.
- Piešķirt finanšu reģistrācijas procesus pārdošanas punkta (POS) funkcionalitātes profiliem.
- Piešķirt savienotāja tehniskos profilus aparatūras profiliem.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Augšupielādējiet fiskālo dokumentu nodrošinātāju konfigurācijas

Finanšu dokumentu nodrošinātājs ir atbildīgs par finanšu dokumentu sagatavošanu, kuri norāda transakcijas un notikumus, kas reģistrēti POS, tādā formātā, kas tiek izmantots arī mijiedarbībai ar finanšu ierīci vai pakalpojumu. Piemēram, finanšu dokumentu nodrošinātājs var izveidot finanšu dokumenta attēlojumu XML formātā.

Lai augšupielādētu fiskālo dokumentu nodrošinātāju konfigurācijas, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **Fiskālo dokumentu sniedzēji** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālo dokumentu sniedzēji**).
1. Augšupielādējiet XML konfigurāciju katrai ierīcei vai pakalpojumam, kuru plānojat izmantot.

> [!TIP]
> Atlasot **Skatīt**, varat skatīt visus funkcionālos profilus, kas ir saistīti ar pašreizējo finanšu dokumentu nodrošinātāju.

> [!NOTE]
> Datu kartēšana tiek uzskatīta par daļu no finanšu dokumentu nodrošinātāja. Lai iestatītu citus datu kartējumus tam pašam savienotājam (piemēram, ja pastāv valstij raksturīgi noteikumi), jums vajadzētu izveidot dažādus finanšu dokumentu nodrošinātājus.

### <a name="upload-configurations-of-fiscal-connectors"></a>Augšupielādējiet fiskālo savienotāju konfigurācijas

Finanšu savienotājs ir atbildīgs par saziņu ar finanšu ierīci vai pakalpojumu. Piemēram, finanšu savienotājs var nosūtīt finanšu dokumentu, kuru izveidoja finanšu dokumentu nodrošinātājs XML formātā, uz fiskālo printeri. Papildinformāciju par fiskālās integrācijas komponentiem skatiet [Fiskālās reģistrācijas process un fiskālās integrācijas paraugi fiskālajām ierīcēm un pakalpojumiem](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Lai augšupielādētu fiskālo savienotāju konfigurācijas, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **Fiskālie savienotāji** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālie savienotāji**).
1. Augšupielādējiet XML konfigurāciju katrai ierīcei vai pakalpojumam, ko plānojat izmantot fiskālās integrācijas nolūkos.

> [!TIP]
> Atlasot **Skatīt**, varat skatīt visus funkcionālos un tehniskos profilus, kas ir saistīti ar pašreizējo finanšu savienotāju.

Finanšu savienotāju un finanšu dokumentu nodrošinātāju konfigurāciju piemērus skatiet tēmā [Finanšu integrācijas paraugi komplektā Commerce SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Izveidojiet savienotāju funkcionālos profilus

Lai izveidotu savienotāja funkcionālos profilus, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **Savienotāju funkcionālie profili** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Savienotāju funkcionālie profili**).
1. Katrai fiskālā savienotāja un fiskālo dokumentu nodrošinātāja kombinācijai, kas ir saistīta ar šo fiskālo savienotāju, izveidojiet savienotāja funkcionālo profilu, veicot šīs darbības:

    1. Atlasiet savienotāja nosaukumu.
    1. Atlasiet kādu dokumentu nodrošinātāju.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Mainiet datu kartēšanas parametrus savienotāja funkcionālajā profilā

Varat mainīt datu kartēšanas parametrus savienotāja funkcionālajā profilā. Šajā tabulā ir sniegti daži savienotāja funkcionālā profila datu kartēšanas parametru piemēri.

| Parametrs | Formāts | Paraugs |
|-----------|--------|---------|
| PVN likmju iestatījumi | value : VATrate | 1 : 2000, 2 : 1800 |
| PVN kodu kartējums | VATcode : value | vat20 : 1, vat18 : 2 |
| Norēķinu tipu kartējums | TenderType : value | Cash : 1, Card : 2 |

Lai atjaunotu noklusējuma parametrus, kas definēti fiskālo dokumentu nodrošinātāja konfigurācijā, atlasiet **Atjaunināt** uz **Savienotāju funkcionālie profili** lappuse.

> [!NOTE]
> Savienotāja funkcionālie profili attiecas tikai uz konkrētu uzņēmumu. Ja plānojat izmantot vienu un to pašu fiskālā savienotāja un fiskālo dokumentu nodrošinātāja kombināciju dažādiem uzņēmumiem, izveidojiet savienotāja funkcionālo profilu katram uzņēmumam.

### <a name="create-connector-technical-profiles"></a>Izveidojiet savienotāju tehniskos profilus

Lai izveidotu savienotāja tehniskos profilus, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **Savienotāju tehniskie profili** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Savienotāju tehniskie profili**).
1. Izveidojiet savienotāja tehnisko profilu katram fiskālajam savienotājam, veicot šīs darbības:

    1. Atlasiet savienotāja nosaukumu.
    1. Izvēlieties savienotāja veidu:

        - Ierīcēm vai pakalpojumiem, kas ir savienoti ar aparatūras staciju vai atrodas lokālajā tīklā, atlasiet **Vietējais**.
        - Ārējiem pakalpojumiem atlasiet **Ārējais**.
        - Iekšējiem savienotājiem Commerce izpildlaikā (CRT), atlasiet **Iekšējais**. 

    1. Izvēlieties savienotāja atrašanās vietu:

        - Ja savienotājs atrodas aparatūras stacijā, atlasiet **Aparatūras stacija**.
        - Ja savienotājs atrodas POS reģistrā, atlasiet **Reģistrēties**.

Parametrus savienotāja tehniskā profila cilnēs **Ierīces** un **Iestatījumi** var mainīt. Lai atjaunotu noklusētos parametrus, kas definēti finanšu savienotāja konfigurācijā, atlasiet **Atjaunināt**. Kamēr tiek ielādēta jauna XML konfigurācijas versija, jūs saņemsit ziņojumu, kurā teikts, ka pašreizējais fiskālais savienotājs vai fiskālā dokumenta nodrošinātājs jau tiek izmantots. Šī procedūra nepārlabo manuālās izmaiņas, kas iepriekš veiktas savienotāja funkcionālajos profilos un savienotāja tehniskajos profilos. Lai lietotu noklusējuma parametru kopu no jaunas konfigurācijas, atlasiet **Atjaunināt** vai nu uz **Savienotāju funkcionālie profili** lapa vai **Savienotāju tehniskie profili** lappuse.

Ja jums ir jāiestata konkrēti parametri atsevišķam POS reģistram vai veikalam, veiciet šīs darbības.

1. Izvēlieties **Ignorēt** izvēlnes vienums.
1. Uz **Ignorēt** lapu, izveidojiet jaunu ierakstu.
1. Izvēlieties veikalu vai POS reģistru. Varat ignorēt atlasītā tehniskā profila parametrus atsevišķam POS reģistram vai visiem POS reģistriem atsevišķā veikalā.
1. Uz **Ierīce** cilnē ievadiet parametrus atlasītajam POS reģistram vai veikalam.

### <a name="create-fiscal-connector-groups"></a>Izveidojiet fiskālo savienotāju grupas

Savienotāju grupā ir apvienoti tādu finanšu savienotāju funkcionālie profili, kuri veic identiskas funkcijas un finanšu reģistrācijas procesā tiek izmantoti tajā pašā darbībā. Piemēram, ja vairākus fiskālo printeru modeļus var izmantot veikalā, finanšu savienotājus šiem fiskālajiem printeriem var apvienot finanšu savienotāju grupā.

Lai izveidotu fiskālo savienotāju grupu, veiciet šīs darbības.

1. Dodieties uz **Fiskālā savienotāja grupa** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālo savienotāju grupas**).
1. Izveidojiet jaunu fiskālo savienotāju grupu.
1. Pievienojiet funkcionālos profilus savienotāju grupai. Cilnē **Funkcionālie profili** atlasiet vienumu **Pievienot** un atlasiet kādu profila numuru. Katram finanšu savienotājam noteiktā savienotāju grupā var būt tikai viens funkcionālais profils.
1. Lai pārtrauktu attiecīgā funkcionālā profila izmantošanu, opcijai **Atspējot** iestatiet vienumu **Jā**. Šīs izmaiņas ietekmē tikai pašreizējo savienotāju grupu. Varat turpināt tā paša funkcionālā profila izmantošanu citās savienotāju grupās.

### <a name="create-a-fiscal-registration-process"></a>Izveidojiet fiskālās reģistrācijas procesu

Finanšu reģistrācijas procesu nosaka reģistrācijas darbību secība un katrā darbībā izmantotā savienotāju grupa.

Lai izveidotu fiskālo reģistrācijas procesu, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **Fiskālās reģistrācijas process** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālās reģistrācijas procesi**).
1. Izveidojiet jaunu ierakstu katram unikālajam fiskālās reģistrācijas procesam.
1. Pievienojiet procesam reģistrācijas darbības, veicot šādas darbības:

    1. Atlasiet **Pievienot**.
    1. Atlasiet finanšu savienotāja tipu.
    1. Laukā **Grupas numurs** atlasiet atbilstošo finanšu savienotāju grupu.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Piešķiriet POS profiliem fiskālās reģistrācijas procesa entītijas

Lai POS profiliem piešķirtu fiskālās reģistrācijas procesa entītijas, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **POS funkcionalitātes profili** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**). 
1. Piešķiriet fiskālās reģistrācijas procesu POS funkcionalitātes profilam.
1. Atlasiet **Rediģēt** un pēc tam cilnes **Finanšu reģistrācijas process** laukā **Procesa numurs** atlasiet procesu.
1. Dodieties uz **POS aparatūras profila** lapu (**Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles).**
1. Piešķiriet savienotāja tehniskos profilus aparatūras profilam. 
1. Atlasiet **Rediģēt** un pēc tam **cilnē Finanšu perifērijas ierīces** pievienojiet rindu. 
1. Laukā **Profila numurs** atlasiet savienotāja tehnisko profilu.

> [!NOTE]
> Tam pašam aparatūras profilam varat pievienot vairākus tehniskos profilus. Tomēr aparatūras profilam vai POS funkcionalitātes profilam jābūt tikai vienam krustpunktam ar jebkuru finanšu savienotāju grupu.

Finanšu reģistrācijas plūsmu nosaka fiskālās reģistrācijas process, kā arī daži fiskālās integrācijas komponentu parametri: CRT finanšu dokumentu nodrošinātāja paplašinājums un finanšu savienotāja aparatūras stacijas paplašinājums.

- Abonēšana notikumiem un transakcijām finanšu reģistrācijā ir iepriekš definēta finanšu dokumentu nodrošinātājā.
- Finanšu dokumentu nodrošinātājs ir atbildīgs arī par fiskālajai reģistrācijai izmantotā finanšu savienotāja identificēšanu. Tas atbilst savienotāja funkcionālajiem profiliem, kas ir iekļauti finanšu savienotāju grupā, kas ir norādīta finanšu reģistrācijas procesa pašreizējai darbībai ar savienotāja tehnisko profilu, kas ir piešķirts tādas aparatūras stacijas aparatūras profilam, ar kuru ir savienots pārī POS.
- Finanšu dokumentu nodrošinātājs izmanto datu kartēšanas iestatījumus no finanšu dokumentu nodrošinātāja konfigurācijas, lai pārveidotu transakciju/notikumu datus, piemēram, nodokļus un maksājumus, kamēr tiek izveidots finanšu dokuments.
- Ja finanšu dokumentu nodrošinātājs izveido finanšu dokumentu, finanšu savienotājs var to nosūtīt uz finanšu ierīci tādu, kāds tas ir, vai parsēt to un pārveidot par ierīces lietojumprogrammas interfeisa (API) komandu sēriju atkarībā no tā, kā tiek apstrādāti sakari.

### <a name="validate-the-fiscal-registration-process"></a>Pārbaudīt finanšu reģistrācijas procesu

Ieteicams validēt fiskālās reģistrācijas procesu šādos gadījumos:

- Esat pabeidzis visus jauna reģistrācijas procesa iestatījumus. Šie iestatījumi ietver reģistrācijas procesu piešķiršanu POS funkcionalitātes profiliem un aparatūras profiliem.
- Jūs esat veicis izmaiņas esošā finanšu reģistrācijas procesā, un šo izmaiņu dēļ izpildlaikā var tikt atlasīts cits finanšu savienotājs. (Piemēram, esat mainījis savienotāju grupu finanšu reģistrācijas procesa solim, iespējojis savienotāja funkcionālo profilu savienotāju grupā vai pievienojis savienotāju grupai jaunu savienotāja funkcionālo profilu.)
- Jūs esat veicis izmaiņas savienotāja tehnisko profilu piešķiršanā aparatūras profiliem.

Lai validētu finanšu reģistrācijas procesu, rīkojieties šādi.

1. Tirdzniecības galvenajā mītnē dodieties uz **Fiskālās reģistrācijas process** lappuse (**Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālās reģistrācijas procesi**).
1. Atlasiet **Validēt**, lai pārbaudītu finanšu reģistrācijas procesu.
1. Lapā **Sadales grafiks** palaidiet darbus **1070** un **1090**, lai pārsūtītu datus uz kanāla datu bāzi.

## <a name="set-up-fiscal-texts-for-discounts"></a>Atlaižu finanšu teksta iestatīšana

Dažos gadījumos uz finanšu dokumenta jādrukā īpašs teksts, ja tiek piemērota atlaide. Atlaižu finanšu tekstu var iestatīt lapā **Finanšu savienotāju grupa** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu savienotāju grupas**).

- Manuālām atlaidēm, kuras tiek piemērotas POS, jāiestata finanšu teksts informācijas kodam vai informācijas kodu grupai, kas POS funkcionalitātes profilā ir norādīti kā informācijas kods **Preces atlaide**.

    1. Lapā **Finanšu savienotāju grupa** atlasiet **Finanšu dokumenta teksts**.
    1. Cilnē **Informācijas kodi** atlasiet **Pievienot** un atlasiet informācijas kodu vai informācijas kodu grupu.
    1. Laukā **Informācijas koda numurs** atlasiet vērtību.
    1. Laukā **Apakškoda numurs** atlasiet vērtību, ja apakškods ir nepieciešams atlasītajam informācijas kodam.
    1. Laukā **Finanšu dokumenta teksts** norādiet finanšu tekstu, kas jādrukā uz finanšu dokumenta.
    1. Iestatiet opcijai **Izdrukāt lietotāja ievadi finanšu dokumentā** vienumu **Jā**, lai pārlabotu tekstu uz finanšu dokumenta ar informāciju, ko lietotājs manuāli ievada POS. Šī opcija attiecas tikai uz informācijas kodiem, kuriem ir ievades veids **Teksts**.

    > [!NOTE]
    > Var norādīt finanšu tekstu vairākiem informācijas kodiem, lai nodrošinātu atbalstu scenārijiem, kuru ietvaros tiek izmantotas informācijas kodu grupas, saistīti informācijas kodi un aktivizēti informācijas kodi. Šajos scenārijos finanšu dokumentā būs ietverti finanšu teksti no visiem informācijas kodiem, kas ir saistīti ar transakcijas rindu, kurai tika piemērota atlaide.

- Kanālam raksturīgu atlaižu gadījumā ir jādefinē finanšu teksts atlaides ID.

    1. Lapā **Finanšu savienotāju grupa** atlasiet **Finanšu dokumenta teksts**.
    1. Cilnē **Atlaides** atlasiet **Pievienot** un atlasiet atlaides ID.
    1. Laukā **Finanšu dokumenta teksts** norādiet finanšu tekstu, kas jādrukā uz finanšu dokumenta.

    > [!NOTE]
    > Ja tai pašai transakcijas rindai tiek piemērotas vairākas atlaides, finanšu dokumentā būs ietverti finanšu teksti no visām atlaidēm, kuras ir saistītas ar attiecīgo transakcijas rindu.

## <a name="set-error-handling-settings"></a>Kļūdu apstrādes iestatījumu veikšana

Kļūdu apstrādes opcijas, kas pieejamas finanšu integrācijā, tiek iestatītas finanšu reģistrācijas procesā. Plašāku informāciju par kļūdu apstrādi finanšu integrācijā skatiet tēmā [Kļūdu apstrāde](fiscal-integration-for-retail-channel.md#error-handling).

Lai iestatītu kļūdu apstrādes iestatījumus, rīkojieties šādi.

1. Lapā **Finanšu reģistrācijas process** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu reģistrācijas procesi**) varat iestatīt šādus parametrus katrai finanšu reģistrācijas procesa darbībai:

    - **Atļaut izlaist** — šis parametrs iespējo opciju **Izlaist** kļūdu apstrādes dialoglodziņā.
    - **Atļaut atzīmēt kā reģistrētu** — šis parametrs iespējo opciju **Atzīmēt kā reģistrētu** kļūdu apstrādes dialoglodziņā.
    - **Atļaut atlikšanu** — šis parametrs iespējo opciju **Atlikt** dialoglodziņā Kļūdu apstrāde.
    - **Kļūdas gadījumā turpināt** — ja šis parametrs ir iespējots, finanšu reģistrācijas process POS reģistrā var turpināties arī tad, ja transakcijas vai notikuma finanšu reģistrācija ir nesekmīga. Pretējā gadījumā, lai palaistu nākamās transakcijas vai notikuma finanšu reģistrāciju, operatoram ir atkārtot jāmēģina izpildīt nesekmīgo finanšu reģistrāciju, jāizlaiž šī reģistrācija vai attiecīgā transakcija vai notikums ir jāatzīmē kā reģistrēts. Plašāku informāciju skatiet rakstā [Neobligātā finanšu reģistrācija](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Ja ir iespējots parametrs **Kļūdas gadījumā turpināt**, parametrs **Atļaut izlaist** un parametrs **Atļaut atzīmēt kā reģistrētu** automātiski tiek atspējots.

1. Dialoglodziņā Izlaist un Atzīmēt kā reģistrētus **opcijās kļūdu apstrāde ir jāiespējo** atļaut izlaist reģistrāciju vai atzīmēt kā reģistrētu **atļauju.** **·** Lai iespējotu šo atļauju, dodieties uz **lapu Atļauju grupas** (**Mazumtirdzniecības un tirdzniecības \> darbinieku \> atļauju grupas**) un iestatiet **opciju Atļaut izlaist reģistrāciju vai atzīmēt kā reģistrētu** uz **Jā**.
1. Lai **opciju Atliktu** dialoglodziņā Kļūdu apstrāde, **ir jāiespējo atļauja Atļaut atlikšanu**. Lai iespējotu atļauju, dodieties uz **lapu Atļauju grupas** (**Mazumtirdzniecības un tirdzniecības \> darbinieku \> atļauju grupas**) un iestatiet **opciju Atļaut atlikšanu** uz **Jā**.
1. Opcijas **Izlaist**, **Atzīmēt kā reģistrētu** un **Atlikt** ļauj operatoriem ievadīt papildinformāciju, ja finanšu reģistrācija neizdodas. Lai padarītu šo funkcionalitāti pieejamu, finanšu savienotāju grupā ir jānorāda **kodi Izlaist**, **Atzīmēt kā reģistrētu** un **Atlikt** informāciju. Pēc tam operatoru ievadītā informācija tiek saglabāta kā informācijas koda transakcija, kas saistīta ar finanšu transakciju. Plašāku informāciju par informācijas kodiem skatiet tēmā [Informācijas kodi un informācijas kodu grupas](../info-codes-retail.md).

    > [!NOTE]
    > Trigera funkcija **Prece** netiek atbalstīta informācijas kodiem, kas tiek izmantoti opcijām **Izlaist** un **Atzīmēt kā reģistrētu** finanšu savienotāju grupās.

    - **Lapas Finanšu savienotāju** grupa **cilnē Informācijas kodi** atlasiet informācijas kodus vai informācijas kodu grupas **laukos Izlaist**, **Atzīmēt kā reģistrētu** un **Atlikt**.

    > [!NOTE]
    > Jebkurā finanšu reģistrācijas procesa darbībā var izveidot vienu finanšu dokumentu un vienu ar finansēm nesaistītu dokumentu. Finanšu dokumentu nodrošinātāja paplašinājums norāda visus transakciju vai notikumu veidus saistībā ar finanšu dokumentiem vai arī ar finansēm nesaistītiem dokumentiem. Kļūdu apstrādes līdzeklis attiecas tikai uz finanšu dokumentiem.
    >
    > - **Finanšu dokuments** — obligāts dokuments, kas ir veiksmīgi jāreģistrē (piemēram, finanšu dokuments).
    > - **Ar finansēm nesaistīts dokuments** — transakcijas vai notikuma papildu dokuments (piemēram, dāvanu karte).

1. Ja operatoram ir jāspēj turpināt pašreizējās operācijas apstrādāšanu (piemēram, transakcijas izveidošanu vai pabeigšanu) arī pēc darbspējas pārbaudes kļūda rašanās, iespējojiet atļauju **Atļaut izlaist darbspējas pārbaudes kļūdu** lapā **Atļauju grupas** (**Retail un Commerce \> Darbinieki \> Atļauju grupas**). Plašāku informāciju par darbspējas pārbaudes procedūru skatiet rakstā [Finanšu reģistrācijas darbspējas pārbaude](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>POS finanšu X/Z pārskatu iestatīšana

Lai iespējotu finanšu X/Z pārskatu izpildi no POS, ir jāpievieno jaunas pogas POS izkārtojumam.

- Lapā **Pogu rindas** sekojiet instrukcijām sadaļā [POS operāciju pievienošana POS izkārtojumam, izmantojot Pogu rindas veidotāju](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), lai instalētu veidotāju un atjauninātu POS izkārtojumu.

    1. Atlasiet atjaunināmo izkārtojumu. 
    1. Pievienojiet jaunu pogu un iestatiet **Drukāt finanšu X** pogas rekvizītu.
    1. Pievienojiet jaunu pogu un iestatiet **Drukāt finanšu Z** pogas rekvizītu.
    1. Lapā **Sadales grafiks** palaidiet darbu **1090**, lai pārsūtītu izmaiņas uz kanāla datu bāzi.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Atliktas finanšu reģistrācijas manuālas izpildes iespējošana

Lai iespējotu atliktas finanšu reģistrācijas manuālu izpildīšanu, POS izkārtojumam jums ir jāpievieno jauna poga.

- Lapā **Pogu rindas** sekojiet instrukcijām sadaļā [POS operāciju pievienošana POS izkārtojumam, izmantojot Pogu rindas veidotāju](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), lai instalētu veidotāju un atjauninātu POS izkārtojumu.

    1. Atlasiet atjaunināmo izkārtojumu.
    1. Pievienojiet jaunu pogu un iestatiet pogas rekvizītu **Pabeigt finanšu reģistrācijas procesu**.
    1. Lapā **Sadales grafiks** palaidiet darbu **1090**, lai jūsu veiktās izmaiņas pārsūtītu uz kanāla datu bāzi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
