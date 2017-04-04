---
title: "Mazumtirdzniecības perifērijas simulators"
description: "Šajā tēmā ir aprakstīts, perifēro simulator rīks, kas tiek nodrošināta ar Microsoft Dynamics 365 operācijām - mazumtirdzniecības."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Mazumtirdzniecības perifērijas simulators

Šajā tēmā ir aprakstīts, perifēro simulator rīks, kas tiek nodrošināta ar Microsoft Dynamics 365 operācijām - mazumtirdzniecības.

<a name="overview"></a>Pārskats
--------

Microsoft Dynamics 365 operācijām - mazumtirdzniecības perifērijas simulators ir rīks, kas palīdz iestatīt, pārbaudītu un novērst ar perifērijas ierīcēm, ko izmanto mazumtirdzniecības vidē. Perifērijas simulators var izmantot, lai racionalizētu mazumtirdzniecības perifērijas ierīču testēšana un novērst problēmas, ko rada nepareiza uzstādīšana vai nepareizi ierīču draiverus. Perifēro simulatora ietver darbvirsmas programmu, kam raksturīga ierīces virtuālās versijās šī dinamika 365 operācijām - mazumtirdzniecības atbalsta. Sadaļa par katru virtuālo ierīce parāda mijiedarbību starp ierīci un mazumtirdzniecības punktam (POS). Jūs varat arī izmantot, lai sniegt ieguldījumu, kas ir derīgs POS dažādus scenārijus. Perifēro simulators nodrošina mijiedarbību starp ražotāju organizācijas un šīs virtuālās ierīces:

-   **Printeris** -perifērijas simulatorā var parādīt ieejas plūsmas, kuras ir konfigurētas POS printerim.
-   **Rindiņu displeja** -jūs varat konfigurēt virtuālā rindu displejs izrādīt aktivitāti fiziska līnija displejā.
-   **Magnētisko svītru lasītāju (MSR)** -mākslīgi radītā magnētiskā svītra notikumi var nosūtīt ro no perifērijas simulators.
-   **Atvilktne** – fiziskās naudas atvilktnes var simulēt.
-   **Drawer 2** -izveidojot otro naudas atvilktne perifērijas simulatorā, varat simulēt scenārijos, kas ietver atsevišķu POS reģistru, kas ir aktīvā divās maiņās.
-   **Skenera** – virtuālā svītru kodu skeneri, kas perifērijas simulatora atbalsta var izdot svītrkods skenēšanas notikumiem.
-   **Mēroga** – virtuālā skala ļauj simulēt krājumu nosvērtajā mijiedarbība ar ražotāju organizācijas.
-   **Personīgo identifikācijas numuru (PIN) pad** -PIN spilventiņu operācijas var simulēt. **Piezīme:** fizisko PIN spilventiņu caur savienotāju maksājumu atbalstu nedrīkst īstenot.
-   **Paraksta uzņemšanas** -perifērijas simulators ir iekļauta virtuālā parakstu tveršanas ierīce, kuru var iestatīt, lai palūgtu norādīt parakstu, kas ir nepieciešami daži piedāvājumi, piemēram, maksājumi no klienta konta.

Perifēro simulatorā var izmantot arī, lai modelētu tastatūras ķīlis notikumiem, kas veidoti no svītru kodu skeneri un MSR. Virtuālās perifērijas simulatora īpaši atbalsta objektu saistīšanas un iegulšanas mazumtirdzniecības POS (OPOS) ierīcēm.

## <a name="key-scenarios"></a>Galvenie scenāriji
### <a name="troubleshooting"></a>Problēmu novēršana

