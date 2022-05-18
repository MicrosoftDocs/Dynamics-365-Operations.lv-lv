---
title: Divkāršās valūtas atbalsts nodokļiem
description: Šajā tēmā skaidrots, kā paplašināt divkāršas valūtu uzskaites funkciju nodokļu jomā, un ietekme uz nodokļu aprēķināšanu un grāmatošanu
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fcd5a3afb442d9c85aba12b7782cf09f88f0e51a
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713049"
---
# <a name="dual-currency-support-for-sales-tax"></a>Divkāršās valūtas atbalsts PVN
[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā paplašināt divkāršas valūtu uzskaites attiecībā uz PVN, un ietekme uz PVN aprēķiniem, grāmatošanu un apmaksu.

Dynamics 365 Finanšu dubultās valūtas līdzeklis tika ieviests versijā 8.1 (2018. gada oktobris). Tas maina veidu, kādā tiek aprēķināti uzskaites ieraksti pārskata valūtā.

Iepriekšējās versijās transakcijas tika konvertētas pārskata valūtā šādā secībā: 

- Transakcijas kopsumma tika aprēķināta transakcijas valūtā > Transakcijas summa tika konvertēta uzskaites valūtā > Uzskaites valūtas summa tika konvertēta pārskata valūtā

Pēc divkāršās valūtas funkcijas iespējošanas transakcijas tika konvertētas pārskata valūtā šādā secībā:

- Transakcijas valūtas summa > Pārskata valūtas summa

Lai iegūtu vairāk informācijas par divkāršo valūtu, lūdzu, skatiet [Divkāršā valūta](dual-currency.md).

Divkāršu valūtu atbalsta rezultātā ir pieejami divi jauni līdzekļi līdzekļu pārvaldībā: 

- PVN konvertēšana (jauns versijā 10.0.13)
- Ievadiet finanšu dimensijas realizētās valūtas korekcijas peļņas/zaudējumu kontos PVN segšanai (jauns versijā 10.0.17)

Divkāršu valūtu atbalsts PVN nodrošina, ka nodokļi tiek precīzi aprēķināti nodokļu valūtā un ka PVN apmaksas bilance tiek precīzi aprēķināta gan uzskaites valūtā, gan pārskata valūtā.

## <a name="sales-tax-conversion"></a>PVN konvertēšana

**PVN konvertēšanas** parametrs nodrošina divas opcijas nodokļa summas konvertēšanai no transakcijas valūtas nodokļa valūtā. 

- Uzskaites valūta: Ceļš būs "Summa transakcijas valūtā > Summa uzskaites valūtā > Summa nodokļa valūtā". Valūtas konvertēšanai tiks izmantots uzskaites valūtas maiņas kursa tips (konfigurēts Virsgrāmatas uzstādījumos).
- Pārskata valūta: Ceļš būs "Summa transakcijas valūtā > Summa pārskata valūtā > Summa nodokļa valūtā". Valūtas konvertēšanai tiks izmantots pārskata valūtas maiņas kursa tips (konfigurēts Virsgrāmatas uzstādījumos).

### <a name="example"></a>Paraugs

Vienkāršs piemērs, lai parādītu šo funkcionalitāti:

Valūtas iestatījums virsgrāmatai un nodoklim

| Transakcijas valūta | Uzskaites valūta | Pārskata valūta | Nodokļu valūta |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | USD                 | GBP                | GBP          |

Maiņas kurss

| No valūtas | Uz valūtu | Koeficients | Maiņas kurss |
| ------------- | ----------- | ------ | ------------- |
| EUR           | USD         | 1.      | 1.11          |
| EUR           | GBP         | 1.      | 0.83          |
| USD           | GBP         | 1.      | 0.75          |

Nodokļu summas aprēķināšana atšķirīgās parametru opcijās

Nodokļu summa = 100 EUR

| PVN konvertēšanas parametri | Transakcijas valūta (EUR) | Uzskaites valūta (USD) | Pārskata valūta (GBP) | Nodokļa valūta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Uzskaites valūta             | 100                        | 111                       | 83                       | **83.25**          |
| Pārskata valūta              | 100                        | 111                       | 83                       | **83**             |

Šo parametru var konfigurēt, pamatojoties uz atbilstības nepieciešamību no nodokļu iestādes.


### <a name="upgrade-consideration"></a>Atjaunināt apsvērumu

Šis līdzeklis attieksies tikai uz jaunām transakcijām. Nodokļa transakcijai, kas jau ir saglabāta tabulā TAXTRANS, bet nav apmaksāta, sistēma neveiks nodokļu summas pārrēķinu nodokļu valūtā, jo nav norādīts valūtas maiņas kurss ar grāmatošanas nodokļa laika punktu.

Lai novērstu iepriekšējo scenāriju, ieteicams mainīt šo parametra vērtību jaunā (tīrā) nodokļu apmaksas periodā, kas nesatur neapmaksātas nodokļu transakcijas. Lai mainītu šo vērtību nodokļa apmaksas perioda vidū, pirms šī parametra vērtības maiņas, lūdzu, palaidiet "nosegt un grāmatot PVN" programmu pašreizējam nodokļu apmaksas periodam.

Šis līdzeklis pievieno grāmatvedības ierakstus, kas precizē peļņu un zaudējumus no valūtas maiņas. Ieraksti tiek veikti realizētās valūtas korekcijas peļņas un zaudējumu kontos, kad pārdošanas nodokļa apmaksas laikā tiek veikta pārvērtēšana. Papildinformāciju skatiet sadaļā [Nodokļu segšanas automātiskā bilance pārskata valūtā](#tax-settlement-auto-balance-in-reporting-currency) vēlāk šajā tēmā.

> [!NOTE]
> Norēķinu laikā informācija par finanšu dimensijām tiek ņemta no PVN kontiem, kas ir bilances konti, un ievadīta valūtas korekcijas peļņas un zaudējumu kontos, kas ir peļņas un zaudējumu pārskata konti. Tā kā finanšu dimensiju vērtības ierobežojumi dažādiem bilances kontiem un peļņas un zaudējumu pārskata kontiem atšķiras, PVN nosegšanas un grāmatošanas procesā var rasties kļūda. Lai nemodificētu kontu struktūras, varat ieslēgt līdzekli "Aizpildīt finanšu dimensijas uz realizētajiem valūtas korekcijas peļņas/zaudējumu kontiem PVN segšanai". Šī iespēja piespiedīs finanšu dimensiju atvasināšanu uz valūtas korekcijas peļņas/zaudējumu kontiem. 

## <a name="track-reporting-currency-tax-amount"></a>Pārskata valūtas nodokļu summas izsekošana

Tika pievienoti trīs jauni lauki ar nodokļiem saistītām tabulām, lai izsekotu summas pārskata valūtā. Šie lauki atrodas tabulās TAXUNCOMMITTED un TAXTRANS:

- TaxAmountRep: nodokļu summa pārskata valūtā
- TaxAmountRep: bāzes summa pārskata valūtā
- TaxInCostPriceRep: neapliekamā summa pārskata valūtā

Nodokļiem, kas saglabāti tikai TAXUNCOMMITTED tabulā, bet vēl nav grāmatoti, sistēma pārrēķinās nodokļu summu pārskata valūtā grāmatošanas laikā un saglabās TAXTRANS tabulā.

Šajā laidienā netiks iekļautas izmaiņas pārskatos un veidlapās, kas uzrāda nodokļa summu pārskata valūtā. Izmaiņas pārskatos un veidlapās tiks nodrošinātas nākotnes laidienos.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Nodokļu apmaksas automātiskā bilance pārskata valūtā

Ja nodokļu apmaksa nav kāda iemesla dēļ iekļauta pārskata valūtas bilancē, piemēram, PVN konvertēšanas ceļš ir "Uzskaites valūta", vai ir radušās maiņas kursa izmaiņas vienā nodokļu apmaksas periodā, sistēma automātiski ģenerēs uzskaites ierakstus, lai koriģētu nodokļu summas novirzi un to kompensētu ar realizēto valūtas peļņas/zaudējumu kontu, kas ir konfigurēts Virsgrāmatas iestatījumos.

Izmantojot iepriekšējo piemēru, lai parādītu šo līdzekli, pieņemsim, ka tabulā TAXTRANS dati grāmatošanas laikā ir šādi.

| PVN konvertēšanas parametri | Transakcijas valūta (EUR) | Uzskaites valūta (USD) | Pārskata valūta (GBP) | Nodokļa valūta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Uzskaites valūta             | 100                        | 111                       | 83                       | **83.25**          |
| Pārskata valūta              | 100                        | 111                       | 83                       | **83**             |

Palaižot PVN apmaksas programmu mēneša beigās, uzskaites ieraksts būs šāds.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Scenārijs: PVN konvertēšana = "Uzskaites valūta"

| Galvenais konts           | Transakcijas valūta (GBP) | Uzskaites valūta (USD) | Pārskata valūta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Maksājamais / saņemamais nodoklis | -83.25                     | -111                      | -83.25                   |
| Nodokļa apmaksa         | 83.25                      | 111                       | 83.25                    |
| Realizētā peļņa / zaudējumi     | 0                          | 0                         | -0.25                    |
| Maksājamais / saņemamais nodoklis | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Scenārijs: PVN konvertēšana = "Pārskata valūta"


| Galvenais konts           | Transakcijas valūta (GBP) | Uzskaites valūta (USD) | Pārskata valūta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Maksājamais / saņemamais nodoklis | -83                        | -110.67                   | -83                      |
| Nodokļa apmaksa         | 83                         | 110.67                    | 83                       |
| Realizētā peļņa / zaudējumi     | 0                          | 0.33                      | 0                        |
| Maksājamais / saņemamais nodoklis | 0                          | -0.33                     | 0                        |



Papildinformāciju skatiet tālāk norādītajās tēmās.

- [Divkāršā valūta](dual-currency.md)
- [PVN pārskats](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
