---
title: "PVN pārskata detaļas Latvija"
description: "Šajā tēmā ir paskaidrots, kā iestatīt PVN deklarācijas juridiskajām personām Latvija."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266864
ms.assetid: 40104afc-cbce-4f03-9318-7d0599bb1323
ms.search.region: Latvia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: 04b5aba27fd4cb8eb0c11f56b06ee787bc55b7cd
ms.lasthandoff: 03/31/2017


---

# <a name="vat-statement-details-for-latvia"></a>PVN pārskata detaļas Latvija

Šajā tēmā ir paskaidrots, kā iestatīt PVN deklarācijas juridiskajām personām Latvija.

Šī tēma ietver valsts/reģiona specifisko informāciju par iestatījumu pievienotās vērtības nodokļa (PVN) deklarācijas juridiskajām personām Latvija tikai. Plašāku informāciju par PVN deklarācijas īstenošanu, sk [PVN atskaišu](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>Nodokļu iestāžu iestatīšana
Radīt PVN deklarāciju attiecīgo nodokļu iestādes nepieciešamajā formātā, ir jāuzstāda PVN iestādes atskaites izkārtojumu. Par **PVN iestādēm** lapa, kas **atskaites izkārtojuma** lauku, lai **Default**. Atlasiet pašu PVN iestādi, kas tiks izmantots PVN kodus PVN apmaksas periodam.

## <a name="set-up-sales-tax-reporting-codes"></a>Iestatīt PVN pārskatu kodus
Lūk, piemērs, kas parāda, kā var iestatīt PVN pārskatu kodi par **atskaites uzstādījumus** FastTab, **PVN kodus** lapu, lai izveidotu PVN deklarācijas.

| PVN pārskata kods | Apraksts (angļu valodā)                                                                    | apraksts                                                                              | XML tagu nosaukums |
|--------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|--------------|
| 41                       | Standarta likmes nodokļa summa                                                                 | Ar standartlikmi apliekamie darījumi                                                     | R41          |
| 411                      | Preču vai pakalpojumu saņēmējs maksā nodokli darījumiem vietējā tirgū      | Iekšzemē veiktie darījumi, par kuriem nodokli maksā preču vai pakalpojumu saņēmējs       | R411         |
| 42                       | Samazināta nodokļa likme                                                                  | Ar samazināto likmi apliekamie darījumi                                                  | R42          |
| 45                       | Preces, kas tiek piegādāti Eiropas Savienības (ES) dalībvalstu                            | Uz ES dalībvalstīm piegādātās preces                                                     | R45          |
| 46                       | Pielāgotā pārdošanas summa krājumos                                                          | Ārpuskopienas preču piegādes tās noliktavās un brīvajās zonās                         | R46          |
| 47                       | ES valstīs piegādā jaunus transportlīdzekļus                                                   | Uz ES dalībvalstīm piegādātie jaunie transportlīdzekļi                                   | R47          |
| 48                       | Sniegtie pakalpojumi                                                                        | Par sniegtajiem pakalpojumiem                                                            | R48          |
| 481                      | Eksporta preču                                                                             | Eksportētās preces                                                                       | R48\_1       |
| 482                      | Darbības citās valstīs                                                         | Citās valstīs veiktie darījumi                                                           | R48\_2       |
| 49                       | Ar nodokli neapliekamie darījumi                                                                 | Ar PVN neapliekamie darījumi                                                             | R49          |
| 50                       | Precēm un pakalpojumiem, kas saņemti no ES dalībvalstīm (standarta likme)                | No ES dalībvalstīm saņemtās preces un pakalpojumi ("standartlikme")                        | R50          |
| 51                       | Precēm un pakalpojumiem, kas saņemti no ES dalībvalstīm (samazinātā likme)                | No ES dalībvalstīm saņemtās preces (samazinātā likme)                                    | R51          |
| 54                       | Saņemtie pakalpojumi                                                                        | Par saņemtajiem pakalpojumiem                                                            | R54          |
| 61                       | Ievestās preces uzņēmuma saimnieciskās darbības                                     | Par importētajām precēm                                                                  | R61          |
| 62                       | Precēm un pakalpojumiem par uzņēmuma saimniecisko darbību iekšzemē                        | Par precēm un pakalpojumiem iekšzemē                                                     | R62          |
| 63                       | Aprēķinātā nodokļa priekšapmaksa                                                                | Aprēķinātā PVN summa saskaņā ar likuma 92. panta pirmās daļas 4. punktu (izņemot 64.rindu) | R63          |
| 64                       | Aprēķinātas nodokļa priekšapmaksa par precēm un pakalpojumiem, kas saņemti no ES dalībvalstīm | Aprēķinātā PVN summa nominālvērtība precēm un pakalpojumiem, kas saņemti no ES dalībvalstīm         | R64          |
| 65                       | Kompensācijas lauksaimniekiem                                                         | Lauksaimniekiem izmaksātā kompensācija                                                   | R65          |
| 66                       | Nemaksājamā nodokļa priekšapmaksa                                                               | PVN summa, kas nav atskaitāma kā priekšnodoklis                                          | R66          |
| 67                       | Nodokļa summas samazinājumu aprēķina, iepriekšējo periodu nodokļu                                 | Iepriekšējos taksācijas periodos samaksai valsts budžetā aprēķinātā nodokļa samazinājums | R67          |
| 57                       | Aprēķinātais priekšapmaksas nodokļu summas samazināšanu, iepriekšējo periodu nodokļu                      | Iepriekšējos taksācijas periodos atskaitītā priekšnodokļa samazinājums                   | R57          |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Konfigurēt elektroniskās ziņošanas modeli un pārskata formātu
Pārskatīt vai mainīt PVN pārskata konfigurāciju uz **atskaišu konfigurācijas** lapu, atlasiet **PVN deklarācijas paraugs** modeļu sarakstā. Noklikšķiniet uz **Designer** pārskatīt vai mainīt modeli. Pārskatīt vai mainīt PVN pārskata formāts, uz **atskaišu konfigurācijas** lapu, atlasiet **PVN deklarācijā (LV)**, un pēc tam noklikšķiniet uz **Designer**.

## <a name="generate-a-vat-statement"></a>Veidot PVN deklarācijas
Radīt PVN XML failu, par **PVN maksājumiem** lapu, atlasiet vienu vai vairākus dokumentus un pēc tam noklikšķiniet uz **PVN eksportēt XML failā**.


