---
title: "Ražošanas apakšuzņēmēja darba pārvaldība"
description: "Šajā tēmā ir aprakstīts, kā programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek pārvaldītas apakšuzņēmēja operācijas. Tas nozīmē, ka tajā ir paskaidrots, kā kreditors pārvalda resursam piešķirtās ražošanas operācijas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0e1368d3f637143fd47c3772c811257e8472cc74
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Ražošanas apakšuzņēmēja darba pārvaldība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek pārvaldītas apakšuzņēmēja operācijas. Tas nozīmē, ka tajā ir paskaidrots, kā kreditors pārvalda resursam piešķirtās ražošanas operācijas.

[Ražošanas procesu](production-process-overview.md) ietvaros darbu var veikt kreditoriem piederoši vai kreditoru administrēti resursi. Parasti kreditora resursi tiek izmantoti, lai apmierinātu periodiski radīto papildu pieprasījumu, kas pārsniedz uzņēmuma resursu ražīgumu. Kreditors, iespējams, var piedāvāt arī īpašas [resursu iespējas](resource-capabilities.md)vai resursus par zemāku cenu.  

Atkarībā no kreditora resursiem, kas tiek izmantoti ražošanas procesā, [maršrutam](routes-operations.md) bieži ir papildu loģistikas prasības, jo materiāli un daļēji pabeigtās preces vispirms ir jātransportē uz kreditora apstrādes vietu. Pēc tam apakšuzņēmēja operācijas rezultāts ir jātransportē uz nākamajai operācijai piešķirto atrašanās vietu vai gatavo preču noliktavu.  

Ja tiek izmantotas apakšuzņēmēja operācijas vai aktivitātes, tās ietekmē visus operāciju posmus no nepieciešamo ražošanas, izmaksu aprēķināšanas, prognozēšanas, plānošanas un grafika izstrādes operāciju definēšanas līdz materiālu, daļēji pabeigto preču un gatavo preču loģistikas pārvaldībai. Turklāt šiem resursiem ir nepieciešami savi uzskaites un izmaksu kontroles procesi.  

Iekšējiem resursiem parasti tiek piešķirta fiksēta izmaksu likme par periodu. Turpretim apakšuzņēmēja resursu izmaksas tiek noteiktas, pamatojoties uz saistītā pakalpojuma pirkšanas cenu. Pakalpojums tiek definēts kā cita prece, un tas tiek izmantots konkrētās apakšuzņēmēja operācijas sagādes un iegādes procesu vadībai.  

Pašlaik programmatūrā Microsoft Dynamics 365 for Finance and Operations nav īpašas daļēji pabeigto preču koncepcijas. Ja ražošanas pasūtījuma ietvaros izejmateriālu pārveidošanai par gatavo preci ir nepieciešamas vairākas operācijas, šī pasūtījuma gatavā prece tiek grāmatota atpakaļ krājumos tikai pēdējās operācijas laikā. Daļēji pabeigtās preces, kas tika iegūtas iepriekšējo operāciju laikā, tiek uzskaitītas kā nepabeigtais darbs (NP), taču tās netiek grāmatotas vai izsekotas krājumos. Lai gan maršrutus un materiālu komplektus (MK) var sadalīt vairākās mazākās vienībās, tādējādi tiek palielināts pārvaldāmo preču, MK un maršrutu skaits.  

Ir pieejamas divas metodes ražošanas operāciju apakšuzņēmēja darbu pārvaldībai. Šīm metodēm atšķiras veids, kā var modelēt apakšlīgumu slēgšanas procesus, kā tiek atainotas daļēji pabeigtās preces procesa ietvaros un kā tiek pārvaldīta izmaksu kontrole.

-   Apakšlīgumu slēgšana par ražošanas pasūtījumu vai partijas pasūtījumu maršruta operācijām
    -   Pakalpojuma precei ir jābūt uzkrātai precei, un tai ir jābūt ietvertai MK.
    -   Šī metode atbalsta principu “pirmais iekšā, pirmais ārā” (FIFIO) vai standarta izmaksas.
    -   Daļēji pabeigtās preces procesa ietveros tiek atainotas kā pakalpojuma prece.
    -   Izmaksu kontrole nodrošina ar apakšuzņēmēja darbu saistīto izmaksu piešķiri materiālu izmaksām.
