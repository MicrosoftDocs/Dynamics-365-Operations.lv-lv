---
title: Vietu konfigurēšana noliktavā ar iespējotu NPS
description: Šajā ceļvedī parādīts, kā konfigurēt novietojuma iestatīšanu jaunai noliktavai ar iespējotu NPS (noliktavai, kas izmanto papildu noliktavas pārvaldības procesus).
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2be3c7cb33225041872e8b747ba28063f897dae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "337329"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Vietu konfigurēšana noliktavā ar iespējotu NPS

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā ceļvedī parādīts, kā konfigurēt novietojuma iestatīšanu jaunai noliktavai ar iespējotu NPS (noliktavai, kas izmanto papildu noliktavas pārvaldības procesus). Procesu parasti veic noliktavas pārvaldnieks. Šo ceļvedi varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai savus datus. Priekšnosacījums: jābūt konfigurētai vismaz vienai vietai.


## <a name="create-a-new-warehouse"></a>Jaunas noliktavas izveide
1. Dodieties uz Noliktavas.
2. Noklikšķiniet uz Jauns.
3. Laukā Noliktava ierakstiet kādu vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Vieta ierakstiet kādu vērtību.
6. Izvērsiet vai sakļaujiet sadaļu Noliktava.
7. Iestatiet opciju Izmantot noliktavas vadības procesus uz Jā.
    * Šis iestatījums ļauj palaist papildu noliktavas procesus, izmantojot noliktavas darbu un mobilās ierīces.  
8. Aizvērt lapu.

## <a name="define-a-location-format"></a>Novietojuma formāta definēšana
1. Dodieties uz Novietojuma formāti.
    * Novietojuma formāti ir nosaukumdošanas sistēma, kuru izmanto, lai izveidotu unikālus un saskanīgus nosaukumus dažādām novietojuma nodalījuma pozīcijām, kas izmantotas noliktavā. Var būt noderīgi izmantot atdalītājus kā daļu no novietojuma formāta, lai būtu vieglāk noteikt sastāvdaļu novietojumu, piemēram, ailes numuru. Šajā piemērā mēs izveidosim nosaukumu ar četriem komponentiem. Piemēram, tie var būt aile, statīvs, plaukts un nodalījums.  
2. Noklikšķiniet uz Jauns.
3. Laukā Novietojuma formāts ierakstiet kādu vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Segmenta apraksts ierakstiet vērtību.
    * Te ir aprakstīts, uz ko attiecas novietojuma nosaukuma pirmais komponents. Piemēram, tā varētu būt aile.  
6. Laukā Garums ievadiet skaitli.
    * Tas nosaka, cik rakstzīmes var būt šai novietojuma nosaukuma daļai. Ņemiet vērā, ka visu komponentu nosaukumā, tostarp atdalītāju, skaits nedrīkst pārsniegt 10 rakstzīmes.  
7. Laukā Atdalītājs ierakstiet vērtību.
    * Tas nosaka, kura rakstzīme vai simbols tiek izmantots starp pirmo un otro nosaukuma komponentu.  
8. Noklikšķiniet uz Jauns.
9. Laukā Segmenta apraksts ierakstiet vērtību.
10. Laukā Garums ievadiet skaitli.
11. Laukā Atdalītājs ierakstiet vērtību.
12. Klikšķiniet Jauns.
13. Laukā Segmenta apraksts ierakstiet vērtību.
14. Laukā Garums ievadiet skaitli.
15. Laukā Atdalītājs ierakstiet vērtību.
16. Klikšķiniet Jauns.
17. Laukā Segmenta apraksts ierakstiet vērtību.
18. Laukā Garums ievadiet skaitli.
19. Noklikšķiniet uz Saglabāt.
20. Aizvērt lapu.

## <a name="define-location-types"></a>Novietojuma tipu definēšana
1. Dodieties uz Novietojuma tipi.
    * Novietojuma tipus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus. Jums vismaz ir nepieciešams izveidot sagatavošanas un galīgos nosūtīšanas novietojuma tipus, lai noteiktu izejošo noliktavas pārvaldības procesu.  
