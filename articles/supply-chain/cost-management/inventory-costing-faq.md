---
title: Bieži uzdotie jautājumi par krājumu izmaksu uzskaiti
description: Šī tēma atbild uz dažiem bieži uzdotiem jautājumiem par krājumu izmaksu ēšanu Microsoft sistēmā Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809305"
---
# <a name="inventory-costing-faq"></a>Bieži uzdotie jautājumi par krājumu izmaksu uzskaiti

[!include [banner](../includes/banner.md)]

Šī tēma atbild uz dažiem bieži uzdotiem jautājumiem par krājumu izmaksu ēšanu Microsoft sistēmā Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Krājumu slēgšana, koriģēšana un pārrēķins

### <a name="is-the-inventory-close-required"></a>Vai ir nepieciešama krājumu slēgšana?

Ja plānojat izmantot krājumu arhivēšanas līdzekli, ir nepieciešama krājumu slēgšana. Ja neplānosit izmantot krājumu arhivēšanas līdzekli, ir ļoti ieteicams joprojām palaist krājumu slēgšanu neatkarīgi no izmantotajiem izmaksu modeļiem.

### <a name="how-often-should-the-inventory-close-be-run"></a>Cik bieži jāveic krājumu slēgšana?

Krājumu slēgšana jāveic vismaz vienu reizi virsgrāmatas periodā. Piemēram, ja virsgrāmata ir iestatīta uz kalendāro mēnesi balstītu finanšu kalendāru, jums ir jāpalaiž krājumu slēgšana vienu reizi mēnesī.

### <a name="is-the-inventory-recalculation-required"></a>Vai krājumu pārrēķins ir nepieciešams?

Nē, krājumu pārrēķins nav nepieciešams. Ja izmantojat periodisko izmaksu aprēķināšanas modeli, piemēram, "pirmais ārā" (first in, first out – FIFO), "pēdējais ārā" (LIFO) vai svērto vidējo, rūpīgi apsveriet, vai krājumu pārrēķināšana tiks veikta. Tā var nodrošināt precīzāku izmaksu ēšanu jūsu atlasītos heiristikas modeļos.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Cik bieži jāpalaiž krājumu pārrēķins?

Ja plānojat darbināt krājumu pārrēķinu, ieteicams to lietot katru dienu kā pakešuzdevumu. Ja jūsu organizācijai nepieprasa biežu krājumu vērtību pārskatu sniegšanu periodiskiem izmaksu modeļiem, varat inventarizācijas aprēķinu veikt mazāk bieži.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Kad lapā Slēgšana un pielāgojumi jāizmanto rīcībā esošo krājumu korekcija?

Rīcībā esošo krājumu korekciju var veikt tikai pēc krājumu slēgšanas pabeigšanas. Parasti tas tiek palaists datumā pēc pēdējās slēgšanas. Rīcībā esošo krājumu koriģēšana var koriģēt tikai tos krājumus, kas vēl ir rīcībā no datuma, kad palaižat korekciju.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Kad jāizmanto krājumu darbību korekcija lapā Slēgšana un Pielāgojumi?

Pirms krājuma slēgšanas jums jāizmanto krājumu darbību koriģēšana. Parasti tas tiek izmantots nepareizas kvīts labošanai. Krājumu darbības korekciju nevar grāmatot pēc krājumu slēgšanas un pēc tam, kad darbība ir nosegta.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Vai pirkšanas pasūtījuma atgriešanas tiek apstrādātas kā citas izejas plūsmas krājumu slēgšanas laikā?

Jā. Pirkšanas pasūtījuma saņemšana ir izdošana, kas tiek segta ar ieejas plūsmu krājumam atlasītajā heiristiskā modelī. Ja izmantojat periodisko izmaksu aprēķināšanas modeli, varat izmantot iezīmēšanu, lai ignorētu heiristisko izmaksu.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Kas tiek darīts ar pārdošanas pasūtījumu atgriešanu krājumu slēgšanas laikā?

Kad jūs palaidiet krājumu slēgšanu, pārdošanas pasūtījuma atgriešana tiek apstrādāta kā saņemšana noliktavā. Izejas plūsmas tiek nosegtas pret krājumiem, balstoties uz krājumam izvēlēto heiristisko modeli.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Kāda izmaksu cena tiek izmantota pārdošanas pasūtījuma atgriešanai?

Kad izveidojat atgriešanu, kas ir saistīta ar pārdošanas pasūtījumu, **vienības** cenas lauka vērtība tiek kopēta no oriģinālā pārdošanas pasūtījuma, un atgriešanas izmaksu cenas lauks atgrieztajā laukā tiek iestatīts uz koriģēto izmaksu cenu no oriģinālās krājumu cenas darbības pārdošanas pasūtījuma rindai, **kas** tiek atgriezta. Ja saistītās **krājumu darbības** opcijas *Vērtība* ir iestatīta uz Jā, krājumu slēgšana var radīt sākotnējā pārdošanas pasūtījuma izdošanas izmaksu atjauninājumus. Šajā **scenārijā atgriešanas** izmaksu cenas lauks nav atjaunināts. Tomēr, kad jūs iegrāmatosiet atgriešanas pasūtījuma pavadzīmi, sistēma pārbauda izmaksu cenu un izmantos atjauninātās izmaksas atgriešanas krājuma darbībā.

Standarta izmaksu krājumam, kas ir saistīts ar pārdošanas pasūtījumu, atgriešanai sistēma izmantos standarta izmaksas no oriģinālā pārdošanas pasūtījuma laika, pat ja krājumam ir aktīvas jaunas standarta izmaksas.

Kad izveidojat atgriešanu, kas nav saistīta ar pārdošanas pasūtījumu, **lauks** Atgrieztā izmaksu cena tiek iestatīts uz aktīvo krājuma cenu, kas jums ir krājumam vietā, kam tiek izveidots atgriešanas pasūtījums. Ja krājuma izmaksu versijā jums nav aktīvas izmaksu cenas, vērtība būs 0 (nulle). Ja atstāsiet vērtību kā 0 (nulli), saņemsit brīdinājumu, ka nav norādīts atgrieztā laidiena ID vai atgrieztās izmaksu cena.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Kāda ir paredzamā krājumu slēgšanas veiktspēja?

Daudzi faktori var ietekmēt krājumu slēgšanas veiktspēju. Šie faktori ietver kopējo krājumu skaitu, kopējo darbību skaitu periodā, jūsu lietotos krājumu modeļus un pakešuzdevumu palīgu skaitu, ko konfigurējat krājumu un noliktavas vadības parametros. Varat gaidīt, ka slēgšana var ilgt cik minūtes vai cik daudz stundu. Nav īpašu ieteikumu par slēgšanas laiku, kas nepieciešams, lai palaistu. Jums vajadzētu noteikt jūsu nestandarta biznesa prasības krājumu slēgšanas veiktspējai un strādāt cieši ar savu partneri, lai noteiktu grafiku krājumu slēgšanas procesa darbinā anai. Ja rodas neparedzēti zema krājumu slēgšanas procesa veiktspēja, jums ir jāatver atbalsta biļete.

## <a name="costing-sheet-and-indirect-costs"></a>Izmaksu aprēķina lapa un netiešās izmaksas

### <a name="which-costing-models-support-the-costing-sheet"></a>Kuri izmaksu aprēķināšanas modeļi atbalsta šo izmaksu aprēķina lapu?

Kaut arī izmaksu aprēķina lapa parasti tiek izmantota uzņēmumos, kas izmanto standarta izmaksu aprēķināšanas metodi, varat to izmantot ar jebkuru izmaksu modeli, kas ir pieejams Piegādes ķēdes pārvaldībā.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Vai man ir vairākas izmaksu aprēķināšanas lapas dažādām manas organizācijas daļām?

Nē. Katrai juridiskajai personai var būt tikai viena aprēķina lapa.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Vai katrai vietai var būt dažādas izmaksu aprēķināšanas lapas?

Nē, katrai vietai nevar būt atšķirīga izmaksu aprēķina lapa. Katrai juridiskajai personai var izveidot tikai vienu aprēķina lapu. Tomēr ir iespējams konfigurēt kopējos mezglus, izmaksu grupas vai netiešo izmaksu mezglus vienai vietai. Šī konfigurācija ir manuāls process, un, ja notiek organizatoriskās vai darbības izmaiņas, hierarhiju un krājumu piešķires izmaksu aprēķina lapā ir jāsaglabā. Ja viens krājums tiek ražots vai pirkts vairāk nekā vienā vietā, nav mehānisma, kas ļauj jums apstrādāt krājumu citādi katras vietas izmaksu aprēķina lapā. Turklāt ievērojiet, ka visiem netiešo izmaksu kodiem ir likme vai piemaksa, kas ir noteikta izmaksu versijā. Jūsu definētās izmaksas vienmēr ir vietas raksturīgās.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Vai izmaksu aprēķināšanas lapas versijas var deaktivizēt un aktivizēt?

