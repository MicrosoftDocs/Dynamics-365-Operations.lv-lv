--- 
title: "Mērvienības pārvaldība"
description: "Šajā procedūrā parādīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: de5baa1e5c30ee998d113f7366c445a65723dfdc
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="manage-unit-of-measure"></a>Mērvienības pārvaldība

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām. Šo procedūru var izmēģināt, izmantojot demonstrācijas datus vai izmantojot savus datus.

1. Dodieties uz Izlaisto preču uzturēšana.
2. Noklikšķiniet uz Mērvienības.

## <a name="create-a-unit-of-measure"></a>Mērvienības izveide
1. Noklikšķiniet uz Jauns.
2. Laukā Mērvienība ierakstiet vērtību.
    * Ievadiet ID vai simbolu, kas jāizmanto, atsaucoties uz mērvienību.  
3. Apraksta laukā ierakstiet vērtību.
    * Ievadiet mērvienības aprakstošo nosaukumu sistēmas valodā.  
4. Laukā Mērvienību kategorija atlasiet opciju.
    * Mērvienību kategorija nosaka, kādam loģiskam grupējumam pieder mērvienība, piemēram, platībai, masai vai daudzumam.  
5. Laukā Decimālā precizitāte ievadiet skaitli.
    * Norādiet decimāldaļu skaitu, līdz kuram jānoapaļo konvertētā mērvienība, kad mērvienības aprēķins ir pabeigts.  
6. Noklikšķiniet uz Saglabāt.

## <a name="define-unit-translations"></a>Vienību tulkojumu definēšana
1. Noklikšķiniet uz Vienības teksti.
2. Noklikšķiniet uz Jauns.
    * Izmantojiet vienības tekstu, lai izveidotu ID vai simbola, kas apzīmē mērvienību, tulkojumu izmantošanai ārējos dokumentos debitoram vai kreditoram specifiskā valodā.  
3. Laukā Valoda ievadiet vai atlasiet kādu vērtību.
4. Ierakstiet vērtību laukā Teksts.
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.
7. Noklikšķiniet uz Tulkotie vienību apraksti.
8. Noklikšķiniet uz Jauns.
    * Definējiet valodai raksturīgus mērvienības aprakstus.  
9. Laukā Valoda ievadiet vai atlasiet kādu vērtību.
10. Apraksta laukā ierakstiet vērtību.
11. Noklikšķiniet uz Saglabāt.
12. Aizvērt lapu.

## <a name="define-unit-conversion-rules"></a>Vienību pārveidošanas noteikumu definēšana
1. Noklikšķiniet uz Mērvienību pārveidošana.
    * Definējiet noteikumus mērvienības pārveidošanai uz citām mērvienībām un no citām mērvienībām atlasītajā mērvienību kategorijā.  
2. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Koeficients ievadiet skaitli.
    * Pārveidošanas koeficients no No vienības uz Uz vienību. Piemēram, pārveidošanas koeficients no centimetriem uz metriem ir 100, jo viena metrā ir 100 centimetru.  
4. Laukā Uz mērvienību ievadiet vai atlasiet kādu vērtību.
5. Laukā Noapaļošana atlasiet opciju.
    * Nosakiet, kā pārveidotā vērtība ir jānoapaļo.  
6. Noklikšķiniet uz OK.
7. Aizvērt lapu.


