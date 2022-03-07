---
title: Kompensācijas debitoriem
description: Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas. Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c313c03c6f3504f132a836eb6a67207e5f3c5636d43124c5f16d13992b9b604
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770765"
---
# <a name="reimburse-customers"></a>Kompensācijas debitoriem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas. Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu. 

Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

| Priekšnosacījums                                                            | Apraksts |
|-------------------------------------------------------------------------|-------------|
| Norādiet juridiskās personas minimālo kompensācijas summu.          | Lapas **Debitoru parādu parametri** apgabala **Vispārīgi** laukā **Minimālā kompensācija** ievadiet minimālo summu, ko var kompensēt saistībā ar debitora pārmaksām. |
| Neobligāti: pievienojiet kreditora kontu katram debitoram, kam var tikt izmaksāta kompensācija. | Lapas **Debitori** kopsavilkuma cilnes **Detalizēta papildinformācija** laukā **Kreditora konts** debitoram atlasiet kreditora kontu. |

Veidojot atlīdzināšanas darbības, tiek izveidots kreditora rēķins par kredīta bilances summu. Izpildot kompensēšanas procesu, no debitora konta tiek atskaitīta kredīta bilance, savukārt debitoram atbilstošajam kreditora kontam tiek izveidota apmaksājama bilance.

1. Debitoros izpildiet procesu **Atmaksa** (**Debitori \> Periodiski uzdevumi \> Atmaksa**).
2. Lai grupētu visus darījumus neatkarīgi no Virsgrāmatas dimensijām, iestatiet opciju **Apkopot debitoru** kā **Jā**. Lai grupētu tikai tos darījumus,, kuriem ir līdzīgas Virsgrāmatas dimensijas, iestatiet opciju kā **Nē**.
3. Atlasiet **Iekļaut debitorus ar nenokārtotiem debeta darījumiem**, lai atlasītu debitorus, kuriem ir nenosegtas debeta summas.
4. Lai atlīdzinātu noteiktus debitora kontus, kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrēt** un pēc tam norādiet debitora kontus vaicājumā.

    Kredīta summas tiek pārskaitītas uz debitoriem atbilstošajiem kreditoru kontiem un apstrādātas kā parasti maksājumi. Ja debitoram nav kreditora konta, debitoram automātiski tiek izveidots vienreizējs kreditora konts.

5. Lai skatītu izveidotos atlīdzības darījumus, izmantojiet pārskatu **Atmaksa** (**Debitori \> Pieprasījumi un pārskati \> Atmaksas pārskats**).
6. Sadaļā Kreditori izveidojiet maksājumu kreditora rēķiniem, kas tika izveidoti, veicot kompensācijas procesu. Informāciju par to, kā apmaksāt kreditorus, skatiet sadaļā [Kreditoru maksājumu pārskats](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]