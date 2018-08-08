---
title: "Daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišana"
description: "Šajā tēmā ir aprakstīts, kā iestatīt un lietot daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišanu no mobilās ierīces."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 4477749c721cf8c8bd244f551d9eca7ec9449fd1
ms.contentlocale: lv-lv
ms.lasthandoff: 02/08/2018

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišana

[!include [banner](../includes/banner.md)]

Funkcionalitāte daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišanai jums ļauj uz noliktavu daļēji pārvietot pārsūtīšanas pasūtījumus, izmantojot pakešuzdevumu.
Tā kā jums ir iespēja izlaist daļēju daudzumu, tad pirms pasūtījuma izlaišanas jums nav jāgaida, līdz noliktavā ir pieejams viss pasūtījuma daudzums.

Pasūtījumu pārvietošana uz noliktavu ir papildu noliktavas vadības process. Šis process ietver tādas aktivitātes kā izdošana, iepakošana un nosūtīšana, kuras noliktavas darbinieks var veikt, izmantojot mobilo ierīci.

## <a name="where-it-applies"></a>Darbības tvērums

Šai funkcionalitātei pārsūtīšanas pasūtījumi uz noliktavu tiek pārvietoti, izmantojot pakešuzdevumu. Šī funkcionalitāte ir noderīga, ja jums noliktavā nav pietiekami daudz krājumu, bet jūs tik un tā vēlaties krājumus no vienas noliktavas pārsūtīt uz citu.

## <a name="how-it-is-set-up"></a>Kā to iestatīt

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Norādīt izpildes kritērijus pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem

Lai pasūtījumu varētu daļēji pārvietot uz noliktavu pakešveidā, ir jābūt izpildītiem izpildes kritērijiem. Šos izpildes kritērijus nosaka izpildes politika.

Izpildes politikas attiecībā uz pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem tiek norādītas uzņēmuma līmenī. Atkarībā no izpildes politikas iestatījumiem pasūtījumu izlaišana pakešveidā tiks pieņemta vai noraidīta. Pēc tam pasūtījumi tiks atbilstoši apstrādāti.

-   Lai izveidotu izpildes politikas pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Pārvietot uz noliktavu** \> **Izpildes politika**, un pēc tam izveidojiet izpildes politiku, ievadot nosaukumu un aprakstu.

-   Lai norādītu izpildes koeficientu, vērtības tipu un ziņojumu, kas tiek rādīts, ja izpildes politika tiek pārkāpta, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Pārvietot uz noliktavu** \> **Izpildes politika** un pēc tam iestatiet laukus **Izpildes koeficients**, **Vērtības tips** un **Izpildes pārkāpumu ziņojums**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Iestatīt izpildes politikas pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem

-   Lai izpildes politikas iestatītu pārsūtīšanas pasūtījumiem, noklikšķiniet uz **Krājumu vadība** \> **Iestatījumi** \> **Krājumu un noliktavas vadības parametri** \> **Pārsūtīšanas pasūtījumi** \> **Noliktavas vadība** un pēc tam atlasiet pārsūtīšanas pasūtījumu izpildes politiku.

-   Lai izpildes politikas iestatītu pārdošanas pasūtījumiem, noklikšķiniet uz **Debitoru parādi** \> **Iestatījumi** \> **Debitoru parādu parametri** \> **Noliktavas vadība** un pēc tam atlasiet pārdošanas pasūtījumu izpildes politiku.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Atļaut izlaišanu pakešveidā un norādīt daudzumu, kas ir jāizlaiž pakešveidā

Pakešuzdevums tiek izmantots pasūtījumu pārvietošanai uz noliktavu pakešveidā. Parametri, kas norāda pasūtījumus, kuri ir jāpalaiž pakešuzdevumā, tiek iestatīti pašā pakešuzdevumā.

Parametrs **Daudzums** norāda, vai paketē ir jāizlaiž viss daudzums vai fiziski rezervētais daudzums. Parametrs **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** nosaka, vai pasūtījumi paketē ir jāpieņem vai jānoraida, ja tie iepriekš bija izlaisti daļēji.

-   Lai parametru **Daudzums** un **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** iestatītu pārsūtīšanas pasūtījumiem, noklikšķiniet uz **Noliktavas vadība** \> **Pārvietot uz noliktavu** \> **Pārsūtīšanas pasūtījumu automātiska pārvietošana**.

-   Lai parametru **Daudzums** un **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** iestatītu pārdošanas pasūtījumiem, noklikšķiniet uz **Noliktavas vadība** \> **Pārvietot uz noliktavu** \> **Pārdošanas pasūtījumu automātiska pārvietošana**.

