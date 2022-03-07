---
title: Pakešuzdevuma izveide
description: Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.
author: maertenm
ms.date: 11/22/2021
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
ms.openlocfilehash: 76c6c68f7effad0c40282b22ea2a6bf991862cf5
ms.sourcegitcommit: d7d997ad84623ad952672411c0eb6740972ae0b1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/24/2021
ms.locfileid: "7864177"
---
# <a name="create-a-batch-job"></a>Pakešuzdevuma izveide

[!include [banner](../../includes/banner.md)]

Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei. Pakešuzdevumi tiek izpildīti, izmantojot darbu izveidojušā lietotāja drošības akreditācijas datus. Lai izveidotu pakešuzdevumu, izpildiet tālāk aprakstīto procedūru. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-the-batch-job"></a>Izveidot pakešuzdevumu
1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Atlasiet **Jauna**.
3. Laukā **Darba apraksts** ievadiet pakešuzdevuma aprakstu.
4. Laukā **Plānotais sākuma** datums/laiks ievadiet datumu un laiku, kad pakešuzdevumam jādarbojas.
5. Atlasiet **Saglabāt**.

## <a name="create-a-recurrence"></a>Izveidot atkārtošanos
1. Darbību rūtī atlasiet **Pakešuzdevums**.
2. Atlasiet **Periodiskums**. Izmantojiet šīs opcijas, lai ievadītu periodiskuma diapazonu un modeli.  
3. Atlasiet **Labi**.

## <a name="add-alerts"></a>Pievienot brīdinājumus
1. Darbību rūtī atlasiet **Pakešuzdevums**.
2. Atlasiet **Brīdinājumus**. Norādiet, vai vēlaties sūtīt brīdinājuma ziņojumus, kad pakešuzdevums beidzas, kad tam ir kļūda vai kad tas tiek atcelts. Pēc tam norādiet, vai vēlaties brīdinājumus rādīt kā uznirstošos ziņojumus.   
3. Atlasiet **Labi**.

## <a name="add-a-task-to-a-batch-job"></a>Pievienot uzdevumu pakešuzdevumam
1.  Lapā **Pakešuzdevumi** atlasiet Skatīt **uzdevumus**.
2.  Izvēlieties **Ctrl+N,** lai izveidotu uzdevumu.
3.  Ievadiet pakešuzdevuma aprakstu.
4.  Laukā **Datu faili atlasiet uzņēmuma datu** bāzi, kurā izpildīt uzdevumu.
5.  Laukā **Klases nosaukums atlasiet uzdevumu** izpildāmo procesu. 
6.  Uzdevumam atlasiet pakešuzdevumu grupu, ja nepieciešams.

    Pakešuzdevumu grupai ir jāpiešķir klienta uzdevumi. Tās tiek automātiski piešķirtas noklusējuma pakešizpildes grupai (ko sauc arī par tukšo pakešuzdevumu grupu).

7.  Atlasiet **Ctrl+S,** lai saglabātu uzdevumu.
8.  Lai izvēlēto uzdevumu izveidotu atkarīgu no cita uzdevuma šajā darbā, izvēlieties režģi Ir nosacījumi un pēc tam izpildiet šīs darbības katram nosacījumam, **kuru** vēlaties definēt:

    1. Atlasiet **Ctrl+N,** lai izveidotu nosacījumu.
    2. Izvēlieties pamatelementa uzdevuma ID.
    3. Izvēlieties statusu, kurš pamata uzdevumam jāsasniedz pirms atkarīgā uzdevuma izpildes.
    4. Atlasiet **Ctrl+S,** lai saglabātu nosacījumu.

    Ja definēsiet vairāk nekā vienu nosacījumu un ja atkarīgā uzdevuma veikšanai ir jāizpilda visi nosacījumi, atlasiet *nosacījuma* tipu **Visi**. Ja atkarīgais uzdevums var tikt *izpildīts* pēc jebkura nosacījuma izpildes, izvēlieties nosacījuma tipu **Jebkurš**.

9.  Atlasiet, kā jārīkojas ar uzdevumu kļūdām. Lai ignorētu konkrēta uzdevuma kļūdu, cilnē Vispārīgi atlasiet šim uzdevumam opciju **Ignorēt** uzdevuma **kļūmi**. Ja ir atlasīta šī opcija, uzdevuma kļūda neizraisīs pakešuzdevuma atteici. Varat izmantot arī lauku Maksimālais atkārtoto mēģinājumu skaits, lai norādītu, cik reižu uzdevums ir atkārtots, pirms tiek uzskatīts, ka uzdevums **nav** izdevies. Saskaņā ar labāko praksi ieteicams neiesakām iestatīt lauku Maksimālais mēģinājumu skaits uz **vērtību**, kas ir lielāka par **5**.

    Papildinformāciju par pakešizpildes mēģinājumiem skatiet [sadaļā Pakešizpildes mēģinājumu](../retryable-batch.md) iespējošana.

## <a name="adjust-batch-job-status"></a>Pakešuzdevuma statusa pielāgošana
1. Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Atlasiet atbilstošo pakešuzdevumu.
3. Darbību rūtī atlasiet pakešuzdevuma **rindas> Funkcijas > mainīt** statusu.
4. Atlasiet atbilstošo statusu.
    - **Aizturēt**: atlasiet pakešuzdevuma statusu **aizturēt**, lai tas tiktu aizturēts no pakešuzdevumu plānotāja. Līdzvērtīgs funkcijai *apturēt*.
    - **Gaida**: atlasiet pakešuzdevuma statusu **gaida**, lai tas gaidītu rindā, līdz to izvēlēsies pakešuzdevumu plānotājs. Līdzvērtīgs funkcijai *sākt*.
5. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
