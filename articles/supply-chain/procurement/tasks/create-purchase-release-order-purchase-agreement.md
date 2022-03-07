---
title: Pirkšanas līguma lietošana, veidojot pirkšanas pasūtījumu
description: Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.
author: Henrikan
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130524dc8e0c8724e35bf13c6b250ab721383711
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570373"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Pirkšanas līguma lietošana, veidojot pirkšanas pasūtījumu

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu. Pirkšanas līgums jālieto, veidojot pirkšanas pasūtījumu, jo pastāv vispārīgi nosacījumi, kas jāiekopē pirkšanas pasūtījuma virsrakstā. Šo uzdevumu parasti veic pirkšanas aģents. Kā šī ceļveža priekšnosacījums, jums jābūt spēkā pirkšanas līgumam ar uz preču daudzumu attiecināmam saistībām kreditoram un krājumiem. To pašu procedūru var izmantot, ja ir pirkšanas līgums ar cita veida saistībām.

## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

1. Dodieties uz **Ražošana un avoti \> Darbvietas \> Pirkšanas pasūtījumu sagatavošana**.
1. Darbību rūtī atlasiet **Jauns pirkšanas pasūtījums**.
1. Atveras dialogs **Izveidot pirkšanas pasūtījumu**. Atlasiet **Kreditora konts**. Pēc nepieciešamības pārbaudiet un koriģējiet citus adreses laukus.
1. Izvērsiet kopsavilkuma cilni **Vispārīgi**.
1. Laukā **Pirkšanas līgums** atrodiet un atlasiet efektīvu līgumu, kuru vēlaties izmantot. Visi pieejamie kreditora līgumi ir uzskaitīti šeit.  
1. Atlasiet **Jā**.
1. Atlasiet **Labi**.

## <a name="add-a-line"></a>Pievienot rindiņu

1. Laukā **Krājuma kods** ierakstiet vērtību. Ja saistībās ir noteikta krājumu vai novietojuma dimensijas, lai izmantotu līgumu, tās pašas vērtības ir jāievada pirkšanas pasūtījuma rindā.
1. Laukā **Vieta** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanas logu. Vieta var jau būt aizpildīta ar noklusēto vērtību no pasūtījuma vai kreditora. Ja tā notiek, izlaidiet šo darbību.  
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Laukā **Daudzums** ierakstiet kādu skaitli. Pārbaudiet, vai no saistībām tiek nokopēta cena.  

## <a name="look-up-the-commitment"></a>Saistību uzmeklēšana

1. Atlasiet **Atjaunināt rindu**.
1. Atlasiet **Pievienots**. Šeit var saņemt detalizētu informāciju par pirkšanas līgumu. Piemēram, jūs varat redzēt cenu un vai cena un atlaide ir fiksētas, kas nozīmē, ka, mainot cenu vai atlaidi pirkšanas pasūtījumā uz citu vērtību, nekā saistībās, sistēma noņems saiti, lai pirkšanas pasūtījuma rinda neizpildītu saistības. Varat apskatīt arī, vai ir atlasīta opcija Sasniegts maksimums, kas nozīmē, ka saistību daudzumu nevar pārsniegt, summējot visus pirkumus, kas izpilda saistības.  
1. Aizvērt lapu.

## <a name="look-up-the-purchase-agreement"></a>Pirkšanas līguma uzmeklēšana

1. **ADarbību rūtī** atlasiet **Vispārīgi**.
1. Atlasiet **Pirkšanas līgums**.
1. Aizvērt lapu.
1. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]