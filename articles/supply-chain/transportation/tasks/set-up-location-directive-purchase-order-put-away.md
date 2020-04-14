---
title: Vietas direktīvas iestatīšana pirkšanas pasūtījuma izvietošanai
description: Šajā tēmā ir izskaidrots, kā iestatīt vienkāršu atrašanās vietas direktīvu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c75696f7147a7a4eb7b9d984936af9c28ef501
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146219"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Vietas direktīvas iestatīšana pirkšanas pasūtījuma izvietošanai

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā iestatīt vienkāršu atrašanās vietas direktīvu. Parādītajā piemērā tiek izveidota novietojuma direktīva, ko jāizmanto, lai noteiktu vietu, kur ievietot krājumus, kuri ir saņemti pirkšanas pasūtījuma ietvaros. Šo uzdevumu ceļvedi var izpildīt, izmantojot minētos datus, izmantojot demonstrācijas datu uzņēmumu USMF. Priekšnosacījumi: ir jāizveido atgriešanas metodes kods. Šajā procedūrā mēs lietojam atgriešanas metodes kodu, ko sauc Mainīt etiķetes. Ja veidojat novietojuma direktīvu savos datos, jums jāiestata savai noliktavai un krājumiem papildu noliktavas pārvaldība. Šī procedūra ir paredzēta noliktavas pārvaldniekam.

1. Navigācijas rūtī ejiet uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Atrašanās vietas direktīvas**.
2. Laukā **Darba pasūtījuma veids** atlasiet **Pirkuma pasūtījumi**.

## <a name="create-a-location-directive-header"></a>Novietojuma direktīvas virsraksta izveide
1. Atlasiet **Jauns**.
2. Ievadiet skaitli laukā **Secības numurs**. Tā ir secība, kādā novietojuma direktīva tiek apstrādāta atlasītajam darba tipam. Ja nepieciešams, secību var arī mainīt.  
3. Laukā **Nosaukums** ierakstiet kādu vērtību. Tas ir šīs veidnes direktīvas unikālais identifikators.  
4. Laukā **Darba veids** atlasiet **Ievietot**. Atlasiet veicamā darba veidu. Direktīvai ar darba pasūtījuma veidu Pirkuma pasūtījums, vērtība **Ievietot** ir vienīgā pieejamā vērtība.  
5. Laukā **Vieta** ievadiet vērtību.
6. Laukā **Noliktava** atlasiet vērtību. Lauku Direktīvas kods atstājiet tukšu.  Direktīvas kodi tiek izmantoti, lai saistītu darbu pasūtījuma rindu ar tipu Izvietot ar īpašu direktīvu. Pirkšanas pasūtījumiem pēdējās darba pasūtījuma rindas ar tipu Ievietot novietojums tiek noteikts pirms darba veidnes noteikšanas. Tāpēc nav iespējams savienot darba veidnes pēdējo rindu ar īpašu direktīvu.   
7. Laukā **Izvietojuma kods** ievadiet vērtību. Atgriešanas metodes kods ierobežo novietojuma direktīvas izmantošanu tā, ka novietojuma direktīva tiek izmantota tikai tad, ja noliktavas darbinieks ievada šo īpašu vērtību, reģistrējot krājumu, izmantojot mobilo ierīci.  
8. Atlasiet **Saglabāt**.

## <a name="edit-the-query-for-directive"></a>Direktīvas vaicājuma rediģēšana
1. Atlasiet **Rediģēt vaicājumu**. Šīs direktīvas izmantošana jau ir ierobežota izmantošanai krājumiem, kas reģistrēti noliktavā, ko norādījāt, un ar atgriešanas metodes kodu, ko norādījāt. Jūs varat pievienot citus ierobežojumus, izmantojot vaicājumu.  
2. Atlasiet **Labi**.

