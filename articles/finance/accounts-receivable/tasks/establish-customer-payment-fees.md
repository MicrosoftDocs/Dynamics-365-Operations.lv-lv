---
title: Debitoru maksājumu papildu maksu izveide
description: Izveidojiet maksāšanas papildmaksas debitoru maksājumiem.
author: ShivamPandey-msft
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc02da71ef6edbf1b88395a52c3fcbfca62cc82f
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714430"
---
# <a name="establish-customer-payment-fees"></a>Debitoru maksājumu papildu maksu izveide

[!include [banner](../../includes/banner.md)]

Izveidojiet maksāšanas papildmaksas debitoru maksājumiem.

Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Debitori > Maksājumu iestatīšana > Komisijas maksa**.
2. Klikšķiniet **Jauns**.
3. Laukā **Maksas ID** ievadiet Maksas ID. Papildmaksas ID tiek attēlots maksājumu žurnālos, tāpēc pārliecinieties, ka tas ir aprakstošs un palīdz saprast papildmaksas veidu.  
4. Laukā **Nosaukums** ievadiet maksas nosaukumu.
5. Laukā **Maksas apraksts** ievadiet maksas aprakstu.
6. Laukā **Iekasētā maksa** atlasiet, vai maksa tiks iekasēta no Klienta vai Virsgrāmatas konta. Ja debitors tiek aplikts ar papildmaksu, izvēlieties Debitors. Ja ar papildmaksu tiks aplikta jūsu organizācija, atlasiet Virsgrāmata. Šajā uzdevumā atlasiet Debitors.  
7. Laukā **Žurnāla tips** atlasiet žurnāla tipu, kas var izmantot šo komisijas maksu. Ja šīs papildmaksas tiek izmantotas debitoru maksājumiem, žurnāla tips visdrīzāk būs Debitora maksājumi.  
8. Noklikšķiniet uz **Saglabāt**.
9. Noklikšķiniet uz **Komisijas maksas iestatīšana**. Maksājuma papildmaksas iestatījumi tiek izmantoti kritēriju definēšanai, lai noteiktu, kad tiks noteikta papildmaksa.  Piemēram, varat definēt, ka papildmaksa tiks aprēķināta, ja bankas konts ir USMF OPER un maksāšanas metode ir čeks.  
10. Laukā **Grupējumi** atlasiet vai nu Tabula, Grupa vai Visi, lai noteiktu, kuri bankas konti tiks novērtēti šai maksai. Ja atlasāt Visi, šī papildmaksa var tikt piemērota visiem bankas kontiem.  Ja atlasāt Tabula, šī papildmaksa var tikt piemērota tikai izvēlētajam bankas kontam. Ja atlasāt Grupa, šī papildmaksa var tikt piemērota tikai bankas kontiem, kas pieder atlasītajai banku grupai.  
11. Laukā **Bankas saite** atlasiet vai nu bankas grupu, vai nu bankas kontu. Atlasot Tabula, bankas konti tiks attēloti, izmantojot uzmeklēšanas funkcionalitāti. Atlasot Grupa, banku grupas tiks attēlotas, izmantojot uzmeklēšanas funkcionalitāti.  
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā **Maksāšanas veids** atlasiet Maksāšanas veidu, kuram šī maksa tiks novērtēta. Piemēram, varat noteikt papildmaksu klientiem, ja tie veic maksājumus, izmantojot čekus nevis elektronisko maksājumu.  
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Ja nepieciešams, laukā **Maksājuma valūta** ievadiet maksājuma valūtu. Apmaksas valūta tiek izmantota kā papildu kritērijs, lai definētu, vai tiks noteikta papildmaksa.  Piemēram, jūsu banka var iekasēt papildu maksu par maksājumiem, kas saņemti USD valūtā, jo tā parasti veic operācijas tikai EUR valūtā.  
16. Atlasiet, vai papildmaksa būs procenti, summa vai intervāls.
17. Laukā **Procenti/Summa** ievadiet maksas summu vai procentuālo vērtību. Ja laukā Procenti/Summa ir atlasīta vērtība Procenti, šeit ievadītā vērtība būs procentuālā daļa. Ja laukā Procenti/Summa ir atlasīta vērtība Summa, šeit ievadītā vērtība būs summa. Ja laukā Procenti/Summa ir atlasīta vērtība Intervāls, pakāpju definēšanai izmantojiet cilni Intervāls.  
18. Laukā **Maksas valūta** atlasiet maksas valūtu. Šī ir valūta, kurā tiks izveidota papildmaksa.  
19. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