Perifēro simulatorā var izmantot, lai novērstu ierīces uzstādīšana. Ja jums nav perifērijas simulatoru vai otro ierīci no tās pašas klases, tas var būt grūti noteikt, kur problēmas cēlušās. Tomēr, kad jums ir perifērijas simulators, var iestatīt virtuālā ierīcēm un palaist pašu kodu ceļus un biznesa loģiku, kas tiek izmantoti fiziskajām ierīcēm. Raugoties no perifērijas simulators, galvenā atšķirība starp virtuālo ierīces un fiziskajām ierīcēm ir pakalpojuma objekts vai ierīces draiveri. Fiziskās ierīces, ierīces ražotāja sniegto pakalpojumu objekts. Turpretī perifērijas simulators, servisa objekti tiek nodrošināti kā daļu no perifērijas simulators. Kad perifērijas simulatora darbojas pareizi, ja ierīce nedarbojas pareizi, pēc aparatūras profilu ierīces nosaukums tiek mainīts uz reālu ierīces nosaukumu, var pieņemt, ka pastāv problēma ar servisa objektu, ko ražotājs sniedz.

### <a name="training"></a>Apmācība

Perifēro simulatorā var izmantot, lai pievienotu reāli slāni, kuru kasieris, mācības, kad fiziskās aparatūras uzstādīšana nav pieejama. Ja perifērā simulators ir iekļautas mācību scenāriju, kasieris efektīvāk var mijiedarboties ar POS, nodrošinot ievade, piemēram, produkta bārs kods skenē un dāvanu kartes swipes, un, ievērojot, kuru apliecinājumi tiek drukāti konkrētai darbībai.

### <a name="testing"></a>Testēšana

Perifēro simulatorā var izmantot, lai pārbaudītu preču svītrkodus, saņemšanas formātus un tā tālāk, bez nepieciešamības izvietot fiziskajai aparatūrai virtuālajā vidē. Tā fiziskā aparatūra nav nepieciešama un nav nepieciešams izvietot POS klientu aparatūras staciju vai fiziskā datorā, varat ātrāk testa izmaiņas, kas veiktas atpakaļ birojā.

## <a name="set-up-the-peripheral-simulator"></a>Iestatītu perifērijas simulators
### <a name="set-up-a-hardware-profile"></a>Iestatīt aparatūras profils

1.  Lai iestatītu perifērijas simulators, dodieties uz **mazumtirdzniecības un komercijas**&gt;**kanāla iestatījumu**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**Hardware Profili**.
2.  Lai izveidotu jaunu profilu, noklikšķiniet uz **New**.
3.  Ievadiet vērtības **profila numuru** un **aprakstu** laukus.
4.  Šādu tabulu izmanto, lai uzstādītu virtuālo ierīces, kas jātestē. Šeit ir paskaidrojums tabulas kolonnām:
    -   **Ierīce** – šajā kolonnā dod vārdu FastTab, kas jūs paplašināt, lai uzstādītu ierīci.
    -   **Ierīces tips** – šajā ailē vērtība, kuru atlasāt laukā, kas ir apzīmēti ar ierīces nosaukumu.
    -   **Ierīces nosaukums** – šajā kolonnā dod precīzu vērtību, ko ievadāt ierīces nosaukumu. **Svarīgi:** ierīču nosaukumi, kas doti šeit ir nepieciešami, jo aparatūras stacijas izmanto šos īpašos nosaukumus, lai risinātu ierīcēm. Ja jūs neizmantojat šos īpašos nosaukumus, ierīce nebūs izmantojamas.

    | Ierīce            | Ierīces veids | Ierīces nosaukums              |
    |-------------------|-------------|--------------------------|
    | Printeris           | OPOS        | MockOPOSPrinter          |
    | Rindu displejs      | OPOS        | MockOPOSLineDisplay      |
    | MJL (magnētiskās joslas lasītājs)               | OPOS        | MockOPOSMSR              |
    | Dokumenta sastādītājs            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Skeneris           | OPOS        | MockOPOSScanner          |
    | Mērogs             | OPOS        | MockOPOSScale            |
    | PIN bloks           | OPOS        | MockOPOSPinPad           |
    | Paraksta ieguve | OPOS        | MockOPOSSignatureCapture |

