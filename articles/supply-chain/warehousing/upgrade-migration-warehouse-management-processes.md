---
title: "Preču un noliktavas vadības migrēšana no AX 2012 uz Finance and Operations"
description: "Šajā tēmā ir sniegts apskats par preču un noliktavas vadības migrēšanas opcijām."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c6d40e3b80a0974c722ad3a88a29adc8dedf585
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>Preču un noliktavas vadības migrēšana no AX 2012 uz Finance and Operations

Šajā tēmā sniegts pārskats par preču un noliktavu pārvaldības migrācijas opcijām Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumā.

<a name="introduction"></a>Ievads
------------

Jaunināšanas uz Finance and Operations laikā preces tiek bloķētas, ja tās ir saistītas ar noliktavas dimensiju grupu, kurā ir iestatījumi, kas neatbilst noliktavas dimensiju grupu iestatījumu prasībām programmatūrā Finance and Operations. Taču pēc jaunināšanas varat izmantot migrācijas opciju kopu procesā **Mainīt noliktavas dimensiju grupu krājumiem**, lai atbloķētu jaunināšanas laikā bloķētās preces. Pēc tam varat apstrādāt transakcijas šīm precēm. Daļa jūsu krājumu jau var būt saistīta ar noliktavas dimensiju grupām, kurās ir aktīvas un fiziski izsekotas krājumu dimensijas Vieta, Noliktava un Novietojums. Šajā gadījumā varat izmantot procesu **Mainīt noliktavas dimensiju grupu krājumiem**, lai ļautu šos krājumus izmantot noliktavas pārvaldības procesos. Šī iespēja ir noderīga, ja vēlaties izmantot noliktavas pārvaldības funkcionalitāti esošajiem krājumiem.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Jaunināšana uz Finance and Operations, ja tiek izmantots modulis AX 2012 R3 WMSII
Finance and Operations vairs neatbalsta Microsoft Dynamics AX 2012 moduli **WMSII**. Tā vietā varat izmantot jauno moduli **Noliktavas pārvaldība**. Iepriekšējās versijās finanšu krājumiem varēja atlasīt krājumu dimensijas Novietojums un Paletes ID. Tomēr jaunināšanas procesa ietvaros finanšu krājumiem vairs nevar iespējot krājumu dimensiju Paletes ID. Visas preces, kuras ir saistītas ar noliktavas dimensiju grupu, kas izmanto krājumu dimensiju Paletes ID, tiks bloķētas un netiks apstrādātas.

### <a name="enabling-items-in-finance-and-operations"></a>Krājumu iespējošana programmatūrā Finance and Operations

Programmatūrā Finance and Operations krājumi, kas tiks izmantoti kā daļa no noliktavas pārvaldības procesiem, ir jāsaista ar noliktavas dimensiju grupu, kurā ir atlasīts parametrs **Izmantot noliktavas pārvaldības procesus**. Ja ir atlasīts šis iestatījums, kļūst aktīvas krājumu dimensijas Vieta, Noliktava, Krājumu statuss, Novietojums un Unikāls noliktavas vienības identifikators. Maiņu uz šī tipa noliktavas dimensiju grupu var veikt tikai krājumiem, kas jau ir saistīti ar noliktavas dimensiju grupām, kurās ir aktīva krājumu dimensija Novietojums.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Krājumi, kas ir bloķēti krājumu atjauninājumiem

Lai skatītu sarakstu ar izlaistajām precēm, kas tika bloķētas jaunināšanas laikā un ko nevar apstrādāt, noklikšķiniet uz **Krājumu pārvaldība** &gt; **Iestatīšana** &gt; **Krājumi** &gt; **Krājumi, kas ir bloķēti krājumu atjauninājumiem**.

### <a name="reapplying-blocked-products"></a>Bloķēto preču atkārtota lietošana

Lai atbloķētu preces, kas tika bloķētas jaunināšanas laikā, ir jāatlasa jauna noliktavas dimensiju grupa precēm. Ņemiet vērā, ka varat mainīt noliktavas dimensiju grupu pat tad, ja pastāv atvērtas krājumu transakcijas. Lai lietotu krājumus, kas tika bloķēti jaunināšanas laikā, ir divas iespējas.

-   Mainiet noliktavas dimensiju grupu krājumam uz noliktavas dimensiju grupu, kurā tiek izmantotas tikai krājumu dimensijas Vieta, Noliktava un Novietojums. Šo izmaiņu rezultātā vairs netiek izmantota krājumu dimensija Paletes ID.
-   Mainiet noliktavas dimensiju grupu krājumam uz noliktavas dimensiju grupu, kurā tiek izmantoti noliktavas pārvaldības procesi. Šo izmaiņu rezultātā tagad tiek izmantota krājumu dimensija Unikāls noliktavas vienības identifikators.

### <a name="migration-processes"></a>Migrācijas procesi

