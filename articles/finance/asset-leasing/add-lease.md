---
title: Nomas pievienošana vai kopēšana (priekšskatījums)
description: Šajā rakstā ir aprakstīts, kā izveidot jaunu nomas maksa, ievadot informāciju par to Pamatlīdzekļu izlaižot vai kopējot informāciju no esošās nomas.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880937"
---
# <a name="add-or-copy-leases-preview"></a>Nomas pievienošana vai kopēšana (priekšskatījums)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izveidot nomas no jauna Pamatlīdzekļu izlaižot, un arī kā izveidot nomu, kopējot esošo nomu. Nomas izveides process no nulles ietver informācijas ievadīšanu jaunajai nomai un pēc tam nomas grafika izveidošanu. Pēc tam, kad ir iestatīta vismaz viena noma, iespējams, uzskatīsiet par vieglāku kopēt informāciju no esošas nomas un pēc tam rediģēt šo informāciju pēc nepieciešamības, lai izveidotu jaunu nomu.

## <a name="create-a-lease"></a>Nomas izveide

Veiciet tālāk norādītās darbības, lai izveidotu nomu Līdzekļu nomā.

1. Lapā **Nomas kopsavilkums** darbību rūtī atlasiet **Jauns**.
2. Ievadiet informāciju par nomu. Obligāti aizpildāmajiem laukiem ir sarkana apmale.

Nomas maksājuma sākuma datums nevar būt agrāks par nomas sākuma datumu. Ja ievadāt nomas maksājuma sākuma datumu, kas ir pirms nomas sākuma datuma, tiks parādīts kļūdas ziņojums.

Pēc noklusējuma opcijas Sadalījuma maksājuma summa kopsavilkuma cilnē Vispārīgi, kas atrodas lapā Detalizēta informācija par nomu, tiek iestatīta uz Nē, **·** **·** **·** **·** **·** **ja opcija Atļaut maksājumu sadalījumu lapā Līdzekļu izlaižšanas parametri** ir iestatīta uz **Jā.** 

Ja opcija **Sadalījuma maksājuma summa** ir iestatīta uz **Jā**, lauks **Maksājuma** summa kopsavilkuma **cilnē Maksājumu grafiks ir** bloķēts. Tā tiks iestatīta uz maksājumu kopsummu, kas vēlāk ir ievadīta maksājumu **summas sadalījuma** katalogā.

Atlasiet **maksājuma summas sadalījumu**, lai atvērtu lapu, kurā varat pievienot informāciju par maksājumu tipiem. Poga **Pievienot kopsummas maksājuma summai** pārvietos kopsummas uz lauku **Maksājuma** summa.

> [!NOTE]
> Ja pievienojat informāciju **par maksājuma summu un pēc tam atlasāt taustiņu Esc**, **·** **ievadītās** summas netiks pievienotas laukam Maksājuma summa kopsavilkuma cilnē Maksājumu grafiks. Tā vietā tie tiks glabāti **maksājuma summas sadalījuma** dialoglodziņā. Ja vēlaties, lai dialoglodziņš rādītu kopējo summu, atlasiet kolonnu Summa, **atlasiet** un turiet to (vai noklikšķiniet ar peles labo pogu) un pēc tam atlasiet **Kopsumma šajā kolonnā**. 

Ar **pogu Kopēt** rindu tiks kopēts depozīts maksājuma sadalījums.

## <a name="create-a-lease-schedule"></a>Nomas grafika izveide

Pēc tam, kad esat pabeidzis ievadīt informāciju par nomu, veiciet tālāk norādītās darbības, lai izveidotu nomas grafiku.

> [!NOTE]
> Finanšu dimensijas var mainīties atkarībā no jebkurām pielāgotajām finanšu dimensijām.

1. Atlasiet **Izveidot grafikus**, lai ģenerētu nomas grāmatas. Nomas grāmatas ietver maksājumu, amortizācijas, nolietojuma un izdevumu grafikus.
2. Lai piekļūtu nomas grāmatām un skatītu jaunizveidotos grafikus, atlasiet cilni **Grāmatas**.

    Lapā **Grāmatas detalizēta informācija** ir parādīts, kā noma tiek uzskaitīta tai piešķirtajās grāmatās. No šejienes varat skatīt nomas grafikus.

    Maksājumu grafiks satur ievades no cilnes **Maksājumu grafika rindas**, kas atrodas lapā **Pievienot nomu**. Joprojām varat mainīt katra maksājuma summu un mainīgās izmaksas. Nomas saistības tiek aprēķinātas, pamatojoties uz modificēto maksājumu grafiku.

    > [!NOTE]
    > Nomas maksājuma sākuma datumam ir jābūt vienādam vai vēlākam par nomas sākuma datumu. Ja maksājuma sākuma datums ir agrāks par nomas sākuma datumu, tiks parādīts kļūdas ziņojums. 

