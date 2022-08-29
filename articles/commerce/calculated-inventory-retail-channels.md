---
title: Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem
description: Šajā rakstā ir aprakstīts, kā uzņēmums Microsoft Dynamics 365 Commerce var izmantot, lai skatītu novērtēto rīcībā esošo preču pieejamību tiešsaistes un veikala kanālos.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8d656cc82472e0515f0f8a64ec21c6c674223ec6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279686"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā uzņēmums Microsoft Dynamics 365 Commerce var izmantot, lai skatītu novērtēto rīcībā esošo preču pieejamību tiešsaistes un veikala kanālos.

## <a name="accuracy-of-inventory-availability"></a>Krājumu pieejamības precizitāte

Commerce izmanto vairākus serverus un datu bāzes, lai nodrošinātu mērogojamību un veiktspēju. Tāpēc ir svarīgi, lai jūs saprastu, ka pieejamās krājumu vērtības, kas tiek nodrošinātas, izmantojot pārdošanas punktu (POS) programmu, e-komercijas krājumu pieejamības programmas programmēšanas interfeisu (API) un rīcībā esošo krājumu lapas programmā Commerce Headquarters, var nebūt 100 procentīgi precīzas reāllaikā. Ja transakcijas, kas ir izveidotas precēm tiešsaistes vai veikala kanālā, vēl nav sinhronizētas ar Headquarters, tad rīcībā esošo krājumu lapas programmā Headquarters var neparādīt precīzu reāllaika krājumu vērtību šīm precēm. Pretējā gadījumā, ja jūs konfigurējāt savu uzņēmumu tā, lai lietotāji programmā Headquarters vai citās integrētās programmās var pārdot, saņemt, atgriezt, vai kā citādi pielāgot krājumus no veikala vai tiešsaistes noliktavas, POS vai tiešsaistes kanālam var nebūt visas informācijas, kas nepieciešama, lai parādītu precīzu reālā laikā krājumu vērtību.

Ir svarīgi saprast, ka visi rīcībā esošie pieejamības dati, kas tiek sniegti darbības dienā, tiek uzskatīti par aptuvenu vērtību. Tāpēc, ja mēģināt salīdzināt rīcībā esošo krājumu informāciju, ko nodrošina programma, ar faktiskajiem fiziskajiem krājumiem plauktos, vai mēģināt salīdzināt rīcībā esošās vērtības, kas tiek rādītas POS, ar rīcībā esošajiem datiem, kas atrodami vienai un tai pašai noliktavai programmā Headquarters, vērtības var atšķirties. Šī atšķirība darbības dienā ir sagaidāma, un to nevajadzētu uzskatīt par problēmu. Ja vēlaties veikt datu auditu un pārliecināties, ka vērtības, kas tiek sniegtas POS, API un Headquarters, atbilst faktiskajām fiziskajām vienībām, kas atrodas jūsu veikalā vai noliktavas plauktos, vislabākais laiks to darīt ir pēc tam, kad kanāla darbības ir uz dienu pārtrauktas un visas darbības ir pareizi sinhronizētas starp Headquarters un kanāliem.

## <a name="channel-side-inventory-calculation"></a>Kanāla puses krājumu aprēķins

Kanāla puses krājumu aprēķināšana ir mehānisms, kas par bāzlīniju izmanto pēdējos zināmos kanāla krājumu datus programmā Commerce Headquarters un pēc tam faktorus papildu krājumu izmaiņu veikšanā kanāla pusē, kas nav iekļautas šajā bāzlīnijā, lai aprēķinātu gandrīz reāllaika novērtēto rīcībā esošo krājumu. 

Pašlaik kanāla puses krājumu aprēķina loģikā tiek apsvērtas šādas krājumu izmaiņas:

- Krājumi, kas pārdoti, izmantojot kases pasūtījumus veikalā
- Krājumi, kas pārdoti, izmantojot debitoru pasūtījumus veikalā vai tiešsaistes kanālā
- Krājums, kas atgriezts veikalā
- Izpildītie krājumi (izdošanas, pakas, nosūtīšanas) no veikala noliktavas

Lai lietotu kanāla puses krājumu aprēķinu, ir jāiespējo līdzeklis **Optimizētie preču pieejamības aprēķini**.

