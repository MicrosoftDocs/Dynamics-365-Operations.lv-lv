---
title: ER funkciju saraksts biznesa jomai specifiskā kategorijā
description: Šajā tēmā ir sniegta informācija par biznesa jomai specifiskām funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3d2055be7a755e35d0e88230e19038cf2d02ccc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748019"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>ER funkciju saraksts biznesa jomai specifiskā kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) domēnam specifiskas funkcijas var izmantot, lai veiktu aprēķinus un datu piekļuves pieprasījumus, kas ir specifiski Microsoft Dynamics 365 Finance ieviešanai. Šajā tēmā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija| Apraksts |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD10 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē vienu finanšu dimensijas ID, kas tiek ņemts no norādītās virknes. Norādītā virkne parāda visas dimensijas kā komatatdalītu ID sarakstu. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Šī funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītas naudas summas konvertēšanai no norādītās avota valūtas norādītajā mērķa valodā, izmantojot norādītā uzņēmuma iestatījumus norādītajā datumā. |
| [CurCredRef](er-functions-other-curcredref.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem. |
| [FA_Balance](er-functions-other-fabalance.md) | Šī funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa bilances datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un pārskata datumu. |
| [FA_Sum](er-functions-other-fasum.md) | Šī funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa summu datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un datumu periodu. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē juridiskās personas (uzņēmuma) kodu, kurā lietotājs šobrīd ir pieteicies. |
| [ISOCredRef](er-functions-other-isocredref.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Šī funkcija atgriež *Būla* vērtību **TRUE**, ja norādītā virkne attēlo derīgu starptautisko bankas konta numuru (IBAN). Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [Mod_97](er-functions-other-mod97.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD97 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē jauno numuru sērijas ģenerēto vērtību, pamatojoties uz norādīto numuru sēriju, tvērumu un tvēruma ID. Tvēruma ID ir vienāds ar uzņēmuma kodu, ko nodrošina konteksts, kurā tiek palaists ER formāts. |
| [RoundAmount](er-functions-other-roundamount.md) | Šī funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītās summas noapaļošanai uz norādītu ciparu aiz komata skaitu saskaņā ar norādīto noapaļošanas kārtulu. |
| [TableName2ID](er-functions-other-tablename2id.md) | Šī funkcija atgriež tabulas ID skaitlisko attēlojumu norādītajam tabulas nosaukumam kā *Vesela skaitļa* vērtību. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]