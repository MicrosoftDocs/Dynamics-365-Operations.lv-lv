---
title: Pirkšanas pieprasījuma apskats
description: Šajā tēmā ir aprakstīta pirkšanas pieprasījuma darbplūsma un iespējamie pirkšanas pieprasījuma statusi.
author: mkirknel
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3b365bf99fcb5c97a1afe1675ddcf34a0db8f07
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207860"
---
# <a name="purchase-requisition-overview"></a>Pirkšanas pieprasījuma apskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta pirkšanas pieprasījuma darbplūsma un iespējamie pirkšanas pieprasījuma statusi.

Atkarībā no jūsu uzņēmuma iestatījumiem, var izveidot organizācijā izmantoto preču pirkšanas pieprasījumus. Pirkšanas pieprasījums ir iekšējs dokuments, kas pilnvaro iepirkumu departamentu pirkt krājumus vai pakalpojumus.  

Kad pirkšanas pieprasījums ir apstiprināts, to var izmantot pirkšanas pasūtījuma izveidei. Pirkšanas pasūtījumi ir ārējie dokumenti, ko iepirkumu departaments iesniedz piegādātājiem.

## <a name="creating-purchase-requisitions"></a>Pirkšanas pieprasījumu izveidošana
Pirkšanas pieprasījumu var izveidot lapā **Mani pirkšanas pieprasījumi**, kur var atlasīt nepieciešamos krājumus un pakalpojumus. Krājumus var izvēlēties jūsu organizācijas izveidotā sagādes katalogā vai var pieprasīt tos krājumus, kas nav atrodami katalogā, atlasot iepirkuma kategoriju un ievadot preces datus.  

Pirms varat iesniegt pirkšanas pieprasījumu pārskatīšanai, programmā ir jākonfigurē darbplūsmas. Izmantojiet darbplūsmu, lai apstrādātu pirkšanas pieprasījumu pārskatīšanas procesā no sākotnējā statusa **Uzmetums** līdz gala statusam **Apstiprināts**.

### <a name="purchase-requisition-statuses"></a>Pirkšanas pieprasījumu statusi

Kad tiek izveidots pirkšanas pieprasījums, tam tiek piešķirts statuss. Statuss tiek piešķirts arī visām pirkšanas pieprasījumā pievienotajām rindām. Kad pirkšanas pieprasījums tiek iesniegts darbplūsmā pārskatīšanai, tā un katras rindas statuss tiek atjaunināts atbilstoši rindu apstrādes gaitai darbplūsmas procesā.  

Pirkšanas pieprasījuma darbplūsmas procesu var konfigurēt, lai pirkšanas pieprasījums darbplūsmas procesā tiek virzīts kā viens dokuments. Papildus atsevišķas pirkšanas pieprasījuma rindas var virzīt attiecīgajiem pārskatītājiem. Ja tiek pārskatītas atsevišķas pirkšanas pieprasījuma rindas, katras pirkšanas pieprasījuma rindas statusu var atjaunināt atbilstoši rindas apstrādes gaitai pārskatīšanas procesā. Kad visu rindu apstrāde pārskatīšanas procesā ir pabeigta un ir veiktas visas pirkšanas pieprasījuma pārskatīšanas darbības, tiek atjaunināts visa pirkšanas pieprasījuma statuss.

### <a name="purchase-requisition-workflow"></a>Pirkšanas pieprasījuma darbplūsma

Nākamajā diagrammā ir redzami pirkšanas pieprasījumam un tā rindām piešķirtais statuss atbilstoši to apstrādes gaitai darbplūsmas procesā.  

