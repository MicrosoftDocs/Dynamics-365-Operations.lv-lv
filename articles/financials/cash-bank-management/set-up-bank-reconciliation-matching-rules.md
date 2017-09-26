---
title: "Iestatīt bankas saskaņošanas atbilstības kārtulas"
description: "Šajā rakstā ir paskaidrots, kā iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas darbību saskaņošanas procesu. Saskaņošanas atbilstības kārtulas ir kritēriju kopa, ko izmanto, lai filtrētu bankas izrakstu rindas un bankas dokumentu rindas saskaņošanas procesa laikā."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 60cd6a7f7b4d5c3acc68aa27c920f42f1d4b910e
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Iestatīt bankas saskaņošanas atbilstības kārtulas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas darbību saskaņošanas procesu. Saskaņošanas atbilstības kārtulas ir kritēriju kopa, ko izmanto, lai filtrētu bankas izrakstu rindas un bankas dokumentu rindas saskaņošanas procesa laikā.

Varat iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas saskaņošanas procesu. Saskaņošanas atbilstības kārtula ir kritēriju kopa, ko izmanto, lai saskaņošanas procesa laikā filtrētu bankas izrakstu rindas un Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise bankas transakciju rindas. Izmantojiet lapu **Saskaņošanas atbilstības kārtulas**, lai iestatītu saskaņošanas atbilstības kārtulas. Varat iestatīt vairāk nekā vienu atbilstības kārtulu un pēc tam izveidot saskaņošanas atbilstības kārtulu kopu lapā **Saskaņošanas atbilstības kārtulu kopas**. 

> [!NOTE] 
> Bankas saskaņošanas atbilstības kārtulas izmanto, lai saskaņotu elektronisku bankas izrakstu, izmantojot detalizētu bankas saskaņošanu. 

Lapā **Saskaņošanas atbilstības kārtulas** varat izvēlēties, kuras darbības un atlases kritēriji tiek izmantoti, palaižot atbilstības kārtulu. Lauku grupā **Darbības** atlasiet darbību, kas tiks veikta, saskaņošanas procesa laikā palaižot atbilstības kārtulu.  

> [!NOTE] 
> Atlasītā opcija nosaka laukus, kas tiek attēloti.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Darbība**                         |                                                                                                                                                                                                                                                                                                               | **Atlases kritēriji, kas ir pieejami, kad ir atzīmēta darbība**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Noteikt atbilstību bankas dokumentam**       | Izveidojiet kritēriju, lai norādītu, kā bankas dokumentu un bankas izrakstu rindas tiek saskaņotas, palaižot atbilstības kārtulu no lapas **Bankas saskaņošanas darblapa**. Transakcijas rindas tiek atlasītas saskaņā ar papildu kritērijiem, kas iestatīti kopsavilkuma cilnēs.                                | **1. darbība: definējiet atbilstības kārtulu** — atlasiet kritērijus, lai norādītu, kuru bankas izrakstu atbilstība Finance and Operations bankas darbībām jānosaka. **2. darbība (nav obligāti): atlasīt izraksta rindas, pret kurām palaist atbilstības kārtulas:** lietojiet filtru, lai noteiktu izraksta rindu, pret kuru palaist kārtulas.                                                                                                                                                                                                                                                                                                               |
| **Notīrīt anulēšanas izraksta rindas** | Izveidojiet kritērijus, lai norādītu, kā anulēšanas izraksta rindas ir jāizņem no lapas **Bankas saskaņošanas darblapa**, palaižot atbilstības kārtulu. Šo opciju izmanto, ja bankas kļūdas dēļ importētajā bankas izrakstā ir uzskaitītas divas bankas izraksta rindas, un rindas ir jāsaskaņo. | **1. solis**:**anulēšanas izraksta rindu atrašana**— pievienojiet atlases kritērijus, lai atlasītu anulēšanas bankas izraksta rindas. Piemēram, lai atlasītu tikai pārbaudes, laukā Lauks atlasiet vienumu **Bankas transakcijas kods**, atlasiet pluss zīmi (+) laukā **Operators** un pēc tam laukā Vērtība ievadiet **Pārbaudes**. **2. solis: oriģinālā izraksta rindu atrašana** — varat pievienot atlases kritērijus, lai saskaņotu bankas dokumenta rindas ar bankas izraksta rindām. **3. solis: Finance and Operations bankas transakciju atrašana **— varat pievienot atlases kritērijus, lai saskaņotu Finance and Operations bankas transakcijas ar bankas izraksta rindām. |
| **Jaunu darījumu atzīmēšana**          | Izveidojiet kritērijus, lai norādītu, kā lapā **Bankas saskaņošanas darblapa** jāatzīmē jaunas transakcijas, palaižot atbilstības kārtulu.                                                                                                                                                                 | **1. darbība: izraksta rindu atrašana**— pievienojiet atlases laukus, lai norādītu, kuras bankas izraksta rindas ir jāatlasa no lapas **Bankas saskaņošanas darblapa**. **2. darbība: Finance and Operations atrašana** — varat pievienot atlases kritērijus, lai meklētu bankas dokumentu rindās. Ja netiek atrasts neviens bankas dokuments, izraksta rinda tiks atzīmēta kā jauna transakcija.                                                                                                                                                                                                                                             |

 







