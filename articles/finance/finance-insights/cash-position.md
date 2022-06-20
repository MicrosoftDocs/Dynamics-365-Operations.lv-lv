---
title: Finansiālais stāvoklis
description: Šajā rakstā ir aprakstīts, kā naudas plūsmas prognozēšanas līdzeklis paredzētu organizācijas skaidras naudas pozīciju noteiktiem laikiem. Tajā ir aprakstītas arī opcijas, kas pieejamas, lai parādītu prognozes dažādiem periodiem.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7581142348d91b3a37cc75cf801e7bfc098cd604
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870254"
---
# <a name="cash-position"></a>Finansiālais stāvoklis

[!include [banner](../includes/banner.md)]

Skaidras naudas pozīcija ir skaidras naudas plūsmas prognoze tuvākajam termiņam. Tā ir balstīta uz skaidras naudas ieņēmumu prognozi no debitoriem, kuri maksā neapmaksātos rēķinus un pasūtījumus, kā arī uz skaidras naudas norēķinu prognozi, kurus kreditori maksā par pirkuma rēķiniem un pasūtījumiem.

Kad sistēma prognozē debitoru maksājumus, tā izmanto maksājuma prognozes no debitora maksājumu prognozēšanas līdzekļa. Bez maksājumu prognozēm, vidējais laiks, kas nepieciešams, lai pārveidotu debitora rēķinu maksājumam katram debitoram, tiek izmantots maksājuma datuma aprēķināšanai. Atvērtajiem debitora pasūtījumiem sistēma aprēķina rēķina datumu, izmantojot vidējo dienu skaitu pasūtījuma rindām katram debitoram, kam tiks izrakstīts rēķins. Pēc tam tā izmanto rēķina datumu kā ievadi maksājuma prognozēšanas funkcionalitātei. Debitora maksājumu prognozēšanas funkcionalitāte aprēķina katra rindā esošā pasūtījuma apmaksas datumu. 

Maksājuma datums nesamaksātajiem rēķiniem ir plānots no maksājuma prognozēm, izvēloties datumu, kas atbilst piecdesmit procentilēm no kumulatīvās sadales funkcijas, kas iegūta no prognozētā groza iespējamības.

Līdzīgu pieeja tiek izmantota, lai prognozētu maksājumus kreditoriem. Katram kreditoram sistēma aprēķina vidējo laiku, kas nepieciešams, lai pārvērstu kreditora rēķinu par maksājumu. Šis dienu skaitu tad arī tiek izmantots, lai aprēķinātu maksāšanas datumu. Atvērtajiem kreditoru pasūtījumiem sistēma aprēķina rēķina datumu, ņemot vērā vidējo dienu skaitu, kas nepieciešams, lai pārvērstu pasūtījuma rindas par rēķinu katram kreditoram. Pēc tam sistēma aprēķina maksājuma datumu, izmantojot vidējo laiku, kas nepieciešams, lai pārvērstu kreditora rēķinu par maksājumu katram kreditoram.

Cilnes **Skaidras naudas pozīcija** augšējā daļā ir ietverta skaidras naudas pozīcijas diagramma. Šī diagramma parāda skaidras naudas ienākšanu un aizplūšanu, un tās ietekmi uz kopējo likviditātes bilanci. Detalizētu informāciju skaidras naudas pozīcijas diagrammā iespējams skatīt ikdienas, nedēļas, mēneša vai ceturkšņa periodos. Atlasot **Ikdienas**, varat skatīt prognozes nākamajai 21 dienai. Atlasot **Nedēļas**, varat skatīt prognozes nākamām 20 nedēļām. Atlasot **Mēneša**, varat skatīt prognozes nākamajiem 12 mēnešiem. Atlasot **Ceturkšņa**, varat skatīt prognozes nākamajiem 12 ceturkšņiem. Varat paslēpt diagrammu, ja ir nepieciešama papildu vieta ekrānā, lai skatītu cilnes **Skaidras naudas pozīcija** saturu.

