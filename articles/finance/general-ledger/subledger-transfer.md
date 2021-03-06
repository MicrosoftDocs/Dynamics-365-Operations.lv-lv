---
title: Pārsūtīt apakšgrāmatu uz Virsgrāmatu
description: Šajā tēmā ir aprakstītas Microsoft Dynamics 365 Finance iespējas, kas saistītas ar apakšgrāmatas pārvirzīšanu virsgrāmatā.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897508"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Pārsūtīt apakšgrāmatu uz Virsgrāmatu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas Microsoft Dynamics 365 Finance iespējas, kas attiecas uz apakšgrāmatas žurnāla ierakstu partiju pārsūtīšanas kārtulām.

Versijā 8.1 tika veiktas izmaiņas, lai varētu pārsūtīt kārtulas, kas novecināja **sinhrono** opciju. Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi programmai Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Apakšgrāmatas partiju pārsūtīšanai ir pieejamas šādas opcijas. 

 - Asinhrons — šī opcija nekavējoties plāno apakšgrāmatas uzskaites ierakstu pārsūtīšanu uz Virsgrāmatu. Virsgrāmatas dokuments tiks ierakstīts, tiklīdz būs brīvi resursi, lai apstrādātu šo pieprasījumu serverī. 

- Plānotā partija — šī opcija pievienos apakšgrāmatas uzskaites ierakstus, kas tiek pārsūtīti uz apstrādes rindu virsgrāmatā, kur ieraksti tiek apstrādāti pasūtījuma saņemšanas laikā. Virsgrāmatas dokuments tiks ierakstīts plānotajā laikā, ja būs brīvi resursi, lai apstrādātu šo pakešuzdevumu serverī. 
 
Versijā 10.0.8 tika veikti uzlabojumi, lai uzlabotu asinhronās opcijas veiktspēju. Šis līdzeklis ir iespējots zem līdzekļa nosaukuma **Apakšgrāmatas pārsūtīšana uz Virsgrāmatas veiktspējas optimizāciju**. 
 
Šī funkcionalitāte uzlabo datu pārsūtīšanu no apakšgrāmatas uz virsgrāmatu. Tas ļauj procesam būt efektīvākam, un tas grupē kopā mazāku darbību kopas, ko pārsūtīt. Tas ļauj efektīvāk izmantot pakešu serveri. Šai funkcionalitātei nepieciešams, ka pakešu serveris ir iestatīts, tiešsaistē un funkcionējošs, lai asinhronās pārsūtīšanas opcija darbotos. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]