Ja jūsu Commerce vides laidiens ir **10.0.8 līdz 10.0.11.**, izpildiet tālāk noteiktās darbības.

1. Commerce galvenajā pārvaldē dodieties uz **Retail un Commerce** \> **Commerce kopīgotie parametri**.
1. Cilnē **Krājums**, laukā **Preču pieejamības uzdevums** atlasiet **Lietot optimizētu preču pieejamības uzdevuma procesu**.

Ja jūsu Commerce vides laidiens ir **10.0.12. vai jaunāks**, izpildiet tālāk noteiktās darbības.

1. Commerce galvenajā pārvaldē dodieties uz **Darbvietas \> Līdzekļu pārvaldība** un iespējojiet **Optimizētās preču pieejamības aprēķinu** līdzekli.
1. Ja jūsu tiešsaistes un veikalu kanāli izmanto vienas un tās pašas izpildes noliktavas, ir jāiespējo arī līdzeklis **Pastiprinātā e-komercijas kanāla puses krājuma aprēķina loģika**. Tādējādi kanāla puses aprēķina loģikā tiks iekļautas negrāmatotās transakcijas, kuras ir izveidotas veikala kanālā. (Šīs transakcijas var būt pārdošanas skaidrā naudā bez piegādes transakcijas, klientu pasūtījumi un atgriešana.)
1. Palaidiet **1070** (**Kanāla konfigurācija**) darbu.

Ja jūsu Commerce vide tika atjaunināta no laidiena, kas ir vecāks par Commerce 10.0.8. versiju, pēc līdzekļa **Optimizētās preču pieejamības aprēķini** iespējošanas ir jāpalaiž arī **Commerce plānotāja inicializēšana**, lai šis līdzeklis stātos spēkā. Lai palaistu inicializāciju, dodieties uz **Retail un Commerce** \>**Galvenās pārvaldes iestatījumi** \>**Commerce plānotājs**.

Lai izmantotu kanāla puses krājumu aprēķinu, kā priekšnosacījums no Headquarters izveidotais krājumu datu periodiskais momentuzņēmums, kas izveidots ar darbu **Preču pieejamība**, ir jāsūta uz kanāla datu bāzēm. Momentuzņēmums attēlo informāciju, kas ir Headquarters rīcībā attiecībā uz krājumu pieejamību noteiktai preču vai preču variantu kombinācijai un noliktavai. Tajā ir iekļautas tikai tās krājumu darbības, kas tika apstrādātas un grāmatotas programmā Headquarters laikā, kad momentuzņēmums tika izveidots, un tas varētu nebūt 100 procenti precīzs reāllaikā sakarā ar konstanto pārdošanas apstrādi, kas notiek sadalītos serveros.

- Ja krājums tika pārdots precei veikalā, izmantojot naudas un pārvadāšanas vai asinhrono klientu pasūtījumu pārdošanu POS programmā, Headquarters nekavējoties netiek iekļauta informācija par saistīto krājumu izdošanas transakciju pārdošanai. Programmā Headquarters būs informācija par krājumiem, kas tiek pārdoti šāda veida veikala pārdošanas darbībām tikai pēc tam, kad P-darbs augšupielādē saistīto transakciju no veikala kanāla datu bāzes programmā Headquarters un saistītais pārdošanas pasūtījumi tiek izveidoti ar izrakstu iegrāmatošanu vai pakāpeniskas plūsmas iegrāmatošanas procesiem. Pasūtījumu izveides process programmā Headquarters izveido saistītās krājumu transakcijas. 
- E-komercijas kanāla pasūtījumiem Headquarters ir informācija par krājumu transakcijām tikai pēc tam, kad darbības tiek nosūtītas uz Headquarters caur P-darbu un ir pabeigts pasūtījuma sinhronizācijas process.

Lai uzņemtu krājumu momentuzņēmumu programmā Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Retail un Commerce \> Retail un Commerce IT \> Preces un krājumi \> Preču pieejamība**.
1. Atlasiet **Labi**, lai palaistu darbu **Preču pieejamība**. Varat arī ieplānot šo darbu, lai to palaistu partijā.

