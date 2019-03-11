---
title: Virsgrāmatas slēgšana perioda beigās
description: Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23d4b9b070a48e1964ecd6896afe071b564d1194
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "329302"
---
# <a name="close-the-general-ledger-at-period-end"></a>Virsgrāmatas slēgšana perioda beigās

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu. 

Virsgrāmatā varat izpildīt perioda vai gada slēgšanas procedūru. Slēgšanas procesi sagatavo sistēmu jaunajam periodam. Lai sistēmu sagatavotu jaunam gadam, ir jāpalaiž gada beigu slēgšanas process. Katrai organizācijai ir atšķirīgi procesi un darbības, kas jāveic perioda beigās. Dažas no neobligātajām darbībām perioda beigās ir šādas:

-   pabeigt visus uzdevumus visiem citiem moduļiem, piemēram, Debitoru parādi, Kreditori un Krājumi;
-   pārbaudīt, vai visi žurnāli ir grāmatoti;
-   palaist ārvalstu valūtas pārvērtēšanas procesu, lai ģenerētu nerealizētās peļņas vai zaudējumu summas;
-   nosegt transakcijas visos virsgrāmatas kontos;
-   apstrādāt visus nepieciešamos sadalījumus;
-   manuāli grāmatot perioda beigu korekcijas;
-   reģistrēt žurnālā darbības un pārskatīt pārskatu **Virsgrāmatas žurnāls**;
-   veikt konsolidāciju, izmantojot konsolidēšanas uzņēmumu vai finanšu pārskatu;
-   ģenerēt perioda beigu finanšu pārskatus, izmantojot finanšu pārskatus;
-   iestatīt virsgrāmatas periodiem statusu **Aizturēta**, lai tālāka grāmatošana netiek veikta. Lai atvieglotu kontroli, var arī ierobežot periodu noteiktai lietotāju grupai, kamēr tiek izpldītas perioda beigu darbības. Nav ieteicams periodiem iestatīt statusu **Neatgriezeniski slēgts**, jo slēgtu periodu nevar atvērt atkārtoti.

Lai kārtotu un izsekotu dažādu periodu beigu procesiem nepieciešamos uzdevumus, var lietot darbvietu Finanšu perioda slēgšana. 


Papildinformāciju skatiet tālāk norādītajās tēmās.
- [Finanšu perioda slēgšanas darbvieta](financial-period-close-workspace.md) 
- [Gada beigu slēgšana](Year-end-close.md)  
- [Masveida finanšu periodu slēgšana](tasks/mass-financial-period-close.md)




