---
title: Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem
description: " Šajā tēmā aprakstīts, kā piešķirt uzdevumu sarakstus veikaliem vai darbiniekiem Microsoft Dynamics 365 Commerce."
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006264"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem

[!include [banner](includes/banner.md)]

 Šajā tēmā aprakstīts, kā piešķirt uzdevumu sarakstus veikaliem vai darbiniekiem Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Uzdevumu pārvaldība programmā Dynamics 365 Commerce ļauj piešķirt uzdevumu sarakstu vairākiem veikaliem vai darbiniekiem vai arī veikalu un darbinieku kombinācijai. Piemēram, reģionālais vadītājs 20 veikaliem varētu vēlēties piešķirt uzdevumu sarakstu **Gatavošanās atvaļinājumu sezonai** visiem 20 veikaliem.

## <a name="start-the-task-list-assignment-process"></a>Sākt uzdevumu saraksta piešķires procesu

Lai sāktu uzdevumu saraksta piešķiršanu, rīkojieties šādi.

1. Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības administrēšana**.
1. Atlasiet uzdevumu sarakstu, ko piešķirt.
1. Atlasiet **Uzsākt procesu**.
1. Dialoglodziņa **Uzsākt procesu** cilnē **Vispārīgi**, laukā **Procesa nosaukums** ievadiet nosaukumu (piemēram, **Austrumu apgabala veikali**).
1. Laukā **Mērķa datums** konkretizējiet datumu.
1. Lai uzdevumu sarakstu piešķirtu veikaliem, cilnē **Veikali** izmantojiet **Organizācijas hierarhijas** filtru, lai atrastu un atlasītu veikalus.

    Lai piešķirtu uzdevumu sarakstu darbiniekiem, cilnē **Darbinieki** meklējiet un atlasiet darbiniekus.

1. Atlasiet **Labi**, lai sāktu procesu. Uzdevumu saraksts ir piešķirts atlasītajiem veikaliem vai darbiniekiem.

Šajā attēlā parādīts piemērs, kā atrast un atlasīt veikalus dialoglodziņā **Uzsākt procesu**.

![Veikalu atrašana un atlasīšana procesa uzsākšanas dialoglodziņā](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Uzdevumu sarakstu periodiska piešķiršana

Mazumtirgotājam reizēm ir periodiski uzdevumi, piemēram, "Ceturtdienas slēgšanas kontrolsaraksts" vai "Mēneša pirmā dienas kontrolsaraksts". Tāpēc viņi var vēlēties uzdevumu sarakstu piešķirt periodiski.

1. Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības administrēšana**.
1. Atlasiet uzdevumu sarakstu, ko piešķirt.
1. Atlasiet **Uzsākt procesu**.
1. Dialoglodziņa **Uzsākt procesu** cilnē **Vispārīgi**, laukā **Procesa nosaukums** ievadiet nosaukumu.
1. Iestatiet opciju **Periodiskums** uz **Jā**.
1. Laukā **Atkārtošanās mērķa datuma nobīde dienās** ievadiet dienu skaitu. Piemēram, ja ievadāt **4**, mērķa datums ir atkārtošanās datums plus četras dienas.
1. Cilnē **Palaist fonā** atlasiet **Periodiskums**.
1. Dialoglodziņā **Definēt periodiskumu** ievadiet biežuma kritērijus un pēc tam atlasiet **Labi**.

Šajā attēlā parādīts piemērs, kā ievadīt biežuma kritērijus dialoglodziņā **Definēt periodiskumu**.

![Biežuma kritēriju ievade dialoglodziņā Definēt periodiskumu](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Izsekot uzdevumu saraksta statusam

Ja esat reģionālais vadītājs vai veikala vadītājs, iespējams, vēlēsities izsekot to uzdevumu sarakstu statusam, kas ir piešķirti vairākiem veikaliem vai nodarbinātajiem. Pēc tam varat sekot līdzi veikaliem vai darbiniekiem, kas nav laicīgi izpildījuši tiem piešķirtos uzdevumus. Commerce operāciju uzskaites daļa ļauj skatīt uzdevumu sarakstu statusu, atkārtoti piešķirt uzdevumus vai mainīt uzdevuma statusu.

Lai izsekotu uzdevumu saraksta statusam visiem uzdevumiem, rīkojieties šādi.

1. Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības procesi**.
1. Atlasiet cilni **Visi uzdevumu saraksti**, lai skatītu visu to uzdevumu sarakstu statusu, kas ir piešķirti dažādiem veikaliem.

Lai izsekotu uzdevumu saraksta statusam visiem uzdevumiem, kas piešķirti jums, rīkojieties šādi.

1. Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības procesi**.
1. Atlasiet cilni **Mani uzdevumi** vai **Visi uzdevumi**, lai skatītu vai atjauninātu jums piešķirto uzdevumu statusu.

## <a name="additional-resources"></a>Papildu resursi

[Uzdevumu pārvaldības pārskats](task-mgmt-overview.md)

[Uzdevumu pārvaldības konfigurēšana](task-mgmt-configure.md)

[Uzdevumu sarakstu izveidošana un uzdevumu pievienošana](task-mgmt-create-lists.md)

[Uzdevumu pārvaldība punktā POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]