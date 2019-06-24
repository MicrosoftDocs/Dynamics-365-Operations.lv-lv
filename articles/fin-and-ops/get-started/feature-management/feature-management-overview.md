---
title: Līdzekļu pārvaldības pārskats
description: Šajā tēmā ir aprakstīts līdzeklis Līdzekļu pārvaldība un tā lietošanas iespējas.
author: mikefalkner
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: b200156a623c67a562cc1a5952899e3a77517528
ms.sourcegitcommit: bbc9aa0d6b94a942e1f4d5b038601509dcc87937
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/05/2019
ms.locfileid: "1619148"
---
# <a name="feature-management-overview"></a>Līdzekļu pārvaldības pārskats

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Katrā pakalpojuma Microsoft Dynamics 365 for Finance and Operations laidienā tiek pievienoti un atjaunināti līdzekļi. Pieredze Līdzekļu pārvaldība nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.

## <a name="the-feature-management-workspace"></a>Darbvieta Līdzekļu pārvaldība

Varat atvērt darbvietu **Līdzekļu pārvaldība** darbvietu, atlasot attiecīgo elementu informācijas panelī. Tiks parādīta lapa ar līdzekļu sarakstu visiem laidieniem, ko atbalsta Līdzekļu pārvaldības pieredze. Laika gaitā korporācija Microsoft uzlabos Līdzekļu pārvaldības pieredzi, lai tā iekļautu papildu funkcionalitāti, kas palīdz pārvaldīt līdzekļus.

Līdzekļu sarakstā ir tālāk norādītā informācija.

- **Līdzekļa nosaukums** — pievienotā līdzekļa apraksts.
- **Iespējošanas statuss** — simbols norāda, vai līdzeklis ir ieslēgts (atzīme), nav ieslēgts (tukšs), tiek plānota tā ieslēgšana (pulkstenis) vai arī ir ieslēgts obligāti (piekaramā atslēga). Šeit redzamais iestatījums tiek izmantots visām juridiskajām personām. Ņemiet vērā, ka pat tad, ja līdzeklis ir ieslēgts, to joprojām kontrolē drošība. Tāpēc šis līdzeklis būs pieejams tikai tiem lietotājiem, kuriem ir piekļuve tam, pamatojoties uz lietotāja drošības lomu. Tas būs pieejams arī tikai juridiskajās personās, kurām lietotājam ir piekļuve.
- **Iespējošanas datums** — datums, kad līdzeklis tika ieslēgts vai kad to ir plānots ieslēgt.
- **Līdzeklis pievienots** — datums, kad līdzeklis tika pievienots jūsu videi. Šis datums tiek ievadīts automātiski, kad mēneša laidiena cikla laikā tiek atjaunināta jūsu vide.
- **Modulis** — modulis, ko ietekmē jaunais līdzeklis.

Kad atlasāt līdzekli, detalizētas informācijas rūtī pa labi no līdzekļu saraksta tiek parādīta papildinformācija. Rūts augšā redzēsit līdzekļa nosaukumu, pievienošanas datumu, moduli, ko ietekmē šis līdzeklis, un saiti **Papildinformācija**. Atlasiet šo saiti, lai skatītu līdzekļa dokumentāciju. Ja dokumentācija nav pieejama, jūs tiekat novirzīts uz pagaidu lapu. Detalizētas informācijas rūtī ir ietverts arī lauks **Komentāri**, kur varat pievienot savus komentārus par šo līdzekli.

Arī darbvietā **Līdzekļu pārvaldība** ir vairākas cilnes, un katrā no tām tiek rādīts līdzekļu saraksts.

- **Jauns** — šajā cilnē tiek rādīti visi līdzekļi, kas ir pievienoti kopš pēdējās ikmēneša atjaunināšanas. Ja esat izlaidis kādu ikmēneša atjauninājumu, šajā cilnē tiek rādīti visi jaunie līdzekļi, kas ir pievienoti kopš pēdējās reizes, kad veicāt atjaunināšanu. Jaunākie līdzekļi tiek parādīti saraksta sākumā. Kopējais jauno līdzekļu skaits tiek rādīts arī lapas augšā esošajā elementā.
- **Nav iespējots** — šajā cilnē tiek rādīti visi līdzekļi, kas nav ieslēgti. Jaunākie līdzekļi tiek parādīti saraksta sākumā. Kopējais jauno, neieslēgto līdzekļu skaits tiek rādīts arī lapas augšā esošajā elementā.
- **Ieplānots** — šajā cilnē tiek rādīti visi līdzekļi, kurus ir plānots ieslēgt nākotnē. Saraksta augšā tiek rādīti līdzekļi, kuru plānotais datums ir visdrīzāk. Kopējais plānoto jauno līdzekļu skaits tiek rādīts arī lapas augšā esošajā elementā.
- **Visi** — šajā cilnē tiek rādīti visi līdzekļi. Jaunākie līdzekļi tiek parādīti saraksta sākumā.

