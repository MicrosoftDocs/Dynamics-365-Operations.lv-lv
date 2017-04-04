---
title: "Darbības jomām balstīta apakšlīgumu slēgšana"
description: "Šajā tēmā aprakstīts sīkāk, kā izmantot apakšuzņēmuma līguma darbību ražošanas plūsmu liesās ražošanā."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Darbības jomām balstīta apakšlīgumu slēgšana

Šajā tēmā aprakstīts sīkāk, kā izmantot apakšuzņēmuma līguma darbību ražošanas plūsmu liesās ražošanā.

Microsoft Dynamics 365 operācijām, pastāv divas pieejas apakšlīguma: ražošanas pasūtījumus un liesās ražošana. Liesās ražošanas pieeju apakšuzņēmuma darbu ir modelēta kā pakalpojums, kas saistīts ar ražošanas plūsmas darbība. Īpaša veida izmaksu grupas tips, kas ir nosaukts **tiešu ārpakalpojumu** ir ieviesta un apakšlīguma pakalpojumi vairs nav daļa no materiālu komplekta (MK). Izmaksu uzskaites apakšuzņēmēju darbu pilnībā integrētu liesās ražošanas pašizmaksas risinājums.

## <a name="production-flows-that-involve-subcontractors"></a>Ražošanas plūsmas, kas iesaista apakšuzņēmējus
Pamatprincips ražošanas plūsmu nemainās, kad darbībām ir noslēgti apakšlīgumi. Materiālu joprojām plūst no viena novietojuma uz otru, procesu darbības pārvērstu materiālu produktu un nodošanas pasākumi pārvietot materiālus vai produktus no vienas atrašanās vietas uz citu. Jūs varat paraugs vietām un strādāt šūnās kā piegādātāja pārvaldīti piešķirot kreditora noliktavu vai resursa, resursu grupas.  

Pamatā šīs iespējas, liesās ražošana neprasa visas īpatnības nolūkā atbalstīt materiālu un produktu plūsmu. Visus iespējamos scenārijus, kas ietver piegādātājus, kā ražošanas vai transporta pakalpojumu sniedzēji var modelēt, pamatojoties uz arhitektūras produkcijas plūsma un aktivitātes.  

Piemēram, apakšuzņēmēja darbi no lielveikals, kas atrodas apakšuzņēmējs. Kad apstrādes vienības iztukšo ar apakšuzņēmēju, asambleja šūnas kopā ar nākamā krava tiek atgriezti kanban kartes. Lielveikalu ar apakšuzņēmēju, kas pēc tam tiek papildināta. Pārvedumi no apakšuzņēmēja un var modelēt kā tiešas nodošanas pasākumi izdošanas un nosūtīšanas procesu atbalstam. Ja skaidri reģistrācija nav vajadzīgs, lai atbalstītu fizisko transportu, pārvietošanas darbības var izlaist.  

Apakšuzņēmējs var izmantot, lai slodze līdzsvaru ražošanas plūsmu kopējo jaudu. Piemēram, ražošanas plūsmas ir modelēta, izmantojot plānoto kanban kārtulas. Plānotāja izmanto kanban plānošanas Padome plānotu un slodzes līmenis gan darba šūnas pēc pieprasījuma. Plānotāja arī uzrauga lielveikalā konsolidētos piegādes grafiks par **piegādes grafiks** lapā. Vairāki apakšuzņēmēji var modelēt vienas vai vairākas ražošanas plūsmām, un varētu būt vairākas kanban kārtulas, kuras var izmantot, lai sniegtu vienu un to pašu produktu uz vienu un to pašu atrašanās vietu, izmantojot dažādas aktivitātes. Plānotāju var pārvērst kanbans alternatīvu kanban noteikums, lai pārplānotu kanban, kas sākotnēji tika izveidota iekšējās ražošanas alternatīvu procesu. Patiesībā, šūnu darbu apakšuzņēmuma līguma raksturu neietekmē ražošanas plūsmu. Tas pats darba princips attiecas divas paralēlas iekšējās darba šūnām vai apakšlīgumā paredzētās divas šūnas.   

