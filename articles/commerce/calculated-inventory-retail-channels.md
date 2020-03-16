---
title: Aprēķināt krājumu pieejamību mazumtirdzniecības kanāliem
description: Šajā tēmā ir aprakstītas opcijas, kas pieejamas, lai parādītu rīcībā esošos krājumus veikalam un tiešsaistes kanāliem.
author: hhainesms
manager: annbe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 8bef8edb46a1942d3efc325e2c437a138ad44839
ms.sourcegitcommit: e1a55b4dc43abedf523c33ba9a8abe7b073f2ec6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2020
ms.locfileid: "3083022"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Aprēķināt krājumu pieejamību mazumtirdzniecības kanāliem

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā uzņēmums var izmantot Microsoft Dynamics 365 Commerce, lai skatītu aplēsto rīcībā esošo pieejamību precēm tiešsaistes un veikala kanālos.

## <a name="accuracy-of-calculation"></a>Aprēķinu precizitāte

Commerce izmanto vairākus serverus un datu bāzes, lai nodrošinātu mērogojamību un veiktspēju. Tāpēc ir svarīgi, lai jūs saprastu, ka pieejamās krājumu vērtības, kas tiek nodrošinātas, izmantojot pārdošanas punktu (POS) programmu, e-komercijas krājumu pieejamības programmas programmēšanas interfeisu (API) un rīcībā esošo krājumu lapas programmā Commerce Headquarters, var nebūt simtprocentīgi precīzas reāllaikā. Ja transakcijas, kas ir izveidotas precēm tiešsaistes vai veikala kanālā, vēl nav sinhronizētas ar Commerce Headquarters serveri un datu bāzi, tad rīcībā esošo krājumu lapas programmā Commerce Headquarters var neparādīt precīzu reāllaika krājumu vērtību šīm precēm. Pretējā gadījumā, ja jūs konfigurējāt savu uzņēmumu tā, lai lietotāji programmā Commerce Headquarters vai citās integrētās programmās var pārdot, saņemt, atgriezt, vai kā citādi pielāgot krājumus no veikala vai tiešsaistes noliktavas, POS vai tiešsaistes kanālam var nebūt visas informācijas, kas nepieciešama, lai parādītu precīzu reālā laikā rīcībā esošo krājumu vērtību.

Šajā tēmā skaidroti datu sinhronizēšanas procesi, ko var veikt bieži, lai mazinātu datu latentumu starp programmām vai kanāliem. Tomēr ir svarīgi, lai jūs saprastu, ka visi rīcībā esošie pieejamības dati, kas tiek sniegti darbības dienā, tiek uzskatīti par aptuvenu vērtību. Tāpēc, ja mēģināt salīdzināt rīcībā esošo krājumu informāciju, ko nodrošina programma, ar faktiskajiem fiziskajiem krājumiem plauktos, vai mēģināt salīdzināt rīcībā esošās vērtības, kas tiek rādītas POS, ar rīcībā esošajiem datiem, kas atrodami vienai un tai pašai noliktavai programmā Commerce Headquarters, vērtības var atšķirties. Šī atšķirība darbības dienā ir sagaidāma, un to nevajadzētu uzskatīt par problēmu. Ja vēlaties veikt datu auditu un pārliecināties, ka vērtības, kas tiek sniegtas krājumu pieejamībai API un Commerce Headquarters, atbilst faktiskajām fiziskajām vienībām, kas atrodas jūsu veikalā vai noliktavas plauktos, vislabākais laiks to darīt ir pēc tam, kad kanāla darbības ir uz dienu pārtrauktas un visas darbības ir pareizi sinhronizētas starp Commerce Headquarters un kanālu.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>E-commerce krājumu pieejamības pieprasījumiem izmantojiet krājumu uzmeklēšanas API

Varat izmantot šādu API, lai parādītu krājuma pieejamību produktam, kad jūsu debitori tiek iepirkti e-komercijas vietnē.

- **GetEstimatedAvailability** — Izmantojiet šo API, lai iegūtu krājumu pieejamību vienumam e-komercijas kanāla noliktavā vai visās noliktavās, kas ir saistītas ar e-komercijas kanāla izpildes grupas konfigurāciju. Šo API var izmantot arī noliktavām noteiktā meklēšanas zonā vai rādiusā, pamatojoties uz garuma un platuma datiem.
- **ProductWarehouseInventoryAvailabilities** — Izmantojiet šo API, lai pieprasītu krājumu vienumam no konkrētas noliktavas. Piemēram, varat to izmantot, lai rādītu krājumu pieejamību scenārijos, kas ietver pasūtījuma savākšanu.

