---
title: "Pārvaldītu apakšuzņēmuma darbu ražošanā"
description: "Šajā tēmā ir paskaidrots, kā apakšuzņēmēju darbības Microsoft Dynamics 365 operācijām, kuras tiek pārvaldītas. Citiem vārdiem sakot, tas izskaidro, kā kreditoru pārvalda ražošanas operācijas, kas ir piešķirti resursi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Pārvaldītu apakšuzņēmuma darbu ražošanā

Šajā tēmā ir paskaidrots, kā apakšuzņēmēju darbības Microsoft Dynamics 365 operācijām, kuras tiek pārvaldītas. Citiem vārdiem sakot, tas izskaidro, kā kreditoru pārvalda ražošanas operācijas, kas ir piešķirti resursi.

Šajā [ražošanas procesu](production-process-overview.md), darbu var veikt no līdzekļiem, kas ir īpašumā vai pārvalda kreditori. Parasti tiek izmantoti kreditoru resursu līmeņa periodiska lieko pieprasījums, kas pārsniedz pieejamo ražīgumu uzņēmuma pašu resursi. Piegādātāju, iespējams, var arī piedāvāt īpašu [resursu iespējas](resource-capabilities.md)vai resursus par zemāku cenu.  

Atkarībā no kreditoru līdzekļiem, ko izmanto ražošanas procesā, [maršruta](routes-operations.md) bieži ir papildu loģistikas prasībām, jo materiālu un pusfabrikātu vispirms jātransportē uz ražotāja vietā. Pēc tam apakšlīgumā paredzētās darbības rezultātiem jāpārvadā vai nu vietā, kas ir piešķirtas līdz nākamajai operācijai vai gatavās produkcijas noliktava.  

Ja izmanto apakšuzņēmuma darbībām vai darbībām, tās ietekmē ikvienā darbības, no darbībām, kas nepieciešamas ražošanai, pašizmaksas, prognozēšana, plānošanā un plānošanu, materiālu, pusfabrikātu un gatavās produkcijas loģistikas pārvaldībā, definīcijas. Visbeidzot, šos resursus pieprasīt savus procesus, uzskaites un izmaksu kontroli.  

Iekšējo resursu fiksēto izmaksu kursu parasti tiek piešķirts uz laiku. Turpretī apakšlīgumā paredzētās resursu izmaksas balstās uz saistīto pakalpojumu iepirkuma cenas. Pakalpojums tiek definēta kā citu produktu, un tiek izmantots, lai vadīt iepirkumu un iepirkuma procesu noteiktu apakšuzņēmuma līguma darbību.  

Pašlaik nav nekādu skaidru koncepciju pusapstrādātu produktu Microsoft Dynamics 365 operācijām. Ražošanas pasūtījumam, kas prasa vairāk nekā vienu darbību, lai pārveidotu izejvielām gatavo laba, pabeigta prece tiek grāmatota atpakaļ noliktavā tikai pēdējā darbībā. Pusfabrikātiem, kas veido agrāko darbību ir jāatskaitās Nepabeigtie projekti (RNR), bet tie nav iegrāmatoti vai reģistrētās noliktavās. Kaut arī maršrutus un materiālu komplektus (MK) var sadalīt vairākās mazākās vienībās, šāda pieeja palielina skaitu produktu, MK un maršrutus, kas ir jāvada.  

Pastāv divas metodes modelēšana apakšuzņēmuma darbu ražošanas operācijām. Šīm metodēm atšķiras tādā veidā, ka apakšlīguma process var modelēt, tā, ka pusfabrikātu ir pārstāvētas šajā procesā, un tiek pārvaldīti tā, ka izmaksu kontrole.

-   Maršruta darbības ražošanas pasūtījumiem vai pasūtījumus paketes apakšuzņēmuma
    -   Pakalpojums produktam ir jābūt uzkrāti produktu, un tai ir jābūt daļai no IMS.
    -   Šī metode atbalsta pirmais iekšā, pirmais ārā (FIFO) vai standarta izmaksām.
    -   Pusfabrikāti tiek attēloti kā pakalpojuma produkta process.
    -   Izmaksu kontroli sadala izmaksas, kas saistītas ar apakšuzņēmēju darba materiālu izmaksas.