**Piezīme:** nav specifiski iestatījumi aparatūras profils ir nepieciešams, lai modelētu notikumiem tastatūras ķīlis, svītru kodu skeneri un MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Aparatūras profilu piešķirt reģistrs

1.  Pēc aparatūras profilu izveides dodieties uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**reģistrē**.
2.  Šajā **POS reģistros** sarakstu, noklikšķiniet uz saites **reģistra numurs** lauku reģistru, kas būtu jāizmanto perifērijas simulators.
3.  Noklikšķiniet uz **Rediģēt**.
4.  Šajā **profili** sadaļa, jo **aparatūras profilu** lauku, izvēlieties, kuru izveidojis virtuālo perifērijas aparatūras profilu.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Sinhronizēt izmaiņas kanālu datu bāzē

1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**.
2.  Atlasiet **1090** sadalījuma grafiks.
3.  Noklikšķiniet uz **bēgtu** sinhronizēt izmaiņas, lai ražotāju organizācijas.

Pēc tam, kad dati tiek sinhronizēti, jaunas aparatūras profilu un izmaiņas reģistrā ir pieejami kanālu datu bāzē.

## <a name="install-the-peripheral-simulator"></a>Instalētu perifērijas simulators
1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**Hardware Profili**.
2.  Noklikšķiniet uz **Download**, un pēc tam noklikšķiniet uz **PeripheralSimulator**. **Piezīme:** uznirstošo logu bloķētāji ir jāizslēdz, pirms varat sākt lejupielādēt perifērijas simulators.
3.  Pēc tam, kad lejupielāde ir pabeigta, atveriet **lejupielādes** mapi un veiciet dubultklikšķi uz **VirtualPeripherals.msi**, lai startētu instalēšanas programmu.
4.  Instalētu perifērijas simulators, izmantojot noklusējuma iestatījumus.

Papildus perifērijas simulators, jāinstalē kopējā kontroles objekti no Monroe Consulting Services. Pretējā gadījumā perifērijas simulatora nedarbosies pareizi. Lai lejupielādētu kopīgas kontroles objekti, dodieties uz <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Izmantojot perifēro simulators
Lai sāktu perifērijas simulators, noklikšķiniet uz **sākt** datorā, ievadiet **mazumtirdzniecības perifērijas simulator**, un pēc tam atlasiet app, kad tā parādās meklēšanas rezultātos. Pēc tam, kad sākat perifērijas simulators, noklikšķiniet uz ierīces nosaukuma, lai skatītu atbalstītajām ierīcēm. Šīs ierīces tiek uzskaitīti kā ciļņu loga kreisajā pusē. Lai skatītu noteiktu ierīci, noklikšķiniet uz cilnes šai ierīcei.

### <a name="line-display-capabilities"></a>Rindiņu displeja iespējām

Līniju displejs ir pirmā ierīce, kas ir uzskaitītas perifērijas simulators. Kad virtuālā rindu displejs ir konfigurēts, tas parāda posteņus kā tie tiek skenēti POS darījumu. Papildus rindas vienumi, displejā tiek parādīts kopējais, kas pienākas izvēloties piedāvājumu pie ražotāju organizācijas. Tas arī parāda atlikums, kas pienākas ja piedāvājums ir ievadīts, bet bilance joprojām ir jāmaksā par darbību. Ražotāju organizācijas nav, ja tiek izmantota ziņojumu var parādīt norāda kases aizvēršanas. Ziņojums ir jākonfigurē **līniju displejs** FastTab aparatūras profilu.

### <a name="cash-drawer-capabilities"></a>Naudas atvilktnes iespējas