Kad darbs **Preču pieejamība** ir pabeigts, notvertie dati ir jāpārceļ uz kanāla datu bāzēm, lai jaunāko Headquarters krājumu momentuzņēmumu varētu iekļaut novērtēto rīcībā esošo krājumu kanāla puses aprēķinā.

Lai sinhronizētu momentuzņēmumu datus no Headquarters jūsu kanāla datu bāzēs, sekojiet šīm darbībām.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Palaidiet darbu **1130** (**Preču pieejamība**) darbu, lai sinhronizētu momentuzņēmuma datus, ko **Preču pieejamības** darbs, kas izveidots no Headquarters, ar jūsu kanāla datu bāzēm.

## <a name="inventory-availability-apis-for-e-commerce"></a>Krājumu pieejamības API interfeisi e-komercijai

Commerce nodrošina šādus API e-komercijas scenārijiem, lai vaicātu preces krājumu pieejamību:

- **GetEstimatedAvailability** - Izmantojiet šo API, lai tiešsaistes kanāla noliktavā vai noliktavās, kas ir saistītas ar tiešsaistes kanāla izpildes grupu, veiktu produkta vai produkta varianta krājumu vaicājumu.
- **GetEstimatedProductWarehouseAvailability** — Izmantojiet šo API, lai pieprasītu krājumu produktam vai produkta variantam no konkrētas noliktavas.

> [!NOTE]
> Šie API aizvieto API **GetProductAvailabilities** un **GetAvailableInventoryNearby** programmas Commerce izlaiduma 10.0.7 versijā un vecākās versijās.

Abi API iekšēji izmanto kanāla puses aprēķina loģiku un atgriež pieprasītās preces un noliktavas novērtēto **fizisko pieejamo** daudzumu, **kopējo pieejamo** daudzumu, **mērvienību (UOM)** un **krājumu līmeni**. Ja vēlaties, atgrieztās vērtības var tikt rādītas e-komercijas vietnē, vai tās var izmantot, lai aktivizētu citu biznesa loģiku jūsu e-komercijas vietnē. Piemēram, var novērst preču iegādi ar krājumu līmeni "ārpus krājumiem".

Lai gan citi API, kas ir pieejami Commerce, var tieši doties uz Headquarters, lai iznestu rīcībā esošos preču daudzumus, mēs neiesakām tos izmantot e-komercijas vidē iespējamo veiktspējas problēmu un ietekmes dēļ, ko šie Biežie pieprasījumi var radīt jūsu Headquarters serveriem. Turklāt ar kanāla puses aprēķinu divas augstāk minētās API var nodrošināt precīzāku aprēķinu par preces pieejamību, ņemot vērā kanālos izveidotās transakcijas, kuras vēl nav zināmas galvenajai pārvaldei.

Lai definētu, kā atgriezt preču daudzumu API izvadē, sekojiet šiem darbībām.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Tirdzniecības parametri**.
1. Atlasiet cilni **Krājumi** un pēc tam kopsavilkuma cilnē **Krājumu pieejamības API e-Komercijai** konfigurējiet iestatījuma **Daudzums API izvadē** vērtību.
1. Palaidiet **1070** (**Kanāla konfigurācija**) darbu, lai sinhronizētu pēdējos iestatījumus kanālos.

Iestatījums **Daudzums API izvadē** nodrošina trīs opcijas:

- **Atgrieztā krājuma daudzums** — Fiziski pieejamais un kopējais pieprasītās preces daudzums, kas atgriezts API izvadē.
- **Atgrieztā krājuma daudzuma noņemšanas krājuma buferis** — Daudzums, ko atgriezusi API izvade, tiek noregulēts, noņemot krājuma bufera vērtību. Papildinformāciju par krājumu buferi skatiet sadaļā [Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md).
- **Nav atgrieztā krājuma daudzuma** — API izvadē tiek atgriezta tikai krājuma atslēga. Papildinformāciju par krājumu līmeņiem skatiet sadaļā [Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md).

Varat izmantot `QuantityUnitTypeValue` API parametru, lai norādītu vienības veidu, kādā vēlaties, lai API atgriež daudzumu. Šis parametrs atbalsta opcijas **krājumu vienība** (noklusējuma), **pirkšanas vienība** un **pārdošanas vienība**. Atgrieztais daudzums tiek noapaļots līdz atbilstošas mērvienības (unit of measure - UOM) definētajai precizitātei programmā Headquarters.

