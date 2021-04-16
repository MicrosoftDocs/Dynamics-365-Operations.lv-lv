---
title: Pārdošanas cenu atlases kritēriju izveide
description: Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a616dcfdd755efc9bf0473e9239acb9127f11f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818161"
---
# <a name="create-sales-price-selection-criteria"></a>Pārdošanas cenu atlases kritēriju izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem. Šīs procedūras veikšanai ir nepieciešams, lai vismaz viens pārdošanas cenu modelis būtu pieejams. Šajā piemērā tiek izmantots cenu modelis Skaļruņa risinājuma pārdošanas cenas modelis paraugdatu uzņēmumā USMF. Parasti produktu menedžeris izmanto šo procedūru.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Jauna kritērija pievienošana esošajam pārdošanas cenas modelim
1. Noklikšķiniet uz Preces varianta modeļa definīcija.
2. Noklikšķiniet uz Preču konfigurācijas modeļi.
3. Sarakstā atlasiet rindu Skaļruņa risinājuma preces modelim, bet nenoklikšķiniet uz modeļa nosaukuma saites.
4. Darbību rūtī noklikšķiniet uz Modelis.
5. Noklikšķiniet uz Cenas modeļa kritēriji.
6. Klikšķiniet Jauns.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]