---
title: "Inicializēt sākumdatus jaunā Retail vidē"
description: "Šajā rakstā ir aprakstīti dati, kas tiek izveidoti kā daļa no inicializēšanas procesa programmatūrai Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Inicializēt sākumdatus jaunā Retail vidē

[!include[banner](includes/banner.md)]


Šajā rakstā ir aprakstīti dati, kas tiek izveidoti kā daļa no inicializēšanas procesa programmatūrai Microsoft Dynamics 365 for Operations - Retail.

Pēc mazumtirdzniecības risinājuma izvietošanas caur Microsoft Dynamics Lifecycle Services (LCS), ir jāinicializē mazumtirdzniecības konfigurācija, lai izveidotu pamata konfigurācijas datus. **Svarīgi:** pirms inicializēt mazumtirdzniecības konfigurāciju, pārliecinieties, ka esat norādījis valodu un pasta adresi katrai juridiskajai personai, kur tiks iestatīti mazumtirdzniecības veikali. Šī darbība ir jāveic katrai juridiskajai personai, kura tiks izmantota mazumtirdzniecībai. Lai inicializētu mazumtirdzniecības konfigurāciju, rīkojieties šādi.

1.  Startējiet Dynamics 365 for Operations klientu.
2.  Noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Headquarters iestatīšana** &gt; **Parametri** &gt; **Mazumtirdzniecības parametri**.
3.  Noklikšķiniet uz **Inicializēt**.

Inicializācija izveido šādus noklusējuma konfigurācijas datus:

-   Mazumtirdzniecības plānotāja darbi un apakšdarbi
-   Mazumtirdzniecības kanāla shēma
-   Mazumtirdzniecības sadales grafiki
-   Noklusējuma ekrāna izkārtojumu, kas ietver pogu rindas, attēlus un tēmas
-   Informācija par laika joslu
-   Pārdošanas punktu (POS) saderība
-   POS atļaujas
-   Kanālu pārskati
-   Atribūta metadati
-   Elementa validēšanas veidnes
-   Pakešuzdevums Commerce Data Exchange sesijas vēstures dzēšanai

Turklāt Dynamics 365 for Operations datu bāzei ir iespējota reģistrēšana, kas ir saistīta ar karšu nozari (PCI). **Piezīme:** pastāv iespēja atsevišķi konfigurēt mazumtirdzniecības plānotāju. Šī opcija ļauj atiestatīt mazumtirdzniecības plānotāja konfigurāciju uz noklusētajiem iestatījumiem. Pēc inicializēšanas pabeigšanas, jums ir jākonfigurē papildu mazumtirdzniecības dati. Daži piemēri:

-   Mazumtirdzniecības parametri
-   Mazumtirdzniecības plānotāja parametri
-   Mazumtirdzniecības kanāli
-   Reģistri un ierīces
-   Preču klāsts