API **GetEstimatedAvailability** piedāvā šādus ievades parametrus, lai atbalstītu dažādus vaicājuma scenārijus:

- `DefaultWarehouseOnly` — Izmantojiet šo parametru, lai izvaicātu krājumu produktam tiešsaistes kanāla noklusējuma noliktavā. 
- `FilterByChannelFulfillmentGroup` un `SearchArea` — Lietojiet šos divus parametrus, lai izvaicātu krājumu precei no visām izdošanas vietām konkrētā meklēšanas apgabalā, pamatojoties `longitude`, `latitude` un `radius`. 
- `FilterByChannelFulfillmentGroup` un `DeliveryModeTypeFilterValue` — Lietojiet šos divus parametrus, lai izvaicātu krājumu precei no konkrētām noliktavām, kuras ir saistītas ar tiešsaistes kanāla izpildes grupu un kas ir konfigurētas noteiktu piegādes režīmu atbalstam. Parametrs `DeliveryModeTypeFilterValue` atbalsta **visas** (noklusētās), **nosūtīšanas** un **savākšanas** opcijas. Piemēram, scenārijā, kad tiešsaistes pasūtījumu var izpildīt no vairākām nosūtīšanas noliktavām, varat izmantot šos divus parametrus, lai vaicātu par preces krājumu pieejamību visās šajās nosūtīšanas noliktavās. Šajā gadījumā API atgriež preces rīcībā esošo daudzumu un krājumu līmeni katrā nosūtīšanas noliktavā, kā arī apkopoto daudzumu un apkopoto krājumu līmeni no visām nosūtīšanas noliktavām vaicājumu tvērumā.
 
Commerce pirkšanas kastea, veikala atlasītāja, vēlmju saraksta, groza un groza ikonas moduļi patērē API un iepriekš minētos parametrus, lai parādītu krājumu līmeņa ziņojumus e-komercijas vietnē. Commerce vietņu veidotājs nodrošina dažādus krājumu iestatījumus, lai kontrolētu tirdzniecību un pirkšanu. Papildinformāciju skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>POS krājumu pārlūkošana ar kanāla puses aprēķinu

Commerce izlaidumā 10.0.9 un vecākās darbība **Krājumu informācijas iegūšana** POS lietoja reāllaika pakalpojuma izsaukumu uz Headquarters, lai iegūtu informāciju par atlasītā produkta krājumu gan lietotāja pašreizējam veikalam, gan visiem citiem veikaliem, kas ir konfigurēti izpildes grupai kā daļa no kanāla konfigurācijas veikalam. Commerce versijā 10.0.10 un jaunākai versijai varat izslēgt reāllaika pakalpojuma izsaukumus programmā Headquarters un tā vietā izmantot kanāla puses aprēķinu Commerce serverī, lai noteiktu rīcībā esošos krājumus, kas ir fiziski pieejami veikalam un visām citām atrašanās vietām, kas ir noteiktas izpildes grupā. Šī kanāla aprēķinātā krājumu konfigurācija ir noderīga arī vietās, kur interneta savienojums nav uzticams, jo jums nav jābūt tiešsaistē, lai iegūtu krājumu uzmeklēšanas rezultātus no Headquarters.

Kad kanāla puses aprēķins ir pareizi konfigurēts un pārvaldīts, tas var nodrošināt uzticamāku pašreizējo veikala krājumu aplēsi, jo tas izmanto transakciju datus, kas ir Commerce Channel datu bāzē, bet kuriem Headquarters varētu vēl nebūt informācijas. Piemēram, ja izmantojat esošo reāllaika pakalpojumu izsaukumu krājumu pārlūkošanai POS, Headquarters, iespējams, vēl nebūs informācijas par pārdošanu skaidrā naudā bez piegādes, kas tikko notikusi saistībā ar preci. Tāpēc rīcībā esošo krājumu vērtība, ko Headquarters atgriež šai precei, iespējams, pārsniedz veikala faktisko rīcībā esošo krājumu daudzumu par vienu vienību. Tomēr, ja izmantojat kanāla puses aprēķinu, pārdošanu skaidrā naudā bez piegādes var iekļaut aprēķinā, un tā tiek atskaitīta no parādītās rīcībā esošās vērtības. Lai gan vērtības, kas gan kanāla puses aprēķinā, gan reāllaika pakalpojuma izsaukumā sniedz tikai aprēķinus par rīcībā esošiem krājumiem, vērtība, ko sniedz kanāla puses aprēķins, ir daudz ticamāka pašreizējam veikalam.

