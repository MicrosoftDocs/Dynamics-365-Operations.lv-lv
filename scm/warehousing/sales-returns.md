---
title: "Pārdošanas ieņēmumi"
description: "Šajā tēmā ir sniegta informācija par atgriešanas pasūtījumu apstrādes procesu. Tajā ir ietverta informācija par debitoru atgriešanām un to ietekmi uz izmaksu aprēķināšanu un rīcībā esošo krājumu daudzumu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 04f8cb1a6375be9371bca2af7e4044392ce7322b
ms.openlocfilehash: 0484723217ccff2ebf717d059429d863ececb797
ms.contentlocale: lv-lv
ms.lasthandoff: 08/02/2017

---

# <a name="sales-returns"></a>Pārdošanas ieņēmumi

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par atgriešanas pasūtījumu apstrādes procesu. Tajā ir ietverta informācija par debitoru atgriešanām un to ietekmi uz izmaksu aprēķināšanu un rīcībā esošo krājumu daudzumu.

Debitori var atgriezt krājumus dažādu iemeslu dēļ. Piemēram, krājums var būt bojāts vai neatbilst debitora prasībām. Atgriešanas pasūtījums sākas, kad debitors iesniedz krājuma atgriešanas pieprasījumu. Pēc debitora pieprasījuma saņemšanas programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek izveidots atgriešanas pasūtījums.

## <a name="return-order-process"></a>Atgriešanas pasūtījuma apstrādes process
Tālāk esošajā attēlā ir sniegts pārskats par atgriešanas pasūtījuma apstrādes procesu.  

