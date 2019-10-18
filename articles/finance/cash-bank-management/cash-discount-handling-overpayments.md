---
title: Termiņatlaižu apstrāde pārmaksām
description: Šajā rakstā ir sniegti scenāriji, kas parāda, kā tiek apstrādāts maksājums, kad debitors izmanto termiņatlaidi, bet arī pārmaksā.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 803cb478bb7631439ebde66ad96182193d3dd1ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188353"
---
# <a name="handling-cash-discounts-for-overpayments"></a>Termiņatlaižu apstrāde pārmaksām

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti scenāriji, kas parāda, kā tiek apstrādāts maksājums, kad debitors izmanto termiņatlaidi, bet arī pārmaksā. 

Rēķins tiek uzskatīts par pārmaksātu, ja maksājuma summa ir lielāka par rēķina summu, atņemot termiņatlaidi. Lai norādītu, kā iegūstamā termiņatlaides starpība tiek uzskaitīta, kad rēķins ir pārmaksāts, izmantojiet laukus **Termiņatlaižu administrēšana** un **Maksimālā pārmaksa vai nepilna samaksa** lapā **Debitoru moduļa parametri**. Tālāk esošajā piemērā debitors ir pārmaksājis rēķinu par 0,50.

| Rēķina kopsumma | Pieejamā termiņatlaide | Maksājamā summa, kurā iekļauta termiņatlaide | Summa, kuru faktiski maksā debitors |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Termiņatlaižu administrēšana = Specifiska
Kad laukā **Termiņatlaižu administrēšana** ir atlasīta vērtība **Specifiska** lapā **Automātisko darījumu konti**, tiek ņemta pilna termiņatlaide. Pārmaksas summa tiek vai nu grāmatota termiņatlaides starpības virsgrāmatas kontā vai paliek kā bilance debitora kontā. Uzvedība ir atkarīga no tā, vai pārmaksas summa ir starp 0,00 un summu, kas ievadīta laukā **Maksimālā pārmaksa vai nepilna samaksa**, vai arī pārmaksas summa ir lielāka nekā summa laukā **Maksimālā pārmaksa vai nepilna samaksa**.

### <a name="scenario-1"></a>1. scenārijs

Šajā scenārijā pārmaksas summa ir starp 0,00 un maksimālo pārmaksu vai nepilnu samaksu. Ir ievadīts rēķins par summu 105,00 un termiņatlaide ir pieejama, ja rēķins tiek apmaksāts septiņu dienu laikā.

| Rēķina kopsumma | Pieejamā termiņatlaide | Maksājamā summa, kurā iekļauta termiņatlaide |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Debitors iesniedz maksājumu par summu 95,00 termiņatlaides perioda ietvaros. Maksājums tiek nosegts atbilstoši rēķinam par summu 105,00. Pēc rēķina un maksājuma nosegšanas debitoram modulī Debitori tiek izveidotas tālāk norādītās transakcijas.

| Transakcija   | Summa | Bilance |
|---------------|--------|---------|
| Rēķins       | 105,00 | 0,00    |
| Maksājums       | -95,00 | 0,00    |
| Termiņatlaide | -10,50 | 0,00    |

Maksājumam un nosegšanai tiek ģenerēti tālāk norādītie uzskaites ieraksti. **Maksājums**;

| Konts             | Debeta summa | Kredīta summa |
|---------------------|--------------|---------------|
| Kase                | 95,00        |               |
| Debitoru parādi |              | 95,00         |

**Segšana**

| Konts                                                                                                          | Debeta summa | Kredīta summa |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Termiņatlaide (laukā **Galvenais konts debitoru atlaidēm** lapā **Termiņatlaides**)                 | 10,50        |               |
| Debitoru parādi                                                                                              |              | 10,50         |
| Debitora termiņatlaide (lauks **Debitora termiņatlaide** lapā **Automātisko darījumu konti**) |              | 0,50          |
| Debitoru parādi                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>2. scenārijs

Šajā scenārijā pārmaksas summa pārsniedz maksimālo pārmaksas vai nepilnas samaksas summu. Ir ievadīts rēķins par summu 105,00 un termiņatlaide ir pieejama, ja rēķins tiek apmaksāts septiņu dienu laikā.

| Rēķina kopsumma | Pieejamā termiņatlaide | Maksājamā summa, kurā iekļauta termiņatlaide |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Debitors iesniedz maksājumu par summu 95,00 termiņatlaides perioda ietvaros. Maksājums tiek nosegts atbilstoši rēķinam par summu 105,00. Pēc rēķina un maksājuma nosegšanas debitoram modulī Debitori tiek izveidotas tālāk norādītās transakcijas.

| Transakcija   | Summa | Bilance |
|---------------|--------|---------|
| Rēķins       | 105,00 | 0,00    |
| Maksājums       | -95,00 | -0,50   |
| Termiņatlaide | -10,50 | 0,00    |

Pārmaksas summa 0,50 tiks saglabāta kā atvērta bilance maksājumā, un to var nosegt atbilstoši citam rēķinam. Maksājumam un nosegšanai tiek ģenerēti tālāk norādītie uzskaites ieraksti. **Maksājums**;

| Konts             | Debeta summa | Kredīta summa |
|---------------------|--------------|---------------|
| Kase                | 95,00        |               |
| Debitoru parādi |              | 95,00         |

**Segšana**

| Konts                                                                                          | Debeta summa | Kredīta summa |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Termiņatlaide (lauks **Galvenais konts debitoru atlaidēm** lapā **Termiņatlaides**) | 10,50        |               |
| Debitoru parādi                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Termiņatlaižu administrēšana = Nepecifiska
Kad laukā **Termiņatlaižu administrēšana** ir atlasīta vērtība **Nespecifiska** lapā **Automātisko darījumu konti**, termiņatlaides summa tiek samazināta par pārmaksas summu. Šī uzvedība vienmēr piemērojama, neatkarīgi no tā, vai pārmaksas summa ir lielāka vai mazāka par summu, kas tiek ievadīta laukā **Maksimālā pārmaksa vai nepilna samaksa**.

### <a name="scenario-3"></a>3. scenārijs

Šajā scenārijā ir ievadīts rēķins par summu 105,00 un termiņatlaide ir pieejama, ja rēķins tiek apmaksāts septiņu dienu laikā.

| Rēķina kopsumma | Pieejamā termiņatlaide | Maksājamā summa, kurā iekļauta termiņatlaide |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Debitors iesniedz maksājumu par summu 95,00 līdz termiņatlaides datumam. Maksājums tiek nosegts atbilstoši rēķinam par summu 105,00. Pēc rēķina un maksājuma nosegšanas debitoram modulī Debitori tiek izveidotas tālāk norādītās transakcijas.

| Transakcija   | Summa | Bilance |
|---------------|--------|---------|
| Rēķins       | 105,00 | 0,00    |
| Maksājums       | -95,00 | -0,00   |
| Termiņatlaide | -10,00 | 0,00    |

Termiņatlaides summa tiek samazināta no 10,50 uz 10,00. Maksājums un rēķins tiek uzskatīti par nosegtiem. **Maksājums**;

| Konts             | Debeta summa | Kredīta summa |
|---------------------|--------------|---------------|
| Kase                | 95,00        |               |
| Debitoru parādi |              | 95,00         |

**Segšana**

| Konts                                                                                          | Debeta summa | Kredīta summa |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Termiņatlaide (laukā **Galvenais konts debitoru atlaidēm** lapā **Termiņatlaides**) | 10,50        |               |
| Debitoru parādi                                                                              |              | 10,50         |





