---
title: Datu bāzu reģistrācijas konfigurēšana un pārvaldība
description: Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10591abee7890d54d721c9324101a4b4bd0a74d2
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924824"
---
# <a name="configure-and-manage-database-logging"></a>Datu bāzu reģistrācijas konfigurēšana un pārvaldība

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
2. Atlasiet **Nākamais**. 
3. Vedņa lapā **Tabulas un lauki** atlasiet tabulas un laukus, kuros vēlaties iespējot datu bāzes reģistrēšanu, un atlasiet **Tālāk**.

   > [!Note]
   > Datu bāzes reģistrēšana nav pieejama visās personāla vadības datu bāzes tabulās. Atlasot **Rādīt visas tabulas** zem saraksta, tiek izvērsts tabulu un lauku saraksts, lai parādītu visas datu bāzes tabulas, kurām ir pieejama datu bāzes reģistrēšana, bet tā būs pilna datu bāzu tabulu saraksta apakškopa.

4. Vedņa lapā **Izmaiņu tipi** atlasiet datu operācijas, kurām vēlaties reģistrēt katras tabulas un lauka izmaiņas, un atlasiet **Tālāk**. Tālāk esošajā tabulā ir sniegts reģistrēšanai pieejamo datu operāciju apraksts.
5. Lapā **Pabeigt** pārskatiet veiktās izmaiņas un atlasiet **Pabeigt**.

| Operācija | Apraksts |
| -- | -- |
| Izsekot jaunās darbības | Izveidojiet žurnālu jauniem ierakstiem, kas izveidoti tabulā. |
| Grāmatot | Izveidojiet žurnālu tabulu ierakstu atjauninājumiem vai atsevišķi atlasītu tabulas lauku atjauninājumiem. Ja izvēlaties reģistrēt tabulas atjauninājumus, žurnāla ieraksts tiek izveidots ikreiz, kad tiek atjaunināts jebkurš tabulas ieraksta lauks. Ja izvēlaties reģistrēt atjauninājumus noteiktiem laukiem, žurnāla ieraksts tiek izveidots tikai tad, kad šiem tabulas ierakstu laukiem tiek veikti atjauninājumi. |
| Delete | Izveidojiet žurnālu ierakstiem, kas izdzēsti no tabulas. |
| Pārdēvēt atslēgu | Kad tabulas atslēga ir pārdēvēta, izveidojiet žurnāla ierakstu. |


## <a name="clean-up-database-logs"></a>Iztīrīt datu bāzes žurnālus

Varat izdzēst visu vai daļu no datu bāzes žurnāliem, izmantojot šādas opcijas:

- Atlasiet visus žurnālus noteiktai tabulai.
- Atlasiet specifiskus datu bāzes žurnāla tipus.
- Atlasiet datumu un laiku, kad tika izveidots žurnāls.

Lai iestatītu datu bāzes žurnāla tīrīšanu, rīkojieties šādi: 

1. Dodieties uz **Sistēmas administrēšana > Saites > Datu bāzes > Datu bāzes žurnāls**. Atlasiet **Tīrīt žurnālu**.
2. Zem **Ieraksti, kas jāiekļauj** virsrakstā, atlasiet **Filtrēt**.
3. Izvēlieties metodi, kas tiks izmantota dzēšamā žurnāla atlasei. Ievadiet vienu no šīm opcijām:

   - Tabulas ID
   - Žurnāla tips
   - Izveidošanas datums un laiks

4. Izmantojiet cilni **Datu bāzes žurnāla tīrīšana**, lai noteiktu, kad palaist žurnāla tīrīšanas uzdevumu. Pēc noklusējuma datu bāzes žurnāli ir pieejami 30 dienas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
