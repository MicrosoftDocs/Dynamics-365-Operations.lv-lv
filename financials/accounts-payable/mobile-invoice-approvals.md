---
title: "Rēķinu apstiprināšana mobilajā ierīcē"
description: "Programmatūrā Microsoft Dynamics 365 for Operations ietvertās mobilās iespējas sniedz biznesa lietotājam iespēju izstrādāt mobilos risinājumus. Sarežģītu scenāriju gadījumā izstrādātāji var arī paplašināt iespējas atbilstoši savām vēlmēm. Visefektīvākais veids, kā apgūt dažas no jaunajām mobilajām ierīcēm paredzētajām koncepcijām, ir jaunu scenāriju procesa izpilde. Šajā tēmā ir aprakstīta praktiska pieeja mobilo scenāriju izstrādei, kā lietojuma gadījumu apskatot kreditoru rēķinu apstiprināšanu mobilajās ierīcēs. Šajā tēmā sniegtā informācija palīdzēs jums izstrādāt arī citus scenāriju variantus, un to var lietot arī citiem scenārijiem, kas nav saistīti ar kreditoru rēķiniem."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 511dc31b96f2f5133dd0c22712d2c8d6f8746e8c
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="mobile-invoice-approvals"></a>Rēķinu apstiprināšana mobilajā ierīcē

[!include[banner](../includes/banner.md)]


Programmatūrā Microsoft Dynamics 365 for Operations ietvertās mobilās iespējas sniedz biznesa lietotājam iespēju izstrādāt mobilos risinājumus. Sarežģītu scenāriju gadījumā izstrādātāji var arī paplašināt iespējas atbilstoši savām vēlmēm. Visefektīvākais veids, kā apgūt dažas no jaunajām mobilajām ierīcēm paredzētajām koncepcijām, ir jaunu scenāriju procesa izpilde. Šajā tēmā ir aprakstīta praktiska pieeja mobilo scenāriju izstrādei, kā lietojuma gadījumu apskatot kreditoru rēķinu apstiprināšanu mobilajās ierīcēs. Šajā tēmā sniegtā informācija palīdzēs jums izstrādāt arī citus scenāriju variantus, un to var lietot arī citiem scenārijiem, kas nav saistīti ar kreditoru rēķiniem.

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnosacījums                                                                                            | Apraksts                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iepriekš izlasiet mobilo risinājumu rokasgrāmatu.                                                                                |(/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform.md)                                                                                                  |
| Dynamics 365 for Operations                                                                             | Vide, kurā ir instalēta Microsoft Dynamics 365 for Operations versija 1611 un Microsoft Dynamics for Operations 3. platformas atjauninājums (2016. gada novembra versija)                   |
| Instalējiet labojumfailu KB 3204341.                                                                              | Uzdevumu reģistrētājs var kļūdaini reģistrēt divas nolaižamo dialoglodziņu aizvēršanas komandas; tas ir ietverts Dynamics 365 for Operations 3. platformas atjauninājumā (2016. gada novembrī izlaistais atjauninājums) |
| Instalējiet labojumfailu KB 3207800.                                                                              | Šis labojumfails sniedz iespēju skatīt pielikumus mobilajā klientā; tas ir ietverts Dynamics 365 for Operations 3. platformas atjauninājumā (2016. gada novembrī izlaistais atjauninājums)           |
| Instalējiet labojumfailu KB 3208224.                                                                              | Kreditoru rēķinu apstiprināšanas mobilās lietojumprogrammas kods; tas ir ietverts lietojumprogrammas Microsoft Dynamics AX versijā 7.0.1 (2016. gada maija izlaidums).                          |
| Android, iOS vai Windows ierīce, kurā ir instalēta Dynamics 365 for Operations mobilā programma | Meklējiet programmu atbilstošajā programmu veikalā.                                                                                                                     |

## <a name="introduction"></a>Ievads
Lai varētu apstiprināt kreditoru rēķinus mobilajā ierīcē, ir nepieciešami trīs labojumfaili, kas ir norādīti sadaļā Priekšnosacījumi. Šie labojumfaili nenodrošina rēķinu apstiprināšanas darbvietu. Lai uzzinātu, kas ir darbvieta attiecībā uz mobilajām ierīcēm, izlasiet mobilo ierīču risinājumu rokasgrāmatu, kas ir pieminēta sadaļā “Priekšnosacījumi”. Rēķinu apstiprināšanas darbplūsma ir jāizstrādā. 

