---
title: "Liesās ražošanas pārskats"
description: "Šajā rakstā ir sniegts apskats un apraksts par lean manufacturing līdzekļiem sistēmā Microsoft Dynamics AX."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3c608f13c93446329702f07ef7e8bb08a29d87b9
ms.lasthandoff: 03/31/2017


---

# <a name="lean-manufacturing-overview"></a>Liesās ražošanas pārskats

Šajā rakstā ir sniegts apskats un apraksts par lean manufacturing līdzekļiem sistēmā Microsoft Dynamics AX.

Lean manufacturing sniedz rīkus, ko varat izmantot, lai modelētu racionālas operācijas. Šie rīki atbalsta un veicina tālāk norādītās koncepcijas un biznesa aktivitātes.
-   Izveidojiet Lean manufacturing pamatu, ražošanas un loģistikas procesus modelējot kā ražošanas plūsmas.
-   Ieviesiet racionālās vilkšanas sistēmu, prasību pieprasījumu signalizēšanai izmantojot Kanban.
-   Pārraugiet un uzturiet Kanban darbus.

Lean manufacturing arhitektūra sistēmā Microsoft Dynamics AX 7 sastāv no ražošanas plūsmām, aktivitātēm un Kanban nosacījumiem. Šīs struktūras ir pilnībā integrētas Microsoft Dynamics AX 7 procesos. Lean manufacturing varat izmantot jaukta režīma ražošanas vidē, kurā ir apvienotas dažādas piegādes, ražošanas un avotu izmantošanas stratēģijas. Šīs stratēģijas iekļauj ražošanas pasūtījumus, partiju pasūtījumus apstrādes rūpniecības nozarēm, pirkšanas pasūtījumus un pārsūtīšanas pasūtījumus.
| **Svarīgi **                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistēmu Microsoft Dynamics AX 7 varat izmantot, lai atbalstītu Lean manufacturing ieviešanu Kanban darbos. Taču sekmīga racionālo principu ieviešana ir atkarīga no jūsu izmantotajiem iekšējiem biznesa procesiem, kā arī no faktiskajiem ražošanas apstākļiem un vides. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Ražošanas un loģistikas procesu kā ražošanas plūsmu modelēšana
Lai izveidotu Lean manufacturing pamatu, ražošanas un loģistikas procesus modelējiet kā ražošanas plūsmas. Šī aktivitāte sastāv no tālāk uzskaitītajiem uzdevumiem.
1.  Identificējiet procesus, kuriem vēlaties īstenot racionālās papildināšanas stratēģiju, un pēc tam modelējiet šos procesus kā ražošanas plūsmas. Pēc tam šos procesus varat analizēt un racionalizēt. Viens no racionālās ieviešanas mērķiem ir samazināt atkritumu daudzumu, uzlabojot materiālu un informācijas plūsmu.
2.  Ražošanas plūsmu definējiet kā secīgas aktivitātes, kas apraksta materiālu plūsmu. Pārsūtīšanas aktivitāte definē preces vai preču kustību no vienas vietas uz citu. Procesa aktivitāte definē pievienotās vērtības operāciju, kas tiek veikta kādai precei.
3.  Izveidojiet ražošanas plūsmas versiju, kas definē izgatavošanas laika pieprasījumus. Šie pieprasījumi tiek izmantoti, lai ražošanas plūsmā aprēķinātu katras aktivitātes cikla laiku. Varat izveidot vairākas ražošanas plūsmu versijas un pēc tam šīs versijas izmantot procesu uzlabošanai.

## <a name="using-kanbans-to-signal-demand-requirements"></a> Kanban izmantošana, lai signalizētu par prasību pieprasījumiem
Vilkšanas sistēma preces rada tikai tad, kad preces ir nepieciešamas. Šī prakse samazina piegādes izpildes laikus un lieko krājumu daudzumu. Lai plānotu, izsekotu un apstrādātu pieprasījumus, kuru pamatā ir ražošanas plūsmas, varat izmantot Kanban. Lai izveidotu Kanban struktūru, izveidojiet Kanban nosacījumus, kas definē, kad tiek izveidoti Kanban un kā tiek izpildīti pieprasījumi. Varat izveidot divus veidu Kanban nosacījumus. Ražošanas nosacījumi izveido procesa Kanban darbus, un atvilkumu Kanban nosacījumi izveido pārsūtīšanas Kanban darbus. Varat iestatīt tālāk aprakstītās papildināšanas stratēģijas.
-   Kanban nosacījumi **Fiksēts daudzums** ir saistīti ar fiksētu skaitu materiālu apstrādes vienību, kas nozīmē, ka aktīvo Kanban skaits ir konstants. Ikreiz, kad visi no Kanban produkti tiek patērēti un apstrādes vienības manuāli iztukšo, tiek izveidots jauns kanban tāda paša tipa. Veidojot noteiktu daudzumu kanban kārtulas, var aprēķināt optimālu kanban daudzumiem un produktu daudzumu, kas tiek izmantoti. Šajā aprēķinā tiek ņemtas vērā prognozes, faktiskais pieprasījums no atvērtajiem pasūtījumiem, izpildes laiks līdz krājumu papildināšanai un vēsturiskais pieprasījums.
-   Kanban nosacījumi **Ieplānots** papildina pieprasījumus, kas tiek aprēķināti ar vispārējo plānošanu. Vispārējā plānošana ģenerē plānotos Kanban, kurus var apstiprināt uz Kanban.
-   Kanban nosacījumi **Notikums** papildina pieprasījumus, kas cēlušies no pārdošanas pasūtījumu rindām, ražošanas MK rindām, Kanban rindām vai minimālo krājumu iestatījumiem. Kad tiek ģenerēti notikumu Kanban, tie tiek piesaistīti izcelsmes pieprasījumiem.

