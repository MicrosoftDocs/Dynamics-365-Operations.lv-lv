---
title: "Virsgrāmatas slēgšana perioda beigās"
description: "Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a7b72dfa98758b14d303d09890bd46729b1cdbe9
ms.lasthandoff: 03/31/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Virsgrāmatas slēgšana perioda beigās

[!include[banner](../includes/banner.md)]


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

Lai kārtotu un izsekotu dažādu periodu beigu procesiem nepieciešamos uzdevumus, var lietot darbvietu Finanšu perioda slēgšana. Plašāku informāciju skatiet tēmā [Finanšu perioda slēgšanas darbvieta](financial-period-close-workspace.md) un [Gada beigu slēgšana](Year-end-close.md). 






