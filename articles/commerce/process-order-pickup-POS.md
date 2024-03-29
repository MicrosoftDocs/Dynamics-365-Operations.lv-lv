---
title: Klientu pasūtījumu izdošanas process programmā POS
description: Šajā rakstā ir paskaidrota funkcionalitāte, kas ir pieejama pārdošanas punkta (POS) programmā debitoru pasūtījumu savākšanas apstrādei.
author: hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 7fd7d08ac59f6fe7381b79d854160188ef1c325a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286362"
---
# <a name="process-customer-order-pickups-in-pos"></a>Klientu pasūtījumu izdošanas process programmā POS

[!include [banner](includes/banner.md)]

Kad [klienta pasūtījums](customer-orders-overview.md) ir izveidots izdošanai veikalā, veikala lietotājs var izmantot pārdošanas punkta (POS) lietojumprogrammu, lai sāktu krājuma izdošanu. POS izpildīs gala maksājuma tveršanu pēc nepiesiešamības. Tas pabeigs arī krājumu un finanšu grāmatošanu izdotajiem daudzumiem.

Ja esat veikala lietotājs, varat veikt izdošanu, izmantojot vai nu **Pasūtījuma atsaukšanas** operāciju, vai **Pasūtījuma izpildīšanas** operāciju programmā POS. Lai **Izdošanas** operāciju padarītu pieejamu, vispirms veiciet kādu no šīm darbībām:

- Lai izmantotu operāciju **Pasūtījuma atsaukšana**, meklējiet un atlasiet izdodamo pasūtījumu.
- Lai izmantotu operāciju **Pasūtījuma izpildīšana**, meklējiet un atlasiet vienu vai vairākas pasūtījuma rindas.

Ja atlasītais pasūtījums vai pasūtījuma rindas šajā konkrētajā veikalā nav konfigurētas, vai pasūtījums jau ir pilnībā izdots, operācija **Izdošana** nebūs pieejama.

![Izdošanas operācija.](media/pickupoperation.png)

Programmas Microsoft Dynamics 365 Commerce versijā 10.0.17 un jaunākās līdzekli **Uzlabota lietotāja pieredze izdošanas pasūtījuma apstrādei pārdošanas punktā** var ieslēgt, izmantojot Commerce Headquarters līdzekļu pārvaldību. Ja šis līdzeklis ir izslēgts, lietotāji nevar atlasīt izdošanas daudzumus. Pēc noklusējuma pilnais daudzums, kas tika pasūtīts rindai, ir daudzums, kas tiks izdots. Šī pieredze var būt problemātiska, jo lietotāji var aizmirst atlasīt dažus krājumus izdošanai, veicot izdošanu, izmantojot pasūtījuma izpildi.

Līdzeklis **Uzlabota lietotāja pieredze izdošanas pasūtījuma apstrādei pārdošanas punktā** sniedz lietotājiem lielāku kontroli pār izdošanai atlasītajām precēm un to preču daudzumu, kas tiks izdots. Lietotājiem nav jāatlasa katra pārdošanas pasūtījuma rinda pasūtījuma izpildes lapā pirms **Izdošanas** atlases. Tiks parādīti visi krājumi, kurus var izdot. Lietotāji var norādīt vairākas rindas izdošanai, pat ja ir atlasīta tikai viena produktu līnija.

Ja ir ieslēgts līdzeklis **Uzlabota lietotāja pieredze izdošanas pasūtījuma apstrādei pārdošanas punktā**, un jūs atlasāt operāciju **Izdošana**, tiks parādīts **Izdošanas** dialoglodziņš. Tajā varat atlasīt krājumus un daudzumus, kas tiks izdoti. Pēc noklusējuma visi krājumu pasūtītie daudzumi, kuri ir izdošanas vai iepakošanas stāvoklī, tiek uzskatīti par piemērotiem izdošanai. Pēc noklusējuma šis daudzums tiek iestatīts kā izdošanas daudzums. Ievadīto daudzumu var mainīt, ja daudzums nav 0 (nulle) un nepārsniedz atlasītās rindas kopējo atvērto (t.i., rēķinā neiekļauto) daudzumu.

![Izdošanas dialoglodziņš.](media/pickupselect.png)

Kad atlasāt izdodamos daudzumus, un pēc tam atlasāt **Izdošana**, tiek parādīta darījuma lapa. Ja [universālā kanāla maksājumu](omni-channel-payments.md) līdzeklis ir ieslēgts un failā ir iepriekš autorizēti kredītkaršu maksājumi, tie tiek attiecināti uz maksājumu.

Darījuma lapā sistēma aprēķina maksājamās summas, aprēķinot kopējo summu, kas ir jāmaksā par atlasītajiem izdošanas krājumiem, un pēc tam atņemot visus iepriekš piemērotos depozītus vai autorizētos kredītkaršu maksājumus. Jums jāapstrādā maksājums, lai pabeigtu izdošanas darījumu. Ja darījuma lapas [ekrāna izkārtojums](pos-screen-layouts.md) ir konfigurēts tā, ka tajā ir iekļauta operācija **Pabeigt darījumu** un summa nav jāmaksā, darījumu var pabeigt, neatlasot maksājuma metodi. Ja operācija **Pabeigt darījumu** nav pieejama, varat atlasīt saiti **summa apmaksai 0,00 $** cilnē **Kopsummas**, lai pabeigtu darījumu, neatlasot maksājuma metodi.

![Klienta pasūtījuma izdošanas darījuma lapa.](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Izdošanas rindu daudzuma mainīšana

Ja nepieciešams mainīt izdošanas daudzumu pēc tam, kad jau atlasīti krājumi izdošanai, varat atlasīt **Iestatīt daudzumu**. Izdošanas daudzumu nevar iestatīt uz **0** (nulli) vai palielināt uz vērtību, kas pārsniedz rēķinā neiekļauto daudzumu, kas atrodas pasūtījuma rindā. Lai noņemtu izdošanas rindu no darījuma groza, atlasiet **Anulēt darījumu**. Pašreizējais darījums tiks pārtraukts, un **Izdošanas** operācijas plūsma tiks restartēta.

Ja līdzeklis **Uzlabota lietotāja pieredze izdošanas pasūtījuma apstrādei pārdošanas punktā** ir ieslēgts, organizācijas var pievienot pogu operācijai **Izdošanas rindu mainīšana** darījuma lapas ekrāna izkārtojumam. Kad programmā POS ir izveidots izdošanas darījuma grozs un atlasīti krājumi, varat izvēlēties **Izdošanas rindu mainīšanu**, ja ir nepieciešams mainīt izdošanas krājumus, bet nevēlaties anulēt visu darījumu. Parādītajā **Izdošanas rindu mainīšanas** dialoglodziņā varat mainīt izdošanas krājumus un daudzumus. Pēc tam darījuma grozs tiek atjaunināts, lai atspoguļotu veiktās izmaiņas.

![Izdošanas krājumu mainīšanas dialoglodziņš.](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
