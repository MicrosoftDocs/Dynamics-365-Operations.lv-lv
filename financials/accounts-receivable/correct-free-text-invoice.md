---
title: "Brīva teksta rēķina labošana"
description: "Šajā rakstā ir paskaidrots, kā labot brīva teksta rēķinu, kas jau ir iegrāmatots, un kā to vēlreiz izsniegt kā labotu rēķinu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>Brīva teksta rēķina labošana

Šajā rakstā ir paskaidrots, kā labot brīva teksta rēķinu, kas jau ir iegrāmatots, un kā to vēlreiz izsniegt kā labotu rēķinu.

Lai koriģētu brīvā teksta rēķina, kas jau ir iegrāmatotas, atvērt iegrāmatoto brīvā teksta rēķina. Par **rēķina** lapu, atlasiet **atcelt**, un pēc tam atlasiet **pareizo rēķina**. Atlasiet iemesla kodu, pievienojiet komentārus un atlasiet datumu jaunajam labotajam rēķinam. Varat modificēt laboto rēķinu un to grāmatot. 

Kad grāmatojat laboto rēķinu, tiek izveidots atcelšanas rēķins par kredīta summu, kas ir vienāda ar sākotnējā rēķina summu. Līdz ar to sākotnējā rēķina un atcelšanas rēķina apvienotā bilance ir 0 (nulle). Atcelšanas rēķins tiek segts pret sākotnējo rēķinu. 

Pēc labotā rēķina grāmatošanas jums ir trīs rēķini:

-   **Sākotnējais rēķins** — rēķins, kas ietver informāciju, kuru jūs labojat.
-   **Atcelšanas rēķins** — sistēmas ģenerēts kredītrēķins, kas tika izveidots, lai atceltu pēdējo laboto rēķinu.
-   **Labotais rēķins** — rēķins, kas ietver labotā rēķina informāciju.

Atcelšanas un labošanas rēķinus varat identificēti divējādi:

-   Lapā **Visi brīva teksta rēķini** ietver kolonnu **Labojums**, kur varat redzēt, kuri rēķini ir atcelšanas rēķini un labotie rēķini.
-   Brīva teksta rēķina virsrakstā norādīts statuss **tiek atcelta rēķina '\[rēķina numurs\]'** vai **izlabota rēķina '\[rēķina numurs\]'**.

> [!NOTE]
> Šis līdzeklis ir pieejams tikai tad, ja **brīvā teksta rēķina labošana** konfigurācijas atslēga ir atzīmēta.