[![Pirkšanas pieprasījuma virsraksta un rindu statusi](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Pirkšanas pieprasījuma virsraksta un rindu statusa attiecības

Pirkšanas pieprasījuma vispārējo statusu nosaka pirkšanas pieprasījuma rindu statuss. Līdz ar to, lai varētu pabeigt visu pirkšanas pieprasījuma pārskatīšanas procesu, ir jāpabeidz visu pirkšanas pieprasījuma rindu pārskatīšanas process. Nākamajā tabulā ir aprakstīts pirkšanas pieprasījumam virsrakstam un rindām piešķirtais statuss atbilstoši pirkšanas pieprasījuma apstrādes gaitai darbplūsmas procesā.

<table>
<thead>
<tr class="header">
<th>Pirkšanas pieprasījuma statuss</th>
<th>Pirkšanas pieprasījuma rindas statuss</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Melnraksts</td>
<td>Melnraksts</td>
<td>Ir izveidots pirkšanas pieprasījums un pirkšanas pieprasījuma rinda, taču tie nav iesniegti pārskatīšanai. Pirkšanas pieprasījumus un pirkšanas pieprasījuma rindas, kuru statuss ir <strong>Melnraksts</strong>, var modificēt. Pirkšanas pieprasījuma vai pirkšanas pieprasījuma rindas statuss ir <strong>Melnraksts</strong> arī tad, ja pieprasījums vai rinda ir atsaukta, taču nav atkārtoti iesniegta pārskatīšanai. <strong>Piezīme.</strong> Pirkšanas pieprasījumu var iesniegt vai atsaukt dokumenta līmenī. Taču nevarat iesniegt vai atsaukt atsevišķu pirkšanas pieprasījuma rindu.</td>
</tr>
<tr class="even">
<td>Tiek pārskatīts</td>
<td><ul>
<li>Tiek pārskatīts</li>
<li>Atteikts</li>
</ul></td>
<td>Ja darbplūsma ir konfigurēta tā, lai pirkšanas pieprasījuma rindas tiek virzītas atsevišķiem pārskatītājiem, katras pirkšanas pieprasījuma rindas statuss ir <strong>Notiek pārskatīšana</strong> vai <strong>Atteikts</strong>. Pirkšanas pieprasījuma statuss tiek atjaunināts, kad visu rindu apstrāde pārskatīšanas procesā ir pabeigta un ir veiktas visas pirkšanas pieprasījuma pārskatīšanas darbības.
<ul>
<li><strong>Notiek pārskatīšana</strong> — pirkšanas pieprasījuma rindas ir iesniegtas pārskatīšanai. Kad pirkšanas pieprasījuma rindas apstrāde darbplūsmas procesā ir pabeigta, šīs rindas statuss saglabājas <strong>Notiek pārskatīšana</strong>, līdz visas pārējās pirkšanas pieprasījuma rindas ir pārskatītas.</li>
<li><strong>Atteikts</strong> — pirkšanas pieprasījuma rinda ir atteikta. Atteiktās pirkšanas pieprasījuma rindas var modificēt iesniegt atkārtoti.</li>
</ul>
Ja atteikta pirkšanas pieprasījuma rinda tiek iesniegta vēlreiz, pārskatīšanas process tiek sākts vēlreiz visām pirkšanas pieprasījuma rindām, kas vēl tiek pārskatītas. </br><strong>Piezīme:</strong> jau iesniegtu pirkšanas pieprasījumu var atsaukt. Ja pirkšanas pieprasījums tiek atsaukts, atsauktas tiek arī visas pārējās pirkšanas pieprasījuma rindas. Atsauktas pirkšanas pieprasījuma rindas var dzēst.</td>
</tr>
<tr class="odd">
<td>Atteikts</td>
<td>Atteikts</td>
<td>Pirkšanas pieprasījums un visas pirkšanas pieprasījuma rindas ir atteiktas. Atteikto pirkšanas pieprasījumu un pirkšanas pieprasījuma rindas var iesniegt vēlreiz.</td>
</tr>
<tr class="even">
<td>Apstiprināts</td>
<td><ul>
<li>Apstiprināts</li>
<li>Atcelts</li>
<li>Slēgts</li>
</ul></td>
<td>Visu pirkšanas pieprasījuma rindu apstrāde pārskatīšanas procesā ir pabeigta un ir veiktas visas pirkšanas pieprasījuma pārskatīšanas darbības.
<ul>
<li><strong>Apstiprināts</strong> — pirkšanas pieprasījuma rindu apstrāde pārskatīšanas procesā ir pabeigta, un rinda ir apstiprināta.</li>
<li><strong>Atcelts</strong> — pirkšanas pieprasījuma rinda ir tikusi apstiprināta, taču tā ir atcelta, jo vairs nav vajadzīga. Anulēt var tikai apstiprinātas pirkšanas pieprasījuma rindas.</li>
<li><strong>Slēgts</strong> — pirkšanas pieprasījuma rinda ir apstiprināta un dokuments ir izveidots atbilstoši pieprasījuma mērķim.
<ul>
<li>Ja pieprasījuma mērķis ir patēriņš, pirkšanas pasūtījuma rindai tiek ģenerēts pirkšanas pieprasījums.</li>
<li>Ja pieprasījuma mērķis ir papildināšana, tiek ģenerēts viens vai vairāki izpildes dokumenti.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Atcelts</td>
<td>Atcelts</td>
<td>Pirkšanas pieprasījums un visas pirkšanas pieprasījuma rindas ir atcelti.</br> <strong>Piezīme.</strong> Ja pirkšanas pieprasījuma rindā norādītais krājums vairs nav nepieciešams un pirkšanas pieprasījuma rinda jau ir apstiprināta, tā ir jāatceļ. Anulēt var tikai apstiprinātas pirkšanas pieprasījuma rindas. Ja kāda pirkšanas pieprasījuma rinda vēl tiek pārskatīta, pirkšanas pieprasījuma statuss ir <strong>Notiek pārskatīšana</strong>. Šajā gadījumā pirkšanas pieprasījumu var atsaukt un dzēst attiecīgo pirkšanas pieprasījuma rindu.</td>
</tr>
<tr class="even">
<td>Slēgts</td>
<td><ul>
<li>Slēgts</li>
<li>Atcelts</li>
</ul></td>
<td>Pirkšanas pieprasījums ir slēgts, un ir ģenerēts viens vai vairāki izpildes dokumenti.
<ul>
<li><strong>Slēgts</strong> — pirkšanas pieprasījuma rinda ir apstiprināta un dokuments ir izveidots atbilstoši pieprasījuma mērķim.
<ul>
<li>Ja pieprasījuma mērķis ir patēriņš, pirkšanas pasūtījuma rindai tiek ģenerēts pirkšanas pieprasījums.</li>
<li>Ja pieprasījuma mērķis ir papildināšana, tiek ģenerēts viens vai vairāki izpildes dokumenti.</li>
</ul></li>
<li><strong>Atcelts</strong> — pirkšanas pieprasījuma rinda ir tikusi apstiprināta, taču tā ir atcelta, jo vairs nav vajadzīga. Anulēt var tikai apstiprinātas pirkšanas pieprasījuma rindas.</li>
</ul>
<strong>Piezīme.</strong> Ja slēgtajā pirkšanas pieprasījuma rindā minētā prece vairs nav vajadzīga, rinda ir jāanulē šai pirkšanas pieprasījuma rindai izveidotajā izpildes dokumentā.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Izmaksu sadalīšana uz vairākiem finanšu kontiem
Varat sadalīt preču izmaksas, kas ir iekļautas pirkšanas pieprasījumā vairākos finanšu kontos. Ja jūsu organizācija izmanto tādas dimensijas kā centru un nodaļu izmaksas, varat sadalīt preču izmaksas dimensijās finanšu kontos.

## <a name="requisition-purposes"></a>Pieprasījuma mērķi
Pieprasījuma mērķi nodrošina lielāku pieprasījuma izpildes elastību. Izveidojot pieprasījumu, tam var piešķirt kādu no diviem mērķiem: patēriņš vai papildināšana. Atkarībā no pieprasījuma mērķa un organizācijas iestatījumiem pieprasījumu var izpildīt, izmantojot pirkšanas pasūtījumu, pārvietošanas pasūtījumu, ražošanas pasūtījumu vai Kanban darbu.  

Izveidojot jūsu organizācijas pieprasījumu un izmantojot iepirkuma procedūras, var kontrolēt pieejamos pieprasījuma mērķus.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Pieprasījumi, kuru mērķis ir papildināšana

Pieprasījums ar patēriņa mērķi attiecas uz to krājumu vai pakalpojumu vajadzības, kas tiks izmantoti iekšēji jūsu uzņēmumā. Šim mērķim izveidotais pieprasījums vienmēr tiek izpildīts pēc pirkšanas pasūtījuma. Ja programmatūra Supply Chain Management ir iestatīta tā, lai pirkšanas pasūtījumi tiktu izveidoti automātiski, tad pēc pirkšanas pieprasījuma apstiprināšanas tiek izveidoti pirkšanas pasūtījumi.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Pieprasījumi, kuru mērķis ir papildināšana

Pieprasījums ar papildināšanas mērķis attiecas uz vajadzību pēc krājumu papildināšanas. Piemēram, tiek izveidots krājumu papildināšanas pieprasījums tā, lai krājumus varētu pārdot konkrētā mazumtirdzniecības vietā noteiktā laikā. No šāda veida pieprasījuma atkarīgās vajadzības var izpildīt, izmantojot pirkšanas pasūtījumu, pārsūtīšanas pasūtījumu, ražošanas pasūtījumu vai Kanban darbu.  

Ja pieprasījuma mērķis ir papildināšana, pieprasījums tiek izteikts kā daudzums, nevis kā naudas summa. Tādējādi šajā gadījumā netiek veikta apgrūtinājumu uzskaite, budžeta kontrole, uzņēmējtransakcijas nosacījumi pamatlīdzekļu noteikšanai (BRAD — business rules for fixed asset determination), projektu uzskaite un citi saistītie nosacījumi. Papildināšanas pieprasījumu var izpildīt tikai tad, kad izmantojat preces, kas tiek uzkrātas un izsniegtas norādītajai juridiskajai personai. Lai definētu preces, kas ir pieejamas, ja pieprasījuma mērķis ir papildināšana, izmantojiet lapu **Papildināšanas kategorijas piekļuves ierobežojuma nosacījumi**.  

Lai izmantotu pirkšanas pieprasījumus, kuru mērķis ir papildināšana, vispārējā plānošana ir jāiestata tā, lai tajā tiktu iekļautas pieprasījumā iekļautās vajadzības. Pēc tam atkarībā no krājumu piegādes politikas, kas ir noteikta jūsu organizācijā un tiek plānota, izmantojot vispārējo plānošanu, automātiski tiek noteikta šī veida pieprasījuma radīto vajadzību izpildes metode.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Pirkšanas un piedāvājuma pieprasījumi
Dažos gadījumos, lai noteikt preču piegādātāju un cenu, kas ir jāuzrāda pirkšanas pieprasījumā, ir jāuzsāk piedāvājuma pieprasījuma (PP) process. PP procesu var uzsākts, kad pirkšanas pieprasījums atrodas pārskatīšanas procesā. Kad tiek pieņemts piedāvājums, informācija par piegādātāju, cenu utt. tiek pārsūtīta uz pieprasījumu.  

Pirkšanas pieprasījumu var aizturēt, atzīmējot izvēles rūtiņu **Aizturēts** lapā **Pirkšanas pieprasījuma detaļas**. Pirkšanas pieprasījuma apstrādi var turpināt tikai pēc tam, kad aizturēšana ir atcelta, noņemot atzīmi no izvēles rūtiņas.  

> [!NOTE]
> Programmā eProcurement piegādātājiem var tikt dota atļauja jūsu pirkšanas pieprasījuma piedāvājuma pieprasījumā pievienot papildu rindas. Šajā gadījumā pirkšanas pieprasījumā būs redzamas apstiprinātas papildu opcijas.

## <a name="demand-consolidation"></a>Pieprasījuma konsolidācija
Konsolidējot pirkšanas pieprasījuma rindas no vairākiem pirkšanas pieprasījumiem, var nodrošināt jums lielākas iespējas sarunās ar kreditoriem iegūt labāku cenu, zemākas piegādes un pasūtījuma apstrādes izmaksas, ka arī samazinātas pieskaitāmās izmaksas.  

Pirkšanas pieprasījuma rindas ir piemērotas pieprasījuma konsolidācijai tikai tad, ja šādi apgalvojumi ir patiesi:

-   Pirkšanas pieprasījums tika apstiprināts.
-   Pirkšanas pieprasījums atbilst pirkšanas ierobežojumu nosacījumu kritērijiem manuālai apstrādei un pieprasījuma konsolidācijai.

Apstiprinātās pirkšanas pieprasījuma rindas, kas atbilst manuālas apstrādes kritērijiem, ir minētas lapā **Apstiprināto pirkšanas pieprasījumu nodošana izpildei**. Ja pirkšanas pieprasījuma rinda atbilst arī vajadzību konsolidācijas kritērijiem, rindu var pievienot konsolidācijas iespējai.  

Konsolidācijas iespēja ir pirkšanas pieprasījuma rindu kopa, kas ir grupētas tā, lai iepirkumu speciālists var vienoties ar piegādātājiem par labāko darījumu. Konsolidācijas iespējai atlasītās pirkšanas pieprasījuma rindas ir redzamas lapā **Pirkšanas pieprasījuma konsolidēšana**. Ja ir jāveic izmaiņas, rindas var mainīt šajā lapā. Konsolidācijas iespējai var pievienot arī jaunas vai noņemt esošās rindas.  

Kad konsolidācijas iespējai ir pievienotas pieprasījuma rindas un veiktas nepieciešamās izmaiņas, var izveidot konsolidētā pirkšanas pieprasījuma rindu pirkšanas pasūtījumu.  

> [!NOTE]
> Lapā **Pirkšanas pieprasījuma konsolidācija** pirkšanas pieprasījuma rindā veiktās izmaiņas ir redzamas izveidotajā pirkšanas pasūtījumā. Tomēr rinda pirkšanas pieprasījumā netiek mainīta, lai saglabātu tās vēsturi.  

Lai izveidotu to pirkšanas pieprasījuma rindu pirkšanas pasūtījumu, kuras nav piemērotas vajadzību konsolidācijai vai nav atlasītas konsolidācijas iespējai, rindas ir jāapstrādā manuāli.

### <a name="consolidating-purchase-requisition-lines"></a>Pirkšanas pieprasījuma rindu konsolidācija

Vajadzību konsolidācijas process sākas brīdī, kad darbplūsmā tiek apstiprināts pirkšanas pieprasījums un, ja programmā ir konfigurēta jūsu organizācijas budžeta kontrole, kad tiek ierakstītas budžeta rezervācijas un apgrūtinājumi bez juridiskām saistībām. Tālāk norādītajā diagrammā ir attēlota vajadzību konsolidācijas procesa gaita.  

[![Pieprasījuma konsolidācijas procesa plūsma](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Lai konsolidētu apstiprinātās pirkšanas pieprasījuma rindas, rīkojieties šādi:

1.  Pārskatiet apstiprinātās pieprasījuma rindas, kas tika aizturētas manuālai apstrādei un kas ir piemērotas vajadzību konsolidācijai.
2.  Atlasiet konsolidācijas iespējai pievienojamās rindas.
3.  Izveidojiet jaunu konsolidācijas iespēju vai pievienojiet pieprasījuma rindas esošajai konsolidācijas iespējai.
4.  Veiciet pieprasījuma rindās nepieciešamās izmaiņas un dzēsiet pieprasījuma rindu vienumus, kas vairs nav jāiekļauj konsolidācijas iespējā.
5.  Izveidojiet pirkšanas pasūtījumus konsolidētām pieprasījuma rindām vai pirkšanas pieprasījuma rindām konsolidācijas iespējā.


<a name="additional-resources"></a>Papildu resursi
--------

[Patēriņa pieprasījuma izveide](tasks/create-requisition-consumption.md)

[Pirkšanas pieprasījuma darbplūsma](purchase-requisitions-workflow.md)



