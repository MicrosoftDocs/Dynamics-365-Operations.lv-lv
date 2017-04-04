---
title: "Pārdošanas ieņēmumi"
description: "Šajā tēmā ir sniegta informācija par procesu, preču atgriešanas pasūtījumos. Tas ietver informāciju par klientu peļņu, un to ietekme uz pašizmaksas un rīcībā esošo krājumu daudzums."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Pārdošanas ieņēmumi

Šajā tēmā ir sniegta informācija par procesu, preču atgriešanas pasūtījumos. Tas ietver informāciju par klientu peļņu, un to ietekme uz pašizmaksas un rīcībā esošo krājumu daudzums.

Krājumus varat atgriezt klientiem, dažādu iemeslu dēļ. Piemēram, vienums, iespējams, ir bojāts, vai tā var neatbilst klienta cerības. Atgriešanas process sākas tad, kad klients izdod sūtīšanas pieprasījumu atgriezt vienumu. Pēc klienta pieprasījuma tiek saņemts atgriezto preču pasūtījumā tiek izveidota Microsoft Dynamics 365 operācijām.

## <a name="return-order-process"></a>Atgriezto pasūtījumu procesu
Attēlā sniegts pārskats par atgriešanas pasūtījumu procesu.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Pastāv divu veidu preču atgriešanas pasūtījuma procesu: fiziskā atgriešanās un tikai kredītu.

-   **Fizisko atgriešanu** – atgriešanās rīkojumu pilnvaro fizisko produktu atgriešanu.
-   **Tikai kredītu** -pilnvaro klientu kredīta atgriešanas pasūtījumu, bet neprasa, ka klients fiziski nododiet izstrādājumus.

### <a name="physical-return-order-process"></a>Fizisko preču atgriešanas pasūtījuma procesu

1.  **Izveidot preču atgriešanas pasūtījumu.** Formāli dokumentu klientam iespēju atgriezt jebkuru bojāto vai nevēlamu produktu tirdzniecības atļaujas. Atgriezto preču pasūtījums neprasa, ka uzņēmumam pieņemt atpakaļ nodotu produktu vai sniegt kredītu, klientam. Ja atpakaļ tiek pieņemts, var atļaut aizvietojamajai precei jānosūta pirms brāķa krājumu ir atgriezti.
2.  **Nonākt pie noliktavas pārbaudi.** Pabeigtu sākotnējās inspekcijas un validācija pret dokumentu atgriešanas pasūtījumu. Atgriezto preču pasūtījums atbalsta arī papildu pārbaudes un kvalitātes kontroles karantīnas atgrieztās preces.
3.  **Noteiktu izvietojuma.** Pabeigt pārbaudes procesu, un izlemt, kas būtu jādara ar atpakaļ nodotu produktu. Kā daļu no šī soļa, izlemt, vai jums būs kredītiestādes klientam, noraidīt produktu atgriešanas vai pieņemt produktu atgriešanas, brāķa ražojumu un atvietotāju produktu nosūtīšanai klientam.
4.  **Ģenerēt ar pavadzīmi.** Ģenerē pavadzīmju un izdarīt izvietojuma lēmums, ko izdarījis 3 solis. Pabeidziet loģistikas procesus.
5.  **Izveidot rēķinu.** Tuvu atgriezto preču pasūtījumā.

### <a name="credit-only-process"></a>Kredītu tikai procesa

1.  **Izveidot preču atgriešanas pasūtījumu.** Formāli dokumentu klientam saņemt kredītu bez atgriežot bojāto vai nevēlamu produktu tirdzniecības atļaujas. **Kredītu tikai** izvietojuma kodu atļauj kredītiestādes klientam bez fiziskā atgriešanās lēmumu.
2.  **Izveidot rēķinu.** Izveidot kredīta notu, un pēc tam aizveriet atgriezto preču pasūtījumā.

## <a name="return-material-authorization"></a>Atgriezto materiālu autorizācija
Atgriezto materiālu autorizācijas (aka) apstrādes balstās uz pārdošanas pasūtījumu funkcionalitāti. AKA ir reģistrēta kā atgriezto preču pasūtījums, kas ir izveidots kā pārdošanas pasūtījums, un var būt citu pārdošanas pasūtījumu, kas saistīts ar to, sauc par rezerves pasūtījuma. Pārdošanas pasūtījumiem saiti uz izcelsmes RMA numuru.