4. Kad esat beidzis maksājumu grafika pārskatīšanu, atlasiet **Apstiprināt grafiku**. Pēc grafika apstiprināšanas noma vairs nav pieejama labošanai.

    > [!NOTE]
    > Sistēma automātiski aprēķina nomas termiņu no maksājumu grafika rindām lapā **Pievienot nomu**.
    >
    > Lai aprēķinātu nomas termiņu mēnešos, sistēma atrod starpību starp noteiktas maksājuma grafika rindas sākuma un beigu datumu. Pēc tam tā pāriet uz nākamo maksājumu grafika rindu un atkal atrod starpību. Visbeidzot sistēma saskaita visas summas, lai noteiktu nomas termiņu mēnešos.

5. Lai skatītu aprēķinātā perioda procentu izdevumus, atveriet lapu **Saistību amortizācijas grafiks**. Lai skatītu aprēķināto lineāro nolietojumu, atveriet lapu **Līdzekļu nolietojuma grafiks**.
6. Pēc tam, kad esat pabeidzis aprēķinātās summas pārskatīšanu, varat izveidot sākotnējās atzīšanas žurnāla ierakstu lapā **Sākotnējā atzīšana**. Jūs saņemat ziņojumu, kurā teikts, ka žurnāls ir izveidots.

    > [!NOTE]
    > Žurnāla ieraksts nebūs iegrāmatots Virsgrāmatā, kamēr manuāli neiegrāmatosiet ierakstu.

7. Lai pārskatītu piedāvāto sākotnējās atzīšanas ierakstu pirms grāmatošanas, atlasiet **Līdzekļu nomas žurnāls**.

    > [!NOTE]
    > Līdzekļu nomas žurnālu nevar izveidot manuāli. Tas tiek izveidots automātiski, izveidojot nomas grafikus.

8. Kad esat pabeidzis pārskatīt sākotnējo atzīšanas žurnāla ierakstu un esat gatavs to grāmatot, atlasiet **Grāmatot**, lai Virsgrāmatā atpazītu lietojuma tiesību līdzekli (LLT) un nomas saistības.

## <a name="copy-a-lease"></a>Nomas kopēšana

Izmantojot līdzekļu nomu, varat kopēt detalizētu informāciju par nomu, lai izveidotu jaunu nomu ar tādu pašu informāciju. Pēc tam varat mainīt nomas laukus, pirms izveidojat grafikus kopētajai nomai.

1. Lapā **Nomas kopsavilkums** atlasiet nomu, ko kopēt, un pēc tam darbību rūtī atlasiet **Kopēt nomu**.

    > [!NOTE]
    > Ja ir izslēgts parametrs **Manuāli** numuru sērijai, kas paredzēta nomas ID, nākamais numurs secībā tiek automātiski ģenerēts kā kopētās nomas ID. Ja parametrs **Manuāli** ir ieslēgts, saņemsiet ziņojumu, kas aicina ievadīt nomas ID pirms nomas kopēšanas turpināšanas.

2. Atlasiet **Kopēt**. Detalizēta informācija par nomu no atlasītās nomas tiek kopētas jaunā nomā. Pēc tam varat rediģēt detalizētu informāciju par jauno nomu, pirms to saglabājat, un izveidot nomas grafikus.

## <a name="asset-leasing-journal"></a>Līdzekļu nomas žurnāls

Visi žurnāla ieraksti, kas ir izveidoti Līdzekļu nomā, ir ietverti Līdzekļu nomas žurnālā. Lapā **Līdzekļu nomas žurnāls** (**Līdzekļu noma \> Žurnāla ieraksti \> Līdzekļu nomas žurnāls**) varat filtrēt pēc grāmatošanas statusa, skatīt konkrētus žurnāla ierakstus un dokumentus, un grāmatot neiegrāmatotos žurnāla ierakstus.

> [!NOTE]
> Līdzekļu nomas žurnālu nevar izveidot manuāli. Tas tiek izveidots automātiski, izveidojot nomas grafikus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