Lai gan izmaksu aprēķina lapai nav saglabāta detalizēta versiju vēsture, varat veikt izmaiņas izmaksu aprēķina lapā un pēc tam, kad esat gatavs, saglabāt un apstiprināt to. Nav mehānisma, kas ietu atpakaļ uz vecāku izmaksu aprēķina lapas versiju vai apskatītu izmaiņas, kas tika veiktas izmaksu aprēķina lapā. Ja sākat izmaiņas un nevēlaties, lai tās stātos spēkā, lapu varat aizvērt, nesaglabājot un validējot izmaiņas. Jums tiks piedāvāts atmest izmaiņas.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Vai katram krājumam var izveidot netiešās izmaksas?

Izmaksu aprēķina lapā varat izveidot netiešo **izmaksu** *kodus, kuru zara tipa lauks ir iestatīts uz Piemaksa*, *Likme* vai *Izvades vienība.* Pēc tam varat definēt likmi vai piemaksas tā, lai tā būtu raksturīga krājuma numuram. Kopsavilkuma cilnē **Likme** **vai** Piemaksa pievienojiet režģim rindu. Laukam **Derīgs** iestatiet vērtību *Tabula* un Saite **lauku** uz noteiktu krājuma kodu.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Vai var izveidot netiešās izmaksas, kas nav saistītas ar noteiktu krājumu?

Jā. Var izveidot netiešo izmaksu kodu, kur zara tipa lauks **ir** iestatīts *uz izvades vienību*. Pēc tam apakštipa **lauku** *var* iestatīt uz Daudzums, *·* *Svars* vai Tilpums, lai norādītu krājumu daudzumu, svaru vai apjomu, ko ražojiet. Likme, kuru norādāt likmes **kopsavilkuma** cilnē, tiks piemērota atlasītajam apakštipam. Piemēram, jūs **iestatāt** *·* **·** *apakštipa lauku uz Daudzums un Likme lauku uz 1,00 USD*, un tad izveidojat ražošanas vai partijas pasūtījumu daudzumam 10. Šajā gadījumā netiešas izmaksas, kas tiks pievienotas pabeigtajai cenai, tiek 10.00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Vai izmantot šo izmaksu aprēķina lapu, lai sadalītu ražošanas izmaksas pēc stundām un materiāliem?

Jā. Izmaksu aprēķināšanas **lapā** varat izveidot kopsummas zarus, lai atdalītu izmaksas ar jebkuru jūsu izvēlēto grupēšanu. Piemēram, varat izveidot vienu mezglu Kopā **ar** nosaukumu Stundas *un* citu mezglu Ar nosaukumu *Materiāli*. Zem mezgla **Stundas** pievienojiet katru ar stundām saistīto kodu grupu. Zem mezgla **Materiāli** pievienojiet katru ar materiāliem saistīto izmaksu grupu.

## <a name="dimension-groups"></a>Dimensiju grupas

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Vai var pārvaldīt izmaksas paketes vai sērijas numura līmenī?

Jā, ja izmantojat periodisku izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO, PRETfofo datumu, svērto vidējo vai svērtā vidējā datumu, **·** **·** **varat** iespējot opciju Finanšu krājumi partijas vai sērijas numura dimensijai izsekošanas dimensiju grupā, lai izsekotu izmaksas detalizētā līmenī.

### <a name="can-i-manage-costs-at-the-location-level"></a>Vai var pārvaldīt izmaksas atrašanās vietas līmenī?

Nē, nevar iespējot finanšu krājumu **opciju atrašanās** vietas **dimensijai** noliktavas dimensiju grupā. Ja jūsu organizācijai ir jāizseko izmaksas detalizētāk, apsveriet, vai varat izveidot virtuālās noliktavas **un** **pēc** tam izvēlieties opciju Finanšu krājumi noliktavas dimensijai jūsu noliktavas dimensiju grupā.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Vai iespējot opciju Izmantot noliktavas pārvaldības procesus noliktavas dimensiju grupai?

Ja domājat, ka turpmāk vēlaties lietot papildu noliktavas vadības funkcijas, **jāiespējo opcija Izmantot noliktavas vadības procesus**. Pēc noliktavas dimensiju grupas saglabāšanas, tai vairs nevar mainīt **opcijas Izmantot noliktavas vadības procesu** iestatījumus. Ja izlemjat noliktavas vadības procesus izmantot vēlāk, jums būs jāizveido jauna noliktava, kur opcija ir iespējota. Nav automatizēta procesa, ko var izmantot, lai pārvietotu visus krājumus no vienas noliktavas uz citu noliktavu vai lai kopētu saistītās konfigurācijas uz jaunu noliktavu.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Vai iespējot noliktavas dimensiju grupai izmantot noliktavas pārvaldības procesus, pat ja neplānoju izmantot detalizētu noliktavu?

Jā, pat ja neplānoat izmantot papildu noliktavas pārvaldības līdzekļus, **varat** iespējot noliktavas dimensiju grupai opciju Izmantot noliktavas vadības procesus. Lai izveidotu un apstrādātu darbības, jums būs jāpabeidz minimālā konfigurācija, piemēram, rezervāciju hierarhijas un vienību secību grupas. Tomēr papildu noliktavas iestatījumi parasti tiek ignorēti, ja manuāli apstrādājāt izdošanas sarakstus, pavadzīmes un produktu ieejas plūsmas (piemēram, pārdošanas pasūtījumu un pirkšanas pasūtījumu lapās).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Kad ir jāiespējo opcija Fiziskie krājumi noliktavas vai izsekošanas dimensiju grupai?

Ja, balstoties uz šo **dimensiju**, jums ir jāiespējo opcija Fiziskie krājumi uzglabāšanas un izsekošanas dimensiju grupām. Parasti visas aktīvas dimensijas arī tiks fiziski izsekotas. Tāpēc atlasītā dimensija izsekos jebkuru krājumu saņemšanu, izdošanu vai kustību. Ja dimensija nav obligāta (piemēram, numura zīme), **·** **var** iespējot opcijas Tukša ieejas plūsma un Tukša izejas plūsma, kas atļauta, lai ļautu lietotājiem saņemt, izsniegt vai pārvietot krājumus pat tad, ja nav norādīta dimensija.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Kad ir jāiespējo opcija Finanšu krājumi noliktavas vai izsekošanas dimensiju grupai?

Ja, veicot detalizētus **finanšu ierakstus, kas** balstīti uz šo dimensiju, glabāšanas un izsekošanas dimensiju grupām ir jāiespējo opcija Finanšu krājumi. Vietas **dimensijas** vienmēr tiek finansiāli izsekotas, bet citas dimensijas finanšu izsekošanai nav obligātas. Ja izmantojat periodisku izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO vai svērto vidējo, iespējojot finanšu krājumu opciju dimensijai, **tiek** norādīts, ka veiksiet nosegšanu tikai gadījumos, kad saņemšanai un izdošanai ir tās pašas dimensijas vērtības. Piemēram, ja **·** **iespējojat** opciju Finanšu krājumi dimensijai Noliktava, jums būs atšķirīgas izmaksas katrā noliktavā, un ieejas un izejas plūsmas no dažādām noliktavām nevar nosegt.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Vai pēc transakcijām var veikt izmaiņas attiecībā uz preci, noliktavu vai izsekošanas dimensiju grupu?

Ja krājumu modeļu **grupā dimensijai ir atzīmēta izvēles rūtiņa Aktīvs, ir iespējams mainīt vajadzību plāna iestatījumu pēc dimensijas,** **·** **·** **pirkšanas cenu un pārdošanas cenu laukiem.** Citas izmaiņas nav atļautas. Piemēram, jūs nevarat iespējot vai atspējot opcijas **Aktīvs**, **Tukša** izejas plūsma atļauta, **Tukša** ieejas plūsma atļauta, **Fiziskie krājumi** un **Finanšu krājumi**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Vai izlaistai precei var mainīt preci, noliktavu vai izsekošanas dimensiju grupu?

Ja preces rīcībā esošo krājumu vērtība ir 0 (nulle) **·** *un* opcija Vērtības atvēršana ir iestatīta uz Nē visām krājumu darbībām, izlaistajā ražošanas lapā varat mainīt noliktavas un izsekošanas dimensiju grupas. Pēc ieraksta izveides preču dimensiju grupu nevar mainīt.

## <a name="item-model-groups"></a>Krājumu modeļu grupas

### <a name="when-should-i-enable-the-stocked-product-option"></a>Kad jāiespējo opcija Uzkrātā prece?

Ir jāiespējo opcija **Uzkrātā prece** jebkuram krājumam, kas tiks izsekots jūsu krājumos. Kad šī opcija ir aktivizēta, tiek paturētas detalizētas krājumu darbības, kas seko krājuma saņemšanai un izdošanai. Šī opcija parasti tiek aktivizēta, piemēram, materiālam krājumam, kas tiek glabāts noliktavā. Šī opcija jāaktivizē arī tad, ja plānojat pievienot nemateriālo krājumu, piemēram, pakalpojumu krājumu materiālu komplektiem (MK) vai formulām. Ja neiespējoat **opciju** Uzkrātā prece, krājumu apakšgrāmatā netiek izsekotas krājumu darbības, un krājumu izmaksas parasti tiek izmaksātas virsgrāmatā. Šī opcija bieži tiek izmantota, piemēram, ražotnes piegādēm vai pakalpojumiem, kas nav iekļauti jūsu MK vai formulās.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Kad jāiespējo opcija Grāmatot fiziskos krājumus?