-   **Atgriezto preču pasūtījums** -reģistrēties aka, veidojot preču atgriešanas pasūtījums, kas ir pārdošanas pasūtījums, kuram ir piešķirts tipa, **atpakaļ pasūtījuma.** Jebkuras izmaiņas, ko veicat RMA informācija tiek automātiski atjauninātas šajā pārdošanas pasūtījumu. Līdz atgriešanas pasūtījumu statuss ir **Open**, tas neparādīsies pārdošanas pasūtījumu sarakstu. Izmantojat RMA rīkoties ar ierašanos un atgriezto preču saņemšanas, kā arī atļaut kredītu vienīgā izvietojuma darbība (sk. sadaļu **izvietojuma kodus un izvietojuma darbības**). Pārdošanas pasūtījums ir jāapstrādā citiem turpmākajiem procesiem.
-   **Nomaiņa pasūtījuma** – kad Nomaiņa pasūtījums ir nosūtīts klientam, RMA var iekļaut otro saistīto pārdošanas pasūtījumu. Varat manuāli veidot Nomaiņa rīkojuma par atbalsta tiešā sūtījuma RMA. Alternatīvi, Nomaiņa pasūtījumu var izveidot automātiski, pēc ierašanās, pārbaudi un pieņemšanas ir pabeigta RMA rindas precei, kas ir izvietojuma kodu, kas norāda Nomaiņa. Nomaiņa pasūtījumam ir tāda pati funkcionalitāte, kas ir saistīts ar pārdošanas pasūtījumu. Piemēram, jūs var izmantot, lai konfigurētu pielāgotus produktu kā aizvietojamajai precei, veidot ražošanas pasūtījumu atgrieztajam krājumam remonts, izveidot tiešo piegādi pirkšanas pasūtījumu nosūtīt Nomaiņa no piegādātāja vai atbalstu citiem mērķiem.

## <a name="create-a-return-order"></a>Atgriešanas pasūtījuma izveidošana
Atgriezto preču pasūtījums process sākas, kad klients sazinās ar uzņēmumā defektīvas vai nevēlamu izstrādājuma atgriešanai un/vai tiktu ieskaitīti. Pēc tam, kad jūsu organizācija pieņem atpakaļ, atgriezties dokumentē preču atgriešanas pasūtījumu. Šo preču atgriešanas pasūtījumu kļūst kontaktpunktu iekšējās apstrādes atgrieztās preces. Sekojošajā attēlā redzama procedūra preču atgriešanas pasūtījuma izveide.  

