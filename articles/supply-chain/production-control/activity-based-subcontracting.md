---
title: No aktivitātēm atkarīgu apakšlīgumu slēgšana
description: Šajā tēmā ir detalizēti aprakstīts, kā lean manufacturing ražošanas plūsmā izmantot apakšlīgumā paredzētas aktivitātes.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ec47a13d9119c755702e019d09c76e1281b4a6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250228"
---
# <a name="activity-based-subcontracting"></a>No aktivitātēm atkarīgu apakšlīgumu slēgšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir detalizēti aprakstīts, kā lean manufacturing ražošanas plūsmā izmantot apakšlīgumā paredzētas aktivitātes.

Programmā Microsoft Dynamics 365 Supply Chain Management ir pieejamas divas apakšlīgumu slēgšanas metodes: ražošanas pasūtījumi un lean manufacturing. Ja izmantojat lean manufacturing metodi, tad apakšlīgumā paredzētais darbs tiek modelēts kā pakalpojums, kas ir saistīts ar kādu ražošanas plūsmas aktivitāti. Ir ieviests īpašs izmaksu grupas tips ar nosaukumu **Tiešie ārpakalpojumi**, un šādi apakšlīgumā paredzētie pakalpojumi vairs neveido daļu no materiālu komplektiem (MK). Apakšlīgumā paredzēto darbu izmaksu uzskaite ir pilnīgi integrēta lean manufacturing izmaksu aprēķināšanas risinājumā.

## <a name="production-flows-that-involve-subcontractors"></a>Ražošanas plūsmas, kurās piedalās apakšuzņēmēji
Ja par kādām aktivitātēm ir noslēgts apakšlīgums, ražošanas plūsmas pamatprincipi nemainās. Joprojām notiek materiālu plūsma starp novietojumiem, procesa aktivitātes materiālus pārvērš par precēm un pārsūtīšanas aktivitātes materiālus vai preces pārvieto no viena novietojuma uz citu. Novietojumus un darba šūnas varat modelēt kā kreditora pārvaldītas, piešķirot kreditora kontu kādai noliktavai vai kādam resursu grupas resursam.  

Pamatojoties uz šīm iespējām, lean manufacturing izmantošanai nav nepieciešami nekādi specifiski līdzekļi, lai atbalstītu materiālu un preču plūsmu. Visus iespējamos scenārijus, kuros kreditori ir iesaistīti kā ražošanas vai transportēšanas pakalpojumu nodrošinātāji, var modelēt, pamatojoties uz ražošanas plūsmas un aktivitāšu arhitektūru.  

Piemēram, kāds apakšuzņēmējs strādā ārpus lielveikala, kurš atrodas pie šī apakšuzņēmēja. Kad pie šī apakšuzņēmēja tiek iztukšotas materiālu apstrādes vienības, Kanban kartes tiek atgrieztas uz komplektēšanas šūnu kopā ar nākamo sūtījumu. Pēc tam lielveikals pie apakšuzņēmēja tiek papildināts. Pārsūtīšanu apakšuzņēmējam un no tā var modelēt kā skaidras pārsūtīšanas aktivitātes, lai tiktu atbalstīts izdošanas un nosūtīšanas process. Ja nav nepieciešama skaidra reģistrēšana, lai atbalstītu fizisko transportēšanu, tad pārsūtīšanas aktivitātes var nelietot.  