-   Ražošanas plūsmas aktivitāšu apakšlīgumu slēgšana racionālās ražošanas plūsmā
    -   Pakalpojums ir neuzkrāta pakalpojuma prece, un tas nav ietverts MK.
    -   Šajā metodē pirkšanas līgumi tiek lietoti kā pakalpojumu līgumi.
    -   Šajā metodē tiek lietota atgriezeniskā izmaksu aprēķināšana.
    -   Šī metode sniedz iespēju veikt uzkrāto un asinhrono sagādi. (Materiālu plūsma ir neatkarīga no sagādes procesa.)
    -   Izmaksu kontrole nodrošina apakšuzņēmēja darba piešķiri atsevišķā izmaksu sadalījuma blokā.

## <a name="subcontracting-of-route-operations"></a>Maršruta operāciju apakšlīgumu slēgšana
Lai izmantotu ražošanas vai partijas pasūtījumu maršruta operāciju apakšlīgumus, pakalpojuma sagādei izmantotajai pakalpojuma precei ir jābūt definētai kā veida **Pakalpojums** precei. Turklāt tās krājumu mērķu grupai sadaļā **Krājumu politika** ir jābūt iestatītai opcijas **Uzkrātā prece** vērtībai **Jā**. Izmantojot šo opciju, tiek definēts tas, vai prece saņemšanas laikā tiek uzskaitīta kā krājums (**Uzkrātā prece** = **Jā**) vai arī preces izdevumi tiek grāmatoti peļņas un zaudējumu kontā (**Uzkrātā prece** = **Nē**). Lai gan šī darbība var šķist neatbilstoša, tas tiek darīts, pamatojoties uz to, ka tikai preces ar šo politiku rada krājumu transakcijas, kuras var izmantot izmaksu kontrolē, lai aprēķinātu plānotās izmaksas un noteiktu faktiskās izmaksas, kad ir pabeigts ražošanas pasūtījums.  

Lai pakalpojums tiktu ņemts vērā plānošanas un izmaksu aprēķina procesā, tas ir jāpievieno MK. MK rindas veidam ir jābūt **Kreditors**, un tā ir jāpiešķir tai maršruta operācijai, kurai ir piešķirts pakalpojums. Šai maršruta operācijai ir jābūt izmaksu aprēķināšanas resursam un resursu pieprasījumam, kas norāda uz veida **Kreditors** resursu, kurš saista operāciju un saistīto pakalpojumu ar atbilstošo kreditora kontu.  

Ja tiek izmantota šāda konfigurācija, saistītajai pakalpojuma precei tiek izveidots pirkšanas pakalpojums, pamatojoties uz ražošanas pasūtījuma novērtējumu. Pakalpojuma pirkšanas pasūtījums tiek izmantots kā apakšuzņēmēja operācijas enkurs. Apakšuzņēmēja darbu var pārvaldīt, izmantojot saraksta lapu **Apakšuzņēmēja darbs** sadaļā Ražošanas vadība. Apakšuzņēmēja darbs tiek izmantots, lai nosūtītu izejmateriālus un beidzot arī daļēji pabeigtās preces kreditoram, tādējādi sagatavojoties operācijas veikšanai. Tas tiek arī izmantots, lai saņemtu apakšuzņēmēja operācijas rezultāta preci krājumu saņemšanas laikā, kad daļēji pabeigtās preces saņemšana tiek atainota, izmantojot pakalpojuma preci. Kad tiek saņemta pirkšanas pasūtījuma rinda, ražošanas operācijas statuss tiek mainīts uz Pabeigts.  

Ražošanas pasūtījumam var būt daudz operāciju, un katra operācija var būt piešķirta atšķirīgam kreditoram. Tāpēc pilnīgs ražošanas pasūtījums var aktivizēt vairākus pirkšanas pasūtījumus.