-   Apakšuzņēmuma līgumu slēgšana ražošanas plūsmas darbību liesās ražošanas plūsmu
    -   Pakalpojums ir pakalpojums nav uzkrāti produkts, un tas nav daļa no IMS.
    -   Šī metode izmanto pirkšanas līgumus par pakalpojumu līgumiem.
    -   Šo metodi izmanto backflush maksā.
    -   Šī metode ļauj apkopoto un asinhronā iepirkumu. (Materiāla plūsmu ir neatkarīga no iepirkuma procesā).
    -   Izmaksu kontroli piešķir apakšuzņēmēju darbu savu izmaksu sadalījums blokā.

## <a name="subcontracting-of-route-operations"></a>Apakšuzņēmuma līgumu slēgšana par maršruta operācijas
Izmantot, apakšlīgumu slēgšanu par maršruta operācijas ražošanai vai partijas rīkojumus, pakalpojumu produkts, kas izmanto pakalpojumu iepirkumam jābūt definētam kā produkts **pakalpojumu** tips. Turklāt tai jābūt krājumu modeļa grupu, ko ir **Stocked produkta** opciju zem **krājuma politikas** iestatīts **Jā**. Šī opcija nosaka, vai produkts uzskaita kā krājumus pēc produkta saņemšanas (**Stocked produkta** = **Jā**), vai, vai produkta ieraksta peļņas un zaudējumu kontos (**Stocked produkta** = **Nr**). Kaut arī šāda uzvedība var šķist pretrunīgi, ir balstīta uz faktu, ka tikai produktiem, kas ir šī politika radīs krājumu darbības, kas var tikt izmantoti izmaksu kontroli, lai aprēķinātu plānoto izmaksu un noteikt faktisko pašizmaksu, kad ražošanas pasūtījums ir.  

Jāņem vērā, plānojot un izmaksu aprēķinu, pakalpojums ir jāpievieno MK. MK rindā jābūt **kreditoru** tipa, un tas jāpiešķir maršruta operācijas, kas piešķirts pakalpojums. Operācija maršrutā jābūt pašizmaksas resursu un resursu vajadzību, kas norāda uz resursu **kreditoru** veids, kas savieno operācijas un saistīto pakalpojumu atbilstošā piegādātāja kontā.  

Izmantojot šo konfigurāciju, pirkšanas pasūtījumu izveido saistīto pakalpojumu produktam, pamatojoties uz ražošanas pasūtījuma novērtējumu. Pirkšanas pasūtījuma pakalpojumu izmanto kā enkurs apakšlīgumā paredzētās darbības. Apakšuzņēmēju darbs, kas jāpārvalda ar **apakšlīgumu darbu** saraksta lapu ražošanas kontroli. Apakšuzņēmēju darbs tiek izmantots, lai kuģis izejvielas un visbeidzot pusfabrikāts kreditoram gatavojoties operācijai. To izmanto arī, lai saņemtu iegūtais produkts apakšlīgumā paredzētās darbības krājumu saņemšanas, kur produkts pakalpojums tiek izmantots, lai identificētu pusfabrikātiem ierašanos. Saņemot pirkuma pasūtījuma rinda, ražošanas operācija tiek atjaunināta kā pabeigtu.  

Ražošanas pasūtījumā var būt daudz darbības un katrai operācijai var piešķirt piegādātājam. Tādēļ, izbeigt end ražošanas pasūtījumam var izraisīt vairākus pirkšanas pasūtījumus.

