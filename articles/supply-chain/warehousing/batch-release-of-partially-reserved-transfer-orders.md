---
title: Daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišana
description: Šajā rakstā ir aprakstīts, kā iestatīt un lietot partijas laidienu daļēji rezervētiem pārsūtīšanas pasūtījumiem no mobilās ierīces.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218688"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišana

[!include [banner](../includes/banner.md)]

Funkcionalitāte daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišanai jums ļauj uz noliktavu daļēji pārvietot pārsūtīšanas pasūtījumus, izmantojot pakešuzdevumu.
Tā kā jums ir iespēja izlaist daļēju daudzumu, tad pirms pasūtījuma izlaišanas jums nav jāgaida, līdz noliktavā ir pieejams viss pasūtījuma daudzums.

Pasūtījumu nosūtīšana uz noliktavu ir noliktavas vadības procesu (WMS) process. Šis process ietver tādas aktivitātes kā izdošana, iepakošana un nosūtīšana, kuras noliktavas darbinieks var veikt, izmantojot mobilo ierīci.

## <a name="where-it-applies"></a>Darbības tvērums

Šai funkcionalitātei pārsūtīšanas pasūtījumi uz noliktavu tiek pārvietoti, izmantojot pakešuzdevumu. Šī funkcionalitāte ir noderīga, ja jums noliktavā nav pietiekami daudz krājumu, bet jūs tik un tā vēlaties krājumus no vienas noliktavas pārsūtīt uz citu.

## <a name="how-it-is-set-up"></a>Kā to iestatīt

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Norādīt izpildes kritērijus pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem

Lai pasūtījumu varētu daļēji pārvietot uz noliktavu pakešveidā, ir jābūt izpildītiem izpildes kritērijiem. Šos izpildes kritērijus nosaka izpildes politika.

Izpildes politikas attiecībā uz pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem tiek norādītas uzņēmuma līmenī. Atkarībā no izpildes politikas iestatījumiem pasūtījumu izlaišana pakešveidā tiks pieņemta vai noraidīta. Pēc tam pasūtījumi tiks atbilstoši apstrādāti.

- Lai izveidotu pārsūtīšanas pasūtījumu un pārdošanas pasūtījumu izpildes politikas, **\>\>\>** pārejiet uz sadaļu Noliktavas vadības iestatīšana, lai nodotu izpildei noliktavas izpildes politikām, un izveidojiet izpildes politiku, ievadot nosaukumu un aprakstu.
- Lai norādītu izpildes koeficientu, vērtības tipu un ziņojumu, kas tiek rādīts, ja izpildes politika ir pārkāpta, **\>\>\>** **dodieties uz Noliktavas vadības iestatījums Nodot izpildei noliktavas izpildes politikām un iestatiet izpildes** koeficientu, **·** **vērtības tipu un izpildes pārkāpuma ziņojuma** laukus.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Iestatīt izpildes politikas pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem

- Lai pārsūtīšanas pasūtījumiem iestatītu izpildes politikas, **\>\>** dodieties uz sadaļu Krājumu vadības iestatīšana krājumu un noliktavas vadības parametri **un** **pēc** tam cilnē Pārsūtīšanas pasūtījumi sadaļā Noliktavas pārvaldība atlasiet pārsūtīšanas pasūtījuma izpildes politiku.
- Lai iestatītu pārdošanas pasūtījumu izpildes politikas, **\>\>** **dodieties** uz sadaļu Debitoru parādu iestatīšanas debitoru parādu parametri un pēc tam cilnē Noliktavas pārvaldība atlasiet pārdošanas pasūtījuma izpildes politiku.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Atļaut nodot izpildei partijā un norādīt daudzumu, kas ir jālaiž partijā

Pakešuzdevums tiek izmantots pasūtījumu pārvietošanai uz noliktavu pakešveidā. Parametri, kas norāda pasūtījumus, kuri ir jāpalaiž pakešuzdevumā, tiek iestatīti pašā pakešuzdevumā.

Parametrs **Daudzums** norāda, vai paketē ir jāizlaiž viss daudzums vai fiziski rezervētais daudzums. Parametrs **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** nosaka, vai pasūtījumi paketē ir jāpieņem vai jānoraida, ja tie iepriekš bija izlaisti daļēji.

- Lai iestatītu daļēji izlaisto pasūtījumu parametru daudzumu **un atļautu izpildi pārsūtīšanas pasūtījumiem,** **pārejiet** uz sadaļu Noliktavas vadības pārvietošana uz noliktavu Automātiska pārsūtīšanas pasūtījumu izlaišana.**\>\>**
- Lai iestatītu daļēji izlaisto pasūtījumu parametru daudzumu **un atļautu izpildi pārdošanas pasūtījumiem,** **pārejiet** uz sadaļu Noliktavas vadības izlaišana noliktavai Automātiska pārdošanas pasūtījumu izlaišana.**\>\>**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