Katra organizācija atšķirīgā veidā vada un definē savu kreditoru rēķinu biznesa procesu. Pirms kreditoru rēķinu apstiprināšanas mobilā risinājuma izstrādes ir jāņem vērā tālāk norādītie biznesa procesa aspekti. Mērķis ir pēc iespējas vairāk izmantot šos datu punktus, lai optimizētu lietotāja iespējas ierīcē.

-   Kurus rēķina galvenes laukus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?
-   Kurus rēķina rindu laikus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?
-   Cik rēķina rindu ir rēķinā? Lietojiet 80/20 nosacījumu un optimizējiet atbilstoši 80 procentiem.
-   Vai lietotāji vēlas pārskatīšanas laikā mobilajā ierīcē redzēt uzskaites sadales (rēķina kodu). Ja atbilde uz šo jautājumu ir apstiprinoša, ņemiet vērā tālāk norādītos jautājumus.
    -   Cik uzskaites sadales elementu (pilna cena, PVN, izmaksas, dalījumi utt.) ir vienā rēķina rindā? Atkal lietojiet 80/20 nosacījumu.
    -   Vai rēķina galvenē arī ir uzskaites sadales? Jā tā ir, vai šīm uzskaites sadalēm ir jābūt pieejamām ierīcē?

> [!NOTE]
> Šajā tēmā nav paskaidrots, kā rediģēt uzskaites sadales, jo šī funkcionalitāte pašlaik netiek atbalstīta mobilajiem scenārijiem.

-   Vai lietotāji vēlēsies ierīcē redzēt rēķina pielikumus?

Rēķinu apstiprināšanas mobilā risinājuma izstrāde atšķiras atkarībā no atbildēm uz šiem jautājumiem. Mērķis ir optimizēt lietotāja iespējas darbam ar biznesa procesu mobilajā ierīcē organizācijas ietvaros. Šīs tēmas turpinājumā ir aprakstīti scenārija varianti, kas ir izstrādāti, pamatojoties uz dažādām atbildēm uz iepriekš norādītajiem jautājumiem. 

Vienmēr, kad strādājat ar mobilo programmu veidotāju, noteikti publicējiet izmaiņas, lai nepieļautu atjauninājumu zaudēšanu.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Vienkārša rēķinu apstiprināšanas scenārija izstrāde uzņēmumam Contoso
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
<td>Kurus rēķina galvenes laukus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</td>
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
<td>Kurus rēķina rindu laikus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</td>
<td><ol>
<li>Sagādes kategorija</li>
<li>Daudzums</li>
<li>Vienības cena</li>
<li>Rindas neto summa</li>
<li>1099. summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Cik rēķina rindu ir rēķinā? Lietojiet 80/20 nosacījumu un optimizējiet atbilstoši 80 procentiem.</td>
<td>1.</td>
</tr>
<tr class="even">
<td>Vai lietotāji vēlas pārskatīšanas laikā mobilajā ierīcē redzēt uzskaites sadales (rēķina kodu).</td>
<td>Jā</td>
</tr>
<tr class="odd">
<td>Cik uzskaites sadales elementu (pilna cena, PVN, izmaksas utt.) ir vienā rēķina rindā? Atkal lietojiet 80/20 nosacījumu.</td>
<td>Pilna cena: 2, PVN: 0, izmaksas: 0</td>
</tr>
<tr class="even">
<td>Vai rēķina galvenē arī ir uzskaites sadales? Jā tā ir, vai šīm uzskaites sadalēm ir jābūt pieejamām ierīcē?</td>
<td>Netiek lietots</td>
</tr>
<tr class="odd">
<td>Vai lietotāji vēlēsies ierīcē redzēt rēķina pielikumus?</td>
<td>Jā</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Darbvietas izveide