2. Noklikšķiniet uz Jauns.
3. Laukā Novietojuma tips ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Aizvērt lapu.

## <a name="define-location-profile"></a>Novietojuma profila definēšana
1. Dodieties uz Novietojuma profili.
    * Ir ļoti svarīgi definēt novietojuma profilus. Grupētu novietojumu noslodzes var kontrolēt šeit, kā arī politikas, saistībā ar kurām krājums tiek uzglabāts un kā tas tiek glabāts. Novietojumu profilus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus. Lai iespējotu noliktavas pārvaldības procesus, ir jāizveido vismaz lietotāja novietojuma profils.  
2. Noklikšķiniet uz Jauns.
3. Laukā Novietojuma profila ID ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Novietojuma formāts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Novietojuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Atzīmējiet izvēles rūtiņu Atļaut jauktus krājumu statusus vai noņemiet tās atzīmi.
    * Aktivizējiet šo opciju, ja vēlaties atļaut jauktas krājumu statusa vērtības novietojumos, kas jāgrupē pēc šī novietojuma profila.  
12. Atzīmējiet izvēles rūtiņu Ignorēt partijas dienu kārtulas vai noņemiet tās atzīmi.
    * Iespējojiet šo opciju, lai ignorētu nosacījumu, par cik dienām var atšķirties krājumu partijas derīguma termiņi, lai atļautu to krājumu partiju sajaukšanu, kas nav pakļautas šim nosacījumam.  
13. Atzīmējiet izvēles rūtiņu Atļaut cikla inventarizāciju vai noņemiet tās atzīmi.
    * Aktivizējiet šo opciju, ja vēlaties atļaut cikla inventarizācijas apstrādi visos novietojumos, kas tiks grupēti pēc šī novietojuma profila.  
14. Izvērsiet vai sakļaujiet sadaļu Dimensijas.
    * Cilne Dimensijas ļauj definēt parametrus un metodes, lai iespējotu precīzus noslodzes aprēķinus katrā no novietojumiem.  
15. Aizvērt lapu.

## <a name="enable-warehouse-management-parameters"></a>Noliktavas vadības parametru iespējošana
1. Dodieties uz Noliktavas vadības parametri.
    * Lai varētu apstrādāt noliktavas darbu, ir jāiestata parametri lietotāja novietojuma profilam kā sagatavošanas posma novietojuma tipam un galīgās nosūtīšanas novietojuma tipam. Tiklīdz izejošais process beidzas jūsu definētajā gala nosūtīšanas novietojuma tipā, saistītās izejošās transakcijas tiks atjauninātas uz "Izdots".  
2. Izvērsiet vai sakļaujiet sadaļu Novietojuma profili.
3. Laukā Lietotāja novietojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Izvērsiet vai sakļaujiet sadaļu Novietojuma veidi.
6. Laukā Sagatavošanas posma novietojuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Galīgās nosūtīšanas novietojuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Aizvērt lapu.

## <a name="define-warehouse-zone-groups"></a>Noliktavas zonu grupu definēšana
1. Dodieties uz Noliktavas zonu grupas.
    * Noliktavas zonas var izmantot kā opciju filtrus, lai kontrolētu dažādus noliktavas pārvaldības procesus. Pirms varēsiet definēt zonu, jums ir nepieciešams izveidot zonu grupu.  
2. Noklikšķiniet uz Jauns.
3. Laukā Zonu grupas ID ierakstiet kādu vērtību.
4. Laukā Zonu grupas nosaukums ierakstiet kādu vērtību.
5. Aizvērt lapu.

## <a name="define-warehouse-zones"></a>Noliktavas zonu definēšana
1. Dodieties uz Zonas.
2. Noklikšķiniet uz Jauns.
3. Laukā Zonas ID ierakstiet kādu vērtību.
4. Laukā Zonas nosaukums ierakstiet kādu vērtību.
5. Laukā Zonu grupas ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Aizvērt lapu.

