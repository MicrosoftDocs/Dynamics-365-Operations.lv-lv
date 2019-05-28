---
title: Zvanu centra kanālu iestatīšana
description: Šajā tēmā ir sniegta informācija par to, kā apstrādāt zvanu centru pasūtījumus, izmantojot Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 04/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bfbb763b8ded2a0ce90b66eb686379b1dc92a6d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549363"
---
# <a name="set-up-call-center-channels"></a>Zvanu centra kanālu iestatīšana

[!include [banner](includes/banner.md)]

Uzņēmums var definēt vairākus zvanu centra kanālus programmā Microsoft Dynamics 365 for Retail. Zvanu centra kanāli tiek konfigurēti sadaļā **Retail** \> **Kanāli** \> **Zvanu centri** \> **Visi zvanu centri**, un tie tiek noteikti juridiskajai iestādei.

Kad ir izveidots jauns zvanu centra kanāls, tam tiek sistemātiski piešķirts pārvaldības struktūrvienības numurs. Tā kā zvanu centri tiek izveidoti kā pārvaldības struktūrvienības, zvanu centra kanālu lietotāji var piesaistīt dažādiem Retail līdzekļiem, piemēram, preču klāstiem, katalogiem un konkrētiem piegādes veidiem.

Zvanu centra kanālam var konfigurēt noklusējuma noliktavu. Kad šajā kanālā tiek veidoti pārdošanas pasūtījumi, noklusējuma noliktava tiek automātiski ievadīta pārdošanas pasūtījuma virsrakstā, ja vien šim pārdošanas pasūtījumam atlasītajam debitoram nav definēta cita noliktava. Tādā gadījumā pēc noklusējuma tiek ievadīta šī debitora noliktava.

Lai izmantotu zvanu centra līdzekļus, lietotājiem ir jābūt saistītiem ar zvanu centra kanālu. Visi pārdošanas pasūtījumi, ko lietotājs izveido programmatūrā Retail, tiek automātiski saistīti ar šī lietotāja zvanu centra kanālu. Pašlaik viens lietotājs nevar būt vienlaikus saistīts ar vairākiem zvanu centra kanāliem.

Zvanu centra kanālam var konfigurēt arī e-pasta paziņojumu profilu. Profils nosaka e-pasta veidņu kopu, kas tiek izmantota, sūtot e-pasta ziņojumu debitoriem, kuri veic pasūtījumus, izmantojot attiecīgo zvanu centra kanālu. E-pasta trigerus var konfigurēt attiecībā pret sistēmas notikumiem, piemēram, pasūtījuma iesniegšanu vai pasūtījuma nosūtīšanu.

Lai pārdošanu varētu pareizi apstrādāt, izmantojot zvanu centra kanālu, šim kanālam ir nepieciešams definēt pareizas [maksāšanas metodes](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) un piegādes veidus.

Zvanu centra kanāla līmenī varat definēt citas noklusējuma vērtības, kas ir saistītas ar finanšu dimensijām, kuras tiks saistītas ar šī kanāla izveidotajiem pasūtījumiem.

## <a name="options-for-order-processing-behavior"></a>Pasūtījumu apstrādes uzvedības opcijas

Trīs iestatījumiem zvanu centra konfigurācijā ir būtiska ietekme uz līdzekļiem un funkcijām, kuras ir pieejamas pret attiecīgo zvanu centru izveidotajiem pārdošanas pasūtījumiem. Šie iestatījumi ir: **Iespējot pasūtījuma pabeigšanu**, **Iespējot tiešo pārdošanu** un **Iespējot pasūtījuma cenu kontroli**.

### <a name="enable-order-completion"></a>Iespējot pasūtījuma pabeigšanu

Iestatījumam **Iespējot pasūtījuma pabeigšanu** zvanu centra kanālā ir būtiska ietekme uz attiecīgajam kanālam ievadīto pārdošanas pasūtījumu apstrādes plūsmu. Ja šis iestatījums ir ieslēgts, visiem pārdošanas pasūtījumiem ir jāizpilda apstiprināšanas kārtulu kopa, un tikai pēc tam tos var apstiprināt. Šīs kārtulas varat palaist, atlasot pogu **Pabeigt**, kas ir pievienota darbību rūtij šī pārdošanas pasūtījuma lapā. Visiem pārdošanas pasūtījumiem, kas tiek izveidoti, kad iestatījums **Iespējot pasūtījuma pabeigšanu** ir ieslēgts, ir jāizpilda pasūtījuma pabeigšanas process. Šis process liek izmantot maksājuma tveršanu un maksājuma validēšanas loģiku. Papildus maksājuma realizēšanai pasūtījuma iesniegšanas process var izsaukt [krāpniecības pārbaudes](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts), kuras sistēmā varat konfigurēt. Pasūtījumi, kas neiztur maksājumu vai krāpniecības validācijas, tiek aizturēti, un tos nevar nodot tālākai apstrādāšanai (piemēram, izdošanai vai nosūtīšanai), kamēr nav atrisināta problēma, kas šo aizturēšanu izraisīja.

