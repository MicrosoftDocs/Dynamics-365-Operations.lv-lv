---
title: Žurnālu rindu un dokumentu publicēšana programmā Excel
description: Šajā rakstā ir izskaidrots, kā ievadīt un publicēt virsgrāmatas žurnālu rindas Microsoft Excel. Tajā ir ietverta informācija par dažādajām veidnēm, ko varat izmantot atkarībā no ievadītās transakcijas veida.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb3e7a420f7f048ba93b6fadf5491e312e7ce33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872475"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>Žurnālu rindu un dokumentu publicēšana programmā Excel

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā ievadīt un publicēt virsgrāmatas žurnālu rindas Microsoft Excel. Tajā ir ietverta informācija par dažādajām veidnēm, ko varat izmantot atkarībā no ievadītās transakcijas veida.

Lietotāji var ievadīt un publicēt finanšu žurnālu rindas programmā Microsoft Excel. Pēc tam, kad lietotājs ir izveidojis žurnālu, izmantojot pogu **Atvērt rindas programmā Excel**, var skatīt pieejamās veidnes. Veidnes ir izstrādātas noteiktiem scenārijiem, taču žurnālā netiek atbalstītas visas konta veidu kombinācijas. Tālāk esošajā tabulā ir redzamas pieejamās veidnes un to atbalstītie kontu veidi.

| Veidne             | Atbalstītie kontu veidi | Piekļuve veidnei                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Virsgrāmatas žurnāla rindas     | Konts: Virsgrāmata, Debitors, Kreditors, Banka Korespondējošais konts: Virsgrāmata, Debitors, Kreditors, Banka Tiek atbalstīti starpuzņēmumu konti       | Virsgrāmatas žurnāls                                                                         |
| Rēķinu reģistrs         | Konts: Kreditors Korespondējošais konts: Virsgrāmata Starpuzņēmumu konti netiek atbalstīti                                                    | Parādu kreditoriem rēķinu reģistrs                                                                     |
| Rēķinu žurnāls          | Konti: Kreditors Korespondējošais konts: Virsgrāmata Tiek atbalstīti starpuzņēmumu konti                                                      | Kreditora rēķinu žurnāls                                                                      |
| Kreditora rēķins           |                                                                                                                         | Kreditora rēķins                                                                          |
| Debitoru rēķinu žurnāls | Konts: Debitors Korespondējošais konts: Virsgrāmata Tiek atbalstīti starpuzņēmumu konti                                                     | Virsgrāmatas žurnāls                                                                         |
| Brīva teksta rēķins        |                                                                                                                         | Lapā **Brīva teksta rēķins** noklikšķiniet uz **Atvērt programmā Excel** ( Microsoft Office ikona). |
| Pamatlīdzekļu žurnāls     | Virsgrāmatas, bankas, debitora vai kreditora līdzeklis. Starpuzņēmumu konti netiek atbalstīti.                                               | Pamatlīdzekļu žurnāls                                                                     |
| Kreditoru maksājumu žurnāls   | Konts: Kreditors Korespondējošais konts: Virsgrāmata, banka Tiek atbalstīti starpuzņēmumu konti                                                 | Kreditoru maksājumu žurnāls                                                                  |
| Debitoru maksājumu žurnāls | Konts: Debitors Korespondējošais konts: Virsgrāmata, Banka Tiek atbalstīti starpuzņēmumu konti                                               | Debitoru maksājumu žurnāls                                                                |
| Projekta izdevumu žurnāls  | Konts: Projekts, Virsgrāmata, Debitors, Kreditors Korespondējošais konts: Projekts, Virsgrāmata, Debitors, Kreditors Tiek atbalstīti starpuzņēmumu konti | Virsgrāmatas žurnāla izdevumi (Sadaļā Projektu vadība un uzskaite)                       |

Kad rindas tiek publicētas, tās tiek validētas, lai pārliecinātos, ka tās atbilst finanšu žurnālos iestatītajām kārtulām. Kad rindas ir publicētas, lietotāji var rediģēt vai grāmatot dokumentus no Dynamics 365 Finance. 

Lai pievienotu veidnei finanšu dimensijas, ir jāveic papildu izmaiņas. Papildinformāciju skatiet rakstā [Dimensiju pievienošana Microsoft Excel veidnei](../../fin-ops-core/dev-itpro/financial/add-dimensions-excel-templates.md). Pēc dimensiju pievienošanas elementam tās ir pieejamas Excel veidotājā un tās var pievienot veidnei.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
