---
title: Krājumu pieejamības pārbaude
description: Šajā procedūrā parādīts, kā pārbaudīt rīcībā esošos un fiziski rīcībā esošos krājumus noteiktam krājuma kodam.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d04abae36e144b429b8ebc73b4c110389fecd1f0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000163"
---
# <a name="check-the-availability-of-stock"></a>Krājumu pieejamības pārbaude

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā pārbaudīt rīcībā esošos un fiziski rīcībā esošos krājumus noteiktam krājuma kodam. Aprakstīts arī tas, kā iegūt piegādes informāciju, kas saistīta ar krājumu. Fiziskie rīcībā esošie krājumi ir rīcībā esoši krājumi, kas ir pieejami, tas ir, tie ir nopirkti, saņemti un reģistrēti. Rīcībā esošie krājumi ietver pieejamos rīcībā esošos krājumus, kā arī krājumus, kas ir pasūtīti un tiek gaidīti, bet vēl nav saņemti vai nav reģistrēti. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja izmantojat USMF varat izmantot piemēra vērtības, kas parādītas. Šos uzdevumus parasti veic noliktavas darbinieks.


## <a name="check-on-hand-inventory-for-an-item"></a>Krājuma rīcībā esošo krājumu pārbaude
1. Pārejiet uz **Navigācijas rūts > Moduļi > Krājumu vadība > Uzziņas un pārskati > Rīcībā esošie krājumi**.
2. Atlasiet rindu **Krājuma numurs**. Lai izpildītu vaicājumu rīcībā esošiem krājumiem pēc krājuma koda, atlasiet rindu, kur tabulai ir iestatīti **Rīcībā esošie krājumi** un laukā ir iestatīts **Krājuma kods**.
3. Laukā **Kritēriji** atlasiet krājumu, kuram vēlaties izpildīt vaicājumu. Ja lietojat demonstrācijas datu uzņēmumu USMF, varat atlasīt “M9201”.  
4. Noklikšķiniet uz **Labi**.
5. **Darbību rūtī** noklikšķiniet uz **Dimensijas**. Cilne **Dimensijas** ļauj atlasīt, cik daudz informācijas vēlaties redzēt par jūsu rīcībā esošajiem krājumiem. Ja jums ir nepieciešami dati, kas attiecas uz rezervāciju, ir jāattēlo visas krājumu dimensijas krājumiem, kas izmanto papildu noliktavas (WMS) procesus.
6. Noklikšķiniet uz **Labi**.
7. **Darbību rūtī** noklikšķiniet uz **Saistītā informācija**. Ja šī opcija nav redzama, iespējams, ir nepieciešams noklikšķināt uz elipses pogas (...), lai redzētu papildu Darbību rūts opcijas.
8. Noklikšķiniet uz **Piegādes pārskats**. Cilne **Piegādes pārskats** sniedz piegādes informāciju noteiktam krājumam, piemēram, rīcībā esošo daudzumu, izpildes laiku un kreditora informāciju.  
9. Izvērsiet sadaļu **Rīcībā esošs**.
10. Izvērsiet sadaļu **Piegādātāji**.
11. Aizvērt lapu.
12. Aizvērt lapu.

## <a name="check-physical-on-hand-inventory"></a>Fizisko rīcībā esošo krājumu pārbaude
1. Pārejiet uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Uzziņas un pārskati > Fiziskie rīcībā esošie krājumi**.
2. Laukā **Krājuma kods** ierakstiet vērtību. Laukus Vieta un Noliktava var izmantot krājumu sarakstu filtrēšanai. 
3. Atsvaidziniet lapu.
4. Darbību rūtī **Darbību rūtī** noklikšķiniet uz **Parādīt dimensijas**. Cilne Dimensiju ekrāns ļauj atlasīt, cik daudz informācijas vēlaties redzēt par jūsu rīcībā esošajiem krājumiem.
5. Noklikšķiniet uz **Labi**.
6. Aizvērt lapu.

## <a name="check-on-hand-inventory-by-location"></a>Rīcībā esošo krājumu pārbaude pēc atrašanās vietas
1. Pārejiet uz **Navigācijas rūts > Moduļi > Npliktava vadība > Uzziņas un pārskati > Fiziskie rīcībā esošie pēc atrašanās vietas**.
2. Laukā **Noliktava** atlasiet vērtību. Ja jūs izmantojat USMF demonstrācijas datus uzņēmuma, varat izmantot '51'.  
3. Atsvaidziniet lapu.
4. Noklikšķiniet uz **Parādīt dimensijas**.
5. Noklikšķiniet uz **Labi**.
6. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]