Lai konfigurētu POS operāciju **Krājumu uzmeklēšana** Commerce Headquarters, lai izmantotu kanāla puses aprēķina loģiku un izslēgtu reāllaika pakalpojuma izsaukumu, vispirms aktivizējiet līdzekli **Optimizētās preču pieejamības aprēķināšana**, izmantojot darbvietu **Līdzekļu pārvaldība** programmā Commerce Headquarters un pēc tam izpildiet šīs darbības.

1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**.
1. Atlasiet funkcionalitātes profilu.
1. Kopsavilkuma cilnes **Funkcijas** sadaļā **Krājuma pieejamības aprēķins** mainiet lauka **Krājuma pieejamības aprēķina režīms** no **Reāllaika pakalpojums** uz **Kanāls**. Pēc noklusējuma visi funkcionalitātes profili izmanto reāllaika pakalpojumu izsaukumus. Šī lauka vērtība ir jāmaina, ja vēlaties izmantot kanāla puses aprēķina loģiku. Visus mazumtirdzniecības veikalus, kas ir saistīti ar izvēlēto funkcionalitātes profilu, ietekmēs šīs izmaiņas.

Pēc tam ir jāsinhronizē izmaiņas kanālos ar sadales grafika procesu programmā Headquarters, veicot šādas darbības:

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Palaidiet **1070** (**Kanāla konfigurācija**) darbu.

Pēc tam, kad konfigurācija ir pabeigta, informācija, kas tiek sniegta par fiziski pieejamiem krājumiem, vairs neizmanto reāllaika pakalpojuma zvanu, kad lietotājs POS lietojumprogrammā izmanto **krājumu uzmeklēšanas** operāciju (standarta un matricas skatījumi). Tā vietā dati par fiziski pieejamiem krājumiem pašreizējam veikalam un visi veikali izpildes grupā tiek aprēķināti, pamatojoties uz pēdējo zināmo momentuzņēmumu, kas tika piegādāts kanāla datu bāzei no Commerce Headquarters. Momentuzņēmuma vērtību tālāk rafinētu kanāla puses aprēķins, lai koriģētu fiziski pieejamo vērtību, pamatojoties uz papildu pārdošanas vai atgriešanas transakcijām, kas ir izveidotas atlasītajam produktam kanāla datu bāzē, kas netika iekļauta pēdējā sinhronizēts momentuzņēmums no 1130 darba. Ja kanāla datu bāzē nav ietverti darbības dati kādai no noliktavām vai veikaliem izpildes grupā, tas nesatur papildu darbības, kuras var iekļaut vērtības pārrēķinā. Tāpēc vislabākā rīcībā esošo krājumu aplēse, kas var tikt rādīta šīm noliktavām vai veikaliem, ir dati no pēdējā zināmā Commerce Headquarters momentuzņēmuma.

POS ekrāni **Pasūtījuma izpilde** piesaista arī kanāla puses aprēķinu, lai parādītu rīcībā esošos krājumus vienumiem, kad ir atlasīta pasūtījuma izpildes rinda, un lietotājs skata paneli **Detalizēta informācija** par atlasītā vienuma rīcībā esošajiem krājumiem.

## <a name="optimize-your-inventory-data"></a>Optimizējiet krājumu datus

Lai nodrošinātu labāko iespējamo krājumu aplēsi, ir svarīgi, lai tiktu izmantoti šādi Commerce pakešuzdevumi un tie tiktu bieži izpildīti:

