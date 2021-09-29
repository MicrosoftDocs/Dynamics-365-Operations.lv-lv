---
title: Līdzekļu pārvaldības pārskats
description: Šajā tēmā ir aprakstīts līdzeklis Līdzekļu pārvaldība un tā lietošanas iespējas.
author: Peakerbl
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 1318093d66cfc30a04815311cce332df010d4b69
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488182"
---
# <a name="feature-management-overview"></a>Līdzekļu pārvaldības pārskats

[!include [banner](../../includes/banner.md)]

Katrā laidienā tiek pievienoti un atjaunināti līdzekļi. Pieredze Līdzekļu pārvaldība nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu. Pēc tam varat izmantot darbvietu, lai skatītu līdzekļu dokumentāciju un iespējotu vai deaktivizētu līdzekļus.

## <a name="the-feature-management-workspace"></a>Darbvieta Līdzekļu pārvaldība

Varat atvērt darbvietu **Līdzekļu pārvaldība** darbvietu, atlasot attiecīgo elementu informācijas panelī. Tiks parādīta lapa ar līdzekļu sarakstu visiem laidieniem, ko atbalsta Līdzekļu pārvaldības pieredze. 

Līdzekļu sarakstā ir tālāk norādītā informācija:

- **Līdzekļa nosaukums** — pievienotā līdzekļa apraksts.
- **Statuss** — simbols norāda, vai līdzeklis ir ieslēgts (atzīme), nav ieslēgts (tukšs), tiek plānota tā ieslēgšana (pulkstenis) vai arī ir ieslēgts obligāti (piekaramā atslēga); ir jāpievērš uzmanība, pirms to ieslēdzat (brīdinājums), vai to nevar iespējot (X). Redzamais iestatījums tiek izmantots visām juridiskajām personām. Ņemiet vērā, ka pat tad, ja līdzeklis ir ieslēgts, to joprojām kontrolē drošība. Tāpēc šis līdzeklis būs pieejams tikai tiem lietotājiem, kuriem ir piekļuve tam, pamatojoties uz lietotāja drošības lomu. Tas būs pieejams arī tikai juridiskajās personās, kurām lietotājam ir piekļuve.
- **Iespējošanas datums** — datums, kad līdzeklis tika ieslēgts vai kad to ir plānots ieslēgt.
- **Līdzeklis pievienots** — datums, kad līdzeklis tika pievienots jūsu videi. Šis datums tiek ievadīts automātiski, kad mēneša laidiena cikla laikā tiek atjaunināta jūsu vide.
- **Līdzekļa stāvoklis** — pašreizējais funkcijas dzīves cikla stāvoklis: **Priekšskatījums**, **Nodots izpildei** (norādīts kā tukšs), **Pēc noklusējuma** un **Obligāts**. Tālāk šajā tēmā šie statusi ir smalkāk aprakstīti. 
- **Modulis** — modulis, ko ietekmē jaunais līdzeklis.

> [!NOTE]
> **Līdzekļu stāvokļa** kolonna ir iekļauta versijā 10.0.21.

Kad atlasāt līdzekli, detalizētas informācijas rūtī pa labi no līdzekļu saraksta tiek parādīta papildinformācija. Rūts augšā redzēsit līdzekļa nosaukumu, pievienošanas datumu, moduli, ko ietekmē šis līdzeklis, un saiti **Papildinformācija**. Atlasiet šo saiti, lai skatītu līdzekļa dokumentāciju. Ja dokumentācija nav pieejama, jūs tiekat novirzīts uz pagaidu lapu. Detalizētas informācijas rūtī ir ietverts arī lauks **Komentāri**, kur varat pievienot savus komentārus par šo līdzekli.

Arī darbvietā **Līdzekļu pārvaldība** ir vairākas cilnes, un katrā no tām tiek rādīts līdzekļu saraksts.