## <a name="turn-on-a-feature"></a>Līdzekļa ieslēgšana

Ja līdzeklis nav ieslēgts, detalizētas informācijas rūtī tiek rādīta poga **Iespējot tūlīt**. Varat izmantot šo pogu, lai līdzekli ieslēgtu.

- Atlasiet līdzekli, ko vēlaties ieslēgt, un pēc tam detalizētās informācijas rūtī atlasiet **Iespējot tūlīt**. Līdzeklis ir ieslēgts.

Dažus līdzekļus pēc to ieslēgšanas nevar izslēgt. Ja līdzekli, kuru mēģināt ieslēgt, vairs nevar izslēgt, jums tiek parādīts brīdinājums. Šajā brīdī varat atlasīt **Atcelt**, lai atceltu operāciju, un atstāt šo līdzekli izslēgtu. Taču, ja atlasāt **Iespējot**, lai šo līdzekli ieslēgtu, vēlāk to vairs nevarēsit izslēgt.

Pēc līdzekļa ieslēgšanas detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šajā ziņojumā ir norādīts, ka līdzeklis tika ieslēgts, vai arī ir norādīts turpmāks datums, kad šo līdzekli ir plānots ieslēgt. Tas tiek parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli.

Līdzekļi, kuru ieslēgšana ir plānota nākotnē, ir redzami cilnē **Plānots**. Tie tiek ieslēgti ar pakešveida apstrādi norādītā datuma pusnaktī, pamatojoties uz sistēmas datuma norādīto laika zonu.

## <a name="reschedule-a-feature"></a>Līdzekļa pārplānošana

Ja līdzekli ir plānots ieslēgt nākotnē, detalizētas informācijas rūtī tiek rādīta poga **Plānot**. Varat izmantot šo pogu, lai mainītu vērtību **Iespējošanas datums** uz citu.

1. Atlasiet ieplānoto līdzekli, kuru vēlaties pārplānot, un pēc tam detalizētas informācijas rūtī atlasiet **Plānot**.
2. Parādītajā dialoglodziņā, laukā **Iespējošanas datums** norādiet jauno datumu, kad šis līdzeklis ir jāieslēdz.
3. Atlasiet opciju **Iespējot**, lai pārplānotu līdzekli, vai **Atspējot**, lai atceltu ieplānošanu.

## <a name="turn-off-a-feature"></a>Līdzekļa izslēgšana

Ja līdzeklis jau ir ieslēgts, detalizētas informācijas rūtī tiek rādīta poga **Atspējot**. Varat izmantot šo pogu, lai līdzekli izslēgtu. Poga **Atspējot** nav pieejama, ja līdzekli pēc tā ieslēgšanas vairs nevar izslēgt.

- Atlasiet līdzekli, kuru vēlaties izslēgt, un pēc tam detalizētas informācijas rūtī atlasiet **Atspējot**. Līdzeklis ir izslēgts, un lauks **Iespējošanas datums** ir notīrīts.

Pēc līdzekļa izslēgšanas detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šis ziņojums norāda, ka līdzeklis vēl nav bijis ieslēgts. Tas tiek parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli. Līdzekļi, kas vēl nav bijuši ieslēgti, ir redzami cilnē **Nav iespējots**.

## <a name="features-that-must-be-turned-on"></a>Līdzekļi, kam ir jābūt ieslēgtiem

Reizēm tiek piegādāts kritisks līdzeklis, kam ir jāieslēdzas automātiski, kad veicat atjaunināšanu. Šie līdzekļi tiks automātiski ieslēgti datumā, kas ir norādīts laukā **Iespējošanas datums**. Šiem līdzekļiem detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šajā ziņojumā ir norādīts, ka līdzeklis tika ieslēgts, vai arī ir norādīts turpmāks datums, kad šis līdzekli tiks ieslēgts. Tas tiek parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli.

## <a name="turn-on-all-features-automatically"></a>Visu līdzekļu ieslēgšana automātiski

Pēc noklusējuma visi līdzekļi, kas ir pievienoti jūsu videi, ir izslēgti, izņemot gadījumus, ja tie ir obligātie līdzekļi. Taču, ja vēlaties automātiski ieslēgt visus jaunos līdzekļus, varat izmantot nolaižamo sarakstu zem darbvietas nosaukuma, lai mainītu to, kas notiek pēc jaunu līdzekļu pievienošanas.

- Atlasiet **Visi jaunie līdzekļi būs iespējoti pēc noklusējuma**, lai automātiski ieslēgtu visus jaunos līdzekļus, kad tie ir pievienoti jūsu videi.
- Atlasiet **Visi jaunie līdzekļi būs atspējoti pēc noklusējuma**, lai automātiski izslēgtu visus jaunos līdzekļus, kad tie ir pievienoti jūsu videi.

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