---
title: "Iestatīt bankas saskaņošanas atbilstības kārtulas"
description: "Šajā rakstā ir paskaidrots, kā iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas darbību saskaņošanas procesu. Saskaņošanas atbilstības kārtulas ir kritēriju kopa, ko izmanto, lai filtrētu bankas izrakstu rindas un bankas dokumentu rindas saskaņošanas procesa laikā."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: e4c07a6afb90535c57f372d5b850919b5b34aaa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Iestatīt bankas saskaņošanas atbilstības kārtulas

Šajā rakstā ir paskaidrots, kā iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas darbību saskaņošanas procesu. Saskaņošanas atbilstības kārtulas ir kritēriju kopa, ko izmanto, lai filtrētu bankas izrakstu rindas un bankas dokumentu rindas saskaņošanas procesa laikā.

Varat iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas saskaņošanas procesu. Atbilstības kārtulu saskaņošana ir noteikts kritērijus, ko izmanto filtrēšanai bankas paziņojumu rindas un Microsoft Dynamics 365 operācijas bankas darbības rindas saskaņošanas procesā. Izmantojiet lapu **Saskaņošanas atbilstības kārtulas**, lai iestatītu saskaņošanas atbilstības kārtulas. Varat iestatīt vairāk nekā vienu atbilstības kārtulu un pēc tam izveidot saskaņošanas atbilstības kārtulu kopu lapā **Saskaņošanas atbilstības kārtulu kopas**. 

> [!NOTE] 
> Bankas saskaņojuma atbilstības kārtulas izmanto, ja jūs saskaņot elektronisko bankas izrakstā, izmantojot iepriekšēju bankas saskaņojumu. 

Lapā **Saskaņošanas atbilstības kārtulas** varat izvēlēties, kuras darbības un atlases kritēriji tiek izmantoti, palaižot atbilstības kārtulu. Šajā **darbības** lauku grupu, izvēlieties darbību, kas tiks veikta atbilstības kārtulu palaižot saskaņošanas procesā.  

> [!NOTE] 
> Atlasītā opcija, nosaka, ka laukus, kuri parādās.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Darbība**                         |                                                                                                                                                                                                                                                                                                               | **Atlases kritēriji, kas ir pieejami, kad ir atzīmēta darbība**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Noteikt atbilstību bankas dokumentam **       | Izveidojiet kritēriju, lai norādītu, kā bankas dokumentu un bankas izrakstu rindas tiek saskaņotas, palaižot atbilstības kārtulu no lapas **Bankas saskaņošanas darblapa**. Transakcijas rindas tiek atlasītas saskaņā ar papildu kritērijiem, kas iestatīti kopsavilkuma cilnēs.                                | **1. solis: Noteikt atbilstības kārtulu** -izvēlieties criterias, lai norādītu, kuras bankas izraksti jāsaskaņo ar Dynamics 365 banku operācijas darījumus. **2. darbība (nav obligāti): atlasīt izraksta rindas, pret kurām palaist atbilstības kārtulas:** lietojiet filtru, lai noteiktu izraksta rindu, pret kuru palaist kārtulas.                                                                                                                                                                                                                                                                                                               |
| **Notīrīt anulēšanas izraksta rindas ** | Izveidojiet kritērijus, lai norādītu, kā anulēšanas izraksta rindas ir jāizņem no lapas **Bankas saskaņošanas darblapa**, palaižot atbilstības kārtulu. Šo opciju izmanto, ja bankas kļūdas dēļ importētajā bankas izrakstā ir uzskaitītas divas bankas izraksta rindas, un rindas ir jāsaskaņo. | **1. solis**:** anulēšanas izraksta rindu atrašana **— pievienojiet atlases kritērijus, lai atlasītu anulēšanas bankas izraksta rindas. Piemēram, lai atlasītu tikai pārbaudes, laukā Lauks atlasiet vienumu **Bankas transakcijas kods**, atlasiet pluss zīmi (+) laukā **Operators** un pēc tam laukā Vērtība ievadiet **Pārbaudes**. **2. solis: oriģinālā izraksta rindu atrašana** — varat pievienot atlases kritērijus, lai saskaņotu bankas dokumenta rindas ar bankas izraksta rindām. * * 3. solis: Rast operācijas bankas darbības dinamiku 365 * *-var pievienot atlases kritēriji, kuriem atbilst Dynamics 365 operācijas bankas darījumiem banka deklarācijas rindas. |
| **Mark new transactions**          | Izveidojiet kritērijus, lai norādītu, kā lapā **Bankas saskaņošanas darblapa** jāatzīmē jaunas transakcijas, palaižot atbilstības kārtulu.                                                                                                                                                                 | **1. darbība: izraksta rindu atrašana **— pievienojiet atlases laukus, lai norādītu, kuras bankas izraksta rindas ir jāatlasa no lapas **Bankas saskaņošanas darblapa**. * * Step 2: Find Dynamics 365 operācijas bankas darījumiem * *-var pievienot atlases kritēriji, lai meklētu bankas dokumenta rindām. Ja netiek atrasts neviens bankas dokuments, izraksta rinda tiks atzīmēta kā jauna transakcija.                                                                                                                                                                                                                                             |

 