Opcija **Grāmatot fiziskos krājumus** parasti tiek aktivizēta tad, ja **ir aktivizēta** opcija Uzkrātā prece. Kad tiek atlasīta šī opcija, sistēma izsekos fizisko krājumu atjaunināšanu krājuma darbībā. Šī opcija tiek izmantota kopā ar parametriem kreditoriem, debitoriem un ražošanas kontroli, kas norāda, ka fiziskajam atjauninājumam ir jāizveido dokuments. Parasti šī opcija tiek iespējota, ja vēlaties, lai Virsgrāmata tiktu atjaunināta ikreiz, kad fiziski atjaunināsiet krājumu. Ja Piegādes ķēdes pārvaldība nav jūsu finanšu ierakstu sistēma, jūs, iespējams, vēlēsieties atspējot šo opciju.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Kad jāiespējo opcija Grāmatot finanšu krājumus?

Opcija **Grāmatot finanšu krājumus** parasti tiek aktivizēta tad, ja **ir aktivizēta** opcija Uzkrātā prece. Šī opcija tiek izmantota kopā ar parametriem kreditoriem, debitoriem un ražošanas kontroli, kas norāda, ka finanšu atjauninājumam ir jāizveido dokuments. Parasti šo opciju aktivizēsiet gadījumā, ja vēlaties, lai Virsgrāmata tiktu atjaunināta vienmēr, kad finansiāli atjaunināsiet krājumus (piemēram, izrakstot rēķinus pārdošanas pasūtījumiem un pirkšanas pasūtījumiem vai beidzot ražošanas pasūtījumu). Ja Piegādes ķēdes pārvaldība nav jūsu finanšu ierakstu sistēma, jūs, iespējams, vēlēsieties atspējot šo opciju.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Kad iespējot opciju Grāmatot atlikto ieņēmumu kontā pārdošanas piegādē?

Izmantojiet opciju Grāmatot **atlikto ieņēmumu** kontā pārdošanas piegādē, lai norādītu, vai vēlaties atpazīt ieņēmumus Virsgrāmatā, kad grāmatojat pārdošanas pasūtījuma pavadzīmi. Šī opcija parasti tiek izmantota, ja ir ilga aizkave starp pavadzīmi un rēķinu pārdošanas pasūtījumā vai ja nav iespējams izrakstīt rēķinu visiem pārdošanas pasūtījumiem periodā. Parasti šī opcija tiek deaktivizēta, ja iegrāmatosiet pārdošanas pasūtījuma rēķinus uzreiz pēc pavadzīmes grāmatošanas. Šādā veidā var izvairīties no papildu Virsgrāmatas grāmatojumu ģenerēšanas, kas nekavējoties tiks anulēti, izrakstot rēķinu pārdošanas pasūtījumam.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Kad iespējot opciju Uzkrājumu saistības produktu ieejas plūsmā?

Lielākajai daļai organizāciju jūs **vēlaties** iespējot opciju Uzkrāt saistības produktu ieejas plūsmā visām krājumu modeļu grupām neatkarīgi no tā, vai ir uzkrāta prece vai prece, kas nav uzkrāta. Šī opcija tiek izmantota, lai grāmatotu uzkrājumu Virsgrāmatā, balstoties uz produktu ieejas plūsmas cenu. Tā kā parasti pastāv aizkave starp produktu ieejas plūsmas grāmatošanu pirkšanas pasūtījumam un rēķina grāmatošanu, lielākajai daļai organizāciju ir jāatpazīst bilances saistības, lai tās atbilstu vietējiem noteikumiem, piemēram, Vispārpieņemtā grāmatvedības prakse (GAAP). Ja Piegādes ķēdes pārvaldība nav jūsu finanšu ierakstu sistēma, jūs, iespējams, vēlēsieties atspējot šo opciju. Ja jūsu organizācija pirkšanas pasūtījumos izmanto sagādes kategorijas, jūs varat kontrolēt uzkrājumu prasības, **iespējojot opciju Uzkrāt** **pirkšanas** izdevumus ieejas plūsmā kategorijas ierobežojuma nosacījumiem pirkšanas ierobežojumu lapā.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Kā novērst iespēju lietotājam grāmatot pirkšanas pasūtījuma produktu ieejas plūsmu, ja vēl nav grāmatota saņemšanas reģistrācija?

Jūs variet neļaut lietotājam grāmatot pirkšanas pasūtījuma produktu **ieejas** plūsmu, ja pirkšanas pasūtījuma reģistrācija vēl nav notikusi, aktivizējot reģistrācijas prasību opciju krājumu modeļu grupai. Šī opcija parasti tiek izmantota uzņēmumos, kas izmanto divas pakešapstrādes saņemšanas procesu, vai scenārijos, kuros jāreģistrē paketes vai sērijas numurs, piemēram, krājumiem, ko saņemat. Reģistrācijas **prasību opcija** attiecas ne tikai *uz* pirkšanas pasūtījumiem, bet uz visām krājuma ieejas plūsmām. Piemēram, tas attiecas uz krājumu žurnālu, kam ir pozitīvs daudzums un ražošanas pasūtījuma pabeigšanas žurnāls.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Kā var novērst iespēju lietotājam grāmatot pirkšanas pasūtījuma rēķinu, ja produktu ieejas plūsma vēl nav grāmatota?

Jūs variet neļaut lietotājam grāmatot pirkšanas pasūtījuma produktu rēķinu, ja pirkšanas pasūtījuma produktu **ieejas** plūsma vēl nav radusies, iespējojot saņemšanas prasību opciju krājumu modeļu grupai. Šī opcija parasti tiek izmantota uzņēmumos, kas pieprasa, lai ieņēmumus fiziski atpazītu Virsgrāmatā uzkrājumiem. Opcija **Saņemšanas prasības** attiecas ne tikai *uz* pirkšanas pasūtījumiem, bet uz visām krājuma ieejas plūsmām. Piemēram, tas attiecas uz krājumu žurnālu, kam ir pozitīvs daudzums un ražošanas pasūtījuma pabeigšanas žurnāls. Ja jūsu organizācija pirkšanas pasūtījumos izmanto sagādes kategorijas, varat kontrolēt saņemšanas vajadzību, **·** **iespējojot saņemšanas prasību opciju kategorijas ierobežojuma nosacījumiem lapā Pirkšanas** ierobežojumi.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Kā novērst to, ka lietotājs nevar grāmatot pārdošanas pasūtījuma pavadzīmi, ja vēl nav iegrāmatots pārdošanas pasūtījumu izdošanas saraksts?

Jūs variet **neļaut lietotājam iegrāmatot pārdošanas pasūtījuma pavadzīmi vai rēķinu, ja pārdošanas pasūtījuma izdošanas saraksts vēl nav izveidots, aktivizējot izdošanas prasību** opciju krājumu modeļu grupai. Šī opcija parasti tiek izmantota uzņēmumos, kas noliktavā veic fiziskas izdošanas procesu (piemēram, izmantojot noliktavas mobilo ierīci preču izdošanai). Izdošanas **vajadzību opcija** attiecas ne tikai *uz* pārdošanas pasūtījumiem, bet arī uz visām krājuma izejas izdošanām. Piemēram, tas attiecas uz krājumu žurnālu, kam ir negatīvs daudzums un ražošanas pasūtījuma izdošanas saraksta žurnāls.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Kā var novērst iespēju lietotājam grāmatot pārdošanas pasūtījuma rēķinu, ja pārdošanas pasūtījuma pavadzīme vēl nav grāmatota?

Jūs varat neļaut lietotājam **grāmatot** pārdošanas pasūtījuma rēķinu, ja vēl nav radusies pārdošanas pasūtījuma pavadzīme, aktivizējot ieturējuma prasību opciju krājumu modeļu grupai. Šī opcija parasti tiek izmantota organizācijās, kas veic fiziskas iepakošanas procesu noliktavā (piemēram, izmantojot mobilo programmu Noliktavas pārvaldība, lai veiktu iepakošanu vai ģenerētu dokumentu, kas tiks ietverts nosūtītajiem krājumiem). Ieturējumu **vajadzības** opcija attiecas *ne* tikai uz pārdošanas pasūtījumiem, bet arī uz visām krājuma izejas problēmām. Piemēram, tas attiecas uz krājumu žurnālu, kam ir negatīvs daudzums un ražošanas pasūtījuma izdošanas saraksta žurnāls.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Vai neļaut pārdot krājumus, kas ir reģistrēti?

Kad krājums ir reģistrēts jūsu krājumos Piegādes ķēžu pārvaldībā, daudzums ir fiziski pieejams piegādei sistēmā. Ja *krājumiem*, kas ir reģistrēti, bet vēl nav saņemti, jābūt pieejamiem lai tos izsniegtu pārdošanas pasūtījumiem vai ražošanas pasūtījumiem, piemēram, apsveriet iespēju izmantot krājumu statusu, krājuma bloķēšanu, kvalitātes pasūtījumus, karantīnas pasūtījumus vai rezervēšanas līdzekļus, lai pārvaldītu darījumu procesu.

