--- 
title: "Iestatīt atsevišķas numuru sērijas"
description: "Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus pamatdatu ierakstu identifikatorus un darījumu ierakstus, kam tie ir nepieciešami."
author: sericks007
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e2808e57dc8d137fac892d48e99d7687ff1bf81
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Iestatīt atsevišķas numuru sērijas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus pamatdatu ierakstu identifikatorus un darījumu ierakstus, kam tie ir nepieciešami. Pamatdati vai darījumu ieraksts, kam nepieciešams identifikators, tiek saukts par atsauci. Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci. Varat iestatīt visas nepieciešamās numuru sērijas vienlaicīgi, izmantojot vedni Numuru sēriju iestatīšana, vai arī varat izveidot vai modificēt atsevišķas numuru sērijas, izmantojot lapu Numuru sērijas.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Numuru secība > Numuru secība.
2. Noklikšķiniet uz Numuru sērija.
3. Laukā Numuru sērijas kods, ierakstiet kādu vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Izvērsiet sadaļu Tvēruma parametri.
    * Kopsavilkuma cilnē Apjoma parametri, atlasiet numuru sērijas tvēruma diapazonu un atlasiet tvēruma vērtības.     Tvērums definē, kuras organizācijas izmanto šo numuru sēriju. Turklāt numuru sērijām, kuru tvērums nav Koplietots, var būt segmenti, kas atbilst to tvērumam. Piemēram, numuru sērija ar tvērumu Juridiska persona var ietvert juridiskas personas segmentu. Papildinformāciju par tvērumiem skatiet palīdzības tēmā “Numuru sēriju apskats”.  
6. Izvērsiet sadaļu Segmenti.
    * Kopsavilkuma cilnē Segmenti, definējiet formātu numuru sērijai, pievienojot, noņemot un pārkārtojot segmentus.  
    * Visu tvērumu numuru sērijas var saturēt konstantus segmentus un burtciparu segmentus. Konstanti segmenti satur burtciparu rakstzīmju kopu, kas nemainās. Izmantojiet šo segmenta tipu, lai pievienotu defisi vai citus atdalītājus starp numuru sērijas segmentiem. Burtciparu segmenti satur numura zīmju (#) un zīmju ampersand (&) kombināciju. Šīs rakstzīmes apzīmē burtus un ciparus, kas pieaug katru reizi, kad tiek izmantots skaitlis no šīs sērijas. Norādiet numura zīmi (#), lai norādītu pieaugošus numurus, un zīmi &, lai norādītu pieaugošus burtus. Piemēram, formāts #####_2014 izveido sēriju 00001_2014, 00002_2014 utt.     Nepieciešams vismaz viens burtu un ciparu segments. Tvērumu segmenti, piemēram, uzņēmums vai juridiskā persona, nav obligāti. Tomēr, ja formātā neiekļaujat tvēruma segmentus, katrai atlasītajai atsaucei tik un tā tiek ģenerēti numuri katram tvērumam.  
7. Izvērsiet sadaļu Atsauces.
    * Kopsavilkuma cilnē Atsauces, atlasiet dokumentu tipu vai pārskatu, kam piešķirt šo numuru sēriju.     Šis solis nav obligāts sērijām, kas definētas īpašiem lietojumprogrammas izmantošanas modeļiem. Šajos gadījumos jauns numurs tiek ģenerēts, izmantojot numuru sērijas koda vai ID vērtību, neizmantojot atsauci. Īpašo programmu lietošanas modeļa piemērs ir dokumentu sērija, ko izmanto konkrētiem žurnālu nosaukumiem. Tomēr nav ieteicams izmantot šādus modeļus.  
8. Izvērsiet sadaļu Vispārīgi.
    * Kopsavilkuma cilnē Vispārīgi, norādiet, vai numuru sērija ir manuāla, un nepārtraukta vai ar pārtraukumiem. Turklāt, ievadiet mazāko un lielāko numuru, ko var izmantot šajā numuru sērijā.     Nav ieteicams numuru sēriju ar pārtraukumiem mainīt pret nepārtrauktu numuru sēriju. Šāda numuru sērija nevar būt patiesi nepārtraukta. Šī izmaiņa var izraisīt arī atslēgu dublikātu pārkāpumus datu bāzē. Turklāt nepārtrauktām numuru sērijām ir lielāka ietekme uz veiktspēju.   
9. Noklikšķiniet uz Saglabāt.


