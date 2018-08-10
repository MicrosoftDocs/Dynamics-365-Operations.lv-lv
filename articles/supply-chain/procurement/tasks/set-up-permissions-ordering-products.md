--- 
title: "Atļauju iestatīšana preču pasūtīšanai kāda cita vārdā"
description: "Šajā procedūrā ir parādīts, kā nodarbinātajiem piešķirt atļauju sagatavot pirkšanas pieprasījumus citu nodarbināto vārdā."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Atļauju iestatīšana preču pasūtīšanai kāda cita vārdā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā nodarbinātajiem piešķirt atļauju sagatavot pirkšanas pieprasījumus citu nodarbināto vārdā. Citiem vārdiem sakot, pirkšanas pieprasījuma "sagatavotājs" var izveidot pieprasījuma cita "pieprasītāja" vajadzībām. Šajā procedūrā skaidrots arī, kā piešķirt darbinieku atļaujas pasūtīt krājumus un pakalpojumus dažādās juridiskajās personās vai pārvaldības struktūrvienībās. Parasti šos uzdevumus veic pirkšanas pārvaldnieks. Šo procedūru varat lietot ar datiem demonstrācijas datu uzņēmumam USMF vai ar paši saviem datiem.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Piešķirt atļauju ievadīt pirkšanas pieprasījumus cita nodarbinātā vārdā
1. Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas pieprasījumu atļaujas.
    * Pārliecinieties, ka laukam Pašreizējais skats ir iestatīta vērtība Pēc sagatavotāja.  Kreisajā rūtī esošajā sarakstā tiek rādītas personas, kurām var piešķirt atļauju sagatavot pieprasījumus citu personu vārdā.  
2. Atlasiet personu, kurai piešķirt atļauju (sagatavotāju).
3. Noklikšķiniet uz Pievienot.
4. Atrodiet un atlasiet personu, ko pievienot kā pieprasītāju.
    * Pieprasītājs ir persona, kuras vārdā sagatavotājs varat izveidot pieprasījumus.  
    * Laukā Autorizācija atlasiet vērtību Specifisks, ja sagatavotājam ir jāspēj izveidot pirkšanas pieprasījumus atlasītā nodarbinātā vārdā. Atlasiet vērtību Pārskati, ja sagatavotājam ir arī jāspēj izveidot pirkšanas pieprasījumus visus to nodarbināto vārdā, kuri atskaitās šim nodarbinātajam.  
5. Laukā Ir spēkā ievadiet kādu datumu.
6. Laukā Termiņa beigas ievadiet kādu datumu.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Skatīt sagatavotājus, kuriem ir atļauja izveidot pirkšanas pieprasījumus atlasītajam nodarbinātajam
1. Laukā Pašreizējais skats atlasiet vienumu “Pēc pieprasītāja”.
    * Šajā skatā tiek rādīts saraksts ar sagatavotājiem, kuriem ir piešķirta atļauja izveidot pirkšanas pieprasījumus atlasīta nodarbinātā vārdā.  
2. Izmantojiet ātro filtru, lai atrastu darbinieku, kuru tikko pievienojāt kā prasītāju.
3. Atlasiet šo pieprasītāju.
    * Sarakstā Sagatavotājs tiek rādītas personas, kam ir atļauja pasūtīt krājumus kreisajā rūtī atlasītā pieprasītāja vārdā.   Šeit varat pievienot papildu sagatavotājus.   Šis skats jums ļauj arī piešķirt pieprasītājam atļauju izveidot pieprasījumus juridiskajās personās un pārvaldības struktūrvienībās, kas nav šīs personas primārā juridiskā persona vai pārvaldības struktūrvienība.  


