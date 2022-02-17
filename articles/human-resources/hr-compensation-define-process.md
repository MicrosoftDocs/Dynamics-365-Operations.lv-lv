---
title: Atlīdzības procesa definēšana un rezultātu aprēķināšana
description: Kompensācijas procesi tiek izmantoti, lai noteiktu jaunas atlīdzības summas un piemaksas darbiniekiem, kas reģistrēti fiksētās un mainīgās atlīdzības plānos.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 188a87f580c274e073710601ef306139f723c797
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071726"
---
# <a name="define-compensation-process-and-calculate-results"></a>Atlīdzības procesa definēšana un rezultātu aprēķināšana


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensācijas procesi tiek izmantoti, lai noteiktu jaunas atlīdzības summas un piemaksas darbiniekiem, kas reģistrēti fiksētās un mainīgās atlīdzības plānos. Kompensācijas procesus var izmantot vairākas reizes, lai veiktu iespēju analīzi, lai pārbaudītu, vai visas izmaiņas un iestatījumi ir pareizi. Šīs procedūras ietvaros tiks izveidots atlīdzības process, tiks palaists process un skatīti rezultāti. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.


## <a name="create-a-compensation-process"></a>Atlīdzības procesa izveide
1. Dodieties uz **Kompensāciju pārvaldība**  > **Process**  > **Kompensāciju procesi**.
2. Noklikšķiniet uz **Jauns kompensācijas process**.
3. Laukā **Procesa lauks** ievadiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Procesa veids** atlasiet opciju.
    * Cikls norāda laika periodu, kas tiek vērtēts, lai noteiktu atlīdzību. Novērtējumā tiek ņemti vērā šādi aspekti: darbinieku ieņemtie amati, iekļaujamie veiktspējas vērtējumi, procentuālās attiecības aprēķins laikam, kurā darbinieks bija nodarbināts cikla ietvaros, un citi. Cikla sākuma datuma piemērs var būt pagājušā finanšu gada pirmā diena.  
6. Laukā **Cikla sākums** ievadiet datumu.
    * Cikla beigu datums ir svarīgs, jo tas ir datums, kuru izmanto, lai noteiktu, kuri darba ņēmēji tika aktīvi nodarbināti un reģistrēti vienam vai vairākiem atlīdzību plāniem.  
7. Laukā **Cikla beigas** ievadiet datumu.
    * Darbības aktīvais datums ir datums, kurā jāstājas spēkā janajām atlīdzības likmēm. Daudzi uzņēmumi ietver dažus mēnešus starp cikla beigām un laiku, kad stājas spēkā jaunās atlīdzības likmes. Papildu laiks tiek izmantots jaunās atlīdzības apstrādei un pārskatīšanai.  
8. Laukā **Transakcijas aktīvais datums** ievadiet datumu.
    * Algas datums tiek izmantots mainīgās atlīdzības plāniem, kuri nosaka darbinieka piemaksas summu, balstoties uz to atlīdzības likmēm attiecīgajā brīdī.  
    * Fiksētās algas proporcionālais nomas datums tiek izmantots fiksētas atlīdzības plāniem ar nomas noteikumu **Procenti**. Darbinieki, kuri ir pieņemti darbā starp cikla sākuma datumu un fiksētās maksas likmes nolīgšanas datumu, saņems 100 % no aprēķinātā atlīdzības pieauguma, nevis proporcionāli sadalīto procentuālo vērtību.  
9. Laukā **Fiksētā samaksa uz nominālo līgšanas datumu** ievadiet datumu.
    * Pārskatīšanas termiņš ir datums, līdz kuram ir jāpārskata visi procesa rezultāti, lai tos varētu ielādēt darbinieka atlīdzības ierakstā pirms darbības aktīvā datuma. Šim laukam ir tikai informatīvs raksturs.  
10. Laukā **Pārskata termiņš** ievadiet datumu.
11. Noklikšķiniet uz **Saglabāt**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Izveidojiet kompensācijas plānus un darbības kompensācijas procesam
1. Noklišķiniet uz **Iestatījumi**.
    * Lapu **Iestatījumi** izmanto, lai atlasītu, kurus plānus apstrādāt kā daļu no šī atlīdzību procesa, kā arī kuras darbības vajadzētu veikt saistībā ar katru plānu.  