Apakšuzņēmēju var izmantot, lai ražošanas plūsmai līdzsvarotu vispārējās jaudas noslodzi. Piemēram, kāda ražošanas plūsma ir modelēta, izmantojot plānotus Kanban nosacījumus. Plānotājs lieto Kanban plānošanas paneli, lai plānotu un izlīdzinātu noslodzi abām darba šūnām pēc pieprasījuma. Plānotājs arī uzrauga lielveikala konsolidētās piegādes grafiku lapā **Piegādes grafiks**. Vienā vai vairākās ražošanas plūsmās var modelēt vairākus apakšuzņēmējus, un var pastāvēt vairāki Kanban nosacījumi, kurus varat lietot, lai vienu un to pašu preci piegādātu uz to pašu novietojumu, izmantojot dažādas aktivitātes. Plānotājs Kanban darbus var pārveidot par alternatīvu Kanban nosacījumu, lai kādu Kanban darbu, kurš sākotnēji tika izveidots iekšējai ražošanai, pārplānotu uz alternatīvu procesu. Faktiski apakšlīgumā paredzētās darba šūnas veids nekādi neietekmē ražošanas plūsmu. Tie paši darba principi ir spēkā gan divām paralēlām iekšējām darba šūnām, gan divām apakšlīgumā noteiktajām šūnām.   

Tāpat kā jebkura cita ražošanas plūsmas aktivitāte, arī apakšlīgumā paredzētās aktivitātes var patērēt un piegādāt inventarizētus, neinventarizētus (nepabeigtie projekti \[NP\]) un daļēji pabeigtus materiālus un preces. Visos gadījumos apakšlīgumā paredzēto aktivitāšu plānošana un izpilde ir tāda pati. Turklāt šie procesi ir tādi paši kā iekšējam darbam paredzētie procesi.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Pirkšanas process apakšlīgumā paredzētām aktivitātēm (pakalpojumi)
Pirkšanas process apakšlīgumā paredzētām aktivitātēm ir balstīts uz fizisko materiālu plūsmu, kas tiek reģistrēta ar Kanban darba progresu, piemēram, Sākt vai Pabeigt. Finanšu plūsma, piemēram, apakšlīgumā paredzētā darba izmaksas, ir sekundāra plūsma, kas seko fiziskajai plūsmai. Tajā pašā laikā pirkšanas process ir neatkarīgs process, kurā jebkurā posmā varat veikt manuālas pirkšanas dokumentu korekcijas. Tālāk ir aprakstīts pirkšanas process apakšlīgumā paredzētām aktivitātēm.

1.  Izveidojiet pirkšanas līgumu. Pirkšanas līgums tiek izveidots par pakalpojumu un savienots ar ražošanas plūsmas aktivitāti.
2.  Izveidojiet pirkšanas pasūtījumu. Pakalpojumam var izveidot izlaišanas pirkšanas pasūtījumu, pamatojoties uz ieplānotajiem Kanban darbiem. Viena un tā paša pakalpojuma darbus pirkšanas pasūtījuma rindās var grupēt pēc dienas, nedēļas vai mēneša. Pēc Kanban darba izveidošanas pirkšanas pasūtījuma rindas var izveidot jebkurā laikā. Pirkšanas pasūtījuma rindas var izveidot pat pēc pašas pirkšanas. Šī opcija parasti ir atlasīta tad, ja apakšuzņēmējs pakalpojumus sniedz bez papildu paziņojuma, pamatojoties uz Kanban darbiem vai Kanban kartēm, kuras šis apakšuzņēmējs saņem. Šādā gadījumā novirzes starp pirkšanas pasūtījumu un rēķinu iespējams minimizēt.
3.  Ģenerējiet apakšuzņēmējam sūtāmās Kanban kartes, materiālus un izdošanas sarakstu, lai sagatavotu apstrādāšanai. Pamatojoties uz ražošanas plūsmas detalizēto modelēšanu, procesa aktivitāšu Kanban kartēm tiek veikta sagatavošana, izmantojot izdošanas sarakstu un sagatavošanas funkciju. Ja vēlaties, pārsūtīšanas darbiem sagatavošanu var veikt ar Kanban paneli, izmantojot izdošanas sarakstu un sākšanu vai pabeigšanu. Inventarizētiem materiāliem šos abus procesus var atbalstīt NPS izdošanas un sūtīšanas process. Pēc pieprasījuma var izveidot preču transporta pavadzīmi.
4.  Ģenerējiet Kanban materiālu apstrādes vienības un Kanban kartes. Pēc apstrādāšanas kartes no apakšuzņēmēja tiek atgrieztas. Parasti kartēs ir iekļauta piegādes pavadzīme, kurā ir norādīts sūtītais fiziskais materiāls. Nav nepieciešama atsauce uz sniegtajiem pakalpojumiem. Fakts, ka debitors materiālu vai preci ir saņēmis, tiek reģistrēts Kanban panelī atkarībā no Kanban kartēm. (Atkarībā no modelētajām aktivitātēm tiek izmantots vai nu Kanban panelis procesa aktivitātēm, vai Kanban panelis pārsūtīšanas darbiem.)
5.  Izveidojiet ieejas plūsmas paziņojumu. Ieejas plūsmas paziņojumu var izmantot, lai aizstātu pavadzīmes dokumentu par saņemtajiem pakalpojumiem. Ieejas plūsmas paziņojumu var ģenerēt, pamatojoties uz pabeigtajiem Kanban darbiem attiecībā uz apakšlīgumu aktivitāti atlasītajā periodā. Par katru darbu ieejas plūsmu saistītajā pirkšanas pasūtījuma rindā tiek izveidoti paziņojumi. Ieejas plūsmas paziņojumu var drukāt un sūtīt apakšuzņēmējam ka apstiprinājumu par ieejas plūsmu.
6.  Ģenerējiet rēķinu.

