---
title: Līdzekļu pārvaldības pārskats
description: Šajā tēmā ir aprakstīts līdzeklis Līdzekļu pārvaldība un tā lietošanas iespējas.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538699"
---
# <a name="feature-management-overview"></a>Līdzekļu pārvaldības pārskats

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Katrā pakalpojuma Microsoft Dynamics 365 for Finance and Operations laidienā tiek pievienoti un atjaunināti līdzekļi. Pieredze Līdzekļu pārvaldība nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.

## <a name="the-feature-management-workspace"></a>Darbvieta Līdzekļu pārvaldība

Varat atvērt darbvietu **Līdzekļu pārvaldība** darbvietu, atlasot attiecīgo elementu informācijas panelī. Tiks parādīta lapa ar līdzekļu sarakstu visiem laidieniem, ko atbalsta Līdzekļu pārvaldības pieredze. Laika gaitā korporācija Microsoft uzlabos Līdzekļu pārvaldības pieredzi, lai tā iekļautu papildu funkcionalitāti, kas palīdz pārvaldīt līdzekļus.

Līdzekļu sarakstā ir tālāk norādītā informācija.

- **Līdzekļa nosaukums** — pievienotā līdzekļa apraksts.
- **Iespējošanas statuss** — simbols norāda, vai līdzeklis ir iespējots (atzīme), nav iespējots (tukšs), ir ieplānots iespējošanai (pulkstenis) vai arī ir obligāti iespējots (atslēga). Šeit redzamais iestatījums tiek izmantots visām juridiskajām personām. Ņemiet vērā, ka pat tad, ja līdzeklis ir ieslēgts, to joprojām kontrolē drošība. Tāpēc šis līdzeklis būs pieejams tikai tiem lietotājiem, kuriem ir piekļuve tam, pamatojoties uz lietotāja drošības lomu. Tas būs pieejams arī tikai juridiskajām personām, kurām lietotājam ir piekļuve.
- **Iespējošanas datums** — datums, kad līdzeklis tika ieslēgts vai tiks ieslēgts, ja datums ir nākotnes datums.
- **Līdzeklis pievienots** — datums, kad līdzeklis tika pievienots jūsu videi. Šis datums tiek ievadīts automātiski, kad mēneša laidiena cikla laikā tiek atjaunināta jūsu vide.
- **Modulis** — modulis, ko ietekmē jaunais līdzeklis.

Kad atlasāt līdzekli, detalizētas informācijas rūtī pa labi no līdzekļu saraksta tiek parādīta papildinformācija. Rūts augšā redzēsit līdzekļa nosaukumu, pievienošanas datumu, moduli, ko ietekmē šis līdzeklis, un saiti **Papildinformācija**. Atlasiet šo saiti, lai skatītu līdzekļa dokumentāciju. Ja dokumentācija nav pieejama, tiks atvērta pagaidu lapa. Detalizētas informācijas rūtī ir ietverts arī lauks **Komentāri**, kur varat pievienot savus komentārus par šo līdzekli.

Arī darbvietā **Līdzekļu pārvaldība** ir iekļautas vairākas cilnes ar līdzekļu sarakstu. 
- **Jauns** — tiek rādīti visi līdzekļi, kas ir pievienoti kopš pēdējās ikmēneša atjaunināšanas. Ja esat izlaidis ikmēneša atjauninājumus, šajā laukā būs visi jaunie līdzekļi kopš pēdējās atjaunināšanas reizes. Jaunākie līdzekļi tiek parādīti saraksta sākumā. Kopējais jauno līdzekļu skaits tiek norādīts arī elementā lapas augšā.
- **Nav iespējots** — tiek rādīti visi neiespējotie līdzekļi. Jaunākie līdzekļi tiek parādīti saraksta sākumā. Kopējais jauno līdzekļu skaits tiek norādīts arī elementā lapas augšā.
- **Ieplānots** — tiek rādīti visi līdzekļi, kuriem ir ieplānota iespējošana nākotnē. Saraksta augšā tiks parādīti līdzekļi, kuriem ir agrāks ieplānotais datums. Kopējais jauno līdzekļu skaits tiek norādīts arī elementā lapas augšā.
- **Visi** — tiek rādīti visi līdzekļi. Jaunākie līdzekļi tiek parādīti saraksta sākumā.


## <a name="enable-a-feature"></a>Līdzekļa iespējošana

Ja līdzeklis nav iespējots, detalizētas informācijas rūtī tiek parādīta poga **Iespējot**. Varat izmantot šo pogu līdzekļa iespējošanai.

1. Atlasiet līdzekli, ko vēlaties iespējot, un pēc tam detalizētās informācijas rūtī atlasiet **Iespējot**.
2. Tiek parādīts slīdnis, kurā var norādīt līdzekļa iespējošanas datumu. Pēc noklusējuma šis datums tiek iestatīts kā pašreizējais datums.
3. Atlasiet **Iespējot**, lai iespējotu šo līdzekli.

Dažus līdzekļus nevar atspējot pēc to iespējošanas. Ja līdzekli, kuru mēģināt iespējot, nevar atspējot, tiks parādīts brīdinājums. Šajā brīdī varat atlasīt **Atcelt**, lai atceltu darbību, un saglabāt līdzekli atspējotā statusā. Tomēr, ja atlasāt **Iespējot** un iespējojat līdzekli, nevarēsit to atspējot vēlāk.

