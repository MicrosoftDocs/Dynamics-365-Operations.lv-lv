---
title: Izdevumu politiku definēšana
description: Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus programmā Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514443"
---
# <a name="expense-policies"></a>Izdevumu ierobežojumi

[!include [banner](../includes/banner.md)]

Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus.         
Izdevumu politikas ieviešana var palīdzēt efektīgi pārvaldīt izdevumus.         

Varat iestatīt, piemēram, politiku attiecībā uz viesnīcas izdevumiem Ņujorkā, kurā ir norādīts, ka izdevumi par vienu nakti nedrīkst pārsniegt 250 USD.       
Ja darbinieks iesniedz izdevumu pārskatu vai komandējuma pieprasījumu, kurā maksa par naktsmītni ir lielāka par šo summu, sistēma informēs        
darbinieku par to, ka tika pārsniegta izdevumu politikas summa. Varat konfigurēt ziņojumu, ko parādīt darbiniekam,        
kad definējat politiku.      
        
Varat definēt trīs tipu politikas.         
        
- Brīdinājums — ļauj darbiniekam iesniegt izdevumu pārskatu vai komandējuma pieprasījumu, bet izdevumi tiks atzīmēti visiem apstiprinātājiem un        
  vēlākai ziņošanai.        

- Kļūda — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas liek darbiniekam pārskatīt izdevumus, lai tie atbilstu politikai.       
 
 - Pamatojums — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas darbiniekam vai vadītājam liek ievadīt politikas summas pārsniegšanas pamatojumu.        

# <a name="policy-tips"></a>Politiku padomi
Tālāk ir minēti daži ieteikumi, kas var jums palīdzēt, izveidojot jaunas politikas izmaksu pārvaldībai. 
* Politikām ir spēkā stāšanās datums, un tās nestāsies spēkā, ja politika tiek izveidota ar datumu pēc datuma, kad izdevumi radušies. Piemēram, ja šodien veidojat jaunu politiku, lai ieviestu maksimālos ēdināšanas izdevumus 50 ASV dolāru, apmērā, visi esošie izdevumi, kas ievadīti kopš vakardienas, netiks pārbaudīti attiecībā pret šo politiku.
* Veidojot politiku izdevumu kategorijai, kas var būt detalizēta, apsveriet iespēju pievienot izdevumu rindas tipa nosacījumu. Dažas politikas, piemēram, kvīts pieprasīšana, var būt neatbilstošas detalizētām rindām, un tās ieteicams piemērot tikai virsraksta rindai vai nedetalizētai rindai. 

# <a name="when-to-evaluate-policies"></a>Politiku novērtēšanas laiks

Izdevumu pārvaldības parametros ir iespēja novērtēt izdevumu pārvaldības politikas, kad rinda tiek saglabāta vai kad tiek iesniegts izdevumu pārskats. Ja izvēlaties veikt novērtēšanu, kad rinda tiek saglabāta, tas nodrošina to, ka lietotājam agrāk tiek parādīts, kas jādara, lai pabeigtu izdevumu pārskatu uzreiz. Pretējā gadījumā varat aizkavēt politikas novērtēšanu un ietaupīt laiku, ja validācija tiek veikta beigās, kad notiek iesniegšana darbplūsmā.