Tāpat kā citas darbības ražošanas plūsma, apakšuzņēmuma līguma darbību var patērēt un piegādi neuzskaitītā, izpētīja (darba procesā \[NP\]), un pusfabrikātu materiāliem un produktiem. Procesu plānošana un izpildes apakšuzņēmuma līguma darbību visos gadījumos ir vienādi. Turklāt šo procesu tāds pats kā iekšējie darba procesi.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Pirkšanas procesu par apakšuzņēmēju darbībām (pakalpojumi)
Pirkšanas procesā par apakšuzņēmuma līguma darbību pamatā ir fiziskā materiāla plūsmu, kas ir reģistrējis kanban darbu norisi, piemēram, uzsākt vai pabeigt. Finanšu plūsma, piemēram, apakšuzņēmēju darbu izmaksas ir sekundāro kontūru, kas seko fizisko plūsmu. Tajā pašā laikā pirkšanas procesā ir neatkarīgu procesu, kas ļauj veikt manuālu korekciju iepirkuma dokumentiem ik uz soļa. Šeit ir pirkuma process par apakšuzņēmuma līguma darbību:

1.  Izveidot pirkšanas līgums. Pirkuma līgums ir izveidoti pakalpojumu un pievienots ražošanas plūsmas aktivitāte.
2.  Izveidojiet pirkšanas pasūtījumu. Pirkšanas izpildpasūtījumu var izveidot pakalpojumu, pamatojoties uz plānoto kanban darbavietas. Darbu par vienu un to pašu pakalpojumu var grupēt pirkšanas pasūtījuma rindām, pa dienām, nedēļām vai mēnešiem. Pirkšanas pasūtījumu rindas var izveidot jebkurā laikā pēc tam, kad kanban darbavietu ir izveidots. Pirkšanas pasūtījumu rindas var izveidot pat pēc fakta. Parasti ir atlasīta šī opcija, ja apakšuzņēmējs sniedz pakalpojumus bez papildu brīdinājuma, pamatojoties uz kanbans vai kanban kartes, kas saņem apakšuzņēmējs. Šajā gadījumā var minimizēt novirzes starp pirkšanas pasūtījumam un rēķinam.
3.  Ģenerēt kanban kartes, materiālu un izdošanas sarakstam, lai nosūtītu uz apakšuzņēmēja, lai sagatavotu pārstrādei. Pamatojoties uz detalizētu ražošanas plūsmas modelēšana, sagatavošana tiek veikta kanban valdes darbības procesu, izmantojot izdošanas saraksta un sagatavošanas funkciju. Alternatīvi, sagatavošana tiek veikta kanban kuģa pārvietošanas darbiem, izmantojot izdošanas saraksta un sākuma vai Pabeigšana. Neuzskaitītā materiālam, abos procesos var atbalstīt WMS izdošanas un nosūtīšanas procesā. Pēc pieprasījuma var veidot preču transporta pavadzīmi.
4.  Ģenerēt kanban apstrādes bloki un kanban kartes. Pēc apstrādes kartes tiek atgriezti apakšuzņēmējs. Parasti kartēm ietver piegādes pavadzīme, kas norāda fiziskā materiāla, kas ir nosūtīti. Atsauce uz piedāvātajiem pakalpojumiem, nav nepieciešama. Materiālu vai produktu pie klienta ierašanās ir reģistrēta valdē kanban atkarībā no kanban kartes. (Kanban valdes darbības procesā vai kanban kuģa pārvietošanas darbiem izmanto atkarībā no modelēta darbības.).
5.  Izveidot konsultāciju kvīti. Konsultāciju saņemšana var izmantot, lai aizstātu iepakošanas slīdēšanas dokumentu par saņemtajiem pakalpojumiem. Saņemšanas padomus var ģenerēt atlasītajā periodā, pamatojoties uz aizpildīto kanban darbus par apakšuzņēmuma darbībām. Katra darba saņemšanas ieteikumus izveidotas attiecīgo pirkšanas pasūtījuma rindai. Konsultāciju saņemšana var izdrukāt un nosūtīt apakšuzņēmēja kā apstiprinājums par saņemšanu.
6.  Izveidot rēķinu.

Process beidzas, kad apakšuzņēmēja rēķina periodam. Mača rēķina tiek darīts pret saņemšanas padomus, kas tiek izveidoti. Jo saņemšanas padomus norāda precīzu fizisko materiālu saņemšanas, trīsceļu saskaņošana ir vienkāršota.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurējot darbību apakšlīguma
Nākamajās sadaļās ir aprakstīts, kā konfigurēt par apakšuzņēmuma darbībām.