## <a name="create-locations-using-the-location-setup-wizard"></a>Novietojumu izveide, izmantojot Novietojuma iestatīšanas vedni
1. Dodieties uz Novietojuma iestatīšanas vednis.
2. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Zonas ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Novietojuma profila ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Sarakstā atzīmējiet atlasīto rindu.
12. Laukā No numura ievadiet skaitli.
    * Vērtība laukā No numura un Līdz numuram nosaka, cik daudz novietojumi tiks izveidoti. Piemēram, ja visās četrās novietojuma formāta rindās laukā No numura tiek iestatīta vērtība 1 un laukā Līdz numuram — vērtība 3, tiek izveidots 81 novietojums (3x3x3x3).  
13. Laukā Līdz numuram ievadiet skaitli.
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Laukā No numura ievadiet skaitli.
16. Laukā Līdz numuram ievadiet skaitli.
17. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
18. Laukā No numura ievadiet skaitli.
19. Laukā Līdz numuram ievadiet skaitli.
20. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
21. Laukā No numura ievadiet skaitli.
22. Laukā Līdz numuram ievadiet skaitli.
23. Noklikšķiniet uz Izveidot.

## <a name="create-locations-manually"></a>Novietojumu manuālā izveide
1. Dodieties uz Novietojumi.
    * Novietojumus noliktavā ir viegli veidot manuāli. Novietojuma nosaukums un Novietojuma profila ID ir obligātas vērtības.  
2. Noklikšķiniet uz Jauns.
3. Laukā Noliktava ierakstiet kādu vērtību.
4. Ierakstiet vērtību laukā Vieta.
    * Ņemiet vērā, ka šeit jūs veidojat jaunu novietojumu, tāpēc ir nepieciešams ierakstīt jaunu unikālu nosaukumu nevis atlasīt esošo.  
5. Laukā Novietojuma profila ID ierakstiet vērtību.
6. Aizvērt lapu.

## <a name="define-pack-size-categories"></a>Pakas lielumu kategoriju izveide
1. Dodieties uz Pakas lielumu kategorijas.
    * Pakas lielumu kategorijas var izmantot, lai grupētu krājumus, kuriem ir līdzīgs fiziskā iepakojuma lielums. Šajā piemērā pakas lieluma kategorija tiks izmantota, lai kontrolētu izdošanas vietu ietilpību noteiktā noliktavas zonā. Lūdzu ņemiet vērā, ka pakas lieluma kategorijas ID ir jāpiešķir izlaisto preču elementam, lai to varētu izmantot kā daļu no dimensijas ierobežojumu apstrādes.  
2. Noklikšķiniet uz Jauns.
3. Laukā Pakas lieluma kategorijas ID ierakstiet vērtību.
4. Laukā Pakas lieluma kategorijas nosaukums ierakstiet vērtību.
5. Aizvērt lapu.

## <a name="define-location-stocking-limits"></a>Novietojuma dimensijas ierobežojumu definēšana
1. Dodieties uz Novietojuma dimensijas ierobežojumi.
    * Novietojuma dimensiju ierobežojumi palīdz pārliecināties, ka darbs netiek izveidots, lai pieprasītu krājuma ievietošanu vietā, kurā nav fiziski iespējams šo krājumu ievietot.  
2. Noklikšķiniet uz Jauns.
3. Laukā Noliktava ierakstiet kādu vērtību.
4. Laukā Novietojuma profila ID ierakstiet vērtību.
5. Laukā Pakas lieluma kategorijas ID ierakstiet vērtību.
6. Laukā Daudzums ievadiet skaitli.
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.

## <a name="define-fixed-picking-locations"></a>Fiksētu izdošanas vietu definēšana
1. Dodieties uz Fiksētie novietojumi.
    * Varat definēt novietojumus, kuri tiks izmantoti katrai precei vai katram preces variantam. Ir iespējams izveidot vairākus fiksētos novietojumus vienai un tai pašai precei vienā noliktavā.  
2. Noklikšķiniet uz Jauns.
3. Laukā Krājuma kods ierakstiet kādu vērtību.
4. Laukā Noliktava ierakstiet kādu vērtību.
5. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Aizvērt lapu.

