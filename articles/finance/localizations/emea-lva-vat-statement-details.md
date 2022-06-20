---
title: PVN deklarācijas informācija Latvijai
description: Šajā rakstā skaidrots, kā iestatīt PVN deklarāciju juridiskajām personām Latvijā.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 266864
ms.search.region: Latvia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 60a3abf5b741f9b09f6de6066a4d7e699522120d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880622"
---
# <a name="vat-statement-details-for-latvia"></a>PVN deklarācijas informācija Latvijai

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt PVN deklarāciju juridiskajām personām Latvijā.

Šajā rakstā ir iekļauta valstij/reģionam specifiskā informācija par pievienotās vērtības nodokļa (PVN) pārskata iestatīšanu tikai Latvijas juridiskajām personām. Papildinformāciju par PVN deklarāciju ieviešanu skatiet rakstā [VAT pārskati par Eiropu](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>PVN iestāžu iestatīšana
Lai PVN deklarāciju ģenerētu atbilstošajai nodokļu iestādei pieprasītajā formātā, ir jāiestata pārskata izkārtojums PVN iestādēm. Lapā **PVN iestādes** laukam **Pārskata izkārtojums** iestatiet vērtību **Noklusējums**. Atlasiet PVN iestādi tam PVN apmaksas periodam, kurš tiks izmantots PVN kodiem.

## <a name="set-up-sales-tax-reporting-codes"></a>Iestatīt PVN pārskatu kodus
Šajā piemērā ir parādīts, kā varat iestatīt PVN pārskatu kodus lapas **PVN kodi** kopsavilkuma cilnē **Pārskata iestatīšana**, lai ģenerētu PVN deklarāciju.

| PVN pārskata kods | Apraksts (angliski)                                                                    | Apraksts                                                                              | XML etiķetes nosaukums |
|--------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|--------------|
| 41                       | Standarta nodokļa likmes summa                                                                 | Ar standartlikmi apliekamie darījumi                                                     | R41          |
| 411                      | Iekšzemē veiktie darījumi, par kuriem nodokli maksā preču vai pakalpojumu saņēmējs      | Iekšzemē veiktie darījumi, par kuriem nodokli maksā preču vai pakalpojumu saņēmējs       | R411         |
| 42                       | Samazinātā nodokļu likmes summa                                                                  | Ar samazināto likmi apliekamie darījumi                                                  | R42          |
| 45                       | Uz Eiropas Savienības (ES) dalībvalstīm piegādātās preces                            | Uz ES dalībvalstīm piegādātās preces                                                     | R45          |
| 46                       | Pielāgotā pārdošanas summa krājumos                                                          | Ārpuskopienas preču piegādes muitas noliktavās un brīvajās zonās                         | R46          |
| 47                       | Uz ES dalībvalstīm piegādātie jaunie transportlīdzekļi                                                   | Uz ES dalībvalstīm piegādātie jaunie transportlīdzekļi                                   | R47          |
| 48                       | Provided services                                                                        | Par sniegtajiem pakalpojumiem                                                            | R48          |
| 481                      | Export goods                                                                             | Eksportētās preces                                                                       | R48\_1       |
| 482                      | Citās valstīs veiktie darījumi                                                         | Citās valstīs veiktie darījumi                                                           | R48\_2       |
| 49                       | Ar nodokli neapliekamie darījumi                                                                 | Ar PVN neapliekamie darījumi                                                             | R49          |
| 50                       | No ES dalībvalstīm saņemtās preces un pakalpojumi (standartlikme)                | No ES dalībvalstīm saņemtās preces un pakalpojumi (standartlikme)                        | R50          |
| 51                       | No ES dalībvalstīm saņemtās preces (samazinātā likme)                | No ES dalībvalstīm saņemtās preces (samazinātā likme)                                    | R51          |
| 54                       | Received services                                                                        | Par saņemtajiem pakalpojumiem                                                            | R54          |
| 61                       | Preces, kas importētās izmantošanai uzņēmuma ekonomiskajām aktivitātēm                                     | Par importētajām precēm                                                                  | R61          |
| 62                       | Iekšzemē pieejamās preces, kas paredzētas izmantošanai uzņēmuma ekonomiskajām aktivitātēm                        | Par precēm un pakalpojumiem iekšzemē                                                     | R62          |
| 63                       | Aprēķinātā nodokļa priekšapmaksas summa                                                                | Aprēķinātā PVN summa saskaņā ar likuma 92. panta pirmās daļas 4. punktu (izņemot 64. rindu) | R63          |
| 64                       | Aprēķinātā nodokļa priekšapmaksas summa par precēm un pakalpojumiem, kas saņemtas no ES dalībvalstīm | Aprēķinātā PVN summa par precēm un pakalpojumiem, kas saņemti no ES dalībvalstīm         | R64          |
| 65                       | Lauksaimniekiem izmaksātā kompensācija                                                         | Lauksaimniekiem izmaksātā kompensācija                                                   | R65          |
| 66                       | Nemaksājamā nodokļa priekšapmaksa                                                               | PVN summa, kas nav atskaitāma kā priekšnodoklis                                          | R66          |
| 67                       | Iepriekšējos taksācijas periodos aprēķinātās nodokļa summas samazinājums                                 | Iepriekšējos taksācijas periodos samaksai valsts budžetā aprēķinātā nodokļa samazinājums | R67          |
| 57                       | Iepriekšējos taksācijas periodos aprēķinātā priekšnodokļa samazinājuma summa                      | Iepriekšējos taksācijas periodos atskaitītā priekšnodokļa samazinājums                   | R57          |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Pārskatam konfigurēt elektronisko pārskatu modeli un formātu
Lai pārskatītu vai mainītu PVN deklarācijas konfigurāciju, lapas **Pārskatu konfigurācijas** modeļu sarakstā atlasiet vienumu **PVN deklarācijas modelis**. Pēc tam noklikšķiniet uz **Noformētājs**, lai šo modeli pārskatītu vai mainītu. Lai pārskatītu vai mainītu PVN deklarācijas formātu, lapā **Pārskatu konfigurācijas** atlasiet vienumu **PVN deklarācija (LV)** un pēc tam noklikšķiniet uz **Noformētājs**.

## <a name="generate-a-vat-statement"></a>Ģenerēt VAT deklarāciju
Lai ģenerētu PVN XML failu, lapā **PVN maksājumi** atlasiet vienu vai vairākus dokumentus un pēc tam noklikšķiniet uz **Eksportēt PVN XML failu**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]