1.  Pārlūkprogrammā atveriet programmatūru Dynamics 365 for Operations un pierakstieties.
2.  Pēc pierakstīšanās pievienojiet URL tekstu **&mode=mobile**, kā tas ir redzams šajā piemērā, un atsvaidziniet lapu: https://&lt;jūsuurl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**.
3.  Noklikšķiniet uz pogas **Iestatījumi** (zobrats) lapas augšējā labajā stūrī un pēc tam noklikšķiniet uz **Mobilā programma**. Tiek parādīts mobilo programmu veidotājs, tāpat kā tiek parādīts uzdevuma reģistrētājs.
4.  Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu darbvietu. Šī piemēra ietvaros piešķiriet darbvietai nosaukumu **Mani apstiprinājumi**.
5.  Ievadiet aprakstu.
6.  Atlasiet darbvietas krāsu. Darbvietas krāsa tiek izmantota šīs darbvietas mobilā risinājuma vispārējā stila izveidei.
7.  Atlasiet darbvietas ikonu.
8.  Noklikšķiniet uz **Gatavs**
9.  Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu izmaiņas.

### <a name="vendor-invoices-assigned-to-me"></a>Kreditora rēķini, kas piešķirti man

Pirmā mobilā lapa, kas ir jāizstrādā, ir lietotājam pārskatīšanai piešķirto rēķinu saraksts. Lai izstrādātu šo mobilo lapu, izmantojiet Dynamics 365 for Operations lapu **VendMobileInvoiceAssignedToMeListPage**. Pirms šīs procedūras pabeigšanas pārliecinieties, ka jums pārskatīšanai ir piešķirts vismaz viens kreditora rēķins un ka rēķina rindā ir divi sadales elementi. Šie iestatījumi atbilst šī scenārija prasībām.

