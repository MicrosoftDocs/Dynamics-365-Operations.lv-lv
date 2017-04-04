---
title: "Kompensācijas debitoriem"
description: "Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas. Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5b04558461c7b73e29897cb92de3dc76e2ca0a87
ms.lasthandoff: 03/31/2017


---

# <a name="reimburse-customers"></a>Kompensācijas debitoriem

Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas. Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu. 

Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

| Priekšnosacījums                                                            | Apraksts                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Norādiet juridiskās personas minimālo kompensācijas summu.          | Lapas **Debitoru parādu parametri** apgabala **Vispārīgi** laukā **Minimālā kompensācija** ievadiet minimālo summu, ko var kompensēt saistībā ar debitora pārmaksām. |
| Neobligāti: pievienojiet kreditora kontu katram debitoram, kam var tikt izmaksāta kompensācija. | Lapas **Debitori** kopsavilkuma cilnes **Detalizēta papildinformācija** laukā **Kreditora konts** debitoram atlasiet kreditora kontu.                                           |

Veidojot atlīdzināšanas darbības, tiek izveidots kreditora rēķins par kredīta bilances summu. Izpildot kompensēšanas procesu, no debitora konta tiek atskaitīta kredīta bilance, savukārt debitoram atbilstošajam kreditora kontam tiek izveidota apmaksājama bilance.

1.  Lapā Debitori palaidiet procesu **Kompensācija**.
2.  Izpildiet kādu no norādītajām transakcijām.
    -   Lai kompensāciju atskaitītu no noteiktiem debitora kontiem, noklikšķiniet uz **Atlasīt** un vaicājumā norādiet debitora kontus.
    -   Lai atlīdzinātu visu klientu kontus, klikšķiniet **Labi**.

    Kredīta summas tiek pārskaitītas uz debitoriem atbilstošajiem kreditoru kontiem un apstrādātas kā parasti maksājumi. Ja debitoram nav kreditora konta, debitoram automātiski tiek izveidots vienreizējs kreditora konts.
3.  Lai skatītu izveidotās kompensācijas transakcijas, izmantojiet lapu **Kompensācija**.
4.  Sadaļā Kreditori izveidojiet maksājumu kreditora rēķiniem, kas tika izveidoti, veicot kompensācijas procesu.



