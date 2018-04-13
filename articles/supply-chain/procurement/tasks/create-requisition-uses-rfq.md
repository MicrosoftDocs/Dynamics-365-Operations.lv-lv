--- 
title: "Pieprasījuma izveide, kas lieto PP"
description: "Šajā ceļvedī ir parādīts, kā pirkšanas pieprasījumam pievienot cenas un kreditora informāciju no IP procesa."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Pieprasījuma izveide, kas lieto PP

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā ceļvedī ir parādīts, kā pirkšanas pieprasījumam pievienot cenas un kreditora informāciju no IP procesa. Šajā ceļvedī parādīto piemēru var izmantot ar uzņēmuma USMF demonstrācijas datiem, un jums ir jāpiesakās kā administratoram, lai izpildītu visas darbības. Šajā ceļvedī aprakstītos uzdevumus parasti veiktu sagādes speciālisti.


## <a name="create-a-requisition"></a>Izveidot pieprasījumu
1. Pārejiet uz sadaļu Sagāde un avoti > Pirkuma pieprasījumi > Mani sagatavotie pirkšanas pieprasījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Laukā Pieprasītais datums ievadiet datumu.
5. Laukā Uzskaites datums ievadiet datumu.
6. Noklikšķiniet uz Labi.
7. Laukā Pamatojums ievadiet vai atlasiet kādu vērtību.
8. Noklikšķiniet uz Pievienot rindu.
9. Lauka Sagādes kategorija koka struktūrā atlasiet kādu kategoriju un noklikšķiniet uz Labi.
10. Laukā Preces nosaukums ierakstiet vērtību.
11. Laukā Daudzums ievadiet skaitli.
12. Laukā Vienība ievadiet vai atlasiet kādu vērtību.
13. Noklikšķiniet uz Saglabāt.
14. Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.
15. Klikšķiniet Iesniegt.
16. Aizvērt lapu.
17. Klikšķiniet Iesniegt.

## <a name="reassign-a-workflow-task"></a>Darbplūsmas uzdevuma piešķires maiņa
    * Nākamais uzdevums ir izveidot IP, lai no kreditoriem saņemtu piedāvājumus par preci. USMF demonstrācijas datos pieprasījuma darbplūsma ir iestatīta ar kārtulu, tāpēc, ja nav atlasīts kreditors vai ja vienības cena kādai rindai ir 0, konkrētam nodarbinātajam tiek piešķirts uzdevums izveidot IP. Lai turpinātu ar šo ceļvedi, šis uzdevums ir jāpiešķir citam lietotājam (sev). To varat izdarīt tikai tad, ja esat pieteicies kā Administrators.  
1. Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.
2. Noklikšķiniet uz Skatīt vēsturi.
3. Atsvaidziniet lapu.
4. Izvērsiet sadaļu Izsekošanas detaļas.
5. Koka struktūrā atlasiet vienumu “rinda, kas sākas ar “Rindas darbplūsma aktivizēta””.
6. Noklikšķiniet uz Skatīt darbplūsmas detaļas.
7. Izvērsiet sadaļu Darba vienumi.
8. Noklikšķiniet uz Mainīt piešķiri.
9. Laukā Lietotājs atlasiet vienumu Administrators.
10. Noklikšķiniet uz Mainīt piešķiri.
11. Aizvērt lapu.
12. Aizvērt lapu.

## <a name="create-an-rfq"></a>Izveidot PP
1. Atsvaidziniet lapu.
2. Noklikšķiniet uz Piedāvājuma pieprasījums.
3. Laukā Pērkošā juridiskā persona atlasiet USMF.
    * Jums ir jāatlasa tā pati juridiskā persona, kas ir norādīta pieprasījuma rindā.  
4. Sarakstā atzīmējiet atlasīto rindu.
    * Ja jūsu pirkšanas pieprasījumā bija vairākas rindas, atlasiet visas tās rindas, kuras vēlaties pievienot šim IP.  
5. Noklikšķiniet uz OK.
6. Atsvaidziniet lapu.
7. Atveriet papildinformāciju un pēc tam izvērsiet sadaļu Saistītie dokumenti.
    * Iespējams, jums jau ir atvērta papildinformācija. Meklējiet ikonu, uz kuras ir bultiņa, pa labi no rindu/virsrakstu pārslēgšanas pogām. Ja bultiņa norāda pa labi, tad papildinformācija jau ir atvērta. Ja bultiņa norāda pa kreisi, noklikšķiniet uz tās, lai atvērtu papildinformāciju.  
8. Noklikšķiniet uz saites laukā Piedāvājuma pieprasījums, lai atvērtu tikko izveidoto IP.
9. Noklikšķiniet uz Virsraksts.
10. Noklikšķiniet uz Pievienot.
11. Ievadiet vai atlasiet vērtību laukā kreditora konts.
12. Noklikšķiniet uz Pievienot.
13. Ievadiet vai atlasiet vērtību laukā kreditora konts.
14. Noklikšķiniet uz Sūtīt.
15. Noklikšķiniet uz OK.
16. Noklikšķiniet uz Ievadīt atbildi.
17. Darbību rūtī noklikšķiniet uz Atbilde.
18. Noklikšķiniet uz Kopēt datus uz atbildēm.
    * Šādi no IP uz atbildi tiek kopēti dati, piemēram, daudzums un datumi.  
19. Laukā Vienības cena ievadiet kādu skaitli.
    * Šī ir cena, ko saņēmāt no kreditora. Iespējams, vēlaties arī ievadīt papildinformāciju no kreditora.  
20. Noklikšķiniet uz Akceptēt.
21. Noklikšķiniet uz OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Pārliecinieties, ka uz pieprasījumu ir pārsūtīts kreditors un cena
1. Aizvērt lapu.
2. Noklikšķiniet uz Rindas.
3. Noklikšķiniet uz Saistītā informācija.
4. Noklikšķiniet uz Pirkšanas pieprasījums.
5. Atlasiet rindu, kura tika pārsūtīta uz IP.
    * Pārliecinieties, ka uz pieprasījumu ir pārkopēta cena un kreditors.  
6. Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.
7. Noklikšķiniet uz Pabeigt.
8. Aizvērt lapu.
9. Noklikšķiniet uz Pabeigt.


