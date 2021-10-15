---
title: SEPA kredīta pārskaitījuma apskats
description: Šajā rakstā ir sniegta vispārīga informācija par ISO 20022 kredīta pārskaitījumiem, kas ietver vienotās eiro maksājumu zonas (SEPA) kredīta pārskaitījumus un citus elektroniskos maksājumus kreditoriem. SEPA kredīta pārskaitījums ir noteikta tipa maksājums (eiro valūtā), ko viens uzņēmums vai privātpersona veic citam uzņēmumam vai privātpersonai. Tēmā ir arī paskaidrots, kā iestatīt un pārsūtīt SEPA kredīta pārskaitījuma maksājuma failu.
author: sunfzam
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bc62f6912433d698024b20e61f54b9a6aea2bbb
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594771"
---
# <a name="sepa-credit-transfer-overview"></a>SEPA kredīta pārskaitījuma apskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta vispārīga informācija par ISO 20022 kredīta pārskaitījumiem, kas ietver vienotās eiro maksājumu zonas (SEPA) kredīta pārskaitījumus un citus elektroniskos maksājumus kreditoriem. SEPA kredīta pārskaitījums ir noteikta tipa maksājums (eiro valūtā), ko viens uzņēmums vai privātpersona veic citam uzņēmumam vai privātpersonai. Tēmā ir arī paskaidrots, kā iestatīt un pārsūtīt SEPA kredīta pārskaitījuma maksājuma failu.

## <a name="what-is-a-credit-transfer-message"></a>Kas ir kredīta pārskaitījuma ziņojums?
Kredīta pārskaitījuma ziņojums ir pieprasījums, kuru iniciējošā puse (jūsu uzņēmums) nosūta, lai pārvietotu līdzekļus no sava konta kreditoram. Pastāv daudzi no valstij/reģionam specifiski un bankai specifiski kredīta pārskaitījuma ziņojumu īstenošanas veidi. Daži no tiem tiek izmantoti vienā valstī/reģionā, un daži kļūst par standartiem. Viens no vispāratzītiem globālajiem standartiem ir ISO 20022 un tā iniciēšanas ziņojumi, piemēram, kredīta pārskaitījums. Šajā ilustrācijā parādītas attiecības un segums noteiktiem kredīta pārskaitījuma ziņojumiem. 
![Kredīta pārskaitījums.](./media/credit-transfer.jpg) Kredīta pārsūtīšanas ziņojumi 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Kas ir ISO 20022 un SEPA maksājumi?
Vienoto eiro maksājumu zonu (Single Euro Payments Area — SEPA) ir izveidojusi Eiropas Komisija, un tā nosaka, ka visi elektroniskie maksājumi tiek uzskatīti par iekšzemes maksājumiem neatkarīgi no privātpersonas, uzņēmuma vai organizācijas un bankas atrašanās valsts/reģiona. Starp nacionālajiem maksājumiem un pārrobežu maksājumiem nav nekādas atšķirības. SEPA ietver 28 Eiropas Savienības (ES) dalībvalstis, kā arī Islandi, Lihtenšteinu, Norvēģiju, Šveici, Monako un Sanmarīno. SEPA palīdz veidot vienoto maksājumu transakciju tirgus Eiropas Ekonomikas zonā (EEZ). Visbeidzot, paredzams, ka SEPA samazinās maksājumu formātu skaitu, ar kuru ir jāstrādā bankām, uzņēmumiem un privātpersonām. Eiropas Komisija SEPA maksājumiem juridisko pamatu izveidoja ar Maksājumu pakalpojumu direktīvu (Payment Services Directive — PSD). Eiropas Maksājumu padome (European Payments Council — EPC) atbalsta SEPA ar šādām darbībām:

-   Tā nosaka standartus attiecībā uz SEPA elektroniskajiem maksājumiem, izmantojot ISO 20022 universālās finanšu nozares ziņojumu shēmas XML formātu.
-   Tā nosaka noteikumus un vadlīnijas par eiro maksājumu apstrādi.

EPC, kas sastāv no Eiropas bankām, izstrādā komerciālās un tehniskās struktūras SEPA maksāšanas instrumentiem. Tiek izmantoti trīs tipu SEPA maksājumi:

