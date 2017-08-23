--- 
title: "Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma"
description: "Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu."
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ee4bec20fa2449aaa961ab19891a002702174446
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu. Pirkšanas līgums jālieto, veidojot pirkšanas pasūtījumu, jo pastāv vispārīgi nosacījumi, kas jāiekopē pirkšanas pasūtījuma virsrakstā. Šo uzdevumu parasti veic pirkšanas aģents. Kā šī ceļveža priekšnosacījums, jums jābūt spēkā pirkšanas līgumam ar uz preču daudzumu attiecināmam saistībām kreditoram un krājumiem. To pašu procedūru var izmantot, ja ir pirkšanas līgums ar cita veida saistībām. Šo ceļvedi varat izpildīt demonstrācijas datu uzņēmumā USMF. Ja jūs izmantojat USMF, vispirms var palaist ceļvedi "Pirkšanas līguma izveide", lai iestatītu šim ceļvedim vajadzīgos priekšnoteikumus.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Atveriet pirkšanas pasūtījumu sagatavošanas darbvietu.
2. Noklikšķiniet uz Jauns pirkšanas pasūtījums.
3. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Pārslēdziet sadaļas Vispārīgi paplašinājumu.
7. Laukā Pirkšanas līgums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Visi pieejamie kreditora līgumi ir uzskaitīti šeit. Atrodiet efektīvo līgumu, kuru vēlaties izmantot.  
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz Jā.
10. Noklikšķiniet uz OK.

## <a name="add-a-line"></a>Rindas pievienošana
1. Laukā Krājuma kods ierakstiet kādu vērtību.
    * Ja saistībās ir noteikta krājumu vai novietojuma dimensijas, lai izmantotu līgumu, tās pašas vērtības ir jāievada pirkšanas pasūtījuma rindā.  
2. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Vieta var jau būt aizpildīta ar noklusēto vērtību no pasūtījuma vai kreditora. Ja tā notiek, izlaidiet šo darbību.  
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Daudzums ievadiet skaitli.
    * Pārbaudiet, vai no saistībām tiek nokopēta cena.  

## <a name="look-up-the-commitment"></a>Saistību uzmeklēšana
1. Noklikšķiniet uz Labot rindu.
2. Noklikšķiniet uz Piesaistīts.
    * Šeit var saņemt detalizētu informāciju par pirkšanas līgumu. Piemēram, jūs varat redzēt cenu un vai cena un atlaide ir fiksētas, kas nozīmē, ka, mainot cenu vai atlaidi pirkšanas pasūtījumā uz citu vērtību, nekā saistībās, sistēma noņems saiti, lai pirkšanas pasūtījuma rinda neizpildītu saistības. Varat apskatīt arī, vai ir atlasīta opcija Sasniegts maksimums, kas nozīmē, ka saistību daudzumu nevar pārsniegt, summējot visus pirkumus, kas izpilda saistības.  
3. Aizvērt lapu.

## <a name="look-up-the-purchase-agreement"></a>Pirkšanas līguma uzmeklēšana
1. Darbību rūtī noklikšķiniet uz Vispārīgi.
2. Noklikšķiniet uz Pirkšanas līgums.
3. Aizvērt lapu.
4. Aizvērt lapu.