- **Jauns** — šajā cilnē tiek rādīti visi līdzekļi, kas ir pievienoti kopš pēdējās ikmēneša atjaunināšanas. Ja esat izlaidis kādu ikmēneša atjauninājumu, šajā cilnē tiek rādīti visi jaunie līdzekļi, kas ir pievienoti kopš pēdējās reizes, kad veicāt atjaunināšanu. Jaunākie līdzekļi tiek parādīti saraksta sākumā. Kopējais jauno līdzekļu skaits tiek rādīts arī lapas augšā esošajā elementā.
- **Nav iespējots** — šajā cilnē tiek rādīti visi līdzekļi, kas nav ieslēgti. Jaunākie līdzekļi tiek parādīti saraksta sākumā. Turklāt elementam, kas atrodas lapas augšpusē, ir redzams to jauno funkciju kopskaits, kas pašlaik ir izslēgtas.
- **Ieplānots** — šajā cilnē tiek rādīti visi līdzekļi, kurus ir plānots ieslēgt nākotnē. Saraksta augšā tiek rādīti līdzekļi, kuru plānotais datums ir visdrīzāk. Kopējais plānoto jauno līdzekļu skaits tiek rādīts arī lapas augšā esošajā elementā.
- **Visi** — šajā cilnē tiek rādīti visi līdzekļi. Jaunākie līdzekļi tiek parādīti saraksta sākumā.

## <a name="feature-states"></a>Līdzekļu stāvokļi
Funkcijas var pāriet starp vairākiem statusiem, sākot no funkcionalitātes pārvaldības ieviešanas līdz beidzot ar obligātu preces vadību. Šajā sadaļā aprakstīti derīgie funkciju statusi.

### <a name="preview-features-optional"></a>Priekšskatījuma līdzekļi (pēc izvēles)

Produktu grupas var izlemt sākotnēji sākt jaunu līdzekli kā priekšskatījuma līdzekli. Priekšskatījuma līdzekļi pēc noklusējuma nav aktivizēti, un tie ir izvēles līdzekļi. Piederīgā preču grupa atjauninās funkcijas, kas nodotas izpildei pēc tam, kad tās būs pabeigušas sekmīgu priekšskatījuma periodu.

