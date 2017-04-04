---
title: "SEPA kredīta pārskaitījuma apskats"
description: "Šis raksts sniedz vispārīgu informāciju par ISO 20022 kredīta pārvedumiem, kas ietver vienotu Euro maksājumu telpu (SEPA) pārskaitījumu un citus elektroniskos maksājumus kreditoriem. SEPA kredīta pārskaitījumu ir īpaša veida maksājumu eiro no viena uzņēmuma vai atsevišķu citu uzņēmumu vai individuālo. Rakstā ir arī paskaidrots, kā iestatīt un nosūta kredīta pārskaitījumu maksājuma failu."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>SEPA kredīta pārskaitījuma apskats

Šis raksts sniedz vispārīgu informāciju par ISO 20022 kredīta pārvedumiem, kas ietver vienotu Euro maksājumu telpu (SEPA) pārskaitījumu un citus elektroniskos maksājumus kreditoriem. SEPA kredīta pārskaitījumu ir īpaša veida maksājumu eiro no viena uzņēmuma vai atsevišķu citu uzņēmumu vai individuālo. Rakstā ir arī paskaidrots, kā iestatīt un nosūta kredīta pārskaitījumu maksājuma failu.

## <a name="what-is-a-credit-transfer-message"></a>Kas ir kredīta pārskaitījumu ziņojumu?
Kredītu nodošana ziņa ir pieprasījumu, kuru ierosināšanas partijas (uzņēmuma) nosūta kreditoram pārvietot līdzekļus no sava konta. Pastāv daudzi valstij/reģionam specifiskās un banku specifisko implementācijas pārskaitījuma ziņojumus. Dažas no tām tiek izmantotas vienā valstī/reģionā, un daži kļūst par standartu. Viens labi iekopts globāls standarts ir ISO 20022 un tās uzsākšanu ziņojumus, piemēram, pārskaitījumu. Sekojošajā attēlā redzama attiecības un pārklājuma izvēlēto kredīta pārskaitījumu ziņojumiem. 
![Kredītu tansfer](./media/credit-transfer.jpg) kredīta pārskaitījumu ziņojumus\[/parakstu\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Kas ir ISO 20022 un SEPA maksājumus?
Vienoto eiro maksājumu zonu (Single Euro Payments Area — SEPA) ir izveidojusi Eiropas Komisija, un tā nosaka, ka visi elektroniskie maksājumi tiek uzskatīti par iekšzemes maksājumiem neatkarīgi no privātpersonas, uzņēmuma vai organizācijas un bankas atrašanās valsts/reģiona. Nav nekādas atšķirības starp nacionālo un pārrobežu maksājumus. SEPA ietilpst 28 dalībvalstu Eiropas Savienības (ES) un arī Islandē, Lihtenšteinā, Norvēģijā, Šveicē, Monako un Sanmarīno. SEPA palīdz veidot vienoto maksājumu transakciju tirgus Eiropas Ekonomikas zonā (EEZ). Visbeidzot, paredzams, ka SEPA samazinās maksājumu formātu skaitu, ar kuru ir jāstrādā bankām, uzņēmumiem un privātpersonām. Eiropas Komisija SEPA maksājumiem juridisko pamatu izveidoja ar Maksājumu pakalpojumu direktīvu (Payment Services Directive — PSD). Eiropas Maksājumu padome (European Payments Council — EPC) atbalsta SEPA ar šādām darbībām:

-   Tā nosaka standartus attiecībā uz SEPA elektroniskajiem maksājumiem, izmantojot ISO 20022 universālās finanšu nozares ziņojumu shēmas XML formātu.
-   Tā nosaka noteikumus un vadlīnijas par eiro maksājumu apstrādi.

EPC, kas sastāv no Eiropas bankām, izstrādā komerciālās un tehniskās struktūras SEPA maksāšanas instrumentiem. Tiek izmantoti trīs tipu SEPA maksājumi:

-   Kredīta pārskaitījumi
-   Tiešie debeti
-   Kartes

## <a name="what-is-a-sepa-credit-transfer"></a>Kas ir SEPA kredīta pārskaitījums?
SEPA kredīta pārskaitījums ir viena uzņēmuma vai privātpersonas maksājums citam uzņēmumam vai privātpersonai. Maksājumiem ir jābūt eiro valūtā, un attiecībā uz abām pusēm ir jābūt iekļautam starptautiskajam bankas konta numuram (International Bank Account Number — IBAN) un bankas identifikācijas kodam (Bank Identifier Code — BIC). (BIC tiek dēvēts arī par vispasaules starpbanku finanšu telekomunikāciju sabiedrība \[SWIFT\] kodu.) Turklāt darījuma izmaksas ir jāsadala starp abām pusēm. Starp pusēm veiktajos kredīta pārskaitījumos ir jāizmanto XML faili, kas atbilst ISO 20022 maksājumu apstrādes standartiem un XML formātam, kā noteikusi EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>To, kā tiek ieviesta pārskaitījums?
Eiropas valstu kredīta pārskaitījumu maksājuma formātu tiek īstenota, izmantojot elektroniskās ziņošanas (ER) un maksājuma funkcionalitāti metodes Dynamics 365 operācijām. Dažiem kredīta pārskaitījumu formātiem, kas tiek izmantoti citos reģionos joprojām izmantot mantojums maksājumu ietvaros. Starp daudziem citiem formātiem ir divpadsmit ISO 20022 kredīta pārskaitījumu failu formāti, kuri ir pieejami. Šīs eksporta formāti atbilst SEPA ISO 20022 XML standartam. Tos izmanto, lai ģenerētu-eiro maksājumu pārskaitījumus valstīs/reģionos, kur tie tiek izmantoti un eirozonas maksājumu, kā noteikts 8.2 versiju SEPA Credit Transfer shēmu rokasgrāmatas EPC izlaidumi, kas. Pirms jūs varat īstenot kredīta pārvedumiem, jums jāsazinās ar savu banku, lai iegūtu programmatūru, kas ir nepieciešams, lai augšupielādētu failus elektroniskā banku sistēma. Jūs izmantosiet šo programmatūru pārsūtīt XML faili, kas ietver jūsu bankas maksājuma rīkojumu.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Kāda kredīta pārskaitījumu formātos tiek atbalstītas pašlaik Dynamics 365 operācijām?
Jums vajadzētu vienmēr dodieties uz koplietojamo aktīvu bibliotēku Microsoft Dynamics Lifecycle Services (LCS) un skatītu jaunāko sarakstu pieejams failus, kuriem ir aktīva veida **GER konfigurācijas**. Nākamā sadaļa — "Kas man uzstādīt?", nodrošina saiti uz tēmu, kas izskaidro, kā izveidot LCS repozitoriju, lai pārskatītu pieejamās konfigurācijas un importēt atlasīto konfigurāciju.

## <a name="what-do-i-have-to-set-up"></a>Kas man ir jāiestata?
-   Pirms pārskaitījuma var izveidot failus, vismaz vienu aktīvu kredītu pārsūtīšanas konfigurācijas nedrīkst ievest ER sastāvi. Norādījumus skatiet sadaļā [Download elektroniskās ziņošanas no Lifecycle Services konfigurācijas](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Konfigurējot kontus kreditoru maksāšanas veidiem, atlasiet **Generic elektroniskās ziņošanas** izvēles rūtiņu un izvēlieties attiecīgu kredīta pārskaitījumu formātu (piemēram, **ISO 20022 pārskaitījumu (AT)**) kā eksportēšanas formātu konfigurācija.
-   Ir jāiestata arī juridiskā vienība un bankas konta informācija Dynamics 365 operācijām.
-   Bankas konta numuri IBAN un dažreiz SWIFT kodu (BICs) vai citiem ID ir nepieciešams, lai izveidotu derīgu pārskaitījuma maksājumi. Tādēļ ir jāuzstāda tiem kreditora bankas kontu un bankas konta, organizācija, kura pieprasa nodošanu.
-   Papildu informāciju var pieprasīt, piemēram, pievienotās vērtības nodokļa (PVN) skaitļi attiecībā uz pusēm, kas minētas kredīta pārskaitījumu ziņojumu. Šī informācija ir jāiestata kreditoriem un juridiskajai personai, ja tas tiek pieprasīts.
-   Dažus kontus kreditoru maksāšanas metodēm, pārsvarā ISO 20022 balstītās maksāšanas metodēm, var būt nepieciešamas papildu iestatījumu **maksājuma formātu kodiem**, piemēram, **pakalpojuma veidu** = **SLEV**. Šie kodi tiek izmantoti kā papildu tagu maksājumu darījumiem, maksājumu apstrādes laikā. Noklusētās vērtības maksājumu kodus, piemēram **kategoriju mērķim**, **izmaksu nesēju**, **vietējo instrumentu** un **pakalpojumu līmenis** var iestatīt divās vietās. Pirmajā vietā ir **kontus kreditoru maksājumu žurnāla virsrakstu** un otrais ir **debitoru kreditoru maksājumu metodes**. Pēc maksājumu žurnāla rindas izveide, maksājuma kodu vērtību noteikt maksājumu žurnāla virsraksta tiek pārsūtīta uz žurnāla rindu, ja nav noteikts, izmanto vērtības no maksāšanas veidiem.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Kādi parametri ir pieejami ģenerēšanai kredīta pārskaitījumu maksājumus?
Specifiski parametri saraksts ir atkarīgs no kredīta pārskaitījumu formātā. Nākamā tabula rāda parametrus, kas ir pieejami, kad jūs ģenerēt maksājuma failu ISO 20022 kredītu nodošanu Vācijai kreditoru maksājumu žurnālu. Izmantojot opcijas, kas pieejamas uz **fonā** tab, maksājumu izveidošana var palaist pakešuzdevumu režīmā.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Partijas rezervācija</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai XML failā iekļautu partijas rezervācijas etiķeti.</td>
</tr>
<tr class="even">
<td>Apstrādes datums</td>
<td>Ievadiet datumu, kad bankai vajadzētu apstrādāt maksājumus.</td>
</tr>
<tr class="odd">
<td>Formāts</td>
<td>Atlasiet formātu pārskaitījumu informācijai, atkarībā no jūsu valsts/reģiona vai bankas prasībām:
<ul>
<li><strong>Strd</strong> – atlasiet šo opciju, lai izmantotu strukturētā formātā, kad viena maksājuma rindas tiek nosegta pret vienu rēķinu. Šī opcija nav pieejama valsts/reģiona noteiktu eksporta formāti, Francijā, Vācijā vai Nīderlandē.</li>
<li><strong>Ustrd</strong> — atzīmējiet šo opciju, lai izmantotu nestrukturēto formātu, kad maksājums tiek segts pret vairākiem rēķiniem. Nosegtajiem rēķiniem rēķinu numuri tiek apvienoti un izmantoti kā pārskaitījuma informācija. Saskaņā ar ISO 20022 pamatnostādnes, nestrukturēta pārskaitījuma informācija ir ierobežota līdz 140 rakstzīmēm.</li>
</ul></td>
</tr>
<tr class="even">
<td>Rēķinu skaits</td>
<td>Ievadiet rēķinu skaits šajā <strong>maksājuma dokumentu</strong> atskaite tiek drukāta, no.</td>
</tr>
<tr class="odd">
<td>Sērijas numurs</td>
<td>Ievadiet secības numuru faila identificēšanai. Sērijas numurs ir norādīts uz <strong>apmeklē Piezīme</strong> atskaite.</td>
</tr>
<tr class="even">
<td>Drukāt dalības piezīmi</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai drukātu atskaiti <strong>Dalības piezīme</strong>.</td>
</tr>
<tr class="odd">
<td>Drukāt kontroles pārskatu</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai drukātu atskaiti, kurā ietilpst maksājuma informācija.</td>
</tr>
<tr class="even">
<td>Drukāt pavadvēstuli</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai drukātu atskaiti <strong>Avizo</strong>.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Kas ir IBAN un BIC?
Starptautiskais bankas konta numurs (IBAN) un bankas identifikatora kods (BIC) tiek izmantoti, lai identificētu jebkuru kontu, daudzās valstīs un reģionos visā pasaulē. Tie ietver 34 SEPA valstīm/reģioniem. BIC, ievadiet **SWIFT kods** lauks un IBAN, **IBAN** lauks. Kreditora bankas kontu un klienta bankas kontu, šie lauki atrodas **papildu identifikācijas** FastTab par **bankas konta** cilnē **bankas kontiem** lapā. BIC izmantošanu SEPA maksājumi vairs nav ieviesti.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Kā maksājuma failu nosūtīt uz banku?
Ja maksājumu ģenerēšana, maksājumu fails tiek izveidots un tiek piedāvāts saglabāt to no web pārlūkprogrammas uz jebkuru pieejamo vietu. Nākamais solis ir XML failu nosūtītu uz jūsu bankas. Šis process ir atkarīgs no bankas. Izpildiet savas bankas sniegtās instrukcijas, lai failus iesniegtu apstrādei bankā.


