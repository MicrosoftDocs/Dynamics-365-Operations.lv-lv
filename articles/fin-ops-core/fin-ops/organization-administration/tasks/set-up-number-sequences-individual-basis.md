---
title: Atsevišķu numuru sēriju iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt atsevišķu numuru sēriju.
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 260fae39d9a98feb7bfa82188c5b05de9a533136
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796634"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Atsevišķu numuru sēriju iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt atsevišķu numuru sēriju. Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus pamatdatu ierakstu identifikatorus un darījumu ierakstus, kam tie ir nepieciešami. Pamatdati vai darījumu ieraksts, kam nepieciešams identifikators, tiek saukts par atsauci. Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci. Varat iestatīt visas nepieciešamās numuru sērijas vienlaicīgi, izmantojot vedni **Numuru sēriju iestatīšana** vai arī varat izveidot vai modificēt atsevišķas numuru sērijas, izmantojot lapu **Numuru sērijas**.

1. Pārejiet uz **Navigācijas rūts > Moduļi > Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**.
2. Atlasiet **Numuru sērija**.
3. Laukā **Numuru sērijas kods** ierakstiet kādu vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Kopsavilkuma cilnē **Apjoma parametri** atlasiet numuru sērijas tvēruma diapazonu un atlasiet tvēruma vērtības nolaižamajā sarakstā. Tvērums definē, kuras organizācijas izmanto šo numuru sēriju. Turklāt numuru sērijām, kuru tvērums nav **Koplietots**, var būt segmenti, kas atbilst to tvērumam. Piemēram, numuru sērija ar tvērumu **Juridiska persona** var ietvert juridiskas personas segmentu. Papildinformāciju par tvērumiem skatiet nodaļā [Numuru sēriju pārskats](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview). 
6. Izvērsiet sadaļu **Segmenti**.
    - Definējiet formātu numuru sērijai, pievienojot, noņemot un pārkārtojot segmentus.  
    - Visu tvērumu numuru sērijas var saturēt *Konstantus segmentus* un *Burtciparu segmentus*. Konstanti segmenti satur burtciparu rakstzīmju kopu, kas nemainās. Izmantojiet šo segmenta tipu, lai pievienotu defisi vai citus atdalītājus starp numuru sērijas segmentiem. Burtciparu segmenti satur numura zīmju (#) un zīmju ampersand (&) kombināciju. Šīs rakstzīmes apzīmē burtus un ciparus, kas pieaug katru reizi, kad tiek izmantots skaitlis no šīs sērijas. Norādiet numura zīmi (#), lai norādītu pieaugošus numurus, un zīmi &, lai norādītu pieaugošus burtus. Piemēram, formāts `#####_2014` izveido sēriju `00001_2014`, `00002_2014` un tā tālāk. Nepieciešams vismaz viens burtu un ciparu segments. Tvērumu segmenti, piemēram, uzņēmums vai juridiskā persona, nav obligāti. Tomēr, ja formātā neiekļaujat tvēruma segmentus, katrai atlasītajai atsaucei tik un tā tiek ģenerēti numuri katram tvērumam.  
7. Izvērsiet sadaļu **Atsauces**. Atlasiet dokumentu veidu vai ierakstu, kam piešķirt šo numuru sēriju. Šis solis nav obligāts sērijām, kas definētas īpašiem lietojumprogrammas izmantošanas modeļiem. Šajos gadījumos jauns numurs tiek ģenerēts, izmantojot numuru sērijas koda vai ID vērtību, neizmantojot atsauci. Īpašo programmu lietošanas modeļa piemērs ir dokumentu sērija, ko izmanto konkrētiem žurnālu nosaukumiem. Tomēr nav ieteicams izmantot šādus modeļus.  
8. Izvērsiet sadaļu **Vispārīgi**. Kopsavilkuma cilnē Vispārīgi, norādiet, vai numuru sērija ir manuāla, un nepārtraukta vai ar pārtraukumiem. Turklāt, ievadiet mazāko un lielāko numuru, ko var izmantot šajā numuru sērijā. Nav ieteicams numuru sēriju ar pārtraukumiem mainīt pret nepārtrauktu numuru sēriju. Šāda numuru sērija nevar būt patiesi nepārtraukta. Šī izmaiņa var izraisīt arī atslēgu dublikātu pārkāpumus datu bāzē. Turklāt nepārtrauktām numuru sērijām ir lielāka ietekme uz veiktspēju.   
9. Noklikšķiniet uz **Saglabāt**.