1.  Dynamics 365 for Operations URL tekstā aizstājiet izvēlnes elementa nosaukumu ar **VendMobileInvoiceAssignedToMeListPage**, lai atvērtu moduļa **Parādi kreditoriem** lapas **Gaidošie kreditoru rēķini, kas piešķirti man** mobilo versiju. Atkarībā no tā, cik rēķinu jums ir piešķirts sistēmā, šajā lapā tiek rādīti šie rēķini. Lai atrastu konkrētu rēķinu, varat izmantot kreisajā pusē esošo filtru. Taču šī piemēra ietvaros nav nepieciešams konkrēts rēķins. Ir nepieciešams jebkurš jums piešķirts rēķins, ko var izmantot mobilās lapas izstrādei. Jaunās pieejamās lapas ir īpaši izstrādātas kreditoru rēķinu mobilo scenāriju izstrādei. Tāpēc ir jāizmanto šīs lapas. URL ir jālīdzinās šim URL, un pēc tā ievades ir jātiek atvērtai attēlā redzamajai lapai: https://&lt;jūsuURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Lapa Gaidošie kreditoru rēķini, kas piešķirti man](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Noklikšķiniet uz pogas **Iestatījumi** (zobrats) lapas augšējā labajā stūrī un pēc tam noklikšķiniet uz **Mobilā programma**.
3.  Atlasiet savu darbvietu un noklikšķiniet uz **Rediģēt**.
4.  Noklikšķiniet uz **Pievienot lapu**, lai izveidotu pirmo mobilo lapu.
5.  Ievadiet nosaukumu, piemēram, **Mani kreditoru rēķini**, un aprakstu, piemēram, **Man pārskatīšanai piešķirtie kreditoru rēķini**.
6.  Noklikšķiniet uz **Gatavs**.
7.  Mobilo programmu veidotāja cilnē **Lauki** noklikšķiniet uz **Atlasīt laukus**. Saraksta lapā redzamajām kolonnām ir jālīdzinās tālāk esošajam attēlam. [![Kolonnas lapā Gaidošie kreditoru rēķini, kas piešķirti man](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Pievienojiet tās kolonnas no saraksta lapas, kuras ir jārāda lietotājiem mobilajā lapā. Pievienošanas secība atbilst secībai, kādā laiki tiek rādīti lietotājam. Vienīgais veids, kā mainīt laiku secību, ir atkārtoti atlasīt visus laukus. Pamatojoties uz šī scenārija prasībām, ir nepieciešami astoņi tālāk norādītie lauki. Taču dažiem lietotājiem var šķist, ka astoņi lauki ir pārāk daudz informācijas, ko skatīt mobilajā ierīcē. Tāpēc mobilās lapas saraksta skatā tiks rādīti tika svarīgākie lauki. Pārējie laiki tiks rādīti detalizētās informācijas skatā, kas tiks izstrādāts vēlāk. Pagaidām tiks pievienoti tālāk norādītie lauki. Noklikšķiniet uz pluszīmes (**+**) šajās kolonnās, lai pievienoto mobilajai lapai.
    1.  Kreditora nosaukums
    2.  Rēķina kopsumma
    3.  Rēķina konts
    4.  Rēķina numurs
    5.  Rēķina datums

    Pēc laiku pievienošanas mobilajai lapai ir jālīdzinās tālāk esošajam attēlam. [![Lapa pēc lauku pievienošanas](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Tagad ir jāpievieno arī tālāk norādītās kolonnas, lai vēlāk varētu iespējot darbplūsmas darbības.
    1.  Rādīt pabeigšanas uzdevumu
    2.  Rādīt deleģēšanas uzdevumu
    3.  Rādīt atsaukšanas uzdevumu
    4.  Rādīt noraidīšanas uzdevumu
    5.  Rādīt pabeigšanas pieprasījuma uzdevumu
    6.  Rādīt atkārtotas iesniegšanas uzdevumu

10. Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
11. Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
12. Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.
13. Parādu kreditoriem parametru veidlapas sadaļā **Rēķins** iespējojiet opiju **Rādīt rēķina kopsummu gaidošo kreditoru rēķinu sarakstā**. Ņemiet vērā, ka rēķinu kopsummas tiek aprēķinātas un rādītas gaidošo kreditoru rēķinu saraksta lapā tikai tad, ja ir iespējots šis parametrs. Tā ir jauna iespēja, kas ir ietverta priekšnoteikuma labojumfailā KB 3208224.

### <a name="vendor-invoice-details"></a>Kreditora rēķina detalizēta informācija

Lai izstrādātu rēķina detalizētas informācijas lapu mobilajām ierīcēm, izmantojiet Dynamics 365 for Operations lapu **VendMobileInvoiceHeaderDetails**. Ņemiet vērā, ka atkarībā no rēķinu skaita jūsu sistēmā šajā lapā tiek rādīti vecākie rēķini (rēķini, kas tika izveidoti pirmie). Lai atrastu konkrētu rēķinu, varat izmantot kreisajā pusē esošo filtru. Taču šī piemēra ietvaros nav nepieciešams konkrēts rēķins. Ir nepieciešami dažu rēķinu dati, lai varētu izstrādāt mobilo lapu. [![Lapa Darbplūsma](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Dynamics 365 for Operations URL tekstā aizstājiet izvēlnes elementa nosaukumu ar **VendMobileInvoiceHeaderDetails**, lai atvērtu veidlapu.
2.  Atveriet mobilo programmu veidotāju, izmantojot pogu **Iestatījumi** (zobrats).
3.  Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.
4.  Atlasiet lapu **Mani kreditoru rēķini**, ko iepriekš izveidojāt, un pēc tam noklikšķiniet uz **Rediģēt**.
5.  Cilnē **Lauki** noklikšķiniet uz kolonnas galvenes **Režģis**.
6.  Noklikšķiniet uz **Rekvizīti** &gt; **Pievienot lapu**. **Piezīme.** Kad noklikšķināt uz galvenes **Režģis** un pievienojat lapu, tiek automātiski izveidotas attiecības ar detalizētas informācijas lapu.
7.  Ievadiet lapas nosaukumu, piemēram, **Rēķina detalizēta informācija**, un aprakstu, piemēram, **Skatīt rēķina galvenes un rindu detalizētu informāciju**.
8.  Noklikšķiniet uz **Atlasīt laukus**. Ņemiet vērā, ka pievienošanas secība atbilst secībai, kādā laiki tiek rādīti lietotājam. Vienīgais veids, kā mainīt laiku secību, ir atkārtoti atlasīt visus laukus.
9.  Pievienojiet tālāk norādītos laukus no galvenes, pamatojoties uz šī scenārija prasībām.
    1.  Kreditora nosaukums
    2.  Rēķina kopsumma
    3.  Rēķina konts
    4.  Rēķina numurs
    5.  Rēķina datums
    6.  Rēķina apraksts
    7.  Izpildes termiņš
    8.  Rēķina valūta

10. Pievienojiet tālāk norādītos laukus no lapas rindu režģa.
    1.  Sagādes kategorija
    2.  Daudzums
    3.  Vienības cena
    4.  Rindas neto summa
    5.  1099. summa

11. Kad ir pievienoti visi divu iepriekšējo darbību aprakstā norādītie lauki, noklikšķiniet uz **Gatavs**. Lapai ir jālīdzinās tālāk esošajam attēlam. [![Lapa pēc lauku pievienošanas](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
13. Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
14. Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.

### <a name="workflow-actions"></a>Darbplūsmas darbības

Lai pievienotu darbplūsmas darbības, izmantojiet Dynamics 365 for Operations lapu **VendMobileInvoiceHeaderDetails**. Lai atvērtu šo lapu, aizstājiet izvēlnes elementa nosaukumu URL tekstā, kā to darījāt iepriekš. Pēc tam tveriet mobilo programmu veidotāju, izmantojot pogu **Iestatījumi** (zobrats). Izpildiet tālāk norādītās darbības, lai pievienotu darbplūsmas darbības detalizētas informācijas lapā.

1.  Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.
2.  Atlasiet lapu **Rēķina detalizēta informācija**, ko iepriekš izveidojāt, un pēc tam noklikšķiniet uz **Rediģēt**.
3.  Cilnē **Darbības** noklikšķiniet uz **Pievienot darbību**.
4.  Ievadiet darbības nosaukumu, piemēram, **Apstiprināt**, un aprakstu, piemēram, **Apstiprināt rēķinu**. Ņemiet vērā, ka šeit ievadītais darbības nosaukums kļūst par darbības nosaukumu, kas tiek rādīts lietotājam mobilajā programmā.
5.  Noklikšķiniet uz **Gatavs**.
6.  Noklikšķiniet uz **Atlasīt laukus**.
7.  Pārskatiet darbplūsmas procesu lapā **VendMobileInvoiceHeaderDetails** un veiciet darbību, ko vēlaties ierakstīt. Šī procesa laikā noteikti ievadiet darbplūsmas komentārus, lai mobilajā risinājumā tiktu ietverts arī komentāru lauks.
8.  Pēc darbplūsmas darbības veikšanas noklikšķiniet uz **Gatavs**, lai pabeigtu darbību Atlasīt laukus.
9.  Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
10. Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
11. Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.
12. Atkārtojiet 3.-11. darbību, lai ierakstītu visas nepieciešamās darbplūsmas darbības. Ņemiet vērā, ka, lai jums būtu pieejamas darbplūsmas darbības, kuras vēlaties izstrādāt, jums ir jābūt piešķirtiem rēķiniem ar konkrētu stāvokli, kas sniedz iespēju veikt šīs darbības.
13. Atveriet programmu Piezīmjbloks vai Microsoft Visual Studio un ielīmējiet tālāk norādīto kodu. Saglabājiet failu .js formātā. Šis kods nodrošina divas darbības.
    1.  Tas paslēpj ar darbplūsmu saistītās papildu kolonnas, kas iepriekš tika pievienotas mobilajā saraksta lapā. Šīs kolonnas tika pievienotas, lai programmā būtu pieejama šī informācija kontekstā un varētu veikt nākamo darbību.
    2.  Pamatojoties uz aktīvajiem darbplūsmas soļiem, tiek lietota loģika, lai rādītu tikai šīs darbības.

Ņemiet vērā, ka lapas nosaukumam un citām vadīklām JS kodā ir jābūt vienādām ar šiem elementiem darbvietā.

1.  function main(metadataService, dataService, cacheService, $q) {        return {            appInit: function (appMetadata) {                // Paslēpt nepieciešamās vadīklas, kurām nav jābūt redzamām                metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });              metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });            metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });            },            pageInit: function (pageMetadata, params) {     if (pageMetadata.Name == 'Invoice-details') {                    // Rādīt/paslēpt darbplūsmas darbības, pamatojoties uz darbplūsmas soli                    metadataService.configureAction('Accept', { visible: true });                    metadataService.configureAction('Approve', { visible: true });                    metadataService.configureAction('Reject', { visible: true });                    metadataService.configureAction('Delegate', { visible: true });                    metadataService.configureAction('Request-change', { visible: true });                    metadataService.configureAction('Recall', { visible: true });                    metadataService.configureAction('Complete', { visible: true });                    metadataService.configureAction('Resubmit', { visible: true });

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

2.  Augšupielādējiet koda failu darbvietā, atlasot cilni **Loģika**.
3.  Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
4.  Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
5.  Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.

### <a name="vendor-invoice-attachments"></a>Kreditoru rēķinu pielikumi

1.  Noklikšķiniet uz pogas **Iestatījumi** (zobrats) lapas augšējā labajā stūrī un pēc tam noklikšķiniet uz **Mobilā programma**.
2.  Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.
3.  Atlasiet lapu **Rēķina detalizēta informācija**, ko iepriekš izveidojāt, un pēc tam noklikšķiniet uz **Rediģēt**.
4.  Iestatiet opcijas **Dokumentu vadība** vērtību **Ja**, kā tas ir redzams tālāk. **Piezīme.** Ja nav nepieciešams rādīt pielikumus mobilajā ierīcē, varat atstāt šīs opcijas vērtību **Nē**, kas ir noklusējuma iestatījums.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
7.  Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
8.  Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.

### <a name="vendor-invoice-line-distributions"></a>Kreditora rēķina rindas sadales

Saskaņā ar šī scenārija prasībām tiks lietotas tikai rindas līmeņa sadales un rēķinā vienmēr būs tikai viena rinda. Tā kā šis ir vienkāršs scenārijs, arī lietotāja iespējām mobilajā ierīcē ir jābūt pietiekami vienkāršām, sniedzot lietotājam iespēju skatīt sadales, nepiekļūstot vairākiem zemākiem līmeņiem. Programmatūrā Dynamics 365 for Operations ir pieejama kreditoru rēķinu opcija, kas sniedz iespēju rādīt visas rēķina galvenē ietvertās sadales. Šis risinājums ir jāizmanto mobilajā scenārijā. Tāpēc šīs mobilā scenārija daļās izstrādei ir jāizmanto lapa **VendMobileInvoiceAllDistributionTree**. 

> [!NOTE] 
> Tas, ka ir zināmas prasības, palīdz scenārija izstrādes laikā izvēlēties konkrētu izmantojamo lapu un to, kā optimizēt mobilo risinājumu atbilstoši lietotāja vajadzībām. Otrā scenārija ietvaros sadales rādīšanai tiks izmantotas citas lapas, jo šī scenārija prasības atšķiras.

1.  Aizstājiet izvēlnes elementa nosaukumu URL tekstā, kā to darījāt iepriekš. Parādītajai lapai ir jālīdzinās tālāk esošajam attēlam. [![Lapa Visas sadales](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Atveriet mobilo programmu veidotāju, izmantojot pogu **Iestatījumi** (zobrats).
3.  Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu. **Piezīme.** Ir automātiski izveidotas divas jaunas lapas. Sistēmā šīs lapas tiek izveidotas, jo, veicot iepriekšējā sadaļā aprakstītās darbības, jūs ieslēdzāt dokumentu vadību. Varat ignorēt šīs divas lapas.
4.  Noklikšķiniet uz **Pievienot lapu**.
5.  Ievadiet lapas nosaukumu, piemēram, **Skatīt uzskaiti**, un aprakstu, piemēram, **Skatīt rēķina uzskaiti**.
6.  Noklikšķiniet uz **Gatavs**.
7.  Cilnē **Lauki** noklikšķiniet uz **Atlasīt laukus**, sadales elementu lapā atlasiet tālāk norādītos laukus un pēc tam noklikšķiniet uz **Gatavs**:
    1.  Summa
    2.  Valūta
    3.  Virsgrāmatas konts

> [!NOTE] 
> Sadales režģī netika atlasīta kolonna **Apraksts**, jo saskaņā ar šī scenārija prasībām pilna cena ir vienīgā summa, kam ir sadale. Tāpēc lietotājam nebūs vajadzīgs cits lauks, lai norādīto summas veidu, uz ko attiecas sadale. Taču nākamā scenārija ietvaros šī informācija **tiks** izmantota, jo saskaņā ar tā scenārija prasībām sadales ir arī citiem summas veidiem (piemēram, PVN).
8.  Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
9.  Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
10. Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.

**Piezīme.** Mobilā lapa **Skatīt uzskaiti** pašlaik nav saistīta ne ar vienu citu līdz šim izveidoto mobilo lapu. Tā kā lietotājam ir jāvar mobilajā ierīcē pāriet no lapas **Rēķina detalizēta informācija** uz lapu **Skatīt uzskaiti**, ir jānodrošina navigācija no lapas **Rēķina detalizēta informācija** uz lapu **Skatīt uzskaiti**. Šī navigācija tiek nodrošināta, izmantojot papildu loģiku valodā JavaScript.

1.  Atveriet iepriekš izveidoto .js formāta failu un pievienojiet tālāk esošā koda iezīmētās rindas. Šis kods nodrošina divas darbības.
    1.  Tas palīdz nodrošināt, ka lietotāji nevar tieši navigēt no darbvietas uz lapu **Skatīt uzskaiti**.
    2.  Tas nodrošina navigācijas vadīklu navigācijai no lapas **Rēķina detalizēta informācija** uz lapu **Skatīt uzskaiti**.

> [!NOTE] 
> Lapas nosaukumam un citām vadīklām JS kodā ir jābūt vienādām ar šiem elementiem darbvietā.

1.  function main(metadataService, dataService, cacheService, $q) {        return {            appInit: function (appMetadata) {                // Paslēpt nepieciešamās vadīklas, kurām nav jābūt redzamām                metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });              metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });            metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });                // Paslēpt lapas, kas neattiecas uz saknes navigāciju                metadataService.hideNavigation('View-accounting');                //Saite uz lapu Skatīt atskaiti                metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);            },            pageInit: function (pageMetadata, params) {     if (pageMetadata.Name == 'Invoice-details') {                    // Rādīt/paslēpt darbplūsmas darbības, pamatojoties uz darbplūsmas soli                    metadataService.configureAction('Accept', { visible: true });                    metadataService.configureAction('Approve', { visible: true });                    metadataService.configureAction('Reject', { visible: true });                    metadataService.configureAction('Delegate', { visible: true });                    metadataService.configureAction('Request-change', { visible: true });                    metadataService.configureAction('Recall', { visible: true });                    metadataService.configureAction('Complete', { visible: true });                    metadataService.configureAction('Resubmit', { visible: true });

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

2.  Augšupielādējiet koda failu darbvietā, atlasot cilni **Loģika**, lai pārrakstītu iepriekšējo kodu.
3.  Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.
4.  Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.
5.  Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.

### <a name="validation"></a>Validācija

Mobilajā ierīcē atveriet programmu un izveidojiet savienojumu ar Dynamics 365 for Operations instanci. Pārliecinieties, ka pierakstāties uzņēmumā, kurā jums pārskatīšanai ir piešķirti kreditoru rēķini. Jums ir jāvar veikt tālāk norādītās darbības.

-   Skatīt darbvietu **Mani apstiprinājumi**.
-   Detalizēti skatīt darbvietu **Mani apstiprinājumi** un skatīt lapu **Mani kreditoru rēķini**.
-   Detalizēti skatīt lapu **Mani kreditoru rēķini** un skatīt jums piešķirto rēķinu sarakstu.
-   Detalizēti skatīt vienu no rēķiniem un skatīt rēķina galvenes un rindu detalizētu informāciju.
-   Detalizētas informācijas lapā redzēt pielikumu saiti un to izmantoto, lai navigētu uz pielikumu sarakstu un skatītu pielikumus.
-   Detalizētas informācijas lapā redzēt saiti uz lapu **Skatīt uzskaiti** un izmantot šo saiti, lai navigētu uz sadales lapu un skatītu sadales.
-   Detalizētas informācija lapas apakšdaļā noklikšķināt uz izvēlnes **Darbības** un veikt darbplūsmas darbības, kas attiecas uz konkrēto darbplūsmas soli.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Sarežģīta rēķina apstiprināšanas scenārija izstāde uzņēmumam Fabrikam
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
<td>Kurus rēķina galvenes laukus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</td>
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
<td>Kurus rēķina rindu laikus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</td>
<td><ol>
<li>Sagādes kategorija</li>
<li>Daudzums</li>
<li>Vienības cena</li>
<li>Rindas neto summa</li>
<li>1099. summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Cik rēķina rindu ir rēķinā? Lietojiet 80/20 nosacījumu un optimizējiet atbilstoši 80 procentiem.</td>
<td>5.</td>
</tr>
<tr class="even">
<td>Vai lietotāji vēlas pārskatīšanas laikā mobilajā ierīcē redzēt uzskaites sadales (rēķina kodu).</td>
<td>Jā</td>
</tr>
<tr class="odd">
<td>Cik uzskaites sadales elementu (pilna cena, PVN, izmaksas utt.) ir vienā rēķina rindā? Atkal lietojiet 80/20 nosacījumu.</td>
<td>Pilna cena: 2, PVN: 2, izmaksas: 2</td>
</tr>
<tr class="even">
<td>Vai rēķina galvenē arī ir uzskaites sadales? Jā tā ir, vai šīm uzskaites sadalēm ir jābūt pieejamām ierīcē?</td>
<td>Netiek lietots</td>
</tr>
<tr class="odd">
<td>Vai lietotāji vēlēsies ierīcē redzēt rēķina pielikumus?</td>
<td>Jā</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Vingrinājums

Pamatojoties uz 2. scenārija prasībām, var izstrādāt tālāk norādītos 1. scenārija variantus. Izmantojiet šo scenāriju kā vingrinājumu, ko varat veikt mācību nolūko

1.  Tā kā 2. scenārija ietvaros ir paredzēts apstrādāt vairāk rēķina rindu, tālāk norādītās izstrādes izmaiņas palīdzēs optimizēt lietotāja iespējas mobilajā ierīcē.
    1.  Tā vieta, lai skatītu rēķina rindas detalizētas informācijas lapā (kā 1. scenārijā), lietotāji var izvelēties skatīt rindas atsevišķā mobilajā lapā.
    2.  Tā kā šī scenārija ietvaros ir paredzēts apstrādāt vairākas rēķina rindas, ja mobilās sadales lapas izstrādei tiek izmantota lapa **VendMobileInvoiceAllDistributionTree** (kā 1. scenārijā), lietotājam var būt grūti saistīt rindas ar sadalēm. Tāpēc sadales lapas izstrādei izmantojiet lapu **VendMobileInvoiceLineDistributionTree**.
    3.  Ideālā gadījumā šī scenārija ietvaros sadales ir jārāda rēķina rindas kontekstā. Tāpēc nodrošiniet, lai lietotājs varētu detalizēti skatīt rindas informāciju, tādējādi piekļūstot sadales lapai. Izmantojiet lapas saites iespēju, lai nodrošinātu detalizēto apskati, tāpat kā to darījāt galvenes lapai un detalizētās informācijas lapai 1. scenārija ietvaros.

2.  Tā kā 2. scenārija ietvaros ir paredzēts apstrādāt vairākus summas veidus (PVN, izmaksas utt.), ir noderīgi rādīt summas veida sadali. (Šī informācija tika atmesta 1. scenārija ietvaros.)

## <a name="conclusion"></a>Nobeigums
Mobilā platforma un lietojumprogrammas iespējas sniedz iespēju izstrādāt mobilos scenārijus, kas ir optimizēti atbilstoši organizācijas lietotāju vajadzībām. Pamatojoties uz šajā rēmā sniegtajiem piemēriem, jūs varat izmēģināt citus variantus un izveidot atšķirīgus risinājumus, kas atbilst noteiktām vajadzībām.




