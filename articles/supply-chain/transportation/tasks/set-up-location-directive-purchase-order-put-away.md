--- 
title: "Novietojuma direktīvas iestatīšana pirkšanas pasūtījuma atlikšanai"
description: "Šajā procedūrā parādīts, kā iestatīt vienkāršu novietojuma direktīvu."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e1e54c807597d4d5ff7370748012cbf28c1c6b
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Novietojuma direktīvas iestatīšana pirkšanas pasūtījuma atlikšanai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt vienkāršu novietojuma direktīvu. Parādītajā piemērā tiek izveidota novietojuma direktīva, ko jāizmanto, lai noteiktu vietu, kur ievietot krājumus, kuri ir saņemti pirkšanas pasūtījuma ietvaros. Šo uzdevumu ceļvedi var izpildīt, izmantojot minētos datus, izmantojot demonstrācijas datu uzņēmumu USMF. Priekšnosacījumi: ir jāizveido atgriešanas metodes kods. Šajā procedūrā mēs lietojam atgriešanas metodes kodu, ko sauc Mainīt etiķetes. Ja veidojat novietojuma direktīvu savos datos, jums jāiestata savai noliktavai un krājumiem papildu noliktavas pārvaldība.  Šī procedūra ir paredzēta noliktavas pārvaldniekam.

1. Dodieties uz Noliktavas vadība > Iestatīšana > Novietojuma direktīvas.
2. Laukā Darba pasūtījuma tips atlasiet “Pirkšanas pasūtījumi”.

## <a name="create-a-location-directive-header"></a>Novietojuma direktīvas virsraksta izveide
1. Noklikšķiniet uz Jauns.
2. Ievadiet skaitli laukā Secības numurs.
    * Tā ir secība, kādā novietojuma direktīva tiek apstrādāta atlasītajam darba tipam. Ja nepieciešams, secību var arī mainīt.  
3. Laukā Nosaukums ierakstiet kādu vērtību.
    * Tas ir šīs veidnes direktīvas unikālais identifikators.  
4. Laukā Darba tips atlasiet vienumu “Izvietošana”.
    * Atlasiet veicamā darba veidu. Direktīvai ar darba pasūtījuma tipu Pirkšanas pasūtījums vienīgā atbalstītā vērtība ir Izvietot.  
5. Laukā Vieta ierakstiet kādu vērtību.
6. Laukā Noliktava ierakstiet kādu vērtību.
    * Lauku Direktīvas kods atstājiet tukšu.  Direktīvas kodi tiek izmantoti, lai saistītu darbu pasūtījuma rindu ar tipu Izvietot ar īpašu direktīvu. Pirkšanas pasūtījumiem pēdējās darba pasūtījuma rindas ar tipu Ievietot novietojums tiek noteikts pirms darba veidnes noteikšanas. Tāpēc nav iespējams savienot darba veidnes pēdējo rindu ar īpašu direktīvu.   
7. Laukā Atgriešanas metodes kods ierakstiet vērtību.
    * Atgriešanas metodes kods ierobežo novietojuma direktīvas izmantošanu tā, ka novietojuma direktīva tiek izmantota tikai tad, ja noliktavas darbinieks ievada šo īpašu vērtību, reģistrējot krājumu, izmantojot mobilo ierīci.  
8. Noklikšķiniet uz Saglabāt.

## <a name="edit-the-query-for-directive"></a>Direktīvas vaicājuma rediģēšana
1. Noklikšķiniet uz Rediģēt vaicājumu.
    * Šīs direktīvas izmantošana jau ir ierobežota izmantošanai krājumiem, kas reģistrēti noliktavā, ko norādījāt, un ar atgriešanas metodes kodu, ko norādījāt. Jūs varat pievienot citus ierobežojumus, izmantojot vaicājumu.  
2. Noklikšķiniet uz OK.

## <a name="add-directive-lines"></a>Direktīvas rindu pievienošana
1. Noklikšķiniet uz Jauns.
    * Tā ir secība, kādā novietojuma direktīvas rindas tiek apstrādātas atlasītajam darba tipam. Ja nepieciešams, secību var arī mainīt.  
2. Laukā No daudzuma ierakstiet kādu skaitli.
    * Tas ir zemākais daudzums, kam šī direktīvas rinda ir piemērota.  
