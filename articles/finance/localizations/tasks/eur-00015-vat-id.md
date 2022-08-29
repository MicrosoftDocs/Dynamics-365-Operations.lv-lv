---
title: EUR-00015 PVN ID iestatīšana
description: Šajā procedūrā parādīti PVN ID reģistrācijas priekšnosacījumi, piemēram, reģistrācijas tipa iestatīšana un reģistrācijas kategorijas piešķiršana.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
ms.openlocfilehash: 26120765b61a27cab544c37163a34a0ef18da30a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283791"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015 PVN ID iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīti PVN ID reģistrācijas priekšnosacījumi, piemēram, reģistrācijas tipa iestatīšana un reģistrācijas kategorijas piešķiršana. Reģistrācijas ID palīdzības rakstā varat atrast papildinformāciju par reģistrācijas ID un reģistrācijas ID apstrādi, ieskaitot nepieciešamos priekšnosacījumus. 

Šeit sniegtā informācija attiecas uz visām Eiropas valstīm/reģioniem. Šis uzdevums ir izveidots, izmantojot demonstrācijas uzņēmuma DEMF datus, norādot Vāciju kā juridiskās personas primārās adreses valsti. Šis uzdevums ir paredzēts sistēmas administratoriem. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

1. Dodieties uz Organizācijas administrēšana > Globālā adrešu grāmata > Reģistrācijas tipi > Reģistrācijas tipi.
2. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Nosaukums ierakstiet 'PVN ID'.
4. Laukā Apraksts, PVN numuru.
5. Laukā Valsts/reģions ievadiet vai atlasiet vērtību DEU
6. Laukā Unikāls atlasiet Jā.
    * Atzīmējiet šo izvēles rūtiņu, lai pārbaudītu, vai PVN ID ir unikāls.  
7. Atlasiet Jā laukā Primārais valstij.
    * Atzīmējiet šo izvēles rūtiņu, ja PVN ID ir spēkā visām adresēm, kas pieder norādītajai valstij/reģionam.  
8. Noklikšķiniet uz Izveidot.
9. Noklikšķiniet uz Pievienot.
10. Laukā Valsts/reģions ievadiet vai atlasiet vērtību ITA
11. Laukā Formāts ierakstiet '###########'.
    * Ievadot šī tipa reģistrācijas ID atlasītajai valstij/reģionam, reģistrācijas ID tiks pārbaudīts ar šo formātu.  
12. Atzīmējiet izvēles rūtiņu Unikāls.
    * Atzīmējiet šo izvēles rūtiņu, lai pārbaudītu, vai PVN ID ir unikāls.  
13. Atlasiet Primārais valstij izvēles rūtiņu.
    * Atzīmējiet šo izvēles rūtiņu, ja PVN ID ir spēkā visām adresēm, kas pieder norādītajai valstij/reģionam.  
14. Noklikšķiniet uz Saglabāt.
15. Dodieties uz Organizācijas administrēšana > Globālā adrešu grāmata > Reģistrācijas tipi > Reģistrācijas kategorijas.
16. Noklikšķiniet uz Jauns.
17. Laukā Valsts/reģions ievadiet vai atlasiet vērtību PVN ID, DEU
18. Laukā Reģistrācijas kategorija atlasiet 'PVN ID'.
    * Piešķirt reģistrācijas tipu, ko jūs izveidojāt agrāk iepriekš definētai Reģistrācijas kategorijai.  
19. Noklikšķiniet uz Jauns.
20. Laukā Valsts/reģions ievadiet vai atlasiet vērtību PVN ID, ITA
21. Laukā Reģistrācijas kategorija atlasiet 'PVN ID'.
    * Piešķirt reģistrācijas tipu, ko jūs izveidojāt iepriekš definētai reģistrācijas kategorijai.  
22. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