> [!NOTE]
> Šie API aizvieto API **GetProductAvailabilities** un **GetAvailableInventoryNearby** programmas Dynamics 365 Retail 10.0.7 versijā un vecākās versijās.

Abi API iegūst datus no Commerce Server un nodrošina rīcībā esošo krājumu aplēsi konkrētai preces vai preces varianta kombinācijai un noliktavai. Lai gan citi API, kas ir pieejami Commerce Server, var tieši doties uz Commerce Headquarters, lai iznestu rīcībā esošos preču daudzumus, mēs neiesakām tos izmantot e-komercijas vidē iespējamo veiktspējas problēmu un saistītās ietekmes dēļ, ko šie Biežie pieprasījumi var radīt jūsu Commerce Headquarters serveriem. Turklāt, ja rīcībā esošie krājumi tiek aprēķināti, izmantojot Commerce Server, aprēķinos ir lielāka iespējamība iekļaut krājumus, kas tika pārdoti pēdējos e-komercijas darījumos, kas vēl nav sinhronizēti ar Commerce Headquarters. Lai gan Commerce Headquarters, iespējams, nav informācijas par šīm transakcijām, Commerce Server un kanāla datu bāzei ir dati. Tāpēc dati tiks iegūti, un tie var palīdz nodrošināt precīzāku produkta pieejamo krājumu aplēsi.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Sākt darbu ar e-komercijas aprēķināto krājumu pieejamību

Pirms izmantojat divus iepriekšminētos API, ir jāveic parametra maiņa programmā Commerce Headquarters, lai nodrošinātu, ka momentuzņēmums krājumu vērtībām, ko Commerce Headquarters aprēķina, izmantojot **Preču pieejamības** darbu, tiek ievadīts pareizajās tabulās.

Lai iestatītu parametru, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**.
1. Cilnes **Krājumi** sadaļā **Preču pieejamības darbs** atlasiet **Izmantot optimizēšanas procesu produktu pieejamības darbam**. Šis iestatījums nodrošina, ka optimālais funkciju komplekts tiek izmantots, lai aprēķinātu kanāla rīcībā esošos krājumus, izmantojot Commerce Server.

Pirms API var aprēķināt vislabāko krājumu pieejamības aplēsi vienumam, ir jāapstrādā periodisks krājumu pieejamības momentuzņēmums no Commerce Headquarters un tas jānosūta uz kanāla datu bāzi, ko izmanto e-komercijas pakalpojumu mēroga vienība Momentuzņēmums attēlo informāciju, kas ir Commerce Headquarters rīcībā attiecībā uz krājumu pieejamību noteiktai preču vai preču variantu kombinācijai un noliktavai. Tas var ietvert krājumu korekcijas vai kustības, ko radījusi krājumu ieejas plūsma, vai kravas vai citi procesi, kas tiek veikti Commerce Headquarters un par kuriem e-komercijas kanālam ir informācija tikai sinhronizācijas procesa dēļ.

Datu bāzes momentuzņēmums, ko izveido darbs **Preču pieejamība**, aprēķina tikai tās krājumu darbības, kas tika apstrādātas un grāmatotas programmā Commerce Headquarters laikā, kad tika veikts momentuzņēmums. Ja krājums tika pārdots precei veikala noliktavā, izmantojot naudas un pārvadāšanas vai asinhrono klientu pasūtījumu pārdošanu POS programmā, Commerce Headquarters nekavējoties netiek iekļauta informācija par saistīto krājumu izdošanas transakciju pārdošanai. Tajā būs informācija par krājumiem, kas tiek pārdoti šāda veida veikala pārdošanas darbībām tikai pēc tam, kad P-darbs augšupielādē saistīto transakciju no veikala kanāla datu bāzes programmā Commerce Headquarters un saistītais pārdošanas pasūtījums tiek izveidots ar izrakstu iegrāmatošanu vai pakāpeniskas plūsmas iegrāmatošanas procesiem. Pasūtījuma izveides process programmā Commerce Headquarters izveido saistītās krājumu transakcijas E-komercijas kanāla pasūtījumiem Commerce Headquarters ir informācija par krājumu transakcijām tikai pēc tam, kad darbības tiek nosūtītas uz Commerce Headquarters caur P-darbu un ir pabeigts pasūtījuma sinhronizācijas process. Tāpēc ir svarīgi, lai jūs saprastu, ka krājumu momentuzņēmuma vērtība, kas ir norādīta darbā **Preces pieejamība**, var nebūt simtprocentīgi precīza reālajā laikā, nepārtrauktas pārdošanas apstrādes dēļ, kas notiek starp izplatītajiem serveriem.

