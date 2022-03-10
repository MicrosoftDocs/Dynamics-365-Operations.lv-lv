---
title: Informācijas par nosūtīšanu iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt piegādes informāciju Kopējo izmaksu modulim.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 86350acfd056be2b43fc856e3b76b1632989a804
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579692"
---
# <a name="shipping-information-setup"></a>Informācijas par nosūtīšanu iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt piegādes informāciju **Kopējo izmaksu** modulim.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Preču apraksts

Preču apraksti palīdz identificēt reisu, nosūtīšanas konteineru vai preču folio un tajā uzglabātās preces. Preču aprakstu var atlasīt nosūtīšanas konteinerā vai folio galvenē.

Lai strādātu ar preču aprakstiem, dodieties uz **Kopējās izmaksas \> Nosūtīšanas informācijas iestatījumi \> Preču apraksts**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst preču aprakstu ierakstus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Preču apraksts | Ievadiet unikālu identifikācijas nosaukumu/numuru preču tipam, kas izmantos šo aprakstu. |
| Apraksts | Ievadiet šajā kategorijā preču tipa aprakstu. |

## <a name="vessels"></a><a name="vessels"></a>Kuģis

Kuģis ir unikāls nosūtīšanas vai kuģa nosaukums, ko izmanto kravu nosūtīšanas uzņēmums vai aģentūra. Kad izveidojat reisu, tam vienmēr ir jāatlasa vai jāievada kuģis. Ja bieži izmantojat vienu un to pašu, tad ir iespējams ātrāk un vieglāk izveidot jaunu reisu, izveidojot kuģa ierakstu katram no tiem, tādējādi ļaujot lietotājiem izvēlēties kuģi no saraksta, nevis katru reizi ievadīt nosaukumu vai numuru manuāli.

Lai strādātu ar nosūtīšanas ostām, dodieties uz sadaļu **Kopējās izmaksas \> Piegādes informācijas iestatīšana \> Kuģi**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ierakstus par kuģiem. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Kuģis | Ievadiet unikālu identifikācijas nosaukumu/numuru nosūtīšanai, kas tiks izmantota preču transportēšanai reisā. |
| Apraksts | Ievadiet kuģa aprakstu. Parasti šis apraksts identificē nosūtīšanas un nosūtīšanas uzņēmuma/aģenta nosaukumu. |
| Piegādes veids | Atlasiet kuģa izmantoto piegādes veidu (piemēram, _gaiss_, _okeāns_ vai _vilciens_). |

## <a name="exporters"></a>Eksportētāji

Katrs eksportētāja ieraksts norāda kreditoru vai eksportētāju, ko var definēt kā reisa kreditoru. Eksportētāju var saistīt ar reisu un izmantot pārskatiem.

Lai strādātu ar eksportētājiem, dodieties uz **Kopējās izmaksas \> Piegādes informācijas iestatīšana \> Eksportētāji**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ierakstus par eksportētājiem. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Eksportētājs | Ievadiet unikālu identifikācijas nosaukumu/numuru, lai eksportētu reisā transportējamās preces. |
| Apraksts | Ievadiet eksportētāja aprakstu. Parasti šis apraksts identificē pilnu nosūtīšanas uzņēmuma/aģenta nosaukumu. |

## <a name="commodity-codes"></a>Preču kodi

Preču kodi tiek lietoti, lai palīdzētu ar muitas identifikāciju un nodokļu likmju aprēķināšanu precēm reisā. Lai atlasītu preču kodus lapā **Izlaistās preces**, varat atlasīt preču kodus.

Lai strādātu ar preču kodiem, dodieties uz **Kopējās izmaksas \> Piegādes informācijas iestatīšana \> Preču kodi**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst preču kodu ierakstus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Preču kods | Ievadiet šī veida preces unikālo kodu. |
| Apraksts | Ievadiet preces tipa aprakstu. |

## <a name="customs-description"></a>Muitošanas apraksts

Muitas apraksti palīdz identificēt preces muitas vajadzībām. **Izlaisto preču** lapā vai pirkšanas pasūtījuma rindās varat atlasīt muitas aprakstu.

Lai strādātu ar muitas aprakstiem, dodieties uz **Kopējās izmaksas \> Nosūtīšanas informācijas iestatījumi \> Muitas apraksts**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst muitas aprakstu ierakstus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Muitošanas apraksts | Ievadiet šī veida muitas klasifikācijas unikālo kodu. Bieži šis kods ir oficiāls apraksts, ko muitas iestāde sniedz preču aprakstam un kvalitatīvai vērtībai. |
| Apraksts | Ievadiet muitas klasifikācijas aprakstu. |
