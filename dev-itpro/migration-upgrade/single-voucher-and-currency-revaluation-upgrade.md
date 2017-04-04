---
title: "Vienotā dokumenta un valūtas pārvērtēšanas uzlabot Microsoft Dynamics 365 darbību versija 1611"
description: "Dažas organizācijas ievadiet žurnāli, kas ietver vienu dokumentu, kurā ir vairāk par vienu debitoru vai kreditoru, un tās tāpat vada debitoru parādos vai kontu jāmaksā ārvalstu valūtā, pārvērtēšanas procesā. Šajā tēmā ir aprakstīts, soļi, kas šīm organizācijām vajadzētu sekot, kad tās jaunināšanu uz Microsoft Dynamics 365 darbību versija 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Vienotā dokumenta un valūtas pārvērtēšanas uzlabot Microsoft Dynamics 365 darbību versija 1611

Dažas organizācijas ievadiet žurnāli, kas ietver vienu dokumentu, kurā ir vairāk par vienu debitoru vai kreditoru, un tās tāpat vada debitoru parādos vai kontu jāmaksā ārvalstu valūtā, pārvērtēšanas procesā. Šajā tēmā ir aprakstīts, soļi, kas šīm organizācijām vajadzētu sekot, kad tās jaunināšanu uz Microsoft Dynamics 365 darbību versija 1611.

Jaunināšanas uz Microsoft Dynamics 365 darbību versija 1611, izpildiet šīs darbības.

1.  Pirms jaunināt uz dinamiku 365 operācijām, izpilda ārvalstu valūtas pārvērtēšanas procesi debitoru parādos un parādos kreditoriem. Iestatiet **metodi** lauku, lai **rēķina datumu,**. Kas apvērš pēdējā ārvalstu valūtas pārvērtēšanas tiek izveidota pārvērtēšanas darbība. Tādēļ, atvērtās darbības tiek vērtēts pēc to sākotnējā uzskaites valūtā.
2.  Jaunināt uz dinamiku 365 darbību versija 1611.
3.  Vēlreiz palaidiet debitoru parādos un kontu jāmaksā ārzemju valūtas pārvērtēšanas procesi. Šajā laikā uzstādīt **metodi** lauku, lai **standarta**. Jauns pārvērtēšanas darbība tiek izveidota, pamatojoties uz pašreizējo valūtas maiņas kursu. Šo darbību reģistrē nerealizētā peļņa/zaudējumi un pareiza kopsavilkuma Virsgrāmatas kontu.



