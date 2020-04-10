---
title: Konteinerizēšanas iestatīšana
description: Šajā tēmā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9dbf62e1c518b0cd77da693127588a04f17d622
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148266"
---
# <a name="set-up-containerization"></a>Konteinerizēšanas iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība. Automatizētā konteinerizēšanas izveido konteinerus un izdošanas darbu kravām, kad kopums ir apstrādāts un darba rindas var sadalīt daudzumos, kas atbilst konteineriem. Tas palīdz noliktavas darbiniekiem izdot krājumus tieši uz izvēlēto konteineru. Salīdzinot ar manuālo iepakošanas procesu, uzdevumus, piemēram, konteinera izveide, krājumu piešķiršana vai konteineru slēgšana automatizē sistēma. Šī procedūra izmanto USMF demonstrācijas uzņēmumu, un to veic noliktavas pārvaldnieks.


## <a name="set-up-a-wave-template"></a>Iestatiet kopuma veidni
1. Navigācijas rūtī dodieties uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Kopumi > Kopumu veidnes**.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Kopuma veidnes nosaukums**.
4. Laukā **Kopuma veidnes apraksts** ierakstiet kādu vērtību.
5. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību.
6. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību.
7. Izvērsiet sadaļu **Metodes**. Rūtī **Atlasītās metodes** tiek uzskaitītas atlasītā kopuma veidnes veida metodes. Kopuma veidnei ir jāietver konteinerizēšanas metode.  
8. Laukā **Kopuma darbības kods** ierakstiet vērtību. Ievadiet kopuma darbības kodu pievienotajai metodei, kas var būt jebkurš kods. Ir iespējams pievienot metodi vairāk nekā vienu reizi, un piešķirt dažādus kopuma darbību kodus. Lai to izdarītu, atlasiet kopuma procesa metodes **Atkārtojams šai metodei** lapā **Kopuma procesa metodes**.  
9. Atlasiet **Saglabāt**.
10. Aizvērt lapu.

## <a name="set-up-a-container-type"></a>Konteinera tipa iestatīšana
1. Navigācijas rūtī dodieties uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Konteineri > Konteineru veidi**. Varat definēt konteinerus lapā **Konteineru veidi**. Jūs varat konfigurēt konteineru fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un augstumu. Šajā piemērā, mums ir trīs dažādu izmēru kastes.  
2. Atlasiet **Jauns**.
3. Laukā **Konteinera veida kods** ierakstiet vērtību.
4. Laukā **Taras svars** ievadiet skaitli.
5. Ievadiet skaitli laukā **Maksimālais svars**.
6. Laukā **Tilpums** ievadiet skaitli.
7. Laukā **Garums** ievadiet skaitli.
8. Laukā **Platums** ievadiet skaitli.
9. Ievadiet skaitli laukā **Augstums**.
10. Laukā **Apraksts** ierakstiet kādu vērtību.
11. Atlasiet **Saglabāt**.
13. Atkārtojiet 2-11. darbību divas reizes, lai izveidotu trīs kopējos konteineru veidus.
14. Aizvērt lapu.

## <a name="set-up-a-container-group"></a>Konteineru grupas iestatīšana
1. Navigācijas rūtī dodieties uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Konteineri > Konteineru grupas**.
2. Darbību rūtī atlasiet **Jauns**. Varat iestatīt konteineru tipu loģiskās grupas. Katrai grupai varat norādīt secību, kādā konteineri ir jāiepako, kā arī konteineru aizpildes procentus. Programma izmanto krājuma lieluma dimensijas, lai noteiktu, vai šis krājums ietilpst konteinerā. Tiek izmantots konteiners, kas ir vistuvāk krājuma izmēru dimensijām. Ja vienā grupā ir vairāki konteineru tipi, ieteicams izveidot secību pēc lieluma, lai lielākais konteiners būtu pirmais, šīs secības 1. numurs, un vismazākais konteiners būtu pēdējais.    
3. Laukā **Konteineru grupas ID** ievadiet iepriekš izveidoto vērtību.
4. Laukā **Apraksts** ierakstiet vērtību.
5. Atkārtojiet 2-4. darbību visiem trim iepriekš izveidotajiem konteineru veidiem.
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.

## <a name="set-up-a-container-build-template"></a>Konteinera būvējuma veidnes iestatīšana
1. Navigācijas rūtī dodieties uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Konteineri > Konteinera būvējuma veidnes**.
2. Atlasiet **Jauns**. Konteinera būvējuma veidne ir balstīta uz to, kuri konteinerizēšanas procesi tiek veikti. Katra konteinera būvējuma veidne nosaka vienu konteinerizēšanas procesu, kas tiks izmantots kopuma veidnē. Opcija **Rediģēt vaicājumu** ļauj definēt nosacījumus, kuros tiks apstrādāta atlasītā veidne. Piemēram, jūs varat palaist konteinerizēšanu tikai noteiktiem debitoriem, produktiem vai noliktavām, vai jūs veidnei varat pievienot atbilstošus vaicājuma diapazonus. Lauks **Kopuma darbību kods** parāda, kā konteinera būvējuma veidne tiek saistīta ar darbībām kopuma veidnē. Izpildot kopumu, tā nosaka, kura konteinera būvējuma veidne(-s) tiek izmantota, lai uzsāktu konteinerizēšanu. Lauks Bāzes vaicājuma veids nosaka, ko iepakot un uz ko balstīt filtra vaicājumu. 
3. Laukā **Konteinera veidnes ID** ierakstiet vērtību.
4. Laukā **Konteinera grupas ID** ievadiet vai atlasiet kādu vērtību.
5. Laukā **Kopuma darbības kods** ierakstiet vērtību.
6. Atzīmējiet izvēles rūtiņu **Atļaut izdošanu sadali**.
7. Atlasiet **Saglabāt**.
8. Atlasiet **Konteineru kombinēti ierobežojumi**. Kombinēšanas loģikas pārtraukumpunkti ļauj iestatīt noteikumus iepakošanas sadalījuma rindām konteineros. Piemēram, ja pievienojat lauku **Krājuma numurs**, kad krājumi tiek piešķirti konteineriem, jauns konteineris tiks izveidots, parādoties jaunam krājuma kodam. Tas novērsīs darbiniekus no iepakojuma sadalījuma rindām diviem dažādiem klientiem vienā konteinerā.  
9. Atlasiet **Jauns**.
10. Laukā **Tabula** atlasiet opciju.
11. Laukā **Atlasīt lauku** ievadiet vai atlasiet kādu vērtību.
12. Atlasiet **Labi**.