Cilnes **Skaidras naudas pozīcija** apakšējā daļa parāda detalizētu informāciju par pozīciju, skaidras naudas plūsmu, prognozētajiem maksājumiem un bankas kontu.

- Informācija režģī **Detalizēta informācija par pozīciju** ir trīs sadaļās: likviditātes kontu saraksts, to dokumentu saraksts, kas rada skaidras naudas ienākšanu, un dokumentu saraksts, kas rada skaidras naudas aizplūšanu. Režģī tiek parādītas arī skaidras naudas pozīcijas bilances. Pirmajam apskatāmajam periodam likviditātes kontu bilance ir sākuma bilance. Turpmākiem periodiem likviditātes kontu bilances tiek aprēķinātas, pamatojoties uz naudas ienākšanas pievienošanu un izejošās naudas plūsmu atņemšanu no iepriekšējiem periodiem. Lai skatītu detalizētu informāciju par darījumiem, kas veido bilanci, atlasiet saiti **Bilance**.
- Režģis **Naudas plūsma** rāda skaidras naudas ienākošo plūsmu, skaidras naudas izejošo plūsmu apkopojumu pa periodiem un to ietekmi uz likviditātes kontu bilancēm. Pirmajam periodam likviditātes kontu bilance ir sākuma bilance. Turpmākiem periodiem likviditātes kontu bilances tiek aprēķinātas, pamatojoties uz naudas ienākšanas pievienošanu un izejošās naudas plūsmu atņemšanu no iepriekšējiem periodiem.
- Režģis **Prognozētā bankas bilance** parāda paredzamās skaidras naudas ienākošās plūsmas un to ietekmi uz likviditātes kontiem.
- Režģis **Bankas konts** parāda sagaidāmās naudas ienākošās plūsmas un izejošās plūsmas ietekmi uz bankas bilanci.

Lai saglabātu un rediģētu skaidras naudas pozīciju, izveidojiet momentuzņēmumu. Lai iegūtu papildinformāciju par to, kā strādāt ar momentuzņēmumiem, skatiet [Pārskats par momentuzņēmumiem](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Detalizēta informācija par skaidras naudas pozīcijas spēju 

Funkcija Skaidras naudas pozīcija ietver šādu funkcionalitāti. 

- Skaidras naudas pozīcijas funkcija parāda kases plūsmu, balstoties uz sistēmā esošajiem dokumentiem, kā arī naudas ieplūdes un aizplūšanas rindām, kas importētas no ārējām sistēmām.
- Ļauj viegli integrēt naudas plūsmas datus no ārējām sistēmām Dynamics 365 finansēs. Skaidras naudas pozīcija var izmantot arī datu importēšanas/eksportēšanas struktūru. Šī struktūra atvieglo integrāciju ar Excel OData. Jūs varat kombinēt arī datus no vairākiem avotiem, lai izveidotu vispārēju skaidras naudas pozīcijas risinājumu.
- Iepazīstina ar programmējamo skaidras naudas pozīciju. Skaidras naudas pozīcija tiek izveidota, balstoties uz debitora maksājumu uzvedību, lai paredzētu, kad uzņēmums var gaidīt skaidras naudas pienākšanu kontos.
- Debitoru pasūtījumiem un rēķiniem debitoru maksājumu prognozēšanas AI funkcionalitāte tiek izmantota, lai noteiktu vēsturisko debitora maksājumu uzvedību, kad tiks maksāts pasūtījums vai rēķins.
- Kreditoru pasūtījumos un rēķinos tiek izmantots vidējais laiks starp nosūtīšanu un rēķinu un rēķina apmaksu katram kreditoram, lai noteiktu, kad kreditora pasūtījums vai rēķins tiks apmaksāts, veicot naudas izdevumu precīzāku.

Tas izveido precīzāku naudas plūsmas skatu, balstoties uz kasiera vēsturisko maksājumu uzvedību. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
