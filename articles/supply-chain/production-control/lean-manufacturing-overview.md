---
title: Pārskats par metodi lean manufacturing
description: Šajā rakstā ir sniegts apskats un apraksts par lean manufacturing līdzekļiem programmā Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow, Kanban, KanbanQuantityOverview, KanbanAssignCard, KanbanCirculatingCards, KanbanRules, WHSKanbanWaveTableManagePickingListPool
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19371"
- intro-internal
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c8b5ec4d4a391773e32a61a321c28868678baa
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985940"
---
# <a name="lean-manufacturing-overview"></a>Lean manufacturing apskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts apskats un apraksts par lean manufacturing līdzekļiem programmā Dynamics 365 Supply Chain Management.

Lean manufacturing sniedz rīkus, ko varat izmantot, lai modelētu racionālas operācijas. Šie rīki atbalsta un veicina tālāk norādītās koncepcijas un biznesa aktivitātes.
-   Izveidojiet Lean manufacturing pamatu, ražošanas un loģistikas procesus modelējot kā ražošanas plūsmas.
-   Ieviesiet racionālās vilkšanas sistēmu, prasību pieprasījumu signalizēšanai izmantojot Kanban.
-   Pārraugiet un uzturiet Kanban darbus.

Lean manufacturing arhitektūra sastāv no ražošanas plūsmām, aktivitātēm un Kanban nosacījumiem. Šīs struktūras ir pilnīgi integrētas Supply Chain Management procesos. Varat izmantot Lean ražošanas procesu jaukta režīma ražošanas vidē, kurā ir apvienotas dažādas piegādes, ražošanas un avotu izmantošanas stratēģijas. Šīs stratēģijas iekļauj ražošanas pasūtījumus, partiju pasūtījumus apstrādes rūpniecības nozarēm, pirkšanas pasūtījumus un pārsūtīšanas pasūtījumus.

| **Svarīgi**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistēmu Supply Chain Management varat izmantot, lai atbalstītu Lean ražošanas procesa ieviešanu Kanban darbos. Taču sekmīga racionālo principu ieviešana ir atkarīga no jūsu izmantotajiem iekšējiem biznesa procesiem, kā arī no faktiskajiem ražošanas apstākļiem un vides. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a>Ražošanas un loģistikas procesu kā ražošanas plūsmu modelēšana
Lai izveidotu Lean ražošanas procesa pamatu, ražošanas un loģistikas procesus modelējiet kā ražošanas plūsmas. Šī aktivitāte sastāv no tālāk uzskaitītajiem uzdevumiem:
1.  Identificējiet procesus, kuriem vēlaties īstenot racionālās papildināšanas stratēģiju, un pēc tam modelējiet šos procesus kā ražošanas plūsmas. Pēc tam šos procesus varat analizēt un racionalizēt. Viens no racionālās ieviešanas mērķiem ir samazināt atkritumu daudzumu, uzlabojot materiālu un informācijas plūsmu.
2.  Ražošanas plūsmu definējiet kā secīgas aktivitātes, kas apraksta materiālu plūsmu. Pārsūtīšanas aktivitāte definē preces vai preču kustību no vienas vietas uz citu. Procesa aktivitāte definē pievienotās vērtības operāciju, kas tiek veikta kādai precei.
3.  Izveidojiet ražošanas plūsmas versiju, kas definē izgatavošanas laika pieprasījumus. Šie pieprasījumi tiek izmantoti, lai ražošanas plūsmā aprēķinātu katras aktivitātes cikla laiku. Varat izveidot vairākas ražošanas plūsmu versijas un pēc tam šīs versijas izmantot procesu uzlabošanai.

