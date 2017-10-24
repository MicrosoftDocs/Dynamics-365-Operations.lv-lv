--- 
title: "Algas/atlīdzības organizācijas un plānu izstrāde"
description: "Šajā uzdevuma ceļvedī ir aprakstīts fiksētas atlīdzības plāna izveidošanas process un procedūra, kā darbiniekiem ļaut reģistrēties šādā plānā, izmantojot piemērotības kārtulas."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3cb6b9d8ee6a3d70731c89d26352eb3869ce3d11
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="develop-salarycompensation-structure-and-plans"></a>Algas/atlīdzības organizācijas un plānu izstrāde

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī ir aprakstīts fiksētas atlīdzības plāna izveidošanas process un procedūra, kā darbiniekiem ļaut reģistrēties šādā plānā, izmantojot piemērotības kārtulas. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF, un uzdevums ir paredzēts lietotājiem ar lomu Atlīdzību un atvieglojumu vadītājs.


## <a name="create-fixed-compensation-plan"></a>Izveidot fiksētas atlīdzības plānu
1. Noklikšķiniet uz Atlīdzību pārvaldība.
2. Noklikšķiniet uz Fiksētās atlīdzības plāni.
3. Noklikšķiniet uz Jauns.
4. Laukā Plāns ierakstiet kādu vērtību.
5. Apraksta laukā ierakstiet vērtību.
6. Laukā Spēkā stāšanās datums ievadiet kādu datumu.
7. Laukā Tips atlasiet, vai šis Fiksētas atlīdzības plāns ir Joslas, Līmeņa vai Pakāpes plāns.
8. Izvēles rūtiņa Ieteikšana atļauta darbojas kā noklusējuma vērtība visām darbībām, kas šim plānam tiek pievienotas apstrādes notikumā.  Ja ieteikšana ir atļauta, atlīdzības apstrādāšanas laikā varat ignorēt aprēķināto vadlīniju summu.
9. Vienums Tolerance ārpus diapazona jums ļauj norādīt, kā vēlaties apstrādāt atlīdzības summas, kuras attiecīgajam līmenim neietilpst norādītajā atlīdzību struktūras diapazonā.  Ja vienuma Tolerance ārpus diapazona vērtība ir Nav, tiek atļauts lietot jebkādu atlīdzības summu.  Ja vērtība ir Nestingra tolerance, tad lietotājs tiek brīdināts, ja atlīdzības summa ir mazāka par minimālo atsauces punkta summu attiecīgajam līmenim vai lielāka par maksimālo summu šim līmenim. Lietotājs var ignorēt šo brīdinājumu un turpināt.  Ja vērtība ir Stingra tolerance, tad tiek ģenerēta kļūda, kad darbinieka atlīdzība tiek iestatīta ārpus minimālā un maksimālā atsauces punkta diapazona attiecīgajam līmenim, un darbinieka atlīdzība tiek automātiski pielāgota, lai ietilptu diapazonā.
10. Lauks Nolīgšanas kārtula tiek izmantots, kad tiek palaists atlīdzības apstrādes notikums, lai aprēķinātu darbinieka atlīdzību.  Ja vienuma Nolīgšanas kārtula vērtība ir Procenti, tad tiek aprēķināts palielinājums, kas ir proporcionāli sadalīts laika ilgumam, kādu darbinieks ir bijis nodarbināts attiecīgajā ciklā.
11. Laukā Valūta ierakstiet kādu vērtību.
12. Laukā Apmaksas likmes konvertēšana ievadiet vai atlasiet kādu vērtību.
13. Izvērsiet sadaļu Diapazona lietojuma matrica.
    * Pēc izvēles pievienojiet diapazona izmantošanas ierakstus, lai darbinieki līdz savam viduspunktam nokļūtu ātrāk un tiktu kavēta darbinieku diapazona maksimuma sasniegšana.  
