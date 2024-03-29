---
title: Līdzekļa lietošanas tiesību nolietojuma reģistrēšana (priekšskatījums)
description: Šajā rakstā skaidrots, kā izveidot žurnāla ierakstu norakstīšanas, kas ir nepieciešama nomas maksai, kas tiek atpazīta organizācijas bilancē.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903281"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Līdzekļa lietošanas tiesību nolietojuma reģistrēšana (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Nomām, kas tiek atzītas organizācijas bilancē, lietošanas tiesību LLT tiek amortizēts reizi mēnesī. Šajā rakstā skaidrots, kā izveidot žurnāla ierakstu amortizācijai. Amortizācija debetē izdevumu Virsgrāmatas kontu un kreditē uzkrātā nolietojuma Virsgrāmatas kontu, pamatojoties uz jūsu grāmatošanas profila iestatījumiem un nomas tipu. Šos ierakstus var izveidot katrai nomai, vai arī tos var izveidot vairākām nomām, izmantojot žurnāla pakešuzdevuma funkcionalitāti.

## <a name="asset-depreciation-schedule"></a>Līdzekļu nolietojuma grafiks

1. Lapā **Nomas kopsavilkums** atlasiet nomu. Pēc tam atlasiet **Grāmatas \> Līdzekļa nolietojuma grafiks**, lai atvērtu lapu **Līdzekļu nolietojuma grafiks**.

    LLT nolietojuma izdevumu žurnāla ieraksts ir balstīts uz summu kolonnā **Nolietojuma izdevumi**. Piemēram, grāmatvedības [standarta saskaņotības norādījumos skatiet](#calculation-of-rou-asset-amortization-expense-for-finance-leases) finanšu nomas finanšu nomas nolietojuma izmaksu aprēķinu tālāk šajā rakstā.
    
2. Atlasiet nolietojuma periodu un pēc tam atlasiet **Izveidot žurnālu**. Tiek parādīts ziņojums, ka tika izveidots žurnāls, kas tiks izmantots nolietojuma reģistrēšanai.
3. Atlasiet **Žurnāli \> Līdzekļu nomas žurnāli**, lai atvērtu lapu **Līdzekļu nomas žurnāls**, kur varat skatīt izveidoto nolietojuma izdevumu žurnāla ierakstu.

   Sistēma bloķē noteiktus finanšu laukus, lai novērstu novirzes starp darbībām un grafikiem. Dažos bloķētos laukos ir iekļauts: **Konts**, **Summa**, **Finanšu dimensijas**, **Valūta** un **Darbības tips**. Turklāt nevarēsit pievienot vai dzēst žurnāla ierakstu rindas jebkurās Pamatlīdzekļu izlaižot žurnāla ierakstos, jo tas var izraisīt novirzes starp grafikiem un darbībām.

4. Atlasiet žurnāla ierakstu un pēc tam atlasiet **Grāmatot**, lai ierakstītu nolietojuma ierakstu Virsgrāmatā.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>LLT amortizācijas izdevumu aprēķins operatīvajām nomām

Operatīvās nomas nolietojuma izdevumi tiek aprēķināti kā starpība starp ikmēneša taisnvirziena nomas izdevumiem un ikmēneša procentu izdevumiem par nomas saistībām saskaņā ar uzskaites standartu kodifikācijas tēmu 842 (ASC 842), kas ir standarts vispārpieņemtajos uzskaites principos ASV (US GAAP). Taisnvirziena nomas izdevumus aprēķina kā visu nomas maksājumu summu, kas dalīta ar nomas termiņu mēnešos. (Nomas maksājumu summa ietver visas priekšapmaksas, sākotnējās tiešās izmaksas, demontāžas izmaksas un nomas stimulus.) Šajā tabulā ir parādīts operatīvās nomas amortizācijas izdevumu piemērs.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>LLT amortizācijas izdevumu piemērs operatīvajām nomām

| Lauks                                          | Vērtība       |
|------------------------------------------------|-------------|
| Maksājuma summa                                 | 1000       |
| Maksājumu biežums                              | Mēnesis     |
| Nomas termiņš (mēnešos)                            | 24          |
| Kopējie nomas maksājumi                           | 24,000      |
| Salīdzināmā aizņēmuma procentu likme                     | 5%          |
| Gada maksājuma veids                                   | Atlikušais gada maksājums |
| Pievienošanas intervāls                           | Mēnesis     |
| Nākotnes minimālo nomas maksājumu pašreizējā vērtība | 22,888.87   |

Kā iepriekš minēts, taisnvirziena nomas izdevumus aprēķina kā visu maksājumu summu, kas dalīta ar nomas termiņu. Sistēma automātiski aprēķina ikmēneša procentu izdevumus saistību amortizācijas grafikā. Procentu izdevumi tiek aprēķināti, izmantojot efektīvo procentu likmes metodi. Sistēma izmantos tiešās nomas izmaksas, lai atņemtu procentu izdevumus katram mēnesim. Vērtība tiek izmantota, lai samazinātu LLT.

| mēnesis; | Lineārās nomas izmaksas | Maksājamie procenti                        | LLT amortizācijas izdevumu aprēķins |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24 000 ÷ 24) = 1000,00 | (22 888,87 – 1000) × (5% ÷ 12) = 91,20 | 1000 – 91,20 = 908,80                        |
| 2     | (24 000 ÷ 24) = 1000,00 | (21 980,08 – 1000) × (5% ÷ 12) = 87,42 | 1000 – 87,42 = 912,58                        |
| 3     | (24 000 ÷ 24) = 1000,00 | (21 067,49 – 1000) × (5% ÷ 12) = 83,62 | 1000 – 83,62 = 916,39                        |