Lai uzņemtu krājumu momentuzņēmumu programmā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Retail un Commerce \>Retail un Commerce IT \>Preces un krājumi \>Preču pieejamība**.
1. Atlasiet **Labi**, lai palaistu darbu **Preču pieejamība**. Varat arī ieplānot šo darbu, lai tas tiktu palaists partijā.

Kad darbs **Preču pieejamība**ir pabeigts, notvertie dati ir jāpārceļ uz e-komercijas kanāla datu bāzēm, lai jaunāko Commerce Headquarters krājumu momentuzņēmumu varētu iekļaut novērtēto rīcībā esošo krājumu aprēķinā.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Palaidiet darbu **1130** (**Preču pieejamība**) darbu, lai sinhronizētu momentuzņēmuma datus, ko **Preču pieejamības** darbs, kas izveidots no Commerce Headquarters, ar jūsu kanāla datu bāzēm.

Kad ir pieprasīta krājumu pieejamība no **GetEstimatedAvailability** vai **ProductWarehouseInventoryAvailabilities** API, tiek palaists aprēķins, lai mēģinātu iegūt labāko iespējamo preces krājumu aplēsi. Aprēķina atsauces uz jebkuriem e-komercijas klientu pasūtījumiem, kas atrodas kanāla datu bāzē, bet nav ietverti Snapshot datos, ko ir norādījis 1130 darbs. Šī loģika tiek veikta, izsekojot pēdējo apstrādāto krājumu transakciju no Commerce Headquarters un salīdzinot to ar transakcijām kanāla datu bāzē. Tas sniedz bāzlīniju kanāla aprēķina loģikai, lai papildu krājumu kustības, kas tika notikušas debitora pasūtījuma pārdošanas darbībām e-komercijas kanāla datu bāzē, var iekļaut novērtētajā krājumu vērtībā, ko sniedz API.

Kanāla puses aprēķina loģika atgriež aprēķināto fiziski pieejamo vērtību un visu pieprasīto preču un noliktavu pieejamo vērtību. Ja vēlaties, vērtības var tikt rādītas e-komercijas vietnē, vai tās var izmantot, lai aktivizētu citu biznesa loģiku jūsu e-komercijas vietnē. Piemēram, jūs varat parādīt paziņojumu "nav krājumā", nevis faktisko rīcībā esošo daudzumu, kuru nodeva API.

Aprēķina loģika, kuru kanāla e-komercijas API izmanto, lai aplēstā krājumu vērtība varētu novērtēt krājumu, pamatojoties tikai uz to klientu pasūtījumiem, kas ir izveidoti kanāla datu bāzē, bet kas vēl nav sinhronizēti un grāmatoti Commerce Headquarters. Ja jūsu kanāla datu bāze satur arī transakciju datus, kas attiecas uz pārdošanu skaidrā naudā bez piegādes veikalam paredzētām noliktavām, šāda pārdošana netiek ņemta vērā kanāla puses e-komercijas aprēķināšanai šīm noliktavām.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Konfigurēt krājumu uzmeklēšanas darbību POS kanālā

Retail versijā 10.0.9 un vecākās darbība **Krājumu informācijas iegūšana** no POS lietoja reāllaika pakalpojuma izsaukumu uz Commerce Headquarters, lai iegūtu informāciju par atlasītā produkta krājumu gan lietotāja pašreizējam veikalam, gan visiem citiem veikaliem, kas ir konfigurēti izpildes grupai kā daļa no kanāla konfigurācijas veikalam. Commerce versijā 10.0.10 un jaunākās varat izslēgt reāllaika pakalpojuma izsaukumus uz Commerce Headquarters. Tā vietā, lai noteiktu rīcībā esošos krājumus, kas ir fiziski pieejami veikalā un citās vietās, kas definētas izpildes grupā, pakalpojumā Commerce Server var izmantot kanāla puses aprēķinu. Šī kanāla aprēķinātā krājumu konfigurācija ir noderīga arī vietās, kur interneta savienojums nav uzticams, jo jums nav jābūt tiešsaistē, lai iegūtu krājumu uzmeklēšanas rezultātus no Commerce Headquarters.

