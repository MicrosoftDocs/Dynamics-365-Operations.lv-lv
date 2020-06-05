---
title: Izdevumu politiku definēšana
description: Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus programmā Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389719"
---
# <a name="define-expense-policies"></a>Izdevumu politiku definēšana

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

## <a name="policy-tips"></a>Politiku padomi
Tālāk ir minēti daži ieteikumi, kas var jums palīdzēt, veidojot jaunas politikas izmaksu pārvaldībai. 
* Politikām ir spēkā stāšanās datums, un tās nestāsies spēkā, ja politika tiek izveidota ar datumu pēc datuma, kad izdevumi radušies. Piemēram, ja šodien veidojat jaunu politiku, lai ieviestu maksimālos ēdināšanas izdevumus 50 ASV dolāru, apmērā, visi esošie izdevumi, kas ievadīti kopš vakardienas, netiks pārbaudīti attiecībā pret šo politiku.
* Veidojot politiku izdevumu kategorijai, kas var būt detalizēta, apsveriet iespēju pievienot izdevumu rindas tipa nosacījumu. Dažas politikas, piemēram, kvīts pieprasīšana, var būt neatbilstošas detalizētām rindām, un tās ieteicams piemērot tikai virsraksta rindai vai nedetalizētai rindai. 
* Izdevumu pārvaldības politikas tiek novērtētas attiecībā pret noklusējuma avota elementu. Starpuzņēmumu scenārijos varat iestatīt politiku, kas ir jāizvērtē, salīdzinot ar mērķa elementu (piesaistīšanas juridiskā persona). Lai palaistu ar mērķa elementu salīdzināmu politiku, **Līdzekļu pārvaldības** darbvietā ieslēdziet līdzekli "novērtēt izdevumu politiku salīdzinājumā ar piesaistīšanas juridisko personu".

## <a name="when-to-evaluate-policies"></a>Politiku novērtēšanas laiks

Izdevumu pārvaldības parametros ir iespēja novērtēt izdevumu pārvaldības politikas, kad rinda tiek saglabāta vai kad tiek iesniegts izdevumu pārskats. Ja izvēlaties veikt novērtēšanu, kad rinda tiek saglabāta, tas nodrošina to, ka lietotājam agrāk tiek parādīts, kas jādara, lai pabeigtu izdevumu pārskatu uzreiz. Pretējā gadījumā varat aizkavēt politikas novērtēšanu un ietaupīt laiku, ja validācija tiek veikta beigās, kad notiek iesniegšana darbplūsmā.
