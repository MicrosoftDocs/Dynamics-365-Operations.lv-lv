---
title: Procentu likmju iestatīšana interešu kodam
description: Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09808433140f71bf2d7bfaaca87b6c27adb56d86c4c14ad44b37592d416fa2b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716721"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a>Procentu likmju iestatīšana interešu kodam

[!include [banner](../includes/banner.md)]

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

- Procentu summa attiecas uz visām valūtām.
- Iespējams ievadīt neobligātus procentu summas ierobežojumus.
- Vienums **Procenti** ir atlasīts laukā **Aprēķināt procentus, pamatojoties uz**, kurš atrodas lapā **Iestatīt procentu kodus**.

Piemēram, lai iestatītu procentu kodu, kas novērtē 5 procentu soda naudu par katriem diviem mēnešiem, kuros rēķina maksājums pārsniedz transakcijas izpildes datumu, laukā **Aprēķināt procentus ik pēc šāda laikposma** ir jāievada 2 un jāatlasa **Mēnesis**.

> [!NOTE] 
> Jaunais algoritms procentu paziņojuma aprēķināšanai ir pievienots, izmantojot līdzekļu pārvaldību. Lai lietotu šo algoritmu, iespējojiet līdzekli **(GBL) Ļauj aprēķināt procentus par dienu kā gada procentus, dalītus ar 365**. Papildinformāciju par šā līdzekļa iespējošanu skatiet rakstā [Pārskats par līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
> 
> Procentu paziņojuma summas aprēķina formula ir šāda: 
>  
> Procentu paziņojuma summa = maksājamā summa * gada procenti % / 365 * nokavēto dienu skaits
>  
> Šis līdzeklis ir pieejams versijā 10.0.18 vai jaunākās versijās.    
 
## <a name="interest-rates-based-on-amounts"></a>Uz summām balstītas procentu likmes
Varat iestatīt procentu likmes, kas aprēķina norādīto summu pēc valūtām.
- Procentu summa tiek norādīta katrai valūtai procentu kodā.
- Iespējams ievadīt neobligātus procentu summas ierobežojumus.
- Vienums **Summa** ir atlasīts laukā **Aprēķināt procentus, pamatojoties uz**, kurš atrodas lapā **Iestatīt procentu kodus**.

Piemēram, lai iestatītu procentu kodu, kas novērtē 25,00 soda naudu par katrām 20 dienām, kurās rēķina maksājums pārsniedz transakcijas izpildes datumu, laukā **Aprēķināt procentus ik pēc šāda laikposma** ir jāievada 20 un ir jāatlasa vienums **Diena**.

## <a name="interest-rates-based-on-ranges"></a>Uz diapazoniem balstītas procentu likmes
Varat iestatīt procentu likmes, kas svārstās atkarībā no nokavētās maksājuma summas, nokavēto dienu skaita vai nokavēto mēnešu skaita.
-   Varat lietot cilni **Ieņēmumi pēc valūtas**, lai katrai valūtai definētu konkrētus procentu iestatījumus. Šeit jūs arī definējat diapazonu.
-   Izmantojiet pogu **Diapazoni**, lai pievienotu rindas, kas apzīmē diapazonus, kurus vēlaties iestatīt. Vērtība **No** apzīmē diapazona sākumu, un skaitlis **Procentu vērtība** apzīmē procentuālu daudzumu vai summu, atkarībā no atlases laukā **Aprēķināt procentus, pamatojoties uz**, lapā **Iestatīt procentu kodus**.

## <a name="example-1-interest-by-range--amount"></a>1. piemērs: procenti pēc diapazona = summa
Iestatiet procentu kodu, kas novērtē procentus vienu reizi katrus trīs mēnešus, par kuriem rēķina maksājums pārsniedz darījuma izpildes datumu. Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem summu intervāliem. Procentu vērtība būs 1 procents rēķina summām līdz 1000,00, 2 procenti summām no 1001,00 līdz 5000,00 un 3 procenti summām, kas lielākas par 5000,00. Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.

| **Lauka nosaukums**                  | **Lauka vērtība** |
|---------------------------------|-----------------|
| **Soda naudas kods**               | 3M%ByAmt        |
| **Aprēķināt procentus ik pēc šāda laikposma:**    | 3/Mēnesis         |
| **Procenti pēc diapazona**           | Summa          |
| **Aprēķināt procentus, pamatojoties uz** | Procenti      |

Iestatiet diapazona informāciju, kā norādīts tālāk.

| **No vērtības** | **Procentu vērtība** |
|----------------|--------------------|
| 0              | 1.                  |
| 1,001          | 2.                  |
| 5,001          | 3.                  |


## <a name="example-2-interest-by-range--days"></a>2. piemērs: procenti pēc diapazona = dienas

Iestatiet procentu kodu, kas novērtē procentus vienu reizi katras 15 dienas, par kurām rēķina maksājums pārsniedz darījuma izpildes datumu. Aprēķini jābalsta uz soda naudas vērtību summā saskaņā ar pakāpeniskajiem dienu intervāliem. Procentu vērtība būs 10,00 15 dienas pirmajās 60 dienās, 15,00 15 dienas no 61 līdz 90 dienām, un 20,00 15 dienas, sākot no 91 dienas. Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.

| **Lauka nosaukums**                  | **Lauka vērtība** |
|---------------------------------|-----------------|
| **Soda naudas kods**               | 15DAmtXDay      |
| **Aprēķināt procentus ik pēc šāda laikposma:**    | 15/Diena          |
| **Procenti pēc diapazona**           | Dienas            |
| **Aprēķināt procentus, pamatojoties uz** | Summa          |

Iestatiet diapazona informāciju, kā norādīts tālāk.

| **No vērtības** | **Procentu vērtība** |
|----------------|--------------------|
| 0              | 10.                 |
| 61             | 15.                 |
| 91             | 20.                 |


## <a name="example-3-interest-by-range--months"></a>3. piemērs: procenti pēc diapazona = mēneši

Iestatiet procentu kodu, kas novērtē procentus vienu reizi katru mēnesi, par kuru rēķina maksājums pārsniedz darījuma izpildes datumu. Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem mēnešu intervāliem. Procentu vērtība būs 1,5 procenti mēnesī par pirmajiem trim nokavētajiem mēnešiem, 2,0 procenti mēnesī par nākamajiem trim mēnešiem un 2,5 procenti mēnesī pēc pirmajiem sešiem mēnešiem. Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.

| **Lauka nosaukums**                  | **Lauka vērtība** |
|---------------------------------|-----------------|
| **Soda naudas kods**               | 1M%ByMth        |
| **Aprēķināt procentus ik pēc šāda laikposma:**    | 1/Mēnesis         |
| **Procenti pēc diapazona**           | Mēneši          |
| **Aprēķināt procentus, pamatojoties uz** | Procenti      |

Iestatiet diapazona informāciju, kā norādīts tālāk.

| **No vērtības** | **Procentu vērtība** |
|----------------|--------------------|
| 0              | 1.5                |
| 4.              | 2.                  |
| 7.              | 2,5                |

## <a name="new-versions"></a>Jaunas versijas
Procentu kodiem ir spēkā stāšanās datums. Ja procentu likmi vēlaties mainīt, varat izveidot **jaunu versiju**, kas ir spēkā no nākotnes datuma.

Lai skatītu citādas versijas, varat izmantot izvēlnes vienumu **No datuma**, lai atlasītu robeždatuma. Varat arī atlasīt vienumu **Rādīt visus ierakstus**, lai skatītu visus procentu kodus lapā.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
