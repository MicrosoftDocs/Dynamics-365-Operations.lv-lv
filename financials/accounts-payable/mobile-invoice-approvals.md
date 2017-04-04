---
title: "Mobilais rēķinu apstiprinājumu"
description: "Mobilo sakaru iespējas Microsoft Dynamics 365 operācijām ļauj biznesa lietotājiem izstrādāt mobilo pieredzi. Par papildu scenārijus, platformas arī pieņemsim izstrādātājiem paplašina iespējas, kā viņi vēlas. Visefektīvākais veids, kā iemācīties dažas jaunas koncepcijas mobilajā telefonā ir iet caur procesu projektēšana dažus scenārijus. Šajā tēmā ir paredzēts, lai sniegtu praktisku pieeju projektēšana mobilās scenārijus, piedaloties kreditoru rēķinu apstiprinājumu mobilajiem tālruņiem, kā izmantošanas gadījumā. Šīs tēmas palīdzēs jums noformēt citus variantus scenāriji un var lietot arī citi gadījumi, kas nav saistītas ar piegādātāju rēķiniem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobilais rēķinu apstiprinājumu

Mobilo sakaru iespējas Microsoft Dynamics 365 operācijām ļauj biznesa lietotājiem izstrādāt mobilo pieredzi. Par papildu scenārijus, platformas arī pieņemsim izstrādātājiem paplašina iespējas, kā viņi vēlas. Visefektīvākais veids, kā iemācīties dažas jaunas koncepcijas mobilajā telefonā ir iet caur procesu projektēšana dažus scenārijus. Šajā tēmā ir paredzēts, lai sniegtu praktisku pieeju projektēšana mobilās scenārijus, piedaloties kreditoru rēķinu apstiprinājumu mobilajiem tālruņiem, kā izmantošanas gadījumā. Šīs tēmas palīdzēs jums noformēt citus variantus scenāriji un var lietot arī citi gadījumi, kas nav saistītas ar piegādātāju rēķiniem.

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnoteikumi                                                                                            | apraksts                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobilais rokasgrāmata iepriekš lasīt                                                                                |(/ dynamics365/darbības/dev-itpro/mobilais-apps / mobile-platform.md)                                                                                                  |
| Dinamika 365 operācijām                                                                             | Vidi, kas ir Microsoft Dynamics 365 darbību versija 1611 un Microsoft Dynamics darbības platformu update 3 (2016. gada novembrī)                   |
| Instalējiet labojumfailu KB 3204341.                                                                              | Uzdevuma rakstītāju kļūdaini ieraksta divus tuvu komandas nolaižamajā dialogus, tas ir iekļauts Dynamics 365 darbības platformu Update 3 (November 2016 atjauninājums) |
| Instalējiet labojumfailu KB 3207800.                                                                              | Šis labojumfails ļauj pielikumus, apskatīt mobilās klientu, tas ir iekļauts Dynamics 365 darbības platformu Update 3 (November 2016 atjauninājums).           |
| Instalējiet labojumfailu KB 3208224.                                                                              | Programmas kods mobilo kreditora rēķina apstiprinājuma pieteikumu, tas ir iekļauts Microsoft Dynamics AX lietojumprogrammu 7.0.1 (maija 2016).                          |
| Android vai ISP vai Windows ierīces, kas ir mobilo app uzstādīta Dynamics 365 operācijām | Meklētu app atbilstošu app Store.                                                                                                                     |

## <a name="introduction"></a>Ievads
Mobilo apstiprinājumus kreditoru rēķinu pieprasa trīs labojumfaili, kas ir minēti sadaļā "Priekšnoteikumi". Šos labojumfailus nesniedz darbvietu rēķinu apstiprinājumu. Lai uzzinātu, kas darbvietu saistībā ar mobilo, nolasa mobilo rokasgrāmatu, kas ir minēti sadaļā "Priekšnoteikumi". Rēķinu apstiprinājumu darbvieta ir jāplāno. 

Katrai organizācijai nenovēršami un atšķirīgi definē tās biznesa procesu par kreditora rēķiniem. Pirms noformējat mobilo pieredzi kreditora rēķinu apstiprinājumu, jums vajadzētu apsvērt šādus biznesa procesa aspektiem. Ideja ir, lai izmantotu šos datu punktiem, cik vien iespējams optimizēt lietotāja pieredzi ierīcē.