Šis process beidzas, kad apakšuzņēmējs ir izrakstījis rēķinu par kādu periodu. Rēķinu saskaņošana tiek veikta pret izveidotajiem ieejas plūsmas paziņojumiem. Tā kā ieejas plūsmas paziņojumi atspoguļo tieši materiāla fizisko ieejas plūsmu, trīsvirzienu atbilstība ir vienkāršota.

## <a name="configuring-activities-for-subcontracting"></a>Aktivitāšu konfigurēšana apakšlīgumu slēgšanai
Nākamajās sadaļās ir aprakstīts, kā konfigurēt aktivitātes apakšlīgumu slēgšanai.

### <a name="subcontracted-services"></a>Apakšlīgumā paredzētie pakalpojumi

Maksājuma krājumam, kas tiek izmantots no aktivitātēm atkarīga apakšlīgumu slēgšanā, ir jābūt precei ar tālāk uzskaitītajām īpašībām.

-   **Preces tips:** Pakalpojums
-   **Krājumu modeļu grupa:** Noliktavā neesošs

Šī prasība liek izmantot krājumu modeli “pirmais iekšā, pirmais ārā” (first in, first out – FIFO). **Piezīme.** Preču izmaksu aprēķināšana nosaka, ka ir nepieciešams definēt pakalpojuma standarta izmaksas. Ir jābūt ar kreditoru noslēgtam pirkšanas līgumam. Pretējā gadījumā pakalpojumu nevar izmantot no aktivitātēm atkarīgai apakšlīgumu slēgšanai.

### <a name="subcontracted-process-activities"></a>Apakšlīgumā paredzētās procesa aktivitātes

Lai procesa aktivitāti konfigurētu kā apakšlīgumā paredzētu aktivitāti, izpildiet tālāk sniegtos norādījumus.