Pēc līdzekļa iespējošanas detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šajā ziņojumā tiek norādīts, ka līdzeklis ir iespējots, vai arī tiek norādīts līdzekļa iespējošanas datums nākotnē. Ja izmantosit nākotnes datumu, līdzeklis tiks parādīts sarakstā **Plānotie**. Šis ziņojums tiks parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli. Nākotnē ieplānotie līdzekļi tiks iespējoti pusnaktī, izmantojot pakešveida apstrādi un pamatojoties uz sistēmas datuma pārstāvēto laika joslu. 

## <a name="reschedule-a-feature"></a>Līdzekļa pārplānošana

Ja līdzeklis ir iespējots nākotnē, detalizētas informācijas rūtī tiek parādīta poga **Pārplānot**. Varat izmantot šo pogu, lai mainītu datumu **Iespējošanas datums** uz citu.

1. Atlasiet ieplānotu līdzekli, ko vēlaties pārplānot, un pēc tam detalizētās informācijas rūtī atlasiet **Pārplānot**.
2. Tiek parādīts slīdnis, kurā var norādīt līdzekļa iespējošanas datumu. 
3. Atlasiet opciju **Iespējot**, lai pārplānotu līdzekli, vai **Atspējot**, lai atceltu ieplānošanu.

## <a name="disable-a-feature"></a>Līdzekļa atspējošana

Ja līdzeklis jau ir iespējots, detalizētas informācijas rūtī tiek parādīta poga **Atspējot**. Varat izmantot šo pogu līdzekļa atspējošanai. Poga **Atspējot** nav pieejama, ja līdzekli nevar atspējot pēc tā iespējošanas.

- Atlasiet līdzekli, ko vēlaties izslēgt, un pēc tam detalizētās informācijas rūtī atlasiet **Atspējot**.

- Līdzeklis tiek atspējots, un datums tiek dzēsts.

Pēc līdzekļa atspējošanas detalizētas informācijas rūtī zem saites **Papildinformācija** tiek rādīts ziņojums. Šajā ziņojumā ir norādīts, ka līdzeklis vēl nav iespējots un tas tiks parādīts sarakstā **Nav iespējots**. Ziņojums tiks parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli.

## <a name="features-that-must-be-enabled"></a>Līdzekļi, kam jābūt iespējotiem

Var tikt piegādāts kritisks līdzeklis, kas ir jāaktivizē automātiski atjaunināšanas laikā. Tas tiks automātiski aktivizēts datumā **Iespējošanas datums**. Detalizētās informācijas rūtī zem saites **Papildinformācija** tiks parādīts ziņojums. Šajā ziņojumā ir norādīts, ka līdzeklis ir iespējots vai tiks automātiski iespējots datumā **Iespējošanas datums**. Tas tiks parādīts katru reizi, kad līdzekļu sarakstā atlasāt šo līdzekli.

## <a name="assigning-roles"></a>Lomu piešķiršana

Darbvietu **Līdzekļu pārvaldība** var atvērt sistēmas administratori un lietotāji, kuriem ir piešķirta loma Līdzekļu pārvaldnieks vai Līdzekļu skatītājs; šīs lomas tika izveidotas, lai atbalstītu pieredzi Līdzekļu pārvaldība. Lietotāji ar līdzekļu pārvaldnieka lomu var ieslēgt vai izslēgt jebkuru līdzekli. Viņi var arī atjaunināt līdzekļa komentāru sadaļu. Lietotāji ar līdzekļu skatītāja lomu var tikai skatīt darbvietu **Līdzekļu pārvaldība**. Tie nevar ieslēgt vai izslēgt līdzekļus.

Līdzekļu pārvaldnieka loma un līdzekļu skatītāja loma neignorē esošo drošību, kas ir lietotājam. Lomas kontrolē tikai līdzekļu iespējošanas piekļuvi. Tas nenodrošina piekļuvi līdzekļiem.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Līdzekļu pārvaldības izmantošana, lai iespējotu ISV līdzekļus vai pielāgotus līdzekļus

Līdzekļu pārvaldības process pašlaik nav pieejams ISV līdzekļiem vai pielāgotajiem līdzekļiem. Mēs pievienojam papildu funkcionalitāti, lai uzlabotu līdzekļu pārvaldību, un, kad šie uzlabojumi tiks pabeigti, mēs padarīsim līdzekļu pārvaldību pieejamu visiem līdzekļiem un nodrošināsim konkrētus norādījumus, kā atjaunināt jūsu līdzekli tās izmantošanai.

## <a name="feature-management-and-flighting"></a>Funkciju pārvaldība un būvējumu izsniegšana

Līdzekļu pārvaldība ļauj kontrolēt līdzekļus, kas tiek nosūtīti katrā laidienā. Būvējumu izsniegšana ļauj Microsoft darba grupām izlaist līdzekļus ierobežotam klientu skaitam, lai tos varētu testēt un pārbaudīt, neietekmējot visus klientus. Līdzekļu pārvaldība nekontrolē līdzekļu būvējumu izsniegšanu.