Naudas atvilktne ir otrā ierīce, kas ir uzskaitītas perifērijas simulators. Aparatūras profils ir konfigurēts izmantot virtuālās naudas atvilktnes, POS tiek atvērts naudas atvilktnes aktīvo SHIFT, atbildot uz atvilktni operācijas, piemēram, konkursu deklarācijām, un tādējādi var veikt kases mainīt vai noguldīt naudas standarta cash-and-carry transakciju laikā. Virtuālās naudas atvilktnes ir etiķetes **galvenajiem atvilktne** un **vidējā atvilktne**. Šīs etiķetes attēlotu atvilktnes un atvilktnes 2 aparatūras profilu, attiecīgi. Atvilktne ir slēgts, slēgtā naudas atvilktne attēls tiek parādīts un uz slēgto naudas atvilktnes poga ir iezīmēta **atvērtas atvilktnes**. Ja noklikšķināt uz šīs pogas, attēls tiek aizstāta ar attēlu atvērtu kases dokumenta sastādītāja, norāda, ka atvilktnes tagad ir atvērts. Pogas atvērt naudas atvilktne ir apzīmēts **tuvu atvilktne**. Vairākām operācijām pie ražotāju organizācijas var izraisīt naudas atvilktnes atvēršanai. Lielākā daļa operāciju nevar turpināt, kamēr naudas atvilktne ir atvērts. Izņēmums ir dažas dienas beigu procedūras. Ja POS lietotājs saņem kļūdas ziņojumu, kurā teikts, ka darbību nevar veikt, kamēr ir atvērts naudas atvilktnes, lietotājam jāaizver fiziskās vai virtuālās naudas atvilktnes, lai turpinātu. Ja naudas atvilktne ir atzīmēts kā **Shared** aparatūras profilu sistēma nav pārbaudīt, ka atvilktnē ir slēgta pirms operācijas. Darbības ieņēmumi kā parasti, pat tad, ja naudas atvilktne ir atvērts. Šo darbību atbalsta scenārijus, kur naudas atvilktnes var koplietot pārdošanas partneri un kur viena saistīt izmanto naudas atvilktnes, kamēr vēl viens asociētais nesaistītiem uzdevumiem veic sava POS ierīces. Izmaiņām, kas veiktas ar kases atvilktni nav acīmredzama, kamēr pašreizējās pārmaiņas ir aizvērts, un tiek atvērts jaunā maiņa.

### <a name="msr-capabilities"></a>MSR iespējas

Perifēro simulators nodrošina spēcīgu atbalstu virtuālā MSR operācijas, strādā vai nu OPOS vai tastatūras ķīlis režīmā. OPOS režīmu, nepieciešams konfigurēt MSR, strādāt kā OPOS ierīces aparatūras profilu. Tastatūras ķīlis režīmā tikai nosūta Microsoft Windows tastatūras ķīļa datus notikumiem. Bez atšķirības iestatījumā, OPOS un tastatūras ķīlis veidiem atšķiras šādos veidos:

-   POS klientu ļauj OPOS MSR ierīcēm noteiktiem scenārijiem, piemēram, scenārijus, kas ļauj lojalitātes vai dāvanu kartes ierakstu magnētiskās joslas datu.
-   Tastatūru režīmā ķīlis perifērijas simulators nosūta tastatūras ķīļa datus laukā, kas ir aktīva, kad dati tiek nosūtīti. Šāda darbība līdzinās uzvedība, kas notiek, ja dati ir ievadīti, izmantojot tastatūru. Lai izmantotu MSR, keyboard wedge, lietotājs jāpārslēdzas uz mazumtirdzniecības mūsdienu POS (MPOS) lai pārliecinātos par pareizu jomā ir saņemti dati. Tādēļ, kavēšanās var konfigurēt tā, lai lietotājam ir laiks, lai pārliecinātos, ka dati tiks nosūtīti uz pareizo lauku.

#### <a name="testing-gift-and-payment-card-swipes"></a>Dāvana un maksājumu karšu swipes testēšana