3. Laukā Līdz daudzumam ierakstiet kādu skaitli.
4. Laukā Mērvienība ierakstiet vērtību.
    * Vienības, kurā izteiktas vērtības No daudzuma un Līdz daudzumam. Ja atstājat šo lauku tukšu, tiek izmantota krājuma vienība no krājuma.  
5. Laukā Novietot daudzumu atlasiet opciju.
    * Nav vai Numura zīmes daudzums: daudzums, kas reģistrēts katrā numura zīmē. Izmantotais daudzums: viss reģistrētais daudzums. Atlikušais daudzums: daudzums, kas vēl jāreģistrē no pirkšanas pasūtījuma rindas. Paredzētais daudzums: kopējais daudzums, kas norādīts pirkšanas pasūtījuma rindā.  
6. Atzīmējiet izvēles rūtiņu Ierobežot atbilstoši vienībai vai noņemiet tās atzīmi.
    * Ja atlasāt šo opciju un norādāt vienību lapā Ierobežot atbilstoši vienībai, novietojumā varēs tikt novietoti tikai krājumi ar šo mērvienību. Piemēram, ja mērvienība ir PL (paletes), šajā novietojumā var novietot tikai krājumus paletēs.  
7. Atzīmējiet izvēles rūtiņu Atļaut sadalījumu vai noņemiet tās atzīmi.
    * Tas ļauj direktīvai sadalītu daudzumu pa vairākiem novietojumiem.  
8. Noklikšķiniet uz Saglabāt.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Direktīvas rindas ierobežošana ar īpašu vienību
1. Noklikšķiniet uz Ierobežot atbilstoši vienībai.
    * Šī poga ir pieejama tikai tad, kad nospiežat Saglabāt pēc tam, kad ir atzīmēta izvēles rūtiņa Ierobežot atbilstoši vienībai.  
2. Laukā Mērvienība ierakstiet vērtību.
3. Aizvērt lapu.

## <a name="add-a-location-directive-action-line"></a>Novietojuma direktīvas darbības rindas pievienošana
1. Noklikšķiniet uz Jauns.
    * Tā ir secība, kādā novietojuma direktīvas darbības rindas tiek apstrādātas atlasītajam darba tipam. Ja nepieciešams, secību var arī mainīt.  
2. Laukā Nosaukums ierakstiet kādu vērtību.
    * Tas ir šīs direktīvas aktivitātes unikālais identifikators.  
3. Laukā Fiksētā novietojuma lietojums atlasiet opciju.
    * Fiksētie un nefiksētie novietojumi: ir derīgi visi nefiksētie novietojumi, kā arī konkrētas preces fiksētais novietojums vaicājumā norādītajā diapazonā.  Tikai preces fiksētais novietojums: ir derīgi preces fiksētie novietojumi, un visi preču varianti koplieto vienu un to pašu fiksēto novietojumu kopu. Tikai preču variantu fiksētie novietojumi: katram preces variantam derīgi tikai fiksēti novietojumi.  
4. Laukā Stratēģija atlasiet opciju.
    * Darba pasūtījumi ar tipu Pirkšanas pasūtījums atbalsta šādas stratēģijas: Nav: krājumu novieto pirmajā atrastajā novietojumā. Apvienot: krājumu novieto vietā, kur jau ir pieejamai līdzīgi krājumi. Tukšs novietojums bez ienākoša darba: krājums tiek novietots pirmajā atrastajā tukšajā novietojumā. Novietojums tiek uzskatīts par tukšu, ja tajā nav fizisku krājumu un nav gaidāms ienākošais darbs.  
5. Noklikšķiniet uz Saglabāt.

## <a name="edit-the-query-for-directive-action-line"></a>Direktīvas darbības rindas vaicājuma rediģēšana
1. Noklikšķiniet uz Rediģēt vaicājumu.
2. Noklikšķiniet uz Pievienot.
3. Laukā Lauks ierakstiet "novietojuma profila ID".
    * Šajā piemērā mēs ierobežosim iespējamos novietojumus, izmantojot novietojuma profila ID.  
4. Laukā Kritēriji ierakstiet kādu vērtību.
5. Noklikšķiniet uz OK.
    * Varat turpināt pievienot direktīvas rindas un direktīvas darbības, līdz tiks ņemti vērā visi iespējamie scenāriji jūsu noliktavā.  