2. Laukā **Plāns** ievadiet vai atlasiet kādu vērtību.
3. Noklikšķiniet uz **Saglabāt**.
4. Noklikšķiniet uz **Pievienot**.
5. Laukā **Darbība** atlasiet darbības veidu **Kapitāls**.
6. Noklikšķiniet uz **Pievienot**.
7. Laukā **Darbība** atlasiet darbības veidu **Palielinājums par nopelniem**.
    * Atlīdzību darbības var savienot kopā, izmantojot lauku **Izmantot iepriekšējo rezultātu**, lai norādītu, vai atlasītājai darbībai vajadzētu izmanto darbinieku bāzes samaksu vai iepriekšējās darbības rezultātu kā šīs darbības aprēķina sākumpunktu.  
8. Izvēlieties **Jā** iekš **Izmantojiet iepriekšējo rezultātu** lauks.
9. Noklikšķiniet uz **Pievienot**.
10. Laukā **Darbība** atlasiet darbības veidu **Vispārīgi**.
    * Dažādi atlīdzības darbību tipi iespējo dažādus laukus. Darbības tipam Vispārīgi var norādīt palielinājuma procentus vai palielinājuma summu.  
11. Atlasiet opciju **Atlasīt pieauguma daudzumu**.
12. Laukā **Pieauguma daudzums** ievadiet skaitu.
13. Noklikšķiniet uz **Pievienot**.
14. Laukā **Darbība** atlasiet darbības veidu **Paaugstinājums**.
    * Darbības tipi Paaugstināšana amatā vai Citu līmeņu maiņa ļauj lietotājiem veikt manuālas darbinieku atlīdzības korekcijas. Šiem darbību tipiem, kā arī citiem darbību tipiem var iespējot ieteikumus, lai jūs varētu ievadīt darbiniekam jaunu rekomendētās atlīdzības vērtību.  
15. Noklikšķiniet uz **Pievienot**.
16. Atlasiet opciju laukā **Tips**.
    * Fiksētās un mainīgās atlīdzības plānus var izmantot vienā un tajā pašā atlīdzības procesā.  
17. Laukā **Plāns** ievadiet vai atlasiet kādu vērtību.
    * Izmantojiet aizzīmes lodziņu **Iespējot samaksu par sniegumu**, lai noteiktu, vai fiksētās un mainīgās atlīdzību summas vajadzētu pielāgot, pamatojoties darbinieka snieguma novērtējumā.  
    * Līdzekļus var ignorēt mainīgās atlīdzības plānos.  
18. Noklikšķiniet uz **Saglabāt**.
19. Noklikšķiniet uz **Pievienot**.
20. Aizvērt lapu.

## <a name="run-the-compensation-process"></a>Atlīdzības procesa palaišana
1. Noklikšķiniet **Palaist procesu**.
    * Vadīkla **Rādīt apstrādes rezultātus** ļauj skatīt apstrādes ziņojumus visam kompensāciju procesam, kad apstrāde ir pabeigta.  
2. Laukā **Rādīt apstrādes rezultātus** atlasiet **Jā**.
3. Noklikšķiniet uz **Labi**.

## <a name="view-the-results"></a>Rezultātu skatīšana
1. Noklikšķiniet uz **Procesa rezultāti**.
2. Noklikšķiniet uz **Darbinieka rezultāti**.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Paplašiniet **Fiksēta kompensācija** sadaļā.
    * Izvērsiet kopsavilkuma cilnes, lai skatītu procesa rezultātus. Ja opcija **Iespējot ieteikumus** tika atzīmēta atlīdzību darbībai, šai darbībai tiks iespējoti **Ieteikumu** lauki.  
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Viena darbinieka rezultātus var skatīt, noklikšķinot uz pogas **Skatīt rezultātus**.  
    * Ir iespējams pārrakstīt aprēķināto atlīdzības summu, noregulējot procentus vai palielinot summu laukos **Ieteikumi**.  
6. Laukā **Ieteicamie procenti** ievadiet skaitu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Laukā **Ieteicamie procenti** ievadiet skaitu.
    * Pārrēķināšanu var izmantot, lai ignorētu visas esošajā ierakstā veiktās izmaiņas un ģenerētu jaunu atlīdzības rezultātu atlasītajam darbiniekam.  
    * Kad visas izmaiņas saistībā ar darbinieku ir pabeigtas, nomainiet statusu uz **Apstiprināts**.  
9. Noklikšķiniet uz **Mainīt statusu**.
10. Noklikšķiniet uz **Apstiprināts**.
    * Pēc ieraksta apstiprināšanas to var ielādēt darbinieka oficiālajā atlīdzības ierakstā. Jaunā atlīdzība stājas spēkā darbības datumā, kas iestatīts kompensācijas procesā.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
