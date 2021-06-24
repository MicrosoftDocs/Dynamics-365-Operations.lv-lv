---
title: Skaidras naudas pozīcija (priekšskatījums)
description: Šajā tēmā aprakstīts, kā skaidras naudas plūsmas prognozēšanas līdzeklis prognozē organizācijas skaidras naudas pozīciju noteiktam laikam. Tajā ir aprakstītas arī opcijas, kas pieejamas, lai parādītu prognozes dažādiem periodiem.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: b3b32bac436dc0be7ae4c072f4e560ad6d8b6d81
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186496"
---
# <a name="cash-position-preview"></a>Skaidras naudas pozīcija (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

#### <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