## <a name="subcontracting-of-production-flow-activities"></a>Ražošanas plūsmas aktivitāšu apakšlīgumu slēgšana
Risinājums [lean manufacturing](lean-manufacturing-overview.md)modelē apakšuzņēmēja darbu kā pakalpojumu, kas ir saistīts ar [ražošanas plūsmas](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (uzdevuma ceļveža tēma) aktivitāti. Tāpēc šī veida apakšlīgumu slēgšana tiek saukta arī par [no aktivitātēm atkarīgu apakšlīguma slēgšanu.](activity-based-subcontracting.md) Ir ieviests īpašs izmaksu grupas veids **Tiešie ārpakalpojumi**, un apakšuzņēmēju pakalpojumi nav ietverti gatavo preču MK. Ja lietojat metodi lean manufacturing, visas aktivitātes tiek definētas, izmantojot Kanban, kas var būt saistīts ar vienu vai vairākām ražošanas plūsmas aktivitātēm. Pagaidām šis skaidrojums līdzinās ražošanas pasūtījumu skaidrojumam. Taču atšķirībā no ražošanas pasūtījumiem, kurus pabeidzot, vienmēr ir jāiegūst gatava prece, varat izveidot Kanban, lai piegādātu daļēji pabeigtu preci. Nav nepieciešams ieviest jaunu preci un MK līmeni.  

Kanban nosacījumi var būt ļoti dinamiski, tāpēc varat modelēt dažādus vienas preces piegādes variantus ražošanas plūsmā. Ja lietojat racionalizēto apakšlīgumu slēgšanu, materiālu plūsma un finanšu plūsma ir stingri atdalītas. Visu materiālu plūsma ir atainota, izmantojot Kanban aktivitātes. Pakalpojumu preču pirkšanas pasūtījumu un šo pakalpojumu ieejas plūsmu grāmatošanu var automatizēt, pamatojoties uz Kanban darbu statusu ražošanas plūsmā. Kanban darbus var sākt un pabeigt pat pirms pirkšanas pasūtījumu izveides. Apakšlīgumu slēgšanas dokumentus (pakalpojuma pirkšanas pasūtījumu un pirkšanas ieejas plūsmas dokumentu) var apkopot pēc perioda un pakalpojuma. Tādējādi var samazināt pirkšanas dokumentu un rindu skaitu pat ļoti bieži atkārtotu operāciju gadījumā, kad kreditori nodrošina apakšuzņēmēju pakalpojumus viengabala plūsmā.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Ražošanas plūsmas apakšlīgumu slēgšanas modelēšana

[Racionālās ražošanas plūsmas](lean-manufacturing-modeling-lean-organization.md) ietvaros procesa aktivitāti var definēt kā apakšuzņēmēja aktivitāti, ja tā ir piešķirta darba šūnai (resursu grupai), kam ir viens kreditora resurss. Kad ir noslēgts apakšlīgums par darba šūnu, saistītās procesa aktivitātes ir jāsaista ar aktīvu pirkšanas pasūtījuma rindu, kurā ir ietverts pakalpojuma krājums un pakalpojuma cena. Aktivitātes pakalpojuma līgums nosaka arī aprēķina attiecību starp Kanban darba preces daudzumu un rezultāta pakalpojuma daudzumu. Varat izvēlēties, vai pakalpojuma daudzums tiek aprēķināts, pamatojoties uz darbu skaitu, darbiem norādīto derīgo preču daudzumu vai kopējo preču daudzumu (šajā kopējā daudzumā ir ietvertas brāķētās preces).  

Arī pārsūtīšanas aktivitātes var definēt kā apakšuzņēmēja aktivitātes. Šī definēšana tiek veikta netiešā veidā, kad atlasāt par nosūtīšanu atbildīgo pusi pārsūtīšanas aktivitātes ietvaros. Ja atlasāt opciju **Kravas nosūtītājs** vai **Saņēmējs** un attiecīgā avota vai mērķa noliktava ir kreditora pārvaldīta noliktava, aktivitāte tiek uzskatīta par apakšuzņēmēja aktivitāti. Ja atlasāt opciju **Pārvadātājs**, aktivitāte vienmēr ir apakšuzņēmēja aktivitāte. Tāpat kā apakšuzņēmēja procesa aktivitātes, arī apakšuzņēmēja pārsūtīšanas aktivitāte ir jāsavieno ar pakalpojuma līgumu, pirms var aktivizēt ražošanas plūsmu.

### <a name="backflush-costing"></a>Atgriezeniska izmaksu aprēķināšana

Apakšuzņēmēja darba izmaksu uzskaite ir pilnībā integrēta risinājuma lean manufacturing izmaksu aprēķinā (atgriezeniska izmaksu aprēķināšana) Kad tiek grāmatota pirkšanas pakalpojuma ieejas plūsma vai tiek izrakstīts rēķins, pakalpojuma izmaksas tiek piešķirtas ražošanas plūsmai. Atgriezeniskās izmaksu aprēķināšanas ietvaros tiek aprēķināta apakšuzņēmēja pakalpojumu novirze, atņemot saņemto preču standarta izmaksu apakšlīguma bloku no faktiskā saņemtā un rēķinos ietvertā pakalpojuma daudzuma.

## <a name="material-supply-for-subcontracted-operations"></a>Materiālu piegāde apakšuzņēmēja operācijām
Daļēji pabeigtās preces un citi saistītie materiāli ir jāpārsūta uz atrašanās vietu, kur tiek fiziski veikts darbs. Ja lietojat apakšuzņēmēja operācijas un aktivitātes, šī pārsūtīšana bieži ir saistīta ar papildu transportēšanu uz kreditora pārvaldītu vietu. Piešķirot apakšuzņēmēja operācijai MK ietvertu materiālu, jūs norādāt, ka materiālam ir jābūt pieejamam piešķirtajam resursam atbilstošās grupas ievades atrašanās vietā. Šādā gadījumā materiāls tiek nodrošināts šajā atrašanās vietā, izmantojot vispārējo plānošanu vai racionālo papildināšanu.  

Lai modelētu kreditora atrašanās vietā esošos krājumus, nozares labākā prakse ir definēt kreditora pārvaldītu noliktavu. Varat viegli definēt kreditora pārvaldītu noliktavu, izveidojot jaunu noliktavu un piešķirot kreditora kontu. Lai dokumentētu to, ka materiāls ir jāpārsūta kreditoram, pirms var veikt operāciju, kreditora pārvaldītā noliktava ir jāpiešķir resursam atbilstošās resursu grupas ievades noliktavai.  

Lai papildinātu materiālus šajā noliktavā, varat izmantot dažādas stratēģijas.

-   Pārsūtīšanas pasūtījumi
-   Pārsūtījumu žurnāli
-   Ieturēšanas Kanban
-   Tieša pirkšana ar piegādi kreditora atrašanās vietā

Šis noteikums neattiecas uz daļēji pabeigtajām precēm. Lai pārsūtītu daļēji pabeigtās preces, varat izmantot tikai tālāk norādītās iespējas.

-   Ja tiek apstrādāts ražošanas vai partijas pasūtījums, daļēji pabeigtās preces var pārsūtīt tikai loģiskā veidā, izmantojot izdošanas saraksta žurnāla veidlapu, kas ir pieejama saraksta lapā **Apakšuzņēmēja darbs**. Izmamtojot šo žurnālu, tiek izveidots piegādes pavadzīmes dokuments, ko var izmantot, lai pārsūtītu kreditoram daļēji pabeigtās preces un izejmateriālus.
-   Ražošanas plūsmu apakšuzņēmēja operāciju ietvaros daļēji pabeigto preču pārsūtīšana tiek dokumentēta, saņemot atvilkumu vai ražošanas Kanban kreditora atrašanās vietā. Lai modelētu tiešu pārsūtīšanas aktivitāti, varat pabeigt ražošanas Kanban ar papildu pārsūtīšanas aktivitāti.

**Piezīme.** Viena ražošanas pasūtījuma ražošanas maršruts nedrīkst ietvert vairākas vietas. Šis noteikums attiecas arī uz apakšuzņēmēja darbu. Tāpēc kreditora pārvaldītām materiālu atrašanās vietām atbilstošās noliktavas ir jādefinē tajā pašā vietā, kur ir definēti maršrutā izmantotie iekšējie resursi. Lai gan ražošanas plūsmas var ietvert vairākas vietas, to ietvaros daļēji pabeigtās preces nevar transportēt no vienas vietas uz citu, jo šī operācija ir saistīta ar izmaksu konteksta izmaiņām.  

Parasti apakšuzņēmēja resursu grupas atrašanās vieta un izvades noliktava tiek tieši piešķirtas atrašanās vietai un noliktavai, kas tiek izmantotas nākamajā maršruta vai ražošanas plūsmas posmā. Šāda iestatīšana palīdz samazināt izveidojamo darba pārskatu skaitu vai modelējamo papildu pārsūtīšanas operāciju skaitu.




