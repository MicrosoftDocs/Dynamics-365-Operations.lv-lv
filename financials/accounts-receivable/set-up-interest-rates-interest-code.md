---
title: "Procentu likmju iestatīšana interešu kodam"
description: "Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Procentu likmju iestatīšana interešu kodam

Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem.

Varat iestatīt vienu procentu kodu un piemērot to vairākiem debitora grāmatošanas profiliem, norēķinu kodiem vai noteiktām rēķina rindām. Mainoties procentu kodu detaļām, visas funkcijas, kuras lieto kodu, automātiski veiks izmaiņas jaunos darījumos. Katram procentu kodam varat uzstādīt divu veidu likmes.
-   Likmes procentu ieņēmumiem — tie ir ieņēmumi, kas ir nopelnīti, iekasējot procentus no rēķiniem vai rēķinu paziņojumiem.
-   Likmes procentu maksājumiem — tie pārstāv izmaksas, kas ir samaksāti par procentiem kredīta notās.

Abi šie likmju veidi var eksistēt vienlaicīgi vienā un tajā pašā procentu kodā. Procentu likmes pamatā var būt trīs aprēķinu veidi.
-   Procentu likme pēc procentuālā daudzuma.
-   Procentu likme pēc summas.
-   Procentu likme pēc diapazona, kas ir izteikts kā viens procentuāls daudzums vai summa.

Kad procentu kods tiek izmantots, lai aprēķinātu procentus, tiek izveidots atsevišķs procentu paziņojums katrai procentu likmei, kas ir spēkā laika posmā, kad maksājums pārsniedz darījuma apmaksas datumu. Izmantojiet cilni **Ienākumi** lapā **Procentu kods**, lai iestatītu procentu likmes procentiem, ko nopelnāt, iekasējot procentus. Izmantojiet cilni **Maksājumi**, lai iestatītu procentu likmes tiem procentiem, ko maksājat jūs.

## <a name="interest-rates-based-on-a-percentage"></a>Uz procentuālu daudzumu balstītas procentu likmes
Varat iestatīt procentu likmes, kas aprēķina noteiktu procentu.

-   Procentu summa attiecas uz visām valūtām.
-   Iespējams ievadīt neobligātus procentu summas ierobežojumus.
-   **Procentu** atzīmēta * * * *, **aprēķināt procentus, kas balstās uz** lauku **iestatīt soda naudas kodus** lapu.

Piemēram, lai iestatītu soda naudas kodiem, kas novērtē procentu likmi 5 procenti, ik pēc diviem mēnešiem rēķina maksājums pārsniedz darījuma izpildes datums būtu jāievada 2 **aprēķināt procentus katru** lauka un atlasiet **mēnesī**.

## <a name="interest-rates-based-on-amounts"></a>Uz summām balstītas procentu likmes
Varat iestatīt procentu likmes, kas aprēķina norādīto summu pēc valūtām.
-   Procentu summa tiek norādīta katrai valūtai procentu kodā.
-   Iespējams ievadīt neobligātus procentu summas ierobežojumus.
-   * * Summa * * atlasīta **aprēķināt procentus, kas balstās uz** lauku **iestatīt soda naudas kodus** lapā.

Piemēram, lai iestatītu soda naudas kodiem, kas izvērtē 25,00 interešu ik pēc 20 dienām, rēķina maksājums pārsniedz darbības izpildes datumu, ievadiet 20 **aprēķināt procentus katru** lauka un atlasiet **dienu**.

## <a name="interest-rates-based-on-ranges"></a>Uz diapazoniem balstītas procentu likmes
Varat iestatīt procentu likmes, kas svārstās atkarībā no nokavētās maksājuma summas, nokavēto dienu skaita vai nokavēto mēnešu skaita.
-   Varat lietot cilni **Ieņēmumi pēc valūtas**, lai katrai valūtai definētu konkrētus procentu iestatījumus. Šeit jūs arī definējat diapazonu.
-   Izmantojiet pogu **Diapazoni**, lai pievienotu rindas, kas apzīmē diapazonus, kurus vēlaties iestatīt. Vērtība **No** apzīmē diapazona sākumu, un skaitlis **Procentu vērtība** apzīmē procentuālu daudzumu vai summu, atkarībā no atlases laukā **Aprēķināt procentus, pamatojoties uz**, lapā **Iestatīt procentu kodus**.