1.  Konfigurējiet apakšlīguma paredzētu darba šūnu. Lai kādu darba šūnu konfigurētu kā paredzētu apakšlīgumā, ir jāizveido resurss ar tipu **Kreditors** un šis resurss ir jāsaista ar attiecīgo darba šūnu (resursu grupu). Šai darba šūnai ir jāpiešķir izpildlaika izmaksu kategorija ar izmaksu grupas tipu **Tiešie ārpakalpojumi**. Izmaksu kategorijas iestatīšanai un daudzumam nav obligātas.
2.  Kad procesa aktivitāte ir izveidota un saistīta ar apakšlīgumā paredzētu darba šūnu, jums ir jākonfigurē pakalpojums šai aktivitātei, lai varētu aktivizēt šo ražošanas plūsmas versiju. Šī darbība ir jāveic lapā **Detalizēta informācija par** **aktivitāti**. Aktivitātēm, kas ir saistītas ar apakšlīgumā paredzētu darba šūnu, tiek rādīta kopsavilkuma cilne **Pakalpojuma nosacījumi**. Šajā kopsavilkuma cilnē pievienojiet noklusējuma pakalpojumu, kas ir derīgs visiem izejošās plūsmas krājumiem. Ja konkrētiem izejas plūsmas krājumiem ir nepieciešami citādi pakalpojumi vai citādi pakalpojuma aprēķināšanas parametri (piemēram, citāds pakalpojuma koeficients), šai aktivitātei varat pievienot citus pakalpojumus.

## <a name="subcontracted-transfer-activities"></a>Apakšlīgumā paredzētās pārsūtīšanas aktivitātes
Pārsūtīšanas aktivitāte kā apakšlīgumā paredzēta aktivitāte tiek konfigurēta atkarībā no šīs pārsūtīšanas aktivitātes iestatījuma **Kravas pārvadātājs**. Pieejamas šādas opcijas

-   **Nosūtītājs** — aktivitāte ir paredzēta apakšlīgumā, ja pārsūtīšanu no noliktavas pārvalda kāds kreditors (kā definēts ar noliktavas rekvizītu). Visiem atlasītajiem pirkšanas līgumiem attiecībā uz pakalpojumiem ir nepieciešams tāds pats kreditora ID kā noliktavai.
-   **Saņēmējs** — aktivitāte ir paredzēta apakšlīgumā, ja pārsūtīšanu uz noliktavu pārvalda kāds kreditors (kā definēts ar noliktavas rekvizītu). Visiem atlasītajiem pirkšanas līgumiem attiecībā uz pakalpojumiem ir nepieciešams tāds pats kreditora ID kā noliktavai.
-   **Pārvadātājs** — aktivitāte ir paredzēta apakšlīgumā jebkuram kreditoram, kurš nodrošina šādu pakalpojumu. Lai pārvadātājs būtu derīgs, tas ir jāizveido no noliktavas vadības un tam ir nepieciešams piesaistīts kreditora konts.

Attiecībā uz procesa aktivitātēm lapas **Detalizēta informācija par** **aktivitāti** kopsavilkuma cilnē **Pakalpojuma nosacījumi** jums ir jākonfigurē noklusējuma pakalpojums apakšlīgumā paredzētajām pārsūtīšanas aktivitātēm.

## <a name="service-quantity-calculation"></a>Pakalpojuma daudzuma aprēķins
Viss pirkšanas process ir balstīts uz krājuma atsauci kādam pakalpojumam. Šī krājuma atsauce tiek mērīta pakalpojuma mērvienībās. Parasti pakalpojumu daudzums tiek izteikts kā pakalpojumu skaits (vienības) vai laiks. Lai aprēķinātu pakalpojuma daudzumu, pamatojoties uz reģistrēto Kanban darbu pabeigšanu, varat izmantot tālāk aprakstītās metodes.