-   Kādus laukus no rēķina virsrakstā lietotājs vēlēsies redzēt mobilo pieredzi, un kādā secībā?
-   Kādus laukus no rēķina rindām lietotājs vēlēsies redzēt mobilo pieredzi, un kādā secībā?
-   Cik daudz rēķina rindās ir rēķins? 80-20 noteikums attiecas, un optimizēt par 80 procentiem.
-   Lietotāji vēlēsies redzēt uzskaites sadali (rēķina kodēšana) mobilajā ierīcē laikā atsauksmes Ja atbilde uz šo jautājumu ir "Jā", apsveriet šādus jautājumus:
    -   Cik daudz uzskaites sadali (paplašinātā cena, PVN, maksa, plaisām un tā tālāk) ir rēķina rindai? Atkal, piemēro 80-20 noteikums.
    -   Vai rēķinos ir arī uzskaites sadales rēķina virsrakstā? Tādā gadījumā šīs uzskaites sadali būtu pieejamas ierīcē?

> [!NOTE]
> Šajā tēmā neizskaidro kā rediģēt uzskaites sadali, jo šī funkcija pašlaik nav atbalstīts mobilo scenārijiem.

-   Lietotāji vēlēsies redzēt pielikumus rēķina ierīcē

Rēķinu apstiprinājumu mobilajai pieredzei dizains atšķirsies atkarībā no atbildēm uz šiem jautājumiem. Mērķis ir optimizēt lietotāja pieredzi biznesa procesa organizācijā mobilajā telefonā. Pārējā šo tēmu, mēs apskatīsim divu scenāriju variācijas, kas pamatā ir dažādas atbildes uz šiem jautājumiem. 

Kā vispārēji norādījumi, strādājot ar mobilo dizainers, pārliecinieties, vai publicēt izmaiņas, lai novērstu zaudē atjauninājumus.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Vienkāršs rēķins apstiprinājuma scenārijs projektēšana Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenārija atribūts</th>
<th>Atbilde</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kādus laukus no rēķina virsrakstā lietotājs vēlēsies redzēt mobilo pieredzi, un kādā secībā?</td>
<td><ol>
<li>Kreditora nosaukums</li>
<li>Rēķina kopsumma</li>
<li>Rēķina konts</li>
<li>Rēķina numurs</li>
<li>Rēķina datums</li>
<li>Rēķina apraksts</li>
<li>Izpildes termiņš</li>
<li>Rēķina valūta</li>
</ol></td>
</tr>
<tr class="even">
<td>Kādus laukus no rēķina rindām lietotājs vēlēsies redzēt mobilo pieredzi, un kādā secībā?</td>
<td><ol>
<li>Sagādes kategorija</li>
<li>Daudzums</li>
<li>Vienības cena</li>
<li>Rindas neto summa</li>
<li>1099. summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Cik daudz rēķina rindās ir rēķins? 80-20 noteikums attiecas, un optimizēt par 80 procentiem.</td>
<td>1.</td>
</tr>
<tr class="even">
<td>Lietotāji vēlēsies redzēt uzskaites sadali (rēķina kodēšana) mobilajā ierīcē laikā atsauksmes</td>
<td>Jā</td>
</tr>
<tr class="odd">
<td>Cik daudz uzskaites sadali (paplašinātā cena, PVN, maksa utt.) pastāv rēķina rindai? Atkal, piemēro 80-20 noteikums.</td>
<td>Paplašinātā cena: 2 PVN: 0 izdevumi: 0</td>
</tr>
<tr class="even">
<td>Vai rēķinos ir arī uzskaites sadales rēķina virsrakstā? Tādā gadījumā šīs uzskaites sadali būtu pieejamas ierīcē?</td>
<td>Netiek lietots</td>
</tr>
<tr class="odd">
<td>Lietotāji vēlēsies redzēt pielikumus rēķina ierīcē</td>
<td>Jā</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Izveidot darbvietu