## <a name="subcontracting-of-production-flow-activities"></a>Apakšuzņēmuma līgumu slēgšana ražošanas plūsmas darbības
[Liesās ražošanas](lean-manufacturing-overview.md)risinājuma modeļus apakšuzņēmuma darbu kā pakalpojums, kas saistīts ar darbību [ražošanas plūsmu](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (uzdevuma rokasgrāmata tēmu). Tādēļ šāda veida apakšuzņēmuma līgumus dēvē arī par [darbībās balstīta apakšlīgumu slēgšanu.](activity-based-subcontracting.md) Īpašu izmaksu grupas tips **tiešu ārpakalpojumu**, ir ieviesta un apakšlīguma pakalpojumi nav daļa no gatavās preces IMS. Lietojot liesās ražošana, visu darbību nosaka kanbans, kas var būt saistīti ar vienu vai vairākas ražošanas plūsmas darbībām. Tik tālu, ka skaidrojums izklausās tāpat kā paskaidrojums par ražošanas pasūtījumiem. Tomēr tā kā ražošanas pasūtījumu vienmēr ir jābeidzas ar galaproduktu, var izveidot kanbans piegādāt pusfabrikāts. Jums nav jāievieš jauns produkts un MK līmenī.  

Jo kanban normas var būt ļoti dinamisks, varam modelis dažādi varianti par vienu un to pašu produktu piegādes uz ražošanas plūsmu. Lietojot liesās apakšuzņēmuma līgumus, audumam slīdēt un finanšu plūsma tiek stingri atdalīti. Visu materiālu plūsmas attēlo kanban aktivitātēm. Pirkšanas pasūtījumus, minēto pakalpojumu saņemšanas grāmatojumus un pakalpojumu produktiem, var tikt automatizētas, pamatojoties uz kanban darbu ražošanas plūsmu statusu. Kanban darbus var sākta un pabeigta vēl pirms pirkšanas pasūtījums netiek izveidots. Apakšlīguma dokumenti (pirkšanas pasūtījums un pirkšanas saņemšanas dienesta) var apkopot noteiktā laika posmā un pakalpojumu. Tāpēc iepirkuma dokumentos un rindu skaits var tur maza, pat augsti atkārtotām operācijām, kur pārdevēji Monolītā plūsmas apakšuzņēmēju pakalpojumu sniegšanas.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Apakšlīgumu slēgšana ražošanas plūsmas modelēšana

Šajā [liesās ražošanas plūsmu](lean-manufacturing-modeling-lean-organization.md), procesu darbības var definēt kā slēgts apakšlīgums, piešķirot darba šūnai (resursu grupa), kas ir atsevišķu kreditora resurss. Kad darba šūna ir slēgts apakšlīgums, saistīto procesu darbības ir jāsaista ar aktīvu pirkuma līguma rindu, kas satur apkalpojamās preces un pakalpojuma cena. Pakalpojuma līguma darbības definē arī aprēķina attiecību starp kanban darba produkta daudzumu un rezultātā pakalpojumu daudzums. Var izvēlēties, vai pakalpojumu daudzums tiek aprēķināts, pamatojoties uz darbiem, laba produkta daudzums, kas tiek ziņots par darba vai kopējo saražoto daudzumu (Šis kopējais daudzums ietver Norakstīto līdzekļu) skaits.  

Pārvietošanas darbības var definēt arī kā apakšlīgumu. Šī definīcija netieši rodas atbildīgo personu par kuģniecības atlasot pārsūtīšanas darbība. Ja atlasāt **nosūtītājs** vai **adresātu**, ja atbilstošā avota vai mērķa noliktavā ir piegādātāja pārvaldīti noliktava, darbība tiek uzskatīta par apakšlīgumu. Ja atlasāt **Carrier**, aktivitātes vienmēr ir noslēgti apakšlīgumi. Apakšuzņēmuma līguma procesu darbības, piemēram, nodošana apakšlīgumā paredzētās aktivitātes ir jāsavieno ar pakalpojuma līgums pirms ražošanas plūsmu var aktivizēt.

### <a name="backflush-costing"></a>Atgriezeniska izmaksu aprēķināšana

Apakšuzņēmēju darbu izmaksu novērtējumā pilnībā integrēta maksā liesās ražošanas risinājumu (backflush maksā). Grāmatojot pirkšanas pasūtījumu saņemšanas dienesta vai rēķinu rodoties, pakalpojumu izmaksām tiek piešķirta ražošanas plūsmu. Backflush maksā, apakšuzņēmēju pakalpojumus dispersiju aprēķina, kompensējot apakšuzņēmuma bloka standarta izmaksu saņemto produktu daudzumiem, kas faktiski saņemts un rēķinā iekļauts pakalpojums pret.

## <a name="material-supply-for-subcontracted-operations"></a>Materiālu piegādes apakšuzņēmēju darbībām
Pusfabrikātu un citi saistīti materiāli jāpārvieto uz vietu, kur darbs tiek veikts fiziski. Izmantojot apakšuzņēmuma līguma darbību un darbību, šī nodošana bieži saistītas ar papildu transporta kreditora darbināmu vietā. Sadalot materiāla MK apakšuzņēmuma līguma darbību, jums paziņot, ka materiāls ir posmveidīgu ievades resursa grupai piešķirtais resurss vietā. Vispārējā (grafika) plānošanā vai tad liesās papildināšanas noteikumi materiālu šai vietai.  

Lai modelētu krājumu, kas atrodas kreditora vietā, tas ir labāko praksi nozarē, lai noteiktu piegādātāju pārvalda noliktavas. Viegli var definēt piegādātāja pārvaldīti noliktavas, izveidojot jaunu noliktavu un piešķirot kreditora kontā. Lai dokumentētu šo materiālu ir jāpārsūta kreditoram pirms operācijas var veikt, jums vajadzētu piešķirt piegādātājam pārvaldīt noliktavu ievades noliktavā esošās resursu grupas, kas ietver šo resursu.  

Papildināt materiālu šajā noliktavā, var izmantot vairākas stratēģijas:

-   Pārsūtīšanas pasūtījumi
-   Pārsūtījumu žurnāli
-   Atsaukšanu, kanbans
-   Tiešo pirkumu pārdevēja atrašanās vietu

Pusfabrikātu ir izņēmums no šī noteikuma. Lai pārsūtītu pusfabrikātiem, jūs tikai šīs opcijas:

-   Ražošanai un partijas rīkojumus, ar pusfabrikātu var pārsūtīt tikai loģiski, izmantojot izdošanas saraksta žurnālu, no **apakšlīgumu darbu** saraksta lapu. Šo žurnālu radīs pavadzīmei dokumentu, ko var izmantot, lai pārsūtītu pusfabrikātiem un izejvielu piegādātājam.
-   Apakšuzņēmuma līguma operācijām ražošanas plūsmām, pusfabrikātu nodošanu tiek dokumentēts ar saņemšanas atsaukšanu vai ražošanas kanbans pārdevēja atrašanās vietā. Lai modelētu tiešas nodošanas darbību, var beigt ražošanas kanban ar papildu pārvietošanas darbību.

**Piezīme:** ražošanas maršrutā vienu ražošanas pasūtījumam nevar šķērsot vairākas vietnes. Šis noteikums attiecas arī uz apakšuzņēmēju darbu. Tādēļ, noliktavām, kas attēlo piegādātāja pārvaldīti materiāls, vietām jābūt definētam tajā pašā vietnē, kur iekšējos resursus, kas tiek izmantotas šajā maršrutā. Gan ražošanas plūsmas var šķērsot vietās, viņi nevar transporta pusfabrikāti no vienas vietas uz citu, jo šī operācija nozīmē izmaiņas izmaksas saistībā.  

Parasti, produkcijas noliktavu un apakšuzņēmēju resursu grupu atrašanās vieta tieši attiecina uz noliktavu un nākamais solis operācijas maršrutu vai ražošanas plūsmas vietā. Šis iestatījums palīdz samazināt apjomu ziņošanu, kas rodas darba vai numuru papildu pārvietošanas operāciju, kas ir modelēts.