14. Šajā brīdī jums ir jāsaglabā šis Fiksētas atlīdzības plāns, lai iespējotu pogu Iestatīt atlīdzību un turpinātu definēt atlīdzību struktūru savam plānam.  Noklikšķiniet uz Saglabāt.
15. Noklikšķiniet uz Iestatīt atlīdzību.
    * Atlīdzību struktūru iespējams izveidot trīs veidos. 1: izveidot pilnīgi jaunu struktūru, atlasot atsauces punktu kopu un pievienojot līmeņus, lai izveidotu pats savu struktūru. 2: kādu atlīdzību struktūru no jau esoša plāna kopēt kā sākuma punktu un to pārveidot jaunajam plānam. 3: atlasīt jau esošu atlīdzību režģi. Ja atlīdzību režģis jau tiek izmantots kādam citam plānam, visas režģim veiktās izmaiņas tiks atspoguļotas arī otram plānam.  
16. Atzīmējiet opciju Izveidot jaunu no jau esošas atlīdzības matricas.
17. Laukā Kopēt no režģa ievadiet vai atlasiet kādu vērtību.
    * Ja vēlaties, varat mainīt nosaukumu jaunajam atlīdzību režģim, kas tiks izveidots kā atlasītā režģa kopija.  
18. Noklikšķiniet uz OK.
19. Noklikšķiniet Masveida izmaiņas.
    * Masveida izmaiņas jums ļauj uzturēt atlīdzību matricas summas, lietojot procentuālus vai fiksētus summas pieaugumus vienam vai vairākiem līmeņiem un/vai atsauces punktiem.  
20. Laukā Korekcijas summa ievadiet kādu skaitli.
21. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
22. Noklikšķiniet uz Lietot režģim.
23. Aizvērt lapu.
    * Kad atlīdzību struktūra ir izveidota vai atlasīta, varat atlasīt, kuri no atsauces punktiem fiksētas atlīdzības plānā ir jālieto kā Atskaites punkts.  Atskaites punkts tiek izmantots, lai aprēķinātu darbinieka algas koeficientu.  
24. Laukā Atskaites punkts ievadiet vai atlasiet kādu vērtību.
25. Aizvērt lapu.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Izveidot piemērotības kārtulu jaunajam fiksētas atlīdzības plānam
    * Jauno fiksētas atlīdzības plānu kādam darbiniekam var piešķirt tikai pēc tam, kad šim plānam ir definētas piemērotības kārtulas.  
1. Noklikšķiniet uz Piemērotības kārtulas.
2. Noklikšķiniet uz Jauns.
3. Laukā Piemērotība ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Spēkā stāšanās datums ievadiet kādu datumu.
    * Piemērotības kārtulas tiek lietotas gan fiksētās, gan mainīgās atlīdzības plāniem.  Laukā Tips atlasiet, kura tipa plānam ir paredzēta šī piemērotības kārtulu kopa.  
6. Laukā Plāns ievadiet vai atlasiet kādu vērtību.
    * Atlasiet kritērijus, kādiem darbiniekam ir jāatbilst, lai darbinieks būtu piemērots šim atlīdzību plānam. Kritēriji var ietvert faktorus Nodaļa, Arodbiedrība, Atrašanās vieta (Atlīdzības reģions), Darbs, Funkcija, Darba tips vai Atlīdzības līmenis. Lai darbinieks būtu piemērots atlīdzību plānam, šim darbiniekam ir jāatbilst visiem norādītajiem kritērijiem. Ja nav norādīts neviens kritērijs, šim atlīdzību plānam ir piemēroti visi darbinieki. Ja darbinieks neatbilst piemērotības kārtulās norādītajiem kritērijiem vai kādam atlīdzību plānam nav norādīta piemērotības kārtula, tad šis atlīdzību plāns netiks parādīts uzmeklēšanā, kad darbiniekam tiek veidots Fiksētas atlīdzības ieraksts.  
7. Aizvērt lapu.
8. Aizvērt lapu.