-   **No darbu skaita atkarīgais aprēķins** — viens Kanban darbs ir vienāds ar *n* pakalpojuma vienībām neatkarīgi no piegādātā preču daudzuma. Ja izmantojat lean manufacturing, tad viens darbs atbilst vienai materiālu apstrādes vienībai. Šī aprēķināšanas metode attiecas uz visiem pakalpojumiem, kam ir fiksēta cena par materiālu apstrādes vienību. Tādēļ šī metode parasti attiecas uz pārsūtīšanas aktivitātēm. Taču to var lietot arī tādu aktivitāšu apstrādāšanai, kurās tiek apstrādātas veselas materiālu apstrādes vienības.
-   **No preču daudzuma atkarīgais aprēķins** — pakalpojuma daudzums tiek izteikts relatīvi pret plānoto/piegādāto preču daudzumu. Kad ir aprēķināts piegādāto preču daudzums, kļūdainos daudzumus var iekļaut vai izslēgt. Šī aprēķināšanas metode attiecas uz visiem gadījumiem, kad pastāv vienošanās par pakalpojuma cenu par apstrādātās preces vienību.
-   **No aktivitātes laika atkarīgais aprēķins** — teorētiskie aktivitātes laiki tiek aprēķināti, pamatojoties uz aktivitātes apstrādāšanas laiku, kopējo apstrādāto daudzumu un apstrādātās preces caurlaides koeficientu. Šī aprēķināšanas metode attiecas uz pakalpojumiem, kas tiek apmaksāti pēc stundu skaita un kam pastāv novirze attiecībā uz apstrādātās preces laiku.

## <a name="cost-accounting-of-subcontracted-services"></a>Apakšlīgumā paredzēto pakalpojumu izmaksu uzskaite
Kad ir grāmatots ieejas plūsmas paziņojums vai kreditora pavadzīme par ražošanas plūsmai izveidotu pirkšanas pasūtījumu (citiem vārdiem — pirkšanas pasūtījums, kas bija ģenerēts, pamatojoties uz Kanban darbiem apakšlīgumā paredzētām aktivitātēm), tad ieejas plūsmas vērtība tiek iekļauta ražošanas plūsmas NP kontos. Arī rēķinu novirzes tiek iekļautas šajā ražošanas plūsmā. Ir ieviesta izmaksu kategorija apakšlīgumā paredzētam darbam. Šī izmaksu kategorija nodrošina caurskatāmu izsekošanu par apakšlīgumā paredzētā darba vērtību tādiem darbiem, kas ir piešķirti NP un tiek patērēti periodā.  

Atgriezeniska izmaksu aprēķināšana attiecībā uz lean manufacturing izmaksu aprēķināšanas perioda beigās aprēķina faktiskās novirzes precēm, kas attiecīgajā izmaksu aprēķināšanas periodā ir saražotas no ražošanas plūsmas.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Pārsūtīšanu kā apakšlīgumā paredzēto aktivitāšu modelēšana
Bieži vien ļaudis uzskata, ka transportēšana nav produktīva un nevairo nekādu vērtību. Taču kad apakšlīgumu slēgšanas izmaksas salīdzina ar iekšējās ražošanas izmaksām, ir jāņem vērā transportēšanas aktivitāšu papildu izmaksas. Ražošanas plūsmai, kas aptver vairākas atrašanās vietas un kurai ir nepieciešami transportēšanas pakalpojumi, transportēšanas izmaksas ir jāmodelē kā daļa no izmaksām par preču piegādi klientam. 

Kad izmantojat lean manufacturing, no aktivitātēm atkarīga apakšlīgumu slēgšana jums ļauj integrēt pārvadātājus un transporta kreditorus, kuri materiālus un preces pārvieto starp atrašanās vietām ražošanas plūsmā. Modelējot transportēšanas aktivitāti, varat piešķirt pārvadātāju vai kreditoru. Pārsūtīšanas aktivitātes/darbs ir atkarīgs no pakalpojuma un pirkšanas līguma, un pirkšanas pasūtījumus un ieejas plūsmas paziņojumus varat izveidot, pamatojoties uz faktiskajiem pārsūtīšanas darbiem. Šī funkcionalitāte ir tāda pati kā funkcionalitāte apakšlīgumā paredzētajām procesa aktivitātēm.  

Supply Chain Management tagad atbalsta MK aprēķinu, kas ietver transportēšanas pakalpojumus, saistīto pirkšanas pasūtījumu izveidi, integrētu ieejas plūsmas reģistrēšanu un transportēšanas pakalpojumu izmaksu integrēšanu ražošanas plūsmas izmaksu aprēķināšanā.