## <a name="add-directive-lines"></a>Direktīvas rindu pievienošana
1. Atlasiet **Jauns**. Tā ir secība, kādā novietojuma direktīvas rindas tiek apstrādātas atlasītajam darba tipam. Ja nepieciešams, secību var arī mainīt.  
2. Laukā **No daudzuma** ievadiet skaitu. Tas ir zemākais daudzums, kam šī direktīvas rinda ir piemērota.  
3. Laukā **Līdz daudzumam** ievadiet skaitu.
4. Laukā **Vienība** ierakstiet vērtību. Vienības, kurā izteiktas vērtības No daudzuma un Līdz daudzumam. Ja atstājat šo lauku tukšu, tiek izmantota krājuma vienība no krājuma.  
5. Atlasiet opciju laukā **Atrast daudzumu**.
    - Nav vai Numura zīmes daudzums: daudzums, kas reģistrēts katrai numura zīmei.  
    - Izmantotais daudzums: viss reģistrētais daudzums.  
    - Atlikušais daudzums: daudzums, kas vēl jāreģistrē no pirkšanas pasūtījuma rindas.  
    - Paredzētais daudzums: kopējais daudzums, kas norādīts pirkšanas pasūtījuma rindā.  
6. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Ierobežot pēc vienības**. Ja jūs atlasāt šo opciju un norādāt vienību lapā **Ierobežot pēc vienības**, tikai vienības ar šo mērvienību varēs novietot šajā atrašanās vietā. Piemēram, ja mērvienība ir PL (paletes), šajā novietojumā var novietot tikai krājumus paletēs.  
7. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Atļaut sadalījumu**. Tas ļauj direktīvai sadalītu daudzumu pa vairākiem novietojumiem.  
8. Atlasiet **Saglabāt**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Direktīvas rindas ierobežošana ar īpašu vienību
1. Atlasiet **Ierobežot pēc vienības**. Poga ir pieejama tikai pēc **Saglabāt** nospiešanas, kad ir atlasīta izvēles rūtiņa **Ierobežot pēc vienības**.  
2. Laukā **Vienība** ierakstiet vērtību.
3. Aizvērt lapu.

## <a name="add-a-location-directive-action-line"></a>Novietojuma direktīvas darbības rindas pievienošana
1. Atlasiet **Jauns**. Tā ir secība, kādā novietojuma direktīvas darbības rindas tiek apstrādātas atlasītajam darba tipam. Ja nepieciešams, secību var arī mainīt.  
2. Laukā **Nosaukums** ierakstiet kādu vērtību. Tas ir šīs direktīvas aktivitātes unikālais identifikators.  
3. Atlasiet opciju laukā **Fiksētās atrašanās vietas lietojums**.
    - Fiksētie un nefiksētie novietojumi: ir derīgi visi nefiksētie novietojumi, kā arī konkrētas preces fiksētais novietojums vaicājumā norādītajā diapazonā.  
    - Tikai preces fiksētais novietojums: ir derīgi preces fiksētie novietojumi, un visi preču varianti koplieto vienu un to pašu fiksēto novietojumu kopu.  
    - Tikai preču variantu fiksētie novietojumi: katram preces variantam derīgi tikai fiksēti novietojumi.  
4. Atlasiet opciju laukā **Stratēģija**. Darba pasūtījumi, kuru veids ir Pirkuma pasūtījums, atbalsta tālāk norādītās stratēģijas. 
    - Neviena: elements tiek novietots pirmajā atrastajā vietā.  
    - Apvienot: krājumu novieto vietā, kur jau ir pieejamai līdzīgi krājumi.  
    - Tukšs novietojums bez ienākoša darba: krājums tiek novietots pirmajā atrastajā tukšajā novietojumā. Novietojums tiek uzskatīts par tukšu, ja tajā nav fizisku krājumu un nav gaidāms ienākošais darbs.  
5. Atlasiet **Saglabāt**.

## <a name="edit-the-query-for-directive-action-line"></a>Direktīvas darbības rindas vaicājuma rediģēšana
1. Atlasiet **Rediģēt vaicājumu**.
2. Atlasiet **Pievienot**.
3. Laukā **Lauks** ievadiet `location profile ID`. Šajā piemērā mēs ierobežosim iespējamos novietojumus, izmantojot novietojuma profila ID.  
4. Laukā **Kritēriji** ierakstiet kādu vērtību.
5. Atlasiet **Labi**. Varat turpināt pievienot direktīvas rindas un direktīvas darbības, līdz tiks ņemti vērā visi iespējamie scenāriji jūsu noliktavā.  