Kad tiek veidoti Kanban, tiek ģenerēts viens vai vairāki Kanban darbi, pamatojoties uz Kanban nosacījumos definētajām Kanban plūsmas aktivitātēm.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Kanban darbu pārraudzīšana un uzturēšana
Lean manufacturing nodrošina redzamību par Kanban nosacījumu noteikto ražošanas un loģistikas aktivitāšu pašreizējo statusu. Tādējādi varat plānot tālāk uzskaitītos uzdevumus un noteikt to prioritāti.

-   Gūstiet pārskatu par pašreizējo Kanban darbu grafiku.
-   Plānojiet un pārplānojiet Kanban darbus.
-   Izsekojiet un reģistrējiet Kanban darbu statusu.

Šajā sarakstā ir aprakstīti specializētie Kanban paneļi:
-   Kanban darbu plānošana — sniedz pārskatu par Kanban darbiem. Šajā panelī tiek rādīti Kanban darbi un to statuss vienai vai vairākās darba šūnās. Darbi ir uzskaitīti atbilstoši plānošanas periodiem (dienām vai nedēļām), kas ir definēti ražošanas plūsmas modelī. Šajā panelī tiek rādīts arī noslodzes patēriņš katram plānošanas periodam, lai jūs varētu pārraudzīt plānoto noslodzi. Varat mainīt Kanban darbu statusu, pārplānot Kanban darbus uz citiem plānošanas periodiem un veikt citus uzdevumus.
-   Kanban panelis pārsūtīšanas darbiem — šajā panelī tiek sniegts apskats par pašreizējiem pārsūtīšanas darbiem. Varat atjaunināt un reģistrēt izdošanas sarakstus, sākt un pabeigt pārsūtīšanas darbus, kā arī veikt citus uzdevumus.
-   Kanban panelis procesa darbiem — šis panelis ir paredzēts, lai atbalstītu normālo ražošanas plūsmu un sniegt apskatu par pašreizējo situāciju vienā vai vairākās darba šūnās. No šī paneļa Kanban darbiem var noteikt prioritātes, tos var izdot vai ražot. Šis panelis ir arī paredzēts, lai atbalstītu svītrkoda skenēšanu Kanban atskaitēm.

## <a name="kanban-jobs-and-integration-with-microsoft-dynamics-ax-processes"></a> Kanban darbi un integrēšana Microsoft Dynamics AX procesos
Kanban darbi ir pilnībā integrēti pašreizējos procesos attiecībā uz krājumu transakcijām sistēmā Microsoft Dynamics AX.
-   Varat veikt izdošanas aktivitātes, lai papildinātu materiālu, kas tiek izmantots, lai izpildītu Kanban darbu pieprasījumus.
-   Varat drukāt Kanban kartes, atkārtoti izmantojamās Kanban kartes un izdošanas sarakstus, lai atbalstītu Kanban izmantošanu. Šie dokumenti tiek izmantoti, lai attēlotu, izsekotu un reģistrētu Kanban darbus noliktavā un ražotnē.
-   Izdošanas un pārsūtīšanas aktivitātes varat reģistrēt krājumos, skenējot svītrkodus.

Turklāt Lean manufacturing atbalsta pirkšanas un rēķinu izrakstīšanas procesus attiecībā uz pakalpojumiem, uz kuriem atsaucas apakšlīgumā paredzētās aktivitātes.
-   Pirkšanas līguma rindas un pakalpojumus var piešķirt apakšlīgumā paredzētajām aktivitātēm.
-   Varat izveidot periodiskus pirkšanas pasūtījumus un paziņojumus par saņemšanu, lai atbalstītu pakalpojumu pirkšanu un rēķinu izrakstīšanu.