### <a name="subcontracted-services"></a>Apakšuzņēmēju pakalpojumi

Ko izmanto darbībās balstīta apakšuzņēmuma maksājumu vienumam ir jābūt produkts, kuram ir šādas īpašības:

-   **Produkta tips:** pakalpojumu
-   **Ārējo krājumu modeļu grupā:** Non uzkrāti

Šo prasību izpilda pirmo lietošanu iekšā, pirmais ārā (FIFO) krājumu modelim. **Piezīme:** izmaksu produkti aprēķinam noteikt standarta pakalpojumu izmaksām. Pirkuma līgums ar piegādātāju, ir nepieciešama. Pretējā gadījumā pakalpojums nevar izmantot attiecībā uz darbības jomām balstīta apakšuzņēmuma līgumus.

### <a name="subcontracted-process-activities"></a>Apakšuzņēmuma līguma procesu darbības

Lai konfigurētu procesu aktivitātes, kā apakšuzņēmēju aktivitāte, rīkojieties šādi.

1.  Konfigurēt apakšuzņēmēju darbu šūnas. Lai konfigurētu darba šūna kā slēgts apakšlīgums, jāizveido resursu **kreditoru** tips un jāsaista ar darba šūnu (resursu grupa). Runtime izmaksu kategorija **tiešu ārpakalpojumu** izmaksu grupas tipam jāpiešķir šūnu darbu. Izmaksu kategorijas uzstādīšanas un daudzums nav nepieciešami.
2.  Pēc procesa aktivitāte ir izveidots un saistīto apakšuzņēmēju darbu šūnai, ir jākonfigurē servisa aktivitātes ražošanas plūsmas versiju var aktivizēt. Pabeidzot šo soli par **aktivitātes****detaļas** lapu. Par darbībām, kas saistītas ar apakšuzņēmēju darbu šūnu, **ziņā servisa** FastTab ir redzams. Par FastTab, pievienojiet noklusējuma pakalpojums, kas ir spēkā attiecībā uz visiem izejas elementiem. Ja konkrētam izvades elementiem nepieciešams dažādu pakalpojumu vai citu pakalpojumu aprēķinu parametrus (piemēram, dažādu pakalpojumu attiecība), var pievienot citus pakalpojumus aktivitāti.

## <a name="subcontracted-transfer-activities"></a>Nodošana apakšlīgumā paredzētās darbības
Pārvietošanas darbības ir konfigurēta kā apakšuzņēmēju aktivitāte, atkarībā no **Freighted** iestatījumu pārsūtīšanas darbības. Pieejamas šādas opcijas

-   **Ekspeditora** – aktivitāte ir slēgts apakšlīgums, ja pārsūtīšanai no noliktavas tiek vadīts, izmantojot piegādātāju (kā to nosaka noliktavas īpašuma). Visas atlasītās pirkšanas līgumus pakalpojumiem jābūt paša piegādātāja ID kā noliktava.
-   **Saņēmēja** – aktivitāte apakšlīgumu, ja pārsūtīšana uz noliktavu pārvalda kreditoru (kā to nosaka noliktavas īpašuma). Visas atlasītās pirkšanas līgumus pakalpojumiem jābūt paša piegādātāja ID kā noliktava.
-   **Pārvadātāja** – aktivitāte ir slēgts apakšlīgums piegādātājam, kas sniedz pakalpojumu. Būtu derīgs, pārvadātājam jāizveido noliktavas pārvaldības un piešķirtā piegādātāja konts.

Attiecībā uz procesu darbības, jums jākonfigurē noklusējuma pakalpojumu nodošana apakšlīgumā paredzētās darbības par **ziņā servisa** FastTab, **aktivitātes****detaļas** lapā.

## <a name="service-quantity-calculation"></a>Pakalpojuma daudzuma aprēķins
Visu iepirkuma procesa pamatā ir krājuma atsauce par pakalpojumu. Šī krājuma atsauce tiek mērīta pakalpojums mērvienība. Pakalpojumi parasti tiek mērītas dienestu (vienību) skaits vai laikā. Lai aprēķinātu pakalpojumu daudzumu, pamatojoties uz reģistrētā pabeigšana kanban darbavietas, var izmantot šādas metodes:

