---
title: QR koda vai svītrkoda pievienošana transakciju un kvīšu e-pastiem
description: Šajā tēmā paskaidrots, kā ievietot QR kodus un svītrkodus, kuri norāda uz pasūtījuma ID, transakciju un kvīšu e-pastos risinājumā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3cc4fcb1237f8409a89b3d4818c132c60c57b5a0
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555426"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>QR koda vai svītrkoda pievienošana transakciju un kvīšu e-pastiem

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā paskaidrots, kā ievietot QR kodus un svītrkodus, kuri norāda uz pasūtījuma ID, transakciju un kvīšu e-pastos risinājumā Microsoft Dynamics 365 Commerce.

Jūs varat viegli iekļaut QR kodus un svītrkodus transakciju e-pastos, lai paātrinātu pasūtījuma uzmeklēšanas procesu mazumtirdzniecības vidē. Lai e-pastos ievadītu QR kodus un svītrkodus, jūs izmantojat HTML **\<img\>** atzīmi, kura pieprasa QR koda vai svītrkoda attēlu no ģenerēšanas un atveides pakalpojuma. Korporācija Microsoft nenodrošina šo pakalpojumu. Taču ir daudzi bezmaksas vai izdevīgi pakalpojumi, kuri apkalpo QR kodus vai svītrkodus, kuri tiek dinamiski ģenerēti, balstoties kārtībā, kas tiek padota pieprasījumu virknē.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>QR koda vai svītrkoda pievienošana transakcijas e-pastam

Lai ievietotu QR kodu vai svītrkodu transakcijas e-pastā, kas tiek izsūtīts kā daļa no e-komercijas pirkuma, izpildiet šīs darbības:

1. Atveriet transakcijas e-pasta veidnes HTML un pievienojiet HTML **\<img\>** atzīmi, kura norāda uz jūsu QR koda vai svītrkoda pakalpojumu. Tālāk ir minēts piemērs.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Šeit ir iepriekšējā parauga skaidrojums:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE**  norāda uz jūsu QR koda vai svītrkoda pakalpojuma domēnu.
    - **dati** ir parametrs, kuru QR koda vai svītrkoda pakalpojums izmanto, lai saņemtu saturu, kuru vajadzētu atveidot kā QR kodu vai svītrkodu.

        Šim parametram ir jāpiešķir vērtība **%salesid%**. Ievērojiet, ka šajā piemērā vērtība tiek arī izmantota kā attēla alternatīvais teksts.

    - **param1** un **param2** norāda uz papildu, neobligātiem parametriem.

1. Dodieties uz **Retail un Commerce \> Galvenās pārvaldes iestatīšana \> Parametri \> Organizācijas e-pastu veidnes** un augšupielādējiet atjaunināto HTML atbilstošajā transakcijas e-pasta veidnē.

> [!NOTE]
> Parametri var atšķirties QR koda un svītrkoda pakalpojumu sniedzēju starpā. Tāpēc pārliecinieties, ka sazināties ar savu pakalpojumu sniedzēju, lai apstiprinātu parametrus, kuriem jums ir jāpiešķir vērtības.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>QR koda vai svītrkoda pievienošana kvīts e-pastam 

Lai ievietotu QR kodu vai svītrkodu kvīts e-pastā, ko var nosūtīt pēc pirkuma veikšanas pārdošanas punktā (POS), izpildiet šīs darbības:

1. Atveriet kvīts e-pasta veidnes HTML un pievienojiet HTML **\<img\>** atzīmi, kura norāda uz jūsu QR koda vai svītrkoda pakalpojumu. Tālāk sniegts piemērs.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Šeit ir iepriekšējā parauga skaidrojums:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE**  norāda uz jūsu QR koda vai svītrkoda pakalpojuma domēnu.
    - **dati** ir parametrs, kuru QR koda vai svītrkoda pakalpojums izmanto, lai saņemtu saturu, kuru vajadzētu atveidot kā QR kodu vai svītrkodu.

        Šim parametram ir jāpiešķir vērtība **%receiptid%**. Ievērojiet, ka šajā piemērā vērtība tiek arī izmantota kā attēla alternatīvais teksts.

    - **param1** un **param2** norāda uz papildu, neobligātiem parametriem.

1. Dodieties uz **Retail un Commerce \> Galvenās pārvaldes iestatīšana \> Parametri \> Organizācijas e-pastu veidnes** un augšupielādējiet atjaunināto HTML e-pasta veidnē ar e-pasta ID **emailrecpt**.

> [!NOTE]
> Parametri var atšķirties QR koda un svītrkoda pakalpojumu sniedzēju starpā. Tāpēc pārliecinieties, ka sazināties ar savu pakalpojumu sniedzēju, lai apstiprinātu parametrus, kuriem jums ir jāpiešķir vērtības.

## <a name="additional-resources"></a>Papildu resursi

[E-pasta kvīšu sūtīšana no Modern POS (MPOS)](email-receipts.md)

[E-pasta ziņojumu veidņu izveide transakciju notikumiem](email-templates-transactions.md)
