---
title: Kreditora rēķina elementi
description: Šajā rakstā ir sniegta informācija par kreditora rēķina elementiem, kas iespējo izmaksu tipu kodu konfigurēšanu iekšējām izmaksām vai ārēji iegūtām izmaksām.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 171b383e1549babd76fd18e4932436a66aa62cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873932"
---
# <a name="vendor-invoice-entities"></a>Kreditora rēķina elementi

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Zemes **izmaksu modulis** ļauj konfigurēt izmaksu tipu kodus iekšējām izmaksām vai ārēji iegūtām izmaksām. Ja izmaksas uzņēmumā nav ārējas, no pakalpojumu sniedzēja tiek gaidīts rēķins. Šis rēķins tiek apstrādāts kā rēķinu žurnāls, ko var saistīt ar reisu, un rēķina vērtību var sadalīt starp vienu vai vairākām reisa izmaksām.

Kreditora rēķina entītijas ļauj žurnāla rindas vērtību sadalīt pa vienu vai vairākām reisa izmaksām, kas koplieto vienu un to pašu izmaksu tipa kodu.

Izmaksas var sadalīt tikai tad, ja pastāv rēķinu žurnāla virsraksts un rēķinu žurnāla rindas.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Kreditora reisa izmaksu sadalīumi (ITMLedgerJournalCostLinesVoyagesEntity)

Kreditora reisa izmaksu sadalījuma datu elements ļauj kreditora rēķina rindu sadalīt pa vienu vai vairākām izmaksām, kas tiek piemērotas reisa izmaksu apgabalam. Šo funkcionalitāti atbalsta elements `ITMLedgerJournalCostLinesVoyagesEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piešķirtā summa | ITMLedgerJournalCostLines.Amount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu transakcijas rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla rindas numurs | ITMLedgerJournalCostLines.RefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla numurs | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jā** | Nē |
| Reiss | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Kreditora piegādes konteinera izmaksu sadalīumi (ITMLedgerJournalCostLinesContainersEntity)

Kreditora piegādes konteinera izmaksu sadalījuma datu elements ļauj kreditora rēķina rindu sadalīt pa vienu vai vairākām izmaksām, kas tiek piemērotas nosūtīšanas konteinera izmaksu apgabalam. Šo funkcionalitāti atbalsta elements `ITMLedgerJournalCostLinesContainersEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piešķirtā summa | ITMLedgerJournalCostLines.Amount | Skaitlis (32, 6) | Nē | Nē |
| Nosūtīšanas konteiners | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |
| Izmaksu transakcijas rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla rindas numurs | ITMLedgerJournalCostLines.RefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla numurs | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jā** | Nē |
| Reiss | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Kreditora folio izmaksu sadalīumi (ITMLedgerJournalCostLinesLleiosEntity)

Kreditora folio izmaksu sadalījuma datu elements ļauj kreditora rēķina rindu sadalīt starp vienu vai vairākām izmaksām, kas tiek piemērotas folio izmaksu apgabalam. Šo funkcionalitāti atbalsta elements `ITMLedgerJournalCostLinesFoliosEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piešķirtā summa | ITMLedgerJournalCostLines.Amount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu transakcijas rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Folio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |
| Žurnāla rindas numurs | ITMLedgerJournalCostLines.RefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla numurs | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jā** | Nē |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Kreditora pirkšanas pasūtījuma izmaksu sadalīumi (ITMLedgerJournalCostLinesPurchTableEntity)

Kreditora pirkšanas pasūtījuma izmaksu sadalījuma datu elements ļauj kreditora rēķina rindu sadalīt starp vienu vai vairākām izmaksām, kas tiek piemērotas pirkšanas pasūtījuma izmaksu apgabalam. Šo funkcionalitāti atbalsta elements `ITMLedgerJournalCostLinesPurchTableEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piešķirtā summa | ITMLedgerJournalCostLines.Amount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu transakcijas rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla rindas numurs | ITMLedgerJournalCostLines.RefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla numurs | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jā** | Nē |
| Pirkšanas pasūtījums | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Kreditora krājumu izmaksu sadalīumi (ITMLedgerJournalCostLinesPurchLineEntity)

