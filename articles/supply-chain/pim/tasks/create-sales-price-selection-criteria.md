--- 
title: "Pārdošanas cenu atlases kritēriju izveide"
description: "Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59f6a4131f6a27c0089a1259e3f849f91a47bc87
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-price-selection-criteria"></a>Pārdošanas cenu atlases kritēriju izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem. Šīs procedūras veikšanai ir nepieciešams, lai vismaz viens pārdošanas cenu modelis būtu pieejams. Šajā piemērā tiek izmantots cenu modelis Skaļruņa risinājuma pārdošanas cenas modelis demonstrācijas datu uzņēmumā USMF. Parasti produktu menedžeris izmanto šo procedūru.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Jauna kritērija pievienošana esošajam pārdošanas cenas modelim
1. Noklikšķiniet uz Preces varianta modeļa definīcija.
2. Noklikšķiniet uz Preču konfigurācijas modeļi.
3. Sarakstā atlasiet rindu Skaļruņa risinājuma preces modelim, bet nenoklikšķiniet uz modeļa nosaukuma saites.
4. Darbību rūtī noklikšķiniet uz Modelis.
5. Noklikšķiniet uz Cenas modeļa kritēriji.
6. Noklikšķiniet uz Jauns.
7. Laukā Nosaukums ierakstiet 'Debitoru grupa 10'.
    * Cenas modeļa kritērija nosaukums tiek izmantots, lai palīdzētu identificēt pamata atlases kritērijus.  
8. Laukā Cenas modelis ievadiet vai atlasiet kādu vērtību.
9. Laukā Pasūtījuma tips atlasiet Pārdošanas pasūtījums.
    * Pasūtījuma tips nosaka datu bāzes laukus, kas būs pieejami atlases vaicājumā.  
10. Laukā Spēkā no ievadiet datumu.
11. Laukā Beidzas pēc ievadiet datumu.
12. Noklikšķiniet uz Saglabāt.

## <a name="create-the-query-for-the-selection-criteria"></a>Izveidot vaicājumu atlases kritērijiem
1. Noklikšķiniet uz Rediģēt.
2. Laukā Tabula atlasiet Debitorus. 
3. Laukā Lauks atlasiet Debitoru grupu.
    * Šajā piemērā atlases kritērijiem tiks izmantota noteikta debitoru grupa.  
4. Laukā Kritēriji atlasiet debitoru grupu 10. 
5. Noklikšķiniet uz OK.