## <a name="example-1-interest-by-range--amount"></a>1. piemērs: procenti pēc diapazona = summa
Iestatiet procentu kodu, kas novērtē procentus vienu reizi katrus trīs mēnešus, par kuriem rēķina maksājums pārsniedz darījuma izpildes datumu. Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem summu intervāliem. Procentu vērtība būs 1 procents rēķina summām līdz 1000,00, 2 procenti summām no 1001,00 līdz 5000,00 un 3 procenti summām, kas lielākas par 5000,00. Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.

| **Lauka nosaukums**                  | **Lauka vērtība** |
|---------------------------------|-----------------|
| **Soda naudas kods**               | 3M%ByAmt        |
| **Aprēķināt procentus ik pēc šāda laikposma:**    | 3/month         |
| **Procenti pēc diapazona**           | Summa          |
| **Aprēķināt procentus, pamatojoties uz** | Procenti      |

Iestatiet diapazona informāciju, kā norādīts tālāk.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.                  |
| 1,001          | 2.                  |
| 5,001          | 3.                  |

 
## <a name="example-2-interest-by-range--days"></a>2. piemērs: procenti pēc diapazona = dienas
--------------------------------------------------

Iestatiet procentu kodu, kas novērtē procentus vienu reizi katras 15 dienas, par kurām rēķina maksājums pārsniedz darījuma izpildes datumu. Aprēķini jābalsta uz soda naudas vērtību summā saskaņā ar pakāpeniskajiem dienu intervāliem. Procentu vērtība būs 10,00 15 dienas pirmajās 60 dienās, 15,00 15 dienas no 61 līdz 90 dienām, un 20,00 15 dienas, sākot no 91 dienas. Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.

| **Lauka nosaukums**                  | **Lauka vērtība** |
|---------------------------------|-----------------|
| **Soda naudas kods**               | 15DAmtXDay      |
| **Aprēķināt procentus ik pēc šāda laikposma:**    | 15/Diena          |
| **Procenti pēc diapazona**           | Dienas            |
| **Aprēķināt procentus, pamatojoties uz** | Summa          |

Iestatiet diapazona informāciju, kā norādīts tālāk.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 10.                 |
| 61             | 15.                 |
| 91             | 20.                 |

 
## <a name="example-3-interest-by-range--months"></a>3. piemērs: procenti pēc diapazona = mēneši
----------------------------------------------------

Iestatiet procentu kodu, kas novērtē procentus vienu reizi katru mēnesi, par kuru rēķina maksājums pārsniedz darījuma izpildes datumu. Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem mēnešu intervāliem. Procentu vērtība būs 1,5 procenti mēnesī par pirmajiem trim nokavētajiem mēnešiem, 2,0 procenti mēnesī par nākamajiem trim mēnešiem un 2,5 procenti mēnesī pēc pirmajiem sešiem mēnešiem. Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.

| **Lauka nosaukums**                  | **Lauka vērtība** |
|---------------------------------|-----------------|
| **Soda naudas kods**               | 1M%ByMth        |
| **Aprēķināt procentus ik pēc šāda laikposma:**    | 1/month         |
| **Procenti pēc diapazona**           | Mēneši          |
| **Aprēķināt procentus, pamatojoties uz** | Procenti      |

Iestatiet diapazona informāciju, kā norādīts tālāk.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.5                |
| 4.              | 2.                  |
| 7.              | 2,5                |

## <a name="new-versions"></a>Jaunas versijas
Procentu kodiem ir spēkā stāšanās datums. Ja procentu likmi vēlaties mainīt, varat izveidot **jaunu versiju**, kas ir spēkā no nākotnes datuma.

Lai skatītu citādas versijas, varat izmantot izvēlnes vienumu **No datuma**, lai atlasītu robeždatuma. Varat arī atlasīt vienumu **Rādīt visus ierakstus**, lai skatītu visus procentu kodus lapā.


