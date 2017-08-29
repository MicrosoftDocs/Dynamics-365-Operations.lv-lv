--- 
title: "Pakešuzdevuma izveide"
description: "Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ca2b755406fb7fce4b11457be86f6a8685004438
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-batch-job"></a>Pakešuzdevuma izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei. Pakešuzdevumi tiek izpildīti, izmantojot darbu izveidojušā lietotāja drošības akreditācijas datus. Lai izveidotu pakešuzdevumu, izpildiet tālāk aprakstīto procedūru. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-the-batch-job"></a>Izveidot pakešuzdevumu
1. Doties uz Sistēmas administrēšana > Vaicājumi > Pakešuzdevumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Darba apraksts ierakstiet kādu vērtību.
4. Laukā Plānotais sākuma datums/laiks ievadiet datumu un laiku.
5. Noklikšķiniet uz Saglabāt.

## <a name="create-a-recurrence"></a>Izveidot atkārtošanos
1. Darbību rūtī noklikšķiniet uz Pakešuzdevums.
2. Noklikšķiniet uz Periodiskums.
    * Izmantojiet šīs opcijas, lai ievadītu periodiskuma diapazonu un modeli.  
3. Noklikšķiniet uz OK.

## <a name="add-alerts"></a>Pievienot brīdinājumus
1. Darbību rūtī noklikšķiniet uz Pakešuzdevums.
2. Noklikšķiniet uz Brīdinājumi.
    * Norādiet, vai vēlaties sūtīt brīdinājuma ziņojumus, kad pakešuzdevums beidzas, kad tam ir kļūda vai kad tas tiek atcelts. Pēc tam norādiet, vai vēlaties brīdinājumus rādīt kā uznirstošos ziņojumus.   
3. Noklikšķiniet uz OK.


