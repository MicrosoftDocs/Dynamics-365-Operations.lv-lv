--- 
title: "Pārdošanas piedāvājumu izveide un labošana"
description: "Šajā procedūrā ir parādīts, kā izveidot un atjaunināt pārdošanas piedāvājumu."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a>Pārdošanas piedāvājumu izveide un labošana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot un atjaunināt pārdošanas piedāvājumu. Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.


## <a name="create-a-sales-quotation"></a>Pārdošanas piedāvājuma izveidošana
1. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Konta tips atlasiet Potenciālais klients.
4. Laukā Potenciālais klients ievadiet vai atlasiet kādu vērtību.
5. Izvērsiet sadaļu Vispārīgi.
    * Ta kā jūs izvēlējāties izveidot piedāvajumu no Pārdošanas un mārketinga zonas, tips tiek automātiski iestatīts uz Pārdošanas piedāvājums. Lai izveidotu piedāvājumu projektam, tam ir jāpiekļūst no projektu vadības un uzskaites moduļa.   
6. Noklikšķiniet uz OK.
    * Lauki un darbības piedāvājuma rindās ir ļoti līdzīgi laukiem un darbībām pārdošanas pasūtījuma rindās.   Tāpat kā pārdošanas pasūtījumus arī piedāvājumus var izveidot noteiktam krājumam, vai arī gadījumā, ja krājuma numurs nav zināms vai nepastāv piedāvājuma izveides laikā, piedāvājumus var izveidot pārdošanas kategorijai.  
7. Laukā Krājums ievadiet vai atlasiet kādu vērtību.
8. Laukā Krājums ierakstiet vērtību.
9. Aizvērt lapu.
10. Laukā Daudzums ievadiet skaitli.
    * Ja rindā atlasītajam krājumam ir derīgi tirdzniecības līgumi, piemērojamā cena un atlaides automātiski tiks kopētas uz piedāvājuma rindu. Pārliecinieties, ka laukā Vienības cena ir vērtība, un, ja vēlaties, varat ievadīt arī atlaižu vērtības.  
11. Noklikšķiniet uz Saglabāt.
12. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas piedāvājums.
13. Noklikšķiniet uz Kopsummas.
14. Noklikšķiniet uz OK.
15. Uzklikšķiniet uz Pārdošanas piedāvājuma rinda.
16. Klikšķiniet uz Cenas.
    * Lapā Izpildīt cenu simulāciju varat eksperimentēt ar piedāvājuma prognozēto ieņēmumu vai ienesīguma pielāgošanu, balstoties uz vēlamo vienības cenu, atlaides summu, atlaidi procentos, kopējo summu, uzcenojumu vai seguma summas normu.   Kad esat apmierināts ar mērķa rādītājiem, piemērojiet priekšlikumu piedāvājuma rindai, un tās ar cenu saistītie lauki tiks attiecīgi atjaunināti.  
    * Varat izveidot tik daudz cenu simulāciju, cik vēlaties. Noklikšķinot uz Jauns, lapā tiek kopēti cenu nosacījumi no pašreizējās piedāvājuma rindas. Jūs varat pārveidot vērtības visos ar cenu saistītajos laukos uz mērķvērtībām. Izmaiņas vienā no laukiem izraisīs pārrēķinu visos pārējos laukos. Lai sistēma aprēķinātu seguma summu un seguma summas normu, ir jābūt zināmām preces vienības izmaksām. Lietojiet cilni Simulētās cenas, lai iegūtu detalizētu skatījumu par sākotnējām cenām, ierosinātajām izmaiņām un to ietekmi uz piedāvājumu kopsummām.   Parasti, ja simulācija, ar kuru tiek noteikta jauna summa, tiek izmantota piedāvājuma rindā, sistēma pārrēķina un ievada jaunu vērtību laukā Vienības cena. Ja simulācija ir balstīta uz jaunu seguma summu vai jaunu seguma summas normu, tiek atjaunināts tikai lauks Neto summa un lauks Vienības cena ir tukšs. Abos gadījumos visas atlaides, kas bija piedāvājuma rindā pirms simulācijas, tiks dzēstas.  
17. Aizvērt lapu.
18. Darbību rūtī noklikšķiniet uz Piedāvājums.
19. Noklikšķiniet uz Sūtīt piedāvājumu.
20. Laukā Drukāt piedāvājumu atlasiet Jā.
21. Noklikšķiniet uz OK.
    * Pārskata izveidošana var aizņemt kādu laiku. Neaizveriet lapu, līdz tā aizveras pati.  
22. Aizvērt lapu.

## <a name="update-a-sales-quotation"></a>Pārdošanas piedāvājuma labošana
1. Darbību rūtī noklikšķiniet uz Sekošana.
2. Noklikšķiniet uz Pārvērst par debitoru.
3. Laukā Debitora konts ierakstiet kādu vērtību.
4. Noklikšķiniet uz Pārbaudīt.
    * Pārliecinieties, ka tiek parādīts ziņojums, ka ierakstītais konta numurs ir pieejams izmantošanai.  
5. Noklikšķiniet uz OK.
    * Sistēma ir izveidojusi jaunu debitora kontu potenciālajam klientam piedāvājumā.  
6. Aizvērt lapu.
7. Darbību rūtī noklikšķiniet uz Sekošana.
8. Noklikšķiniet uz Apstiprināt.
9. Laukā Pamatojums ievadiet vai atlasiet kādu vērtību.
10. Noklikšķiniet uz OK.
11. Darbību rūtī noklikšķiniet uz Vispārīgi.
12. Noklikšķiniet uz Pārdošanas pasūtījumi.
13. Aizvērt lapu.