> [!NOTE]
> Uz priekšskatījuma funkcijām attiecas specifiski priekšskatījuma [noteikumi un nosacījumi](https://go.microsoft.com/fwlink/?linkid=2105274). 

### <a name="released-features-optional"></a>Izpildei nodotās funkcijas (neobligāti)

Šo **Līdzekļu stāvokļa** kolonna ir tukša. Līdzekļi, kas sākotnēji ir pievienoti kā nodoti izpildei, pēc noklusējuma nav ieslēgti un to iespējošana nav obligāta. Līdzekļi, kas ir atjaunināti no priekšskatījuma, saglabās to iespējošanas statusu.

### <a name="on-by-default-features-optional"></a>Pēc noklusējuma līdzekļiem (neobligāti)

Līdzekļi, kas atjaunināti **Pēc noklusējuma** ir ieslēgti pēc noklusējuma, bet tos var deaktivizēt. Pēc tam, kad atspējotās funkcijas vismaz sešus mēnešus ir **Nodotas izpildei stāvoklī**, tām ir paredzams pāriet uz šo stāvokli nākamajā lielajā laidienā. Funkcijas, kas pāriet uz **Pēc noklusējuma** tiek prognozētas, lai tās tiktu tam nodotas sarakstā [Kas jauns](../whats-new-changed.md) par laidienu. Atjauninājumu uzsāka piederošo preču grupa.

> [!NOTE]
> Tā kā šīs funkcijas tiks aktivizētas automātiski, ir svarīgi noteikt, vai organizācija ir gatava izmantot šīs funkcijas vai arī nepieciešams vairāk laika. Ja nepieciešams vairāk laika, var būt nepieciešams uz laiku deaktivizēt šīs funkcijas. Ievērojiet, ka funkcijas pāreja uz **Pēc noklusējuma** parasti tiek veikta galvenajā laidienā, pirms līdzeklis ir paredzēts, lai kļūtu par **Obligātu**. Šajā brīdī jums nebūs opcijas atspējot šo līdzekli. 

### <a name="released-features-mandatory"></a>Izpildei nodotās funkcijas (obligātas)

**Nodots izpildei** ir pēdējais līdzekļu stāvoklis. Tas norāda, ka līdzekļi ir ieslēgti un tos nevar deaktivizēt, nesazinoties ar korporāciju Microsoft. Pēc diviem galvenajiem laidieniem izvēles funkcijas ir sagaidāmas kā obligātas. Kritiskās funkcijas izņēmuma gadījumā var tikt ieviestas kā obligātas.

## <a name="example-of-expected-feature-lifecycles"></a>Prognozēto līdzekļu dzīves cikla piemērs

Funkcijas, kuras var atspējot un kuras tika pievienotas kā izpildei nodotas un neobligātas pirms vai kā daļa no aprīļa versijas, visticamāk, pāries uz **Pēc noklusējuma** oktobra laidienā. Ar to tiek paredzēts, ka tie kļūs par **obligātiem** nākamā gada aprīlī.

Funkcijas, kuras var atspējot un kuras tika pievienotas kā izpildei nodotas un neobligātas pirms vai kā daļa no aprīļa versijas, visticamāk, pāries uz **Obligāām** nākamā gada aprīlī.

## <a name="enable-a-feature"></a>Līdzekļa iespējošana

Ja līdzeklis nav ieslēgts, detalizētas informācijas rūtī tiek rādīta poga **Iespējot tūlīt**. Varat izmantot šo pogu līdzekļa iespējošanai.

Dažus līdzekļus nevar atspējot pēc to iespējošanas. Ja līdzekli, kuru mēģināt ieslēgt, vairs nevar izslēgt, saņemsiet brīdinājumu. Šajā brīdī varat atlasīt **Atcelt**, lai atceltu darbību, un saglabāt līdzekli atspējotā statusā. Tomēr, ja atlasāt **Iespējot** un iespējojat līdzekli, nevarēsit to atspējot vēlāk.

Daži līdzekļi, pirms tos ieslēgsit, parādīs ziņojumu, kas sniedz papildu informāciju. Šie līdzekļi ir apzīmēti ar dzeltenu brīdinājuma simbolu. Jums vajadzētu rūpīgi izlasīt papildu informāciju, lai labāk saprastu, kas notiks, kad šis līdzeklis tiks iespējots. Tomēr joprojām varat atlasīt **Iespējot**, lai ieslēgtu šo funkciju.

Dažas funkcijas parādīs ziņojumu, ka funkciju nevar iespējot, kamēr nav veikta darbība. Šīs funkcijas ir apzīmētas ar sarkanu X simbolu. Pirms funkcija tiek iespējota, ir jāveic aprakstā minētās darbības. Piemēram, ja nevarat izmantot funkciju, līdz konfigurācijas atslēga tiek atspējota, vispirms atspējojiet konfigurācijas atslēgu un pēc tam atgriezieties Funkciju pārvaldībā, lai iespējotu funkciju.

Pēc līdzekļa iespējošanas detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šajā ziņojumā ir norādīts, ka līdzeklis tika ieslēgts, vai arī ir norādīts turpmāks datums, kad šo līdzekli ir plānots ieslēgt. Tas tiek parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli.

Līdzekļi, kuru ieslēgšana ir plānota nākotnē, ir redzami cilnē **Plānots**. Tie tiek ieslēgti ar pakešveida apstrādi norādītā datuma pusnaktī, pamatojoties uz sistēmas datuma norādīto laika zonu.

## <a name="reschedule-a-feature"></a>Līdzekļa pārplānošana

Ja līdzekli ir plānots ieslēgt nākotnē, detalizētas informācijas rūtī tiek rādīta poga **Plānot**. Varat izmantot šo pogu, lai mainītu vērtību **Iespējošanas datums** uz citu.

1. Atlasiet ieplānoto līdzekli, kuru vēlaties pārplānot, un pēc tam detalizētas informācijas rūtī atlasiet **Plānot**.
2. Parādītajā dialoglodziņā, laukā **Iespējošanas datums** norādiet jauno datumu, kad šis līdzeklis ir jāieslēdz.
3. Atlasiet opciju **Iespējot**, lai pārplānotu līdzekli, vai **Atspējot**, lai atceltu ieplānošanu.

## <a name="disable-a-feature"></a>Līdzekļa atspējošana

Ja līdzeklis jau ir iespējots, detalizētas informācijas rūtī tiek parādīta poga **Atspējot**. Varat izmantot šo pogu līdzekļa atspējošanai. Poga **Atspējot** nav pieejama, ja līdzekli nevar atspējot pēc tā iespējošanas. 

Pēc līdzekļa iespējošanas detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šis ziņojums norāda, ka līdzeklis vēl nav bijis ieslēgts. Tas tiek parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli. Līdzekļi, kas vēl nav bijuši ieslēgti, ir redzami cilnē **Nav iespējots**.

## <a name="features-that-must-be-enabled"></a>Līdzekļi, kam jābūt iespējotiem

Reizēm tiek piegādāts kritisks līdzeklis, kam ir jāieslēdzas automātiski, kad veicat atjaunināšanu. Šie līdzekļi tiks automātiski ieslēgti datumā, kas ir norādīts laukā **Iespējošanas datums**. Šiem līdzekļiem detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šajā ziņojumā tiek norādīts, ka līdzeklis ir iespējots, vai arī tiek norādīts līdzekļa iespējošanas datums nākotnē. Tas tiek parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli.

## <a name="enable-all-features"></a>Iespējot visus līdzekļus

Varat iespējot visus līdzekļus, atlasot pogu **Iespējot visu**. 

Atlasot opciju **Iespējot visu**, tiek parādīta opcija, kur jums ir jāsniedz šāda informācija:

- Visu to līdzekļu saraksts, kuriem nepieciešams apstiprinājums, lai tos varētu iespējot. Ja vēlaties iespējot līdzekļus sarakstā, atlasiet **Jā** pogai **Iespējot līdzekļus, kuriem nepieciešams apstiprinājums**.
- Tiks parādīts visu to līdzekļu saraksts, kurus nevar iespējot. Šie līdzekļi netiks iespējoti.

Visi līdzekļi, kurus var iespējot, tiks iespējoti. Ja līdzeklim nākotnē jau ir ieplānota iespējošana, grafiks nemainīsies. 

## <a name="enable-all-features-automatically"></a>Visu līdzekļu ieslēgšana automātiski

Taču, ja vēlaties automātiski ieslēgt visus jaunos līdzekļus, varat izmantot nolaižamo sarakstu zem darbvietas nosaukuma, lai mainītu to, kas notiek pēc jaunu līdzekļu pievienošanas.

- Atlasiet **Automātiski iespējot jaunus līdzekļus**, lai automātiski ieslēgtu visus jaunus līdzekļus, pievienojot tos jūsu videi.
- Atlasiet **Automātiski neiespējot jaunus līdzekļus**, lai pēc noklusējuma izslēgtu visus jaunus līdzekļus, pievienojot tos jūsu videi.

Ja iespējosit visus līdzekļus automātiski, tas iespējos visus līdzekļus, kas tiktu iespējoti, noklikšķinot uz pogas **Iespējot visu**. Tas neiespējos līdzekļus, kuriem ir nepieciešams apstiprinājums, vai līdzekļus, kurus nevar iespējot līdz brīdim, kad tiek veikta darbība.

## <a name="check-for-updates"></a>Pārbaudīt, vai nav atjauninājumu

Līdzekļi tiek pievienoti jūsu videi pēc katra atjauninājuma. Tomēr atjauninājumus var pārbaudīt manuāli, noklikšķinot uz pogas **Pārbaudīt, vai nav atjauninājumu**. Jebkurš līdzeklis, kas tika pievienots sistēmai pēc atjauninājuma, tiks pievienots līdzekļu sarakstam. Piemēram, ja pēc izlaišanas ir iespējots būvētais līdzeklis, varat pārbaudīt, vai nav atjauninājumu, un šis līdzeklis tiks pievienots sarakstam.

## <a name="assigning-roles"></a>Lomu piešķiršana

Darbvietu **Līdzekļu pārvaldība** var atvērt sistēmas administratori, kā arī lietotāji, kuriem ir piešķirta loma Līdzekļu pārvaldnieks vai Līdzekļu skatītājs. Abas šīs lomas tika izveidotas, lai atbalstītu funkcionalitāti Līdzekļu pārvaldība. Lietotāji ar līdzekļu pārvaldnieka lomu var ieslēgt vai izslēgt jebkuru līdzekli. Viņi līdzeklim var arī atjaunināt lauku **Komentāri**. Lietotāji ar līdzekļu skatītāja lomu var tikai skatīt darbvietu **Līdzekļu pārvaldība**. Tie nevar ieslēgt vai izslēgt līdzekļus.

Līdzekļu pārvaldnieka loma un līdzekļu skatītāja loma neignorē esošo drošību, kas ir lietotājam. Šīs lomas tikai kontrolē to, vai lietotājs līdzekļus var ieslēgt un izslēgt. Tās nenodrošina piekļuvi pašiem līdzekļiem.

## <a name="features-that-use-configuration-keys"></a>Līdzekļi, kas izmanto konfigurācijas atslēgas

Ja kāds līdzeklis izmanto konfigurācijas atslēgu, bet tā konfigurācijas atslēga nav ieslēgta, darbvieta **Līdzekļu pārvaldība** šo līdzekli nerāda pieejamo līdzekļu sarakstā. Pēc konfigurācijas atslēgas ieslēgšanas jums ir jāatjaunina līdzekļu saraksts, izmantojot izvēlnes vienumu **Pārbaudīt, vai nav atjauninājumu**. Pēc tam līdzeklis kļūst redzams līdzekļu sarakstā.

Ja izslēdzat šo konfigurācijas atslēgu, līdzeklis netiek noņemts no līdzekļu saraksta.

## <a name="data-entities"></a>Datu elementi

Datu elements ar nosaukumu **Līdzekļu pārvaldība** ļauj jums eksportēt iestatījumus “Līdzekļu pārvaldība” no vienas vides un pēc tam importēt tos citā vidē. Šis elements atjaunina tikai esošos līdzekļus. Biznesa loģika šajā elementā palīdz arī garantēt, ka pēc importēšanas tiek piemērotas tās pašas kārtulas, kuras tiek lietotas darbvietā **Līdzekļu pārvaldība**. Piemēram, jūs nevar pārrakstīt obligātu līdzekļa iestatījumu, importēšanas laikā noņemot datumu.

Nākamajos piemēros ir aprakstīts, kas notiek, kad datu importēšanai izmantojat elementu **Līdzekļu pārvaldība**.

- Ja lauka **Iespējots** vērtību maināt uz **Jā**, līdzeklis tiek ieslēgts un lauks **Iespējošanas datums** tiek iestatīts uz pašreizējo datumu.
- Ja lauka **Iespējots** vērtību maināt uz **Nē** vai lauku **EnableDate** atstājat tukšu, līdzeklis tiek izslēgts un lauks **Iespējošanas datums** tiek notīrīts. Jūs nevarat izslēgt obligātu līdzekli vai līdzekli, ko nevar izslēgt pēc tā ieslēgšanas.
- Ja lauka **EnableDate** vērtību maināt uz turpmāku datumu, līdzeklis tiek ieplānots attiecīgajam datumam.
- Ja lauka **Iespējots** vērtību maināt uz **Jā** un lauka **EnableDate** vērtību maināt uz turpmāku datumu, līdzeklis tiek ieplānots attiecīgajam datumam. 
- Ja lauka **Iespējots** vērtību maināt uz **Nē**, bet arī lauka **EnableDate** vērtību maināt uz turpmāku datumu, līdzeklis tiek ieplānots attiecīgajam datumam.
- Ja līdzeklis ir ieslēgts un jūs pievienojat lauku **EnableDate**, kas ir iestatīts uz turpmāku datumu, šis līdzeklis paliek ieslēgts. Lai šo līdzekli pārplānotu, jums lauka **Iespējots** vērtība ir jāmaina uz **Nē**.

## <a name="feature-management-and-flighting"></a>Funkciju pārvaldība un būvējumu izsniegšana

Līdzekļu pārvaldība ļauj jums kontrolēt līdzekļus, kas tiek piegādāti katrā laidienā. Būvējumu izsniegšana ļauj Microsoft darba grupām izlaist līdzekļus ierobežotam klientu skaitam, lai šos līdzekļus varētu testēt un pārbaudīt, neietekmējot visus klientus. Līdzekļu pārvaldība nekontrolē neviena līdzekļa būvējumu izsniegšanu.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Līdzekļu pārvaldības izmantošana, lai ieslēgtu ISV līdzekļus vai pielāgotus līdzekļus

Līdzekļu pārvaldība pašlaik nav pieejama līdzekļiem, ko piedāvā neatkarīgi programmatūras izstrādātāji (independent software vendor — ISV), un pielāgotajiem līdzekļiem. Taču Microsoft pievieno papildu funkcionalitāti, lai uzlabotu līdzekļu pārvaldību. Kad šie uzlabojumi būs pabeigti, Microsoft padarīs līdzekļu pārvaldību pieejamu visiem līdzekļiem un sniegs norādījumus par jūsu līdzekļu atjaunināšanu, lai varētu to izmantot.

## <a name="frequently-asked-questions-faq"></a>Bieži uzdotie jautājumi (BUJ)

### <a name="when-are-features-added-removed-or-changed"></a>Kad ir pievienoti, noņemti vai mainīti līdzekļi? 
Piederošo produktu grupas pievieno, noņem un maina funkcijas ar kodu izmaiņām. Lai saņemtu šīs izmaiņas, ir jāatjaunina vides.

### <a name="does-a-feature-become-mandatory-automatically"></a>Vai funkcija automātiski kļūst obligāta? 
Nē, līdzeklis automātiski nekļūst obligāts. Piederošo preču komandām ir jāveic koda izmaiņas.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Kāpēc nav noteikts “obligāti iespējotais datums”? 
Atjaunināšanas izlaišanas laiks ir mainīgs, vides atjaunināšanas laiks ir mainīgs, un klienti var izvēlēties izlaist dažus atjauninājumus. Tāpēc konkrētus datumus ir grūti noteikt. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Kur atrodas dokumentācija par līdzekļiem, kas ir obligāti? 
Šī dokumentācija tiek iegūta no katras Dynamics 365 programmas komandas. Bieži šie līdzekļi ir minēti [Klienta līdzekļu stāvokļu atjauninājumos](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) vai [Noņemtie vai novecojuši līdzekļi](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Vai ir produkta paziņojums vai signāls, ka līdzeklis būs obligāti jāaktivizē? 
Paziņojuma mehānisms, kas saistīts ar līdzekļa obligātu izveidi, šobrīd neeksistē.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Vai funkcijas kādreiz tiek iespējotas, klientam nezinot par to? 
Jā, funkcijas var iespējot, debitoram nezinot, šādās situācijās:
- Šī funkcija ir pārvietota uz **Ieslēgtu pēc noklusējuma**. Šajā stāvoklī šo līdzekli joprojām var atspējot. 
- Funkcija ir atjaunināta uz **Obligātu**. Šīs izmaiņas notiks tikai kombinācijā ar galveno laidienu. Kritiskas funkcijas izņēmuma dēļ var tikt pārvietotas uz **Obligātām** jebkurā atjauninājumā.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Kas ir funkciju lidošana un kā tā ir saistīta ar funkciju pārvaldību? 
Funkciju lidojumi ir reāllaika ieslēgšanas/izslēgšanas slēdži, ko kontrolē Microsoft. Tie ir atsevišķi no klienta kontroles, ko nodrošina Līdzekļu pārvaldība. 
- Privātās priekšskatījuma funkcijas netiks uzskaitītas funkciju pārvaldībā, kamēr tās netiks ieslēgtas. Ražošanā klientam ir jāpiekrīt piedalīties īpašā programmā, lai tas notiktu.
- Publiskais priekšskatījums un Izlaistie (vispārīgi pieejamie) līdzekļi tiks uzskaitīti Funkciju pārvaldībā, ja vien tie netiek izslēgti. Funkcijas izslēgšana tiek uzskatīta par pēdējo iespēju produktu komandām, ja tiek atrasta kritiska problēma, un tā parasti ir viena klienta darbība.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Vai funkcijas kādreiz tiek izslēgtas, klientam nezinot par to? 
Jā, ja līdzeklis ietekmē tādas vides darbību, kurai nav funkcionālas ietekmes, tad to var iespējot pēc noklusējuma.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Kā var pārbaudīt līdzekļa iespējošanu kodā?
Lietojiet metodi **isFeatureEnabled**, kas atrodas klasē **FeatureStateProvider**, padodot tai līdzekļu klases instanci. Piemērs:

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Kā var pārbaudīt līdzekļa iespējošanu metadatos?
**FeatureClass** rekvizītu var izmantot, lai norādītu, ka daži metadati ir saistīti ar līdzekli. Jāizmanto līdzeklim izmantotais klases nosaukums, piemēram, **BatchContentionPreventionFeature**. Šie metadati ir redzami tikai šajā līdzeklī. **Rekvizīts FeatureClass** ir pieejams izvēlnēs, izvēlnes elementos, uzskaitījuma vērtībās un tabulas/skata laukos.

### <a name="what-is-a-feature-class"></a>Kas ir līdzekļu klase?
Līdzekļu pārvaldības līdzekļi ir definēti kā *līdzekļu klases*. Līdzekļu klases **ievieš IFeatureMetadata** un izmanto līdzekļu klases atribūtu, lai identificētu sevi līdzekļu pārvaldības darbvietā. Ir pieejami daudzi līdzekļu klašu piemēri, ko var pārbaudīt, lai iespējotu kodu, izmantojot **FeatureStateProvider** API, un metadatos, izmantojot **FeatureClass** rekvizītu. Piemērs:

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Kāds IFeatureLifecycle ir ieviests ar dažām funkciju klasēm?
IFeatureLifecycle ir iekšējs Microsoft mehānisms līdzekļu dzīves cikla stadijas norādīšanai. Līdzekļi var būt šādi:
- `PrivatePreview` — lai būtu redzams, nepieciešams lidojums.
- `PublicPreview` — tiek parādīts pēc noklusējuma, bet ar brīdinājumu, ka līdzeklis ir priekšskatījumā.
- `Released`– pilnībā nodots izpildei.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
