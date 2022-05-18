---
title: Mazu paku nosūtīšana
description: Šajā tēmā ir sniegta informācija par mazu paku nosūtīšanas (SPS) līdzekli. Šis līdzeklis ļauj korporācijai Microsoft Dynamics 365 Supply Chain Management iesniegt pārvadātājam datus par iepakotu konteineru un pēc tam no šī pārvadātāja saņemt atpakaļ nosūtīšanas etiķeti, nosūtīšanas likmi un izsekošanas numuru.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e8e2bda39b9de241d17fcf3cb9acce2b8015efd2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687621"
---
# <a name="small-parcel-shipping"></a>Mazu paku nosūtīšana

[!include [banner](../../includes/banner.md)]

Izmantojot maza sūtījuma (SPS) līdzekli, korporācija Microsoft Dynamics 365 Supply Chain Management var tieši sazināties ar nosūtīšanas pārvadātājiem, izmantojot pārvadātāju API sakaru struktūru. Šī funkcionalitāte ir noderīga, ja noslogojiet atsevišķus pārdošanas pasūtījumus caur komerciālajiem kravu pārvadātājiem, nevis izmantojot konteinera nosūtīšanu vai mazāk nekā-kravas (LTL) slodzi.

SPS funkcija mijiedarbojas ar jūsu sūtījumu pārvadātāju, izmantojot *atvēlēto likmes* programmu. Jūsu organizācijai attīstiet šo likmes programmu sadarbības ar jūsu pārvadātāja vai pārvadātāja pārkraušanas centra pakalpojumu. Šis līdzeklis ļauj Supply Chain Management iesniegt pārvadātājam datus par iepakotu konteineru un pēc tam no šī pārvadātāja saņemt atpakaļ nosūtīšanas etiķeti, nosūtīšanas likmi un izsekošanas numuru.

Atgrieztā nosūtīšanas likme ir pievienota saistītajam pārdošanas pasūtījumam kā papildmaksa. Pēc tam atgriezto nosūtīšanas etiķeti var automātiski izdrukāt, izmantojot Zebra programmēšanas valodas (ZPL) printeri un pielietojot sūtījumam. Pārvadātājs skenēs šo nosūtīšanas etiķeti, saņemot savā noliktavā iepakojumus.

## <a name="prepare-your-system-to-support-sps"></a>Sistēmas sagatavošana SPS atbalstam

Pirms varat sākt lietot SPS funkcionalitāti, līdzekļa pārvaldībā ieslēdziet SPS funkciju, pievienojiet likmes programmu un iestatiet **Transportēšanas pārvaldības** un **Noliktavas pārvaldības moduļus** tā atbalstam.

### <a name="turn-on-the-sps-feature"></a>SPS līdzekļa iespējošana

Lai varētu izmantot SPS līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Transportēšanas pārvaldība*
- **Līdzekļa nosaukums:** *Mazu paku nosūtīšana*

### <a name="deploy-and-set-up-rate-engines"></a>Izvietot un iestatīt likmes programmas

Supply Chain Management nav ietverta neviena likmes programma. Ir jāiegūst vai jāizveido likmes programmas, kas jums nepieciešamas, un pēc tam tās jāpievieno jūsu sistēmai. Tomēr Microsoft sniedz likmes paraugprogrammu, ko varat izmantot testēšanai.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Lejupielādēt un izvietot demonstrācijas likmes programmu

Izpildiet šīs darbības, lai iegūtu likmes paraugprogrammu.