1.  Pārlūkprogrammā, atveriet Dynamics 365 operācijām un pieteikties.
2.  Pēc tam, kad esat pieteicies, pievienot **& režīmā = mobilo** kā redzams, šādu piemēru, un atsvaidzināt lapu URL: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& režīmā = mobilo**
3.  Noklikšķiniet uz **iestatījumus** (rīku) pogu augšējā labajā stūrī lapā, un pēc tam noklikšķiniet uz **mobilo app**. Mobilo app dizainers ir parādās tikai kā uzdevumu ieraksti rāda uz augšu.
4.  Noklikšķiniet uz **pievienot**, lai izveidotu jaunu darbvietu. Šajā piemērā vārds darbvietu **manu apstiprinājumu**.
5.  Ievadiet aprakstu.
6.  Atlasiet krāsu telpas. Krāsu telpas tiks izmantots stils kopumā mobilo pieredzi šai darbvietai.
7.  Atlasīt darbvietas ikona.
8.  Noklikšķiniet uz **darīts**
9.  Noklikšķiniet uz **publicēt darbvietu** saglabāt veiktās izmaiņas

### <a name="vendor-invoices-assigned-to-me"></a>Kreditora rēķini, kas piešķirti man

Rēķinu sarakstu, kas ir piešķirti lietotājam pārskatīšanai ir pirmā mobilā lapa, kas jums jāizstrādā. Noformēt šo mobilo lapā, lietojiet **VendMobileInvoiceAssignedToMeListPage** lapu Dynamics 365 operācijām. Pirms šī procedūra būs paveikta, pārliecinieties, ka ir vismaz viena kreditora rēķina tiek piešķirts jums pārskatīšanai, un rēķina rinda ir divi sadalēm. Šis iestatījums atbilst šim scenārijam.

