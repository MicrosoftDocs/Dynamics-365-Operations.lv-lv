---
title: Atlīdzības procesa definēšana un rezultātu aprēķināšana
description: Kompensācijas procesi tiek izmantoti, lai noteiktu jaunas atlīdzības summas un piemaksas darbiniekiem, kas reģistrēti fiksētās un mainīgās atlīdzības plānos.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e5b0bb5558a8b71d02b5988c6f82f53f4f42646
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "325737"
---
# <a name="define-compensation-process-and-calculate-results"></a>Atlīdzības procesa definēšana un rezultātu aprēķināšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kompensācijas procesi tiek izmantoti, lai noteiktu jaunas atlīdzības summas un piemaksas darbiniekiem, kas reģistrēti fiksētās un mainīgās atlīdzības plānos. Kompensācijas procesus var izmantot vairākas reizes, lai veiktu iespēju analīzi, lai pārbaudītu, vai visas izmaiņas un iestatījumi ir pareizi. Šīs procedūras ietvaros tiks izveidots atlīdzības process, tiks palaists process un skatīti rezultāti. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-compensation-process"></a>Atlīdzības procesa izveide
1. Dodieties uz Personāla vadība > Atlīdzība > Process > Atlīdzības procesi.
2. Noklikšķiniet uz Jauns.
3. Laukā Process ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Procesu tips atlasiet opciju.
    * Cikls norāda laika periodu, kas tiek vērtēts, lai noteiktu atlīdzību. Novērtējumā tiek ņemti vērā šādi aspekti: darbinieku ieņemtie amati, iekļaujamie veiktspējas vērtējumi, procentuālās attiecības aprēķins laikam, kurā darbinieks bija nodarbināts cikla ietvaros, un citi. Cikla sākuma datuma piemērs var būt pagājušā finanšu gada pirmā diena.  
6. Ievadiet datumu laukā Cikla sākums.
    * Cikla beigu datums ir svarīgs, jo tas ir datums, kas tiek izmantots, lai noteiktu, kuri darbinieki tika aktīvi nodarbināti un reģistrēti vienā vai vairākos atlīdzības plānos.  
7. Ievadiet datumu laukā Cikla beigas.
    * Darbības aktīvais datums ir datums, kurā jāstājas spēkā janajām atlīdzības likmēm. Daudzi uzņēmumi ietver dažus mēnešus starp cikla beigām un laiku, kad stājas spēkā jaunās atlīdzības likmes. Papildu laiks tiek izmantots jaunās atlīdzības apstrādei un pārskatīšanai.  
8. Ievadiet datumu laukā Darbības aktīvais datums.
    * Algas datums tiek izmantots mainīgās atlīdzības plāniem, kuri nosaka darbinieka piemaksas summu, balstoties uz to atlīdzības likmēm attiecīgajā brīdī.  
    * Fiksētās maksas likmes nolīgšanas datums tiek izmantots ar fiksētās atlīdzības plāniem, ja nolīgšanas kārtulas vērtība ir Procenti.  Darbinieki, kuri ir pieņemti darbā starp cikla sākuma datumu un fiksētās maksas likmes nolīgšanas datumu, saņems 100 % no aprēķinātā atlīdzības pieauguma, nevis proporcionāli sadalīto procentuālo vērtību.  
9. Ievadiet datumu laukā Fiksētās maksas likmes nolīgšanas datums.
    * Pārskatīšanas termiņš ir datums, līdz kuram ir jāpārskata visi procesa rezultāti, lai tos varētu ielādēt darbinieka atlīdzības ierakstā pirms darbības aktīvā datuma. Šim laukam ir tikai informatīvs raksturs.  
10. Laukā Pārskatīt termiņu ievadiet kādu datumu.
11. Noklikšķiniet uz Saglabāt.

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a>Atlīdzības plānu un darbību atlīdzības procesam iestatīšana
1. Noklišķiniet uz Iestatījumi.
    * Lapa Iestatījumi tiek izmantota, lai atlasītu, kuri plāni tiks apstrādāti šī atlīdzības procesa ietvaros, kā arī kuras darbības jāveic attiecībā uz katru plānu.  
