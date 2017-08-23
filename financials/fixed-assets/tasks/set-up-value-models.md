--- 
title: "Iestatīt grāmatas"
description: "Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grāmatu un sasaistīt to ar pamatlīdzekļu grupu."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 668fea64810524e8ce0c3833d25656c026f2780a
ms.openlocfilehash: 7e57b26c17d3bf773a719f9725d5f47dce2af6f7
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2017

---
# <a name="set-up-books"></a>Iestatīt grāmatas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grāmatu un sasaistīt to ar pamatlīdzekļu grupu. Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.


## <a name="create-a-book"></a>Izveidot grāmatu
1. Dodieties uz pamatlīdzekļi > Iestatījumi > Grāmatas.
2. Noklikšķiniet uz Jauns.
3. Laukā Grāmata, ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
    * Ja ir atlasīta iespēja Aprēķināt nolietojumu, saistīto pamatlīdzekļu grāmata tiks iekļauta nolietojuma priekšlikumos. Ja tā nav atlasīta, pamatlīdzekļu grāmata netiks aprēķināta automātiski.  
5. Atlasiet Jā laukā Aprēķināt nolietojumu.
6. Laukā Nolietojuma profils, ievadiet vai atlasiet kādu vērtību.
    * Alternatīva nolietojuma metode ir zināma arī kā nolietojuma pārslēgšanas metode. Nolietojuma priekšlikums pārslēgsies uz šo metodi, kad alternatīvās metodes aprēķinātā nolietojuma summa ir vienāda ar vai lielāka par noklusējuma nolietojuma metodes summu.  
    * Ārkārtas nolietojuma metode tiem izmantota līdzekļa papildu nolietošanai neparastos apstākļos. Piemēram, šo opciju varat izmantot, lai reģistrētu nolietojumu, ko izraisa dabas katastrofas.  
    * Atlasot Izveidot nolietojuma korekcijas ar pamata pielāgojumiem, nolietojuma korekcijas tiks izveidotas automātiski atjauninot līdzekļa vērtību. Ja tā nav atlasīta, atjauninātā līdzekļa vērtība ietekmēs tikai turpmākos nolietojuma aprēķinus.  
7. Atlasiet Jā, laukā Izveidot nolietojuma korekcijas ar pamata pielāgojumiem.
    * Pēc noklusējuma pamatlīdzekļa grāmatas darbības tiks grāmatotas virsgrāmatā. Jūs varat atslēgt grāmatas grāmatošanu virsgrāmatā, iestatot lauku Grāmatot virsgrāmatā uz Nē. Grāmatas, kas netiek grāmatotas virsgrāmatā parasti tiek izmantotas nodokļu pārskatu veidošanai. Tas dod jums papildu elastību vēsturisko darbības pamatlīdzekļu grāmatas dzēšanai, jo tie nav iekļauti virsgrāmatā.  
    * Grāmatošanas līmenis pēc noklusējuma ir Pašreizējais līmenis, ja tiek grāmatots virsgrāmatā, un Nav, ja to nevar grāmatot virsgrāmatā. Atjauniniet grāmatošanas līmeni, ja šīs grāmatas darbības nepieciešams grāmatot citā līmenī.  
8. Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.
    * Atvasinātās grāmatas var grāmatot darbības dažādās grāmatas vienlaicīgi. Jūs varat izveidot darbības, izmantojot primāro grāmatu, un grāmatošanas laikā, precīza darbības kopija tiek grāmatota atvasinātajā grāmatā. Atvasinātās grāmatas darbībām nav nekādu pārrēķinu, tāpēc to nevajadzētu izmantot nolietojuma darbībās.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Saistīt grāmatu ar pamatlīdzekļu grupu
1. Noklikšķiniet uz Pamatlīdzekļu grupas.
2. Ievadiet vai atlasiet vērtību laukā Pamatlīdzekļu grupa.
3. Ievadiet skaitli laukā Lietošanas ilgums.
    * Ņemiet vērā, ka Nolietojuma periodi tiek aprēķināti pēc vērtības Lietošanas ilgums iestatīšanas.  
    * Jūs varat arī iestatīt nolietojuma aprēķināšanas metodi, ja nepieciešams nodokļu vajadzībām.  


