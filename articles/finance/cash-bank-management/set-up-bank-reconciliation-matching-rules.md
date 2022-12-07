---
title: Bankas darbību saskaņošanas atbilstības kārtulu iestatīšana
description: Šajā rakstā ir paskaidrots, kā iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas darbību saskaņošanas procesu. Saskaņošanas atbilstības kārtulas ir kritēriju kopa, ko izmanto, lai filtrētu bankas izrakstu rindas un bankas dokumentu rindas saskaņošanas procesa laikā.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803942"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Bankas darbību saskaņošanas atbilstības kārtulu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas darbību saskaņošanas procesu. Saskaņošanas atbilstības kārtulas ir kritēriju kopa, ko izmanto, lai filtrētu bankas izrakstu rindas un bankas dokumentu rindas saskaņošanas procesa laikā.

Varat iestatīt saskaņošanas atbilstības kārtulas un saskaņošanas atbilstības kārtulu kopas, lai atvieglotu bankas saskaņošanas procesu. Saskaņošanas atbilstības kārtula ir kritēriju kopa, ko izmanto, lai filtrētu bankas izraksta rindas un Dynamics 365 finanšu bankas darbību rindas saskaņošanas procesa laikā. Izmantojiet lapu **Saskaņošanas atbilstības kārtulas**, lai iestatītu saskaņošanas atbilstības kārtulas. Varat iestatīt vairāk nekā vienu atbilstības kārtulu un pēc tam izveidot saskaņošanas atbilstības kārtulu kopu lapā **Saskaņošanas atbilstības kārtulu kopas**. 

> [!NOTE] 
> Bankas saskaņošanas atbilstības kārtulas izmanto, lai saskaņotu elektronisku bankas izrakstu, izmantojot detalizētu bankas saskaņošanu. 

Lapā **Saskaņošanas atbilstības kārtulas** varat izvēlēties, kuras darbības un atlases kritēriji tiek izmantoti, palaižot atbilstības kārtulu. Lauku grupā **Darbības** atlasiet darbību, kas tiks veikta, saskaņošanas procesa laikā palaižot atbilstības kārtulu.  

Pēc noklusējuma atbilstības kārtulas atbilst pirmajam bankas dokumentam, kas atbilst atbilstības noteikuma kritērijiem. Ja vairāki bankas dokumenti atbilst noteikuma kritērijiem, tad parametru, kas pieprasa manuālu saskaņošanu, var ieslēgt, atverot **Skaidras naudas un bankas pārvaldība > Iestatījumi > Skaidras naudas un bankas pārvaldības parametri > Bankas darbību saskaņošana > Pieprasiet manuālu atbilstību, ja uzlabotās bankas saskaņošanas kārtulas atrod vairākus dokumentus, kas atbilst summai**.

> [!NOTE] 
> Atlasītā opcija nosaka laukus, kas tiek attēloti.

| Darbība | Apraksts   | Atlases kritēriji, kas ir pieejami, kad ir atzīmēta darbība     |
|--------|---------------|----------------------------------------------------------|
| **Noteikt atbilstību bankas dokumentam**       | Izveidojiet kritēriju, lai norādītu, kā bankas dokumentu un bankas izrakstu rindas tiek saskaņotas, palaižot atbilstības kārtulu no lapas **Bankas saskaņošanas darblapa**. Transakcijas rindas tiek atlasītas saskaņā ar papildu kritērijiem, kas iestatīti kopsavilkuma cilnēs. | <ul><li>**1. darbība: definēt atbilstības kārtulu** — atlasiet kritēriju, lai norādītu, kuru bankas izrakstu atbilstība Finance bankas darbībām jānosaka.</li><li> **2. darbība (nav obligāti): atlasīt izraksta rindas, pret kurām palaist atbilstības kārtulas:** lietojiet filtru, lai noteiktu izraksta rindu, pret kuru palaist kārtulas.</li></ul>                                       |
| **Notīrīt anulēšanas izraksta rindas** | Izveidojiet kritērijus, lai norādītu, kā anulēšanas izraksta rindas ir jāizņem no lapas **Bankas saskaņošanas darblapa**, palaižot atbilstības kārtulu. Šo opciju izmanto, ja bankas kļūdas dēļ importētajā bankas izrakstā ir uzskaitītas divas bankas izraksta rindas, un rindas ir jāsaskaņo. |<ul><li> **1. solis**:**anulēšanas izraksta rindu atrašana**— pievienojiet atlases kritērijus, lai atlasītu anulēšanas bankas izraksta rindas. Piemēram, lai atlasītu tikai čekus, **·**  **laukā** Lauks atlasiet bankas darbības kodu, laukā Operatora atlasiet plus zīmi (+) **·**  **·**  **un** pēc tam laukā Vērtība ievadiet Čekus. </li><li>**2. solis: oriģinālā izraksta rindu atrašana** — varat pievienot atlases kritērijus, lai saskaņotu bankas dokumenta rindas ar bankas izraksta rindām. </li><li>**3. solis: Finance bankas transakciju atrašana** — varat pievienot atlases kritērijus, lai saskaņotu Finance bankas transakcijas ar bankas izraksta rindām.</li></ul>  |
| **Atzīmēt jaunus darījumus**          | Izveidojiet kritērijus, lai norādītu, kā lapā **Bankas saskaņošanas darblapa** jāatzīmē jaunas transakcijas, palaižot atbilstības kārtulu.                                                                                                                                                                 | <ul><li>**1. darbība: izraksta rindu atrašana**— pievienojiet atlases laukus, lai norādītu, kuras bankas izraksta rindas ir jāatlasa no lapas **Bankas saskaņošanas darblapa**.</li><li> **2. darbība: finanšu un operāciju**  atrašana – varat pievienot atlases kritērijus meklēšanai bankas dokumenta rindās. Ja netiek atrasts neviens bankas dokuments, izraksta rinda tiks atzīmēta kā jauna transakcija. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