- **P-darbs** – P-darbs tiek atrasts lapā **Sadales grafiki**, un tas ir jāizpilda bieži. Šis darbs apvieno e-komercijas pasūtījumus, asinhronos debitoru pasūtījumus, kas izveidoti POS, un pārdošanas skaidrā naudā bez piegādes pasūtījumus, ko POS izveidoja no kanāla datu bāzēm programmā Commerce Headquarters, lai tos varētu apstrādāt tālāk. Līdz brīdim, kad šie dati tiek sinhronizēti no kanāla uz Commerce Headquarters, Commerce Headquarters nav informācijas par krājumu korekcijām precēm noliktavās, kas rodas no šīm transakcijām.
- **Sinhronizēt pasūtījumus** — šis darbs apstrādā neapstrādātos transakciju datus programmā Commerce Headquarters, kurus P-darbs sniedz un pārvērš e-komerciju un asinhronu debitoru pasūtījumu transakcijas pārdošanas pasūtījumos programmā Commerce Headquarters. Kamēr šis darbs netiek apstrādāts un pārdošanas pasūtījumi nav izveidoti, transakcijas darbības netiek veidotas. Tāpēc rīcībā esošie krājumi programmā Commerce Headquarters neņems vērā transakcijas.
- **Aprēķināt transakciju izrakstus paketē** – pārdošanas darījumiem skaidrā naudā bez piegādes, kas ir izveidoti veikalā, pakāpeniskās padeves grāmatošanas procesā tiek nodrošināts, ka ar pārdošanu saistītie krājumi tiek atjaunināti efektīvi. Lai iegūtu visefektīvāko krājumu transakciju pārdošanas skaidrā naudā bez piegādes darījumu transakcijām, pārliecinieties, ka konfigurējat sistēmu, lai izmantotu [pakāpeniskās padeves grāmatošanu](./trickle-feed.md).
- **Grāmatot transakciju paziņojumus partijā** — šis darbs ir nepieciešams arī pakāpeniskās padeves grāmatošanai. Tas seko darbam **Aprēķināt transakciju paziņojumus partijā**. Šis darbs sistemātiski veic aprēķināto paziņojumu grāmatošanu, lai pārdošanas pasūtījumi pārdošanas pasūtījumiem skaidrā naudā bez piegādes tiktu izveidoti programmā Commerce Headquarters un Commerce Headquarters precīzāk atainotu jūsu veikala krājumus.
- **Preču pieejamība** — šis darbs izveido krājumu momentuzņēmumu no Commerce Headquarters.
- **1130 (Preču pieejamība)** - Šis darbs ir atrodams lapā **Sadales grafiki**, un tas ir jāizpilda uzreiz pēc darba **Preču pieejamība**. Šis darbs transportē krājumu momentuzņēmuma datus no Commerce Headquarters uz kanāla datu bāzēm.

> [!NOTE]
> - Ir ieteicams palaist darbus **Produktu pieejamība** un **1130** stundas laikā, lai plānotu P-darbu, sinhronizētu pasūtījumus un veiktu vienādas vai augstākas frekvences ar pastu saistītus darbus.
> - Veiktspējas apsvērumu dēļ, kad kanāla puses krājumu pieejamības aprēķini tiek izmantoti, lai veiktu krājumu pieejamības pieprasījumu, izmantojot e-komercijas API vai POS kanāla puses krājumu loģiku, aprēķins izmanto kešatmiņu, lai noteiktu, vai ir pagājis pietiekami daudz laika, lai attaisnotu aprēķina loģikas atkārtotu palaišanu. Noklusējuma kešdarbe ir iestatīta uz 60 sekundēm. Piemēram, jūs ieslēdzāt sava veikala kanāla puses aprēķinu un apskatījāt rīcībā esošos krājumus, kas paredzēti precei lapā **Krājumu uzmeklēšana**. Ja pēc tam tiek pārdota viena preces vienība, **Krājumu uzmeklēšanas** lapa nerāda samazinātos krājumus, līdz kešatmiņa nav notīrīta. Pēc tam, kad lietotāji grāmato darījumus POS, tiem ir jāgaida 60 sekundes, pirms tie pārbauda, vai rīcībā esošie krājumi ir samazināti.

Ja jūsu biznesa scenārijs prasa mazāku kešatmiņas laiku, sazinieties ar savu preču atbalsta pārstāvi, lai saņemtu palīdzību.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
