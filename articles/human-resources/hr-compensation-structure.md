---
title: Atlīdzības organizācijas izstrāde
description: Šajā tēmā aprakstīts, kā izveidot fiksētu atlīdzības plānu un reǵistrēt darbiniekus plānam, izmantojot piemērotības kārtulas.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec30d6259b755bf7c304e8796b32d373027ce7ff
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483956"
---
# <a name="develop-a-compensation-structure"></a>Atlīdzības organizācijas izstrāde

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts, kā izveidot fiksētu atlīdzības plānu un reǵistrēt darbiniekus plānam, izmantojot piemērotības kārtulas. Šajā rakstā tiek izmantoti USMF demonstrācijas dati, un tie attiecas uz atlīdzību un atvieglojumu pārvaldniekiem.

## <a name="create-a-fixed-compensation-plan"></a>Fiksētās atlīdzības plāna izveide

1. Atlasiet **Kompensāciju pārvaldība**.

2. Atlasiet **Fiksētu atlīdzību plāni**.

3. Atlasiet **Jauns**.

4. Laukā **Plāns** ievadiet vērtību.

5. Laukā **Apraksts** ievadiet kādu vērtību.

6. Laukā **Spēkā stāšanās datums** ievadiet datumu.

7. Laukā **Tips** atlasiet, vai šis fiksētas atlīdzības plāns ir **Joslas**, **Līmeņa** vai **Pakāpes** plāns.

8. Izvēles rūtiņa **Ieteikšana atļauta** darbojas kā noklusējuma vērtība visām darbībām, kas šim plānam tiek pievienotas apstrādes notikumā. Ja ieteikšana ir atļauta, atlīdzības apstrādāšanas laikā varat ignorēt aprēķināto vadlīniju summu.

9. Lauks **Tolerance ārpus diapazona** jums ļauj norādīt, kā vēlaties apstrādāt atlīdzības summas, kuras attiecīgajam līmenim neietilpst norādītajā atlīdzību struktūras diapazonā. Iestatot lauku **Tolerance ārpus diapazona** uz **Nav**, varat izmantot jebkuru atlīdzības summu. **Nestingrā tolerance** brīdina lietotājus, ja atlīdzības summa ir mazāka par minimālo atsauces punkta summu attiecīgajam līmenim vai lielāka par maksimālo atsauces punktu summu šim līmenim. Lietotāji var ignorēt šo brīdinājumu un turpināt. **Stingrā tolerance** ģenerē kļūdu, kad darbinieka atlīdzība tiek iestatīta ārpus minimālā un maksimālā atsauces punkta diapazona attiecīgajam līmenim, un darbinieka atlīdzība tiek automātiski pielāgota, lai ietilptu diapazonā.

10. Lauks **Nolīgšanas kārtula** aprēķina darbinieka atlīdzību procesa notikuma laikā. **Nolīgšanas kārtula** **Procenti** aprēķina palielinājumu, kas ir proporcionāli sadalīts laika ilgumam, kādu darbinieks ir bijis nodarbināts attiecīgajā ciklā.

11. Laukā **Valūta** ierakstiet vērtību.

12. Laukā **Apmaksas likmes konvertēšana** ievadiet vai atlasiet kādu vērtību.

13. Izvērsiet sadaļu **Diapazona lietojuma matrica**. Pēc izvēles pievienojiet diapazona izmantošanas ierakstus, lai darbinieki līdz savam viduspunktam nokļūtu ātrāk un tiktu kavēta darbinieku diapazona maksimuma sasniegšana.

14. Atlasiet **Saglabāt**. Tas aktivizē pogu **Atlīdzības iestatīšana** un turpina definēt jūsu atlīdzības organizāciju plānam.

15. Atlasiet **Atlīdzības iestatīšana**. Varat izveidot atlīdzības organizāciju, izmantojot vienu no šīm trim metodēm:

    - Izveidojiet pilnīgi jaunu struktūru, atlasot atsauces punktu kopu un pievienojot līmeņus, lai izveidotu pats savu struktūru.
    - Kādu atlīdzību struktūru no jau esoša plāna kopējiet kā sākuma punktu un to pārveidot jaunajam plānam.
    - Atlasiet jau esošu atlīdzību režģi. Ja atlīdzību režģi jau izmanto cits plāns, šis plāns arī atspoguļo jebkādas izmaiņas, kas izdarītas režģim.

16. Atlasiet **Izveidot jaunu no jau esošas atlīdzības matricas**.

17. Laukā **Kopēt no režģa** ievadiet vai atlasiet kādu vērtību. Ja vēlaties, varat mainīt nosaukumu jaunajam atlīdzību režģim, ko izveidojat, kopējot atlasīto režģi.

18. Atlasiet **Labi**.

19. Atlasiet **Masveida izmaiņas**. **Masveida izmaiņas** jums ļauj uzturēt atlīdzību matricas summas, lietojot procentuālus vai fiksētus summas pieaugumus vienam vai vairākiem līmeņiem vai atsauces punktiem.

20. Laukā **Korekcijas summa** ievadiet kādu skaitli.

21. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.

22. Noklikšķiniet uz **Piemērot režģim**.

23. Aizvērt lapu. Kad izveidojat atlīdzību organizāciju, varat atlasīt, kuru no atsauces punktiem izmantot kā fiksētās atlīdzības plāna atskaites punktu. Atskaites punkts tiek izmantots, lai aprēķinātu darbinieka algas koeficientu.

24. Laukā **Atskaites punkts** ievadiet vai atlasiet kādu vērtību.

25. Aizvērt lapu.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Izveidot piemērotības kārtulu jaunajam fiksētas atlīdzības plānam

Varat piešķirt fiksētas atlīdzības plānu nodarbinātajam, līdz plānam ir definētas piemērotības kārtulas.  

1. Atlasiet **Piemērotības kārtulas**.

2. Atlasiet **Jauns**.

3. Laukā **Piemērotība** ievadiet vērtību.

4. Laukā **Apraksts** ievadiet kādu vērtību.

5. Laukā **Spēkā stāšanās datums** ievadiet datumu. Gan fiksēto, gan mainīgo atlīdzību plāni izmanto piemērotības kārtulas. Laukā **Veids** atlasiet plāna veidu.

6. Laukā **Plāns** ievadiet vai atlasiet kādu vērtību. Atlasiet kritērijus, kādiem darbiniekam ir jāatbilst, lai darbinieks būtu piemērots šim atlīdzību plānam. Kritēriji var ietvert:

    - **Nodaļa**
    - **Arodbiedrība**
    - **Atrašanās vieta** (**Atlīdzības reģions**)
    - **Darbs**
    - **Funkcija**
    - **Darba tips**
    - **Atlīdzības līmenis**
    
    Lai darbinieks būtu piemērots atlīdzību plānam, šim darbiniekam ir jāatbilst visiem norādītajiem kritērijiem. Ja nenorādāt kritērijus, visi nodarbinātie ir piemēroti atlīdzību plānam. Ja darbinieks neatbilst piemērotības kārtulās norādītajiem kritērijiem vai kādam atlīdzību plānam nav norādīta piemērotības kārtula, tad šis atlīdzību plāns netiks parādīts uzmeklēšanā, kad darbiniekam tiek veidots fiksētas atlīdzības ieraksts.

7. Aizvērt lapu.

8. Aizvērt lapu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