Virtuālais MSR, kas perifērijas simulators piedāvā arī ļauj konfigurēt īpašu MSR datu testa scenāriju dāvanu un maksājumu karšu swipes. Lai izveidotu karti, noklikšķiniet uz plusa zīmes (**+**) pogas un izvēlieties kartes veidu. Pēc tam norādīt kartes numurs vai izsekot datiem, kas jānosūta POS, kā arī derīguma termiņa beigu mēnesim un gadam kartei, ko definējat. Vērtība, kuru atlasāt **kartes veida** lauks ir tikai etiķete, kas var kartēt uz kartes. Šī uzlīme ļauj vieglāk noteikt kartes, ja viņi novēcināja caur perifērijas simulators. Atlasiet kartes, kas konfigurēti perifērijas simulatorā, izmantojot bultiņas pa kreisi (**&lt;**) un labo bultiņu (**&gt;**) pogas virs kartes attēls. Var rediģēt un dzēst, izmantojot kartes **rediģēt** un **dzēst** uz pluszīmes blakus pogām (**+**) pogu.

### <a name="pin-pad"></a>PIN bloks

Jūs varat konfigurēt PIN spilventiņu simulatora simulēt OPOS PIN spilventiņu. Elektronisko naudas pārskaitījumu (EFT) darbība tiek veikta pie POS un prasa PIN ierakstu, staciju aparatūras prasa PIN ierīce pieprasa PIN ievadnē. Strādāt, PIN spilventiņu perifērijas simulatorā prasa EFT maksājumu savienotājs atbalsta.

### <a name="printer"></a>Printeris

Perifēro virtuālo printeri tikai parāda ieejas, kā tie tiek drukāti no POS. Ja drukas darbība rada vairākas ieejas, varat ritināt kvītis.

#### <a name="configure-receipt-printing"></a>Konfigurējiet drukāšanas saņemšanas

1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**Hardware Profili**.
2.  Atlasiet, kuru izveidojis virtuālo perifērijas aparatūras profilu.
3.  Par **printera** FastTab, noklikšķiniet uz **rediģēt**.
4.  Šajā **saņemšanas profila ID** lauku, atlasiet saņemšanas profilu.
5.  Click **Save**.

### <a name="scale"></a>Mērogs

Mēroga produktu pievienota POS darbībai un skalas ir konfigurēta, ro svaru iegūst mērogu. Gan virtuālo un fizisko mērogs, produktu vai svars jānorāda pirms produkts ir pievienota darbība. Pirms pievienojat mēroga produktu darbība, doties uz skalas perifērijas simulatorā un izmantojiet pluszīmes (**+**) un mīnusa zīme (**-**) taustiņu, lai regulētu svars, kuru mērogs būtu jāziņo. Var arī ievadīt tieši vēlamo svaru **pašreizējo vērtību** lauks. Vienību svara skalu var pielāgot, izmantojot pluszīmi (**+**), **rediģēt**, un **dzēst** pogas. Šādā veidā vienībām var norādīt, pamatojoties uz produktiem, ko nosver vai kur skala tiek izmantota locale.

#### <a name="configure-a-scale-product"></a>Konfigurēt mēroga produktu

1.  Dodieties uz **mazumtirdzniecības un****komercijas**&gt;**produktiem un kategorijas**&gt;**atbrīvo produktus pēc kategorijām**.
2.  Preces ieraksta atvēršana.
3.  Atlasiet produkta svars.
4.  Par **mazumtirdzniecības** FastTab, iestatiet **mēroga produktu** opciju no **Nr** uz **Jā**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Sinhronizēt izmaiņas kanālu datu bāzē

1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**.
2.  Atlasiet **1040** sadalījuma grafiks.
3.  Noklikšķiniet uz **bēgtu** sinhronizēt izmaiņas, lai ražotāju organizācijas.

Pēc tam, kad dati tiek sinhronizēti, pievienojot POS darījumu apjoma produktu, ražotāju organizācijas pārbauda svaru skalu.

### <a name="signature-capture"></a>Paraksta ieguve

Virtuālā parakstu tveršanas ierīce liek lietotājam sniegt parakstu virtuālā parakstu uzņemšanas laukumā, kad piedāvājums, kas tiek izmantots nepieciešams paraksts. Lietotājs var akceptēt parakstu liecina, ka ražotāju organizācijas. Kasieris, tad var pieņemt paraksts. Parakstu, tad tiek saglabātas kopā ar konkursa un tiek sinhronizētas atpakaļ iestādei, kā arī citus darījumu datus.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Konkursa uzstādījums ir pieprasīt parakstu

