---
title: Vietu konfigurēšana noliktavā ar iespējotu NPS
description: Šajā rokasgrāmatā ir parādīts, kā konfigurēt atrašanās vietas iestatījumus jaunai, ar WMS iespējotu noliktavu (noliktava, kas izmanto noliktavas vadības procesus (WMS)).
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45195698b48d6a22697f99044a8ae49beaf7156e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067279"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Vietu konfigurēšana noliktavā ar iespējotu noliktavas pārvaldības sistēmu

[!include [banner](../../includes/banner.md)]

Šajā rokasgrāmatā ir parādīts, kā konfigurēt atrašanās vietas iestatījumus jaunai, ar WMS iespējotu noliktavu (noliktava, kas izmanto noliktavas vadības procesus (WMS)). Procesu parasti veic noliktavas pārvaldnieks. Šo ceļvedi varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai savus datus. Priekšnosacījums: jābūt konfigurētai vismaz vienai vietai.


## <a name="create-a-new-warehouse"></a>Jaunas noliktavas izveide
1. Dodieties uz **Navigācijas rūti > Moduļi > Krājumu pārvaldība > Iestatīšana > Krājumu sadalījums > Noliktavas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Noliktava** atlasiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Vieta** atlasiet vai ierakstiet esošu vietas vērtību.
6. Izvērsiet **Noliktava** atlasi.
7. Iestatiet **Izmantot noliktavas vadības procesus opciju** uz Jā. Izmantojot šo iestatījumu, varat darbināt noliktavas vadības procesus (WMS), izmantojot noliktavas darbu un mobilās ierīces.
8. Aizvērt lapu.

## <a name="define-a-location-format"></a>Novietojuma formāta definēšana
1. Dodieties uz **Navigācijas rūti > Moduļi > Noliktavas pārvaldība > Iestatīšana > Noliktava >Atrašanās vietas formati**. Novietojuma formāti ir nosaukumdošanas sistēma, kuru izmanto, lai izveidotu unikālus un saskanīgus nosaukumus dažādām novietojuma nodalījuma pozīcijām, kas izmantotas noliktavā. Var būt noderīgi izmantot atdalītājus kā daļu no novietojuma formāta, lai būtu vieglāk noteikt sastāvdaļu novietojumu, piemēram, ailes numuru. Šajā piemērā mēs izveidosim nosaukumu ar četriem komponentiem. Piemēram, tie var būt aile, statīvs, plaukts un nodalījums.
2. Klikšķiniet **Jauns**.
3. Ierakstiet vērtību laukā **Atrašanās vietas formāts**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Ierakstiet vērtību laukā **Segmenta apraksts**. Te ir aprakstīts, uz ko attiecas novietojuma nosaukuma pirmais komponents. Piemēram, tā varētu būt 'Aile'.
6. Laukā **Garums** ievadiet skaitli. Tas nosaka, cik rakstzīmes var būt šai novietojuma nosaukuma daļai. Ņemiet vērā, ka visu komponentu nosaukumā, tostarp atdalītāju, skaits nedrīkst pārsniegt 10 rakstzīmes.    
7. Ierakstiet vērtību laukā **Atdalītājs**. Tas nosaka, kura rakstzīme vai simbols tiek izmantots starp pirmo un otro nosaukuma komponentu.  
8. Sadaļā **Detalizēta informācija** noklikšķiniet uz **Jauns**.
9. Ierakstiet vērtību laukā **Segmenta apraksts**.
10. Laukā **Garums** ievadiet skaitli.
11. Ierakstiet vērtību laukā **Atdalītājs**.
12. Sadaļā **Detalizēta informācija** noklikšķiniet uz **Jauns**.
13. Ierakstiet vērtību laukā **Segmenta apraksts**.
14. Laukā **Garums** ievadiet skaitli.
15. Ierakstiet vērtību laukā **Atdalītājs**.
16. Sadaļā **Detalizēta informācija** noklikšķiniet uz **Jauns**.
17. Ierakstiet vērtību laukā **Segmenta apraksts**.
18. Laukā **Garums** ievadiet skaitli.
19. Noklikšķiniet uz **Saglabāt**.
20. Aizvērt lapu.

## <a name="define-location-types"></a>Novietojuma tipu definēšana
1. Dodieties uz **Navigācijas rūti > Moduļi > Noliktavas pārvaldība > iestatīšana > Noliktava > Atrašanās vietas veidi**. Novietojuma tipus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus. Jums vismaz ir nepieciešams izveidot sagatavošanas un galīgos nosūtīšanas novietojuma tipus, lai noteiktu izejošo noliktavas pārvaldības procesu. 
2. Klikšķiniet **Jauns**.
3. Ierakstiet vērtību laukā **Atrašanās vietas**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Aizvērt lapu.