-   Kredīta pārskaitījumi
-   Tiešie debeti
-   Kartes

## <a name="what-is-a-sepa-credit-transfer"></a>Kas ir SEPA kredīta pārskaitījums?
SEPA kredīta pārskaitījums ir viena uzņēmuma vai privātpersonas maksājums citam uzņēmumam vai privātpersonai. Maksājumiem ir jābūt eiro valūtā, un attiecībā uz abām pusēm ir jābūt iekļautam starptautiskajam bankas konta numuram (International Bank Account Number — IBAN) un bankas identifikācijas kodam (Bank Identifier Code — BIC). (BIC arī tiek saukts par Pasaules starpbanku finanšu telekomunikāciju sabiedrības \[SWIFT\] kodu.) Turklāt transakcijas izmaksas ir jāsadala starp abām pusēm. Starp pusēm veiktajos kredīta pārskaitījumos ir jāizmanto XML faili, kas atbilst ISO 20022 maksājumu apstrādes standartiem un XML formātam, kā noteikusi EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Kā tiek īstenots kredīta pārskaitījums?
Eiropas valstu kredīta pārskaitījuma maksājuma formāts ir ieviests, izmantojot programmas Microsoft Dynamics 365 Finance elektronisko pārskatu izveides (Electronic reporting — ER) un maksājuma veidu funkcionalitāti. Dažiem kredīta pārskaitījuma formātiem, kuri tiek lietoti citos reģionos, joprojām tiek izmantota mantojuma maksājumu struktūra. Daudzu citu formātu vidū ir pieejami 12 ISO 20022 kredīta pārskaitīšanas failu formāti. Šie eksporta formāti atbilst SEPA ISO 20022 XML standartam. Tie tiek izmantoti, lai izveidotu maksājumu pārsūtīšanas valūtā, kas nav eiro, valstīm/reģioniem, kuros tie tiek izmantoti, un eiro maksājumus atbilstoši EPC izlaistās SEPA kredīta pārskaitījumu shēmas noteikumu rokasgrāmatas versijai 8.2. Lai varētu ieviest kredīta pārskaitījumus, jums ir jāsazinās ar savu banku, lai iegūtu programmatūru, kas ir nepieciešama elektronisko banku operāciju failu augšupielādēšanai. Šo programmatūru jūs izmantosit, lai pārsūtītu XML failus, kas ietver maksājumu uzdevumus uz jūsu banku.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Kādi kredīta pārskaitījuma formāti pašlaik tiek atbalstīti?
Vienmēr atveriet koplietojamo līdzekļu bibliotēku portālā Microsoft Dynamics Lifecycle Services (LCS) un skatiet jaunāko to pieejamo failu sarakstu, kuru pamatlīdzekļa tips ir **GER konfigurācija**. Nākamajā sadaļā “Kas man ir jāiestata?” ir norādīta saite uz tēmu, kurā paskaidrots, kā izveidot LCS repozitoriju, lai pārskatītu pieejamās konfigurācijas un importētu atlasītās konfigurācijas.