1. GitHub lejupielādēt [dinamiskās saites bibliotēku (DLL) likmes paraugprogrammu](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. Supply Chain Management serverī saglabājiet DLL mapē **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Izveidot un izvietot funkcionālās likmes programmas

Informāciju par to, kā izveidot un izvietot funkcionālās likmes programmas, lai tās varētu izmantot ražošanas vai testēšanas vidē, skatiet šādas tēmas:

- [Jaunas transportēšanas pārvaldības programmas izveide](../transportation/create-new-transportation-management-engine.md)
- [Transportēšanas pārvaldības programmu iestatīšana](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Papildinformāciju par SPS likmes programmas izveidošanas veidu skatiet tālāk šajā rakstā: [Mazo paku nosūtīšana: kā līdzsvarot mazu paku nosūtīšanas Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Iestatīt likmes programmu Supply Chain Management

Kad esat izveidojis un izvietojis SPS likmes programmu, veiciet šos soļus, lai to iestatītu.

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatīšana \> Vērtējums \> Likmes šablons**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādus laukus:

    - **Likmes programma** - ievadiet unikālu likmes programmas nosaukumu. Ja izmantojat demonstrācijas likmes programmu, ievadiet *Likmes paraugprogrammu*.
    - **Nosaukums** – ievadiet likmes programmas īsu aprakstu. Ja izmantojat demonstrācijas likmes programmu, ievadiet *Likmes paraugprogrammu*.
    - **Vērtējuma metadatu ID** - izvēlieties pamatu, kas ir jāizmanto, lai aprēķinātu jūsu likmi. Piemēram, jūsu likme var tikt aprēķināta, pamatojoties uz attālumu. Ja izmantojat likmes paraugprogrammu, varat atstāt šo lauku tukšu.
    - **Programmas komplektācija** - ievadiet izvietotās DLL pakotnes faila nosaukumu. Ja izmantojat likmes paraugprogrammu, ievadiet *TMSSmallParcelShippingEngine.dll*.
    - **Programmas klase** – ievadiet klases nosaukumu, kas tika izveidots jūsu likmes programmai. Ja izmantojat likmes paraugprogrammu, ievadiet *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Piemērs

Šajā piemērā ir parādīts, kā iestatīt un izmantot SPS pēc tam, kad esat sagatavojis sistēmu, kā aprakstīts iepriekš šajā tēmā. Šajā scenārijā tiek izmantota iepriekš minētā likmes paraugprogramma.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [paraugdati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

### <a name="set-up-the-scenario"></a>Scenārija iestatīšana

Šajā piemērā jums ir jābūt demonstrācijas pārvadātājam, pārvadātāju grupai, iepakošanas politikai un iepakošanas profilam. Tālākajāš apakšdaļās ir izskaidrots, kā sagatavot scenārijam nepieciešamos ierakstus. Ražošanas scenārijā iestatīšanas process parasti ir līdzīgs šeit aprakstītajam procesam. Tomēr jūs iestatīsiet dažādas vērtības.

#### <a name="set-up-carriers"></a>Sūtījumu pārvadātāju iestatīšana

Lai iestatītu pārvadātāju, rīkojieties šādi.

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Sūtījumu pārvadātāji**.
1. Lai pievienotu pārvadātāju, darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*
    - **Nosaukums:** *Parauga pārvadātājs*
    - **Režīms:** *Sauszeme*

1. Kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības:

    - **Aktivizējiet nosūtījuma pārvadātāja:** *Jā*
    - **Aktivizējiet pārvadātāja vērtēšanu:** *Jā*

1. Kopsavilkuma cilnē **Pakalpojumi** atlasiet **Jauns**, lai pievienotu režģim pakalpojumu.
1. Iestatiet šādas vērtības jaunajam pakalpojumam:

    - **Pārvadātāja pakalpojums:** *Parauga pārvadātāja pakalpojums*
    - **Nosaukums:** *Parauga pārvadātāja pakalpojums*
    - **Transportēšanas metode:** *Sauszeme*

    Pēc vajadzības ievadiet vērtību visiem citiem laukiem. (Saglabājot jauno sūtījuma pārvadātāja ierakstu, tiks izveidots jauns piegādes veids un **Piegādes veida** lauks tiks iestatīts automātiski.)

1. Kopsavilkuma cilnē **Novērtējuma profili** noklikšķiniet uz **Jauns**, lai pievienotu režģim novērtējuma profilu.
1. Iestatiet šādas vērtības jaunajam profilam:

    - **Novērtējuma profils:** *Parauga pārvadātāja pakalpojums*
    - **Nosaukums:** *Parauga pārvadātāja pakalpojums*
    - **Likmes likmes programma:** *Likmes paraugprogramma*

    Pēc vajadzības ievadiet vērtību visiem citiem laukiem.

1. Darbību rūtī atlasiet **Saglabāt**.

Plašāku informāciju par to, kā iestatīt abonementus, skatiet tēmā [Nosūtīšanas pārvadātāju iestatīšana](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Iestatīt pārvadātāju pakalpojumu kontus

Lai iestatītu pārvadātāja pakalpojuma kontu, rīkojieties šādi.

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatīšana \> Vērtējums \> Pārvadātāja pakalpojuma konts**.
1. Lai pievienotu pārvadātāja pakalpojuma kontu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet šādas vērtības jaunajam kontam:

    - **Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*
    - **Pārvadātāja pakalpojums:** *Parauga pārvadātāja pakalpojums*
    - **Pārvadātāja debitora konta numurs:** Pārvadātāja debitora konta numurs, kas tiek izmantots, lai pārbaudītu un autentificētu savienojumu ar sūtījuma pārvadātāju. Šo vērtību nodrošina jūsu pārvadātājs. Ja izmantojat demonstrācijas pakalpojumu, varat ievadīt papildu vērtību.
    - **Vieta:** *6*
    - **Noliktava:** *62*

    > [!NOTE]
    > Bieži **Pārvadātāja debitora konta numura vērtība** ir vienīgā vērtība, kas nepieciešama, lai autentificētu savienojumu. Tomēr, ja jūsu pārvadātājam ir nepieciešami papildu autentifikācijas parametri, jūsu uzņēmumam šī lapa ir jāpielāgo, lai pievienotu atbilstošus papildu laukus.

#### <a name="set-up-a-container-packing-policy"></a>Konteineru iepakošanas politiku iestatīšana

Lai iestatītu konteinera iepakošanas politiku, izpildiet tālāk aprakstītās darbības.

1. Ja vēl neesat iestatījis ZPL printera definīciju, lai to iestatītu, izmantojiet dokumentu maršrutēšanas aģenta programmu. Papildinformāciju skatiet [Dokumentu drukāšanas apskatu](../../fin-ops-core/dev-itpro/analytics/print-documents.md) un saistītās tēmas.
1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru iepakošanas politikas**.
1. Lai pievienotu pārvadātāja pakalpojuma kontu, darbību rūtī atlasiet **Jauns**.
1. Jaunās politikas galvenē iestatiet tālāk norādītās vērtības:

    - **Konteinera iepakošanas politika:** *Iepakošanas parauga politika*
    - **Apraksts:** Politikas apraksts

1. Kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības:

    - **Noliktava:** *62*
    - **Noklusējuma galīgā sūtījuma novietojums:** *Nosūtīšanas krava*
    - **Svara vienība:** *KG*
    - **Konteineru slēgšanas politika:** *Automātiska izlaide*
    - **Konteinera izlaišanas politika:** *Padarīt pieejamu beigu nosūtīšanas vietā*

1. Kopsavilkuma cilnē **Konteinera manifests** varat iestatīt šādas vērtības:

    - **Automātisks manifests konteinera slēgšanas laikā:** *Jā*
    - **Konteinera manifesta prasības:** *Transportēšanas pārvaldība*
    - **Drukāt konteinera saturu:** *Nē*

1. Kopsavilkuma cilnē **Pārvadātāja etiķetes drukāšana** varat iestatīt šādas vērtības:

    - **Drukāt konteinera nosūtīšanas etiķeti:** *Vienmēr*
    - **Printera nosaukums:** ZPL printera nosaukums, kam jādrukā nosūtīšanas etiķetes

#### <a name="set-up-a-packing-profile"></a>Iepakošanas profila iestatīšana

Lai iestatītu iepakošanas profilu, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Iepakošana \> Iepakošanas profili**.
1. Lai pievienotu režģim iepakošanas profilu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet šādas vērtības jaunajam profilam:

    - **Iepakošanas profila ID:** *Iepakošanas parauga profils*
    - **Apraksts:** Profila apraksts
    - **Konteinera iepakošanas politika:** *Iepakošanas parauga politika*
    - **Konteinera ID režīms:** *Automātiski*
    - **Konteinera veids:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Iestatīt debitoru SPS pārvadātāja izmantošanai

Veiciet šīs darbības, lai iestatītu debitoru un varētu izmantot izveidoto pārvadātāju.

1. Dodieties uz sadaļu **Debitori \> debitori \> Visi debitori**.
1. Režģī atrodiet un atlasiet debitoru *US-027*.
1. Darbību rūtī cilnes **Vispārīgi** grupā **Iestatījumi** atlasiet **Pārvadātāja debitora konti**.
1. Lapā **Pārvadātāja debitora konti** darbību rūtī atlasiet **Jauns**, lai pievienotu režģim kontu.
1. Iestatiet šādas vērtības jaunajam kontam:

    - **Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*
    - **Pārvadātāja debitora konta numurs:** *12345* (Vērtība nav būtiska šim scenārijam, bet tā tiks pievienota nākamajā sadaļā.)

### <a name="go-through-the-example-scenario"></a>Iet cauri piemēra scenārijam

Pēc visu parauga datu iestatīšanas atbilstoši iepriekšējā sadaļā aprakstītajam, varat iziet cauri piemēra scenārijam.

#### <a name="create-a-sales-order-and-process-the-work"></a>Izveidot un apstrādāt pārdošanas pasūtījumu un darbu

Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Pārdošanas pasūtījuma izveide** **Klienta konta** laukā atlasiet *US-027*.
1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma galvene** laukā **Pārvadātāja debitora kods** iestatiet vērtību, kuru atlasījāt šim debitoram iepriekš (*12345*).
1. Sadaļā **Pārdošanas pasūtījuma rindas** pievienojiet pārdošanas rindu un iestatiet tai šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *1*
    - **Vieta:** *6*
    - **Noliktava:** *62*

1. Pārejiet uz skatu **Galvene**.
1. Kopsavilkuma cilnē **Piegāde** iestatiet šādas vērtības:

    - **Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*
    - **Pārvadātāja pakalpojums:** *Parauga pārvadātāja pakalpojums*

1. Pārejiet atpakaļ uz skatu **Rindas**. Ja tiek piedāvāts atjaunināt pārdošanas rindu piegādes veidu, atlasiet **Jā**.
1. Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet iepriekš iestatīto pasūtījuma rindu un pēc tam atlasiet **Krājums \> Rezervēšana**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Darbs ir izveidots, lai pārvietotu krājumus no izdošanas vietas uz iepakošanas staciju.

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava \> Detalizēta informācija par sūtījumu**.
1. Lapā **Detalizēta informācija** par sūtījumu atzīmējiet sūtījuma ID. Tas būs nepieciešams, kad iepakosiet sūtījumu iepakošanas stacijā.
1. Aizveriet **Detalizēta informācija par sūtījumu** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Atzīmējiet pārdošanas pasūtījuma numuru un pēc tam dodieties uz darbu **Noliktavas pārvaldība \> Darbs \> Visi darbi**.
1. Izmantojiet pārdošanas pasūtījuma numuru, lai atrastu un atlasītu darbu, kas tika izveidots pasūtījumam.
1. Darbību rūts cilnē **Darbs** atlasiet **Pabeigt darbu**.
1. **Darba pabeigšanas** lapas **Lietotāja ID** laukā atlasiet lietotāja ID. Darbību rūtī atlasiet **Apstiprināt darbu**.
1. Ja darbs tiek validēts, atlasiet darbību rūtī **Pabeigt darbu**.

    Darbs ir atzīmēts kā pabeigts, lai simulētu krājumu kustību uz iepakošanas staciju.

#### <a name="pack-the-shipment"></a>Sūtījuma iepakošana

Lai iepakotu sūtījumu, veiciet sekojošās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbinieks** un pārliecinieties, vai noliktavas pārvaldībai jūsu lietotāja konts ir saistīts ar darbinieka kontu.
1. Dodieties uz **Noliktavas pārvaldība \> Izdošana un konteinerizēšana \> Iepakot**.
1. Dialoglodziņā **Atlasīt iepakošanas vietu** iestatiet sekojošas vērtības:

    - **Vieta:** *6*
    - **Noliktava:** *62*
    - **Atrašanās vieta:** *Pakotne*
    - **Iepakošanas profila ID:** *Iepakošanas parauga profils*

1. Atlasiet **Labi**.
1. Tiek atvērta lapa **Iepakošana**. Ražošanas scenārijā darbinieks skenēs numura zīmi vai sūtījuma ID. Tomēr šajā scenārijā atveriet lapu **Visas kravas** un uzmeklēs sūtījuma numuru sūtījumam, ko tikko izveidojāt. Pēc tam ievadiet šo vērtību laukā **Numura zīme vai krava** lapā **Iepakošana**. Vai arī ievadiet projekta ID, kuru iepriekš atzīmējāt.
1. Darbību rūtī atlasiet **Jauns konteiners**.
1. Dialoglodziņš, kurā ir redzama detalizēta informācija par jauno konteineru. Atstājiet noklusējuma vērtības un pēc tam atlasiet **Labi**.
1. **Pakotnes** lapas **Krājumu iepakojuma** kopsavilkuma cilnes laukā **Identifikators** atlasiet *A0002*, lai šo krājumu iepakotu. Krājums ir pievienots konteineram.
1. Darbību rūtī atlasiet **Sūtījumu konteineri**.

    Parādītajā **Kravas konteineru** lapā ir tā konteinera rinda, kuru tikko izveidojāt. Tomēr **Konteinera manifesta ID** lauks šajā rindā pašlaik ir tukšs, jo neesat vēl saņēmis nosūtīšanas etiķeti un izsekošanas numuru no pārvadātāja.

1. Darbību rūtī atlasiet **Slēgt konteineru**.
1. Dialoglodziņā **Aizvērt konteineru** iestatiet lauku **Bruto svars** uz *1 kg* un pēc tam atlasiet **Labi**.

    Nosūtīšanas uzlīme tagad ir jādrukā iepriekš atlasītajā ZPL printerī. Tiem vajadzētu līdzināties šādam piemēram.

    ![Nosūtīšanas uzlīmes piemērs.](media/sps-label-example.png "Nosūtīšanas uzlīmes piemērs")

1. Ievērojiet, ka **Konteinera manifesta ID** un **Kopējās kravas** vērtības ir pievienotas kā saņemtas no pārvadātāja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]