Programmatūrā Finance and Operations krājumu izsekošana ir daļa no noliktavas pārvaldības procesiem. Šiem procesiem visām noliktavām un to novietojumiem ir jābūt saistītiem ar novietojuma profilu. Ja vēlaties izmantot noliktavas pārvaldības procesus, ir jāveic divi procesi.

-   Esošajām noliktavām ir jāiespējo noliktavas pārvaldības procesu lietošana.
-   Esošās izlaistās preces ir jāsaista ar jaunu noliktavas dimensiju grupu, kas izmanto noliktavas pārvaldības procesus.

Ja avota noliktavas dimensiju grupas izmanto krājumu dimensiju Paletes ID, to rīcībā esošo krājumu novietojumi, kas izmantoja krājumu dimensiju Paletes ID, ir jāsaista ar novietojuma profilu, kurā ir atlasīts parametrs **Izmantot unikālā noliktavas vienības identifikatora izsekošanu**. Ja esošās noliktavas nedrīkst iespējot noliktavas pārvaldības procesu lietošanai, rīcībā esošo krājumu noliktavas dimensiju grupas varat mainīt uz grupām, kurās tiek apstrādātas tikai krājumu dimensijas Vieta, Noliktava un Novietojums.

### <a name="using-the-warehouse-management-processes"></a>Noliktavas pārvaldības procesu izmantošana

Pirms izlaisto preču lietošanas modulī **Noliktavas pārvaldība** precēm ir jāizmanto noliktavas dimensiju grupa, kurā ir atlasīts parametrs **Izmantot noliktavas pārvaldības procesus**.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Noliktavas pārvaldības procesu lietošanas iespējošana noliktavām

1.  Izveidojiet vismaz vienu jaunu novietojuma profilu.
2.  Noklikšķiniet uz **Noliktavas pārvaldība** &gt; **Iestatīšana** &gt; **Iespējot noliktavas pārvaldības procesus** &gt; **Iespējot noliktavas iestatīšanu**.
3.  Lapā **Iespējot noliktavas iestatīšanu** pievienojiet noliktavas, kas jāiespējo. Šo darbību var veikt tieši lapā vai izmantojot Microsoft Office integrāciju.
4.  Piešķiriet novietojuma profilu visiem novietojumiem. Šo darbību var ērti veikt, izmantojot Microsoft Office integrāciju tieši no lapas. Varat eksportēt un importēt datus vai arī izmantot datu elementa apstrādi sadaļā [Datu pārvaldība](../../dev-itpro/data-entities/data-entities.md).
5.  Pārbaudiet izmaiņas. Kā daļa no pārbaudes procesa notiek dažādas datu integritātes pārbaudes. Lielāka jaunināšanas procesa ietvaros, iespējams, avota ieviešanā ir jākoriģē radušās problēmas. Šajā gadījumā būs nepieciešama papildu datu jaunināšana.
6.  Apstrādājiet izmaiņas.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Noliktavas dimensiju grupas maiņa krājumiem, lai tā izmantotu noliktavas pārvaldības procesus

1.  Izveidojiet jaunu vienuma **Krājumu statuss** vērtību un piešķiriet to kā vienuma **Noklusējuma krājumu statusa ID** vērtību vienuma **Noliktavas pārvaldības parametri** iestatījumos.
2.  Izveidojiet jaunu noliktavas dimensiju grupu, kurā ir atlasīts parametrs **Izmantot noliktavas pārvaldības procesus**.
3.  Lapā **Rezervāciju hierarhija** definējiet jaunu rezervāciju hierarhiju saskaņā ar krājuma noliktavas un izsekošanas dimensiju grupām.
4.  Izveidojiet vienu vai vairākas vienību secību grupas, kas ietver vismaz tās pašas vienības, kas tiek izmantotas krājumu uzskaites vienībām.
5.  Noklikšķiniet uz **Noliktavas pārvaldība** &gt; **Iestatīšana** &gt; **Iespējot noliktavas pārvaldības procesus** &gt; **Mainīt noliktavas dimensiju grupu krājumiem**.
6.  Lapā **Mainīt noliktavas dimensiju grupu krājumiem** pievienojiet krājumu kodus, noliktavas dimensiju grupas un vienību secību grupas. Šo darbību var veikt tieši lapā, izmantojot Microsoft Office integrāciju, vai izmantojot datu elementa apstrādi sadaļā [Datu pārvaldība](../../dev-itpro/data-entities/data-entities.md).
7.  Pārbaudiet izmaiņas. Kā daļa no pārbaudes procesa notiek dažādas datu integritātes pārbaudes. Lielāka jaunināšanas procesa ietvaros, iespējams, avota ieviešanā ir jākoriģē radušās problēmas. Šajā gadījumā būs nepieciešama papildu datu jaunināšana.
8.  Apstrādājiet izmaiņas. Visu krājumu dimensiju atjaunināšana var ilgt kādu laiku. Varat pārraudzīt norisi, izmantojot pakešuzdevumus.