Kreditora krājumu izmaksu sadalījuma datu elements ļauj kreditora rēķina rindu sadalīt pa vienu vai vairākām izmaksām, kas tiek piemērotas krājuma izmaksu apgabalam. Krājuma izmaksu zona sedz izmaksas pirkšanas pasūtījuma rindā. Šo funkcionalitāti atbalsta elements `ITMLedgerJournalCostLinesPurchLineEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piešķirtā summa | ITMLedgerJournalCostLines.Amount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu transakcijas rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla rindas numurs | ITMLedgerJournalCostLines.RefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla numurs | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jā** | Nē |
| Pirkšanas pasūtījums | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |
| Pirkšanas pasūtījuma rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Kreditora pārsūtīšanas pasūtījuma rindas izmaksu sadalīumi (ITMLedgerJournalCostLinesTransferLineEntity)

Kreditora pārsūtīšanas pasūtījuma rindas izmaksu iedalīšanas datu elements ļauj kreditora rēķina rindu sadalīt starp vienu vai vairākām izmaksām, kas tiek piemērotas pārsūtīšanas rindas izmaksu apgabalam. Šo funkcionalitāti atbalsta elements `ITMLedgerJournalCostLinesTransferLineEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piešķirtā summa | ITMLedgerJournalCostLines.Amount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu transakcijas rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla rindas numurs | ITMLedgerJournalCostLines.RefRecId | Skaitlis (32, 16) | **Jā** | Nē |
| Žurnāla numurs | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jā** | Nē |
| Pārsūtīšanas pasūtījums | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jā** | Nē |
| Pārsūtīšanas pasūtījuma rindas numurs | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitlis (32, 16) | **Jā** | Nē |

### <a name="reference-table"></a>Atsauču tabula

Reisa izmaksu rindām ir tieša saistība ar izmaksu darbības ierakstu. Šis ieraksts ietver atsauces **tabulas ID** vērtību. Šī vērtība ir unikāla katrai izmaksu zonai (reiss, pārvadāšanas konteiners utt.). Kad datiem, kas izveidoti, izmantojot datu elementus, ir atsauces uz noteiktiem tabulu numuriem, šie elementi tiek sadalīti, pamatojoties uz atsauces **tabulas ID** vērtībām.

Atsauces tabulas (`RefTableId`) un darbības tipa (`TransType`) vērtības ir netieši ietvertas atlasē vai nu zemes izmaksu pirkšanas rindai, vai zemes izmaksu pārsūtīšanas rindas elementam.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Kreditoru rēķinu žurnāla rindas (VendorInvoiceJournalLineEntity)

Pirms žurnāla rindas vērtību var piešķirt vienai vai vairākām izmaksām **zemes izmaksu modulī**, žurnāla rindai jābūt saistītai ar izmaksu apgabalu. Lai atbalstītu šo funkcionalitāti, **Landed izmaksu modulis** pievieno dažus jaunus laukus žurnālu rindu tabulai (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Kreditora rēķinu žurnāla rindas elementam pievienotie lauki

Šajā tabulā ir uzskaitīti lauki, ko zemes **izmaksu modulis** pievieno kreditora rēķina žurnāla rindas elementam (`VendorInvoiceJournalLineEntity`). Šie lauki iespējo sistēmu veidot žurnāla rindas un sadalīt tiem izmaksas.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Izmaksu apgabals | LedgerJournalTrans.ITMCostArea | Int | Nē | Nē |
| Izmaksu veida kods | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nē | Nē |

### <a name="mainoffset-account"></a>Galvenais/korespondējošais konts

Galveno/korespondējošo kontu rēķina žurnāla rindai, kas ir saistīta ar zemes izmaksu reisu, nosaka izmaksu tipa kods. Kad izmaksu tipa kods ir iekļauts rēķina žurnāla rindā, klīringa konts kodam tiks izmantots kā galvenais konts vai korespondējošais konts atkarībā no scenārija:

- **Vienas rindas žurnāls** – ja galvenais konts (citiem vārdiem, kreditora konts) ir definēts un tiek norādīts izmaksu tipa kods, šī izmaksu tipa koda klīringa konta vērtība tiks ievadīta korespondējošā kontā.
- **Vairāku rindu žurnāls** — ja galvenais konts nav definēts, bet tiek norādīts izmaksu tipa kods, šī izmaksu tipa koda klīringa konta vērtība tiks ievadīta galvenajā kontā. Žurnāla rinda, kas tiek kreditēts kreditoram, neļaus jums izveidot atsauci uz izmaksu tipa kodu.

## <a name="sequencing"></a>Secība

Tā kā žurnāla un žurnāla rindu tabulas ir atkarības, vispirms jāizveido reisa ieraksts. Reisa rindas var izveidot tikai pēc reisa, nosūtīšanas konteinera un sarakstu izveidošanas.

Lai piešķirtu reisa rēķinu, sistēmai ir jāapstrādā entītijas šādā secībā:

1. Rēķinu žurnāla virsraksts (`VendInvoiceJournalHeaderEntity`)
1. Rēķinu žurnāla rinda (`VendInvoiceJournalLineEntity`)
1. Kopējās zemes izmaksu sadalīumi (`ITMLedgerJournalEntities`)