## <a name="using-kanbans-to-signal-demand-requirements"></a>Kanban izmantošana, lai signalizētu par prasību pieprasījumiem
Vilkšanas sistēma preces rada tikai tad, kad preces ir nepieciešamas. Šī prakse samazina piegādes izpildes laikus un lieko krājumu daudzumu. Lai plānotu, izsekotu un apstrādātu pieprasījumus, kuru pamatā ir ražošanas plūsmas, varat izmantot Kanban. Lai izveidotu Kanban struktūru, izveidojiet Kanban nosacījumus, kas definē, kad tiek izveidoti Kanban un kā tiek izpildīti pieprasījumi. Varat izveidot divus veidu Kanban nosacījumus. Ražošanas nosacījumi izveido procesa Kanban darbus, un atvilkumu Kanban nosacījumi izveido pārsūtīšanas Kanban darbus. Varat iestatīt tālāk aprakstītās papildināšanas stratēģijas:
-   **Fiksēts daudzums** Kanban kārtulas ir saistītas ar fiksētu skaitu materiālu apstrādes vienību, kas nozīmē, ka aktīvo Kanban skaits ir konstants. Ikreiz, kad ir patērētas visas preces no Kanban un ir manuāli iztukšotas materiālu apstrādes vienības, tiek izveidots jauns tāda paša tipa Kanban. Kad izveidojat fiksēta daudzuma Kanban kārtulas, varat aprēķināt optimālos Kanban daudzumus un izmantotos preču daudzumus. Šajā aprēķinā tiek ņemtas vērā prognozes, faktiskais pieprasījums no atvērtajiem pasūtījumiem, izpildes laiks līdz krājumu papildināšanai un vēsturiskais pieprasījums.
-   Kanban nosacījumi **Ieplānots** papildina pieprasījumus, kas tiek aprēķināti ar vispārējo plānošanu. Vispārējā plānošana ģenerē plānotos Kanban, kurus var apstiprināt uz Kanban.
-   Kanban kārtulas **Notikums** papildina pieprasījumus, kas cēlušies no pārdošanas pasūtījumu rindām, ražošanas MK rindām, Kanban rindām vai minimālo krājumu iestatījumiem. Kad tiek ģenerēti notikumu Kanban, tie tiek piesaistīti izcelsmes pieprasījumiem.

Kad tiek veidoti Kanban, tiek ģenerēts viens vai vairāki Kanban darbi, pamatojoties uz Kanban nosacījumos definētajām Kanban plūsmas aktivitātēm.

## <a name="monitoring-and-maintaining-kanban-jobs"></a>Kanban darbu pārraudzīšana un uzturēšana
Lean manufacturing nodrošina redzamību par Kanban nosacījumu noteikto ražošanas un loģistikas aktivitāšu pašreizējo statusu. Tādējādi varat plānot tālāk uzskaitītos uzdevumus un noteikt to prioritāti.

-   Gūstiet pārskatu par pašreizējo Kanban darbu grafiku.
-   Plānojiet un pārplānojiet Kanban darbus.
-   Izsekojiet un reģistrējiet Kanban darbu statusu.

Šajā sarakstā ir aprakstīti specializētie Kanban paneļi:
-   Kanban darbu plānošana — sniedz pārskatu par Kanban darbiem. Šajā panelī tiek rādīti Kanban darbi un to statuss vienai vai vairākās darba šūnās. Darbi ir uzskaitīti atbilstoši plānošanas periodiem (dienām vai nedēļām), kas ir definēti ražošanas plūsmas modelī. Šajā panelī tiek rādīts arī noslodzes patēriņš katram plānošanas periodam, lai jūs varētu pārraudzīt plānoto noslodzi. Varat mainīt Kanban darbu statusu, pārplānot Kanban darbus uz citiem plānošanas periodiem un veikt citus uzdevumus.
-   Kanban panelis pārsūtīšanas darbiem — šajā panelī tiek sniegts apskats par pašreizējiem pārsūtīšanas darbiem. Varat atjaunināt un reģistrēt izdošanas sarakstus, sākt un pabeigt pārsūtīšanas darbus, kā arī veikt citus uzdevumus.
-   Kanban panelis procesa darbiem — šis panelis ir paredzēts, lai atbalstītu normālo ražošanas plūsmu un sniegt apskatu par pašreizējo situāciju vienā vai vairākās darba šūnās. No šī paneļa Kanban darbiem var noteikt prioritātes, tos var izdot vai ražot. Šis panelis ir arī paredzēts, lai atbalstītu svītrkoda skenēšanu Kanban atskaitēm.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanban darbu un integrēšanas ar Supply Chain Management procesi
Kanban darbi ir pilnīgi integrēti pašreizējos procesos attiecībā uz krājumu transakcijām Supply Chain Management.
-   Varat veikt izdošanas aktivitātes, lai papildinātu materiālu, kas tiek izmantots, lai izpildītu Kanban darbu pieprasījumus.
-   Varat drukāt Kanban kartes, atkārtoti izmantojamās Kanban kartes un izdošanas sarakstus, lai atbalstītu Kanban izmantošanu. Šie dokumenti tiek izmantoti, lai attēlotu, izsekotu un reģistrētu Kanban darbus noliktavā un ražotnē.
-   Izdošanas un pārsūtīšanas aktivitātes varat reģistrēt krājumos, skenējot svītrkodus.

Turklāt Lean manufacturing atbalsta pirkšanas un rēķinu izrakstīšanas procesus attiecībā uz pakalpojumiem, uz kuriem atsaucas apakšlīgumā paredzētās aktivitātes.
-   Pirkšanas līguma rindas un pakalpojumus var piešķirt apakšlīgumā paredzētajām aktivitātēm.
-   Varat izveidot periodiskus pirkšanas pasūtījumus un paziņojumus par saņemšanu, lai atbalstītu pakalpojumu pirkšanu un rēķinu izrakstīšanu.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]