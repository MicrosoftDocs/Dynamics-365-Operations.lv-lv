---
title: Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu
description: Šajā rakstā ir izskaidrots, kā izmantot rēķinu reģistru, lai izveidotu rēķinus, un pēc tam izmantot apstiprinājumu žurnālu, lai atjauninātu izdevumu kontus.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afe1471949bbf892f4e28ed3bea830ee491a517f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909219"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izmantot rēķinu reģistru, lai izveidotu rēķinus, un pēc tam izmantot apstiprinājumu žurnālu, lai atjauninātu izdevumu kontus.

## <a name="create-and-post-and-invoice"></a>Izveidot un grāmatot rēķinu
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu reģistrs**.
2. Atlasiet **Jauns**.
3. Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.
4. Atlasiet **Rindas**, lai atvērtu reģistru un ievadītu izmaksu rindas.
5. Atlasiet kreditoru. Piemēram, ievadiet vai atlasiet `US-104`.
6. Laukā **Rēķins** ierakstiet kādu vērtību.
7. Laukā **Apraksts** ierakstiet kādu vērtību.
8. Laukā **Kredīts** ievadiet kādu skaitli.
9. Laukā **Apstiprināja** nolaižamajā izvēlnē atlasiet apstiprinātāju.
10. Atlasiet **Grāmatot**.

## <a name="approve-an-invoice"></a>Apstiprināt rēķinu
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu apstiprināšana**.
2. Atlasiet **Jauns**.
3. Atlasiet nosaukumu tam rēķinu apstiprinājumu žurnālam, kuru vēlaties lietot.
4. Atlasiet **Rindas**, lai attēlotu lapu, kurā jūs varēsit atlasīt rēķinus, kurus vēlaties apstiprināt.
5. Atlasiet **Atrast dokumentus**, lai uzrādītu visus rēķinus, kuri ir gatavi apstiprināšanai.
6. Atzīmējiet rēķinu, kuru izveidojāt, tad noklikšķiniet uz **Atlasīt**. Jūsu iepriekš atlasītie dokumenti pēc to atlasīšanas tiek pārvietoti uz šo sarakstu.  
7. Atlasiet **Labi**.
8. Atlasiet lauku **konta numurs**, lai rēķinam pievienotu izdevumu kontu.
9. Ievadiet konta numuru un lauka cilni. Piemēram, ievadiet `600120`.
10. Atlasiet **Grāmatot**.
11. Atlasiet **Dokuments**, lai skatītu ievietotos ierakstus. Konts Rēķins, kas gaida apstiprinājumu, tiek anulēts un aizstāts ar faktisko izdevumu kontu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