[![Atgriešanas pasūtījuma apstrādes process](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Ir pieejami divi atgriešanas pasūtījuma apstrādes procesa veidi: fiziskā atgriešana un tikai kreditēšana.

-   **Fiziskā atgriešana** — ar atgriešanas pasūtījumu tiek autorizēta preces fiziska atgriešana.
-   **Tikai kredītā** — ar atgriešanas pasūtījumu tiek autorizēta debitora kreditēšana, taču debitoram netiek pieprasīta preču fiziska atgriešana.

### <a name="physical-return-order-process"></a>Fiziskās atgriešanas pasūtījumu apstrādes process

1.  **Izveidojiet atgriešanas pasūtījumu.** Oficiāli dokumentējiet debitora autorizāciju atgriezt jebkuras bojātās vai nevajadzīgās preces. Atgriešanas pasūtījums neuzliek uzņēmumam pienākumu pieņemt atgrieztās preces vai nodrošināt debitora kreditēšanu. Ja atgriešana tiek pieņemta, varat autorizēt aizstāšanas krājuma nosūtīšanu pirms bojātā krājuma atgriešanas.
2.  **Ierodieties noliktavā, lai veiktu pārbaudi.** Veiciet sākotnējo pārbaudi un salīdziniet rezultātus ar atgriešanas pasūtījuma dokumentu. Atgriešanas pasūtījums atbalsta arī atgriezto krājumu karantīnu, lai veiktu papildu pārbaudi un kvalitātes kontroli.
3.  **Nosakiet atgriešanas metodi.** Pabeidziet pārbaudes procesu un nolemiet, ko darīt ar atgrieztajām precēm. Šīs darbības ietvaros nolemiet, vai kreditēsiet debitoru, noraidīsiet preces atgriešanu vai pieņemsiet preces atgriešanu, norakstīsiet preci un pēc tam nosūtīsiet debitoram aizstāšanas preci.
4.  **Ģenerējiet pavadzīmi.** Ģenerējiet pavadzīmi un apstipriniet 3. darbības ietvaros pieņemto lēmumu par atgriešanas metodi. Pabeidziet loģistikas procesus.
5.  **Ģenerējiet rēķinu.** Slēdziet atgriešanas pasūtījumu.

### <a name="credit-only-process"></a>Tikai kreditēšanas process

1.  **Izveidojiet atgriešanas pasūtījumu.** Oficiāli dokumentējiet debitora autorizāciju saņemt kredītu, neatgriežot bojātās vai nevajadzīgās preces. Izmantojot atgriešanas metodes kodu **Tikai kredītā**, tiek autorizēts lēmums kreditēt debitoru, nepieprasot fizisku atgriešanu.
2.  **Ģenerējiet rēķinu.** Ģenerējiet kredīta notu un pēc tam slēdziet atgriešanas pasūtījumu.

## <a name="return-material-authorization"></a>Atgrieztā krājuma autorizācija
Atgrieztā krājuma autorizācijas (AKA) apstrādes pamatā ir pārdošanas pasūtījuma funkcionalitāte. AKA tiek reģistrēta kā atgriešanas pasūtījums, kas tiek izveidots kā pārdošanas pasūtījums un var būt saistīts ar citu pārdošanas pasūtījumu, kurš tiek saukts par aizstāšanas pasūtījumu. Abi pārdošanas pasūtījumi ir saistīti ar avota AKA kodu.

-   **Atgriešanas pasūtījums** — lai reģistrētu AKA, tiek izveidots atgriešanas pasūtījums, kas ir pārdošanas pasūtījums, kuram piešķirtais veids ir **Atgrieztais pasūtījums.** Visas AKA informācijas izmaiņas tiek automātiski atjauninātas pārdošanas pasūtījumā. Kamēr atgriešanas pasūtījuma statuss ir **Atvērts**, tas nav redzams pārdošanas pasūtījumu sarakstā. AKA tiek izmantota, lai apstrādātu atgriezto krājumu saņemšanu un ieejas plūsmu, kā arī autorizētu tikai kreditēšanas atgriešanas metodes darbību (skatiet sadaļu **Atgriešanas metožu kodi un atgriešanas metožu darbības**). Visi citi turpmākie procesi ir jāapstrādā pārdošanas pasūtījuma ietvaros.
-   **Aizstāšanas pasūtījums** — ja debitoram ir jānosūta aizstāšanas pasūtījums, AKA var iekļaut otru saistīto pārdošanas pasūtījumu. Varat manuāli izveidot AKA aizstāšanas pasūtījumu, lai nodrošinātu tūlītēju nosūtīšanu. Aizstāšanas pasūtījums var arī tikt izveidots automātiski pēc tam, kad ir pabeigta tāda AKA rindas krājuma saņemšana, pārbaude un ieejas plūsmas darbība, kura atgriešanas metodes kods norāda uz aizstāšanu. Aizstāšanas pasūtījuma funkcionalitāte ir tāda pati kā ar pārdošanas pasūtījumu saistītā funkcionalitāte. Piemēram, varat to izmantot, lai konfigurētu pielāgotas preces kā aizstāšanas krājumu, izveidotu ražošanas pasūtījumu, lai remontētu atgriezto krājumu, izveidotu tiešās piegādes pirkšanas pasūtījumu, lai nosūtītu aizstāšanas krājumu no kreditora vai lai sasniegtu citus mērķus.

## <a name="create-a-return-order"></a>Atgriešanas pasūtījuma izveidošana
Atgriešanas pasūtījuma apstrādes process sākas, kad debitors sazinās ar jūsu organizāciju, lai atgrieztu bojātu vai nevajadzīgu preci un/vai pieprasītu kreditēšanu. Kad jūsu organizācija pieņem atgriešanu, tā tiek dokumentēta atgriešanas pasūtījumā. Šis atgriešanas pasūtījums kļūst par galveno dokumentu, kas tiek izmantots atgrieztās preces iekšējai apstrādei. Tālāk esošajā attēlā ir redzama atgriešanas pasūtījuma izveides procedūra.  

[![Atgriešanas pasūtījuma izveides procedūra](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Atgriešanas pasūtījuma galvenes izveide

Izveidojot atgriešanas pasūtījumu, tajā ir jāietver tālāk esošajā tabulā norādītā informācija.

| Lauks              | Apraksts                                              | Komentāri                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitora konts   | Atsauce uz tabulu Aprēķini                       | Ir jānodrošina esošs debitora konts.                                                                                                                                                                                                                                                                                                  |
| Piegādes adrese   | Adrese, uz kuru tiek atgriezts krājums.                 | Pēc noklusējuma tiek lietota organizācijas adrese. Ja galvenē ir atlasīta noteikta noliktava, piegādes adrese tiek mainīta uz šīs noliktavas piegādes adresi. Šo adresi var mainīt lapā **Atgriezto pasūtījuma informācija**.                                                                                                  |
| Vieta/noliktava     | Vieta vai noliktava, kur tiek saņemta atgrieztā prece | Atgriešanas pasūtījuma piegādes adrese tiek noteikta, pamatojoties uz vietas vai noliktavas piegādes adresi.                                                                                                                                                                                                                                 |
| AKA kods         | Atgriešanas pasūtījumam piešķirtais ID              | AKA kods tiek izmantots kā alternatīva atslēga visa atgriešanas pasūtījuma apstrādes procesa laikā. AKA kods tiek piešķirts, pamatojoties uz AKA koda numuru sēriju , kas ir iestatīta lapā **Debitoru moduļa parametri**.                                                                                                                              |
| Termiņš           | Pēdējais datums, kad var atgriezt krājumu               | Noklusējuma vērtība tiek aprēķināta, pašreizējam datumam pieskaitot derīguma periodu. Piemēram, ja atgriešana ir derīga tikai 90 dienas no atgriešanas pasūtījuma izveides datuma un atgriešanas pasūtījums ir izveidots 1. maijā, laika vērtība ir **30. jūlijs**. Derīguma periodu var iestatīt lapā **Debitoru moduļa parametri**. |
| Atgriešanas iemesla kods | Debitora iemesls preces atgriešanai          | Iemesla kodu var atlasīt lietotāja definētu iemeslu kodu sarakstā. Šo lauku varat atjaunināt jebkurā laikā.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Atgriešanas pasūtījuma rindu izveide

Pēc atgriešanas galvenes pabeigšanas varat izveidot atgriešanas rindas, izvēloties kādu no tālāk norādītajām metodēm.

-   Manuāli ievadiet krājuma informāciju, daudzumu un citu informāciju katrā atgriešanas rindā.
-   Izveidojiet atgriešanas rindu, izmantojot funkciju **Atrast pārdošanas pasūtījumu**. Ir ieteicams atgriešanas pasūtījuma izveides laikā izmantot šo funkciju. Funkcija **Atrast pārdošanas pasūtījumu** nodrošina atsauces izveidi starp atgriešanas rundu un rēķinā iekļauto pārdošanas pasūtījuma rindu un rindas informācijas, piemēram, krājuma numura, daudzuma, cenas, atlaides un izmaksu vērtību, izgūšanu no pārdošanas rindas. Atsauce palīdz nodrošināt, ka tad, kad prece tiek atgrieza uzņēmumam, tās vērtība ir tāda pati kā vienības cena pārdošanas laikā. Atsauce arī nepieļauj atgriešanas pasūtījumu izveidi daudzumam, kas pārsniedz rēķinā norādīto pārdoto daudzumu.

**Piezīme.** Atgriešanas rindas, kurām ir atsauce uz pārdošanas pasūtījumu, tiek apstrādātas kā pārdošanas korekcijas vai atcelšanas. Papildinformāciju skatiet šīs tēmas nākamajā sadaļā “Grāmatošana Virsgrāmatā”.

### <a name="charges"></a>Papildmaksas

Atgriešanas pasūtījumam var pievienot maksas un papildmaksas, izmantojot vienu vai vairākas no tālāk norādītajām metodēm.

-   Varat manuāli pievienot maksas atgriešanas pasūtījuma galvenei, atgriešanas pasūtījuma rindai vai abām.
-   Maksas var tikt automātiski pievienotas atgriešanas pasūtījuma galvenei, izmantojot no atgriešanas iemesla koda atkarīgu funkciju.
-   Maksas var tikt automātiski pievienotas atgriešanas pasūtījuma rindai, pamatojoties uz rindas atgriešanas metodes kodu.

Maksas tiek automātiski pievienotas pēc tam, kad rindai tiek piešķirts atgriešanas iemesla kods vai atgriešanas metodes kods. Ja iemesla kods vēlāk tiek mainīts, esošais maksas ieraksts netiek noņemts, taču var tikt pievienots jauns maksas ieraksts, kas atbilst jaunajam iemesla kodam. Kad pievienojat maksas atgriešanas pasūtījuma rindām, maksas, kas tiek aprēķinātas kā procenti no rindas vai pasūtījuma vērtības, kļūst negatīvas, ja rindas vai rindas pasūtījuma vērtība ir negatīva, ja vien arī procentu vērtība nav negatīva. Maksa ar negatīvu vērtību ir debitoram izmaksājams kredīts.

### <a name="return-reason-codes"></a>Atgriešanas iemeslu kodi

Lietojot iemeslu kodus, varat palīdzēt atvieglot atgriešanas modeļu analīzi. Iemeslu kodi sniedz informāciju par to, kāpēc debitors vēlas atgriezt krājumus. Dažās organizācijās ir daudz iemeslu kodu. Šīs organizācijas var grupēt iemeslu kodus iemeslu kodu grupās, lai nodrošinātu labāku pārskatāmību un varētu izveidot apkopojuma pārskatus.

### <a name="disposition-codes-and-disposition-actions"></a>Atgriešanas metošu kodi un atgriešanas metožu darbības

Svarīga atgriešanas pasūtījuma apstrādes procesa darbība ir atgriešanas metodes koda piešķiršana atgriešanas pasūtījuma rindai saņemšanas reģistrēšanas ietvaros. Atgriešanas metodes kods nosaka tālāk norādīto informāciju.

-   **Finansiālās sekas** — vai debitors ir jākreditē par atgrieztajiem krājumiem, un vai atgriešanas pasūtījuma rinda ir jāpievieno kādas maksas?
-   **Atgrieztā krājuma atgriešanas metode** — vai krājuma vienība ir jāpievieno atpakaļ krājumiem, jānoraksta vai jāatgriež debitoram?
-   **Atgrieztā krājuma loģistika** — vai debitoram ir jāizsniedz aizstāšanas krājums?

Papildus atgriezto preču atgriešanas metodes noteikšanai atgriešanas metožu kodi var izraisīt maksu lietošanu atgriešanas rindām. Tos var izmantot arī atgriešanu grupēšanai statikas datu analīzes nolūkā. Atgriešanas metožu kodi tiek definēti atgriešanas pasūtījumu iestatīšanas ietvaros. Taču katram atgriešanas metodes kodam ir jābūt atsaucei uz kādu no iebūvētajām atgriešanas metožu darbībām. Tālāk esošajā tabulā ir norādīti iebūvētie atgriešanas metožu kodi un to darbības. **Svarīgi!** Ja krājums nav jāatgriež, taču debitors joprojām ir jākreditē, piešķiriet atgriešanas rindai atgriešanas metodes kodu **Tikai kredītā**.

<table>
<thead>
<tr class="header">
<th>Atgriešanas metodes kods</th>
<th>Finansiālās sekas</th>
<th>Ar loģistiku saistītās sekas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tikai kredītā</td>
<td><ul>
<li>Klients tiek kreditēts par summu, kas tiek aprēķināta, no pārdošanas cenas atņemot visas maksas vai papildmaksas.</li>
<li>Virsgrāmatā tiek grāmatoti krājuma norakstīšanas radītie zaudējumi.</li>
</ul></td>
<td>Krājums nav jāatgriež. Šī atgriešanas metodes darbība tiek izmantotā tālāk norādītajos gadījumos.
<ul>
<li>Puses pietiekamā mērā uzticas viena otrai.</li>
<li>Bojātā krājuma atgriešanas izmaksas ir pārāk lielas.</li>
<li>Krājuma vienības nevar pievienot atpakaļ krājumiem. Fiziska atgriešana nav nepieciešama citu apstākļu dēļ.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredītkarte</td>
<td><ul>
<li>Klients tiek kreditēts par summu, kas tiek aprēķināta, no pārdošanas cenas atņemot visas maksas vai papildmaksas.</li>
<li>Krājumu vērtība tiek palielināta par atgrieztā krājuma izmaksām.</li>
</ul></td>
<td>Krājuma vienība tiek atgriezta un pievienota atpakaļ krājumiem.</td>
</tr>
<tr class="odd">
<td>Aizstāt un kreditēt</td>
<td><ul>
<li>Klients tiek kreditēts par summu, kas tiek aprēķināta, no pārdošanas cenas atņemot visas maksas vai papildmaksas.</li>
<li>Krājumu vērtība tiek palielināta par atgrieztā krājuma izmaksām.</li>
<li>Tiek izveidots atsevišķs aizstāšanas pārdošanas pasūtījums, kas tiek apstrādāts atsevišķi.</li>
</ul></td>
<td>Krājuma vienība tiek atgriezta un pievienota atpakaļ krājumiem.</td>
</tr>
<tr class="even">
<td>Aizstāt un izbrāķēt</td>
<td><ul>
<li>Klients tiek kreditēts par summu, kas tiek aprēķināta, no pārdošanas cenas atņemot visas maksas vai papildmaksas.</li>
<li>Virsgrāmatā tiek grāmatoti krājuma norakstīšanas radītie zaudējumi.</li>
<li>Tiek izveidots atsevišķs aizstāšanas pārdošanas pasūtījums, kas tiek apstrādāts atsevišķi.</li>
</ul></td>
<td>Krājums tiek atgriezts un norakstīts.</td>
</tr>
<tr class="odd">
<td>Atgriezt debitoram</td>
<td>Nekas, izņemot jebkuras maksa vai papildmaksas.</td>
<td>Krājums tiek atgriezts, taču pēc pārbaudes tas tiek nosūtīts atpakaļ debitoram. Šo atgriešanas metodes darbību var izmantot, ja krājums ir tīši sabojāts vai ir anulēta garantija.</td>
</tr>
<tr class="even">
<td>Norakstīt</td>
<td><ul>
<li>Klients tiek kreditēts par summu, kas tiek aprēķināta, no pārdošanas cenas atņemot visas maksas vai papildmaksas.</li>
<li>Virsgrāmatā tiek grāmatoti krājuma norakstīšanas radītie zaudējumi.</li>
</ul></td>
<td>Krājums tiek atgriezts vai norakstīts.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Ierašanās noliktavā, lai veiktu pārbaudi
Pirms atgriezto krājumu fiziskas saņemšanas krājumos, grāmatojot pavadzīmi, krājumiem vispirms ir jāveic reģistrācijas un neobligātas pārbaudes process. Tālāk esošajā attēlā ir sniegts pārskats par saņemšanas procesu. Nākamajās sadaļās ir aprakstīta katra attēlā redzamā darbība.  

[![Saņemšanas process](./media/salesreturn03.png)](./media/salesreturn03.png)  

Pastāv vairākas citas šī procesa variācijas, kas nav aprakstītas šajā tēmā. Tālāk ir norādītas dažas no šīm variācijām.

-   Saņemšanas žurnāla izveidei neizmantojiet sarakstu **Saņemšanas darbību apskats**. Tā vietā manuāli izveidojiet saņemšanas žurnālu. Atgriešanas pasūtījumu atsauce ir **pārdošanas pasūtījums**.
-   Ja lietojat moduli Noliktavas vadība, ģenerējiet palešu transportēšanas darbības. Palešu transportēšanas laikā atgriešanas rindas statuss ir **Pienācis**.
-   Reģistrējiet atgrieztā krājuma saņemšanu tiešā veidā no atgriešanas pasūtījuma rindas, izmantojot funkciju **Reģistrācija**.

Saņemšanas procesa laikā atgriešanas tiek integrētas vispārīgajā noliktavā saņemto krājumu apstrādes procesā. Saņemšanas process sniedz iespēju arī izveidot karantīnas pasūtījumus tiem atgrieztajiem krājumiem, kam ir jāveic atsevišķa pārbaude.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identificējiet preces sarakstā Saņemšanas darbību apskats.

Lapā **Saņemšanas darbību apskats** ir norādītas visas ieplānotās saņemšanas. **Piezīme.** Atgriešanas pasūtījumu saņemšanas transakcijas ir jāapstrādā atsevišķi no citu veidu saņemšanas transakcijām. Pēc ienākošā iepakojuma identificēšanas lapā **Saņemšanas darbību apskats** (piemēram, izmantojot pavadošo AKA dokumentu) darbību rūtī noklikšķiniet uz **Sākt saņemšanu**, lai izveidotu un inicializētu saņemšanas žurnālu, kas atbilst saņemšanai.

### <a name="edit-the-arrival-journal"></a>Saņemšanas žurnāla rediģēšana

Iestatot opcijas **Karantīnas pārraudzība** vērtību **Jā**, varat izveidot atgriešanas rindas karantīnas pasūtījumu. Ja rinda ir nosūtīta karantīnā pārbaudes veikšanai, nevarat norādīt atgriešanas metodes kodu. **Piezīme.** Ja krājuma vienības krājumu modeļa grupā iestatāt opcijas **Karantīnas pārraudzība** vērtību **Jā**, saņemšanas žurnāla rindai lapā **Žurnāla rindas** tiek atzīmēta opcija **Karantīnas pārvaldība** un to nevar mainīt. Ja rinda ir nosūtīta karantīnā, ir jānorāda atbilstošā karantīnas noliktava. Ja saņemšanas rinda netiek nosūtīta pārbaudei, noliktavas saņemšanas daļas darbiniekam ir tiešā veidā jānorāda atgriešanas metodes kods saņemšanas žurnāla rindā un pēc tam jāgrāmato saņemšanas žurnāls. Ja visam atgriešanas rindas daudzumam nav jāpiešķir viens atgriešanas metodes kods vai nav saņemts viss rindas daudzums, rinda ir jāsadala. Sadalot saņemšanas žurnāla rindu, tiek sadalīta arī atgriešanas rinda (**SalesLine**) un izveidots jauns partijas ID. Rindu var sadalīt, samazinot saņemšanas žurnāla rindas daudzumu. Grāmatojot žurnālu, atlikušajam daudzumam tiek izveidota jauna atgriešanas rinda ar statusu **Paredzamai**. Rindu var arī sadalīt, noklikšķinot uz **Funkcijas** &gt; **Sadalīt**.

### <a name="process-the-quarantine-order"></a>Karantīnas pasūtījuma apstrāde

Ja atgrieztās preces tiek nosūtītas pārbaudei karantīnas noliktavā, visa papildu apstrāde tiek veikta karantīnas pasūtījumā. Katrai saņemšanas rindai, kas tiek nosūtīta karantīnā, tiek izveidots viens karantīnas pasūtījums. Atgriešanas metodes kods norāda pārbaudes procesa rezultātu. Karantīnas pasūtījumu var sadalīt tādā pašā veidā kā saņemšanas žurnālu. Sadalot karantīnas pasūtījumu, tiek izraisīta atbilstoša atgriešanas rindas sadalīšana. Pēc atgriešanas metodes koda ievades pabeidziet karantīnas pasūtījumu, izmantojot funkciju **Beigt** vai **Ziņot kā pabeigtu**. Ja atlasāt **Ziņot kā pabeigtu**, norādītajā noliktavā tiek izveidota jauna saņemšana. Pēc tam varat apstrādāt šo saņemšanu, izmantojot lapu **Saņemšanas darbību apskats**. Ja saņemšana ir izveidota no karantīnas pasūtījuma, nevarat mainīt pārbaudes laikā piešķirto atgriešanas metodes kodu. Ja pabeidzat karantīnas pasūtījumu, izmantojot funkciju **Beigt**, partija tiek automātiski reģistrēta. Dažreiz krājums var tikt nosūtīts atpakaļ no karantīnas noliktavas uz nosūtīšanas un saņemšanas nodaļu. Piemēram, karantīnas inspektors, iespējams, nezina, kur noliktavā uzglabāt šo krājumu. Šādā gadījumā ir jāatjaunina atbilstošā pavadzīme, lai pareizi reģistrētu karantīnas dēļ norādīto atgriešanas metodes kodu un rīkotos atbilstoši tam. Reģistrējot atgriešanas rindu, debitoram var nosūtīt ieejas plūsmas apstiprinājumu. Pārskats **Atgriešanas apstiprinājums** līdzinās atgriešanas pasūtījuma dokumentam. Pārskats **Atgriešanas apstiprinājums** netiek reģistrēts žurnālā vai citā veidā reģistrēts sistēmā, un tā izveide nav obligāta atgriešanas pasūtījuma apstrādes procesa darbība.

## <a name="replace-a-product"></a>Preces aizstāšana
Preču aizstāšanu var pārvaldīt divos veidos.

-   **Iepriekšēja aizstāšana** — aizstājiet preci pirms atgrieztās preces saņemšanas no debitora.
-   **Aizstāšana pēc atgriešanas metodes koda** — automātiski izveidojiet jaunu aizstāšanas pasūtījuma rindu.

### <a name="up-front-replacement"></a>Priekšpuses aizstāšana

Izmantojot iepriekšējo aizstāšanu, aizstāšanas krājumu var piegādāt debitoram pirms krājuma atgriešanas. Šī metode ir noderīga, piemēram, ja krājums ir iekārtas daļa, ko nevar noņemt, ja vien nav pieejama rezerves daļa tās nomaiņai, vai arī ja vēlaties, lai debitors pēc iespējas ātrāk saņemtu aizstāšanas preci. Iepriekšējās aizstāšanas pasūtījums ir neatkarīgs pārdošanas pasūtījums. Galvenes informācija sākotnēji tiek ņemta no debitora, bet rindas informācija sākotnēji tiek ņemta no atgriešanas pasūtījuma. Aizstāšanas pasūtījumu var rediģēt, apstrādāt un dzēst neatkarīgi no atgriešanas pasūtījuma. Kad dzēšat aizstāšanas pasūtījumu, saņemat ziņojumu par to, ka pasūtījums tika izveidots kā aizstāšanas pasūtījums. Tālāk esošajā attēlā ir redzams iepriekšējas aizstāšanas process.  

![Iepriekšējas aizstāšanas process](./media/SalesReturn04.png)

Atgriešanas pasūtījumā ir ietverta atsauce uz aizstāšanas pasūtījumu. Ja pirms bojātā krājuma atgriešanas tiek izveidots atgriešanas pasūtījuma iepriekšējas aizstāšanas pasūtījums, pēc bojātā krājuma atgriešanas nevarat atlasīt aizstāšanas atgriešanas metodes kodus.

### <a name="replacement-by-disposition-code"></a>Aizstāšana pēc atgriešanas metodes koda

Ja nosūtāt debitoram aizstāšanas krājumu un atgriešanas pasūtījumam izmantojat atgriešanas metodes darbību **Aizstāt un izbrāķēt** vai **Aizstāt un kreditēt**, izmantojiet tālāk esošajā attēlā redzamo procesu.  

![Aizstāšanas process, ja tiek izmantots atgriešanas metodes kods](./media/SalesReturn05.png)

Aizstāšanas krājums tiek piegādāts, izmantojot neatkarīgu pārdošanas pasūtījumu — aizstāšanas pārdošanas pasūtījumu. Šis pārdošanas pasūtījums tiek izveidots atgriešanas pasūtījuma pavadzīmes ģenerēšanas laikā. Pasūtījuma galvenā tiek izmantota informācija no debitora, uz kuru ir atsauce atgriešanas pasūtījuma galvenē. Rindas informācija tiek apkopota no lapā **Krājuma aizstājējs** ievadītās informācijas. Lapā **Krājuma aizstājējs** ir jāievada informācija par rindām, kuru atgriešanas metožu darbību nosaukums sākas ar vārdu “aizstāt”. Taču netiek pārbaudīts vai ierobežots ne aizstāšanas krājuma daudzums, ne tā identitāte. Šī funkcionalitāte ir piemērota gadījumiem, kad debitors vēlas saņemt tā paša krājuma atšķirīgas konfigurācijas vai izmēra variantu vai kad debitors vēlas saņemt pilnīgi citu krājumu. Pēc noklusējuma lapā **Krājuma aizstājējs** tiek ievadīta informācija par tieši tādu pašu krājumu. Taču varat atlasīt citu krājumu, ja vien ir iestatīta šī funkcija. **Piezīme.** Pēc aizstāšanas pārdošanas pasūtījuma izveides varat to rediģēt un dzēst.

## <a name="generate-a-packing-slip"></a>Pavadzīmes ģenerēšana
Lai atgrieztās krājuma vienības varētu saņemt krājumos, vispirms ir jāatjaunina tā pasūtījuma pavadzīme, kurā ir ietvertas šīs krājuma vienības. Tāpat kā rēķina atjaunināšanas process finanšu transakcijas atjaunināšana, pavadzīmes atjaunināšanas process ir fiziska krājumu ieraksta atjaunināšana. Citiem vārdiem sakot, šis process izraisa krājumu izmaiņas. Atgriešanas gadījumā darbības, kas ir piešķirtas atgriešanas metodes darbībai, tiek ieviestas pavadzīmes atjaunināšanas laikā. Kad ģenerējat pavadzīmi, notiek tālāk norādītais.

-   Noliktavā tiek izmantots standarta process, lai veiktu fiziskas ieejas plūsmas darbību. Ja ir atbilstoši iestatīta krājumu modeļu grupa (**Grāmatot fiziskos krājumus**) un debitoru moduļa parametri (**Pavadzīmes grāmatošana Virsgrāmatā**), tiek ģenerēti Virsgrāmatas ieraksti.
-   Krājumi, kas ir atzīmēti ar atgriešanas metodes darbību, kuras nosaukumā ir vārds “izbrāķēt”, tiek norakstīti, un Virsgrāmatā tiek grāmatota krājumu zaudēšana.
-   Krājumi, kas ir atzīmēti ar atgriešanas metodes darbību **Atgriezt debitoram**, tiek saņemti un piegādāti debitoram. Šīs krājuma vienības tieši neietekmē krājumus.
-   Tiek izveidots aizvietošanas pārdošanas pasūtījums. Šis pārdošanas pasūtījums tiek izveidots, pamatojoties uz informāciju lapā **Krājuma aizstājējs**.

Pavadzīmi varat ģenerēt tikai tām rindām, kuru atgriešanas statuss ir **Reģistrēts**, un tikai visam atgriešanas rindas daudzumam. Ja vairākām atgriešanas pasūtījuma rindām ir statuss **Reģistrēts**, varat ģenerēt pavadzīmi rindu apakškopai, dzēšot pārējās rindas no lapas **Grāmatot pavadzīmi**. Daļējas atgriešanas tiek definētas atbilstoši atgriešanas pasūtījuma rindām, nevis atgriešanas pasūtījuma sūtījumiem. Tāpēc, ja saņemat visu vienā atgriešanas pasūtījuma rindā norādīto daudzumu, taču nesaņemat neko no citās atgriešanas pasūtījuma rindās norādītā, piegāde nav daļēja piegāde. Taču, ja atgriešanas pasūtījuma rindā ir norādīts, ka ir jāatgriež 10 krājuma vienības, taču jūs saņemat tikai četras vienības, piegāde ir daļēja piegāde. Ja nav saņemti visi paredzētie atgriešanas krājumi, varat atlikt sūtījuma apstrādi un gaidīt pārējā atgriežamā daudzuma saņemšanu. Varat arī reģistrēt un grāmatot daļēji piegādāto daudzumu. Pavadzīmju grāmatošanas procesa ietvaros debitora nosūtīšanas dokumentos norādīto pavadzīmes atsauces numuru var saistīt ar pasūtījuma rindām. Šī saistīšana nav obligāta un tiek izmantota tikai kā atsauce. Tā neizraisa nekādus transakcijas atjauninājumus. Vispārīgā gadījumā varat izlaist pavadzīmes apstrādes procesu un uzreiz pāriet pie rēķina izrakstīšanas. Šādā gadījumā darbības, ko jūs būtu veicis pavadzīmes ģenerēšanas laikā, tiek veiktas rēķina izrakstīšanas laikā.

## <a name="generate-an-invoice"></a>Ģenerēt rēķinu
Lai gan lapā **Atgriešanas pasūtījums** ir ietverta informācija un darbības, kas ir nepieciešamas, lai apstrādātu atgriešanas pasūtījuma īpašos loģistikas aspektus, rēķina izrakstīšanas procesa pabeigšanai ir jāizmanto lapa **Pārdošanas pasūtījums**. Šādā gadījumā jūsu organizācija var vienlaikus izrakstīt rēķinus par atgriešanas pasūtījumiem un pārdošanas pasūtījumiem un tā pati persona var pabeigt rēķinu izrakstīšanas procesu, ja tas ir nepieciešams. Lai lapā **Pārdošanas pasūtījums** skatītu atgriešanas pasūtījumu, noklikšķiniet uz pārdošanas pasūtījuma numura saites, lai atvērtu saistīto pārdošanas pasūtījumu. Atgriešanas pasūtījumam var piekļūt arī lapā **Visi pārdošanas pasūtījumi**. Atgriešanas pasūtījumi ir pārdošanas pasūtījumi, kuru pasūtījuma veids ir **Atgrieztais pasūtījums**.

### <a name="credit-correction"></a>Kredīta korekcija

Rēķina izrakstīšanas procesa ietvaros pārbaudiet, vai visas papildmaksas ir pareizas. Lai Virsgrāmatas ierakstus padarītu par korekciju (storno), rēķina/kredīta notas grāmatošanas laikā ir ieteicams izmantot opciju **Kredīta korekcija**, kas ir pieejama lapas **Rēķina grāmatošana** cilnē **Cits**. **Piezīme.** Pēc noklusējuma opcija **Kredīta korekcija** ir aktivizēta, ja lapā **Debitoru moduļa parametri** ir iespējota opcija **Kredīta nota kā korekcija**. Taču nav ieteicams grāmatot atgriešanas, izmantojot storno.

## <a name="create-intercompany-return-orders"></a>Starpuzņēmumu atgriešanas pasūtījumu izveide
Atgriešanas pasūtījumus var izpildīt starp diviem uzņēmumiem jūsu organizācijas ietvaros. Tālāk ir norādīti atbalstītie scenāriji.

-   Vienkāršas starpuzņēmumu atgriešanas starp diviem uzņēmumiem, kas piedalās starpuzņēmumu relācijā
-   Starpuzņēmumu ķēde, kas tiek izveidota, kad pārdošanas uzņēmumā tiek izveidots debitora atgriešanas pasūtījums
-   Starpuzņēmumu ķēde, kas tiek izveidota, kad pirkšanas uzņēmumā tiek izveidots kreditora atgriešanas pasūtījums
-   Tiešas piegādes sūtījumu atgriešanas starp ārēju debitoru un diviem uzņēmumiem, kas piedalās starpuzņēmumu relācijā

### <a name="setup"></a>Iestatīšana

Tālāk esošajā attēlā ir redzami minimālie iestatījumi, kas ir nepieciešami, lai divi uzņēmumi varētu piedalīties starpuzņēmumu relācijā un izmanot starpuzņēmumu tirdzniecības iespējas  

![Minimālais uzstādījums](./media/SalesReturn06.png)

Tālāk aprakstītajā scenārijā CompBuy ir pirkšanas uzņēmums un CompSell ir pārdošanas uzņēmums. Parasti pārdošanas uzņēmums nosūta preces pirkšanas uzņēmuma vai tiešās piegādes sūtījuma scenārijos tieši gala debitoram. Uzņēmumā CompBuy kreditors IC\_CompSell ir definēts kā starpuzņēmumu galapunkts, kas ir saistīts ar uzņēmumu CompSell. Vienlaikus uzņēmumā CompSell debitors IC\_CompBuy ir definēts kā starpuzņēmumu galapunkts, kas ir saistīts ar uzņēmumu CompBuy. Abos uzņēmumos ir jābūt definētai atbilstošai darbību politikas informācijai un vērtību kartējumiem. Tiešās piegādes sūtījuma scenārija ietvaros pārdošanas uzņēmumā tiek izveidots starpuzņēmumu atgriešanas pasūtījums, kas ir arī starpuzņēmumu pārdošanas pasūtījums. Starpuzņēmumu atgriešanas pasūtījuma AKA kods var tikt iegūts no AKA koda numuru sērijas uzņēmumā CompSell vai kopēts no AKA koda, kas ir piešķirts sākotnējam atgriešanas pasūtījumam uzņēmumā CompBuy. Šīs darbības ir atkarīgas no darbības politikas **PurchaseRequisition** iestatījuma uzņēmumā CompBuy. Ja AKA kods tiek sinhronizēts, ir jāsagatavojas novērst kodu dublēšanos gadījumā, ja abos uzņēmumos tiek izmantota viena numuru sērija.

### <a name="simple-intercompany-returns"></a>Vienkāršas starpuzņēmumu atgriešanas

Šajā scenārijā ir iesaistīti divi uzņēmumi vienā organizācijā, kā tas ir redzams tālāk esošajā attēlā.  

![Vienkārša starpuzņēmumu atgriešana](./media/SalesReturn07.png)

Pasūtījumu ķēdi var izveidot, ja pirkšanas uzņēmumā tiek izveidots kreditora atgriešanas pasūtījums vai pārdošanas uzņēmumā tiek izveidots debitora atgriešanas pasūtījums. Programmatūra Dynamics 365 for Finance and Operations nodrošina attiecīgā pasūtījuma izvedi otrā uzņēmumā, kā arī to, ka galvenes un rindas informācija kreditora atgriešanas pasūtījumā atbilst iestatījumiem debitora atgriešanas pasūtījumā. Izveidotajā atgriešanas pasūtījumā var tikt ietverta atsauce (**Atrast pārdošanas pasūtījumu**) uz esošu debitora rēķinu, vai arī šī atsauce var tikt izslēgta. Abu pasūtījumu rēķinus un pavadzīmes var apstrādāt atsevišķi. Piemēram, nav nepieciešams ģenerēt kreditora atgriešanas pasūtījuma pavadzīmi pirms debitora atgriešanas pasūtījuma pavadzīmes ģenerēšanas.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Tiešās piegādes sūtījuma atgriešanas starp trim pusēm

Šo scenāriju var īstenot, ja iepriekš ir veikta veida **Tiešā piegāde** pārdošana un uzņēmumā, kas mijiedarbojas ar debitoru, pastāv šim debitoram izrakstīts rēķins. Tālāk esošajā attēlā ir redzams, ka uzņēmums CompBuy iepriekš ir pārdevis rēķinos ietvertas preces debitoram Extern. Preces tika tieši nosūtītas debitoram no uzņēmuma CompSell, izmantojot starpuzņēmumu pasūtījumu ķēdi.  

![Tiešās piegādes sūtījuma atgriešanas starp trim pusēm](./media/SalesReturn08.png)

Ja debitors Extern vēlas atgriezt preces, uzņēmumā CompBuy debitoram tiek izveidots atgriešanas pasūtījums (RMA02). Lai izveidotu starpuzņēmumu ķēdi, atgriešanas pasūtījums ir jāatzīmē tiešajai piegādei. Ja atgriežamā debitora rēķina izvēlei izmantojat funkciju **Atrast pārdošanas pasūtījumu**, tiek izveidota starpuzņēmumu pasūtījumu ķēde, kas sastāv no tālāk norādītajiem dokumentiem.

-   **Sākotnējais atgriešanas pasūtījums:** RMA02 (uzņēmums CompBuy)
-   **Pirkšanas pasūtījums:** PO02 (uzņēmums CompBuy)
-   **Starpuzņēmumu atgriešanas pasūtījums:** RMA\_00032 (uzņēmums CompSell)

Pēc tiešās piegādes starpuzņēmumu ķēdes izveides visas fiziskās darbības ar atgriešanām un to apstrāde ir jāveic uzņēmumā CompSell izveidotā starpuzņēmumu atgriešanas pasūtījuma RMA\_00032 kontekstā. Preces nevar saņemt uzņēmumā CompBuy. Kad starpuzņēmumu atgriešanas pasūtījumam tiek piešķirts atgriešanas metodes kods, tas tiek sinhronizēts ar sākotnējo atgriešanas pasūtījumu, lai nodrošinātu pareizu sākotnējā pasūtījuma rēķina izrakstīšanu.

## <a name="post-to-the-ledger"></a>Grāmatošana Virsgrāmatā
Virsgrāmatas ierakstus, kas tiek ģenerēti atgriešanas pasūtījuma rēķina izrakstīšanas laikā, ietekmē daži svarīgi iestatījumi un parametri.

-   **Vienības izmaksu cena** — krājumu modeļiem, kas nav **Standarta izmaksas**, parametrs **Vienības izmaksu cena** nosaka krājuma vienības izmaksas brīdī, kad tā tiek pieņemta atpakaļ krājumos vai norakstīta. Lai aprēķinātu pareizo krājumu vērtību, ir svarīgi pareizi iestatīt parametru **Vienības izmaksu cena**. Ja izmantojat funkciju **Atrast pārdošanas pasūtījumu**, lai izveidotu atgriešanas pasūtījuma rindu, kurā ir atsauce uz debitora rēķinu, parametra **Vienības izmaksu cena** vērtība ir vienāda ar pārdotā krājuma izmaksu cenu. Pretējā gadījumā izmaksu cenas vērtība tiek iegūta no krājuma iestatījumiem vai to var ievadīt manuāli.
-   **Kredīta korekcijas/Storno** — parametrs **Kredīta korekcija** lapā **Rēķina grāmatošana** nosaka, vai ieraksti ir jāgrāmato kā pozitīvas vērtības (debets/kredīts) vai kā korekcijas ar negatīvu vērtību.

Tālāk sniegtajos piemēros atgrieztās vienības izmaksu cena ir norādīta kā **Krāj. izmaksu cena**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>1. piemērs. Atgriešanas pasūtījumā nav atsauces uz debitora rēķinu

Atgriešanas pasūtījumā nav atsauces uz debitora rēķinu. Atgrieztais krājums tiek kreditēts. Ģenerējot atgriešanas pasūtījuma rēķinu vai kredīta notu, nav atlasīts parametrs **Kredīta korekcija**.  

![Atgriešanas pasūtījumā nav atsauces uz debitora rēķinu](./media/SalesReturn09.png)  

**Piezīme.** Kā parametra **Vienības izmaksu cena** noklusējuma vērtība tiek izmantota krājuma šablona cena. Noklusējuma cena atšķiras no izmaksu cenas krājumu izejas plūsmas laikā. Tāpēc sekas ir 3 naudas vienību zaudējums. Turklāt atgriešanas pasūtījumā nav ietverta atlaide, kas debitoram tika piešķirta pārdošanas pasūtījumā. Tāpēc rodas pārāk liels kredīts.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>2. piemērs. Atgriešanas pasūtījumam ir atlasīts parametrs Kredīta korekcija

2. piemērs ir tāds pats kā 1. piemērs, taču, ģenerējot atgriešanas pasūtījuma rēķinu, ir atlasīts parametrs **Kredīta korekcija**.  

![Atgriešanas pasūtījums, kam ir atlasīts parametrs Kredīta korekcija ](./media/SalesReturn10.png)  

**Piezīme.** Virsgrāmatas ieraksti ir grāmatoti kā korekcijas ar negatīvu vērtību.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>3. piemērs. Atgriešanas pasūtījuma rinda ir izveidota, izmantojot funkciju Atrast pārdošanas pasūtījumu

Šajā piemērā atgriešanas pasūtījuma rinda ir izveidota, izmantojot funkciju **Atrast pārdošanas pasūtījumu**. Veidojot rēķinu, nav atlasīts parametrs **Kredīta korekcija**.  

![Atgriešanas pasūtījuma rinda, kas ir izveidota, izmantojot funkciju Atrast pārdošanas pasūtījumu ](./media/SalesReturn11.png)  

**Piezīme.** Parametri **Atlaide** un **Vienības izmaksu cena** ir iestatīti pareizi. Tāpēc notiek debitora rēķina precīza anulēšana.