[![Procedūru preču atgriešanas pasūtījuma izveide](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Izveidot preču atgriešanas pasūtījuma virsrakstā

Veidojot preču atgriešanas pasūtījums, jāiekļauj tabulā norādīto informāciju.

| Lauks              | apraksts                                              | Komentāri                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitora konts   | Atsauce uz tabulu Customers                       | Ir jānorāda esošajam debitora kodam.                                                                                                                                                                                                                                                                                                  |
| Piegādes adrese   | Adrese, kuru priekšmets tiek atdots atpakaļ, lai                 | Pēc noklusējuma, organizācijas adrese tiek izmantota. Ja konkrētai noliktavai ir atlasīta galvene, piegādes adrese tiek mainīta uz piegādes adresi no noliktavas. Varat mainīt šo adresi uz **atgriešanas pasūtījumu detaļas** lapā.                                                                                                  |
| Vieta/noliktavas     | Vietā vai noliktavā, kas saņem atpakaļ nosūtīto preču | Atgriešanas pasūtījumu piegādes adreses ir noteikts, pamatojoties uz piegādes adreses vietā vai noliktavā.                                                                                                                                                                                                                                 |
| AKA kods         | ID, kas tiek piešķirts atgriezto preču pasūtījums              | RMA numurs tiek izmantots kā alternatīvā atslēga preču atgriešanas pasūtījuma procesa gaitā. RMA numuru, kas piešķirts pamatā RMA numuru sēriju, kas iestatīta uz **Accounts receivable parameters** lapā.                                                                                                                              |
| Termiņš           | Pēdējais datums, kurā preces var atgriezt               | Noklusējuma vērtību, tiek aprēķināts kā pašreizējais datums plus derīguma termiņu. Piemēram, ja atgriešanās ir derīgs tikai 90 dienas no datuma, kad atgriešanas pasūtījums tiek veidots, un 1. maijā tika izveidota atgriezto preču pasūtījums, lauka vērtība ir **30 jūlijs**. Derīguma laiks ir iestatīts uz **Accounts receivable parameters** lapā. |
| Atgriešanas iemesla kods | Izstrādājuma atgriešanu klienta iemesls          | Iemesla kodu ir atlasīta lietotāja definētus iemesla kodu sarakstu. Šo lauku var atjaunināt jebkurā brīdī.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Preču atgriešanas pasūtījuma rindu izveide

Pēc pabeigšanas atgriezties galvenes, atgriešanas rindas var izveidot, izmantojot vienu no šādām metodēm:

-   Manuāli ievadītu vienumu detaļas, daudzumu un cita informācija par katru atgriezto rindu.
-   Atgriezto rindu izveide, izmantojot **atrast pārdošanas pasūtījumā** funkciju. Mēs iesakām izmantot šo funkciju izveidojot atgriešanas pasūtījumu. **Atrast pārdošanas pasūtījumā** funkcija nosaka atgrieztās rindas atsauci uz rēķinā pārdošanas pasūtījumu rindas un iegūst rindas detaļas, piemēram, preces numuru, daudzumu, cenu, atlaižu un izmaksu vērtības no pārdošanas rindas. Atskaites palīdz garantēt, ja uzņēmumam tiek atgriezts produkts, tā ir vērtē pašu vienības pašizmaksu tas bija pārdoti. Atsauce arī apstiprina, ka atgriešanas pasūtījumi nav izveidoti par daudzumu, kas pārsniedz daudzumu, kas tika pārdots par rēķinu.

**Piezīme:** atgriešanas rindas, kurās ir atsauce uz pārdošanas pasūtījumu rīkojas kā labojumus vai maiņu par pārdošanu. Lai iegūtu papildinformāciju, skatiet sadaļu "Post Virsgrāmatā", šajā tēmā.

### <a name="charges"></a>Papildmaksas

Maksām un atlīdzību var pievienot preču atgriešanas pasūtījumu, izmantojot vienu vai vairākas no šīm metodēm:

-   Var manuāli pievienot izmaksas preču atgriešanas pasūtījuma virsrakstā, preču atgriešanas pasūtījuma rindas vai abus.
-   Preču atgriešanas pasūtījuma virsrakstā var automātiski pievienot maksu atkarībā no atgriešanas iemesla kodu.
-   Maksājumus var automātiski pievienot atgriešanas pasūtījumu rindai, pamatojoties uz izvietojuma koda rindiņas.

Maksas tiek pievienotas automātiski pēc atgriešanas iemesla kodu vai rindai piešķirtais izvietojuma kodu. Ja iemesla kods ir mainīta vēlāk, esošās maksas ieraksts netiks izņemts, bet varētu pievienot jaunu maksas ierakstu, pamatojoties uz jauno iemesla kodu. Pievienojot maksas atgriešanas pasūtījumu rindas, maksas, kuras tiek aprēķinātas procentos no līnijas vai pasūtījuma vērtība kļūst negatīvs, kad rindu vai rindas kārtībā ir negatīvs, ja vien procents arī ir negatīvs skaitlis. Maksa, kas ir negatīva vērtība atspoguļo kredītu debitoram.

### <a name="return-reason-codes"></a>Atgriešanas iemeslu kodi

Lietojot iemeslu kodus pārskatiem, varat palīdzēt atgriešanās rakstus vieglāk analizēt. Iemesla kodi ir sniegta informācija par kāpēc klients vēlas, lai atgrieztos krājumus. Dažos uzņēmumos ir daudz iemeslu kodus. Šīs organizācijas varētu grupēt iemeslu kodus iemesla kodu grupās, lai gūtu labāku pārskatu un uzkrātā pārskatiem.

### <a name="disposition-codes-and-disposition-actions"></a>Izvietojuma kodus un izvietojuma darbības

Nozīmīgs solis šajā atgriezto preču pasūtījums procesā ir izvietojuma kodu preču atgriešanas pasūtījuma rindā piešķiršanu kā daļa no ierašanās reģistrācijas. Izvietojuma kodu nosaka šādu informāciju:

-   **Finansiālās sekas** – klienta jākreditē atgrieztajiem krājumiem un jebkuri maksājumi jāiekļauj preču atgriešanas pasūtījuma rindas?
-   **Izvietojums atgrieztajam krājumam** -būtu priekšmets var būt pievienota krājumiem, to norakstīšanai vai tas jāatgriež klientam?
-   **Atgrieztā krājuma loģistikas** -aizvietojamajai precei ir jāizsniedz klientam?

Papildus noteikt kā atpakaļ nosūtītas preces iznīcina, izvietojuma kodus var izraisīt maksājumus piemērot atgriešanas rinda. Tās var arī izmantot, lai grupētu atgriež statistisku analīzi. Izvietojuma kodi ir definēti kā daļa no atgriešanas pasūtījumu uzstādīšana. Tomēr katru izvietojuma kodu ir viens no pasākumiem, kas iebūvēts izvietojuma atsauces. Šajā tabulā ir iebūvēts izvietojuma kodi un to darbības. **Svarīgi:** ja vajadzētu atgriezt vienumu, bet klientam joprojām jākreditē, piešķirt **kredītu tikai** izvietojuma kodu atgriezto rindu.

<table>
<thead>
<tr class="header">
<th>Atgriešanas metodes kods</th>
<th>Finansiālās sekas</th>
<th>Ietekme uz loģistikas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tikai kredītā</td>
<td><ul>
<li>Klientam tiek kreditēts pārdošanas cena mīnus jebkuras nodevas vai maksas.</li>
<li>Zaudējumi no nodošanu metāllūžņos krājums tiek grāmatots Virsgrāmatā.</li>
</ul></td>
<td>Vienumu nevar nosūtīt atpakaļ. Šī izvietojuma darbība tiek izmantots šādos gadījumos:
<ul>
<li>Nav pietiekamas uzticēšanās starp pusēm.</li>
<li>Atgriežot bojāto krājumu izmaksas ir aizliedzošas.</li>
<li>Vienumus nevar pieļaut atpakaļ noliktavā. Citu apstākļu dēļ nav nepieciešama fizisko atgriešanu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredītkarte</td>
<td><ul>
<li>Klientam tiek kreditēts pārdošanas cena mīnus jebkuras nodevas vai maksas.</li>
<li>Krājumu vērtība palielinās par atgriezto krājumu izmaksu.</li>
</ul></td>
<td>Vienums tiek atgriezts un pievieno atpakaļ noliktavā.</td>
</tr>
<tr class="odd">
<td>Aizstāt un kreditēt</td>
<td><ul>
<li>Klientam tiek kreditēts pārdošanas cena mīnus jebkuras nodevas vai maksas.</li>
<li>Krājumu vērtība palielinās par atgriezto krājumu izmaksu.</li>
<li>Atsevišķa pārdošanas pasūtījumu Nomaiņa ir izveidota un tiek apstrādāta atsevišķi.</li>
</ul></td>
<td>Vienums tiek atgriezts un pievieno atpakaļ noliktavā.</td>
</tr>
<tr class="even">
<td>Aizstāt un izbrāķēt</td>
<td><ul>
<li>Klientam tiek kreditēts pārdošanas cena, atskaitot jebkuras nodevas vai maksu.</li>
<li>Zaudējumi no nodošanu metāllūžņos krājums tiek grāmatots Virsgrāmatā.</li>
<li>Atsevišķa pārdošanas pasūtījumu Nomaiņa ir izveidota un tiek apstrādāta atsevišķi.</li>
</ul></td>
<td>Krājums ir atgriezies un norakstīts.</td>
</tr>
<tr class="odd">
<td>Atgriezt debitoram</td>
<td>Neviens, izņemot jebkuras nodevas vai maksas.</td>
<td>Vienums tiek atgriezts, bet nosūta atpakaļ klientam pēc pārbaudes. Šo dispozīciju darbību var izmantot, ja vienums ir tīši bojāts vai garantija ir anulēts.</td>
</tr>
<tr class="even">
<td>Norakstīt</td>
<td><ul>
<li>Klientam tiek kreditēts pārdošanas cena mīnus jebkuras nodevas vai maksas.</li>
<li>Zaudējumi no nodošanu metāllūžņos krājums tiek grāmatots Virsgrāmatā.</li>
</ul></td>
<td>Krājums ir atgriezti vai norakstīts.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Pienākšanas noliktavā pārbaudei
Pirms jūs fiziski var saņemt atgrieztās preces noliktavā, grāmatojot pavadzīmi, krājumi ir jāiziet cauri ierašanās reģistrācija un papildu pārbaudi. Attēlā sniegts pārskats par saņemšanas process. Šajās sadaļās aprakstīts katrs solis, kas ir redzams attēlā.  

[![Ierašanās procesu](./media/salesreturn03.png)](./media/salesreturn03.png)  

Procesam ir vairākas variācijas, kas nav iekļauta šajā tēmā. Šeit ir dažas no šīm izmaiņām:

-   Nelietot **ierašanās pārskats** sarakstu, lai izveidotu saņemšanas žurnālā. Tā vietā manuāli izveidot saņemšanas žurnāla. Atgriešanas pasūtījumiem ir **pārdošanas pasūtījumu** atsaucei.
-   Ja lietojat noliktavas vadības, izveidot palešu transportēšanu. Atgrieztās rindas būs statuss **saņemts** palešu transportēšanas laikā.
-   Reģistrējiet ierašanos atgrieztās preces tieši no preču atgriešanas pasūtījuma rindas, izmantojot **reģistrācijas** funkciju.

Ierašanās laikā, atdeve ir integrēti ar vispārējo procesu saņemšana noliktavā. Ierašanās process nodrošina arī karantīnas pasūtījumiem Atgrieztie krājumi, kas jāveic atsevišķa apskate izveide.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identificēt produktu saraksta saņemšanas pārskats

**Ierašanās pārskats** lappusē uzskaitīti plānotie ienākošo iebraucēju. **Piezīme:** iebraucēju no atgriešanas pasūtījumiem ir jāapstrādā atsevišķi no citiem ierašanās darījumu veidiem. Pēc tam, kad esam noteikuši ienākošā pakete par **ierašanās pārskats** lapā (piemēram, izmantojot RMA pavaddokuments), darbību rūtī, noklikšķiniet uz **sākt ierašanās** izveidot un inicializēt saņemšanas žurnālu, kas atbilst ierašanos.

### <a name="edit-the-arrival-journal"></a>Labojiet saņemšanas žurnāla

Iestatot **karantīnas pārvaldība** iespēju **Jā**, jūs varat izveidot karantīnas pasūtījuma atgriešanas rindas. Ja rinda ir tikusi nosūtīta karantīnas inspekcijas, izvietojuma kodu nevar norādīt. **Piezīme:** ja iestatāt **karantīnas pārvaldība** iespēju **Jā**, krājumu modeļu grupā, **karantīnas pārvaldība** opciju uz **žurnāla rindas** lapa tiks atzīmēta žurnāla rindai ierašanās, un to nevar mainīt. Ja rinda tiek nosūtīta karantīnas, jānorāda attiecīgi karantīnas noliktavā. Ja ierašanās rinda nav nosūtīta pārbaudei, noliktavas saņemšanas ierēdnis nedrīkst norādīt izvietojuma kodu tieši no saņemšanas žurnāla rindas un pēc tam Grāmatojiet žurnālu ierašanās. Ja vienu un to pašu kodu izvietojums nav jāpiešķir visu atgriezto rindu daudzuma vai nav saņemts pilns daudzums rindā, nedrīkst sadalīt rindu. Kad jūs sadalīt ierašanās žurnāla rindā, sadalīt arī atgriezto rindu (**Salesline_scrap_more**) un izveidot jaunu partijas ID. Sadalīt rindu, samazinot daudzumu saņemšanas žurnāla rindas. Kad žurnāls ir iegrāmatots, tas ir statuss tiek veidota jauna rinda atgriešanās **sagaidāmajām** attiecībā uz atlikušo daudzumu. Var sadalīt rindu, noklikšķinot uz **funkcijas**&gt;**Split**.

### <a name="process-the-quarantine-order"></a>Karantīnas pasūtījuma apstrādē

Sūtīts atpakaļ nodotu produktu pārbaudei karantīnas noliktavā, karantīnas pasūtījums ir pabeigts jebkādu papildu apstrādi. Vienā karantīnas pasūtījums ir izveidots katrai ierašanās līnijai, kas tiek nosūtīts uz karantīnas. Izvietojuma kodu norāda pārbaudes procesa rezultāts. Karantīnas pasūtījuma, var sadalīt, tāpat, kā varat sadalīt saņemšanas žurnāla. Ja jūs sadaliet karantīnas pasūtījumu, jūs izraisīt atbilstošās atgriezto rindu sadalītu. Pēc tam, kad ir ievadīts kods izvietojuma, pabeigt karantīnas pasūtījuma, izmantojot vai nu **gala** funkciju vai **Pabeigtie** funkciju. Ja atlasāt **Pabeigtie**, jaunpienācēju ir izveidotas norādītajā noliktavā. Tad jūs varat apstrādāt šo ierašanos, izmantojot **ierašanās pārskats** lapā. Ja ierašanās veidojas no karantīnas pasūtījums, veicot pārbaudes piešķirtais izvietojuma kodu nevar mainīt. Ja karantīnas pasūtījums var aizpildīt, izmantojot **gala** funkciju, šī partija tiek reģistrēts automātiski. Dažreiz, vienums varētu nosūtīt atpakaļ no karantīnas nosūtīšanas un saņemšanas departaments. Piemēram, karantīnas inspektors varētu nezināt, kur glabāt preces noliktavā. Šādā gadījumā atbilstošo pavadzīmē ir jāatjaunina, lai pareizi reģistrēt un reaģētu uz norādīto karantīnas dēļ izvietojuma kodu. Saņemšanu var nosūtīt klientam, reģistrējot atgriezto rindu. **Atgriezto apliecinājumu** pārskats atgādina dokumentu atgriešanas pasūtījumu. **Atgriezto apliecinājumu** atskaite nav žurnālā reģistrētās vai citādi reģistrēts sistēmā, un tas nav nepieciešamo preču atgriešanas pasūtījuma procesa solī.

## <a name="replace-a-product"></a>Produkta vietā
Pastāv divas metodes produkta Nomaiņa pārvaldīšanai:

-   **Up-front Nomaiņa** – produkta vietā pirms atgriezto preču saņemšanas no klienta.
-   **Aizstāšana ar izvietojuma kodu** – automātiski izveidotu jaunu pasūtījuma rindu Nomaiņa.

### <a name="up-front-replacement"></a>Priekšpuses aizstāšana

Up-front Nomaiņa aizvietojamajai precei var piegādāt klientam pirms priekšmets tiek atdots atpakaļ. Šī metode ir noderīga, ja, piemēram, preces ir mašīnas daļa, ko nevar noņemt, ja rezerves daļas ir pieejamas ieņemt savu vietu, vai ja jūs vienkārši vēlaties savam klientam ir atvietotāju produktu pēc iespējas ātrāk. Up-front Nomaiņa secība ir neatkarīgas pārdošanas pasūtījumu. Virsrakstu informācija tiek atvērts no klienta un rindas informācija tiek inicializēta no atgriešanas pasūtījumu. Var rediģēt, apstrādāt un dzēst pasūtījumu Nomaiņa, neatkarīgi no preču atgriešanas pasūtījumu. Dzēšot Nomaiņa pasūtījumu, saņemat ziņojumu par rezerves rīkojumu tika izveidots pasūtījums. Sekojošajā attēlā redzama uzreiz nomaiņas process.  

[![Up-front Nomaiņa procesa](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Atgriezto preču pasūtījums ir atsauce uz pasūtījuma Nomaiņa. Ja atgriezto preču pasūtījums tiek izveidots up-front Nomaiņa pasūtījums pirms brāķa priekšmets tiek atdots atpakaļ, nevar atlasīt izvietojuma kodu Nomaiņa pēc bojāto krājumu ir atgriezti.

### <a name="replacement-by-disposition-code"></a>Pēc izvietojuma koda Nomaiņa

Ja aizvietojamajai precei tiek nosūtītas klientam, un izmantot **Replace un lūžņu** vai **Replace un kredīta** izvietojuma rīcības atgriešanas pasūtījumu, izmantojiet to procesu, kurš ir parādīts nākamajā ilustrācijā.  

[![Kad izvietojuma kodu izmanto Nomaiņa procesa](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Aizvietojamajai precei tiks piegādātas, izmantojot neatkarīgas pārdošanas pasūtījuma pārdošanas pasūtījuma Nomaiņa. Šim pārdošanas pasūtījumam ir izveidots ģenerējot pavadzīmes preču atgriešanas pasūtījumu. Pasūtījuma virsraksta informāciju no klienta, uz kuru ir atsauce izmanto preču atgriešanas pasūtījuma virsrakstā. Rindas informācija tiek apkopota informācija, kas ievadīta **aizvietojamajai precei** lapā. **Aizvietojamajai precei** lapa ir jāaizpilda rindām, kam ir atsavināšanas darbības, kas sākas ar vārdu "aizvietot". Tomēr daudzumu, nedz aizvietojamajai precei identitāte ir pārbaudīti vai ierobežots. Šī darbība ļauj gadījumos, ja klients vēlas vienai un tai pašai precei, bet citu konfigurāciju vai lieluma, kā arī gadījumos ja klienti vēlas pilnīgi citu elementu. Pēc noklusējuma tiek ievadīta identiska preču **aizvietojamajai precei** lapā. Taču var atlasīt citu krājumu, ar noteikumu, ka šī funkcija ir iestatīta. **Piezīme:** var rediģēt un dzēst Nomaiņa pārdošanas pasūtījumu pēc tā izveidošanas.

## <a name="generate-a-packing-slip"></a>Ģenerēt ar pavadzīmi
Pirms atgrieztās preces noliktavā var saņemt, jums ir jāatjaunina pasūtījumu, kas pieder preces pavadzīmes. Tāpat, kā rēķinu atjaunināšanas process ir finanšu darbības atjaunināšanu, pavadzīmes atjaunināšanas process ir fiziski grāmatojot krājumu ieraksta. Citiem vārdiem sakot, šajā procesā izdara izmaiņas noliktavā. Attiecībā uz peļņu, tiek īstenoti soļus, kas tiek piešķirti darbībai izvietojuma laikā pavadzīmes atjauninājumu. Ģenerējot pavadzīmes, šādi notikumi:

-   Noliktavā, standarta process tiek izmantots, lai veiktu fiziskās ieejas plūsmas. Tiek ģenerētas Virsgrāmatas grāmatojumus, ja krājumu modeļu grupas (**pastu inventarizācijas**) un Accounts receivable parameters (**Pavadzīmes grāmatošana Virsgrāmatā**) ir iestatīts atbilstoši.
-   Vienumi, kas atzīmēti ar izvietojuma rīcību, kas satur vārdu "brāķi" ir norakstīti un krājumu zaudējumi tiek grāmatots Virsgrāmatā.
-   Vienumi, kas atzīmēti ar **atgriezties pie klienta** izvietojuma rīcību ir saņemti un piegādāti debitoram. Šos vienumus neietekmē neto krājumu.
-   Pārdošanas pasūtījums tiek izveidots rezerves. Šim pārdošanas pasūtījumam ir balstīts uz informāciju par **aizvietojamajai precei** lapā.

Var ģenerēt pavadzīmes tikai rindas, kurās atgriešanas statusu **ierakstītā**, un tikai par pilnu daudzumu atgriešanas rindas. Ja vairākas preču atgriešanas pasūtījuma rindas ir **ierakstītā** statusu, var formēt pavadzīmes rindu apakškopa, izdzēšot rindas no **Pavadzīmes grāmatošana** lapā. Daļēja atgriešanās ir definēti kā atgriezto preču pasūtījumā rindas, nevis kā atgriezto pasūtījumu piegādēm. Tādēļ, ja jūs saņemat pilnu daudzums vienā preču atgriešanas pasūtījuma rindā ir norādīts, bet nekas, saņemot no citas preču atgriešanas pasūtījuma rindas, piegādes nav daļējas piegādes. Tomēr, ja preču atgriešanas pasūtījuma rindas prasa atpakaļ 10 preces vienību, bet jūs saņemat tikai četrām vienībām, piegāde ir daļējas piegādes. Ja ne visu paredzamo atgrieztos krājumus ir ieradušies, var atlikt sūtījumu un gaidīt pārējo atgrieztais daudzums ierasties. Alternatīvi, var reģistrēties un grāmatotu daļēju daudzumu. Procesā pavadzīmes grāmatošanai pavadzīmes atsauces numuru no klienta nosūtīšanas dokumentos var saistīt ar pasūtījuma rindas. Šī asociācija nav obligāta un ir tikai kā atsauce. Tas nerada transakciju atjauninājumi. Vispār, jūs varat izlaist iepakošanas slīdēšanas procesu un doties tieši uz rēķinu izrakstīšanu. Šajā gadījumā darbības, kuras jūs būtu jāizpilda laikā iepakošanas slīdēšanas paaudzes pabeigti rēķinu.

## <a name="generate-an-invoice"></a>Ģenerēt rēķinu
Kaut arī **atgriezto preču pasūtījums** lapa satur informāciju un darbības, kas ir vajadzīgas, lai apstrādātu atgriezto preču pasūtījums, īpašus loģistikas aspekti ir jāizmanto **pārdošanas pasūtījuma** lapu, lai pabeigtu rēķinu izrakstīšanas procesu. Jūsu organizācija var pēc tam rēķina preču atgriešanas pasūtījumi un pārdošanas pasūtījumi, tajā pašā laikā, un viena un tā pati persona var aizpildīt rēķinu izrakstīšanas procesu, kā to prasa. Lai apskatītu atgriešanas pasūtījumu no **pārdošanas pasūtījumu** lapu, noklikšķiniet uz saites, lai atvērtu saistītās pārdošanas pasūtījuma pārdošanas pasūtījuma numuru. Jūs varat arī atrast atgriezto preču pasūtījums **visus pārdošanas pasūtījumus** lapā. Atgriešanas pasūtījumiem ir pasūtījuma tips ir pārdošanas pasūtījumu **atpakaļ pasūtījuma**.

### <a name="credit-correction"></a>Kredīta korekcija

Kā daļu no rēķinā iekļaušanas procesā, pārliecinieties, vai ir pareizi visas papildmaksas. Izraisīt Virsgrāmatas grāmatojumus kļūt korekcijas (Storno), apsveriet iespēju izmantot **kredīta korekciju** opciju uz **citu** cilnē **rēķina grāmatošanas** lapa, grāmatojot rēķinu/kredīta notu. **Piezīme:** pēc noklusējuma **kredīta korekciju** iespēja ir aktivizēta, ja **kredīta notu kā labojumu** opciju uz **Accounts receivable parameters** lapa, ir iespējota. Tomēr mēs iesakām, ka jums nav amatā atgriežas ar Storno.

## <a name="create-intercompany-return-orders"></a>Izveidot starpuzņēmumu atgriezto pasūtījumu
Preču atgriešanas pasūtījumus var izpildīt starp diviem uzņēmumiem, jūsu organizācijā. Tiek atbalstīti šādi scenāriji:

-   Vienkārša starpuzņēmumu atgriež starp diviem uzņēmumiem, kas piedalās starpuzņēmumu attiecības
-   Starpuzņēmumu ķēdē, kas ir noteikta klienta atgriezto pasūtījumu veidojot pārdošanas uzņēmumā
-   Starpuzņēmumu ķēdē, kas tiek izveidota, kad piegādātājam atgriezto preču pasūtījums tiek izveidots pircēja uzņēmumam
-   Tiešās piegādes nosūtīšanas atgriež ārējam debitoram un divi uzņēmumi, kas piedalās starpuzņēmumu attiecības starp

### <a name="setup"></a>Iestatīšana

Attēlā parādīts minimālais uzstādīšanas tas ir nepieciešami divi uzņēmumi starpuzņēmumu attiecības piedalīties un gūt labumu no starpuzņēmumu tirdzniecībai.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Šādā gadījumā CompBuy ir uzņēmums, kas pērk un CompSell ir pārdošanas uzņēmums. Parasti, pārdošanas uzņēmumam kuģiem preces pircēja uzņēmumam vai, tiešās piegādes nosūtīšanas gadījumos tieši līdz gala debitoram. Šajā CompBuy, piegādātāja SU\_CompSell ir definēts kā starpuzņēmumu galapunktam, kas saistīta ar uzņēmuma CompSell. Tajā pašā laikā CompSell, klienta SU\_CompBuy ir definēts kā starpuzņēmumu galapunktam, kas saistīta ar uzņēmuma CompBuy. Abos uzņēmumos ir jānosaka attiecīgas darbības politikas detaļas un vērtību kartēšanas. Tiešās piegādes nosūtīšanas scenārija gadījumā starpuzņēmumu atgriezto pasūtījumu, kas arī ir starpuzņēmumu pārdošanas pasūtījumu, tiek izveidots pārdošanas uzņēmumā. AKA kodu no starpuzņēmumu atgriezto preču pasūtījums var izdot no RMA numuru sērijas, kas CompSell, vai to var nokopēt no RMA numuru, kas piešķirts sākotnējais preču atgriešanas pasūtījums, CompBuy. RMA numuru iestatījumus uz **pirkšanas pieprasījums** CompBuy rīcības politiku nosaka šīs darbības. Ja RMA numurs tiek sinhronizēts, jums vajadzētu plānot numuru sadursmes riska mazināšanai, ja divi uzņēmumi lieto numuru sēriju.

### <a name="simple-intercompany-returns"></a>Vienkārša starpuzņēmumu atgriež

Šis scenārijs ietver divas uzņēmējsabiedrības pašas organizācijas, kā parādīts sekojošajā attēlā.  

[![Vienkārši atgriezties starpuzņēmumu](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Secības ķēdi var tikt izveidota, kad piegādātājam atgriezto preču pasūtījums tiek izveidots pircēja uzņēmumam vai klienta atgriezto preču pasūtījums tiek izveidots, pārdošanas uzņēmumā. Dinamika 365 operācijām veido atbilstošo pasūtījumu citā uzņēmumā, un pārliecinās, ka galvenes un rindu informāciju par kreditora atgriešanas pasūtījumu atspoguļo klienta iestatījumus atgriezto preču pasūtījums. Atgriezto preču pasūtījums, kas ir reģistrēta var vai nu iekļaut vai neiekļaut atsauci (**atrast pārdošanas pasūtījumā**) uz esošo klientu rēķinu. Pavadzīmēm un rēķiniem, divi pasūtījumi var apstrādāt atsevišķi. Piemēram, lai ģenerētu pavadzīmi piegādātājam atgriezto preču pasūtījums pirms jums radīt klienta atgriezto pasūtījumu pavadzīmes nav.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Tiešās piegādes nosūtīšanas atgriež starp trim pusēm

Šis scenārijs var noteikt, ja iepriekšējā pārdošana **tiešu piegādi** tips ir pabeigts un ja pret rēķins klientam pastāv uzņēmumā, kas mijiedarbojas ar klientu. Tālāk redzamajā attēlā uzņēmums CompBuy iepriekš pārdoti un rēķins klientam Extern produktu. Produkti tika nosūtīti tieši no uzņēmuma CompSell klientu caur starpuzņēmumu secības ķēdi.  

[![Tiešās piegādes nosūtīšanas atgriež starp trim pusēm](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Ja Extern klients vēlas, lai atgrieztos produktu, atgriezto preču pasūtījumā (RMA02) ir izveidots klientu uzņēmuma CompBuy. Izveidot starpuzņēmumu ķēdē, atgriezto preču pasūtījumā ir jāmarķē tiešajai piegādei. Izmantojot **atrast pārdošanas pasūtījumā** funkciju izvēlēties atgriezties, debitora rēķina tiek izveidots starpuzņēmumu secības ķēdi, kas sastāv no šādiem dokumentiem:

-   **Oriģinālo preču atgriešanas pasūtījumu:** RMA02 (uzņēmums CompBuy)
-   **Pirkšanas pasūtījumu:** PO02 (uzņēmums CompBuy)
-   **Starpuzņēmumu atgriezto preču pasūtījums:** aka\_00032 (uzņēmuma CompSell)

Pēc tam, kad izveidots starpuzņēmumu tiešās piegādes ķēdē, un apstrādes atgriež fizisko apstrādi saistībā ar starpuzņēmumu atgriezto pasūtījumu RMA jānotiek\_00032 uzņēmuma CompSell. Produktu nevar saņemt uzņēmuma CompBuy. Kad izvietojuma kodu tiek piešķirts starpuzņēmumu atgriezto preču pasūtījums, tas tiek sinhronizēts ar sākotnējo preču atgriešanas pasūtījums, lai ļautu pienācīgi izrakstīšanai no oriģinālā pasūtījuma.

## <a name="post-to-the-ledger"></a>Grāmatošanai Virsgrāmatā
Virsgrāmatas grāmatojumus, kas tiek ģenerēti, kad atgriezto preču pasūtījums ir iekļauts rēķinā, ko ietekmē daži svarīgi iestatījumi un parametri:

-   **Atgriezt pašizmaksu** – par krājumu modeļiem, izņemot **standarta izmaksu**, **atgriezt pašizmaksu** parametrs nosaka krājumu izmaksu, ja tas ir pieņemts atpakaļ noliktavā vai nodod atkritumos. Lai aprēķinātu pareizo krājumu novērtēšanai, ir svarīgi, ka jūs iestatāt **atgriezt pašizmaksu** parametrs pareizi. Ja izmantojat **atrast pārdošanas pasūtījumā** funkcijas, lai izveidotu preču atgriešanas pasūtījuma rindā ir atsauce uz klientu rēķina, **atgriezt pašizmaksu** vērtība ir vienāda ar izmaksu cena krājumam, kas tiek pārdots. Pretējā gadījumā izmaksu cenu vērtības nāk no krājuma iestatījuma vai var ievadīt manuāli.
-   **Kredīta korekciju/Storno** - **kredīta korekciju** parametru par **rēķina grāmatošanas** lappusē nosaka, vai piedāvājumi būtu ierakstītas kā pozitīvs (DR/CR) ierakstus vai labojot, negatīvo ierakstu.

Sekojošie piemēri atgriezto izmaksu cenas tiek uzradīta **Inv izmaksu cenu**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>1. piemērs: Atgriezto preču pasūtījumā nav atsauces debitora rēķina

Atgriezto preču pasūtījums nav atsauces uz klienta rēķina. Atgrieztajam krājumam tiek kreditēts. **Kredīta korekciju** parametrs nav atlasīta, kad preču atgriešanas pasūtījuma rēķina vai kredīta notas tiek ģenerēts.  

[![Atgriezto preču pasūtījums nav atsauces klientu invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Piezīme:** krājuma vispārējās cenu tiek izmantota kā noklusētā vērtība **atgriezt pašizmaksu** parametrs. Noklusētā cena atšķiras no izmaksu cenas krājumu izdošanas laikā. Tādējādi netieši ir sedzis zaudējumus 3. Turklāt, atgriezto preču pasūtījumā neietver atlaides, kas bija veltīta klientu pārdošanas pasūtījumā. Tādēļ rodas pārmērīga kredītu.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>2. piemērs: Atgriezto preču pasūtījums ir atlasīts kredīta korekciju

2. piemērs ir tas pats, piemēram, % 1, bet **kredīta korekciju** ģenerējot rēķina preču atgriešanas pasūtījums ir atlasīts parametrs.  

[![Atgriezto preču pasūtījums, ja ir atlasīts kredīta korekciju](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Piezīme:** Virsgrāmatas grāmatojumus tiek ievadīts kā negatīva labojumus.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>3. piemērs: Atgriešanas pasūtījumu līnija ir izveidota, izmantojot funkcijas Find pārdošanas pasūtījumu

Šajā piemērā atgriešanas pasūtījumu līnija ir izveidota, izmantojot **atrast pārdošanas pasūtījumā** funkciju. **Kredīta korekciju** parametrs nav atlasīts pēc rēķina izveidošanas.  

[![Pasūtījuma rindai, kas izveidots, izmantojot Find pārdošanas pasūtījuma atgriešanas](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Piezīme:****Discount** un **atgriezt pašizmaksu** ir iestatītas pareizi. Tādēļ rodas precīzu atsaukšana debitora rēķina.


