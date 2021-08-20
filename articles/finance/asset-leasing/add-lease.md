---
title: Nomas pievienošana vai kopēšana (priekšskatījums)
description: Šajā tēmā aprakstīts, kā izveidot jaunu nomu, ievadot informāciju par to Līdzekļa nomā vai kopējot informāciju no esošas nomas.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2f2e6837819158688f3fd6bc28909a106a05a098ca917cab9032a2d0044042fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761330"
---
# <a name="add-or-copy-leases-preview"></a>Nomas pievienošana vai kopēšana (priekšskatījums)

[!include [banner](../includes/banner.md)]

Šajā tēmā paskaidrots, kā Līdzekļu nomā izveidot nomu no nulles un kā izveidot nomu, kopējot esošu nomu. Nomas izveides process no nulles ietver informācijas ievadīšanu jaunajai nomai un pēc tam nomas grafika izveidošanu. Pēc tam, kad ir iestatīta vismaz viena noma, iespējams, uzskatīsiet par vieglāku kopēt informāciju no esošas nomas un pēc tam rediģēt šo informāciju pēc nepieciešamības, lai izveidotu jaunu nomu.

## <a name="create-a-lease"></a>Nomas izveide

Veiciet tālāk norādītās darbības, lai izveidotu nomu Līdzekļu nomā.

1. Lapā **Nomas kopsavilkums** darbību rūtī atlasiet **Jauns**.
2. Ievadiet informāciju par nomu. Obligāti aizpildāmajiem laukiem ir sarkana apmale.

## <a name="create-a-lease-schedule"></a>Nomas grafika izveide

Pēc tam, kad esat pabeidzis ievadīt informāciju par nomu, veiciet tālāk norādītās darbības, lai izveidotu nomas grafiku.

> [!NOTE]
> Finanšu dimensijas var mainīties atkarībā no jebkurām pielāgotajām finanšu dimensijām.

1. Atlasiet **Izveidot grafikus**, lai ģenerētu nomas grāmatas. Nomas grāmatas ietver maksājumu, amortizācijas, nolietojuma un izdevumu grafikus.
2. Lai piekļūtu nomas grāmatām un skatītu jaunizveidotos grafikus, atlasiet cilni **Grāmatas**.

    Lapā **Grāmatas detalizēta informācija** ir parādīts, kā noma tiek uzskaitīta tai piešķirtajās grāmatās. No šejienes varat skatīt nomas grafikus.

    Maksājumu grafiks satur ievades no cilnes **Maksājumu grafika rindas**, kas atrodas lapā **Pievienot nomu**. Joprojām varat mainīt katra maksājuma summu un mainīgās izmaksas. Nomas saistības tiek aprēķinātas, pamatojoties uz modificēto maksājumu grafiku.

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