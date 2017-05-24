---
title: "Detalizētās bankas darbību saskaņošanas pārskats"
description: "Šajā rakstā ir aprakstīta detalizētās bankas darbību saskaņošanas procesa plūsma. Detalizētās bankas darbību saskaņošanas līdzeklis jums ļauj importēt bankas izrakstus, kurus var automātiski saskaņot bankas transakciju ietvaros."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6977cb3b315a90b504fc6748d2a4d02854a9d5ef
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Detalizētās bankas darbību saskaņošanas pārskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīta detalizētās bankas darbību saskaņošanas procesa plūsma. Detalizētās bankas darbību saskaņošanas līdzeklis jums ļauj importēt bankas izrakstus, kurus var automātiski saskaņot bankas transakciju ietvaros.

Detalizētās bankas darbību saskaņošanas funkcija ļauj importēt banku izrakstus. Pēc tam importēto bankas izrakstu var automātiski saskaņot no bankas transakciju vides. Šeit aprakstīti soļi detalizētās bankas darbību saskaņošanas plūsmā.

1.  Iestatiet bankas izraksta importēšanu.
    -   Importējiet bankas izrakstus, izmantojot datu elementu struktūru.
    -   Ir iebūvēti trīs tipiski bankas izrakstu formāti: ISO20022, BAI2 un MT940.
    -   Šī funkcionalitāte var tikt paplašināta uz jebkuru formātu.

2.  Iestatiet numuru sēriju, kuru lietot detalizētajai bankas darbību saskaņošanai un definējiet bankas darbību saskaņošanas atbilstības kārtulas.
    -   Saskaņošanas atbilstības kārtula ir kritēriju kopa, ko izmanto, lai saskaņošanas procesa laikā filtrētu bankas izrakstu rindas un Microsoft Dynamics 365 for Operations bankas transakciju rindas. Atkarībā no jūsu biznesa prakses varat iestatīt vairākas atbilstības kārtulas, lai automatizētu un optimizētu saskaņošanas procesu.

3.  Saskaņojiet bankas izrakstus ar Dynamics 365 for Operations bankas transakcijām.
    -   Veiciet automātisku atbilstības noteikšanu un saskaņošanas žurnālu izveidi.
    -   Bankas izrakstus un Dynamics 365 for Operations banku transakcijas varat apskatīt vienu otram līdzās.
    -   Automātiski grāmatojiet Dynamics 365 for Operations bankas transakcijas, ja tās ir redzamas bankas izrakstā, bet nav redzamas programmā Dynamics 365 for Operations.
    -   Izveidojiet saskaņošanas paziņojumu.