> [!NOTE]
> Saskaņā ar ASC 842, LLT nolietojums operatīvai nomai tiek klasificēts kā nomas izdevumi peļņas vai zaudējumu aprēķinā. Redzamībai tlīdzekļu noma apraksta ierakstu kā LLT nolietojumu. Tomēr debeta ieraksts ir jāpiešķir operatīvās nomas izdevumu kontam, un kredīta ieraksts ir jāpiešķir tieši operatīvas nomas LLT. Nomas parametros var norādīt, ka uzkrātā nolietojuma kontā LLT līdzekļiem ir jāizveido kredīta ieraksti.

Ja noma ir klasificēta kā operācijas noma, ikmēneša nolietojums pēc pasliktināšanās tiks aprēķināts, izmantojot lineāro nolietojumu.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>LLT amortizācijas izdevumu aprēķins finanšu nomām

Nomām, kam ir finanšu klasifikācija, sistēma aprēķina LLT nolietojumu, pamatojoties uz lineāro. Tāpēc nolietojuma izdevumi būs vienādi katram mēnesim.

Saskaņā ar starptautisko finanšu pārskatu standartu 16 (IFRS 16) un ASC 842, līdzeklis tiks amortizēts vai nu nomas termiņa vai līdzekļa lietderīgās lietošanas laikā atkarībā no tā, kas ir mazāks. Turklāt, ja **nomas īpašumtiesību** parametrs ir aktivizēts nomai, nomas maksa automātiski tiks nolietota līdzekļa lietderīgās lietošanas laikā.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>LLT amortizācijas izdevumu piemērs finanšu nomām

| Lauks                                | Vērtība                                   |
|--------------------------------------|-----------------------------------------|
| Līdzekļa lietošanas tiesību bilances sākums | 22,889.87                               |
| Nomas termiņš (mēnešos)                  | 24                                      |
| Līdzekļa lietderīgās lietošanas laiks (mēnešos)           | 36                                      |
| mēnesis;                                | Līdzekļa lietošanas tiesību amortizācijas izdevumi |
| 1                                    | 22 889,87 ÷ 24 = 953,74                 |
| 2                                    | 22 889,87 ÷ 24 = 953,74                 |
| 3                                    | 22 889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
