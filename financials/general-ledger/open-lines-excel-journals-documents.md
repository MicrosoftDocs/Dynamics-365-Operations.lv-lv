---
title: "Publicētu žurnāla rindās un dokumentus no Excel"
description: "Šajā tēmā izskaidrots, kā ievadīt un publicēt rindas Virsgrāmatas žurnālos no programmas Microsoft Excel. Tas ietver informāciju par dažādām veidnes, kuras var izmantot, atkarībā no tā, kāda veida darbības, kas jūs ievadot."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publicētu žurnāla rindās un dokumentus no Excel

Šajā tēmā izskaidrots, kā ievadīt un publicēt rindas Virsgrāmatas žurnālos no programmas Microsoft Excel. Tas ietver informāciju par dažādām veidnes, kuras var izmantot, atkarībā no tā, kāda veida darbības, kas jūs ievadot.

Lietotāji var ievadīt un publicēt finanšu žurnālos no programmas Microsoft Excel rindas. Pēc tam, kad lietotājs izveido žurnāla **līnijas atvēršana programmā Excel** pogas, tiek parādīts veidnes, kas pieejamas. Veidnes ir paredzētas, lai atbalstītu noteiktu scenāriju, tomēr ne katra konta tipu kombinācija tiek atbalstīta žurnālā. Šajā tabulā apskatāms, veidnēm, kas pieejamas un kontu tipiem, kas tās atbalsta.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Atbalstīto kontu tipi**                                                                                             | **Kā piekļūt veidni**                                                          |
| Virsgrāmatas žurnāla rindas     | Konts: Virsgrāmatas, klientu, piegādātāju, bankas korespondējošais konts: Virsgrāmatas, klientu, piegādātāju, bankas starpuzņēmumu tiek atbalstīts.       | Virsgrāmatas žurnāls                                                                         |
| Rēķinu reģistrs         | Konts: Kreditora korespondējošais konts: starpuzņēmumu virsgrāmatu nav atbalstīts.                                                    | Kreditoru rēķinu reģistrs                                                                     |
| Rēķinu žurnāls          | Konti: Kreditora korespondējošais konts: starpuzņēmumu Virsgrāmatas tiek atbalstīts.                                                      | Kreditora rēķinu žurnāls                                                                      |
| Kreditora rēķins           |                                                                                                                         | Kreditora rēķins                                                                          |
| Debitoru rēķinu žurnāls | Konts: Klientu korespondējošais konts: starpuzņēmumu Virsgrāmatas tiek atbalstīts.                                                     | Virsgrāmatas žurnāls                                                                         |
| Brīva teksta rēķins        |                                                                                                                         | Par **brīvā teksta rēķina** lapu, noklikšķiniet uz **atvērta programmā Excel** (Microsoft Office ikonu). |
| Pamatlīdzekļu žurnāls     | Pamatlīdzeklis, lai grāmatas, bankas, klientu vai piegādātāju. Starpuzņēmumu vai nav atbalstīta.                                               | Pamatlīdzekļu žurnāls                                                                     |
| Kreditoru maksājumu žurnāls   | Konts: Kreditora korespondējošais konts: grāmatas, bankas starpuzņēmumu tiek atbalstīts.                                                 | Kreditoru maksājumu žurnāls                                                                  |
| Debitoru maksājumu žurnāls | Konts: Klientu korespondējošais konts: grāmatas, bankas starpuzņēmumu tiek atbalstīts.                                               | Debitoru maksājumu žurnāls                                                                |
| Projekta izdevumu žurnāls  | Konts: Projektu Virsgrāmatas, klientu, kreditora korespondējošais konts: tiek atbalstīts projekts, Virsgrāmatas, klientu, piegādātāju starpuzņēmumu. | Virsgrāmatas žurnāla izdevumu (saskaņā ar projekta vadības un grāmatvedības)                       |

Publicējot līnijas, tie tiek pārbaudīti, lai pārliecinātos, ka tās atbilst noteikumiem, kas iestatīti finanšu žurnālos. Pēc tam, kad ir publicētas līnijām, lietotāji var rediģēt vai grāmatot dokumentus no Microsoft Dynamics 365 operācijām. 

Lai pievienotu veidni finanšu dimensijas, nepieciešami papildu izmaiņas. Lai iegūtu papildu informāciju, skatiet [Microsoft Excel veidnei pievienotu dimensijas](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Pēc dimensijām tiek pievienoti entītijas, tie ir pieejami programmā Excel dizainers un var pievienot veidnei.




