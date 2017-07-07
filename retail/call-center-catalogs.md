---
title: Zvanu centra katalogi
description: "Šajā rakstā ir aprakstīta zvanu centram specifiskā funkcionalitāte, kas tiek lietota katalogiem programmatūrā Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: c98cdb9c94a179577caecff7f57a99b91e4878a4
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017



---

# <a name="call-center-catalogs"></a>Zvanu centra katalogi

[!include[banner](includes/banner.md)]


Šajā rakstā ir aprakstīta zvanu centram specifiskā funkcionalitāte, kas tiek lietota katalogiem programmatūrā Microsoft Dynamics 365 for Retail.

Zvanu centrā preču katalogus var izmantot, lai identificētu preces, kuras vēlaties piedāvāt debitoriem. Zvanu centros parasti tiek izmantoti drukātie katalogi. Drukāta kataloga noformēšana un ražošana tiek veikta ārpus programmatūras Dynamics 365 for Retail. Taču varat izveidot un saglabāt katalogu digitālā formātā, izmantojot tās pašas lapas, ko lietojat tiešsaistes mazumtirdzniecības katalogu iestatīšanai. Lai varētu izveidot katalogu, jāiestata preču klāsti un jāpiešķir tie zvanu centram. Pēc tam pievienojiet preces katalogam, atlasot preces no šiem preču klāstiem. Kad preces ir pievienotas katalogam un katalogs ir pabeigts, validējiet katalogu, lai verificētu datus. Pēc tam iesniedziet katalogu pārskatīšanai un apstiprināšanai. Kad katalogs ir apstiprināts, to var publicēt. Kad esat izveidojis zvanu centra katalogu, kataloga publicēšanas brīdī varat izveidot kataloga datu momentuzņēmumu. Šī momentuzņēmumu funkcionalitāte ļauj piekļūt noteiktām kataloga versijām pat tad, ja katalogā vēlāk tiek veiktas izmaiņas un tas tiek atjaunināts. Zvanu centra katalogiem arī var iestatīt, lai tiktu iekļauti šādi izvēles līdzekļi:

-   **Avota kodi** – avota kodi, kas tiek izmantoti, lai izsekotu debitora reakciju uz noteiktiem kataloga pasta sūtījumiem.
-   **Bezmaksas preces** – preces, kas var būt iekļautas debitora pasūtījumā bez papildu maksas. Šīs preces automātiski tiek pievienotas pasūtījumam, ja pasūtījumā ir ievadīts kataloga avota kods.
-   **Skripti** – skripti ir teksti, kurus zvanu centra darbinieks nolasa debitoram, kad tiek izveidots pārdošanas pasūtījums. Skriptos var iekļaut sveicienus vai ieteikumus pirkumu veikšanai.
-   **Lapas izkārtojums** – lapas izkārtojums tver produktu lapas pozīciju drukātā katalogā. Šī informācija tiek izmantota kataloga zonas analīzes pārskatam.





