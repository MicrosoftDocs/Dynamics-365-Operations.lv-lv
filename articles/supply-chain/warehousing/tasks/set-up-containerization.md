---
title: Konteinerizēšanas iestatīšana
description: Šajā procedūrā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558060"
---
# <a name="set-up-containerization"></a>Konteinerizēšanas iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība. Automatizētā konteinerizēšanas izveido konteinerus un izdošanas darbu kravām, kad kopums ir apstrādāts un darba rindas var sadalīt daudzumos, kas atbilst konteineriem. Tas palīdz noliktavas darbiniekiem izdot krājumus tieši uz izvēlēto konteineru. Salīdzinot ar manuālo iepakošanas procesu, uzdevumus, piemēram, konteinera izveide, krājumu piešķiršana vai konteineru slēgšana automatizē sistēma. Šī procedūra izmanto USMF demonstrācijas uzņēmumu, un to veic noliktavas pārvaldnieks.


## <a name="set-up-a-wave-template"></a>Iestatiet kopuma veidni
1. Dodieties uz Noliktavas vadība > Iestatīšana > Kopumi > Kopumu veidnes.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Kopuma veidnes nosaukums.
4. Laukā Kopuma veidnes apraksts ierakstiet kādu vērtību.
5. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
6. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
7. Izvērsiet sadaļu Metodes.
    * Atlasīto metožu rūtī tiek uzskaitītas atlasītā kopuma veidnes veida metodes. Kopuma veidnei ir jāietver konteinerizēšanas metode.  
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Laukā Kopuma darbības kods, ierakstiet vērtību.
    * Ievadiet kopuma darbības kodu pievienotajai metodei, kas var būt jebkurš kods. Ir iespējams pievienot metodi vairāk nekā vienu reizi, un piešķirt dažādus kopuma darbību kodus. Lai to izdarītu, kopuma procesa metodes lapā atlasiet Atkārtojams šai metodei.  
10. Noklikšķiniet uz Saglabāt.
11. Aizvērt lapu.

## <a name="set-up-a-container-type"></a>Konteinera tipa iestatīšana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.
    * Jūs varat definēt konteinerus lapā Konteineru veidi. Jūs varat konfigurēt konteineru fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un augstumu. Šajā piemērā, mums ir trīs dažādu izmēru kastes.  
2. Noklikšķiniet uz Jauns.
3. Laukā Konteinera veida kods ierakstiet vērtību.
4. Laukā Taras svars ievadiet skaitli.
5. Ievadiet skaitli laukā Maksimālais svars.
6. Laukā Tilpums ievadiet skaitli.
7. Laukā Garums ievadiet skaitli.
8. Ievadiet skaitli laukā Platums.
9. Ievadiet skaitli laukā Augstums.
10. Apraksta laukā ierakstiet vērtību.
11. Noklikšķiniet uz Saglabāt.
12. Noklikšķiniet uz Jauns.
13. Laukā Konteinera veida kods ierakstiet vērtību.
14. Apraksta laukā ierakstiet vērtību.
15. Laukā Taras svars ievadiet skaitli.
16. Ievadiet skaitli laukā Maksimālais svars.
17. Laukā Tilpums ievadiet skaitli.
18. Laukā Garums ievadiet skaitli.
19. Ievadiet skaitli laukā Platums.
20. Ievadiet skaitli laukā Augstums.
21. Noklikšķiniet uz Saglabāt.
22. Noklikšķiniet uz Jauns.
23. Laukā Konteinera veida kods ierakstiet vērtību.
24. Apraksta laukā ierakstiet vērtību.
25. Laukā Taras svars ievadiet skaitli.
26. Ievadiet skaitli laukā Maksimālais svars.
27. Laukā Tilpums ievadiet skaitli.
28. Laukā Garums ievadiet skaitli.
29. Ievadiet skaitli laukā Platums.
30. Ievadiet skaitli laukā Augstums.
31. Noklikšķiniet uz Saglabāt.
32. Aizvērt lapu.

## <a name="set-up-a-container-group"></a>Konteineru grupas iestatīšana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru grupas.
2. Noklikšķiniet uz Jauns.
    * Varat iestatīt konteineru tipu loģiskās grupas. Katrai grupai varat norādīt secību, kādā konteineri ir jāiepako, kā arī konteineru aizpildes procentus. Programma izmanto krājuma lieluma dimensijas, lai noteiktu, vai šis krājums ietilpst konteinerā. Tiek izmantots konteiners, kas ir vistuvāk krājuma izmēru dimensijām. Ja vienā grupā ir vairāki konteineru tipi, ieteicams izveidot secību pēc lieluma, lai lielākais konteiners būtu pirmais, šīs secības 1. numurs, un vismazākais konteiners būtu pēdējais.    
3. Laukā Konteinera grupas ID, ievadiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Klikšķiniet Jauns.
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.
8. Klikšķiniet Jauns.
9. Sarakstā atzīmējiet atlasīto rindu.
10. Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.
11. Klikšķiniet Jauns.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.

## <a name="set-up-a-container-build-template"></a>Konteinera būvējuma veidnes iestatīšana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteinera būvējuma veidnes.
2. Noklikšķiniet uz Jauns.
    * Konteinera būvējuma veidne ir balstīta uz to, kuri konteinerizēšanas procesi tiek veikti. Katra konteinera būvējuma veidne nosaka vienu konteinerizēšanas procesu, kas tiks izmantots kopuma veidnē. Opcija Rediģēt vaicājumu ļauj definēt nosacījumus, kuros tiks apstrādāta atlasītā veidne. Piemēram, jūs varat palaist konteinerizēšanu tikai noteiktiem debitoriem, produktiem vai noliktavām, vai jūs veidnei varat pievienot atbilstošus vaicājuma diapazonus. Lauks Kopuma darbību kods ir kā konteinera būvējuma veidne tiek saistīta ar darbībām kopuma veidnē. Izpildot kopumu, tā nosaka, kura konteinera būvējuma veidne(-s) tiek izmantota, lai uzsāktu konteinerizēšanu. Lauks Bāzes vaicājuma veids nosaka, ko iepakot un uz ko balstīt filtra vaicājumu.  
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Konteinera veidnes ID, ierakstiet vērtību.
5. Laukā Konteinera grupas ID, ievadiet vai atlasiet kādu vērtību.
6. Laukā Kopuma darbības kods, ierakstiet vērtību.
7. Atzīmējiet izvēles rūtiņu Atļaut izdošanu sadali.
8. Noklikšķiniet uz Saglabāt.
9. Noklikšķiniet uz Konteineru kombinēti ierobežojumi.
    * Kombinēšanas loģikas pārtraukumpunkti ļauj iestatīt noteikumus iepakošanas sadalījuma rindām konteineros. Piemēram, ja pievienojat lauku Krājuma numurs, kad krājumi tiek piešķirti konteineriem, jauns konteineris tiks izveidots, parādoties jaunam krājuma kodam. Tas novērsīs darbiniekus no iepakojuma sadalījuma rindām diviem dažādiem klientiem vienā konteinerā.  
10. Noklikšķiniet uz Jauns.
11. Laukā Tabula, atlasiet opciju.
12. Laukā Atlasīt lauku, ievadiet vai atlasiet kādu vērtību.
13. Noklikšķiniet uz OK.

