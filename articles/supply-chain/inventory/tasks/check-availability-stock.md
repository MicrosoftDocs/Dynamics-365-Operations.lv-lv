---
title: "Krājumu pieejamības pārbaude"
description: "Šajā procedūrā parādīts, kā pārbaudīt rīcībā esošos un fiziski rīcībā esošos krājumus noteiktam krājuma kodam."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Krājumu pieejamības pārbaude

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā pārbaudīt rīcībā esošos un fiziski rīcībā esošos krājumus noteiktam krājuma kodam. Aprakstīts arī tas, kā iegūt piegādes informāciju, kas saistīta ar krājumu. Fiziskie rīcībā esošie krājumi ir rīcībā esoši krājumi, kas ir pieejami, tas ir, tie ir nopirkti, saņemti un reģistrēti. Rīcībā esošie krājumi ietver pieejamos rīcībā esošos krājumus, kā arī krājumus, kas ir pasūtīti un tiek gaidīti, bet vēl nav saņemti vai nav reģistrēti. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja izmantojat USMF varat izmantot piemēra vērtības, kas parādītas. Šos uzdevumus parasti veic noliktavas darbinieks.


## <a name="check-on-hand-inventory-for-an-item"></a>Krājuma rīcībā esošo krājumu pārbaude
1. Dodieties uz Krājumu vadība > Uzziņas un atskaites > Rīcībā esošie krājumi.
2. Izvēlieties krājuma koda rindu.
    * Lai izpildītu vaicājumu rīcībā esošiem krājumiem pēc krājuma koda, atlasiet rindu, kur tabulai ir iestatīti rīcībā esošie krājumi un laukā ir iestatīts krājuma kods.  
3. Laukā Kritēriji atlasiet krājumu, kuram vēlaties izpildīt vaicājumu.
    * Ja lietojat demonstrācijas datu uzņēmumu USMF, varat atlasīt “M9201”.  
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Dimensijas.
    * Cilne Dimensijas ļauj atlasīt, cik daudz informācijas vēlaties redzēt par jūsu rīcībā esošajiem krājumiem. Ja jums ir nepieciešami dati, kas attiecas uz rezervāciju, ir jāattēlo visas krājumu dimensijas krājumiem, kas izmanto papildu noliktavas (WHS) procesus.  
6. Noklikšķiniet uz OK.
7. Darbību rūtī noklikšķiniet uz Saistītā informācija.
    * Ja tie nav redzami, iespējams, ir nepieciešams noklikšķināt uz elipses pogas (...), lai redzētu papildu darbību rūts opcijas.  
8. Noklikšķiniet uz Piegādes pārskats.
    * Cilne Piegādes pārskats sniedz piegādes informāciju noteiktam krājumam, piemēram, rīcībā esošo daudzumu, izpildes laiku un kreditora informāciju.  
9. Izvērsiet sadaļu Rīcībā esošs.
10. Izvērsiet sadaļu Kreditori.
11. Aizvērt lapu.
12. Aizvērt lapu.

## <a name="check-physical-on-hand-inventory"></a>Fizisko rīcībā esošo krājumu pārbaude
1. Dodieties uz Noliktavas vadība > Uzziņas un atskaites > Fiziski rīcībā esošie krājumi.
2. Laukā Krājuma kods ierakstiet kādu vērtību.
    * Laukus Vieta un Noliktava var izmantot krājumu sarakstu filtrēšanai.  
3. Atsvaidziniet lapu.
4. Noklikšķiniet uz Parādīt dimensijas.
    * Cilne Dimensiju ekrāns ļauj atlasīt, cik daudz informācijas vēlaties redzēt par jūsu rīcībā esošajiem krājumiem.  
5. Noklikšķiniet uz OK.
6. Aizvērt lapu.

## <a name="check-on-hand-inventory-by-location"></a>Rīcībā esošo krājumu pārbaude pēc atrašanās vietas
1. Dodieties uz Noliktavas vadība > Uzziņas un atskaites > Rīcībā esošie krājumi pēc novietojuma.
2. Laukā Noliktava ierakstiet kādu vērtību.
    * Ja jūs izmantojat USMF demonstrācijas datus uzņēmuma, varat izmantot '51'.  
3. Atsvaidziniet lapu.
4. Noklikšķiniet uz Parādīt dimensijas.
5. Noklikšķiniet uz OK.
6. Aizvērt lapu.