1.  Darbības URL Dynamics 365, aizstāt ar izvēlnes elementa nosaukums **VendMobileInvoiceAssignedToMeListPage** atvērt mobilā versija **izskata kreditoru rēķinus piešķirts man** saraksta lapu **kreditoru parādi** modulis. Atkarībā no jūsu sistēmas piešķirto jums rēķinu skaits, šī lapa parādīs šos rēķinus. Lai atrastu norādīto rēķinu, var izmantot filtru kreisajā pusē. Tomēr mums neprasa īpašu rēķins šim piemēram. Mēs pieprasām tikai daži rēķina piešķirts jums, kas notiek, lai jūs varētu dizains mobilo lapā. Jaunas lapas, kas ir pieejami ir paredzēti īpaši attīstīt mobilo scenārijus attiecībā uz piegādātāja rēķina. Tāpēc ir jālieto šajās lapās. URL vajadzētu līdzināties šādu URL un pēc tam, kad to ievadāt, lapa, kas ir redzams attēlā jānorāda: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& režīmā = mobilo [![izskata kreditoru rēķinus piešķirts man lapa](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Noklikšķiniet uz **iestatījumus** (rīku) pogu augšējā labajā stūrī lapā, un pēc tam noklikšķiniet uz **Mobile app**
3.  Atlasīt darbvietas un noklikšķiniet **rediģēt**
4.  Noklikšķiniet uz **pievienot lapu** pirmo mobilo lapas izveidei.
5.  Ievadiet nosaukumu, piemēram, **manu kreditora rēķiniem**, un aprakstu, piemēram, **kreditoru rēķinus piešķirts man pārskatīšanai**.
6.  Click **Done**.
7.  Mobilo sakaru rīkā par **lauki** cilni, noklikšķiniet uz **atlasiet laukus,**. Kolonnu saraksta lapā nedrīkst līdzināties attēlā. [![Kolonnās pa gaida kreditoru rēķinus piešķirts man lapu](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Pievienojiet nepieciešamās kolonnas no saraksta lappuses, kas ir jāparāda lietotājiem mobilo lapā. Kurā jāpievieno secība ir secība, kādā lauki parādās gala lietotājam. Vienīgais veids, kā mainīt lauku secību, būs atkārtoti izvēloties visus laukus. Balstoties uz šāda scenārija prasībām, šādos astoņos laukos nepieciešami. Tomēr daži lietotāji varētu apsvērt astoņos laukos pārāk daudz informācijas ir par mobilo ierīci. Tāpēc mēs parādīsim tikai vissvarīgākie lauki mobilā saraksta skatā. Skats detaļas mēs izstrādās vēlāk parādīsies atlikušajos laukos. Tagad mēs pievienot šādus laukus. Noklikšķiniet uz plusa zīmes (**+**) šajās ailēs, lai pievienotu mobilo lapā.
    1.  Kreditora nosaukums
    2.  Rēķina kopsumma
    3.  Rēķina konts
    4.  Rēķina numurs
    5.  Rēķina datums

    Pēc lauku pievienošanas mobilo lapā nedrīkst līdzināties attēlā. [![Pēc lauku pievienošanas lapā](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Jums jāpievieno arī šādas kolonnas tagad, tāpēc, ka mēs vēlāk var iespējot darbplūsmas darbības.
    1.  Parāda uzdevuma izpildei
    2.  Deleģēt uzdevumu parādīt
    3.  Parāda uzdevuma atsaukšana
    4.  Rādīt noraidītu uzdevuma
    5.  Parādīt uzdevumu pieprasījumu Pabeigšana
    6.  Parādīt uzdevumu atkārtoti

10. Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
11. Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
12. Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu.
13. Iespējot **parādiet rēķinu par kopējo izskata kreditoru rēķinu sarakstu** kontus kreditoru parametrus formā zem **rēķina**. Ņemiet vērā, ka tikai šis parametrs, ļaujot rēķina kopsummas tiks aprēķināts jārāda lapā gaida kreditoru rēķinu sarakstu. Šis ir jaunu iespēju, kas ir daļa no iepriekš nepieciešamo karstā noteikt 3208224.

### <a name="vendor-invoice-details"></a>Kreditora rēķina detaļas

Lai noformētu rēķina informācijas lapā Mobile, izmantojiet **VendMobileInvoiceHeaderDetails** lapu Dynamics 365 operācijām. Piezīme Atkarībā no tā, cik rēķini, ka jums ir jūsu sistēmā, šī lapa rāda vecākajām rēķina (pavadzīme, kas tika izveidots pirmais). Lai atrastu norādīto rēķinu, var izmantot filtru kreisajā pusē. Tomēr mums neprasa īpašu rēķins šim piemēram. Mēs tikai nepieciešama rēķinu datus tā, ka mēs varam dizains mobilo lapā. [![Lapā Darbplūsmas](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Darbības URL Dynamics 365, aizstāt ar izvēlnes elementa nosaukums **VendMobileInvoiceHeaderDetails**, lai atvērtu formu
2.  Atveriet mobilā dizainers no **iestatījumus** (rīku) pogu.
3.  Noklikšķiniet uz **rediģēt** pogu, lai sāktu rediģēšanas režīmā darbvietā.
4.  Izvēlieties * * mans kreditoru rēķinus * *, kuru izveidojāt iepriekšējās lappuses un pēc tam noklikšķiniet uz **rediģēt**.
5.  Par **lauki** cilni, noklikšķiniet uz **Grid** kolonnas virsraksta.
6.  Noklikšķiniet uz **Properties**&gt;**pievienot lapu**. **Piezīme:** noklikšķinot uz **Grid** pozīcijā un pievienot lapu, attiecības ar detaļu lappuse tiek izveidots automātiski.
7.  Ievadiet lapas nosaukumu, piemēram, **rēķina detaļas**, un aprakstu, piemēram, **skatiet rēķina virsrakstu un rindas detaļu**.
8.  Noklikšķiniet uz **atlasiet laukus,**. Ievērojiet, ka jūs pievienot secība ir secība, kādā lauki parādās gala lietotājam. Vienīgais veids, kā mainīt lauku secību, būs atkārtoti izvēloties visus laukus.
9.  No virsraksta, balstoties uz šāda scenārija prasībām pievienot šādus laukus:
    1.  Kreditora nosaukums
    2.  Rēķina kopsumma
    3.  Rēķina konts
    4.  Rēķina numurs
    5.  Rēķina datums
    6.  Rēķina apraksts
    7.  Izpildes termiņš
    8.  Rēķina valūta

10. No režģa līnijām, lappusē pievienot šādus laukus:
    1.  Sagādes kategorija
    2.  Daudzums
    3.  Vienības cena
    4.  Rindas neto summa
    5.  1099. summa

11. Kad ir pievienoti visi lauki no iepriekšējos divus soļus, noklikšķiniet uz **darīts**. Lapa ir līdzināties attēlā. [![Pēc lauku pievienošanas lapā](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
13. Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
14. Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu

### <a name="workflow-actions"></a>Darbplūsmas darbības

Lai pievienotu darbplūsmas darbības, lietojiet **VendMobileInvoiceHeaderDetails** lapu Dynamics 365 operācijām. Atvērt šo lapu, aizstāt izvēlnes elementa vietrādi URL nosaukums, kā to darījāt agrāk. Pēc tam atveriet mobilā dizainers no **iestatījumus** (rīku) pogu. Izpildiet šīs darbības, lai pievienotu darbplūsmu darbības informācijas lapā.

1.  Noklikšķiniet uz **rediģēt** pogu, lai sāktu rediģēšanas režīmā darbvietā.
2.  Atlasiet **rēķina detaļas**, kuru izveidojāt iepriekšējās lappuses un pēc tam noklikšķiniet uz **rediģēt**.
3.  Par **darbības** cilni, noklikšķiniet uz **pievienot darbību**.
4.  Ievadiet darbības nosaukumu, piemēram, **apstiprināt**, un aprakstu, piemēram, **apstiprināt rēķina**. Ievērojiet, ka darbības nosaukums, kuru ievadāt šeit kļūst darbības nosaukumu, kas tiek rādīta lietotājam mobilo app.
5.  Click **Done**.
6.  Noklikšķiniet uz **atlasiet laukus,**.
7.  Iet caur darbplūsmas procesa **VendMobileInvoiceHeaderDetails** lapu un pabeigtu darbību, ko vēlaties ierakstīt. Pārliecinieties, vai ierakstāt darbplūsmas komentārus šajā procesā tā, lai komentāri jomā ir iekļauta arī mobilo pieredzi.
8.  Pēc tam, kad palaist darbplūsmas darbību, noklikšķiniet uz **darīts** izvēlieties laukus uzdevuma pabeigšanai.
9.  Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
10. Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
11. Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu
12. Atkārtojiet soļus no 3. līdz 11 reģistrēt visas nepieciešamās darbplūsmas darbības. Ņemiet vērā, ka tas ir prasība, lai būtu jums piešķirti rēķiniem, kas tādā stāvoklī, lai darbplūsmas darbības pieejams jums, ka esat gatavojas izstrādāt.
13. Atveriet Notepad vai Microsoft Visual Studio un ielīmējiet šo kodu. Saglabājiet failu kā. js failu. Šis kods dara divas lietas:
    1.  Tas slēpj pievienojām iepriekšējās mobilā saraksta lapā papildu darbplūsmas saistīto kolonnu. Mēs pievienojām šīs kolonnas tā, ka app ir šāda informācija kontekstā un var darīt nākamo soli.
    2.  Pamatojoties uz darbplūsmas solis, kas ir aktīva, tas attiecas loģika, lai parādītu tikai tās darbības.

Ņemiet vērā, ka lapas nosaukumu un citas vadīklas JS kods jābūt tādai pašai no darbvietas.

1.  Galvenā funkcija (metadataService, dataService, cacheService, $q) {atgriezties {appInit: funkcija (appMetadata) {/ / paslēpt vadīklas, kas ir klāt, bet nav redzams metadataService.configureControl ('My-kreditoram-rēķini, 'ShowAccept', {paslēptas: patiess}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowApprove', {paslēptas: patiess}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowReject', {paslēptas: patiess}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowDelegate', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowRequestChange', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowRecall', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowComplete', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķinus, 'ShowResubmit' { slēptās: true}); }, pageInit: funkcija (pageMetadata, parametri) {ja (pageMetadata.Name = = 'Rēķina detaļas') {/ / Rādīt/paslēpt darbplūsmas darbības, pamatojoties uz darbplūsmas solis metadataService.configureAction ("Akceptēt", {redzams: taisnība}); metadataService.configureAction ('Apstiprināt', {redzams: patiess}); metadataService.configureAction ('Noraidīt', {redzams: patiess}); metadataService.configureAction ("Deleģēt", {redzams: patieso}); metadataService.configureAction (' pieprasījuma izmaiņas ', {redzams: patieso}); metadataService.configureAction ("Atsaukšana" {redzams: patieso}); metadataService.configureAction ('Complete', {redzams: patieso}); metadataService.configureAction ('Iesniedziet' {redzams: patieso});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Augšupielādēt failu kods šai darbvietai, izvēloties **Logic** tab
3.  Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
4.  Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
5.  Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu

### <a name="vendor-invoice-attachments"></a>Kreditora rēķina pielikumus

1.  Noklikšķiniet uz **iestatījumus** (rīku) pogu augšējā labajā stūrī lapā, un pēc tam noklikšķiniet uz **Mobile app**
2.  Noklikšķiniet uz **rediģēt** pogu, lai sāktu rediģēšanas režīmā darbvietā.
3.  Izvēlieties * * rēķinu informāciju * *, kuru izveidojāt iepriekšējās lappuses un pēc tam noklikšķiniet uz **rediģēt**.
4.  Iestatiet **dokumentu pārvaldība** iespēju **Jā** kā parādīts zemāk. **Piezīme:**, ja nav nekādas prasības, lai pierādītu pielikumiem mobilajā ierīcē, varat atstāt šo opciju iestatītu uz **Nr**, kas ir noklusējuma iestatījums.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
7.  Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
8.  Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu

### <a name="vendor-invoice-line-distributions"></a>Kreditora rēķina rindas sadalījumu

Šī scenārija prasībām apstiprina būs tikai rindas līmenī sadali un ka rēķina vienmēr ir tikai viena rinda. Šis scenārijs ir vienkāršs, tāpēc lietotāju pieredzi mobilajā ierīcē arī jābūt pavisam vienkārši, ka lietotājam nav urbt uz leju vairākos līmeņos, lai apskatītu sadalēm. Pārdevēja rēķinus sistēmā Dynamics 365 operācijām ietver iespēju rāda visus sadali no rēķina virsrakstā. Šī pieredze ir, mums ir nepieciešams mobilās scenārija. Tāpēc mēs izmantojam **VendMobileInvoiceAllDistributionTree** lapu izveidot šī mobilās scenārija daļa. 

> [!NOTE] 
> Zinot prasības palīdz mums izlemt, kurš noteiktu lapu, izmantot un kā tieši, lai optimizētu lietotāja mobilajai pieredzei, kad mēs izstrādājam šo scenāriju. Otrajā scenārijā mēs izmantosim citu lapu parāda sadali, jo šis scenārijs prasības atšķiras.

1.  URL, kā jūs darījāt pirms aizstāt izvēlnes elementa nosaukums. Lappuse, kas parādās vajadzētu līdzināties attēlā. [![Visas sadales lapa](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Atveriet mobilā dizainers no **iestatījumus** (rīku) pogu.
3.  Noklikšķiniet uz **rediģēt** pogu, lai sāktu rediģēšanas režīmā darbvietā. **Piezīme:** jūs redzēsiet, ka automātiski tika izveidotas divas jaunas lapas. Sistēma veido šī sacerējuma lappusēs, jo jūs ieslēdzāt dokumentu pārvaldību iepriekšējā sadaļā. Jūs varat ignorēt šo jauno lapu.
4.  Noklikšķiniet uz **pievienot lapu**.
5.  Ievadiet lapas nosaukumu, piemēram, **View grāmatvedības**, un aprakstu, piemēram, **View grāmatvedības rēķinu**.
6.  Click **Done**.
7.  Par **lauki** cilni, noklikšķiniet uz **atlasiet laukus,**, atlasiet šādus laukus no sadalījumiem lapas un pēc tam noklikšķiniet uz **darīts**:
    1.  Summa
    2.  Valūta
    3.  Virsgrāmatas konts

> [!NOTE] 
> Mēs neatlasījāt **aprakstu** kolonnu no sadalījumiem režģi, jo prasības šim scenārijam apstiprināja, ka paplašinātā cena ir tikai summu, kas būs sadales. Tāpēc lietotājam nebūs nepieciešama citu lauku, lai noteiktu atbilstoši summas tipam, kas paredzēta izplatīšanas. Tomēr, ja nākamais scenārijs, mēs **tiks** izmanto šo informāciju, jo šī scenārija prasībām norādīta cita summa ir sadalījumiem (piemēram, PVN).
8.  Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
9.  Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
10. Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu

**Piezīme:****View grāmatvedības** mobilo lapā šobrīd nav saistīts ar jebkuru mobilo lapas, kuras mēs līdz šim esam izstrādājuši. Jo lietotājam jāspēj orientēties uz **View grāmatvedības** lapa no **rēķina detaļas** lapu mobilajā ierīcē ir jāsniedz navigāciju no **rēķina detaļas** lapu, lai **View grāmatvedības** lapu. Mēs veidojam šo navigācija, izmantojot papildu loģiku, izmantojot JavaScript.

1.  Atveriet. js failu, ko izveidojāt iepriekš un pievienot rindas, kuras ir marķētas ar šādu kodu. Šis kods dara divas lietas:
    1.  Tas palīdz garantēt, ka lietotāji nevar naviģēt tieši no darbvietu, lai **View grāmatvedības** lapā.
    2.  To izveido navigācijas vadīklu no **rēķina detaļas** lapu, lai **View grāmatvedības** lapā.

> [!NOTE] 
> Lapas un citas vadīklas JS kodu nosaukumu jāsakrīt no darbvietas.

1.  Galvenā funkcija (metadataService, dataService, cacheService, $q) {atgriezties {appInit: funkcija (appMetadata) {/ / paslēpt vadīklas, kas ir klāt, bet nav redzams metadataService.configureControl ('My-kreditoram-rēķini, 'ShowAccept', {paslēptas: patiess}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowApprove', {paslēptas: patiess}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowReject', {paslēptas: patiess}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowDelegate', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowRequestChange', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowRecall', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķini, 'ShowComplete', {paslēptas: patieso}); metadataService.configureControl ('My-kreditoram-rēķinus, 'ShowResubmit' { slēptās: true}); Slēpt lapas nav piemērojams saknes navigācijas metadataService.hideNavigation('View-accounting'); Saiti, lai apskatītu grāmatvedības metadataService.addLink ("Rēķina-detaļas, ' Skatīt grāmatvedības ', ' Skatīt grāmatvedības nav kontrole", 'Skatīt grāmatvedības', true); }, pageInit: funkcija (pageMetadata, parametri) {ja (pageMetadata.Name = = 'Rēķina detaļas') {/ / Rādīt/paslēpt darbplūsmas darbības, pamatojoties uz darbplūsmas solis metadataService.configureAction ("Akceptēt", {redzams: taisnība}); metadataService.configureAction ('Apstiprināt', {redzams: patiess}); metadataService.configureAction ('Noraidīt', {redzams: patiess}); metadataService.configureAction ("Deleģēt", {redzams: patieso}); metadataService.configureAction (' pieprasījuma izmaiņas ', {redzams: patieso}); metadataService.configureAction ("Atsaukšana" {redzams: patieso}); metadataService.configureAction ('Complete', {redzams: patieso}); metadataService.configureAction ('Iesniedziet' {redzams: patieso});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Augšupielādēt failu kods šai darbvietai, izvēloties **Logic** tab, lai pārrakstītu iepriekšējo kodu
3.  Noklikšķiniet uz **darīts** iziet no rediģēšanas režīma.
4.  Noklikšķiniet uz **atkal** un tad **darīts,**, lai aizvērtu darbvietu
5.  Noklikšķiniet uz **publicēt darbvietu** saglabāt savu darbu

### <a name="validation"></a>Validācija

No mobilās ierīces, atvērt app, un savienot ar savu dinamiku 365 operācijas gadījumā. Pārliecinieties, ka piesakāties uzņēmumam kur kreditora rēķiniem jums tiek piešķirti par pārskata. Jums vajadzētu būt iespējai veikt šādas darbības:

-   Sk **manu apstiprinājumu** darbvietu.
-   Detalizēt **manu apstiprinājumu** darbvietu un skatiet tēmu **manu kreditora rēķiniem** lapu.
-   Detalizēt **manu kreditora rēķiniem** lapu un apskatīt rēķinu sarakstu, kas jums tiek piešķirti.
-   Urbt vērā vienu rēķinu, un redzēt detalizētu rēķinu galvenes informāciju un rindas detaļu.
-   Lapā detaļu redzat saiti uz pielikumiem, un izmantojiet šo saiti, lai virzītos uz saraksta pielikumus un skatīt pielikumus.
-   Lapā detaļu redzat saiti uz **skatīt grāmatvedības** lapa un izmantojiet šo saiti, lai virzītos uz sadali lapu un apskatīt sadalēm.
-   Informācijas lapā, noklikšķiniet uz **darbības** izvēlnes apakšdaļā un veiktu darbplūsmas darbības, kas attiecas uz darbplūsmas soli.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Izstrādājot kompleksa rēķina apstiprināšanas scenārijs fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenārija atribūts</th>
<th>Atbilde</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kādus laukus no rēķina virsrakstā lietotājs vēlēsies redzēt mobilo pieredzi, un kādā secībā?</td>
<td><ol>
<li>Kreditora nosaukums</li>
<li>Rēķina summa</li>
<li>Rēķina konts</li>
<li>Rēķina numurs</li>
<li>Rēķina datums</li>
<li>Rēķina apraksts</li>
<li>Izpildes termiņš</li>
<li>Rēķina valūta</li>
</ol></td>
</tr>
<tr class="even">
<td>Kādus laukus no rēķina rindām lietotājs vēlēsies redzēt mobilo pieredzi, un kādā secībā?</td>
<td><ol>
<li>Sagādes kategorija</li>
<li>Daudzums</li>
<li>Vienības cena</li>
<li>Rindas neto summa</li>
<li>1099. summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Cik daudz rēķina rindās ir rēķins? 80-20 noteikums attiecas, un optimizēt par 80 procentiem.</td>
<td>5.</td>
</tr>
<tr class="even">
<td>Lietotāji vēlēsies redzēt uzskaites sadali (rēķina kodēšana) mobilajā ierīcē laikā atsauksmes</td>
<td>Jā</td>
</tr>
<tr class="odd">
<td>Cik daudz uzskaites sadali (paplašinātā cena, PVN, maksa utt.) pastāv rēķina rindai? Atkal, piemēro 80-20 noteikums.</td>
<td>Paplašinātā cena: 2 PVN: 2 izmaksas: 2</td>
</tr>
<tr class="even">
<td>Vai rēķinos ir arī uzskaites sadales rēķina virsrakstā? Tādā gadījumā šīs uzskaites sadali būtu pieejamas ierīcē?</td>
<td>Netiek lietots</td>
</tr>
<tr class="odd">
<td>Lietotāji vēlēsies redzēt pielikumus rēķina ierīcē</td>
<td>Jā</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Uzdevums

Sekojošiem variantiem var izdarīt scenāriju 1, balstoties uz prasībām 2. scenārijs. Izmantojiet šo sadaļu kā uzdevumā, ko var aizpildīt mācību nolūkos.

1.  Jo vairāk rēķina rindās ir paredzēts scenārijā 2, šādas izmaiņas konstrukcijā palīdzēs optimizēt lietotāja pieredzi mobilajā ierīcē:
    1.  Nevis skatīšanās rēķina rindas (kā 1. scenārijs) informācijas lapā, lietotāji var izvēlēties, lai apskatītu rindas atsevišķā lapā mobile.
    2.  Jo vairāk nekā viena rēķina rinda ir paredzēts šajā scenārijā, ja **VendMobileInvoiceAllDistributionTree** lapa tiek izmantota, lai izstrādātu sadalījumu lapā Mobile (kā 1. scenārijs), var rasties juceklis lietotājam savstarpēji saistīt rindu sadalījumu. Tādēļ izmanto **VendMobileInvoiceLineDistributionTree** lapu dizains sadali lapu.
    3.  Ideālā gadījumā jāuzrāda rēķina rindu šādā kontekstā sadalēm. Tāpēc pārliecinieties, ka lietotājs var rakties, ierindā, lai aplūkotu sadali lapu. Lietot lapu saite iespējas izveidot drill-caur, tāpat _ kā jūs to darījāt galvenes un detaļas lapām 1 scenārijs.

2.  Jo vairāk nekā viena tipa summa gaidāms par sadali 2. scenārijs (PVN, maksa utt.), būs noderīgas, lai parādītu summas tipa apraksts. (Mēs izlaista šo informāciju 1. scenārijs).

## <a name="conclusion"></a>Nobeigums
Mobilā platforma un lietojumprogrammu iespējas ļauj izveidot mobilo sakaru gadījumi, kas ir optimizētas lietotāja bāzes organizācijā. Balstoties uz piemēriem, kas tiek sniegti šajā tēmā, varat izmēģināt citas variācijas un izveidot dažādas pieredzes, kas apmierinātu īpašas vajadzības.


