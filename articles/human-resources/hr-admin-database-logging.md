---
title: Datu bāzu reģistrācijas konfigurēšana un pārvaldība
description: Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443587"
---
# <a name="configure-and-manage-database-logging"></a>Datu bāzu reģistrācijas konfigurēšana un pārvaldība

Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu. Šajā tēmā ir aprakstīts, kā:

- Pārvaldīt drošības un veiktspējas datu bāzes reģistrēšanu
- Iestatīt datu bāzes reģistrēšanu
- Iztīrīt datu bāzes žurnālus

## <a name="overview-of-database-logging"></a>Datu bāzes reģistrācijas pārskats

Datubāzes reģistrēšana izseko specifiskas izmaiņas Microsoft Dynamics 365 Human Resources tabulās un laukos. Šīs izmaiņas ietver ievietošanu, atjaunināšanu vai dzēšanu. Datu bāzes reģistrācija saglabā ierakstu par izmaiņām tabulās vai laukos datu bāzes žurnāla tabulā.

Biznesa datu bāzes reģistrācijas izmantošana ietver:

- Tiek izveidots audita ieraksts par izmaiņām noteiktās tabulās, kurās ir sensitīva informācija.
- Atsevišķu darbību izsekošana. Datu bāzes reģistrēšana nav paredzēta automatizēto darbību izsekošanai, kas darbojas pakešuzdevumos.

## <a name="security-for-database-logging"></a>Drošība datu bāzes reģistrēšanai

Datubāzes žurnālos var būt sensitīvi dati. Ierobežojiet piekļuvi, lai iekļautu tikai tās drošības lomas, kurām nepieciešama piekļuve žurnāla datiem.

## <a name="database-logging-and-performance"></a>Datu bāzes reģistrēšana un veiktspēja

Lai gan no biznesa perspektīvas tā ir vērtīga, datu bāzes reģistrēšana resursu izmantošanā un vadībā var būt dārga. Datu bāzes reģistrēšanas veiktspējas ietekme ietver:

- Datu bāzes žurnāla tabula var ātri augt un radīt datu bāzes apjoma palielinājumu. Pieaugums ir atkarīgs no reģistrēto datu apjoma, ko izlemjat paturēt. Pēc noklusējuma datu bāzes žurnāla tabula uztur tikai 30 dienu žurnāla datus. 

- Datu bāzes reģistrācija var negatīvi ietekmēt ilgstošos automatizētos procesus, piemēram, ilgstošo datu importēšanu.

### <a name="best-practices"></a>Noteikumi

Lai uzlabotu veiktspēju, ierobežojiet reģistrēšanas ierakstus, atlasot reģistrēšanai īpašus laukus, bet nereģistrējiet visas tabulas. Lai palīdzētu uzturēt vispārējo veiktspēju, datu bāzes reģistrēšana ir ierobežota līdz 20 tabulām.

> [!NOTE]
> Dažreiz laukiem var reģistrēt tikai atjauninājumus.

## <a name="set-up-database-logging"></a>Iestatīt datu bāzes reģistrēšanu

Varat izmantot **Reģistrēšanas datu bāzes izmaiņu** ceļvedi, lai iestatītu datu bāzes reģistrēšanu. Ceļvedis sniedz elastīgu veidu, kā iestatīt reģistrāciju tabulām vai laukiem.

1. Dodieties uz **Sistēmas administrēšanu > Saites > Datu bāzes > Datu bāzes žurnāla iestatījumi**. Atlasiet **Jauns**, lai sāktu **Datu bāzes izmaiņu reģistrēšanas** ceļvedi.
2. Pabeidziet ceļvedi.

## <a name="clean-up-database-logs"></a>Iztīrīt datu bāzes žurnālus

Varat izdzēst visu vai daļu no datu bāzes žurnāliem, izmantojot šādas opcijas:

- Atlasiet visus žurnālus noteiktai tabulai.
- Atlasiet specifiskus datu bāzes žurnāla tipus.
- Atlasiet datumu un laiku, kad tika izveidots žurnāls.

Lai iestatītu datu bāzes žurnāla tīrīšanu, rīkojieties šādi: 

1. Dodieties uz **Sistēmas administrēšana > Saites > Datu bāzes > Datu bāzes žurnāls**. Atlasiet **Tīrīt žurnālu**.

2. Izvēlieties metodi, kā atlasīt žurnālus dzēšanai, ievadot vienu no šīm opcijām:

   - Tabulas ID
   - Žurnāla tips
   - Izveidotais datums un laiks

3. Izmantojiet cilni **Datu bāzes žurnāla tīrīšana**, lai noteiktu, kad palaist žurnāla tīrīšanas uzdevumu. Pēc noklusējuma datu bāzes žurnāli ir pieejami 30 dienas.