Kad kanāla puses aprēķins ir pareizi konfigurēts un pārvaldīts, tas var nodrošināt uzticamāku pašreizējo veikala krājumu aplēsi, jo tas izmanto transakciju datus, kas ir Commerce Channel datu bāzē, bet kuriem Commerce Headquarters varētu vēl nebūt informācijas. Piemēram, ja izmantojat esošo reāllaika pakalpojumu izsaukumu krājumu pārlūkošanai POS, Commerce Headquarters, iespējams, vēl nebūs informācijas par pārdošanu skaidrā naudā bez piegādes, kas tikko notikusi saistībā ar preci. Tāpēc rīcībā esošo krājumu vērtība, ko Commerce Headquarters atgriež šai precei, iespējams, pārsniedz veikala faktisko rīcībā esošo krājumu daudzumu par vienu vienību. Tomēr, ja izmantojat kanāla puses aprēķinu, pārdošanu skaidrā naudā bez piegādes var iekļaut aprēķinā, un tā tiek atskaitīta no parādītās rīcībā esošās vērtības. Lai gan vērtības, kas gan kanāla puses aprēķinā, gan reāllaika pakalpojuma izsaukumā sniedz tikai aprēķinus par rīcībā esošiem krājumiem, vērtība, ko sniedz kanāla puses aprēķins, ir daudz ticamāka pašreizējam veikalam.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Sākt darbu ar POS kanāla puses aprēķināto krājumu pieejamību

Lai izmantotu kanāla puses aprēķina loģiku un izslēgtu reāllaika pakalpojuma izsaukumus no POS lietojumprogrammas, vispirms jāveic divas parametru izmaiņas. Pēc tam ir jāsinhronizē izmaiņas kanālā, izmantojot sadales grafika procesu.

Lai iestatītu pirmo parametru, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**.
1. Cilnes **Krājumi** sadaļā **Preču pieejamības darbs** atlasiet **Izmantot optimizēšanas procesu produktu pieejamības darbam**. Šis iestatījums nodrošina, ka optimālais funkciju komplekts tiek izmantots, lai aprēķinātu kanāla rīcībā esošos krājumus, izmantojot Commerce Server.

Lai iestatītu otro parametru, veiciet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Retail un Commerce\> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**.
1. Atlasiet funkcionalitātes profilu.
1. Kopsavilkuma cilnes **Funkcijas** sadaļā **Krāj. pieejamības aprēķins** mainiet lauka **Krāj. pieejamības aprēķina režīms** no **Reāllaika pakalpojums** uz **Kanāls**. Pēc noklusējuma visi funkcionalitātes profili izmanto reāllaika pakalpojumu izsaukumus. Tāpēc šī lauka vērtība ir jāmaina, ja vēlaties izmantot kanāla puses aprēķina loģiku. Visus mazumtirdzniecības veikalus, kas ir saistīti ar izvēlēto funkcionalitātes profilu, ietekmēs šīs izmaiņas.

Lai atjauninātu serverus, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Palaidiet **1070** (**Kanāla konfigurācija**) darbu.

Pēc tam, kad konfigurācija ir pabeigta, informācija, kas tiek sniegta par fiziski pieejamiem krājumiem, vairs neizmanto reāllaika pakalpojuma zvanu, kad lietotājs POS lietojumprogrammā izmanto **krājumu uzmeklēšanas** operāciju (standarta un matricas skatījumi). Tā vietā dati par fiziski pieejamiem krājumiem pašreizējam veikalam un visi veikali izpildes grupā tiek aprēķināti, pamatojoties uz pēdējo zināmo momentuzņēmumu, kas tika piegādāts kanāla datu bāzei no Commerce Headquarters. Momentuzņēmuma vērtību tālāk rafinētu kanāla puses aprēķins, lai koriģētu fiziski pieejamo vērtību, pamatojoties uz papildu pārdošanas vai atgriešanas transakcijām, kas ir izveidotas atlasītajam produktam kanāla datu bāzē, kas netika iekļauta pēdējā sinhronizēts momentuzņēmums no 1130 darba. Ja kanāla datu bāzē nav ietverti darbības dati kādai no noliktavām vai veikaliem izpildes grupā, tas nesatur papildu darbības, kuras var iekļaut vērtības pārrēķinā. Tāpēc vislabākā rīcībā esošo krājumu aplēse, kas var tikt rādīta šīm noliktavām vai veikaliem, ir dati no pēdējā zināmā Commerce Headquarters momentuzņēmuma.

POS ekrāni **Pasūtījuma izpilde** piesaista arī kanāla puses aprēķinu, lai parādītu rīcībā esošos krājumus vienumiem, kad ir atlasīta pasūtījuma izpildes rinda, un lietotājs skata paneli **Detalizēta informācija** par atlasītā vienuma rīcībā esošajiem krājumiem.