1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**kanālus**&gt;**mazumtirdzniecības veikali**&gt;**visiem mazumtirdzniecības veikali**.
2.  Atlasiet mazumtirdzniecības veikalu.
3.  Noklikšķiniet uz **Rediģēt**.
4.  Noklikšķiniet uz **iestatīt**, un pēc tam **iestatīt** noklikšķiniet uz **maksāšanas**.
5.  Noklikšķiniet uz **Rediģēt**.
6.  Atlasiet maksāšanas metode, kas paredz parakstu.
7.  Šajā **vispārējās** sadaļu zem **paraksta Capture**, iestatiet **izmantot parakstu tveršanas ierīce** iespēju **Jā**.
8.  Šajā **paraksta uzņemšanas minimālā summa** ievadiet minimālo summu, kurai vajadzētu izraisīt paraksta uzņemšanas.

#### <a name="synchronize-changes-to-the-channel-database"></a>Sinhronizēt izmaiņas kanālu datu bāzē

1.  Dodieties uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**.
2.  Atlasiet **1070** sadalījuma grafiks.
3.  Noklikšķiniet uz **bēgtu** sinhronizēt izmaiņas, lai ražotāju organizācijas.

Pēc tam, kad dati tiek sinhronizēti, kad piedāvājums tiek izmantots, kas nepieciešams parakstu un summa atbilst paraksta slieksni, POS prasa parakstu uz virtuālā parakstu tveršanas ierīce.

## <a name="additional-configuration"></a>Papildu konfigurācijas
Jūs varat rediģēt perifērijas simulator konfigurācijas failu, lai pareizāk risināt jūs testēšanas scenāriji. Jūs varat atrast konfigurācijas failu c\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurācijas failā definē vienības, kas ir pieejams testēšanai uz skalas, karšu tipus, kas ir pieejams testēšanai un svītrkodu tipus. Mainot teksta vērtības ar konfigurācijas failu, var pievienot, piemēram, jaunas kartes tipu vai mērvienības, ko var atlasīt izpildlaikā. Jaunās vērtības tiks parādītas pēc restartēšanas app.

## <a name="troubleshooting"></a>Problēmu novēršana
Perifēro simulatora aktivitātes tiek reģistrēti laikā perifērijas simulators. Jūs varat atrast log c\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Perifēro simulatorā arī atskaitās jautājumiem Windows notikumu žurnālam, kuram var piekļūt pie **lietojumprogrammu un pakalpojumu žurnāli,**&gt;**Microsoft**&gt;**DynamicsAX**. Ja izmaiņas, ko veicāt aparatūras profilu vai citās jomās nav acīmredzama, izmantojot MPOS vai perifērijas simulators, pārbaudiet izplatīšanas plānotāju darba vietas, kas tu lieto, lai sinhronizētu datus ar kanālu datu bāzi. Ja izmaiņas tika sinhronizēti, taču joprojām nav skaidrs, pie POS, restartējiet POS klientu. Izmaiņas, lai konfigurētu naudas atvilktnes nav efektīvi, līdz brīdim, kad tiek veidota jaunā maiņa. Tādēļ, ja vēlaties veikt izmaiņas naudas atvilktnes, pārliecinieties, vai vienmēr Aizvērt esošo pāreja uz jauno naudas atvilktnes setup tests. Dažreiz, ja ražotāja draiveris ir instalēts pēc kopīgas kontroles objekti no Monroe Consulting Services, vadītājs var radīt kopējas kontroles objekti vairs nedarbojas pareizi. Šajā gadījumā jums atkārtoti jāinstalē kopējā kontroles objekti.

<a name="see-also"></a>Skatiet arī
--------

[Retail peripherals overview](retail-peripherals-overview.md)


