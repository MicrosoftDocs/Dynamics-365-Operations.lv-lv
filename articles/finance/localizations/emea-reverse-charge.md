---
title: PVN/GST shēmas apgrieztās maksāšanas mehānisms
description: Šajā tēmā ir paskaidrots, kā iestatīt apgriezto pievienotās vērtības nodokli (PVN) Eiropas valstīs, Saūda Arābijā un Singapūrā.
author: epodkolz
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 007fab0594c443a3060d6b6640b032ec270f5298
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236249"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>PVN/GST shēmas apgrieztās maksāšanas mehānisms

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta vispārēja pieeja apgrieztās maksāšanas funkcionalitātes iestatīšanai valstīm/reģioniem, kas pieņem PVN vai GST shēmas.
                                                                                 
Valsts/reģiona pieejamību funkcionalitātei pārvalda tālāk norādītie līdzekļi darbvietā **Līdzekļu pārvaldība**.

| Funkcija                                              | Valsts/reģions                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nav raksturīgu līdzekļu                                | Austrija </br>Beļģija </br>Bulgārija </br>Horvātija </br>Kipra </br>Čehijas Republika </br>Dānija  </br>Igaunija  </br>Somija  </br>Francija  </br>Vācija  </br>Ungārija  </br>Islande  </br>Īrija  </br>Itālija  </br>Latvija  </br>Lihtenšteina  </br>Lietuva  </br>Luksemburga  </br>Nīderlande  </br>Norvēģija, Polija </br>Portugāle </br>Rumānija  </br>Saūda Arābija </br>Singapūra  </br>Slovākija  </br>Slovēnija  </br>Spānija  </br>Zviedrija  </br>Šveice  </br>Apvienotā Karaliste  </br>Apvienotie Arābu Emirāti |
| Apgrieztā maksāšana citām valstīm            | Bahreina  </br>Kuveita  </br>Omāna  </br>Katara                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PVN/GST shēmas apgrieztās maksāšanas mehānisma iespējošana | Visas citas valstis/reģioni, izņemot:  </br>Brazīlija  </br>Indija  </br>Krievija                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Lai iegūtu papildu informāciju, skatiet sadaļu [PVN/GST shēmas apgrieztās maksāšanas mehānisma līdzekļa iespējošana](#enable-reverse-charge) tālāk šajā tēmā.

Apgrieztā maksāšana ir nodokļu maksāšanas metode, kuras ietvaros atbildība par PVN uzskaiti un ziņošanu tiek pārnesta no pārdevēja uz preču un/vai pakalpojumu pircēju. Tādējādi preču un/vai pakalpojumu saņēmēji savā PVN deklarācijā ziņo gan par pārdošanas PVN (kā pārdevējs), gan pirkšanas PVN (kā pircējs).

Dažās valstīs vai reģionos apgrieztās maksāšanas metode ir ieviesta tikai dažām precēm un/vai pakalpojumiem un ir noteikti papildu pārdošanas summas nosacījumi vai sliekšņi. Citās valstīs vai reģionos atbildība par PVN maksāšanu ir atkarīga no piegādātāja un pircēja statusa. Ja pircējam ir jāmaksā PVN, tam ir jābūt skaidri norādītam piegādātāja izrakstītajā rēķinā. Piemēram, rēķinā ir jābūt ietvertam tekstam “apgrieztā maksāšana” un norādītām pozīcijām, uz kurām attiecas apgrieztā maksāšana. 

Lai lietotu atgriezto maksāšanu, ir jāveic tālāk norādītie iestatījumi.

## <a name="set-up-sales-tax-codes"></a>Iestatīt PVN kodus
Ir ieteicams pārdošanas un pirkšanas operācijām izmantot atsevišķus PVN kodus.

<table>
<body>
<tr>
<td><strong>Pārdošanas PVN kods</strong></td>
<td>Izveidojiet PVN kodu apgrieztās maksāšanas pārdošanas operācijām (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN kodi</strong>).
</td>
</tr>
<tr>
<td><strong>Pirkšanas PVN kods</strong></td>
<td><p>Izveidojiet pozitīvā un negatīvā PVN kodus pirkšanas apgrieztajam PVN (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN kodi</strong>).</p>
<ol>
<li>Izveidojiet pozitīvas vērtības PVN kodu.</li>
<li>Izveidojiet negatīvas vērtības PVN kodu. Iestatiet opcijas <strong>Atļaut negatīvu PVN likmi</strong> vērtību <strong>Jā</strong>.
Šis negatīvas vērtības PVN kods ir jāpiešķir krājumu PVN grupai, un pēc tam šī krājumu PVN grupa ir jāpiešķir krājumiem, uz kuriem attiecas apgrieztais PVN.</li>
</ol>
<p>Papildinformāciju skatiet nākamajā sadaļā &quot;PVN grupu un krājumu PVN grupu iestatīšana&quot;.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>PVN grupu un krājumu PVN grupu iestatīšana
Ir ieteicams pārdošanas un pirkšanas operācijām izmantot atsevišķas PVN grupas.

<table>
<tr>
<td><strong>Pārdošanas PVN grupas</strong></td>
<td>Izveidojiet PVN grupu apgrieztās maksāšanas pārdošanas operācijām (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN grupas</strong>). Cilnē <strong>Iestatīšana</strong> ietveriet šajā grupā apgrieztās maksāšanas PVN kodu. Atzīmējiet pārdošanas PVN koda izvēles rūtiņas <strong>Neapliekams</strong> un <strong>Atgriezes maksa</strong>.</td>
</tr>
<tr>
<td><strong>Pirkšanas PVN grupas</strong></td>
<td>Izveidojiet PVN grupu apgrieztās maksāšanas pirkšanas operācijām (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN grupas</strong>). Cilnē <strong>Iestatījumi</strong> ietveriet šajā grupā gan pozitīvās, gan negatīvās vērtības PVN kodus. Atzīmējiet negatīvās vērtības PVN koda izvēles rūtiņu <strong>Atgriezes maksa</strong>.</td>
</tr>
<tr>
<td><strong>Krājumu PVN grupas</strong></td>
<td>Izveidojiet vai atjauniniet krājumu PVN grupu, izmantojot negatīvās vērtības PVN kodu (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>Krājumu PVN grupas</strong>). Produktiem un kategorijām, uz kuriem attiecas apgrieztā maksāšana, ir jāpiešķir noklusējuma krājumu PVN grupa.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Apgrieztās maksāšanas krājuma grupu iestatīšana
Lapā **Atgriezes maksas krājumu grupas** (**Nodokļi** &gt; **Iestatīšana** &gt; **PVN** &gt; **Atgriezes maksas krājumu grupas**) varat definēt preču vai pakalpojumu grupas vai atsevišķas preces vai pakalpojumus, uz kuriem var attiecināt apgriezto maksāšanu. Katrai apgrieztās maksāšanas krājumu grupai definējiet pārdošanas un/vai pirkšanas krājumu, krājumu grupu un kategoriju sarakstu.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Apgrieztās maksāšanas kārtulu iestatīšana
Lapā **Atgriezes maksas kārtulas** (**Nodokļi** &gt; **Iestatīšana** &gt; **PVN** &gt; **Atgriezes maksas kārtulas**) varat definēt pirkšanai un pārdošanai lietojamās kārtulas. Varat konfigurēt apgrieztās maksāšanas piemērotības kārtulu kopu. Katrai kārtulai iestatiet tālāk norādītos laukus.

- **Dokumenta tips** – atlasiet **Pirkšanas pasūtījums**, **Kreditoru rēķinu žurnāls**, **Pārdošanas pasūtījums**, **Brīva teksta rēķins**, **Debitoru rēķinu žurnāls** un/vai **Kreditora rēķins**.
- **Partnera valsts/reģiona veids** – Atlasiet **Iekšzemes**, **ES**, **GCC** vai **Ārvalstu**. Ja kārtulu var lietot visiem tirdzniecības partneriem neatkarīgi no partneru adreses valsts vai reģiona, atlasiet opciju **Visi**.
- **Iekšzemes piegādes adrese** – atzīmējiet šo izvēles rūtiņu, lai lietotu kārtulu piegādēm tajā pašā valstī vai reģionā. Šo izvēles rūtiņu nevar atzīmēt, ja ir iestatīts dokumenta tips **Kreditoru rēķinu žurnāls** vai **Debitoru rēķinu žurnāls**.
- **Atgriezes maksas krājumu grupa** – atlasiet grupu, kam var lietot kārtulu.
- **Sliekšņa summa** – apgrieztās maksāšanas metode tiek lietota rēķinam tikai tad, ja apgrieztās maksāšanas krājumu grupā ietverto preču un/vai pakalpojumu vērtība pārsniedz šajā laukā norādīto ierobežojumu.

Varat arī izmantot laukus **Spēkā stāšanās datums** un **Beigu datums**, lai definētu kārtulas darbības periodu.

Varat arī norādīt to, vai gadījumā, ja ir izpildīts dokumenta rindas nosacījums, tiek parādīts paziņojums un šī rinda tiek atjaunināta, izmantojot noklusējuma apgrieztā PVN grupu. Pieejamas šādas opcijas

- **Nav** – dokumenta rinda netiek atjaunināta.
- **Uzvedne** – tiek parādīts paziņojums, lai apstiprinātu, ka var lietot apgriezto maksāšanu.
- **Iestatīt** – dokumenta rinda tiek atjaunināta bez papildu paziņojuma.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Valsts/reģiona rekvizītu iestatīšana
Lapā **Ārējās tirdzniecības parametri** (**Nodokļi** &gt; **Iestatījumi** &gt; **PVN** &gt; **Ārējā tirdzniecība** &gt; **Ārējās tirdzniecības parametri**), cilnē **Valsts/reģiona rekvizīti** iestatiet pašreizējās juridiskās personas valsti/reģionu uz *Iekšzemes*. ES valstīm/reģioniem, kas piedalās ES tirdzniecībā ar pašreizējo juridisko personu, **Valsts/reģiona veids** iestatiet uz *ES*. GCC valstīm/reģioniem, kas piedalās GCC tirdzniecībā ar pašreizējo juridisko personu, **Valsts/reģiona veids** iestatiet uz *ES*.

## <a name="set-up-default-parameters"></a>Noklusējuma parametru iestatīšana
Lai iespējotu funkcionalitāti attiecībā uz apgriezto PVN, lapas **Virsgrāmatas parametri** cilnē **Atgriezes maksa** iestatiet opcijas **Aktivizēt apgriezto maksu** vērtību **Jā**. Laukos **Pirkšanas pasūtījuma PVN grupa** un **Pārdošanas pasūtījuma PVN grupa** atlasiet noklusējuma PVN grupas. Ja ir izpildīts apgrieztās maksāšanas piemērotības nosacījums, pārdošanas vai pirkšanas rinda tiek atjaunināta, izmantojot šīs PVN grupas.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Apgrieztā maksāšana pārdošanas rēķinā
Ja pārdošanai tiek izmantota apgrieztās maksāšanas metode, pārdevējs neiekasē PVN. Tā vietā rēķinā ir norādīti gan krājumi, uz kuriem attiecas apgrieztais PVN, gan apgrieztā PVN kopsumma.

Kad tiek grāmatots pārdošanas rēķins, kurā ir ietverta apgrieztā maksāšana, **PVN transakciju** nodokļa virziens ir maksājamais PVN, tām ir PVN nulles likme un tiek atzīmēti izvēles rūtiņi **Atgriezes maksa** un **Atbrīvots** .

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Apgrieztā maksāšana pirkšanas rēķinā
Ja pirkšanai tiek izmantota apgrieztās maksāšanas metode, pircējs, kurš saņem apgrieztajai maksāšanai paredzēto rēķinu, pilda gan pārdevēja, gan pircēja PVN uzskaites pienākumus.

Kad tiek grāmatots pirkšanas rēķins, kurā ir ietverta apgrieztā maksāšana, tiek izveidotas divas PVN transakcijas. Vienas transakcijas nodokļu virziens ir **Saņemtais PVN**. Otras transakcijas nodokļu virziens ir **Maksājamais PVN**, un tai ir atzīmēta izvēles rūtiņa **Atgriezes maksa**.

Tālāk redzamajā ekrānuzņēmumā vienai transakcijai ir virziens **Saņemtais PVN** un otrai transakcijai — virziens **Maksājamais PVN**. 

![Grāmatotais PVN](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>PVN/GST shēmas apgrieztās maksāšanas mehānisma līdzekļa iespējošana
Darbvietā **Līdzekļa pārvaldība** atrodiet līdzekli un atlasiet **Iespējot**.

Pēc līdzekļa iespējošanas cilne **Apgrieztā maksāšana** ir pieejama visās juridiskajās personās. Iespējojiet apgrieztās maksāšanas funkcionalitāti juridiskai personai, iestatot opciju **Iespējot apgriezto maksāšanu** uz **Jā**.

Būs pieejamas tālāk norādītās lapas un izvēlnes vienumi, kas saistīti ar līdzekļa iestatīšanu.
 - **Apgrieztās maksāšanas krājuma grupas** (**Nodoklis** > **Iestatījumi** > **PVN** > **Apgrieztās maksāšanas krājuma grupas**). Plašāku informāciju skatiet sadaļā [Apgrieztās maksāšanas krājuma grupas iestatīšana](#reverse-charge-item-group).
 - **Apgrieztās maksāšanas kārtulas** (**Nodoklis** > **Iestatījumi** > **PVN** > **Apgrieztās maksāšanas kārtulas**). Skatiet [Apgrieztās maksāšanas kārtulu iestatīšana](#reverse-charge-rules).
 - **Ārējās tirdzniecības parametri** (**Nodoklis** > **Iestatījumi** > **PVN** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**). Skatiet [Valsts/reģiona rekvizītu iestatīšana](#Set-up-Country/region-properties).

Izvēles rūtiņa **Apgrieztā maksāšana** būs pieejama lapās **PVN grupa** un **Grāmatotais PVN**. Lai iegūtu papildu informāciju, skatiet sadaļas [PVN grupu un krājumu PVN grupu iestatīšana](#sales-tax-item-sales-tax-groups), [Apgrieztā maksāšana pārdošanas rēķinā](#reverse-charge-sale) un [Apgrieztā maksāšana pirkšanas rēķinā](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]