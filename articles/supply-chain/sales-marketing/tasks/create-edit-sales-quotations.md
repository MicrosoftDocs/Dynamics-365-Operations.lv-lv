---
title: Pārdošanas piedāvājumu izveide un labošana
description: Šajā procedūrā ir parādīts, kā izveidot un atjaunināt pārdošanas piedāvājumu.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ddad2814915e14821f03efda72858d9a57f2d4e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204405"
---
# <a name="create-and-edit-sales-quotations"></a>Pārdošanas piedāvājumu izveide un labošana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot un atjaunināt pārdošanas piedāvājumu. Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.


## <a name="create-a-sales-quotation"></a>Pārdošanas piedāvājuma izveidošana
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi pārdošanas piedāvājumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Konta tips** atlasiet 'Potenciālais klients'.
4. Laukā **Potenciālais klients** ievadiet vai atlasiet kādu vērtību.
5. Izvērsiet sadaļu **Vispārīgi**. Ta kā jūs izvēlējāties izveidot piedāvajumu no Pārdošanas un mārketinga zonas, tips tiek automātiski iestatīts uz 'Pārdošanas piedāvājums'. Lai izveidotu piedāvājumu projektam, tam ir jāpiekļūst no moduļa **Projektu vadība un uzskaite**.
6. Noklikšķiniet uz **Labi**. Lauki un darbības piedāvājuma rindās ir ļoti līdzīgi laukiem un darbībām pārdošanas pasūtījuma rindās.   Tāpat kā pārdošanas pasūtījumus arī piedāvājumus var izveidot noteiktam krājumam, vai arī gadījumā, ja krājuma numurs nav zināms vai nepastāv piedāvājuma izveides laikā, piedāvājumus var izveidot pārdošanas kategorijai.     
7. Laukā **Krājums** ievadiet vai atlasiet kādu vērtību.
8. Laukā **Vieta** ievadiet vērtību.
9. Laukā **Daudzums** ierakstiet kādu skaitli. Ja rindā atlasītajam krājumam ir derīgi tirdzniecības līgumi, piemērojamā cena un atlaides automātiski tiks kopētas uz piedāvājuma rindu. Pārliecinieties, ka laukā Vienības cena ir vērtība, un, ja vēlaties, varat ievadīt arī atlaižu vērtības. 
10. Noklikšķiniet uz **Saglabāt**.
11. **Darbību rūtī** noklikšķiniet uz vienuma **Pārdošanas piedāvājums**.
12. Noklikšķiniet uz **Kopsummas**.
13. Noklikšķiniet uz **Labi**.
14. Atlasiet pārdošanas piedāvājuma rindu.
15. **Darbību rūtī** noklikšķiniet uz **Piedāvājums**.
16. Noklikšķiniet uz **Cenu simulācija**.
    - Lapā **Izpildīt cenu simulāciju** varat eksperimentēt ar piedāvājuma prognozēto ieņēmumu vai ienesīguma pielāgošanu, balstoties uz vēlamo vienības cenu, atlaides summu, atlaidi procentos, kopējo summu, uzcenojumu vai seguma summas normu. Kad esat apmierināts ar mērķa rādītājiem, piemērojiet priekšlikumu piedāvājuma rindai, un tās ar cenu saistītie lauki tiks attiecīgi atjaunināti.  
    - Varat izveidot tik daudz cenu simulāciju, cik vēlaties. Noklikšķinot uz **Jauns**, lapā tiek kopēti cenu nosacījumi no pašreizējās piedāvājuma rindas. Jūs varat pārveidot vērtības visos ar cenu saistītajos laukos uz mērķvērtībām. Izmaiņas vienā no laukiem izraisīs pārrēķinu visos pārējos laukos. Lai sistēma aprēķinātu seguma summu un seguma summas normu, ir jābūt zināmām preces vienības izmaksām. Lietojiet cilni Simulētās cenas, lai iegūtu detalizētu skatījumu par sākotnējām cenām, ierosinātajām izmaiņām un to ietekmi uz piedāvājumu kopsummām. Parasti, ja simulācija, ar kuru tiek noteikta jauna summa, tiek izmantota piedāvājuma rindā, sistēma pārrēķina un ievada jaunu vērtību laukā Vienības cena. Ja simulācija ir balstīta uz jaunu seguma summu vai jaunu seguma summas normu, tiek atjaunināts tikai lauks Neto summa un lauks Vienības cena ir tukšs. Abos gadījumos visas atlaides, kas bija piedāvājuma rindā pirms simulācijas, tiks dzēstas.
17. **Darbību rūtī** noklikšķiniet uz **Piedāvājums**.
18. Noklikšķiniet uz **Sūtīt piedāvājumu**.
19. Laukā **Drukāt piedāvājumu** atlasiet 'Jā'.
20. Noklikšķiniet uz **Labi**. Pārskata izveidošana var aizņemt kādu laiku. Neaizveriet lapu, līdz tā aizveras pati.

## <a name="update-a-sales-quotation"></a>Pārdošanas piedāvājuma labošana
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi pārdošanas piedāvājumi**.
2. **Darbību rūtī** noklikšķiniet uz **Sekošana**.
3. Noklikšķiniet uz **Pārvērst par debitoru**.
4. Laukā **Debitora konts** ierakstiet kādu vērtību.
5. Noklikšķiniet uz **Pārbaudīt**. Pārliecinieties, ka tiek parādīts ziņojums, ka ierakstītais konta numurs ir pieejams izmantošanai.  
6. Noklikšķiniet uz **Labi**. Sistēma ir izveidojusi jaunu debitora kontu potenciālajam klientam piedāvājumā.  
7. Aizvērt lapu.
8. **Darbību rūtī** noklikšķiniet uz **Sekošana**.
9. Noklikšķiniet uz **Apstiprināt**.
10. Laukā **Iemesls** ievadiet vai atlasiet vērtību.
11. Noklikšķiniet uz **Labi**.
12. **Darbību rūtī** noklikšķiniet uz **Vispārīgi**.
13. Noklikšķiniet uz **Pārdošanas pasūtījumi**.
14. Aizvērt lapu.