2. Laukā Plāns ievadiet vai atlasiet kādu vērtību.
3. Noklikšķiniet uz Saglabāt.
4. Noklikšķiniet uz Pievienot.
5. Laukā Darbība atlasiet darbības tipu Kapitāls.
6. Noklikšķiniet uz Pievienot.
7. Laukā Darbība atlasiet darbības tipu Nopelni.
    * Atlīdzības darbības var "saistīt" kopā, izmantojot lauku Izmantot iepriekšējo rezultātu, lai norādītu, vai atlasītajai darbībai jāizmanto darbinieku pamatalga vai iepriekšējās darbības rezultāts kā sākuma dati šīs darbības aprēķinam.  
8. Laukā Izmantot iepriekšējo rezultātu atlasiet Jā.
9. Noklikšķiniet uz Pievienot.
10. Laukā Darbība atlasiet darbības tipu Vispārīgi.
    * Dažādi atlīdzības darbību tipi iespējo dažādus laukus. Darbības tipam Vispārīgi var norādīt palielinājuma procentus vai palielinājuma summu.  
11. Atlasiet opciju Atlasīt pielikuma summu.
12. Laukā Palielināt summu ievadiet skaitli.
13. Noklikšķiniet uz Pievienot.
14. Laukā Darbība atlasiet darbības tipu Paaugstināšana amatā.
    * Darbības tipi Paaugstināšana amatā vai Citu līmeņu maiņa ļauj lietotājiem veikt manuālas darbinieku atlīdzības korekcijas. Šiem darbību tipiem, kā arī citiem darbību tipiem var iespējot ieteikumus, lai jūs varētu ievadīt darbiniekam jaunu rekomendētās atlīdzības vērtību.  
15. Noklikšķiniet uz Pievienot.
16. Atlasiet opciju laukā Tips.
    * Fiksētās un mainīgās atlīdzības plānus var izmantot vienā un tajā pašā atlīdzības procesā.  
17. Laukā Plāns ievadiet vai atlasiet kādu vērtību.
    * Izmantojiet izvēles rūtiņu Iespējot algu par rezultātiem, lai noteiktu, vai fiksētās un mainīgās atlīdzības summas ir jākoriģe, pamatojoties uz darbinieka veiktspējas vērtējumu.  
    * Līdzekļus var ignorēt mainīgās atlīdzības plānos.  
18. Noklikšķiniet uz Saglabāt.
19. Noklikšķiniet uz Pievienot.
20. Aizvērt lapu.

## <a name="run-the-compensation-process"></a>Atlīdzības procesa palaišana
1. Noklikšķiniet uz Palaist procesu.
    * Funkcija Rādīt apstrādes rezultātus ļauj apskatīt apstrādes ziņojumus par visu atlīdzības procesu, kad process ir pabeigts.  
2. Laukā Rādīt apstrādes rezultātus atlasiet Jā.
3. Noklikšķiniet uz OK.

## <a name="view-the-results"></a>Rezultātu skatīšana
1. Noklikšķiniet uz Procesa rezultāti.
2. Noklikšķiniet uz Darbinieku rezultāti.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Izvērsiet sadaļu Fiksēta atlīdzība.
    * Izvērsiet kopsavilkuma cilnes, lai skatītu procesa rezultātus. Ja atlīdzības darbībai tika atzīmēts Iespējot ieteikumus, attiecīgajai darbībai būs iespējoti lauki Ieteikumi.  
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Viena darbinieka rezultātus var skatīt, noklikšķinot uz pogas Skatīt rezultātus.  
    * Aprēķināto atlīdzības summu var pārrakstīt, koriģējot procentuālo vērtību vai palielinājuma summu laukos Ieteikumi.  
6. Rekomendējamās procentuālās vērtības laukā ievadiet skaitli.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Rekomendējamās procentuālās vērtības laukā ievadiet skaitli.
    * Pārrēķināšanu var izmantot, lai ignorētu visas esošajā ierakstā veiktās izmaiņas un ģenerētu jaunu atlīdzības rezultātu atlasītajam darbiniekam.  
    * Kad visas izmaiņas darbiniekam ir pabeigtas, mainiet statusu uz Apstiprināts.  
9. Noklikšķiniet uz Mainīt statusu.
10. Noklikšķiniet uz Apstiprināts.
    * Pēc ieraksta apstiprināšanas to var ielādēt darbinieka oficiālajā atlīdzības ierakstā. Jaunā atlīdzība stājas spēkā darbības datumā, kas iestatīts kompensācijas procesā.  

