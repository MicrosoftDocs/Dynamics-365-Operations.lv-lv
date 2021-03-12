---
title: Sākumdatu inicializēšana jaunās Commerce vidēs
description: Šajā rakstā ir aprakstīti dati, kas tiek izveidoti Dynamics 365 Commerce inicializācijas procesa ietvaros.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8fd0b2743deab758538922f312853b622a512c0a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000749"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Sākumdatu inicializēšana jaunās Commerce vidēs

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīti dati, kas tiek izveidoti Dynamics 365 Commerce inicializācijas procesa ietvaros.

Pēc Commerce risinājuma izvietošanas, izmantojot portālu Microsoft Dynamics Lifecycle Services (LCS), ir jāinicializē Commerce konfigurācija, lai izveidotu pamata konfigurācijas datus.

> [!IMPORTANT]
> Pirms komercijas konfigurācijas inicializēšanas, pārliecinieties, ka esat norādījis valodu un pasta adresi katrai juridiskajai personai, kur tiks iestatīti veikali. Šī darbība ir jāveic katrai juridiskajai personai, kura tiks izmantota komercijai.

Lai inicializētu konfigurāciju, veiciet talāk norādītās darbības.

1. Palaidiet Commerce klientu.
2. Noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Headquarters iestatīšana** &gt; **Parametri** &gt; **Komercijas parameteri**.
3. Noklikšķiniet uz **Inicializēt**.

Inicializācija izveido šādus noklusējuma konfigurācijas datus:

- Commerce plānotāja darbi un apakšdarbi
- Komercijas kanāla shēma
- Commerce sadales grafiki
- Noklusējuma ekrāna izkārtojumu, kas ietver pogu rindas, attēlus un tēmas
- Informācija par laika joslu
- Pārdošanas punktu (POS) saderība
- POS atļaujas
- Kanālu pārskati
- Atribūta metadati
- Elementa validēšanas veidnes
- Commerce Data Exchange sesijas vēstures dzēšanas pakešuzdevums

Turklāt, Commerce datu bāzei ir iespējota reģistrācija, kas ir saistīta ar maksājumu karšu nozari (PCI).

> [!NOTE]
> Pastāv iespēja atsevišķi konfigurēt Commerce plānotāju. Šī opcija ļauj atiestatīt Commerce plānotāja konfigurāciju uz noklusētajiem iestatījumiem.

Pēc inicializēšanas pabeigšanas, jums ir jākonfigurē papildu komercijas dati. Daži piemēri:

- Komercijas parametri
- Komercijas plānotāja parametri
- Commerce kanāli.
- Reģistri un ierīces
- Preču klāsts
