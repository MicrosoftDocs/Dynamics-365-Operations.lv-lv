---
title: "Tāda daļēja debitora maksājuma segšana, kam ir atlaides debitora kredītrēķiniem"
description: "Šajā rakstā ir aprakstīts scenārijs, kurā kredīta notai tiek piemērota termiņatlaide, ja sākotnējam rēķinam arī ir piemērota termiņatlaide."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4fbbd4d4b4ff9ecfcb30cd0ded2bc366d07dc1c4
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Tāda daļēja debitora maksājuma segšana, kam ir atlaides debitora kredītrēķiniem

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts scenārijs, kurā kredīta notai tiek piemērota termiņatlaide, ja sākotnējam rēķinam arī ir piemērota termiņatlaide. 

Fabrikam ļauj klientiem veikt termiņatlaides daļējiem maksājumiem, kā arī par kredīta notām (kredītrēķini). Termiņatlaidi var ņemt ar kredīta notu, kad kredīta nota tiek izsniegta rēķinam, par ko debitors ieguva termiņatlaidi. Kredīta par pilnu summu sniegšanas vietā varat kreditēt debitora bilance par summu, kas izslēdz termiņatlaides procentuālo vērtību, ko debitors ieguva. Nosegšanas parametri atrodas lapā **Debitoru moduļa parametri**.

## <a name="invoice-and-credit-note"></a>Rēķins un kredīta nota
Debitoram 4035 ir rēķins par 1000,00 un kredīta nota par 100,00. Katrā dokumentā ir 1 % atlaide, to apmaksājot 14 dienu laikā. Arnijs var apskatīt šo informāciju lapā **Debitoru darbības**.

| Dokuments    | Darījuma veids | Datums      | Rēķins  | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance  | Valūta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Rēķins          | 28.06.2015 | 10050    | 1000,00                             |                                       | 1000,00 | USD      |
| CCRN-10050 | Kredīta nota      | 28.06.2015 | CR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Kredīta notas nosegšana ar rēķinu
Lapā **Debitoru darbības** Arnijs atver lapu **Transakciju nosegšana**. Viņš var izmantot lapu **Transakciju nosegšana**, lai nosegtu gan rēķinu, gan kredītrēķinu. Kā daļu no segšanas procesa viņš skata termiņatlaides datumus un summas. Viņš atzīmē divus dokumentus un pēc tam noklikšķina uz **Grāmatot**, lai nosegtu transakcijas. Tā kā Fabrikam ir atlaides kredīta notās, atlaide sastāda -1,00 kredīta notā.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments    | Konts | Datums      | Izpildes datums  | Rēķins  | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10050  | 4035    | 28.06.2015 | 28.07.2015 | 10050    | 1000,00                       | USD      | 990,00           |
| Atlasīts | Parastais            | CCRN-10050 | 4035    | 28.06.2015 | 28.07.2015 | CR-10050 | -100,00                        | USD      | -99,00           |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 12.07.2015 |
| Termiņatlaides summa         | -1,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -1,00     |

Nosegšana būs 100,00; tiks iekļauts maksājums 99,00 un atlaide 1,00.