Kad zvanu centra kanālam ir ieslēgts iestatījums **Iespējot pasūtījuma pabeigšanu**, ja pārdošanas pasūtījumā tiek ievadīti rindu vienumi un kanāla lietotājs mēģina aizvērt pārdošanas pasūtījuma formu vai aiziet no tās, pirms tam neatlasot vienumu **Pabeigt**, sistēma liek izmantot pasūtījuma pabeigšanas procesu, atverot pārdošanas pasūtījuma kopsavilkuma lapu un pieprasot, lai lietotājs šo pasūtījumu iesniedz pareizi. Ja pasūtījumu nevar pareizi iesniegt kopā ar maksājumu, lietotājs var izmantot funkcionalitāti [pasūtījuma aizturēšanas](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), lai šo pasūtījumu aizturētu. Ja lietotājs mēģina pasūtījumu atcelt, lietotājam tas ir pareizi jāatceļ, izmantojot funkciju Atcelt vai funkciju Dzēst — atkarībā no lietotāja drošības atļautās funkcijas.

Ja zvanu centra kanālam ir ieslēgts iestatījums **Iespējot pasūtījuma pabeigšanu**, šim pasūtījumam tiek izsekots lauks **Maksājuma statuss**. Sistēma aprēķina vērtību **Maksājuma statuss**, kad pārdošanas pasūtījums ir iesniegts. Tikai pasūtījumiem, kuriem ir apstiprināts maksājuma statuss, ir atļauts pārvietoties sistēmā papildu pasūtījuma apstrādes darbību veikšanai, piemēram, izdošanai un nosūtīšanai. Ja maksājumi tiek noraidīti, detalizētajā informācijā par pārdošanas pasūtījuma statusu tiek iespējots karodziņš **neapstrādāt**; šādi pasūtījums tiek aizturēts, līdz maksājuma problēma ir atrisināta.

Turklāt, ja ir ieslēgts iestatījums **Iespējot pasūtījuma pabeigšanu**, kad lietotāji izveido pārdošanas pasūtījumus un ir atvēruši rindas vienuma ievadīšanas režīmu, galvenajā pārdošanas pasūtījuma virsrakstā ir pieejams lauks **Avots**. Lauks **Avots** tiek izmantots, lai tvertu [kataloga pirmkodu](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) tiešā mārketinga pārdošanas scenārijā. Pēc tam šis kods var vadīt īpašas cenas un reklāmas akcijas.

Pat tad, ja iestatījums **Iespējot pasūtījuma pabeigšanu** ir izslēgts, lietotāji pārdošanas pasūtījumam joprojām var lietot pirmkodu. Taču viņiem vispirms ir jāatver pārdošanas pasūtījuma virsraksta detalizētā informācija, lai piekļūtu laukam **Avots**. Citiem vārdiem sakot, ir jāveic daži papildu klikšķi. Tāda pati uzvedība attiecas uz tādiem līdzekļiem kā nosūtīšanas pabeigšana un paātrinātās izpildes pasūtījumi. Šie līdzekļi ir pieejami visiem pasūtījumiem, kas ir izveidoti šajā zvanu centrā. Taču, kad ir ieslēgts iestatījums **Iespējot pasūtījuma pabeigšanu**, lietotāji var redzēt šo līdzekļu konfigurāciju pārdošanas virsrakstā, kamēr ir ieslēgts rindas ieraksta skats. Viņiem nav nepieciešams detalizēti meklēt pārdošanas pasūtījuma virsraksta informācijā, lai atrastu atbilstošos iestatījumus un laukus.

### <a name="enable-direct-selling"></a>Iespējot tiešo pārdošanu