## <a name="define-location-profile"></a>Novietojuma profila definēšana
1. Dodieties uz **Navigācijas rūti > moduļi > Noliktavas pārvaldība > Iestatīšana > Noliktava > Atrašanās vietas profili**. Ir ļoti svarīgi definēt novietojuma profilus. Grupētu novietojumu noslodzes var kontrolēt šeit, kā arī politikas, saistībā ar kurām krājums tiek uzglabāts un kā tas tiek glabāts. Novietojumu profilus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus. Lai iespējotu WMS, jāizveido vismaz lietotāja atrašanās vietas profils.
2. Klikšķiniet **Jauns**.
3. Laukā **Atrašanās vietas ID** ierakstiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Atrašanās vietas formāts**.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Atrašanās vietas veids**.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Atzīmējiet vai notīriet izvēles rūtiņu **Atļaut jauktus krājumu statusus**. Aktivizējiet šo opciju, ja vēlaties atļaut jauktas krājumu statusa vērtības novietojumos, kas jāgrupē pēc šī novietojuma profila. 
12. Atzīmējiet vai notīriet izvēles rūtiņu **Ignorēt partijas dienu kārtulas**. Iespējojiet šo opciju, lai ignorētu nosacījumu, par cik dienām var atšķirties krājumu partijas derīguma termiņi, lai atļautu to krājumu partiju sajaukšanu, kas nav pakļautas šim nosacījumam.  
13. Atzīmējiet vai notīriet izvēles rūtiņu **Atļaut cikla inventarizāciju**. Aktivizējiet šo opciju, ja vēlaties atļaut cikla inventarizācijas apstrādi visos novietojumos, kas tiks grupēti pēc šī novietojuma profila. 
14. Izvērsiet vai sakļaujiet sadaļu **Dimensijas**. Cilne Dimensijas ļauj definēt parametrus un metodes, lai iespējotu precīzus noslodzes aprēķinus katrā no novietojumiem.  
15. Aizvērt lapu.

## <a name="enable-warehouse-management-parameters"></a>Noliktavas vadības parametru iespējošana
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Noliktavas vadības parametri**. Lai varētu apstrādāt noliktavas darbu, ir jāiestata parametri lietotāja atrašanās vietas profilam kā sagatavošanas posma atrašanās vietas veidam un galīgās nosūtīšanas atrašanās vietas veidam. Tiklīdz izejošais process beidzas jūsu definētajā gala nosūtīšanas atrašanās vietas veidā, saistītās izejošās transakcijas tiks atjauninātas uz "Izdots".
2. Izvērsiet sadaļu **Atrašanās vietas profili**.
3. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Lietotāja atrašanās vieta**.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Izvērsiet sadaļu **Atrašanās vietas veidi**.
6. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Sagatavošanas posma atrašanās vietas veids**.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Galīgās nosūtīšanas atrašanās vietas veids**.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Aizvērt lapu.

## <a name="define-warehouse-zone-groups"></a>Noliktavas zonu grupu definēšana
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Noliktavas zonu grupas**. Noliktavas zonas var izmantot kā opciju filtrus, lai kontrolētu dažādus noliktavas pārvaldības procesus. Pirms varēsiet definēt zonu, jums ir nepieciešams izveidot zonu grupu.   
2. Klikšķiniet **Jauns**.
3. Ierakstiet vērtību laukā **Zonu grupas ID**.
4. Ierakstiet vērtību laukā **Zonu grupas nosaukums**.
5. Aizvērt lapu.

## <a name="define-warehouse-zones"></a>Noliktavas zonu definēšana
1. Dodieties uz **Navigācijas rūti > Moduļi > Noliktavas pārvaldība > Iestatīšana > Noliktava > Zonas**.
2. Klikšķiniet **Jauns**.
3. Ierakstiet vērtību laukā **Zonas ID**.
4. Ierakstiet vērtību laukā **Zonas nosaukums**.
5. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Zonu grupas ID**.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Aizvērt lapu.