## <a name="optimize-your-inventory-data"></a>Optimizējiet krājumu datus

Lai nodrošinātu labāko iespējamo krājumu aplēsi, ir svarīgi, lai tiktu izmantoti šādi Commerce pakešuzdevumi un tie tiktu bieži izpildīti:

- **P-darbs** – P-darbs tiek atrasts lapā **Sadales grafiki**, un tas ir jāizpilda bieži. Šis darbs apvieno e-komercijas pasūtījumus, asinhronos debitoru pasūtījumus, kas izveidoti POS, un pārdošanas skaidrā naudā bez piegādes pasūtījumus, ko POS izveidoja no kanāla datu bāzēm programmā Commerce Headquarters, lai tos varētu apstrādāt tālāk. Līdz brīdim, kad šie dati tiek sinhronizēti no kanāla uz Commerce Headquarters, Commerce Headquarters nav informācijas par krājumu korekcijām precēm noliktavās, kas rodas no šīm transakcijām.
- **Sinhronizēt pasūtījumus** — šis darbs apstrādā neapstrādātos transakciju datus programmā Commerce Headquarters, kurus P-darbs sniedz un pārvērš e-komerciju un asinhronu debitoru pasūtījumu transakcijas pārdošanas pasūtījumos programmā Commerce Headquarters. Kamēr šis darbs netiek apstrādāts un pārdošanas pasūtījumi nav izveidoti, transakcijas darbības netiek veidotas. Tāpēc rīcībā esošie krājumi programmā Commerce Headquarters neņems vērā transakcijas.
- **Aprēķināt transakciju izrakstus paketē** – pārdošanas darījumiem skaidrā naudā bez piegādes, kas ir izveidoti veikalā, pakāpeniskās padeves grāmatošanas procesā tiek nodrošināts, ka ar pārdošanu saistītie krājumi tiek atjaunināti efektīvi. Lai iegūtu visefektīvāko krājumu transakciju pārdošanas skaidrā naudā bez piegādes darījumu transakcijām, pārliecinieties, ka konfigurējat sistēmu, lai izmantotu [pakāpeniskās padeves grāmatošanu ](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Grāmatot transakciju paziņojumus partijā** — šis darbs ir nepieciešams arī pakāpeniskās padeves grāmatošanai. Tas seko darbam **Aprēķināt transakciju paziņojumus partijā**. Šis darbs sistemātiski veic aprēķināto paziņojumu grāmatošanu, lai pārdošanas pasūtījumi pārdošanas pasūtījumiem skaidrā naudā bez piegādes tiktu izveidoti programmā Commerce Headquarters un Commerce Headquarters precīzāk atainotu jūsu veikala krājumus.
- **Preču pieejamība** — šis darbs izveido krājumu momentuzņēmumu no Commerce Headquarters.
- **1130 (Preču pieejamība)** - Šis darbs ir atrodams lapā **Sadales grafiki**, un tas ir jāizpilda uzreiz pēc darba **Preču pieejamība**. Šis darbs transportē krājumu momentuzņēmuma datus no Commerce Headquarters uz kanāla datu bāzēm.

> [!NOTE]
> Veiktspējas apsvērumu dēļ, kad kanāla puses krājumu pieejamības aprēķini tiek izmantoti, lai veiktu krājumu pieejamības pieprasījumu, izmantojot e-komercijas API vai jauno POS kanāla puses krājumu loģiku, aprēķins izmanto kešatmiņu, lai noteiktu, vai ir pagājis pietiekami daudz laika, lai attaisnotu aprēķina loģikas atkārtotu palaišanu. Noklusējuma kešdarbe ir iestatīta uz 60 sekundēm. Piemēram, jūs ieslēdzāt sava veikala kanāla puses aprēķinu un apskatījāt rīcībā esošos krājumus, kas paredzēti precei lapā **Krājumu uzmeklēšana**. Ja pēc tam tiek pārdota viena preces vienība, **Krājumu uzmeklēšanas** lapa nerāda samazinātos krājumus, līdz kešatmiņa nav notīrīta. Pēc tam, kad lietotāji grāmato darījumus POS, tiem ir jāgaida 60 sekundes, pirms tie pārbauda, vai rīcībā esošie krājumi ir samazināti.

Ja jūsu biznesa scenārijs prasa mazāku kešatmiņas laiku, sazinieties ar savu preču atbalsta pārstāvi, lai saņemtu palīdzību.