## <a name="production-costing"></a>Ražošanas izmaksu aprēķināšana

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Vai es variet izmantot vienu izmaksu aprēķināšanas modeli izejmateriāliem un atšķirīgu izmaksu modeli pabeigtām precēm?

Jā, katram krājumam var izmantot dažādus izmaksu aprēķināšanas modeļus. Ražotājiem nav izmantojams periodiskais izmaksu aprēķināšanas modelis izejmateriāliem un standarta izmaksas daļēji pabeigtām un pabeigtām precēm.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Kā var vadīt pieskaitāmās mašīnas izmaksas?

Lai vadītu jūsu datora papildu pieskaitāmās izmaksas, jāizveido resursi un resursu grupas katrai mašīnai atbilstoši jūsu biznesa prasībām. Katru resursu vai resursu grupu var piešķirt izmaksu kategorijām, lai kontrolētu iekārtas izmaksas. Katra izmaksu kategorija var būt saistīta ar izmaksu grupu, un katru izmaksu grupu var izmantot par pamatu netiešo izmaksu aprēķināšanai izmaksu aprēķina lapā.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Kā izmaksu aprēķina lapā atpazīt izmaksas, kas ir saistītas ar enerģijas patēriņu (piemēram, kurts, enerģijas vai gāzes patēriņš) ?

Parasti ir iespējams atpazīt izmaksas, kas ir saistītas ar enerģijas patēriņu vienā no diviem veidiem:

- Izveidojiet rindu savā MK vai formulā. Parasti šī rinda tiek veidota kā pakalpojuma krājums un var norādīt mērvienību, ko patērē saistībā ar jūsu ražoto daudzumu. Šādā veidā lietotājs ražošanas procesa laikā var patērēt atšķirīgu daudzumu. Varat automātiski patērēt krājumus, balstoties uz vērtību, kas atlasīta laukā **Tīrīšanas** princips.
- Izveidojiet netiešās izmaksas izmaksu aprēķina lapā. Parasti šī pieeja tiek izmantota, lai iedalītu kopējās jūsu enerģijas patēriņa izmaksas jūsu ražošanas procesā. Varat izmantot izmaksu grupu un izmaksu bāzi, lai, piemēram, samazināt patēriņu, balstoties uz maršrutā izmantotajiem materiāliem vai darbaspēku.

Jums jāizvēlas vislabākā opcija, balstoties uz jūsu pārskatiem, saskaņošanu un darbības prasībām.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Vai es varētu iegūt detalizētu informāciju par resursiem MK vai formulā?

Resursu datus var saglabāt tikai maršruta operācijā. Kaut arī varat izveidot pakalpojuma krājumu, lai tas pārstāvētu resursu un piešķirtu izmaksas, lai palielinātu izmaksu aprēķinu pabeigtai precei, mēs parasti neiesakām šo pieeju. Tā vietā ieteicams izveidot vienkāršu maršrutu, kuram ir viena rinda, lai atsekotu resursu izmaksas, un konfigurēt operāciju tā, lai tā automātiski tiktu patērēta ražošanas pasūtījuma sākumā vai beigās.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Vai aprēķinu detaļas var skatīt, ja izmaksas ir ievadītas manuāli?

Nē. Ja lapai Krājuma cenas lapa ievadāt **cenu** manuāli, **nav pieejamas pogas Skatīt aprēķinu informāciju** **un** Pārskata aprēķinu informāciju. Ja atlasāt **pogu** Izmaksu apkopojums pēc izmaksu grupas manuāli ievadītai izmaksu cenai, tiek parādīta apkopota rinda un visas izmaksas tiek apkopotas līdz pabeigtam preču krājumam.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Vai sistēma aprēķina novirzes ražošanas pasūtījumā, manuāli ievadot izmaksas?

Jā, sistēma aprēķina novirzes, manuāli ievadot standarta izmaksas. Tomēr, ja to aprēķināšanas vietā manuāli ievadāt standarta izmaksas, visas materiālu, maršrutu un netiešo izmaksu patēriņu ražošanas pasūtījumā tiek uzskatītas par aizvietošanas noviržu. Ja pastāv papildu novirzes, piemēram, papildu materiālu vai darbaspēka patēriņš, tās arī tiks reģistrētas kā novirzes no ražošanas MK. Tāpēc stingri ieteicams vienmēr veikt aprēķinu krājumiem, kuriem ir MK, maršruts vai netiešās izmaksas.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Kā es variet veikt novirzes no pakārtotā ražošanas pasūtījuma uz pamata ražošanas pasūtījumu?

Ja izmantojat periodisku izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO vai svērto vidējo, tad apakšražošanas izmaksas tiks atpazītas heiristiskā modelī, ko esat atlasījis šiem krājumiem. Ja nepieciešama faktiskā izmaksu aprēķināšana, apsveriet iespēju izmantot iezīmēšanas principu, lai norādītu, kurš pakārtotais ražošanas pasūtījums tiek izsniegts pamata ražošanas pasūtījumam. Alternatīvi apsveriet iespēju **izmantot finanšu krājumu** opciju paketes **vai** sērijas **numura** dimensijai, piemēram, izsekošanas dimensiju grupā.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Kā tīrīšanas princips ietekmē patēriņu?

Tīrīšanas princips MK, formulā vai maršruta rindā kontrolē hronometrāžas un tehnikas, kas tiek izmantotas, lai patērētu vienību vai darbaspēku. Ja, sākot *ražošanas* pasūtījumu, tiek automātiski patērēts krājums vai darbs. Atlasot *Pabeigt*, krājums vai darbs tiek automātiski patērēts, kad ziņojiet par ražošanas pasūtījuma pabeigšanu. Ja izvēlaties *Manuāli*, lietotājam ir manuāli jāizņem materiāli vai jāieraksta laiks darba vai maršruta kartes žurnālā. MK un formulām ir arī opcija Pieejams *atrašanās* vietā. Atlasot šo opciju, krājumi tiek automātiski patērēti pēc to pārsūtīšanas uz ražošanas vietu.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Kā veikt izmaksu aprēķinus, ja man ir vairāku līmeņu MK vai formulas?

Ieteicams sākt mk vai aprēķina formulas zemāko līmeni. Lai atvieglotu filtrēšanu, kad tiek veidoti masveida izmaksu aprēķini, aprēķinu grupas var izmantot, lai palīdzētu sadalīt preces. Ieteicams arī palaist periodisko darbu *MK līmeņu* pārrēķināšana, pirms sākat izmaksu aprēķinu masveida aprēķināšanu. Katrai organizācijai ir jāņem vērā preču kopums un jānosaka stratēģija, kas atbilst jūsu produkta un MK vai formulas struktūrām specifiskajām vajadzībām.

## <a name="transfer-order-costing"></a>Pārsūtīšanas pasūtījuma izmaksu aprēķināšana

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Vai ir veids, kā piešķirt kravu pārsūtīšanas pasūtījuma izmaksām?

Jūs varat pievienot maksas pārsūtīšanas pasūtījumam, lai pievienotu izmaksas. Maksu kods nosaka debeta un kredīta maksu, ko pievienojat. Vispirms izveidojiet izmaksu kodus krājumu **vadības modulī**. Lai pārsūtīšanas pasūtījumam pievienotu maksu, atlasiet **maksas** pārsūtīšanas pasūtījuma rindā, kurai vēlaties pievienot maksu.

## <a name="variances"></a>Novirzes

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Vai es variet apstrādāt novirzes atšķirīgi, balstoties uz vietu vai noliktavu?

Nav opcijas konfigurēt novirzes kontus pēc vietas. Kad izlaistajām precei izmantojat standarta izmaksu grāmatošanu, jūs varat izvēlēties galveno kontu, kas tiek izmantots standarta izmaksu novirzes grāmatojumu grāmatošanai **lapā Grāmatošana**. Varat atlasīt, lai konfigurētu kontus vienam krājumam, krājumu grupai vai visiem krājumiem. Var konfigurēt arī vienu izmaksu grupu, izmaksu grupu vai visas izmaksu grupas.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Vai es variet atdalīt novirzes, kas ir valūtas maiņas kursu rezultāts no citiem noviržu tipiem?

Ja novirze ir valūtas maiņas kursa starpības starp pirkšanas pasūtījuma cenu un krājuma standarta izmaksām, maiņas kursa starpības no citām novirzēm nav iespējams atdalīt.

## <a name="reporting"></a>Pārskatu veidošana

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Cik krājumu vērtības pārskata konfigurācijas var izveidot un izmantot?

Krājumu vērtības pārskata konfigurāciju skaits, ko varat izveidot, nav ierobežots. Jums jānovērtē specifiskas pārskatu prasības un jāizveido konfigurāciju skaits, kas nepieciešams, lai apmierinātu šīs prasības. Lai palaistu pārskatu vai pārskata glabāšanas opciju, ir nepieciešama vismaz viena krājumu vērtības pārskata konfigurācija.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Vai izmantot krājumu vērtības pārskatu, lai analizētu krājumu izmaksas katrā noliktavā?