-   **Aprēķins, kas balstās uz darbavietu skaitu** – ir vienāds ar vienu kanban darbu *n* vienības pakalpojumu, neatkarīgi no produkta daudzuma, kas tiek nodrošināts kopā. Liesās ražošanas viens darbs atbilst vienas vienības. Šī aprēķina metode attiecas uz visiem pakalpojumiem, kas ir fiksētas cenas par vienu vienību norādē. Tādēļ šī metode parasti attiecas uz pārsūtīšanas darbībām. Tomēr to var arī lietot procesu darbības, kas apstrādā visu apstrādes vienības.
-   **Aprēķins, kas pamatojas uz produkta daudzumu** – pakalpojumu daudzums, salīdzinot ar produkta daudzums, kas ir plānoti vai piegādāts. Kad norādītais preču daudzums tiek aprēķināts, kļūdu daudzumu var vai nu iekļaut vai neiekļaut. Šo aprēķinu metodi piemēro visos gadījumos, kur pakalpojuma cena uz vienu vienību pārstrādātam produktam ir panākta vienošanās.
-   **Aprēķināšanu, kas balstīta uz darbības laiku** – teorētiskās aktivitātes laiku aprēķina, pamatojoties uz pārstrādes laiku aktivitātes, kopējais pārstrādes daudzumu un caurlaides koeficients pārstrādāto produktu. Šī aprēķina metode attiecas uz pakalpojumiem, kas apmaksāti ar stundu un ir novirze laikā par katru pārstrādāto produktu.

## <a name="cost-accounting-of-subcontracted-services"></a>Apakšuzņēmēju pakalpojumu izmaksu uzskaiti
Iegrāmatojot saņemšanas padomdevēju vai piegādātāju pavadzīmi pirkšanas pasūtījuma, kurš izveidots ražošanas plūsmas (citiem vārdiem sakot, pirkšanas pasūtījumu, kas tika ģenerēts, pamatojoties uz kanban darbu apakšuzņēmuma līguma darbību), ražošanas plūsmu RNR kontos uzskaita saņemšanas vērtība. Novirzes no rēķiniem, tiek uzskaitītas arī ražošanas plūsmu. Ir ieviesta apakšuzņēmēju darbu izmaksu kategoriju. Šīs izmaksu kategorijas Iespējot caurspīdīgu uzskaites vērtību apakšuzņēmēju darbs, kas ir piešķirti NP un patērē vienā periodā.  

Backflush, kalkulāciju liesās ražošanas pašizmaksas aprēķināšanas perioda beigās aprēķina faktisko dispersijas no produktiem, kas ir ražoti no ražošanas plūsmas izmaksu aprēķināšanas periodā.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelēšanas nodošanu apakšlīgumā paredzētās darbības
Cilvēki bieži uzskata transporta neproduktīvo un domāju, ka tā piebilst, nav vērtības. Tomēr apakšlīgumu izmaksas salīdzinājumā ar iekšējo ražošanas izmaksas, jāņem vērā papildu transporta izmaksas. Ražošanas plūsmas, kas sniedzas pāri vairākām vietām un pieprasa transporta pakalpojumi būtu modeļa transporta izmaksas, piegādājot pircējam preces izmaksu daļu. 

Liesās ražošanas darbībās balstīta apakšlīgumu noslēgšana ļauj integrēt pārvadātājiem un transporta pārdevēji, materiālu un izstrādājumu pārvietošanu starp vietām, kur notiek ražošanas plūsmu. Ar modelēšana nodošanas darbību, var piešķirt pārvadātājam vai kreditoru. Pārvietošanas darbības/darba pamatā ir pakalpojumu un pirkuma līgums, un var izveidot pirkšanas pasūtījumus un saņemšanas ieteikumus, pamatojoties uz reālajiem pārskaitīšanas darbavietas. Šī funkcionalitāte ir tāda pati kā apakšuzņēmēju procesu darbības funkcionalitāti.  

Tādēļ, Dynamics 365 tagad atbalsta MK aprēķinu, kas ietver transporta pakalpojumu izveidi saistīto pirkšanas pasūtījumus, integrētu saņemšanas reģistrācijas un transporta integrāciju operācijām pakalpojumu izmaksas par ražošanas plūsmas izmaksu.


