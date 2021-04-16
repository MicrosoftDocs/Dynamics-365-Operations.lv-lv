---
title: Pakešuzdevuma izveide
description: Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.
author: maertenm
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f498014555e0beccbc8965dd43e5162944867978
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745865"
---
# <a name="create-a-batch-job"></a>Pakešuzdevuma izveide

[!include [banner](../../includes/banner.md)]

Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei. Pakešuzdevumi tiek izpildīti, izmantojot darbu izveidojušā lietotāja drošības akreditācijas datus. Lai izveidotu pakešuzdevumu, izpildiet tālāk aprakstīto procedūru. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-the-batch-job"></a>Izveidot pakešuzdevumu
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Pienākumu apraksts** ierakstiet kādu vērtību.
4. Laukā **Plānotais sākuma datums/laiks** ievadiet datumu un laiku.
5. Noklikšķiniet uz **Saglabāt**.

## <a name="create-a-recurrence"></a>Izveidot atkārtošanos
1. Darbību rūtī noklikšķiniet uz **Pakešuzdevums**.
2. Noklikšķiniet uz **Periodiskums**. Izmantojiet šīs opcijas, lai ievadītu periodiskuma diapazonu un modeli.  
3. Noklikšķiniet uz **Labi**.

## <a name="add-alerts"></a>Pievienot brīdinājumus
1. Darbību rūtī noklikšķiniet uz **Pakešuzdevums**.
2. Noklikšķiniet uz **Brīdinājumi**. Norādiet, vai vēlaties sūtīt brīdinājuma ziņojumus, kad pakešuzdevums beidzas, kad tam ir kļūda vai kad tas tiek atcelts. Pēc tam norādiet, vai vēlaties brīdinājumus rādīt kā uznirstošos ziņojumus.   
3. Noklikšķiniet uz **Labi**.

## <a name="adjust-batch-job-status"></a>Pakešuzdevuma statusa pielāgošana
1. Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Atlasiet atbilstošo pakešuzdevumu.
3. Darbību rūtī noklikšķiniet uz **Pakešuzdevums > Funkcijas > Mainīt statusu**.
4. Atlasiet atbilstošo statusu.
    - **Aizturēt**: atlasiet pakešuzdevuma statusu **aizturēt**, lai tas tiktu aizturēts no pakešuzdevumu plānotāja. Līdzvērtīgs funkcijai *apturēt*.
    - **Gaida**: atlasiet pakešuzdevuma statusu **gaida**, lai tas gaidītu rindā, līdz to izvēlēsies pakešuzdevumu plānotājs. Līdzvērtīgs funkcijai *sākt*.
5. Noklikšķiniet uz **Labi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]