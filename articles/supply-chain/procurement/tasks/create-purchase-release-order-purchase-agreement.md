---
title: Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma
description: Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.
author: kamaybac
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd3f837590cd7fe09ad385d0baac6c16fcf145d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812263"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu. Pirkšanas līgums jālieto, veidojot pirkšanas pasūtījumu, jo pastāv vispārīgi nosacījumi, kas jāiekopē pirkšanas pasūtījuma virsrakstā. Šo uzdevumu parasti veic pirkšanas aģents. Kā šī ceļveža priekšnosacījums, jums jābūt spēkā pirkšanas līgumam ar uz preču daudzumu attiecināmam saistībām kreditoram un krājumiem. To pašu procedūru var izmantot, ja ir pirkšanas līgums ar cita veida saistībām. Šo ceļvedi varat izpildīt paraugdatu uzņēmumā USMF. Ja jūs izmantojat USMF, vispirms var palaist ceļvedi "Pirkšanas līguma izveide", lai iestatītu šim ceļvedim vajadzīgos priekšnoteikumus.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. **Navigācijas rūtī** ejiet uz **Darbvietas > Pirkšanas pasūtījuma sagatavošana**. 
2. Klikšķiniet uz **Jauns pirkšanas pasūtījums**.
3. Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet kopsavilkuma cilni **Vispārīgi**.
7. Laukā **Pirkuma līgums** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai. Visi pieejamie kreditora līgumi ir uzskaitīti šeit. Atrodiet efektīvo līgumu, kuru vēlaties izmantot.  
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz pogas **Jā**.
10. Noklikšķiniet uz **Labi**.

## <a name="add-a-line"></a>Rindas pievienošana
1. Laukā **Krājuma kods** ierakstiet vērtību. Ja saistībās ir noteikta krājumu vai novietojuma dimensijas, lai izmantotu līgumu, tās pašas vērtības ir jāievada pirkšanas pasūtījuma rindā.  
2. Laukā **Vieta** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu. Vieta var jau būt aizpildīta ar noklusēto vērtību no pasūtījuma vai kreditora. Ja tā notiek, izlaidiet šo darbību.  
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā **Daudzums** ierakstiet kādu skaitli. Pārbaudiet, vai no saistībām tiek nokopēta cena.  

## <a name="look-up-the-commitment"></a>Saistību uzmeklēšana
1. Noklikšķiniet uz **Atjaunināt rindu**.
2. Noklikšķiniet uz **Pievienots**. Šeit var saņemt detalizētu informāciju par pirkšanas līgumu. Piemēram, jūs varat redzēt cenu un vai cena un atlaide ir fiksētas, kas nozīmē, ka, mainot cenu vai atlaidi pirkšanas pasūtījumā uz citu vērtību, nekā saistībās, sistēma noņems saiti, lai pirkšanas pasūtījuma rinda neizpildītu saistības. Varat apskatīt arī, vai ir atlasīta opcija Sasniegts maksimums, kas nozīmē, ka saistību daudzumu nevar pārsniegt, summējot visus pirkumus, kas izpilda saistības.  
3. Aizvērt lapu.

## <a name="look-up-the-purchase-agreement"></a>Pirkšanas līguma uzmeklēšana
1. **Darbību rūtī** noklikšķiniet uz **Vispārīgi**.
2. Klikšķiniet uz **Pirkuma līgums**.
3. Aizvērt lapu.
4. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]