Ja zvanu centra kanālam ir ieslēgts iestatījums **Iespējot tiešo pārdošanu**, lietotāji var izmantot programmatūras Retail papildu pārdošanas un šķērspārdošanas līdzekļus. Tādā gadījumā pasūtījuma izveides laikā tiek parādīti uznirstošie logi un tiek ieteiktas citas preces, kuras zvanu centra lietotājs var piedāvāt debitoram. Ieteiktās preces ir atkarīgas no preces, kuru tikko pasūtīja pārdošanas pasūtījuma rindā. Pašlaik papildu pārdošanas un šķērspārdošanas ieteikumi ir konfigurēti krājuma līmenī precēm vai katalogiem. Ja zvanu centra kanālam iestatījums **Iespējot tiešo pārdošanu** ir izslēgts, pasūtījuma izveides laikā uznirstošie logi netiek parādīti pat tad, ja pasūtītajam krājumam ir definēta derīga papildu pārdošana vai šķērspārdošana.

Kad iestatījums **Iespējot tiešo pārdošanu** ir ieslēgts, ir ieslēgti arī pārdošanas pasūtījuma ievades lapas skripti un attēlu līdzekļi. Tādā gadījumā pasūtījuma izveides laikā informācijas panelis ir pieejams lapas labajā pusē. Šis panelis var rādīt skriptus, kas ir saistīti ar vispārējo pasūtījuma izveides procesu, kataloga pirmkodu, kas tika lietots, vai skriptiem, kas ir saistīti ar pasūtītajiem krājumiem. Turklāt attēlu panelī var tikt rādīts preces attēls krājumiem, kuri tiek pasūtīti, ja attiecīgajam vienumam preču iestatījumos ir definēts attēls.

### <a name="enable-order-price-control"></a>Iespējot pasūtījuma cenu kontroli

Kad ir ieslēgts iestatījums **Iespējot pasūtījuma cenu kontroli**, pasūtījuma izveides laikā krājuma pārdošanas cenu var mainīt tikai autorizēti lietotāji. Šīs izmaiņas nedrīkst pārsniegt noteiktās tolerances. Savukārt lietotājiem, kuriem nav atbilstošu atļauju, ir jāiesniedz pieprasījums mainīt cenu. Pēc tam šis pieprasījuma tiek apstrādāts, izmantojot sistēmas pārskatīšanas un apstiprināšanas darbplūsmas.

## <a name="channel-users"></a>Kanāla lietotāji

Kad definējat zvanu centra kanālu, jums ir jāsaista kanāla lietotāji ar šo zvanu centru. Pretējā gadījumā sistēma šo zvanu centru nevar lietot. Kad lietotāji pierakstās programmatūrā Retail un ievada pārdošanas pasūtījumus vai atgriešanas pasūtījumus kādā lapā, kas ir saistīta ar pasūtījuma izveidi, viņu lietotāja ID tiek validēti attiecībā pret zvanu centra kanāla konfigurāciju. Ja lietotājs ir saistīts ar noteiktu zvanu centra kanālu, tad šī lietotāja izveidotie pasūtījumi pārmanto attiecīgā kanāla iezīmes un noklusējuma vērtības.

Pārdošanas pasūtījuma virsrakstā karodziņš **Pārdošana mazumtirdzniecībā** pēc noklusējuma tiek ieslēgts visiem pasūtījumiem, ko izveido zvanu centra lietotāji. Pēc tam pasūtījumos var izmantot sistēmas mazumtirdzniecībai noteiktos cenu un veicināšanas līdzekļus.

Lietotāji, kas nav saistīti ar zvanu centra kanālu, izmantot Microsoft Dynamics 365 for Finance and Operations standarta pasūtījuma izveides līdzekļus. Pasūtījumi, ko šie lietotāji ievada, izmantojot pārdošanas pasūtījuma izveides formu, netiek sistemātiski identificēti kā Retail pasūtījumi. Turklāt šie lietotāju ievadītie pasūtījumi netiek pakļauti nekādām pasūtījumu pabeigšanas apstrādes kārtulām, mazumtirdzniecības cenu noteikšanas loģikai vai citām pasūtījumu validācijām, kuras var definēt zvanu centra kanāla konfigurācijā vai zvanu centra sistēmas parametros.

Kad esat beidzis konfigurēt zvanu centra kanālu un definēt kanāla lietotājus, lai palīdzētu garantēt vēlamo sistēmas uzvedību, pārliecinieties, vai ir definēti visi nepieciešamie zvanu centra parametri sadaļā **Retail** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Zvanu centra parametri**. Pārliecinieties, vai ir norādītas arī saistītās numuru sērijas.
