---
title: Commerce kanālu finanšu integrācijas iestatīšana
description: Šajā tēmā ir sniegti norādījumi par finanšu integrācijas funkcionalitātes iestatīšanu Commerce kanāliem.
author: EvgenyPopovMBS
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 51a75ce03b0ae6b744ec56df35bd3fdb1f40cf3a
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661753"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce kanālu finanšu integrācijas iestatīšana

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegti norādījumi par finanšu integrācijas funkcionalitātes iestatīšanu Commerce kanāliem. Plašāku informāciju par finanšu integrāciju skatiet tēmā [Apskats par Commerce kanālu finanšu integrāciju](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Iespējot līdzekļus programmā Commerce Headquarters

Lai iespējotu līdzekļus, kas ir saistīti ar finanšu integrācijas funkcionalitāti commerce kanāliem, sekojiet šiem soļiem.

1. Programmā Commerce Headquarters dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Atrodiet un iespējojiet šādas funkcijas:

    - **Tiešā finanšu integrācija no POS reģistriem** — šis līdzeklis paplašina finanšu integrācijas struktūru, pievienojot iespēju izveidot finanšu savienotājus, kas tiks palaisti pārdošanas punktā (POS). Šis savienotāja tips komunicē ar fiskālo ierīci vai pakalpojumu, kas nodrošina HTTP programmas programmēšanas interfeisu (API) un tam nav nepieciešams atvēlēts fizisks dators veikalā. Piemēram, šī funkcionalitāte iespējo fiskālo integrāciju mobilajām ierīcēm, nepieprasot koplietojamu aparatūras staciju.
    - **Fiskālās integrācijas tehniskā** profila ignorēšana — šī funkcija iespējo paplašināt finanšu integrācijas konfigurāciju un pievieno iespēju pārbaudīt savienojuma parametrus POS reģistra iestatījumu lapā. Kad šī funkcija ir aktivizēta, jūs varat ignorēt tehniskā profila parametrus.
    - **POS reģistru finanšu reģistrācijas stāvoklis** - ja šī funkcija ir iespējota, varat atspējot fiskālo reģistrāciju procesu noteiktiem POS reģistriem. Ja POS reģistram ir atspējota finanšu reģistrācija, šajā reģistrā pārdošanas darbības nevar pabeigt.
    - **Fiskālās integrācijas lokālās** krātuves dublējums - šis līdzeklis paplašina finanšu integrācijas struktūras kļūdu apstrādes iespējas. Tas arī iespējo automātisku finanšu reģistrācijas datu dublējumu datu zudums gadījumā, lai dati lokālajā krātuvē tiek atjaunoti ierīces aktivizēšanas laikā.

## <a name="set-up-commerce-parameters"></a>Komercijas parametru iestatīšana

Lai iestatītu Commerce parametrus, sekojiet šiem soļiem.

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
- Piešķiriet finanšu reģistrācijas procesu POS funkcionalitātes profiliem.
- Piešķirt savienotāja tehniskos profilus aparatūras profiliem.
- Piešķiriet savienotāja tehniskos profilus POS aparatūrai vai funkcionalitātes profiliem.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Augšupielādēt finanšu dokumentu nodrošinātāju konfigurācijas

Finanšu dokumentu nodrošinātājs ir atbildīgs par finanšu dokumentu sagatavošanu, kuri norāda transakcijas un notikumus, kas reģistrēti POS, tādā formātā, kas tiek izmantots arī mijiedarbībai ar finanšu ierīci vai pakalpojumu. Piemēram, finanšu dokumentu nodrošinātājs var izveidot finanšu dokumenta attēlojumu XML formātā.

Lai augšupielādētu finanšu dokumentu nodrošinātāju konfigurācijas, sekojiet šiem soļiem.

1. Programmā Commerce headquarters atveriet lapu Finanšu dokumentu **nodrošinātāji** (Mazumtirdzniecības **un Commerce Channel \> iestatīšanas finanšu \> integrācijas finanšu \> dokumentu nodrošinātāji**).
1. Augšupielādējiet XML konfigurāciju katrai ierīcei vai pakalpojumam, ko plānojat izmantot.

> [!TIP]
> Atlasot **Skatīt**, varat skatīt visus funkcionālos profilus, kas ir saistīti ar pašreizējo finanšu dokumentu nodrošinātāju.

> [!NOTE]
> Datu kartēšana tiek uzskatīta par daļu no finanšu dokumentu nodrošinātāja. Lai iestatītu citus datu kartējumus tam pašam savienotājam (piemēram, ja pastāv valstij raksturīgi noteikumi), jums vajadzētu izveidot dažādus finanšu dokumentu nodrošinātājus.

### <a name="upload-configurations-of-fiscal-connectors"></a>Augšupielādēt finanšu savienotāju konfigurācijas

Finanšu savienotājs ir atbildīgs par saziņu ar finanšu ierīci vai pakalpojumu. Piemēram, finanšu savienotājs var nosūtīt finanšu dokumentu, kuru izveidoja finanšu dokumentu nodrošinātājs XML formātā, uz fiskālo printeri. Papildinformāciju par finanšu integrācijas komponentiem skatiet finanšu [reģistrācijas procesā un finanšu integrācijas paraugos fiskālajām ierīcēm un pakalpojumiem](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Lai augšupielādētu finanšu savienotāju konfigurācijas, sekojiet šiem soļiem.

1. Programmā Commerce headquarters dodieties uz lapu **Finanšu savienotāji** (Mazumtirdzniecības **un Commerce \> Channel iestatīšanas finanšu \> integrācijas finanšu \> savienotāji**).
1. Augšupielādējiet XML konfigurāciju katrai ierīcei vai pakalpojumam, ko plānojat izmantot finanšu integrācijas nolūkiem.

> [!TIP]
> Atlasot **Skatīt**, varat skatīt visus funkcionālos un tehniskos profilus, kas ir saistīti ar pašreizējo finanšu savienotāju.

Finanšu savienotāju un finanšu dokumentu nodrošinātāju konfigurāciju piemērus skatiet tēmā [Finanšu integrācijas paraugi komplektā Commerce SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Izveidot savienotāja funkcionālos profilus

Lai izveidotu savienotāja funkcionālos profilus, veiciet šādus soļus.

1. Programmā Commerce headquarters dodieties uz lapu Connector **funkcionālie profili** (**Retail un Commerce \> Channel setup \> Fiscal integration \> Connector funkcionālie profili**).
1. Katrai ar šo finanšu savienotāju saistītā fiskālā savienotāja un finanšu dokumenta nodrošinātāja kombinācijai izveidojiet savienotāja funkcionālo profilu, šādi:

    1. Atlasiet savienotāja nosaukumu.
    1. Atlasiet kādu dokumentu nodrošinātāju.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Mainīt datu kartēšanas parametrus savienotāja funkcionālā profilā

Varat mainīt datu kartēšanas parametrus savienotāja funkcionālajā profilā. Tabulā sniegti daži datu kartēšanas parametru piemēri savienotāja funkcionālā profilā.

| Parametrs | Formāts | Paraugs |
|-----------|--------|---------|
| PVN likmju iestatījumi | value : VATrate | 1 : 2000, 2 : 1800 |
| PVN kodu kartējums | VATcode : value | vat20 : 1, vat18 : 2 |
| Norēķinu tipu kartējums | TenderType : value | Cash : 1, Card : 2 |

Lai atjaunotu noklusējuma parametrus, kas definēti finanšu dokumenta nodrošinātāja konfigurācijā, atlasiet **Atjaunināt** savienotāja **funkcionālā profila** lapā.

> [!NOTE]
> Savienotāja funkcionālie profili attiecas tikai uz konkrētu uzņēmumu. Ja plānojat izmantot vienu fiskālā savienotāja un finanšu dokumenta nodrošinātāja kombināciju dažādiem uzņēmumiem, jāizveido savienotāja funkcionālā profils katram uzņēmumam.

### <a name="create-connector-technical-profiles"></a>Izveidot savienotāja tehniskos profilus

Lai izveidotu savienotāja tehniskos profilus, sekojiet šiem soļiem.

1. Programmā Commerce headquarters dodieties uz lapu **Connector technical profiles** (**Retail un Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**).
1. Izveidojiet savienotāja tehnisko profilu katram finanšu savienotājam, veicot šādas darbības:

    1. Atlasiet savienotāja nosaukumu.
    1. Atlasiet savienotāja tipu:

        - Ierīcēm vai pakalpojumiem, kas ir savienoti ar aparatūras staciju vai ir lokālajā tīklā, atlasiet **Lokāls**.
        - Ārējiem pakalpojumiem atlasiet **Ārējais**.
        - Commerce izpildlaikā iekšējiem savienotājiem (CRT) atlasiet **Iekšējs**. 

    1. Atlasiet savienotāja vietu:

        - Ja savienotājs atrodas aparatūras stacijā, atlasiet Aparatūras **stacija**.
        - Ja savienotājs atrodas POS reģistrā, atlasiet **Reģistrs**.

Parametrus savienotāja tehniskā profila cilnēs **Ierīces** un **Iestatījumi** var mainīt. Lai atjaunotu noklusētos parametrus, kas definēti finanšu savienotāja konfigurācijā, atlasiet **Atjaunināt**. Ielādējot JAUNU XML konfigurācijas versiju, saņemsit ziņojumu, ka pašreizējais fiskālais savienotājs vai finanšu dokumentu nodrošinātājs jau tiek lietots. Šī procedūra nepārlabo manuālās izmaiņas, kas iepriekš veiktas savienotāja funkcionālajos profilos un savienotāja tehniskajos profilos. Lai lietotu noklusētās parametru kopas jaunā konfigurācijā, **·** **atlasiet Atjaunināt vai nu savienotāja funkcionālo** profilu lapā, **vai Connector tehnisko profilu** lapā.

Ja atsevišķai POS kases sistēmā vai veikalā ir jāiestata noteikti parametri, veiciet šīs darbības.

1. Atlasiet izvēlnes **elementu** Ignorēt.
1. **Lapā Ignorēt** izveidojiet jaunu ierakstu.
1. Atlasiet veikalu vai POS kases reģistru. Varat ignorēt atlasītā tehniskā profila parametrus atsevišķam POS kases sistēmai vai visām POS kases sistēmām atsevišķā veikalā.
1. Cilnē Ierīce **ievadiet** atlasītā POS reģistra vai veikala parametrus.

### <a name="create-fiscal-connector-groups"></a>Izveidot finanšu savienotāja grupas

Savienotāju grupā ir apvienoti tādu finanšu savienotāju funkcionālie profili, kuri veic identiskas funkcijas un finanšu reģistrācijas procesā tiek izmantoti tajā pašā darbībā. Piemēram, ja vairākus fiskālo printeru modeļus var izmantot veikalā, finanšu savienotājus šiem fiskālajiem printeriem var apvienot finanšu savienotāju grupā.

Lai izveidotu fiskālā savienotāja grupu, veiciet šos soļus.

1. Dodieties uz lapu Finanšu **savienotāja** grupa (Mazumtirdzniecības **un Commerce Channel \> Setup \> Fiskālās integrācijas \> fiskālā savienotāja grupas**).
1. Izveidot jaunu finanšu savienotāja grupu.
1. Pievienojiet funkcionālos profilus savienotāju grupai. Cilnē **Funkcionālie profili** atlasiet vienumu **Pievienot** un atlasiet kādu profila numuru. Katram finanšu savienotājam noteiktā savienotāju grupā var būt tikai viens funkcionālais profils.
1. Lai pārtrauktu attiecīgā funkcionālā profila izmantošanu, opcijai **Atspējot** iestatiet vienumu **Jā**. Šīs izmaiņas ietekmē tikai pašreizējo savienotāju grupu. Varat turpināt tā paša funkcionālā profila izmantošanu citās savienotāju grupās.

### <a name="create-a-fiscal-registration-process"></a>Izveidot finanšu reģistrācijas procesu

Finanšu reģistrācijas procesu nosaka reģistrācijas darbību secība un katrā darbībā izmantotā savienotāju grupa.

Lai izveidotu fiskālās reģistrācijas procesu, sekojiet šiem soļiem.

1. Programmā Commerce headquarters atveriet lapu Fiskālās reģistrācijas **process** (**Mazumtirdzniecības un Commerce Channel \> iestatīšanas finanšu \> integrācijas finanšu \> reģistrēšanas procesi**).
1. Izveidojiet jaunu ierakstu katram unikālajam finanšu reģistrācijas procesam.
1. Pievienojiet procesam reģistrācijas soļus, izpildot šādas darbības:

    1. Atlasiet **Pievienot**.
    1. Atlasiet finanšu savienotāja tipu.
    1. Laukā **Grupas numurs** atlasiet atbilstošo finanšu savienotāju grupu.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Piešķirt POS profiliem finanšu reģistrācijas procesa elementus

Lai piešķirtu fiskālās reģistrācijas procesa elementus POS profiliem, sekojiet šiem soļiem.

1. Programmā Commerce Headquarters atveriet POS funkcionalitātes **profilu lapu (** Retail **un Commerce Channel \> Setup \> POS iestatīšanas POS profilu \> funkcionalitātes \> profili**). 
1. Piešķiriet finanšu reģistrācijas procesu POS funkcionalitātes profilam.
1. Atlasiet **Rediģēt** un pēc tam cilnes **Finanšu reģistrācijas process** laukā **Procesa numurs** atlasiet procesu.
1. Cilnē Finanšu **pakalpojumi atlasiet** savienotāja tehniskos profilus ar savienotāja atrašanās vietas **reģistru**.
1. Pārejiet uz **POS aparatūras profila lapu** (**Retail un Commerce Channel \> Setup POS iestatīšanas \>\> POS profili aparatūras \> profiliem**).
1. Piešķiriet savienotāja tehniskos profilus aparatūras profilam. 
1. Atlasiet **rediģēt** un pēc tam finanšu perifērijas **ierīču** cilnē pievienojiet rindu. 
1. Laukā **Profila numurs** atlasiet savienotāja tehnisko profilu.
1. Cilnē Finanšu perifērijas **ierīces atlasiet savienotāja tehniskos profilus un savienotāja atrašanās vietas aparatūras** **staciju**.

> [!NOTE]
> Tam pašam aparatūras profilam varat pievienot vairākus tehniskos profilus. Tomēr aparatūras profilam vai POS funkcionalitātes profilam jābūt tikai vienam krustpunktam ar jebkuru finanšu savienotāju grupu.

Finanšu reģistrācijas plūsmu nosaka finanšu reģistrācijas process, kā arī daži fiskālās integrācijas komponentu parametri: CRT finanšu dokumentu nodrošinātāja paplašinājums un aparatūras stacijas paplašinājums finanšu savienotājam.

- Abonēšana notikumiem un transakcijām finanšu reģistrācijā ir iepriekš definēta finanšu dokumentu nodrošinātājā.
- Finanšu dokumentu nodrošinātājs ir atbildīgs arī par fiskālajai reģistrācijai izmantotā finanšu savienotāja identificēšanu. Tas atbilst savienotāja funkcionālajiem profiliem, kas ir iekļauti finanšu savienotāju grupā, kas ir norādīta finanšu reģistrācijas procesa pašreizējai darbībai ar savienotāja tehnisko profilu, kas ir piešķirts tādas aparatūras stacijas aparatūras profilam, ar kuru ir savienots pārī POS.
- Finanšu dokumentu nodrošinātājs izmanto datu kartēšanas iestatījumus no finanšu dokumentu nodrošinātāja konfigurācijas, lai pārveidotu transakciju/notikumu datus, piemēram, nodokļus un maksājumus, kamēr tiek izveidots finanšu dokuments.
- Kad finanšu dokumentu piegādātājs ģenerē finanšu dokumentu, finanšu savienotājs var to nosūtīt uz fiskālo ierīci pēc kārtas vai parsēt to un pārveidot to par ierīces API komandu secību atkarībā no tā, kā komunikācija tiek apstrādāta.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Iestatīt reģistrus ar finanšu reģistrācijas ierobežojumiem

Varat atlasīt reģistrus, kam ir aizliegta finanšu reģistrācija, piemēram, gadījumos, kad šajās ierīcēs ir jānodrošina tikai ar finanšu operāciju, piemēram, preču kataloga meklēšana, debitora meklēšana vai darbību melnraksta izveide.

Lai iestatītu reģistrus ar fiskālās reģistrācijas ierobežojumiem, veiciet šos soļus.

1. Programmā Commerce headquarters pārejiet uz sadaļu **Mazumtirdzniecības un Commerce \> Channel iestatīšanas \> finanšu integrācijas finanšu \> reģistrēšanas procesi**.
1. Atlasiet nepieciešamo procesu.
1. Atlasiet POS reģistrus **ar finanšu procesa ierobežojumu** cilni.
1. Ja nepieciešams, pievienojiet reģistrus ar finanšu procesa ierobežojumiem.

### <a name="validate-the-fiscal-registration-process"></a>Validēt finanšu reģistrācijas procesu

Ir ieteicams pārbaudīt finanšu reģistrācijas procesu šādos gadījumos:

- Esat pabeidzis visus jaunā reģistrācijas procesa iestatījumus. Šie iestatījumi ietver reģistrācijas procesu piešķiršanu POS funkcionalitātes profiliem un aparatūras profiliem.
- Jūs esat veicis izmaiņas esošajā finanšu reģistrācijas procesā, un šīs izmaiņas izpildlaikā var būt par iemeslu atšķirīgam finanšu savienotājam. (Piemēram, ir mainīta savienotāja grupa fiskālās reģistrācijas procesa solim, aktivizēts savienotāja funkcionālā profils savienotāja grupā vai pievienots jauns savienotāja funkcionālā profils savienotāja grupai.)
- Aparatūras profiliem ir veiktas izmaiņas savienotāja tehnisko profilu piešķirē.

Lai validētu finanšu reģistrācijas procesu, sekojiet šiem soļiem.

1. Programmā Commerce headquarters atveriet lapu Fiskālās reģistrācijas **process** (**Mazumtirdzniecības un Commerce Channel \> iestatīšanas finanšu \> integrācijas finanšu \> reģistrēšanas procesi**).
1. Atlasiet **Pārbaudīt,** lai apstiprinātu finanšu reģistrācijas procesu.
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

Lai iestatītu kļūdu apstrādes iestatījumus, sekojiet šiem soļiem.

1. Lapā **Finanšu reģistrācijas process** (**Retail un Commerce \> Kanāla iestatīšana \> Finanšu integrācija \> Finanšu reģistrācijas procesi**) varat iestatīt šādus parametrus katrai finanšu reģistrācijas procesa darbībai:

    - **Atļaut izlaist** — šis parametrs iespējo opciju **Izlaist** kļūdu apstrādes dialoglodziņā.
    - **Atļaut atzīmēt kā reģistrētu** — šis parametrs iespējo opciju **Atzīmēt kā reģistrētu** kļūdu apstrādes dialoglodziņā.
    - **Atļaut atlikšanu** – šis parametrs **aktivizē** opciju Atlikt kļūdu apstrādes dialoglodziņā.
    - **Kļūdas gadījumā turpināt** — ja šis parametrs ir iespējots, finanšu reģistrācijas process POS reģistrā var turpināties arī tad, ja transakcijas vai notikuma finanšu reģistrācija ir nesekmīga. Pretējā gadījumā, lai palaistu nākamās transakcijas vai notikuma finanšu reģistrāciju, operatoram ir atkārtot jāmēģina izpildīt nesekmīgo finanšu reģistrāciju, jāizlaiž šī reģistrācija vai attiecīgā transakcija vai notikums ir jāatzīmē kā reģistrēts. Plašāku informāciju skatiet rakstā [Neobligātā finanšu reģistrācija](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Ja ir iespējots parametrs **Kļūdas gadījumā turpināt**, parametrs **Atļaut izlaist** un parametrs **Atļaut atzīmēt kā reģistrētu** automātiski tiek atspējots.

1. Dialoglodziņa **Kļūdu apstrādes** **opcijas** Izlaist un Atzīmēt kā reģistrētas pieprasa, lai **tiktu iespējota atļauja Atļaut izlaist reģistrāciju vai atzīmēt kā** reģistrētu. Lai iespējotu šo atļauju, **dodieties uz lapu Atļauju grupas (** Mazumtirdzniecības un Commerce **Darbinieku \>\> atļauju grupas)** **un iestatiet opciju Atļaut izlaist reģistrāciju vai atzīmēt kā reģistrētu uz** Jā **.**
1. Dialoglodziņa **Kļūdu** apstrādes opcijas Atlikšana iespējošanai ir jābūt **iespējotai atļaujai** Atļaut atlikšanu. Lai iespējotu šo atļauju, dodieties **uz** lapu Atļauju grupas (**Mazumtirdzniecības un Commerce \> Employees Permission \> grupas**) **un iestatiet opciju Atļaut** atlikšanu uz **Jā**.
1. Opcijas **Izlaist**, **Atzīmēt kā reģistrētas un** Atlikt **ļauj** operatoriem ievadīt papildu informāciju, ja finanšu reģistrācija neizdodas. Lai padarītu šo funkcionalitāti pieejamu, finanšu savienotāja **grupā ir jānorāda** kods **Izlaist**, **Iezīmēt** kā reģistrētu un Atlikt infokods. Pēc tam operatoru ievadītā informācija tiek saglabāta kā informācijas koda transakcija, kas saistīta ar finanšu transakciju. Plašāku informāciju par informācijas kodiem skatiet tēmā [Informācijas kodi un informācijas kodu grupas](../info-codes-retail.md).

    > [!NOTE]
    > Trigera funkcija **Prece** netiek atbalstīta informācijas kodiem, kas tiek izmantoti opcijām **Izlaist** un **Atzīmēt kā reģistrētu** finanšu savienotāju grupās.

    - Finanšu savienotāja **grupas lapas** informācijas **kodu** cilnē atlasiet informācijas kodus vai informācijas **kodu** grupas laukos Izlaist, **Iezīmēt kā** reģistrētu un **Atlikt**.

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


## <a name="view-connection-parameters-and-other-information-in-pos"></a>Skatīt savienojuma parametrus un citu informāciju POS

Lai skatītu savienojuma parametrus un citu informāciju POS, sekojiet šiem soļiem.

1. Atveriet Modern POS (MPOS) vai Cloud POS (CPOS).
1. Atlasiet **Iestatījumi**. Ja finanšu integrācija ir aktivizēta, **finanšu integrācijas** sadaļa labajā pusē parādīs šādu informāciju:

    - Finanšu reģistrācijas statuss
    - Pēdējā finanšu darījuma stāvoklis
    - Gaidošo audita notikumu skaits

1. Atlasiet **Detaļas**, lai skatītu šādu informāciju:

    - Reģistrācijas procesa soļi
    - Savienojuma parametri
    - Audita notikumu papildinformācija
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
