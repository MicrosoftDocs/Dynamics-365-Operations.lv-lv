--- 
title: "Debitoru maksājumu papildu maksu izveide"
description: "Izveidojiet maksāšanas papildmaksas debitoru maksājumiem."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 659f4560747cea73c61a9b748a980946ca252bd6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-fees"></a>Debitoru maksājumu papildu maksu izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izveidojiet maksāšanas papildmaksas debitoru maksājumiem.

Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Komisijas maksa.
2. Noklikšķiniet uz Jauns.
3. Ievadiet papildmaksas ID laukā Papildmaksas ID.
    * Papildmaksas ID tiek attēlots maksājumu žurnālos, tāpēc pārliecinieties, ka tas ir aprakstošs un palīdz saprast papildmaksas veidu.  
4. Ievadiet papildmaksas nosaukumu laukā Nosaukums.
5. Ievadiet papildmaksas aprakstu laukā Papildmaksas apraksts.
6. Atlasiet, vai papildmaksa tiks attiecināta uz debitoru vai Virsgrāmatas kontu.
    * Ja debitors tiek aplikts ar papildmaksu, izvēlieties Debitors. Ja ar papildmaksu tiks aplikta jūsu organizācija, atlasiet Virsgrāmata. Šajā uzdevumā atlasiet Debitors.  
7. Atlasiet žurnāla tipu, kurā atļauts izmantot šo papildmaksu.
    * Ja šīs papildmaksas tiek izmantotas debitoru maksājumiem, žurnāla tips visdrīzāk būs Debitora maksājumi.  
8. Noklikšķiniet uz Saglabāt.
9. Noklikšķiniet uz Maksāšanas papildmaksu iestatījumi.
    * Maksājuma papildmaksas iestatījumi tiek izmantoti kritēriju definēšanai, lai noteiktu, kad tiks noteikta papildmaksa.  Piemēram, varat definēt, ka papildmaksa tiks aprēķināta, ja bankas konts ir USMF OPER un maksāšanas metode ir čeks.  
10. Lai definētu, kuriem bankas kontiem tiks noteikta šī papildmaksa, atlasiet Tabula, Grupa vai Visi.
    * Ja atlasāt Visi, šī papildmaksa var tikt piemērota visiem bankas kontiem.  Ja atlasāt Tabula, šī papildmaksa var tikt piemērota tikai izvēlētajam bankas kontam. Ja atlasāt Grupa, šī papildmaksa var tikt piemērota tikai bankas kontiem, kas pieder atlasītajai banku grupai.  
11. Atlasiet banku grupu vai bankas kontu.
    * Atlasot Tabula, bankas konti tiks attēloti, izmantojot uzmeklēšanas funkcionalitāti. Atlasot Grupa, banku grupas tiks attēlotas, izmantojot uzmeklēšanas funkcionalitāti.  
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Atlasiet maksāšanas metodi, kurai noteikt šo papildmaksu.
    * Piemēram, varat noteikt papildmaksu klientiem, ja tie veic maksājumus, izmantojot čekus nevis elektronisko maksājumu.  
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Ja nepieciešams, ievadiet maksāšanas valūtu.
    * Apmaksas valūta tiek izmantota kā papildu kritērijs, lai definētu, vai tiks noteikta papildmaksa.  Piemēram, jūsu banka var iekasēt papildu maksu par maksājumiem, kas saņemti USD valūtā, jo tā parasti veic operācijas tikai EUR valūtā.  
16. Atlasiet, vai papildmaksa būs procenti, summa vai intervāls.
17. Ievadiet papildmaksas procentus vai summu.
    * Ja laukā Procenti/Summa ir atlasīta vērtība Procenti, šeit ievadītā vērtība būs procentuālā daļa. Ja laukā Procenti/Summa ir atlasīta vērtība Summa, šeit ievadītā vērtība būs summa. Ja laukā Procenti/Summa ir atlasīta vērtība Intervāls, pakāpju definēšanai izmantojiet cilni Intervāls.  
18. Atlasiet papildmaksas valūtu laukā Papildmaksas valūta.
    * Šī ir valūta, kurā tiks izveidota papildmaksa.  
19. Noklikšķiniet uz Saglabāt.