## <a name="what-do-i-have-to-set-up"></a>Kas man ir jāiestata?
-   Lai varētu izveidot kredīta pārskaitījumu failus, jūsu ER konfigurācijās ir nepieciešams importēt vismaz vienu aktīvu kredīta pārskaitījuma konfigurāciju. Norādījumus skatiet sadaļā [Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Kad konfigurējat kreditoru maksājuma metodes, atzīmējiet izvēles rūtiņu **Vispārīga elektronisko atskaišu veidošana** un atlasiet atbilstošo kredīta pārskaitījuma formātu (piemēram, **ISO 20022 kredīta pārskaitījums (AT)**) kā eksporta formāta konfigurāciju.
-   Jums ir arī jāiestata juridiskās personas un bankas konta informācija.
-   Lai izveidotu derīgus kredīta pārsūtīšanas maksājumus, ir nepieciešami bankas kontu numuri, IBAN un dažreiz SWIFT kodi (BIC) vai citi identifikatori. Tādēļ jums tie ir jāiestata gan kreditora bankas kontam, gan bankas kontam tai organizācijai, kas pieprasa pārskaitījumu.
-   Var būt nepieciešama papildinformācija, piemēram, pievienotās vērtības nodokļa (PVN) maksātāja numurs pusēm, kuras ir minētas kredīta pārskaitījuma ziņojumā. Šī informācija jāiestata kreditoriem un juridiskajai personai pēc pieprasījuma.
-   Dažām kreditoru maksājuma metodēm, parasti maksājuma metodēm, kas balstās uz ISO 20022, var būt nepieciešama papildu iestatīšana vienumam **Maksājuma formāta kodu kopas**, piemēram, **Pakalpojuma veids** = **SLEV**. Šie kodi tiek izmantoti kā papildu etiķetes maksājumu darījumiem maksājumu apstrādes laikā. Maksājuma kodu noklusējuma vērtības, piemēram, **Kategorijas nolūks**, **Maksas uzrādītājs**, **Lokālais instruments** un **Pakalpojumu līmenis**, var iestatīt divās vietās. Pirmā vieta ir **Kreditoru maksājumu žurnāla virsraksts**, un otrā — **Kreditoru maksājumu metodes**. Pēc maksājumu žurnāla rindu izveides maksājuma kodu vērtības, kas iestatītas maksājumu žurnāla virsrakstā, tiek pārvietotas uz žurnāla rindu; ja tās nav iestatītas, tiek izmantotas vērtības no sadaļas Maksājumu metodes.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Kādi parametri ir pieejami kredīta pārskaitījumu maksājumu ģenerēšanai?
Noteiktu parametru saraksts ir atkarīgs no kredīta pārskaitījuma formāta. Nākamajā tabulā parādīti parametri, kuri ir pieejami, kad kreditoru maksājumu žurnālā ģenerējat ISO 20022 kredīta pārskaitījuma maksājuma failu Vācijai. Izmantojot cilnē **Palaist fonā** pieejamās opcijas, maksājuma ģenerēšanu varat palaist pakešapstrādes režīmā.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
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
<li><strong>Strd</strong> — atlasiet šo opciju, lai izmantotu strukturēto formātu, kad viena maksājuma rinda tiek segta pret vienu rēķinu. Šī opcija na&#39;v pieejama Francijas, Vācijas un Nīderlandes valstij/reģionam raksturīgajiem eksporta formātiem.</li>
<li><strong>Ustrd</strong> — atzīmējiet šo opciju, lai izmantotu nestrukturēto formātu, kad maksājums tiek segts pret vairākiem rēķiniem. Nosegtajiem rēķiniem rēķinu numuri tiek apvienoti un izmantoti kā pārskaitījuma informācija. Saskaņā ar ISO 20022 vadlīnijām nestrukturētā pārskaitījumu informācija ir ierobežota līdz 140 rakstzīmēm.</li>
</ul></td>
</tr>
<tr class="even">
<td>Rēķinu skaits</td>
<td>Ievadiet rēķinu skaitu, no kāda tiek drukāts pārskats <strong>Avizo</strong>.</td>
</tr>
<tr class="odd">
<td>Sērijas numurs</td>
<td>Ievadiet secības numuru faila identificēšanai. Secības numurs tiek rādīts atskaitē <strong>Dalības piezīme</strong>.</td>
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
Starptautiskais bankas konta numurs (IBAN) un bankas identifikācijas kods (BIC) tiek izmantots, lai identificētu jebkuru kontu daudzās valstīs/reģionos visā pasaulē. Tie ietver 34 SEPA valstis/reģionus. Ievadiet BIC laukā **SWIFT kods** un IBAN laukā **IBAN**. Gan kreditora bankas kontam, gan debitora bankas kontam šie lauki atrodas kopsavilkuma cilnē **Papildu identifikācija**, cilnē **Bankas konts**, lapā **Banku konti**. BIC izmantošana SEPA maksājumiem vairs nav obligāta.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Kā maksājuma failu nosūtīt uz banku?
Kad ģenerējat maksājumus, tiek ģenerēts maksājuma fails, un jums tiek lūgts no tīmekļa pārlūkprogrammas to saglabāt jebkurā pieejamā vietā. Nākamā darbība ir XML faila sūtīšana uz jūsu banku. Šis process ir atkarīgs no bankas. Izpildiet savas bankas sniegtās instrukcijas, lai failus iesniegtu apstrādei bankā.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
