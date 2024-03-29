---
title: Jaunināt noliktavas pārvaldību no Microsoft Dynamics AX 2012 uz Supply Chain Management
description: Šajā rakstā sniegts pārskats par preču un noliktavu pārvaldības migrācijas opcijām.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a88c5a615ec860890578873eaee736fabbeaf08
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065816"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Jaunināt noliktavas pārvaldību no Microsoft Dynamics AX 2012 uz Supply Chain Management 


[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats Microsoft Dynamics AX par procesu, kad tika jaunināts no 2012 R3, uz WMSII moduli un piegādes ķēžu pārvaldība.

Supply Chain Management vairs neatbalsta Microsoft Dynamics AX 2012 mantoto moduli **WMSII**. Tā vietā varat izmantot moduli **Noliktavas pārvaldība**. Modulī WMSII finanšu krājumam varēja atlasīt krājumu dimensiju Novietojums un Paletes ID, taču programmatūrā Supply Chain Management krājumu dimensiju Paletes ID nevar izmantot finanšu krājumam.

Jaunināšanas laikā visas preces, kas ir saistītas ar noliktavas dimensiju grupu, kurā tiek izmantota krājumu dimensija Paletes ID, tiek identificētas, atzīmētas kā bloķētas un netiek apstrādātas jaunināšanai.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Jaunināšana uz Supply Chain Management, izmantojot AX 2012 R3 WMSII
Pēc jaunināšanas varat izmantot opciju kopu formā **Mainīt noliktavas dimensiju grupu krājumiem**, lai atbloķētu preces, kuras jaunināšanas laikā tika bloķētas, un pēc tam apstrādāt transakcijas šīm precēm.

### <a name="enabling-items-in-supply-chain-management"></a>Krājumu iespējošana Supply Chain Management 
Šīs izmaiņas ir nepieciešamas, jo Piegādes ķēdes pārvaldībā krājumu izsekošana ir daļa no noliktavas pārvaldības procesiem (WMS). Šiem procesiem visām noliktavām un to novietojumiem ir jābūt saistītiem ar novietojuma profilu. Ja vēlaties izmantot WMS, jābūt konfigurētiem šādiem nosacījumiem:
-   Lai varētu lietot WMS, jāiespējo esošās noliktavas. 
-   Esošās izlaistās preces ir jāsaista ar noliktavas dimensiju grupu, kas izmanto WMS. 

Ja avota noliktavas dimensiju grupas izmanto krājumu dimensiju Paletes ID, to rīcībā esošo krājumu novietojumi, kas izmantoja krājumu dimensiju Paletes ID, ir jāsaista ar novietojuma profilu, kurā ir atlasīts parametrs **Izmantot unikālā noliktavas vienības identifikatora izsekošanu**. Ja esošās noliktavas nav jāiespējo WMS lietošanai, esošo rīcībā esošo krājumu noliktavas dimensiju grupas var mainīt uz grupām, kas apstrādā tikai vietas, noliktavas un novietojuma krājumu dimensijas. 

> [!NOTE] 
>  Noliktavas dimensiju grupu krājumiem varat mainīt pat tad, ja pastāv atvērtas krājumu transakcijas.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Krājumu dimensijas Paletes ID dēļ bloķēto preču atrašana
Lai skatītu sarakstu ar izlaistajām precēm, kas tika bloķētas jaunināšanas laikā un ko nevar apstrādāt, noklikšķiniet uz **Krājumu pārvaldība** &gt; **Iestatīšana** &gt; **Krājumi** &gt; **Krājumi, kas ir bloķēti krājumu atjauninājumiem**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Noliktavas dimensiju grupas mainīšana bloķētām precēm 
 
Lai krājumu izmantotu kā daļu no noliktavas pārvaldības procesa, šim krājumam ir jābūt saistītam ar kādu noliktavas dimensiju grupu, kurā ir aktīva krājumu dimensija Novietojums un ir atlasīts parametrs **Izmantot noliktavas pārvaldības procesus**. Ja ir atlasīts šis iestatījums, kļūst aktīvas krājumu dimensijas Vieta, Noliktava, Krājumu statuss, Novietojums un Unikāls noliktavas vienības identifikators.

Lai atbloķētu preces, kas tika bloķētas jaunināšanas laikā, ir jāatlasa jauna noliktavas dimensiju grupa precēm. Ņemiet vērā, ka varat mainīt noliktavas dimensiju grupu pat tad, ja pastāv atvērtas krājumu transakcijas. Lai lietotu krājumus, kas tika bloķēti jaunināšanas laikā, ir divas iespējas.

-   Mainiet noliktavas dimensiju grupu krājumam uz noliktavas dimensiju grupu, kurā tiek izmantotas tikai krājumu dimensijas Vieta, Noliktava un Novietojums. Šo izmaiņu rezultātā vairs netiek izmantota krājumu dimensija Paletes ID.
-   Mainiet krājuma noliktavas dimensiju grupu uz noliktavas dimensiju grupu, kas izmanto WMS. Šo izmaiņu rezultātā tagad tiek izmantota krājumu dimensija Unikāls noliktavas vienības identifikators.

## <a name="configure-wms"></a>Konfigurēt WMS
Pirms izlaisto preču lietošanas modulī **Noliktavas pārvaldība** precēm ir jāizmanto noliktavas dimensiju grupa, kurā ir atlasīts parametrs **Izmantot noliktavas pārvaldības procesus**.

### <a name="enable-warehouses-to-use-wms"></a>Iespējot noliktavu WMS izmantošanu

1.  Izveidojiet vismaz vienu jaunu novietojuma profilu.
2.  Noklikšķiniet uz **Noliktavas pārvaldība** &gt; **Iestatīšana** &gt; **Iespējot noliktavas pārvaldības procesus** &gt; **Iespējot noliktavas iestatīšanu**.
3.  Lapā **Iespējot noliktavas iestatīšanu** pievienojiet noliktavas, kas jāiespējo. Šo darbību var veikt tieši lapā vai izmantojot Microsoft Office integrāciju.
4.  Piešķiriet novietojuma profilu visiem novietojumiem. Šo darbību var ērti veikt, izmantojot Microsoft Office integrāciju tieši no lapas. Varat eksportēt un importēt datus vai arī izmantot datu elementa apstrādi sadaļā [Datu pārvaldība](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
5.  Pārbaudiet izmaiņas. Kā daļa no pārbaudes procesa notiek dažādas datu integritātes pārbaudes. Lielāka jaunināšanas procesa ietvaros, iespējams, avota ieviešanā ir jākoriģē radušās problēmas. Šajā gadījumā būs nepieciešama papildu datu jaunināšana.
6.  Apstrādājiet izmaiņas.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-wms"></a>Mainīt noliktavas dimensiju grupu krājumiem tā, lai tas izmanto WMS

1.  Izveidojiet jaunu vienuma **Krājumu statuss** vērtību un piešķiriet to kā vienuma **Noklusējuma krājumu statusa ID** vērtību vienuma **Noliktavas pārvaldības parametri** iestatījumos.
2.  Izveidojiet jaunu noliktavas dimensiju grupu, kurā ir atlasīts parametrs **Izmantot noliktavas pārvaldības procesus**.
3.  Lapā **Rezervāciju hierarhija** definējiet jaunu rezervāciju hierarhiju saskaņā ar krājuma noliktavas un izsekošanas dimensiju grupām.
4.  Izveidojiet vienu vai vairākas vienību secību grupas, kas ietver vismaz tās pašas vienības, kas tiek izmantotas krājumu uzskaites vienībām.
5.  Noklikšķiniet uz **Noliktavas pārvaldība** &gt; **Iestatīšana** &gt; **Iespējot noliktavas pārvaldības procesus** &gt; **Mainīt noliktavas dimensiju grupu krājumiem**.
6.  Lapā **Mainīt noliktavas dimensiju grupu krājumiem** pievienojiet krājumu kodus, noliktavas dimensiju grupas un vienību secību grupas. Šo darbību var veikt tieši lapā, izmantojot Microsoft Office integrāciju vai izmantojot datu elementa apstrādi sadaļā [Datu pārvaldība](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
7.  Pārbaudiet izmaiņas. Kā daļa no pārbaudes procesa notiek dažādas datu integritātes pārbaudes. Lielāka jaunināšanas procesa ietvaros, iespējams, avota ieviešanā ir jākoriģē radušās problēmas. Šajā gadījumā būs nepieciešama papildu datu jaunināšana.
8.  Apstrādājiet izmaiņas. Visu krājumu dimensiju atjaunināšana var ilgt kādu laiku. Varat pārraudzīt norisi, izmantojot pakešuzdevumus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]