---
title: Numuru sēriju iestatīšana mazumtirdzniecības pārskatiem
description: Šajā rakstā ir aprakstīts, kā konfigurēt numuru sērijas, kas ir nepieciešamas mazumtirdzniecības pārskatiem sadaļā Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 917d7b7a905a822ca3b1e074055fe0cd4af5555b
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027190"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Numuru sēriju iestatīšana mazumtirdzniecības pārskatiem

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt numuru sērijas, kas ir nepieciešamas mazumtirdzniecības pārskatiem sadaļā Microsoft Dynamics 365 Commerce.

Tiek izmantoti divi mazumtirdzniecības pārskatu veidi Dynamics 365 Commerce: 

- **Darbību priekšrakstus** ir paredzēts izveidot un grāmatot lielā frekvenci. Šīs darbības tiek izmantotas, lai galvenajā birojā grāmatotu visas ar veikalu nesaistītās Dynamics 365 Commerce darbības. 
- **Finanšu pārskatus** ir paredzēts izveidot un grāmatot vienu reizi darba dienā. Tostarp ir tikai slēgtas maiņas no mazumtirdzniecības veikaliem, kas ir augšupielādēti uz programmu Commerce Headquarters, izmantojot p-darbu.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Konfigurēt izraksta grāmatošanas numuru sēriju

Kad mazumtirdzniecības veikala iestatīšana programmā Commerce Headquarters ir pabeigta, ir jākonfigurē unikāla numuru sērija, kas tiks izmantota izrakstu izveides procesa laikā pārskatiem.

Lai konfigurētu numuru sēriju izrakstu grāmatošanai programmā Commerce Headquarters, sekojiet šiem soļiem.

1. Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Numuru sērijas**.
1. Atlasiet **Jaunu \> numuru sēriju**, lai izveidotu jaunu ierakstu.
1. Kopsavilkuma cilnes **Identifikācija** laukā Numuru sērijas **kods** ievadiet numuru sērijas kodu.
1. Laukā **Numuru sērijas** nosaukums ievadiet nosaukumu.
1. Kopsavilkuma cilnes **Tvēruma** parametri laukā **Tvērums** atlasiet **Pārvaldības struktūrvienība**.
1. Laukā **Pārvaldības struktūrvienība** atlasiet veikalu, kam tiks izmantota numuru sērija.
1. Kopsavilkuma cilnē **Segmenti** definējiet segmentus.
1. Kopsavilkuma cilnē **Atsauces** iestatiet lauku Apgabals **uz** Mazumtirdzniecības **veikals**.
1. Iestatiet atsauces **lauku** uz Pārskata **numurs un** pēc tam atlasiet **Labi**.

    ![Identifikācija, Sfēras parametri, Segmenti un Atsauces Kopsavilkuma cilnes Numuru sērijas lapā.](media/retail-statements-num-seq-setup-01.png)

1. Kopsavilkuma cilnes **Vispārīgi** **sadaļā** Numuru piešķiršana atjauniniet mazākos un lielākos laukus **,** **·** **·** **lai tie atbilstu kopsavilkuma cilnē Segmenti definētā burtciparu segmenta** garumam.
1. Kopsavilkuma cilnē **Veiktspēja** ieteicams iestatīt **opciju** **·** **Numuru rezervēšana uz Jā un lauku Numuru daudzums uz** **25.**

    ![Vispārīgas un veiktspējas kopsavilkuma cilnes numuru sēriju lapā.](media/retail-statements-num-seq-setup-02.png)

1. Darbību rūtī atlasiet Saglabāt, lai **saglabātu** izmaiņas un aizvērtu lapu.
