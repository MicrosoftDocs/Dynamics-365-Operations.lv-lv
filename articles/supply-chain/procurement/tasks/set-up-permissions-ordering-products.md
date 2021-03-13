---
title: Atļauju iestatīšana preču pasūtīšanai kāda cita vārdā
description: Šajā tēmā ir paskaidrots, kā nodarbinātajiem piešķirt atļauju sagatavot pirkšanas pieprasījumus citu nodarbināto vārdā.
author: RichardLuan
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 585f5c6cf83ad93b649e3f36e0d486a037915cd4
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017296"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Atļauju iestatīšana preču pasūtīšanai kāda cita vārdā

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā nodarbinātajiem piešķirt atļauju sagatavot pirkšanas pieprasījumus citu nodarbināto vārdā. Citiem vārdiem sakot, pirkšanas pieprasījuma "sagatavotājs" var izveidot pieprasījuma cita "pieprasītāja" vajadzībām. Šajā procedūrā skaidrots arī, kā piešķirt darbinieku atļaujas pasūtīt krājumus un pakalpojumus dažādās juridiskajās personās vai pārvaldības struktūrvienībās. Parasti šos uzdevumus veic pirkšanas pārvaldnieks. Šo procedūru varat lietot ar datiem demonstrācijas datu uzņēmumam USMF vai ar paši saviem datiem.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Piešķirt atļauju ievadīt pirkšanas pieprasījumus cita nodarbinātā vārdā
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas pieprasījumu atļaujas**. Pārliecinieties, ka laukam **Pašreizējais skats** ir iestatīta vērtība **Pēc sagatavotāja**. Kreisajā rūtī esošajā sarakstā tiek rādītas personas, kurām var piešķirt atļauju sagatavot pieprasījumus citu personu vārdā.  
2. Atlasiet personu, kurai piešķirt atļauju (sagatavotāju).
3. Atlasiet **Pievienot**.
4. Atrodiet un atlasiet personu, ko pievienot kā pieprasītāju.
    - Pieprasītājs ir persona, kuras vārdā sagatavotājs varat izveidot pieprasījumus.  
    - Laukā **Autorizācija** atlasiet vērtību **Specifisks**, ja sagatavotājam ir jāspēj izveidot pirkšanas pieprasījumus atlasītā nodarbinātā vārdā. Atlasiet vērtību **Pārskati**, ja sagatavotājam ir arī jāspēj izveidot pirkšanas pieprasījumus visus to nodarbināto vārdā, kuri atskaitās šim nodarbinātajam.  
5. Laukā **Ir spēkā** ievadiet kādu datumu.
6. Laukā **Termiņa beigas** ievadiet kādu datumu.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Skatīt sagatavotājus, kuriem ir atļauja izveidot pirkšanas pieprasījumus atlasītajam nodarbinātajam
1. Laukā **Pašreizējais skats** atlasiet vienumu **Pēc pieprasītāja**. Šajā skatā tiek rādīts saraksts ar sagatavotājiem, kuriem ir piešķirta atļauja izveidot pirkšanas pieprasījumus atlasīta nodarbinātā vārdā.  
2. Izmantojiet ātro filtru, lai atrastu darbinieku, kuru tikko pievienojāt kā prasītāju.
3. Atlasiet šo pieprasītāju. Sarakstā Sagatavotājs tiek rādītas personas, kam ir atļauja pasūtīt krājumus kreisajā rūtī atlasītā pieprasītāja vārdā.  Šeit varat pievienot papildu sagatavotājus. Šis skats jums ļauj arī piešķirt pieprasītājam atļauju izveidot pieprasījumus juridiskajās personās un pārvaldības struktūrvienībās, kas nav šīs personas primārā juridiskā persona vai pārvaldības struktūrvienība.  

