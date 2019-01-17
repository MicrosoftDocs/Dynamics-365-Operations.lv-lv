---
title: "Sākumdatu inicializēšana jaunās Retail vidēs"
description: "Šajā rakstā ir aprakstīti dati, kas tiek izveidoti kā daļa no inicializēšanas procesa programmatūrai Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="initialize-seed-data-in-new-retail-environments"></a>Sākumdatu inicializēšana jaunās Retail vidēs

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīti dati, kas tiek izveidoti kā daļa no inicializēšanas procesa programmatūrai Microsoft Dynamics 365 for Retail.

Pēc mazumtirdzniecības risinājuma izvietošanas caur Microsoft Dynamics Lifecycle Services (LCS), ir jāinicializē mazumtirdzniecības konfigurācija, lai izveidotu pamata konfigurācijas datus.

> [!IMPORTANT]
> Pirms mazumtirdzniecības konfigurācijas inicializēšanas, pārliecinieties, ka esat norādījis valodu un pasta adresi katrai juridiskajai personai, kur tiks iestatīti mazumtirdzniecības veikali. Šī darbība ir jāveic katrai juridiskajai personai, kura tiks izmantota mazumtirdzniecībai.

Lai inicializētu mazumtirdzniecības konfigurāciju, rīkojieties šādi.

1. Startējiet Dynamics 365 for Retail klientu.
2. Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Headquarters iestatīšana** &gt; **Parametri** &gt; **Mazumtirdzniecības parametri**.
3. Noklikšķiniet uz **Inicializēt**.

Inicializācija izveido šādus noklusējuma konfigurācijas datus:

- Mazumtirdzniecības plānotāja darbi un apakšdarbi
- Mazumtirdzniecības kanāla shēma
- Mazumtirdzniecības sadales grafiki
- Noklusējuma ekrāna izkārtojumu, kas ietver pogu rindas, attēlus un tēmas
- Informācija par laika joslu
- Pārdošanas punktu (POS) saderība
- POS atļaujas
- Kanālu pārskati
- Atribūta metadati
- Elementa validēšanas veidnes
- Pakešuzdevums Commerce Data Exchange sesijas vēstures dzēšanai

Turklāt Dynamics 365 for Retail datu bāzei ir iespējota reģistrēšana, kas ir saistīta ar maksājumu karšu nozari (PCI).

> [!NOTE]
> Pastāv iespēja atsevišķi konfigurēt mazumtirdzniecības plānotāju. Šī opcija ļauj atiestatīt mazumtirdzniecības plānotāja konfigurāciju uz noklusētajiem iestatījumiem.

Pēc inicializēšanas pabeigšanas, jums ir jākonfigurē papildu mazumtirdzniecības dati. Daži piemēri:

- Mazumtirdzniecības parametri
- Mazumtirdzniecības plānotāja parametri
- Mazumtirdzniecības kanāli
- Reģistri un ierīces
- Preču klāsts