## <a name="create-locations-using-the-location-setup-wizard"></a>Novietojumu izveide, izmantojot Novietojuma iestatīšanas vedni
1. Dodieties uz **Navigācijas rūti > Moduļi > Noliktavas pārvaldība > Iestatīšana > Noliktava > Atrašanās vietas iestatīšanas vednis**.
2. Laukā **Noliktava** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Zonas ID**.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Lai atvērtu uzmeklēšanas logu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Atrašanās vietas profila ID**.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Sarakstā atzīmējiet atlasīto rindu.
12. Ievadiet skaitli laukā **No numura**. Vērtība laukā No numura un Līdz numuram nosaka, cik daudz novietojumi tiks izveidoti. Piemēram, ja visās četrās novietojuma formāta rindās laukā No numura tiek iestatīta vērtība 1 un laukā Līdz numuram — vērtība 3, tiek izveidots 81 novietojums (3x3x3x3).   
13. Ierakstiet skaitli laukā **Līdz numuram**.
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Ievadiet skaitli laukā **No numura**.
16. Ierakstiet skaitli laukā **Līdz numuram**.
17. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
18. Ievadiet skaitli laukā **No numura**.
19. Ierakstiet skaitli laukā **Līdz numuram**.
20. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
21. Ievadiet skaitli laukā **No numura**.
22. Ierakstiet skaitli laukā **Līdz numuram**.
23. Noklikšķiniet uz Izveidot.

## <a name="create-locations-manually"></a>Novietojumu manuālā izveide
1. Dodieties uz **Noliktavas vadība > Iestatīšana > Noliktava > Atrašanās vietas**. Novietojumus noliktavā ir viegli veidot manuāli. Atrašanās vietas nosaukums un atrašanās vietas profila ID ir obligātas vērtības. 
2. Klikšķiniet **Jauns**.
3. Laukā **Noliktava** atlasiet vērtību.
4. Ierakstiet vērtību laukā **Atrašanās vieta**. Ņemiet vērā, ka šeit jūs veidojat jaunu novietojumu, tāpēc ir nepieciešams ierakstīt jaunu unikālu nosaukumu nevis atlasīt esošo.
5. Laukā **Atrašanās vietas ID** ierakstiet vērtību.
6. Aizvērt lapu.

## <a name="define-pack-size-categories"></a>Pakas lielumu kategoriju izveide
1. **Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Novietojumu profili.** Pakas lielumu kategorijas var izmantot, lai grupētu krājumus, kuriem ir līdzīgs fiziskā iepakojuma lielums. Šajā piemērā pakas lieluma kategorija tiks izmantota, lai kontrolētu izdošanas vietu ietilpību noteiktā noliktavas zonā. Lūdzu ņemiet vērā, ka pakas lieluma kategorijas ID ir jāpiešķir izlaisto preču elementam, lai to varētu izmantot kā daļu no dimensijas ierobežojumu apstrādes.  
2. Klikšķiniet **Jauns**.
3. Ierakstiet vērtību laukā **Pakas lieluma kategorijas ID**.
4. Ierakstiet vērtību laukā **Pakas lieluma kategorijas nosaukums**.
5. Aizvērt lapu.

## <a name="define-location-stocking-limits"></a>Novietojuma dimensijas ierobežojumu definēšana
1. Dodieties uz **Noliktavas vadība > Iestatīšana > Noliktava > Atrašanās vietas dimensijas ierobežojumi**. Novietojuma dimensiju ierobežojumi palīdz pārliecināties, ka darbs netiek izveidots, lai pieprasītu krājuma ievietošanu vietā, kurā nav fiziski iespējams šo krājumu ievietot.  
2. Klikšķiniet **Jauns**.
3. Laukā **Noliktava** atlasiet vērtību.
4. Laukā **Atrašanās vietas ID** ierakstiet vērtību.
5. Ierakstiet vērtību laukā **Pakas lieluma kategorijas ID**.
6. Laukā **Daudzums** ierakstiet kādu skaitli.
7. Noklikšķiniet uz **Saglabāt**.
8. Aizvērt lapu.

## <a name="define-fixed-picking-locations"></a>Fiksētu izdošanas vietu definēšana
1. Dodieties uz **Noliktavas vadība > Iestatīšana > Noliktava > Fiksētās atrašanās vietas**. Varat definēt novietojumus, kuri tiks izmantoti katrai precei vai katram preces variantam. Ir iespējams izveidot vairākus fiksētos novietojumus vienai un tai pašai precei vienā noliktavā.     
2. Klikšķiniet **Jauns**.
3. Laukā **Krājuma kods** ierakstiet vērtību.
4. Laukā **Noliktava** atlasiet vērtību.
5. Lai atvērtu uzmeklēšanu, noklikšķiniet uz nolaižamā saraksta pogas laukā **Atrašanās vieta**.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