Jā. Varat aktivizēt opciju Skatīt **vai** **Kopsumma** katrai Noliktavas dimensijai **krājumu** vērtības pārskata konfigurācijā. Tomēr pārskatā tiks rādītas tikai tās dimensijas vērtības, kurās **noliktavas dimensiju** grupai ir iespējota opcija Finanšu krājumi. Citām dimensijām tā rādīs tukšas kolonnas. Papildinformāciju skatiet krājumu vērtības [pārskata piemēros un loģikā](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Kā es variet aplūkot krājumu daudzumu uz noteiktu datumu ar svērto vidējo?

Varat izmantot pārskatu Krājumu **vecumstruktūra**, kurā **iekļauta kolonna Vidējās** vienības izmaksas, kas parāda krājumu vērtību no noteikta datuma. Papildinformāciju skatiet krājumu vecumstruktūras [pārskatu piemēros un loģikā](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Kā var skatīt, kuras saņemšanas darbības ir nosegtas pret izdošanas darbību?

Krājumu darbības segšanas **darbības var skatīt, atlasot Nosegšanas** **·** **·** **·** **vai Izmaksu pārlūks cilnes Krājumi rūtī Krājumu darbība vai Detalizēta informācija par krājumu** darbību lapu. Ja izvēlaties kvīti, lai skatītu problēmas, kas attiecas uz darbību, izmaksu pārlūks nerāda detalizētu informāciju. Detaļas tiek rādītas tikai atlasot izejas plūsmas darbību.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Kā krājumu vērtības pārskats rāda krājumus ar pozitīvu fizisko daudzumu un negatīvu finanšu vērtību?

Krājumu vērtības pārskats atdala fiziskās un finanšu summas un daudzumus savas kolonnās. Pārskatā parādītās vērtības ir no datumu diapazona, ko atlasījāt, izpildot pārskatu. Parādītais summēšanas līmenis ir atkarīgs no jūsu atlasītajiem iestatījumiem. Ja krājumam ir darbības, kas ir fiziski saņemtas un finansiāli izsniegtas, daudzumi un vērtības tiek summētas neatkarīgi. Ja atlasīts skatīt detalizācijas līmeni kā darbības, rindas katrai saņemšanai un izdošanai tiek rādītas atsevišķi, attiecīgi tiek rādīti fiziskie un finanšu daudzumi un summas. Papildinformāciju skatiet krājumu vērtības [pārskata piemēros un loģikā](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Kāda ir noliktavas un izsekošanas dimensiju grupu ietekme uz krājumu vērtību pārskatu?

Ja iespējojat **opciju** Finanšu vērtība dimensijai noliktavas vai izsekošanas dimensiju grupā, **varat atlasīt opciju Skatīt** **vai Kopsumma** dimensijai krājumu vērtības pārskata konfigurācijā. Ja dimensijai **, kur** nav **atlasīta** opcija Finanšu **vērtība**, atlasāt opciju Skatīt vai Kopsumma, pārskata izvade kolonna būs tukša. **Ja** dimensijai noliktavas vai izsekošanas dimensiju grupā ir iespējota opcija Finanšu vērtība un krājumu vērtības pārskata konfigurācijā nav atlasīta opcija Skatīt vai Kopsumma, sistēma apkopos to atlasīto dimensiju vērtības, **·** **kuras** tās ir finansiāli izsekotas.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Vai iegultos pārskatus Power BI var pielāgot izmaksu pārskatiem?

Jā, lietotāji ar pareizām drošības atļaujām var atjaunināt pārskata dizainu canvas Power BI jebkuram iegultam pārskatam Piegādes ķēžu pārvaldībā. Papildinformāciju skatiet sadaļā Iegulto [pārskatu pielāgošana analītiskajām darbvietām](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Kur var skatīt noviržu analīzes pārskatu?

Jūs variet piekļūt noviržu analīzes pārskatam, ejot uz Izmaksu pārvaldības vaicājumiem un pārskatiem Krājumu uzskaite - **\>\> analīzes pārskati vai Izmaksu pārvaldības pieprasījumi un pārskati** Ražošanas uzskaite - analīzes pārskati.**\>\>** Abas opcijas atver vienu un to pašu pārskatu, un pārskatam ir vienāds režīms.

## <a name="item-prices-and-default-costs"></a>Krājuma cenas un noklusējuma izmaksas

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Vai uzturēt katra preces varianta izmaksas?

Jā. Lai iespējotu cenu noteikšanu **pēc preces varianta** **·** **·**, lapas Izlaistā prece cilnē Pārvaldīt izmaksas, varat iespējot opciju Izmantot izmaksu cenu pēc varianta. (Šī opcija ir pieejama tikai preces šabloniem.) Pēc tam **lapā Krājuma cena (** **·** **kuru varat atvērt vai nu no lapas Izmaksu versija, vai Izlaistā prece),** **·** **varat atlasīt Dimensiju displeju, lai norādītu, vai vēlaties rādīt konfigurāciju,** izmēru **,** **krāsu vai** stila dimensiju.**·** Lai saglabātu iestatījumu un lietotu atlasītās dimensijas ikreiz, kad atverat lapu, **iespējojiet opciju Saglabāt** iestatījumu un pēc tam atlasiet **Labi**. Dimensijas varat ievadīt tikai krājumiem, kur dimensijas ir aktīvas preču dimensiju grupā.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Vai uzturēt izmaksas katrai noliktavai?

Nē, krājuma cenu nevar uzturēt pēc noliktavas. Tomēr varat uzturēt tirdzniecības līgumus par pirkšanas cenām vai pārdošanas cenām pēc noliktavas. Vispirms izvēlieties opciju "**Pirkšanas cenas** **" vai "Pārdošanas** cenas" dimensijai lapā **Noliktavas dimensiju** grupa. Pēc tam, izveidojot tirdzniecības līgumu žurnālu un atverot dimensiju rindas, atlasiet Krājumu rādīšanas dimensijas, **\>** lai atlasītu, kura dimensija režģī jāparāda. Lai saglabātu iestatījumu un lietotu atlasītās dimensijas ikreiz, kad atverat lapu, **iespējojiet opciju Saglabāt** iestatījumu un pēc tam atlasiet **Labi**. Dimensijas varat ievadīt tikai krājumiem, kur dimensijas ir aktīvas preču dimensiju grupā.

### <a name="what-are-price-charges"></a>Kādas ir cenas izmaksas?

Cenu maksas ir veids, kā krājuma cenai vai tirdzniecības līgumam pievienot fiksētu summu. Kad ievadāt summu laukā **Cenas izmaksas**, varat ievadīt vērtību arī laukā **Izmaksu** daudzums. Cenas maksas tiek amortizētas jūsu norādītajā papildmaksu daudzumā. Ja krājuma **cenā vēlaties iekļaut** cenas maksas, aktivizējiet opciju Iekļaut vienības cenā. Šī opcija vienmēr tiek aktivizēta standarta izmaksām.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Kā jākonfigurē cenas krājumiem, kas tiek radīti vairākās valūtās?

Ja **ievadāt** **noklusējuma** cenu laukā Pirkšanas cena lapā Izlaistā prece, tiek pieņemts, ka jūsu juridiskās personas uzskaites valūta ir Virsgrāmatā. Tāpat arī ievadot pirkšanas cenu izmaksu versijā, kur lauks Cenas tips ir iestatīts uz Pirkšana, tiek pieņemts, **·** *ka* cena ir jūsu juridiskās personas uzskaites valūtā. Veidojot pirkšanas pasūtījumu kreditoram, kuram ir atšķirīga valūta, **sistēma** automātiski konvertēs valūtu no uzskaites valūtas summas uz darbības valūtu, izmantojot valūtas maiņas kursu, kas norādīts Virsgrāmatas laukā Uzskaites valūtas maiņas kursa tips.

Veidojot tirdzniecības līgumu žurnālu, varat norādīt valūtu, kurā cena tiek izteikta katrā rindā. Varat izveidot tirdzniecības līgumus vairākām valūtām, noteiktiem kreditoriem un daudzām citām faktoru kombinācijām. Ja izveidojat pirkšanas pasūtījumu, kur pastāv tirdzniecības līgums atlasītajai valūtai, sistēma izmantos tirdzniecības līgumu ar atbilstošu valūtu. Grāmatojot tādas darbības kā produktu ieejas plūsmas vai rēķini, summa tiks konvertēta Virsgrāmatas uzskaites valūtā, izmantojot uzskaites valūtas maiņas kursu, kas norādīts Virsgrāmatā.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Kā jākonfigurē izmaksas krājumiem, kas tiek radīti vairākās valūtās?

Izmaksas nevar konfigurēt vairāk kā vienā valūtā. Izmaksas, **·** **·** **kuras** norādāt krājuma cenai vai noklusējuma izmaksām, ko ievadāt lapas Izlaistās preces laukā Cena, kopsavilkuma cilnē Pārvaldīt izmaksas, vienmēr tiek izteiktas atlasītās juridiskās personas Virsgrāmatas uzskaites valūtā.

Ja jūsu organizācija izmanto standarta izmaksu aprēķinu, jums ir jādefinē stratēģija izmaksu noteikšanai, kad ir vairākas valūtas. Būtu arī jānosaka process izmaksu regulārai atjaunināšanai, lai palīdzētu samazināt iegrāmatoto noviržu skaitu.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Vai izmantot peļņas iestatījumu izmaksu grupas lapā, lai aprēķinātu pārdošanas cenas?

Jā, varat izmantot peļņas iestatījumu **lapā** **Izmaksu** grupa, lai pievienotu procentus, kad pārdošanas cenas tiek aprēķinātas, izmantojot izmaksu aprēķinu. Plašāku informāciju skatiet MK [aprēķinos](bom-calculations.md).

## <a name="marking"></a>Iezīmēšana

### <a name="how-does-marking-affect-periodic-costing-models"></a>Kā iezīmēšana ietekmē periodiskos izmaksu aprēķināšanas modeļus?

Ja izmantojat periodisko izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO vai svērto vidējo, un esat atzīmējis saņemšanas darbību pret izdošanas darbību, krājumu heirisiskais modelis tiek ignorēts krājumu slēgšanas procesa laikā. Tā vietā sistēma izmantos faktiskās saņemšanas izmaksas izejas plūsmas izmaksām.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Kas notiek krājumu slēgšanas laikā, kad es izmantoju atzīmēšanu?

Kad tiek atzīmētas saņemšanas un izejas plūsmas, krājumu slēgšana nokārtos darbības, kas ir atzīmētas kopā. Kad iezīmēšana tiek izmantota nosegšanas veidojiet **, lauks Princips** lapā **Nosegšana** tiks iestatīts uz *Iezīmēšana*. Ja darbība ir atzīmēta pirms tās fiziskās vai finansiāli atjaunināšanas, tad izdotā darbība izmantos iezīmētās vidējās izmaksas, nevis tekošās vidējās izmaksas. Ja darbības ir atzīmētas pēc finanšu grāmatošanas, krājumu slēgšana un koriģēšanas process pielāgos izdošanas izmaksas tā, lai tās atbilstu saņemšanas izmaksām.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Vai, lietojot standarta izmaksu zīmi vai pārvietojot vidējo, darbības var atzīmēt manuāli?

Nē, ieejas vai izejas plūsmas nevar atzīmēt manuāli, ja izmantojat standarta izmaksu aprēķināšanas vai pārvietojamā vidējā vērtību. Ja darbības (piemēram, tiešā piegāde vai starpuzņēmumu pasūtījumi) tiek atzīmētas automātiski, atzīmēšanas ieraksts paliks un darbosies kā stingrā rezervēšana. Tomēr, kad izmantojat standarta izmaksu vai pārvietojat vidējo, ierakstu iezīmēšana neietekmē krājumu izmaksas.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Kā iezīmēšana ietekmē peļņas un zaudējumu pārskatu?

Ja atzīmēsiet izdošanas darbību pret ieejas plūsmu, izdošanas cena saskanēs ar atlasīto ieejas plūsmu. Fiziski un finansiāli grāmatojot izdošanu, grāmatošana ietekmēs pārdoto preču izmaksas, **·** **piegādātās un pārdoto preču izmaksas, rēķinā iekļautais konts,** kuru norādāt krājumu grāmatošanas profilā. Ja darbība ir atzīmēta pēc fiziskās vai finanšu atjaunināšanas, *krājumu* slēgšana un pielāgošanas process izveidos korekciju, kam ir atbilstošs dokuments, kas koriģē pārdoto preču izmaksas, **rēķinā iekļautais konts un korespondējošais konts**, kurā norādāt vienību izmaksām, **par kurām izrakstīts rēķins**(krājumi).

### <a name="how-does-marking-affect-master-planning"></a>Kā iezīmēšana ietekmē vispārējo plānošanu?

Vispārējās **plānošanas parametru** lapas cilne **Standarta atjaunināšana** ietver lauku ar nosaukumu Atjaunināt **iezīmēšanu**. Jūsu atlasītā opcija tiek izmantota, apstiprinot plānoto pasūtījumu, ko ģenerē vispārējā plānošana. Pieejamas šādas opcijas:

- *Nē* – sistēma neveic nekādu iezīmēšanu.
- *Standarta* – sistēma atzīmē ieejas plūsmas pret izejas plūsmām atbilstoši piesaistei. Vajadzību pasūtījums ir iezīmēts pret izpildes pasūtījumu. Ja kāds daudzums paliek izpildē, izpildes pasūtījums netiek iezīmēts.
- *Paplašināts* – sistēma atzīmē gan vajadzību pasūtījumus, gan izpildes pasūtījumus neatkarīgi no tā, vai izpildes pasūtījumā paliek atvērts kāds daudzums.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negatīvi krājumi

### <a name="when-should-i-allow-physical-negative-inventory"></a>Kad atļaut negatīvus fiziskos krājumus?

Parasti nav ieteicams atļaut negatīvus fiziskos krājumus, jo noliktavā materiāla krājuma vērtība nav mazāka par 0 (nulli). Tomēr dažu nozaru un biznesa scenāriju biznesa procesi var ierobežot darbības, kas pieprasa, lai krājumi varētu fiziski tikt negatīvi. Piemēram, mazumtirgotāji nedrīkst kavēt tās preces pārdošanu, kas tiek pārdota kases sistēmā, pat ja sistēma norāda, ka preces nav pieejamas. Procesa ražotāji sniedz citu piemēru. Šiem ražotājiem patērētā summa var pārsniegt formulā ieteikto summu. Alternatīvi patēriņu var aprēķināt, nevis precīzāk, lai patēriņš pārsniegtu summu noteiktā vietā, piemēram, sējumā.

Ja iespējams, jāveic biznesa procesa vērtēšana un jāmēģina uzlabot to, lai nodrošinātu, ka krājumi nevar būt negatīvi. Ja ļautu negatīvu krājumu daudzumu, negatīvs krājums jāapstrādā ar skaidru biznesa procesu, lai koriģētu negatīvos krājumus, jo tie var nelabvēlīgi ietekmēt izmaksu procesu.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Kad ļautu finansiālus negatīvus krājumus?

Ieteicams, lai lielākā daļa organizāciju pieļautu finansiālus negatīvus krājumus. (Vairākumā gadījumu pirkšanas pasūtījumu rēķini netiek apstrādāti pirms krājumu nosūtīšanas.) Šī opcija jāaktivizē, kad ir specifiski biznesa procesi, kam nepieciešams, lai pārdošanas cena atspoguļotu pirkšanas pasūtījuma beigu izmaksas. Piemēram, šī prasība var tikt piemērota nozares "veidot pasūtījums" vai īpašos reģionos, kuros to nosaka likums.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Kas notiek ar manu problēmu izmaksām, ja krājumi ir negatīvi?

Ja jūsu krājuma krājumi ir negatīvi un jūs izdodiet vairāk krājumu, nekā jums ir fiziski, sistēma izmantos noklusējuma krājuma cenu, lai aprēķinātu esošo vidējo, ja izmantojat periodisku izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO vai svērto vidējo. Ja krājumam nav norādīta noklusētā cena, sistēma izdod krājumus ar vērtību 0 (nulle). Tādējādi nākotnes aprēķini par jūsu tekošo vidējo vai pārvietojamu vidējo vērtību var būt neprecīzi.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Vai neļaut krājumu izdot, iepakot vai pārdot pārdošanas pasūtījumos un ražošanas pasūtījumos, ja nav pietiekami daudz rīcībā esošo krājumu?

Jā. Krājumu modeļu grupai ieteicams **deaktivizēt** opciju Fiziskais negatīvs, lai novērstu krājumu izvēli, iepakošanu vai pārdošanu pārdošanas pasūtījumos un ražošanas pasūtījumos.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Vai neļaut krājumus iekļaut pārdošanas pasūtījumā, ja šim krājumam nav izrakstīts rēķins par pirkšanas pasūtījumiem?

Jā. Krājumu modeļu grupai ieteicams **deaktivizēt** opciju Finanšu negatīvais, lai novērstu krājumu rēķina izstšanu pārdošanas pasūtījumā, ja šim krājumam nav izrakstīti pirkšanas pasūtījumi.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Kā negatīvie krājumi ietekmē finanšu koeficientus, piemēram, bruto peļņas normas?

Kad atļaujat krājumiem parādīties negatīvi, krājumu vērtība jūsu bilancē un pārdoto preču izmaksas jūsu peļņas un zaudējumu aprēķinā var tikt nepietiekami novērtētas, it īpaši, ja krājumiem nav konfigurēta noklusējuma cena. Tāpēc finanšu pārskatu un koeficientu, piemēram, bruto peļņas normu, var pārspīlēt, jo izmaksas nav pareizas. Ja izmantojat periodisku izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO vai svērto vidējo, plūsmas vērtību var koriģēt, kad palaižat krājumu slēgšanu un pārrēķina procesu pēc negatīvo krājumu daudzumu izlabošanas. Tomēr, ja izmantojat pārvietojamu vidējo, atsevišķām darbībām nav iespējams pārvērtēt.

### <a name="how-should-i-correct-negative-inventory"></a>Kā labot negatīvos krājumus?

Ieteicams bieži pārraudzīt un labot negatīvos krājumus, ja jūsu organizācija vai biznesa prasības nosaka, ka ļautu krājumiem parādīties negatīvi. Krājumu vērtības var labot, veicot cikla inventarizāciju, grāmatojot korekciju vai grāmatojot kustības žurnālu. Ja neparedzētos ieguvumus no krājuma ir jāatpazīst noteiktā Virsgrāmatas kontā, vajadzētu plānot izmantot kustības žurnālu. Ja izmantojat cikla inventarizācijas vai krājumu pielāgošanas procesu, **·** **sistēma grāmatos krājumu korekciju krājuma ieejas plūsmas kontā un kompensēs krājumu izdevumus, peļņas kontus,** kurus norādāt krājumu grāmatošanas profilā.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Vai ir jāizveido jauns krājums, ja krājumi ir negatīvi un es izmantoju pārvietojamu vidējo?

Nē. Ja jūsu organizācija ļauj krājumiem pārvietoties fiziski un jūs izmantojat pārvietojamu vidējo kā savu krājumu modeli, sistēma izmantos atkāpšanās izmaksu secību, **kas ir piešķirta lapā Krājumu un noliktavas pārvaldības parametri**, lai noteiktu, kā izmaksas tiks piešķirtas jūsu izejas plūsmasm. Parasti ieteicams izvairīties no atļaut krājumam fiziski atgriezties negatīvi. Plašāku informāciju skatiet pārējos jautājumus šīs tēmas [sadaļā](#negative-inventory) Negatīvi krājumi.

## <a name="not-stocked-products"></a>Preces, kas nav uzkrātas

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Vai var grāmatot pārdošanas pasūtījumu izdošanas sarakstus uzkrātām precēm?

Ģenerējot izdošanas sarakstu pārdošanas pasūtījumam, kas ietver krājumus, kas nav uzkrātā krājumu modeļu grupā, jūs neredzēsit nevienu rindu šiem krājumiem, kas nav uzkrāti. Nevar izmantot mobilo programmu Noliktavas pārvaldība, lai apstrādātu nenokrātas preces.

Ģenerējot pavadzīmi pārdošanas pasūtījumam, kas ietver krājumus, kas nav uzkrāti krājumu modeļu grupā, **·** *iestatiet* laukā Daudzums vērtību Izdotais daudzums, nevis uzkrātās preces, lai dokumenta ģenerēšanai iekļautu noliktavā nekrājamos krājumus. Atlasot *Visi*, pavadzīmē tiks iekļauti tikai uzkrātie krājumi.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Vai jāizmanto nenokrāta prece vai kategorija (pārdošanas kategorija vai sagādes kategorija)?

Izvēle starp uzkrāto preci un kategoriju ir atkarīga no jūsu specifiskajām biznesa prasībām. Uzkrātās preces parasti piedāvā lielāku kontroli pār noklusējuma vērtībām, piemēram, daudzumu un cenu pirkšanas pasūtījumos un pārdošanas pasūtījumos. Tāpēc scenārijos, kuros viena prece vai pakalpojums tiek nopirkts vai pārdots vairāk nekā vienu reizi, tiek vēlamās uzkrātās preces. Kategorijas noder scenārijos, kuros cena, krājumi, apraksti u.tt. ir neatbilstīgi no darbības uz darbību. Kategorijas var izmantot arī jebkurai precei, lai palīdzētu klasificēt pārdotās vai nopirktās preces tipu.

## <a name="service-items"></a>Pakalpojumu krājumi

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Kāda ir atšķirība starp pakalpojuma krājumu un uzkrāto preci?

Pakalpojuma krājums ir preces tips. Izveidojot jaunizveidotu preci, lauku Preces tips varat iestatīt **uz Krājums** *vai* *Pakalpojums*. *Krājums* parasti tiek atlasīts, lai norādītu, ka krājums ir materiāli, bet *Pakalpojums parasti tiek* izvēlēts, lai norādītu, ka vienība ir nemateriāla.

Jebkuru izlaisto preci, neņemot vērā to, vai tā ir vienība vai pakalpojuma prece, var uzkrāt vai nebūt uzkrāta. Uzkrātā vai noliktavā neatdotā iestatījums tiek kontrolēts ar krājumu modeļu grupu, ko atlasāt izlaistai precei. Atlasot krājumu grupu, kas nav uzkrāta, sistēma, piemēram, neveidojiet krājumu darbības saistītam pārdošanas pasūtījumam vai pirkšanas pasūtījumam.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Vai MK var ietvert nenokrātas preces?

Nē, nevar ietvert izlaistu preci, kas ir saistīta **ar** krājumu modeļu grupu, kam MK vai formulā ir atspējota opcija Uzkrāts. Nav svarīgi, vai preces tipa **lauks ir iestatīts** kā Krājums *vai* *Pakalpojums*. MK vai formulas rindās var iekļaut tikai krājumus, kas ir uzkrāti.

## <a name="costing-modelspecific-questions"></a>Izmaksu modelī specifiskie jautājumi

### <a name="which-costing-model-should-i-use"></a>Kādu izmaksu modeli izmantot?

Izmaksu modeļi, kurus vajadzētu atlasīt, ir atkarīgi no biznesa prasībām. Pirms izvēlaties cenu modeli izmantošanai Piegādes ķēžu pārvaldībā, jums vajadzētu apstiprināt, ka modeli atļauj jūsu lokālie noteikumi. Mēs iesakām jums apstiprināt savu atlasi ar sertificētu grāmatvedi jūsu reģionā.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Vai organizācijā var izmantot vairākus izmaksu aprēķināšanas modeļus?

Jā. Nav ierobežojuma ar krājumu modeļu grupu vai izmaksu modeļu skaitu, ko varat atlasīt Piegādes ķēdes pārvaldībā.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Vai katram krājumam var izmantot vairākus izmaksu aprēķināšanas modeļus?

Nē. Katrai izlaistai precei var atlasīt tikai vienu izmaksu aprēķināšanas modeli. Šo uzvedību kontrolē krājumu modeļu grupa. Ja ir jāizmanto vairāk nekā viens izmaksu aprēķināšanas modelis, lai ziņotu par krājumu vērtībām, ieteicams izmantot Globālo krājumu uzskaites pievienojumprogrammu.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Kad es izmantoju ražošanas izpildi, kura izmaksu metodoloģijai jāizmanto?

Izmaksu modeļi, kurus vajadzētu atlasīt, ir atkarīgi no biznesa prasībām. Nav īpašu priekšrocību vai metodes, kā izmantot jebkuru izmaksu modeli, ja jūsu organizācija izmanto arī ražošanas izpildi.

### <a name="when-is-fefo-used"></a>Kad tiek izmantota FEFO?

Pirmais derīguma termiņš, pirmais ārā (FEFO) nav izmaksu metodoloģija. Tā vietā ir rezervēšanas tehnika, ko bieži izmanto ražošanas organizācijās. Varat iespējot FEFO rezervācijas **krājumu modeļu grupai, iespējojot FEFO** **opciju, kas tiek kontrolēta, izmantojot datumu, un pēc tam atlasot vērtību laukā Izvēles** kritēriji.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Vai pastāv veiktspējas atvieglojumi viena izmaksu aprēķināšanas modeļa izvēlei pār citu?

Kopumā krājumam atlasītais izmaksu modelis minimāli ietekmē sistēmas veiktspēju kopumā. Tomēr laika apjomu, kas nepieciešams, lai darbinātu krājumu slēgšanu vai pārrēķina procesu, var ietekmēt jūsu atlasītais krājumu izmaksu aprēķināšanas modelis. Piemēram, ja izmantojat standarta izmaksas vai pārvietojamu vidējo, krājumu slēgšanas procesam ir minimālā ietekme uz sistēmu, jo tas neatjaunina katru krājumu darbību un izveido segšanas. Tomēr periodisks izmaksu aprēķināšanas modelis, piemēram, FIFO, LIFO vai svērtais vidējais var palielināt laika apjomu, kas nepieciešams krājumu slēgšanas procesa pabeigšanai. It īpaši aizvēršanas process **var būt garāks** **·** *, ja ievadāt lielu skaitu maksimālo atkārtošanu skaitu, kas atļauts krājuma laukam, vai mazāko skaitu laukā Minimālā atļautā summa krājumu slēgšanas* procesam.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Kad jāizmanto opcija Fiksēta saņemtā krājuma cena?

Atlasot krājuma **izvēles** **rūtiņu** Fiksētas saņemšanas cena krājumu modeļu grupas lapā, sistēma izmantos ieejas plūsmas cenu kā standarta izmaksu krājumu ieejas plūsmai. Ja pastāv starpība starp pirkšanas cenu un noklusējuma krājuma izmaksu cenu, kas ir konfigurēta precei, **·** **starpība** tiks grāmatota fiksētās saņemšanas cenas peļņas vai Fiksētas saņemtā krājuma cenas zaudējumu kontā un **ieskaitīta** fiksētās saņemšanas cenas korespondējošā kontā. (Visi šie konti ir norādīti **Grāmatošanas** lapa.)

Ja virsgrāmatā **tiek** izsekota saņemšanas cena, piemēram, FIFO, LIFO vai svērtā vidējā, jums vajadzētu atzīmēt pirkšanas cenas noviržu Virsgrāmatā, ja ieejas plūsmas cena atšķiras no noklusētajām krājumu izmaksām.

### <a name="moving-average"></a>Vidējās vērtības pārvietošana

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Vai vidējās vērtības tiek pārvietotas tāpat kā peldošais vidējais?

Termini mainīgais vidējais, mainīgais vidējais un tekošais vidējais bieži tiek izmantoti sinonīmi. No šiem nosacījumiem pārvieto vidējais ir vienīgais oficiālais izmaksu modelis, kas ir pieejams Piegādes ķēžu pārvaldībā. Kaut arī tekošais vidējais nav oficiāls izmaksu aprēķināšanas modelis, tas ir tehnika, kas tiek izmantota, kad izmantojat periodisku izmaksu aprēķināšanas modeli, piemēram, FIFO, LIFO vai svērto vidējo. Termins "peldošais vidējais" netiek lietots Piegādes ķēžu pārvaldībā, un tam var būt atšķirīgas konnotācijas citās sistēmās.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Kā var pielāgot starpību starp produktu ieejas plūsmas cenu un rēķina cenu, kad izmantoju pārvietojamu vidējo?

Kad izmantojat pārvietojamu vidējo, fiziskās izmaksas (saņemšanas cena) tiek izmantotas, lai aprēķinātu pārvietojamo vidējo vērtību visām izdošanas darbībām. Ja pastāv starpība starp fiziskajām izmaksām (saņemšanas cenu) un finanšu izmaksām (rēķina cenu), **·** **·** **sistēma** automātiski iegrāmatos starpību galvenajā kontā, kas ir norādīts Cenas starpībai par vidējās vērtības grāmatošanas tipu lapas Krājumu grāmatošanas metode cilnē Krājumi.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Kur cenu starpība vidējās vērtības pārvietošanai ir norādītas Virsgrāmatā?

Ja pastāv cenas atšķirība starp fizisko atjauninājumu grāmatošanu un ieejas plūsmas finanšu atjauninājumu, **·** **·** **starpība** tiek grāmatota galvenajā kontā, kas ir norādīts Cenas starpībai par vidējās vērtības grāmatošanas tipu lapas Krājumu grāmatošanas metode cilnē Krājumi. Papildinformāciju skatiet sadaļā Vidējā [pārvietošana](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Kad es izmantoju pārvieto vidējo, kas notiek, ja pirms saņemšanas ir izejas plūsma?

Parasti pirms ieejas plūsmas var būt izdošana, jo ļaujat krājumu modeļu grupai fiziski negatīvus krājumus vai arī tā ir ar atpakaļejošo datumu. Plašāku informāciju skatiet šīs tēmas [sadaļā Negatīvi](#negative-inventory) krājumi.

Ja esat vieno savas darbības, ieteicams rūpīgi apsvērt biznesa procesu un operācijas, lai noteiktu, vai ir veids, kā izvairīties no šī scenārija. Ja tiek dublēta krājuma darbība, kas izmanto pārvietojamu vidējo, sistēma darbībai piešķirs pašreizējo pārvietojamo vidējo rādītāju. Vēlākās problēmas nav pielāgotas. Papildinformāciju par vidējās vērtības pārvietošanu ar atpakaļeīgām darbībām skatiet sadaļā [Vidējā pārvietošana](moving-average.md).

### <a name="standard-costing"></a>Standarta izmaksu aprēķināšana

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Kāda ir atšķirība starp standarta izmaksu ing un fiksēto saņemtā krājuma cenu?

Standarta izmaksu aprēķināšanai ir nepieciešams definēt krājuma cenu un aktivizēt izmaksas izmaksu versijā. Šīs izmaksas tiek izmantotas visām ieejas un izejas plūsmām. Novirzes no saņemšanām uz krājumiem tiek ierakstītas Virsgrāmatā, izmantojot standarta izmaksu novirzes kontus, ko norādāt lapas Krājumu **grāmatošanas** **profils cilnē Standarta** izmaksas.

Tomēr, ja izmantojat fiksēto saņemšanas cenu, tikai ieejas plūsmu izmaksas ir fiksētas, un sistēma izmanto izmaksas, **·** **ko norādāt izpildei nodotās preces lapas kopsavilkuma cilnē Pārvaldīt** izmaksas. Starpība starp noklusētajām izmaksām un pirkšanas pasūtījuma cenu izraisīs pirkšanas cenas novirzes iegrāmatošanu fiksētās saņemšanas cenas peļņas un zaudējumu kontos. Izejas plūsmas neizmanto fiksēto ieejas plūsmas cenu. Tā vietā izejas plūsmas tiks novērtētas ar esošo vidējo grāmatošanas laikā (ja vien netiek lietota atzīmēšana), un tās tiks pārvērtētas uz heiristisko modeli, ko atlasāt, kad palaižat krājumu slēgšanu.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Vai es variet izmantot FEFO rezervācijas ar standarta izmaksu aprēķināšanas metodi?

Jā, jūs varat izmantot FEFO rezervācijas krājumu modeļu grupā, kad atlasāt standarta izmaksu. FEFO rezervācijas kontrolē rezervēšanas loģiku, kas tiek izmantota krājumu fiziskai apstrādei, bet standarta izmaksu aprēķināšana kontrolē krājuma fiziskās un finanšu izmaksas.

### <a name="can-i-upload-pending-prices"></a>Vai es variet augšupielādēt gaidošas cenas?

Jā, varat izmantot Excel pievienojumprogrammu vai datu pārvaldības struktūru, lai augšupielādētu gaidošu cenu. Ieteicams izmantot šādus elementus:

- Nenokārtotās krājumu cenas (V2)
- Gaidoša maršruta izmaksu kategorijas vienības izmaksas
- Izmaksu aprēķina lapas zara aprēķina koeficienti (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Cik bieži var atjaunināt krājuma standarta izmaksas?

Biežumam nav limita, pie kura var aktivizēt jaunas standarta izmaksas. Aktivizējot jaunu izmaksu krājumam tajā pašā dienā, kad tika aktivizētas pēdējās izmaksas, sistēma izmantos jaunākās aktivizētās izmaksas jaunām darbībām vai atjauninājumiem (piemēram, esošo darbību atjauninājumi).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Vai deaktivizēt vai dzēst aktivizētās izmaksas?

Nē, jūs nevarat deaktivizēt vai dzēst aktivizētās izmaksas. Ja izmaksas ir nepareizi aktivizētas, var aktivizēt jaunu izmaksu, kam ir pareizās izmaksas.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Vai aprēķinu grupas tiek izmantotas ar standarta izmaksu aprēķināšanu?

Aprēķinu grupas var izmantot ar jebkuru krājumu neatkarīgi no jūsu izvēles krājumu modeļu grupas. Aprēķinu grupas tiek izmantotas izmaksu apkopojuma vai izmaksu aprēķina procesa laikā, lai noteiktu iestatījumus, kas jālieto krājumiem, kuriem palaižat aprēķinu. Plašāku informāciju par aprēķina grupām skatiet [MK aprēķinu grupās](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Kad jāizmanto plānotā izmaksu versija?

Izmaksu versijām var būt standarta izmaksu *vai plānoto* *izmaksu tips*. Standarta *izmaksu* tips tiek izmantots izmaksām, kas ir aktīvas sistēmā un tiks grāmatotas darbībās. Plānotais *izmaksu* tips tiek izmantots izmaksu simulāciju veikšanai un neietekmē darbību izmaksas.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Vai viena elementa kopējās izmaksas var pārsūtīt uz citu entītiju kā pārdošanas izmaksas?

Nav automatizēts veids, kā kopēt izmaksas no viena uzņēmuma citā. Turklāt nav automatizēts veids, kā kopēt izmaksas no pirkšanas cenas uz pārdošanas cenu. Ja jūsu organizācijai ir jāveic viens no šiem uzdevumiem, apsveriet, vai jūs variet izmantot Datu pārvaldības struktūru, lai eksportētu datus no jūsu izmaksu aprēķināšanas versijas un augšupielādētu citā uzņēmumā, vai nu kā pārdošanas cenu aprēķina versijā, vai kā tirdzniecības līgumu. Iespējams, būs nepieciešama manuāla manipulācija ar failiem.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Kāds ir labākais veids, kā kopēt plānotās izmaksas uz standarta izmaksu versiju?

Var izmantot pogu Kopēt **cenu** versiju **lapā**, lai kopētu krājumu cenas, izmaksu kategoriju cenas vai netiešās izmaksas no vienas izmaksu versijas uz citu.
