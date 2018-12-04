--- 
title: "Maksājumu metodes iestatīšana ISO20022 tiešajam debetam"
description: "Šajā procedūrā parādīts, kā iestatīt debitora maksājumu metodes ISO20022 tiešajam debetam vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 953a3cffc356ab44163944318e7e7d542a113112
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Maksājumu metodes iestatīšana ISO20022 tiešajam debetam

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt debitora maksājumu metodes ISO20022 tiešajam debetam vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu. 



Pirms uzdevuma pabeigšanas, ir jāiestata eksporta formāta konfigurācijas un maksājumu konti.



Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.



Šī ir trešā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.

1. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas metodes.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību ELECTRONIC.
3. Noklikšķiniet uz Rediģēt.
4. Laukā Maksājumu konts norādiet vērtības DEMF OPER.
5. Izvērsiet sadaļu Failu formāti.
6. Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.
7. Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.
    * Sarakstā atlasiet ISO20022 tiešais debets (DE).  Ja saraksts ir tukšs, tas nozīmē, ka nav importēta un aktīva debitora maksājuma eksporta formāta konfigurācija.  
8. Laukā Pieprasīt pilnvarojumu atlasiet Jā.
    * Atlasiet parametru Pieprasīt pilnvarojumu parametru debitora maksājumu formātiem, kuriem ir nepieciešama informāciju par pilnvarojumu maksājuma ziņojumā, piemēram, SEPA tiešais debets.  
9. Noklikšķiniet uz Saglabāt.


