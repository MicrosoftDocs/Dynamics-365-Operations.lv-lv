---
title: Izveidot piegādes grafiku
description: Šajā procedūrā ir parādīts, kā pārdošanas pasūtījumam izveidot piegādes grafiku.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa9539ce92297a3b4f22ac18af79fdea98759e49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991844"
---
# <a name="create-delivery-schedule"></a>Izveidot piegādes grafiku

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā pārdošanas pasūtījumam izveidot piegādes grafiku. Piegādes grafiks tiek izmantots, kad pasūtījumā vai piedāvājumā minēto daudzumu ir pieprasīts piegādāt vairākos sūtījumos. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="create-delivery-schedule"></a>Izveidot piegādes grafiku
1. Dodieties uz Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz Labi.
5. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
6. Laukā Daudzums ievadiet skaitli, kas ir lielāks par 1.
7. Noklikšķiniet uz Pārdošanas pasūtījuma rinda.
8. Noklikšķiniet uz Piegādes grafiks.
    * Lapa Piegādes grafiks ir vieta, kur varat norādīt sūtījumu skaitu, kādā debitoram tiks piegādāts viss pasūtījuma rindas daudzums.    
    * Pēc noklusējuma sistēma no sākotnējās pārdošanas rindas uz pirmo piegādes grafika rindu kopē kopējo daudzumu un citu piegādes informāciju. Šajā piemērā mēs izveidosim grafiku diviem sūtījumiem, un otrā sūtījuma datumam no pirmā būs nobīde par vienu nedēļu.  
9. Laukā Daudzums ievadiet skaitli, kas ir daļa no kopējā daudzuma.
10. Klikšķiniet Jauns.
11. Laukā Daudzums ievadiet atlikušo daudzumu.
12. Laukā Pieprasītais nosūtīšanas datums ievadiet datumu, kas ir par vienu nedēļu uz priekšu no pirmās piegādes rindas datuma.
    * Abas opcijas kopsavilkuma cilnē Izmaksu konvertēšana kontrolē veidu, kā šīs izmaksas jāsadala pa piegādes grafika rindām, kad tās ir piešķirtas sākotnējai pasūtījuma rindai. Ja atlasāt Kopēt bruto summas, tad uz katru rindu tiek kopēta tāda pati summa. Ar opciju Piešķirt piegādes rindām šīs izmaksas tiek vienmērīgi sadalītas pa piegādes rindām.  
    * Iespējams sadalīt tikai fiksētas izmaksas, bet mainīgās izmaksas joprojām tiks kopētas uz rindām.  
13. Pārvietojiet kursoru prom no otrās piegādes rindas, lai atjauninātu lapu.
    * Piegādes grafika rindām piešķirtajam kopējam daudzumam varat sekot līdzi, apskatot laukus Kopsumma un Atlicis. Ja atlikušais daudzums ir nulle, grafikam ir piešķirts viss daudzums no sākotnējās rindas.   
14. Noklikšķiniet uz OK.
    * Tagad piegādes grafiks ir kopēts uz pasūtījuma rindām.   
    * Sākotnējā pasūtījuma rinda, ko sauc par komerciālo rindu, ir pārvērsta par pasūtījuma rindu ar vairākām piegādēm. Tā ir atzīmēta ar atšķirīgu ikonu un darbojas kā piegādes rindu virsraksts.  
    * Abas jaunās rindas, sauktas par piegādes rindām, veido vienu piegādes grafiku. Pasūtījums tiks apstrādāts pret šīm rindām, nevis sākotnējo rindu. Ja tiek drukāti dokumenti, piemēram, apstiprinājuma pavadzīmes, izdošanas saraksti, pavadzīmes vai rēķini, tiek rādītas tikai piegādes rindas.   
    * Piegādes rindām var būt atšķirīgi piegādes datumi, daudzumi, piegādes režīmi un noliktavas dimensijas, piemēram, vieta un noliktava. Taču preču dimensijām vienmēr ir jāatbilst komerciālajā rindā norādītajām, un tās nevar mainīt.  
15. Laukā Daudzums ievadiet skaitli, kas ir lielāks par pašreizējo.
16. Atlasiet komerciālo rindu, lai redzētu daudzuma pārrēķināšanas ietekmi.
17. Darbību rūtī noklikšķiniet uz Izdot un iepakot.
18. Noklikšķiniet uz Grāmatot pavadzīmi.
19. Izvērsiet sadaļu Parametri.
20. Laukā Daudzums atlasiet vērtību Visi.
    * Ņemiet vērā, ka pavadzīme tiks izveidota abām piegādes grafika rindām, nevis sākotnējai pasūtījuma rindai.  
21. Laukā Drukāt pavadzīmi atlasiet Jā.
22. Noklikšķiniet uz OK.
23. Noklikšķiniet uz Jā.
24. Aizvērt lapu.
